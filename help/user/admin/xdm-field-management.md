---
title: XDM-fälthantering
description: Använd XDM-fälthantering för att styra vilka data som är tillgängliga för Journey Optimizer B2B edition.
feature: Data Management, Integrations
role: User
badgeBeta: label="Beta" type="informative" tooltip="Den här funktionen är för närvarande i en begränsad betaversion"
source-git-commit: 046d3648c5e482a69719d0095c297a766dd852ea
workflow-type: tm+mt
source-wordcount: '944'
ht-degree: 0%

---


# XDM-fälthantering

XDM-fält (Experience Data Model) är schemaelement som tillhandahåller data till programmet [!DNL Journey Optimizer B2B Edition]. Använd XDM-fält som filter och begränsningar för resor, inköpsgrupper och funktioner, som e-postpersonalisering och villkorat innehåll.

Scheman definierar fält baserade på standard-XDM-klasser. Standard-XDM-klasserna omfattar Individual Profile, Business Account och Experience Event. Relationsscheman definierar även fält som gör att du kan modellera strukturerade data på liknande sätt som traditionella relationsdatabaser.

Adobe Experience Platform (AEP)-scheman innehåller vanligtvis många fält i komplexa hierarkier. Det tar tid att gå igenom XDM-schematräd. XDM-fälthantering effektiviserar fältvalet genom att endast visa fält som är relevanta för varje resa. Administratörer styr vilka fält som visas för personer som skapar resan. Administratörer kan även ange att fält ska vara skrivskyddade eller redigerbara. Dessa åtgärder förbättrar effektiviteten under utformningen av kundresan.

Administratörer som förstår XDM och samarbetar med datatekniker eller intressenter för CDP-datamodellering (B2B customer data platform) bör använda procedurerna på den här sidan.

