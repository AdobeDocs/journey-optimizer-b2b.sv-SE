---
title: Avancerat HTML-läge för design av e-postmallar
description: Använd avancerat HTML-läge för att direkt visa och redigera HTML-råkällan för e-postmallsinnehållet i e-postdesignområdet i Journey Optimizer B2B edition.
feature: Email Authoring, Templates, Content Design Tools
level: Experienced
role: User
source-git-commit: 95dba963e08125370f998cf3960d51ede94c2fb9
workflow-type: tm+mt
source-wordcount: '577'
ht-degree: 0%

---

# Avancerat HTML-läge för design av e-postmallar

_Avancerat HTML-läge_ ger en vy där erfarna användare kan visa och redigera råkällkoden för e-postmallens innehåll direkt. Det här läget är idealiskt när du vill infoga avancerade uttryck, t.ex. villkorslogik, direkt i källan. Det är också användbart om du vill göra strukturjusteringar som går utöver vad de visuella designverktygen visar.

<!-- We don't have the code editor at this point 
>[!NOTE]
>
>_Advanced HTML mode_ is different from the code editor option that is available when you start a new design. The code editor does not allow you to change to the visual design space. With _advanced HTML mode_, you can toggle back and forth between the HTML source view and the visual design view at any time. -->

>[!AVAILABILITY]
>
>Den här funktionen är för närvarande i _Begränsad tillgänglighet_ och är inte tillgänglig för alla användare.

## Viktiga begränsningar

Innan du använder avancerat HTML-läge för att skapa [e-postmallar](./email-template-authoring.md) måste du känna till följande begränsningar:

* **Ingen validering** - HTML-redigeraren utför inte syntaxkontroll eller layoutverifiering. Granska koden noggrant innan du sparar.

* **Innehållsuppdateringar** - Framtida systemändringar kan påverka eller skriva över ändringar som gjorts i standardkoden i avancerat HTML-läge. Kontrollera innehållet efter produktuppdateringarna för att säkerställa att det återges som förväntat.

* **Begränsat stöd** - Adobe kan inte felsöka återgivningsproblem eller innehållsfel som beror på anpassade kodändringar som gjorts i avancerat HTML-läge.

* **Förhandsvisningsbegränsningar** - Innehållssimulering (förhandsvisning med profiler) är bara tillgängligt i skrivbordsvyn, inte direkt från HTML-källvyn.

### Använd avancerat HTML-läge

Det avancerade HTML-läget är tillgängligt från verktygsfältet längst upp i den visuella designrymden när du har en e-postmall inläst på arbetsytan.

1. Öppna eller [skapa en e-postmall](./email-templates.md#create-an-email-template) och öppna designområdet för att redigera innehållet.

1. Klicka på ikonen _[!UICONTROL HTML]_( ![HTML-ikon](../assets/do-not-localize/icon-code.svg) ) i designområdet.

   ![Klicka på HTML-ikonen i verktygsfältet för e-postmalldesign](./assets/email-template-advanced-html-mode-toolbar.png){width="750" zoomable="yes"}

   Om det här är första gången du öppnar avancerat HTML-läge (eller en månad eller mer har gått) visas ett varningsmeddelande. Granska informationen och klicka på **[!UICONTROL OK]** för att fortsätta.

   ![Granska varningen för avancerat HTML-läge och klicka på OK för att fortsätta](./assets/email-template-html-mode-warning.png){width="500"}

   Designarbetsytan växlar till källvyn i HTML.

1. Granska koden och lägg till önskade ändringar i e-postinnehållet.

   I _avancerat HTML-läge_ har du direktåtkomst till den fullständiga HTML-källan för ditt e-postmallinnehåll:

   * Visa och ändra valfri del av HTML-koden.
   * Infoga avancerade [personaliseringsuttryck](./personalization.md) direkt i källan.
   * Lägg till logik för [villkorligt innehåll](./conditional-content.md) med uttryckssyntax.
   * Lägg till anpassade HTML-attribut, spårningstaggar eller annan kod som inte är tillgänglig via de visuella redigeringskontrollerna.

   ![Avancerat HTML-läge med HTML råformat för e-postinnehållet](./assets/email-template-advanced-html-mode.png){width="800" zoomable="yes"}

   >[!IMPORTANT]
   >
   >Ange korrekt HTML- och CSS-kod. Adobe har ingen syntaxvalidering eller stöd för anpassad kod.

   Simulering och sparande av innehåll är inte tillgängligt i avancerat HTML-läge av kompatibilitetsskäl. Du kan växla tillbaka till skrivbordsvyn för att förhandsgranska innehållet och spara mallen. Alla redigeringar du gör bevaras när du växlar mellan HTML källvy och den visuella designvyn.

   Om du klickar på **[!UICONTROL Save]** eller **[!UICONTROL Save & close]** längst upp till höger när du är i avancerat HTML-läge visas en varningsdialogruta som informerar dig om att du måste växla från avancerat HTML-läge innan du sparar mallen och avslutar designområdet.

   ![Varningsdialogrutan som sparas är inaktiverad i avancerat HTML-läge](./assets/email-template-advanced-html-save-disabled-alert.png){width="500"}

1. Klicka på ikonen _[!UICONTROL Desktop]_( ![Skrivbord-ikon ](../assets/do-not-localize/icon-desktop-spectrum-1.svg) ) i verktygsfältet för att växla från avancerat HTML-läge (HTML källvy) till den visuella arbetsytan.

   Dina redigeringar bevaras när du byter vy.
