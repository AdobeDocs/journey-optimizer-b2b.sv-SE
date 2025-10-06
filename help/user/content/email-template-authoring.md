---
title: Redigering av e-postmallar
description: Skapa återanvändbara e-postmallar med visuella designverktyg, anpassad CSS, fragment och personalisering för kontoresor i Journey Optimizer B2B edition.
feature: Templates, Email Authoring, Content
role: User
exl-id: 2d532f93-c452-400a-8a82-e1f0eb89b199
source-git-commit: 9f8953423e3b6d578155431c7638e4fec9abf86a
workflow-type: tm+mt
source-wordcount: '526'
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

### Lägga till bildresurser

{{$include /help/_includes/content-design-assets.md}}

### Navigera mellan lager, inställningar och format

{{$include /help/_includes/content-design-navigation.md}}

### Anpassa innehåll

{{$include /help/_includes/content-design-personalization-email.md}}

### Redigera länkad URL-spårning

{{$include /help/_includes/content-design-links.md}}

### Använda format i mörkt läge

Använd _mörkt läge_ för att granska din e-postvisning för ett mörkt tema i en e-postklient. I ett mörkt läge eller tema kan en e-postklient eller app som stöder det visa e-postmeddelanden med mörkare bakgrund och ljusare färger för text, knappar och andra visuella element. Överst till höger på arbetsytan ändrar du väljaren till _Mörkt läge_ ( ![Mörkt läge-ikon](../assets/do-not-localize/icon-content-dark-mode.svg) ). Förhandsgranska och definiera sedan specifika anpassade inställningar som ska användas för visning av e-postklienter när deras mörka tema är aktiverat.

![Designarbetsyta för e-post visar väljaren för mörkt läge och e-postinnehåll som visas i mörkt läge](./assets/email-color-mode-dark-selector.png){width="700" zoomable="yes"}

Mer information om formatet för mörkt läge och de effektivaste strategierna finns i [Mörkt läge för e-postinnehåll](./email-dark-mode.md).

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
