---
title: Aktivera Marketo Engage för att stödja reseåtgärder
description: Aktivera Marketo Engage-anslutningar för att stödja kundresor så att marknadsförarna kan samordna kampanjer mellan Marketo Engage och Journey Optimizer B2B edition.
feature: Integrations, Audiences, Buying Groups
role: User, Admin
source-git-commit: 9b77570ddb9b416251f38db51a57507a935a526a
workflow-type: tm+mt
source-wordcount: '433'
ht-degree: 0%

---


# Aktivera Marketo Engage-instanser för att stödja åtgärder

Marketo Engage-åtgärder är _personbaserade_-åtgärder som gör att du kan koordinera din _kontobaserade_ marknadsföringssamordning mellan Journey Optimizer B2B edition och dina _lead-baserade_ marknadsföringssatsningar i Marketo Engage. Använd dessa åtgärder för att samordna statiskt listmedlemskap och för att placera personer i kampanjer.

Om du vill använda Marketo Engage reseåtgärder skapar en administratör först en [anpassad tjänst](https://experienceleague.adobe.com/sv/docs/marketo-developer/marketo/rest/custom-services){target="_blank"} i Marketo Engage, som tillhandahåller de autentiseringsuppgifter som krävs för autentisering. Därefter använder en produktadministratör för Journey Optimizer B2B edition inloggningsuppgifterna för att skapa en anslutning till Marketo Engage. Journey Optimizer B2B edition-användare kan sedan referera till anslutningen för att konfigurera Marketo Engage-åtgärder på <!-- person and -->kontoresor, som att lägga till eller ta bort personer från Marketo Engage-listor eller lägga till dem i kampanjförfrågningar.

## Konfigurera en Marketo Engage-anslutning {#external-marketo-configure}

>[!CONTEXTUALHELP]
>id="ajo-b2b_marketo-configure-connections"
>title="Extern Marketo Engage-anslutning"
>abstract="Produktadministratörer kan konfigurera anslutningar till externa Marketo Engage-instanser, vilket gör dem tillgängliga för reseåtgärder."

Utför följande uppgifter för att konfigurera en extern Marketo Engage-instans för användning med reseåtgärder.

### Skapa Marketo Engage anpassade tjänst

1. Logga in på Marketo Engage som administratör och [skapa en anpassad tjänst](https://experienceleague.adobe.com/sv/docs/marketo/using/product-docs/administration/additional-integrations/create-a-custom-service-for-use-with-rest-api){target="_blank"}.
1. Kopiera följande värden som ska användas för Journey Optimizer B2B edition-anslutningen:

   * MUNCHKIN ID
   * Klient-ID
   * Klienthemlighet

Synligheten för Marketo Engage-arbetsytan för resurser, som listor och kampanjer, styrs av rollbehörigheterna [som tilldelats i den anpassade tjänsten](https://experienceleague.adobe.com/sv/docs/marketo-developer/marketo/rest/custom-services#permission-list){target="_blank"}. Marknadsförarna kan använda samma uppkoppling flera gånger under en resa och använda olika Marketo Engage-anslutningar under samma resa.

### Lägg till integreringen

![Lägg till integreringsinformation](assets/integration-connection-details.png){width="800" zoomable="yes"}

1. I Journey Optimizer B2B edition går du till **[!UICONTROL Administration]** > **[!UICONTROL Configurations]**.
1. Välj till fliken **[!UICONTROL Integrations]**.
1. Klicka på **[!UICONTROL Create a connection]**.
1. Ange **[!UICONTROL Name]** (obligatoriskt) och **[!UICONTROL Description]** (valfritt).
1. Välj den uppdateringsprincip som används för att tillämpa en åtgärd på en matchande personpost.

   När en åtgärd körs för den anslutna Marketo Engage-instansen avgör den valda _uppdateringsprincipen_ personposterna i Marketo Engage och väljer om det finns flera identifierare i den enhetliga personprofilen.

   * **[!UICONTROL Update all matching records]**
   * **[!UICONTROL Update only the oldest matching record]**
   * **[!UICONTROL Update only the newest matching record]**

   >[!NOTE]
   >
   >Folk går igenom resan oavsett vilken matchning de har, förutom när ett fel inträffar.

1. Ange Munchkin-ID, klient-ID och klienthemlighet för tjänsten som skapades i den externa Marketo Engage-instansen.
1. Klicka på **[!UICONTROL Connect to Marketo]**.
1. Klicka på **[!UICONTROL Create]**.

## Använda anslutningen i en reseåtgärd

När en marknadsförare använder en Marketo Engage-åtgärd under en resa kan de konfigurera noden med hjälp av anslutningsnamnet.

Med den slutförda integreringen är Marketo Engage-åtgärder tillgängliga från **Åtgärder på:** i nodegenskaperna.

![Marketo-åtgärdslista](assets/marketo-actions-list.png){width="800" zoomable="yes"}