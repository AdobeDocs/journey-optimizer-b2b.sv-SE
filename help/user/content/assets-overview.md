---
title: Assets
description: Hantera bildresurser från Marketo Engage Design Studio och AEM Assets för e-post, mallar och fragment i Journey Optimizer B2B edition.
feature: Assets, Content
role: User
exl-id: f3848e65-3196-4d1f-90cf-7aa6ceeafabb
source-git-commit: 79012352c3ae4e2f3d38b632b1f523d262f74f96
workflow-type: tm+mt
source-wordcount: '865'
ht-degree: 0%

---

# Assets

I [!DNL Adobe Journey Optimizer B2B Edition] är resurser vanligtvis de bilder som används vid design av innehåll som stöder kontoresor. Du kan använda de här bilderna i e-postmeddelanden, e-postmallar och fragment från resursväljaren eller i ett enkelt dra och släpp-gränssnitt i den visuella designrymden.

[!DNL Journey Optimizer B2B Edition] ger marknadsförare åtkomst till två typer av resursbibliotek: [!DNL Adobe Marketo Engage] [!DNL Design Studio] och [!DNL Adobe Experience Manager Assets as a Cloud Service]. Du kanske bara använder Adobe Marketo Engage Design Studio eller båda biblioteken som är konfigurerade samtidigt (baserat på den [!DNL Experience Manager Assets]-licens du har).

## Resurshantering

Om du har etablerats med [!DNL Adobe Experience Manager as a Cloud Services] har du åtkomst till databaserna för både [!DNL Marketo Engage Design Studio] och [!DNL Adobe Experience Manager Assets as a Cloud Service] när ditt användarkonto har de behörigheter som krävs. Dessa databaser är separata och inte synkroniserade. Du kan använda bilder från båda källorna.

### Adobe Marketo Engage-resurser

Resurskatalogen [!DNL Adobe Marketo Engage Design Studio] tillhandahålls som standard med varje [!DNL Journey Optimizer B2B Edition]-prenumeration. Det innebär att du har tillgång till alla bildresurser som lagras i [!DNL Adobe Marketo Engage] ([!UICONTROL Design Studio] > [!UICONTROL Images & Files]). Du kan använda den här databasen som ditt lokala resursbibliotek, inklusive funktioner för överföring och hämtning av resurser. Du kan också använda dessa resurser i ditt reseinnehåll.

Det finns inbyggda skyddsräcken som förhindrar redigering av [!DNL Marketo Engage]-resurser från [!DNL Journey Optimizer B2B Edition] samt borttagnings- och flyttåtgärder. Dessa skydd säkerställer att källresurserna (Marketo Engage Design Studio) bevaras samtidigt som sömlös läsning och återanvändning tillåts i [!DNL Journey Optimizer B2B Edition].

Filformat som stöds: JPG, JPEG, GIF, PNG, EPS, SVG och RGB

### Adobe Experience Manager Assets as a Cloud Service

Sammanför arbetsflöden för marknadsföring och kreativitet med [!DNL Adobe Experience Manager Assets]. Den är inbyggd i [!DNL Journey Optimizer B2B Edition], så du kan enkelt komma åt Assets as a Cloud Service för att upptäcka och använda digitala resurser. Den ger åtkomst till din Assets-databas för resurser som du kan använda för att fylla i dina meddelanden.

[!DNL Adobe Journey Optimizer B2B Edition] kan ansluta till [!DNL Adobe Experience Manager Assets as a Cloud Service] för centraliserad resurshantering som utökar ditt kreativa system och förenar digitala resurser för upplevelseleverans. [!DNL Adobe Experience Manager Assets as a Cloud Service] erbjuder en lättanvänd molnlösning för effektiv hantering av digitala resurser och dynamiska media. Programmet innehåller smidigt avancerade funktioner, bland annat artificiell intelligens och maskininlärning.

