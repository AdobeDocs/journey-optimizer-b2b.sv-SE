---
title: Assets
description: Läs om filhantering i Journey Optimizer B2B edition.
feature: Assets, Content
role: User
exl-id: f3848e65-3196-4d1f-90cf-7aa6ceeafabb
source-git-commit: 323b2d781e9ee46b71e3ea01853f6c1321739de0
workflow-type: tm+mt
source-wordcount: '978'
ht-degree: 0%

---

# Assets

I Adobe Journey Optimizer B2B edition är resurser vanligtvis de bilder som används för att utforma innehåll som stöder kontoresor. Du kan använda dessa bilder i e-postmeddelanden, e-postmallar och fragment via en resursväljare eller ett enkelt dra och släpp-gränssnitt i den visuella innehållsredigeraren.

Adobe Journey Optimizer B2B edition ger marknadsförarna tillgång till två typer av mediebibliotek: Adobe Marketo Engage Design Studio och Adobe Experience Manager Assets as a Cloud Service. Du får endast använda Adobe Marketo Engage Design Studio, eller använda båda biblioteken konfigurerade samtidigt (baserat på den AEM Assets-licens du har).

## Resurshantering

Om du har Adobe Experience Manager som molntjänster har du tillgång till databaserna för både Marketo Engage Design Studio och Adobe Experience Manager Assets as a Cloud Service när ditt användarkonto har de behörigheter som krävs. Dessa databaser är separata och inte synkroniserade. Du kan använda bilder från båda källorna.

### Adobe Marketo Engage-resurser

Adobe Marketo Engage Design Studio-resurskatalogen ingår som standard i alla Journey Optimizer B2B edition-prenumerationer. Det innebär att du har tillgång till alla bildresurser som lagras i Adobe Marketo Engage ([!UICONTROL Design Studio] > [!UICONTROL Images & Files]). Du kan använda den här databasen som ditt lokala resursbibliotek, inklusive funktioner för överföring och hämtning av resurser. Du kan också använda dessa resurser i ditt reseinnehåll.

Det finns inbyggda skyddsmekanismer som förhindrar redigering av Marketo Engage-resurser från Journey Optimizer B2B edition samt borttagning och flytt av åtgärder. Dessa skydd säkerställer att källmaterialet (Marketo Engage Design Studio) bevaras samtidigt som det går att läsa och återanvända i Journey Optimizer B2B edition.

Filformat som stöds: JPG, JPEG, GIF, PNG, EPS, SVG och RGB

### Adobe Experience Manager Assets as a Cloud Service

Samla marknadsförings- och kreativa arbetsflöden med Adobe Experience Manager Assets. Programmet är integrerat med Adobe Journey Optimizer B2B edition så att du enkelt kan komma åt Assets as a Cloud Service för att upptäcka och använda digitalt material. Den ger åtkomst till din Assets-databas för resurser som du kan använda för att fylla i dina meddelanden.

Adobe Journey Optimizer B2B edition kan ansluta till Adobe Experience Manager Assets as a Cloud Service för centraliserad resurshantering som utökar ert kreativa system och sammanför digitala resurser för leverans av upplevelser. Adobe Experience Manager Assets as a Cloud Service är en lättanvänd molnlösning för effektiv hantering av digitala resurser och dynamiska media. Programmet innehåller smidigt avancerade funktioner, bland annat artificiell intelligens och maskininlärning.

