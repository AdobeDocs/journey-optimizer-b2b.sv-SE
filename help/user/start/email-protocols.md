---
title: Protokoll för spårning och e-postleverans
description: Konfigurera leveransprotokoll för e-post - konfigurera DNS-, SPF-, DKIM-, DMARC- och IP-tillåtelselista för optimal spårning och leveransbarhet i Journey Optimizer B2B edition.
feature: Setup, Channels
role: Admin
exl-id: 3d56f147-ad0a-4686-b14e-375c2eca8806
source-git-commit: d3247a48ff1fbda54c559fa03580865da7252935
workflow-type: tm+mt
source-wordcount: '1800'
ht-degree: 0%

---

# Protokoll för spårning och e-postleverans

Adobe Journey Optimizer B2B edition utnyttjar e-postkanalsfunktionerna och händelsespårningen i Marketo Engage. För att e-postleveransen ska fungera som förväntat för organisationer som använder en begränsande brandvägg eller proxyserverinställningar måste systemadministratören lägga till vissa domäner och IP-adressintervall i tillåtelselista.

>[!NOTE]
>
>Om din organisation redan använder den anslutna Marketo Engage-instansen för att köra sina marknadsföringsåtgärder bör dessa protokoll och konfigurationer redan finnas på plats.

Se till att följande domäner (inklusive asterisken) läggs till i tillåtelselista för att aktivera alla Marketo Engage-resurser och webbsocketar:

* `*.experience.adobe.com`
* `*.adobe.net`
* `*.marketo.com`
* `*.marketodesigner.com`
* `*.mktoweb.com`

Följ de här stegen för att säkerställa spårning och e-postleverans:

