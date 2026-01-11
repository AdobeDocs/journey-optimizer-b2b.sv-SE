---
title: Single-page Applications
description: Skapa webbupplevelser för single-page-applikationer (SPA) - konfigurera vyspårning, hantera dynamiskt innehåll och hantera klientnavigering i Journey Optimizer B2B edition.
feature: Channels, Personalization
role: User
badgeBeta: label="Beta" type="informative" tooltip="Den här funktionen är för närvarande i en begränsad betaversion"
source-git-commit: e50b6830736bf763d3aae6a58595e868bbac36e0
workflow-type: tm+mt
source-wordcount: '832'
ht-degree: 0%

---

# Single-page applications

Single-page-applikationer (SPA) utgör unika utmaningar för webbpersonalisering eftersom de dynamiskt uppdaterar sidinnehåll utan att behöva ladda om hela sidor. Journey Optimizer B2B edition har specialverktyg för effektiv hantering av SPA-personalisering.

## Om SPA

Till skillnad från traditionella flersidiga webbplatser, där varje navigering aktiverar en helsidesinläsning, använder SPA-program JavaScript för att uppdatera innehåll dynamiskt samtidigt som man underhåller en enda HTML-sida. Den här metoden skapar flera överväganden för webbupplevelser:

* **Ingen sidomladdning** - Innehållsändringar inträffar utan att traditionella sidinläsningshändelser aktiveras.
* **Virtuella vyer** - Olika _vyer_ eller _skärmar_ i SPA som måste spåras som separata sidor.
* **routning på klientsidan** - JavaScript-routrar (som React Router, Vue Router och Angular Router) hanterar navigering i stället för serverförfrågningar.
* **Dynamisk DOM** - Sidelement kan skapas, ändras eller tas bort efter den första sidinläsningen.

## Konfigurera SPA-stöd

Om du vill anpassa SPA-program effektivt måste du konfigurera vyspårning så att Journey Optimizer B2B edition kan identifiera när användare navigerar mellan virtuella vyer.

### Ställ in vydeklarationer

Samarbeta med utvecklingsteamet för att implementera vydeklarationer med Adobe Web SDK. När du använder dessa vydeklarationer måste du anropa kommandot `sendEvent` med visningsinformation när SPA navigerar till en ny vy.

**Exempel på implementering:**

```javascript
// When a new view is rendered in your SPA
alloy("sendEvent", {
  "xdm": {
    "web": {
      "webPageDetails": {
        "viewName": "product-detail",
        "URL": window.location.href
      }
    }
  },
  "data": {
    "__adobe": {
      "target": {
        "viewName": "product-detail"
      }
    }
  }
});
```

### Visa namnkonventioner

Använd konsekventa beskrivande vynamn som matchar programmets logiska struktur:

| Visa | Exempelnamn |
| ---- | ------------ |
| Startsida | `home` |
| Produktlista | `product-list` |
| Produktinformation | `product-detail` |
| Kundvagn | `cart` |
| Utcheckning | `checkout` |
| Kontrollpanel för konto | `account-dashboard` |

>[!NOTE]
>
>Vynamn är skiftlägeskänsliga. Använd en konsekvent namngivningskonvention (små bokstäver med bindestreck rekommenderas) i implementeringen.

## Skapa webbupplevelser för SPA

När du skapar webbupplevelser för SPA-program bör du tänka på följande bästa tillvägagångssätt:

### Målspecifika vyer

* I [webbkanalskonfigurationen](../admin/configure-channels-web.md) ställer du in URL-matchningsregler som är anpassade till din SPA-routningsstruktur.

* När du skapar ändringar anger du vyn där ändringen ska gälla.

* Använd CSS-väljare som anger specifika element för varje vy som mål.

### Hantera dynamiskt innehåll

SPA-filer läser ofta in innehåll dynamiskt efter den inledande sidåtergivningen. Använd dessa tekniker för att säkerställa att ändringarna tillämpas korrekt:

#### Vänta på element

Konfigurera ändringar som väntar på att målelementen ska finnas innan du använder:

1. I den icke-visuella redigeraren lägger du till en ändring med en CSS-väljare.

1. Aktivera **[!UICONTROL Wait for element]** och ange maximal väntetid.

1. Ändringen tillämpas när målelementet visas i DOM.

