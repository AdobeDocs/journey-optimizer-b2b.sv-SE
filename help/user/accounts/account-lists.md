---
title: Kontolistor
description: Skapa statiska och dynamiska kontolistor med anpassade filter för riktad resesamordning och kontobaserad marknadsföring i Journey Optimizer B2B edition.
feature: Account Lists
role: User
exl-id: 7d7f5612-f0fe-4bb8-ae16-29aa3552f0f9
source-git-commit: 937101d6570a8217ff11037822c414350c6026ae
workflow-type: tm+mt
source-wordcount: '1273'
ht-degree: 0%

---

# Kontolistor

I Journey Optimizer B2B edition är en kontolista en samling namngivna konton som marknadsförare kan använda för riktad resesamordning. En kontolista kan ha namngivna konton som mål enligt dina definierade kriterier, t.ex. bransch, plats eller företagets storlek. Det finns två typer av kontolistor:

* **Statisk** - Med en statisk kontolista ändras listan bara när du lägger till kontona. Du kan lägga till konton manuellt genom att använda en filteruppsättning för att fylla i listan baserat på aktuella kontodata eller lägga till och ta bort konton under en kontoresa.
* **Dynamisk** - Med en dynamisk kontolista definierar du en filteruppsättning som automatiskt väljer listan. Systemet använder den här filteruppsättningen för att lägga till och ta bort konton efter ändringar i kontoinformationen. Den här listhanteringen liknar [målgruppssegmentering i kunddataplattformen &#x200B;](https://experienceleague.adobe.com/sv/docs/experience-platform/rtcdp/segmentation/b2b){target="_blank"} i realtid.

När en kontolista är i läget _Live_ (publicerad) är den tillgänglig för [användning i kontoresor och Marketo Engage-program](./account-lists-journeys.md).

![Video](../../assets/do-not-localize/icon-video.svg){width="30"} [Se videoöversikten](#overview-video)

>[!NOTE]
>
>Kontolistor använder kontodata från Marketo Engage för att skapa kontosegment och listor. Det innebär att om ett kontosegment från Adobe Experience Platform inte är aktivt synkroniserat till Marketo Engage är konton i det Experience Platform-segmentet kanske inte tillgängliga i Journey Optimizer B2B edition-kontolistor. Därefter inkluderas endast personer från konton i Experience Platform-segment som synkroniseras med Marketo Engage i antalet personliga medlemskap och utlösande händelser.

## Få åtkomst till och bläddra bland kontolistor

Expandera **[!UICONTROL Accounts]** till vänster och klicka på **[!UICONTROL Account lists]**.

![Åtkomstkontoresor](./assets/account-lists-browse.png){width="800" zoomable="yes"}

Sidan _[!UICONTROL Account lists]_&#x200B;som visas innehåller följande kolumner:

* [!UICONTROL Name] (klicka på namnet på kontolistan för att visa information)
* [!UICONTROL Status]
* [!UICONTROL Type]
* [!UICONTROL Last updated on]
* [!UICONTROL Last updated by]
* [!UICONTROL Creation date]
* [!UICONTROL Created by]

Tabellen innehåller möjligheten att söka efter namn. Sorteringsfunktionen är inte tillgänglig just nu.

Du kan anpassa den visade tabellen genom att klicka på ikonen _Kolumninställningar_ ( ![Kolumninställningar](../assets/do-not-localize/icon-column-settings.svg) ) i det övre högra hörnet och markera eller avmarkera kryssrutorna.

![Välj de kolumner som ska visas i listan för kontoresor](./assets/account-lists-list-columns.png){width="300"}

Om du vill visa beskrivningen för en kontolista klickar du på ikonen _Information_ ( ![Informationsikon](../assets/do-not-localize/icon-info.svg) ) bredvid namnet.

## Skapa en kontolista

När du skapar en kontolista definierar du en uppsättning filter för att generera listan. Du kan till exempel använda den för att skapa en lista över konton där hälso- och sjukvården är och där intäkterna är över 100 miljoner dollar.

1. Klicka på _[!UICONTROL Account lists]_&#x200B;längst upp till höger på sidan **[!UICONTROL Create account list]**.

   ![Klicka på Skapa kontolista](./assets/account-lists-create.png){width="700" zoomable="yes"}

1. I dialogrutan _[!UICONTROL Create account list]_&#x200B;anger du en unik **[!UICONTROL Name]**(obligatoriskt) och en **[!UICONTROL Description]**(valfritt).

1. Välj _[!UICONTROL Type]_&#x200B;för kontolistan,**[!UICONTROL Static]**&#x200B;eller **[!UICONTROL Dynamic]**.

   ![Välj Statisk eller Dynamisk för kontolistan](./assets/account-list-create-dialog.png){width="380"}

1. Klicka på **[!UICONTROL Create]**.

   En ny statisk kontolista öppnas med en tom lista över konton. En ny dynamisk kontolista öppnas med panelen _[!UICONTROL Add accounts by filter]_&#x200B;på sidan.

## Lägg till konton i kontolistan

För en statisk lista kan du fortsätta att publicera den tomma kontolistan och lägga till konton genom en kontoresa. Du kan också lägga till konton manuellt genom att tillämpa en filteruppsättning innan du publicerar den.

För en dynamisk kontolista måste du lägga till den filteruppsättning som du vill använda för att hantera listan automatiskt innan du publicerar den.

>[!BEGINTABS]

>[!TAB Statisk kontolista]

När du har skapat den statiska kontolistan kan du fylla i listan genom att använda en filteruppsättning. Du kan också använda en filteruppsättning för att lägga till konton i en statisk kontolista efter att den har publicerats (_Live_).

>[!NOTE]
>
>Om du vill att kontolistan ska börja som tom väljer du inga filter och publicerar bara kontolistan. Det är användbart att börja med en tom lista när du tänker lägga till medlemmar via en kontoresa (se [Ta en åtgärdsnod - Lägg till i konto](#take-an-action-node---add-to-account)).

1. CLick **[!UICONTROL Add accounts]**.

   ![Lägg till ett kontofilter för att fylla i listan &#x200B;](./assets/account-lists-static-new-add-accounts.png){width="700" zoomable="yes"}

   Du kan öppna den här funktionen på den tomma listsidan eller i det övre högra hörnet.

1. I dialogrutan _[!UICONTROL Add accounts by filter]_&#x200B;använder du menyn **[!UICONTROL Account Filters]**&#x200B;för att lägga till de attribut och aktiviteter som du vill använda för att skapa filteruppsättningen:

   Filtren kapslas in i kategorimappar. Du kan expandera varje mapp och bläddra igenom listan med tillgängliga filter. Du kan också använda _sökverktyget_ längst upp för att hitta det filter du behöver.

   * Dra och släpp filtret från den vänstra menyn till filterdefinitionsrymden.
   * Slutför definitionen av matchningsutvärderingen.
   * Upprepa dessa åtgärder för varje filter som du vill inkludera.

     ![Lägg till filter för att fylla i kontolistan &#x200B;](./assets/account-lists-static-add-accounts-by-filters.png){width="700" zoomable="yes"}

   * Du kan finjustera dina villkor genom att använda **[!UICONTROL Filter logic]** högst upp. Du kan välja att matcha alla attributvillkor eller alla villkor.

     ![Filterlogik för kontolista](./assets/account-lists-filter-logic.png){width="450"}

1. När filteruppsättningen och logiken är klara klickar du på **[!UICONTROL Populate accounts]**.

   Ifyllningsprocessen kan ta en stund, beroende på antalet konton som ska utvärderas och fyllas i (storleken på databasen och filtervillkoren som du har valt). Det kan ta upp till två timmar för konton att fylla i din lista.

Du kan fortsätta att publicera listan så att den blir tillgänglig för att lägga till och ta bort åtgärder i en kontoresa.

>[!TAB Dynamisk kontolista]

När du har skapat en dynamisk kontolista definierar du den filteruppsättning som används för att hantera listan (lägga till/ta bort konton) när den är _Live_ (publicerad). Du kan inte lägga till/ta bort konton via kontoresor, men en publicerad dynamisk kontolista är tillgänglig för målnoden för det inledande kontot.

1. Klicka på **[!UICONTROL Select filters]**.

   ![Välj filter som används för att fylla i listan dynamiskt &#x200B;](./assets/account-lists-dynamic-new-select-filters.png){width="700" zoomable="yes"}

1. I dialogrutan _[!UICONTROL Add accounts by filter]_&#x200B;använder du menyn **[!UICONTROL Account Filters]**&#x200B;för att lägga till de attribut och specialfilter som du vill använda för att skapa filteruppsättningen:

   Filtren kapslas in i kategorimappar. Du kan expandera varje mapp och bläddra igenom listan med tillgängliga filter. Du kan också använda _sökverktyget_ längst upp för att hitta det filter du behöver.

   * Dra och släpp filtret från den vänstra menyn till filterdefinitionsrymden.
   * Slutför definitionen av matchningsutvärderingen.
   * Upprepa dessa åtgärder för varje filter som du vill inkludera.

     ![Lägg till filter för att fylla i kontolistan &#x200B;](./assets/account-lists-dynamic-add-accounts-by-filters.png){width="700" zoomable="yes"}

   * Du kan finjustera dina villkor genom att använda **[!UICONTROL Filter logic]** högst upp. Du kan välja att matcha alla attributvillkor eller alla villkor.

     ![Filterlogik för kontolista](./assets/account-lists-filter-logic.png){width="450"}

1. När filteruppsättningen och logiken är klara klickar du på **[!UICONTROL Done]**.

   Om du är nöjd med filteruppsättningen kan du fortsätta att [publicera listan](#publish-an-account-list) så att den blir tillgänglig för den inledande [målgruppsnoden](#account-audience-node) i en kontoresa.

   >[!NOTE]
   >
   >Du kan inte uppdatera filtren för en dynamisk kontolista efter att listan har publicerats.

   Ifyllningsprocessen kan ta en stund, beroende på antalet konton som ska utvärderas och fyllas i (storleken på databasen och filtervillkoren som du har valt). Det kan ta upp till två timmar för konton att fylla i din lista.

>[!ENDTABS]

## Publicera en kontolista

Du kan publicera en kontolista så snart filteruppsättningen är klar.

>[!BEGINTABS]

>[!TAB Statisk kontolista]

1. Klicka på **[!UICONTROL Publish]** överst till höger.

   ![Klicka på Publicera överst till höger](./assets/account-lists-static-publish.png){width="700" zoomable="yes"}

1. Bekräfta genom att klicka på _[!UICONTROL Publish static account list]_&#x200B;i dialogrutan **[!UICONTROL Publish]**.

   ![Bekräfta publicering för en statisk kontolista](./assets/account-lists-static-publish-confirm.png){width="400"}

Statusen för den statiska kontolistan ändras till _[!UICONTROL Live]_&#x200B;och är tillgänglig för [användning i en kontoresa](#account-list-usage-in-account-journeys).

>[!TAB Dynamisk kontolista]

Du kan publicera en dynamisk kontolista så snart filteruppsättningen är klar. När kontolistan har statusen Live kan du välja den i en kundkundkundresa.

1. Klicka på **[!UICONTROL Publish]** överst till höger.

   ![Klicka på Publicera överst till höger](./assets/account-lists-dynamic-publish.png){width="700" zoomable="yes"}

1. Bekräfta genom att klicka på _[!UICONTROL Publish dynamic account list]_&#x200B;i dialogrutan **[!UICONTROL Publish]**.

   ![Bekräfta publicering för en dynamisk kontolista](./assets/account-lists-dynamic-publish-confirm.png){width="400"}

Status för den dynamiska kontolistan ändras till _[!UICONTROL Live]_&#x200B;och är tillgänglig för [användning i en kontoresa](#account-list-usage-in-account-journeys).

>[!ENDTABS]

## Videoöversikt

>[!VIDEO](https://video.tv.adobe.com/v/3448653/?learn=on&captions=swe)
