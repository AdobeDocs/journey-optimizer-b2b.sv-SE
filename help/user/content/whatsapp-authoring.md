---
title: WhatApp Authoring
description: Skapa whatsApp-meddelanden för kontoresor med godkända Meta-mallar, personaliseringstoken och leveransinställningar i Journey Optimizer B2B edition.
feature: Content, Channels, Account Journeys
role: User
source-git-commit: a9077a4fb5c90166433204d7a0a124f4f2e5ab92
workflow-type: tm+mt
source-wordcount: '779'
ht-degree: 0%

---

# WhatApp authoring

Använd Adobe Journey Optimizer B2B edition för att skicka whatsApp-meddelanden till kontomedlemmar på deras mobila enheter. Du kan skapa, anpassa och förhandsgranska meddelanden med godkända Meta-meddelandemallar från WhatsApp-redigeraren. <!-- Test your WhatsApp messages before publishing the account journey to ensure your intended rendering, accurate personalization, and proper configuration of all settings. -->

Innan du skapar WhatsApp-meddelanden för kontoresor måste du kontrollera att du har den nödvändiga [WhatsApp-kanalen konfigurerad](../admin/configure-channels-whatsapp.md) i _[!UICONTROL Administrator]_-inställningarna.

>[!NOTE]
>
>Endast _utgående_ WhatsApp-meddelandeelement stöds i Journey Optimizer B2B edition.

+++ Meddelandeelement och uppmaningar att vidta åtgärder som stöds

Följande meddelandetyper stöds i WhatsApp:

| Meddelandeelement | Beskrivning |
| - | - |
| Sidhuvuden | Valfri text som visas ovanför meddelandetexten. |
| Text | Stöder dynamiskt innehåll via parametrar. |
| Bilder (JPEG, PNG) | Måste vara i 8-bitars RGB- eller RGBA-format och mindre än 5 MB. |
| Videor | Måste vara 3GPP eller MP4, under 16 MB, och värd via URL. |
| Ljud | Endast tillgängligt för svarsmeddelanden. Måste vara AAC-, AMR-, MP3-, MP4- eller OGG-format, värd på en URL och under 16 MB. |
| Dokument | Måste vara mindre än 100 MB, lagras på en URL och i något av följande format: `.txt`, `.xls`/`.xlsx`, `.doc`/`.docx`, `.ppt`/`.pptx` eller `.pdf`. |
| Brödtext | Stöder dynamiskt innehåll via parametrar. |
| Sidfotstext | Stöder dynamiskt innehåll via parametrar. |

Följande call-to-action-alternativ är tillgängliga för dina WhatsApp-meddelanden:

| Call to action | Beskrivning |
| - | - |
| Besök webbplatsen | Endast en knapp tillåts med variabelparametrar. |
| Anropa whatsApp | Tillhandahåller en knapp som öppnar en whatsApp-chatt med det angivna telefonnumret direkt från meddelandet. |
| Telefonnummer | Tillhandahåller en knapp som initierar ett telefonsamtal till det angivna numret när användaren knackar på det. |

+++

## Lägg till en WhatsApp-åtgärd i en kontoresa

Du kan konfigurera WHatsApp-meddelandeleveranser i en kontoresa när du [lägger till en _[!UICONTROL Take an action]_nod](../journeys/action-nodes.md) och gör följande:

1. Välj **[!UICONTROL People]** för målet _[!UICONTROL Action on]_.

1. Välj **[!UICONTROL Send WhatsApp]** för _[!UICONTROL Action on people]_.

   ![Vidta en åtgärd - skicka whatsApp](./assets/whatsapp-journey-node.png){width="500" zoomable="yes"}

## Skapa meddelandet WhatsApp

1. Klicka på **[!UICONTROL Create WhatsApp]** längst ned på panelen _[!UICONTROL Take an action]_.

1. Ange en unik **[!UICONTROL Name]** (obligatoriskt) och **[!UICONTROL Description]** (valfritt) för WhatsApp-meddelandet i dialogrutan.

   ![Skapa en ny dialogruta för meddelanden i WhatsApp](./assets/whatsapp-create-dialog.png){width="400"}

