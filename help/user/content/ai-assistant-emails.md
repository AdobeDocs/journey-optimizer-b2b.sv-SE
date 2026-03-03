---
title: AI-assistenten för e-postinnehåll
description: Generera e-postinnehåll med AI Assistant - skapa meddelandeinnehåll, ämnesrader och rubriker med varumärkesresurser och köpa grupprollmål i  [!DNL Journey Optimizer B2B Edition].
feature: AI Assistant, Generative AI, Email Authoring
role: User
exl-id: b66d72e4-3afc-49ad-9bc2-bedc047ecca4
source-git-commit: c7c08dc1d9b041bfc83cf8b5766a953fa765f4c9
workflow-type: tm+mt
source-wordcount: '3426'
ht-degree: 0%

---

# AI-assistenten för e-postinnehåll

I takt med att marknadsföringsbranschen blir mer konkurrenskraftig söker varumärkena effektiva sätt att snabbt och effektivt generera slagkraftigt innehåll. AI Assistant för e-postredigering i [!DNL Adobe Journey Optimizer B2B Edition] är en Adobe AI-baserad funktion för innehållsgenerering som revolutionerar det sätt på vilket marknadsförare skapar professionellt och varumärkesenhetligt e-postinnehåll. Med avancerade generativa AI-modeller och god förståelse för varumärkesriktlinjerna genererar AI Assistant automatiskt personaliserat, engagerande och effektivt innehåll. Det utnyttjar ert marknadsföringsmål och optimerar innehållet för varumärkeskonturerade format, layouter, färgton och mycket annat. AI Assistant gör det enkelt att skapa och genomföra e-postkampanjer intuitivt, utan krångel. Genom att lägga till den här funktionen i arbetsflödena kan du spara tid, förbättra effektiviteten och få bättre resultat.

Den här nya funktionen ger snabb generering av innehåll för att skapa kompletta e-postmeddelanden eller som är avsett för komponenter i e-poststrukturen. För bilder kan du generera nya bildresurser eller helt enkelt generera rekommendationer inifrån bildkatalogen i varumärkesresursen. Du kan också använda den här funktionen för att generera optimala ämnesrader och preheaders för att påverka öppningsfrekvensen för e-postmeddelanden.

