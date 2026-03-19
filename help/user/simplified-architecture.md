---
title: Förenklad arkitekturkonfiguration
description: Installera Journey Optimizer B2B edition på den förenklade arkitekturen. Konfigurera XDM-scheman, e-post-/SMS-kanaler, Marketo Engage reseåtgärder och användare.
feature: Setup, Administration
role: Admin, Data Engineer
exl-id: 81232976-09d6-4e10-a034-5c193a63b7df
source-git-commit: 38d1794ed30a34dbb34dfaec2d3088bc3a4680ac
workflow-type: tm+mt
source-wordcount: '884'
ht-degree: 7%

---

# Förenklad arkitekturkonfiguration

Adobe Journey Optimizer B2B edition finns nu i en förenklad arkitektur. Med den här arkitekturen finns Journey Optimizer B2B edition och Marketo Engage inte längre i samma system och datalager. Journey Optimizer B2B edition tar endast emot data från Adobe Experience Platform. Men man fortsätter att förlita sig på Marketo Engage-berättiganden och vissa backend-funktioner, som e-postleverans, för att etablera och konfigurera systemet.

Den förenklade arkitekturen utgör grunden för nya funktioner i Journey Optimizer B2B edition:

* **Gör era data enhetliga och skalbara enkelt:** Den nya plattformen har stöd för komplexa datamodeller, inklusive anpassade objekt, inköpsgrupper och kontohändelser.

* **Koppla ihop flera Adobe Marketo Engage-instanser:** Hantera och förena data från flera Marketo Engage-miljöer på ett och samma ställe.

* **Skyddar dina data:** Avancerade sekretess- och säkerhetsfunktioner som skyddar din kundinformation. (_Kommer snart_)

* **Skapat för framtiden:** Den här uppgraderingen konfigurerar dig för kontinuerliga förbättringar och innovation.

För miljöer som har etablerats för den här arkitekturen använder du följande riktlinjer för konfiguration.

Använd checklistan för att slutföra installationen av Journey Optimizer B2B edition på den förenklade arkitekturen.

## &#x200B;1. Generera B2B-namnutrymmen och scheman

<table>
<thead>
<tr>
<th colspan="2">Uppgift</th>
<th>Detaljer och instruktioner</th>
</tr>
</thead>
<tbody>
<tr>
<td colspan="2"><strong>Miljöinställningar:</strong></td>
<td></td>
</tr>
<tr>
<td><img src="../assets/do-not-localize/icon-checkbox.svg" width="25" alt="Kryssruta"/></td>
<td>Hämta verktyget för automatisk generering av namnområde och schema från GitHub.</td>
<td><a href="./data/namespaces-schemas.md#set-up-the-auto-generation-utility">Läs mer</a></td>
</tr>
<tr>
<td><img src="../assets/do-not-localize/icon-checkbox.svg" width="25" alt="Kryssruta"/></td>
<td>Samla in Experience Platform API-uppgifter och obligatoriska rubriker.</td>
<td><a href="https://experienceleague.adobe.com/sv/docs/experience-platform/landing/platform-apis/api-guide">Läs mer</a></td>
</tr>
<tr>
<td><img src="../assets/do-not-localize/icon-checkbox.svg" width="25" alt="Kryssruta"/></td>
<td>Använd miljövärden i Postman.</td>
<td><a href="./data/namespaces-schemas.md#environment-values">Läs mer</a></td>
</tr>
<tr>
<td colspan="2"><strong>Kör skripten:</strong></td>
<td></td>
</tr>
<tr>
<td><img src="../assets/do-not-localize/icon-checkbox.svg" width="25" alt="Kryssruta"/></td>
<td>Kör genereringsverktyget <em>Namnutrymmen och scheman</em> i Postman och bekräfta att namnutrymmen och scheman har skapats.</td>
<td><a href="./data/namespaces-schemas.md#run-the-scripts">Läs mer</a></td>
</tr>
</tbody>
</table>

## &#x200B;2. Konfigurera XDM-fält och -händelser

