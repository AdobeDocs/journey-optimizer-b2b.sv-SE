---
title: Målgrupper
description: Läs mer om kontomålgrupper och hur de möjliggör kontobaserade resor.
source-git-commit: 3d3f0e4d6e62aa7126e915cfd5b54151d1bf9186
workflow-type: tm+mt
source-wordcount: '467'
ht-degree: 0%

---


# Målgrupper

En målgrupp är en uppsättning personer som har liknande beteenden och/eller egenskaper. Journey Optimizer B2B Edition använder de kontosegmenteringsfunktioner som finns i Adobe Real-time Customer Data Platform B2B- och B2P-utgåvorna. Med kontosegmentering kan användarna generera kontomgrupper genom att utnyttja data från alla B2B-enheter i systemet. Dessa målgrupper fungerar som indata för kontoresor med Journey Optimizer B2B Edition, vilket underlättar smidig aktivering och personalisering.

Läs mer om kontomålgrupper och hur du definierar dem i [Adobe Experience Platform Segmentation Service-dokumentationen](https://experienceleague.adobe.com/en/docs/experience-platform/segmentation/ui/account-audiences).

## Arbetsflöde för målgrupp

Du kan tänka dig Journey Optimizer B2B Edition som ett mål för Experience Platform (AEP) som inte visas i målkatalogen. Aktivera kontomålgrupper för Journey Optimizer B2B Edition med följande steg:

1. Skapa scheman för dina data i AEP.
1. Lägg in data i AEP.
1. Skapa ett kontosegment för att utvärdera dina data.
1. Aktivera utvärderade data i Journey Optimizer B2B Edition.

I Journey Optimizer B2B Edition används kontomålgrupper som indata för kontobaserade resor, vilket gör att ni kan inrikta er på personer på dessa konton. Du kan t.ex. använda kontomålgrupper för att hämta poster för alla konton som inte har kontaktinformation för någon med titeln Chief Operating Officer (COO) eller Chief Marketing Officer (CMO).

Med Journey Optimizer B2B Edition kan ni skapa kontogrupper för Adobe Experience Platform (AEP) direkt från den vänstra navigeringen och införliva dem i era kontoresor.

![Åtkomst till målgrupper på konton](./assets/account-audiences-browse.png){width="800" zoomable="yes"}

## Skapa en kontopublik

Definiera målgruppen genom att skapa en kontosegmentering. Du kan skapa kontosegmenteringen direkt i Journey Optimizer B2B Edition eller använda [segmentbyggargränssnittet](https://experienceleague.adobe.com/en/docs/experience-platform/segmentation/ui/segment-builder). Nedan följer de steg du kan använda för att skapa en kontosegmentering i Journey Optimizer B2B Edition.

1. Välj **[!UICONTROL Accounts]** > **[!UICONTROL Audiences]** i den vänstra navigeringen.

1. Klicka på **[!UICONTROL Create audience]** överst till höger.

1. Skapa segmentdefinitionen.

   Kontoattributen och målgrupperna visas i det vänstra navigeringsfältet. På fliken _[!UICONTROL Attributes]_kan du lägga till både plattformsskapade och anpassade attribut. Dra varje attribut för att skapa logiken för segmentet.

   >[!TIP]
   >
   >När du skapar en kontopublik ska du vara medveten om att händelser listas under _[!UICONTROL People]_eftersom dessa attribut är kopplade till personer.<br/>
   >
   >Under fliken _[!UICONTROL Audiences]_kan du lägga till tidigare skapade personbaserade målgrupper som du kan bygga vidare på när du skapar en egen målgrupp.

   I följande exempel definieras målgrupper som skapats med `Country Code`, `Revenue Amount` och `Market segment`. Frågan på engelska skulle vara:&quot;Jag vill ha alla konton i USA som finns i finanssegmentet vars intäkter överstiger 1 miljon dollar.&quot;

   ![exempel på segmentbyggare för kontomublik](./assets/audience-segment-builder-US-finance-1M.png){width="700" zoomable="yes"}

1. Klicka på **[!UICONTROL Save and Close]** överst till höger.

Om du vill aktivera din kontomålgrupp för Journey Optimizer B2B Edition måste du [lägga till den i en kontoresa](../journeys/journey-overview.md#add-the-account-audience-for-your-journey) och [publicera resan](../journeys/journey-overview.md).