>[!IMPORTANT]
>
>Om du vill få åtkomst till de här funktionerna i Adobe Journey Optimizer B2B edition måste du ha behörighet _[!UICONTROL AI Assistant]_>_[!UICONTROL Generate Content]_. Mer information om hur en produktadministratör kan bevilja funktionsbehörigheter finns i [Redigera roller för produktbehörigheter](../admin/user-management.md#edit-roles-for-product-permissions).

## Riktlinjer och begränsningar

Läs [riktlinjerna och begränsningarna](../ai-assistant/generative-ai-content.md#general-guidelines-and-limitations) innan du börjar använda den här funktionen. [Godkännande av användaravtal ](https://www.adobe.com/legal/licenses-terms/adobe-dx-gen-ai-user-guidelines.html){target="_blank"} krävs också innan du kan använda AI-funktioner i [!DNL Journey Optimizer B2B Edition]. Kontakta Adobe om du vill ha mer information.

Med Adobe åtagande att främja genomskinlighet vid användning av generativa AI-verktyg när du skapar media, tillämpar Adobe [innehållsuppgifter](https://helpx.adobe.com/firefly/web/get-started/learn-the-basics/content-credentials-overview.html){target="_blank"} för allt innehåll eller projekt som innehåller en Firefly-genererad resurs när den hämtas eller exporteras.

Följande begränsningar och riktlinjer gäller för AI Assistant-funktioner som används för att generera e-postinnehåll i [!DNL Journey Optimizer B2B Edition]:

* Engelska är det enda språk som stöds.
* Genererat innehåll kanske inte är korrekt - dela med dig av dina synpunkter så att Adobe tekniker kan förfina modellerna.
* Du kan överföra flera referensresurser för innehåll, men du kan bara använda en för en viss generation.
* Använd en varumärkesspecifik eller anpassad mall för att generera innehåll för ett fullständigt e-postmeddelande. E-postmallar med upp till 8-10 bilder rekommenderas.
* Rapportera eventuella problematiska utdata med hjälp av ikonerna för tummen upp, reglaget ned eller flagga när du väljer genererade varianter.

## Indata och inställningar för generering av innehåll

Du kan generera fullständigt innehåll för ett e-postmeddelande eller för valda komponenter i e-postmeddelandet. När du använder AI Assistant-verktygen för att generera det innehåll du behöver anger du indata, inklusive uppmaningar och referensinnehåll samt inställningar för text och bilder.

### Fråga

Använd väldefinierade instruktioner för den generativa AI-modellen för att tolka med precision. Marknadsföringsmålet/uppmaningen att ni tillhandahåller påverkar kvaliteten på det genererade innehållet i hög grad.

![Fråga fält](./assets/gen-ai-prompt.png){width="320"}

Mer information om hur du skapar effektiva uppmaningar finns i _[Fråga om bästa praxis](../ai-assistant/generative-ai-content.md#generative-ai-prompting-guide)_.

>[!BEGINSHADEBOX]

#### Fråga bibliotek

Ett effektivt tips är nödvändigt för att skapa så bra innehåll som möjligt. Om du vill ha hjälp med att skapa din fråga klickar du på ikonen _Uppmaningsbibliotek_ ![Uppmaningsbibliotek](../assets/do-not-localize/icon-library.svg) för att få tillgång till ett bibliotek med tips som är ordnade efter mål. Ange text i sökfältet för att hitta en fråga baserad på en nyckelordssträng.

![AI Assistant - gå till frågebiblioteket](./assets/gen-ai-prompt-library.png){width="600" zoomable="no"}

Välj den fråga som bäst återspeglar dina avsedda mål och klicka på **[!UICONTROL Try this Prompt]**. Ersätt eventuella platshållare (till exempel `[Key Feature/Information]`) i fältet _[!UICONTROL Prompt]_med de värden som krävs för att ange varumärket, erbjudandet, kampanjen och användningsfall.

>[!ENDSHADEBOX]

### Textinställningar

Expandera **[!UICONTROL Text settings]** på den högra panelen och ange alternativ för genererad text.

* **[!UICONTROL Buying group]** - Välj den [köpgruppsroll](../buying-groups/buying-groups-role-templates.md) som ska användas för ditt meddelande. [!DNL Journey Optimizer B2B Edition] har fem standardroller för B2B-inköpsgrupper direkt. Varje inköpsgruppsroll har ett tydligt meddelandefokus:

  | Roll | Meddelandefokus |
  | ---- | --------------- |
  | Verkställande kommitté | Produktinformation <br/>Priser <br/>Information om teknisk integration <br/>Funktioner och funktioner |
  | Påverkande | Kvalitetsbevis <br/>Enkel implementering <br/>Ämnesexpertis <br/>Konkurrensfördelar |
  | Beslutsfattare | Avkastning på investering <br/>Ekonomiskt värde (RoI) <br/>Nöjda kunder |
  | Yrkesverksamma | Enkel användning <br/>Produktfunktioner och -funktionalitet <br/>Produktkompatibilitet <br/>Enkel produktintegrering |
  | Champion | Utbildningsinnehåll <br/>Tankledarinnehåll <br/>Nöjda kunder |

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

![Panelen Bildinställningar med alternativen Innehållstyp, Visuell intensitet, Färg och Ton, Ljus och Disposition ](./assets/gen-ai-image-settings.png){width="350" zoomable="yes"}

Klicka på vänsterpilen för att gå tillbaka till huvudpilen _[!UICONTROL Settings]_.

### Referensinnehåll

Ladda upp referensmaterial för att generera korrekt varumärkesanpassat innehåll. I annat fall baseras det genererade innehållet på offentligt tillgänglig information. Referensinnehåll fungerar som källa för innehållsgenerering och bildrekommendationer. Riktlinjer och bästa praxis finns i _[Optimerat referensinnehåll](../ai-assistant/generative-ai-content.md#reference-content)_.

Klicka på **[!UICONTROL Upload file]** i inställningarna för **[!UICONTROL Reference content]** för att lägga till resurser som innehåller innehåll som du vill använda för ytterligare kontext.

![Överför fil som ska användas för referensinnehåll](./assets/gen-ai-reference-content-upload.png){width="350" zoomable="yes"}

Filen som ska överföras kan ha följande format: PDF-, JPEG-, PNG- eller ZIP-filer (som innehåller filformat som stöds). Den maximala storleken för en överförd varumärkesresurs är 50 MB. Större filer eller ett stort antal bilder kan fungera, men detta ökar bearbetningstiden.

Om du vill välja en tidigare överförd fil expanderar du listan **[!UICONTROL Uploaded reference content]** och aktiverar den resurs som du vill använda för att generera innehåll.

![Aktivera befintligt referensinnehåll för användning](./assets/gen-ai-reference-content-select.png){width="350" zoomable="yes"}

## Generera e-postegenskaper med AI Assistant

När du [lägger till en e-poståtgärd](./add-email.md#add-an-email-action-node-in-a-journey) till en kontoresa, definierar du en uppsättning e-postegenskaper som används för att skicka e-postmeddelandet. AI Assistant kan hjälpa till att få bättre e-postengagemang genom att generera rekommenderat innehåll för e-postens **_ämnesrad_** och **_preheader_**.

När du skapar ett e-postmeddelande från en resa eller öppnar ett befintligt e-postmeddelande från en kundnod visas sidan för förhandsgranskning av e-post med _[!UICONTROL Email properties]_till höger. På fliken_[!UICONTROL Summary]_ kan du använda verktygen för innehållsgenerering i AI Assistant för att generera en ämnesrad, en preheader eller båda.

>[!BEGINTABS]

>[!TAB Ämnesradgenerering]

I följande steg beskrivs aktivitetssekvensen för hur du använder AI Assistant för att generera en optimerad ämnesrad för e-postmeddelandet:

1. Bläddra nedåt till fältet **[!UICONTROL Subject line]** på panelen _Sammanfattning_ med fliken _Detaljer_ markerad.

1. Klicka på ikonen för AI-assistenten ( ![AI Assistant-ikon](../../assets/do-not-localize/icon-gen-ai-email-properties.svg){width="30"} ) till höger om fältet.

   ![AI Assistant-åtkomst till ämnesrad för e-post](./assets/email-properties-ai-assistant-subject-line-icon.png){width="600" zoomable="yes"}

   Dialogrutan _[!UICONTROL Generate Subject Line]_öppnas med genereringsinställningarna för e-postens ämnesrad.

1. (Obligatoriskt) I fältet **[!UICONTROL Prompt]** anger du en beskrivning av vad du vill generera.

   Använd [promptbiblioteket](#prompt-library) om du behöver hjälp med att skapa en effektiv fråga.

1. (Valfritt) Slutför inställningarna för innehållshjälpmedel för att få ytterligare indata för generering av förrubriken:

   * [**[!UICONTROL Text settings]**](#text-settings) - Ange vägledning för det genererade textinnehållet.
   * [**[!UICONTROL Reference content]**](#reference-content) - Ange den innehållsresurs som fungerar som källa för innehållsgenerering.

1. Klicka på **[!UICONTROL Generate]** när din fråga och dina inställningar är klara.

   De genererade varianterna visas i dialogrutan.

   ![AI-assistenten - Ämnesraden som genereras i e-postmeddelanden ](./assets/email-properties-ai-assistant-subject-line.png){width="600" zoomable="yes"}

1. Rulla på AI Assistant-panelen och bläddra igenom de genererade variationerna för att se vilken som passar bäst.

   Du kan [skicka feedback](#submit-variation-feedback) för en genererad variant genom att klicka på ikonen _Thumbs Up_, _Thumbs Down_ eller _Flag_ och välja den orsak som bäst sammanfattar din feedback.

1. Klicka på alternativet **[!UICONTROL Refine]** om du vill komma åt ytterligare anpassningsfunktioner:

   * **[!UICONTROL Rephrase]** - Skriv om meddelandet med bibehållen betydelse. Med det här alternativet kan du generera alternativa ordalydelser eller justera fraser utan att ändra huvudbudskapet.

   * **[!UICONTROL Use simpler language]** - Förenkla språket och säkerställ tydlighet och tillgänglighet för en större publik.

   * **[!UICONTROL Translate]** - Översätt texten till ett annat språk. (Engelska är för närvarande det enda språk som stöds. Andra språk planeras för framtida versioner.)

   * **[!UICONTROL Change tone]** - Justera tonen i meddelandet så att det passar din kommunikationsstil, till exempel för att göra det mer användarvänligt, professionellt, brådskande eller inspirerande.

   * **[!UICONTROL Change Communication strategy]** - Ändra meddelandetillvägagångssättet baserat på dina mål, till exempel skapa en tränglighet eller framhäva en spännande tilltalande upplevelse.

   ![AI Assistant - förfining av ämnesrad](./assets/email-properties-ai-assistant-subject-line-refine.png){width="600" zoomable="yes"}

1. Klicka på **[!UICONTROL Select]** om du vill ersätta ämnesraden med den valda varianten och återgå till e-postegenskaperna.

>[!TAB Förhuvudgenerering]

En e-postförrubrik är den korta sammanfattningstexten som följer efter ämnesraden när ett e-postmeddelande visas i inkorgen. Det är ett valfritt element för ett e-postmeddelande, men en utmärkt möjlighet att förbättra engagemanget. I följande steg beskrivs aktivitetssekvensen för hur du använder AI Assistant för att generera en optimerad förrubrik för e-postmeddelandet:

1. Bläddra nedåt och markera kryssrutan **[!UICONTROL Preheader]** på panelen _Sammanfattning_ med fliken _Detaljer_ markerad.

   ![AI-assistentåtkomst för e-postförrubrik](./assets/email-properties-ai-assistant-preheader-icon.png){width="600" zoomable="yes"}

   Dialogrutan _[!UICONTROL Generate Preheader]_öppnas med genereringsinställningarna för e-postförrubriken.

1. (Obligatoriskt) I fältet **[!UICONTROL Prompt]** anger du en beskrivning av vad du vill generera.

   Använd [promptbiblioteket](#prompt-library) om du behöver hjälp med att skapa en effektiv fråga.

1. (Valfritt) Slutför inställningarna för innehållshjälpmedel för att få ytterligare indata för generering av förrubriken:

   * [**[!UICONTROL Text settings]**](#text-settings) - Ange vägledning för det genererade textinnehållet.
   * [**[!UICONTROL Reference content]**](#reference-content) - Ange den innehållsresurs som fungerar som källa för innehållsgenerering.

1. Klicka på **[!UICONTROL Generate]** när din fråga och dina inställningar är klara.

   De genererade varianterna visas i dialogrutan.

   ![AI-assistenten - varianter som genererats av e-postförhuvudet](./assets/email-properties-ai-assistant-preheader.png){width="600" zoomable="yes"}

1. Rulla på AI Assistant-panelen och bläddra igenom de genererade variationerna för att se vilken som passar bäst.

   Du kan [skicka feedback](#submit-variation-feedback) för en genererad variant genom att klicka på ikonen _Thumbs Up_, _Thumbs Down_ eller _Flag_ och välja den orsak som bäst sammanfattar din feedback.

1. Klicka på alternativet **[!UICONTROL Refine]** om du vill komma åt ytterligare anpassningsfunktioner:

   * **[!UICONTROL Rephrase]** - Skriv om meddelandet med bibehållen betydelse. Med det här alternativet kan du generera alternativa ordalydelser eller justera fraser utan att ändra huvudbudskapet.

   * **[!UICONTROL Use simpler language]** - Förenkla språket och säkerställ tydlighet och tillgänglighet för en större publik.

   * **[!UICONTROL Translate]** - Översätt texten till ett annat språk. (Engelska är för närvarande det enda språk som stöds. Andra språk planeras för framtida versioner.)

   * **[!UICONTROL Change tone]** - Justera tonen i meddelandet så att det passar din kommunikationsstil, till exempel för att göra det mer användarvänligt, professionellt, brådskande eller inspirerande.

   * **[!UICONTROL Change Communication strategy]** - Ändra meddelandetillvägagångssättet baserat på dina mål, till exempel skapa en tränglighet eller framhäva en spännande tilltalande upplevelse.

   ![AI Assistant - fördefiniering av sidhuvuden](./assets/email-properties-ai-assistant-preheader-refine.png){width="500" zoomable="yes"}

1. Klicka på **[!UICONTROL Select]** om du vill ersätta förrubriken med den valda varianten och återgå till e-postegenskaperna.

>[!ENDTABS]

## Generera e-postinnehåll med AI Assistant {#generative-ai-email-design}

När du har [skapat och anpassat din e-post](./email-authoring.md) använder du AI Assistant i [!DNL Journey Optimizer B2B Edition], som drivs av generativ AI för att lyfta ditt innehåll i e-postbrödtexten till nästa nivå.

I e-postdesignområdet kan AI Assistant hjälpa dig att optimera effekten av dina leveranser genom att generera hela e-postbrödtexten, riktat textinnehåll och bilder som får genklang hos din målgrupp. Den här optimeringen av era e-postkampanjer är utformad för att ge ett bättre engagemang. Välj _AI-assistenten_ ( ![AI-assistentmenyn för att växla](../../assets/do-not-localize/icon-gen-ai-content.svg){width="25" zoomable="no"} ) för att visa de innehållsgenereringsverktyg som är tillgängliga för det aktuella innehållsvalet.

![AI Assistant växlar i e-postdesignern](./assets/email-designer-ai-assistant-button.png){width="600" zoomable="yes"}

Följ de här stegen för den typ av generering av e-postinnehåll som du vill använda:

>[!BEGINTABS]

>[!TAB Fullständig e-postgenerering]

Följ de här stegen för att använda AI Assistant för att skapa fullständig e-post genom att förfina en befintlig e-postmall:

1. Klicka på **[!UICONTROL Edit email content]** när du har [skapat e-postmeddelandet](./add-email.md).

1. Välj en mall.

   För att generera fullständigt innehåll krävs en mall. Det kan vara en standardmall från Adobe eller en sparad mall. Du kan också använda alternativet _[!UICONTROL Import HTML]_för att importera en mall.

   Mer information om hur du använder en e-postmall finns i _[Välja en mall](./email-authoring.md#select-a-template)_.

1. I e-postdesignområdet öppnar du AI Assistant-menyn genom att klicka på ikonen ( ![AI Assistant-menyn till höger](../../assets/do-not-localize/icon-gen-ai-content.svg){width="25"} ).

   AI Assistant-inställningarna till höger återspeglar _Generera e-post_.

   ![AI Assistant - fråga biblioteket om du vill generera e-postinnehåll](./assets/email-designer-ai-assistant-full.png){width="600" zoomable="yes"}

1. Välj din **[!UICONTROL Brand]** för att se till att det AI-genererade innehållet överensstämmer med dina varumärkesspecifikationer.

   Om det inte finns några publicerade varumärken klickar du på **[!UICONTROL Create a brand]** för att definiera dina [återanvändbara varumärkesriktlinjer](./brands-overview.md).

1. I fältet **[!UICONTROL Prompt]** anger du en beskrivning av vad du vill generera.

   Använd [promptbiblioteket](#prompt-library) om du behöver hjälp med att skapa en effektiv fråga.

   >[!TIP]
   >
   >Om du inte är van vid att fråga efter genererat innehåll går du igenom _[Bästa praxis](../ai-assistant/generative-ai-content.md#generative-ai-prompting-guide)_ när du frågar.

1. Slutför inställningarna för innehållsanvisningar för att anpassa det genererade innehållet:

   * [**[!UICONTROL Text settings]**](#text-settings) - Ange vägledning för det genererade textinnehållet.
   * [**[!UICONTROL Image settings]**](#image-settings) - Om du vill inkludera bilder i det genererade innehållet aktiverar du bildgenerering och tillhandahåller vägledning.
   * [**[!UICONTROL Reference content]**](#reference-content) - Ange den innehållsresurs som fungerar som källa för innehållsgenerering.

1. Klicka på **[!UICONTROL Generate]** när din fråga och dina inställningar är klara.

   De genererade variationerna visas på den högra panelen.

1. Bläddra igenom de genererade variationerna eller klicka på ikonen _Helskärm_ ( ![Helskärmsikon](../assets/do-not-localize/icon-full-screen.svg) ) för att öppna dialogrutan _[!UICONTROL Generate Email]_.

   Dialogrutan innehåller ytterligare utrymme för att jämföra variationerna, justera inställningarna för text och referensinnehåll (om det behövs) och för att generera om variationerna.

   Du kan också finjustera en variation genom att använda förfiningsåtgärder och skicka feedback för de genererade variationerna. Mer information om variationsförfining och feedback finns i _[Förhandsgranska och innehållsförfining](#preview-and-content-refinement)_.

   ![AI Assistant-förhandsgranskning av e-postvariationer och förfiningsalternativ](./assets/email-designer-ai-assistant-full-refine.png){width="700" zoomable="yes"}

1. Klicka på **[!UICONTROL Select]** om du vill ersätta mallinnehållet med den valda varianten och återgå till e-postdesignområdet.

   Du kan använda redigerings- och formateringsverktygen på arbetsytan för att ändra det genererade innehållet samt alternativen _[!UICONTROL Settings]_och_[!UICONTROL Style]_ till höger.

>[!TAB Endast text]

Följ de här stegen för att använda AI Assistant för att förfina eller förbättra textinnehållet i ett befintligt e-postmeddelande:

1. I e-postdesignområdet väljer du en _Text_ -komponent för att ange det specifika innehållet som mål.

1. Markera ikonen _AI Assistant_ ( ![AI Assistant-menyn ](../../assets/do-not-localize/icon-gen-ai-content.svg){width="25"} ) på den yttre listen på den högra panelen.

   Inställningarna till höger återspeglar inställningarna för innehållsgenerering för textkomponenten.

1. Välj din **[!UICONTROL Brand]** för att se till att det AI-genererade innehållet överensstämmer med dina varumärkesspecifikationer.

   Om det inte finns några publicerade varumärken klickar du på **[!UICONTROL Create a brand]** för att [definiera riktlinjerna för ditt återanvändbara varumärke](./brands-overview.md).

1. I fältet **[!UICONTROL Prompt]** anger du en beskrivning av vad du vill generera.

   ![AI-assistenten - textinställningar](./assets/email-designer-ai-assistant-text.png){width="600" zoomable="yes"}

   Använd [promptbiblioteket](#prompt-library) om du behöver hjälp med att skapa en effektiv fråga.

1. Slutför inställningarna för innehållsanvisningar för att anpassa det genererade innehållet:

   * [**[!UICONTROL Text settings]**](#text-settings) - Ange vägledning för det genererade textinnehållet.

   * [**[!UICONTROL Reference content]**](#reference-content) - Ange de innehållsresurser som fungerar som källa för innehållsgenerering.

1. Klicka på **[!UICONTROL Generate]** när din fråga och dina inställningar är klara.

1. Bläddra igenom de genererade variationerna eller klicka på ikonen _Helskärm_ ( ![Helskärmsikon](../assets/do-not-localize/icon-full-screen.svg) ) för att öppna dialogrutan _[!UICONTROL Generate Text]_.

   Dialogrutan innehåller ytterligare utrymme för att jämföra variationerna, justera inställningarna för text och referensinnehåll (om det behövs) och för att generera om variationerna.

   Du kan också finjustera en variation genom att använda förfiningsåtgärder och skicka feedback för de genererade variationerna. Mer information om variationsförfining och feedback finns i _[Förhandsgranska och innehållsförfining](#preview-and-refine-the-content)_.

   ![AI Assistant-förhandsgranskning av textvariation och förfiningsalternativ](./assets/email-designer-ai-assistant-text-refine.png){width="700" zoomable="yes"}

1. När du har det innehåll du vill ha klickar du på **[!UICONTROL Select]** för att ersätta texten med den valda varianten och återgå till e-postdesignområdet.

   Du kan använda redigerings- och formateringsverktygen på arbetsytan för att ändra texten, samt alternativen _[!UICONTROL Settings]_och_[!UICONTROL Style]_ till höger.

>[!TAB Endast bild]

Följ de här stegen för att använda AI Assistant för att förfina eller förbättra bildinnehållet för ett befintligt e-postmeddelande:

1. I e-postdesignområdet väljer du en _bild_ -komponent som ska ha det specifika innehållet som mål.

1. Markera ikonen _AI Assistant_ ( ![AI Assistant-menyn ](../../assets/do-not-localize/icon-gen-ai-content.svg){width="25"} ) på den yttre listen på den högra panelen.

   Inställningarna för AI-assistenten till höger återspeglar bildkomponentens genereringsinställningar.

1. Välj din **[!UICONTROL Brand]** för att se till att det AI-genererade innehållet överensstämmer med dina varumärkesspecifikationer.

   Om det inte finns några publicerade varumärken klickar du på **[!UICONTROL Create a brand]** för att [definiera riktlinjerna för ditt återanvändbara varumärke](./brands-overview.md).

1. Ange en beskrivning av vad du vill ha i fältet **[!UICONTROL Prompt]**.

   ![AI Assistant - ange en fråga för bildkomponenten](./assets/email-designer-ai-assistant-image.png){width="600" zoomable="yes"}

   Använd [promptbiblioteket](#prompt-library) om du behöver hjälp med att skapa en effektiv fråga.

1. Slutför inställningarna för innehållsanvisningar för att anpassa det genererade innehållet:

   * [**[!UICONTROL Image settings]**](#image-settings) - Om du vill inkludera bilder i det genererade innehållet aktiverar du bildgenerering och använder inställningarna för vägledning.

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

1. Markera bilden som du vill använda och klicka på **[!UICONTROL Select]** för att ersätta bilden eller platshållaren med det markerade objektet och återgå till designområdet för e-postmeddelanden.

   Du kan använda redigerings- och formateringsverktygen på arbetsytan för att ändra bilden samt alternativen _[!UICONTROL Settings]_och_[!UICONTROL Style]_ till höger.

>[!ENDTABS]

## Förhandsgranska och förfina innehållet {#refine-finalize}

När du har genererat innehållsvariationer kan du finjustera resultatet för att säkerställa att det uppfyller dina exakta krav. Granska varumärkesjusteringen, justera ton och språk och förbered innehållet för ett granskningsbart utkast. Du kan även skicka in feedback för en variation som hjälper dig att utbilda AI Assistant och förbättra framtida resultat.

### Öppna helskärmsvyn

1. Bläddra bland **[!UICONTROL Variations]** efter den första genereringen av innehåll.

1. Identifiera den variation som är den bästa matchningen för dina mål och klicka på ikonen _Helskärm_ ( ![Helskärmsikon](../assets/do-not-localize/icon-full-screen.svg) ) för att visa den valda variationen mer ingående.

   ![Öppna förhandsvisningsdialogrutan](./assets/gen-ai-preview-text-refine.png){width="700" zoomable="yes"}

1. När du är nöjd med den valda variationen klickar du på **[!UICONTROL Select]** för att använda den på arbetsytan.

### Förfina en variation

Klicka på alternativet **[!UICONTROL Refine]** för att få tillgång till ytterligare anpassningsfunktioner för e-post och textvarianter:

* **[!UICONTROL Elaborate]** - AI Assistant kan hjälpa dig att expandera specifika ämnen och ge dig ytterligare information för bättre förståelse och engagemang.

* **[!UICONTROL Summarize]** - Lång information kan överlagra sidvisningsprogram. Använd AI Assistant för att komprimera viktiga punkter till tydliga, kortfattade sammanfattningar som får dem att lyssna och uppmuntrar dem att läsa vidare.

* **[!UICONTROL Rephrase]** - Skriv om meddelandet med bibehållen betydelse. Med det här alternativet kan du generera alternativa ordalydelser, förbättra flödet eller justera fraser utan att ändra huvudbudskapet.

* **[!UICONTROL Use simpler language]** - Förenkla språket och säkerställ tydlighet och tillgänglighet för en större publik.

* **[!UICONTROL Translate]** - Översätt texten till ett annat språk. (Engelska är för närvarande det enda språk som stöds. Andra språk planeras för framtida versioner.)

* **[!UICONTROL Change tone]** - Justera tonen i meddelandet så att det passar din kommunikationsstil, till exempel för att göra det mer användarvänligt, professionellt, brådskande eller inspirerande.

* **[!UICONTROL Change Communication strategy]** - Ändra meddelandetillvägagångssättet baserat på dina mål, till exempel skapa en tränglighet eller framhäva en spännande tilltalande upplevelse.

<!-- is this option coming back? * **[!UICONTROL Use as reference content]** - Select this option to use the variant as the reference content for generating other results. -->

![Förfina meny med alternativ för innehållsförfining](./assets/gen-ai-preview-text-refine.png){width="700" zoomable="yes"}

### Skicka feedback

Ge feedback för de genererade varianterna genom att klicka på ikonen _Tummen uppåt_, _Tummen nedåt_ eller _Flagga_ och välj den orsak som bäst sammanfattar dina synpunkter.

![AI Assistant - förhandsgranska de genererade variationerna](./assets/gen-ai-preview-feedback-thumbs-up.png){width="700" zoomable="yes"}

### Kontrollera varumärkets justering (Beta)

<!-- Are we surfacing scoring here in the future, or will it be a separate post-creation task? 1. Click the percentage icon to view your **[!UICONTROL Brand Alignment Score]** and identify any misalignments with your brand. -->

Tack vare utvärderingen och poängsättningen av varumärkesanpassningen kan ni säkerställa enhetlighet i fråga om ton, meddelanden och visuell identitet i alla era e-postkampanjer, samtidigt som ni kan tjäna som en kvalitetskontroll innan ert innehåll publiceras. När e-postinnehållet är klart klickar du på ikonen _Varumärkesjustering_ ( ![Varumärkesjustering](../assets/do-not-localize/icon-brand-compliance.svg) ) till höger för att öppna den högra panelen för _Varumärkesjustering_ i e-postdesignområdet.

![Få åtkomst till varumärkesjusteringsverktygen](./assets/brands-alignment-sidebar.png){width="600" zoomable="yes"}

Mer information finns i [Validera din varumärkesjustering](./brand-alignment.md#validate-your-brand-alignment)
