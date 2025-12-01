---
title: Gör något
description: Konfigurera åtgärdsnoder för konto- och personåtgärder - skicka e-post, uppdatera inköpsgrupper, ändra poäng och integrera med Marketo Engage i Journey Optimizer B2B edition.
feature: Account Journeys
role: User
exl-id: 167cb627-96ee-42a8-8657-bb8040bb4bfe
source-git-commit: ab6629f97231ecde67dcc38d3fcb815b29eb5e37
workflow-type: tm+mt
source-wordcount: '1514'
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
| [!UICONTROL Account Interesting Moment] | Typ (e-post, milstolpe eller webb)<br/>Beskrivning (valfritt) |
| [!UICONTROL Activate to destination] | Välj ett mål |
| [!UICONTROL Add Account to (other) Journey] | Välj Live-kontoresa |
| [!UICONTROL Add to account list] | Välj lista med aktiva statiska konton |
| [!UICONTROL Remove Account from Journey] | Välj Live-kontoresa |
| [!UICONTROL Remove from account list] | Välj en lista med statiska Live-konton |
| [!UICONTROL Send Sales Alert] | Välj lösningsintresse<br/>Skicka e-post till |
| [!UICONTROL Update account profile] | Välj attribut<br/>Nytt värde |
| [!UICONTROL Update Buying Group Stage] | Välj lösningsintresse<br/>Välj inköpsgruppfas |
| [!UICONTROL Update Buying Group Status] | Välj lösningsintresse<br/>Status (krävs, max 50 tecken) |

