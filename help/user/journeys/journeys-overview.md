---
title: Resehantering
description: Effektivisera efterfrågegenereringen med resor - skapa, publicera, hantera inköpsgruppsengagemang via e-post, SMS och event i Journey Optimizer B2B edition.
feature: Account Journeys
role: User
exl-id: 5c22f11f-1967-4b55-8aee-16371173c040
source-git-commit: 6511f40329df34db665ed6f971fa20670be0ae32
workflow-type: tm+mt
source-wordcount: '1443'
ht-degree: 0%

---


# Resehantering

I Journey Optimizer B2B edition är resor automatiserade, flerstegskonton och ledsbaserade marknadsföringsplaner som samordnar personaliserade upplevelser över alla kanaler som svar på engagemang, affärsevenemang och schemalagda kampanjer. Definiera säljdrivet engagemang som inkluderar e-post, SMS och mycket mer för att koordinera inkommande marknadsföring med utgående försäljningsaktiviteter för varje medlem i köpgruppen.

Journey Optimizer B2B edition har stöd för två typer av resor:

* **Kontoresor** - Effektivisera generering av efterfrågan och köp av gruppkvalificering och öka den kvalificerade efterfrågan för dina förvärvs-, merförsäljnings-/korsförsäljningsprogram samt lojalitetsprogram. Skräddarsy era resor för varje inköpsgrupp och medlem i inköpsgruppen med hjälp av automatiserat engagemang via e-post, SMS, event med mera.

  ![Video](../../assets/do-not-localize/icon-video.svg){width="30"} [Titta på videofilmen om kontoresan](#overview-video)

* **Personresor** - (Beta) Samordna ledande marknadsföring med Experience Platform målgrupper och data. Med personresor är era marknadsföringsaktiviteter inte beroende av Marketo Engage eller tillfälliga lösningar för Adobe Campaign/B2C-verktygskedjor så att de kan arbeta med B2B-användningsfall.

  När en personresa används tillsammans med kontoresor och inköpsgrupper kan marknadsförarna få möjlighet att använda fullständig samordning på köpresan.

  +++Aktuella begränsningar för personresor

  Det finns begränsningar som kan blockera vissa användningsfall eller göra det svårt att skapa personresor. Många problem beror på den initiala betaprogramsimplementeringen som kommer att åtgärdas i framtiden.

   * Händelser kan inte kombineras med profilattribut för att begränsa målgruppsdefinitioner.
   * Kontexten för händelsen som kvalificerar en profil för en resa kan inte användas för personalisering eller samordning.
   * Resor kan för närvarande inte ha både ett villkor för en händelse och ett profilsegment.
   * Händelseavlyssnare kan inte lyssna efter flera händelser.
   * Det finns för närvarande inga alternativ för veckodag eller tidpunkt för dagens avslutningskriterier i Wait-noder.
   * E-postredigeraren refererar felaktigt till funktioner och attribut som bara är tillgängliga för kontoresor
   * Stöd för anpassade resetoken (_Mina token_) är inte tillgängligt än.
   * Noderna Lägg till och Ta bort från personresa är för närvarande inte tillgängliga från någon av resetyperna.
   * Händelsehistorik kan inte användas för samordning eller personalisering.
   * Relaterade objekt (t.ex. konto, inköpsgrupp, affärsmöjlighet och anpassade objekt) kan inte användas för samordning eller personalisering.
   * Webb-, SMS- och annonsplattformskanaler stöds för närvarande inte.

  +++

## Kom igång med en resa

Så här kommer du igång med din första resa:

1. [Skapa en resa](./create-publish-journey.md#create-a-journey).
1. [Lägg till noderna](./create-publish-journey.md#add-a-node) och [definiera reseflödet](./create-publish-journey.md#add-and-delete-a-path) i färdkartan.
1. [Publicera resan](./create-publish-journey.md#publish-a-journey).

## Få åtkomst till och bläddra bland dina resor

>[!BEGINTABS]

>[!TAB Kontoresor]

Expandera **[!UICONTROL Journey Management]** till vänster och klicka på **[!UICONTROL Account journeys]**.

Ange text i _sökverktyget_ längst upp i listan om du vill filtrera den visade listan efter namn.

![Filtrera kontoreselistan](./assets/account-journeys-list-search-filter.png){width="800" zoomable="yes"}

>[!TAB Personresor (Beta)]

[!BADGE Beta]{type=Informative tooltip="Finns som betaversion av den förenklade arkitekturen"}

Expandera **[!UICONTROL Journey Management]** till vänster och klicka på **[!UICONTROL Person journeys]**.

Ange text i _sökverktyget_ längst upp i listan om du vill filtrera den visade listan efter namn.

![Filtrera personreselistan](./assets/person-journeys-list-search-filter.png){width="800" zoomable="yes"}

>[!ENDTABS]

### Reselistkolumner

Sidan med reselistan innehåller följande kolumner:

* [!UICONTROL Name] (klicka på namnet för att öppna resan för redigering)
* [!UICONTROL Status]
* [!UICONTROL Creation date]
* [!UICONTROL Created by]
* [!UICONTROL Last update]
* [!UICONTROL Last updated by]
* [!UICONTROL Published on]
* [!UICONTROL Published by]
* [!UICONTROL Start date]
* [!UICONTROL End date]

Du kan sortera listan efter _[!UICONTROL Status]_,_[!UICONTROL Creation date]_ eller _[!UICONTROL Last update]_&#x200B;genom att klicka på kolumnrubriken.

Om du vill anpassa (visa/dölja) de kolumner som visas i tabellen klickar du på ikonen _Anpassa tabell_ ( ![Anpassa tabell](../assets/do-not-localize/icon-column-settings.svg) ) i det övre högra hörnet. Markera eller avmarkera kryssrutorna i dialogrutan och klicka på **[!UICONTROL Apply]**.

![Välj vilka kolumner som ska visas i reselistan](./assets/account-journeys-list-columns.png){width="800" zoomable="yes"}

### Resestatus

Status för en resa kan ändras beroende på vilka åtgärder du vidtar. Beroende på statusen för en resa är vissa åtgärder inte tillgängliga från den högra sidan av huvudet.

| Status | Beskrivning | Tillgängliga åtgärder |
| ------ | ----------- | ----------------- |
| _&#x200B;**Utkast**&#x200B;_ | En opublicerad resa som är redigerbar. | <li>[Publicera](./create-publish-journey.md#publish-a-journey)<li>[Duplicera](#duplicate-journey) <li>[Ta bort](#delete-journey) |
| _&#x200B;**Live**&#x200B;_ | Resans status ändras från _Utkast_ till _Live_ när en resa publiceras. I det här läget går det inte längre att redigera. | <li>[Duplicera](#duplicate-journey)<li>[Stäng till nya poster](#close-to-new-entries) <li>[Avbryt](#abort-journey) |
| _&#x200B;**Stängda till nya poster**&#x200B;_ | Resursstatusen ändras från _Live_ till _Stängd till nya poster_ när du klickar på [!UICONTROL Close to new entries] i den övre navigeringen. | <li>[Duplicera](#duplicate-journey) <li>[Avbryt](#abort-journey) |
| _&#x200B;**Avbruten**&#x200B;_ | Resans status ändras från _Live_ eller _Stängd till nya poster_ när du avbryter en resa. En avbruten resa kan inte startas om. | <li>[Duplicera](#duplicate-journey) <li>[Ta bort](#delete-journey) |
| _&#x200B;**Slutförd**&#x200B;_ | När alla konto- eller målgruppsmedlemmar på en resa slutför resan ändras statusen från _Live_ eller _Stängd till nya poster_ till _Slutförd_. | <li>[Duplicera](#duplicate-journey) <li>[Ta bort](#delete-journey) |

## Resekartor

Klicka på namnet (visas som en länk) i reselistan för att granska detaljer, göra ändringar och vidta åtgärder.

![Arbetsyta för kontoresa](./assets/account-journey-workspace.png){width="800" zoomable="yes"}

Rubriken för varje färdplan omfattar:

* Resensnamn
* Redigera verktyg för resenamnet ( ikonen ![Redigera &#x200B;](../assets/do-not-localize/icon-edit.svg) _Redigera_ )
* [Status](#journey-status) för resan

Från färdkartan kan du [lägga till noderna](./create-publish-journey.md#add-a-node) och [definiera reseflödet](./create-publish-journey.md#add-and-delete-a-path).

## Reseåtgärder

På sidan med reselistan finns alla konto- eller personresor i din instans av Journey Optimizer B2B edition. På listsidan kan du använda ett antal åtgärder på en resa.

### Avbryta resan

Om du avbryter (stoppar) en live eller planerad resa avbryter konton eller personer på resan omedelbart deras framsteg och ingen ytterligare reseentré kan ske. En avbruten resa kan inte startas om.

>[!IMPORTANT]
>
>När resan används i en annan resa från en _Utför en åtgärd_-nod med åtgärden _[!UICONTROL Add Account to (other) Journey]_&#x200B;och avbryter den åtgärden i den resan.

1. Klicka på resenamnet för att öppna det.

1. Klicka på menyn **[!UICONTROL More...]** längst upp till höger och välj **[!UICONTROL Abort]**.

   ![Klicka på Mer längst upp till höger](./assets/account-journey-live-more-menu.png){width="450"}

1. Klicka på **[!UICONTROL Abort]** i bekräftelsedialogrutan.

### Stäng till nya poster

Om du stänger en live-resa fortsätter konton som för närvarande befinner sig på resan att ta sin väg på den resan och ingen ytterligare reseentré kan ske. Det går inte att starta om en stängd resa. Du kan duplicera en stängd resa.

>[!IMPORTANT]
>
>När resan används i en annan resa från en _Utför en åtgärd_-nod med åtgärden _[!UICONTROL Add Account to (other) Journey]_&#x200B;och stänger den till nya poster blockerar åtgärden från den resan.

1. Klicka på resenamnet för att öppna det.

1. Klicka på menyn **[!UICONTROL More...]** längst upp till höger och välj **[!UICONTROL Close to new entries]**.

1. Klicka på **[!UICONTROL Close to new entries]** i bekräftelsedialogrutan.

### Duplicera en resa

En duplicerad åtgärd liknar en klonfunktion, men en duplicerad resa innehåller inte något skapat innehåll för resan. Du kan duplicera informationen för resan eller bara en enkel _skelett_ av flödes- och sökvägsstrukturen.

>[!NOTE]
>
>Den här åtgärden är för närvarande inte tillgänglig för personresor.

1. Klicka på ikonen _Mer_ (**..**) bredvid resans namn och välj **[!UICONTROL Duplicate]**.

   ![Klicka på ...-ikonen och välj Duplicera](./assets/account-journeys-list-more-menu.png){width="450"}

   Beroende på resans status kan du även komma åt den duplicerade åtgärden från reseinformationen eller färdkartan:

   * Klicka på menyn **[!UICONTROL More...]** längst upp till höger och välj **[!UICONTROL Duplicate]** för ett utkast.

   * Klicka **[!UICONTROL Duplicate]** längst upp till höger för alla andra statuslägen för resan.

     ![Klicka på Duplicera överst till höger](./assets/account-journey-duplicate-button.png){width="450"}

1. I dialogrutan _Duplicera resa_ anger du **[!UICONTROL Name]** och **[!UICONTROL Description]** för den nya resan.

   Som standard används namnet på den duplicerade resan som har lagts till med __copy_ i dialogrutan. Ange ett annat unikt namn för resan efter behov.

   ![Dialogrutan Duplicera resa](./assets/account-journey-duplicate-dialog.png){width="400"}

1. Välj dupliceringen **[!UICONTROL Type]**:

   * **[!UICONTROL Partial content duplication]** - Använd den här typen om du vill kopiera allt på resan, exklusive skapade e-postmeddelanden eller SMS-meddelanden. Noder som refererar till ett Marketo Engage-mejl eller SMS är helt intakta.

   * **[!UICONTROL Duplicate without details]** - Använd den här typen för att endast kopiera nodstrukturen och sökvägarna. Alla nodinställningar och sökvägsvillkor är odefinierade (standard), så att du kan återanvända basflödet med olika inställningar för målgrupper, åtgärder och bansegmentering. Alla _Wait_-noder använder standardvärdet på fem dagar.

1. Klicka på **[!UICONTROL Duplicate]**.

   Den duplicerade resan öppnas i färdkartan, där du kan ange detaljer och skapa reseinnehåll efter behov.

### Ta bort en resa

Använd en raderingsåtgärd för att ta bort en resa permanent. Du kan inte ta bort en direktsänd eller schemalagd resa.

1. Klicka på ikonen _Mer_ (**..**) bredvid resans namn och välj **[!UICONTROL Delete]**.

   Beroende på resans status kan du även komma åt borttagningsåtgärden från reseinformationen eller färdkartan:

   * Klicka på menyn **[!UICONTROL More...]** längst upp till höger och välj **[!UICONTROL Delete]** för ett utkast.

   * Klicka _längst upp till höger för andra status för resan, till exempel_ Slutförd _eller_ Avbruten **[!UICONTROL Delete]**.

1. Klicka på **[!UICONTROL Delete]** i bekräftelsedialogrutan.

## Granska kontostatus

För en publicerad kontoresa som finns i en _Live_-, _Stängd på nya poster_-, _Avbruten_- eller _Färdig_-status kan du öppna färdplanen för att granska kontostatus för kundnoderna. Varje nod på kartan visar antalet konton som ska nå den noden och, för direktresor, antalet konton på den noden.

![Förloppsinformation för resenodkonto](./assets/node-account-progression-observability.png){width="400"}

När du markerar noden klickar du på numret för att visa en lista över konton som har angetts i noden eller som för närvarande befinner sig i det steget av resan.

![Förloppsinformation för resenodkonto](./assets/node-accounts-entered-list.png){width="700" zoomable="yes"}

## Översikt över kontoresan - video {#overview-video}

>[!VIDEO](https://video.tv.adobe.com/v/3443211/?captions=swe&learn=on)
