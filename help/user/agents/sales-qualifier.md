---
title: Försäljningskvalificerare
description: Lär dig hur du använder Sales Qualifier för att snabba upp och underhålla dina resor.
feature: Account Journeys, AI Assistant
role: User
source-git-commit: 8fb86fe3434a5acdec6fd638fad571a0bc901884
workflow-type: tm+mt
source-wordcount: '1292'
ht-degree: 0%

---


# Försäljningskvalificerare

>[!NOTE]
>Den här funktionen är för närvarande begränsad och inte tillgänglig för alla användare.
>

Försäljningskvalificeraren är ett AI-drivet tillägg till Adobe Journey Optimizer B2B edition som innehåller Account Qualification Agent och är utformat för att effektivisera arbetsflöden för BDR (Business Development Representants). Säljkvalificeraren automatiserar arbetsflödena för kvalificering av potentiella kunder, utåtriktad verksamhet och köpengagemang i alla kanaler, vilket minskar den manuella BDR-belastningen och snabbar upp pipeline-hastigheten för företag B2B-företag.
Använd webbläsar- och e-postpluginerna för att få tillgång till affärsinformation direkt i CRM- eller Outlook.

Försäljningskvalificeraren ingår i AJO B2B men är en separat app i AEP Experience Cloud.

![Startsida för försäljningskvalificerare](assets/home-screen.png)

## Account Qualification Agent

Account Qualification Agent (AQA) är hjärtat i Sales Qualifier. AQA använder AI för att läsa dina konton och avgöra vilka som är klara för nästa steg.  Det hjälper till med forskning, e-postframtagning och CRM-uppdateringar.

![Account Qualification Agent](assets/acc-qualification-agent.png)

* **Prospekterad forskning**

  Genomför undersökning av potentiella kunder med automatisk hämtning och visning av viktig information om potentiella kunder (t.ex. befattning, senaste engagemang, medlemskap för inköpsgrupper) för att få en komplett bild på några sekunder.

* **Kontoanalys**

  Genomför kontoundersökningar med automatisk hämtning och visning av detaljerad information om organisationen för en potentiell kund. Den här informationen innehåller viktiga företagsdokument, senaste nytt, strategiska prioriteringar och engagerade medlemmar.

* **Utkastmeddelanden**

  Generera e-postutkast genom att syntetisera forskning från presumtiva kunder och kontoinsikter för att skapa relevant, personaliserat e-postinnehåll baserat på BDR:s mål.

* **E-post om engagemangsplan**

  Skapa e-postutkast för engagemangsplanering som är personaliserade för varje steg i en BDR-definierad utdatacache, och se till att hela sekvensen är personaliserad

### Grundläggande användning

Adobe AI-agenter använder _frågor för naturligt språk_, vilket innebär att de använder samma språk i textprompten som när du pratar med en person. Ju mer detaljerad du är, desto bättre resultat.

Med naturspråket kan du be agenten att:

* Visa mina tilldelade leads utan någon interaktion än
* Visa alla mina ledtrådar som inte ingår i något självständigt engagemang
* Ge mig en detaljerad sammanfattning om `<company>`, inklusive deras inköpsgrupp, senaste avsiktssignaler och vårt tidigare engagemang.

Ni kan omedelbart förstå vilka konton och leads som är mest aktiva och visa det högsta avsikten, så att ni kan fokusera er energi där den har störst effekt.

Iterera längs hela kundresan genom att förfina era uppmaningar för att få de resultat ni behöver. Exempel:

* Utforma en uppföljning av e-postritning från ett sammanhang som inkomstsamtal eller rapporter. Upp till 120 ord. Ämnesrad: Engagerande, inbyggt nyckeltema. Intro: Ansluta med ett direkt citat från sammanhangskällor. Brödtext: Koppla samman med problempunkter och värdeförslag. CTA: föreslå ett kort samtal för att utforska vidare.

* Målet med det här e-postmeddelandet är att inleda ett samtal och bygga upp trovärdighet. Skriv ett e-postmeddelande med 120 ord som har en rådgivande och empatisk ton. Se till att du undviker en alltför välbekant metod eller försäljningsmetod och använd inte fraserna&quot;hoppas att du mår bra&quot;,&quot;bara checkar in&quot; eller&quot;snälla&quot;.

## Prospekt

I det här fönstret visas alla leads som du har tillgång till. Det går snabbt att kontrollera saker som ledstatus och senaste aktivitet.

![Visa alla dina leads i tabellen Leads](assets/prospects.png)

Klicka på filterikonen ![Filterikonen](../assets/icon-filter.png) om du vill filtrera efter lead-status.

## Förlovningsplaner

I det här fönstret finns information om definierade engagemangsplaner.

![Åtagandeplaner](assets/engagement-plans.png)

Klicka på **[!UICONTROL Create engagement plan]** om du vill skapa en ny engagemangsplan.

