---
title: Lyssna efter en händelse
description: Läs mer om avlyssningen av en händelsnodtyp som du kan använda för att ordna dina kontoresor i Journey Optimizer B2B edition.
feature: Account Journeys
exl-id: d852660b-f1da-4da0-86f0-85271f55b79f
source-git-commit: d03e0e2d8070916d38bb956adff8dea3f3873aad
workflow-type: tm+mt
source-wordcount: '1297'
ht-degree: 1%

---

# Lyssna efter en händelse

Lägg till noden _Lyssna efter en händelse_ om du vill flytta målgruppen framåt till nästa steg i kontoresan när en händelse inträffar.

![Video](../../assets/do-not-localize/icon-video.svg){width="30"} [Se översiktsvideon](#overview-video)

>[!NOTE]
>
>Du kan inte lägga till den här nodtypen på delad sökväg av personer.

## Kontohändelser

Lyssna efter en händelse som baseras på kontot när du vill flytta kontot framåt i resan enligt händelser som utlöses av kontoaktivitet.

### Händelser och begränsningar

| Händelse | Begränsningar |
| ----- | ----------- |
| Kontot hade en intressant stund | Typ (e-post, milstolpe eller webb)<br/>Ytterligare begränsningar (valfritt): <li>Beskrivning</li><li>Källa</li><li>Aktivitetsdatum</li> <br/>Timeout (valfritt) |
| Ändra värde för kontodata | Attribut<br/>Ytterligare begränsningar (valfritt): <li>Nytt värde</li><li>Föregående värde</li><li>Aktivitetsdatum</li> <br/>Timeout (valfritt) |
| Ändringar i köpgruppsfasen | Intresse av lösning<br/>Ytterligare begränsningar (valfritt): <li>Ny fas</li><li>Föregående fas</li><li>Aktivitetsdatum</li><br/> Timeout (valfritt) |
| Ändring i inköpsgruppsstatus | Intresse av lösning<br/>Ytterligare begränsningar (valfritt): <li>Ny status</li><li>Föregående status</li><li>Aktivitetsdatum</li><br/> Timeout (valfritt) |
| Ändrad slutförandepoäng | Intresse av lösning<br/>Ytterligare begränsningar (valfritt): <li>Nytt musikspår</li><li>Föregående poäng</li><li>Aktivitetsdatum</li><br/> Timeout (valfritt) |
| Ändrad engagemangspoäng | Intresse av lösning<br/>Ytterligare begränsningar (valfritt): <li>Nytt musikspår</li><li>Föregående poäng</li><li>Aktivitetsdatum</li><br/> Timeout (valfritt) |

### Lägg till en kontohändelse

1. Navigera till reseeditorn.

1. Klicka på plusikonen ( **+** ) på en bana och välj **[!UICONTROL Listen for an event]**.

1. Välj **[!UICONTROL Accounts]** som händelsetyp i nodegenskaperna till höger.

   ![Resensnod - lyssna på händelser på konto](./assets/node-listen-events-account.png){width="700" zoomable="yes"}

1. Välj en händelse i listan.

1. Klicka på **[!UICONTROL Edit event]** och definiera information för händelsen.

## Personhändelser

Lyssna efter en händelse som baseras på personer när du vill flytta kontot framåt i resan enligt händelser som triggas av personaktivitet.

### Händelser och begränsningar

| Indatatyp | Händelse | Begränsningar |
| ---------- | ----- | ----------- |
| Journey Optimizer B2B | Tilldelad till inköpsgrupp | Intresse av lösning<br/><br/>Ytterligare begränsningar (valfritt): <li>Roll</li><li>Aktivitetsdatum</li><br/>Timeout (valfritt) |
| | Klicka på länken i e-postmeddelandet | E-post<br/><br/>Ytterligare begränsningar (valfritt): <li>Länk</li><li>Länk-ID</li><li>Är mobil enhet</li><li>Enhet</li><li>Plattform</li><li>Webbläsare</li><li>Är prediktivt innehåll</li><li>Är robotaktivitet</li><li>Punktaktivitetsmönster</li><li>Webbläsare</li><li>Aktivitetsdatum</li><li>Min. antal gånger</li><br/>Timeout (valfritt) |
| | Klicka på länken i SMS | E-post<br/><br/>Ytterligare begränsningar (valfritt): <li>Länk</li><li>Enhet</li><li>Plattform</li><li>Aktivitetsdatum</li><li>Min. antal gånger</li><br/>Timeout (valfritt) |
| | Ändringar av datavärde | Personattribut<br/><br/>Ytterligare begränsningar (valfritt): <li>Nytt värde</li><li>Föregående värde</li><li>Orsak</li><li>Källa</li><li>Aktivitetsdatum</li><li>Min. antal gånger</li><br/>Timeout (valfritt) |
| | Öppnar e-post | E-post<br/><br/>Ytterligare begränsningar (valfritt): <li>Länk</li><li>Länk-ID</li><li>Är mobil enhet</li><li>Enhet</li><li>Plattform</li><li>Webbläsare</li><li>Är prediktivt innehåll</li><li>Är robotaktivitet</li><li>Punktaktivitetsmönster</li><li>Webbläsare</li><li>Aktivitetsdatum</li><li>Min. antal gånger</li><br/>Timeout (valfritt) |
| | Borttagen från inköpsgrupp | Lösning, intresse<br/>Aktivitetsdatum (valfritt)<br/>Tidsgräns (valfritt) |
| | Poängen har ändrats | Efternamn<br/><br/>Ytterligare begränsningar (valfritt):<li>Ändra</li><li>Nytt musikspår</li><li>Akut</li><li>Prioritet</li><li>Relativ poäng</li><li>Relativ brådska</li><li>Aktivitetsdatum</li><li>Min. antal gånger</li><br/>Timeout (valfritt) |
| | SMS-studsar | SMS<br/><br/>Ytterligare begränsningar (valfritt): <li>Aktivitetsdatum</li><li>Minsta antal gånger</li><br/>Timeout (valfritt) |
| Marketo Engage | Besök webbsida | Webbsida <br/> Välj en eller flera Marketo Engage-sidor som ska matchas. <br/><br/>Ytterligare begränsningar (valfritt): <li>Frågesträng</li><li>Klientens IP-adress</li><li>Referent</li><li>Användaragent</li><li>Sökmotor</li><li>Sökfråga</li><li>Token</li><li>Webbläsare</li><li>Plattform</li><li>Enhet</li><li>Aktivitetsdatum</li> |
| | Fyller i formulär | Formulär <br/> Välj ett eller flera Marketo Engage-formulär som ska matchas.  <br/><br/>Ytterligare begränsningar (valfritt): <li>Aktivitetsdatum</li><li>Frågesträng</li><li>Klientens IP-adress</li><li>Referent</li><li>Användaragent</li><li>Plattform</li><li>Enhet</li><br/>Timeout (valfritt) |
| Adobe Experience Platform | Händelsedefinition | Händelsetyp <br/><br/>Ytterligare begränsningar (valfritt): <li>Fält</li> <br/>Ytterligare begränsningar (stöds inte): <li>Aktivitetsdatum</li><li>Min. antal gånger</li><br/> Timeout (valfritt) |

### Lägg till en personhändelse

1. Navigera till reseeditorn.

1. Klicka på plusikonen ( **+** ) på en bana och välj **[!UICONTROL Listen for an event]**.

1. Välj **[!UICONTROL People]** som händelsetyp i nodegenskaperna till höger.

   ![Resensnod - lyssna på händelser på personer](./assets/node-listen-events-people.png){width="700" zoomable="yes"}

1. Välj en händelse i listan.

1. Klicka på **[!UICONTROL Edit event]** och definiera information för händelsen.

### Lyssna efter Marketo Engage event

Om du har webbsidor som skapats i den anslutna Marketo Engage-instansen kan du utlösa en händelse som baseras på ett besök eller inget besök på Marketo Engage webbsidor, samt på Marketo Engage-formulär som fyllts i eller inte fyllts i.

1. Välj en **[!UICONTROL Listen for an event]**-nod i reseredigeraren.

1. Välj **[!UICONTROL People]** som händelsetyp i nodegenskaperna till höger.

1. Klicka på pilen för väljaren **[!UICONTROL Select people event]** och rulla menyn till avsnittet **[!UICONTROL Marketo Engage]**.

1. Välj en marknadsengagerande aktivitetstyp:

   * **[!UICONTROL Visits Web Page]**.
   * **[!UICONTROL Fills Out Form]**

   ![Lyssna efter en upplevelsehändelse](./assets/node-listen-events-people-me-event.png){width="700" zoomable="yes"}

1. Klicka på **[!UICONTROL Edit event]** och definiera en eller flera webbsidor som ska matcha och eventuella ytterligare begränsningar för händelsen.

   * (Obligatoriskt) I dialogrutan _[!UICONTROL Edit event]_definierar du formulärbegränsningen **[!UICONTROL Web page]**eller Fyller i. Använd **[!UICONTROL is]**(standard) för att matcha på en eller flera valda sidor eller formulär. Använd **[!UICONTROL is not]**för att matcha på alla sidbesök/formulär med undantag för en eller flera valda sidor/formulär. Du kan också använda **[!UICONTROL is any]**för att matcha vid besök på Marketo Engage webbsidor eller i ifyllda formulär.

   * (Valfritt) Klicka på **[!UICONTROL Add constraint]** och välj det fält som du vill använda som begränsning. Ange operatorn och fältets värde.

     ![Lyssna efter en upplevelsehändelse](./assets/node-listen-events-people-me-event-edit-dialog.png){width="700" zoomable="yes"}

     Du kan upprepa den här åtgärden för att inkludera ytterligare fältbegränsningar efter behov.

   * När begränsningarna har definierats klickar du på **[!UICONTROL Done]**.

1. Om det behövs anger du alternativet **[!UICONTROL Timeout]** för att begränsa hur lång tid det tar att lyssna efter händelsen (se [Lägg till en timeout i en händelsnod](#add-a-timeout-to-an-event-node)).

1. Lägg till nästa nod som ska köras när händelsen inträffar i reseredigeraren.

### Lyssna efter en upplevelsehändelse

Administratörer kan konfigurera Adobe Experience Platform (AEP)-baserade händelsedefinitioner, som gör att marknadsförare kan skapa kontoresor som reagerar på [AEP Experience Events](https://experienceleague.adobe.com/en/docs/experience-platform/xdm/classes/experienceevent). Att använda AEP-upplevelsehändelser i kontoresor är en tvåstegsprocess:

1. [Skapa och publicera en AEP-händelsedefinition](../admin/configure-aep-events.md).

2. Lägg till en _Lyssna efter en händelse_-nod i en kontoresa och välj en Experience Platform-händelsdefinition för en personbaserad händelse.

_Så här tar du med en upplevelsehändelse i din resa:_

1. Välj en **[!UICONTROL Listen for an event]**-nod i reseredigeraren.

1. Välj **[!UICONTROL People]** som händelsetyp i nodegenskaperna till höger.

1. Klicka på pilen för väljaren **[!UICONTROL Select people event]** och rulla menyn till avsnittet **[!UICONTROL Adobe Experience Platform]**.

   ![Lyssna efter en upplevelsehändelse](./assets/node-listen-events-people-aep-events.png){width="700" zoomable="yes"}

1. Markera händelsen.

   Händelsetypen visas som tom i nodinformationen.

   ![Redigera händelsen](./assets/node-listen-events-people-aep-events-edit.png){width="400" zoomable="yes"}

1. Klicka på **[!UICONTROL Edit event]** och definiera händelsetyperna och eventuella ytterligare begränsningar för händelsen.

   * (Obligatoriskt) Definiera händelsetypen i dialogrutan _[!UICONTROL Edit event]_. Du kan använda standardoperatorn **[!UICONTROL is]**för att matcha en eller flera valda händelsetyper. Du kan också använda operatorn **[!UICONTROL is not]**för att matcha alla händelsetyper med undantag för en eller flera valda händelsetyper.

   * (Valfritt) Klicka på **[!UICONTROL Add constraint]** och välj det fält som du vill använda som begränsning. Ange operatorn och fältets värde.

     ![Lyssna efter en upplevelsehändelse](./assets/node-listen-events-people-aep-events-edit-dialog.png){width="700" zoomable="yes"}

     >[!NOTE]
     >
     >Begränsningarna för _aktivitetsdatum_ och _minsta antal gånger_ stöds inte.

     Du kan upprepa den här åtgärden för att inkludera ytterligare fältbegränsningar efter behov.

   * När begränsningarna har definierats klickar du på **[!UICONTROL Done]**.

1. Om det behövs anger du alternativet **[!UICONTROL Timeout]** för att begränsa hur lång tid det tar att lyssna efter händelsen (se [Lägg till en timeout i en händelsnod](#add-a-timeout-to-an-event-node)).

1. Lägg till nästa nod som ska köras när händelsen inträffar i reseredigeraren.

1. Slutför de återstående noderna för din resa och [publicera den](./journey-overview.md).

   När resan är live (publicerad) och når noden _Lyssna efter en händelse_ börjar den lyssna efter AEP Experience Events.

## Lägga till en timeout i en händelsnod

Ange vid behov hur lång tid resan väntar på händelsen. Resan avslutas efter en timeout såvida du inte definierar en timeout-sökväg, där du kan lägga till andra noder.

1. Aktivera alternativet **[!UICONTROL Timeout]**.

1. Välj hur länge resan väntar på att en händelse ska inträffa innan den inträffar.

   Du kan välja att avsluta banan här eller utföra en annan åtgärd genom att ange en annan bana.

1. Om du vill skapa en ny sökväg under resan där du kan lägga till åtgärder och händelser som gäller konton när händelsen inte inträffar, markerar du kryssrutan **[!UICONTROL Set timeout path]**.

   ![Resans händelsnod - ange tidsgräns](./assets/node-event-timeout-set-path.png){width="700" zoomable="yes"}

## Videoöversikt

>[!VIDEO](https://video.tv.adobe.com/v/3443219/?learn=on)