#### Använd mutationsobjekt

För mycket dynamiskt innehåll innehåller Web SDK inbyggda mutationsobjekt som identifierar när nya element läggs till på sidan. Dessa observatörer ser till att ändringarna tillämpas även när elementen läses in asynkront.

### SPA-ramverk

Journey Optimizer B2B edition webbupplevelser fungerar med populära SPA-ramverk:

| Ramverk | Överväganden |
| --------- | -------------- |
| **Reagera** | Ändringarna tillämpas när React återger komponenter i DOM. Använd klassnamn eller dataattribut för mål. |
| **Angular** | Målelement när Angular ändringsspårning körs. Undvik målelement med `*ngIf` innan de återges. |
| **Vue.js** | Vänta på att Vue:s `nextTick` kontrollerar att elementen finns i DOM. Använd referenser eller anpassade attribut för stabil målinriktning. |
| **Next.js / Nuxt.js** | För SSR-/SSG-sidor kontrollerar du att Web SDK-hydrering är slutförd innan ändringar förväntas. |

## Bästa tillvägagångssätt för SPA-personalisering

### Använd stabila väljare

SPA genererar ofta dynamiska klassnamn eller ID (särskilt med CSS-in-JS-lösningar). Du kan också använda:

* **Dataattribut** - Lägg till anpassade dataattribut (`data-testid`, `data-section` osv.) till de element som du vill ha som mål.
* **Semantisk HTML** - Mål baserat på HTML struktur och semantiska element.
* **ID-attribut** - Använd stabila ID-attribut där det är möjligt.

**Exempel:**

```html
<!-- Instead of targeting dynamic class names -->
<button class="css-1a2b3c4d">Sign Up</button>

<!-- Add a stable data attribute -->
<button class="css-1a2b3c4d" data-action="signup">Sign Up</button>
```

**CSS-väljare:** `[data-action="signup"]`

### Testvyer

När SPA-webbupplevelser testas:

1. Navigera genom alla vyer där ändringarna tillämpas.

1. Testa hela användarflödet, inklusive:
   * Direktnavigering till en vy (djuplänkning)
   * Navigering från andra vyer i SPA
   * Navigering bakåt och framåt

1. Kontrollera att ändringarna tillämpas igen när du återgår till en tidigare besökt vy.

### Hantera vyövergångar

Vissa SPA-program använder animeringar eller övergångar mellan vyer. Fundera:

* **Timing** - Kontrollera att ändringarna tillämpas när övergångsanimeringarna är klara.
* **Elementsynlighet** - Element kan finnas men vara dolda under övergångar.
* **Flickering** - Använd ändringarna tillräckligt tidigt för att undvika synliga innehållsändringar.

## Felsökning

När du granskar ändringarna i SPA-designen bör du använda följande rekommendationer för att lösa några vanliga problem:

* **Ändringarna visas inte** - Om ändringarna inte visas i SPA:

   1. **Kontrollera vyspårning** - Kontrollera att `sendEvent` anrop innehåller rätt vynamn.

   1. **Verifiera elementförekomst** - Kontrollera att målelementen finns i DOM när ändringarna tillämpas.

   1. **Granska väljare** - Bekräfta att CSS-väljarna matchar den faktiska DOM-strukturen.

   1. **Kontrollera konsolen** - Sök efter JavaScript-fel som kan förhindra ändringar.

* **Ändringar som visas en kort stund och sedan försvinner** - Det här problemet inträffar vanligtvis när SPA återger och ersätter ändrade element:

   1. Använd mer specifika CSS-väljare som är stabila över alla renderingar.

   1. Gör det möjligt för mutationsobjekt att återanvända ändringar när elementen återskapas.

   1. Samarbeta med utvecklingsteamet för att lägga till stabila attribut till målelementen.

* **Duplicera ändringar** - Om ändringarna förekommer flera gånger:

   1. Kontrollera att vyspårningshändelser endast utlöses en gång per vyövergång.

   1. Kontrollera att ändringarna omfattar specifika vyer i stället för att tillämpas globalt.

## Relaterade ämnen

* [Översikt över webbupplevelser](./web-experiences.md)
* [Design av webbupplevelser](./web-experience-design.md)
* [Konfigurationer av webbkanaler](../admin/configure-channels-web.md)