---
title: B2B-namnutrymmen och scheman
description: Konfigurera Experience Platform B2B-namnutrymmen och scheman för Journey Optimizer B2B edition med hjälp av Postman autogenereringsverktyg.
feature: Setup, Data Management
role: Admin
source-git-commit: 023e44e1ad2baed2a5586d95a26ef8693020667a
workflow-type: tm+mt
source-wordcount: '1010'
ht-degree: 0%

---

# B2B-namnutrymmen och scheman

I Journey Optimizer B2B edition-inställningarna för den förenklade arkitekturen ingår konfiguration av Experience Platform namnutrymmen och scheman som används med B2B-källor. Postman automatiseringsverktyg krävs för att skapa B2B-namnutrymmen och scheman.

>[!AVAILABILITY]
>
>- Du måste ha tillgång till [Adobe Real-Time Customer Data Platform B2B edition](https://experienceleague.adobe.com/en/docs/experience-platform/rtcdp/intro/rtcdpb2b-intro/b2b-overview){target="_blank"} för att dina B2B-scheman ska vara kvalificerade i [kundprofilen i realtid](https://experienceleague.adobe.com/en/docs/experience-platform/profile/home){target="_blank"}.
>
>- Experience Platform B2B-entiteter måste använda de standardrelationer som beskrivs i [B2B-namnutrymmen och schemaguiden](https://experienceleague.adobe.com/en/docs/experience-platform/rtcdp/schemas/b2b){target="_blank"}.

Granska följande information om den underliggande inställningen för de namnutrymmen och scheman som ska användas med B2B-källor. Här finns också information om hur du konfigurerar Postman automatiseringsverktyg, vilket krävs för att generera B2B-namnutrymmen och scheman.

## Konfigurera verktyget för automatisk generering

Mer information om krav och detaljerad information om hur du konfigurerar [!DNL Postman]-miljön så att den stöder B2B-namnområdet och automatisk schemagenerering finns i följande resurser.

- Hämta samlingen och miljön för automatisk generering av namnområde och schema från [GitHub-databasen](https://github.com/adobe/experience-platform-postman-samples/tree/master/Postman%20Collections/CDP%20Namespaces%20and%20Schemas%20Utility){target="_blank"}.
- Mer information om hur du använder Experience Platform API:er, inklusive information om hur du samlar in värden för obligatoriska huvuden och läser API-anrop från exempel, finns i [_Komma igång med Adobe Experience Platform API:er_](https://experienceleague.adobe.com/en/docs/experience-platform/landing/platform-apis/api-guide){target="_blank"}.
- Mer information om hur du genererar autentiseringsuppgifter för Experience Platform API:er finns i [_Autentisera och få åtkomst till Experience Platform API:er_](https://experienceleague.adobe.com/en/docs/experience-platform/landing/platform-apis/api-authentication){target="_blank"}.
- Mer information om hur du konfigurerar [!DNL Postman] för Experience Platform API:er finns i [_[!DNL Postman] i Adobe Experience Platform _](https://experienceleague.adobe.com/en/docs/experience-platform/landing/platform-apis/postman){target="_blank"}.

### Miljövärden

Med en Experience Platform-utvecklarkonsol och [!DNL Postman] konfigurerad kan du använda lämpliga miljövärden i din [!DNL Postman] -miljö. Följande tabell innehåller exempelvärden och ytterligare information om hur du fyller i din [!DNL Postman]-miljö:

| Variabel | Beskrivning | Exempel |
| --- | --- | --- |
| `CLIENT_SECRET` | En unik identifierare som används för att generera `{ACCESS_TOKEN}`. | `{CLIENT_SECRET}` |
| `API_KEY` | En unik identifierare som används för att autentisera anrop till Experience Platform API:er. | `c8d9a2f5c1e03789bd22e8efdd1bdc1b` |
| `ACCESS_TOKEN` | Den auktoriseringstoken som krävs för att slutföra anrop till Experience Platform API:er. | `Bearer {ACCESS_TOKEN}` |
| `META_SCOPE` | Med avseende på [!DNL Journey Optimizer B2B] och [!DNL Marketo Engage] är det här värdet fast och alltid inställt på: `ent_dataservices_sdk`. | `ent_dataservices_sdk` |
| `CONTAINER_ID` | Behållaren `global` innehåller alla standardklasser som tillhandahålls av Adobe- och Experience Platform-partners, schemafältgrupper, datatyper och scheman. Med avseende på [!DNL Marketo] är det här värdet fast och ställs alltid in på `global`. | `global` |
| `TECHNICAL_ACCOUNT_ID` | En autentiseringsuppgift som används för att integrera med Adobe I/O. | `D42AEVJZTTJC6LZADUBVPA15@techacct.adobe.com` |
| `IMS` | Identity Management System (IMS) utgör ramverket för autentisering till Adobes tjänster. Med avseende på [!DNL Journey Optimizer B2B] och [!DNL Marketo Engage] är det här värdet fast och alltid inställt på: `ims-na1.adobelogin.com`. | `ims-na1.adobelogin.com` |
| `IMS_ORG` | En företagsenhet som kan äga eller licensiera produkter och tjänster och ge åtkomst till sina medlemmar. | `ABCEH0D9KX6A7WA7ATQE0TE@adobeOrg` |
| `SANDBOX_NAME` | Namnet på den virtuella sandlådepartition som du använder. | `prod` |
| `TENANT_ID` | Ett ID som används för att se till att de resurser du skapar namnges korrekt och finns i din organisation. | `b2bcdpproductiontest` |
| `PLATFORM_URL` | URL-slutpunkten som du gör API-anrop till. Det här värdet är fast och är alltid inställt på: `http://platform.adobe.io/`. | `http://platform.adobe.io/` |

{style="table-layout:auto"}

### Kör skripten

När miljövärdena är på plats använder du gränssnittet [!DNL Postman] för att köra skriptet för att skapa namnutrymmen och scheman. Markera rotmappen för verktyget för autogenerering och välj sedan **[!DNL Run]** i den övre rubriken.

![Rotmappen för generatorn för namnutrymmen och scheman i Postman-gränssnittet](./assets/namespaces-schemas-postman-root-folder.png){width="500" zoomable="yes"}

Gränssnittet [!DNL Runner] visas. Se till att alla kryssrutor är markerade och välj sedan **[!DNL Run Namespaces and Schemas Autogeneration Utility]**.

![Postman-gränssnitt med flera begäranden i samlingen Namespace och Schemas markerade.](./assets/namespaces-schemas-postman-run-generator.png){width="800" zoomable="yes"}

En lyckad begäran skapar de nödvändiga B2B-namnutrymmena och schemana.

## B2B-namnutrymmen

Identitetsnamnutrymmen är en komponent i Experience Platform [[!DNL Identity Service]](https://experienceleague.adobe.com/en/docs/experience-platform/identity/home){target="_blank"} som kan skilja kontexten för en identitet åt. En fullständigt kvalificerad identitet innehåller ett identitetsvärde och ett namnutrymme. Mer information finns i [översikten över namnutrymmen](https://experienceleague.adobe.com/en/docs/experience-platform/identity/features/namespaces){target="_blank"}.

B2B-namnutrymmen används i entitetens primära identitet.

| Profilnamn | Identitetssymbol | Identitetstyp |
| --- | --- | --- |
| B2B-person | `b2b_person` | `CROSS_DEVICE` |
| B2B-konto | `b2b_account` | `B2B_ACCOUNT` |
| B2B-säljprojekt | `b2b_opportunity` | `B2B_OPPORTUNITY` |
| Personrelation för B2B-säljprojekt | `b2b_opportunity_person_relation` | `B2B_OPPORTUNITY_PERSON` |
| B2B-kampanj | `b2b_campaign` | `B2B_CAMPAIGN` |
| B2B-kampanjmedlem | `b2b_campaign_member` | `B2B_CAMPAIGN_MEMBER` |
| B2B-marknadsföringslista | `b2b_marketing_list` | `B2B_MARKETING_LIST` |
| B2B Marketing List-medlem | `b2b_marketing_list_member` | `B2B_MARKETING_LIST_MEMBER` |
| B2B-konto, personrelation | `b2b_account_person_relation` | `B2B_ACCOUNT_PERSON` |

{style="table-layout:auto"}

## B2B-scheman

Experience Platform använder scheman för att beskriva datastrukturen på ett konsekvent och återanvändbart sätt. Genom att definiera data på ett enhetligt sätt i olika system blir det enklare att behålla sin betydelse och därmed få värde av data.

Innan Experience Platform kan importera data måste det finnas ett schema som beskriver datastrukturen och innehåller begränsningar för den typ av data som kan finnas i varje fält. Scheman består av en basklass och noll eller flera schemafältgrupper.

Mer information om schemakompositionsmodellen, inklusive designprinciper och bästa praxis, finns i [_Grundläggande om schemakomposition_](https://experienceleague.adobe.com/en/docs/experience-platform/xdm/schema/composition){target="_blank"}.

+++ B2B-konto

<table>
    <tr>
        <td style="width: 30%;">Basklass</td>
        <td style="width: 70%;"><a href="https://experienceleague.adobe.com/en/docs/experience-platform/xdm/classes/b2b/business-account" target="_blank">XDM Business Account</a></td>
    </tr>
    <tr>
        <td>Fältgrupper</td>
        <td>XDM Business Account Details</td>
    </tr>
    <tr>
        <td>[!DNL Profile] i schema</td>
        <td>Aktiverad</td>
    </tr>
    <tr>
        <td>Primär identitet</td>
        <td><code>accountKey.sourceKey</code> i basklassen</td>
    </tr>
    <tr>
        <td>Namnutrymme för primär identitet</td>
        <td>B2B-konto</td>
    </tr>
    <tr>
        <td>Sekundär identitet</td>
        <td><code>extSourceSystemAudit.externalKey.sourceKey</code> i basklassen</td>
    </tr>
    <tr>
        <td>Namnutrymme för sekundär identitet</td>
        <td>B2B-konto</td>
    </tr>
    <tr>
        <td>Relation</td>
        <td><ul><li><code>accountParentKey.sourceKey</code> i fältgruppen XDM Business Account Details</li><li>Egenskapen Destination: <code>/accountKey/sourceKey</code></li><li>Typ: en-till-en</li><li>Referensschema: B2B-konto</li><li>Namnutrymme: B2B-konto</li></ul> </td>
    </tr>
</table>

+++

+++ B2B-person

<table>
    <tr>
        <td style="width: 30%;">Basklass</td>
        <td style="width: 70%;"><a href="https://experienceleague.adobe.com/en/docs/experience-platform/xdm/classes/individual-profile">Individuell XDM-profil</a>{target="_blank"}</td>
    </tr>
    <tr>
        <td>Fältgrupper</td>
        <td><ul><li>Information om XDM Business Person</li><li>XDM Business Person Components</li><li>IdentityMap</li><li>Information om samtycke och inställningar</li></ul> </td>
    </tr>
    <tr>
        <td>[!DNL Profile] i schema</td>
        <td>Aktiverad</td>
    </tr>
    <tr>
        <td>Primär identitet</td>
        <td><code>b2b.personKey.sourceKey</code> i fältgruppen XDM Business Person Details</td>
    </tr>
    <tr>
        <td>Namnutrymme för primär identitet</td>
        <td>B2B-person</td>
    </tr>
    <tr>
        <td>Sekundär identitet</td>
        <td><ol><li><code>extSourceSystemAudit.externalKey.sourceKey</code> fältgruppen XDM Business Person Details</li><li><code>workEmail.address</code> fältgruppen XDM Business Person Details</li></ol></td>
    </tr>
    <tr>
        <td>Namnutrymme för sekundär identitet</td>
        <td><ol><li>B2B-person</li><li>E-post</li></ol></td>
    </tr>
    <tr>
        <td>Relation</td>
        <td><ul><li><code>personComponents.sourceAccountKey.sourceKey</code> fältgruppen XDM Business Person Components</li><li>Typ: Flera till ett</li><li>Referensschema: B2B-konto</li><li>Namnutrymme: B2B-konto</li><li>Destinationsegenskap: accountKey.sourceKey</li><li>Relationsnamn från aktuellt schema: Konto</li><li>Relationsnamn från referensschema: Personer</li></ul> </td>
    </tr>
</table>

+++

<!--

+++B2B Opportunity

<table>
    <tr>
        <td style="width: 30%;">Base class</td>
        <td style="width: 70%;"><a href="https://experienceleague.adobe.com/en/docs/experience-platform/xdm/classes/b2b/business-opportunity">XDM Business Opportunity</a>{target="_blank"}</td>
    </tr>
    <tr>
        <td>Field groups</td>
        <td>XDM Business Opportunity Details</td>
    </tr>
    <tr>
        <td>[!DNL Profile] in Schema</td>
        <td>Enabled</td>
    </tr>
    <tr>
        <td>Primary identity</td>
        <td><code>opportunityKey.sourceKey</code> in the base class</td>
    </tr>
    <tr>
        <td>Primary identity namespace</td>
        <td>B2B Opportunity</td>
    </tr>
    <tr>
        <td>Secondary identity</td>
        <td><code>extSourceSystemAudit.externalKey.sourceKey</code> in the base class</td>
    </tr>
    </tr>
    <tr>
        <td>Secondary identity namespace</td>
        <td>B2B Opportunity</td>
    </tr>
    <tr>
        <td>Relationship</td>
        <td><ul><li><code>accountKey.sourceKey</code> in the base class</li><li>Type: Many-to-one</li><li>Reference Schema: B2B Account</li><li>Namespace: B2B Account</li><li>Destination property: <code>accountKey.sourceKey</code></li><li>Relationship name from current schema: Account</li><li>Relationship name from reference schema: Opportunities</li></ul></td>
    </tr>
</table>

+++

+++B2B Opportunity Person Relation

<table>
    <tr>
        <td style="width: 30%;">Base class</td>
        <td style="width: 70%;"><a href="https://experienceleague.adobe.com/en/docs/experience-platform/xdm/classes/b2b/business-opportunity-person-relation">XDM Business Opportunity Person Relation</a>{target="_blank"}</td>
    </tr>
    <tr>
        <td>Field groups</td>
        <td>None</td>
    </tr>
    <tr>
        <td>[!DNL Profile] in Schema</td>
        <td>Enabled</td>
    </tr>
    <tr>
        <td>Primary identity</td>
        <td><code>opportunityPersonKey.sourceKey</code> in the base class</td>
    </tr>
    <tr>
        <td>Primary identity namespace</td>
        <td>B2B Opportunity Person Relation</td>
    </tr>
    <tr>
        <td>Secondary identity</td>
        <td>None</td>
    </tr>
    </tr>
    <tr>
        <td>Secondary identity namespace</td>
        <td>None</td>
    </tr>
    <tr>
        <td>Relationship</td>
        <td> **First relationship**<ul><li><code>personKey.sourceKey</code> in the base class</li><li>Type: Many-to-one</li><li>Reference Schema: B2B Person</li><li>Namespace: B2B Person</li><li>Destination property: <code>b2b.personKey.sourceKey</code></li><li>Relationship name from current schema: Person</li><li>Relationship name from reference schema: Opportunities</li></ul>**Second relationship**<ul><li><code>opportunityKey.sourceKey</code> in the base class</li><li>Type: Many-to-one</li><li>Reference Schema: B2B Opportunity </li><li>Namespace: B2B Opportunity </li><li>Destination property: <code>opportunityKey.sourceKey</code></li><li>Relationship name from current schema: Opportunity</li><li>Relationship name from reference schema: People</li></ul> </td>
    </tr>
</table>


+++

+++B2B Campaign

<table>
    <tr>
        <td style="width: 30%;">Base class</td>
        <td style="width: 70%;"><a href="https://experienceleague.adobe.com/en/docs/experience-platform/xdm/classes/b2b/business-campaign">XDM Business Campaign</a>{target="_blank"}</td>
    </tr>
    <tr>
        <td>Field groups</td>
        <td>XDM Business Campaign Details</td>
    </tr>
    <tr>
        <td>[!DNL Profile] in Schema</td>
        <td>Enabled</td>
    </tr>
    <tr>
        <td>Primary identity</td>
        <td><code>campaignKey.sourceKey</code> in the base class</td>
    </tr>
    <tr>
        <td>Primary identity namespace</td>
        <td>B2B Campaign</td>
    </tr>
    <tr>
        <td>Secondary identity</td>
        <td>None</td>
    </tr>
    </tr>
    <tr>
        <td>Secondary identity namespace</td>
        <td>None</td>
    </tr>
    <tr>
        <td>Relationship</td>
        <td>None</td>
    </tr>
</table>

+++

+++B2B Campaign Member

<table>
    <tr>
        <td style="width: 30%;">Base class</td>
        <td style="width: 70%;"><a href="https://experienceleague.adobe.com/en/docs/experience-platform/xdm/classes/b2b/business-campaign-members">XDM Business Campaign Members</a>{target="_blank"}</td>
    </tr>
    <tr>
        <td>Field groups</td>
        <td>XDM Business Campaign Member Details</td>
    </tr>
    <tr>
        <td>[!DNL Profile] in Schema</td>
        <td>Enabled</td>
    </tr>
    <tr>
        <td>Primary identity</td>
        <td><code>campaignMemberKey.sourceKey</code> in the base class</td>
    </tr>
    <tr>
        <td>Primary identity namespace</td>
        <td>B2B Campaign Member</td>
    </tr>
    <tr>
        <td>Secondary identity</td>
        <td>None</td>
    </tr>
    </tr>
    <tr>
        <td>Secondary identity namespace</td>
        <td>None</td>
    </tr>
    <tr>
        <td>Relationship</td>
        <td>**First relationship**<ul><li><code>personKey.sourceKey</code> in the base class</li><li>Type: Many-to-one</li><li>Reference Schema: B2B Person</li><li>Namespace: B2B Person</li><li>Destination property: <code>b2b.personKey.sourceKey</code></li><li>Relationship name from current schema: Person</li><li>Relationship name from reference schema: Campaigns</li></ul>**Second relationship**<ul><li><code>campaignKey.sourceKey</code> in the base class</li><li>Type: Many-to-one</li><li>Reference Schema: B2B Campaign</li><li>Namespace: B2B Campaign</li><li>Destination property: <code>campaignKey.sourceKey</code></li><li>Relationship name from current schema: Campaign</li><li>Relationship name from reference schema: People</li></ul></td>
    </tr>
</table>

+++B2B Marketing List

<table>
    <tr>
        <td style="width: 30%;">Base class</td>
        <td style="width: 70%;"><a href="https://experienceleague.adobe.com/en/docs/experience-platform/xdm/classes/b2b/business-marketing-list">XDM Business Marketing List</a>{target="_blank"}</td>
    </tr>
    <tr>
        <td>Field groups</td>
        <td>None</td>
    </tr>
    <tr>
        <td>[!DNL Profile] in Schema</td>
        <td>Enabled</td>
    </tr>
    <tr>
        <td>Primary identity</td>
        <td><code>marketingListKey.sourceKey</code> in the base class</td>
    </tr>
    <tr>
        <td>Primary identity namespace</td>
        <td>B2B Marketing List</td>
    </tr>
    <tr>
        <td>Secondary identity</td>
        <td>None</td>
    </tr>
    </tr>
    <tr>
        <td>Secondary identity namespace</td>
        <td>None</td>
    </tr>
    <tr>
        <td>Relationship</td>
        <td>None</td>
    </tr>
</table>

>[!NOTE]
>
>Static List in [!UICONTROL Marketo Engage] is not synced from Salesforce and therefore does not have a secondary identity.

+++

+++B2B Marketing List Member

<table>
    <tr>
        <td style="width: 30%;">Base class</td>
        <td style="width: 70%;"><a href="https://experienceleague.adobe.com/en/docs/experience-platform/xdm/classes/b2b/business-marketing-list-members">XDM Business Marketing List Members</a>{target="_blank"}</td>
    </tr>
    <tr>
        <td>Field groups</td>
        <td>None</td>
    </tr>
    <tr>
        <td>[!DNL Profile] in Schema</td>
        <td>Enabled</td>
    </tr>
    <tr>
        <td>Primary identity</td>
        <td><code>marketingListMemberKey.sourceKey</code> in the base class</td>
    </tr>
    <tr>
        <td>Primary identity namespace</td>
        <td>B2B Marketing List Member</td>
    </tr>
    <tr>
        <td>Secondary identity</td>
        <td>None</td>
    </tr>
    </tr>
    <tr>
        <td>Secondary identity namespace</td>
        <td>None</td>
    </tr>
    <tr>
        <td>Relationship</td>
        <td>**First relationship**<ul><li><code>personKey.sourceKey</code> in the base class</li><li>Type: Many-to-one</li><li>Reference Schema: B2B Person</li><li>Namespace: B2B Person</li><li>Destination property: <code>b2b.personKey.sourceKey</code></li><li>Relationship name from current schema: Person</li><li>Relationship name from reference schema: Marketing Lists</li></ul>**Second relationship**<ul><li><code>marketingListKey.sourceKey</code> in the base class</li><li>Type: Many-to-one</li><li>Reference Schema: B2B Marketing List</li><li>Namespace: B2B Marketing List</li><li>Destination property: <code>marketingListKey.sourceKey</code></li><li>Relationship name from current schema: Marketing List</li><li>Relationship name from reference schema: People</li></ul></td>
    </tr>
</table>

>[!NOTE]
>
>Static List member in [!UICONTROL Marketo Engage] is not synced from Salesforce and therefore does not have a secondary identity.

+++

+++B2B Account Person Relation

<table>
    <tr>
        <td style="width: 30%;">Base class</td>
        <td style="width: 70%;"><a href="https://experienceleague.adobe.com/en/docs/experience-platform/xdm/classes/b2b/business-account-person-relation">XDM Business Account Person Relation</a>{target="_blank"}</td>
    </tr>
    <tr>
        <td>Field groups</td>
        <td>Identity Map</td>
    </tr>
    <tr>
        <td>[!DNL Profile] in Schema</td>
        <td>Enabled</td>
    </tr>
    <tr>
        <td>Primary identity</td>
        <td><code>accountPersonKey.sourceKey</code> in the base class</td>
    </tr>
    <tr>
        <td>Primary identity namespace</td>
        <td>B2B Account Person Relation</td>
    </tr>
    <tr>
        <td>Secondary identity</td>
        <td>None</td>
    </tr>
    </tr>
    <tr>
        <td>Secondary identity namespace</td>
        <td>None</td>
    </tr>
    <tr>
        <td>Relationship</td>
        <td>**First relationship**<ul><li><code>personKey.sourceKey</code> in the base class</li><li>Type: Many-to-one</li><li>Reference Schema: B2B Person</li><li>Namespace: B2B Person</li><li>Destination property: <code>b2b.personKey.sourceKey</code></li><li>Relationship name from current schema: People</li><li>Relationship name from reference schema: Account</li></ul>**Second relationship**<ul><li><code>accountKey.sourceKey</code> in the base class</li><li>Type: Many-to-one</li><li>Reference Schema: B2B Account</li><li>Namespace: B2B Account</li><li>Destination property: <code>accountKey.sourceKey</code></li><li>Relationship name from current schema: Account</li><li>Relationship name from reference schema: People</li></ul></td>
    </tr>
</table>

+++

-->
