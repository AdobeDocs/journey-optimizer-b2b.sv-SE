---
title: SMS-redigering
description: Lär dig hur du skickar textmeddelanden (SMS) till dina kunder på deras mobila enheter och hur du anpassar och förhandsgranskar meddelanden i textformat från SMS-redigeraren.
feature: SMS Authoring, Content
exl-id: bd648253-74de-4083-a37a-ab7ceaea2746
source-git-commit: e38ec0f128e811fd4ac21c624d9018854b91c78b
workflow-type: tm+mt
source-wordcount: '1927'
ht-degree: 0%

---

# SMS-redigering

Använd Adobe Journey Optimizer B2B Edition för att skicka SMS-meddelanden till dina kunder på deras mobila enheter. Du kan skapa, anpassa och förhandsgranska meddelanden i textformat från SMS-redigeraren.

## SMS-konfiguration

Adobe Journey Optimizer B2B edition skickar textmeddelanden via SMS-tjänstleverantörer (eller SMS-gatewayleverantörer). Innan du skapar SMS-meddelandet måste du konfigurera tjänsteleverantören från inställningarna för _Administratör_.

### SMS-gatewaytjänstleverantörer

Adobe Journey Optimizer B2B edition är för närvarande integrerat med tredjepartsleverantörer som erbjuder textmeddelandetjänster oberoende av varandra. Leverantörer av textmeddelanden som stöds är Sinch, Twilio och Infobip.

Innan du konfigurerar en SMS-kanal i Adobe Journey Optimizer B2B edition måste du skapa ett konto hos någon av dessa leverantörer för att få API-token och service-ID. Dessa autentiseringsuppgifter krävs för att konfigurera anslutningen mellan Adobe Journey Optimizer B2B edition och den aktuella providern.

>[!IMPORTANT]
>
>Din användning av SMS-tjänster regleras av ytterligare villkor från tillämplig leverantör. Som tredjepartslösningar finns Sinch, Twilio och Infobip tillgängliga för användare av Adobe Journey Optimizer B2B edition via en integrering. Adobe kontrollerar inte, och ansvarar inte för, tredjepartsprodukter. Kontakta din leverantör om du har problem eller vill ha hjälp med SMS.

### Verifiera en befintlig SMS API-konfiguration

>[!NOTE]
>
>De beskrivna inställningarna är bara tillgängliga för användare med SMS-administratörsbehörighet.

1. Utöka avsnittet **[!UICONTROL Administrator]** till vänster och klicka på **[!UICONTROL Channels]**.

   ![Åtkomst till konfigurationen av SMS API-autentiseringsuppgifter](./assets/config-sms-api.png){width="800" zoomable="yes"}

1. Välj **[!UICONTROL API Credentials]** på navigeringspanelen.

   På sidan visas de tillgängliga API-konfigurationerna för din instans.

1. Om det behövs klickar du på ikonen _Filter_ ( ![Visa eller dölj filterikon](../assets/do-not-localize/icon-filter.svg) ) och väljer alternativ för att visa listan över konfigurerade API-autentiseringsuppgifter av SMS-tjänstprovidern eller den som har skapat SMS.

   ![Klicka på Filterikonen för att förfina listan över API-autentiseringsuppgifter](./assets/config-sms-api-filter.png){width="600" zoomable="yes"}

### Skapa nya API-autentiseringsuppgifter för en SMS-tjänstleverantör

>[!BEGINTABS]

>[!TAB Dra]

_Så här konfigurerar du Sinch som SMS-leverantör med Adobe Journey Optimizer B2B Edition:_

1. Utöka avsnittet **[!UICONTROL Administrator]** till vänster och klicka på **[!UICONTROL Configuration]**.

1. Klicka på **[!UICONTROL Create new API credentials]** överst till höger i listan _[!UICONTROL API credentials]_.