1. Klicka på **[!UICONTROL Create]**.

   Designrymden _WhatsApp_ öppnas där du kan definiera whatsApp-åtgärder och skapa innehåll för att skicka meddelandet.

### Välj åtgärdskonfiguration

1. Välj fliken **[!UICONTROL Actions]** i designområdet _WhatsApp_.

1. För **[!UICONTROL WhatsApp configuration]** väljer du den [konfiguration](../admin/configure-channels-whatsapp.md#create-channel-configuration) som har stöd för marknadsföringsåtgärder och inställningar för meddelandeleverans efter dina behov.

   ![Skapa whatsApp - fliken Åtgärder](./assets/whatsapp-create-actions-tab.png){width="700" zoomable="yes"}

1. Klicka på **[!UICONTROL Edit content]** om du vill gå vidare till meddelandeparametrarna och texten.

### Välj en meddelandemall

>[!IMPORTANT]
>
>**Hantering av godkännande för whatsApp**: I enlighet med Meta policyer och tillämpliga bestämmelser får alla marknadsföringsmeddelanden för WhatsApp endast skickas till mottagare som har valt att ta emot kommunikation. Vilka som helst kan avanmäla sig när som helst genom att svara med ett avanmälningsnyckelord. Svaren för avanmälan respekteras automatiskt och motsvarande profiler tas bort från framtida målgrupper för marknadsföringsmeddelanden.

Meddelanden i appar skickas med förhandsgodkända meddelandemallar från ditt Meta WhatsApp Business Account. **Mallar måste granskas och godkännas av Meta** innan du kan använda dem i Journey Optimizer B2B edition. Arbeta med kontoadministratören för [!DNL Meta Business Manager] för att hantera och skicka in mallar för godkännande.

1. Välj något av följande för **[!UICONTROL Select template category]**:

   * Marknadsföring
   * Verktyg
   * Autentisering

1. För **[!UICONTROL Select WhatsApp template]** väljer du en godkänd mall för konfigurationens affärskonto.

   Mallinnehållet läses in i meddelanderedigeraren och visar mallstrukturen och eventuella variabelfält som är tillgängliga för anpassning.

   ![Meddelandemallen WhatsApp har valts och meddelandet har lästs in i förhandsgranskningsfönstret](./assets/whatsapp-create-select-template.png){width="700" zoomable="yes"}

   Mallar är ordnade efter kategori (_Marknadsföring_, _Verktyg_ och _Autentisering_) och status. Endast **_Godkända_** mallar är tillgängliga för markering. Mer information om hur du skapar whatsApp-mallar finns i [_Skapa meddelandemallar för ditt WhatsApp Business-konto_](https://www.facebook.com/business/help/2055875911147364?id=2129163877102343) i Meta-dokumentationen.

### Bild-URL

Om mallen innehåller några bilder använder du fältet **[!UICONTROL Image URL]** för att lägga till media-URL:er för att ersätta eventuella platshållare i mallen. Meta mallmedier är bara platshållare. Om du vill visa bilder, ljud eller video på rätt sätt måste du använda externa URL:er från Adobe Experience Manager eller andra källor.

### Anpassa meddelandeinnehållet

Godkända whatsApp-mallar kan innehålla variabelplatshållare som du definierar med hjälp av profildata eller dynamiska värden.

För varje variabelfält som visas i mallen klickar du på ikonen _Anpassa_ ( ![Anpassa ikon ](../assets/do-not-localize/icon-personalize.svg) ) bredvid fältet.

![Variabler i whatsApp-mallen](./assets/whatsapp-create-variables.png){width="700" zoomable="yes"}

Dialogrutan ger åtkomst till kontotokens, persontoken och systemtokens. Både standardvariabler och anpassade variabler ingår. Du kan använda fältet _Sök_ för att hitta den token du behöver, eller navigera i mappträdet för att hitta och välja någon av tokenerna.

Mer information om hur du använder variabler för personalisering finns i [Innehållspersonalisering](./personalization.md).

När dina personaliseringstoken definieras klickar du på **[!UICONTROL Save]** för att spara ändringarna och återgå till huvudarbetsytan för WhatsApp-meddelandet.