Läs mer i [Adobe Experience Manager as a Cloud Service-dokumentationen](https://experienceleague.adobe.com/en/docs/experience-manager-cloud-service/content/assets/overview){target="_blank"}.

{{aem-assets-licensing-note}}

Gå till [!DNL Adobe Experience Manager Assets] direkt i [!DNL Journey Optimizer B2B Edition] från **[!UICONTROL Experience Manager Assets]**-objektet i den vänstra navigeringen i innehållsdesignen. Du kan också komma åt resurser och mappar när du utformar e-post, e-postmallar och visuellt fragmentinnehåll.

För närvarande kan du bara använda bilder från Adobe Experience Manager Assets i Adobe Journey Optimizer B2B edition.

## Använda resurser för att skapa innehåll

Använd resurser när du skapar e-postmeddelanden, e-postmallar och visuella fragment. Den visuella innehållsredigeraren ger åtkomst till bilderna i dina anslutna resurskataloger. Om du har en prenumeration på Experience Manager Assets as a Cloud Service tillsammans med standardversionen av Adobe Marketo Engage Design Studio kan du välja bildresurser från båda källorna. Du kan också överföra en bildresurs, vilket placerar den på arbetsytan [!DNL Journey Optimizer B2B Edition] i den anslutna [!DNL Marketo Engage Design Studio]-databasen.

Du kan välja bildkälla när du redigerar inställningarna för en bildkomponent eller direkt på arbetsytan:

* **_Inställningar för bildkomponent_** - När du har markerat en bildkomponent i det visuella designområdet kan du visa och redigera inställningarna på den högra panelen. Om du vill lägga till eller ändra bildfilen som visas i komponenten väljer du källtyp och väljer en bildfil.

  ![Redigera bildkomponentsinställningarna på den högra panelen](./assets/content-assets-image-settings.png){width="350"}

* **_Tom komponent_** - När du lägger till en bildkomponent i den visuella designrymden är den tom och ger enkel åtkomst för att välja en källa och välja en bildfil.

  ![Välj en källa för att välja en bildfil för den tomma bildkomponenten](./assets/content-assets-image-component-empty.png){width="500"}

* **_Verktygsfältet Bildkomponent_** - När du har markerat en bildkomponent i den visuella designrymden kan du enkelt välja en källa och välja bildfilen i verktygsfältet.

  ![Använd verktygsfältet för att välja en källa för att välja en bildfil för bildkomponenten](./assets/content-assets-image-toolbar-settings.png){width="500"}

Du kan lägga till en bildresurs när du redigerar innehållet, beroende på bildresurskällan. Du kan också välja en bildresurs i bakgrundsinställningarna för en strukturkomponent.

>[!BEGINTABS]

>[!TAB Marketo Engage Assets]

Klicka på **[!UICONTROL Marketo Engage Assets]** för att öppna resursväljaren, där du kan välja en bild från en [!DNL Marketo Engage] -arbetsyta eller Journey Optimizer B2B edition-arbetsytan.

![Välj en bildresurs på arbetsytan](./assets/content-assets-image-me-selected.png){width="700" zoomable="yes"}

Du kan använda sök och filter för att hitta den önskade bildresursen. Markera resursen och klicka på **[!UICONTROL Select]** för att använda den för bildkomponenten.

Mer detaljerad information om hur du använder [!DNL Marketo Engage] bildresurser finns i [Använda resurser i ditt innehåll](./marketo-engage-design-studio.md#use-assets-in-your-content).

>[!TAB Experience Manager Assets]

Klicka på **[!UICONTROL Experience Manager Assets]** för att öppna resursväljaren, där du kan välja en bild från Experience Manager Assets-databasen.

![Välj en bildresurs i AEM Assets-databasen](./assets/content-assets-image-aem-selected.png){width="700" zoomable="yes"}

Du kan använda sök och filter för att hitta den önskade bildresursen. Markera resursen och klicka på **[!UICONTROL Select]** för att använda den för bildkomponenten.

Mer information om hur du använder bildfiler från [!DNL Experience Manager Assets] finns i [Åtkomst till AEM Assets-bilder](./aem-assets.md#access-aem-assets-images).

>[!TAB Importera media]

Klicka på **[!UICONTROL Import media]** om du vill välja en bildfil och importera den som en resurs som kan användas för Journey Optimizer B2B edition-innehåll.

![Välj en egen bildfil att importera som en resurs](./assets/content-assets-image-import-file-selected.png){width="500" zoomable="yes"}

När du har dragit och släppt filen eller markerat den från filsystemet klickar du på **[!UICONTROL Import]**. Den importerade resursen lagras på arbetsytan [!DNL Journey Optimizer B2B Edition] i databasen [!DNL Adobe Marketo Engage Design Studio].

>[!ENDTABS]
