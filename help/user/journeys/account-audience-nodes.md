---
title: Målgruppsnoder för konto
description: Lär dig mer om vilken typ av kontomålsnod du kan använda för att definiera indata för kontoresor i Journey Optimizer B2B edition.
feature: Account Journeys, Audiences, Account Lists
role: User
exl-id: 288ac5a8-79ed-4654-8ac1-83da2af04f2c
source-git-commit: 4a54548ad061fc778fae3bc4b8499f3716850e4a
workflow-type: tm+mt
source-wordcount: '254'
ht-degree: 0%

---

# Nod för kundresa

Noden Account publice definierar indatakontona för resan. När du [skapar en kontoresa](./journey-overview.md#create-an-account-journey) börjar den alltid med en _målgruppsnod_ som definierar resans indata.

Det finns två typer av indata som du kan använda för den här noden:

* **[Kontomålgrupp](../audiences/account-audience-overview.md)** - Det här är den grundläggande målgruppen som synkroniseras från Experience Platform segmenteringstjänst.
* **[Kontolista](../accounts/account-lists.md)** - Det här är en samling namngivna konton som du kan använda för riktad resesamordning. En kontolista har som mål att namnge konton enligt definierade kriterier, t.ex. bransch, plats eller storlek för företaget.

_Så här anger du målgrupp för noden:_

1. Klicka på noden **[!UICONTROL Account audience]** för att visa nodegenskaperna till höger.

   ![Nod för kontomålgrupp](./assets/account-journey-account-audience-node.png){width="700" zoomable="yes"}

1. Välj indatatyp för konton som ska registrera resan:

   * **[!UICONTROL Account audience]**

     Välj den här typen och klicka sedan på **[!UICONTROL Add account audience]**.

     I dialogrutan _[!UICONTROL Add audience]_&#x200B;väljer du ett målgruppssegment som tidigare skapats och klickar på&#x200B;**[!UICONTROL Add audience]**.

     ![Välj ett målgruppssegment för noden](./assets/node-audience-add-dialog.png){width="700" zoomable="yes"}

   * **[!UICONTROL Account list]**

     Välj den här typen och klicka sedan på **[!UICONTROL Add account list]**.

     I dialogrutan _[!UICONTROL Select live account list]_&#x200B;väljer du en kontolista som tidigare har publicerats och klickar på&#x200B;**[!UICONTROL Save]**.

     ![Välj en Live-kontolista för noden](./assets/account-journey-account-audience-select-account-list.png){width="700" zoomable="yes"}

     Gå till [Kontolistor](../accounts/account-lists.md) om du vill ha mer information om hur du skapar och publicerar kontolistor.

_Så här skapar du ett målgruppssegment:_

1. Välj **[!UICONTROL Accounts]** > **[!UICONTROL Audiences]** i den vänstra navigeringen.

1. Klicka på **[!UICONTROL Create audience]** överst till höger.

   ![Skapa ett målgruppssegment](./assets/audiences-list-create.png){width="800" zoomable="yes"}

1. Följ stegen som beskrivs i [Segmenteringstjänstguiden](https://experienceleague.adobe.com/en/docs/experience-platform/segmentation/ui/account-audiences){target="_blank"}.
