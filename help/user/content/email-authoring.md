---
title: E-postredigering
description: Lär dig hur du skapar anpassat e-postinnehåll som används i en kontoresa.
feature: Email Authoring, Content
exl-id: 0f4ae644-ade7-49a0-935c-7f4779c25ffb
source-git-commit: 5f53f4156c670d1c7b751844ab0bda0aef352973
workflow-type: tm+mt
source-wordcount: '1161'
ht-degree: 0%

---

# Framtagning av e-post

Använd Adobe Journey Optimizer B2B Edition för att skicka e-postmeddelanden till dina kunder. Du kan skapa, anpassa och förhandsgranska meddelanden i e-post-Designer.

## Lägg till en e-poståtgärd i en kontoresa

Du kan konfigurera e-postleveranser på en kontoresa när du lägger till en _[!UICONTROL Take an action]_-nod och gör följande:

1. Välj **[!UICONTROL People]** för målet _[!UICONTROL Action on]_.
1. Välj **[!UICONTROL Send email]** för _[!UICONTROL Action on people]_.
1. Välj **[!UICONTROL Create new email]** för _[!UICONTROL Email source]_.

   Du kan också välja alternativet _[!UICONTROL Select email from Adobe Marketo Engage]_om du vill använda ett av de redan skapade e-postmeddelandena i Marketo Engage och skicka det som en del av kontoresan.

   >[!NOTE]
   >
   >Om du skapar ett e-postmeddelande för första gången kontrollerar du att e-postkanalen har konfigurerats inifrån Adobe Marketo Engage. Mer information finns i [Säkerställ e-postleverans](https://experienceleague.adobe.com/en/docs/marketo/using/getting-started/initial-setup/setup-steps#ensure-email-deliverability) i Marketo Engage-dokumentationen.

   ![Vidta en åtgärd - skicka ett e-postmeddelande](assets/journey-node-send-email.png){width="700" zoomable="yes"}

1. Klicka på **[!UICONTROL Create email]** längst ned på panelen _[!UICONTROL Take an action]_.

1. Ange en unik **[!UICONTROL Name]** för e-postmeddelandet och en **[!UICONTROL Subject line]** i dialogrutan.

   ![Skapa ny e-postdialogruta](assets/create-new-email.png){width="400"}

1. Klicka på **[!UICONTROL Create]**.

   Fälten _[!UICONTROL From email]_och_[!UICONTROL Reply to address]_ är redan konfigurerade i avsnittet _[!UICONTROL Email properties]_på sidan för e-postinnehåll. Du kan ange värden för fälten_[!UICONTROL From name]_ och _[!UICONTROL Description]_(valfritt).

## Skapa e-postinnehåll

Klicka på **[!UICONTROL Add email content]** högst upp på förhandsvisningspanelen i _[!UICONTROL Email]_.

![Klicka på Lägg till e-postinnehåll ](./assets/add-email-content.png){width="700" zoomable="yes"}

Den här åtgärden startar e-post-Designer, där du kan välja hur du vill utforma e-postmeddelandet bland följande alternativ:

* [Designa din e-post från grunden](#design-your-email-from-scratch) med e-post-Designer-gränssnittet.

* [Importera befintligt HTML-innehåll](#import-existing-html-content) från en fil eller en ZIP-mapp.

* [Välj en befintlig mall](#select-a-template) i en lista med inbyggda eller anpassade e-postmallar.

Om du vill konfigurera och anpassa ämnesraden med uttrycksredigeraren klickar du på ikonen _Personalization_ och lägger till någon av Marketo Engage-tokenerna.

När du har skapat och anpassat e-postinnehållet kan du exportera innehållet för validering eller för senare bruk. Klicka på **[!UICONTROL Export HTML]** om du vill spara innehållet som en ZIP-fil som innehåller HTML och resurser.

>[!TIP]
>
>Använd AI Assistant i Adobe Journey Optimizer B2B Edition med generativ AI för att lyfta materialet till nästa nivå. AI Assistant kan hjälpa er att optimera effekten av era leveranser genom att generera hela e-postmeddelanden, riktat textinnehåll och få AI Assistant-rekommendationer för bilder som får genklang hos er målgrupp. [Läs mer](./ai-assistant-emails.md)

### Designa din e-post från grunden {#design-from-scratch}

>[!CONTEXTUALHELP]
>id="ajo-b2b_structure_components_landing_page"
>title="Lägg till strukturkomponenter"
>abstract="Strukturkomponenter definierar landningssidans layout. Dra och släpp en **Structure**-komponent på arbetsytan för att börja designa innehållet på landningssidan."

>[!CONTEXTUALHELP]
>id="ajo-b2b_content_components_landing_page"
>title="Om innehållskomponenter"
>abstract="Innehållskomponenterna är tomma platshållare för innehåll som du kan använda för att skapa layouten för en landningssida."

Använd den visuella innehållsredigeraren för att definiera strukturen för e-postinnehållet. Genom att lägga till och flytta strukturella komponenter med enkla dra och släpp-åtgärder kan du designa formen på det återanvändbara e-postinnehållet på några sekunder.

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

### Importera befintligt HTML-innehåll

{{$include /help/_includes/content-design-import.md}}

![importera html-innehåll i en ZIP-fil](./assets/email-import-zip-file.png){width="500"}

>[!NOTE]
>
>Om du använder en `<table>`-tagg som det första lagret i en HTML-fil kan du förlora stilar, inklusive inställningar för bakgrund och bredd i den översta lagertaggen.

Du kan anpassa det importerade innehållet efter behov med de visuella redigeringsverktygen för e-post.

### Välj en mall

{{$include /help/_includes/content-design-select-template.md}}

## Lägga till struktur och innehåll {#structure-content}

>[!CONTEXTUALHELP]
>id="ajo-b2b_structure_components_email"
>title="Lägg till strukturkomponenter"
>abstract="Strukturkomponenter definierar layouten för e-postmeddelandet. Dra och släpp en **Structure**-komponent på arbetsytan för att börja designa ditt e-postinnehåll."

>[!CONTEXTUALHELP]
>id="ajo-b2b_content_components_email"
>title="Om innehållskomponenter"
>abstract="Innehållskomponenterna är tomma platshållare för innehåll som du kan använda för att skapa layouten för ett e-postmeddelande."

{{$include /help/_includes/content-design-components.md}}

### Lägg till fragment

Ikonen _Fragments_ visas till vänster i den visuella innehållsredigeraren. I följande exempel beskrivs stegen för att lägga till fragment i mallinnehållet.

1. Om du vill öppna fragmentlistan klickar du på ikonen _Fragment_ .

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
>Om du vill lägga till fragmentet så att det upptar hela den vågräta layouten i e-postmeddelandet lägger du till en 1:1-kolumnstruktur och drar och släpper fragmentet i den.

När e-postmeddelandet har sparats visas det på fragmentinformationssidan när du väljer fliken _[!UICONTROL Used By]_i sammanfattningen. Fragment som läggs till i en e-postmall kan inte redigeras i mallen. Innehållet definieras av källfragmentet.

### Lägga till resurser

{{$include /help/_includes/content-design-assets.md}}

### Navigera mellan lager, inställningar och format

{{$include /help/_includes/content-design-navigation.md}}

### Anpassa innehåll

{{$include /help/_includes/content-design-personalization.md}}

### Redigera länkad URL-spårning

{{$include /help/_includes/content-design-links.md}}

### Visningsalternativ

Utnyttja de alternativ för visning och innehållsvalidering som finns i den visuella e-postredigeraren.

* Zooma in/ut i innehållet genom förinställda zoomalternativ.

* Växla mellan att visa innehållet på datorer, mobiler eller endast text/normal text.
   * Klicka på ikonen _Ögon_ om du vill förhandsgranska innehåll på olika enheter.
   * Välj en av de färdiga enheterna eller ange anpassade dimensioner för att förhandsgranska innehållet.

## Kontrollera aviseringar

När du utformar innehållet i e-postmeddelanden visas varningar i gränssnittet (längst upp till höger på sidan) när nyckelinställningarna saknas.

Om knappen inte visas finns det inga identifierade problem.

Det finns två typer av varningar:

* **_Varningar_** som hänvisar till rekommendationer och bästa praxis, som:

   * `The opt-out link is not present in the email body`: det är bäst att lägga till en länk för att avbryta prenumerationen i e-postmeddelandet.

     >[!NOTE]
     >
     >E-postmeddelanden i marknadsföringsstil måste innehålla en länk för avanmälan, vilket inte krävs för transaktionsmeddelanden.

   * `Text version of HTML is empty`: glöm inte att definiera en textversion av din e-postbrödtext, som används när HTML-innehåll inte kan visas.

   * `Empty link is present in email body`: Kontrollera att alla länkar i e-postmeddelandet är korrekta.

   * `Email size has exceeded the limit of 100KB`: Kontrollera att e-postmeddelandets storlek inte överstiger 100 kB för optimal leverans.

* **_Fel_** som hindrar dig från att testa eller aktivera resan/kampanjen så länge de inte är lösta, till exempel:

   * `The subject line is missing`: Ämnesraden för e-post är obligatorisk.

   * `The email version of the message is empty`: Det här felet visas när e-postinnehållet inte har konfigurerats.

## Kontrollera och testa e-postmeddelandet {#preview-test}

>[!CONTEXTUALHELP]
>id="ajo-b2b_email_preview_simulate"
>title="Kontrollera hur innehållet renderar"
>abstract="När innehållet är definierat kan du förhandsgranska det och kontrollera om återgivningen är korrekt för den kanal som du använder."

När meddelandeinnehållet är definierat kan du använda testprofiler för att förhandsgranska det, skicka korrektur och styra återgivningen i populära dator-, mobil- och webbaserade klienter. Om du infogade anpassat innehåll kan du förhandsgranska hur innehållet visas i meddelandet med hjälp av testprofilsdata.

Om du vill förhandsgranska e-postinnehållet klickar du på **[!UICONTROL Simulate content]** och lägger sedan till en testprofil för att kontrollera meddelandet med testprofildata.

![Simulera e-postinnehållet för att kontrollera din design](./assets/email-designer-simulate-content.png){width="700" zoomable="yes"}
