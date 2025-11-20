---
title: Lyssna efter en händelse
description: Konfigurera händelsnoder för konto- och personutlösare - lyssna efter ändringar i köpgrupper, e-postklick, formulärfyllningar och Experience Platform-händelser i Journey Optimizer B2B edition.
feature: Account Journeys
role: User
exl-id: d852660b-f1da-4da0-86f0-85271f55b79f
source-git-commit: 53875f5b1b61b5a4a87e3361eacae80a5c14d878
workflow-type: tm+mt
source-wordcount: '1616'
ht-degree: 1%

---

# Lyssna efter en händelse

Lägg till noden _Lyssna efter en händelse_ om du vill flytta målgruppen framåt till nästa steg i kontoresan när en händelse inträffar.

![Video](../../assets/do-not-localize/icon-video.svg){width=&quot;30&quot;, vertical-align=&quot;middle&quot;} [Se översiktsvideon](#overview-video)

>[!NOTE]
>
>Du kan inte lägga till den här nodtypen på delad sökväg av personer.

## Kontohändelser

Lyssna efter en händelse som baseras på kontot när du vill flytta kontot framåt i resan enligt händelser som utlöses av kontoaktivitet.

### Händelser och begränsningar

| Händelse | Begränsningar |
| ----- | ----------- |
| [!UICONTROL Account had interesting moment] | Typ (e-post, milstolpe eller webb)<br/>Ytterligare begränsningar (valfritt): <li>Beskrivning</li><li>Källa</li><li>Aktivitetsdatum</li> <br/>Timeout (valfritt) |
| [!UICONTROL Change in Account Data Value] | Attribut<br/>Ytterligare begränsningar (valfritt): <li>Nytt värde</li><li>Föregående värde</li><li>Aktivitetsdatum</li> <br/>Timeout (valfritt) |
| [!UICONTROL Change in Buying Group Stage] | Intresse av lösning<br/>Ytterligare begränsningar (valfritt): <li>Ny fas</li><li>Föregående fas</li><li>Aktivitetsdatum</li><br/> Timeout (valfritt) |
| [!UICONTROL Change in Buying Group Status] | Intresse av lösning<br/>Ytterligare begränsningar (valfritt): <li>Ny status</li><li>Föregående status</li><li>Aktivitetsdatum</li><br/> Timeout (valfritt) |
| [!UICONTROL Change in Completeness Score] | Intresse av lösning<br/>Ytterligare begränsningar (valfritt): <li>Nytt musikspår</li><li>Föregående poäng</li><li>Aktivitetsdatum</li><br/> Timeout (valfritt) |
| [!UICONTROL Change in Engagement Score] | Intresse av lösning<br/>Ytterligare begränsningar (valfritt): <li>Nytt musikspår</li><li>Föregående poäng</li><li>Aktivitetsdatum</li><br/> Timeout (valfritt) |

### Lägg till en kontohändelse

1. Navigera till resekartan.

1. Klicka på plusikonen ( **+** ) på en bana och välj **[!UICONTROL Listen for an event]**.

1. Välj **[!UICONTROL Accounts]** som händelsetyp i nodegenskaperna till höger.

   ![Resensnod - lyssna på händelser på konto](./assets/node-listen-events-account.png){width="700" zoomable="yes"}

1. Välj en händelse i listan.

1. Klicka på **[!UICONTROL Edit event]** och definiera information för händelsen.

## Personhändelser

Lyssna efter en händelse som baseras på personer när du vill flytta kontot framåt i resan enligt händelser som triggas av personaktivitet. Du kan också filtrera händelser efter personattribut,

### Händelser och begränsningar

| Indatatyp | Händelse | Begränsningar |
| ---------- | ----- | ----------- |
| Journey Optimizer B2B | [!UICONTROL Assigned to Buying Group] | Intresse av lösning<br/><br/>Ytterligare begränsningar (valfritt): <li>Roll</li><li>Aktivitetsdatum</li><br/>Timeout (valfritt) |
| | [!UICONTROL Clicks link in email] | E-post<br/><br/>Ytterligare begränsningar (valfritt): <li>Länk</li><li>Länk-ID</li><li>Är mobil enhet</li><li>Enhet</li><li>Plattform</li><li>Webbläsare</li><li>Är prediktivt innehåll</li><li>Är robotaktivitet</li><li>Punktaktivitetsmönster</li><li>Webbläsare</li><li>Aktivitetsdatum</li><li>Min. antal gånger</li><br/>Timeout (valfritt) |
| | [!UICONTROL Clicks link in SMS] | E-post<br/><br/>Ytterligare begränsningar (valfritt): <li>Länk</li><li>Enhet</li><li>Plattform</li><li>Aktivitetsdatum</li><li>Min. antal gånger</li><br/>Timeout (valfritt) |
| | [!UICONTROL Data value changes] | Personattribut<br/><br/>Ytterligare begränsningar (valfritt): <li>Nytt värde</li><li>Föregående värde</li><li>Orsak</li><li>Källa</li><li>Aktivitetsdatum</li><li>Min. antal gånger</li><br/>Timeout (valfritt) |
| | [!UICONTROL Opens email] | E-post<br/><br/>Ytterligare begränsningar (valfritt): <li>Länk</li><li>Länk-ID</li><li>Är mobil enhet</li><li>Enhet</li><li>Plattform</li><li>Webbläsare</li><li>Är prediktivt innehåll</li><li>Är robotaktivitet</li><li>Punktaktivitetsmönster</li><li>Webbläsare</li><li>Aktivitetsdatum</li><li>Min. antal gånger</li><br/>Timeout (valfritt) |
| | [!UICONTROL Removed from Buying Group] | Lösning, intresse<br/>Aktivitetsdatum (valfritt)<br/>Tidsgräns (valfritt) |
| | [!UICONTROL Score is changed] | Efternamn<br/><br/>Ytterligare begränsningar (valfritt):<li>Ändra</li><li>Nytt musikspår</li><li>Akut</li><li>Prioritet</li><li>Relativ poäng</li><li>Relativ brådska</li><li>Aktivitetsdatum</li><li>Min. antal gånger</li><br/>Timeout (valfritt) |
| | [!UICONTROL SMS Bounces] | SMS<br/><br/>Ytterligare begränsningar (valfritt): <li>Aktivitetsdatum</li><li>Minsta antal gånger</li><br/>Timeout (valfritt) |
| Marketo Engage | [!UICONTROL Visits Web Page] | Webbsida <br/> Välj en eller flera Marketo Engage-sidor som ska matchas. <br/><br/>Ytterligare begränsningar (valfritt): <li>Frågesträng</li><li>Klientens IP-adress</li><li>Referent</li><li>Användaragent</li><li>Sökmotor</li><li>Sökfråga</li><li>Token</li><li>Webbläsare</li><li>Plattform</li><li>Enhet</li><li>Aktivitetsdatum</li> |
| | [!UICONTROL Fills out form] | Formulär <br/> Välj ett eller flera Marketo Engage-formulär som ska matchas. <br/><br/>Ytterligare begränsningar (valfritt): <li>Aktivitetsdatum</li><li>Frågesträng</li><li>Klientens IP-adress</li><li>Referent</li><li>Användaragent</li><li>Plattform</li><li>Enhet</li><br/>Timeout (valfritt) |
| Adobe Experience Platform | [!UICONTROL Event definition] | Händelsetyp <br/><br/>Ytterligare begränsningar (valfritt): <li>Fält</li> <br/>Ytterligare begränsningar (stöds inte): <li>Aktivitetsdatum</li><li>Min. antal gånger</li><br/> Timeout (valfritt) |

### Personhändelsefilter

| Filter | Beskrivning |
| ------------ | ----------- |
| [!UICONTROL Activity history] > [!UICONTROL Email] | E-postaktiviteter baserade på villkor som utvärderas med ett eller flera valda e-postmeddelanden från tidigare under resan: <li>[!UICONTROL Clicked link in email] <li>Öppnad e-post <li>Levererades via e-post <li>Skickades via e-post <!-- <br>**[!UICONTROL Switch to inactivity filter]** - Use this option to filter based on lack of activity (a person did not have the email activity).--> |
| [!UICONTROL Activity history] > [!UICONTROL SMS Message] | SMS-aktiviteter baserade på villkor som utvärderas med ett eller flera valda SMS-meddelanden från tidigare körningar: <li>[!UICONTROL Clicked link in SMS] <li>[!UICONTROL SMS Bounced] <!--  <br>**[!UICONTROL Switch to inactivity filter]** - Use this option to filter based on lack of activity (a person did not have the SMS activity). --> |
| [!UICONTROL Activity history] > [!UICONTROL Data Value Changed] | En värdeändring har gjorts för ett markerat personattribut. De här ändringstyperna är: <li>Nytt värde<li>Föregående värde<li>Orsak<li>Källa<li>Aktivitetsdatum<li>Min. antal gånger <!--  <br>**[!UICONTROL Switch to inactivity filter]** - Use this option to filter based on lack of activity (a person did not have a data value change). --> |
| [!UICONTROL Activity history] > [!UICONTROL Had Interesting Moment] | Intressanta ögonblick som definieras i den associerade Marketo Engage-instansen. Begränsningarna är: <li>Milstolpe<li>E-post<li>Webb <!-- <br>**[!UICONTROL Switch to inactivity filter]** - Use this option to filter based on lack of activity (a person did not have an interesting moment).--> |
| [!UICONTROL Activity history] > [!UICONTROL Visited web page] | Webbsidesaktivitet som för en eller flera webbsidor hanteras av den associerade Marketo Engage-instansen. Begränsningarna är: <li>Webbsida (obligatoriskt)<li>Aktivitetsdatum<li>Klientens IP-adress <li>Frågesträng <li>Referent <li>Användaragent <li>Sökmotor <li>Sökfråga <li>Anpassad URL <li>Token <li>Webbläsare <li>Plattform <li>Enhet <li>Min. antal gånger <!-- <br>**[!UICONTROL Switch to inactivity filter]** - Use this option to filter based on lack of activity (a person did not visit the web page). --> |
| [!UICONTROL Person Attributes] | Attribut från personprofilen, inklusive: <li>Ort <li>Land <li>Födelsedatum <li>E-postadress <li>Ogiltig e-postadress <li>E-postmeddelandet har pausats <li>Förnamn <li>Ingångsregion<li>Befattning <li>Efternamn <li>Mobiltelefonnummer <li>Personengagemangspoäng <li>Telefonnummer <li>Postnummer <li>Stat <li>Avprenumererad <li>Orsak till avbeställning |
| [!UICONTROL Special filters] > [!UICONTROL Member of Buying Group] | Personen är eller är inte medlem i en inköpsgrupp och utvärderas utifrån ett eller flera av följande kriterier: <li>Intresse av lösningar</li><li>Status för inköpsgrupp</li><li>Slutförandepoäng</li><li>Engagement Score</li><li>Roll</li> |
| [!UICONTROL Special filters] > [!UICONTROL Member of List] | Personen är eller är inte medlem i en eller flera Marketo Engage-listor. |
| [!UICONTROL Special filters] > [!UICONTROL Member of Program] | Personen är eller är inte medlem i ett eller flera Marketo Engage-program. |

### Lägg till en personhändelse

1. Navigera till resekartan.

1. Klicka på plusikonen ( **+** ) på en bana och välj **[!UICONTROL Listen for an event]**.

1. Välj **[!UICONTROL People]** som händelsetyp i nodegenskaperna till höger.

   ![Resensnod - lyssna på händelser på personer](./assets/node-listen-events-people.png){width="700" zoomable="yes"}

1. Välj en händelse i listan.

1. Klicka på **[!UICONTROL Edit event]** och definiera information för händelsen.

### Lyssna efter en Marketo Engage-händelse

Om du har webbsidor i den anslutna Marketo Engage-instansen kan du utlösa en händelse baserat på ett besök eller inget besök på dessa webbsidor, samt på Marketo Engage-formulär som fyllts i eller inte fyllts i.

1. Välj en **[!UICONTROL Listen for an event]**-nod på färdkartan.

1. Välj **[!UICONTROL People]** som händelsetyp i nodegenskaperna till höger.

1. Klicka på pilen för väljaren **[!UICONTROL Select people event]** och rulla menyn till avsnittet **[!UICONTROL Marketo Engage]**.

1. Välj en marknadsengagerande aktivitetstyp:

   * **[!UICONTROL Visits Web Page]**.
   * **[!UICONTROL Fills Out Form]**

   ![Lyssna efter en upplevelsehändelse](./assets/node-listen-events-people-me-event.png){width="700" zoomable="yes"}

1. Klicka på **[!UICONTROL Edit event]** och definiera en eller flera webbsidor som ska matcha och eventuella ytterligare begränsningar för händelsen.

   * (Obligatoriskt) I dialogrutan _[!UICONTROL Edit event]_definierar du begränsningen **[!UICONTROL Web page]**eller **[!UICONTROL Fills out form]**. Använd **[!UICONTROL is]**(standard) för att matcha på en eller flera valda sidor eller formulär. Använd **[!UICONTROL is not]**för att matcha på alla sidbesök/formulär med undantag för en eller flera valda sidor/formulär. Du kan också använda operatorn **[!UICONTROL is any]**för att matcha ett besök på en Marketo Engage-webbsida eller i ett ifyllt formulär.

   * (Valfritt) Klicka på **[!UICONTROL Add constraint]** och välj det fält som du vill använda som begränsning. Ange operatorn och fältets värde.

     ![Lyssna efter en upplevelsehändelse](./assets/node-listen-events-people-me-event-edit-dialog.png){width="700" zoomable="yes"}

     Du kan upprepa den här åtgärden för att inkludera ytterligare fältbegränsningar efter behov.

   * Om det behövs väljer du fliken **[!UICONTROL Filters]** för att [lägga till filter för händelsen](#add-a-filter-to-the-people-event).

   * När begränsningarna och filtren har definierats klickar du på **[!UICONTROL Done]**.

1. Om det behövs anger du alternativet **[!UICONTROL Timeout]** för att begränsa hur lång tid det tar att lyssna efter händelsen (se [Lägg till en timeout i en händelsnod](#add-a-timeout-to-an-event-node)).

1. Lägg till nästa nod som ska köras när händelsen inträffar i färdkartan.

### Lyssna efter en upplevelsehändelse

Administratörer kan välja [Adobe Experience Platform (AEP) Experience Events](https://experienceleague.adobe.com/en/docs/experience-platform/xdm/classes/experienceevent){target="_blank"} som gör att marknadsförare kan skapa resor som reagerar på händelserna i nära realtid. Att använda upplevelsehändelser under resor är en tvåstegsprocess:

1. En administratör [väljer händelsetyper och intressefält](../admin/configure-aep-events.md#select-an-event) för att göra dem tillgängliga på resorna.

2. Lägg till en _Lyssna efter en händelse_-nod på en resa och välj en Experience Platform-händelsetyp för en personbaserad händelse.

<!--
![Video](../../assets/do-not-localize/icon-video.svg){width="30", vertical-align="middle"} [Watch the video overview](../admin/configure-aep-events.md#overview-video) -->

_Inkludera en upplevelsehändelse i din resa :_

1. Välj en **[!UICONTROL Listen for an event]**-nod på färdkartan.

1. Välj **[!UICONTROL People]** som händelsetyp i nodegenskaperna till höger.

1. Klicka på pilen för väljaren **[!UICONTROL Select people event]** och rulla menyn till avsnittet **[!UICONTROL Adobe Experience Platform]**.

   ![Lyssna efter en upplevelsehändelse](./assets/node-listen-events-people-aep-events.png){width="700" zoomable="yes"}

1. Markera händelsen.

   Händelsetypen visas som tom i nodinformationen.

   ![Redigera händelsen](./assets/node-listen-events-people-aep-events-edit.png){width="400" zoomable="yes"}

1. Klicka på **[!UICONTROL Edit event]** och definiera en eller flera begränsningar för händelsen.

   De tillgängliga begränsningarna definieras som hanterade fält för händelsekonfigurationen.

   * Klicka på **[!UICONTROL Add constraint]** och välj det fält som du vill använda som begränsning.

   * Slutför villkoret för villkoret.

     Du kan använda standardoperatorn **[!UICONTROL is]** för att matcha ett eller flera fältvärden. Du kan också använda operatorn **[!UICONTROL is not]** för att matcha alla värden med undantag för ett eller flera angivna värden.

     ![Lyssna efter en upplevelsehändelse](./assets/node-listen-events-people-aep-events-edit-dialog.png){width="700" zoomable="yes"}

   * Om det behövs väljer du fliken **[!UICONTROL Filters]** för att [lägga till filter för händelsen](#add-a-filter-to-the-people-event).

   * (Valfritt) Klicka på **[!UICONTROL Add constraint]** och upprepa de här stegen för att inkludera ytterligare fältbegränsningar efter behov.

   * När begränsningarna och filtren har definierats klickar du på **[!UICONTROL Done]**.

1. Om det behövs anger du alternativet **[!UICONTROL Timeout]** för att begränsa hur lång tid det tar att lyssna efter händelsen (se [Lägg till en timeout i en händelsnod](#add-a-timeout-to-an-event-node)).

1. Lägg till nästa nod som ska köras när händelsen inträffar i färdkartan.

1. Slutför de återstående noderna för din resa och [publicera den](./journey-overview.md).

   När resan är live (publicerad) och når noden _Lyssna efter en händelse_ börjar den lyssna efter AEP Experience Events.

### Lägg till filter i personhändelsen

1. När du har definierat händelsen väljer du fliken **[!UICONTROL Filters]** i dialogrutan _[!UICONTROL Edit Event]_.

   ![Lyssna efter händelsnod av personer - Välj fliken Filter för att redigera händelsen](./assets/node-listen-event-people-edit-event-filters.png){width="700" zoomable="yes"}

1. Lägg till ett eller flera filter för att ange personer som mål för händelsen.

   * Dra och släpp något av [personfiltren](#people-event-filters) från den vänstra navigeringen och slutför matchningsdefinitionen.

     >[!NOTE]
     >
     >Om du har definierat anpassade personfält i kontots målgruppsschema i Experience Platform, är dessa fält även tillgängliga under **[!UICONTROL Attributes]** och kan användas som personattribut i filter.

   * Finjustera filtreringen genom att använda **[!UICONTROL Filter logic]** överst. Du väljer att matcha alla filter eller något filter.

     ![Personfilter som används i en händelsedefinition](./assets/node-split-conditions-people.png){width="700" zoomable="yes"}

   * Klicka på **[!UICONTROL Done]**.

## Lägga till en timeout i en händelsnod

Ange vid behov hur lång tid resan väntar på händelsen. Resan avslutas efter en timeout såvida du inte definierar en timeout-sökväg, där du kan lägga till andra noder.

1. Aktivera alternativet **[!UICONTROL Timeout]**.

1. Välj hur länge resan väntar på att en händelse ska inträffa innan den inträffar.

   Du kan välja att avsluta banan här eller utföra en annan åtgärd genom att ange en annan bana.

1. Om du vill skapa en ny sökväg under resan där du kan lägga till åtgärder och händelser som gäller konton när händelsen inte inträffar, markerar du kryssrutan **[!UICONTROL Set timeout path]**.

   ![Resans händelsnod - ange tidsgräns](./assets/node-event-timeout-set-path.png){width="700" zoomable="yes"}

<!-- ## Overview video

>[!VIDEO](https://video.tv.adobe.com/v/3443219/?learn=on) -->
