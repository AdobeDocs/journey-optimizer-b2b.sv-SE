---
title: Inställningar för Appkanal
description: Koppla ditt WhatsApp Business-konto via Meta Cloud API för att aktivera meddelanden i WhatsApp på Journey Optimizer B2B edition-kontoresor.
feature: Setup, Channels
role: Admin
exl-id: b554129e-b607-486a-be7b-aa3452a2fdad
source-git-commit: a6a5fefe75b675c0e0708f5a93be60cb032dc736
workflow-type: tm+mt
source-wordcount: '1355'
ht-degree: 5%

---

# Inställningar för whatsApp-kanal

Adobe Journey Optimizer B2B edition skickar whatsApp-meddelanden via Meta Cloud API. Innan marknadsförare kan skapa whatsApp-meddelanden för kontoresor måste en produktadministratör konfigurera en WhatsApp-kanal.

![WhatApp-uppgiftsflöde för Journey Optimizer B2B edition](./assets/whatsapp-flow-diagram.png)

## Förutsättningar

Kontrollera att du har följande innan du konfigurerar whatsApp-kanalen:

* [Ett Meta Business Manager-konto](https://business.facebook.com/)
* [Ett WhatsApp Business-konto med ett verifierat avsändarnamn och telefonnummer](https://developers.facebook.com/docs/whatsapp/overview/business-accounts/)
* [En Meta-token för användarauktorisering med rätt behörigheter](https://developers.facebook.com/blog/post/2022/12/05/auth-tokens/)
* [Godkända meddelandemallar i whatsApp Business Account](https://developers.facebook.com/docs/whatsapp/message-templates/guidelines/)

>[!IMPORTANT]
>
>Din användning av whatsApp-meddelandetjänster regleras av villkoren från Meta. Genom att gå till WhatsApp-meddelanden via Journey Optimizer B2B edition bekräftar du att du har granskat och samtycker till att följa [Meta WhatsApp Business policies](https://www.whatsapp.com/legal/business-policy/).

## Begränsningar {#limitations}

Följande begränsningar gäller för WhatsApp-kanalen:

* Adobe Journey Optimizer B2B edition är **inte HIPAA-kompatibelt och inte HIPAA-klart**. Dessutom omfattas inte tredjepartsleverantörer av Adobe BAA. Kunderna ansvarar för sin egen regelefterlevnad och leverantörsvalidering.

* Automatiska eller fördefinierade svarsmeddelanden stöds ännu inte.

* Från och med april 2025 upphörde Meta tillfälligt med leveransen av alla marknadsföringsmallmeddelanden till WhatsApp-användare som har ett amerikanskt telefonnummer (ett nummer bestående av en +1-uppringningskod och en amerikansk riktkod). [Läs mer i Meta-dokumentationen](https://developers.facebook.com/documentation/business-messaging/whatsapp/templates/marketing-templates/per-user-limits/)

* Integreringsfunktionen tillåter inte integrering med Business Service Provider (BSP) från tredje part.

## Slutför kanalkonfigurationen

Innan du skickar ett whatsApp-meddelande måste du konfigurera din Journey Optimizer B2B edition-miljö och ansluta den till ditt WhatsApp-konto.

Utför följande uppgifter:

1. [Skapa API-autentiseringsuppgifter för WhatsApp](#create-whatsapp-api-credentials)
1. [Lägg till webbhookarna för whatsApp](#configure-webhooks)
1. [Skapa konfigurationen för WhatsApp-kanalen](#create-channel-configuration)

### Skapa API-autentiseringsuppgifter för whatsApp

>[!NOTE]
>
>De beskrivna inställningarna är bara tillgängliga för användare med administratörsbehörighet.

1. Utöka avsnittet **[!UICONTROL Administration]** till vänster och klicka på **[!UICONTROL Channels]**.

1. Expandera **[!UICONTROL WhatsApp Settings]** på panelen och välj **[!UICONTROL API Credentials]**.

   ![Administration > Kanaler med whatsApp-inställningarna utökade](./assets/config-whatsapp-channels.png){width="800" zoomable="yes"}

1. Klicka på **[!UICONTROL Create new API credentials]** överst till höger.

1. Konfigurera dina API-autentiseringsuppgifter enligt nedanstående:

   * **[!UICONTROL Name]** - Ange ett unikt namn för autentiseringsuppgifterna
   * **[!UICONTROL API Token]** - Ange din API-token. Mer information finns i [Meta-dokumentationen](https://developers.facebook.com/blog/post/2022/12/05/auth-tokens/).
   * **[!UICONTROL Business Account ID]** - Ange det unika nummer som hör till din företagsportfölj. Mer information finns i [Meta-dokumentationen](https://www.facebook.com/business/help/1181250022022158?id=180505742745347).

   ![API-autentiseringsuppgifter för whatsApp-inställningar ](./assets/config-whatsapp-channels-api-credentials.png){width="500" zoomable="yes"}

1. Klicka på **[!UICONTROL Continue]**.

1. Välj den **[!UICONTROL WhatsApp Business Account]** som du vill ansluta till dina API-autentiseringsuppgifter för WhatsApp.

   ![API-autentiseringsuppgifter för whatsApp-inställningar väljer företagskonto](./assets/config-whatsapp-channels-api-credentials-details.png){width="500" zoomable="yes"}

1. Välj **[!UICONTROL Sender name]** som ska användas för att skicka WhatsApp-meddelanden.

   Telefonnummerinställningarna anges automatiskt:

   * **Kvalitetsklassificering** - Återger kundfeedback för meddelanden som skickats de senaste 24 timmarna.
      * Grön: Hög kvalitet
      * Gul: Medium-kvalitet
      * Röd: Låg kvalitet

     Mer information finns i [_Kvalitetsklassificering_](https://www.facebook.com/business/help/766346674749731#) i Meta-dokumentationen.

   * **Genomströmning** - anger den hastighet med vilken ditt telefonnummer kan skicka meddelanden.

1. Klicka på **[!UICONTROL Submit]** när du är klar med konfigurationen av dina API-autentiseringsuppgifter.

När du klickar på _[!UICONTROL Submit]_valideras och sparas inloggningsuppgifterna omedelbart, och du omdirigeras till listsidan för_[!UICONTROL API credentials]_.

Om de skickade autentiseringsuppgifterna är ogiltiga visas ett HTTP 500-felmeddelande. I så fall kan du välja att avbryta konfigurationen eller uppdatera den och skicka den igen.

+++HTTP 500 felsökning

Om du får ett HTTP 500-fel när du konfigurerar API-autentiseringsuppgifter för WhatsApp följer du dessa felsökningssteg:

1. Verifiera dina Adobe-berättiganden - Bekräfta att din organisation har _cjm_ whatsapp_-berättigandet etablerat. Utan det här berättigandet kan inte whatsApp-kanalen konfigureras.

1. Validera företagskontofälten - Kontrollera att alla obligatoriska fält är korrekta:

   * API-token - måste vara en giltig [Meta-åtkomsttoken med rätt behörighet](https://developers.facebook.com/blog/post/2022/12/05/auth-tokens/).
   * Konto-ID - måste matcha ditt [Meta Business Account ID](https://www.facebook.com/business/help/1181250022022158?id=180505742745347) exakt.

1. Testa autentiseringsuppgifterna externt - Verifiera dina autentiseringsuppgifter direkt med Meta API för att bekräfta om problemet gäller autentiseringsuppgifterna eller med hantering av autentiseringsuppgifter i Journey Optimizer B2B edition.

<!-- 1. Enable advanced logging - To identify internal server or authentication misconfigurations, enable advanced logs in your Journey Optimizer B2B Edition environment to provide detailed information about the API call failures. 
do we have advanced logs? How are they enabled?-->

1. Kontakta Adobe - Om miljön och berättigandena har bekräftats vara giltiga men HTTP 500-felet kvarstår kontaktar du Adobe.

+++

### Lägg till webbhookarna för whatsApp {#configure-webhooks}

>[!CONTEXTUALHELP]
>id="ajo_b2b_admin-whatsapp-webhook-inbound-keyword-category"
>title="Ankommande nyckelordskategori"
>abstract="<b>Opt-In</b>: skickar ditt definierade autosvar när en användare prenumererar. <br/><b>Avanmäl dig</b>: skickar ditt definierade autosvar när en användare avbeställer prenumerationen. <br/><b>Hjälp</b>: skickar det definierade automatiska svaret när en användare begär hjälp eller support. <br/><b>Standard</b>: skickar det automatiska svaret för reservlösningar när inga nyckelord matchar."

>[!CONTEXTUALHELP]
>id="ajo_b2b_admin_whatsapp-webhook-inbound-keyword"
>title="Ange dina nyckelord"
>abstract="Du kan definiera nyckelord för att aktivera specifika automatiska svar baserat på vilken användartext som visas. Nyckelord är inte skiftlägeskänsliga (stopp och STOP behandlas på samma sätt)."

>[!CONTEXTUALHELP]
>id="ajo_b2b_admin-whatsapp-webhook-webhook-url"
>title="Återanrops-URL"
>abstract="Verifieringsbegäran och webkrok-meddelanden för det här objektet skickas till den angivna URL:en."

>[!CONTEXTUALHELP]
>id="ajo_b2b_admin-whatsapp-webhook-verify-token"
>title="Verifiera token"
>abstract="Den token som Meta återställer för att bekräfta och verifiera återanrops-URL:en under verifieringsprocessen."

Med webbhooks kan Journey Optimizer B2B edition ta emot inkommande meddelanden, medgivanden och leveransmeddelanden från ditt WhatsApp Business Account. Konfigurera webbhooks för att säkerställa korrekt hantering av samtycke och meddelandespårning.

>[!NOTE]
>
>Utan angivna nyckelord för anmälan eller avanmälan aktiveras inte standardmeddelanden för samtycke.

När inloggningsuppgifterna för WhatsApp API har skapats kan du konfigurera webhooks.

1. Välj **[!UICONTROL WhatsApp Webhooks]** på navigeringspanelen.

1. Klicka på **[!UICONTROL Create Webhook]**.

1. Ange en **[!UICONTROL Name]** för webbkrokkonfigurationen.

1. För **[!UICONTROL Configuration]** väljer du API-autentiseringsuppgifterna (som skapades i föregående uppgift) som ska associeras med webkroken.

1. För **[!UICONTROL Inbound keyword category]** väljer du en kategori för att definiera nyckelord och svarsmeddelandet:

   * **[!UICONTROL Opt-in]** - Användare måste aktivt godkänna att ta emot meddelanden i WhatsApp, som ofta hanteras via formulär på din webbplats eller i din app.
   * **[!UICONTROL Opt-out]** - Konfigurera din webkrok så att den lyssnar efter fraser som `Stop` eller `No Message` så att användare automatiskt markeras som avanvisade.
   * **[!UICONTROL Help]** - Tillåt att automatiska system identifierar när en användare skickar `HELP` (eller liknande nyckelord som `Unknown`) och automatiskt svarar med specifik information, till exempel tjänstanvisningar.
   * **[!UICONTROL Default]** - Hantera inkommande meddelanden som inte matchar specifikt definierade nyckelord. Den fungerar som en reservkategori för att aktivera spårningshändelser (som öppnings- och leveransrapporter) i Adobe Experience Platform datamängder.

   När du väljer nyckelordskategori fylls standardnyckelorden i.

1. För **[!UICONTROL Enter a keyword]** kan du ange ett anpassat nyckelord och klicka på _Lägg till_ ( **+** ).

   Du kan lägga till flera nyckelord per kategori.

   >[!NOTE]
   >
   >Nyckelord är inte skiftlägeskänsliga (`stop` och `STOP` behandlas på samma sätt).

1. Ange **[!UICONTROL Reply message]** som ska skickas automatiskt när ett mottaget meddelande matchar ett nyckelord i den här kategorin.

   ![WhatApp-inställningswebhooks med nyckelord för deltagande och svarsmeddelande](./assets/config-whatsapp-channels-webhooks.png){width="500" zoomable="yes"}

1. För varje ytterligare nyckelordskategori som du vill konfigurera klickar du på _Lägg till_ (**+**) längst upp till höger och upprepar steg 5-7.

1. Klicka på **[!UICONTROL Submit]** om du vill spara webbkrokkonfigurationen.

### Kopiera token och URL

När webbkroken har skickats kan du hämta token- och URL-värdena och sedan registrera den i Meta.

1. I listan **[!UICONTROL WhatsApp Webhooks]** klickar du på ikonen Redigera ( ![ikonen Redigera ](../assets/do-not-localize/icon-edit.svg) ) för den webkrok du skapade.

1. Kopiera värdena **[!UICONTROL Verify Token]** och **[!UICONTROL Webhook URL]**.

   ![WattApp-inställningar för webkrok-inställningar som kopierar URL:en och verifierar token](./assets/config-whatsapp-channels-webhooks-copy-token-url.png){width="500" zoomable="yes"}

1. I [Meta för utvecklare-portalen](https://developers.facebook.com/) navigerar du till dina WhatsApp-programinställningar och konfigurerar webkroken med de värden som du kopierade.

### Skapa kanalkonfiguration {#create-channel-configuration}

En kanalkonfiguration definierar leveransinställningarna som används när WhatsApp-meddelanden skickas från en reseåtgärdsnod.

1. Välj **[!UICONTROL Channel configurations]** under _[!UICONTROL General settings]_på navigeringspanelen.

   ![Kanalkonfigurationslista](./assets/config-whatsapp-channels-general.png){width="600" zoomable="yes"}

1. Klicka på **[!UICONTROL Create channel configuration]** överst till höger.

1. Ange **[!UICONTROL Name]** och **[!UICONTROL Description]** (valfritt) för konfigurationen.

   >[!NOTE]
   >
   >Namnet måste börja med en bokstav (A-Z) och får bara innehålla alfanumeriska tecken, understreck (`_`), punkter (`.`) och bindestreck (`-`).

1. Välj `WhatsApp` för **[!UICONTROL Select channel]**.

   <!-- 1. For **[!UICONTROL Marketing action]**, select one or more marketing actions to associate consent policies with this configuration. -->

   <!-- Make sure to include all applicable marketing actions to ensure compliance with customer preferences. -->

   <!-- All consent policies associated with a selected marketing action are automatically leveraged in order to respect the preferences of your customers. For example, any WhatsApp message using that configuration in a journey is only sent to the profiles who have consented to receive WhatsApp messages from you. Profiles who have not consented to receive these communications are excluded. -->

1. Under _[!UICONTROL WhatsApp Settings]_väljer du **[!UICONTROL WhatsApp configuration]**(API-autentiseringsuppgifter) som du skapade i föregående uppgift.

1. Ange **[!UICONTROL Sender phone number]** som ska användas för meddelandeleverans.

   ![Information om konfiguration av whatsApp-kanal](./assets/config-whatsapp-channels-general-create.png){width="500" zoomable="yes"}

1. (Gäller för närvarande inte Journey Optimizer B2B edition) För **[!UICONTROL WhatsApp Execution Field]** väljer du det profilattribut som ska användas som prioritetstelefonnummer när flera telefonnummer är tillgängliga för en mottagare.

1. Klicka på **[!UICONTROL Submit]** om du vill spara eller **[!UICONTROL Save as draft]** om du vill slutföra och skicka konfigurationen senare.

Konfigurationen visas först med statusen _Bearbetar_ när valideringskontrollerna körs. När alla kontroller har slutförts ändras statusen till **_Aktiv_** och konfigurationen är klar att väljas när marknadsförare redigerar WhatsApp-meddelanden i resåtgärder.
