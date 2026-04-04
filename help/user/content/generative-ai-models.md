---
title: Generativa AI-modeller
description: Skapa och hantera generativa AI-bildmodeller som marknadsförare kan välja för att generera bilder för e-post- och landningssidinnehåll.
topic: Artificial Intelligence
feature: Generative AI, Brand Identity, Content
role: User
level: Beginner, Intermediate
source-git-commit: 0612c3caa0673a7eb65a0aac0010edcf12c5d553
workflow-type: tm+mt
source-wordcount: '470'
ht-degree: 0%

---

# Generativa AI-modeller för varumärkesjustering

Utöka era funktioner för att skapa AI-bilder med inbyggda modeller, anpassade Firefly-modeller och tredjepartsleverantörer av bildgenerering för att uppfylla just era behov och förbättra varumärkesjusteringen:

- **[!UICONTROL Adobe model]**, som drivs av Firefly Image Model 4, levereras direkt från kartongen och kan användas för att generera bilder direkt utan ytterligare konfiguration.
- **[!UICONTROL Partner model]**, som drivs av Gemini 2.5 Flash, erbjuder specialfunktioner för specifika användningsområden.
- **[!UICONTROL Custom models]** är varumärkesspecifika modeller som har utbildats på dina egna resurser och lagts till av din organisation.

Läs om anpassade modeller i [Adobe Firefly-dokumentationen](https://helpx.adobe.com/se/firefly/web/work-with-enterprise-features/train-custom-models/custom-models-overview.html){target="_blank"}.

Marknadsförarna kan välja någon av de aktiverade generativa modellerna när de genererar bilder för e-post- eller landningssidans innehåll.

## Hantera generativa modeller

Från en central plats kan du visa alla tillgängliga modeller, filtrera och söka efter specifika modeller och konfigurera modellinställningar för dina varumärken.

1. Gå till **[!UICONTROL Content Management]** > **[!UICONTROL Brands]** i den vänstra navigeringen.

1. Välj fliken **[!UICONTROL Generative models]** på sidan.

![Öppna listan med generativa modeller](./assets/brands-gen-models-list.png){width="800" zoomable="yes"}

### Filtrera och söka i listan

Klicka på ikonen _Filter_ ![Filter &#x200B;](../../assets/do-not-localize/icon-react-filter.svg) för att öppna filtermenyn. Filtrera modeller efter **[!UICONTROL Type]** eller **[!UICONTROL Status]**.

![Filtrera listan med generativa modeller](./assets/brands-gen-models-filter.png){width="700" zoomable="yes"}

Du kan också använda sökfältet för att hitta en specifik generativ modell efter namn.

### Modellåtgärder

Om det finns en anpassad modell i listan klickar du på ikonen _Mer meny_ ![Mer meny](../../assets/do-not-localize/icon-more-menu.svg) . Du kan välja **[!UICONTROL Enable]** eller **[!UICONTROL Disable]** om du vill ändra modellens tillgänglighetsstatus eller välja **[!UICONTROL Delete]** om du vill ta bort modellen från listan.

![Mer meny i listan med generativa modeller](./assets/brands-gen-models-more-menu.png){width="450"}

För en inbyggd modell klickar du på ikonen _Aktivera_ ( ![Aktivera ikon](../../assets/do-not-localize/icon-enable.svg) ) eller _Inaktivera_ ( ![Inaktivera ikon](../../assets/do-not-localize/icon-disable.svg) ) för att ändra modelltillgängligheten för bildgenerering.

>[!NOTE]
>
>Endast egna modeller kan tas bort.

## Lägg till en generativ modell

Skapa egna Firefly-modeller eller anslut tredjepartsleverantörer av bildgenerationer för att utöka era generativa AI-funktioner.

>[!NOTE]
>
>För att kunna skapa anpassade Firefly-modeller krävs ett Firefly ETLA-avtal.

1. Klicka på **[!UICONTROL Add model]** på fliken _[!UICONTROL Generative models]_.

1. Ange **[!UICONTROL Name]** som modell.

<!-- 1. Select a **[!UICONTROL Model provider]**. future development -->

1. Ange **[!UICONTROL Model ID]**.

   Du hittar ditt modell-ID på Firefly webbplats och navigerar till dina utbildade modeller. Den unika identifieraren är tillgänglig i modellens hanteringsavsnitt efter att den har publicerats. Mer information finns i [dokumentationen för anpassade Firefly-modeller](https://helpx.adobe.com/se/firefly/web/work-with-enterprise-features/train-custom-models/custom-models-overview.html){target="_blank"}.

1. Du kan också ange en **[!UICONTROL Description]** för att hjälpa till att identifiera modellen och dess avsedda användning.

   ![Lägg till modell - generativa modeller](./assets/brands-gen-models-add-model.png){width="550" zoomable="yes"}

1. Klicka på **[!UICONTROL Test connection]** för att verifiera modellkonfigurationen.

1. När anslutningstestet har slutförts klickar du på **[!UICONTROL Save]** för att spara modellkonfigurationen.

   När du sparar modellen läggs den till i listan över generativa modeller, där du kan aktivera den för marknadsförare. Du kan också när som helst inaktivera eller ta bort den.

   ![Välja en generativ modell för bildgenerering](./assets/gen-ai-model-selection.png){width="600" zoomable="yes"}
