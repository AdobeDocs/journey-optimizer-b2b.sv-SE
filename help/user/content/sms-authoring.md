---
title: SMS-redigering
description: Skapa SMS-meddelanden för kontoresor med personalisering, länkar och godkännandehantering - förhandsgranska innehåll och konfigurera leveransinställningar i Journey Optimizer B2B edition.
feature: SMS Authoring, Content, Channels
role: User
exl-id: bd648253-74de-4083-a37a-ab7ceaea2746
source-git-commit: aa79e0655737541f122801f28db73d9f31ebb2f7
workflow-type: tm+mt
source-wordcount: '1243'
ht-degree: 0%

---

# SMS-redigering

Använd Adobe Journey Optimizer B2B edition för att skicka textmeddelanden (SMS) till dina kunder på deras mobila enheter. Du kan skapa, anpassa och förhandsgranska meddelanden i textformat från SMS-redigeraren.

Innan du skapar SMS-meddelanden för kontoresor måste du kontrollera att [SMS-tjänstprovidern är konfigurerad](../admin/configure-channels-sms.md) från inställningarna för _[!UICONTROL Administrator]_.

## Lägg till en SMS-åtgärd i en kontoresa

Du kan ställa in textmeddelandeleveranser under en kontoresa när du lägger till en _[!UICONTROL Take an action]_-nod och gör följande:

1. Välj _[!UICONTROL Action on]_&#x200B;för målet **[!UICONTROL People]**.

1. Välj _[!UICONTROL Action on people]_&#x200B;för **[!UICONTROL Send SMS]**.

   ![Vidta en åtgärd - skicka sms](assets/journey-node-send-sms.png){width="800" zoomable="yes"}

1. Klicka på _[!UICONTROL Take an action]_&#x200B;längst ned på panelen **[!UICONTROL Create SMS]**.

1. Ange en unik **[!UICONTROL Name]** för SMS-meddelandet i dialogrutan.

   ![Skapa ny SMS-dialogruta](assets/create-new-sms.png){width="400"}

1. Klicka på **[!UICONTROL Create]**.

   _Resurskartan_ öppnas och du kan skapa meddelandet och ange SMS-egenskaper för att skicka meddelandet.

### Skapa SMS-meddelandet

>[!IMPORTANT]
>
>**SMS-medgivandehantering**<br/>
>
>I enlighet med branschens standarder och bestämmelser måste alla SMS-marknadsföringsmeddelanden innehålla ett sätt för mottagarna att enkelt avbryta prenumerationen. För att göra detta kan SMS-mottagare svara med nyckelord för deltagande och avanmälan. Alla standardnyckelord för deltagande och avanmälan stöds och respekteras. Dessutom stöds och respekteras alla anpassade nyckelord som konfigurerats för ditt SMS-tjänstleverantörskonto.

Ange texten som du vill skicka i fältet **[!UICONTROL Message]**.

Du kan skapa ett meddelande med upp till 1 600 tecken där var 160:e tecken betraktas som ett enda SMS-meddelande.

![Skapa SMS-meddelandet](./assets/sms-message-compose.png){width="800" zoomable="yes"}

#### Anpassa textmeddelandet

1. Placera markören på den plats i meddelandet där du vill lägga till en personaliseringstoken.

1. Klicka på ikonen _Anpassa_ ( ![Anpassa ikon](../assets/do-not-localize/icon-personalize.svg) ) till höger om textmeddelanderutan.

   Dialogrutan ger åtkomst till kontotokens, persontoken och systemtokens. Både standardvariabler och anpassade variabler ingår. Du kan använda fältet _Sök_ för att hitta den token du behöver, eller navigera i mappträdet för att hitta och välja någon av tokenerna.

1. Lägg till en token genom att klicka på plustecknet ( **+** ) bredvid den.

   Om du vill lägga till variabeln med ett reservalternativ (standard som visas om fältet inte är tillgängligt för en lead) klickar du på ikonen _Mer_ ( **..** ) och väljer **[!UICONTROL Insert with fallback text]**.

   ![Klicka på ellipserna om du vill använda ett reserv för token](./assets/sms-message-personalize-ellipsis-fallback.png){width="700" zoomable="yes"}

