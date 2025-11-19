---
title: XDM-fälthantering
description: Använd XDM-fälthantering för att styra vilka data som är tillgängliga för Journey Optimizer B2B edition.
feature: Data Management, Integrations
role: User
badgeBeta: label="Beta" type="informative" tooltip="Den här funktionen är för närvarande i en begränsad betaversion"
source-git-commit: de7f5620556a48fe6f12ed1c70e925e11ec770f1
workflow-type: tm+mt
source-wordcount: '990'
ht-degree: 0%

---


# XDM-fälthantering

XDM-fält (Experience Data Model) är schemaelement som tillhandahåller data till programmet [!DNL Journey Optimizer B2B Edition]. Du använder XDM-fält som filter och begränsningar för resor, inköpsgrupper och funktioner, som e-postpersonalisering och villkorat innehåll.

Scheman definierar fält baserade på standard-XDM-klasser. Standard-XDM-klasserna omfattar Individual Profile, Business Account och Experience Event. Relationsscheman definierar även fält som gör att du kan modellera strukturerade data på liknande sätt som traditionella relationsdatabaser.

Adobe Experience Platform (AEP)-scheman innehåller vanligtvis många fält i komplexa hierarkier. Det tar tid att gå igenom XDM-schematräd. XDM-fälthantering effektiviserar fältvalet genom att endast visa fält som är relevanta för varje resa. Administratörer styr vilka fält som visas för personer som skapar resan. Administratörer kan även ange att fält ska vara skrivskyddade eller redigerbara. Dessa åtgärder förbättrar effektiviteten under utformningen av kundresan.

Administratörer som förstår XDM och samarbetar med datatekniker eller intressenter för CDP-datamodellering (B2B customer data platform) följer procedurerna i den här handboken.

