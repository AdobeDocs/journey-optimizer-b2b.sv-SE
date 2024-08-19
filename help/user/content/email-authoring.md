---
title: E-postredigering
description: Lär dig hur du skapar anpassat e-postinnehåll som används i kontoresor.
feature: Email Authoring, Content
exl-id: 0f4ae644-ade7-49a0-935c-7f4779c25ffb
source-git-commit: 3bdfdd8484063400f385120be87e6c460ef46d02
workflow-type: tm+mt
source-wordcount: '1388'
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
>id="ajo-b2b_structure_components_email"
>title="Lägg till strukturkomponenter"
>abstract="Strukturkomponenter definierar layouten för e-postmeddelandet. Dra och släpp en **Structure**-komponent på arbetsytan för att börja designa ditt e-postinnehåll."

>[!CONTEXTUALHELP]
>id="ajo-b2b_structure_components_landing_page"
>title="Lägg till strukturkomponenter"
>abstract="Strukturkomponenter definierar landningssidans layout. Dra och släpp en **Structure**-komponent på arbetsytan för att börja designa innehållet på landningssidan."

>[!CONTEXTUALHELP]
>id="ajo-b2b_structure_components_fragment"
>title="Lägg till strukturkomponenter"
>abstract="Strukturkomponenter definierar fragmentets layout. Dra och släpp en **Structure**-komponent på arbetsytan för att börja designa innehållet i fragmentet."

>[!CONTEXTUALHELP]
>id="ajo-b2b_content_components_email"
>title="Om innehållskomponenter"
>abstract="Innehållskomponenterna är tomma platshållare för innehåll som du kan använda för att skapa layouten för ett e-postmeddelande."

>[!CONTEXTUALHELP]
>id="ajo-b2b_content_components_landing_page"
>title="Om innehållskomponenter"
>abstract="Innehållskomponenterna är tomma platshållare för innehåll som du kan använda för att skapa layouten för en landningssida."

>[!CONTEXTUALHELP]
>id="ajo-b2b_content_components_fragment"
>title="Om innehållskomponenter"
>abstract="Innehållskomponenter är tomma platshållare för innehåll som du kan använda för att skapa layouten för ett fragment."

1. På Designer hemsida väljer du alternativet **[!UICONTROL Design from scratch]**.

1. Om du vill starta innehållsdesignen drar du ett objekt från **[!UICONTROL Structures]** och släpper det på arbetsytan.

   Upprepa det här steget för varje strukturkomponent för att skapa layouten för ditt e-postmeddelande.

1. Lägg till så många objekt från _Strukturer_ som du behöver och redigera inställningarna för varje objekt i rutan till höger.

   Markera n:n-kolumnkomponenten för att definiera hur många kolumner du vill ha (mellan tre och 10). Du kan också definiera bredden på varje kolumn genom att flytta pilarna under kolumnen.

   Varje kolumnstorlek får inte vara mindre än 10 % av strukturkomponentens totala bredd. Endast tomma kolumner kan tas bort.

1. Expandera avsnittet **[!UICONTROL Contents]** och lägg till så många element du behöver i en eller flera strukturkomponenter.

1. Om det behövs kan du göra ytterligare anpassningar för varje komponent på flikarna _[!UICONTROL Settings]_eller_[!UICONTROL Style]_.

   Du kan till exempel ändra textstil, utfyllnad eller marginal för varje komponent.

1. I resursväljaren kan du välja resurser som lagras direkt i Assets-biblioteket.

   Dubbelklicka på mappen som innehåller dina resurser. Dra och släpp objekten i en strukturkomponent.

1. Infoga anpassningsfält för att anpassa innehållet utifrån profilattribut, målgruppsmedlemskap, sammanhangsbaserade attribut med mera.

<!-- 1. Click **[!UICONTROL Enable condition content]** to add dynamic content and adapt the content to the targeted profiles based on conditional rules.
-->
1. Välj fliken **[!UICONTROL Links]** i den vänstra rutan för att visa alla URL:er för ditt innehåll som spåras.

   Du kan ändra _spårningstypen_ eller _etiketten_ och lägga till taggar om det behövs.

Om det behövs kan du anpassa din e-post ytterligare genom att klicka på **[!UICONTROL Switch to code editor]** på den avancerade menyn. Med kodredigeraren kan du redigera e-postkällkoden, till exempel lägga till spårning eller egna HTML-taggar.

>[!CAUTION]
>
>Du kan inte återgå till den visuella designern för det här e-postmeddelandet efter att du har växlat till kodredigeraren.

När innehållet är klart klickar du **[!UICONTROL Simulate content]** längst upp för att kontrollera återgivningen. Du kan välja skrivbordsvy eller mobilvy.

När du är klar klickar du på Spara.

### Importera befintligt HTML-innehåll

Importerat innehåll kan vara:

* En HTML-fil med en infogad formatmall
* En ZIP-mapp som innehåller en HTML-fil, formatmallen (.css) och bildfiler

>[!NOTE]
>
>ZIP-filstrukturen har inga begränsningar. Referenserna måste dock vara relativa och passa in i trädstrukturen i ZIP-mappen.

_Så här importerar du en fil som innehåller HTML-innehåll:_

1. Välj **[!UICONTROL Import HTML]** på startsidan för e-post till Designer.

1. Dra och släpp HTML- eller ZIP-filen med ditt HTML-innehåll och klicka på [!UICONTROL Import].

   När innehållsöverföringen för HTML är klar är ditt innehåll i _kompatibilitetsläge_. I det här läget kan du bara anpassa texten, lägga till länkar eller inkludera resurser i innehållet.

### Välj en mall

Du kan välja mellan:

* Exempelmallar. Journey Optimizer-gränssnittet innehåller 20 färdiga e-postmallar som du kan välja bland.

* Sparade mallar.

* En anpassad mall som du antingen skapade från grunden med menyn _Mallar_ eller sparade från ett e-postmeddelande på en resa med alternativet _[!UICONTROL Save as content template]_.

_Så här börjar du skapa innehåll med någon av exempelmallarna eller sparade mallar:_

1. Få åtkomst till _e-post-Designer_ från arbetsytan för redigering av e-postinnehåll.

   Fliken **[!UICONTROL Sample templates]** är markerad som standard på sidan _[!UICONTROL Create your email]_.

1. Om du vill använda en anpassad mall väljer du fliken **[!UICONTROL Saved templates]**.

   Listan över alla innehållsmallar som skapats i den aktuella sandlådan visas. Du kan sortera dem efter namn, senast ändrade eller senast skapade.

1. Välj önskad mall i listan.

1. När du har valt en kategori kan du navigera mellan alla mallar i den kategorin (exempel eller spara beroende på vad du har valt) med höger- och vänsterpilarna.

1. Klicka på **[!UICONTROL Use this template]** överst till höger på sidan.

1. Redigera innehållet efter behov i _e-postmeddelandet för Designer_.

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
