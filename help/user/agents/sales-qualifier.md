---
title: Försäljningskvalificerare
description: Automatisera kvalificering av B2B-potentiella kunder och utåtriktad verksamhet med säljkvalificerare. Det innehåller AI-driven forskning, e-postskisser, CRM-integrering och engagemangsplaner för BDR.
feature: AI Assistant, Sales Insights, Account Journeys
role: User
source-git-commit: 467a8d824b9a21ff7b80c3a170265c591fc94f9e
workflow-type: tm+mt
source-wordcount: '1320'
ht-degree: 0%

---


# Försäljningskvalificerare

>[!NOTE]
>
>Den här funktionen är för närvarande begränsad och inte tillgänglig för alla användare.

Sales Qualifier är ett AI-drivet tilläggsprogram till Adobe Journey Optimizer B2B edition som innehåller Account Qualification Agent och är utformat för att effektivisera arbetsflöden för BDR (Business Development Representants). Säljkvalificeraren automatiserar arbetsflödena för kvalificering av potentiella kunder, utåtriktad verksamhet och köpengagemang i alla kanaler. Det minskar den manuella belastningen på BDR och snabbar upp pipelinehastigheten för företag inom B2B.
Använd webbläsar- och e-postpluginerna för att få tillgång till affärsinformation direkt i CRM- eller Outlook.

## Demonstrationsvideo

I följande video visas en kort demonstration av Sales Qualifier och Account Qualification Agent.