>[!NOTE]
>[Relationsscheman](https://experienceleague.adobe.com/en/docs/experience-platform/xdm/schema/relational#) är tillgängliga för [!DNL Journey Optimizer B2B Edition] som en begränsad version. Data Mirror och relationsscheman är tillgängliga för innehavare av Journey Optimizer Orchestrated-kampanjlicenser. Relationsscheman är också tillgängliga som en begränsad release för Customer Journey Analytics-användare, beroende på din licens och aktivering av funktioner. Kontakta din Adobe-representant för att få åtkomst.

## Åtkomst till XDM-klasser

1. Välj **[!UICONTROL Administration]** > **[!UICONTROL Configuration]** i den vänstra navigeringen.

1. Klicka på **[!UICONTROL XDM Classes]** på panelen mellan.

   * Använd flikarna **[!UICONTROL Standard]** och **[!UICONTROL Relational]** för att lägga till nya fält och göra dem tillgängliga i Journey Optimizer B2B edition.

   * Använd fliken **Händelser** för att [välja specifika AEP Experience Events och tillhörande fält](./configure-aep-events.md) som ska användas för reseventnoder.

## Fältval

>[!IMPORTANT]
>
>Du kan när som helst uppdatera fältvalet genom att markera nya fält eller avmarkera fält som du inte längre behöver. När du publicerar en resa med det här schemat låser du schemastrukturen. Det går inte att ta bort eller byta namn på schemat, lägga till nya fält eller ändra fälttyper, vilket kan leda till att resan misslyckas.

Använd följande riktlinje för att göra fältmarkeringar:

* Du kan bara lägga till nya fält efter att ett schema aktivt används under en resa.
* Om du tar bort, byter namn på eller ändrar fälttyper kan det medföra problem med resefunktionen. Var försiktig när du manipulerar scheman.
* Byt inte namn på eller ta bort scheman och ändra inte nycklar i relationsscheman.

### Standardklasser

På fliken _[!UICONTROL Standard]_kan du redigera_ hanterade fält _och_ uppdateringsbara fält _för standardklasserna:

* Hanterade fält visas på resor, i inköpsgrupper och i personaliseringsfunktioner.
* Uppdateringsbara fält fungerar som begränsningar för noderna _Uppdatera kontoprofil_ och _Uppdatera personprofil_.

![Fliken Standardklasser som visar konfigurationen för XDM-klassen](assets/xdm-standard.png){width="600" zoomable="yes"}

Listan innehåller två klasser:

* **[!UICONTROL XDM Individual Profile]**
* **[!UICONTROL XDM Business Account]**

Den klassinformation som visas omfattar:

* Antal hanterade fält
* Antal uppdateringsbara fält
* Senaste uppdateringstid

Om du vill välja fält från unionsschemat för standard-XDM-klasser klickar du på klassnamnet för att öppna dialogrutan _Hanterade fält_ eller klickar på ikonen _Mer meny_ ( **...** ) för att välja mellan _[!UICONTROL Managed fields]_och_[!UICONTROL Updatable fields]_.

![Klicka på ikonen Mer för att välja mellan hanterade fält och uppdateringsbara fält](./assets/xdm-classes-standard-more-menu.png){width="550" zoomable="yes"}

>[!NOTE]
>
>Ett fält måste först vara _hanterat_ innan det kan vara _uppdateringsbart_. De _uppdateringsbara fält_ som du väljer måste finnas i det schema som användaren tillhandahåller.

#### Hanterade fält

När du väljer **[!UICONTROL Managed fields]** visas alla konfigurerbara fält i dialogrutan _Välj fält_.

1. Välj upp till 100 fält för varje XDM-klass.

   Använd fältet _[!UICONTROL Search]_för att filtrera den visade listan efter namn. Använd skjutreglaget **[!UICONTROL Only show selected fields]**för att granska de aktuella markeringarna.

   ![Dialogrutan för val av hanterade fält för standard-XDM-klasser som visar alternativ för konfigurerbara fält](assets/xdm-standard-managed-fields.png){width="450" zoomable="yes"}

1. Klicka på **[!UICONTROL Save]** för att bekräfta dina val.

#### Uppdateringsbara fält

När du väljer **[!UICONTROL Updatable fields]** kan du välja fält från andra datakällor i dialogrutan _Markera fält_.

1. För **[!UICONTROL Datasets]** väljer du den datakälla som du vill konfigurera.
1. Redigera fälten från den markerade datauppsättningen.

   ![Dialog för att välja uppdateringsbara fält från datauppsättningar i XDM-schemakonfigurationen](./assets/xdm-select-updateable.png){width="450" zoomable="yes"}

1. Klicka på **[!UICONTROL Save]** för att tillämpa ändringarna.

### Relationsscheman

Med Relationsscheman kan du skapa anpassade dataklasser. Med tillgång till flera datauppsättningar kan du skapa klasser som är särskilt anpassade efter dina databehov. Använd relationsscheman för affärsenheter som inköp, licenser och händelseregistreringar i resebeslut och e-postpersonalisering. Du kan välja upp till 50 scheman och upp till 100 fält per schema.

>[!NOTE]
>
>Den här funktionen har för närvarande stöd för kontorelaterade anpassade användningsfall för objekt, med planer på att i framtiden stödja fler körklara användningsfall för objekt.

Du kan skapa relationsscheman med schemaredigeraren (gå till **[!UICONTROL Data Management]** > **[!UICONTROL Schemas]** i den vänstra navigeringen).

När du skapar ett schema för användning med [!DNL Journey Optimizer B2B Edition] krävs följande konfigurationsvärden:

* Beteende: Post
* Segmentering: Aktiverad
* Relationstyp: många-till-ett
* Referensschema: B2B-konto
* Obligatoriska fält: Primär nyckel, sekundärnyckel och versionsbeskrivning
* Associerad datauppsättning: Definierad och mappad till schemat

Så här väljer du relationsschemafält som ska användas i [!DNL Journey Optimizer B2B Edition]:

1. Välj fliken **[!UICONTROL Relational]** för att visa dina scheman.

   ![Fliken Relationsscheman i Schemaredigeraren visar företagsenhetsfält för Adobe Journey Optimizer B2B edition](assets/xdm-relational.png){width="600" zoomable="yes"}

1. Klicka på **[!UICONTROL Select relational XDM schema]**.

   >[!NOTE]
   >
   >I den här betafunktionen stöds bara _Account many-to-one Custom Objects_.

1. Välj ett relationsschema och klicka på **[!UICONTROL Next]**.

   >[!NOTE]
   >
   >I den här betafunktionen kan du inte ta bort ett schema från listan efter att du har valt det.

   ![Välj ett relationsschema i dialogrutan](./assets/xdm-classes-relational-select-schema-dialog.png){width="500" zoomable="yes"}

1. Ange ett namnutrymme eller använd standardnamnutrymmet. Klicka på **[!UICONTROL Next]**.

   Du kan bara ange namnutrymmet en gång och kan inte ångra den här åtgärden.

   ![Standardnamnutrymmet i dialogrutan Skapa namnutrymme](./assets/xdm-classes-relational-create-namespace.png){width="400" zoomable="yes"}

1. Granska relationsschemafälten.

   Klicka på ikonen _Info_ ![Info](../assets/do-not-localize/icon-info-light.svg) för att visa fältets metadata.

1. Välj de fält som ska aktiveras för resor och personalisering.

   Plattformen väljer automatiskt följande obligatoriska fält:

   * Sekundärnyckel
   * Primär nyckel
   * Versionsbeskrivare

   Använd fältet _[!UICONTROL Search]_för att filtrera den visade listan efter namn. Använd skjutreglaget **[!UICONTROL Only show selected fields]**för att granska de aktuella markeringarna.

   ![Välj fält för relationsschemat i dialogrutan](./assets/xdm-classes-relational-select-schema-fields.png){width="500" zoomable="yes"}

1. Klicka på **[!UICONTROL Save]**.
