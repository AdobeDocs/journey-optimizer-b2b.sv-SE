---
title: Redigering av e-postmallar
description: Lär dig hur du skapar e-postmallar för innehåll som kan användas för e-postmeddelanden om kontoresa för att återanvända dina designer enkelt och effektivt.
feature: Email Authoring, Content
source-git-commit: 8315c760e573aa36819652798a400206e6268ccc
workflow-type: tm+mt
source-wordcount: '483'
ht-degree: 0%

---

# Framtagning av e-postmallar

När du har [skapat en e-postmall](./email-templates.md#create-an-email-template) använder du den visuella designern för att skapa struktur- och innehållskomponenterna i din e-postmall.

## Lägga till struktur och innehåll {#structure-content}

>[!CONTEXTUALHELP]
>id="ajo-b2b_structure_components_template"
>title="Lägg till strukturkomponenter"
>abstract="Strukturkomponenter definierar mallens layout. Dra och släpp en **Struktur**-komponent på arbetsytan för att börja designa innehållet för mallen."

>[!CONTEXTUALHELP]
>id="ajo-b2b_content_components_template"
>title="Om innehållskomponenter"
>abstract="Innehållskomponenter är tomma platshållare för innehåll som du kan använda för att skapa layouten för en mall."

{{$include /help/_includes/content-design-components.md}}

### Lägg till fragment

Ikonen _Fragments_ visas till vänster i den visuella innehållsredigeraren. I följande exempel beskrivs stegen för att lägga till fragment i mallinnehållet.

1. Om du vill öppna fragmentlistan väljer du ikonen _Fragment_ ( ![Fragment-ikon](../assets/do-not-localize/icon-fragments.svg) ).

   Du kan:

   * Sortera listan.
   * Bläddra, sök eller filtrera listan.
   * Växla mellan miniatyr- och listvy.
   * Uppdatera listan så att den återspeglar något av de nyligen skapade fragmenten.

   ![Välj ett fragment i listan](./assets/visual-designer-fragments.png){width="700" zoomable="yes"}

1. Dra och släpp något av fragmenten i platshållaren för strukturelement.

   Redigeraren återger fragmentet i avsnittet/elementet i e-poststrukturen.

Fragmentets innehåll uppdateras dynamiskt i strukturen för att visa hur innehållet visas i e-postmeddelandet.

>[!TIP]
>
>Om du vill att fragmentet ska uppta hela den vågräta layouten i e-postmeddelandet lägger du till en 1:1-kolumnstruktur och drar och släpper fragmentet i den.

När e-postmeddelandet har sparats visas det på fragmentinformationssidan när du väljer fliken _[!UICONTROL Used By]_i sammanfattningen. Fragment som läggs till i en e-postmall kan inte redigeras i mallen - källfragmentet definierar innehållet.

### Lägga till resurser

{{$include /help/_includes/content-design-assets.md}}

### Navigera mellan lager, inställningar och format

{{$include /help/_includes/content-design-navigation.md}}

### Anpassa innehåll

{{$include /help/_includes/content-design-personalization.md}}

### Redigera länkad URL-spårning

{{$include /help/_includes/content-design-links.md}}

## Visningsalternativ

Utnyttja de alternativ för visning och innehållsvalidering som är tillgängliga i den visuella designern.

* Zooma in/ut i innehållet genom förinställda zoomalternativ.

* Växla mellan att visa innehållet på datorer, mobiler eller endast text/normal text.
   * Klicka på ikonen _Ögon_ om du vill förhandsgranska innehåll på olika enheter.
   * Välj en av de färdiga enheterna eller ange anpassade dimensioner för att förhandsgranska innehållet.

### Fler alternativ

På menyn _[!UICONTROL More ...]_högst upp i e-postdesignern kan du utföra följande åtgärder:

![Klicka på Mer för att komma åt mallåtgärder](./assets/visual-designer-more-menu.png){width="500"}

* **[!UICONTROL Reset template]** - Klicka på det här alternativet om du vill rensa arbetsytan för den visuella designern till ett tomt läge och starta om skapandet av innehåll.
* **[!UICONTROL Save as fragment]** - Spara alla eller delar av mallen som ett fragment som kan återanvändas i flera e-postmallar eller e-postmallar. Du anger ett namn och en beskrivning för fragmentet och sparar det i listan över tillgängliga fragment.
* **[!UICONTROL Change your design]** - Återgå till sidan _Designa mallen_. Därifrån kan du välja att designa mallen från grunden eller använda en befintlig mall för att starta om designprocessen.
* **[!UICONTROL Export HTML]** - Hämta innehåll på den visuella arbetsytan till ditt lokala system i HTML-format som paketerats som en zip-fil.
