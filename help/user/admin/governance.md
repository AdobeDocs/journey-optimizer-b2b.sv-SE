---
title: Styrningsfunktioner
description: Läs mer om funktioner för styrning som för närvarande finns i Journey Optimizer B2B Edition.
exl-id: 2845272b-987c-4a37-adf4-6ee5bfd59fc0
source-git-commit: 78d82aa8b3bb8b8d432eeb187d75e2354dbff3ee
workflow-type: tm+mt
source-wordcount: '373'
ht-degree: 0%

---

# Styrningsfunktioner

Journey Optimizer B2B Edition är en integrerad Adobe Experience Platform-app och har flera tjänster och verktyg som gör att du kan kontrollera insamlade upplevelsedata på ett säkert sätt för att följa företagets rutiner, juridiska skyldigheter och utvecklingsprocesser. Avsnitten nedan innehåller en sammanfattning av alla dessa styrningsfunktioner.

## Integritet - GDPR

Journey Optimizer B2B Edition använder de befintliga funktionerna för styrning av Marketo Engage GDPR som tillhandahålls av Privacy Servicen och Marketo tjänst för integritetsutjämning.

## Rollbaserad åtkomstkontroll (RBAC)

Med Journey Optimizer B2B Edition och tillgång till Adobe Admin Console kan administratörer ge användare behörigheter för en enhetstyp (visa-segment, hantera segment, hantera resor osv.). Den här funktionen ingår i UPF (Unified Permissions Framework) som gör att alla Adobe Experience Platform-kunder kan definiera och hantera roller och behörigheter för sin organisation.

## Datakryptering

**_Kryptering av vilande data_** - Alla konton och personprofiler som överförs från Adobe Experience Platform till Journey Optimizer B2B Edition krypteras för att bibehålla kompatibiliteten från Experience Platform. Alla enheter med ursprung i Journey Optimizer B2B Edition, t.ex. resor och köpgrupper, krypteras också.

**_Kryptering för data som överförs_** (via ett offentligt nätverk) - Alla Journey Optimizer B2B Edition-API:er och enheter krypteras under överföring med TLS 1.2.

## Medgivande - anmälan/avanmälan

Medgivande om deltagande/avanmälan är en form av styrning där en profil kan avanmäla sig från en kommunikationskanal, t.ex. e-post eller SMS, och en profil bör sedan uteslutas från en sådan kommunikationskanal.

Med Journey Optimizer B2B Edition kan du skapa och hantera användningsfall för prenumeration/avprenumeration för e-post och SMS-leverans. Dessa medgivandeinställningar lagras i XDM Profile Consent Field Group och synkroniseras till och från Journey Optimizer B2B Edition som en del av Data Sync Framework. De här inställningarna används vid leveranstillfället för att exkludera avanvisade profiler från leveranser.

## Inte tillgängligt ännu

Följande styrningsfunktioner är ännu inte tillgängliga, men ingår i produktfärdplanen:

* Tillämpning av etikett för dataanvändning (DULE) / användningsprinciper
* Datahygien
* Återställ sandlåda
* Samtyckesprinciper
* Åtkomstkontroll på fältnivå (FLAC)
* Åtkomstkontroll på objektnivå (OLAC)
* CMK-kryptering för vilande data
* Plattformsgranskningstjänst
