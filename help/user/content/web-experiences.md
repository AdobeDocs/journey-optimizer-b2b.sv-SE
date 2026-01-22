---
title: Webbupplevelser
description: Skapa, designa och publicera personaliserade webbupplevelser för kontoresor - leverera riktade innehållsändringar till webbplatsbesökare i Journey Optimizer B2B edition.
feature: Content, Channels
role: User
badgeBeta: label="Beta" type="informative" tooltip="Den här funktionen är för närvarande i en begränsad betaversion"
source-git-commit: e3c00ab4657c7bf05573e049bbcb4bb3628e751e
workflow-type: tm+mt
source-wordcount: '1423'
ht-degree: 0%

---

# Webbupplevelser

Med webbkanalen i Adobe Journey Optimizer B2B edition kan ni skapa personaliserade upplevelser direkt på er webbplats, så att ni kan kommunicera med kunderna på meningsfulla sätt. Den här funktionen erbjuder en flexibel verktygslåda som du kan använda för att förbättra engagemanget med skräddarsytt innehåll och sömlöst integrera det med andra kanaler, som e-post och SMS.

Med webbupplevelser kan ni

* Gör personaliserade innehållsändringar för riktade webbplatsbesökare
* Anpassa webbplatselement som banners, text, bilder och knappar baserat på kontoattribut
* Ange specifika sidor eller ändra på flera sidor med URL-matchningsregler
* Spåra engagemanget och övervaka effekten av era webbpersonaliseringssatsningar

>[!BEGINSHADEBOX]

## Förutsättningar

Innan du kan skapa webbupplevelser måste du se till att följande krav uppfylls:

* En produktadministratör har konfigurerat en eller flera webbkanaler för att definiera de URL:er (sidor) som ska inkluderas för en webbupplevelse. Mer information finns i [Konfigurationer för webbkanaler](../admin/configure-channels-web.md).

