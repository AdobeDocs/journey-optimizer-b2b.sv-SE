---
title: Person Audience Nodes
description: Konfigurera personmålgruppsnoder med segment- eller händelsebaserade målgrupper för att definiera startpunkter för personresor för riktad samordning i Journey Optimizer B2B edition.
feature: Audiences
role: User
badgeBeta: label="Beta" type="informative" tooltip="Den här funktionen är för närvarande i en begränsad betaversion"
source-git-commit: f5170767a6df14874fab5de203264a5a5e3e245a
workflow-type: tm+mt
source-wordcount: '681'
ht-degree: 0%

---

# Personens målgruppsnoder

Noden _Personpublik_ anger vilka personprofiler som går in på resan. När du [skapar en personresa](./create-publish-journey.md#create-a-journey) börjar alltid resan med en personmålsnod som definierar dess indata. Personens målgruppsnod kan ha en av två typer av målgruppsindata: CDP-segment eller händelsebaserat medlemskap. Segment- och händelsebaserade målgruppsdefinitioner kan inte kombineras.

Använd något av följande inmatningsalternativ för noden för målgruppsresa:

* **Profilmålgrupp** - Använd segmentmålgrupper som definierats i en CDP. Alla profiler som kvalificerar sig för målgruppen läggs till som medlemmar på resan. Nyligen kvalificerade profiler för segmentet läggs till på resan under de dagliga [aktiviteterna för profilinhämtning](#profile-ingestion). Om en profil inte längre är kvalificerad för segmentet tas den **_inte_** bort från resan.

* **Händelsemottagare** - Använd kvalificerande händelser för att definiera målgruppen. Dessa händelser definieras i nodkonfigurationen och måste använda [XDM-händelser som konfigurerats i administrationsinställningarna](../admin/configure-aep-events.md). Upp till 10 event stöds för händelsebaserat medlemskap. En profil kvalificerar sig omedelbart för resan efter den första matchande händelsen som deras profil tar.

  >[!NOTE]
  >
  >Händelser kan inte kombineras med profilattribut för att begränsa målgruppsdefinitioner. Förbättringar för att ta itu med denna begränsning planeras för framtida versioner.

## Intag av profiler

I Journey Optimizer B2B edition synkroniseras profiler med Experience Platform med målgruppsinhämtning varje natt. Även om händelsebaserade personresor kan kvalificera profiler som inte är en del av en profil eller en målgrupp som är inkapslad/används av Journey Optimizer B2B edition, leder det till inkapslade profiler som förblir inaktuella, såvida de inte är en del av en målgrupp som används av en personresa, kontoresa eller köpgrupp. Om en profil är inkapslad och senare läggs till i en målgrupp utförs sammanfogning av profiler och profilen är synkroniserad med Experience Platform. Förbättringar av synkroniseringen av profildata planeras för framtida versioner.

En nyligen skapad profil som hämtas av en händelsebaserad personresa kanske inte har den uppdaterade profilinformationen vid tidpunkten för intaget. Om en profil till exempel skapas via en formulärfyllningshändelse, och en person som besöker dem från den kvalificerande formulärfyllningshändelsen, kanske de data som skickas i formuläret ännu inte synkroniseras med profilen när resan importerade dem. Resultatet kan vara ofullständiga data för personalisering (till exempel i e-postinnehåll). Förbättringar av den här profilhändelsedatasynkroniseringen planeras för framtida versioner.

Evenemangsbaserade personresor kan kvalificera profiler som fortfarande är anonyma/utan e-postadresser och endast innehåller ECID. Det är vanligast när du har kvalificeringslogik för webbsidesaktivitet. Överdrivet bred händelsebaserad målgruppslogik kan resultera i att instansen når upp till 40 miljoner profiler om för många profiler kvalificerar sig. Begränsa det möjliga omfånget för er målgrupp för att förhindra detta scenario.

>[!IMPORTANT]
>
>Under det aktuella betaprogrammet är det idealiska sättet att använda personresor att kvalificera sig enbart för profiler som du också riktar in dig på kontoresor och köper gruppdefinitioner. Den här användningen garanterar en fullständig profil som är synkroniserad med Experience Platform.

## Ange målgrupp för målgruppsnoden

1. Klicka på noden **[!UICONTROL Person audience]**.

   Den här åtgärden visar nodegenskaperna till höger.

   ![Personens målgruppsnod](./assets/person-journey-person-audience-node.png){width="700" zoomable="yes"}

1. Välj indatatyp för personer som ska resa:

   * **[!UICONTROL Profile audience]**

     Välj alternativet _[!UICONTROL Profile audience]_. Klicka sedan på&#x200B;**[!UICONTROL Add profile audience]**.

     I dialogrutan _[!UICONTROL Add audience]_&#x200B;väljer du ett tidigare skapat målgruppssegment. Klicka sedan på&#x200B;**[!UICONTROL Add audience]**.

     ![Välj en profilmålgrupp för noden](./assets/node-person-audience-add-audience-dialog.png){width="700" zoomable="yes"}

   * **[!UICONTROL Event audience]**

     Välj alternativet _[!UICONTROL Event audience]_. Klicka sedan på&#x200B;**[!UICONTROL Add event criteria]**.

     I dialogrutan _[!UICONTROL Edit event criteria]_&#x200B;lägger du till en eller flera händelser som du vill använda för att kvalificera målgruppsmedlemmar. För varje händelse som du lägger till klickar du på&#x200B;**[!UICONTROL Add constraint]**&#x200B;för att välja ett händelseattribut för en matchning. Ange utvärderingen som du vill använda för en matchning. Du kan lägga till flera begränsningar för att matcha händelsen.

     ![Lägg till händelser och matchningskriterier för att kvalificera en personprofil](./assets/node-person-audience-edit-event-criteria-dialog.png){width="700" zoomable="yes"}

     Klicka på **[!UICONTROL Save]** när händelsevillkoren har definierats.

     Mer information om konfiguration för händelser som stöds under resan finns i [Hantera upplevelsehändelser](../admin/configure-aep-events.md#manage-experience-events).
