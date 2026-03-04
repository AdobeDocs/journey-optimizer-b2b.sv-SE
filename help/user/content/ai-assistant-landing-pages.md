---
title: AI Assistant för landningssidans innehåll
description: Generera material för landningssidor med AI Assistant - skapa sidtext och bilder med referensmaterial och köpa grupproller för målinriktning i Journey Optimizer B2B edition.
feature: Generative AI, Landing Pages, Content
badgeBeta: label="Beta" type="informative" tooltip="Den här funktionen är för närvarande i en begränsad betaversion"
topic: Artificial Intelligence
role: User
level: Beginner
exl-id: d1e818fb-7450-4c13-bc6c-24da5fb71285
source-git-commit: ce4df9a2726cf842c088738521b3e5dd88dd768f
workflow-type: tm+mt
source-wordcount: '2540'
ht-degree: 0%

---

# AI Assistant för landningssidans innehåll {#generative-full-content}

AI Assistant för landningssidinnehåll i [!DNL Adobe Journey Optimizer B2B Edition] använder Adobe funktioner för generering av AI-drivet innehåll och revolutionerar det sätt på vilket marknadsförare skapar professionellt och varumärkesenhetligt innehåll på landningssidor. Med avancerade generativa AI-modeller och god förståelse för varumärkesriktlinjerna genererar AI Assistant automatiskt personaliserat, engagerande och effektivt innehåll. Det utnyttjar ert marknadsföringsmål och optimerar innehållet för varumärkeskonturerade format, layouter, färgton och mycket annat. Med AI Assistant blir det enklare, enklare och krångligare att skapa och genomföra kampanjer och program. Genom att lägga till den här funktionen i arbetsflödena kan du spara tid, förbättra effektiviteten och få bättre resultat.

Ni kan generera kompletta innehållsupplevelser för era landningssidor, både text och bilder. Denna robusta funktionalitet hjälper er att skapa övertygande varumärkesanpassat innehåll som når ut till er målgrupp.

>[!NOTE]
>
>Funktionen finns i Beta-versionen och kan ändras utan föregående meddelande.

