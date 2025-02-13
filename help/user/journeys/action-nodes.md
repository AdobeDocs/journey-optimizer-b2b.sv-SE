---
title: Gör något
description: Läs mer om nodtypen Ta en åtgärd som du kan använda för att samordna dina kontoresor i Journey Optimizer B2B edition.
feature: Account Journeys
exl-id: 167cb627-96ee-42a8-8657-bb8040bb4bfe
source-git-commit: d03e0e2d8070916d38bb956adff8dea3f3873aad
workflow-type: tm+mt
source-wordcount: '1045'
ht-degree: 0%

---

# Agera

Under din kontoresa kan du lägga till en _[!UICONTROL Take an action]_-nod för att utföra en åtgärd, som att skicka ett e-postmeddelande, ändra poängen, tilldela till en inköpsgrupp och så vidare. Åtgärder är vanligtvis vad du vill ska hända som ett resultat av någon typ av utlösare, till exempel en händelse eller en tidigare åtgärd.

![Video](../../assets/do-not-localize/icon-video.svg){width="30"} [Se översiktsvideon](#overview-video)

## Kontoåtgärder

Använd en åtgärd för konton när du vill använda en ändring för alla personer som är en del av konton på nodsökvägen.

### Åtgärder och begränsningar {#account-action-constraints}

| Åtgärd | Begränsningar |
| ------ | ----------- |
| [!UICONTROL Account Change Data Value] | Välj attribut<br/>Nytt värde |
| [!UICONTROL Account Interesting Moment] | Typ (e-post, milstolpe eller webb)<br/>Beskrivning (valfritt) |
| [!UICONTROL Add Account to (other) Journey] | Välj Live Account Journey |
| [!UICONTROL Add to account list] | Välj en lista med statiska Live-konton |
| [!UICONTROL Remove Account from Journey] | Välj Live Account Journey |
| [!UICONTROL Remove from account list] | Välj en lista med statiska Live-konton |
| [!UICONTROL Send Sales Alert] | Välj lösningsintresse<br/>Skicka e-post till |
| [!UICONTROL Update Buying Group Stage] | Välj lösningsintresse<br/>Välj inköpsgruppfas |
| [!UICONTROL Update Buying Group Status] | Välj lösningsintresse<br/>Status (krävs, max 50 tecken) |

### Lägg till en kontobaserad åtgärd

1. Navigera till reseeditorn.

1. Klicka på plusikonen ( **+** ) på en bana och välj **[!UICONTROL Take an action]**.

   ![Lägg till kundtjänstnod - utför en åtgärd](./assets/add-node-action.png){width="400"}

1. Välj **[!UICONTROL Accounts]** för åtgärden i nodegenskaperna till höger.

1. Välj en åtgärd i listan och ange värden för åtgärden.

   ![Resensnod - utför en åtgärd på ett konto](./assets/node-take-action-account.png){width="700" zoomable="yes"}

## Personåtgärder

Använd en åtgärd för personer när du vill använda en ändring för alla personer på nodsökvägen. Den här nodtypen kan användas i den delade sökvägen av personer eller dela upp sökvägen efter konton.

### Åtgärder och begränsningar {#people-action-constraints}

| Kontext | Åtgärd | Begränsningar |
| ------- | ------ | ----------- |
| [Journey Optimizer B2B](#journey-optimizer-b2b-actions) | [!UICONTROL Add to external customer audience] | Välj extern kundpublik |
| | [!UICONTROL Assign to Buying Group] | Välj lösningsintresse<br/>Välj roll |
| | [!UICONTROL Change Data Value] | Välj personattribut<br/>Ange nytt värde |
| | [!UICONTROL Change Score] | Poängnamn<br/>Förändring i poäng |
| | [!UICONTROL Person Interesting Moment] | Typ<br/>Beskrivning |
| | [!UICONTROL Remove from Buying Group] | Välj lösningsintresse |
| | [!UICONTROL Send email] | Skapa nytt e-postmeddelande<br/>Välj e-post från Marketo Engage |
| | [!UICONTROL Send SMS] | Skapa SMS |
| [Marketo Engage](#marketo-engage-actions) | [!UICONTROL Add to List] | Välj Marketo Engage-arbetsyta<br/>Listnamn |
| | [!UICONTROL Add to Marketo Engage Request campaign] | Välj Marketo Engage-arbetsyta<br/>Välj kampanj för begäran |
| | [!UICONTROL Change People Partition in Marketo Engage] | Ny partition |
| | [!UICONTROL Remove from List] | Välj Marketo Engage-arbetsyta<br/>Listnamn |

### Lägga till en personbaserad åtgärd

1. Navigera till reseeditorn.

1. Klicka på plusikonen ( **+** ) på en bana och välj **[!UICONTROL Take an action]**.

1. Välj **[!UICONTROL People]** för åtgärden i nodegenskaperna till höger.

1. Välj en åtgärd i listan och ange värden för åtgärden.

![Resensnod - utför en åtgärd på personer](./assets/node-take-action-people.png){width="700" zoomable="yes"}

### Journey Optimizer B2B-åtgärder

Journey Optimizer personbaserade B2B-åtgärder är utformade för att hantera kommunikation via de konfigurerade kanalerna och hantera personkategorisering inom era inköpsgrupper och konton. Resan utför åtgärden när ett kvalificerande konto med personprofiler når noden.

+++[!UICONTROL Add to external customer audience]

Använd den här åtgärden för att skicka människor till en extern publik som kan aktiveras i en betald mediekanal för att ytterligare rikta in er på köpgrupper. Den här åtgärden utförs via Real-Time CDP B2B/P Edition.

>[!NOTE]
>
>När ett kvalificerande konto med personprofiler når noden _Lägg till i den externa kundmålgruppen_ i en publicerad resa kan det ta upp till 48 timmar för dessa profiler att fylla i den externa målgruppen.

![Vidta en åtgärd - Lägg till för extern kundpublik](./assets/node-action-add-to-external-audience-options.png){width="300"}

När du väljer den här personbaserade åtgärden kan du skapa en ny extern målgrupp eller välja från en befintlig extern målgrupp. För befintliga målgrupper kan ni välja bland externa kundmålgrupper som bara har skapats i Journey Optimizer B2B edition. När du skapar en målgrupp och använder den för den här reseåtgärden måste du koppla målgruppen. Mer information finns i [Skapa en ny målanslutning](https://experienceleague.adobe.com/en/docs/experience-platform/destinations/ui/connect-destination){target="_blank"} och [Aktiveringsöversikt](https://experienceleague.adobe.com/en/docs/experience-platform/destinations/ui/activate/activation-overview#activate-audiences-from-the-destinations-catalog){target="_blank"} i Experience Platform-dokumentationen).

_Så här skapar du en extern målgrupp:_

1. Välj **[!UICONTROL Create new]**.

1. Klicka på **[!UICONTROL Create external customer audience]**.

1. Ange **[!UICONTROL Name]** (obligatoriskt) och **[!UICONTROL Description]** (valfritt) för den nya externa målgruppen.

   ![Lägg till för extern kundpublik - Skapa målgrupp](./assets/node-action-add-to-external-create-new.png){width="300"}

1. Klicka på **[!UICONTROL Create]**.

   Systemet skapar den nya målgruppen och visar ett bekräftelsemeddelande. Sedan kan du fortsätta att använda den som en befintlig målgrupp för nodåtgärden.

_Så här använder du en befintlig målgrupp:_

1. Klicka på **[!UICONTROL Select external customer audience]**.

1. Välj den målgrupp du vill använda i dialogrutan.

   ![Lägg till i extern kundpublik - Lägg till målgrupp](./assets/node-action-add-to-external-audience-select.png){width="700" zoomable="yes"}

1. Klicka på **[!UICONTROL Add audience]**.

+++

+++[!UICONTROL Assign to Buying Group]

Använd den här åtgärden om du vill lägga till personprofiler i en [inköpsgrupp](../buying-groups/buying-groups-overview.md) baserat på ett valt lösningsintresse och en vald roll.

![Vidta en åtgärd - Lägg till i inköpsgrupp](./assets/node-action-add-to-buying-group.png){width="300"}

+++

+++[!UICONTROL Change Data Value]

Använd den här åtgärden om du vill ändra värdet för ett [personprofilattribut](../data/field-mapping.md#xdm-business-person-attributes). Markera attributet och ange sedan det nya värdet.

![Vidta en åtgärd - Ändra datavärde](./assets/node-action-change-data-value.png){width="300"}

+++

+++[!UICONTROL Change Score]

Använd den här åtgärden om du vill ändra personpoängen i Marketo Engage. [Läs mer](https://experienceleague.adobe.com/en/docs/marketo-learn/tutorials/lead-and-data-management/lead-scoring-learn){target="_blank"}

![Vidta en åtgärd - Ändra poäng](./assets/node-action-change-score.png){width="300"}

+++

+++[!UICONTROL Person Interesting Moment]

Använd den här åtgärden för att logga en intressant stund för personprofiler. Välj en typ (E-post, Milstolpe eller Webb) och lägg till en beskrivning (valfritt).

![Vidta en åtgärd - Personens intressanta ögonblick](./assets/node-action-person-interesting-moment.png){width="300"}

+++

+++[!UICONTROL Remove from Buying Group]

Använd den här åtgärden om du vill ta bort personprofiler från en [inköpsgrupp](../buying-groups/buying-groups-overview.md) baserat på ett valt lösningsintresse.

![Vidta en åtgärd - Lägg till i inköpsgrupp](./assets/node-action-remove-from-buying-group.png){width="300"}

+++

+++[!UICONTROL Send email]

Använd den här åtgärden om du vill skicka ett e-postmeddelande. Du kan skapa, anpassa och förhandsgranska e-postmeddelanden i den visuella designern (se [Skapa e-post](../content/email-authoring.md)). Du kan också skicka ett [e-postmeddelande från Marketo Engage](https://experienceleague.adobe.com/en/docs/marketo/using/product-docs/email-marketing/general/creating-an-email/create-an-email){target="_blank"}. Markera arbetsytan i Marketo Engage och välj sedan det e-postmeddelande som du vill skicka.

![Vidta en åtgärd - Skicka e-post](./assets/node-action-send-email-from-marketo.png){width="300"}

+++

+++[!UICONTROL Send SMS]

Använd den här åtgärden om du vill skicka ett SMS-meddelande. Du kan skapa, anpassa och förhandsgranska SMS-meddelanden i den visuella designern (se [SMS-redigering](../content/sms-authoring.md)).

![Vidta en åtgärd - Skicka SMS](./assets/node-action-send-sms.png){width="300"}

+++

### Marketo Engage-åtgärder

Marketo Engage personbaserade marknadsföringsverktyg är utformade för att samordna er kontobaserade marknadsföring i Journey Optimizer B2B edition med era ledande marknadsföringssatsningar i Marketo Engage. Använd dessa åtgärder för att samordna listmedlemskap, personpartitioner och begära kampanjer.

+++[!UICONTROL Add to list]

Använd den här åtgärden om du vill ta bort personer från en [smart lista](https://experienceleague.adobe.com/en/docs/marketo/using/product-docs/core-marketo-concepts/smart-lists-and-static-lists/understanding-smart-lists){target="_blank"} i Marketo Engage.

Markera först arbetsytan i den anslutna Marketo Engage-instansen. Välj sedan listnamnet.

![Vidta en åtgärd - Lägg till i listan](./assets/node-action-add-to-list-options.png){width="300"}

+++

+++[!UICONTROL Add to Marketo Request campaign]

Använd den här åtgärden om du vill lägga till personprofiler i en [begärankampanj](https://experienceleague.adobe.com/en/docs/marketo/using/product-docs/core-marketo-concepts/smart-campaigns/flow-actions/request-campaign){target="_blank"} i Marketo Engage.

Markera först arbetsytan i den anslutna Marketo Engage-instansen. Välj sedan kampanjnamnet för begäran.

![Vidta en åtgärd - Lägg till i Marketo Request-kampanj](./assets/node-action-add-to-request-campaign-options.png){width="300"}

+++

+++[!UICONTROL Change people partition in Marketo Engage]

Använd den här åtgärden om du vill ändra [personpartitionen](https://experienceleague.adobe.com/en/docs/marketo/using/product-docs/administration/workspaces-and-person-partitions/understanding-workspaces-and-person-partitions#person-partitions){target="_blank"} i Marketo Engage.

![Vidta en åtgärd - Ändra personpartition i Marketo Engage](./assets/node-action-change-people-partition-options.png){width="300"}

+++

+++[!UICONTROL Remove from list]

Använd den här åtgärden om du vill ta bort personer från en [smart lista](https://experienceleague.adobe.com/en/docs/marketo/using/product-docs/core-marketo-concepts/smart-lists-and-static-lists/understanding-smart-lists){target="_blank"} i Marketo Engage. Markera först arbetsytan i den anslutna Marketo Engage-instansen. Välj sedan listnamnet.

![Vidta en åtgärd - Ta bort från listan](./assets/node-action-remove-from-list-options.png){width="300"}

Om personprofilen inte var medlem i den smarta listan ignoreras åtgärden.

+++

## Videoöversikt

>[!VIDEO](https://video.tv.adobe.com/v/3443207/?learn=on)