>[!NOTE]
>
>Åtgärden _[!UICONTROL Account Change Data Value]_&#x200B;har tagits bort för version 2025.10. Den ersätts med&#x200B;_[!UICONTROL Update account profile]_ för den [förenklade arkitekturen](../simplified-architecture.md).<br/>
>
>En administratör kan konfigurera tillgängliga attribut för XDM Business Account genom att uppdatera fälten i _[!UICONTROL XDM Classes]_>_[!UICONTROL Standard classes]_. Mer information finns i [Standardklasser](../admin/xdm-field-management.md#standard-classes).

### Lägg till en kontobaserad åtgärd

1. Navigera till resekartan.

1. Klicka på plusikonen ( **+** ) på en bana och välj **[!UICONTROL Take an action]**.

   ![Lägg till kundtjänstnod - utför en åtgärd](./assets/add-node-action.png){width="400"}

1. Välj **[!UICONTROL Accounts]** för åtgärden i nodegenskaperna till höger.

1. Välj en åtgärd i listan och ange värden för åtgärden.

   ![Resensnod - utför en åtgärd på ett konto](./assets/node-take-action-account.png){width="700" zoomable="yes"}

>[!BEGINSHADEBOX]

### Aktivera till ett LinkedIn-mål

Använd åtgärden _Aktivera till mål_ för konton om du vill aktivera konton till Experience Platform-mål direkt från din resa. Med den här åtgärden kan ni överföra kvalificerade konton (baserat på inköpsgruppfilter, engagemangspoäng och andra kriterier) till matchande målgrupper på de destinationer som stöds. Den

Från och med version 2025.10 är **_LinkedIn_** den första måltypen som stöds. Använd åtgärden för ett LinkedIn-mål för att effektivisera kampanjkörningen genom att eliminera överlämningar i flera system och minska latensen. Som marknadsförare kan du till exempel automatiskt aktivera återannonsering med hög återgivning av konton till LinkedIn när nyckelinköpsroller saknas, eller återaktivera vilande konton baserat på inaktivitetsfilter.

Mer information om hur du använder kontomatchade målgrupper för ett LinkedIn-mål finns i [Matchade målgrupper för LinkedIn-konto](../data/linkedin-account-matched-audiences.md).

+++ Ange aktivering av konton för en LinkedIn-destination

1. Med noden _Vidta en åtgärd_ markerad på arbetsytan för resan ställer du in **[!UICONTROL Action on accounts]** på **[!UICONTROL Activate to destination]**.

1. Klicka på **[!UICONTROL Select destination]**.

   ![Resensnod - utför en åtgärd på konton - aktivera till mål](./assets/node-activate-destination-select-destination.png){width="600" zoomable="yes"}

1. I dialogrutan väljer du det konfigurerade LinkedIn-målet och klickar på **[!UICONTROL Save]**.

![Resensnod - utför en åtgärd på konton - aktivera till mål - välj måldialogruta](./assets/node-activate-destination-select-destination-dialog.png){width="700" zoomable="yes"}

1. Ange **[!UICONTROL Audience name]** som används för att identifiera den aktiverade målgruppen i målet.

   ![Resensnod - utför en åtgärd på konton - aktivera till mål - slutförda inställningar](./assets/node-activate-destination-settings.png){width="550" zoomable="yes"}

+++

>[!ENDSHADEBOX]

## Personåtgärder

Använd en åtgärd för personer när du vill använda en ändring för alla personer på nodsökvägen. Den här nodtypen kan användas i den delade sökvägen av personer eller dela upp sökvägen efter konton.

### Åtgärder och begränsningar {#people-action-constraints}

| Kontext | Åtgärd | Begränsningar |
| ------- | ------ | ----------- |
| [Journey Optimizer B2B](#journey-optimizer-b2b-actions) | [!UICONTROL Add to external customer audience] | Välj extern kundpublik |
| | [!UICONTROL Assign to Buying Group] | Välj lösningsintresse<br/>Välj roll |
| | [!UICONTROL Change Score] | Poängnamn<br/>Förändring i poäng |
| | [!UICONTROL Person Interesting Moment] | Typ<br/>Beskrivning |
| | [!UICONTROL Remove from Buying Group] | Välj lösningsintresse |
| | [!UICONTROL Send email] | Skapa nytt e-postmeddelande<br/>Välj e-post från Marketo Engage |
| | [!UICONTROL Send SMS] | Skapa SMS |
| | [!UICONTROL Update person profile] | Välj personattribut<br/>Ange nytt värde |
| [Marketo Engage](#marketo-engage-actions) | [!UICONTROL Add to Marketo Engage Request campaign] | Välj Marketo Engage-arbetsyta<br/>Välj kampanj för begäran |
| | [!UICONTROL Add to Marketo list] | Ange namnet på den externa Marketo-anslutningen <br/>Listnamn |
| | [!UICONTROL Remove from Marketo list] | Ange namnet på den externa Marketo-anslutningen <br/>Listnamn |

>[!NOTE]
>
>Åtgärden _[!UICONTROL Change People Partition in Marketo Engage]_&#x200B;är föråldrad för version 2025.10 och är inte tillgänglig för den [förenklade arkitekturen](../simplified-architecture.md) för Journey Optimizer B2B edition.<br/>
>
>Åtgärden _[!UICONTROL Change Data Value]_&#x200B;har tagits bort för version 2025.10. Den ersätts med&#x200B;_[!UICONTROL Update person profile]_ på den förenklade arkitekturen.

### Lägga till en personbaserad åtgärd

1. Navigera till resekartan.

1. Klicka på plusikonen ( **+** ) på en bana och välj **[!UICONTROL Take an action]**.

1. Välj **[!UICONTROL People]** för åtgärden i nodegenskaperna till höger.

1. Välj en åtgärd i listan och ange värden för åtgärden.

![Resensnod - utför en åtgärd på personer](./assets/node-take-action-people.png){width="700" zoomable="yes"}

### Journey Optimizer B2B-åtgärder

Journey Optimizer personbaserade B2B-åtgärder är utformade för att hantera kommunikation via de konfigurerade kanalerna och hantera personkategorisering inom era inköpsgrupper och konton. Resan utför åtgärden när ett kvalificerande konto med personprofiler når noden.

+++[!UICONTROL Add to external customer audience]

Använd den här åtgärden för att skicka människor till en extern publik som kan aktiveras i en betald mediekanal för att ytterligare rikta in er på köpgrupper. Den här åtgärden utförs via Real-Time CDP B2B edition.

>[!NOTE]
>
>När ett kvalificerande konto med personprofiler når noden _Lägg till i den externa kundmålgruppen_ i en publicerad resa kan det ta upp till 48 timmar för dessa profiler att fylla i den externa målgruppen.

![Vidta en åtgärd - Lägg till för extern kundpublik](./assets/node-action-add-to-external-audience-options.png){width="300"}

När du väljer den här personbaserade åtgärden kan du skapa en ny extern målgrupp eller välja från listan med befintliga externa målgrupper.

* För befintliga målgrupper kan du välja bland externa kundmålgrupper som bara skapades i [!DNL Journey Optimizer B2B Edition].
* När du skapar en målgrupp och använder den för den här reseåtgärden måste du koppla målgruppen. Mer information finns i [Skapa en ny målanslutning](https://experienceleague.adobe.com/sv/docs/experience-platform/destinations/ui/connect-destination){target="_blank"} och [Aktiveringsöversikt](https://experienceleague.adobe.com/sv/docs/experience-platform/destinations/ui/activate/activation-overview#activate-audiences-from-the-destinations-catalog){target="_blank"} i [!DNL Experience Platform]-dokumentationen.

![Video](../../assets/do-not-localize/icon-video.svg){width="30"} [Titta på en videoöversikt för betald mediasamordning](../data/linkedin-account-matched-audiences.md#orchestrate-paid-media-engagement)

Från och med version 2025.10 kan du även orkestrera via externa målgrupper som skapats i [!DNL Experience Platform], till exempel [!DNL Adobe Target] mål. Mer information om den här målgruppsintegreringen finns i [Adobe Target externa målgrupper](../audiences/target-external-audience.md).

_Skapa en extern publik :_

1. Välj **[!UICONTROL Create new]**.

1. Klicka på **[!UICONTROL Create external customer audience]**.

1. Ange **[!UICONTROL Name]** (obligatoriskt) och **[!UICONTROL Description]** (valfritt) för den nya externa målgruppen.

   ![Lägg till för extern kundpublik - Skapa målgrupp](./assets/node-action-add-to-external-create-new.png){width="300"}

1. Klicka på **[!UICONTROL Create]**.

   Systemet skapar den nya målgruppen och visar ett bekräftelsemeddelande. Sedan kan du fortsätta att använda den som en befintlig målgrupp för nodåtgärden.

   >[!NOTE]
   >
   >När en ny extern kundpublik skapas från Journey Optimizer B2B edition dirigeras den med en dummy-post (`test@email.com`). Den här posten skrivs över så snart den första riktiga profilen läggs till den externa publiken från resan.

_Använd en befintlig målgrupp :_

1. Klicka på **[!UICONTROL Select external customer audience]**.

1. Välj den målgrupp du vill använda i dialogrutan.

   ![Lägg till i extern kundpublik - Lägg till målgrupp](./assets/node-action-add-to-external-audience-select.png){width="700" zoomable="yes"}

1. Klicka på **[!UICONTROL Add audience]**.

+++

+++[!UICONTROL Assign to Buying Group]

Använd den här åtgärden om du vill lägga till personprofiler i en [inköpsgrupp](../buying-groups/buying-groups-overview.md) baserat på ett valt lösningsintresse och en vald roll.

![Vidta en åtgärd - Lägg till i inköpsgrupp](./assets/node-action-add-to-buying-group.png){width="300"}

+++

+++[!UICONTROL Change Score]

Använd den här åtgärden om du vill ändra personpoängen i Marketo Engage. [Läs mer](https://experienceleague.adobe.com/sv/docs/marketo-learn/tutorials/lead-and-data-management/lead-scoring-learn){target="_blank"}

![Vidta en åtgärd - Ändra poäng](./assets/node-action-change-score.png){width="300"}

+++

+++[!UICONTROL Person Interesting Moment]

Använd den här åtgärden för att logga ett intressant ögonblick för människor. Välj en typ (E-post, Milstolpe eller Webb) och lägg till en beskrivning (valfritt).

![Vidta en åtgärd - Personens intressanta ögonblick](./assets/node-action-person-interesting-moment.png){width="300"}

+++

+++[!UICONTROL Remove from Buying Group]

Använd den här åtgärden om du vill ta bort personprofiler från en [inköpsgrupp](../buying-groups/buying-groups-overview.md) baserat på ett valt lösningsintresse.

![Vidta en åtgärd - Lägg till i inköpsgrupp](./assets/node-action-remove-from-buying-group.png){width="300"}

+++

+++[!UICONTROL Send email]

Använd den här åtgärden om du vill skicka ett e-postmeddelande. När du har [skapat e-postmeddelandet](../content/add-email.md#add-an-email-to-your-journey) för noden kan du utforma, anpassa och förhandsgranska e-postmeddelanden i e-postdesignområdet (se [Skapa e-post](../content/email-authoring.md)). Du kan också skicka ett [e-postmeddelande från Marketo Engage](https://experienceleague.adobe.com/sv/docs/marketo/using/product-docs/email-marketing/general/creating-an-email/create-an-email){target="_blank"}. Markera arbetsytan i Marketo Engage och välj sedan det e-postmeddelande som du vill skicka.

![Vidta en åtgärd - Skicka e-post](./assets/node-action-send-email-from-marketo.png){width="300"}

+++

+++[!UICONTROL Send SMS]

Använd den här åtgärden om du vill skicka ett SMS-meddelande. Du kan skapa, anpassa och förhandsgranska SMS-meddelanden i den visuella designrymden (se [SMS-redigering](../content/sms-authoring.md)).

![Vidta en åtgärd - Skicka SMS](./assets/node-action-send-sms.png){width="300"}

+++

+++[!UICONTROL Update person profile]

Använd den här åtgärden om du vill ändra värdet för ett [personprofilattribut](../admin/field-mapping.md#xdm-business-person-attributes). Markera attributet och ange sedan det nya värdet.

![Vidta en åtgärd - Uppdatera personprofil](./assets/node-action-update-person-profile.png){width="300"}

>[!NOTE]
>
>_[!UICONTROL Update person profile]_&#x200B;ersätter åtgärden&#x200B;_[!UICONTROL Change Data Value]_ för den [förenklade arkitekturen](../simplified-architecture.md).<br/>
>
>En administratör kan konfigurera tillgängliga attribut för den enskilda XDM-profilen genom att uppdatera fälten i _[!UICONTROL XDM Classes]_> [!UICONTROL Standard classes]. Mer information finns i [Standardklasser](../admin/xdm-field-management.md#standard-classes).

+++

### Marketo Engage-åtgärder

Marketo Engage personbaserade åtgärder är utformade för att samordna er kontobaserade marknadsföringssamordning i Journey Optimizer B2B edition med era ledande marknadsföringssatsningar i Marketo Engage. Använd dessa åtgärder för att samordna listmedlemskap och begära kampanjer.

>[!NOTE]
>
>Marketo Engage-åtgärderna kräver konfigurerad integrering med en eller flera externa Marketo Engage-instanser. <!-- For detailed information about configuring these connections, see #. -->

Du kanske vill inaktivera kampanjer i Marketo Engage för personer som är en del av inköpsgrupper i Journey Optimizer B2B edition. I det här fallet kan du skapa en statisk lista i Marketo Engage specifikt för att tillgodose lösningsbehovet. Använd sedan åtgärden _Lägg till i Marketo-lista_ från en kundnod på en delad sökväg genom att köpa en grupp. Den här åtgärden lägger till köpgruppsmedlemmar i en viss statisk lista i en ansluten Marketo Engage-instans. Använd sedan den statiska listan med lösningsintresse för ett smart listfilter i Marketo Engage.

+++[!UICONTROL Add to Marketo Engage Request campaign]

Använd den här åtgärden om du vill lägga till personprofiler i en [begärankampanj](https://experienceleague.adobe.com/sv/docs/marketo/using/product-docs/core-marketo-concepts/smart-campaigns/flow-actions/request-campaign){target="_blank"} i Marketo Engage.

Välj först en ansluten Marketo Engage-instans. Välj sedan kampanjnamnet för begäran.

![Vidta en åtgärd - Lägg till i Marketo Engage Request-kampanj](./assets/node-action-add-to-request-campaign-options.png){width="300"}

+++

+++[!UICONTROL Add to Marketo list]

Använd den här åtgärden om du vill lägga till personer i en [statisk lista](https://experienceleague.adobe.com/sv/docs/marketo/using/product-docs/core-marketo-concepts/smart-lists-and-static-lists/static-lists/understanding-static-lists){target="_blank"} i Marketo Engage.

Välj först en ansluten Marketo Engage-instans. Välj sedan listnamnet.

![Vidta en åtgärd - Lägg till i Marketo-listan](./assets/node-action-add-to-list-options.png){width="300"}

+++

+++[!UICONTROL Remove from Marketo list]

Använd den här åtgärden om du vill ta bort personer från en [statisk lista](https://experienceleague.adobe.com/sv/docs/marketo/using/product-docs/core-marketo-concepts/smart-lists-and-static-lists/static-lists/understanding-static-lists){target="_blank"} i Marketo Engage.

Välj först en ansluten Marketo Engage-instans. Välj sedan listnamnet.

![Vidta en åtgärd - Ta bort från Marketo-listan](./assets/node-action-remove-from-list-options.png){width="300"}

+++

## Videoöversikt

>[!VIDEO](https://video.tv.adobe.com/v/3443207/?learn=on)
