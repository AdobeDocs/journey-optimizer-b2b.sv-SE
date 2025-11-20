---
title: Välj upplevelsehändelser och fält
description: Välj Experience Platform-händelser och -fält för att aktivera realtidsbeslut i resor baserat på kundbeteende.
feature: Setup, Integrations
role: Admin
badgeBeta: label="Beta" type="informative" tooltip="Den här funktionen är för närvarande i en betaversion"
solution: Journey Optimizer B2B Edition, Experience Platform
exl-id: a7696d03-f4c4-4f64-8ef2-b15e59b59770
source-git-commit: 046d3648c5e482a69719d0095c297a766dd852ea
workflow-type: tm+mt
source-wordcount: '620'
ht-degree: 0%

---

# Välj upplevelsehändelser och fält

Administratörer kan välja specifika [AEP Experience Events](https://experienceleague.adobe.com/en/docs/experience-platform/xdm/classes/experienceevent){target="_blank"} och tillhörande fält i Experience Event-unionens schema. Efter markeringen kan användarna konfigurera beslutsregler så att de lyssnar på Experience Events för att aktivera dynamiska och målinriktade kampanjåtgärder baserat på händelsedata i nära realtid.

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

Ange text i fältet _[!UICONTROL Search]_för att filtrera de händelser som visas så att de matchar händelsenamnet.

![Filtrera listan med markerade händelser efter namn](./assets/configurations-xdm-classes-events-search.png){width="600" zoomable="yes"}

### Lägg till en händelse

Om du vill göra en Experience Event tillgänglig för en _Lyssna efter en händelse_-nod under en resa, markerar du händelsen och de fält som stöds.

>[!NOTE]
>
>I betaversionen kan du inte ta bort händelser från listan. Se till att alla händelser du lägger till är avsedda att användas av organisationen.

1. Klicka på **[!UICONTROL Select experience event]** överst till höger.

   Sidan med händelseinformation visas. På den här sidan kan du välja händelsetyp och fält.

   ![Händelseinformation för en ny händelse](./assets/configurations-xdm-classes-events-select-new.png){width="700" zoomable="yes"}

1. Välj händelsetyp.

   * Klicka på **[!UICONTROL Select event type]**.

   * Välj händelsetyp i dialogrutan.

     Använd fältet _[!UICONTROL Search]_för att filtrera den visade listan efter namn. Använd skjutreglaget **[!UICONTROL Only show selected fields]**för att granska de aktuella markeringarna.

     ![Dialogrutan Välj händelsetyp](./assets/configurations-xdm-classes-select-event-type-dialog.png){width="450" zoomable="yes"}

   * Klicka på **[!UICONTROL Select]**.

1. Välj ett eller flera fält för händelsetypen.

   * Klicka på **[!UICONTROL Select fields]**.

   * I dialogrutan väljer du de fält som du vill använda som begränsningar för matchande händelser.

     Använd fältet _[!UICONTROL Search]_för att filtrera den visade listan efter namn. Använd skjutreglaget **[!UICONTROL Only show selected fields]**för att granska de aktuella markeringarna.

     ![Dialogrutan Välj fält](./assets/configurations-xdm-classes-select-fields-dialog.png){width="450" zoomable="yes"}

   * Klicka på **[!UICONTROL Select]**.

1. Klicka på **[!UICONTROL Save]** på sidan med händelseinformation.

Den sparade händelsen visas i listan på fliken _[!UICONTROL Events]_.

### Redigera en händelse

Redigera händelseinformationen för att ändra fälten.

1. Klicka på händelsenamnet eller klicka på ikonen _Mer meny_ ( **...** ) och välj **[!UICONTROL Edit]**.

   ![Klicka på ikonen Mer på menyn ](./assets/configurations-xdm-classes-events-more-menu.png){width="500" zoomable="yes"}

1. Klicka på **[!UICONTROL Edit fields]** om du vill lägga till fler fält eller ta bort befintliga markeringar i dialogrutan _[!UICONTROL Select fields]_.

1. Klicka på **[!UICONTROL Select]** om du vill spara dina val.

### Ta bort en händelse

>[!NOTE]
>
>I Beta-versionen av den här funktionen kan du inte ta bort en händelse från listan med markerade händelser. Händelseborttagning planeras för GA-versionen.

<!-- ## Overview video

>[!VIDEO](https://video.tv.adobe.com/v/3448637/?learn=on) -->