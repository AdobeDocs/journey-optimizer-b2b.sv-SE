---
title: Versionsinformation om Journey Optimizer B2B edition
description: Upptäck de senaste funktionerna, förbättringarna och felkorrigeringarna i Adobe Journey Optimizer B2B edition. Håll dig uppdaterad med nya funktioner och produktförbättringar.
role: User, Admin
exl-id: 7d3f1c26-d8a6-4065-a70f-5b30cb975dc8
source-git-commit: 204b293d3bc526b139f68766ed45ff549a74ed34
workflow-type: tm+mt
source-wordcount: '4053'
ht-degree: 5%

---

# Versionsinformation för Journey Optimizer B2B edition

Adobe Journey Optimizer B2B edition ger kontinuerligt nya funktioner, förbättringar av befintliga funktioner och felkorrigeringar.

Journey Optimizer B2B edition är inbyggt i [!DNL Adobe Experience Platform] och ärver från de senaste innovationerna och förbättringarna. Läs mer om de här ändringarna i [Adobe Experience Platform versionsinformation](https://experienceleague.adobe.com/en/docs/experience-platform/release-notes/latest){target="_blank"}.

Granska [produktbeskrivningen](https://helpx.adobe.com/legal/product-descriptions/adobe-journey-optimizer-b2b.html){target="_blank"} om du vill ha information om berättiganden, prestandaskydd och begränsningar.

## AI-funktioner

Följande agentiska AI-funktioner är nu tillgängliga för Journey Optimizer B2B edition i AI Assistant-gränssnittet:

| Agent | Uppdatering | Beskrivning |
| ----- | ------ | ----------- |
| Journey Build Agent | Nytt och uppdaterat | Journey Build Agent analyserar, identifierar och skapar resor i realtid så att marknadsförarna kan starta snabbare, förbättra engagemanget och öka konverteringsgraden. [Läs mer](../agents/journey-agent.md) |
| Audience-agent | Nyhet | Audience Agent identifierar och bygger automatiskt upp inköpsgrupper med hjälp av strukturerade och ostrukturerade data. Det hjälper marknadsförarna att inrikta sig på rätt personer snabbare och exaktare. [Läs mer](../agents/audience-agent-b2b.md) |
| Försäljningskvalificerare | Nyhet | Försäljningskvalificeraren är ett AI-drivet tillägg till Adobe Journey Optimizer B2B edition som innehåller Account Qualification Agent och är utformat för att effektivisera arbetsflöden för BDR (Business Development Representants). Det automatiserar arbetsflöden för kvalificering av potentiella kunder, utåtriktad verksamhet och köpengagemang i olika kanaler [Läs mer](../agents/sales-qualifier.md) |

## Versionsinformation 2026.1

**Distributionsdatum**: 3 februari 2026

| Typ | Objekt | Beskrivning |
| ---- | ---- | ----------- |
| Funktion | Varumärkessatser | (Beta) Definiera ett varumärke i Journey Optimizer B2B edition för att ge den kreativa teamet den källa som de vill använda när de skapar visuellt eller skrivet innehåll. När dessa riktlinjer sammanställs och varumärkesresurserna delas kan alla teammedlemmar eller medarbetare skapa varumärkesinnehåll för din produkt. |
| Funktion | Varumärken för generering av e-postinnehåll | Ni kan definiera riktlinjer för ert varumärke och använda den här informationen för att generera e-postinnehåll. Med den här funktionen justeras e-postinnehåll efter varumärkesspecifika riktlinjer, format och ton för copywriting. |
| Förbättring | Resa _Vänta_-nod - avancerade inställningar | För en _Wait_-nod i en resa kan du nu ange avslutsdagar och -tider och välja tidszoner. Den här förbättringen ger er bättre kontroll över er resesamordning och kampanjtiming. |
| Förbättring | Specialfiltret Medlem i inköpsgrupp - Begränsningen är borttagen | Specialfiltret _[!UICONTROL Member of Buying Group]_&#x200B;innehåller nu begränsningen_&#x200B;Är borttagen _. När du lägger till den här begränsningen i filtret kan du ta med borttagna köpgruppsmedlemmar eller exkludera dem. Den stöds också i Marketo Engage smarta listor, där du kan använda den nya begränsningen i filtret&#x200B;_[!UICONTROL Member of Buying Group]_. |
| Förbättring | E-postdesign - punkter på flera nivåer | Verktygen för design av e-postinnehåll har nu stöd för underpunkter (punktnivåer). |

<!--
| Feature | Custom external actions for journeys | [!BADGE Simplfified architecture]{type=Informative tooltip="Available for simplified architecture"} (Beta) Developers can now use APIs to  build integrations with their first-party systems. | 
| -->

>[!NOTE]
>
>Dessa ändringar börjar driftsättas den 3 februari 2026, med en fasad driftsättning av varje funktion. Releasedatum för funktioner och förbättringar kan komma att ändras.

## Versionsinformation 2025.10

**Distributionsdatum**: 31 oktober 2025

| Typ | Objekt | Beskrivning |
| ---- | ---- | ----------- |
| Funktion | Aktivera till destinationen för resor | Använd den nya _Aktivera till mål_-företagskontoåtgärden för att aktivera direkt till företag, i stället för enskilda. (Begränsat till LinkedIn-företag för den här versionen.) [Läs mer](../journeys/action-nodes.md#activate-to-a-linkedin-destination) |
| Funktion | Varumärkesteman | Med varumärkesteman kan icke-tekniska användare nu skapa återanvändbart innehåll som passar ett visst varumärke och designspråk genom att lägga in egen formatering ovanpå standardmallarna. [Läs mer](../content/brand-themes.md) |
| Funktion | E-postmallar - konvertera bild till HTML | Nu kan du använda dina designfiler som lagras som JPG- eller PNG-bildfiler och automatiskt generera e-postmallar. [Läs mer](../content/email-template-image-convert.md) |
| Funktion | Personmappning | Koppla kontomedlemmar med etablerade profiler med attributmappning. [Läs mer](../admin/persona-mapping.md) |
| Funktion | Försäljningsinsikter för Salesforce och Dynamics | Medlemmar i säljteam kan nu visa mognadslagrade inköpsgrupper och relaterade insikter inom en Salesforce- eller Dynamics-integrering för att identifiera nya möjligheter. Information om inköpsgrupper som stage, score och relaterade medlemmar ingår. [Läs mer](../buying-groups/incrm-insights.md) |
| Funktion | Aktivera målgrupp för [!DNL Adobe Target] | Nu kan du aktivera en målgrupp från en kontoresa till en extern kundmålgrupp och skicka den till [!DNL Adobe Target]. Med den här integreringen kan du leverera en målgrupp som är kvalificerad genom en färdssekvens för en webbupplevelse som är utformad i [!DNL Target]. [Läs mer](../audiences/target-external-audience.md) |
| Funktion | Instrumentpanel för webbengagemang | En ny instrumentpanel som ger insikter i hur besökarna interagerar med nyckelinnehållet. Det segmenterar data mellan kontobranscher och regioner för att hjälpa er att förstå engagemangstrender. [Läs mer](../dashboards/web-engagement-dashboard.md) |
| Funktion | Kontrollpanel för rollinsikter | Den nya _[!UICONTROL Role Insights]_-instrumentpanelen ger insikter i hur era kampanjer och resor påverkar inköp av rollförvärv och engagemang i grupper. [Läs mer](../buying-groups/buying-group-role-insights.md) |
| Förbättring | Förbättrad poängsättning av kundgruppens fullständighetsbedömning | Nu kan ni se till att inköpsgrupperna återspeglar det faktiska beslutsfattandet med anpassningsbara tröskelvärden för rollmedlemmar för att få en fullständig bedömning.  [Läs mer](../buying-groups/completeness-scores.md) |
| Förbättring | Köpa gruppunderhållsjobb | Jobbfrekvensen för inköpsgruppsunderhåll uppdateras från varje vecka till varje dag. |
| Förbättring | Förlopp för kontoresa | För en publicerad resa som finns i statusvärdet _Live_, _Stängd på nya poster_, _Avbruten_ eller _Färdig_ kan du öppna färdplanen och granska en lista med konton för varje kundnod. |

>[!NOTE]
>
>Dessa ändringar börjar driftsättas den 31 oktober 2025, med en stegvis lansering av varje funktion. Releasedatum för funktioner och förbättringar kan komma att ändras.

### Förenklad arkitektur

Adobe Journey Optimizer B2B edition finns nu i en förenklad arkitektur. Med den här uppdaterade arkitekturen finns Journey Optimizer B2B edition och Marketo Engage inte längre i samma system och datalager. Journey Optimizer B2B edition tar endast emot data från Adobe Experience Platform. Men det fortsätter att förlita sig på Marketo Engage-berättiganden och vissa konfigurationsfunktioner för att etablera och konfigurera systemet.

Den uppdaterade arkitekturen ger flera fördelar:

* **Gör data enhetliga och skalbara**: Den uppdaterade plattformen har stöd för komplexa datamodeller, inklusive anpassade objekt, inköpsgrupper och kontohändelser.
* **Anslut flera Adobe Marketo Engage-instanser**: Hantera och sammanfoga data från flera Adobe Marketo Engage-miljöer på ett och samma ställe.
* **Skydda dina data**: Avancerade sekretess- och säkerhetsfunktioner skyddar din kundinformation.
* **Skapat för framtiden**: Den här uppdateringen ställer in din organisation på kontinuerliga förbättringar och innovation.

>[!NOTE]
>
>Om miljön har etablerats på den här arkitekturen kan du läsa riktlinjerna för [konfiguration](../simplified-architecture.md).

Med den förenklade arkitekturen finns följande nya funktioner och förbättringar i version 2010:

| Typ | Objekt | Beskrivning |
| ---- | ---- | ----------- |
| Funktion | Relationsdatamodell | Utnyttja relationsdata som är länkade till B2B-konton för att filtrera konton inom en kontoresa eller för att personalisera e-postinnehåll. Dessa relationsdata kan representera verkliga affärsenheter som inköpsposter, händelseregistreringar, programvarulicenser, serviceabonnemang eller reservationer. [Läs mer](../admin/xdm-field-management.md#relational-schemas) |
| Funktion | Flera Marketo Engage-aktiveringar | Konfigurera anslutningar till fjärrinstanser av Marketo Engage och använd dessa anslutningar för att konfigurera Marketo Engage-åtgärder för resor. Dessa åtgärder, som att lägga till/ta bort personer från listor eller lägga till personer i en begärandekampanj, gäller för den angivna Marketo Engage-instansen. [Läs mer](../admin/marketo-actions-connect.md) |
| Funktion | Borttagning av trötthet i e-post | Nu kan du aktivera borttagning av dubbletter av e-post för att se till att samma e-post inte skickas flera gånger till samma adress under en resa. Duplicerade adresser blockeras tills den första posten med den e-postadressen slutför resan.  [Läs mer](../content/email-deduplication.md) |
| Förbättring | Kommunikationsbegränsningar | Systemet respekterar nu de kombinerade kommunikationsgränserna för både Marketo Engage och Journey Optimizer B2B edition. [Läs mer](../admin/configure-channels-emails.md#communication-limits) |

<!-- There are additional functional changes with the simplified architecture:

| Item | Description |
| ---- | ----------- |
| Asset management | The system supports an internal asset repository where you can organize folders, edit images, import images, and remove images. It does not support Marketo Engage Design Studio workspaces for asset management. |
| | | -->

<!-- hold for later release 

| Feature | Landing pages | You can now create and publish landing pages in Journey Optimizer B2B Edition to support your journeys and programs. _(Previously a Beta program feature.)_ [Learn more](../content/landing-pages.md) |
| Feature | Forms | You can now create and publish re-usable form components to enable data submission from landing pages that are created and published in Journey Optimizer B2B Edition. _(Previously a Beta program feature.)_ [Learn more](../content/forms.md) |

-->

## Versionsinformation 2025.9

**Distributionsdatum**: 30 september 2025

Den här versionen innehåller följande nya funktioner och förbättringar:

| Typ | Objekt | Beskrivning |
| ---- | ---- | ----------- |
| Funktion | Samarbete med e-postinnehåll | Nu kan du kommentera samarbetet med andra Journey Optimizer B2B edition-användare i samband med en e-postresurs. Du kan tagga dina teammedlemmar så att de får ett e-postmeddelande med information om kommentaren. Meddelande finns också tillgängligt som ett pulsmeddelande. [Läs mer](../content/email-collaboration-tools.md) |
| Funktion | Mörkt läge för e-postdesign | I e-postdesignområdet kan du nu växla till _mörkt läge_. I mörkt läge kan du förhandsgranska e-postinnehållet och definiera anpassade inställningar som ska visas specifikt för mottagare som visar sina e-postmeddelanden i mörkt läge. [Läs mer](../content/email-dark-mode.md) |
| Förbättring | Resor - Dela upp bana efter antal personer i roll | Använd en delad sökväg per kontonod för att ange ett konto som mål med antalet personer i en eller flera inköpsgruppsroller. På vägen kan ni utvärdera inköpsgruppens beredskap för säljaviseringar och annat engagemang baserat på rolldjupet. [Läs mer](../journeys/split-merge-paths-nodes.md#buying-group-filtering-for-accounts) |
| Förbättring | Resor - personfilter för händelser | Använd personfilter för att lyssna efter personhändelser. Dessa filter inkluderar möjligheten att rikta sig till en viss roll för en matchad inköpsgrupp. [Läs mer](../journeys/listen-for-event-nodes.md#add-filters-to-the-people-event) |

>[!NOTE]
>
>De här versionsändringarna börjar driftsättas 30 september 2025, med en stegvis utrullning av varje funktion. Releasedatum för funktioner och förbättringar kan komma att ändras.

## Versionsinformation 2025.8

**Distributionsdatum**: 26 augusti 2025

Den här versionen innehåller följande nya funktioner och förbättringar:

| Typ | Objekt | Beskrivning |
| ---- | ---- | ----------- |
| Funktion | Personpoängfilter för rollmallar och resor | Du kan nu använda _Personens engagemangspoäng_ som ett filter i rollmallar som används för att skapa inköpsgrupper och i delade sökvägsnoder. [Läs mer](../buying-groups/buying-groups-role-templates.md#add-the-template-roles) |
| Funktion | Konfiguration av anpassade roller för inköpsgrupper | Nu kan du konfigurera anpassade roller för inköpsgrupper, så att du kan definiera de roller som är specifika för dina användningsfall. [Läs mer](../buying-groups/default-custom-roles.md) |
| Funktion | Viktningskonfiguration för engagemangspoäng | Du kan nu tilldela vikter till aktiviteter som påverkar poängen för köpgruppsengagemang. I den här funktionen ingår att definiera egna anpassade poängmodeller och ändra den aktiva modellen som påverkar poängberäkningarna för engagemang. [Läs mer](../admin/engagement-score-weighting.md) |
| Förbättring | Villkorligt innehåll för fragment | Nu kan du använda verktygen för villkorligt innehåll för design av visuella fragment. [Läs mer](../content/conditional-content.md) |
| Förbättring | Uppdateringar av engagemangsmusik | Logiken för att köpa gruppengagemang uppdateras för att normalisera poängen. Dessutom kan ni arbeta med engagemangspoäng på medlemsnivå och poäng för kollektiva engagemang för hela inköpsgruppen. [Läs mer](../buying-groups/engagement-scores.md) |
| Förbättring | Aktiv resesynlighet - konton på varje nod | För en aktiv kontoresa kan du komma åt en lista över konton som har nått varje kontonod under resan. |

## Versionsinformation 2025.6

**Distributionsdatum**: 15 juli 2025

Den här versionen innehåller följande nya funktioner och förbättringar:

| Typ | Objekt | Beskrivning |
| ---- | ---- | ----------- |
| Funktion | Integrering med GenStudio for Performance Marketing | (Begränsad tillgänglighet) Nu kan du integrera GenStudio for Performance Marketing e-postupplevelser med Journey Optimizer B2B edition för att förbättra marknadsföringens effektivitet och upprätthålla varumärkets enhetlighet. Med den här integreringen kan du kombinera GenStudio AI-baserade innehållsskapande med de avancerade orkestreringsfunktionerna i Journey Optimizer B2B edition. [Läs mer](../content/genstudio-email-workflow.md) |
| Funktion | Rapportering om skräppostidentifiering | För att undvika skräppostfilter och för att säkerställa att meddelanden levereras till målgruppsinkorgar kan du generera en _skräppostrapport_ direkt i e-postdesignområdet. [Läs mer](../content/email-spam-report.md) |
| Funktion | Personinformationssida | Nu kan du klicka på en persons namn när det visas (som en hyperlänk) på den intelligenta kontrollpanelen, sidan med information om köpgrupper och sidan med kontoinformation. Den här åtgärden öppnar sidan med information om den associerade personen, vilken information som ska visas för kontakten, deras aktivitet och de mest engagerade inköpsgrupperna. [Läs mer](../accounts/person-details.md) |
| Funktion | Åtgärder för konto och inköpsgrupp | Vidta åtgärder direkt från kontoinformation och köp av informationssidor för grupper för snabbt och avsiktligt engagemang. <li>Använd åtgärden _Skicka e-post_ för att skicka ett godkänt Marketo Engage-e-postmeddelande till valda kontokontakter eller till medlemmar i inköpsgrupper. [Läs mer](../accounts/account-details.md#send-emails) <li>Bland köpgruppsinformationen ingår även _Tilldela en ny medlem_, _Ta bort en medlem_ och _Redigera en roll_. [Läs mer](../buying-groups/buying-group-details.md#members-tab) |
| Funktion | Åtkomst till detaljsidor i CRM | Nu kan du konfigurera direktlänkar till Journey Optimizer B2B edition-informationssidor för konton, kontakter och leads i CRM-verktyget (Customer Relationship Management), som Salesforce eller Microsoft Dynamics. [Läs mer](../accounts/crm-linking.md) |
| Funktion | Anpassat CSS-stöd för innehållsdesign | Nu kan du lägga till egen anpassad CSS när du skapar e-post- och landningssidinnehåll i designområdet. [Läs mer](../content/design-custom-css.md) |
| Funktion | Konfiguration av återgivningsnyckelordsmappning | Om du vill aktivera och hantera återgivningsidentifieringsmodellen kan du nu överföra ett kalkylblad för att definiera en kategori för avsiktsdatamappning. [Läs mer](../admin/intent-data.md) |
| Förbättring | Simulera innehåll från e-postsammanfattning | Nu kan du komma åt verktygen _Simulera innehåll_ från e-postsammanfattningen (information och egenskaper) när du öppnar ett e-postmeddelande från e-postlistan. Den här åtkomsten är utöver e-postdesignområdet. [Läs mer](../content/email-simulate-content.md#display-the-email-preview) |
| Förbättring | Visa totalt antal för rollmallslista | Listsidan _[!UICONTROL Roles templates]_&#x200B;har förbättrats med en visning av det totala antalet bredvid sökfältet. |

<!-- The following capabilities are currently available only for a set of program participants (Beta):

**Brand Kit with AI Assistant** - Maintain brand consistency across email assets by storing and managing brand assets. Add assets, such as colors, fonts, logos, themes, visual content, and compliance guidelines, and use them for your generative AI content creation. -->

## Versionsinformation 2025.5

**Distributionsdatum**: 3 juni 2025

Den här versionen innehåller följande nya funktioner och förbättringar:

| Typ | Objekt | Beskrivning |
| ---- | ---- | ----------- |
| Funktion | E-posttestning med Litmus | Med ett [Litmus Enterprise-konto](https://www.litmus.com/email-testing){target="_blank"} kan du nu förhandsgranska din e-poståtergivning i vanliga e-postklienter från Journey Optimizer B2B edition. Tack vare den här integreringen kan du se till att e-postinnehållet ser bra ut och fungerar som det är avsett i varje e-postinkorg. [Läs mer](../content/email-test-rendering.md) |
| Förbättring | Duplicera e-post | När du lägger till ett e-postmeddelande för en kundtjänstnod kan du nu duplicera ett befintligt e-postmeddelande. Ändra inställningen eller innehållet för det duplicerade e-postmeddelandet, eller lämna det intakt.  [Läs mer](../content/add-email.md#add-an-email-to-your-journey) |
| Förbättring | Hanteringsfältstokenformat för e-post | Personalization-tokens för e-postinnehåll använder nu ett uppdaterat format som är helt kompatibelt med Handlebar-skript. Det här formatet använder _kamelskiftläge_ eller understreck, vilket eliminerar mellanslag. [Läs mer](../content/email-authoring.md#content-authoring---personalization) |
| Förbättring | Visa totalt antal för listor | Listsidorna _[!UICONTROL Solution Interests]_&#x200B;och&#x200B;_[!UICONTROL Account Journeys]_ har förbättrats med visningen av det totala antalet bredvid sökfältet. |

## Versionsinformation 2025.4

**Distributionsdatum**: 29 april 2025

Den här versionen innehåller följande nya funktioner och förbättringar:

| Typ | Objekt | Beskrivning |
| ---- | ---- | ----------- |
| Funktion | Kontolistor | Nu kan du skapa en statisk eller dynamisk kontolista för att rikta in namngivna konton efter dina definierade kriterier, till exempel bransch, plats eller företagets storlek. <a href="../accounts/account-lists.md">Läs mer</a> |
| Funktion | Resesamordning för kontolista | Använd noder för reseåtgärder för att lägga till och ta bort konton för statiska kontolistor. <a href="../accounts/account-lists-journeys.md#take-an-action-node---add-to-account">Läs mer</a> |
| Förbättring | Filtrera resemedlemskap i Marketo Engage | Använd Adobe Journey Optimizer B2B edition-kontolistor för kundresan och använd sedan filtret _Medlem i en kontolista_ i Marketo Engage smarta listor. <a href="../accounts/account-lists-journeys.md#marketo-engage-program---member-of-account-list">Läs mer</a> |
| Funktion | Inaktivitetsfilter | Samordna resor baserat på inaktivitet inom Marketo Engage kampanjer och program, inklusive inaktivitet via e-post, intressanta ögonblick, förändringar av datavärde och besökta webbsidor. <a href="../journeys/split-merge-paths-nodes.md#activity-filtering">Läs mer</a> |
| Förbättring | Besökt webbsidesfilter | Samordna resor baserat på aktivitet för besökta webbsidor som är kopplade till Marketo Engage kampanjer och program. <a href="../journeys/split-merge-paths-nodes.md#people-path-filters">Läs mer</a> |
| Förbättring | E-postlista | Visa en global lista över aktiva e-postmeddelanden och utkast för att söka, granska och uppdatera dem över tillhörande kontoresor. <a href="../content/emails-list.md">Läs mer</a> |

## Versionsinformation 2025.3

**Distributionsdatum**: 1 april 2025

Den här versionen innehåller följande nya funktioner och förbättringar:

| Typ | Objekt | Beskrivning |
| ---- | ---- | ----------- |
| Funktion | Duplicera kontoresor | En dubblettåtgärd finns nu tillgänglig för kontoresor. Du kan duplicera informationen för kontoresan eller bara ett enkelt skelett i flödes- och sökvägsstrukturen. <a href="../journeys/journeys-overview.md#duplicate-journey">Läs mer</a> |
| Funktion | Mina token för kontoresor | Nu kan du definiera en uppsättning anpassade tokens med värden som är specifika för kontoresan. Den här uppsättningen anpassade tokens kallas _Mina token_ och någon av dessa anpassade tokens är till för personalisering när du redigerar e-postmeddelanden om resan. <a href="../content/personalization-my-tokens.md">Läs mer</a> |
| Funktion | Ta bort inköpsgruppsfaser | Du kan ta bort inköpsgruppens fasmodell när den är i ett utkast eller publicerat tillstånd. Om den publiceras (live) kan du bara ta bort den när den inte är kopplad till ett lösningsintresse. <a href="../buying-groups/buying-group-stages.md#delete-the-buying-group-stages-model">Läs mer</a> |
| Förbättring | Antal resantnoder | Ökad synlighet i antalet publicerade resemedlemskap på nodnivå. I _resekartan_ visas _[!UICONTROL Total accounts entered]_&#x200B;noder. När du väljer en åtgärdsnod innehåller informationen till höger även&#x200B;_[!UICONTROL Accounts not yet actioned on]_. Och information om _Lyssna efter en händelse_-nod innehåller _[!UICONTROL Accounts at this step]_. Använd den här informationen för att validera kontoutvecklingen på dina resor, som är färdiga och avbrutna. |

## Versionsinformation 2025.2

**Distributionsdatum**: 11 mars 2025

Den här versionen innehåller följande nya funktioner och förbättringar:

| Typ | Objekt | Beskrivning |
| ---- | ---- | ----------- |
| Funktion | Anpassningsbara fält - innehållsfragment | Vid design av visuella fragment kan du ange parametrar för en komponent i fragmentet som redigerbara. Med den här funktionen kan e-postförfattaren eller mallskaparen ange ett anpassat fältvärde som är specifikt för deras behov. Den här anpassningsflaggan är begränsad till visuella komponenter för bild, text och knappar. <a href="../content/fragment-authoring.md#enable-fragment-customization">Läs mer</a> |
| Funktion | Typer av resedubbletter | När du duplicerar en kontoresa kan du inkludera nodinformation, exklusive e-post och SMS-meddelanden som skapats i Journey Optimizer B2B edition. Du kan också skapa en skelettkopia av struktur- och sökvägsflödena utan nodinformation och inställningar. <a href="../journeys/journeys-overview.md#duplicate-journey">Läs mer</a> |
| Förbättring | Fyra extra exempel på e-postmallar | Exempelbiblioteket med e-postmallar innehåller nu fyra SecurFinancial-mallar som exempel för återengagemang, information, näring och exempel på feedback |

<!-- | Feature | B2B built-in roles and product permissions | Experience Platform now includes a set of built-in (default) roles that you can use to manage access to the B2B product capabilities. <a href="../admin/user-management.md#b2b-built-in-roles">Learn more</a> <br/>Administrators can now define custom roles in Adobe Experience Platform to include Journey Optimizer B2B Edition product permissions.  <a href="../admin/user-management.md#b2b-product-permissions">Learn more</a> | -->

## Versionsinformation 2025.1 {#Jan-2025}

**Distributionsdatum**: 6 februari 2025

Den här versionen innehåller följande nya funktioner och förbättringar:

| Typ | Objekt | Beskrivning |
| ---- | ---- | ----------- |
| Funktion | Vidarebefordra upplevelsehändelser | Administratörer kan konfigurera Adobe Experience Platform (AEP)-baserade händelsedefinitioner. Med dessa konfigurationer kan marknadsförare skapa kontoresor som reagerar på AEP Experience Events.  <a href="../admin/configure-aep-events.md">Läs mer</a> |
| Funktion | Betalda mediemål | Kvalificera kända personer för betalda mediekampanjer från en kontoresa så att ni kan engagera dem ytterligare på annonsplattformar som LinkedIn. Använd en delad sökvägsnod för att segmentera målgrupper baserat på specifika beteenden och för att identifiera konton som motiverar ytterligare engagemang. Lägg sedan till personer från dessa konton till en extern kundpublik via CDP i realtid till ett betalmediemål som stöds. <a href="../journeys/action-nodes.md#journey-optimizer-b2b-actions">Läs mer</a> |
| Funktion | Intelligent kontrollpanel | Se hur köpgrupperna fortskrider på sina kontoresor, inklusive AI-genererade insikter för mer intelligent analys och korrekt kontoprioritering. <a href="../dashboards/intelligent-dashboard.md">Läs mer</a> |
| Funktion | Information om inköpsgrupp och konto | Se insikter på köpgrupps- och kontonivå för att få mer kontext och historiska data när ni börjar engagera en kund.<p>Köpgruppens information innehåller alla tredjepartsmetoder som upptäcks. <a href="../buying-groups/buying-group-details.md">Läs mer</a><p>Kontona för kontoinformation belyser den ökning i engagemang som upptäckts, så att ni kan informera om försäljning på konton som är klara för anpassat säljfokuserat engagemang.  <a href="../accounts/account-details.md">Läs mer</a> |
| Funktion | Reseöversikt | När du får åtkomst till kontoresor ger fliken Översikt en omfattande ögonblicksbild av dina aktiva kontoresor, med detaljerad information om kontoförloppet med hjälp av cirkel- och stapeldiagram som kategoriserar och kvantifierar slutföranden samt engagemangsaktiviteter.  <a href="../dashboards/journeys-dashboard.md">Läs mer</a> |
| Funktion | Adobe Express bildredigering | Med Adobe Express snabbåtgärder kan du göra enkla redigeringar (till exempel beskära och ändra storlek) av bilder för att få ett mer elegant utseende i ditt innehåll. <a href="../content/image-edit-adobe-express.md#quick-actions-in-adobe-express">Läs mer</a>  <p>För en mer omfattande uppsättning designverktyg ger integreringen en fullständig Adobe Express-licens för Journey Optimizer B2B edition. Med den här konfigurationen blir Adobe Express hela användargränssnitt tillgängligt på den lokala resursytan. <a href="../content/image-edit-adobe-express.md#adobe-express-enterprise-license">Läs mer</a> |
| Funktion | Återgivningsfilter för inköp av grupproller | När du skickar in dina intent-nyckelord förutser Intent Detection-modellen en lösning/produkt av intresse med tillräcklig säkerhet baserat på en leads aktivitet. <a href="../admin/intent-data.md">Läs mer</a> <p>Den här återgivningsinformationen är tillgänglig för att definiera villkor för inköpsgrupproller <a href="../buying-groups/buying-groups-role-templates.md#add-the-template-roles">Läs mer</a> |
| Förbättring | Stöd för Marketo Engage event under resor | Noden _Lyssna efter händelse_ har nu stöd för två Marketo Engage-händelser på personnivå: _Besökswebbsida_ och _Fyller i formulär_. <a href="../journeys/listen-for-event-nodes.md#listen-for-marketo-engage-event">Läs mer</a> |
| Förbättring | Köpa gruppfilter för Marketo Engage smarta listor | Visa och skapa smarta listor med inköpsgruppsfilter i Marketo Engage. Med dessa filter kan ni inaktivera och inkludera köp av gruppmedlemmar i Marketo Engage-kampanjer och program från kontoresor inom Journey Optimizer B2B edition. <a href="../buying-groups/marketo-engage-smart-list-buying-group-filters.md">Läs mer</a> |
| Förbättring | Marketo Engage listmedlemsfilter för resor och roller | I Journey Optimizer B2B kontrollerar du om Marketo Engage-listmedlemskap är ett villkor för en _delad sökväg av personnoden_ för att undvika dubbletter i reseaktiviteter. <a href="../journeys/split-merge-paths-nodes.md#add-a-split-path-by-people-node">Läs mer</a> <p> Använd listmedlemskap som rollvillkor när du köper grupprollmallar. <a href="../buying-groups/buying-groups-role-templates.md#add-the-template-roles">Läs mer</a> |
| Förbättring | Instrumentpanel för översikt av engagemang | Kontrollpanelen uppdateras för att ge en heltäckande bild av engagemanget. Här visas realtidsstatistik över konton och enskilda interaktioner genom snapshot circle-diagram och trendavslöjande linjediagram över tiden. <a href="../dashboards/engagement-dashboard.md">Läs mer</a> |

## 2024 års utgåvor

Expandera följande listor med funktioner och förbättringar för Journey Optimizer B2B edition som lanserades 2024.

+++Versionsinformation oktober 2024

**Distributionsdatum**: 29 oktober 2024

Den här versionen innehåller följande nya funktioner och förbättringar:

| Typ | Objekt | Beskrivning |
| ---- | ---- | ----------- |
| Funktion | Villkorligt innehåll i e-postmeddelanden | Anpassa ert e-postinnehåll baserat på mottagarnas beteende och profilegenskaper på både konto- och lead-nivå. <p>När du skapar ett e-postmeddelande för din kontoresa i den visuella e-postdesignrymden kan du använda villkorsregler för att definiera flera varianter för valfri innehållskomponent. <a href="../content/conditional-content.md">Läs mer</a> |
| Funktion | _Lägg till i listan_ och _Ta bort från listan_ personåtgärder i resor | Anpassa ert e-postinnehåll baserat på mottagarnas beteende och profilegenskaper på både konto- och lead-nivå. <a href="../journeys/action-nodes.md">Läs mer</a> |
| Funktion | Innehållsstyrning och låsning av komponenter | Om du vill vara säker på att du följer godkända innehållsdesigner kan du använda funktioner för innehållsstyrning för att låsa innehållskomponenter i e-postmallar. När innehållsstyrning är aktiverat i e-postmallen kan marknadsförarna bara ändra de tillåtna elementen för att se till att det är i linje med innehållsstrategin. <a href="../content/template-content-governance.md">Läs mer</a> |
| Funktion | Köpgruppsfaser | När du definierar och publicerar en anpassad testmodell för inköpsgrupper kan du följa upp köpgruppsutvecklingen genom inköpsgruppens livscykelfaser. Använd de här faserna för att identifiera nästa bästa åtgärd för medlemmar i inköpsgrupper. Du konfigurerar övergångsreglerna och resenoderna som bestämmer scenens förlopp och utlöser åtgärder baserat på ändringar. <a href="../buying-groups/buying-group-stages.md">Läs mer</a> |
| Förbättring | Nya färdiga e-postmallar | Exempelmallsbiblioteket innehåller nu ytterligare e-postmallar som utformats för B2B-marknadsförare. Använd de här exempelmallarna som utgångspunkt och lägg till egna varumärken och meddelanden. <a href="../content/email-templates.md#select-a-design-template">Läs mer</a> |
| Förbättring | Anpassade fält som personattribut | Om du har definierat anpassade personfält i kontots målgruppsschema i Experience Platform är dessa fält även tillgängliga som personattribut under villkor. Använd dessa anpassade attribut i: <li>Rollmallar <a href="../buying-groups/buying-groups-role-templates.md#add-the-template-roles">Läs mer</a></li><li>Dela banor efter personresenoder <a href="../journeys/split-merge-paths-nodes.md#add-a-split-path-by-people-node">Läs mer</a></li> |
| Förbättring | Inställningar för e-postkanal | E-postinställningarna visas nu i Journey Optimizer B2B edition-gränssnittet. Du kan snabbt granska aktuella konfigurationer och administratörer kan klicka på _[!UICONTROL Edit settings]_&#x200B;för att gå direkt till inställningarna i Marketo Engage och uppdatera dem enligt organisationens krav. <a href="../admin/configure-channels-emails.md">Läs mer</a> |

+++

+++Versionsinformation september 2024

**Distributionsdatum**: 7 oktober 2024

Den här versionen innehåller följande nya funktioner och förbättringar:

| Typ | Objekt | Beskrivning |
| ---- | ---- | ----------- |
| Förbättring | Bibliotek för centrala resurser | Med det förbättrade biblioteket för _centrala resurser_ kan du använda alla bildresurser i din Marketo Engage-instans på Design Studio-arbetsytorna. Det finns inbyggda skyddsfunktioner som förhindrar redigering av Marketo Engage-resurser från Journey Optimizer B2B edition samt borttagning och flytt. Dessa skydd säkerställer att källmaterialet (Marketo Engage Design Studio) bevaras samtidigt som det går att läsa och återanvända i Journey Optimizer B2B edition.<p>För resurser som endast är avsedda att användas i Journey Optimizer B2B edition har en specifik arbetsyta fullständiga funktioner för resurshantering. <a href="../content/internal-image-assets.md">Läs mer</a> |
| Funktion | Senast använda resurser | Hemsidan i Journey Optimizer B2B edition-appen innehåller nu avsnittet _[!UICONTROL Recently accessed]_, som innehåller en lista över de senast använda resurserna för marknadsföraren eller administratören. Du kan använda den här listan för att gå direkt till resursen som du nyligen arbetade med utan att navigera genom en serie resurssidor och söka. <p>Listan innehåller ytterligare information om ändringen så att du kan bestämma vilken av resurserna som behöver ändras ytterligare från det senaste mötet. För e-postresurser visas den kontoresa där e-postresursen används. <a href="../home-page.md">Läs mer</a> |
| Förbättring | Delad resenod - ändra ordning på banor | I noder med delade sökvägar utvärderas banfiltreringen i uppifrån och ned-ordning. Varje person eller konto fortsätter längs den första vägen som matchar. Du kan ändra ordning på de definierade banorna genom att klicka på upp- och nedpilarna längst upp till höger på varje bankort för att flytta dem högre eller lägre i listan. <a href="../journeys/split-merge-paths-nodes.md#split-paths">Läs mer</a> |
| Förbättring | Delningsnod för resa - ytterligare villkorsattribut för aktivitetshistorik | När du använder villkor för att definiera sökvägsfiltrering för en delad nod av personer finns det ytterligare två attribut: _Öppnad e-post_ och _Levererades via e-post_. Dessa tillägg ger större flexibilitet vid filtrering av personer under resan baserat på e-postaktivitet. <a href="../journeys/journey-nodes.md#split-paths">Läs mer</a> |

+++

+++Versionsinformation augusti 2024

**Distributionsdatum**: 29 augusti 2024

Den här versionen innehåller följande nya funktioner och förbättringar:

| Typ | Objekt | Beskrivning |
| ---- | ---- | ----------- |
| Funktion | LinkedIn-konto matchar målgrupper | Generera LinkedIn Ad-målgrupper via Account Matched Audiences för att hjälpa er att fylla tomma roller i era inköpsgrupper. Genom att definiera en uppsättning inköpsgruppfilter kan du upprätthålla en LinkedIn Matched Audience för att rikta presumtiva kunder som matchar köpgruppsparametrarna. <p>Den här funktionen utnyttjar Experience Platform Destinations för att hantera vissa aspekter av integreringen. <a href="../data/linkedin-account-matched-audiences.md">Läs mer</a> |
| Förbättring | Statuslivscykel för visuella innehållsfragment | Visuella fragment hanteras nu med en statuslivscykel. Fragmentstatusen avgör om den är tillgänglig för användning i en e-post- eller e-postmall och vilka ändringar du kan göra i den. <p>Det här förbättrade arbetsflödet gör det enkelt att hantera återanvänt innehåll enligt din kampanj- och kommunikationskalender. <a href="../content/fragments.md#fragment-status-and-lifecycle">Läs mer</a> |

+++