Läs mer i [Adobe Experience Manager as a Cloud Service-dokumentationen](https://experienceleague.adobe.com/en/docs/experience-manager-cloud-service/content/assets/overview){target="_blank"}.

{{aem-assets-licensing-note}}

Få tillgång till Adobe Experience Manager Assets direkt inifrån Journey Optimizer B2B edition från **[!UICONTROL Experience Manager Assets]**-objektet i den vänstra navigeringen i innehållsdesignen. Du kan också komma åt resurser och mappar när du utformar e-post, e-postmallar och visuellt fragmentinnehåll.

För närvarande kan du bara använda bilder från Adobe Experience Manager Assets i Adobe Journey Optimizer B2B edition.

## Använda resurser för att skapa innehåll

Använd resurser när du skapar e-postmeddelanden, e-postmallar och visuella fragment. Den visuella innehållsredigeraren ger åtkomst till bilderna i dina anslutna resurskataloger. Om du har en prenumeration på Experience Manager Assets as a Cloud Service tillsammans med standardversionen av Adobe Marketo Engage Design Studio kan du välja bildresurser från båda källorna. Du kan också överföra en bildresurs, som placerar den på arbetsytan i Journey Optimizer B2B edition i den anslutna Marketo Engage Design Studio-databasen.

Du kan välja bildkälla när du redigerar inställningarna för en bildkomponent eller direkt på arbetsytan:

* **_Inställningar för bildkomponent_** - När du har markerat en bildkomponent i den visuella designern kan du visa och redigera inställningarna i den högra panelen. Om du vill lägga till eller ändra bildfilen som visas i komponenten väljer du källtyp och väljer en bildfil.

  ![Redigera bildkomponentsinställningarna på den högra panelen](./assets/content-assets-image-settings.png){width="350"}

* **_Tom komponent_** - När du lägger till en bildkomponent i den visuella designern är den tom och ger enkel åtkomst för att välja en källa och välja en bildfil.

  ![Välj en källa för att välja en bildfil för den tomma bildkomponenten](./assets/content-assets-image-component-empty.png){width="500"}

* **_Verktygsfältet för bildkomponenter_** - När du har markerat en bildkomponent i den visuella designern är det enkelt att välja en källa och välja bildfilen i verktygsfältet.

  ![Använd verktygsfältet för att välja en källa för att välja en bildfil för bildkomponenten](./assets/content-assets-image-toolbar-settings.png){width="500"}

Du kan lägga till en bildresurs när du redigerar innehållet, beroende på bildresurskällan. Du kan också välja en bildresurs i bakgrundsinställningarna för en strukturkomponent.

>[!BEGINTABS]

>[!TAB Marketo Engage Assets]

Klicka på **[!UICONTROL Marketo Engage Assets]** för att öppna resursväljaren, där du kan välja en bild från en Marketo Engage-arbetsyta eller Journey Optimizer B2B edition-arbetsytan.

![Välj en bildresurs på arbetsytan](./assets/content-assets-image-me-selected.png){width="700" zoomable="yes"}

Du kan använda sök och filter för att hitta den önskade bildresursen. Markera resursen och klicka på **[!UICONTROL Select]** för att använda den för bildkomponenten.

Mer detaljerad information om hur du använder Marketo Engage bildresurser finns i [Använda resurser i ditt innehåll](./marketo-engage-design-studio.md#use-assets-in-your-content).

>[!TAB Experience Manager Assets]

Klicka på **[!UICONTROL Experience Manager Assets]** för att öppna resursväljaren, där du kan välja en bild från Experience Manager Assets-databasen.

![Välj en bildresurs i AEM Assets-databasen](./assets/content-assets-image-aem-selected.png){width="700" zoomable="yes"}

Du kan använda sök och filter för att hitta den önskade bildresursen. Markera resursen och klicka på **[!UICONTROL Select]** för att använda den för bildkomponenten.

Mer information om hur du använder bildfiler från Experience Manager Assets finns i [Åtkomst till AEM Assets-bilder](./aem-assets.md#access-aem-assets-images).

>[!TAB Importera media]

Klicka på **[!UICONTROL Import media]** om du vill välja en bildfil och importera den som en resurs som kan användas för Journey Optimizer B2B edition-innehåll.

![Välj en egen bildfil att importera som en resurs](./assets/content-assets-image-import-file-selected.png){width="500" zoomable="yes"}

När du har dragit och släppt filen eller markerat den från filsystemet klickar du på **[!UICONTROL Import]**. Den importerade resursen lagras på arbetsytan i Journey Optimizer B2B edition i Adobe Marketo Engage Design Studio-databasen.

>[!ENDTABS]
