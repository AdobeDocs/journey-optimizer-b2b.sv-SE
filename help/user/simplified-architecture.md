---
title: Förenklad arkitekturkonfiguration
description: Installera Journey Optimizer B2B edition på den förenklade arkitekturen. Konfigurera XDM-scheman, e-post-/SMS-kanaler, Marketo Engage reseåtgärder och användare.
feature: Setup, Administration
role: Admin, Data Engineer
hide: true
hidefromtoc: true
source-git-commit: d2f33c30dba1ce44842f41bd2dbbfada24a8ff9c
workflow-type: tm+mt
source-wordcount: '1292'
ht-degree: 1%

---

# Förenklad arkitekturkonfiguration

Adobe Journey Optimizer B2B edition finns nu i en förenklad arkitektur. Med den här uppdaterade arkitekturen finns Journey Optimizer B2B edition och Marketo Engage inte längre i samma system och datalager. Journey Optimizer B2B edition tar endast emot data från Adobe Experience Platform. Men det fortsätter att förlita sig på Marketo Engage-berättiganden och vissa konfigurationsfunktioner för att etablera och konfigurera systemet.

Den förenklade arkitekturen utgör grunden för nya funktioner i Adobe Journey Optimizer B2B edition:

* **Gör era data enhetliga och skalbara enkelt:** Den nya plattformen har stöd för komplexa datamodeller, inklusive anpassade objekt, inköpsgrupper och kontohändelser. 

* **Koppla ihop flera Adobe Marketo Engage-instanser:** Hantera och förena data från flera Adobe Marketo Engage-miljöer på ett och samma ställe.

* **Skyddar dina data:** Avancerade sekretess- och säkerhetsfunktioner som skyddar din kundinformation. (_Kommer snart_)

* **Skapat för framtiden:** Den här uppgraderingen konfigurerar dig för kontinuerliga förbättringar och innovation. 

För miljöer som har etablerats för den här arkitekturen använder du följande riktlinjer för konfiguration.

## Namnutrymmen och scheman

