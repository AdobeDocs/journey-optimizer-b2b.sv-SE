---
title: XDM-fält
description: Granska standardattributfälten som är synkroniserade mellan Adobe Experience Platform och Journey Optimizer B2B edition.
exl-id: 8c65fdec-e32d-4ba8-be7b-48522cc3dace
source-git-commit: 9031191ead88652df95137a122f379b0ae2516a7
workflow-type: tm+mt
source-wordcount: '1346'
ht-degree: 5%

---

# XDM-fält

Målgruppsdata lagras som attribut i både XDM Business Account- och XDM Business Person-klasserna. Data synkroniseras regelbundet mellan Adobe Experience Platform och Journey Optimizer B2B edition. I följande avsnitt visas standarduppsättningarna med attribut.

>[!TIP]
>
>Du kan modellera XDM Business Person- och XDM Business Account-klasser i en många-till-många-relation genom att använda klassen XDM Business Account Person Relation enligt beskrivningen i [Experience Platform XDM-dokumentationen](https://experienceleague.adobe.com/en/docs/experience-platform/xdm/tutorials/relationship-b2b){target="_blank"}.

## XDM Business Account Person Relation-attribut

| [Egenskap](https://github.com/adobe/xdm/blob/master/docs/reference/mixins/profile/b2b-person-details.schema.md){target="_blank"} | Visningsnamn | Journey Optimizer B2B-visningsnamn | Datatyp | Beskrivning |
|------------------- |---------------------------------- |--------------------------- |-------- |--------------- |
| `personRoles` | Personroller | Roll | Strängarray | En array med roller som är associerade med personen på kontot, till exempel `owner, accountant, designer`. |

## XDM Business Person-attribut

>[!IMPORTANT]
>
>Attributet `workEmail.Address` krävs. Om det är tomt för en medlem i en kontomålgrupp är den personen inte införtärd och utelämnas från kontoresor och inköpsgrupper som refererar till målgruppen.

| [Egenskap](https://github.com/adobe/xdm/blob/master/docs/reference/mixins/profile/b2b-person-details.schema.md){target="_blank"} | Visningsnamn | Journey Optimizer B2B-visningsnamn | Datatyp | Beskrivning |
|------------------- |---------------------------------- |--------------------------- |-------- |--------------- |
| `b2b.isMarketingSuspended` | Indikator för pausad marknadsföring | Marknadsföring har pausats | Boolean | Värdet anger om marknadsföringen har avbrutits för personen. |
| `b2b.marketingSuspendedCause` | Orsak till pausad marknadsföring | Orsak till pausad marknadsföring | Sträng | Om marknadsföringen avbryts för personen anger denna egenskap anledningen till detta. |
| `b2b.personStatus` | Personstatus | Leadkälla | Sträng | Fältregistrering av den aktuella marknadsförings-/försäljningsstatusen för personen. |
| `consents.marketing.email.reason` | Anledning till avanmälan | Orsak till avprenumeration | Sträng | Orsak som är associerad med e-postavanmälan. |
| `consents.marketing.email.val` | Avprenumererad | Avprenumererad | Sträng | Om det är sant att prenumerera (till exempel värde = 1) anger du `consents.marketing.email.val` som (n). Om det är falskt att avsluta prenumerationen (till exempel värde = 0) anger du `consents.marketing.email.val` som null. |
| `extendedWorkDetails.jobTitle` | Befattning | Befattning | Sträng | Personens befattning. |
| `faxPhone.number` | Nummer | Faxnummer | Sträng | Faxnummer. |
| `mobilePhone.number` | Nummer | Mobiltelefon | Sträng | Det mobiltelefonnummer som är associerat med personen. |
| `person.birthDate` | Födelsedatum (ÅÅÅ-MM-DD) | Födelsedatum | Sträng | Det fullständiga datumet då en person föddes. YYY-MM-DD |
| `person.name.courtesyTitle` | Titel | Titel | Sträng | Vanligtvis en förkortning av en persons titel, ära eller hälsningsfras. Artikeltiteln används framför det fullständiga namnet eller efternamnet i öppningstexter. Till exempel herr, fröken eller doktor |
| `person.name.firstName` | Förnamn | Förnamn | Sträng | Det första segmentet i namnet i den skriftliga ordningen som oftast används på namnet. I många kulturer är det det primära personliga namnet eller förnamnet. Egenskaperna firstName och lastName har införts för att bibehålla kompatibiliteten med befintliga system som modellerar namn på ett förenklat, icke-semantiskt och icke-internationaliserbart sätt. `xdm:fullName` är alltid att föredra. |
| `person.name.lastName` | Efternamn | Efternamn | Sträng | Det sista segmentet i namnet i den skriftliga ordningen som oftast används på namnet. I många kulturer är det det ärvda familjenamnet, efternamnet, patronymiskt eller matronymiskt namn. Egenskaperna firstName och lastName har införts för att bibehålla kompatibiliteten med befintliga system som modellerar namn på ett förenklat, icke-semantiskt och icke-internationaliserbart sätt. `xdm:fullName` är alltid att föredra. |
| `person.name.middleName` | Mellannamn | Mellannamn | Sträng | Mellannamn, alternativa namn eller ytterligare namn som anges mellan förnamnet och efternamnet. |
| `workAddress.city ` | Ort | Ort | Sträng | Namnet på staden. |
| `workAddress.country` | Land | Land | Sträng | Namnet på det statligt administrerade territoriet. Förutom `xdm:countryCode` är det ett friformsfält som kan ha landsnamnet på vilket språk som helst. |
| `workAddress.postalCode` | Postnummer | Postnummer | Sträng | Postnumret för platsen. Postnummer är inte tillgängliga för alla länder. I vissa länder innehåller den endast en del av postnumret. |
| `workAddress.state` | Stat | Stat | Sträng | Namnet på tillståndet för adressen. Det är ett frihandsfält. |
| `workAddress.street1` | Gatuadress 1 | Adress | Sträng | Primär information om gatuminivå, lägenhetsnummer, gatunummer och gatunamn. |
| `workEmail.address` | Adress | E-postadress | Sträng | **Obligatoriskt fält** <br/>Den tekniska adressen, till exempel `<name@domain.com>`, som vanligen definieras i RFC2822 och efterföljande standarder. |
| `workEmail.status` | Status | E-post pausad | Sträng | En indikation på möjligheten att använda e-postadressen. |
| `workPhone.number` | Nummer | Telefonnummer | Sträng | Telefonnummer till arbetet. |

## XDM Business Account-attribut

>[!IMPORTANT]
>
>Attributet `accountName` krävs. Om det är tomt för ett konto hos en målgrupp, är det kontot inte inmatat och utelämnas från kontoresor och inköpsgrupper som refererar till målgruppen.

| [Egenskap](https://github.com/adobe/xdm/blob/master/docs/reference/mixins/account/account-details.schema.md){target="_blank"} | Visningsnamn | Journey Optimizer B2B-visningsnamn | Datatyp | Beskrivning |
|------------------- |---------------------------------- |--------------------------- |-------- |--------------- |
| `accountBillingAddress.city` | Ort | Ort | Sträng | Namnet på den ort som används i faktureringsadressen. |
| `accountBillingAddress.country` | Land | Land | Sträng | Namnet på det myndighetsadministrerade området som används i faktureringsadressen. Förutom `xdm:countryCode` är det ett friformsfält som kan ha landsnamnet på vilket språk som helst. |
| `accountBillingAddress.postalCode` | Postnummer | Adress Postnummer | Sträng | Postnummer för platsen för faktureringsadressen. Postnummer är inte tillgängliga för alla länder. I vissa länder innehåller den endast en del av postnumret. |
| `accountBillingAddress.region` | Län | Adressregion | Sträng | Faktureringsadressens region, län eller distrikt. |
| `accountBillingAddress.state` | Stat | Stat | Sträng | Namnet på delstat för faktureringsadressen. Det är ett frihandsfält. |
| `accountBillingAddress.street1` | Gatuadress 1 | Gatuadress 1 | Sträng | Primär gatuminivåinformation för faktureringsadressen, som vanligtvis ska innehålla lägenhetsnummer, gatunummer och gatunamn. |
| `accountName` | Namn | Namn | Sträng | **Obligatoriskt fält** <br/>Företagets namn. I det här fältet tillåts upp till 255 tecken. |
| `accountOrganization.annualRevenue.amount` | Årlig intäkt | Årlig intäkt | Nummer | Organisationens beräknade årsomsättning. |
| `accountOrganization.industry` | Bransch | Bransch | Sträng | Branschen tillskrivs organisationen. Det är ett frihandsfält och du bör använda ett strukturerat värde för frågor eller egenskapen `xdm:classifier`. |
| `accountOrganization.logoUrl` | URL för logotyp | URL för logotyp | Sträng | Sökväg som ska kombineras med URL:en för en Salesforce-instans (till exempel `https://yourInstance.salesforce.com/`) för att generera en URL för att begära den profilbild för sociala nätverk som är associerad med kontot. Den genererade URL:en returnerar en HTTP-omdirigering (kod 302) till profilbilden för det sociala nätverket för kontot. |
| `accountOrganization.numberOfEmployees` | Antal anställda | Antal anställda | Heltal | Antalet anställda i organisationen. |
| `accountOrganization.SICCode` | SNI-kod | SNI-kod | Sträng | Koden för standardnäringsgrensindelning (SIC) är en fyrsiffrig kod som kategoriserar de branscher som företagen tillhör baserat på deras affärsverksamhet. |
| `accountOrganization.website` | Webbplatsens URL | Domännamn | Sträng | URL till organisationens webbplats. |
| `accountPhone.number` | Ej tillämpligt | Telefonnummer till konto | Sträng | Telefonnumret som är associerat med kontot. |
| `accountSourceType` | Ej tillämpligt | Source Type | Sträng | Source-typ för kontot. |

## XDM Affärsmöjlighetsattribut

Dessutom lagras affärsmöjlighetsdata som attribut i klassen XDM Business Opportunity, som kan kopplas till klassen XDM Business Account via en många-till-en-relation, vilket beskrivs i [dokumentationen för Experience Platform](https://experienceleague.adobe.com/en/docs/experience-platform/xdm/tutorials/relationship-b2b#relationship-field){target="_blank"}.

| [Egenskap](https://github.com/adobe/xdm/blob/master/docs/reference/adobe/experience/marketo/opportunity-marketo.schema.md){target="_blank"} | Visningsnamn | Journey Optimizer B2B-visningsnamn | Datatyp | Beskrivning |
|------------------- |---------------------------------- |--------------------------- |-------- |--------------- |
| `expectedCloseDate` | Förväntat stängningsdatum | Förväntat stängningsdatum för affärsmöjlighet | Sträng | Förväntat slutdatum för affärsmöjligheten. |
| `expectedRevenue.amount` | Förväntade intäkter | Förväntad intäkt för affärsmöjlighet | Sträng | Beräknad intäkt baserad på belopp och sannolikhet. |
| `fiscalQuarter` | Räkenskapskvartal | Räkenskapskvartal för affärsmöjlighet | Sträng | Det avsedda räkenskapskvartalet för affärsmöjligheten. |
| `fiscalYear` | Räkenskapsår | Räkenskapsår för affärsmöjlighet | Sträng | Det avsedda räkenskapsåret för affärsmöjligheten. |
| `forecastCategory` | Prognoskategori | Prognoskategori för affärsmöjlighet | Sträng | Prognoskategori som bestäms av värdet för affärsmöjlighetsfasen. |
| `forecastCategoryName` | Prognoskategorinamn | Kategorinamn för prognos för affärsmöjlighet | Sträng | Prognoskategorinamn som visas i rapporter för en viss prognoskategori. |
| `isClosed` | Stängd flagga | Affärsmöjligheten har stängts | Sträng | Flagga som anger om affärsmöjligheten är stängd. |
| `isWon` | Won-flagga | Vunnen affärsmöjlighet | Sträng | Flagga som anger om affärsmöjligheten vinner. |
| `lastActivityDate` | Senaste aktivitetsdatum | Senaste aktivitetsdatum | Sträng | Senaste aktivitetsdatum för affärsmöjligheten. |
| `leadSource` | Leadkälla | Leadkälla | Sträng | Source om affärsmöjligheten, som Advertisement, Partner eller Web. |
| `nextStep` | Nästa steg | Nästa steg i affärsmöjligheten | Sträng | Beskrivning av nästa uppgift för att stänga affärsmöjligheten. |
| `opportunityAmount.amount` | Affärsmöjlighet - belopp | Totalt belopp för affärsmöjlighet | Sträng | Uppskattat totalt försäljningsbelopp för affärsmöjligheten. |
| `opportunityDescription` | Beskrivning av affärsmöjlighet | Beskrivning av affärsmöjlighet | Sträng | Ytterligare information som beskriver möjligheten, till exempel möjliga produkter att sälja eller tidigare inköp från kunden. |
| `opportunityName` | Affärsmöjlighetens namn | Affärsmöjlighetens namn | Sträng | Ämne- eller beskrivande namn, t.ex. den förväntade ordern eller företagsnamnet, för affärsmöjligheten. |
| `opportunityQuantity` | Kvantitet för affärsmöjlighet | Kvantitet för affärsmöjlighet | Sträng | Totalt av alla fältvärden för kvantitet för alla produkter i den relaterade produktlistan för affärsmöjligheten. |
| `opportunityStage` | Affärsmöjlighet | Möjlighetsfas | Sträng | Försäljningsfasen där säljteamet kan hjälpa säljarna att vinna. |
| `opportunityType` | Typ av affärsmöjlighet | Typ av affärsmöjlighet | Sträng | Typ som tilldelats affärsmöjligheten, till exempel _Befintlig verksamhet_ eller _Ny verksamhet_ |
| `probabilityPercentage` | Sannolikhetsprocent | Sannolikhet för affärsmöjlighet i procent | Sträng | Sannolikheten för att stänga affärsmöjligheten anges i procent. |
