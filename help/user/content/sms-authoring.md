---
title: SMS-redigering
description: Lär dig hur du skickar textmeddelanden (SMS) till dina kunder på deras mobila enheter och hur du anpassar och förhandsgranskar meddelanden i textformat från SMS-redigeraren.
feature: SMS Authoring, Content
exl-id: bd648253-74de-4083-a37a-ab7ceaea2746
source-git-commit: e0d9359560f31b3e66f593426c66e64d31044d54
workflow-type: tm+mt
source-wordcount: '1151'
ht-degree: 0%

---

# SMS-redigering

Använd Adobe Journey Optimizer B2B Edition för att skicka SMS-meddelanden till dina kunder på deras mobila enheter. Du kan skapa, anpassa och förhandsgranska meddelanden i textformat från SMS-redigeraren.

## SMS-konfiguration

Adobe Journey Optimizer B2B Edition skickar textmeddelanden via SMS-tjänstleverantörer (eller SMS-gatewayleverantörer). Konfigurera tjänsteleverantören från administratörsinställningarna innan du skapar SMS-meddelandet.

### SMS-gatewaytjänstleverantörer

Adobe Journey Optimizer B2B Edition är för närvarande integrerat med tredjepartsleverantörer som erbjuder textmeddelandetjänster oberoende av varandra. Leverantörer av textmeddelanden som stöds är Sinch, Twilio och Infobip.

Innan du konfigurerar en SMS-kanal i Adobe Journey Optimizer B2B Edition måste du skapa ett konto hos någon av dessa leverantörer för att få API-token och Service ID. Dessa autentiseringsuppgifter krävs för att konfigurera anslutningen mellan Adobe Journey Optimizer B2B Edition och den tillämpliga leverantören.

>[!IMPORTANT]
>
>Din användning av SMS-tjänster regleras av ytterligare villkor från tillämplig leverantör. Som tredjepartslösningar är Sinch, Twilio och Infobip tillgängliga för användare av Adobe Journey Optimizer B2B Edition genom en integrering. Adobe kontrollerar inte, och ansvarar inte för, tredjepartsprodukter. Kontakta din leverantör om du har problem eller vill ha hjälp med SMS.

### Verifiera en befintlig SMS API-konfiguration

>[!NOTE]
>
>De beskrivna inställningarna är bara tillgängliga för användare med SMS-administratörsbehörighet.

Utöka avsnittet **[!UICONTROL Administrator]** till vänster och klicka på **[!UICONTROL Configuration]**.

![Åtkomst till konfigurationen av AMA API-autentiseringsuppgifter](./assets/config-sms-api.png){width="800" zoomable="yes"}

På sidan visas de tillgängliga API-konfigurationerna för din instans. Du kan filtrera API-autentiseringsuppgifterna som visas av SMS-tjänstleverantören eller den som skapat dem.

![Klicka på filterikonen för att filtrera listan över API-autentiseringsuppgifter](./assets/config-sms-api-filter.png){width="500"}

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

_Så här konfigurerar du Twilio som SMS-leverantör med Adobe Journey Optimizer B2B Edition:_

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

_Så här konfigurerar du Infobip som SMS-leverantör med Adobe Journey Optimizer B2B Edition:_

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

1. Ange en unik **[!UICONTROL Name]** för e-postmeddelandet och en **[!UICONTROL Subject line]** i dialogrutan.

   ![Skapa ny SMS-dialogruta](assets/create-new-sms.png){width="500"}

## Skapa SMS-meddelandet

>[!IMPORTANT]
>
>**SMS-medgivandehantering**<br/>
><br/>
>I enlighet med branschens standarder och bestämmelser måste alla SMS-marknadsföringsmeddelanden innehålla ett sätt för mottagarna att enkelt avbryta prenumerationen. För att göra detta kan SMS-mottagare svara med nyckelord för deltagande och avanmälan. Alla standardnyckelord för deltagande och avanmälan stöds och respekteras. Dessutom stöds och respekteras alla anpassade nyckelord som konfigurerats för ditt SMS-tjänstleverantörskonto.

1. Ange texten som du vill skicka i fältet **[!UICONTROL Message]**.

   Du kan skapa ett meddelande med upp till 1 600 tecken där var 160:e tecken betraktas som ett enda SMS-meddelande.

