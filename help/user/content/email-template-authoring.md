---
title: Redigering av e-postmallar
description: Lär dig hur du skapar e-postmallar för innehåll som kan användas för e-postmeddelanden om kontoresa för att återanvända dina designer enkelt och effektivt.
feature: Templates, Email Authoring, Content
role: User
exl-id: 2d532f93-c452-400a-8a82-e1f0eb89b199
source-git-commit: f8d70f2e1cff6055ff353bad0c5a0f625d426db8
workflow-type: tm+mt
source-wordcount: '409'
ht-degree: 0%

---

# Framtagning av e-postmallar

När du har [skapat en e-postmall](./email-templates.md#create-an-email-template) använder du den visuella designrymden för att skapa struktur- och innehållskomponenterna i din e-postmall.

## Lägga till struktur och innehåll {#structure-content}

{{$include /help/_includes/content-design-components.md}}

### Lägg till anpassad CSS

Du kan lägga till egen anpassad CSS direkt i e-postmallens designutrymme. Använd anpassad CSS för att använda avancerad och specifik formatering, vilket ger större flexibilitet och kontroll över utseendet på innehållet. Det är en god vana att lägga till den här formateringen på den högsta nivån innan du inkluderar komponenter som bilder, knappar och text.

Med minst en innehållskomponent på arbetsytan väljer du komponenten **[!UICONTROL Body]** i det vänstra navigeringsträdet för att komma åt den anpassade CSS-redigeraren.

![Få åtkomst till brödtextformaten](./assets/email-template-body-styles.png){width="800" zoomable="yes"}

{{$include /help/_includes/content-design-custom-css.md}}

### Lägg till fragment

>[!NOTE]
>
>Fragment är inte korskompatibla mellan _temaläge_ och _manuellt läge_ i e-postinnehållet. Om du vill använda ett fragment i e-postinnehåll där ett tema används måste fragmentet också skapas i _temaläge_.

{{$include /help/_includes/content-design-use-fragments.md}}

När mallen har sparats visas den på fragmentinformationssidan när du väljer fliken _[!UICONTROL Used By]_i sammanfattningen.

### Lägga till resurser

{{$include /help/_includes/content-design-assets.md}}

### Navigera mellan lager, inställningar och format

{{$include /help/_includes/content-design-navigation.md}}

### Anpassa innehåll

{{$include /help/_includes/content-design-personalization-email.md}}

### Redigera länkad URL-spårning

{{$include /help/_includes/content-design-links.md}}

## Visningsalternativ

Utnyttja de alternativ för visning och innehållsvalidering som finns i det visuella designutrymmet.

* Zooma in/ut i innehållet genom förinställda zoomalternativ.

* Växla mellan att visa innehållet på datorer, mobiler eller endast text/normal text.
   * Klicka på ikonen _Ögon_ om du vill förhandsgranska innehåll på olika enheter.
   * Välj en av de färdiga enheterna eller ange anpassade dimensioner för att förhandsgranska innehållet.

### Fler alternativ

På menyn _[!UICONTROL More ...]_högst upp i e-postdesignområdet kan du utföra följande åtgärder:

![Klicka på Mer för att komma åt mallåtgärder](./assets/visual-designer-more-menu.png){width="500"}

* **[!UICONTROL Reset template]** - Klicka på det här alternativet om du vill rensa arbetsytan till en tom platta och starta om skapandet av innehåll.
* **[!UICONTROL Save as fragment]** - Spara alla eller delar av mallen som ett fragment som kan återanvändas i flera e-postmallar eller e-postmallar. Du anger ett namn och en beskrivning för fragmentet och sparar det i listan över tillgängliga fragment.
* **[!UICONTROL Change your design]** - Återgå till sidan _Designa din e-post_. Därifrån kan du välja en annan mall för att starta om designprocessen. Du kan också välja att designa innehållet från grunden med en tom arbetsyta (_Klassiskt läge_) eller med ett [varumärkestema](./brand-themes.md) (_Temalläge_).
* **[!UICONTROL Export HTML]** - Hämta innehållet på den visuella arbetsytan till ditt lokala system i HTML-format som paketerats som en zip-fil.