1. Konfigurera dina SMS API-autentiseringsuppgifter:

   ![Konfigurera autentiseringsuppgifterna för SMS-API för SSI](./assets/config-sms-api-sinch.png){width="500"}

   * **[!UICONTROL SMS vendor]** - Välj `Sinch` som SMS-provider.

   * **[!UICONTROL Name]** - Ange ett namn för API-autentiseringsuppgifterna.

   * **[!UICONTROL Service ID]** och **[!UICONTROL API Token]** - Gå till API:er-sidan från ditt Sinch-konto (du hittar dina autentiseringsuppgifter på fliken SMS).

   Mer information om hur du söker efter den här informationen för ditt Sinch-konto finns i [dokumentationen för Sinch-utvecklare](https://developers.sinch.com/docs/sms/getting-started/#2-get-credentials)

1. Klicka på **[!UICONTROL Submit]** när konfigurationsinformationen för dina API-autentiseringsuppgifter är klar.

>[!TAB Twilio]

_Så här konfigurerar du Twilio som SMS-leverantör med Adobe Journey Optimizer B2B edition:_

1. Utöka avsnittet **[!UICONTROL Administrator]** till vänster och klicka på **[!UICONTROL Configuration]**.

1. Klicka på **[!UICONTROL Create new API credentials]** överst till höger i listan _[!UICONTROL API credentials]_.

1. Konfigurera dina SMS API-autentiseringsuppgifter:

   ![Konfigurera Twilio SMS API-autentiseringsuppgifter](./assets/config-sms-api-twilio.png){width="500"}

   * **[!UICONTROL SMS vendor]** - Välj `Twilio` som SMS-provider.

   * **[!UICONTROL Name]** - Ange ett namn för API-autentiseringsdefinitionen.

   * **[!UICONTROL Account SID]** och **[!UICONTROL Auth Token]** - Gå till rutan _Kontoinformation_ på Twilio Console Dashboard-sidan för att hitta dina autentiseringsuppgifter.

   Mer information om hur du hittar den här informationen för ditt Twilio-konto finns i [Twilio Help Center](https://help.twilio.com/articles/14726256820123-What-is-a-Twilio-Account-SID-and-where-can-I-find-it-).

1. Klicka på **[!UICONTROL Submit]** överst till höger på sidan när konfigurationsinformationen för dina API-autentiseringsuppgifter är klar.

>[!TAB Infobip]

_Så här konfigurerar du Infobip som SMS-leverantör med Adobe Journey Optimizer B2B edition:_

1. Utöka avsnittet **[!UICONTROL Administrator]** till vänster och klicka på **[!UICONTROL Configuration]**.

1. Klicka på **[!UICONTROL Create new API credentials]** överst till höger i listan _[!UICONTROL API credentials]_.

1. Konfigurera dina SMS API-autentiseringsuppgifter:

   ![Konfigurera autentiseringsuppgifterna för SMS API för Infobip](./assets/config-sms-api-infobip.png){width="500"}

   * **[!UICONTROL SMS vendor]** - Välj `Infobip` som SMS-provider.

   * **[!UICONTROL Name]** - Ange ett namn för API-autentiseringsdefinitionen.

   * **[!UICONTROL API base URL]** och **[!UICONTROL API key]** - Gå till webbgränssnittets hemsida eller API-nyckelhanteringssidan för ditt InfoBp-konto för att hitta dina autentiseringsuppgifter.

   Mer information om hur du hittar den här informationen för ditt InfoBitp-konto finns i [informationsdokumentationen](https://www.infobip.com/docs/api/_blank).

1. Klicka på **[!UICONTROL Submit]** överst till höger på sidan när konfigurationsinformationen för dina API-autentiseringsuppgifter är klar.

>[!ENDTABS]

När du klickar på _[!UICONTROL Submit]_valideras och sparas inloggningsuppgifterna omedelbart, och du omdirigeras till listsidan för_[!UICONTROL API credentials]_. Om de skickade inloggningsuppgifterna är ogiltiga visas ett felmeddelande på listsidan. I så fall kan du välja att avbryta konfigurationen eller att uppdatera den och skicka den igen.

## Lägg till en SMS-åtgärd i en kontoresa

Du kan ställa in textmeddelandeleveranser på en kontoresa när du lägger till en _[!UICONTROL Take an action]_-nod och gör följande:

1. Välj **[!UICONTROL People]** för målet _[!UICONTROL Action on]_.

1. Välj **[!UICONTROL Send SMS]** för _[!UICONTROL Action on people]_.

   ![Vidta en åtgärd - skicka sms](assets/journey-node-send-sms.png){width="800" zoomable="yes"}

1. Klicka på **[!UICONTROL Create SMS]** längst ned på panelen _[!UICONTROL Take an action]_.

1. Ange en unik **[!UICONTROL Name]** för SMS-meddelandet i dialogrutan.

   ![Skapa ny SMS-dialogruta](assets/create-new-sms.png){width="400"}

1. Klicka på **[!UICONTROL Create]**.

   _Researney-innehållsdesignern_ öppnas och du kan skapa meddelandet och ange SMS-egenskaperna för att skicka meddelandet.

### Skapa SMS-meddelandet

>[!IMPORTANT]
>
>**SMS-medgivandehantering**<br/>
>
>I enlighet med branschens standarder och bestämmelser måste alla SMS-marknadsföringsmeddelanden innehålla ett sätt för mottagarna att enkelt avbryta prenumerationen. För att göra detta kan SMS-mottagare svara med nyckelord för deltagande och avanmälan. Alla standardnyckelord för deltagande och avanmälan stöds och respekteras. Dessutom stöds och respekteras alla anpassade nyckelord som konfigurerats för ditt SMS-tjänstleverantörskonto.

Ange texten som du vill skicka i fältet **[!UICONTROL Message]**.

Du kan skapa ett meddelande med upp till 1 600 tecken där var 160:e tecken betraktas som ett enda SMS-meddelande.

![Klicka på ikonen Anpassa om du vill lägga till variabler i meddelandet](./assets/sms-message-compose.png){width="800" zoomable="yes"}

#### Anpassa textmeddelandet

1. När du vill när du redigerar textmeddelandet klickar du på ikonen _Anpassa_ ( ![Anpassa ikon](../assets/do-not-localize/icon-personalize.svg) ) till höger om textmeddelanderutan.

   Den visade sidan ger åtkomst till dina Adobe Marketo Engage Lead- och System-tokens. Både standardvariabler och anpassade variabler ingår. Du kan använda fältet _Sök_ för att hitta den token du behöver, eller navigera i mappträdet för att hitta och välja någon av lead-/systemtokenerna.

1. Placera markören på den plats i meddelandet där du vill lägga till variabeln.

1. Lägg till en token genom att klicka på plustecknet ( **+** ) bredvid den.

   Om du vill lägga till variabeln med ett reservalternativ (standard som visas om fältet inte är tillgängligt för en lead) klickar du på ikonen _Mer_ ( **..** ) och väljer **[!UICONTROL Insert with fallback text]**.

   ![Klicka på ellipserna om du vill använda ett reserv för token](./assets/sms-message-personalize-ellipsis-fallback.png){width="700" zoomable="yes"}

1. I dialogrutan _[!UICONTROL Enter fallback value]_anger du den text som visas som reserv och klickar sedan på&#x200B;**[!UICONTROL Add]**.

   ![Ange grundtexten för token](./assets/sms-message-personalize-fallback-text.png){width="400"}

1. När du placerar dina personaliseringstoken klickar du på **[!UICONTROL Save]** för att spara ändringarna och återgå till SMS-huvudarbetsytan.

   Du kan fortsätta att redigera meddelandet med token efter behov.

#### Lägga till länkar (URL:er) till textmeddelandet

1. När du har angett meddelandetexten klickar du på ikonen _Länk_ ( ![Länkikon](../assets/do-not-localize/icon-link.svg) ) till höger om textrutan.

1. I dialogrutan väljer du vilken typ av URL-adresser som ska länkas:

   * **[!UICONTROL Landing Page]** - Välj det här alternativet om du vill välja någon av de godkända Adobe Marketo Engage Design Studio-landningssidorna från Marketo Engage-instansen. Markera arbetsytan och välj sedan landningssidan.

   * **[!UICONTROL External URL]** - Den här typen är en extern URL som du anger i textrutan.

1. Om du väljer att använda en landningssida anger du spårningsalternativen.

   * **[!UICONTROL Enable tracking]** - Markera den här kryssrutan om du vill aktivera spårning, vilket kräver _förkortning_ av URL:en. För en landningssida används underdomänen Marketo Engage för den förkortade URL:en. Ett exempel på det förkortade URL-formatet visas. Den faktiska URL:en skapas när SMS:et skickas till mottagaren.

   * **[!UICONTROL Include mkt_tok]** - Markera den här kryssrutan om du vill spåra aktiviteter mot en användare.

     >[!NOTE]
     >
     >När du tillåter spårning men inaktiverar _[!UICONTROL Include mkt_tok]_innehåller mål-URL:en inte frågesträngsparametern `mkt_tok` efter omdirigering. Den här parametern används av landningssidor på Marketo Engage och Munchkin för att säkerställa att spårning av personaktiviteter (t.ex. när en person säger upp prenumerationen på ett e-postmeddelande) sker. Inaktivera inte det här alternativet om inte parametern orsakar problem på webbplatsen.<br/>
     >Mer information om hur du använder Munchkin spårningskoder på din webbplats finns i [Marketo Engage-dokumentationen](https://experienceleague.adobe.com/en/docs/marketo/using/product-docs/administration/additional-integrations/add-munchkin-tracking-code-to-your-website){target="_blank"}.

   ![Dialogrutan Lägg till länk för SMS-meddelande](./assets/sms-add-link-dialog.png){width="470"}

1. När länkalternativen är klara klickar du på **[!UICONTROL Add]** för att spara ändringarna och lägga till URL-länken i SMS-meddelandet.

### Ange SMS-egenskaper

1. I avsnittet _[!UICONTROL SMS properties]_anger du **[!UICONTROL Name]**(obligatoriskt, högst 100 tecken) och **[!UICONTROL Description]**(valfritt, högst 300 tecken) för meddelandet.

   Alpha, numeriska specialtecken är tillåtna för dessa fält. Följande reserverade tecken är **inte tillåtna**: `\`, `/`, `:`, `*`, `?`, `"`, `<`, `>` och `|`.

1. Välj **[!UICONTROL SMS Type]**:

   * Använd `Marketing` för kampanjtextmeddelanden, som kräver användarens samtycke.
   * Använd `Transactional` för icke-kommersiella meddelanden, till exempel orderbekräftelse, meddelanden om lösenordsåterställning eller leveransinformation.

1. Välj en av de fördefinierade API-konfigurationerna för **[!UICONTROL SMS configuration]**.

   Den här inställningen avgör vilken SMS gateway-tjänstleverantör och vilket konto som används för att leverera meddelandet.

1. Ange den **[!UICONTROL Sender number]**-&#x200B; som du vill använda för dina meddelanden.

   ![Vidta en åtgärd - skicka sms](./assets/sms-properties.png){width="700" zoomable="yes"}

   Mottagarnumret är alltid mappat till fältet `Lead.mobilePhone` i Marketo Engage.

### Simulera textmeddelandets innehåll {#preview-test}

>[!CONTEXTUALHELP]
>id="ajo-b2b_sms_preview_simulate"
>title="Kontrollera hur innehållet renderar"
>abstract="När innehållet är definierat kan du förhandsgranska det och kontrollera återgivningen för den kanal som du använder."

När meddelandeinnehållet har definierats kan du använda testprofiler för att simulera (förhandsgranska) innehållet. Om du har infogat anpassat innehåll kan du kontrollera hur det här innehållet visas i meddelandet med hjälp av testprofildata.

>[!IMPORTANT]
>
>Spara SMS-meddelandet innan du fortsätter att simulera textmeddelandet.

1. Klicka på **[!UICONTROL Simulate Content]** högst upp på SMS-redigeringsarbetsytan.

1. Klicka på **[!UICONTROL Add People]** på sidan _[!UICONTROL Simulate Content]_.

1. Använd sidan _Simulera innehåll_ för att hantera leads som används för din testprofil.

   I listan som visas kan du söka efter och lägga till alla leads (upp till 10 leads i taget) från databasen för lead i Marketo Engage.

   Om du vill söka anger du hela e-postadressen och trycker på _Retur_. Motsvarande lead-profil visas för val.

   Förhandsgranskningen uppdaterar personaliseringsfälten för den valda profilen.

   Alla tillagda leads visas till vänster.

   Du kan hantera den här listan genom att lägga till fler personer och ta bort enskilda leads från profillistan (de tas inte bort från databasen).

1. Simulera innehåll för en vald lead.

   Välj något av leads till vänster. SMS-förhandsgranskningen på sidan uppdateras för den valda leadet.

   Du kan också välja en lead i väljaren ovanför förhandsvisningsområdet för att uppdatera SMS-förhandsgranskningen på sidan för motsvarande lead.

1. Om du vill avsluta sidan _[!UICONTROL Simulate Content]_och gå tillbaka till SMS-redigeringsarbetsytan klickar du på&#x200B;**[!UICONTROL Close]**överst till höger.

## Hantering av SMS-medgivande

Ett juridiskt krav är att mottagarna kan säga upp prenumerationen på kommunikation från ett varumärke och följa detta val. Om ni inte följer dessa regler medför detta juridiska risker för ert varumärke. Den här funktionen hjälper dig också att undvika att skicka oombedd kommunikation till dina mottagare, vilket kan göra att de markerar dina meddelanden som skräppost och skadar ditt rykte.

När du anger det här alternativet kan SMS-mottagare svara med nyckelord för anmälan och avanmälan. Alla standardnyckelord för deltagande och avanmälan stöds och respekteras, och alla anpassade nyckelord som konfigureras hos SMS-tjänstleverantören. När du säger upp prenumerationen tas profilerna automatiskt bort från målgruppen för framtida marknadsföringsmeddelanden.

Journey Optimizer B2B Edition ger möjlighet att hantera avanmälan i SMS-meddelanden med följande logik:

* Som standard, om en lead har avanmält sig från att ta emot meddelanden från dig, kommer motsvarande profil att uteslutas från efterföljande SMS-leveranser

* Detta lead-medgivande kommer från olika källor (som AEP eller SMS-tjänstleverantören) synkroniseras med Journey Optimizer B2B edition. För närvarande stöder den endast ett enda medgivandetillstånd per lead på instansnivå (en lead &#39;John Doe&#39; är antingen prenumererad på eller avbeställd från all SMS i instansen). Det stöder för närvarande inte dubbelanmälan på varumärkesnivå/nivå av godkännande av enskilda prenumerationer.