>[!IMPORTANT]
>
>Om du vill få åtkomst till de här funktionerna i [!DNL Journey Optimizer B2B Edition] måste du ha behörigheten _[!UICONTROL AI Assistant]_>_[!UICONTROL Generate Content]_. Mer information om hur en produktadministratör kan bevilja funktionsbehörigheter finns i [Redigera roller för produktbehörigheter](../admin/user-management.md#edit-roles-for-product-permissions).

## Riktlinjer och begränsningar

Läs [riktlinjerna och begränsningarna](../ai-assistant/generative-ai-content.md#general-guidelines-and-limitations) innan du börjar använda den här funktionen. [Godkännande av användaravtal &#x200B;](https://www.adobe.com/legal/licenses-terms/adobe-dx-gen-ai-user-guidelines.html){target="_blank"} krävs också innan du kan använda AI-funktioner i [!DNL Journey Optimizer B2B Edition]. Kontakta Adobe om du vill ha mer information.

Med Adobe åtagande att främja genomskinlighet vid användning av generativa AI-verktyg när du skapar media, tillämpar Adobe [innehållsuppgifter](https://helpx.adobe.com/firefly/web/get-started/learn-the-basics/content-credentials-overview.html){target="_blank"} för allt innehåll eller projekt som innehåller en Firefly-genererad resurs när den hämtas eller exporteras.

Följande begränsningar och riktlinjer gäller för AI Assistant-funktioner som används för att generera innehåll på landningssidor i [!DNL Journey Optimizer B2B Edition]:

* Engelska är det enda språk som stöds.
* Genererat innehåll kanske inte är korrekt - dela med dig av dina synpunkter så att Adobe tekniker kan förfina modellerna.
* Du kan överföra flera referensresurser för innehåll, men du kan bara använda en för en viss generation.
* Använd en varumärkesspecifik eller anpassad mall för att generera innehåll för en komplett landningssida. Vi rekommenderar mallar för landningssidor med upp till 8-10 bilder.
* Rapportera eventuella problematiska utdata med hjälp av ikonerna för tummen upp, reglaget ned eller flagga när du väljer genererade varianter.

## Indata och inställningar för generering av innehåll

Du kan generera allt innehåll för en landningssida eller för valda komponenter på sidan. När du använder AI Assistant-verktygen för att generera det innehåll du behöver anger du indata, inklusive uppmaningar och referensinnehåll samt inställningar för text och bilder.

### Fråga

Använd väldefinierade instruktioner för den generativa AI-modellen för att tolka med precision. Marknadsföringsmålet/uppmaningen att ni tillhandahåller påverkar kvaliteten på det genererade innehållet i hög grad.

![Fråga fält](./assets/gen-ai-prompt.png){width="320"}

Mer information om hur du skapar effektiva uppmaningar finns i _[Fråga om bästa praxis](../ai-assistant/generative-ai-content.md#generative-ai-prompting-guide)_.

>[!BEGINSHADEBOX]

**Fråga bibliotek**

Ett effektivt tips är nödvändigt för att skapa så bra innehåll som möjligt. Om du vill ha hjälp med att skapa din fråga klickar du på ikonen _Uppmaningsbibliotek_ ![Uppmaningsbibliotek](../assets/do-not-localize/icon-library.svg) för att få tillgång till ett bibliotek med tips som är ordnade efter mål. Ange text i sökfältet för att hitta en fråga baserad på en nyckelordssträng.

![AI Assistant - gå till frågebiblioteket](./assets/gen-ai-prompt-library.png){width="600" zoomable="no"}

Välj den fråga som bäst återspeglar dina avsedda mål och klicka på **[!UICONTROL Try this Prompt]**. Ersätt eventuella platshållare (till exempel `[Key Feature/Information]`) i fältet _[!UICONTROL Prompt]_&#x200B;med de värden som krävs för att ange varumärket, erbjudandet, kampanjen och användningsfall.

>[!ENDSHADEBOX]

### Textinställningar

Expandera **[!UICONTROL Text settings]** på den högra panelen och ange alternativ för genererad text.

* **[!UICONTROL Buying group]** - Välj den [köpgruppsroll](../buying-groups/buying-groups-role-templates.md) som ska användas för ditt meddelande.
* **[!UICONTROL Marketing journey stage]** - Välj den [inköpsgruppscen](../buying-groups/buying-group-stages.md) som ska användas för att rikta meddelandet.
* **[!UICONTROL Communication strategy]** - Välj det format som passar bäst för den genererade texten.
* **[!UICONTROL Language]** - Välj språk för det genererade innehållet.
* **[!UICONTROL Tone]** - Tonen ska få genklang hos din publik. Du kan till exempel justera meddelandet så att det blir informativt, lekfullt eller övertygande.

![Panelen Textinställningar som visar inköpsgrupp, stadium av marknadsföringsresan, kommunikationsstrategi, språk och tonalternativ](./assets/gen-ai-text-settings.png){width="350" zoomable="yes"}

Klicka på vänsterpilen för att gå tillbaka till huvudpilen _[!UICONTROL Settings]_.

### Bildinställningar

Om du vill inkludera bilder i ditt genererade innehåll expanderar du **[!UICONTROL Image settings]** på den högra panelen och anger alternativen.

Alternativet **[!UICONTROL Generate images using AI]** är inaktiverat som standard. Aktivera den här funktionen och ange följande alternativ för att inkludera genererade bilder i de föreslagna innehållsvarianterna:

<!-- * **[!UICONTROL Generative model]**: Select from available built-in models, custom Firefly models trained on your brand assets, or third-party image generation providers to create images that align with your specific needs and brand requirements. -->
* **[!UICONTROL Aspect ratio]**: När en bildkomponent är markerad bestämmer den här inställningen objektets bredd och höjd. Du kan välja bland vanliga proportioner som 16:9, 4:3, 3:2 eller 1:1, eller så kan du ange en anpassad storlek.
* **[!UICONTROL Content type]**: Typen kategoriserar det visuella elementets karaktär och skiljer mellan olika former av visuell representation, till exempel foton, grafik eller grafik.
* **[!UICONTROL Visual intensity]**: Kontrollera bildens påverkan genom att justera dess intensitet. En lägre inställning (till exempel 2) skapar ett mjukare och mer begränsat utseende, medan en högre inställning (till exempel 10) gör bilden mer levande och visuellt kraftfull.
* **[!UICONTROL Color and tone]**: Det övergripande utseendet på färgerna i en bild och stämningen eller atmosfären som den förmedlar.
* **[!UICONTROL Lighting]**: Den ljusstil som används för bilden, som formar atmosfären och markerar specifika element.
* **[!UICONTROL Composition]**: Elementets placering inom en bilds bildruta.

![Panelen Bildinställningar med alternativen Innehållstyp, Visuell intensitet, Färg och Ton, Ljus och Disposition &#x200B;](./assets/gen-ai-image-settings.png){width="350" zoomable="yes"}

Klicka på vänsterpilen för att gå tillbaka till huvudpilen _[!UICONTROL Settings]_.

### Referensinnehåll

Ladda upp referensmaterial för att generera korrekt varumärkesanpassat innehåll. I annat fall baseras det genererade innehållet på offentligt tillgänglig information. Referensinnehåll fungerar som källa för innehållsgenerering och bildrekommendationer. Riktlinjer och bästa praxis finns i _[Optimerat referensinnehåll](../ai-assistant/generative-ai-content.md#reference-content)_.

Klicka på **[!UICONTROL Upload file]** i inställningarna för **[!UICONTROL Reference content]** för att lägga till resurser som innehåller innehåll som du vill använda för ytterligare kontext.

![Överför fil som ska användas för referensinnehåll](./assets/gen-ai-reference-content-upload.png){width="350" zoomable="yes"}

Filen som ska överföras kan ha följande format: PDF-, JPEG-, PNG- eller ZIP-filer (som innehåller filformat som stöds). Den maximala storleken för en överförd varumärkesresurs är 50 MB. Större filer eller ett stort antal bilder kan fungera, men detta ökar bearbetningstiden.

Om du vill välja en tidigare överförd fil expanderar du listan **[!UICONTROL Uploaded reference content]** och aktiverar den resurs som du vill använda för att generera innehåll.

![Aktivera befintligt referensinnehåll för användning](./assets/gen-ai-reference-content-select.png){width="350" zoomable="yes"}

## Använd de generativa AI-verktygen {#gen-ai-tools}

Öppna innehållsredigeraren för landningssidan och gå till de genererande AI-verktygen på den yttre rälen på den högra panelen för att börja generera ditt innehåll. Välj _AI-assistenten_ ( ![AI-assistenten för innehållsväxling](../../assets/do-not-localize/icon-gen-ai-content.svg){width="25" zoomable="no"} ) för att visa de innehållsgenereringsverktyg som är tillgängliga för det aktuella innehållsvalet.

Följ de här stegen för den typ av generering av landningssidans innehåll som du vill använda:

>[!BEGINTABS]

>[!TAB Helsida]

Följ de här stegen för att använda AI Assistant för att skapa hela landningssidor genom att förfina en befintlig landningssidmall:

1. När [har skapat landningssidan](./landing-pages.md#create-a-landing-page) klickar du på **[!UICONTROL Edit landing page]**.

1. Välj en mall.

   För att generera fullständigt innehåll krävs en mall. Det kan vara en standardmall från Adobe eller en sparad mall. Du kan också använda alternativet _[!UICONTROL Import HTML]_&#x200B;för att importera en mall.

   Mer information om hur du använder en landningssidmall finns i _[Välja en sparad mall eller exempelmall](./landing-pages.md#select-a-saved-or-sample-template)_.

1. Markera ikonen _AI Assistant_ ( ![AI Assistant för innehållsväxling](../../assets/do-not-localize/icon-gen-ai-content.svg){width="25" zoomable="no"} ) på den yttre listen på den högra panelen.

   ![AI Assistant växlar i designområdet för landningssidan](./assets/gen-ai-full-landing-page-ai-panel.png){width="600" zoomable="yes"}

   Inställningarna för AI Assistant till höger återspeglar genereringsinställningarna för den fullständiga landningssidan.

1. (Beta) Markera din **[!UICONTROL Brand]** för att se till att det AI-genererade innehållet överensstämmer med dina varumärkesspecifikationer.

   Om det inte finns några publicerade varumärken klickar du på **[!UICONTROL Create a brand]** för att definiera dina [återanvändbara varumärkesriktlinjer](./brands-overview.md).

1. I fältet **[!UICONTROL Prompt]** anger du en beskrivning av vad du vill generera.

   Använd [promptbiblioteket](#prompt-library) om du behöver hjälp med att skapa en effektiv fråga.

   ![AI Assistant - fråga biblioteket om du vill generera innehåll för landningssidor](./assets/email-designer-ai-assistant-full.png){width="600" zoomable="yes"}

   >[!TIP]
   >
   >Om du inte är van vid att fråga efter genererat innehåll går du igenom _[Bästa praxis](../ai-assistant/generative-ai-content.md#generative-ai-prompting-guide)_ när du frågar.

1. Slutför inställningarna för innehållsanvisningar för att anpassa det genererade innehållet:

   * [**[!UICONTROL Text settings]**](#text-settings) - Ange vägledning för det genererade textinnehållet.
   * [**[!UICONTROL Image settings]**](#image-settings) - Om du vill inkludera bilder i det genererade innehållet aktiverar du bildgenerering och tillhandahåller vägledning.
   * [**[!UICONTROL Reference content]**](#reference-content) - Ange den innehållsresurs som fungerar som källa för innehållsgenerering.

1. Klicka på **[!UICONTROL Generate]** när din fråga och dina inställningar är klara.

1. Bläddra nedåt på AI Assistant-panelen och bläddra igenom de varianter som skapas för att se vilken som passar bäst.

   * Klicka på ikonen _Helskärm_ ( ![Helskärm &#x200B;](../assets/do-not-localize/icon-full-screen.svg) ) för att öppna dialogrutan _[!UICONTROL Generate Landing Page]_

   * Om det behövs kan du använda [förfiningsåtgärderna](#refine-a-variation) för att finjustera variationen så att den uppfyller dina exakta krav.

   * [Skicka feedback](#submit-variation-feedback) för de genererade varianterna genom att klicka på ikonen _Thumbs Up_, _Thumbs Down_ eller _Flag_ och välja den orsak som bäst sammanfattar dina kommentarer.

1. Klicka på **[!UICONTROL Select]** om du vill ersätta mallinnehållet med den valda varianten och återgå till designområdet för landningssidan.

   Du kan använda redigerings- och formateringsverktygen på arbetsytan för att ändra det genererade innehållet samt alternativen _[!UICONTROL Settings]_&#x200B;och&#x200B;_[!UICONTROL Style]_ till höger.

>[!TAB Endast text]

Följ de här stegen för att använda AI Assistant för att förfina eller förbättra textinnehållet för en befintlig landningssida:

1. I designområdet för landningssidan väljer du en _Text_ -komponent för att ange det specifika innehållet som mål.

1. Markera ikonen _AI Assistant_ ( ![AI Assistant för innehållsväxling](../../assets/do-not-localize/icon-gen-ai-content.svg){width="25" zoomable="no"} ) på den yttre listen på den högra panelen.

   ![AI Assistant växlar i designområdet för landningssidan](./assets/email-designer-ai-assistant-button.png){width="600" zoomable="yes"}

   Inställningarna till höger återspeglar inställningarna för innehållsgenerering för textkomponenten.

1. (Beta) Markera din **[!UICONTROL Brand]** för att se till att det AI-genererade innehållet överensstämmer med dina varumärkesspecifikationer.

   Om det inte finns några publicerade varumärken klickar du på **[!UICONTROL Create a brand]** för att [definiera riktlinjerna för ditt återanvändbara varumärke](./brands-overview.md).

1. I fältet **[!UICONTROL Prompt]** anger du en beskrivning av vad du vill generera.

   ![AI-assistenten - textinställningar](./assets/email-designer-ai-assistant-text.png){width="600" zoomable="yes"}

   Använd [promptbiblioteket](#prompt-library) om du behöver hjälp med att skapa en effektiv fråga.

1. Slutför inställningarna för innehållsanvisningar för att anpassa det genererade innehållet:

   * [**[!UICONTROL Text settings]**](#text-settings) - Ange vägledning för det genererade textinnehållet.

   * [**[!UICONTROL Reference content]**](#reference-content) - Ange de innehållsresurser som fungerar som källa för innehållsgenerering.

1. Klicka på **[!UICONTROL Generate]** när din fråga och dina inställningar är klara.

1. Bläddra nedåt på AI Assistant-panelen och bläddra igenom de varianter som skapas för att se vilken som passar bäst.

   * Klicka på ikonen _Helskärm_ ( ![Helskärm &#x200B;](../assets/do-not-localize/icon-full-screen.svg) ) för att öppna dialogrutan _[!UICONTROL Generate Text]_

   * Om det behövs kan du använda [förfiningsåtgärderna](#refine-a-variation) för att finjustera variationen så att den uppfyller dina exakta krav.

   * [Skicka feedback](#submit-variation-feedback) för de genererade varianterna genom att klicka på ikonen _Thumbs Up_, _Thumbs Down_ eller _Flag_ och välja den orsak som bäst sammanfattar dina kommentarer.

1. När du har önskat innehåll klickar du på **[!UICONTROL Select]** för att ersätta texten med den valda varianten och återgå till designutrymmet för landningssidan.

   Du kan använda redigerings- och formateringsverktygen på arbetsytan för att ändra texten, samt alternativen _[!UICONTROL Settings]_&#x200B;och&#x200B;_[!UICONTROL Style]_ till höger.

>[!TAB Endast bild]

Följ de här stegen för att använda AI Assistant för att förfina eller förbättra bildinnehållet för en befintlig landningssida:

1. Markera en _Bild_ -komponent i designområdet för landningssidan för att ange det specifika innehållet som mål.

1. Markera ikonen _AI Assistant_ ( ![AI Assistant för innehållsväxling](../../assets/do-not-localize/icon-gen-ai-content.svg){width="25" zoomable="no"} ) på den yttre listen på den högra panelen.

   ![AI Assistant växlar i designområdet för landningssidan](./assets/email-designer-ai-assistant-button.png){width="600" zoomable="yes"}

   Inställningarna för AI-assistenten till höger återspeglar bildkomponentens genereringsinställningar.

1. (Beta) Markera din **[!UICONTROL Brand]** för att se till att det AI-genererade innehållet överensstämmer med dina varumärkesspecifikationer.

   Om det inte finns några publicerade varumärken klickar du på **[!UICONTROL Create a brand]** för att [definiera riktlinjerna för ditt återanvändbara varumärke](./brands-overview.md).

1. Ange en beskrivning av vad du vill ha i fältet **[!UICONTROL Prompt]**.

   ![AI-assistenten - textinställningar](./assets/email-designer-ai-assistant-image.png){width="600" zoomable="yes"}

   Använd [promptbiblioteket](#prompt-library) om du behöver hjälp med att skapa en effektiv fråga.

1. Slutför inställningarna för innehållsanvisningar för att anpassa det genererade innehållet:

   * [**[!UICONTROL Image settings]**](#image-settings) - Om du vill inkludera bilder i det genererade innehållet aktiverar du bildgenerering och tillhandahåller vägledning.

   * [**[!UICONTROL Reference content]**](#reference-content) - Ange de innehållsresurser som fungerar som källa för innehållsgenerering.

1. När du är nöjd med uppmaningen och inställningarna klickar du på **[!UICONTROL Generate]**.

   AI Assistant bearbetar begäran och genererar bilder som passar bäst utifrån uppmaningen och andra indata.

   >[!IMPORTANT]
   >
   >Om det inte finns några bilder i referensinnehållet eller om det inte finns några bilder som är relevanta för inmatningsprompten, är utdata tomma.

1. Bläddra igenom de genererade variationerna eller klicka på ikonen _Helskärm_ ( ![Helskärmsikon](../assets/do-not-localize/icon-full-screen.svg) ) för att öppna dialogrutan _[!UICONTROL Generate Image]_.

   Dialogrutan innehåller ytterligare utrymme för att jämföra variationerna, justera bild- och referensinnehållsinställningarna (om det behövs) och återskapa variationerna.

   Du kan välja en variant och klicka på **[!UICONTROL Generate Similar]** om du vill generera ytterligare bilder som liknar den valda varianten. Du kan också klicka på **[!UICONTROL Edit in Adobe Express]** om du vill göra egna ändringar i bilden. Se [Snabbåtgärder i Adobe Express](./image-edit-adobe-express.md#quick-actions-in-adobe-express) för mer information om hur du använder Adobe Express för att förfina dina bilder.

   ![AI Assistant-förhandsgranskning av textvariation och förfiningsalternativ](./assets/email-designer-ai-assistant-image-refine.png){width="700" zoomable="yes"}

   Du kan också [skicka feedback](#submit-variation-feedback) för de genererade variationerna.

1. Markera bilden som du vill använda och klicka på **[!UICONTROL Select]** för att ersätta bilden eller platshållaren med det valda objektet och återgå till designutrymmet för landningssidan.

   Du kan använda redigerings- och formateringsverktygen på arbetsytan för att ändra bilden samt alternativen _[!UICONTROL Settings]_&#x200B;och&#x200B;_[!UICONTROL Style]_ till höger.

>[!ENDTABS]

## Förhandsgranska och förfina innehåll {#refine-finalize}

När du har genererat innehållsvariationer kan du finjustera resultatet för att säkerställa att det uppfyller dina exakta krav. Granska varumärkesjusteringen, justera ton och språk och förbered innehållet för ett granskningsbart utkast. Du kan även skicka in feedback för en variation som hjälper dig att utbilda AI Assistant och förbättra framtida resultat.

### Öppna helskärmsvyn

1. Bläddra bland **[!UICONTROL Variations]** efter den första genereringen av innehåll.

1. Identifiera den variation som är bäst för dina mål och klicka på ikonen _Helskärm_ ( ![Helskärm &#x200B;](../assets/do-not-localize/icon-full-screen.svg) ) för att öppna dialogrutan.

   ![Öppna dialogrutan Generera](./assets/gen-ai-preview-text-refine.png){width="700" zoomable="yes"}

1. När du är nöjd med den valda variationen klickar du på **[!UICONTROL Select]** för att använda den på arbetsytan.

### Förfina en variation

Klicka på alternativet **[!UICONTROL Refine]** för att få tillgång till ytterligare anpassningsfunktioner för landningssidor och textvarianter:

* **[!UICONTROL Elaborate]** - AI Assistant kan hjälpa dig att expandera specifika ämnen och ge dig ytterligare information för bättre förståelse och engagemang.

* **[!UICONTROL Summarize]** - Lång information kan överlagra sidvisningsprogram. Använd AI Assistant för att komprimera viktiga punkter till tydliga, kortfattade sammanfattningar som får dem att lyssna och uppmuntrar dem att läsa vidare.

* **[!UICONTROL Rephrase]** - Skriv om meddelandet med bibehållen betydelse. Med det här alternativet kan du generera alternativa ordalydelser, förbättra flödet eller justera fraser utan att ändra huvudbudskapet.

* **[!UICONTROL Use simpler language]** - Förenkla språket och säkerställ tydlighet och tillgänglighet för en större publik.

* **[!UICONTROL Translate]** - Översätt texten till ett annat språk. (Engelska är för närvarande det enda språk som stöds.)

* **[!UICONTROL Change tone]** - Justera tonen i meddelandet så att det passar din kommunikationsstil, till exempel för att göra det mer användarvänligt, professionellt, brådskande eller inspirerande.

* **[!UICONTROL Change Communication strategy]** - Ändra meddelandetillvägagångssättet baserat på dina mål, till exempel skapa en tränglighet eller framhäva en spännande tilltalande upplevelse.

<!-- * **[!UICONTROL Use as reference content]** - Select this option to use the variant as the reference content for generating other results. -->

![Förfina meny med alternativ för innehållsförfining](./assets/gen-ai-preview-text-refine.png){width="700" zoomable="yes"}

### Skicka feedback

Ge feedback för de genererade varianterna genom att klicka på ikonen _Tummen uppåt_, _Tummen nedåt_ eller _Flagga_ och välj den orsak som bäst sammanfattar dina synpunkter.

![AI Assistant - förhandsgranska de genererade variationerna](./assets/gen-ai-preview-feedback-thumbs-up.png){width="700" zoomable="yes"}

### Kontrollera varumärkets justering (Beta)

<!-- Are we surfacing scoring here in the future, or will it be a separate post-creation task? 1. Click the percentage icon to view your **[!UICONTROL Brand Alignment Score]** and identify any misalignments with your brand. -->

Tack vare utvärderingen och poängsättningen av varumärkesanpassningen kan ni säkerställa enhetlighet i fråga om ton, meddelanden och visuell identitet i alla era kampanjer, samtidigt som ni fungerar som en kvalitetskontroll innan ert innehåll publiceras. När innehållet på landningssidan är klart klickar du på ikonen _Varumärkesjustering_ ( ![Varumärkesjustering](../assets/do-not-localize/icon-brand-compliance.svg) ) till höger för att öppna den högra panelen _Märkesjustering_ i designområdet för landningssidan.

![Få åtkomst till varumärkesjusteringsverktygen](./assets/brands-alignment-sidebar.png){width="600" zoomable="yes"}

Mer information finns i [Validera din varumärkesjustering](./brand-alignment.md#validate-your-brand-alignment)