* På webbplatsen har [Adobe Experience Platform Web SDK](https://experienceleague.adobe.com/en/docs/experience-platform/collection/js/js-overview) (`alloy.js`) implementerats för besöksidentifiering och innehållsleverans. Kontrollera att Adobe Experience Platform Web SDK version är 2.16 eller senare.

* Du har de [behörigheter](../admin/user-management.md#b2b-product-permissions) som krävs för att skapa och hantera webbupplevelser under en resa:
   * _[!UICONTROL Campaigns]_>_[!UICONTROL Manage Campaigns]_ - Krävs för att lägga till eller uppdatera en åtgärdsnod för webbanpassning.
   * _[!UICONTROL Campaigns]_>_[!UICONTROL View Campaigns]_ - Krävs för att visa information för en åtgärdsnod för webbanpassning.
   * _[!UICONTROL Campaigns]_>_[!UICONTROL Approve and Publish Campaigns]_ - Krävs för att publicera en resa som har en eller flera åtgärdsnoder för webbpersonalisering.

* Webbläsartillägget [Hjälp för visuell redigering](#install-the-visual-editing-helper-extension) är installerat för din webbläsare. Det här tillägget krävs för att du ska kunna öppna, redigera och förhandsgranska dina webbsidor på ett tillförlitligt sätt i designområdet för Journey Optimizer B2B edition.

  >[!NOTE]
  >
  >Google Chrome och Microsoft Edge är för närvarande de enda webbläsare som har stöd för att skapa webbsidor i Journey Optimizer B2B edition.

>[!ENDSHADEBOX]

## Installera tillägget Hjälp för visuell redigering

1. Öppna en ny flik i webbläsaren ([!DNL Google Chrome] eller [!DNL Microsoft Edge]).

1. Gå till [Google Chrome Web Store](https://chromewebstore.google.com/category/extensions).

   Om du använder [!DNL Microsoft Edge] väljer du _Tillåt tillägg_ från andra butiker på den översta banderollen. Om du aktiverar det här alternativet kan du lägga till tillägg från [!DNL Chrome Web Store] till [!DNL Microsoft Edge].

1. Sök och navigera till webbläsartillägget _[!DNL Adobe Experience Cloud Visual Editing Helper]_.

   ![Hjälptillägg för Adobe Experience Cloud Visual Editing för Google Chrome](./assets/web-experience-google-chrome-adobe-visual-editing-extension.png){width="800" zoomable="yes"}

1. Klicka på **[!UICONTROL Add to Chrome]** och sedan på **[!UICONTROL Add Extension]** i bekräftelsedialogrutan.

   Om du använder [!DNL Microsoft Edge] läggs tillägget till i [!DNL Edge].

1. Kontrollera att webbläsartillägget [!DNL Visual Editing Helper] är korrekt aktiverat i webbläsarens verktygsfält.

   ![Tilläggsikonen Adobe Experience Cloud Visual Editing Helper i Google Chrome-verktygsfältet](./assets/web-experience-google-chrome-adobe-visual-editing-extension-icon.png){width="450"}

[!DNL Adobe Experience Cloud Visual Editing Helper] aktiveras nu automatiskt när en webbplats öppnas i den visuella redigeraren i Journey Optimizer B2B edition för webbupplevelser. Tillägget har inga villkorsinställningar och hanterar automatiskt alla inställningar, inklusive cookies för SameSite.

>[!NOTE]
>
>Vissa webbplatser kanske inte öppnas som de ska i Journey Optimizer B2B edition webbredigerare på grund av något av följande:
>
>* Webbplatsen har strikta säkerhetsprinciper.
>* Webbplatsen ligger i en iframe.
>* Kundens QA- eller scenwebbplats är inte tillgänglig externt (webbplatsen är intern).

## Skapa en webbupplevelse

Du kan konfigurera webbupplevelser under en resa när du [lägger till en _[!UICONTROL Take an action]_&#x200B;nod](../journeys/action-nodes.md) och gör följande:

1. Välj _[!UICONTROL Action on]_&#x200B;för målet **[!UICONTROL People]**.

1. Välj _[!UICONTROL Action on people]_&#x200B;för **[!UICONTROL Personalize web experience]**.

   ![Vidta en åtgärd - anpassa webbupplevelsen](./assets/web-experience-add-journey-node.png){width="500"}

1. Klicka på **[!UICONTROL Create web experience]**.

1. Ange ett användbart _[!UICONTROL Create web experience]_&#x200B;och **[!UICONTROL Name]**(valfritt) i dialogrutan **[!UICONTROL Description]**.

   * Namn - Max 100 tecken, måste vara unikt, skiftlägeskänsligt

   * Beskrivning - högst 300 tecken

   >[!NOTE]
   >
   >Namnfält och beskrivningsfält har stöd för alfavärden, numeriska tecken och specialtecken. Reserverade tecken (`\ / : * ? " < > |`) är **_inte tillåtna_**.

   ![Dialogrutan Skapa webbupplevelse](./assets/web-experience-create-dialog.png){width="400"}

<!-- What is this for? 1. Properties? -->

1. Ange beskrivningen för webbupplevelsen på fliken **[!UICONTROL Properties]**.

1. Klicka på fliken **[!UICONTROL Actions]** och välj den **[!UICONTROL Web channel]** som ska användas för webbupplevelsen.

   Webbkanalskonfigurationen avgör var innehållsändringarna tillämpas baserat på de konfigurerade sidmatchningsreglerna. Mer information finns i [Webbkanalskonfigurationer](../admin/configure-channels-web.md).

   ![Markerad webbkanalskonfiguration](./assets/web-experience-journey-node-actions-tab.png){width="700" zoomable="yes"}

1. Om du vill definiera webbändringarna klickar du på **[!UICONTROL Edit content]**.

   Redigeraren öppnas på fliken _[!UICONTROL Content]_&#x200B;där du kan definiera ändringarna för webbupplevelsen. Mer information om hur du använder designverktygen för att lägga till innehållsändringar i webbupplevelsen finns i [Utformning av webbupplevelser](./web-experience-design.md).

1. I den högra panelen anger du webbupplevelseegenskaperna efter hur du vill definiera och hantera den.

   * **[!UICONTROL Visual editor]** - Växla mellan den [visuella och den icke-visuella redigeraren](./web-experience-design.md#web-design-tools) för design av webbupplevelseändringar.
   * **[!UICONTROL Visitor redirection]** - Aktivera det här alternativet för att [omdirigera besökare till en annan befintlig URL](#redirect-to-url) i stället för att skapa en ny variant på innehållsfliken.

   ![Växla egenskaper för den visuella redigeraren och omdirigerings-URL:en &#x200B;](./assets/web-experience-journey-node-content-properties.png){width="700" zoomable="yes"}

1. Klicka på **[!UICONTROL Edit web page]** om du vill [utforma dina webbändringar](./web-experience-design.md).

1. När ändringarna är klara klickar du på vänsterpilen ovanför redigeraren för att gå tillbaka till fliken Innehåll och egenskaperna för den anpassade webbupplevelsenoden.

   Du kan klicka på vänsterpilen längst upp för att återgå till arbetsytan.

## Redigera en webbupplevelse

1. Öppna resan och välj åtgärdsnoden **[!UICONTROL Personalize web experience]**.

1. Klicka på **[!UICONTROL Edit web experience]** om du vill ändra webbkanalens konfiguration eller innehåll.

1. Välj fliken **[!UICONTROL Actions]** och ändra webbkonfigurationen efter behov.

1. Välj fliken **[!UICONTROL Content]** och använd de visuella designverktygen efter behov.

   * _Visuell redigerare_ - Klicka på **[!UICONTROL Edit Content]**.
   * _Icke-visuell redigerare_ - klicka **[!UICONTROL Add a modification]**.

   Mer information finns i [Utformning av webbupplevelser](./web-experience-design.md).

1. När ändringsdefinitionerna är klara klickar du på vänsterpilen ovanför redigeraren för att återgå till innehålls- och webbupplevelseegenskaperna.

   Du kan klicka på vänsterpilen längst upp för att återgå till arbetsytan.

## Omdirigera till URL

När du skapar en webbupplevelse kan du dirigera om besökare till en annan befintlig URL i stället för att skapa en ny variant i innehållsredigeraren. Det här alternativet är användbart när du vill köra ett innehållsexperiment där två olika upplevelser jämförs, i stället för att bara ändra ett fåtal element på en sida.

Skapa till exempel en webbkampanj med två behandlingar:

I Behandling A kan du skapa en webbupplevelse med innehållsredigeraren för halva målpopulationen.

I Behandling B väljer du alternativet _[!UICONTROL Redirect to URL]_&#x200B;för den andra halvan av målpopulationen. Ange URL-adressen till en sida med en alternativ design som du skapade utanför Journey Optimizer B2B edition.

![Ange omdirigering av besökare för att dirigera om besökare till en specifik URL](./assets/web-experience-journey-node-content-visitor-redirection.png){width="500" zoomable="yes"}

>[!NOTE]
>
>När det här alternativet är markerat visas inte webbplatsförhandsvisningen och växlingen _[!UICONTROL Visual editor]_&#x200B;är inaktiverad.

När webbkampanjen är aktiv kan ni spåra hur den webbupplevelse ni definierade i Journey Optimizer B2B edition fungerar mot webbupplevelser som har omdirigerats till den alternativa sidan.

## Testa webbupplevelsen

När innehållsdesignen är klar för webbupplevelsen kan du använda funktionen _Simulera innehåll_ för att förhandsgranska webbsidesändringarna. Om du har infogat anpassat innehåll kan du använda testprofildata för att kontrollera hur innehållet återges. Simuleringsverktygen är tillgängliga på fliken _[!UICONTROL Content]_&#x200B;för webbupplevelsen eller den visuella designredigeraren för innehåll.

1. Klicka på **[!UICONTROL Simulate content]** överst till höger.

1. Välj en testprofil.

1. Lägg till en testprofil för att kontrollera webbsidan med testprofildata.

<!-- This works differently than emails (rely on Marketo data), currently. Will expand when we figure it out -->

## Aktivera din webbupplevelse

Din webbupplevelse aktiveras och blir synlig för publiken när du [publicerar resan](../journeys/create-publish-journey.md#publish-a-journey). Innan du aktiverar en webbupplevelse under en resa bör du tänka på följande:

* Om du publicerar en resa med en webbupplevelse som påverkar samma sidor som en annan resa som redan är aktiv, tillämpas alla ändringar på webbsidorna.

* Om flera resor uppdaterar samma element på webbplatsen har den senast använda ändringen företräde.

### Leveranskrav

Om du vill aktivera leverans av webbupplevelser måste följande inställningar definieras:

* I Adobe Experience Platform Data Collection kontrollerar du att du har en dataström som är definierad med alternativet Adobe Journey Optimizer B2B edition aktiverat under tjänsten Adobe Experience Platform.

  Med den här konfigurationen kan Adobe Experience Platform Edge hantera inkommande händelser korrekt. [Läs mer](https://experienceleague.adobe.com/en/docs/experience-platform/datastreams/configure)

* Kontrollera att du har en sammanfogningsprincip med alternativet _[!UICONTROL Active-On-Edge Merge Policy]_&#x200B;aktiverat i Adobe Experience Platform.

  Välj en profil på Experience Platform-menyn Kund > Profiler > Sammanfoga profiler. [Läs mer](https://experienceleague.adobe.com/en/docs/experience-platform/profile/merge-policies/ui-guide#configure)

  Den här sammanfogningsprincipen används av inkommande kanaler i Journey Optimizer B2B edition för att korrekt aktivera och publicera inkommande webbupplevelser. [Läs mer](https://experienceleague.adobe.com/en/docs/experience-platform/profile/merge-policies/ui-guide)

### Felsökning

Du kan använda Edge Delivery-vyn i Adobe Experience Platform Assurance för att felsöka leveransen av Journey Optimizer B2B edition webbupplevelser. Med denna plugin kan du granska detaljerade förfrågningar, verifiera förväntade gränsanrop och granska profildata. Profildata innehåller identitetskartor, segmentmedlemskap och inställningar för samtycke. Du kan även granska kvalificerade och okvalificerade aktiviteter för begäran.

Mer information om Edge Delivery-vyn i Assurance finns i [Experience Platform-dokumentationen](https://experienceleague.adobe.com/en/docs/experience-platform/assurance/view/edge-delivery).
