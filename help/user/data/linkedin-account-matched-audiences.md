---
title: LinkedIn Account Matched Auditions
description: Lär dig hur du ansluter ett LinkedIn-konto och aktiverar ett dataflöde för inköpsgrupper.
hidefromtoc: true
hide: true
source-git-commit: 63bf202e179895d72cd8b3f40e1bf5333bcd4c48
workflow-type: tm+mt
source-wordcount: '590'
ht-degree: 0%

---

# LinkedIn Account Matched Auditions

Journey Optimizer B2B Edition ger möjlighet att generera LinkedIn Ad-målgrupper via kontomatchade målgrupper och är utformat för att hjälpa er att fylla tomma roller i era inköpsgrupper. Genom att definiera en uppsättning inköpsgruppsfilter kan du upprätthålla en LinkedIn Matched Audience för att rikta presumtiva kunder som matchar era köpgruppsparametrar. Den här funktionen utnyttjar Experience Platform Destinations för att hantera vissa aspekter av integreringen. Det finns en gräns på tio dataflöden.

Innan du initierar ett dataflöde från Journey Optimizer B2B Edition måste du ha minst en instans av [(Companies) LinkedIn Matched Audience-målkopplingen ](https://experienceleague.adobe.com/en/docs/experience-platform/destinations/catalog/social/linkedin#connect) med ett LinkedIn Campaign Manager-konto konfigurerat i ditt Experience Platform-program.

## Konfigurera en ny LinkedIn-kontoanslutning {#linkedin-destination-setup}

>[!CONTEXTUALHELP]
>id="ajo-b2b_linkedin_destination_setup"
>title="LinkedIn destinationsinställning krävs"
>abstract="Skicka konton som filtrerats genom inköpsgrupper till en länkad destination för att kunna interagera med potentiella köpgruppsmedlemmar. Du kan skapa upp till 10 dataflöden för 10 olika grupper med filtrerade konton. Om du vill komma igång med den här funktionen lägger du till ett länkat mål först."

1. I Experience Platform går du till **[!UICONTROL Connections]** > **[!UICONTROL Destinations]** i den vänstra navigeringen och väljer fliken **[!UICONTROL Catalog]**.

1. Leta reda på **[!UICONTROL (Companies) LinkedIn Matched Audience]**-kopplingen i katalogen och klicka på **[!UICONTROL Set Up]**.

   ![Åtkomst till (företag) LinkedIn Matched Audience Connector](./assets/aep-destinations-catalog-linkedin.png){width="800" zoomable="yes"}

1. Välj **[!UICONTROL New Account]** > **[!UICONTROL Connect to LinkedIn]**.

1. Ange dina LinkedIn-uppgifter och logga in.

   LinkedIn-kontot är anslutet som mål.

## Uppdatera kontoinformationen

Namnet och beskrivningen för LinkedIn-kontot visas för inköpsgrupper i Journey Optimizer B2B Edition. Det är en god vana att uppdatera denna information så att den är lätt att identifiera för de marknadsförare som arbetar med inköpsgrupper. Du kan ändra kontoinformationen i användargränssnittet för Experience Platform eller Journey Optimizer B2B Edition.

1. Gå till **[!UICONTROL Connections]** > **[!UICONTROL Destinations]** i den vänstra navigeringen och välj fliken **[!UICONTROL Accounts]**.

1. Klicka på menyn _Mer_ (**..**) för det nya kontot som du har skapat och välj **[!UICONTROL Edit details]**.

   ![Redigera kontoinformation](./assets/aep-destinations-accounts-edit-details.png){width="800" zoomable="yes"}

1. Uppdatera namn och beskrivning i dialogrutan.

   ![Redigera namnet och beskrivningen](./assets/destinations-linkedin-account-edit-details-dialog.png){width="500"}

1. Klicka på **[!UICONTROL Save]**.

## Aktivera kontot för inköpsgrupper

>[!NOTE]
>
>Om du redan har tio dataflöden kan du inte skapa ytterligare. Om du har nått maxgränsen tar du bort en i Experience Platform innan du skapar en ny i Journey Optimizer B2B Edition.

1. I Journey Optimizer B2B Edition går du till **[!UICONTROL Accounts]** > **[!UICONTROL Buying groups]** till vänster.

1. Välj fliken **[!UICONTROL Browse]**.

1. Klicka på **[!UICONTROL Activate to LinkedIn Destination]** överst till höger.

   ![Redigera kontoinformation](./assets/activate-linkedin-destination.png){width="800" zoomable="yes"}

1. Ge dataflödet ett beskrivande namn och en beskrivning (valfritt).

   När du har sparat det läggs det namn du anger för dataflödet till _AJOB2B_ som hjälp när du identifierar dataflödet i Experience Platform.

1. Ange [konto-ID:t för ditt LinkedIn Campaign Manager-konto](https://www.linkedin.com/help/lms/answer/a424270).

   Du kan hitta ditt konto-ID med ditt kontonamn i gränssnittet för Campaign Manager.

   ![Lägg till dataflödesinformation](./assets/destinations-linkedin-activate-details.png){width="700" zoomable="yes"}

1. Klicka på **[!UICONTROL Select buying group filters]** och definiera parametrarna för din kontopublik.

   >[!IMPORTANT]
   >
   >För närvarande går det inte att redigera filter efter att dataflödet har aktiverats. Dubbelkontrollera arbetet innan du aktiverar dataflödet.

   ![Ange kontomålets filtrering enligt inköpsgrupper](./assets/destinations-linkedin-activate-buying-group-filters.png){width="400"}

   För **[!UICONTROL Engagement score]** är operatorn `Between` inkluderande, liksom procentintervall. 5.1 och 5 är till exempel både _mellan_ 5 och 6.

   Tomma villkor behandlas som `Is Any`.

   Klicka på **[!UICONTROL Save]** om du vill lägga till de angivna filtren.

1. Klicka på **[!UICONTROL Select LinkedIn destination]** och välj det konfigurerade LinkedIn-mål som du vill använda.

   Vid aktivering skapar den här inställningen dataflödet med målkonfigurationen och ett motsvarande virtuellt segment.

1. Dubbelkontrollera inställningarna och klicka på **[!UICONTROL Activate]** längst upp till höger.

   Klicka på **[!UICONTROL Activate]** igen i bekräftelsedialogrutan.

   En banderoll visas med en länk till dataflödesmenyn i Experience Platform så att du kan kontrollera dataflödesposten.