1. **Anpassa textmeddelandet**.

   När du vill när du redigerar textmeddelandet klickar du på ikonen _Anpassa_ till höger om textrutan.

   ![Klicka på ikonen Anpassa om du vill lägga till variabler i meddelandet](./assets/sms-message-personalize-icon.png){width="800" zoomable="yes"}

   Den visade sidan ger åtkomst till dina Adobe Marketo Engage Lead- och System-tokens. Både standardvariabler och anpassade variabler ingår. Du kan använda sökfältet för att hitta den token du behöver, eller navigera i mappträdet för att hitta och välja någon av lead-/systemtokenerna.

   Placera markören på den plats i meddelandet där du vill lägga till variabeln. Lägg till en token genom att klicka på plustecknet ( **+** ) bredvid den. Om du vill lägga till en variabel med en reserv (standard som visas om fältet inte är tillgängligt för en lead) klickar du på ellipsen ( **..** ) och väljer **[!UICONTROL Insert with fallback text]**.

   ![Klicka på ellipserna om du vill använda ett reserv för token](./assets/sms-message-personalize-ellipsis-fallback.png){width="700" zoomable="yes"}

   I dialogrutan _[!UICONTROL Enter fallback value]_anger du den text som visas som reserv och klickar sedan på&#x200B;**[!UICONTROL Add]**.

   ![Ange grundtexten för token](./assets/sms-message-personalize-fallback-text.png){width="400"}

   När du placerar dina personaliseringstoken klickar du på **[!UICONTROL Save]** för att spara ändringarna och återgå till SMS-huvudarbetsytan. Du kan fortsätta att redigera meddelandet med token efter behov.

<!-- 1. **Add URLs to text message**.

   After defining your content, you can add URLs to your message by clicking the _Link_ icon.
   
   You can add two types of URLs: 

   External URLs - This is ANY external URL that can be directly typed into/ pasted into the input text box
   Adobe Marketo Engage Design Studio Landing Pages - Selecting this option, you will see a 'Landing Page picker' from which you can select any of the listed approved Landing Pages from Marketo Engage

   You can choose to 'shorten' either of these URLs by selecting the checkbox
   Note that the URL shortening function, uses the Marketo subdomain for shortening
   The shortened URL appears as a read-only field within the modal
   You can optionally track clicks on the URL
   You can also choose to include 'mkt_tok' for tracking activity against a user
   Click on Add to save changes & add the chosen URL to the SMS message
-->

## Ange SMS-egenskaper

1. I avsnittet _[!UICONTROL SMS properties]_anger du **[!UICONTROL Name]**(obligatoriskt, maximalt 100 cha\racter) och **[!UICONTROL Description]**(valfritt, maximalt 300 tecken) för meddelandet.

   Alpha, numeriska specialtecken är tillåtna för dessa fält. Följande reserverade tecken är **inte tillåtna**: `\`, `/`, `:`, `*`, `?`, `"`, `<`, `>` och `|`.

1. Välj **[!UICONTROL SMS Type]**:

   * Använd `Marketing` för kampanjtextmeddelanden, som kräver användarens samtycke.
   * Använd `Transactional` för icke-kommersiella meddelanden, till exempel orderbekräftelse, meddelanden om lösenordsåterställning eller leveransinformation.

1. Välj en av de fördefinierade API-konfigurationerna för **[!UICONTROL SMS configuration]**.

   Den här inställningen avgör vilken SMS gateway-tjänstleverantör och vilket konto som används för att leverera meddelandet.

1. Ange den **[!UICONTROL Sender number]**-&#x200B; som du vill använda för dina meddelanden.

   ![Vidta en åtgärd - skicka sms](./assets/sms-properties.png){width="700" zoomable="yes"}

   Mottagarnumret är alltid mappat till fältet `Lead.MainPhone` i Marketo Engage.

<!-- ## Preview the text message content

When your message content is defined, you can use test profiles to preview its content. If you inserted personalized content, you can check how this content is displayed in the message, using test profile data.

1. Click **[!UICONTROL Simulate Content]** at the top of the SMS authoring workspace.

1. From the _[!UICONTROL Simulate Content]_ page, click **[!UICONTROL Add People]**.

1. Use the # page to manage the leads used for your test profile.

   In the displayed list, you can search for and add any of the leads (up to 10 leads at a time) from the Marketo Engage lead database.

   To search, enter the whole email address and click enter. The corresponding lead profile shows up for selection.

   The preview updated to the personalization fields for the selected profile.

   All the added leads appear on the left rail of the 'Simulate Content' page

   You can manage this list by adding more people and deleting individual leads from the profile listing (it does not remove them from the database).

1. Simulate content for a lead.

   Select any of the leads listed on the left rail of the Simulate Content page and the SMS preview on the page updates for the corresponding lead.

   You can also select a lead from the 'drop-down' box above the preview space and the SMS preview on the page updates for the corresponding lead

1. To exit the _[!UICONTROL Simulate Content]_ page and return back to the SMS authoring workspace, click Close. -->
