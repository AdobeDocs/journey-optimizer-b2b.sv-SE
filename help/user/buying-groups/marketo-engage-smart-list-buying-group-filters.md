---
title: Buying Group Filters in Market Engage
description: Läs om hur du använder medlemskap i inköpsgrupper för att definiera filter i Marketo Engage Smart Lists.
feature: Buying Groups, Integrations
role: User
exl-id: b137e787-808e-4d36-8e8b-a1c7b999f8a2
source-git-commit: 4a54548ad061fc778fae3bc4b8499f3716850e4a
workflow-type: tm+mt
source-wordcount: '394'
ht-degree: 0%

---

# Köpa gruppfilter i Market Engage

Som marknadsförare kanske ni vill inaktivera kampanjer i Marketo Engage för personer som ingår i inköpsgrupper i Journey Optimizer B2B edition. Du kan också informera arbetsflödena för poängsättning av leads i Marketo Engage med information om leads som är kopplade till inköpsgrupper. Exempel:

* Ingår denna lead i en inköpsgrupp?
* Är inköpsgruppen färdig och engagerad?

Om dessa villkor är uppfyllda kan du välja att poängsätta det högre. Annars kan du välja att inte markera det som ett marknadsföringsgodkänt lead (MQL).

I din Marketo Engage-instans som är ansluten till Journey Optimizer B2B edition kan du använda filtret _[!UICONTROL Member of Buying Group]_i dina smarta listor för att identifiera dessa leads enligt din kampanjstrategi.

1. När du har [skapat en smart lista i Marketo Engage](https://experienceleague.adobe.com/en/docs/marketo/using/product-docs/core-marketo-concepts/smart-lists-and-static-lists/creating-a-smart-list/create-a-smart-list){target="_blank"} öppnar du filterredigeraren på fliken **[!UICONTROL Smart List]** .

1. I filterlistan till höger rullar du nedåt i listan och expanderar mappen **[!UICONTROL Special Filters]**.

1. Klicka på filtret **[!UICONTROL Member of Buying Group]** och dra det till filterdefinitionsområdet.

   ![Lägg till medlemmen i filtret Buying Group i den smarta listan](./assets/me-member-of-buying-group-filter-add.png){width="700" zoomable="yes"}

1. Ställ in alternativet _[!UICONTROL Member of Buying Group]_på&#x200B;**[!UICONTROL true]**eller **[!UICONTROL false]**.

   Den här begränsningen krävs för definitionen.

1. (Valfritt) Lägg till andra inköpsgrupprelaterade begränsningar i filtret enligt hur du vill identifiera leads för den smarta listan.

   * Klicka på **[!UICONTROL Add Constraint]** längst upp till höger på filterkortet.

     ![Välj en annan begränsning](./assets/me-member-of-buying-group-filter-add-constraint.png){width="700" zoomable="yes"}

   * Välj den begränsning som du vill lägga till, till exempel _Slutförandepoäng_ eller _Lösningsintresse_.

   * Ange utvärderingen som du vill använda för en matchning. För poäng kan du använda en exakt matchning, eller ett intervall som är över eller under talet som du anger.

     För ett enskilt objekt, t.ex. de lösningsintressen som definieras i Journey Optimizer B2B edition, kan du välja ett eller flera alternativ för listan.

     ![Välj ett värde för begränsningen i listan](./assets/me-member-of-buying-group-filter-constraint-list.png){width="600" zoomable="yes"}

     Markera den första och klicka på väljaren igen för att öppna dialogrutan _[!UICONTROL Multiple Value Chooser]_.

     ![Välj flera värden för begränsningen](./assets/me-member-of-buying-group-filter-constraint-multiple-value.png){width="500" zoomable="yes"}

     Flytta över något av de återstående objekten till höger och klicka på **[!UICONTROL OK]** när du har en lista över objekt som du vill använda för begränsningen.

   * Upprepa dessa åtgärder om du vill lägga till så många av de begränsningar du behöver.

   ![Medlem i Buying Group-filter med flera begränsningar](./assets/me-member-of-buying-group-filter-constraints-complete.png){width="600" zoomable="yes"}
