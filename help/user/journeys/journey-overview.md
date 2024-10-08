---
title: Kontoresor
description: Lär dig mer om kontoresor och hur du kan skapa och hantera dem.
feature: Account Journeys
exl-id: 5c22f11f-1967-4b55-8aee-16371173c040
source-git-commit: 78d82aa8b3bb8b8d432eeb187d75e2354dbff3ee
workflow-type: tm+mt
source-wordcount: '1068'
ht-degree: 0%

---


# Kontoresor

Definiera säljdriven interaktion som inkluderar e-post, SMS och andra kundresor för att koordinera inkommande marknadsföring med utgående försäljningsaktiviteter för varje medlem i köpgruppen.

## Få åtkomst till och bläddra bland kontoresor

1. Klicka på Adobe Journey Optimizer B2B Edition på startsidan för Adobe Experience Platform.

1. Klicka på **[!UICONTROL Account journeys]** i den vänstra navigeringen.

   ![Åtkomstkontoresor](./assets/account-journey-browse.png){width="800" zoomable="yes"}

   Den visade resesidan innehåller följande kolumner:

   * [!UICONTROL Name] (klicka på namnet för att öppna kontoresan för redigering)
   * [!UICONTROL Status]
   * [!UICONTROL Description]
   * [!UICONTROL Created by]
   * [!UICONTROL Last updated at]
   * [!UICONTROL Last updated by]
   * [!UICONTROL Published on]
   * [!UICONTROL Published by]

Tabellen innehåller möjligheten att söka efter namn och skapad av. Sortering är inte tillgängligt just nu.

Du kan anpassa den visade tabellen genom att klicka på ikonen _Kolumner_ i det övre högra hörnet och markera eller avmarkera kryssrutorna.

![Välj de kolumner som ska visas i listan för kontoresor](./assets/account-journeys-list-columns.png){width="800" zoomable="yes"}

## Analys av en kontoresa

Klicka på namnet (visas som en länk) i listan _[!UICONTROL Account journeys]_om du vill granska informationen, göra ändringar och vidta åtgärder.

![Arbetsyta för kontoresa](./assets/account-journey-workspace.png){width="800" zoomable="yes"}

Redigeringsrubriken för varje kontoresa omfattar:

* Resensnamn
* Möjlighet att redigera namnet (_ikonen Redigera_)
* Status för resan

Följande åtgärder är tillgängliga i sidhuvudet:

* **Publish** - Du kan publicera en resa om det inte finns några blockeringsfel. När en resa publiceras ändras den till _Live_. Om resan innehåller fel tonas knappen ned med innehållsinformation: `Resolve errors before publishing`.
* **Duplicera** - Den här åtgärden liknar en klonfunktion, men den duplicerade resan innehåller inga resurser.
* **Nära nya poster** - Om du stänger en resa fortsätter konton som för närvarande befinner sig på resan att vara på vägen och ingen ytterligare reseentré kan ske. Det går inte att starta om en stängd resa. Du kan duplicera en stängd resa.
* **Avbryt** - Om du avbryter en resa avbryts kundens framsteg omedelbart om du gör en ny resa. Det går inte att starta om en stoppad resa. Om du blockerar nya ingångar utan att stoppa folks framsteg, överväg att stänga resan istället.
* **Ta bort** - Den här åtgärden tar bort resan permanent.

Status för en resa ändras baserat på de åtgärder som du tillämpar. Beroende på statusen för en resa är vissa åtgärder inte tillgängliga i sidhuvudet.

| Status | Beskrivning | Tillgängliga åtgärder |
| ------ | ----------- | ----------------- |
| _**Utkast**_ | En opublicerad resa som är redigerbar. | <ul><li>Publish</li><li>Duplicera </li><li>Ta bort </li></ul> |
| _**Live**_ | Resans status ändras från utkast till Live när en resa publiceras. I det här läget går det inte längre att redigera. | <ul><li>Duplicera </li><li>Stäng till nya poster </li><li>Avbryt </li></ul> |
| _**Stängda till nya poster**_ | Resursstatusen ändras från _Live_ till _Stängd till nya poster_ när du klickar på [!UICONTROL Close to new entries] i den övre navigeringen. | <ul><li>Duplicera </li><li>Avbryt </li></ul> |
| _**Avbruten**_ | Resans status ändras från _Live_ eller _Stängd till nya poster_ när du avbryter en resa. En avbruten resa kan inte startas om. | <ul><li>Duplicera </li><li>Ta bort </li></ul> |
| _**Slutförd**_ | När alla konton i en resa har slutfört resan ändras statusen från Live eller Stängd till nya poster till Slutförd. | <ul><li>Duplicera </li><li>Ta bort </li></ul> |

## Kom igång med en resa

Om du vill komma igång med en kontoresa skapar du resan och skapar sedan noderna och reseflödet i reseeditorn.

### Skapa en kontoresa

1. Klicka på **[!UICONTROL Account journeys]** i den vänstra navigeringen.

1. Klicka på **[!UICONTROL Create Account Journey]** överst till höger på sidan.

