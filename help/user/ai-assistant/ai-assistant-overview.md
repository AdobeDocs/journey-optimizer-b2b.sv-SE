---
title: AI Assistant i Journey Optimizer B2B edition
description: Platshållare
feature: AI Assistant
level: Beginner
exl-id: 52ff66d2-1969-4e2c-985a-c75e613368de
source-git-commit: f09f3f5b7d4419ead5308e4c5be3b518b4e16ff5
workflow-type: tm+mt
source-wordcount: '1243'
ht-degree: 1%

---

# AI Assistant i Journey Optimizer B2B edition

AI Assistant i Journey Optimizer B2B edition skapas från samma tekniska grund som [AI Assistant i Adobe Experience Platform](https://experienceleague.adobe.com/en/docs/experience-platform/ai-assistant/home). Det är en samtalsupplevelse som du kan använda för att snabba upp arbetsflödena i Adobe Journey Optimizer B2B edition. Du kan använda AI Assistant för att få mer förståelse för produktens funktioner, felsöka problem eller söka igenom information och hitta operativa insikter för Journey Optimizer B2B Edition.

>[!IMPORTANT]
>
>Ett godkännande av [användarriktlinjerna](https://www.adobe.com/legal/licenses-terms/adobe-dx-gen-ai-user-guidelines.html) krävs innan du kan använda AI Assistant i Journey Optimizer B2B Edition. Det här avtalet innehåller även det offentliga betaavtalet så att du kan använda ytterligare AI Assistant-funktioner när de lanseras i en betakapacitet.

+++Visa gränssnittet för användaravtal

![Den första sidan i användaravtalet.](./assets/user-agreement-1.png)

![Den sista sidan i användaravtalet.](./assets/user-agreement-2.png)

+++

## AI Assistant-funktioner i Journey Optimizer B2B edition

Om du vill formulera ett svar på dina inskickade frågor skickar AI Assistant en fråga till en databas och översätter data från databasen till ett läsbart svar. Det här svaret är en intern representation av underliggande data och kallas även _&#x200B;**_kunskapsdiagram_**&#x200B;_ - en omfattande webbplats med koncept, data och metadata för ett givet svar. Kunskapsdiagrammet består av deldiagram som refereras när frågor skickas:

* Experience League dokumentation.
* Operativa artefakter som scheman, fält, målgrupper och resor.

Ta reda på vilken typ av fråga du behöver innan du skickar en AI Assistant-fråga:

### Produktkunskap

Produktkännedom avser begrepp och ämnen som behandlas i Journey Optimizer B2B edition-dokumentationen om Adobe Experience League. Produktkunskapsfrågor kan specificeras ytterligare i följande undergrupper:

| Produktkunskap | Exempel |
| --- | --- |
| Undervisning | <li>Vad är en inköpsgrupp? <li> Visa mig ett exempel på en mall för inköpsgrupproller? |
| Öppna identifiering | <li>Hur skapar man inköpsgrupper? <li>Hur använder jag anpassade fält i en mall för inköpsgrupproller? |
| Felsökning | <li>Varför skapades inte grupper för min resa? <li>Varför kan jag inte hitta Experience Events att lyssna på under resan? |

### Driftsinsikter

_Driftsinsikter_ hänvisar till svar som AI Assistant genererar om dina metadata-objekt (attribut, kontomålgrupper, dataflöden, datauppsättningar, destinationer, kontoresor, scheman, källor, köp av gruppmallar och lösningsintressen). Dessa insikter omfattar antal, sökningar och linjepåverkan. De tittar inte på några data i sandlådan.

* Vilken kontopublik har den största målgruppen och hur stor är den?
* Hur många kontomålgrupper har aldrig använts på några resor?
* Vilka aktiva resor använder lösningsintresse _x_?

Du kan ställa frågor till AI Assistant om dina operativa insikter i följande domäner:

| Domän | Metadata som stöds | Metadata som inte stöds |
| --- | --- | --- |
| Attribut/fält | <li>Sök attributnamn <li>Attribut - schemarelation <li>Attribut - datauppsättningsrelation <li>Attribut - målgruppsrelation <li>Attribut - målrelation | <li>Klassen Attribute <li>Granskning <li>Föråldringsstatus <li>Etiketter <li>Värde lagrat i attribut |
| Kontomålgrupper <br><br>**_Obs!_**&#x200B;AJO B2B AI Assistant kan bara svara på målgruppsfrågor för kontomålgrupper, medan Experience Platform AI Assistant bara kan svara på frågor för målgrupper | <li>Antal målgrupper <li>Målgruppstyp (direktuppspelning eller batch) <li>Skapande-/ändringsdatum <li>Aktiveringsstatus <li>Antal medlemmar <li>Duplicera målgrupper <li>Sök namn och ID | <li>Målgruppsöverlappningar <li>Målgruppsaktivering <li>Granskning <li>Skapa/ändra <li>Etiketter <li>Trender för medlemskvalifikationer |
| Dataflöden | <li>Antal dataflöden <li>Status för dataflöde <li>Dataflöde – datauppsättningsrelation <li>Dataflöde – källrelation | <li>Skapande/ändring <li>Dataflödesbatchrelationer <li>Antal infogningsprofiler |
| Datauppsättningar | <li>Antal data <li>Aktivera profilstatus <li>Skapad/ändrad den <li>Datauppsättning - schemarelation <li>Datauppsättning - målgruppsrelation <li>Datauppsättning - attributrelation <li>Datauppsättning - dataflödesrelation <li>Namnsökning <li>Sök namn och ID | <li>Granskning <li>Skapad av <li>Datauppsättning - batchrelation <li>Skapa/ändra datauppsättning <li>Datauppsättningsstorlek <li>Antal profiler <li>Antal rader <li>Värdesökning |
| Mål | <li>Konfigurerade destinationsantal <li>Mål - målgruppsrelation <li>Destinationsattributrelation | <li>Kontoinställning <li>Autentiseringsinformation för konto <li>Unika profiler har aktiverats |
| Resor (kontoresor) | <li>Antal <li>Sök namn och ID <li>Resestatus <li>Skapande-/ändringsdatum | <li>Attribut - granskning av reserelationer <li>Skapande/ändring <li>Skapad av |
| Scheman | <li>Antal scheman <li>Skapad/ändrad den <li>Schema - attributrelation <li>Schema - datauppsättningsrelation <li>Schema - målgruppsrelation <li>Aktivera profilstatus <li>Namnsökning <li>Sök namn och ID | <li>Granskning <li>Skapande/ändring <li>Skapad av <li>Fältgrupper <li>Identiteter <li>Identitetsnamnutrymmen <li>Etiketter <li>Antal profiler |
| Källor | <li>Konton <li>Kontostatus <li>Aktiva/inaktiva dataflöden för varje konto <li>Källanslutning – dataflödesrelation <li>Källkonto – dataflödesrelation | <li>Information om kontouppgifter <li>Konfigurera kontoMätvärden för datainmatning <li>Antal profilerKälla - batchrelationer |
| Buying Group Template | <li>Antal <li>Status <li>Roller <li>Sök namn och ID | <li>Rollregler |
| Intresse av lösningar | <li>Antal <li>Status <li>Solution Interest - Buying Group Template relationship <li>Sök namn och ID | <li>Solution Interest - Buying Group relationship |

{style="table-layout:fixed"}

För frågor om operativa insikter kanske svaren inte återspeglar det aktuella tillståndet för användargränssnittet. De data som stöder dessa frågor uppdateras en gång var 24:e timme. Ändringar som användare gör i Real-Time CDP under dagtid synkroniseras till exempel med datalagren på natten, och sedan blir de tillgängliga för användarfrågor på morgonen. Logga in på en sandlåda för att fråga om specifika data relaterade till objekt.

### Funktionens omfattning

För närvarande är omfattningen av AI Assistant följande:

* [Produktkunskap](https://experienceleague.adobe.com/en/docs/experience-platform/ai-assistant/home#product-knowledge): AI Assistant kan svara på frågor om produktkunskap för Real-Time Customer Data Platform och Adobe Journey Optimizer B2B Edition.

* [Driftsinsikter](https://experienceleague.adobe.com/en/docs/experience-platform/ai-assistant/home#operational-insights): Du kan ställa frågor till AI Assistant om operativa insikter för följande dataobjekt: attribut, kontomålgrupper, dataflöden, datauppsättningar, destinationer, kontoresor, scheman, källor, köp av gruppmallar och lösningsintressen.

### Integritet, säkerhet och styrning

AI Assistant i Journey Optimizer B2B edition har tagits fram med sekretess, säkerhet och styrning i framkanten. Läs följande information om du vill veta mer om de funktioner som är inriktade på kundförtroende och som du kan förvänta dig av AI Assistant:

* Inga personuppgifter används av AI Assistant idag, inte ens i utbildningssyfte.

* AI Assistant känner inte till kunddata, som människor, konton, möjligheter och inköpsgrupper.

* Du måste ha uttrycklig behörighet att interagera med AI Assistant.

   * En administratör kan ange behörigheter med [behörighetsgränssnittet](https://experienceleague.adobe.com/en/docs/experience-platform/access-control/abac/permissions-ui/permissions) och [Admin Console](https://experienceleague.adobe.com/en/docs/experience-platform/access-control/ui/browse).

   * Behörigheterna är detaljerade och din sandlådeadministratör kan konfigurera vilka användare som kan ställa olika frågekategorier (produktkunskapsbaserade frågor med AI Assistant eller frågor om driftsinsikter).

* Du kan visa en logg över dina tidigare interaktioner med AI Assistant med en 30-dagars bevarandeprincip.

* AI-assistenten omges av sandlådespecifika data och offentlig Adobe-dokumentation när användaren besvarar uppmaningar. Data delas inte över sandlådor.

* Frågar som du anger för AI Assistant delas inte med andra kunder.

### Frågor och svar

Nedan följer en lista med svar på vanliga frågor om AI Assistant i Journey Optimizer B2B edition.

**Har AI Assistant-information tillhandahållits i realtid?**

Data som presenteras i AI Assistant-svar uppdateras dagligen. Den här cykeln innebär att de data som ingår i svaren kan vara upp till 24 timmar äldre än de data som visas i användargränssnittet vid tidpunkten för svaret.

**Vilka funktioner har AI Assistant?**

AI Assistant kan hantera Adobe frågor om produktkunskap och svara på frågor om driftsinsikter om era operativa artefakter.

**Kan AI Assistant tillhandahålla information om kunddata?**

Nej. AI Assistant har inte tillgång till kunddata och därför varken kontrolleras eller används den av AI Assistant.

**Används mina personuppgifter i AI Assistants utbildningsdata?**

AI Assistant använder inte personuppgifter för utbildningsändamål. Lämna inga personuppgifter om dig själv (ditt namn eller din kontaktinformation) eller andra parter i AI Assistant.

## Nästa steg

Med en allmän förståelse för AI Assistant fortsätter du med att aktivera och använda AI Assistant under dina arbetsflöden. Mer information finns i följande dokumentation:

* [Aktivera åtkomst till AI Assistant](./enable-ai-assistant-access.md)
* [Frågevägledning](./question-guidance.md)
* [Använd AI-assistenten](./use-ai-assistant.md)
