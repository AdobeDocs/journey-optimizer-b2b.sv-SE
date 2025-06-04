---
title: Redigering av e-postmeddelanden
description: Lär dig skapa e-postinnehåll i Adobe Journey Optimizer B2B. Använd mallar, HTML-import och AI-baserade verktyg för att personalisera och optimera e-postkommunikationen.
feature: Email Authoring, Content Design Tools
role: User
exl-id: 0f4ae644-ade7-49a0-935c-7f4779c25ffb
source-git-commit: 8793e92054f57f64f311b039cc8161281b6269a8
workflow-type: tm+mt
source-wordcount: '892'
ht-degree: 0%

---

# Redigering av e-postmeddelanden

När du har [lagt till en ny<!-- or duplicated -->-e-postresurs till en åtgärdsnod för resan](./add-email.md) kan du definiera innehållet för e-postmeddelandet.

Klicka på **[!UICONTROL Edit email content]** på fliken _[!UICONTROL Details]_på den högra panelen.

![Klicka på Redigera e-postinnehåll ](./assets/add-email-content.png){width="700" zoomable="yes"}

Den här åtgärden startar e-postdesignverktygen, där du kan välja hur du vill utforma e-postmeddelandet bland följande alternativ:

* [Designa din e-post från grunden](#design-your-email-from-scratch) med e-post-Designer-gränssnittet.

* [Importera befintligt HTML-innehåll](#import-existing-html-content) från en fil eller en ZIP-mapp.

* [Välj en befintlig mall](#select-a-template) i en lista med inbyggda eller anpassade e-postmallar.

När du har skapat och anpassat e-postinnehållet kan du exportera innehållet för validering eller för senare bruk. Klicka på **[!UICONTROL Export HTML]** om du vill spara innehållet som en ZIP-fil som innehåller ditt HTML och dina resurser.

>[!TIP]
>
>Använd AI Assistant i Adobe Journey Optimizer B2B edition med generativ AI som lyfter materialet till nästa nivå. AI Assistant kan hjälpa er att optimera effekten av era leveranser genom att generera hela e-postmeddelanden, riktat textinnehåll och få AI Assistant-rekommendationer för bilder som får genklang hos er målgrupp. [Läs mer](./ai-assistant-emails.md)

## Designa din e-post från grunden {#design-from-scratch}

>[!CONTEXTUALHELP]
>id="ajo-b2b_structure_components_landing_page"
>title="Lägg till strukturkomponenter"
>abstract="Strukturkomponenter definierar landningssidans layout. Dra och släpp en **Structure**-komponent på arbetsytan för att börja designa innehållet på landningssidan."

>[!CONTEXTUALHELP]
>id="ajo-b2b_content_components_landing_page"
>title="Om Innehållskomponenter"
>abstract="Innehållskomponenterna är tomma platshållare för innehåll som du kan använda för att skapa layouten för en landningssida."

Använd det visuella designområdet för att definiera strukturen och innehållet i e-postmeddelandet. Genom att lägga till och flytta strukturella komponenter med enkla dra och släpp-åtgärder kan du designa formen på det återanvändbara e-postinnehållet på några sekunder.

1. Välj alternativet **[!UICONTROL Design from scratch]** på startsidan för _[!UICONTROL Design your template]_.
1. [Lägg till struktur och innehåll](#add-structure-and-content) i e-postmeddelandet.
1. [Lägg till bildresurser](#add-assets) i e-postmeddelandet.
1. [Anpassa e-postinnehållet](#personalize-content).
1. [Granska och uppdatera länkar](#preview-and-edit-linked-urls).

<!-- If needed, you can further personalize your email by clicking **[!UICONTROL Switch to code editor]** from the advanced menu. The code editor allows you to edit the email source code, such as adding tracking or custom HTML tags.

>[!CAUTION]
>
>You cannot revert back to the visual designer for this email after switching to the code editor. -->

När innehållet är klart klickar du **[!UICONTROL Simulate content]** längst upp för att kontrollera återgivningen. Du kan välja skrivbordsvy eller mobilvy.

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
> Sparade mallar kan ha styrningsinställningar (innehållslås) för en eller flera komponenter. Den visuella designern ger riktlinjer om låsta komponenter när du [redigerar ett e-postmeddelande från en styrd mall](./email-authoring-governance.md).

## Lägga till struktur och innehåll {#structure-content}

>[!CONTEXTUALHELP]
>id="ajo-b2b_structure_components_email"
>title="Lägg till strukturkomponenter"
>abstract="Strukturkomponenter definierar layouten för e-postmeddelandet. Dra och släpp en **Structure**-komponent på arbetsytan för att börja designa ditt e-postinnehåll."

>[!CONTEXTUALHELP]
>id="ajo-b2b_content_components_email"
>title="Om Innehållskomponenter"
>abstract="Innehållskomponenterna är tomma platshållare för innehåll som du kan använda för att skapa layouten för ett e-postmeddelande."

{{$include /help/_includes/content-design-components.md}}

### Lägg till fragment

{{$include /help/_includes/content-design-use-fragments.md}}

När e-postmeddelandet har sparats visas det på fragmentinformationssidan när du väljer fliken _[!UICONTROL Used By]_i sammanfattningen.

### Lägga till resurser

{{$include /help/_includes/content-design-assets.md}}

### Navigera mellan lager, inställningar och format

{{$include /help/_includes/content-design-navigation.md}}

### Anpassa innehåll

{{$include /help/_includes/content-design-personalization-email.md}}

>[!NOTE]
>
>Om _[!UICONTROL My Tokens]_har definierats för kontoresan kan du även använda dessa kundspecifika tokens för ditt e-postinnehåll. Mer information finns i [Anpassade token för e-postanpassning](./personalization-my-tokens.md).

### Redigera länkad URL-spårning

{{$include /help/_includes/content-design-links.md}}

### Visningsalternativ

Utnyttja de alternativ för visning och innehållsvalidering som finns i den visuella e-postredigeraren.

* Zooma in/ut i innehållet genom förinställda zoomalternativ.

* Växla mellan att visa innehållet på datorer, mobiler eller endast text/normal text.
   * Klicka på ikonen _Visa_ om du vill förhandsgranska innehåll på olika enheter.
   * Välj en av de färdiga enheterna eller ange anpassade dimensioner för att förhandsgranska innehållet.

### Fler alternativ

På menyn _[!UICONTROL More ...]_högst upp i e-postdesignområdet kan du utföra följande åtgärder:

![Klicka på Mer för att komma åt mallåtgärder](./assets/email-designer-more-menu.png){width="500"}

* **[!UICONTROL Reset email]** - Klicka på det här alternativet om du vill rensa arbetsytan för den visuella e-postdesignern till ett tomt läge och börja bygga om innehållet.
* **[!UICONTROL Save as fragment]** - Spara hela eller delar av e-postmeddelandet som ett fragment som kan återanvändas i flera e-postmallar eller e-postmallar. Du anger ett namn och en beskrivning för fragmentet och sparar det i listan över tillgängliga fragment.
* **[!UICONTROL Change your design]** - Återgå till sidan _Designa din e-post_. Därifrån kan du välja en annan mall för att starta om designprocessen eller välja att designa innehållet från början på en svart arbetsyta.\
* **[!UICONTROL Save as content template]** - Spara e-postbrödtexten som en e-postmall som kan återanvändas i flera e-postmallar eller e-postmallar. Du anger ett namn och en beskrivning för mallen och sparar den i listan över sparade e-postmallar.
* **[!UICONTROL Export HTML]** - Hämta innehållet på den visuella arbetsytan till ditt lokala system i HTML-format som paketerats som en zip-fil.

## Kontrollera och testa e-postmeddelandet {#preview-test}

>[!CONTEXTUALHELP]
>id="ajo-b2b_email_preview_simulate"
>title="Kontrollera hur innehållet renderar"
>abstract="När innehållet är definierat kan du förhandsgranska det och kontrollera om återgivningen är korrekt för den kanal som du använder."

När meddelandeinnehållet är definierat kan du använda testprofiler för att förhandsgranska det, skicka korrektur och styra återgivningen i populära dator-, mobil- och webbaserade klienter. Om du infogade anpassat innehåll kan du förhandsgranska hur innehållet visas i meddelandet med hjälp av testprofilsdata.

Om du vill förhandsgranska e-postinnehållet klickar du på **[!UICONTROL Simulate content]** och lägger sedan till en testprofil för att kontrollera meddelandet med testprofildata.

![Simulera e-postinnehållet för att kontrollera din design](./assets/email-designer-simulate-content.png){width="700" zoomable="yes"}