<table>
<thead>
<tr>
<th colspan="2">Uppgift</th>
<th>Detaljer och instruktioner</th>
</tr>
</thead>
<tbody>
<tr>
<td colspan="2"><strong>XDM-standardklasser</strong>: Konfigurera enskilda XDM-profiler och XDM Business Account-klasser.</td>
<td></td>
</tr>
<tr>
<td><img src="../assets/do-not-localize/icon-checkbox.svg" width="25" alt="Kryssruta"/></td>
<td>Välj hanterade fält att visa för resor, inköpsgrupper och e-postpersonalisering.</td>
<td><a href="./admin/xdm-field-management.md#standard-classes">Läs mer</a></td>
</tr>
<tr>
<td><img src="../assets/do-not-localize/icon-checkbox.svg" width="25" alt="Kryssruta"/></td>
<td>Redigera uppdateringsbara fält för scheman.</td>
<td><a href="./admin/xdm-field-management.md#updatable-fields">Läs mer</a></td>
</tr>
<tr>
<td colspan="2"><strong>Relationsscheman</strong>: Välj relationsklassen XDM (Account many-to-one Custom Object).</td>
<td></td>
</tr>
<tr>
<td><img src="../assets/do-not-localize/icon-checkbox.svg" width="25" alt="Kryssruta"/></td>
<td>Kontrollera att scheman har de konfigurationsvärden som krävs.</td>
<td><a href="./admin/xdm-field-management.md#relational-schemas">Läs mer</a></td>
</tr>
<tr>
<td colspan="2"><strong>Händelser</strong>: Konfigurera händelsetyper och fält för Experience Platform.</td>
<td></td>
</tr>
<tr>
<td><img src="../assets/do-not-localize/icon-checkbox.svg" width="25" alt="Kryssruta"/></td>
<td>Konfigurera varje Experience Platform-händelsetyp med fält som ska stödjas i sökvägar för resebeslut/delning.</td>
<td><a href="./admin/configure-aep-events.md">Läs mer</a></td>
</tr>
</tbody>
</table>

## &#x200B;3. Konfigurera spårning och e-postleverans

Om du vill skicka e-postmeddelanden från [!DNL Journey Optimizer B2B Edition] på den förenklade arkitekturen konfigurerar du e-postspårning och leverans i den bifogade [!DNL Marketo Engage]-produktionsinstansen och i [!DNL Journey Optimizer B2B Edition]-appen.

<table>
<thead>
<tr>
<th colspan="2">Uppgift</th>
<th>Detaljer och instruktioner</th>
</tr>
</thead>
<tbody>
<tr>
<td colspan="2"><strong>Inledande konfiguration</strong> för den bifogade Marketo Engage-instansen</td>
<td></td>
</tr>
<tr>
<td><img src="../assets/do-not-localize/icon-checkbox.svg" width="25" alt="Kryssruta"/></td>
<td>Konfigurera ny CNAME för spårning av länkar i DNS-poster</td>
<td><a href="./start/email-protocols.md#create-dns-records-for-landing-pages-and-email">Läs mer</a></td>
</tr>
<tr>
<td><img src="../assets/do-not-localize/icon-checkbox.svg" width="25" alt="Kryssruta"/></td>
<td>Konfigurera profileringsdomäner för den bifogade Marketo Engage-instansen</td>
<td><a href="./start/branding-domains.md">Läs mer</a></td>
</tr>
<tr>
<td><img src="../assets/do-not-localize/icon-checkbox.svg" width="25" alt="Kryssruta"/></td>
<td>Konfigurera DKIM och SPF till den bifogade Marketo Engage-instansen</td>
<td><a href="./start/email-protocols.md#set-up-spf-and-dkim">Läs mer</a></td>
</tr>
<tr>
<td><img src="../assets/do-not-localize/icon-checkbox.svg" width="25" alt="Kryssruta"/></td>
<td>Konfigurera DMARC</td>
<td><a href="./start/email-protocols.md#set-up-dmarc">Läs mer</a></td>
</tr>
<tr>
<td><img src="../assets/do-not-localize/icon-checkbox.svg" width="25" alt="Kryssruta"/></td>
<td>Konfigurera MX-poster för din domän</td>
<td><a href="./start/email-protocols.md#set-up-mx-records-for-your-domain">Läs mer</a></td>
</tr>
<tr>
<td><img src="../assets/do-not-localize/icon-checkbox.svg" width="25" alt="Kryssruta"/></td>
<td>Lägg till utgående IP-adresser till tillåtelselista</td>
<td><a href="./start/email-protocols.md#outbound-ip-addresses">Läs mer</a></td>
</tr>
<tr>
<td colspan="2"><strong>E-postkonfiguration</strong> för den bifogade Marketo Engage-instansen</td>
<td></td>
</tr>
<tr>
<td><img src="../assets/do-not-localize/icon-checkbox.svg" width="25" alt="Kryssruta"/></td>
<td>Konfigurera <em>Från e-post</em> och <em>Från etikett</em> (valfritt)</td>
<td><a href="./start/email-setup.md#from-email-and-label">Läs mer</a></td>
</tr>
<tr>
<td><img src="../assets/do-not-localize/icon-checkbox.svg" width="25" alt="Kryssruta"/></td>
<td>Konfigurera <em>Avbeställ HTML</em> och <em>Avbeställ text</em></td>
<td><a href="./start/email-setup.md#unsubscribe-messaging">Läs mer</a></td>
</tr>
<tr>
<td><img src="../assets/do-not-localize/icon-checkbox.svg" width="25" alt="Kryssruta"/></td>
<td>Konfigurera <em>Visa som webbsida HTML</em> och <em>Visa som webbsidetext</em></td>
<td><a href="./start/email-setup.md#view-as-web-page">Läs mer</a></td>
</tr>
<tr>
<td><img src="../assets/do-not-localize/icon-checkbox.svg" width="25" alt="Kryssruta"/></td>
<td>Konfigurera <em>gränser för hämtning av anpassade objekt</em></td>
<td><a href="./start/email-setup.md#custom-object-retrieval-limits">Läs mer</a></td>
</tr>
<tr>
<td><img src="../assets/do-not-localize/icon-checkbox.svg" width="25" alt="Kryssruta"/></td>
<td>Konfigurera <em>anpassade rubrikalternativ</em></td>
<td><a href="./start/email-setup.md#custom-header-options">Läs mer</a></td>
</tr>
<tr>
<td><img src="../assets/do-not-localize/icon-checkbox.svg" width="25" alt="Kryssruta"/></td>
<td>Konfigurera filtrering av <em>punktaktivitet</em></td>
<td><a href="./start/email-setup.md#filter-email-bots">Läs mer</a></td>
</tr>
<tr>
<td colspan="2"><strong>Konfigurera e-postkanal</strong> för Journey Optimizer B2B edition</td>
<td></td>
</tr>
<tr>
<td><img src="../assets/do-not-localize/icon-checkbox.svg" width="25" alt="Kryssruta"/></td>
<td>Konfigurera <em>kommunikationsbegränsningar</em> i Journey Optimizer B2B edition</td>
<td><a href="./admin/configure-channels-emails.md#communication-limits">Läs mer</a></td>
</tr>
</tbody>
</table>

