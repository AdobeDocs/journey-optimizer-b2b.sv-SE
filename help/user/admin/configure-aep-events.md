---
title: Välj upplevelsehändelser och fält
description: Välj Experience Platform-händelser och -fält för att aktivera realtidsbeslut i resor baserat på kundbeteende.
feature: Setup, Integrations
role: Admin
badgeBeta: label="Beta" type="informative" tooltip="Den här funktionen är för närvarande i en betaversion"
solution: Journey Optimizer B2B Edition, Experience Platform
exl-id: a7696d03-f4c4-4f64-8ef2-b15e59b59770
source-git-commit: 5f3d7bb8eb72c48409273de43b03114d273cb80c
workflow-type: tm+mt
source-wordcount: '1423'
ht-degree: 0%

---

# Välj upplevelsehändelser och fält

Administratörer kan välja specifika [AEP Experience Events](https://experienceleague.adobe.com/sv/docs/experience-platform/xdm/classes/experienceevent){target="_blank"} och tillhörande fält i Experience Event-unionens schema. Efter markeringen kan användarna konfigurera beslutsregler så att de lyssnar på Experience Events för att aktivera dynamiska och målinriktade kampanjåtgärder baserat på händelsedata i nära realtid.

<!-- ![Video](../../assets/do-not-localize/icon-video.svg){width="30"} [Watch the video overview](#overview-video) -->
Att använda AEP upplevelsehändelser under resor är en tvåstegsprocess:

1. En administratör [lägger till AEP Experience-händelser och fält](#add-an-event) i Journey Optimizer B2B edition-konfigurationerna.

2. Under en resa lägger en marknadsförare till en _Lyssna efter en händelse_-nod och [väljer en Experience Event](../journeys/listen-for-event-nodes.md#listen-for-an-experience-event).

   * Väljer den händelse som ska användas i noden.
   * Väljer de fält som ska användas som begränsningar.

>[!BEGINSHADEBOX]

## Riktlinjer och begränsningar

När du väljer händelser för att uppnå dina organisationsmål bör du tänka på följande:

* Du kan välja upp till 50 händelser och upp till 100 fält per händelse.

* Resor kan lyssna på Experience Events som är inkapslade med Experience Platform direktuppspelningsfunktioner, som Web SDK eller HTTP API.

* Ni kan använda Experience Events för att fatta beslut inom en resa, men de behålls inte. Därför kan ni inte utnyttja tidigare erfarenheter av Experience Events i Journey Optimizer B2B edition.

* När du använder en Experience Event och publicerar resan kan du lägga till fler fält, men du kan inte ta bort fält som tidigare har markerats.

* Du kan referera till en upplevelsehändelse på flera resor eller använda en mer än en gång under samma resa.

>[!ENDSHADEBOX]

## Hantera upplevelsehändelser

1. Välj **[!UICONTROL Administration]** > **[!UICONTROL Configurations]** i den vänstra navigeringen.

1. Klicka på **[!UICONTROL XDM Classes]** på den mellanliggande panelen och klicka sedan på fliken **[!UICONTROL Events]** för att visa listan över tillgängliga händelser.

   ![Få åtkomst till de valda upplevelsehändelserna](./assets/configurations-xdm-classes-events.png){width="800" zoomable="yes"}

   Tabellen sorteras efter kolumnen _[!UICONTROL Last update]_, med de senast uppdaterade händelserna högst upp som standard.

   Från den här sidan kan du [välja](#add-an-event) och [redigera](#edit-an-event) händelser som ska användas i resor.

   Klicka på händelsenamnet för att få tillgång till information om en vald händelse.

### Filtrera händelselistan

Ange text i fältet _[!UICONTROL Search]_&#x200B;för att filtrera de händelser som visas så att de matchar händelsenamnet.

![Filtrera listan med markerade händelser efter namn](./assets/configurations-xdm-classes-events-search.png){width="600" zoomable="yes"}

### Lägg till en händelse

Om du vill göra en Experience Event tillgänglig för en _Lyssna efter en händelse_-nod under en resa, markerar du händelsen och de fält som stöds.

>[!NOTE]
>
>I betaversionen kan du inte ta bort händelser från listan. Se till att alla händelser du lägger till är sådana som din organisation har för avsikt att använda.

1. Klicka på **[!UICONTROL Select experience event]** överst till höger.

   Sidan med händelseinformation visas. På den här sidan kan du välja händelsetyp och fält.

   ![Händelseinformation för en ny händelse](./assets/configurations-xdm-classes-events-select-new.png){width="700" zoomable="yes"}

1. Välj händelsetyp.

   * Klicka på **[!UICONTROL Select event type]**.

   * Välj händelsetyp i dialogrutan.

     Använd fältet _[!UICONTROL Search]_&#x200B;för att filtrera den visade listan efter namn. Använd skjutreglaget **[!UICONTROL Only show selected fields]**&#x200B;för att granska de aktuella markeringarna.

     ![Dialogrutan Välj händelsetyp](./assets/configurations-xdm-classes-select-event-type-dialog.png){width="450" zoomable="yes"}

   * Klicka på **[!UICONTROL Select]**.

1. Välj ett eller flera fält för händelsetypen.

   * Klicka på **[!UICONTROL Select fields]**.

   * I dialogrutan väljer du de fält som du vill använda som begränsningar för matchande händelser.

     Använd fältet _[!UICONTROL Search]_&#x200B;för att filtrera den visade listan efter namn. Använd skjutreglaget **[!UICONTROL Only show selected fields]**&#x200B;för att granska de aktuella markeringarna.

     ![Dialogrutan Välj fält](./assets/configurations-xdm-classes-select-fields-dialog.png){width="450" zoomable="yes"}

   * Klicka på **[!UICONTROL Select]**.

1. Klicka på **[!UICONTROL Save]** på sidan med händelseinformation.

Den sparade händelsen visas i listan på fliken _[!UICONTROL Events]_.

### Redigera en händelse

Redigera händelseinformationen för att ändra fälten.

1. Klicka på händelsenamnet eller klicka på ikonen _Mer meny_ ( **...** ) och välj **[!UICONTROL Edit]**.

   ![Klicka på ikonen Mer på menyn &#x200B;](./assets/configurations-xdm-classes-events-more-menu.png){width="500" zoomable="yes"}

1. Klicka på **[!UICONTROL Edit fields]** om du vill lägga till fler fält eller ta bort befintliga markeringar i dialogrutan _[!UICONTROL Select fields]_.

1. Klicka på **[!UICONTROL Select]** om du vill spara dina val.

### Ta bort en händelse

>[!NOTE]
>
>I Beta-versionen av den här funktionen kan du inte ta bort en händelse från listan med markerade händelser. Händelseborttagning planeras för GA-versionen.

## Händelser och fält

För [!DNL Journey Optimizer B2B Edition] hämtas vissa aktiviteter på personnivå som [!DNL Experience Platform] Experience Events. Dessa händelser lagras i en systemdatamängd som använder XDM Experience Event-schemat och innehåller resespecifika fältgrupper. Du kan använda de här händelserna i [!UICONTROL Journey Optimizer B2B Edition] precis som andra Experience Event-händelser.

Varje händelse visar en definierad uppsättning fält som kan användas i resan _Lyssna efter en händelse_-nod (beslut baserat på händelser). Granska de tillgängliga händelsetyperna och fälten för att avgöra vilka händelser och fält som ska användas i dessa resednoder:

### E-post skickad

Den här händelsen spårar när ett marknadsföringsmeddelande skickades till en person.

Händelsetyp: `directMarketing.emailSent`

+++Fält

| Fält | Fälttyp |
| ----- | ---------- |
| Identifierare | `_id` |
| Händelsetyp | `eventType` |
| Tidsstämpel | `timestamp` |
| Person-ID | `personID` |
| Personens käll-ID | `personKey.sourceID` |
| Typ av personkälla | `personKey.sourceType` |
| Instans-ID för personkälla | `personKey.sourceInstanceID` |
| Personkällnyckel | `personKey.sourceKey` |
| Käll-ID för e-post | `directMarketing.emailSent.mailingKey.sourceID` |
| Typ av e-postkälla | `directMarketing.emailSent.mailingKey.sourceType` |
| Instans-ID för e-postkälla | `directMarketing.emailSent.mailingKey.sourceInstanceID ` |
| E-postkällnyckel | `directMailing.emailSent.mailingKey.sourceKey` |
| Utskicksnamn | `directMarketing.emailSent.mailingName` |
| Rese-ID | `_experience.journeyOrchestration.stepEvents.journeyID` |
| Nod-ID | `_experience.journeyOrchestration.stepEvents.nodeID` |

+++

### E-post levererad

Den här händelsen spårar när ett e-postmeddelande har levererats till en persons e-posttjänst.

Händelsetyp: `directMarketing.emailDelivered `

+++Fält

| Fält | Fälttyp |
| ----- | ---------- |
| Identifierare | `_id` |
| Händelsetyp | `eventType` |
| Tidsstämpel | `timestamp` |
| Person-ID | `personID` |
| Personens käll-ID | `personKey.sourceID` |
| Typ av personkälla | `personKey.sourceType` |
| Instans-ID för personkälla | `personKey.sourceInstanceID` |
| Personkällnyckel | `personKey.sourceKey` |
| ID för utskickskälla | `directMarketing.mailingKey.sourceID` |
| Källtyp för brev | `directMarketing.mailingKey.sourceType` |
| Instans-ID för utskickskälla | `directMarketing.mailingKey.sourceInstanceID` |
| Källnyckel för e-post | `directMarketing.mailingKey.sourceKey` |
| Utskicksnamn | `directMarketing.mailingName` |
| Rese-ID | `_experience.journeyOrchestration.stepEvents.journeyID` |
| Nod-ID | `_experience.journeyOrchestration.stepEvents.nodeID` |

+++

### E-post öppnad

Den här händelsen spårar när en person öppnar ett marknadsföringsmeddelande.

Händelsetyp: `directMarketing.emailOpened`

+++Fält

| Fält | Fälttyp |
| ----- | ---------- |
| Identifierare | `_id` |
| Händelsetyp | `eventType` |
| Tidsstämpel | `timestamp` |
| Person-ID | `personID` |
| Personens käll-ID | `personKey.sourceID` |
| Typ av personkälla | `personKey.sourceType` |
| Instans-ID för personkälla | `personKey.sourceInstanceID` |
| Personkällnyckel | `personKey.sourceKey` |
| ID för utskickskälla | `directMarketing.mailingKey.sourceID` |
| Källtyp för brev | `directMarketing.mailingKey.sourceType` |
| Instans-ID för utskickskälla | `directMarketing.mailingKey.sourceInstanceID` |
| Källnyckel för e-post | `directMarketing.mailingKey.sourceKey` |
| Utskicksnamn | `directMarketing.mailingName` |
| Är mobil enhet | `device.isMobileDevice` |
| Enhetsmodell | `device.model` |
| Användaragent | `environment.browserDetails.userAgent` |
| Operativsystem | `environment.operatingSystem` |
| Rese-ID | `_experience.journeyOrchestration.stepEvents.journeyID` |
| Nod-ID | `_experience.journeyOrchestration.stepEvents.nodeID` |

+++

### E-post klickad

Den här händelsen spårar när en person klickade på en länk i ett marknadsföringsmeddelande.

Händelsetyp: `directMarketing.emailClicked`

+++Fält

| Fält | Fälttyp |
| ----- | ---------- |
| Identifierare | `_id` |
| Händelsetyp | `eventType` |
| Tidsstämpel | `timestamp` |
| Person-ID | `personID` |
| Personens käll-ID | `personKey.sourceID` |
| Typ av personkälla | `personKey.sourceType` |
| Instans-ID för personkälla | `personKey.sourceInstanceID` |
| Personkällnyckel | `personKey.sourceKey` |
| ID för utskickskälla | `directMarketing.mailingKey.sourceID` |
| Källtyp för brev | `directMarketing.mailingKey.sourceType` |
| Instans-ID för utskickskälla | `directMarketing.mailingKey.sourceInstanceID` |
| Källnyckel för e-post | `directMarketing.mailingKey.sourceKey` |
| Utskicksnamn | `directMarketing.mailingName` |
| Länk-URL | `directMarketing.linkURL` |
| Är mobil enhet | `device.isMobileDevice` |
| Modell | `device.model` |
| Användaragent | `environment.browserDetails.userAgent` |
| Operativsystem | `environment.operatingSystem` |
| Rese-ID | `_experience.journeyOrchestration.stepEvents.journeyID` |
| Nod-ID | `_experience.journeyOrchestration.stepEvents.nodeID` |

+++

### E-post studsade

Den här händelsen spåras när ett e-postmeddelande skickas till en person.

Händelsetyp: `directMarketing.emailBounced`

+++Fält

| Fält | Fälttyp |
| ----- | ---------- |
| Identifierare | `_id` |
| Händelsetyp | `eventType` |
| Tidsstämpel | `timestamp` |
| Person-ID | `personID` |
| Personens käll-ID | `personKey.sourceID` |
| Typ av personkälla | `personKey.sourceType` |
| Instans-ID för personkälla | `personKey.sourceInstanceID` |
| Personkällnyckel | `personKey.sourceKey` |
| ID för utskickskälla | `directMarketing.mailingKey.sourceID` |
| Källtyp för brev | `directMarketing.mailingKey.sourceType` |
| Instans-ID för utskickskälla | `directMarketing.mailingKey.sourceInstanceID` |
| Källnyckel för e-post | `directMarketing.mailingKey.sourceKey` |
| Utskicksnamn | `directMarketing.mailingName` |
| E-post | `directMarketing.email` |
| E-poststudentkod | `directMarketing.emailBouncedCode` |
| E-poststudsade detaljer | `directMarketing.emailBouncedDetails` |
| Rese-ID | `_experience.journeyOrchestration.stepEvents.journeyID` |
| Nod-ID | `_experience.journeyOrchestration.stepEvents.nodeID` |

+++

### E-poststudsade mjuka

Den här händelsen spårar när ett e-postmeddelande till en person studsar på skärmen.

Händelsetyp: `directMarketing.emailBouncedSoft`

+++Fält

| Fält | Fälttyp |
| ----- | ---------- |
| Identifierare | `_id` |
| Händelsetyp | `eventType` |
| Tidsstämpel | `timestamp` |
| Person-ID | `personID` |
| Personens käll-ID | `personKey.sourceID` |
| Typ av personkälla | `personKey.sourceType` |
| Instans-ID för personkälla | `personKey.sourceInstanceID` |
| Personkällnyckel | `personKey.sourceKey` |
| ID för utskickskälla | `directMarketing.mailingKey.sourceID` |
| Källtyp för brev | `directMarketing.mailingKey.sourceType` |
| Instans-ID för utskickskälla | `directMarketing.mailingKey.sourceInstanceID` |
| Källnyckel för e-post | `directMarketing.mailingKey.sourceKey` |
| Utskicksnamn | `directMarketing.mailingName` |
| E-post | `directMarketing.email` |
| E-poststudentkod | `directMarketing.emailBouncedCode` |
| E-poststudsade detaljer | `directMarketing.emailBouncedDetails` |
| Rese-ID | `_experience.journeyOrchestration.stepEvents.journeyID` |
| Nod-ID | `_experience.journeyOrchestration.stepEvents.nodeID` |

+++

### Avbeställ e-post

Den här händelsen spårar när en person säger upp prenumerationen på ett marknadsföringsmejl.

Händelsetyp: `directMarketing.emailUnsubscribed `

+++Fält

| Fält | Fälttyp |
| ----- | ---------- |
| Identifierare | `_id` |
| Händelsetyp | `eventType` |
| Tidsstämpel | `timestamp` |
| Person-ID | `personID` |
| Personens käll-ID | `personKey.sourceID` |
| Typ av personkälla | `personKey.sourceType` |
| Instans-ID för personkälla | `personKey.sourceInstanceID` |
| Personkällnyckel | `personKey.sourceKey` |
| ID för utskickskälla | `directMarketing.mailingKey.sourceID` |
| Källtyp för brev | `directMarketing.mailingKey.sourceType` |
| Instans-ID för utskickskälla | `directMarketing.mailingKey.sourceInstanceID` |
| Källnyckel för e-post | `directMarketing.mailingKey.sourceKey` |
| Utskicksnamn | `directMarketing.mailingName` |
| Rese-ID | `_experience.journeyOrchestration.stepEvents.journeyID` |
| Nod-ID | `_experience.journeyOrchestration.stepEvents.nodeID` |

+++

### Besök webbsidan

Den här händelsetypen är standardmetoden för att markera träffen som en sidvy.

Händelsetyp: `web.webpagedetails.pageViews`

+++Fält

| Fält | Fälttyp |
| ----- | ---------- |
| Identifierare | `_id` |
| Händelsetyp | `eventType` |
| Tidsstämpel | `timestamp` |
| Person-ID | `personID` |
| Personens käll-ID | `personKey.sourceID` |
| Typ av personkälla | `personKey.sourceType` |
| Instans-ID för personkälla | `personKey.sourceInstanceID` |
| Personkällnyckel | `personKey.sourceKey` |
| Källa-ID för webbsida | `web.webPageDetails.webPageKey.sourceID` |
| Källtyp för webbsida | `web.webPageDetails.webPageKey.sourceType` |
| Källinstans-ID för webbsida | `web.webPageDetails.webPageKey.sourceInstanceID` |
| Källnyckel för webbsida | `web.webPageDetails.webPageKey.sourceKey` |
| Webbsidans namn | `web.webPageDetails.name` |
| Webbsidans URL | `web.webPageDetails.URL` |
| Frågeparametrar för webbsidor | `web.webPageDetails.queryParameters` |
| Webbsides-ID | `web.webPageDetails.webPageID` |
| Användaragent | `environment.browserDetails.userAgent` |
| Referent-URL | `web.webReferrer.URL` |

+++

### Formulär ifyllt

Den här händelsen spårar när en person fyller i ett formulär på en webbsida.

Händelsetyp: `web.formFilledOut`

+++Fält

| Fält | Fälttyp |
| ----- | ---------- |
| Identifierare | `_id` |
| Händelsetyp | `eventType` |
| Tidsstämpel | `timestamp` |
| Person-ID | `personID` |
| Personens käll-ID | `personKey.sourceID` |
| Typ av personkälla | `personKey.sourceType` |
| Instans-ID för personkälla | `personKey.sourceInstanceID` |
| Personkällnyckel | `personKey.sourceKey` |
| Källa-ID för webbformulär | `web.fillOutForm.webFormKey.sourceID` |
| Källtyp för webbformulär | `web.fillOutForm.webFormKey.sourceType` |
| Instans-ID för webbformulärkälla | `web.fillOutForm.webFormKey.sourceInstanceID` |
| Källnyckel för webbformulär | `web.fillOutForm.webFormKey.sourceKey` |
| Webbformulär-ID | `web.fillOutForm.webFormID` |
| Namn på webbformulär | `web.fillOutForm.webFormName` |
| Frågeparametrar för webbsidor | `web.webPageDetails.queryParameters` |
| Webbsides-ID | `web.webPageDetails.webPageID` |
| Användaragent | `environment.browserDetails.userAgent` |
| Referent-URL | `web.webReferrer.URL` |

+++

### Webblänk klickad

Händelsen signalerar att Web SDK automatiskt spelar in ett länkklick.

Händelsetyp: `web.webinteraction.linkClicks`

+++Fält

| Fält | Fälttyp |
| ----- | ---------- |
| Identifierare | `_id` |
| Händelsetyp | `eventType` |
| Tidsstämpel | `timestamp` |
| Person-ID | `personID` |
| Personens käll-ID | `personKey.sourceID` |
| Typ av personkälla | `personKey.sourceType` |
| Instans-ID för personkälla | `personKey.sourceInstanceID` |
| Personkällnyckel | `personKey.sourceKey` |
| Källa-ID för webbinteraktion | `web.webInteraction.webInteractionKey.sourceID` |
| Källtyp för webbinteraktion | `web.webInteraction.webInteractionKey.sourceType` |
| Källinstans-ID för webbinteraktion | `web.webInteraction.webInteractionKey.sourceInstanceID` |
| Källnyckel för webbinteraktion | `web.webInteraction.webInteractionKey.sourceKey` |
| Länk-ID för webbinteraktion | `web.webInteraction.linkID` |
| Webblänk-URL | `web.webInteraction.linkURL` |
| Frågeparametrar för webbsidor | `web.webPageDetails.queryParameters` |
| Webbsides-ID | `web.webPageDetails.webPageID` |
| Användaragent | `environment.browserDetails.userAgent` |
| Referent-URL | `web.webReferrer.URL` |

+++

### Intressant ögonblick

Den här händelsen spårar när en intressant stund spelades in för en person.

Händelsetyp: `leadOperation.interestingMoment `

+++Fält

| Fält | Fälttyp |
| ----- | ---------- |
| Identifierare | `_id` |
| Händelsetyp | `eventType` |
| Tidsstämpel | `timestamp` |
| Person-ID | `personID` |
| Personens käll-ID | `personKey.sourceID` |
| Typ av personkälla | `personKey.sourceType` |
| Instans-ID för personkälla | `personKey.sourceInstanceID` |
| Personkällnyckel | `personKey.sourceKey` |
| Senaste datum | `leadOperation.interestingMoment.date` |
| Beskrivning av stund | `leadOperation.interestingMoment.description` |
| Tidskälla | `leadOperation.interestingMoment.source` |
| Typ av stund | `leadOperation.interestingMoment.type` |
| Rese-ID | `_experience.journeyOrchestration.stepEvents.journeyID` |
| Nod-ID | `_experience.journeyOrchestration.stepEvents.nodeID` |

+++

<!-- ## Overview video

>[!VIDEO](https://video.tv.adobe.com/v/3448637/?learn=on) -->