1. [Skapa DNS-poster för ](#create-dns-records-for-landing-pages-and-email)
1. [Konfigurera SPF och DKIM](#set-up-spf-and-dkim)
1. [Konfigurera DMARC](#set-up-dmarc)
1. [Konfigurera MX-poster för din domän](#set-up-mx-records-for-your-domain)
1. [Lägg till utgående IP-adresser till tillåtelselista](#outbound-ip-addresses)

## Skapa DNS-poster för <!-- landing pages and -->e-post

Genom att ansluta en CNAME-post kan marknadsförarna lagra webbversioner av e-postmeddelanden, landningssidor och bloggar med enhetlig märkning som förbättrar trafik och konverteringar. Vi rekommenderar starkt att du lägger till CNAME:er i din rotdomänvärd så att Marketo Engage kan vara värd för dina marknadsföringsfokuserade webbresurser. Som administratör bör du samarbeta med ditt marknadsföringsteam för att planera och implementera en CNAME-post för spårningslänkarna som ingår i e-postmeddelanden som skickas via Marketo Engage.
<!-- As an administrator, you should work with your Marketing team to plan and implement two CNAME records. The first one is for landing page URLs, so that the landing pages appear in URLs that reflect your domain and not Adobe Marketo Engage (the actual host). The second one is for the tracking links that are included in the emails sent through Marketo Engage.

### Add the CNAME for landing pages

Add the landing page CNAME to your DNS record, so that `[YourLandingPageCNAME]` points to the unique account string that is assigned to your landing pages. Log in to your domain registrar's site and enter the landing page CNAME and account string. This entry usually involves three fields:

* Alias: Enter `[YourLandingPageCNAME]`
* Type: CNAME
* Point to: Enter `[MunchkinID].mktoweb.com`
-->

### Lägg till CNAME för e-postspårningslänkar

Lägg till e-postmeddelandet CNAME så att `[YourEmailCNAME]` pekar på `[MktoTrackingLink]`, som är standardspårningslänken som Marketo Engage har tilldelat, i formatet:

`[YourEmailCNAME].[YourDomain].com` I CNAME `[MktoTrackingLink]`

Exempel:

`pages.abc.com IN CNAME mkto-a0244.com`

>[!NOTE]
>
>Värdet `[MktoTrackingLink]` måste vara [varumärkningsdomänens ](../admin/configure-channels-emails.md#branding-domains) standardvärde.

### Tillhandahåll SSL-certifikatet

Kontakta [Adobe Support](https://experienceleague.adobe.com/home?lang=en&support-tab=home#support){target="_blank"} för att starta processen med att etablera ett SSL-certifikat.

Denna process kan ta upp till tre arbetsdagar att slutföra.

## Konfigurera SPF och DKIM

Marknadsföringsteamet bör tillhandahålla den DKIM-information (Domain Keys Identified Mail) som ska läggas till i din DNS-resurspost. Följ de här stegen för att konfigurera DKIM och SPF (Sender Policy Framework) och meddela sedan marknadsföringsteamet när det uppdateras.

1. Om du vill konfigurera SPF lägger du till följande rad i DNS-posterna:

   ```
   [CompanyDomain] IN TXT v=spf1 mx ip4:[CorpIP]  
   include: mktomail.com ~all
   ```

   Om du redan har en SPF-post i DNS-posten lägger du bara till följande:

   ```
   include: mktomail.com
   ```

   Ersätt `CompanyDomain` med huvuddomänen för din webbplats (till exempel `company.com/`) och `CorpIP` med IP-adressen för företagets e-postserver (till exempel `255.255.255.255`). Om du tänker skicka e-post från flera domäner via Marketo Engage lägger du till den här raden för varje domän (på en rad).

1. För DKIM skapar du DNS-resursposter för varje domän.

   Lägg till värdposter och TXT-värden för varje domän:

   `[DKIMDomain1]`: Värdposten är `[HostRecord1]` och TXT-värdet är `[TXTValue1]`.

   `[DKIMDomain2]`: Värdposten är `[HostRecord2]` och TXT-värdet är `[TXTValue2]`.

   Kopiera `HostRecord` och `TXTValue` för varje DKIM-domän efter att ha följt [instruktionerna](https://experienceleague.adobe.com/en/docs/marketo/using/product-docs/email-marketing/deliverability/set-up-a-custom-dkim-signature){target="_blank"} i Marketo Engage-dokumentationen. Du kan verifiera domänerna i Journey Optimizer B2B edition (se [SPF/DKIM](../admin/configure-channels-emails.md#spfdkim)).

## Konfigurera DMARC

DMARC (domänbaserad meddelandeautentisering, rapportering och överensstämmelse) är ett autentiseringsprotokoll som används för att hjälpa organisationer att skydda sin domän mot obehörig användning. Det utökar befintliga autentiseringsprotokoll, som SPF och DKIM, så att mottagarservrar informeras om vilka åtgärder som ska vidtas om ett autentiseringsfel inträffar på deras domän. DMARC är valfritt, men vi rekommenderar starkt att du skyddar ditt varumärke och ditt rykte. Större leverantörer, som Google och Yahoo, började kräva DMARC för bulkavsändare från och med februari 2024.

För att DMARC ska fungera måste du ha minst en av följande DNS TXT-poster:

* En giltig SPF
* A valid DKIM Record for your FROM: domain (recommended for Marketo Engage and Journey Optimizer B2B edition)

Du måste också ha en DMARC-specifik DNS TXT-post för din `FROM:`-domän. Du kan också ange en e-postadress som anger var DMARC-rapporter ska placeras i organisationen för rapportövervakning.

### Exempel på DMARC-arbetsflöde

>[!TIP]
>
>Det är bäst att implementera DMARC som en _långsam utrullning_. Eskalera din DMARC-princip från `p=none` till `p=quarantine` och sedan till `p=reject` när du får en förståelse för den potentiella effekten och ställ in din DMARC-policy på att avspända justeringen för SPF och DKIM.

Om du får rapporter från DMARC bör du göra följande:

1. Använd `p=none` och analysera den feedback och de rapporter du får. Rapporterna instruerar mottagaren att inte utföra några åtgärder mot meddelanden som inte kan autentiseras och skickar e-postrapporter till avsändaren.

   * Om legitimt meddelande inte kan autentiseras, ska du granska och åtgärda problemen med SPF/DKIM.

   * Kontrollera om SPF eller DKIM är anpassade och skickar autentisering för alla giltiga e-postmeddelanden.

   * Granska rapporterna för att säkerställa att resultatet blir det som förväntas baserat på din SPF/DKIM-policy.

1. Justera principen till `p=quarantine`, som anger för den mottagande e-postservern att skicka e-postmeddelanden som inte kan autentiseras (som oftast placerar meddelandena i skräppostmappen).

   Granska rapporter för att se till att resultatet blir som du tänkt dig.

1. Om du är nöjd med beteendet för meddelanden på `p=quarantine`-nivå kan du justera principen till (`p=reject`).

   Avvisningsprincipen uppmanar mottagaren att neka (studsa) alla e-postmeddelanden för domänen som inte kan autentiseras. När den här principen är aktiverad är det bara e-post som verifieras som 100 % autentiserad av din domän som har en chans att placeras i inkorgen.

   >[!CAUTION]
   >
   >Använd den här profilen med försiktighet och kontrollera om den passar din organisation.

### DMARC-rapportering

DMARC erbjuder möjlighet att få rapporter om e-postmeddelanden som inte godkänns i SPF/DKIM. Det finns två olika rapporter som skapats av Internet-leverantörstjänster som en del av autentiseringsprocessen. Avsändare kan ta emot dessa rapporter via RUA/RUF-taggar i sin DMARC-policy.

* **Aggregate Reports (RUA)**: Innehåller inte någon PII (Personally Identiitable Information) som kan vara känslig för GDPR (General Data Protection Regulation).

* **Forensiska rapporter (RUF)** - innehåller e-postadresser som är GDPR-känsliga. Innan du implementerar den här rapporten bör du kontrollera din organisationsprofil för hantering av information som måste vara GDPR-kompatibel.

Det viktigaste användningsområdet för dessa rapporter är att få en översikt över e-postmeddelanden som försöker förfalskas. De är mycket tekniska rapporter och de beskrivs bäst med hjälp av ett verktyg från tredje part.

### Exempel på DMARC-poster

* Minsta lediga post: `v=DMARC1; p=none`

* Post som dirigerar till en e-postadress för att ta emot rapporter: `v=DMARC1; p=none;  rua=mailto:emaill@domain.com;  ruf=mailto:email@domain.com`

### DMARC-taggar

DMARC-poster har flera komponenter som kallas _DMARC-taggar_. Varje tagg har ett värde som anger en viss aspekt av DMARC.

| Märkordsnamn | Använd | Funktion | Exempel | Standardvärde |
|-----------|------------------------|-----------|----------|-----------------------------------|
| `v` | Obligatoriskt | Anger versionen. Det finns bara en version, så den har ett fast värde på `v=DMARC1` | V=DMARC1 DMARC1 | DMARC1 |
| `p` | Obligatoriskt | Anger DMARC-principen som instruerar mottagaren att rapportera, karantän eller avvisa e-post som inte kan autentiseras. | `p=none`, `p=quarantine` eller `p=reject` | – |
| `fo` | Valfritt | Låter domänägaren ange rapportalternativ. | `0`: Generera en rapport om både SPF och DKIM misslyckas <br> `1` - Generera en rapport om antingen SPF eller DKIM misslyckas <br> `d` - Generera en rapport om DKIM misslyckas <br> `s` - Generera en rapport om SPF misslyckas | `1` (rekommenderas för DMARC-rapporter) |
| `pct` | Valfritt | Anger procentandelen meddelanden som ska filtreras. | `pct=20` | `100` |
| `rua` | Valfritt (rekommenderas) | Anger var aggregerade rapporter levereras. | `rua=mailto:aggrep@example.com` | – |
| `ruf` | Valfritt (rekommenderas) | Anger var kriminaltekniska rapporter levereras. | `ruf=mailto:authfail@example.com` | – |
| `sp` | Valfritt | Anger DMARC-principen för den överordnade domänens underdomäner. | `sp=reject` | – |
| `adkim` | Valfritt | Anger en strikt (`s`) eller relaxerad (`r`) justering. Avlastad justering innebär att domänen används i DKIM-signaturen och kan vara en underdomän till adressen `From:`. Strikta justeringar innebär att domänen används i DKIM-signaturen och måste vara en exakt matchning av domänen som används i `From:`-adressen. | `adkim=r` | `r` |
| `aspf` | Valfritt | Kan vara strikt (`s`) eller avslappnad (`r`). Avstängt läge innebär att domänen Return-Path kan vara en underdomän till adressen `From:`. Strikt läge innebär att domänen Return-Path måste vara en exakt matchning med adressen `From:`. | `aspf=r` | `r` |

Mer information om DMARC och alla dess alternativ finns i [https://dmarc.org/](https://dmarc.org/){target="_blank"}.

### DMARC implementering av Marketo Engage

Det finns två typer av justering för DMARC:

* **Justering av DKIM** (Domain Keys Identified Mail): Den domän som anges i ett e-postmeddelandes `From:`-huvud matchar DKIM-signaturen. DKIM-signaturen innehåller ett `d=`-värde där domänen har angetts för matchning med `From:`-huvuddomänen.

  DKIM-justering validerar om avsändaren har behörighet att skicka e-post från domänen och verifierar att inget innehåll har ändrats under e-postöverföring. Så här implementerar du DKIM-anpassade DMARC:

   * Konfigurera DKIM för e-postmeddelandets MAIL FROM-domän. Använd [instruktionerna](https://experienceleague.adobe.com/en/docs/marketo/using/product-docs/email-marketing/deliverability/set-up-a-custom-dkim-signature){target="_blank"} i Marketo Engage-dokumentationen.

   * Konfigurera DMARC för domänen DKIM MAIL FROM.

  >[!NOTE]
  >
  >DKIM justering rekommenderas för Marketo Engage.

* **SPF**-justering (Sender Policy Framework): Domänen i huvudet `From:` måste matcha domänen i huvudet Return-Path:. Om båda DNS-domänerna är desamma matchar (justerar) SPF-filen och ger ett passresultat. Så här implementerar du SPF-justerad DMARC:

   * Konfigurera domänen för varumärkesskyddad retursökväg.

      * Konfigurera lämplig SPF-post.
      * Ändra MX-posten så att den pekar tillbaka till standardvärdet för MX för det datacenter som e-postmeddelandet skickas från

   * Konfigurera DMARC för domänen Return-Path.

  >[!NOTE]
  >
  >Strikta SPF-justeringar stöds inte och rekommenderas inte för Marketo Engage.

### Dedikerade IP-adresser och delad pool

Om du skickar e-post via Marketo Engage via en dedikerad IP-adress och inte har implementerat en profilerad retursökväg (eller om du inte vet om du har det), öppnar du en biljett med [Adobe Support](https://experienceleague.adobe.com/home?lang=en&support-tab=home#support){target="_blank"}.

Betrodda IP-adresser är en delad pool med IP-adresser som är reserverade för användare med lägre volym som skickar mindre än 75 kB per månad och som inte är kvalificerade för en dedikerad IP-adress. Dessa användare måste också uppfylla kraven på god praxis.

* Om du skickar e-post via Marketo Engage med en delad pool med IP-adresser kan du kontrollera om du är berättigad till betrodda IP-adresser genom att [ansöka om det betrodda IP-sändningsintervallprogrammet](https://na-sjg.marketo.com/lp/marketoprivacydemo/Trusted-IP-Sending-Range-Program.html){target="_blank"}. Den varumärkesskyddade retursökvägen inkluderas när du skickar från Marketo Engage betrodda IP-adresser. Om du godkänner programmet kan du kontakta Adobe Support för att skapa en egen returneringsväg.

* Om du skickar mer än 100 000 meddelanden per månad och vill skicka e-post via Marketo Engage via delade IP-adresser kontaktar du Adobe Account Team (din kontohanterare) för att köpa en dedikerad IP-adress.

## Konfigurera MX-poster för din domän

Med en MX-post kan du ta emot e-post till domänen som du skickar e-post från för att bearbeta svar och automatiska svar. Om du skickar från din företagsdomän är den förmodligen redan konfigurerad. Annars kan du vanligtvis konfigurera den för att mappa till företagets domän-MX-post.

## Utgående IP-adresser

En utgående anslutning upprättas av Marketo Engage till en server på Internet åt dig. Din IT-organisation och vissa partners/leverantörer kan använda tillåtelselista för att begränsa åtkomsten till servrar. Om så är fallet måste du förse dem med utgående IP-adressblock från Marketo Engage som kan läggas till i deras tillåtelselista.

<!-- ### Webhooks

Marketo Engage webhooks are an outbound integration mechanism. When a Smart Campaign executes a _Call Webhook_ flow action, it makes an HTTP request to an external web service. If the web service publisher uses an allowlist on the firewall of the network where the external web service is located, the publisher must add the IP address blocks listed below to their allowlist. For more information, see [Create a webhook](https://experienceleague.adobe.com/en/docs/marketo/using/product-docs/administration/additional-integrations/create-a-webhook){target="_blank"} and [Call Webhook](https://experienceleague.adobe.com/en/docs/marketo/using/product-docs/core-marketo-concepts/smart-campaigns/flow-actions/call-webhook){target="_blank"} in the Marketo Engage documentation.

### CRM sync

Marketo Engage Salesforce CRM Sync and Microsoft Dynamics Sync are integration mechanisms that make outbound HTTP requests to APIs published by your CRM vendor. Ensure that your IT organization does not block any of the IP address blocks below from accessing your CRM vendor APIs. For more information, see [Add an Existing Salesforce Field to the Marketo Sync](https://experienceleague.adobe.com/en/docs/marketo/using/product-docs/crm-sync/salesforce-sync/sfdc-sync-details/add-an-existing-salesforce-field-to-the-marketo-sync){target="_blank"} and [Understanding the Microsoft Dynamics Sync](https://experienceleague.adobe.com/en/docs/marketo/using/product-docs/crm-sync/microsoft-dynamics/understanding-the-microsoft-dynamics-sync){target="_blank"} in the Marketo Engage documentation. -->

## Utgående IP-adressblock

Följande listor täcker alla Marketo Engage-servrar som gör utgående samtal. Se de här listorna för att konfigurera en IP-tillåtelselista, server, brandvägg, åtkomstkontrollista, säkerhetsgrupp eller tredjepartstjänst för att ta emot utgående anslutningar från Marketo Engage.

| IP-block (CIDR-notering) | Enskild IP-adress |
| ------------------------ | --------------------- |
| <ul><li>`94.236.119.0/26`</li><li>`103.237.104.0/22`</li><li>`130.248.172.0/24`</li><li>`130.248.173.0/24`</li><li>`130.248.244.88/29`</li><li>`185.28.196.0/22`</li><li>`192.28.144.0/20`</li><li>`192.28.160.0/19`</li><li>`199.15.212.0/22`</li></ul> | <ul><li>`13.237.155.207`</li><li>`13.55.192.247`</li><li>`18.200.201.81`</li><li>`34.247.24.245`</li><li>`35.165.244.220`</li><li>`44.235.171.179`</li><li>`52.20.211.99`</li><li>`52.64.109.86`</li><li>`54.160.246.246`</li><li>`54.212.167.17`</li><li>`54.220.138.65`</li><li>`54.237.141.197`</li><li>`130.248.168.16`</li><li>`130.248.168.17`</li></ul> |
