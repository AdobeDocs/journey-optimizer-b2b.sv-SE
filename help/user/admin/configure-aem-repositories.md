---
title: Konfigurera Experience Manager-resurskataloger
description: Koppla Experience Manager Assets-arkiv till Journey Optimizer B2B edition för smidig åtkomst till digitalt material vid framtagning av material.
feature: Assets, Integrations
role: Admin
exl-id: 4cdfc8bc-823f-4320-a2c3-08226f26eec2
source-git-commit: 9ed2d2a36dbdaf39c107a18632d951003c86197b
workflow-type: tm+mt
source-wordcount: '693'
ht-degree: 0%

---

# Konfigurera Experience Manager resurskataloger

[!DNL Adobe Journey Optimizer B2B Edition] integreras med [!DNL Adobe Experience Manager Assets as a Cloud Service] och tillåter att resurser används i ditt e-postinnehåll. Det garanterar genomskinlighet genom att utbyta information med [!DNL Experience Manager Assets]. Konfigurera anslutningen till [!DNL Adobe Experience Assets] för att aktivera den här funktionen.

Adobe Experience Manager Cloud Manager är indelat i program och varje program har flera miljöer och databaser ([Läs mer](https://experienceleague.adobe.com/en/docs/experience-manager-cloud-service/content/implementing/using-cloud-manager/programs/program-types){target="_blank"}). När du konfigurerar Adobe Experience Manager Assets i Adobe Journey Optimizer B2B edition skapar du anslutningar till alla databaser som du vill använda för att komma åt digitala resurser.

{{aem-assets-licensing-note}}

## Förutsättningar

* Generera autentiseringsuppgifter för tjänsten för den önskade miljön på AEM Headless Developer Console ([Läs mer](https://experienceleague.adobe.com/en/docs/experience-manager-learn/getting-started-with-aem-headless/authentication/service-credentials#generate-service-credentials){target="_blank"}).
* Köp de certifikat som krävs för anslutningen. Som en god praxis bör du se till att certifikaten har minst sex månader kvar innan de upphör att gälla. Certifikaten upphör att gälla var 365:e dag.
* Adobe Journey Optimizer B2B edition ger åtkomst till en digital resurshanteringskälla åt gången. Kontrollera att de nödvändiga resurserna är tillgängliga i Adobe Experience Manager innan du byter.

>[!IMPORTANT]
>
>Tjänstidentifierarna är äkta och innehåller en privat nyckel. Dessa uppgifter måste lagras, hanteras och vara åtkomliga enligt din organisations IT-policy och säkerhetspolicy.

## Lägga till en databasanslutning

1. Välj **[!UICONTROL Administration]** > **[!UICONTROL Configuration]** i den vänstra navigeringen.

1. Klicka på **[!UICONTROL Assets]** på panelen mellan.

   ![Åtkomst till Assets konfigurationsutrymme](./assets/configuration-assets-aem.png){width="700" zoomable="yes"}

<!--   The default digital asset management option is configured as `Adobe Marketo Engage`.
-->
Härifrån kan du konfigurera anslutningarna till varje AEM-miljödatabas en i taget.

1. Klicka på pilen bredvid _[!UICONTROL Adobe Experience Manager Assets]_&#x200B;i rutan **[!UICONTROL Configure a repository]**&#x200B;och välj databasen.

   ![Välj en AEM Assets-databas](./assets/configure-assets-aem-choose-respository.png){width="500"}

1. Klicka på **[!UICONTROL Add a certificate]** och använd dialogverktygen för att överföra filen.

   Du kan överföra en JSON-fil genom att dra den till dialogrutan. Du kan också klicka på länken för att hitta och välja en fil i systemet.

   ![Överför certifikat-JSON-filen](./assets/configuration-assets-aem-upload-cert.png){width="500"}

   När överföringen är klar visas certifikatet längst ned.

   >[!NOTE]
   >
   >Om en ogiltig fil används visas ett fel längst ned i dialogrutan.

   Klicka på **[!UICONTROL Add]** för att slutföra certifikatet.

1. Klicka på bakåtpilen (¥) för att gå tillbaka till huvudkonfigurationssidan.

   Den konfigurerade databasen visas i tabellen under urvalspanelen. Du kan lägga till ytterligare en databas genom att upprepa steg 3-4.

   ![Granska de konfigurerade AEM-resursdatabaserna](./assets/configuration-assets-aem-repositories.png){width="600" zoomable="yes"}

När du har konfigurerat databaserna kan teammedlemmarna välja [!DNL Adobe Experience Manager Assets] när de redigerar innehållet.

>[!NOTE]
>
>Adobe Journey Optimizer B2B edition har stöd för åtkomst till en digital resurshanteringskälla i taget när du redigerar innehåll. 

## Ersätta ett certifikat

Certifikat upphör att gälla var 365:e dag från det att de skapades. Om du vill vara säker på att ditt team kan fortsätta få åtkomst till resurser ersätter du certifikatet innan det upphör att gälla.

>[!NOTE]
>
>[!DNL Adobe Journey Optimizer B2B Edition] kommunicerar med [!DNL Experience Manager Assets] för användningsinformation. Anslutningen måste vara aktiv för tillförlitlig synkronisering av användningsdata och för att förhindra datameddelanden. Administratörer får meddelanden om att certifikat upphör att gälla via meddelanden i appen. Förfallodatum visas också i underavsnittet _Assets_ i _[!UICONTROL Administration]_-området.

1. På sidan för hantering av digitala resurser letar du reda på listan över konfigurerade databaser.

1. Klicka på den databas som du vill ersätta certifikatet med.

1. Klicka på ikonen för ovaler (**..**) för certifikatfilen för att visa alternativen för åtgärder på den.

   ![Öppna alternativmenyn för AEM-certifikatet för resurslagringsplatsen](./assets/configuration-assets-aem-repo-menu.png){width="600" zoomable="yes"}

1. Välj **[!UICONTROL Replace]** för att öppna dialogrutan för filöverföring.

1. Överför en fil antingen genom att dra den till dialogrutan eller genom att använda länken. Kontrollera att filen är av JSON-typ.

   ![Överför den nya JSON-filen för AEM-resurslagerdatabascertifikat](./assets/configuration-assets-aem-upload-replacement-cert.png){width="500"}

1. Klicka på **[!UICONTROL Replace]** för att bekräfta överföringen.

## Visa ett certifikat

Du kan visa JSON-certifikatfilen som är kopplad till databasanslutningen.

1. På sidan för hantering av digitala resurser letar du reda på listan över konfigurerade databaser.

1. Klicka på den anslutna databasen.

1. Klicka på ikonen för ovaler (**..**) för certifikatfilen för att visa alternativen för åtgärder på den.

1. Välj **[!UICONTROL View]**.

   ![Visa JSON-certifikatfilen för en ansluten AEM-resurskatalog](./assets/configuration-assets-aem-view-cert.png){width="600"}

1. Klicka på **[!UICONTROL Close]** för att återgå till sidan Konfigurera databas.

## Ta bort en databasanslutning

När du tar bort en databas tas användaråtkomst till Experience Manager Assets-miljön bort i Journey Optimizer B2B edition.

1. På sidan _[!UICONTROL Digital asset management]_&#x200B;letar du reda på listan med konfigurerade resursdatabaser.

1. Klicka på det databasnamn du vill redigera anslutningen.

1. Klicka på ikonen för ovaler (**..**) för certifikatfilen för att visa alternativen för åtgärder på den.

1. Välj **[!UICONTROL Delete]**.

1. Klicka på **[!UICONTROL Delete]** i bekräftelsedialogrutan.
<!--

## Switch back to Adobe Marketo Engage Assets

Select Adobe Marketo Engage digital asset management in the Assets section.

After the confirmation, the Adobe Marketo Engage assets library is available for users.
-->