>[!VIDEO](https://video.tv.adobe.com/v/3476565?captions=swe)

Säljkvalificerare ingår i [!UICONTROL Journey Optimizer B2B Edition], men det är en separat app i Experience Platform Experience Cloud.

![Kontrollpanel för säljkvalificerare som automatiserar BDR-kvalificering och utdataanslutning för företag B2B](assets/home-screen.png)

## Account Qualification Agent

Account Qualification Agent (AQA) är hjärtat i Sales Qualifier. AQA använder AI för att läsa dina konton och avgöra vilka som är klara för nästa steg. Det hjälper till med forskning, e-postframtagning och CRM-uppdateringar.

![AI-baserad Account Qualification Agent-instrumentpanel för potentiell kund inom försäljning och kontoanalys](assets/acc-qualification-agent.png)

* **Prospekterad forskning**

  Genomför undersökning av potentiella kunder med automatisk hämtning och visning av viktig information om potentiella kunder (t.ex. befattning, senaste engagemang, medlemskap för inköpsgrupper) för att få en komplett bild på några sekunder.

* **Kontoanalys**

  Genomför kontoundersökningar med automatisk hämtning och visning av detaljerad information om organisationen för en potentiell kund. Den här informationen innehåller viktiga företagsdokument, senaste nytt, strategiska prioriteringar och engagerade medlemmar.

* **Utkastmeddelanden**

  Generera e-postutkast genom att syntetisera forskning från presumtiva kunder och kontoinsikter för att skapa relevant, personaliserat e-postinnehåll baserat på BDR:s mål.

* **E-post om engagemangsplan**

  Skapa e-postutkast för engagemangsplanering som är personaliserade för varje steg i en BDR-definierad utdatacache, och se till att hela sekvensen är personaliserad.

### Grundläggande användning

Adobe AI-agenter använder _naturliga språkfrågor_, vilket innebär att de använder samma språk i textprompten som när du pratar med en person. Ju mer detaljerad du är, desto bättre resultat.

Med naturspråket kan du be agenten att:

* `Show me my assigned leads with no engagement yet`
* `Show me all my leads that are not part of any autonomous engagement`
* `Give me a detailed summary on Acme company, including their buying group, recent intent signals, and our past engagement.`

Ni kan omedelbart förstå vilka konton och leads som är de mest aktiva och visa det högsta avsikten, så att ni kan fokusera er energi där den har störst effekt.

Iterera längs hela kundresan genom att förfina era uppmaningar för att få de resultat ni behöver. Exempel:

* Utforma en uppföljning av e-postritning från ett sammanhang som inkomstsamtal eller rapporter. Upp till 120 ord. Ämnesrad: Engagerande, inbyggt nyckeltema. Intro: Ansluta med ett direkt citat från sammanhangskällor. Brödtext: Koppla samman med problempunkter och värdeförslag. CTA: föreslå ett kort samtal för att utforska vidare.

* Målet med det här e-postmeddelandet är att inleda ett samtal och bygga upp trovärdighet. Skriv ett e-postmeddelande med 120 ord som har en rådgivande och empatisk ton. Se till att du undviker en alltför välbekant metod eller försäljningsmetod och använd inte fraserna&quot;hoppas att du mår bra&quot;,&quot;bara checkar in&quot; eller&quot;snälla&quot;.

## Prospekt

I det här fönstret visas alla leads som du har tillgång till. Det är en snabb kontroll av saker som ledstatus och senaste aktivitet.

![Leadregister som visar lead-status och senaste aktivitet för hantering av potentiella kunder](assets/prospects.png)

Klicka på ikonen _Filter_ ![Filter &#x200B;](../../assets/do-not-localize/icon_filter-outline.svg) för att filtrera den visade listan efter lead-status.

## Förlovningsplaner

I det här fönstret finns information om definierade engagemangsplaner.

![Kontrollpanel för engagemangsplan med planinformation, valda leads och schemainställningar](assets/engagement-plans.png)

Klicka på **[!UICONTROL Create engagement plan]** om du vill skapa en ny engagemangsplan.

1. Ange ett namn och en valfri beskrivning i _Detaljer_ -scenen. Klicka på **[!UICONTROL Save and Continue]**.
1. I fasen _Välj potentiella kunder_ väljer du de leads som ska ingå i den här planen.
1. Ange parametrarna för planen i scenen _Definiera gräns_.
1. Kontrollera att allt fungerar som det ska i _förhandsgranskningsfasen_.

## E-postutkorg

I panelen E-postutkorgen visas alla automatiska e-postmeddelanden som du har skickat.

## Mötesbokningar

På den här panelen visas alla möten som ställts in via automatisering.

## Chattinkorg

På den här panelen visas alla dina chattrådar.

![Panel med chatttrådar med kontakt- och trådsammanfattningar för säljautomatisering](assets/chat-inbox.png)

Du kan interagera med kunder och se sammanfattningar för kontakten och tråden så att du snabbt kan se var du befinner dig i tråden.

## Integreringar

Med integreringar kan säljkvalificeraren utnyttja CRM och andra datakällor för att berika kundprofiler och utnyttja säljaktiviteter:

* Integrera med e-postinkorgen för att hålla reda på relevanta inkommande e-postmeddelanden och hjälpa till att generera svar.
* Läs och uppdatera CRM-data, som Salesforce eller Microsoft® Dynamics, ZoomInfo eller BuiltWith.

![Integrering av säljkvalificerare med Microsoft Outlook, med e-post- och kontaktsammanfattningar](assets/outlook.png)

### Konfigurera en ny integrering

Om du vill starta en ny integrering klickar du på **[!UICONTROL Create integration]** längst upp till höger.

![Formulär för integreringskonfiguration med URL, HTTP-metod, rubriker och autentiseringsalternativ](assets/integration-details.png)

Definiera URL:en för integreringen och upprätta nyttolasten som ska skickas:

1. Ange ett unikt namn och en beskrivning (valfritt) för integreringen.
1. Ange URL-fältet till integreringsautentiseringsslutpunkten för integreringswebbplatsen.
1. Ange HTTP-metoden i Sökvägsparametrar.
1. I Huvudparametrar anger du eventuella HTTP-huvuden som ska skickas. Vanligtvis är det ett JSON-objekt som skickas och som kräver en rubrik av innehållstyp.
1. Ange eventuella obligatoriska parametrar i Frågeparametrar.
1. Under Autentisering anger du inloggningsinformation för integrationsplatsen.

   * Ingen
   * OAuth 2.0
   * API-nyckel
   * Grundläggande autentisering

1. Ange begränsning och cachevärden i avsnittet **[!UICONTROL Payload configuration]**.
   * Klicka på pennikonen.
   * Klistra in eller ange JSON-nyttolastobjektet i dialogrutan _Klistra in nyttolast_ .

      * **[!UICONTROL Request payload]** - Ett JSON-objekt som innehåller data som ska skickas till integrationsplatsen.
      * **[!UICONTROL Response payload]** - Den datastruktur du förväntar dig ska returneras.

1. Klicka på **[!UICONTROL Test Connection]** för att kontrollera att inställningarna är korrekta.

När anslutningsinställningarna är giltiga klickar du på **[!UICONTROL Save as draft]**.

När du är tillbaka i huvudtabellen _[!UICONTROL Integrations]_&#x200B;markerar du integreringen och klickar på&#x200B;**[!UICONTROL Activate]**&#x200B;för att göra integreringen offentlig. Om du inte är redo att aktivera den klickar du på&#x200B;**[!UICONTROL Save as draft]**.

#### Hantera åtkomst

Du kan hantera åtkomst till användare och den typ av data som delas med olika användargrupper.

Klicka på **[!UICONTROL Manage access]** för att öppna dialogrutan _[!UICONTROL Manage Access]_.

I den här dialogrutan visas alla etiketter som har skapats för din organisation. Välj de etiketter som du vill använda för den här integreringen.

Om du behöver en ny etikett klickar du på **[!UICONTROL Create label]** och anger etikettinformationen:

* Namn
* Eget namn
* Beskrivning

## Representativa inställningar

Representantinställningarna anger information om dig själv, inklusive personliga detaljer, e-post- och kalenderinställningar samt chatttillgänglighet.

### Information

På fliken **[!UICONTROL Details]** anger du information om dig själv:

![Fliken Detaljer som visar personlig information, e-post och tillgänglighetsinställningar för chatt för representanter](assets/details.png)

### E-postinställningar

Konfigurera e-postanslutningarna på fliken **[!UICONTROL Email settings]**.

![Fliken E-postinställningar med alternativ för e-postanslutning och konfiguration för e-postsignatur](assets/email-settings.png)

* **[!UICONTROL Email connections]** - Klicka på **[!UICONTROL Connect]** och följ inloggningsproceduren för Microsoft.

* **[!UICONTROL Email signature]** - Konfigurera e-postsignaturen som används i automatiskt genererade e-postmeddelanden.

### Kalenderinställningar

Ange din tidszon och tillgänglighet på fliken **[!UICONTROL Calendar settings]**.

![Fliken Kalenderinställningar som visar tidszon och alternativ för tillgänglighet](assets/calendar-settings.png)

* **[!UICONTROL Calendar connection]** - Klicka på **[!UICONTROL Connect]** och följ inloggningsproceduren för Microsoft för att integrera din kalender.

* **[!UICONTROL Meeting confirmation email]** - När en klient bekräftar ett möte med dig får de bekräftelsemeddelandet via e-post som svar. Använd de här inställningarna för att definiera e-postmeddelandets ämne och innehåll.

* **[!UICONTROL Preferences]** - Ange din standardlängd för mötet och hur länge du vill växla mellan möten.

### Chattinställningar

På fliken **[!UICONTROL Chat settings]** anger du din tillgängliga tidszonslive-chatt.

![Fliken Chattinställningar för att konfigurera tidszon och live-chatttillgänglighet](assets/chat-settings.png)

## Representativ förvaltning

Panelen _[!UICONTROL Representative management]_&#x200B;visar de definierade representanterna och deras kalenderstatus.

## Mötesprestanda

Den här panelen ger analyser kring de slutförda mötena.

## Konfigurera plugin-programmet för Chrome

Chrome-plugin-programmet för AI Assistant finns på [Google Store](https://chromewebstore.google.com/detail/ai-assistant/hancbabllcmckehonngbdkhilocpdfji?authuser=0&hl=en).

När plugin-programmet är installerat i Chrome visas Adobe logotyp i mitten till höger när du är på en integrerad webbplats:

* Adobe webbprogram
* Salesforce
* Outlook
* Microsoft Dynamics och webbprogram
* Google-program

## Redigera det vänstra navigeringsfältet

Klicka på **[!UICONTROL Edit]** längst ned till vänster i programmet för att kontrollera vilka ikoner som visas i navigeringen. Du kan också dra och släppa dem för att ändra ordningen.
