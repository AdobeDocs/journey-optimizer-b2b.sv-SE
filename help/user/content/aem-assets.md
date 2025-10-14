---
title: Arbeta med Experience Manager Assets
description: Få åtkomst till och använd AEM Assets-bilder vid redigering av innehåll - dra och släpp, sök, filtrera och synkronisera ändringar automatiskt i Journey Optimizer B2B edition.
feature: Assets, Content, Integrations
role: User
exl-id: c6864981-209c-4123-8d3f-24deb07026a0
source-git-commit: 79012352c3ae4e2f3d38b632b1f523d262f74f96
workflow-type: tm+mt
source-wordcount: '531'
ht-degree: 0%

---

# Arbeta med Experience Manager resurser

När [!DNL Adobe Experience Manager Assets as a Cloud Service] är integrerat med [!DNL Adobe Journey Optimizer B2B Edition] kan du enkelt identifiera och få tillgång till digitala resurser som du kan använda i ditt marknadsföringsinnehåll. När du redigerar ditt innehåll är resurserna tillgängliga från objektet _[!UICONTROL Experience Manager Assets]_&#x200B;i den vänstra navigeringen och när du redigerar e-postinnehåll för en kontoresa.

{{aem-assets-licensing-note}}

När du använder dessa digitala resurser sprids de senaste ändringarna i [!DNL Assets as a Cloud Service] automatiskt till aktiva e-postkampanjer via länkade referenser. Om bilder tas bort i [!DNL Adobe Experience Manager Assets as a Cloud Service] visas bilderna med en bruten referens i e-postmeddelandena. När resurser som för närvarande används på kontoresor ändras eller tas bort, meddelas författarna av resan om bildändringarna och listan över resor som använder bilden. Alla ändringar av resurserna måste göras i den centrala databasen [!DNL Adobe Experience Manager Assets].

När miljön har en eller flera [Assets-databasanslutningar](../admin/configure-aem-repositories.md) kan innehållsförfattare använda [!DNL Experience Manager Assets] som källa för resurser när de skapar e-post, e-postmallar eller visuellt fragment.

>[!IMPORTANT]
>
>En administratör måste lägga till användare som behöver tillgång till Assets i produktprofilerna Assets Consumer Users eller/och Assets Users. [Läs mer](https://experienceleague.adobe.com/sv/docs/experience-manager-cloud-service/content/security/ims-support#managing-products-and-user-access-in-admin-console){target="_blank"}

## Öppna AEM Assets-bilder

Klicka på ikonen _[!UICONTROL Experience Manager Assets]_( ![&#x200B; Experience Manager Assets-ikon &#x200B;](../../assets/do-not-localize/icon-assets-aem.svg) ) i det vänstra sidofältet i designområdet. Detta ändrar verktygspanelen till en lista med tillgängliga resurser i den valda databasen.

![Klicka på Assets-väljarikonen för att komma åt bildresurserna](./assets/content-assets-selector-aem-assets.png){width="700" zoomable="yes"}

>[!NOTE]
>
>För närvarande stöds endast bildresurser från [!DNL Adobe Experience Manager Assets] i [!DNL Adobe Journey Optimizer B2B Edition]. Ändringar av resurserna måste göras från den centrala databasen [!DNL Adobe Experience Manager Assets]. [Läs mer](https://experienceleague.adobe.com/sv/docs/experience-manager-cloud-service/content/assets/manage/manage-digital-assets){target="_blank"}

### Ändra den databas som visas

Om du har fler än en ansluten AEM-databas klickar du på menypilen för **[!UICONTROL Repository]** för att välja den databas som du vill visa i den vänstra panelen.

![Välj en AEM Assets-databas för att komma åt bildresurserna](./assets/content-assets-selector-aem-repo.png){width="700" zoomable="yes"}

Det finns flera metoder för att lägga till en bildresurs på arbetsytan.

### Dra och släpp en bild

1. Bläddra bland miniatyrbilderna som visas i den vänstra panelen.

1. Dra bildminiatyrbilden och släpp den på arbetsytan där du vill lägga till den nya bildkomponenten.

   ![Dra och släpp en bildresurs](./assets/content-drag-drop-image-aem-assets.png){width="700" zoomable="yes"}

## Söka efter och markera en bild

1. Lägg till en bildkomponent på arbetsytan och klicka på **[!UICONTROL Experience Manager Assets]** för att öppna dialogrutan _[!UICONTROL Select Assets]_.

   ![Välj en resurs för bildkomponenten](./assets/content-image-component-empty.png){width="600" zoomable="yes"}

1. I dialogrutan väljer du en bild med de tillgängliga verktygen för att hitta den resurs du behöver:

   * Ändra **[!UICONTROL Repository]** överst till höger.

   * Klicka på **[!UICONTROL Manage assets]** överst till höger för att öppna Assets-databasen på en annan webbläsarflik och använda AEM Assets hanteringsverktyg.

   * Klicka på _vytypsväljaren_ längst upp till höger för att ändra visningen till **[!UICONTROL List View]**, **[!UICONTROL Grid View]**, **[!UICONTROL Gallery View]** eller **[!UICONTROL Waterfall View]**.

   * Klicka på ikonen _Sorteringsordning_ om du vill ändra sorteringsordningen mellan stigande och fallande.

     ![Använd verktyg i dialogrutan Välj Assets för att hitta och välja en bildresurs](./assets/content-select-assets-dialog-aem.png){width="700" zoomable="yes"}

   * Klicka på menypilen **[!UICONTROL Sort by]** om du vill ändra sorteringsvillkoren till **[!UICONTROL Name]**, **[!UICONTROL Size]** eller **[!UICONTROL Modified]**.

   * Klicka på ikonen _Filter_ längst upp till vänster om du vill filtrera de visade objekten enligt dina kriterier.

   * Ange text i sökfältet för att filtrera de visade objekten så att de matchar resursnamnet.

   ![Använd filter och sökfält för att hitta resursen](./assets/content-select-assets-dialog-aem-filter.png){width="700" zoomable="yes"}

1. Klicka på **[!UICONTROL Select]**.
<!-- 

## Upload assets

To import files to Assets as a Cloud Service, you first need to browse or create the folder to be used for storage. You can then import an asset and add it to your email content. After assets are uploaded, you can [use the image assets as you author content](./assets-overview.md#add-assets-to-your-content).

1. While authoring your content in the email designer, drag an image element into the canvas. 

   The properties on the right reflect the image element selection. 

1. Click **[!UICONTROL Import media]** to open the _[!UICONTROL Upload image]_ dialog.

1. If your file system is open to your image file, drag and drop the file on the box in the dialog.

   ![Upload image file to Assets repository](./assets/email-designer-image-upload.png){width="700" zoomable="yes"}

   You can also click the **[!UICONTROL Select a file from your computer]** link and use your file system to locate and select the image file. Click Open and the image file is displayed in the box.

1. Click **[!UICONTROL Import]**.
-->