<!-- TBD for later 

<tr>
<td><img src="../assets/do-not-localize/icon-checkbox.svg" width="25" alt="Checkbox"/></td>
<td>Configure <em>Email CC Settings</em></td>
<td>[Learn more](TBD)</td>
</tr>

<tr>
<td colspan="2"><strong>Additional configurations</strong></td>
<td></td>
</tr>
<tr>
<td><img src="../assets/do-not-localize/icon-checkbox.svg" width="25" alt="Checkbox"/></td>
<td>Configure <em>Location Settings</em> for the attached Marketo Engage instance</td>
<td>< [Learn more](TBD)</td>
</tr>
<tr>
<td><img src="../assets/do-not-localize/icon-checkbox.svg" width="25" alt="Checkbox"/></td>
<td>Define and configure which Binding Groups / IPs to move over</td>
<td>[Learn more](TBD)</td>
</tr>
<tr>
<td><img src="../assets/do-not-localize/icon-checkbox.svg" width="25" alt="Checkbox"/></td>
<td>Test Email Send</td>
<td>[Learn more](TBD)</td>
</tr>
-->

## &#x200B;4. Konfigurera ytterligare innehållskanaler

Konfigurera ytterligare kanaler för att ge marknadsförarna stöd för att inkludera andra kanaler på deras resor.

