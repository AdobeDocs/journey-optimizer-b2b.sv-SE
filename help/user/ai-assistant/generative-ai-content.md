---
title: Generativ AI för innehåll
description: Lär dig att skapa personaliserade e-postmeddelanden och landningssidor med generativ AI i  [!DNL Journey Optimizer B2B Edition], inklusive tips och tips.
feature: AI Assistant, Generative AI, Content
level: Beginner
topic: Artificial Intelligence
role: User
exl-id: 36baf7f9-2fff-4c33-bca0-7d43ec48e74a
source-git-commit: ce4df9a2726cf842c088738521b3e5dd88dd768f
workflow-type: tm+mt
source-wordcount: '2482'
ht-degree: 0%

---

# Generativ AI för innehåll {#generative-ai-content}

>[!CONTEXTUALHELP]
>id="ajo_b2b_ai-generation-settings"
>title="Generering av AI-innehåll"
>abstract="När du har skapat layouten kan du använda de generativa AI-verktygen i [!DNL Journey Optimizer B2B Edition] för att förbättra innehållet. Den här funktionen förenklar processen för personalisering och innehållsförbättring genom att finjustera innehållet enligt din beskrivande uppmaning."

>[!CONTEXTUALHELP]
>id="ajo_b2b_ai-generation-reference-context"
>title="Referensinnehåll"
>abstract="Använd _Referensinnehåll_ för att överföra en resursfil som innehåller innehåll som ger ytterligare kontext för generativ AI i [!DNL Journey Optimizer B2B Edition], eller för att välja en tidigare överförd fil. Med det här alternativet kan du säkerställa att allt nödvändigt material finns tillgängligt för att förbättra kvaliteten och relevansen för genererat innehåll."

>[!CONTEXTUALHELP]
>id="ajo_b2b_ai-generation-start"
>title="Adobe generativa AI-termer"
>abstract="Du måste godkänna Adobe Experience Cloud Generative AI User Guidelines. Granska alla utdata från den här funktionen och se till att de passar dina behov."
>additional-url="https://www.adobe.com/legal/licenses-terms/adobe-dx-gen-ai-user-guidelines.html" text="Adobe Generative AI User Guidelines"

Generativ AI för innehåll i [!DNL Adobe Journey Optimizer B2B Edition], som drivs av Microsoft Azure OpenAI och Adobe Firefly, ger förebyggande förslag på innehållsvarianter för text och bilder. Optimera innehållet genom att experimentera med olika förtexter och bilder.

Använd de generativa AI-funktionerna för att skapa innehåll i [!DNL Journey Optimizer B2B Edition] för att utnyttja Adobe generativa AI-funktioner. Skapa personlig text och bilder för e-post, SMS-meddelanden, landningssidor med mera. När ni bygger en hel kampanj eller bara finjusterar specifika resurser hjälper dessa funktioner er att anpassa innehållet sömlöst efter varumärkesriktlinjerna samtidigt som ni sparar värdefull tid.

<!--
Generate multiple variants and build an experiment to compare them. Leveraging Journey Optimizer Content Experiment, you can define multiple message treatments to measure which one performs best for your target audience. You can choose to vary the delivery content, or subject. The message audience is randomly allocated to each treatment to determine which one works best in terms of the specified metric. Learn more about Content Experiment in this section. -->

