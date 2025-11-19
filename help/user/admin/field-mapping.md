---
title: XDM-fält
description: Granska standardattributfälten som är synkroniserade mellan Adobe Experience Platform och Journey Optimizer B2B edition.
feature: Data Management, Integrations
role: User
exl-id: 8c65fdec-e32d-4ba8-be7b-48522cc3dace
source-git-commit: de7f5620556a48fe6f12ed1c70e925e11ec770f1
workflow-type: tm+mt
source-wordcount: '1153'
ht-degree: 6%

---

# XDM-fält

Målgruppsdata lagras som attribut i både XDM Business Account- och XDM Business Person-klasserna. Data synkroniseras regelbundet mellan Adobe Experience Platform och Journey Optimizer B2B edition. I följande avsnitt visas standarduppsättningarna med attribut.

>[!TIP]
>
>Du kan modellera XDM Business Person- och XDM Business Account-klasser i en många-till-många-relation genom att använda klassen XDM Business Account Person Relation enligt beskrivningen i [Experience Platform XDM-dokumentationen](https://experienceleague.adobe.com/en/docs/experience-platform/xdm/tutorials/relationship-b2b){target="_blank"}.

>[!NOTE]
>Data Mirror och relationsscheman är tillgängliga för innehavare av Adobe Journey Optimizer Orchestrated-kampanjlicenser. De finns också som en begränsad version för Customer Journey Analytics-användare, beroende på licens- och funktionsinställningarna. Kontakta din Adobe-representant för att få åtkomst. Relationsscheman finns också i en begränsad version för Adobe Journey Optimizer B2B edition.
>


## XDM Business Account Person Relation-attribut

| [Egenskap](https://github.com/adobe/xdm/blob/master/docs/reference/mixins/profile/b2b-person-details.schema.md){target="_blank"} | Visningsnamn | Journey Optimizer B2B-visningsnamn | Datatyp | Beskrivning |
|------------------- |---------------------------------- |--------------------------- |-------- |--------------- |
| `personRoles` | Personroller | Roll | Strängarray | En array med roller som är associerade med personen på kontot, till exempel `owner, accountant, designer`. |

## XDM Business Person-attribut

>[!IMPORTANT]
>
>E-postadressattributet är obligatoriskt och måste fyllas i för att funktionen ska fungera korrekt. Som standard använder systemet `workEmail.Address`. Om du tänker använda ett annat attribut kontaktar du Adobe Support innan du publicerar några resor för att säkerställa korrekt konfiguration.<br/>
>
>Kontrollera att e-postattributet inte är null eftersom detta kan påverka datasynkronisering och processer längre fram i kedjan.
><ul><li>Om e-postattributet är null i realtid, CDP B2B, och personen finns i Journey Optimizer B2B edition, skrivs attributet i över i Journey Optimizer B2B edition med ett null-värde under synkronisering. Därefter behålls det som null i Marketo Engage.<li>Om e-postattributet är null i realtid CDP B2B och personen inte finns i Journey Optimizer B2B edition synkroniseras inte personposten.<ul/>

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

<!-- ## XDM Business Opportunity attributes

Additionally, opportunity data is stored as attributes in the XDM Business Opportunity class, which can be associated with the XDM Business Account class through a many-to-one relationship, as described in the [Exerience Platform documentation](https://experienceleague.adobe.com/en/docs/experience-platform/xdm/tutorials/relationship-b2b#relationship-field){target="_blank"}.

|[Property](https://github.com/adobe/xdm/blob/master/docs/reference/adobe/experience/marketo/opportunity-marketo.schema.md){target="_blank"} |Display name |Journey Optimizer B2B display name |Data type |Description |
|------------------- |---------------------------------- |--------------------------- |-------- |--------------- |
|`expectedCloseDate` | Expected Close Date  | Expected opportunity close date   | String | Expected date of closure for the opportunity.   |
|`expectedRevenue.amount` | Expected Revenue  | Total opportunity expected revenue   | String | Calculated revenue based on the Amount and Probability.   |
|`fiscalQuarter` | Fiscal Quarter   | Opportunity fiscal quarter  | String | The targeted fiscal quarter for the opportunity.   |
|`fiscalYear` | Fiscal Year   | Opportunity fiscal year   | String | The targeted fiscal year for the opportunity.   |
|`forecastCategory`|Forecast Category | Opportunity Forecast category | String | Forecast Category determined by the opportunity Stage value. |
|`forecastCategoryName`|Forecast Category Name | Opportunity forecast category name | String | Forecast category name that is displayed in reports for a particular forecast category. |
|`isClosed` | Closed Flag  | Opportunity closed   | String | Flag that indicates if the opportunity is closed.   |
|`isWon` | Won Flag  | Opportunity won   | String | Flag that indicates if the opportunity is won.  |
|`lastActivityDate` | Last Activity Date  | Last activity date   | String | Last activity date for the opportunity.  |
|`leadSource` | Lead Source  | Lead source   | String | Source of the opportunity, such as Advertisement, Partner, or Web.   |
|`nextStep` | Next Step  | Opportunity next step   | String | Description of the next task for closing the opportunity.   |
|`opportunityAmount.amount` | Opportunity Amount  | Total Opportunity Amount | String | Estimated total sale amount for the opportunity.   |
|`opportunityDescription` | Opportunity Description   | Opportunity description  |String  | Additional information to describe the opportunity, such as possible products to sell or past purchases from the customer. |
|`opportunityName` | Opportunity Name   | Opportunity name |String  | Subject or descriptive name, such as the expected order or company name, for the opportunity. |
|`opportunityQuantity` | Opportunity Quantity  | Opportunity quantity   | String | Total of all quantity field values for all products in the related Products list for the opportunity.   |
|`opportunityStage` | Opportunity Stage   | Opportunity stage   | String | Sales stage of the opportunity to aid the sales team in their efforts to win it.  |
|`opportunityType` | Opportunity Type   | Opportunity type   | String | Type assigned to the opportunity, such as _Existing Business_ or _New Business_  |
|`probabilityPercentage` | Probability Percentage  | Opportunity probability percentage  | String | Likelihood of closing the opportunity, stated as a percentage.  |
 -->