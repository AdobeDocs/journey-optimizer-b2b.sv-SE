---
title: Audience Agent för B2B
description: Audience Agent B2B in Journey OptimizerB2B Edition använder intentanalys och personmappning för att skapa inköpsgrupper och snabba upp arbetsflödena för B2B-marknadsföring.
feature: Audiences, AI Assistant
role: User
source-git-commit: fa53458db4576af037dcf4b16ab1bf7b103b2fdd
workflow-type: tm+mt
source-wordcount: '3066'
ht-degree: 0%

---

# Audience Agent för B2B

Audience Agent B2B är tillgänglig i Journey Optimizer B2B edition med [Adobe Experience Platform Agent Orchestrator](https://experienceleague.adobe.com/sv/docs/experience-cloud-ai/experience-cloud-ai/agents/agent-orchestrator). Med denna agent blir det effektivare och effektivare att utforska och skala målgrupper, vilket snabbar upp framtagningen av inköpsgrupper och smidiga arbetsflöden för aktivering av kundresan:

* **_Prioritera målgrupper utifrån avsikt_**: Använd personprofiler baserat på produktavsikt för olika målgrupper och effektivisera kampanjplaneringen, minska tiden som läggs på målgruppsvalidering.

* **_Använd AI för att identifiera inköpsgrupper_**: Använd AI, strukturerade, ostrukturerade data och enhetliga förstahandsdata för att effektivisera identifiering och skapande av inköpsgrupper.

![Audience Agent för B2B i helsidesläge](./assets/audience-agent-full.png){width="700" zoomable="yes"}

>[!PREREQUISITES]
>
>För att kunna använda Audience Agent för B2B finns det obligatoriska datadefinitioner och mappningar:<br/>
>
>* [Återkommande datataxonomi/mappning](../admin/intent-data.md)
>* [XDM-fältets taxonomi/mappning](#xdm-data-prerequisites)

## Audience Agent för B2B-funktioner

| Område | Vad det gör | Affärsvärde |
| ---- | ------------ | -------------- |
| Intresseanalys | <li> Mät kontonametodens styrka (till exempel låg, medel och hög) för specifika produkter. <li>Jämför produktintressetrender över tid (t.ex. de viktigaste produkterna under de senaste _n_ dagarna). <li>Identifiera konton som aktivt visar intresse för specifika produkter. <li>Surface Engagement patterns som kombinerar kontoaktivitet med personlig täckning. | <li>Hjälper team att fokusera på rätt konton vid rätt tidpunkt. <li>Förbättrar kvaliteten på pipeline genom att prioritera konton med äkta inköpssignaler. <li>Möjliggör proaktivt engagemang innan konkurrenterna agerar. |
| Personmappning | <li>Identifiera och rangordna de främsta personerna efter produktmetod. <li>Identifiera personer som deltar i köp av en eller flera produkter. <li>Koppla personligheter till funktionella roller (till exempel _Champion_, _Decision Maker_ och _Influencer_) med motivering. <li>Validera varför en viss person anses vara segrare. | <li>Ser till att säljteamet engagerar de verkliga beslutsfattarna och påverkarna. <li>Minskar slöseriet med kontakter som har liten effekt. <li>Ökar vinsterna genom att anpassa utåtkomsten till köpdynamiken. |
| Utvärdering av inköpsgrupp | <li>Utvärdera inköpsgruppens storlek (till exempel grupper med fler än _n_ medlemmar). <li>Mät personlig täckning mellan konton (till exempel under _x_%). <li>Spåra skillnader i rolldistribution och täckning inom inköpsgrupper. <li>Markera konton med kampanjer som identifierats i de senaste avtalen. | <li>Visar luckor i täckningen som kan stoppa avtal. <li>Förstärk flertrådsstrategier genom att säkerställa en fullständig representation. <li>Förbättrar spårningen av avtal genom interaktionsinsikter på gruppnivå. |

## Exempel på fråga

De här frågeexemplen visar några sätt att använda agenten:

* Visa trendfönstret: tidigast och senast uppdaterat för kontoproduktavsikt per produkt.
* För `<product>` anger du inköpsgrupper med produktavsikt och poäng.
* För `<product>` anger du personligheter och roller med deras affärsmöjlighetsstatistik (vinstfrekvens, medlemskapsnivå, antal).
* För konton i `<industry>`, vad är det genomsnittliga antalet kontoprofiler för `<product>`?
* Vilka konton har låg återgivning för någon produkt men har fortfarande öppna möjligheter (värd att vårda)?
* Vilka konton har lagt till nya intent-signaler för `<account_name>` den här veckan?

## Concepts

| Koncept | Förklaring |
| ------- | ----------- |
| Målgruppsidentifiering | Bakom kulisserna tittar agenten på förstahandssignaler utifrån två saker: hur engagerade människor är med ert varumärke och den typ av personer som de representerar. Analysen tar en titt tillbaka under de senaste 18 månaderna av aktiviteten för att identifiera produktavsikt för alla på kontot, särskilt under tiden som en stängning av affärsmöjligheten sker. Denna analys hjälper agenten att lyfta fram de personer som mest sannolikt kommer att påverka avtalet.<br/><br/>Ibland har konton inte alla sina affärsmöjlighetsdata i perfekt form, vilket är bra och agenten kan fortfarande identifiera produktåtergivning enbart utifrån interaktionsmönster. |
| Persona | Personerna representerar de typer av personer som är engagerade i ett konto. Agenten bygger den genom att titta på befattning, funktion och tjänsteålder och sedan normalisera informationen så att den är konsekvent mellan olika konton. I stället för att gå vilse i röriga titlar kan du snabbt se om du når beslutsfattare, påverkare eller supportroller. Personas hjälper er att förstå vem som visar intresse, inte bara hur mycket intresse det finns. <br/><br/> När agenten mappar profiler till att köpa grupproller, väljs den typ av identifierad person som baseras på deras jobbtitel, funktion, tjänsteålder och andra attribut som du väljer att lägga till, och de anpassas till de roller som de troligen kommer att spela i ett inköpsbeslut, till exempel _beslutsfattare_, _påverkare_ eller _mästare_. Dessa roller är relevanta för den aktuella produkten, så att du kan se vilka som är viktigast för den möjligheten. Agenten visar också täckning för varje roll, vilket hjälper er att snabbt förstå vilka roller som är väl representerade och var det kan finnas luckor i er engagemangsstrategi. |
| Mappa inköpsgruppsroller | När personerna har mappats till roller samlar du dem i en inköpsgrupp. Tänk på det som det fullständiga teamet i kontot som troligen kommer att påverka eller besluta om köpet. Varje roll (till exempel _beslutsfattare_, _påverkare_ eller _mästare_) lägger till en del av bilden så att du får en tydlig bild av hela kommittén som driver avtalet. <br/><br/> När du mappar profiler för att köpa grupproller, tar du typen av identifierad person utifrån deras jobbtitel, funktion, tjänsteålder och andra attribut som du väljer att lägga till och justerar dem efter den roll som de troligast spelar i ett inköpsbeslut, till exempel _beslutsfattare_, _påverkare_ eller _mästare_. Dessa roller är relevanta för den aktuella produkten, så att du kan se vilka som är viktigast för den möjligheten. Agenten visar täckningen för varje roll, vilket hjälper er att snabbt förstå vilka roller som är väl representerade och var det kan finnas luckor i er engagemangsstrategi. |
| Köpgrupper | Genom att köpa grupper kan marknadsförarna hantera den verkliga komplexiteten hos inköpskommittéer, inte isolerade leads eller konton. Adobe Journey Optimizer B2B edition har verktygen (AI-styrda insikter, rollbaserade resor och spårning av fullständighet) för att skapa struktur, personalisering och analytisk tydlighet i den processen, vilket i slutänden gör att marknadsföring och försäljning justeras närmare intäkterna.<br/><br/>Att skapa en inköpsgrupp handlar om att sammanföra tre viktiga saker: rätt målgrupp, produktkontext och inköpsgruppsroller. Här följer en stegvis förhandsvisning av hur det fungerar: <ol><li>**Identifiera din målgrupp** <ul><li>Först upptäcker agenten konton som är mest relevanta för din produkt. Den här upptäckten innehåller konton som redan visar ränta och konton med potential.<li>På dessa konton identifieras de personer (dina nyckelpersoner) som kan påverka eller vara en del av köpbeslutet.<li>Den väljer från konton till yta: en kontolista eller en kontopublik.</ul><li>**Överväg produktsammanhanget**<ul><li>Sedan tittar vi på den produkt eller lösning som du fokuserar på, vilket ser till att de identifierade personerna faktiskt är relevanta för det du vill sälja eller marknadsföra.<li>Det kan även lyfta fram eventuella luckor i täckningen (vissa roller saknas kanske för produkten) så att du vet var du ska fokusera.</ul> <li>**Mappa persona till att köpa grupproller** <ul><li>Slutligen mappar agenten dessa profiler till specifika köpgruppsroller, som beslutsfattare, påverkare och mästare.<li>Utifrån den här mappningen kan agenten rekommendera en inköpsgruppdisposition åt dig, som du kan granska, justera eller bekräfta.</ul> </ol> När de här tre komponenterna är samlade skapas en inköpsgrupp med medlemsinformation, roller och insikter som du kan använda. |
| Köpa grupper under en resa | Inom en resa kan en inköpsgrupp användas som central enhet i orkestrationen, vilket gör det möjligt för marknadsförare att utforma upplevelser som anpassar sig till gruppens dynamik i stället för att behandla enskilda medlemmar. Du kan till exempel rikta in dig på hela gruppen med samordnade meddelanden och samtidigt anpassa rollspecifikt innehåll till beslutsfattare, påverkare eller slutanvändare. Som intent-signaler och engagemangsdata flödar in kan resor förgrenas baserat på gruppberedskap, ytvarningar för försäljning när kritiska roller aktiveras eller automatiskt utlösa närliggande steg om viktiga personligheter saknas. Detta flöde garanterar att alla kontaktytor (från e-post till kontobaserade annonser till utåtriktade säljprojekt) fungerar tillsammans för att föra gruppen framåt i deras inköpsprocess, vilket ökar konsensusfrekvensen och minskar friktionen på vägen till inköp. |
| Resor i Journey Optimizer B2B edition | En resa kan byggas med eller utan en köpgrupp, men precisionen och effekten ändras avsevärt:<ul><li>**Utan en inköpsgrupp** byggs resor vanligtvis runt konton. Marknadsförarna kan fortfarande använda signaler som avsikt, beteende eller produktintresse för att utlösa vårdsflöden och utåtriktad verksamhet. Den här metoden fungerar för enklare rörelser eller när du har begränsade data om ett konto. Det riskerar dock att förbise en bredare uppsättning intressenter som påverkar avtalet, vilket kan minska konverteringsgraden eller skapa luckor i engagemanget.<li>**Med en inköpsgrupp** orkestreras resor runt hela uppsättningen personer som deltar i ett inköpsbeslut. Ni kan anpassa stegen till milstolpar på gruppnivå (t.ex. när kommittén når ett slutresultat eller visar gemensamt engagemang), samtidigt som ni personaliserar kontaktytorna för varje roll. Med den här metoden kan ni utforma ett samordnat flertrådigt engagemang: en beslutsfattare kan få strategisk avkastning, medan påverkarna får djupgående produktinformation och försäljningen uppmärksammas när viktiga roller engagerar. Genom att kartlägga både den individuella och den kollektiva resan kan marknadsförare och säljare snabba upp konsensusskapandet och föra möjligheterna framåt effektivare. </ul> |
| Identifiera persondata med hjälp av affärsmöjlighetsdata | För att ni ska få en så korrekt bild som möjligt av vem som är engagerande och var deras intressen finns, vänder er agenten till en personlig rankning och produktavsikt enligt följande: <ul><li>Bästa scenario: Om du kan tillhandahålla data som _säljprojektsfas_, _avslutsdatum för säljprojekt_ och en tydlig _säljprojekt-till-produkt-mappning_ kan agenten säkert rangordna personifierade per produkt.<li>Den här rankningen ger en exakt förståelse för engagemang och intresse i hela kontot. </ul>Men agenten vet att informationen inte alltid är fullständig, vilket är OK. Det innehåller smarta reservfunktioner som håller fart på saker och ting:<ul><li>Agenten analyserar aktivitetsvolymen och ger mer vikt åt de senaste aktiviteterna med tidsminskning.<li>Med den här viktningen kan agenten differentiera och rangordna personer, även utan fullständiga data om affärsmöjligheter. </ul>När det gäller att länka möjligheter till produkter, så här hanterar agenten det:<ul><li>_Idealiskt_: Du anger eller hjälper agenten att skapa mappningstabellen.<li>_Om inte tillgängligt_: Agenten använder otydlig matchning för att ansluta punkterna.<li>_Ingen länkning alls_: Agenten ger upphov till produktåtergivning baserat på de senaste aktiviteterna före stängningsdatumet.</ul>Med detta lageruppbyggda tillvägagångssätt kan agenten fortfarande leverera meningsfulla insikter, även när data inte är perfekta. |
| Affärsmöjlighetsanalys | Agenten tittar på historiska affärsmöjligheter för att förstå vilka faktorer som mest förutser en vinst och använder tre huvuddimensioner för att göra det:<ol><li>Vinstfrekvens: Visar hur ofta avtal stängs när vissa personer är inblandade. Om konton med ett visst personmönster (som en teknisk utvärderare eller en beslutsfattare på VP-nivå) ofta konverteras ger modellen en högre vikt till det mönstret. Den här informationen är en procentandel av de totala möjligheterna, till exempel affärsmöjligheter som är stängda eller vunna.<li>Medlemskap: Mäter hur ofta en viss typ visas över möjligheterna för en viss produkt. Om vissa personligheter konsekvent visas i lyckade avtal anger det att de spelar en viktig roll i köpprocessen.<li>Personlig påverkan: kvantifierar hur mycket en viss person bidrar till resultatet, inte bara om de är närvarande, utan hur deras engagemang eller aktivitetsnivå korrelerar med vinsterna.</ol>Dessa signaler hjälper tillsammans till att avgöra vilka personer som har störst effekt på köpresultatet, även när affärsmöjligheterna är ofullständiga. Med tiden kan systemet identifiera de personer och mönster som är mest prediktiva för att lyckas med avtal, och som sedan informerar om kontoavsikt, personmappning och rekommendationer för köpgrupper. |
| Återgivning | När någon besöker en webbsida eller klickar på en e-postlänk som är relaterad till en produkt, är det en signal om att de är intresserade och det kallas _återgivning_.<br/><br/>Agenten börjar med en taxonomi, som i princip är en lista över kundens produkter och nyckelorden som beskriver dem. Denna information hjälper agenten att förstå vad varje innehålls- eller interaktionsdel handlar om.<br/><br/>Därefter använder agenten den taxonomin för att etikettera besökaraktivitet, till exempel vilka nyckelord eller produkter deras åtgärder relaterar till.<br/><br/>Sedan tittar agenten på hur djupt någon engagerar sig, till exempel hur många sidor de besöker eller hur ofta de interagerar. Den här informationen används för att beräkna poängen för de enskilda avsikterna för specifika nyckelord, produkter eller produktkategorier. Varje poängmetod samlas i metoden _Hög_, _Medium_ eller _Låg_ för att ange räntestyrkan. (Låg återgivning: `<=0.2`, Medium-återgivning: `0.2 < score <= 0.6`, hög återgivning: `0.6 < score <= 1`)<br/><br/>Slutligen kombinerar agenten återgivningspoängen för alla personer från samma företag (konto) för att se den övergripande återgivningsmetoden, som visar vilka produkter eller ämnen som företaget verkar vara mest intresserade av. |
| Roller som påverkar en inköpsgrupp | Varje inköpsgrupp består av roller som bidrar på ett annat sätt till inköpsbeslutet, till exempel _Beslutsfattaren_, _Påverkaren_, _Författaren_ och _Slutanvändaren_. Varje roll har olika effekt.<br/><br/>Beslutsfattare har störst påverkan och styr vanligtvis budgetgodkännanden. Påverkar formutvärderingen och rekommendationerna. Champions hjälper till att skapa intern konsensus, medan slutanvändarna validerar produktens kvalitet.<br/><br/>Genom att visa dessa roller hjälper agenten dig att förstå vem som driver köpbeslutet, var ditt engagemang är som störst och var det kan finnas luckor i täckningen. Med den här informationen kan du fokusera på de roller som är viktigast för den här produkten. |
| Personlig eller rolltäckning | För en given produkt finns det vanligtvis en uppsättning nyckelroller och -profiler som kan påverka köpet (_N_ -roller eller -roller).<br/><br/>För varje konto beräknar agenten täckning genom att kontrollera hur många av dessa _N_-roller som representeras av minst en person i det kontot.<br/><br/>Om det finns alla _N_-roller har kontot full täckning. Om endast vissa roller representeras är disponeringen partiell.<br/><br/>I enkla termer mäter roll och personlig täckning hur komplett din inköpsgrupp är för en produkt, baserat på om alla viktiga beslutsfattare, påverkare och mästare är inkluderade. |

## Krav för XDM-data

Audience Agent ger insikter om konton som visar förstahandsval för produkter och beräknar persona och roller baserat på definierade data. Kontrollera att följande nödvändiga data är konfigurerade att använda Audience Agent-funktioner:

### XDM-fältmappning

<table>
  <tbody>
    <tr>
      <th>XDM-fält</th>
      <th>Entitet</th>
      <th>Affärsdefinition</th>
      <th>Ytterligare information</th>
    </tr>
    <tr>
      <td>
        <p>
          <span>b2b.accountKey.sourceKey</span>
        </p>
      </td>
      <td>
        <p>
          <span>Profiler</span>
        </p>
      </td>
      <td>Kontoidentifierare, används i kopplingar till data för affärsmöjlighet, händelse och avsikt</td>
      <td rowspan="2">Affärsmöjlighetsanalys<br/>Kontoprospektering<br/>
        <br/>
      </td>
    </tr>
    <tr>
      <td>
        <p>
          <span>b2b.personKey.sourceKey</span>
        </p>
      </td>
      <td>
        <p>
          <span>Profiler</span>
        </p>
      </td>
      <td>Personidentifierare, används i kopplingar som innehåller händelsedata till profildata</td>
    </tr>
    <tr>
      <td>
        <p>
          <span>extendedWorkDetails.avdelningarna</span>
        </p>
      </td>
      <td>
        <p>
          <span>  Profiler </span>
        </p>
      </td>
      <td>Profil/person på jobbavdelningen</td>
      <td rowspan="5">
        <p>
          <br/>
        </p>
        <p>Personamappning</p>
      </td>
    </tr>
    <tr class="">
      <td>
        <p>
          <span>extendedWorkDetails.jobTitle</span>
        </p>
      </td>
      <td>
        <p>
          <span>  Profiler </span>
        </p>
      </td>
      <td>Befattning över profil/person som används vid beräkning av personuppgifter</td>
    </tr>
    <tr>
      <td>
        <p>
          <span>person.name.firstName</span>
        </p>
      </td>
      <td>
        <p>
          <span >Profiler</span>
        </p>
      </td>
      <td>Förnamn på person som används av Audience Agent för att visa namn i användargränssnittet när det uppfyller något villkor</td>
    </tr>
    <tr class="">
      <td>
        <p>
          <span>person.name.fullName</span>
        </p>
      </td>
      <td>
        <p>
          <span> profiler</span>
        </p>
      </td>
      <td>Fullständigt namn på person som används av Audience Agent för att visa namn i användargränssnittet när villkoren uppfylls</td>
    </tr>
    <tr class="">
      <td>
        <p>
          <span>person.name.lastName</span>
        </p>
      </td>
      <td>
        <p>
          <span> profiler</span>
        </p>
      </td>
      <td>Efternamn, används av Audience Agent för att visa namn i användargränssnittet när det uppfyller något villkor</td>
    </tr>
    <tr>
      <td>
        <p>
          <span>accountKey.sourceKey</span>
        </p>
      </td>
      <td>
        <p>
          <span> konton</span>
        </p>
      </td>
      <td>Kontoidentifierare, används i kopplingar till data för affärsmöjlighet, händelse och avsikt</td>
      <td>Affärsmöjlighetsanalys<br/>Kontoprospektering</td>
    </tr>
    <tr>
      <td>
        <p>
          <span>accountName</span>
        </p>
      </td>
      <td>
        <p>
          <span>Konton</span>
        </p>
      </td>
      <td>Kontonamn som används av Audience Agent för att visas i användargränssnittet när det uppfyller något villkor i användarfrågan</td>
      <td rowspan="4">
        <p>
          <br/>
        </p>
        <p>
          <br/>
        </p>
        <p>
          <br/>
        </p>
        <p>Kontoprospektering</p>
      </td>
    </tr>
    <tr>
      <td>
        <p>
          <span>accountDescription</span>
        </p>
      </td>
      <td>
        <p>
          <span>Konton</span>
        </p>
      </td>
      <td>Beskrivning av konto/företag som används av Audience Agent för att tillämpa filter på konton baserat på användarfråga i användargränssnittet </td>
    </tr>
    <tr>
      <td>
        <p>
          <span>accountOrganization.industry</span>
        </p>
      </td>
      <td>
        <p>
          <span>  Konton </span>
        </p>
      </td>
      <td>Bransch för konto/företag som används av Audience Agent för att tillämpa filter på konton baserat på användarfråga i användargränssnittet </td>
    </tr>
    <tr>
      <td>
        <p>
          <span>accountBillingAddress.region</span>
        </p>
      </td>
      <td>
        <p>
          <span>  Konton </span>
        </p>
      </td>
      <td>Faktureringsadress för konto/företag som används av Audience Agent för att tillämpa filter på konton baserat på användarfråga i användargränssnittet </td>
    </tr>
    <tr>
      <td>
        <p>
          <span>accountKey.sourceKey</span>
        </p>
      </td>
      <td>
        <p>
          <span>Möjlighet</span>
        </p>
      </td>
      <td>Kontoidentifierare, används i kopplingar till data för affärsmöjlighet, händelse och avsikt</td>
      <td rowspan="2">
        <p>Affärsmöjlighetsanalys<br/>Kontoprospektering</p>
      </td>
    </tr>
    <tr>
      <td>
        <p>
          <span>OpportunityKey.sourceKey</span>
        </p>
      </td>
      <td>
        <p>
          <span>Möjlighet</span>
        </p>
      </td>
      <td>Affärsmöjlighets-ID, används i kopplingar för att kontodata</td>
    </tr>
    <tr>
      <td>
        <p>
          <span>affärsmöjlighetsnamn</span>
        </p>
      </td>
      <td>
        <p>
          <span> säljprojekt</span>
        </p>
      </td>
      <td>Namn på affärsmöjlighet som används av Audience Agent </td>
      <td rowspan="5">
        <p>
          <br/>
        </p>
        <p>
          <br/>
        </p>
        <p>
          <br/>
        </p>
        <p>
          <br/>
        </p>
        <p>
          <br/>
        </p>
        <p>Affärsmöjlighetsanalys</p>
      </td>
    </tr>
    <tr>
      <td>
        <p>
          <span>isWon</span>
        </p>
      </td>
      <td>
        <p>
          <span>Möjlighet</span>
        </p>
      </td>
      <td>om affärsmöjligheten vinner (binärt)</td>
    </tr>
    <tr>
      <td>
        <p>
          <span>affärsmöjlighetBeskrivning</span>
        </p>
      </td>
      <td>
        <p>
          <span>Möjlighet</span>
        </p>
      </td>
      <td>Beskrivning av affärsmöjlighet som används av Audience Agent </td>
    </tr>
    <tr>
      <td>
        <p>
          <span>affärsmöjlighetBelopp</span>
        </p>
      </td>
      <td>
        <p>
          <span>Möjlighet</span>
        </p>
      </td>
      <td>Summa $ som ingår i affärsmöjligheten</td>
    </tr>
    <tr class="">
      <td>
        <p>
          <span>OpportunityType</span>
        </p>
      </td>
      <td>
        <p>
          <span>Möjlighet</span>
        </p>
      </td>
      <td>Typ av affärsmöjlighet</td>
    </tr>
    <tr>
      <td>
        <p>
          <span>OpportunityStage</span>
        </p>
      </td>
      <td>
        <p>
          <span> säljprojekt</span>
        </p>
      </td>
      <td>Affärsmöjlighetens stadium (stängd, förlorad eller någon av de mellanliggande faserna) </td>
      <td rowspan="4">
        <p>Affärsmöjlighetsanalys<br/>Kontoprospektering</p>
      </td>
    </tr>
    <tr>
      <td>
        <p>
          <span>actualCloseDate</span>
        </p>
      </td>
      <td>
        <p>
          <span>Möjlighet</span>
        </p>
      </td>
      <td>Faktiskt stängt datum för affärsmöjlighet</td>
    </tr>
    <tr>
      <td>
        <p>
          <span>expectedCloseDate</span>
        </p>
      </td>
      <td>
        <p>
          <span> säljprojekt</span>
        </p>
      </td>
      <td>Förväntat stängningsdatum för affärsmöjlighet</td>
    </tr>
    <tr>
      <td>
        <p>
          <span>extSourceSystemAudit.createdDate</span>
        </p>
      </td>
      <td>
        <p>
          <span>Möjlighet</span>
        </p>
      </td>
      <td>Skapat datum för affärsmöjligheten</td>
    </tr>
  </tbody>
</table>

### Taxonomidata

Audience Agent utnyttjar förstahandsmetoder som identifierats i Journey Optimizer B2B edition:

1. Beräkning av återgivning kräver taxonomidata (kundprodukter och motsvarande nyckelord) från kunder > Taxonomi
1. Taxonomidata används för att etikettera händelsedata (tillgångsmärkning). Dessa data ger insikter om vilka nyckelord och produkter besökare är intresserade av baserat på deras händelsedata > Resursetiketter 
1. Etiketterade resurser (händelsedata) kombineras med besökarbeteenden (antal besökta sidor) för att fastställa besökarens avsikt på nyckelords-, produkt- och produktkategorinivå → Beräkning av återgivning
1. Resultat av återgivning på besökarprofilnivå samlas på kontonivå för att fastställa kontoåtergivning i ett visst nyckelord, en viss produkt och produktkategori > Intent Account Aggregation

Följande fält är obligatoriska utöver [konfigurering av intent taxonomy](../admin/intent-data.md):

<table>
  <tbody>
    <tr>
      <th>XDM-fält</th>
      <th>Entitet</th>
      <th>Affärsdefinition</th>
    </tr>
    <tr>
      <th>
        <br/>
      </th>
      <th>
        <br/>
      </th>
      <td>personprofil</td>
    </tr>
    <tr>
      <td>
        <p>
          <span>_acp_system_metadata.primaryIdentity.namespace.code<br/>
          </span>
        </p>
      </td>
      <td>
        <p>
          <span>Profil</span>
        </p>
      </td>
      <td>Hjälper dig att identifiera en person (e-post eller b2b_person)</td>
    </tr>
    <tr>
      <td>
        <p>
          <span>_acp_system_metadata.primaryIdentity.id
          </span>
        </p>
      </td>
      <td>
        <p>
          <span>Profil</span>
        </p>
      </td>
      <td>namespace_id</td>
    </tr>
    <tr>
      <td>
        <ul>
          <li>nyckelord_id</li>
          <li>nyckelordsnamn</li>
          <li>product_id</li>
          <li>product_name</li>
          <li>product_category_id</li>
          <li>product_category_name</li>
        </ul>
      </td>
      <td>
        <p>
          <br/>
        </p>
      </td>
      <td>Används som en taxonomi för att etikettera resurser (upplevelsehändelser, som klickade e-postmeddelanden, besökta webbsidor)</td>
    </tr>
    <tr>
      <td>
        <p>
          <span>tidsstämpel</span>
        </p>
      </td>
      <td>
        <p>
          <span>Upplevelsehändelse</span>
        </p>
      </td>
      <td>Används för att få bakåtfyllnad och inkrementell körning</td>
    </tr>
    <tr>
      <td>
        <p>
          <span>eventType</span>
        </p>
      </td>
      <td>
        <p>
          <span>Upplevelsehändelse</span>
        </p>
      </td>
      <td>Hämta händelsetypen eftersom agenten endast bearbetar fyra händelser (<span>directMarketing.emailClicked, directMarketing.emailOpened, directMarketing.emailUnsubscribed, web.webpagedetails.pageViews)</span>
      </td>
    </tr>
    <tr>
      <td>
        <p>
          <span>directMarketing.mailingName</span>
        </p>
      </td>
      <td>
        <p>
          <span>Upplevelsehändelse</span>
        </p>
      </td>
      <td>Endast för referens-/bokföring; information om kampanjnamnet</td>
    </tr>
    <tr>
      <td>
        <p>
          <span>directMarketing.mailingKey.sourceID</span>
        </p>
      </td>
      <td>
        <p>
          <span>Upplevelsehändelse</span>
        </p>
      </td>
      <td>Endast för referens-/bokföring; Information om käll-ID:t som e-postmeddelandet riktar sig till</td>
    </tr>
    <tr>
      <td>
        <p>
          <span>directMarketing.mailingKey.sourceInstanceID<br/>
          </span>
        </p>
      </td>
      <td>
        <p>
          <span>Upplevelsehändelse</span>
        </p>
      </td>
      <td>Endast för referens-/bokföring; Information om källinstansen som e-postmeddelandet riktar sig till</td>
    </tr>
    <tr>
      <td>
        <p>
          <span>directMarketing.mailingKey.sourceKey<br/>
          </span>
        </p>
      </td>
      <td>
        <p>
          <span>Upplevelsehändelse</span>
        </p>
      </td>
      <td>Används för att hämta e-postinnehåll från Marketo Engage datacenter. Det består av (SourceID@SourceInsatceID.SourceType)</td>
    </tr>
    <tr>
      <td>
        <p>
          <span>directMarketing.mailingKey.sourceType<br/>
          </span>
        </p>
      </td>
      <td>
        <p>
          <span>Upplevelsehändelse</span>
        </p>
      </td>
      <td>Endast för referens-/bokföring; Information om källans typ eller varifrån källan kommer </td>
    </tr>
    <tr>
      <td>
        <p>
          <span>web.webPageDetails<br/>
          </span>
        </p>
      </td>
      <td>
        <p>
          <span>Upplevelsehändelse</span>
        </p>
      </td>
      <td>Information om källan som e-postmeddelandet är avsett för</td>
    </tr>
    <tr>
      <td>
        <p>
          <span>web.webPageDetails.name<br/>
          </span>
        </p>
      </td>
      <td>
        <p>
          <span>Upplevelsehändelse</span>
        </p>
      </td>
      <td>Faktisk URL som används för att hämta innehåll</td>
    </tr>
    <tr>
      <td>
        <p>
          <span>web.webPageDetails.queryParameters</span>
        </p>
      </td>
      <td>
        <p>
          <span>Upplevelsehändelse</span>
        </p>
      </td>
      <td>Ytterligare frågeparameter för den URL som används för att hämta målinnehåll </td>
    </tr>
    <tr>
      <td>
        <p>
          <span>web.webPageDetails.isPersonalizedURL</span>
        </p>
      </td>
      <td>
        <p>
          <span>Upplevelsehändelse</span>
        </p>
      </td>
      <td>endast för referens-/bokföring</td>
    </tr>
    <tr>
      <td>
        <p>
          <span>web.webPageDetails.webPageKey.sourceID<br/>
          </span>
        </p>
      </td>
      <td>
        <p>
          <span>Upplevelsehändelse</span>
        </p>
      </td>
      <td>Endast för referens-/bokföring; Information om käll-ID:t som e-postmeddelandet riktar sig till</td>
    </tr>
    <tr>
      <td>
        <p>
          <span>web.webPageDetails.webPageKey.sourceInstanceID<br/>
          </span>
        </p>
      </td>
      <td>
        <p>
          <span>Upplevelsehändelse</span>
        </p>
      </td>
      <td>Endast för referens-/bokföring; Information om källinstansen som e-postmeddelandet är riktat till</td>
    </tr>
    <tr class="">
      <td>
        <p>
          <span>web.webPageDetails.webPageKey.sourceKey<br/>
          </span>
        </p>
      </td>
      <td>
        <span>Upplevelsehändelse</span>
      </td>
      <td>Endast för referens-/bokhållning. Den består av (SourceID@SourceInsatceID.SourceType)</td>
    </tr>
    <tr>
      <td>
        <p>
          <span>web.webPageDetails.webPageKey.sourceType</span>
        </p>
      </td>
      <td>
        <span>Upplevelsehändelse</span>
      </td>
      <td>Endast för referens-/bokföring; Information om källans typ eller varifrån källan kommer</td>
    </tr>
    <tr>
      <td>
        <p>
          <span>web.webPageDetails.webPageKey.URL</span>
        </p>
      </td>
      <td>
        <span>Upplevelsehändelse</span>
      </td>
      <td>Används för att hämta den faktiska URL:en om web.webPageDetails.name inte har den.</td>
    </tr>
  </tbody>
</table>
