---
title: Målgruppsnoder för konto
description: Lär dig mer om vilken typ av kontomålsnod du kan använda för att definiera indata för kontoresor i Journey Optimizer B2B edition.
feature: Account Journeys, Audiences, Account Lists
role: User
exl-id: 288ac5a8-79ed-4654-8ac1-83da2af04f2c
source-git-commit: 775c283e63192ee7252330fac9086b5da8160b9f
workflow-type: tm+mt
source-wordcount: '242'
ht-degree: 0%

---


# Nod för kundresa

Kontots målgruppsnod anger vilka konton som anger resan. När du [skapar en kontoresa](./journey-overview.md#create-an-account-journey) börjar resan alltid med en kontomålsnod som definierar dess indata.

Använd något av följande indataalternativ för den här kundnoden:

* **[Kontomålgrupp](../audiences/account-audience-overview.md)** - Kontomålgruppen representerar den grundläggande målgrupp som synkroniseras med Experience Platform segmenteringstjänst.
* **[Kontolista](../accounts/account-lists.md)** - Kontolistan är en samling namngivna konton som du använder för målanpassad resesamordning. En kontolista har mål för namngivna konton med hjälp av definierade kriterier, som bransch, plats eller företagsstorlek.

## Ange målgrupp för kontomålsnoden

1. Klicka på noden **[!UICONTROL Account audience]**. Den här åtgärden visar nodegenskaperna till höger.

   ![Nod för kundresa](./assets/account-journey-account-audience-node.png){width="700" zoomable="yes"}

1. Välj indatatyp för konton som anger resan:

   * **[!UICONTROL Account audience]**

     Välj alternativ för målgrupp. Klicka sedan på **[!UICONTROL Add account audience]**.

     I dialogrutan _[!UICONTROL Add audience]_&#x200B;väljer du ett tidigare skapat målgruppssegment. Klicka sedan på&#x200B;**[!UICONTROL Add audience]**.

     ![Välj ett målgruppssegment för noden](./assets/node-audience-add-dialog.png){width="700" zoomable="yes"}

   * **[!UICONTROL Account list]**

     Välj alternativet för kontolistan. Klicka på **[!UICONTROL Add account list]**.

     Välj en publicerad kontolista i dialogrutan _[!UICONTROL Select live account list]_. Klicka sedan på&#x200B;**[!UICONTROL Save]**.

     ![Välj en Live-kontolista för noden](./assets/account-journey-account-audience-select-account-list.png){width="700" zoomable="yes"}

     Mer information om hur du skapar och publicerar kontolistor finns i [Kontolistor](../accounts/account-lists.md).

## Skapa ett publiksegment

1. Välj **[!UICONTROL Accounts]** > **[!UICONTROL Audiences]** i den vänstra navigeringen.

1. Klicka på **[!UICONTROL Create audience]** i det övre högra hörnet.

   ![Skapa ett målgruppssegment](./assets/audiences-list-create.png){width="800" zoomable="yes"}

1. Följ stegen i [Segmenteringstjänstguiden](https://experienceleague.adobe.com/en/docs/experience-platform/segmentation/types/account-audiences){target="_blank"}.