>[!NOTE]
>[Relationsscheman](https://experienceleague.adobe.com/en/docs/experience-platform/xdm/schema/relational#) är tillgängliga för [!DNL Journey Optimizer B2B Edition] som en begränsad version. Data Mirror och relationsscheman är tillgängliga för innehavare av Journey Optimizer Orchestrated-kampanjlicenser. Relationsscheman är också tillgängliga som en begränsad release för Customer Journey Analytics-användare, beroende på din licens och aktivering av funktioner. Kontakta din Adobe-representant för att få åtkomst.

## Åtkomst till XDM-klasser

Om du vill öppna XDM-fälthanteringsområdet går du till **Konfigurationer** > INSTÄLLNINGAR > **XDM-klasser**.

* Du kan bara lägga till nya fält efter att ett schema aktivt används under en resa.
* Om du tar bort, byter namn på eller ändrar fälttyper kan det medföra problem med resefunktionen. Var försiktig när du manipulerar scheman.
* Byt inte namn på eller ta bort scheman och ändra inte nycklar i relationsscheman.

>[!IMPORTANT]
>Du kan när som helst uppdatera fältvalet genom att markera nya fält eller avmarkera fält som du inte längre behöver. När du har publicerat en resa med det här schemat låser du schemastrukturen. Det går inte att ta bort eller byta namn på schemat, lägga till nya fält eller ändra fälttyper, vilket kan leda till att resan misslyckas.

## Standardklasser

På fliken Standardklasser kan du redigera _hanterade fält_ och _uppdateringsbara fält_.

* Hanterade fält visas på resor, i inköpsgrupper och i personaliseringsfunktioner.
* Uppdateringsbara fält fungerar som begränsningar för noderna _Uppdatera kontoprofil_ och _Uppdatera personprofil_.

![Fliken Standardklasser som visar hanterade och uppdateringsbara fält för XDM-klasskonfigurationen](assets/xdm-standard.png){width="600" zoomable="yes"}

Följ de här stegen för att välja fält från unionsschemat för standard-XDM-klasser:

1. Gå till **Administration** > **Konfigurationer** > **XDM-klasser**.
1. Öppna fliken **Standard**. Välj någon av följande klasser:

   * Individuell XDM-profil
   * XDM Business Account

Tabellen innehåller information om:

* Antal hanterade fält
* Antal uppdateringsbara fält
* Senaste uppdateringstid

Klicka på klassnamnet för att öppna dialogrutan _Hanterade fält_.

![Dialogrutan för val av hanterade fält för standard-XDM-klasser som visar alternativ för konfigurerbara fält](assets/xdm-standard-managed-fields.png){width="600" zoomable="yes"}

1. Klicka på menyn **..** för att växla mellan _[!UICONTROL Managed fields]_och_[!UICONTROL Updatable fields]_. I dialogrutan visas alla konfigurerbara fält.
1. Välj upp till 100 fält för varje XDM-klass.
1. Klicka på **[!UICONTROL Save]** för att bekräfta dina val.

Använd filtret [!UICONTROL Only show selected fields] om du bara vill visa aktiva fält.

För _uppdateringsbara fält_ öppnar du en separat dialogruta där du kan välja fält från andra datakällor:

1. I listrutan Datauppsättningar väljer du den datakälla som du vill konfigurera.
1. Redigera fälten från den markerade datauppsättningen.
1. Klicka på **[!UICONTROL Save]** om du vill använda ändringarna.

![Dialog för att välja uppdateringsbara fält från datauppsättningar i XDM-schemakonfigurationen](assets/xdm-select-updateable.png){width="600" zoomable="yes"}

Fältet måste först vara _hanterat_ innan det kan vara _uppdateringsbart_. De _uppdateringsbara fält_ som du väljer måste finnas i det schema som användaren tillhandahåller.

## Relationsscheman

Med Relationsscheman kan du skapa anpassade dataklasser. Med tillgång till flera datauppsättningar kan du skapa klasser som är särskilt anpassade efter dina databehov.
Använd relationsscheman för affärsenheter som inköp, licenser och händelseregistreringar i resebeslut och e-postpersonalisering. Du kan välja upp till 50 scheman och upp till 100 fält per schema.

![Fliken Relationsscheman i Schemaredigeraren visar företagsenhetsfält för Adobe Journey Optimizer](assets/xdm-relational.png)

>[!NOTE]
>Den här funktionen har för närvarande stöd för kontorelaterade anpassade användningsfall för objekt, med planer på att ge stöd för fler körklara användningsfall för objekt i framtiden.

Skapa relationsscheman med Schemaredigeraren i **Datahantering** > **Scheman**.

Dessa konfigurationsvärden måste inkluderas när du skapar ett schema som ska användas med [!DNL Journey Optimizer B2B Edition]:

* Beteende: Post
* Segmentering: Aktiverad
* Relationstyp: många-till-ett
* Referensschema: B2B-konto
* Obligatoriska fält: Primär nyckel, sekundärnyckel och versionsbeskrivning
* Associerad datauppsättning: Definierad och mappad till schemat

### Skapa ett relationsschema

Följ de här stegen för att välja fält som ska användas i [!DNL Journey Optimizer B2B Edition]:

1. Gå till **Administration** > **Konfigurationer** > **XDM-klasser**.
1. Öppna fliken **Relation** om du vill visa dina scheman.
1. Klicka på **[!UICONTROL Select relational XDM schema]**.

   * I betaversionen stöds bara _Account many-to-one Custom Objects_.

1. Välj ett relationsschema och klicka på **[!UICONTROL Next]**.

   * I betaversionen kan du inte ta bort ett schema från listan när du har valt det.

1. Ange ett namnutrymme eller använd standardnamnutrymmet. Klicka på **[!UICONTROL Next]**.

   * Du kan bara ange namnutrymmet en gång och kan inte ångra den här åtgärden.

1. Granska relationsschemafälten. Klicka på ikonen ![Info](../assets/do-not-localize/icon-info-light.svg) [!UICONTROL Info] för att visa fältets metadata.
1. Välj de fält som ska aktiveras för resor och personalisering. Plattformen väljer automatiskt följande obligatoriska fält:

   * Sekundärnyckel
   * Primär nyckel
   * Versionsbeskrivare

1. Använd reglaget [!UICONTROL Only show selected fields] för att förhandsgranska dina val.
1. Filtrera fält efter namn med hjälp av sökfältet.
1. Klicka på **[!UICONTROL Save]**.

## Händelser

Använd Experience Events och tillhörande fält vid resebeslut. Du kan välja upp till 50 händelser och upp till 100 fält per händelse.

![Fliken Händelser som visar Experience Events-val och schemafält för resor och personalisering](assets/xdm-events.png){width="700" zoomable="yes"}

Klicka på ett händelsenamn om du vill visa information och redigera de konfigurerade fälten.

Följ de här stegen för att välja Experience Events och schemafält:

1. Gå till **Administration** > **Konfigurationer** > **XDM-klasser**.
1. Öppna fliken **Händelser**.
1. Klicka på **[!UICONTROL Select experience event]** om du vill välja fält för en händelse.
1. Klicka på **[!UICONTROL Select event type]** på informationssidan.
1. Välj din händelse i händelselistan.
1. Klicka på **[!UICONTROL Select]** för att stänga dialogrutan.

   * I betaversionen kan du inte ta bort markerade händelser.

1. Klicka på **[!UICONTROL Select fields]**.
1. Använd skjutreglaget [!UICONTROL Only show selected fields] för att visa dina aktuella markeringar.
1. Markera de fält som ska användas i [!DNL Journey Optimizer B2B Edition]. Klicka på **[!UICONTROL Select]** för att stänga dialogrutan.
1. Klicka på [!UICONTROL Save].
