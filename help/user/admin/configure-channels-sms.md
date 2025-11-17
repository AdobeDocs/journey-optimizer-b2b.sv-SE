---
title: SMS-konfiguration
description: Koppla upp SMS-leverantörer som Sinch, Twilio och Infobip med API-behörigheter för att aktivera textmeddelanden på Journey Optimizer B2B edition-resor.
feature: Setup, Channels
role: Admin
exl-id: bd41a5ec-929f-489f-a757-0720c1b44ed2
source-git-commit: 325ae8e8c1f3bbf25e0d96907ede6cb9f2e76e3d
workflow-type: tm+mt
source-wordcount: '657'
ht-degree: 0%

---

# SMS-konfiguration

Adobe Journey Optimizer B2B edition skickar textmeddelanden via SMS-tjänstleverantörer (eller SMS-gatewayleverantörer). Innan du skapar SMS-meddelandet måste du konfigurera tjänsteleverantören från inställningarna för _Administratör_.

## SMS-gatewaytjänstleverantörer

Adobe Journey Optimizer B2B edition är för närvarande integrerat med tredjepartsleverantörer som erbjuder textmeddelandetjänster oberoende av varandra. Leverantörer av textmeddelanden som stöds är Sinch, Twilio och Infobip.

Innan du konfigurerar en SMS-kanal i Adobe Journey Optimizer B2B edition måste du skapa ett konto hos någon av dessa leverantörer för att få API-token och service-ID. Dessa autentiseringsuppgifter krävs för att konfigurera anslutningen mellan Adobe Journey Optimizer B2B edition och den aktuella providern.

>[!IMPORTANT]
>
>Din användning av SMS-tjänster regleras av ytterligare villkor från tillämplig leverantör. Som tredjepartslösningar finns Sinch, Twilio och Infobip tillgängliga för användare av Adobe Journey Optimizer B2B edition via en integrering. Adobe kontrollerar inte och ansvarar inte för tredjepartsprodukter. Kontakta din leverantör om du har problem eller vill ha hjälp med SMS.

## Verifiera en befintlig SMS API-konfiguration

>[!NOTE]
>
>De beskrivna inställningarna är bara tillgängliga för användare med SMS-administratörsbehörighet.

1. Utöka avsnittet **[!UICONTROL Administrator]** till vänster och klicka på **[!UICONTROL Channels]**.

   ![Åtkomst till konfigurationen av SMS API-autentiseringsuppgifter](./assets/config-sms-api.png){width="800" zoomable="yes"}

1. Välj **[!UICONTROL API Credentials]** på navigeringspanelen.

   På sidan visas de tillgängliga API-konfigurationerna för din instans.

1. Om det behövs klickar du på ikonen _Filter_ ( ![Visa eller dölj filterikon](../assets/do-not-localize/icon-filter.svg) ) och väljer alternativ för att visa listan över konfigurerade API-autentiseringsuppgifter av SMS-tjänstprovidern eller den som har skapat SMS.

   ![Klicka på Filterikonen för att förfina listan över API-autentiseringsuppgifter](./assets/config-sms-api-filter.png){width="600" zoomable="yes"}

## Skapa nya API-autentiseringsuppgifter för en SMS-tjänstleverantör

>[!BEGINTABS]

>[!TAB Dra]

_Konfigurera Sinch som SMS-provider med Adobe Journey Optimizer B2B edition :_

1. Utöka avsnittet **[!UICONTROL Administrator]** till vänster och klicka på **[!UICONTROL Configuration]**.

1. Klicka på **[!UICONTROL Create new API credentials]** överst till höger i listan _[!UICONTROL API credentials]_.

1. Konfigurera dina SMS API-autentiseringsuppgifter:

   ![Konfigurera autentiseringsuppgifterna för SMS-API för SSI](./assets/config-sms-api-sinch.png){width="500"}

   * **[!UICONTROL SMS vendor]** - Välj `Sinch` som SMS-provider.

   * **[!UICONTROL Name]** - Ange ett namn för API-autentiseringsuppgifterna.

   * **[!UICONTROL Service ID]** och **[!UICONTROL API Token]** - Gå till API:er-sidan från ditt Sinch-konto (du hittar dina autentiseringsuppgifter på fliken SMS).

   Mer information om hur du söker efter den här informationen för ditt Sinch-konto finns i [dokumentationen för Sinch-utvecklare](https://developers.sinch.com/docs/sms/getting-started)

1. Klicka på **[!UICONTROL Submit]** när konfigurationsinformationen för dina API-autentiseringsuppgifter är klar.

>[!TAB Twilio]

_Konfigurera Twilio som SMS-leverantör med Adobe Journey Optimizer B2B edition :_

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

_Konfigurera Infobip som din SMS-leverantör med Adobe Journey Optimizer B2B edition :_

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

När du klickar på _[!UICONTROL Submit]_&#x200B;valideras och sparas inloggningsuppgifterna omedelbart, och du omdirigeras till listsidan för&#x200B;_[!UICONTROL API credentials]_. Om de skickade inloggningsuppgifterna är ogiltiga visas ett felmeddelande på listsidan. I så fall kan du välja att avbryta konfigurationen eller att uppdatera den och skicka den igen.
