---
title: Redigering av e-postmeddelanden
description: Skapa e-postmeddelanden med visuella designverktyg, HTML-import eller mallar - använd innehållsgenerering i AI Assistant, anpassad CSS och personalisering i Journey Optimizer B2B edition.
feature: Email Authoring, Content Design Tools
role: User
exl-id: 0f4ae644-ade7-49a0-935c-7f4779c25ffb
source-git-commit: 9f8953423e3b6d578155431c7638e4fec9abf86a
workflow-type: tm+mt
source-wordcount: '1119'
ht-degree: 0%

---

# Redigering av e-postmeddelanden

När du har [lagt till en e-postresurs till en åtgärdsnod för resan](./add-email.md) kan du definiera innehållet för e-postmeddelandet.

Klicka på **[!UICONTROL Edit email content]** på fliken _[!UICONTROL Details]_&#x200B;på den högra panelen.

![Klicka på Redigera e-postinnehåll &#x200B;](./assets/add-email-content.png){width="700" zoomable="yes"}

Den här åtgärden startar e-postdesignverktygen, där du kan välja hur du vill utforma e-postmeddelandet bland följande alternativ:

* [Designa din e-post från grunden](#design-your-email-from-scratch) med e-post-Designer-gränssnittet.

* [Importera befintligt HTML-innehåll](#import-existing-html-content) från en fil eller en ZIP-mapp.

* [Välj en befintlig mall](#select-a-template) i en lista med inbyggda eller anpassade e-postmallar.

När du har skapat och anpassat e-postinnehållet kan du exportera innehållet för validering eller för senare bruk. Klicka på **[!UICONTROL Export HTML]** om du vill spara innehållet som en ZIP-fil som innehåller ditt HTML och dina resurser.

>[!TIP]
>
>Använd AI Assistant i Adobe Journey Optimizer B2B edition med generativ AI som lyfter materialet till nästa nivå. AI Assistant kan hjälpa er att optimera effekten av era leveranser genom att generera hela e-postmeddelanden, riktat textinnehåll och få AI Assistant-rekommendationer för bilder som får genklang hos er målgrupp. [Läs mer](./ai-assistant-emails.md)

## Designa din e-post från grunden {#design-from-scratch}

Använd det visuella designområdet för att definiera strukturen och innehållet i e-postmeddelandet. Genom att lägga till och flytta strukturella komponenter med enkla dra och släpp-åtgärder kan du designa formen på det återanvändbara e-postinnehållet på några sekunder.

1. Välj alternativet _[!UICONTROL Design your template]_&#x200B;på startsidan för **[!UICONTROL Design from scratch]**.

1. I dialogrutan _[!UICONTROL Create email]_&#x200B;väljer du vilken typ av e-postinnehåll du vill skapa.

   * **[!UICONTROL Use Themes]** - Välj det här alternativet om du vill skapa e-postmeddelandet i _temaläge_. I det här läget kan du använda ett definierat varumärkestema för att effektivisera innehållsredigeringsprocessen och se till att designen följer definierade standarder.

   * **[!UICONTROL Manual Styling]** - Välj det här alternativet om du vill skapa e-postmeddelandet i _Manuellt läge_. I det här läget anger du formateringen manuellt för alla struktur- och innehållskomponenter som du lägger till på den tomma arbetsytan.

1. [Lägg till struktur och innehåll](./email-authoring.md#add-structure-and-content) i mallen.

1. [Granska och uppdatera länkar](#preview-and-edit-linked-urls).

1. [Testa e-postmeddelandet](#check-and-test-the-email).

<!-- If needed, you can further personalize your email by clicking **[!UICONTROL Switch to code editor]** from the advanced menu. The code editor allows you to edit the email source code, such as adding tracking or custom HTML tags.

>[!CAUTION]
>
>You cannot revert back to the visual design space for this email after switching to the code editor. -->

När du är nöjd med innehållet klickar du på **[!UICONTROL Save]**.

## Importera befintligt HTML-innehåll

{{$include /help/_includes/content-design-import.md}}

![importera html-innehåll i en ZIP-fil](./assets/email-import-zip-file.png){width="500"}

>[!NOTE]
>
>Om du använder en `<table>`-tagg som det första lagret i en HTML-fil kan du förlora format, inklusive inställningar för bakgrund och bredd i den översta lagertaggen.

Du kan anpassa det importerade innehållet efter behov med de visuella redigeringsverktygen för e-post.

## Välj en mall

{{$include /help/_includes/content-design-select-template.md}}

>[!NOTE]
>
> Sparade mallar kan ha styrningsinställningar (innehållslås) för en eller flera komponenter. Det visuella designområdet innehåller riktlinjer om låsta komponenter när du [redigerar ett e-postmeddelande från en styrd mall](./email-authoring-governance.md).

## Lägga till struktur och innehåll {#structure-content}

{{$include /help/_includes/content-design-components.md}}

### Lägg till anpassad CSS

Du kan lägga till egen anpassad CSS direkt i e-postdesignområdet. Använd anpassad CSS för att använda avancerad och specifik formatering, vilket ger större flexibilitet och kontroll över utseendet på innehållet. Det är en god vana att lägga till den här formateringen på den högsta nivån innan du inkluderar innehållskomponenter som bilder, knappar och text.

Med minst en innehållskomponent på arbetsytan väljer du komponenten **[!UICONTROL Body]** i det vänstra navigeringsträdet för att komma åt den anpassade CSS-redigeraren.

>[!NOTE]
>
>Om ditt e-postmeddelande är utformat med en [mall med låst innehåll](./template-content-governance.md) kan du inte lägga till anpassad CSS i innehållet. Knappetiketten ändras till **[!UICONTROL View custom CSS]** och all anpassad CSS som redan finns i innehållet är skrivskyddad.

![Få åtkomst till brödtextformaten](./assets/email-body-styles.png){width="800" zoomable="yes"}

{{$include /help/_includes/content-design-custom-css.md}}

### Lägg till fragment

>[!NOTE]
>
>Fragment är inte korskompatibla mellan _temaläge_ och _manuellt läge_ i e-postinnehållet. Om du vill använda ett fragment i e-postinnehåll där ett tema används måste fragmentet också skapas i _temaläge_.

{{$include /help/_includes/content-design-use-fragments.md}}

När e-postmeddelandet har sparats visas det på fragmentinformationssidan när du väljer fliken _[!UICONTROL Used By]_&#x200B;i sammanfattningen.

### Lägga till bildresurser

{{$include /help/_includes/content-design-assets.md}}

### Navigera mellan lager, inställningar och format

{{$include /help/_includes/content-design-navigation.md}}

### Anpassa innehåll

{{$include /help/_includes/content-design-personalization-email.md}}

>[!NOTE]
>
>Om _[!UICONTROL My Tokens]_&#x200B;har definierats för kontoresan kan du även använda dessa kundspecifika tokens för ditt e-postinnehåll. Mer information finns i [Anpassade token för e-postanpassning](./personalization-my-tokens.md).

### Redigera länkad URL-spårning

{{$include /help/_includes/content-design-links.md}}

### Använda format i mörkt läge

Använd _mörkt läge_ för att granska din e-postvisning för ett mörkt tema i en e-postklient. I ett mörkt läge eller tema kan en e-postklient eller app som stöder det visa e-postmeddelanden med mörkare bakgrund och ljusare färger för text, knappar och andra visuella element. Överst till höger på arbetsytan ändrar du väljaren till _Mörkt läge_ ( ![Mörkt läge-ikon](../assets/do-not-localize/icon-content-dark-mode.svg) ). Förhandsgranska och definiera sedan specifika anpassade inställningar som ska användas för visning av e-postklienter när deras mörka tema är aktiverat.

![Designarbetsyta för e-post visar väljaren för mörkt läge och e-postinnehåll som visas i mörkt läge](./assets/email-color-mode-dark-selector.png){width="700" zoomable="yes"}

Mer information om formatet för mörkt läge och de effektivaste strategierna finns i [Mörkt läge för e-postinnehåll](./email-dark-mode.md).

### Visningsalternativ

Utnyttja de alternativ för visning och innehållsvalidering som finns i den visuella e-postredigeraren.

* Zooma in/ut i innehållet genom förinställda zoomalternativ.

* Växla mellan att visa innehållet på datorer, mobiler eller endast text/normal text.
   * Klicka på ikonen _Visa_ om du vill förhandsgranska innehåll på olika enheter.
   * Välj en av de färdiga enheterna eller ange anpassade dimensioner för att förhandsgranska innehållet.

## Fler alternativ

På menyn _[!UICONTROL More ...]_&#x200B;längst upp i den visuella designrymden kan du utföra följande åtgärder:

![Klicka på Mer för att komma åt mallåtgärder](./assets/email-designer-more-menu.png){width="500"}

* **[!UICONTROL Reset email]** - Klicka på det här alternativet om du vill rensa arbetsytan för e-postdesign till en tom plats och börja bygga om innehållet.
* **[!UICONTROL Save as fragment]** - Spara hela eller delar av e-postmeddelandet som ett fragment som kan återanvändas i flera e-postmallar eller e-postmallar. Du anger ett namn och en beskrivning för fragmentet och sparar det i listan över tillgängliga fragment.
* **[!UICONTROL Change your design]** - Återgå till sidan _Designa din e-post_. Därifrån kan du välja en annan mall för att starta om designprocessen. Du kan också välja att designa innehållet från grunden med en tom arbetsyta (_Klassiskt läge_) eller med ett [varumärkestema](./brand-themes.md) (_Temalläge_).
* **[!UICONTROL Save as content template]** - Spara e-postbrödtexten som en e-postmall som kan återanvändas i flera e-postmallar eller e-postmallar. Du anger ett namn och en beskrivning för mallen och sparar den i listan över sparade e-postmallar.
* **[!UICONTROL Export HTML]** - Hämta innehållet på den visuella arbetsytan till ditt lokala system i HTML-format som paketerats som en zip-fil.

## Kontrollera och testa e-postmeddelandet {#email-testing}

När meddelandeinnehållet har definierats kan du använda testprofiler för att förhandsgranska det, skicka korrektur och granska återgivningen i skrivbordsformat och mobilformat. Om du infogade anpassat innehåll kan du förhandsgranska hur innehållet visas i meddelandet med hjälp av testprofilsdata.

Om du vill [förhandsgranska e-postinnehållet](./email-simulate-content.md) klickar du på **[!UICONTROL Simulate content]** och väljer en testprofil för att kontrollera meddelandet med personprofilsdata.

![Simulera e-postinnehållet för att kontrollera din design](./assets/email-designer-simulate-content.png){width="700" zoomable="yes"}

Du kan använda ytterligare verktyg för att validera och granska e-postinnehållet:

* [Skicka ett bevis](./email-simulate-content.md#send-proofs)
* [Testa återgivning i e-postklienter](./email-test-rendering.md)
<!-- * Generate a spam report -->
