---
title: XDM-fält
description: Granska standardattributfälten som är synkroniserade mellan Adobe Experience Platform och Journey Optimizer B2B edition.
exl-id: 8c65fdec-e32d-4ba8-be7b-48522cc3dace
source-git-commit: 332c25305377398c2338d4b1d4a61b7fcf814232
workflow-type: tm+mt
source-wordcount: '1033'
ht-degree: 7%

---

# XDM-fält

Målgruppsdata lagras som attribut i både XDM Business Account- och XDM Business Person-klasserna. Data synkroniseras regelbundet mellan Adobe Experience Platform och Journey Optimizer B2B edition. I följande avsnitt visas standarduppsättningarna med attribut.

>[!TIP]
>
>Du kan modellera XDM Business Person- och XDM Business Account-klasser i en många-till-många-relation genom att använda klassen XDM Business Account Person Relation enligt beskrivningen i [Experience Platform XDM-dokumentationen](https://experienceleague.adobe.com/en/docs/experience-platform/xdm/tutorials/relationship-b2b).

## XDM Business Account Person Relation-attribut

| [Egenskap](https://github.com/adobe/xdm/blob/master/docs/reference/mixins/profile/b2b-person-details.schema.md) | Visningsnamn | Journey Optimizer B2B-visningsnamn | Datatyp | Beskrivning |
|------------------- |---------------------------------- |--------------------------- |-------- |--------------- |
| `personRoles` | Personroller | Roll | Strängarray | En array med roller som är associerade med personen på kontot, till exempel `owner, accountant, designer`. |

## XDM Business Person-attribut

>[!IMPORTANT]
>
>Attributet `workEmail.Address` krävs. Om det är tomt för en medlem i en kontomålgrupp är den personen inte införtärd och utelämnas från kontoresor och inköpsgrupper som refererar till målgruppen.

| [Egenskap](https://github.com/adobe/xdm/blob/master/docs/reference/mixins/profile/b2b-person-details.schema.md) | Visningsnamn | Journey Optimizer B2B-visningsnamn | Datatyp | Beskrivning |
|------------------- |---------------------------------- |--------------------------- |-------- |--------------- |
| `b2b.companyName` | Företagets namn | Företagets namn | Sträng | Namnet på det företag som en affärsman är associerad med. |
| `b2b.companyWebsite` | Företagets webbplats | Webbplats | Sträng | Webbplats för det företag som en affärsman är kopplad till. |
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

| [Egenskap](https://github.com/adobe/xdm/blob/master/docs/reference/mixins/account/account-details.schema.md) | Visningsnamn | Journey Optimizer B2B-visningsnamn | Datatyp | Beskrivning |
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

<!-- ## XDM Opportunity attributes

|[Property](https://github.com/adobe/xdm/blob/master/docs/reference/adobe/experience/marketo/opportunity-marketo.schema.md) |Display name |Journey Optimizer B2B display name |Data type |Description |
|------------------- |---------------------------------- |--------------------------- |-------- |--------------- |
|`opportunityName` | Opportunity Name   | ? |String  | Subject or descriptive name, such as the expected order or company name, for the opportunity. |
|`opportunityDescription` | Opportunity Description   | ?    |String  | Additional information to describe the opportunity, such as possible products to sell or past purchases from the customer. |
|`opportunityType` | Opportunity Type   | ?   | String | ?   |
|`opportunityStage` | Opportunity Stage   | ?   | String | Sales stage of the opportunity to aid the sales team in their efforts to win it.  |
|`fiscalQuarter` | Fiscal Quarter   | ?   | String | The fiscal quarter that the opportunity is targeted.   |
|`fiscalYear` | Fiscal Year   | ?   | String | The fiscal year that the opportunity is targeted.   |
|`fiscalCategory` | Fiscal Category   | ?   | String | ?   |
|`fiscalCategoryName` | Fiscal Category Name  | ?   | String | Forecast category name that is displayed in reports for a particular forecast category.   |
|`isClosed` | Closed Flag  | ?   | String | Flag that indicates if the opportunity is closed.   |
|`isWon` | Won Flag  | ?   | String | Flag that indicates if the opportunity is won.  |
|`probabilityPercentage` | Probability Percentage  | ?   | String | Likelihood of closing the opportunity, stated as a percentage.  |
|`opportunityAmount.amount` | Opportunity Amount  | ?   | String | Estimated total sale amount for the opportunity.   |
|`expectedRevenue.amount` | Expected Revenue  | ?   | String | Calculated revenue based on the Amount and Probability.   |
|`opportunityQuantity` | Opportunity Quantity  | ?   | String | Total of all quantity field values for all products in the related Products list for the opportunity.   |
|`expectedCloseDate` | Expected Close Date  | ?   | String | Expected date of closure for the opportunity.   |
|`lastActivityDate` | Last Activity Date  | ?   | String | Last activity date for the opportunity.  |
|`leadSource` | Lead Source  | ?   | String | Source of the opportunity, such as Advertisement, Partner, or Web.   |
|`nextStep` | Next Step  | ?   | String | Description of the next task for closing the opportunity.   |
-->
