---
title: Målgrupper
description: Läs mer om kontomålgrupper och hur de möjliggör kontobaserade resor.
exl-id: f9ba690f-bab2-4c31-9000-f0be1342c8b3
source-git-commit: 9031191ead88652df95137a122f379b0ae2516a7
workflow-type: tm+mt
source-wordcount: '537'
ht-degree: 0%

---

# Kontomålgrupper

En målgrupp är en uppsättning personer som har liknande beteenden och/eller egenskaper. Journey Optimizer B2B edition använder de kontosegmenteringsfunktioner som finns i Adobe Real-Time Customer Data Platform B2B- och B2P-utgåvor. Med kontosegmentering kan användarna generera kontomgrupper genom att utnyttja data från alla B2B-enheter i systemet. Dessa målgrupper fungerar som indata för kontoresor med Journey Optimizer B2B edition, vilket underlättar smidig aktivering och personalisering.

Läs mer om kontomålgrupper och hur du definierar dem i [Adobe Experience Platform Segmentation Service-dokumentationen](https://experienceleague.adobe.com/en/docs/experience-platform/segmentation/types/account-audiences){target="_blank"}.

## Arbetsflöde för målgrupp

Du kan tänka dig Journey Optimizer B2B edition som ett Experience Platform-mål (AEP) som inte visas i målkatalogen. Aktivera kontomålgrupper för Journey Optimizer B2B edition med följande steg:

1. Skapa scheman för dina data i AEP.
1. Lägg in data i AEP.
1. Skapa ett kontosegment för att utvärdera dina data.
1. Aktivera utvärderade data för Journey Optimizer B2B edition.

I Journey Optimizer B2B edition används kontomålgrupper som indata för kontobaserade resor, så att ni kan inrikta er på personer på dessa konton. Du kan t.ex. använda kontomålgrupper för att hämta poster för alla konton som inte har kontaktinformation för någon med titeln Chief Operating Officer (COO) eller Chief Marketing Officer (CMO).

Med Journey Optimizer B2B edition kan ni skapa Adobe Experience Platform (AEP)-kontomålgrupper direkt från den vänstra navigeringen och införliva dem i era kontoresor.

![Åtkomst till målgrupper på konton](./assets/account-audiences-browse.png){width="800" zoomable="yes"}

## Skapa en kontopublik

Definiera målgruppen genom att skapa en kontosegmentering. Du kan skapa kontosegmenteringen direkt i Journey Optimizer B2B edition-programmet eller så kan du använda [segmenteringsgränssnittet för segmentbyggaren](https://experienceleague.adobe.com/en/docs/experience-platform/segmentation/ui/segment-builder){target="_blank"}. Här nedan beskrivs de steg du kan använda för att skapa en kontosegmentering i Journey Optimizer B2B edition.

1. Välj **[!UICONTROL Accounts]** > **[!UICONTROL Audiences]** i den vänstra navigeringen.

1. Klicka på **[!UICONTROL Create audience]** överst till höger.

1. Skapa segmentdefinitionen.

   Kontoattributen och målgrupperna visas i det vänstra navigeringsfältet. På fliken _[!UICONTROL Attributes]_&#x200B;kan du lägga till både plattformsskapade och anpassade attribut. Dra varje attribut för att skapa logiken för segmentet.

   >[!TIP]
   >
   >När du skapar en kontopublik ska du vara medveten om att händelser listas under _[!UICONTROL People]_&#x200B;eftersom dessa attribut är kopplade till personer.<br/>
   >
   >Under fliken _[!UICONTROL Audiences]_&#x200B;kan du lägga till tidigare skapade personbaserade målgrupper som du kan bygga vidare på när du skapar en egen målgrupp.

   I följande exempel definieras målgrupper som skapats med `Country Code`, `Revenue Amount` och `Market segment`. Frågan på engelska skulle vara:&quot;Jag vill ha alla konton i USA som finns i finanssegmentet vars intäkter överstiger 1 miljon dollar.&quot;

   ![exempel på segmentbyggare för kontomublik](./assets/audience-segment-builder-US-finance-1M.png){width="700" zoomable="yes"}
   <br/>

   >[!IMPORTANT]
   >
   >Attributet `Account Name` för kontoposter måste innehålla ett värde som ska inkluderas i kontoresor. Om det här attributet är tomt (null) är kontoposten uteslutits.<br/>
   >Om du vill vara säker på att endast konton med ett kontonamn som inte är tomt inkluderas lägger du till attributet **[!UICONTROL Account Name]** och väljer _[!UICONTROL exists]_&#x200B;som matchningsvillkor.<br/>
   >![Attributet för kontonamn finns](./assets/audience-segment-builder-account-name-exists.png){width="600"}
   ><br/>Om du använder ett anpassat attribut för kontonamnet använder du ditt anpassade attributnamn i stället för _[!UICONTROL Account Name]_.

1. Klicka på **[!UICONTROL Save and Close]** överst till höger.

Om du vill aktivera din kontomålgrupp för Journey Optimizer B2B edition måste du [lägga till den i en kontoresa](../journeys/journey-overview.md#add-the-account-audience-for-your-journey) och [publicera resan](../journeys/journey-overview.md).