1. Ange en unik **[!UICONTROL Name]** (obligatoriskt) och **[!UICONTROL Description]** (valfritt) i dialogrutan.

   ![Dialogrutan Skapa kontoresa](./assets/account-journey-create-dialog.png){width="400"}

1. Klicka på **[!UICONTROL Create]**.

### Lägg till kontomålgruppen för din resa

En kontoresa börjar alltid med en kontomålgrupp där du kan lägga till information till din resa.

1. Klicka på noden **[!UICONTROL Account audience]** för att visa nodegenskaperna till höger.

   ![Nod för kontomålgrupp](./assets/account-journey-account-audience-node.png){width="700" zoomable="yes"}

1. Klicka på **[!UICONTROL Add account audience]**.

   Du kan markera ett målgruppssegment som tidigare har valts genom att klicka på _[!UICONTROL Add audiences]_.

1. Om du vill skapa ett nytt målgruppssegment väljer du **[!UICONTROL Account audiences]** i den vänstra navigeringen.

1. Klicka på **[!UICONTROL Create audience]** och följ stegen som beskrivs i [Segmenteringstjänstguiden](https://experienceleague.adobe.com/en/docs/experience-platform/segmentation/ui/account-audiences){target="_blank"}.

### Byggstenar i en resa

_Resans arbetsyta_ är den centrala zonen i resedesignern. Det är i den här zonen som du kan lägga till och konfigurera resenoder. Klicka på en nod för att öppna dess egenskapspanel till höger om arbetsytan och ange dem i enlighet med din design.

Du kan skapa din resa med någon av följande nodtyper:

* [Lyssna efter en händelse](journey-nodes.md#listen-for-an-event)
* [Agera](journey-nodes.md#take-an-action)
* [Dela banor](journey-nodes.md#split-paths)
* [Vänta](journey-nodes.md#wait)
* [Sammanfoga banor](journey-nodes.md#merge-paths)

### Vaktspår

För att hjälpa dig att bygga en resa utan att stöta på fel finns följande vaktskenor:

* _Tar bort en delad sökvägsnod_: Du kan inte ta bort en nod utan att ta bort alla efterföljande noder i varje sökväg.
* _Tar bort en sammanfogningsnod_: En sammanfogningsnod kan bara tas bort när det finns en ansluten sökväg. Om du vill ta bort en sammanfogningsnod låter du bara en sökväg vara markerad.
* _Växlar mellan konto och personer_: Du kan inte ändra urvalet från konton till personer utan att ta bort alla efterföljande noder i varje sökväg.

### Lägg till en nod

1. Navigera till reseeditorn.

1. Klicka på plusikonen ( **+** ) på sökvägen och välj nodtyp.

1. Ange nodegenskaperna till höger.

### Ta bort en nod

1. Navigera till reseeditorn.

1. Klicka på ikonen _Ta bort_ (kontrollkanna) i nodegenskaperna till höger.

1. Klicka på **[!UICONTROL Delete]** i konformationsdialogrutan.

### Lägga till och ta bort en bana

1. Navigera till reseeditorn.

1. Klicka på plusikonen ( **+** ) på sökvägen och lägg till noden för delad sökväg.

1. Välj **[!UICONTROL Account]** i nodegenskaperna till höger.

1. Klicka på **[!UICONTROL Add path]** om du vill lägga till fler sökvägar.

   För varje bana som skapas under resan visas ett nytt bankort i egenskaperna.

1. Navigera till en av sökvägarna i resan och lägg till en åtgärd- eller händelsenod i den här sökvägen med plusikonen .

1. Markera den delade sökvägsnoden för att öppna egenskaperna till höger.

   Observera att sökvägarna som innehåller noder inte kan tas bort.

1. Om du vill ta bort de här banorna måste du först ta bort alla noder på den banan.

### Schemalägg en resa

När du publicerar en resa kan den påbörjas omedelbart eller på ett schemalagt framtida datum. Slutdatumet kan vara högst tre år från startdatumet. När en resa har publicerats (_Live_ status) kan du uppdatera slutdatumet för resan, men inte startdatumet.

1. Navigera till reseeditorn.

1. Schemalägg din resa genom att klicka på [!UICONTROL Journey settings] i huvudet.

1. Ange schemaalternativen i dialogrutan:

   * Välj en schematyp.

     Om du vill aktivera resan vid publiceringstid väljer du **[!UICONTROL Immediately]**.

     Om du vill aktivera resan för ett framtida datum väljer du **[!UICONTROL On a specific date]** och klickar på ikonen _Kalender_ för att välja datumet.

     ![Dialogrutan Reseinställningar](./assets/account-journey-settings-dialog.png){width="400" zoomable="no"}

   * Ange **[!UICONTROL End date]** för resan. Det kan vara högst tre år från startdatumet (detta fält är obligatoriskt).

1. Klicka på **[!UICONTROL Save]**.

   När du är redo att publicera din resa kan du granska de här inställningarna när du klickar på _[!UICONTROL Publish]_.
