---
title: Web Experience Design
description: Designa webbupplevelser med visuella och icke-visuella redigeringsprogram - lägg till ändringar, hantera innehållsuppdateringar, aktivera klickspårning och anpassa innehåll i Journey Optimizer B2B edition.
feature: Content Design Tools, Channels
role: User
badgeBeta: label="Beta" type="informative" tooltip="Den här funktionen är för närvarande i en begränsad betaversion"
source-git-commit: d01f4c14f72ebf78b10e4fc6691df42707bedb47
workflow-type: tm+mt
source-wordcount: '2234'
ht-degree: 0%

---

# Design av webbupplevelser

När du har [skapat en webbupplevelse](./web-experiences.md#create-a-web-experience) använder du designområdet för innehåll för att definiera de ändringar som du vill tillämpa på dina webbsidor.

>[!BEGINSHADEBOX]

**Förutsättningar**

Innan du kan utforma webbupplevelser måste du kontrollera att följande krav uppfylls:

* En produktadministratör har konfigurerat en eller flera webbkanaler för att definiera de URL:er (sidor) som ska inkluderas för en webbupplevelse. Mer information finns i [Konfigurationer för webbkanaler](../admin/configure-channels-web.md).

* På webbplatsen har [Adobe Experience Platform Web SDK](https://experienceleague.adobe.com/sv/docs/experience-platform/collection/js/js-overview) (`alloy.js`) implementerats för besöksidentifiering och innehållsleverans. Adobe Experience Platform Web SDK version 2.16 eller senare krävs.

* Du har de [behörigheter](../admin/user-management.md#b2b-product-permissions) som krävs för att skapa och hantera webbupplevelser under en resa:
   * _[!UICONTROL Campaigns]_>_[!UICONTROL Manage Campaigns]_ - Krävs för att lägga till eller uppdatera en åtgärdsnod för webbanpassning.
   * _[!UICONTROL Campaigns]_>_[!UICONTROL View Campaigns]_ - Krävs för att visa information för en åtgärdsnod för webbanpassning.

>[!ENDSHADEBOX]

>[!IMPORTANT]
>
>Innan du utformar en webbupplevelse bör du kontrollera att webbläsartillägget Adobe Experience Cloud Visual Editing Helper är installerat för webbläsaren. Det här tillägget krävs för att du ska kunna öppna, redigera och förhandsgranska dina webbsidor på ett tillförlitligt sätt i designområdet för webbupplevelsen i Journey Optimizer B2B edition.<br/>
>
>Google Chrome och Microsoft Edge är för närvarande de enda webbläsare som stöder tillägg och redigering av webbupplevelser i Journey Optimizer B2B edition. Mer information finns i [Installera tillägget Hjälp för visuell redigering](./web-experiences.md#install-the-visual-editing-helper-extension).

## Redigerare för webbupplevelser

Journey Optimizer B2B edition har två typer av redigerare för att utforma webbändringar:

| Redigerare | Beskrivning | Bäst för |
| ------ | ----------- | -------- |
| [Visuell redigerare](#visual-editor) | En WYSIWYG-redigerare (_What You See Is What You Get_) som visar webbplatsen och gör att du kan markera och ändra element direkt. Det kräver [hjälptillägget &#x200B;](./web-experiences.md#install-the-visual-editing-helper-extension) för visuell redigering i Google Chrome eller Microsoft Edge webbläsare. | Göra visuella ändringar i synliga sidelement, t.ex. text, bilder, knappar och banners. |
| [Icke-visuell redigerare](#non-visual-editor) | En kodbaserad redigerare för att tillämpa ändringar som inte går att göra med den visuella redigeraren. | Ange målelement som är svåra att markera visuellt, använda avancerade CSS-ändringar eller göra ändringar i dolda element. |

Använd alternativet **[!UICONTROL Visual editor]** i egenskaperna för webbupplevelsen för att fastställa typen av redigerare. Aktivera alternativet att använda den visuella redigeraren eller inaktivera det för att använda den icke-visuella redigeraren.

![Alternativet Visuell redigerare är aktiverat](./assets/web-experience-design-visual-editor-option.png){width="400"}

## Visual editor {#visual-editor}

>[!CONTEXTUALHELP]
>id="ajo-b2b_web_experience_browse"
>title="Använda bläddringsläget"
>abstract="I det här läget kan du navigera till exakt den sida som du vill anpassa för den valda webbkanalskonfigurationen."

Den visuella redigeraren läser in webbsidorna i en iframe, där du kan markera element och använda ändringar direkt i förhandsgranskningen av sidan. Följ de här stegen för att använda den visuella redigeraren för att designa din webbupplevelse:

1. Klicka på _[!UICONTROL Content]_&#x200B;i den högra panelen när fliken **[!UICONTROL Edit web experience]**&#x200B;visas på sidan med information om webbupplevelser.

   Den visuella redigeraren läser in webbplatsen baserat på webbkanalskonfigurationen.

   ![Visuell redigerare för webbupplevelse](./assets/web-experience-design-visual-editor.png){width="800" zoomable="yes"}

1. Om det behövs klickar du på **[!UICONTROL Browse]** längst upp till höger och använder navigeringsfältet för webbplatsen för att läsa in den specifika sida som du vill ändra.

   Du kan också ange sidans URL i fältet längst upp.

   >[!NOTE]
   >
   >Kontrollera att den inlästa sidan matchar de URL-mönster som har definierats i webbkanalskonfigurationen. Klicka på **[!UICONTROL View configuration details]** överst till höger för att visa URL- eller sidmatchningsreglerna för den valda webbkanalskonfigurationen.

   ![Bläddringsläge i den visuella redigeraren](./assets/web-experience-design-visual-editor-browse.png){width="700" zoomable="yes"}

   <!-- If the web channel configuration is defined using page matching rules, use the left and right arrows to sequence through the matched pages -- right now these buttons don't do anything -->

   Klicka på **[!UICONTROL Design]** överst till höger för att läsa in sidan i designområdet.

1. Du kan definiera hur du vill att den visade sidan ska ändras för webbupplevelsen genom att:

   * [Infoga nya komponenter](#insert-new-components) (avdelare, HTML, bild, rubrik, stycke eller länk) på sidan för webbupplevelsen.

   * Markera ett befintligt element på sidan, till exempel en bild, knapp, ett stycke, text, behållare, rubrik eller länk, och [ändra det för webben](#modify-elements).

   * [Lägg till klickspårning](#click-tracking-for-web-experiences) för element som mäter engagemang och samlar in insikter.

1. Upprepa steg 2 för att läsa in andra sidor som du vill inkludera i webbupplevelsen och upprepa steg 3 för att definiera sidändringarna.

1. [Granska dina ändringar](#manage-modifications) och gör nödvändiga justeringar.

1. När ändringarna är klara klickar du på vänsterpilen ovanför redigeraren för att gå tillbaka till webbupplevelseegenskaperna.

### Ändra element

Klicka på ett element på den visade sidan för att markera det. En blå kant anger det markerade elementet och ett kontextverktygsfält visas med ändringsalternativ.

![Markera ett element som du vill ändra](./assets/web-experience-design-select-element.png){width="700" zoomable="yes"}

Vilka alternativ som visas i verktygsfältet beror på den valda komponenttypen:

| Åtgärd | Beskrivning |
| ------ | ----------- |
| **[!UICONTROL Text options]** | Ändra det markerade elementets textelementklass eller textformat. |
| **[!UICONTROL Choose image]** | Ersätt bildkällan eller lägg till en bild i elementet. |
| **[!UICONTROL Edit link / Add link]** | Ändra eller lägg till en länk-URL. |
| **[!UICONTROL Arrange]** | Flytta det markerade elementet bakåt eller framåt i visningen. |
| **[!UICONTROL Add personalization]** | Infoga personalisering. |
| **[!UICONTROL Click track element]** | Lägg till klickspårning för elementet. |
| **[!UICONTROL Delete]** | Ta bort det markerade elementet från sidan. |

För ett markerat element ändras egenskaperna på den högra panelen så att de återspeglar tillgängliga format och åtgärder. Klicka på en åtgärdsikon högst upp på panelen för att duplicera, klicka på-spåra, ta bort eller dölja det markerade elementet.

![klicka på en åtgärdsikon för det markerade elementet](./assets/web-experience-design-visual-editor-element-properties-icons.png){width="300"}

+++Textelement

1. Markera ett textelement på sidan.

1. Ange nytt textinnehåll eller markera en textsträng och ange din ersättningstext.

1. (Valfritt) Använd [textformateringsalternativen](./content-components.md#text), till exempel fet, kursiv och justering.

1. Klicka utanför textelementet för att tillämpa ändringen.

Mer information om alternativ för textformat för textkomponenter finns i [Innehållskomponenter](./content-components.md#text).

+++

+++Bildelement

1. Markera ett bildelement på sidan.

1. Klicka på ikonen _[!UICONTROL Choose image]_&#x200B;i det sammanhangsberoende verktygsfältet eller den högra panelen.

1. Bläddra och välj en bild från ditt resursbibliotek.

1. Använd alternativen för [bildformat](./content-components.md#image) på den högra panelen efter behov.

+++

+++Knappelement

1. Markera ett knappelement på sidan.

1. (Valfritt) Ange ny text för knappen eller markera textsträngen och ange din ersättningstext.

   Du kan använda personalisering för att ändra knapptexten med data från konto- eller personprofiler.

1. Använd [knappformateringsalternativen](./content-components.md#button) på den högra panelen efter behov.

+++

+++ Behållarelement

1. Markera ett behållarelement på sidan.

1. Använd [alternativen för behållarformat](./content-components.md#container) på den högra panelen efter behov.

+++

### Infoga nya komponenter

När du väljer ikonen **+** i den vänstra designnavigeringen för den visuella redigeraren kan du lägga till följande komponenttyper på sidan som en webbredigeringsändring:

* **[!UICONTROL Divider]** - Använd den här komponenten för att infoga en delningslinje för att ordna layouten och innehållet i ditt e-postmeddelande. Du kan justera formatattribut som linjefärg, format och höjd i egenskaperna på den högra panelen. Mer information finns i [Delare](./content-components.md#divider) i _Innehållskomponenter_.
* **[!UICONTROL HTML]** - Använd den här komponenten för att kopiera och klistra in HTML-kod i den befintliga strukturen. Med den kan du skapa kostnadsfria modulära HTML-komponenter för återanvändning av externt innehåll. Mer information finns i [HTML](./content-components.md#html) i _Innehållskomponenter_.
* **[!UICONTROL Image]** - Använd den här komponenten för att infoga en bildfil på sidan. Du kan justera formatattribut som bredd och höjd i egenskaperna på den högra panelen. Mer information finns i [Bild](./content-components.md#image) i _Innehållskomponenter_.
* **[!UICONTROL Heading]** - Använd den här komponenten för att infoga rubriktext. Du kan justera formatattribut som textfärg, stil, teckensnitt och storlek från egenskaperna på den högra panelen. Mer information finns i [Text](./content-components.md#text) i _Innehållskomponenter_.
* **[!UICONTROL Paragraph]** - Använd den här komponenten för att infoga ett standardelement med text. Du kan justera formatattribut som textfärg, stil, teckensnitt och storlek från egenskaperna på den högra panelen. Mer information finns i [Text](./content-components.md#text) i _Innehållskomponenter_.
* **[!UICONTROL Link]** - Använd den här komponenten för att infoga en fristående textlänk till en angiven URL. Du kan justera formatattribut som textfärg, format, justering och storlek från egenskaperna på den högra panelen.

Markera en komponenttyp till vänster och hovra sedan över ett element som ligger intill den plats där du vill lägga till det.

![Gränssnitt för visuell redigerare - ny komponent](./assets/web-experience-design-visual-editor-insert-component.png){width="800" zoomable="yes"}

Placera komponenten genom att klicka på någon av knapparna som visas:

* ***[!UICONTROL Insert before]** - Infoga komponenten före det markerade elementet.
* ***[!UICONTROL Insert after]** - Infoga komponenten efter det markerade elementet.

Om du vill avmarkera en komponenttyp som ska infogas klickar du på **[!UICONTROL ESC]** i den kontextbaserade blå banderollen som visas högst upp på sidan.

## Icke-visuell redigerare {#non-visual-editor}

Använd den icke-visuella redigeraren när du behöver göra ändringar som inte är enkla att göra i den visuella redigeraren. Med den här kodbaserade metoden får ni exakt kontroll över målanpassning och ändring av element. Följ de här stegen för att använda den icke-visuella redigeraren för att designa din webbupplevelse:

1. Klicka på _[!UICONTROL Content]_&#x200B;i den högra panelen när fliken **[!UICONTROL Add modification]**&#x200B;visas på sidan med information om webbupplevelser.

   Den icke-visuella redigeraren läser in en sida baserat på webbkanalskonfigurationen.

   ![Gränssnitt för icke-visuell redigerare](./assets/web-experience-design-non-visual-editor.png){width="800" zoomable="yes"}

1. Definiera den första ändringen som du vill göra.

   På den vänstra panelen visas en lista med befintliga ändringar (om sådana finns). Klicka på **[!UICONTROL Add]** för att definiera en ny ändring. Om inga ändringar har definierats används _[!UICONTROL Add Modification]_-alternativen som standard.

   * Välj **[!UICONTROL Modification type]**:

     | Typ | Beskrivning |
     | ---- | ----------- |
     | [**[!UICONTROL CSS Selector]**](#css-selector-modifications) | Använd en CSS-väljarsträng som målelement. |
     | [**[!UICONTROL Page]**](#page-modifications) | Infoga anpassad HTML, CSS eller JavaScript i sidelement som `<head>` eller `<body>`. |

   * Konfigurera ändringsparametrarna efter typ:

      * **[!UICONTROL CSS Selector]** - Ange en giltig CSS-väljare för specifika målelement.
      * **[!UICONTROL Action type]** - Välj vilken åtgärd som ska utföras (redigera, dölja, ta bort, infoga, ersätta).
      * **[!UICONTROL Content]** - Ange innehållet eller formatet som ska användas.

1. Klicka på **[!UICONTROL Save]** för att tillämpa ändringen.

### Ändringar av CSS-väljare

Med CSS-väljarändringar kan du ange exakta målelement med hjälp av standardsyntaxen för CSS-väljare.

1. Välj **[!UICONTROL CSS Selector]** som ändringstyp.

1. Ange väljaren i fältet **[!UICONTROL CSS Element Selector]**.

<!-- This field helps you find and select the HTML elements (or nodes in the DOM tree). -->

    **Exempelväljare:**
    
    | Väljare | Målgrupper |
    | — | — |
    | `#hero-banner` | Element med ID &quot;hero-banner&quot; |
    | `.cta-button` | Alla element med klassen &quot;cta-button&quot; |
    | &grave;1 | Länkar i navigeringen, inuti rubriken |
    | `[data-offer=&quot;premium&quot;]` | Element med ett specifikt dataattribut |

1. Välj en **[!UICONTROL Action Type]** och ange nödvändig information/nödvändigt innehåll.

   * **[!UICONTROL Set Content]** - Ange texten i fältet **[!UICONTROL Content]** för elementet som identifieras av värdet _[!UICONTROL CSS Element Selector]_.

   * **[!UICONTROL Set Attribute]** - Ange ett attribut som ska associeras med den aktuella CSS-väljaren så att elementet kan identifieras med det här attributet. Ange ett namn i fältet **[!UICONTROL Attribute name]** och ett värde i fältet **[!UICONTROL Content]**. Om attributet redan finns uppdateras värdet. I annat fall läggs ett nytt attribut till med det angivna namnet och värdet.

   ![Ändring av CSS-väljare som inte är visuell redigerare](./assets/web-experience-design-non-visual-editor-modification-css-selector.png){width="800" zoomable="yes"}

1. (Valfritt) Klicka på **[!UICONTROL Add personalization]** och använd [anpassningsredigeraren](./personalization.md#personalization-editor) för att skapa en anpassad anpassning för innehållet.

### Sidändringar

Du kan lägga till anpassad kod med ändringstypen Sida `<head>`. Elementet `<head>` är en behållare för metadata (data om data) och placeras mellan taggen `<html>` och taggen `<body>`. I det här fallet väntar koden inte på body- eller page-load-händelser - den körs i början av sidinläsningen.

Elementet `<head>` används ofta för att lägga till JavaScript- eller CSS-kod högst upp på sidan. Väljare för efterföljande visuella åtgärder beror på vilka HTML-element som har lagts till på den här fliken.

>[!NOTE]
>
>Anpassad kod körs i besökarens webbläsare. Kontrollera att koden är säker, testad och inte påverkar sidprestanda negativt eller användarupplevelsen negativt.

1. Välj **[!UICONTROL Page `<head>`]** som ändringstyp.

1. Lägg till din egen kod i rutan **[!UICONTROL Content]**.

   >[!CAUTION]
   >
   >Du kan bara lägga till elementen `<script>` och `<style>` i avsnittet `<head>`. Om du lägger till `<div>`-taggar och andra element kan det leda till att återstående `<head>`-element fylls i i `<body>`.

   ![Icke-visuell redigering, sidhuvudsändring](./assets/web-experience-design-non-visual-editor-modification-page-head.png){width="800" zoomable="yes"}

1. (Valfritt) Klicka på **[!UICONTROL Add personalization]** och använd [anpassningsredigeraren](./personalization.md#personalization-editor) för att skapa en anpassad anpassning för innehållet.

## Hantera ändringar {#manage-modifications}

>[!CONTEXTUALHELP]
>id="ajo-b2b_web_experience_modifications"
>title="Hantera enkelt alla ändringar"
>abstract="I den här rutan kan du navigera och hantera alla justeringar och tillägg som har definierats för webbsidan."

Alla ändringar som du skapar spåras och kan hanteras från panelen **[!UICONTROL Modifications]** i både den visuella redigeraren och den icke-visuella redigeraren. Klicka på ikonen _[!UICONTROL Modifications]_<!-- ( ![Modifications icon](../assets/do-not-localize/icon-web-exp-modifications.svg) ) --> i det vänstra verktygsfältet om du vill visa alla ändringar.

Varje ändringspost innehåller:

* Målelementet eller väljaren
* Ändringstypen (till exempel redigera, dölja eller infoga)
* En förhandsgranskning av ändringen

![Panelen Ändringar](./assets/web-experience-design-modifications-list.png){width="500" zoomable="yes"}

### Redigera en ändring

1. I listan _[!UICONTROL Modifications]_&#x200B;söker du efter den ändring du vill redigera.

1. Klicka på ikonen _Mer meny_ ( **..** ) och välj **[!UICONTROL Edit]**.

1. Uppdatera ändringsegenskaperna efter behov.

1. Klicka på **[!UICONTROL Save]** om du vill spara ändringarna.

### Ta bort en ändring

1. I listan _[!UICONTROL Modifications]_&#x200B;söker du efter den ändring du vill ta bort.

1. Klicka på ikonen _Mer meny_ ( **..** ) och välj **[!UICONTROL Delete modification]**.

1. Bekräfta borttagningen när du uppmanas till det.

<!-- ### Reorder modifications

Modifications are applied in the order that they appear in the list. If you have multiple modifications that affect the same element, the order may impact the final result.

Drag and drop modifications in the list to change the order. The preview updates to reflect the new modification order. -->

## Förhandsgranska ändringarna

Förhandsgranska hur ändringarna ser ut för besökarna före publiceringen.

Använd alternativen för förhandsvisning av enheter längst upp i den visuella redigeraren för att visa dina ändringar i:

* Skrivbord
* Tablet
* Mobil

![Ändra enhetens storlek för förhandsgranskningen](./assets/web-experience-design-device-view.png){width="550" zoomable="yes"}

Förhandsgranskningen uppdateras för att visa hur ändringarna återges för varje enhetsstorlek.

Använd URL-fältet för att navigera till olika sidor i webbkanalkonfigurationen. Verifiera sedan att ändringarna gäller för målsidorna korrekt baserat på dina URL-matchningsregler.

## Klickspårning för webbupplevelser {#web-click-tracking}

Spåra användarinteraktioner med element för att mäta engagemang och samla insikter. Data för klickspårning finns tillgängliga i era engagemangsrapporter och kan användas för att mäta effekten av dina webbupplevelseändringar.

När webbupplevelsen aktiveras (live) kan du även skapa rapporter med Adobe Customer Journey Analytics (som kräver en produktprenumeration). Om du vill förbättra övervakningen av webbupplevelsen kan du även spåra klick på ett visst element på webbplatsen. Med Spärra/knip kan du visa antalet klick för det elementet i webbrapporterna.

Mer information om Customer Journey Analytics och hur du skapar webbrapporter finns i [Customer Journey Analytics-dokumentationen](https://experienceleague.adobe.com/sv/docs/analytics-platform/using/cja-landing).

1. Välj ett element i webbredigeraren, till exempel en bild eller länk.

1. Klicka på ikonen _[!UICONTROL Click track element]_&#x200B;i elementegenskaperna eller det sammanhangsberoende verktygsfältet.

   ![Aktivera klickspårning för webbupplevelselement](./assets/web-experience-design-visual-editor-click-tracking-icons.png){width="600" zoomable="yes"}

1. Öppna listan Klicka på spår i den vänstra panelen och ändra värdet **[!UICONTROL Tracked actions]** för att identifiera interaktionen i dina rapporter.

   ![Ange klickspårningsidentifiering för webbupplevelse](./assets/web-experience-design-visual-editor-click-tracking-identifier.png){width="600" zoomable="yes"}