>[!IMPORTANT]
>
>Om du vill få åtkomst till de här funktionerna i [!DNL Journey Optimizer B2B Edition] måste du ha behörigheten _[!UICONTROL AI Assistant]_>_[!UICONTROL Generate Content]_. Mer information om hur en produktadministratör kan bevilja funktionsbehörigheter finns i [Redigera roller för produktbehörigheter](../admin/user-management.md#edit-roles-for-product-permissions).

AI Assistant-verktyg för innehållsgenerering stöds med följande resurstyper:

* [E-post](../content/ai-assistant-emails.md)
* [!BADGE Beta] [Landningssidor](../content/ai-assistant-landing-pages.md)

## Allmänna riktlinjer och begränsningar {#general-guidelines-and-limitations}

Användningen av generativa AI-funktioner regleras av [Adobe Experience Cloud Generative AI User Guidelines](https://www.adobe.com/legal/licenses-terms/adobe-dx-gen-ai-user-guidelines.html){target="_blank"}. Med Adobe engagemang för genomskinlighet i användningen av generativa AI-verktyg för att skapa media, tillämpar Adobe [innehållsuppgifter](https://helpx.adobe.com/firefly/web/get-started/learn-the-basics/content-credentials-overview.html){target="_blank"} för allt innehåll eller projekt som innehåller en [!DNL Firefly]-genererad resurs när den hämtas eller exporteras.

Läs de här allmänna riktlinjerna för hur du använder generativ AI för innehåll i [!DNL Journey Optimizer B2B Edition]:

* Använd väldefinierade instruktioner för den generativa AI-modellen för att tolka med precision. Marknadsföringsmålet eller uppmaningen du anger påverkar i hög grad kvaliteten på det genererade innehållet.

* Ladda upp innehållsreferensfiler för korrekt varumärkesanpassat innehåll. Annars baseras innehållet på offentligt tillgänglig information. Det överförda innehållet kan ha följande filformat: PDF, JPEG, PNG eller ZIP (som innehåller filformat som stöds). Den maximala storleken för en överförd fil är 50 MB. Större filer eller ett stort antal bilder kan fungera, men detta ökar bearbetningstiden.

* Använd en varumärkesspecifik eller anpassad mall för att skapa e-postinnehåll. E-postmallar med upp till 8-10 bilder rekommenderas.

* Var noga med att rapportera eventuella problematiska utdata med ikonerna för tummen upp, reglaget ned eller flagga när du väljer varianter.

## Uppmana bästa praxis för generativ AI {#generative-ai-prompting-guide}

>[!CONTEXTUALHELP]
>id="ajo_b2b_ai_content_prompt"
>title="Visa vägledning"
>abstract="Utforska [!DNL Journey Optimizer B2B Edition]-dokumentationen och lär dig hur du skapar effektiva uppmaningar som producerar konverteringsfullt marknadsföringsmaterial."

Den här guiden hjälper er att strukturera era förfrågningar, förmedla avsikter på ett tydligt sätt och se till att AI skapar meddelanden som anpassar sig till varumärkesriktlinjerna, målgruppsbehoven och kampanjmålen.

Lär dig hur du skriver effektiva uppmaningar som gör det möjligt för AI Assistant att generera högkvalitativt marknadsföringsmaterial som är skräddarsytt efter era mål.

### Använda CO-STAR-ramverket {#costar-framework}

För bästa resultat med genererat innehåll kan du ordna dina frågor med hjälp av CO-STAR-ramverket. Denna strukturerade metod ger tydlighet för exakt det du behöver.

| Komponent | Vad det betyder | Varför det spelar någon roll |
| --- | ---- | ------ |
| **C - kontext** | Bakgrund om kampanjen, produkten eller situationen | Förstå helheten |
| **O - Mål** | Ditt specifika marknadsföringsmål | Skapar det som innehållet ska uppnå |
| **S - Format** | Hur du vill kommunicera | Anger metod |
| **T - Ton** | Rörelsekänsla | Formar hur ditt meddelande känns |
| **A - Målgrupp** | Målgruppen ni riktar er mot | Ser till att meddelandet får gensvar hos rätt personer |
| **R - Krav** | Specifika begränsningar eller måste-ha | Definierar gränser och viktiga element |

{style="table-layout:fixed"}

### Viktiga frågor {#key-takeaways}

<table style="table-layout: fixed; width: 100%; border: 0;">
<thead style="border: 0; background-color: #FFFFFF;">
<tr>
<th>Gör</th>
<th>Gör det inte</th>
</tr>
</thead>
<tbody>
<tr style="border: 0;">
<td>
<ul><li>Använd CO-STAR-ramverket för strukturen
<li>Var tydlig med aktuellt och befintligt innehåll
<li>Fokusera på dokumentanvändning med specifik extraheringsvägledning
<li>Gör val för ton, strategi och språkområde
<li>Matcha marknadsföringsmål med innehållstypfunktioner
<li>Generera flera varianter för A/B-testning</ul>
</td>
<td>
<ul><li>Fråga efter strukturändringar, format eller bildredigering i uppmaningar
<li>Ange ton/strategi i uppmaningar, om sådana finns i alternativen
<li>Använd otydliga mål som _marknadsför produkten_
<li>Begär val av villkorliga element
<li>Förvänta dig layoutändringar via uppmaningar</ul>
</td>
</tr>
</tbody>
</table>

### Innehåll som inte stöds i uppmaningar

>[!TIP]
>
>Använd designverktygen eller [!DNL Adobe Express] för visuella ändringar/bildändringar.

Följande förfrågningar stöds **_inte_** och bör hanteras med andra verktyg:

<table style="table-layout: fixed; border: 0;">
<thead style="border: 0; background-color: #FFFFFF">
<tr>
<th><img src="../../assets/do-not-localize/check-box-red.svg" alt="Rött kors">  Ändringar i e-poststrukturen</th>
<th><img src="../../assets/do-not-localize/check-box-red.svg" alt="Rött kors">  Visuella formatändringar</th>
<th><img src="../../assets/do-not-localize/check-box-red.svg" alt="Rött kors">  Bildredigeringsåtgärder</th>
</tr>
</thead>
<tbody>
<tr style="border: 0;">
<td>
<ul>
<li>Markera specifika avsnitt som ska ändras</li>
<li>Ta bort eller klona element</li>
<li>Villkorliga markeringar</li>
<li>Lägga till eller ta bort layoutavsnitt</li>
</ul>
</td>
<td>
<ul>
<li>Textformatering (fet, kursiv, teckensnittsstorlek)</li>
<li>Färgändringar</li>
<li>Layoutstil (kanter, utfyllnad, marginaler)</li>
<li>Visuella effekter (skuggor)</li>
</ul>
</td>
<td>
<ul>
<li>Ändringar i bakgrunden</li>
<li>Lägga till textövertäckningar eller logotyper</li>
<li>Bildbeskärning eller storleksändring</li>
<li>Färgjusteringar</li>
<li>Bildersättning</li>
</ul>
</td>
</tr>
</tbody>
</table>

### Kvalitetskontrolllista {#quality-checklist}

Innan du genererar innehåll bör du kontrollera följande:

![Grön bockmarkering](../../assets/do-not-localize/check-box-green.svg){width="20"} **Rensa mål**: Anger tydligt åtgärden, produkten/tjänsten, värdet och sammanhanget.

![Grön bockmarkering](../../assets/do-not-localize/check-box-green.svg){width="20"} **Definierad målpublik**: Anger demografi, roll eller segment.

![Grön bockmarkering](../../assets/do-not-localize/check-box-green.svg){width="20"} **Justering av innehållstyp**: Målet matchar den valda kanalen eller det valda formatet.

![Grön bockmarkering](../../assets/do-not-localize/check-box-green.svg){width="20"} **Granska markeringar**: Ton, strategi och språkområde har valts, ta inte med dem i uppmaningen.

![Grön bockmarkering](../../assets/do-not-localize/check-box-green.svg){width="20"} **Dokumentfokus anges**: Markerar vilket innehåll eller vilka avsnitt som ska refereras.

![Grön bockmarkering](../../assets/do-not-localize/check-box-green.svg){width="20"} **Varumärke används**: Lämpliga varumärkesriktlinjer har valts.

![Grön bockmarkering](../../assets/do-not-localize/check-box-green.svg){width="20"} **Realistiskt omfång**: Undvik begäranden om layoutändringar, formatering eller strukturändringar.

### Effektiva marknadsföringsmål {#marketing-objectives}

När ni utformar marknadsföringsmålen ska ni se till att de är tydliga, användbara och mätbara. Undvik vaga eller generiska programsatser.

**Exempel på bra mål:**

![Grön bockmarkering](../../assets/do-not-localize/check-box-green.svg){width="20"}&quot;Kör registreringar för den kostnadsfria 30-dagars testversionen av den nya AI-baserade analysinstrumentpanelen&quot;

![Grön bockmarkering](../../assets/do-not-localize/check-box-green.svg){width="20"}&quot;Generera leads för B2B-webbinariet om att minska molnkostnaderna med 40 %&quot; inträffar den 15 mars&quot;

![Grön bockmarkering](../../assets/do-not-localize/check-box-green.svg){width="20"}&quot;Befordra den begränsade 25-procentiga rabatten på premiumprenumerationer, som upphör 25 december&quot;

**Exempel som ska undvikas:**

![Röd genomstrykning](../../assets/do-not-localize/check-box-red.svg){width="20"} &quot;Befordra produkten&quot; (för vagt)

![Rödstrykning](../../assets/do-not-localize/check-box-red.svg){width="20"}&quot;Få människor att skriva under avtal&quot; (otydligt värde)

![Rödtext](../../assets/do-not-localize/check-box-red.svg){width="20"}&quot;E-post om nya funktioner&quot; (utan syfte)

#### Strukturera ditt mål

Ange alltid sammanhang och värdeförslag för att skapa relevant innehåll. Använd följande formel för att hjälpa dig att skriva effektiva mål: **Åtgärd + produkt/tjänst + värde/förmån + brådskande/kontext**

**Exempel på bra mål:**

![Grön bockmarkering](../../assets/do-not-localize/check-box-green.svg){width="20"}&quot;Uppmuntra nedladdningar av den nya mobilappen som hjälper användarna att spåra hållbara levnadsvanor med personaliserade, miljövänliga rekommendationer&quot;

![Grön bockmarkering](../../assets/do-not-localize/check-box-green.svg){width="20"}&quot;Befordra registrering för exklusiv workshop om avancerade datavisualiseringstekniker för marknadsförare&quot;

![Grön bockmarkering](../../assets/do-not-localize/check-box-green.svg){width="20"}&quot;Öka närvaron vid produktstartstillfället med den revolutionerande AI-skrivassistenten som sparar mer än fem timmar per vecka&quot;

**Exempel som ska undvikas:**

![Röd genomstrykning](../../assets/do-not-localize/check-box-red.svg){width="20"} &quot;Announce new app&quot; (värdeförslag och kontext saknas)

![Rödstrykning](../../assets/do-not-localize/check-box-red.svg){width="20"}&quot;Be personer registrera sig för workshop&quot; (ingen information om målgrupp och förmån)

![Röd genomstrykning](../../assets/do-not-localize/check-box-red.svg){width="20"} &quot;Promote event&quot; (ingen tydlig åtgärd, värde eller trängning)

#### Exempeluppmaningar efter kanaltyp {#channel-type-practices}

<table style="table-layout: auto; border: 0;">
<thead>
<tr style="border: 0;background-color: #FFFFFF;">
<th>Kanal</th>
<th>Exempel</th>
</tr>
</thead>
<tbody>
<tr>
<td><strong>E-post</strong></td>
<td>"Ge företagen en skjuts framåt genom att presentera tre framgångsberättelser med detaljerade avkastningsmått (Oracle: 45 % kostnadsminskning, Accenture: 200 % ökning, Microsoft: 60 % tidsbesparing). Rikta er till IT-chefer på företag med över 1 000 anställda"</td>
</tr>
<tr>
<td><strong>Landningssidor</strong></td>
<td>"Konvertera B2B-besökare till kvalificerade leads genom att visa hur företagets säkerhetslösning förhindrar 99,9 % av cyberattackerna, med Fortune 500-utlåtanden och kostnadsfri säkerhetsrevision"</td>
</tr>
</tbody>
</table>

<!-- channels not yet supported
<tr>
<td><strong>SMS</strong></td>
<td>"Alert VIP customers about a 4-hour flash sale on premium electronics with 40% discount, limited to the first 100 customers"</td>
</tr>
<tr>
<td><strong>Push Notifications</strong></td>
<td>"Re-engage users who haven't opened the app in 7 days with personalized content recommendations based on their reading history"</td>
</tr> -->

<!-- Wait on more B2B specific examples

### Industry-specific approaches {#industry-approaches}

<table style="table-layout: fixed; border-collapse: collapse; border: 0;">
<thead>
<tr style="border: 0;background-color: #FFFFFF;">
<th>Industry</th>
<th>Example Prompt</th>
</tr>
</thead>
<tbody>
<tr>
<td><strong>B2B Technology</strong></td>
<td>"Demonstrate ROI and technical specifications while addressing security concerns for IT decision-makers evaluating our cloud infrastructure solution, emphasizing 99.9% uptime SLA, SOC 2 compliance, and 40% cost savings."</td>
</tr>
<tr>
<td><strong>E-commerce Retail</strong></td>
<td>"Create urgency around limited-stock holiday items while highlighting free shipping and easy returns for last-minute shoppers, emphasizing limited quantities (less than 50 remaining) and 24-hour shipping cutoff."</td>
</tr>
<tr>
<td><strong>Financial Services</strong></td>
<td>"Educate clients about investment portfolio diversification strategies while maintaining regulatory compliance, featuring certified financial advisor insights and risk disclaimers."</td>
</tr>
<tr>
<td><strong>Healthcare & Wellness</strong></td>
<td>"Promote preventive care benefits and annual health screenings while maintaining medical accuracy, featuring board-certified physician recommendations and patient privacy assurances."</td>
</tr>
<tr>
<td><strong>Education & Training</strong></td>
<td>"Emphasize career advancement outcomes and industry certifications while showcasing instructor expertise, highlighting 92% job placement rate and project-based curriculum."</td>
</tr>
<tr>
<td><strong>SaaS Platforms</strong></td>
<td>"Highlight time savings and automation benefits with specific metrics while addressing integration concerns, featuring average 25-hour weekly time savings and integration with 200+ popular tools."</td>
</tr>
</tbody>
</table>
 -->

### Nytt innehåll kontra ändring av befintligt innehåll {#new-vs-modify}

Ange tydligt om din begäran inbegriper generering av nytt innehåll eller uppdatering av befintligt material. Skillnaden är viktig eftersom den vägleder AI vid valet av lämplig metod och ger ett mer exakt och användbart resultat.

#### Skapa nytt innehåll

Använd den här strategin när ni lanserar marknadsföringskampanjer, presenterar nya lösningar eller initierar uppdaterad/uppdaterad kommunikation. Det ser till att ert budskap börjar starkt och anpassar sig efter era mål.

**Fråga** ➤ När du skapar nytt innehåll ska du fokusera på ditt marknadsföringsmål utan att referera till befintligt innehåll.

>[!BEGINSHADEBOX &quot;Exempel&quot;]

* **Testversion av SaaS**:&quot;Starta den nya CRM-programvaran för småföretagare, markera 50 % tidsbesparingar, 90 % snabbare leads och erbjuda en 30-dagars kostnadsfri testversion med personlig introduktion&quot;
* **Funktionsmeddelande**:&quot;Nya API-integreringsfunktioner som minskar utvecklingstiden med 60 % för företagskunder, med inriktning på tekniska beslutsfattare&quot;
* **Evenemangskampanj**:&quot;Kör registreringar för webbinariet om Digital Marketing Trends 2024&quot; med experter från Google, Meta och Adobe, och understryka åtgärdbara insikter och begränsade licenser (max 500)&quot;

>[!ENDSHADEBOX]

#### Ändra befintligt innehåll

>[!TIP]
>
>Om du vill använda standardändringar som att bearbeta, sammanfatta eller förenkla väljer du **_Förfina_** i stället för att skriva anpassade uppmaningar.

Använd en ändringsprompt när ni behöver uppdatera, uppdatera eller anpassa era aktuella marknadsföringskampanjer. Den här metoden har stöd för stegvisa förbättringar som säkerställer att ditt meddelande förblir relevant utan att börja om från början.

**Fråga** ➤ Ange tydligt vad du vill ändra och hur det ska ändras när du ändrar befintligt innehåll.

>[!BEGINSHADEBOX &quot;Exempel&quot;]

* **Kampanjuppdatering**:&quot;Ändra e-postmeddelandet om programstart så att det fokuserar på företagssäkerhetsfunktioner i stället för allmänna produktivitetsfördelar, så att IT-beslutsfattare med efterlevnadscertifieringar kan målinriktas&quot;
* **Målgruppsindelning**:&quot;Anpassa programvarudemonstrationen till att rikta in sjukvården specifikt och ersätt generiska exempel med vårdanvändningsfall och HIPAA-efterlevnadsfördelar&quot;
* **Säsongsuppdatering**:&quot;Uppdatera kampanjkampanjen för tredje kvartalet för semesterförsäljning, ändra fokus från skolstart till semester och ge en gåva med snabb betoning på frakt&quot;

>[!ENDSHADEBOX]

## Avancerade textinställningar {#text-settings}

Förutom att använda en tydlig och välformad prompt innehåller textinställningarna i AI Assistant-innehållsverktygen textinställningar som du kan använda för att optimera de genererade utdatafilerna.

>[!TIP]
>
>Använd alternativen _[!UICONTROL Communication strategy]_&#x200B;och&#x200B;_[!UICONTROL Tone]_ i _[!UICONTROL Text settings]_&#x200B;i stället för att ange dessa egenskaper i uppmaningen.

### Typ av kommunikationsstrategi

Er kommunikationsstrategi avgör hur ni förmedlar ert budskap för att maximera effekten. Olika strategier fungerar bättre för olika mål, oavsett om du skapar trängsel, skapar förtroende eller driver omedelbara åtgärder. Välj den strategi som bäst passar era kampanjmål och målgruppsinsikter.

| **Strategi** | **Bäst för** | **Meddelandestil** | **Exempel** |
| ------------ | ------------ | ------------------- | ------------ |
| **Brådskande** | Tidskänsliga erbjudanden, leveranstider, omedelbar åtgärd | Skapar ett omedelbart tryck med ett tidsbaserat språk | <li>&quot;Slå till nu: Erbjudandet gäller till midnatt&quot; <li>&quot;Anmäl dig idag innan fläckarna fylls i&quot; <li>&quot;48-timmars blixtförsäljning börjar nu&quot; |
| **FOMO (rädsla för att saknas)** | Begränsade erbjudanden, evenemang, exklusiv åtkomst | Använder tidsåtgång, knapphet och ledtrådar | <li>&quot;Bara 24 timmar kvar! Begränsat lager med 40 % rabatt&quot; <li>&quot;Sista chansen: Priserna för tidiga fåglar upphör imorgon&quot; <li>&quot;Endast 100 betapunkter återstår&quot; |
| **Socialt korrektur** | Pålitlighetsuppbyggnad, utlåtanden, populära produkter | Utnyttjar andras upplevelser och validering | <li>&quot;Gå med i 50 000+ nöjda kunder&quot; <li>&quot;Betyg 4,9/5 stjärnor per branschen&quot; <li>&quot;Tillförlitligt av Fortune 500-företag&quot; |
| **Scharlakans** | Begränsat lager, exklusiva releaser, efterfrågade artiklar | Framhäver begränsad tillgänglighet och exklusivitet | <li>&quot;Endast 5 kvar i lager&quot; <li>&quot;Limited edition: 100 units available&quot; <li>&quot;Exklusiv release: Först till kvarn får först mala&quot; |
| **Incentive** | Erbjudanden, belöningsprogram, specialerbjudanden | Visar påtagliga fördelar och belöningar | <li>&quot;Få 20 % rabatt på din första beställning&quot; <li>&quot;Vinn dubbla poäng i helgen&quot; <li>&quot;Fraktfritt vid beställningar över 50 dollar&quot; |
| **Exklusivitet** | Premiumprodukter, VIP-upplevelser, erbjudanden som endast är för medlemmar | Använder premiumpositionering och specialåtkomstspråk | <li>&quot;Exklusiv inbjudan till en privat förhandsgranskning&quot; <li>&quot;Elitmedlemskapet ger avancerad analys upp&quot; <li>&quot;Gå med i utvalda Fortune 500-företag som redan använder oss&quot; |
| **Gamification** | Engagerande kampanjer, lojalitetsprogram, interaktivt innehåll | Använder spelmekanik och målgruppsspråk | <li>&quot;Lås upp nästa belöningsnivå&quot; <li>&quot;En hel del utmaningar att vinna märken&quot; <li>&quot;Klättra upp resultatlistan för exklusiva priser&quot; |
| **Informativ** | Utbildning, forskning, komplexa produkter, tankeledarskap | Fakta, data, insikter och förklaringar används | <li>&quot;5 insikter från analys av över 10 000 interaktioner&quot; <li>&quot;Ny forskning avslöjar tre banbrytande metoder&quot; <li>&quot;En komplett guide för implementering av AI i marknadsföringen&quot; |
| **Utbildning och insikter** | Utbildningsinnehåll, branschtrender, bästa praxis | Ger värdefull kunskap och användbara arbetsmetoder | <li>&quot;Lär dig avancerad teknik med en expertguide&quot; <li>&quot;Upptäck sju strategier som marknadsförarna använder mest&quot; <li>&quot;Lär dig optimera arbetsflödet i fem steg&quot; |

### Ange rätt ton {#tone}

Tone formar hur publiken upplever och svarar på ert budskap. Välj alltid en ton som är anpassad efter ert varumärkestrotal och det stadium som profilresan tar.

Granska de tillgängliga färgtonsalternativen, bland annat när varje alternativ fungerar bäst och exempel på innehåll som passar varje format.

| Tonalitet | Bäst för | Exempel på innehåll |
| ---- | ----- | ----- |
| Professional | B2B-kommunikation, formella meddelanden | &quot;Vi har nöjet att meddela vårt strategiska partnerskap ...&quot; |
| Empatetisk | Kundsupport, känsliga ämnen | &quot;Vi förstår hur frustrerande det här problemet måste vara för dig..&quot; |
| Humoristisk | Engagerande kampanjer, lättanvänt innehåll | &quot;Varning: Kan orsaka stora produktivitetsvinster!&quot; |
| Spännande | Produktlanseringar, eventkampanjer | &quot;Det här är ögonblicket du har väntat på!&quot; |
| Inspirerande | Motivationskampanjer, varumärkessyfte | &quot;Tillsammans kan vi göra skillnad i världen..&quot; |
| Engagerande | Försäljningskampanjer, konverteringar | &quot;Missa inte denna tidsbegränsade möjlighet att ...&quot; |
| Egen | Kundengagemang, välkomstmeddelanden | &quot;Jag är glad att du är här med oss!&quot; |
| Formell | Juridiska meddelanden, officiella meddelanden | &quot;Detta är ett meddelande om följande ändringar..&quot; |
| Apologetisk | Återställning av tjänster, problemlösning | &quot;Bodea ber uppriktigt om ursäkt för eventuella olägenheter...&quot; |
| Assertiv | Ledarinnehåll, auktoritativa meddelanden | &quot;Det här måste du göra nu..&quot; |
| saga | Varumärkesberättelser, känslomässiga kopplingar | &quot;Allt började med en enkel fråga..&quot; |
| Konversationslayout | Strukturkampanjer, relationsskapande | &quot;Låt oss prata om hur det här programmet kan hjälpa dig ...&quot; |

## Optimerat referensinnehåll {#reference-content}

>[!TIP]
>
>Om du redan har överfört en resurs via menyn **[!UICONTROL Reference content]** behöver du inte referera till den i uppmaningen. Alla valda dokument används automatiskt.

Referensinnehållsfiler ger faktainformation som berikar det genererade innehållet med specifika, korrekta detaljer. När du överför dokument, t.ex. produktbroschyrer eller tekniska rapporter, ändrar du uppmaningen så att den omfattar vilka delar som har fokus:

* **I stället för** _&quot;Använd produktbroschyren&quot;_ **bör du använda** _&quot;Fokusera på de avancerade säkerhetsfunktionerna och kompatibilitetscertifieringarna, särskilt SOC 2-kompatibilitet och datakryptering&quot;_

* **I stället för** _&quot;Referera fallstudierna&quot;_ **ska du använda** _&quot;Resultat av räntabilitet från vårdklienter, närmare bestämt 40-procentig kostnadsminskning på Regional Medical Center&quot;_

* **I stället för** _&quot;Inkludera teknisk information&quot;_ **ska du använda** _&quot;Fokusera API-integreringsfunktioner och utvecklarfördelar, med fokus på REST API-slutpunkter och 99,9 % aktiv SLA&quot;_

### Innehållsförfining

När innehållet har genererats kan du använda funktionen **_[!UICONTROL Refine]_** för att iterera och förbättra det med följande alternativ:

* **[!UICONTROL Elaborate]** - AI Assistant kan hjälpa dig att expandera specifika ämnen och ge dig ytterligare information för bättre förståelse och engagemang.

* **[!UICONTROL Summarize]** - Lång information kan överlagra sidvisningsprogram. Använd AI Assistant för att komprimera viktiga punkter till tydliga, kortfattade sammanfattningar som får dem att lyssna och uppmuntrar dem att läsa vidare.

* **[!UICONTROL Rephrase]** - Skriv om meddelandet med bibehållen betydelse. Med det här alternativet kan du generera alternativa ordalydelser, förbättra flödet eller justera fraser utan att ändra huvudbudskapet.

* **[!UICONTROL Use simpler language]** - Förenkla språket och säkerställ tydlighet och tillgänglighet för en större publik.

* **[!UICONTROL Translate]** - Översätt texten till ett annat språk. (Engelska är för närvarande det enda språk som stöds.)

* **[!UICONTROL Change tone]** - Justera tonen i meddelandet så att det passar din kommunikationsstil, till exempel för att göra det mer användarvänligt, professionellt, brådskande eller inspirerande.

* **[!UICONTROL Change Communication strategy]** - Ändra meddelandetillvägagångssättet baserat på dina mål, till exempel skapa en tränglighet eller framhäva en spännande tilltalande upplevelse.
