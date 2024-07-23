---
title: XDM-fältmappning
description: Granska fältmappningen mellan AEP XDM-schemat, Marketo Engage och Journey Optimizer B2B Edition.
source-git-commit: af287825508b2372f51aa8ea629cc6eda0a50b35
workflow-type: tm+mt
source-wordcount: '559'
ht-degree: 10%

---

# XDM-fältmappning

Dataöverföringstjänsten (DTS) i ansvarar för att synkronisera data från Adobe Experience Platform till Journey Optimizer B2B Edition. DTS förlitar sig på mappningar mellan Experience Platform XDM-schemafält och deras motsvarigheter i Marketo Engage.

## XDM Business Person - standardfältkopplingar

| XDM Business Person | Marketo Engage personvisningsnamn | AJO B2B-personvisningsnamn | XDM-typ | Marketo Type | XDM-beskrivning |
|------------------- |---------------------------------- |--------------------------- |-------- |------------ |--------------- |
| `workAddress.street1` | Adress | ? | string | text | Primär information om gatuminivå, lägenhetsnummer, gatunummer och gatunamn. |
| `workAddress.city ` | Ort | Ort | string | string | Namnet på staden. |
| `b2b.companyName` | Företagets namn | ? | string | string | Namnet på det företag som en affärsman är associerad med. |
| `workAddress.country` | Land | Land | string | string | Namnet på det statligt administrerade territoriet. Förutom `xdm:countryCode` är det här ett friformsfält som kan ha landsnamnet på vilket språk som helst. |
| `person.birthDate` | Födelsedatum | Födelsedatum | string | datum | Det fullständiga datumet en person föddes.  YYY-MM-DD |
| `workEmail.address` | E-postadress | E-postadress | string | e-post | Den tekniska adressen, till exempel, <name@domain.com>, är den som vanligen definieras i RFC2822 och efterföljande standarder. |
| `workEmail.status` | E-post pausad | E-post pausad | string | boolesk | En indikation på möjligheten att använda e-postadressen. |
| `faxPhone.number` | Faxnummer | ? | string | telefon | Faxnummer. |
| `person.name.firstName` | Förnamn | Förnamn | string | string | Det första segmentet i namnet i den skrivordning som oftast används på namnet. I många kulturer är det här det primära personliga namnet eller förnamnet. Egenskaperna firstName och lastName har införts för att bibehålla kompatibiliteten med befintliga system som modellerar namn på ett förenklat, icke-semantiskt och icke-internationaliserbart sätt. Det är alltid bättre att använda xdm:fullName. |
| `extendedWorkDetails.jobTitle` | Befattning | Befattning | string | string | Personens befattning. |
| `person.name.lastName` | Efternamn | Efternamn | string | string | Det sista segmentet i namnet i den skrivordning som oftast används på namnet. I många kulturer är detta det ärvda familjenamnet, efternamnet, patronymiskt eller matronymiskt namn. Egenskaperna firstName och lastName har införts för att bibehålla kompatibiliteten med befintliga system som modellerar namn på ett förenklat, icke-semantiskt och icke-internationaliserbart sätt. Det är alltid bättre att använda xdm:fullName. |
| `b2b.personStatus` | Leadkälla | ? | string | string | Fältregistrering av den aktuella marknadsförings-/försäljningsstatusen för personen. |
| `b2b.isMarketingSuspended` | Marknadsföring har pausats | ? | boolesk | boolesk | Anger om marknadsföringen har avbrutits för personen. |
| `b2b.marketingSuspendedCause` | Orsak till pausad marknadsföring | ? | string | string | Om marknadsföringen avbryts för personen anger denna egenskap anledningen till detta. |
| `person.name.middleName` | Mellannamn | ? | string | telefon | Mellannamn, alternativa namn eller ytterligare namn som anges mellan förnamnet och efternamnet. |
| `mobilePhone.number` | Mobiltelefon | Mobiltelefon | string | telefon | Mobiltelefonnummer. |
| `workPhone.number` | Telefonnummer | Telefonnummer | string | telefon | Telefonnummer till arbetet. |
| `workAddress.postalCode` | Postnummer | Postnummer | string | string | Postnumret för platsen. Postnummer är inte tillgängliga för alla länder. I vissa länder innehåller detta endast en del av postnumret. |
| `person.name.courtesyTitle` | Titel | ? | string | string | Vanligtvis en förkortning av en persontitel, en personlig ära eller hälsningsfras. Artikeltiteln används framför det fullständiga namnet eller efternamnet i öppningstexter. Till exempel herr, fröken eller dr. |
| `workAddress.state` | Stat | Stat | string | string | Statens namn. Det här är ett frihandsfält. |
| `consents.marketing.email.val` | Avprenumererad | Avprenumererad | string | boolesk | Om det är sant att prenumerera (till exempel värde = 1) anger du `consents.marketing.email.val` som (n). Om unsubscribed är false (till exempel value = 0) anger du consents.marketing.email.val som null. |
| `consents.marketing.email.reason` | Orsak till avprenumeration | Orsak till avprenumeration | string | string |  |
| `b2b.companyWebsite` | Webbplats | ? | string | url | Webbplats för det företag som en affärsman är kopplad till. |