1. I dialogrutan _[!UICONTROL Enter fallback value]_&#x200B;anger du den text som visas som reserv och klickar sedan på&#x200B;**[!UICONTROL Add]**.

   ![Ange grundtexten för token](./assets/sms-message-personalize-fallback-text.png){width="400"}

1. När du placerar dina personaliseringstoken klickar du på **[!UICONTROL Save]** för att spara ändringarna och återgå till SMS-huvudarbetsytan.

   Du kan fortsätta att redigera meddelandet med token efter behov.

#### Lägga till länkar (URL:er) till textmeddelandet

1. När du har angett meddelandetexten klickar du på ikonen _Länk_ ( ![Länkikon](../assets/do-not-localize/icon-link.svg) ) till höger om textrutan.

1. Ange **[!UICONTROL URL]** för länken.
<!--    
1. In the dialog, choose the type of URLs to link:

   * **[!UICONTROL Landing Page]** - Choose this option to select any of the approved Adobe Marketo Engage landing pages from your Marketo Engage instance. Select the workspace, and then select the landing page.

   * **[!UICONTROL External URL]** - This type is any external URL that you enter in the text box. -->

1. Om du väljer att använda en landningssida från Marketo Engage anger du spårningsalternativen.

   * **[!UICONTROL Enable tracking]** - Markera den här kryssrutan om du vill aktivera spårning, vilket kräver _förkortning_ av URL:en. För en landningssida används Marketo Engage-underdomänen som förkortad URL. Ett exempel på det förkortade URL-formatet visas. Den faktiska URL:en skapas när SMS:et skickas till mottagaren.

   * **[!UICONTROL Include mkt_tok]** - Markera den här kryssrutan om du vill spåra aktiviteter mot en användare.

     >[!NOTE]
     >
     >När du tillåter spårning men inaktiverar _[!UICONTROL Include mkt_tok]_&#x200B;innehåller mål-URL:en inte frågesträngsparametern `mkt_tok` efter omdirigering. Den här parametern används av Marketo Engage landningssidor och Munchkin för att säkerställa att spårning av personaktiviteter (t.ex. när en person säger upp prenumerationen på ett e-postmeddelande) sker. Inaktivera inte det här alternativet om inte parametern orsakar problem på webbplatsen.<br/>
     >Mer information om hur du använder Munchkin spårningskoder på din webbplats finns i [Marketo Engage-dokumentationen](https://experienceleague.adobe.com/sv/docs/marketo/using/product-docs/administration/additional-integrations/add-munchkin-tracking-code-to-your-website){target="_blank"}.

   ![Dialogrutan Lägg till länk för SMS-meddelande](./assets/sms-add-link-dialog.png){width="470"}

1. När länkalternativen är klara klickar du på **[!UICONTROL Add]** för att spara ändringarna och lägga till URL-länken i SMS-meddelandet.

### Ange SMS-egenskaper

1. I avsnittet _[!UICONTROL SMS properties]_&#x200B;anger du **[!UICONTROL Name]**(obligatoriskt, högst 100 tecken) och **[!UICONTROL Description]**(valfritt, högst 300 tecken) för meddelandet.

   Alpha, numeriska specialtecken är tillåtna för dessa fält. Följande reserverade tecken är **inte tillåtna**: `\`, `/`, `:`, `*`, `?`, `"`, `<`, `>` och `|`.

1. Välj **[!UICONTROL SMS Type]**:

   * Använd `Marketing` för kampanjtextmeddelanden, som kräver användarens samtycke.
   * Använd `Transactional` för icke-kommersiella meddelanden, till exempel orderbekräftelse, meddelanden om lösenordsåterställning eller leveransinformation.

1. För **[!UICONTROL SMS configuration]** väljer du en av de fördefinierade [SMS API-konfigurationerna](../admin/configure-channels-sms.md#create-new-api-credentials-for-an-sms-service-provider).

   Den här inställningen avgör vilken SMS gateway-tjänstleverantör och vilket konto som används för att leverera meddelandet.

1. Ange den **[!UICONTROL Sender number]**-&#x200B; som du vill använda för dina meddelanden.

   ![SMS-meddelandeegenskaper](./assets/sms-properties.png){width="700" zoomable="yes"}

   Mottagarnumret är alltid mappat till fältet `profile.mobilePhone.number` i Experience Platform.

### Simulera textmeddelandets innehåll {#preview-test}

>[!CONTEXTUALHELP]
>id="ajo-b2b_sms_preview_simulate"
>title="Kontrollera hur innehållet renderar"
>abstract="När innehållet är definierat kan du förhandsgranska och kontrollera återgivningen för den kanal som du använder."

När meddelandeinnehållet har definierats kan du använda testprofiler för att simulera (förhandsgranska) innehållet. Om du har infogat anpassat innehåll kan du kontrollera hur det här innehållet visas i meddelandet med hjälp av testprofildata.

>[!IMPORTANT]
>
>Spara SMS-meddelandet innan du fortsätter att simulera textmeddelandet.

1. Klicka på **[!UICONTROL Simulate Content]** högst upp på SMS-redigeringsarbetsytan.

1. Klicka på _[!UICONTROL Simulate Content]_&#x200B;på sidan **[!UICONTROL Add People]**.

1. Använd sidan _Simulera innehåll_ för att hantera leads som används för din testprofil.

   I listan som visas kan du söka efter och lägga till alla leads (upp till 10 leads i taget) från Marketo Engage lead-databas.

   Om du vill söka anger du hela e-postadressen och trycker på _Retur_. Motsvarande lead-profil visas för val.

   Förhandsgranskningen uppdaterar personaliseringsfälten för den valda profilen.

   Alla tillagda leads visas till vänster.

   Du kan hantera den här listan genom att lägga till fler personer och ta bort enskilda leads från profillistan (de tas inte bort från databasen).

1. Simulera innehåll för en vald lead.

   Välj något av leads till vänster. SMS-förhandsgranskningen på sidan uppdateras för den valda leadet.

   Du kan också välja en lead i väljaren ovanför förhandsvisningsområdet för att uppdatera SMS-förhandsgranskningen på sidan för motsvarande lead.

1. Om du vill avsluta sidan _[!UICONTROL Simulate Content]_&#x200B;och gå tillbaka till SMS-redigeringsarbetsytan klickar du på&#x200B;**[!UICONTROL Close]**&#x200B;överst till höger.

## Hantering av SMS-medgivande

Ett juridiskt krav är att mottagarna kan säga upp prenumerationen på kommunikation från ett varumärke och följa detta val. Om ni inte följer dessa regler medför detta juridiska risker för ert varumärke. Den här funktionen hjälper dig också att undvika att skicka oombedd kommunikation till dina mottagare, vilket kan göra att de markerar dina meddelanden som skräppost och skadar ditt rykte.

När du anger det här alternativet kan SMS-mottagare svara med nyckelord för anmälan och avanmälan. Alla standardnyckelord för deltagande och avanmälan stöds och respekteras, och alla anpassade nyckelord som har konfigurerats med SMS-tjänstleverantören. När du säger upp prenumerationen tas profilerna automatiskt bort från målgruppen för framtida marknadsföringsmeddelanden.

Med Journey Optimizer B2B edition kan du hantera avanmälan i SMS-meddelanden på följande sätt:

* Som standard, om en lead har avanmält sig från att ta emot meddelanden från dig, kommer motsvarande profil att uteslutas från efterföljande SMS-leveranser

* Detta medgivande kommer från olika källor (t.ex. AEP eller SMS) och synkroniseras med Journey Optimizer B2B edition. För närvarande stöder den endast ett enda medgivandetillstånd per lead på instansnivå (en lead &#39;John Doe&#39; är antingen prenumererad på eller avbeställd från all SMS i instansen). Det stöder för närvarande inte dubbelanmälan på varumärkesnivå/nivå av godkännande av enskilda prenumerationer.
