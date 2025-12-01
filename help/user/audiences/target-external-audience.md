---
title: '[!DNL Adobe Target] externa målgrupper'
description: Aktivera externa målgrupper för  [!DNL Adobe Target] via kontoresor. Anpassa B2B-webbupplevelserna och bibehåll enhetligheten på olika plattformar.
feature: Integrations, Audiences, Account Journeys
role: User, Admin
source-git-commit: 598546c62cb2d567f19b26f7f760aa43e4dd0bc9
workflow-type: tm+mt
source-wordcount: '642'
ht-degree: 0%

---

# [!DNL Adobe Target] externa målgrupper

Du kan aktivera och personalisera upplevelser för externa målgrupper i [!DNL Adobe Target] via kontoresor. Använd den här integreringen för att uppnå avancerad och skräddarsydd personalisering som ökar engagemanget och för att upprätthålla enhetlighet mellan olika plattformar i [!DNL Target] och [!DNL Journey Optimizer B2B Edition]. Denna konsekvens säkerställer att teamen anpassar och personaliserar webbkanaler för inköpsgrupper under hela B2B-köpresan.

Det är ett tvåstegsarbetsflöde för att aktivera en extern målgrupp via Adobe Target:

1. [Lägg till i den externa kundmålgruppen](#add-to-customer-external-audience-from-a-journey) från en resa.
2. [Aktivera den externa målgruppen](#activate-the-external-audience-to-target-as-a-destination) till [!DNL Target] som mål i Experience Platform.

## Lägg till externa kunder från en resa

Under din resa [lägger du till en _Vidta en åtgärd_-nod](../journeys/action-nodes.md) för att köra _[!UICONTROL Add to external customer audience]_-åtgärden. Åtgärder är vanligtvis vad du vill ska hända som ett resultat av någon typ av utlösare, till exempel en händelse eller en tidigare åtgärd. Resan utför åtgärden när ett kvalificerande konto med personprofiler når noden.

>[!NOTE]
>
>När ett kvalificerande konto med personprofiler når noden _Lägg till i den externa kundmålgruppen_ i en publicerad resa kan det ta upp till 48 timmar för dessa profiler att fylla i den externa målgruppen.

1. Markera noden _Utför en åtgärd_ på arbetsytan och välj alternativet _[!UICONTROL Action on]_&#x200B;**[!UICONTROL People]**.

1. Välj _[!UICONTROL Action on people]_&#x200B;för **[!UICONTROL Add to external customer audience]**.

   ![Resensnod - utför en åtgärd på personer - lägg till externa kundmålgrupper](./assets/node-add-external-audience.png){width="550" zoomable="yes"}

1. I nodegenskaperna till höger anger du den externa målgruppen.

   * Om det redan finns en eller flera externa målgrupper kan du välja **[!UICONTROL Select existing]** och [välja den målgrupp som du vill använda](#choose-an-external-audience).

   * Om du vill [skapa en målgrupp](#create-an-external-audience) som ska användas för noden väljer du **[!UICONTROL Create new]**.

### Skapa en extern publik

1. När du har valt alternativet **[!UICONTROL Create new]** i nodegenskaperna klickar du på **[!UICONTROL Create external customer audience]**.

   ![Vidta en åtgärd för personer - lägg till externa kunder - skapa nytt alternativ](./assets/node-add-external-audience-create-new-option.png){width="400"}

1. Ange **[!UICONTROL Name]** (obligatoriskt) och **[!UICONTROL Description]** (valfritt) för den nya målgruppen i dialogrutan.

   ![Skapa dialog för extern kundpublik](./assets/create-external-customer-audience-dialog.png){width="400"}

1. Klicka på **[!UICONTROL Create]**.

   Systemet skapar den nya målgruppen och visar ett bekräftelsemeddelande. Sedan kan du fortsätta att använda den som en befintlig målgrupp för nodåtgärden.

### Välj en extern målgrupp

1. När du har valt alternativet **[!UICONTROL Select existing]** i nodegenskaperna klickar du på **[!UICONTROL Select external customer audience]**.

   ![Vidta en åtgärd för personer - lägg till externa kunder - välj det befintliga alternativet](./assets/node-add-external-audience-select-existing-option.png){width="300"}

1. I dialogrutan _[!UICONTROL Add audience]_&#x200B;väljer du den målgrupp som du vill använda.

   Du kan ange text i fältet _Sök_ om du vill filtrera de visade objekten så att de matchar målgruppens namn.

   ![Vidta en åtgärd för människor - lägg till externa kunder - lägg till publikdialog](./assets/add-audience-dialog.png){width="700" zoomable="yes"}

1. Klicka på **[!UICONTROL Add audience]**.

## Aktivera den externa målgruppen som mål

Om du vill aktivera den externa målgruppen för Adobe Target måste du ha konfigurerat [!DNL Adobe Target] som ett mål i [!DNL Real-time Customer Data Platform (RTCDP)]. Mer information om den här konfigurationen finns i [RTCDP-dokumentationen](https://experienceleague.adobe.com/sv/docs/platform-learn/tutorials/destinations/target/configure-the-target-destination){target="_blank"}.

>[!IMPORTANT]
>
>Om du vill aktivera via en resa måste din implementering av RTCDP använda e-postadress som identitet.

Aktiveringsprocessen kräver att du lägger till [!DNL Adobe Target] som en extern målgrupp eller ett externt mål. Du börjar med att skapa en [!DNL Target]-målgrupp i målgruppsverktyget. Du kan också skapa en platshållarmålgrupp och lägga till funktionen för externa målgrupper.

>[!BEGINSHADEBOX]

![Ikon för AEP-behörigheter](../../assets/do-not-localize/icon_permissions-outline.svg) Följande steg kräver följande behörigheter för din tilldelade användarroll:

* **[!UICONTROL Experience Platform]** - För _[!UICONTROL Destinations]_&#x200B;resource: `Activate Destinations`, `Manage and Activate Dataset Destination` och `View Destination`
* **[!DNL Target]** - `Approver`

>[!ENDSHADEBOX]

1. Gå till **[!UICONTROL Connections]** > **[!UICONTROL Destinations]** i den vänstra navigeringen i Experience Platform.

1. Klicka på fliken **[!UICONTROL Browse]**.  

1. Leta reda på målanslutningen som du vill använda för att aktivera dina segment, klicka på ikonen _Mer meny_ ( **..** ) bredvid namnet och välj **[!UICONTROL Activate audiences]**.

   Ange text i fältet _[!UICONTROL Search]_&#x200B;om du vill filtrera de visade målplatserna efter namn.

   ![Experience Platform - mål - bläddra bland målmål - mer meny](./assets/aep-destinations-activate-target-audience.png){width="800" zoomable="yes"}

1. Välj din externa målgrupp i listan _[!UICONTROL Available audiences]_&#x200B;och klicka på&#x200B;**[!UICONTROL Next]**.

   ![Experience Platform - mål - bläddra bland målmål - mer meny](./assets/aep-destinations-activate-target-audience-available-audiences.png){width="700" zoomable="yes"}

1. Utför eventuell ytterligare fältmappning till målet (valfritt) och klicka på **[!UICONTROL Next]**.

1. Granska de nya målgruppsparametrarna och klicka på **[!UICONTROL Finish]**.

   ![Experience Platform - mål - aktivera mål - granskning](./assets/aep-destinations-activate-target-audience-review.png){width="700" zoomable="yes"}

Vid aktiveringen kan du se målgruppen i [Adobe Target](https://experienceleague.adobe.com/en/docs/target/using/audiences/create-audiences/audiences#use-list){target="_blank"} och använda dem i Adobe Target-aktiviteter.

