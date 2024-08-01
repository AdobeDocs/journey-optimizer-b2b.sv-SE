---
title: XML-fältmappning
description: Granska fältmappningen mellan AEP XDM-schemat, Marketo Engage och Journey Optimizer B2B Edition.
exl-id: 8c65fdec-e32d-4ba8-be7b-48522cc3dace
source-git-commit: 78d82aa8b3bb8b8d432eeb187d75e2354dbff3ee
workflow-type: tm+mt
source-wordcount: '946'
ht-degree: 7%

---

# XDM-fältmappning

Dataöverföringstjänsten (DTS) ansvarar för att synkronisera data från Adobe Experience Platform till Journey Optimizer B2B Edition. DTS förlitar sig på mappningar mellan Experience Platform XDM-schemafält och deras motsvarigheter i Marketo Engage.

## XDM Business Person - standardfältkopplingar

| [XDM Business Person](https://github.com/adobe/xdm/blob/master/docs/reference/mixins/profile/b2b-person-details.schema.md) | XDM-visningsnamn | Marketo Engage visningsnamn | XDM-typ | Marketo Type | XDM-beskrivning |
|------------------- |---------------------------------- |--------------------------- |-------- |------------ |--------------- |
| `b2b.companyName` | Företagets namn | Företagets namn | string | string | Namnet på det företag som en affärsman är associerad med. |
| `b2b.companyWebsite` | Företagets webbplats | Webbplats | string | url | Webbplats för det företag som en affärsman är kopplad till. |
| `b2b.isMarketingSuspended` | Indikator för pausad marknadsföring | Marknadsföring har pausats | boolesk | boolesk | Värdet anger om marknadsföringen har avbrutits för personen. |
| `b2b.marketingSuspendedCause` | Orsak till pausad marknadsföring | Orsak till pausad marknadsföring | string | string | Om marknadsföringen avbryts för personen anger denna egenskap anledningen till detta. |
| `b2b.personStatus` | Personstatus | Leadkälla | string | string | Fältregistrering av den aktuella marknadsförings-/försäljningsstatusen för personen. |
| `consents.marketing.email.reason` | Anledning till avanmälan | Orsak till avprenumeration | string | string | Orsak som är associerad med e-postavanmälan. |
| `consents.marketing.email.val` | Avprenumererad | Avprenumererad | string | boolesk | Om det är sant att prenumerera (till exempel värde = 1) anger du `consents.marketing.email.val` som (n). Om unsubscribed är false (till exempel value = 0) anger du consents.marketing.email.val som null. |
| `extendedWorkDetails.jobTitle` | Befattning | Befattning | string | string | Personens befattning. |
| `faxPhone.number` | Nummer | Faxnummer | string | telefon | Faxnummer. |
| `mobilePhone.number` | Nummer | Mobiltelefon | string | telefon | Det mobiltelefonnummer som är associerat med personen. |
| `person.birthDate` | Födelsedatum (ÅÅÅ-MM-DD) | Födelsedatum | string | datum | Det fullständiga datumet då en person föddes. YYY-MM-DD |
| `person.name.courtesyTitle` | Titel | Titel | string | string | Vanligtvis en förkortning av en persons titel, ära eller hälsningsfras. Artikeltiteln används framför det fullständiga namnet eller efternamnet i öppningstexter. Till exempel herr, fröken eller doktor |
| `person.name.firstName` | Förnamn | Förnamn | string | string | Det första segmentet i namnet i den skriftliga ordningen som oftast används på namnet. I många kulturer är det det primära personliga namnet eller förnamnet. Egenskaperna firstName och lastName har införts för att bibehålla kompatibiliteten med befintliga system som modellerar namn på ett förenklat, icke-semantiskt och icke-internationaliserbart sätt. `xdm:fullName` är alltid att föredra. |
| `person.name.lastName` | Efternamn | Efternamn | string | string | Det sista segmentet i namnet i den skriftliga ordningen som oftast används på namnet. I många kulturer är det det ärvda familjenamnet, efternamnet, patronymiskt eller matronymiskt namn. Egenskaperna firstName och lastName har införts för att bibehålla kompatibiliteten med befintliga system som modellerar namn på ett förenklat, icke-semantiskt och icke-internationaliserbart sätt. `xdm:fullName` är alltid att föredra. |
| `person.name.middleName` | Mellannamn | Mellannamn | string | telefon | Mellannamn, alternativa namn eller ytterligare namn som anges mellan förnamnet och efternamnet. |
| `workAddress.city ` | Ort | Ort | string | string | Namnet på staden. |
| `workAddress.country` | Land | Land | string | string | Namnet på det statligt administrerade territoriet. Förutom `xdm:countryCode` är det ett friformsfält som kan ha landsnamnet på vilket språk som helst. |
| `workAddress.postalCode` | Postnummer | Postnummer | string | string | Postnumret för platsen. Postnummer är inte tillgängliga för alla länder. I vissa länder innehåller den endast en del av postnumret. |
| `workAddress.state` | Stat | Stat | string | string | Namnet på tillståndet för adressen. Det är ett frihandsfält. |
| `workAddress.street1` | Gatuadress 1 | Adress | string | text | Primär information om gatuminivå, lägenhetsnummer, gatunummer och gatunamn. |
| `workEmail.address` | Adress | E-postadress | string | e-post | Den tekniska adressen, till exempel `<name@domain.com>`, som den är vanlig definierad i RFC2822 och efterföljande standarder. |
| `workEmail.status` | Status | E-post pausad | string | boolesk | En indikation på möjligheten att använda e-postadressen. |
| `workPhone.number` | Nummer | Telefonnummer | string | telefon | Telefonnummer till arbetet. |

## Standardfältkopplingar för XDM-företagskonto

| [XDM Business Account](https://github.com/adobe/xdm/blob/master/docs/reference/mixins/account/account-details.schema.md) | XDM-visningsnamn | Marketo Engage visningsnamn | XDM-typ | Marketo Engage type | XDM-beskrivning |
|------------------- |---------------------------------- |--------------------------- |-------- |------------ |--------------- |
| `accountBillingAddress.city` | Ort | Ort | string | string | Namnet på den ort som används i faktureringsadressen. |
| `accountBillingAddress.country` | Land | Land | string | string | Namnet på det myndighetsadministrerade området som används i faktureringsadressen. Förutom `xdm:countryCode` är det ett friformsfält som kan ha landsnamnet på vilket språk som helst. |
| `accountBillingAddress.postalCode` | Postnummer | Adress Postnummer | string | string | Postnummer för platsen för faktureringsadressen. Postnummer är inte tillgängliga för alla länder. I vissa länder innehåller den endast en del av postnumret. |
| `accountBillingAddress.region` | Län | Adressregion | string | string | Faktureringsadressens region, län eller distrikt. |
| `accountBillingAddress.state` | Stat | Stat | string | string | Namnet på delstat för faktureringsadressen. Det är ett frihandsfält. |
| `accountBillingAddress.street1` | Gatuadress 1 | Gatuadress 1 | string | string | Primär gatuminivåinformation för faktureringsadressen, som vanligtvis ska innehålla lägenhetsnummer, gatunummer och gatunamn. |
| `accountName` | Namn | Namn | string | string | Företagets namn. I det här fältet tillåts upp till 255 tecken. |
| `accountOrganization.annualRevenue.amount` | Årlig intäkt | Årlig intäkt | tal | valuta | Organisationens beräknade årsomsättning. |
| `accountOrganization.industry` | Bransch | Bransch | string | string | Branschen tillskrivs organisationen. Det är ett frihandsfält och du bör använda ett strukturerat värde för frågor eller egenskapen `xdm:classifier`. |
| `accountOrganization.logoUrl` | URL för logotyp | URL för logotyp | string | string | Sökväg som ska kombineras med URL:en för en Salesforce-instans (till exempel `https://yourInstance.salesforce.com/`) för att generera en URL för att begära den profil för sociala nätverk som är associerad med kontot. Den genererade URL:en returnerar en HTTP-omdirigering (kod 302) till profilbilden för det sociala nätverket för kontot. |
| `accountOrganization.numberOfEmployees` | Antal anställda | Antal anställda | heltal | heltal | Antalet anställda i organisationen. |
| `accountOrganization.SICCode` | SNI-kod | SNI-kod | string | string | The Standard Industrial Classification (SIC) code, som är en fyrsiffrig kod som kategoriserar de branscher som företagen tillhör baserat på deras affärsverksamhet. |
| `accountOrganization.website` | Webbplatsens URL | Domännamn | string | string | URL till organisationens webbplats. |
| `accountPhone.number` | Ej tillämpligt | Telefonnummer till konto | string | string | Telefonnumret som är associerat med kontot. |
| `accountSourceType` | Ej tillämpligt | Source Type | string | string | Source-typ för kontot. |
