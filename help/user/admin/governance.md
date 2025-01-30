---
title: Styrningsfunktioner
description: Läs mer om de styrningsfunktioner som finns i Journey Optimizer B2B edition.
exl-id: 2845272b-987c-4a37-adf4-6ee5bfd59fc0
source-git-commit: 3198ba223125c95263d8dcf5ee8cb285a888a26a
workflow-type: tm+mt
source-wordcount: '413'
ht-degree: 0%

---

# Styrningsfunktioner

Journey Optimizer B2B edition är en integrerad Adobe Experience Platform-app. Den innehåller flera verktyg och tjänster som ger kontroll över era insamlade upplevelsedata i enlighet med era affärspraxis, juridiska skyldigheter och utvecklingsprocesser. Avsnitten nedan innehåller en sammanfattning av alla dessa styrningsfunktioner.

## Integritet - GDPR

Journey Optimizer B2B edition använder de befintliga funktionerna för styrning av GDPR för Marketo Engage som tillhandahålls av Privacy Servicen och Marketo tjänst för integritetsutjämning.

## Rollbaserad åtkomstkontroll (RBAC)

Med Journey Optimizer B2B edition och tillgång till Adobe Admin Console kan administratörer ge en användare behörigheter för en enhetstyp (visa-segment, hantera segment, hantera resor osv.). Den här funktionen ingår i UPF (Unified Permissions Framework) som gör att alla Adobe Experience Platform-kunder kan definiera och hantera roller och behörigheter för sin organisation.

## Datakryptering

**_Kryptering av vilande data_** - Alla konton och personprofiler som överförs från Adobe Experience Platform till Journey Optimizer B2B edition krypteras för att bibehålla den befintliga kompatibiliteten från Experience Platform. Alla enheter med ursprung i Journey Optimizer B2B edition, t.ex. rese- och inköpsgrupper, krypteras också.

**_Kryptering för data som överförs_** (via ett offentligt nätverk) - Alla Journey Optimizer B2B edition API:er och entiteter krypteras under överföring med TLS 1.2.

## Medgivande - anmälan/avanmälan

Medgivande om deltagande/avanmälan är en form av styrning där en profil kan avanmäla sig från en kommunikationskanal, som e-post eller SMS, och en profil utesluts sedan från kommunikationskanalen.

Med Journey Optimizer B2B edition kan du skapa och hantera användningsfall för prenumeration/avprenumeration för e-post och SMS-leverans. Dessa inställningar för samtycke lagras i XDM Profile Consent Field Group och synkroniseras till och från Journey Optimizer B2B edition som en del av Data Sync Framework. De här inställningarna används vid leveranstillfället för att exkludera avanvisade profiler från leveranser.

## Återställ sandlåda

Sandlådeåterställning stöds **inte** för Adobe Journey Optimizer B2B edition. Om du återställer eller tar bort en sandlåda som är mappad till Journey Optimizer B2B edition kan data i Journey Optimizer B2B edition gå förlorade permanent och en ny Journey Optimizer B2B edition-instans kan behöva etableras.

## Inte tillgängligt ännu

Följande styrningsfunktioner är inte tillgängliga än:

* Tillämpning av etikett för dataanvändning (DULE) / användningsprinciper
* Datahygien
* Samtyckesprinciper
* Åtkomstkontroll på fältnivå (FLAC)
* Åtkomstkontroll på objektnivå (OLAC)
* CMK-kryptering för vilande data
* Plattformsgranskningstjänst