En översikt finns i [B2B-namnutrymmen och scheman](https://experienceleague.adobe.com/en/docs/experience-platform/sources/connectors/adobe-applications/marketo/marketo-namespaces) i Experience Platform-dokumentationen.

### Miljöinställningar

Konfigurera en Postman-miljö för att stödja verktyget för automatisk generering av B2B-namnrymder och scheman.

* Du kan hämta samlingen och miljön för automatisk generering av namnområde och scheman från [GitHub-databasen](https://github.com/adobe/experience-platform-postman-samples/tree/master/Postman%20Collections/CDP%20Namespaces%20and%20Schemas%20Utility).

* Mer information om hur du använder Experience Platform API:er, inklusive information om hur du samlar in värden för obligatoriska huvuden och läser exempel-API-anrop, finns i handboken [Komma igång med Experience Platform API:er](https://experienceleague.adobe.com/en/docs/experience-platform/landing/platform-apis/api-guide).

* Mer information om hur du genererar autentiseringsuppgifter för Experience Platform API:er finns i självstudiekursen om [autentisering och åtkomst av Experience Platform API:er](https://experienceleague.adobe.com/en/docs/experience-platform/landing/platform-apis/api-authentication).

* Mer information om hur du konfigurerar Postman för Experience Platform API:er finns i de detaljerade stegen i [Postman i Adobe Experience Platform](https://experienceleague.adobe.com/en/docs/experience-platform/landing/platform-apis/postman).

Med en utvecklarkonsol från Experience Platform och Postman kan du nu börja använda rätt miljövärden i din Postman-miljö.

### Kör skripten

Med Postman samlings- och miljöinställningar kan du köra skriptet via Postman gränssnitt.

I Postman-gränssnittet väljer du rotmappen för verktyget för autogenerering och sedan **Kör** i den övre rubriken.

När Runner-gränssnittet visas kontrollerar du att alla kryssrutor är markerade och väljer sedan **Kör automatisk generering av namnutrymmen och scheman**.

En lyckad begäran skapar de namnutrymmen och scheman som krävs för B2B.

## Val av XDM-fält

Du kan hantera XDM-fälten som är tillgängliga i hela programmet i användargränssnittet för Journey Optimizer B2B edition. Dessa fält hjälper dig att effektivisera instansen genom att endast visa fält som är relevanta för att skapa **_resor_**, **_köpgrupper_** eller **_e-postpersonaliseringar_**.

### XDM-klasser

#### Standardklasser

Använd stegen nedan för att definiera fält för standard-XDM-klasser:

1. Navigera till **[!UICONTROL Administration]>[!UICONTROL Configurations]**.

1. Välj **[!UICONTROL XDM Classes]** på navigeringspanelen.

1. Välj fliken **[!UICONTROL Standard]** för att visa tillgängliga XDM-klasser:

   * Individuell XDM-profil

   * XDM Business Account

#### Hanterade fält

Ange vilka fält som är tillgängliga i hela programmet.

1. Klicka på ikonen _Mer meny_ (**..**) och välj **[!UICONTROL Edit managed fields]**.

1. Granska listan över tillgängliga fält (klicka på ikonen _Information_ för att se om det finns fältmetadata).

1. Markera de fält som du vill ta med och rensa markeringar för de fält som du inte behöver.

1. Använd skjutreglaget **[!UICONTROL Only show selected fields]** för att granska dina val.

1. Klicka på **[!UICONTROL Save]**.

#### Uppdateringsbara fält

Välj vilka fält som kan ändras via **[!UICONTROL Update Account Profile]** eller **[!UICONTROL Update Person Profile]** reseåtgärder.

1. Klicka på ikonen _Mer meny_ (**..**) och välj **[!UICONTROL Edit updatable fields]**.

1. Välj **[!UICONTROL Schema]** och sedan **[!UICONTROL Dataset]**.

   Dessa scheman och datauppsättningar tillhandahålls av din organisation.

1. Granska listan över uppdateringsbara fält (klicka på ikonen _Information_ för metadata).

   Endast hanterade fält kan redigeras.

1. Markera de fält som du vill göra tillgängliga för uppdatering från resor.

1. Klicka på **Spara**

### Relationsscheman

Välj [relationsscheman](https://experienceleague.adobe.com/en/docs/experience-platform/xdm/schema/relational) som ska användas i **_resebeslut_** och **_personalisering_**. För närvarande är dessa scheman avsedda för användning av anpassade objekt. I framtiden kan relationsscheman även användas för andra objektanvändningsfall.

1. Klicka på fliken **[!UICONTROL Relational]**.  

1. Klicka på **[!UICONTROL Select relational XDM class]**.

   För närvarande stöds bara anpassade objekt för många konton (flera till ett).

1. Granska listan med schemafält (klicka på ikonen _information_ för att visa metadata).

1. Markera de fält som du vill ta med.

1. Använd skjutreglaget **[!UICONTROL Only show selected fields]** för att granska dina val.

1. Klicka på **[!UICONTROL Save]**.

>[!NOTE]
>
>Observera att relationsscheman måste ha följande konfigurationer:
>
><li>Beteende: Post
&gt; <li>Segmentering: Aktiverad
&gt; <li>Relationstyp: många till ett
&gt; <li>Referensschema: <a href="https://experienceleague.adobe.com/sv/docs/platform-learn/tutorials/schemas/create-schemas-for-b2b-data">B2B-konto - XDM Business Account-schema</a>
&gt; <li>Obligatoriska fält: Primär nyckel, Sekundär nyckel och Versionsbeskrivning
&gt; <li>Associerad datauppsättning: Definierad och mappad till schemat

### Händelser

Välj de Experience Events som ska användas i **_resebeslut_**.

1. Klicka på fliken **[!UICONTROL Events]**.  

1. Klicka på **[!UICONTROL Select experience event]**.

1. Klicka på **[!UICONTROL Select event type]**, välj händelsetyp och klicka på **[!UICONTROL Select]**.

1. Klicka på **[!UICONTROL Select fields]**, välj de fält som du behöver och klicka på **[!UICONTROL Select]**.

1. Klicka på **[!UICONTROL Save]**.

## E-postkonfiguration

Följande bör konfigureras för att skicka e-post från Journey Optimizer B2B edition.  

[https://experienceleague.adobe.com/en/docs/journey-optimizer-b2b/user/get-started/email-protocols](https://experienceleague.adobe.com/en/docs/journey-optimizer-b2b/user/get-started/email-protocols)

### Protokoll för spårning och e-postleverans

1. [Skapa DNS-poster för e-post](https://experienceleague.adobe.com/en/docs/journey-optimizer-b2b/user/get-started/email-protocols#create-dns-records-for-landing-pages-and-email)

1. [Konfigurera SPF och DKIM](https://experienceleague.adobe.com/en/docs/journey-optimizer-b2b/user/get-started/email-protocols#set-up-spf-and-dkim)

1. [Konfigurera DMARC](https://experienceleague.adobe.com/en/docs/journey-optimizer-b2b/user/get-started/email-protocols#set-up-dmarc)

1. [Konfigurera MX-poster för din domän](https://experienceleague.adobe.com/en/docs/journey-optimizer-b2b/user/get-started/email-protocols#set-up-mx-records-for-your-domain)

1. [Lägg till utgående IP-adresser till tillåtelselista](https://experienceleague.adobe.com/en/docs/journey-optimizer-b2b/user/get-started/email-protocols#outbound-ip-addresses)

1. Om du behöver dela den dedikerade IP-poolen kontaktar du leveransteamet om genomförbarhet och assisterad konfiguration.

### Konfigurationer av e-postkanaler

I den förenklade arkitekturen konfigureras e-postinställningarna från Marketo Engage-programmet. Slutför de e-postrelaterade installationsstegen:

* [https://experienceleague.adobe.com/en/docs/marketo/using/getting-started/initial-setup/setup-steps](https://experienceleague.adobe.com/en/docs/marketo/using/getting-started/initial-setup/setup-steps)

* [https://experienceleague.adobe.com/en/docs/journey-optimizer-b2b/user/admin/channels/configure-channels-emails](https://experienceleague.adobe.com/en/docs/journey-optimizer-b2b/user/admin/channels/configure-channels-emails)

### Kommunikationsbegränsningar

1. Välj **[!UICONTROL Administration]** > **[!UICONTROL Channels]** i den vänstra navigeringen.

1. Välj **[!UICONTROL Communication Limit]** på navigeringspanelen.

1. Skapa en regeluppsättning för global kommunikationsbegränsning (den här regeluppsättningen skapas som standard i alla instanser av Journey Optimizer B2B edition).

   Det finns ingen kommunikationsgräns om den globala regeluppsättningen inte skapas.

<!-- In the future, you can also add local communication limit rule sets (AJO B2C doc can be found here [https://experienceleague.adobe.com/en/docs/journey-optimizer/using/conflict-prioritization/capping-rules/rule-sets](https://experienceleague.adobe.com/en/docs/journey-optimizer/using/conflict-prioritization/capping-rules/rule-sets). We may need a small update for our B2B version.) -->

### Begränsningar för delad kommunikation

Inom den nya arkitekturen har Journey Optimizer B2B edition och Marketo Engage som standard oberoende kommunikationsbegränsningar.

Om du vill att Marketo Engage-instansen ska dela den angivna kommunikationsgränsen i Journey Optimizer B2B edition-instansen kontaktar du Adobe Support för att få hjälp med konfigurationen eller öppnar ett supportärende. På begäran kan ingenjörsteamet möjliggöra delning av kommunikationsbegränsningar mellan Journey Optimizer B2B edition och en eller flera Marketo Engage-instanser.

När de delade kommunikationsgränserna är aktiverade kan du definiera reglerna i Journey Optimizer B2B edition och utöka delningen av dessa begränsningar till Marketo Munchkin-koderna. Mer information finns i [Kommunikationsbegränsningar](./admin/configure-channels-emails.md#communication-limits)

<!-- internal info only 

Currently, the shared communication limit in the Marketo Engage instance must be set up through an API call.

For example, when:

* The munchkinId of the Journey Optimizer B2B Edition instance is `JKL-567-MNO`.
* The munchkinId of the Marketo Engage instance is `ABC-123-DEF` and it is in the SJ datacenter

The API request should look similar to the following:

```
curl --location --request POST 'http://sjrest2a.marketo.org/rest/v1/fm.json?_munchkinId=ABC-123-DEF&featureName=Mktmail%20Config&paramName=ajoB2bMappingMunchkinId&dataType=string&value=JKL-567-MNO'
```
-->

## SMS-kanalskonfiguration

Mer information finns i [_SMS-konfigurationer_](https://experienceleague.adobe.com/en/docs/journey-optimizer-b2b/user/admin/channels/configure-channels-sms).

## Marketo Engage-åtgärder från resor

Du kan konfigurera en eller flera **_Marketo Engage_**-fjärrinstanser för användning med följande reseåtgärder:

* Lägg till i Marketo List
* Ta bort från Marketo List
* Lägg till i Marketo Request Campaign

Utför följande steg för att konfigurera anslutningarna:

1. Navigera till **[!UICONTROL Administration]>[!UICONTROL Configurations]**.

1. Välj **[!UICONTROL XDM Classes]** på navigeringspanelen.

1. Klicka på fliken **[!UICONTROL Integrations]**.  

1. Klicka på **[!UICONTROL Create connection]**.

1. Ange **[!UICONTROL Name]** och **[!UICONTROL Description]**.

1. Välj **[!UICONTROL Update policy]** för matchande personposter.

1. Ange **[!UICONTROL Munchkin ID]**, **[!UICONTROL Client ID]**, **[!UICONTROL Client Secret]** och klicka på **[!UICONTROL Connect to Marketo]**.

1. Klicka på **[!UICONTROL Create]**.

## Användarregistrering

På sidan [Användarhantering](https://experienceleague.adobe.com/en/docs/journey-optimizer-b2b/user/admin/user-management) finns en översikt.

### Befintliga användargrupper

Om alla användare av Journey Optimizer B2B edition behöver tillgång till den nya arkitekturen kan du använda den befintliga användargruppen i Journey Optimizer B2B edition. En systemadministratör eller produktadministratör kan utföra följande steg.

1. Skapa en produktprofil i den dedikerade Marketo Engage.

1. Lägg till en befintlig användargrupp i den skapade produktprofilen.

Profilerna ger alla roller och behörigheter som redan tilldelats den användargruppen, som redan bör konfigureras för att användarna ska få tillgång till Journey Optimizer B2B edition. Om bara en delmängd av användarna ska få tillgång till den nya arkitekturen, ska du slutföra stegen nedan. Mer information finns i den [aktuella dokumentationen](https://experienceleague.adobe.com/en/docs/journey-optimizer-b2b/user/admin/user-management).

### Skapa en ny användargrupp

1. Skapa en produktprofil i den dedikerade Marketo Engage-instansen.
1. Skapa en användargrupp för nya användare.
1. Välj och tilldela de produktprofiler som behövs till användargruppen:

   * Marketo Engage-profil som du har skapat
   * Adobe Experience Platform profiler
      * AEP-Default-All-Users
      * Adobe Experience Platform Data Collection
      * Datainsamling - åtkomst

1. Lägg till användarna i användargruppen.
1. Lägg till en ny användargrupp i Journey Optimizer B2B edition-roller i Experience Platform.