<table>
<thead>
<tr>
<th colspan="2">Uppgift</th>
<th>Detaljer och instruktioner</th>
</tr>
</thead>
<tbody>
<tr>
<td colspan="2"><strong>SMS</strong>-kanalkonfiguration för Journey Optimizer B2B edition.</td>
<td></td>
</tr>
<tr>
<td><img src="../assets/do-not-localize/icon-checkbox.svg" width="25" alt="Kryssruta"/></td>
<td>Konfigurera varje SMS-konto som du vill ha support för.</td>
<td><a href="./admin/configure-channels-sms.md">Läs mer</a></td>
</tr>
<tr>
<td colspan="2"><strong>Konfiguration av landningssidor</strong> (Beta) för kanalkonfiguration för Journey Optimizer B2B edition.</td>
<td></td>
</tr>
<tr>
<td><img src="../assets/do-not-localize/icon-checkbox.svg" width="25" alt="Kryssruta"/></td>
<td>Slutför inställningarna för landningssidan för att ge stöd åt marknadsförare som redigerar och publicerar dessa sidor</td>
<td><a href="./admin/landing-page-settings.md">Läs mer</a></td>
</tr>
<tr>
<td colspan="2"><strong>Konfiguration av webbkanal (Beta) för Journey Optimizer B2B edition</strong></td>
<td></td>
</tr>
<tr>
<td><img src="../assets/do-not-localize/icon-checkbox.svg" width="25" alt="Kryssruta"/></td>
<td>Konfigurera din företagswebbplats så att den stöder Adobe Experience Platform Web SDK.</td>
<td><a href="https://experienceleague.adobe.com/sv/docs/experience-platform/collection/js/js-overview">Läs mer</a></td>
</tr>
<tr>
<td><img src="../assets/do-not-localize/icon-checkbox.svg" width="25" alt="Kryssruta"/></td>
<td>Lägg till webbegenskaper via en URL där innehållet levereras.</td>
<td><a href="./admin/configure-channels-web.md">Läs mer</a></td>
</tr>
<tr>
<td><img src="../assets/do-not-localize/icon-checkbox.svg" width="25" alt="Kryssruta"/></td>
<td>Instruera webbupplevelsens författare att installera webbläsartillägget Adobe Experience Cloud Visual Editing Helper.</td>
<td><a href="./content/web-experiences.md#install-the-visual-editing-helper-extension">Läs mer</a></td>
</tr>
</tbody>
</table>

## &#x200B;5. Anslut Marketo Engage-instansen för att stödja reseåtgärder (valfritt)

Om du tänker komplettera funktionerna i Journey Optimizer B2B edition med kampanjer och program i Marketo Engage, ska du konfigurera stöd för Marketo Engage åtgärder. Med den här åtgärden kan era marknadsföringsteam samordna sin _kontobaserade_ marknadsföring i Journey Optimizer B2B edition och _lead-baserade_ marknadsföringsaktiviteter i Marketo Engage.

<table>
<thead>
<tr>
<th colspan="2">Uppgift</th>
<th>Detaljer och instruktioner</th>
</tr>
</thead>
<tbody>
<tr>
<td colspan="2"><strong>För varje Marketo Engage-instans</strong> som stöder reseåtgärder</td>
<td></td>
</tr>
<tr>
<td><img src="../assets/do-not-localize/icon-checkbox.svg" width="25" alt="Kryssruta"/></td>
<td>Skapa Marketo Engage anpassade tjänst</td>
<td><a href="./admin/marketo-actions-connect.md#create-the-marketo-engage-custom-service">Läs mer</a></td>
</tr>
<tr>
<td><img src="../assets/do-not-localize/icon-checkbox.svg" width="25" alt="Kryssruta"/></td>
<td>Lägg in integreringen i Journey Optimizer B2B edition</td>
<td><a href="./admin/marketo-actions-connect.md#add-the-integration">Läs mer</a></td>
</tr>
</tbody>
</table>

## &#x200B;6. Aktivera användaråtkomst

När etableringen är klar är sandlådor bundna och initiala konfigurationsåtgärder slutförda, konfigurerar du Journey Optimizer B2B edition- och Marketo Engage-åtkomst för ditt team och dina användare.

<table>
<thead>
<tr>
<th colspan="2">Uppgift</th>
<th>Detaljer och instruktioner</th>
</tr>
</thead>
<tbody>
<tr>
<td colspan="2"><strong>Ange produktåtkomst och behörigheter</strong> för användare</td>
<td></td>
</tr>
<tr>
<td><img src="../assets/do-not-localize/icon-checkbox.svg" width="25" alt="Kryssruta"/></td>
<td>Skapa en Marketo Engage-produktprofil i Adobe Admin Console (endast ny Marketo Engage-instans)</td>
<td><a href="./admin/user-management.md#create-the-marketo-engage-product-profile">Läs mer</a></td>
</tr>
<tr>
<td><img src="../assets/do-not-localize/icon-checkbox.svg" width="25" alt="Kryssruta"/></td>
<td>Lägg till en användargrupp för profilen</td>
<td><a href="./admin/user-management.md#add-a-user-group-for-the-profile">Läs mer</a></td>
</tr>
<tr>
<td><img src="../assets/do-not-localize/icon-checkbox.svg" width="25" alt="Kryssruta"/></td>
<td>Konfigurera användarroller för B2B</td>
<td><a href="./admin/user-management.md#b2b-built-in-roles">Läs mer</a></td>
</tr>
<tr>
<td><img src="../assets/do-not-localize/icon-checkbox.svg" width="25" alt="Kryssruta"/></td>
<td>Lägg till användare eller grupper i rollerna</td>
<td><a href="./admin/user-management.md#add-users-to-a-role">Läs mer</a></td>
</tr>
</tbody>
</table>