1. Ange ett namn och en valfri beskrivning på detaljscenen. Klicka på **[!UICONTROL Save and Continue]**.
1. I fasen Välj potentiella kunder väljer du de leads som ska ingå i den här planen.
1. Ange parametrarna för planen i fasen Definiera varaktighet.
1. Kontrollera att allt fungerar som det ska i förhandsgranskningsfasen.

## E-postutkorg

I panelen E-postutkorgen visas alla automatiska e-postmeddelanden som du har skickat.

## Mötesbokningar

På den här panelen visas alla möten som ställts in via automatisering.

## Chattinkorg

På den här panelen visas alla chattrådar.

![Chatinkorg](assets/chat-inbox.png)

Du kan inte bara interagera med kunder, du kan också se en sammanfattning av kontakten och en sammanfattning av tråden, så att du snabbt kan se var du befinner dig i tråden.

## Integreringar

Med integreringar kan säljkvalificeraren utnyttja CRM och andra datakällor för att berika kundprofiler och utnyttja säljaktiviteter:

* Integrera med e-postinkorgen för att hålla reda på relevanta inkommande e-postmeddelanden och hjälpa till att generera svar.
* Läs och uppdatera CRM-data, som Salesforce eller Microsoft® Dynamics, ZoomInfo eller Buildwidth.

![Outlook-integrering för försäljningskvalificerare](assets/outlook.png)

### Konfigurera en ny integrering

Om du vill starta en ny integrering klickar du på **[!UICONTROL Create integration]** längst upp till höger.

![Integreringsinformation](assets/integration-details.png)

Här definierar vi integreringens URL och fastställer nyttolasten som ska skickas.

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

1. Ange begränsnings- och cachevärden i avsnittet för nyttolastkonfiguration.
1. Klicka på pennikonen under Nyttolastskonfigurationen. Klistra in eller ange JSON-nyttolastobjektet i dialogrutan Klistra in nyttolast.
   * Begär nyttolast: Ett JSON-objekt som innehåller data för att skicka integrationsplatsen.
   * Svarets nyttolast: Den datastruktur du förväntar dig ska returneras.
1. Klicka på [!UICONTROL Test Connection] för att kontrollera att inställningarna är korrekta.

När anslutningsinställningarna är giltiga klickar du på **[!UICONTROL Save as draft]**.

När du är tillbaka i huvudintegrationstabellen markerar du integreringen och klickar på **[!UICONTROL Activate]** för att göra integreringen aktiv, eller **[!UICONTROL Save as draft]**.



#### Hantera åtkomst

Du kan hantera åtkomst till användare och vilken typ av data som delas med olika användargrupper.

Klicka på **[!UICONTROL Manage access]** för att öppna dialogrutan Hantera åtkomst.

I den här dialogrutan visas alla etiketter som har skapats av din organisation. Välj de etiketter som du vill använda för den här integreringen.

Om du behöver en ny etikett klickar du på **[!UICONTROL Create label]** och fyller i:

* Namn
* Eget namn
* Beskrivning

## Representativa inställningar

Här anger du information om dig själv: personuppgifter, e-post- och kalenderinställningar samt chatttillgänglighet.

### Information

På fliken Information kan du ange information om dig själv:

![Inställningar för försäljningsinformation för kvalificerare](assets/details.png)

### E-postinställningar

Konfigurera e-postanslutningarna på fliken E-postinställningar.

![E-postinställningar](assets/email-settings.png)

#### E-postanslutningar

Klicka på **[!UICONTROL Connect]** och följ sedan inloggningsproceduren för Microsoft.

#### E-postsignatur

Konfigurera din e-postsignatur som används i automatiskt genererade e-postmeddelanden.

### Kalenderinställningar

Ange din tidszon och tillgänglighet på fliken Kalenderinställningar.

![Kalenderinställningar](assets/calendar-settings.png)

#### Kalenderanslutning

Klicka på **[!UICONTROL Connect]** och följ inloggningsproceduren för Microsoft för att integrera din kalender.

#### E-post med mötesbekräftelse

När en kund bekräftar ett möte med dig får de bekräftelsemeddelandet via e-post som ett svar.
Använd de här inställningarna för att definiera e-postmeddelandets ämne och innehåll.

#### Inställningar

Ange standardlängd för mötet och hur lång tid du vill ha mellan mötena.

### Chattinställningar

På den här fliken anger du din tillgänglighet för tidszonslive-chatt.

![Chatinställningar](assets/chat-settings.png)

## Representativ förvaltning

På den här panelen visas en tabell över alla definierade representanter och deras kalenderstatus.

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

## Demonstrationsvideo

I följande video visas en kort demonstration av Sales Qualifier och Account Qualification Agent.

>[!VIDEO](https://video.tv.adobe.com/v/3476565?captions=swe)
