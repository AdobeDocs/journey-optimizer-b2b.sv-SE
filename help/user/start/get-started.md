---
title: Kom igång med Journey Optimizer B2B Edition
description: Som ny användare av Journey Optimizer B2B Edition får du lära dig mer om de viktigaste områdena att komma igång med.
exl-id: 83f8e666-0b31-4323-9902-4fdf4446424c
source-git-commit: 7103e4f6666482a72511661dfaed1392d4eb16b1
workflow-type: tm+mt
source-wordcount: '623'
ht-degree: 3%

---

# Kom igång med Journey Optimizer B2B Edition

Vilka funktioner och verktyg du vill använda i Adobe Journey Optimizer B2B Edition beror på din roll i teamet.

Beroende på din organisation kan administratörer definiera flera typer av användare och ge dem åtkomst till vissa funktioner beroende på deras behörigheter.

>[!BEGINTABS]

>[!TAB Snabbstart för administratör]

Innan ditt team kan börja använda funktionerna i Adobe Journey Optimizer B2B Edition krävs flera steg för att förbereda din miljö. Utför dessa steg så att datateknikern och marknadsföraren kan börja arbeta med Adobe Journey Optimizer B2B Edition.

Som systemadministratör måste du förstå produktprofiler och tilldela behörigheter för sandlådeadministration och kanalkonfiguration. Du måste också konfigurera sandlådor och hantera dem för de tillgängliga produktprofilerna. Du kan sedan tilldela teammedlemmar till produktprofilerna. Dessa funktioner kan hanteras av produktadministratörer som har tillgång till Adobe Admin Console. [Läs mer om Adobe Admin Console](https://helpx.adobe.com/se/enterprise/using/admin-console.html).

Lär dig mer om åtkomsthantering på följande sidor:

1. **Skapa sandlådor** för att partitionera dina instanser i separata, isolerade virtuella miljöer. [Läs mer](https://experienceleague.adobe.com/en/docs/experience-platform/sandbox/home#understanding-sandboxes)

1. **Konfigurera produktprofilen**. En produktprofil är en uppsättning enhetsrättigheter i Adobe Experience Platform som ger användarna tillgång till vissa funktioner eller objekt i gränssnittet. [Läs mer](../admin/user-management.md#create-the-marketo-engage-product-profile)

1. **Konfigurera användarbehörigheter** för produktprofiler, inklusive sandlådor, och ge teammedlemmarna åtkomst genom att tilldela dem till olika produktprofiler. Den här uppgiften utförs i Admin Console. [Läs mer](../admin/user-management.md#create-a-user-group)

1. **Konfigurera e-postleverans** i Marketo Engage, vilket gör att ditt team kan skicka e-postinnehåll från kontoresor. [Läs mer](https://experienceleague.adobe.com/en/docs/marketo/using/getting-started/initial-setup/setup-steps#ensure-email-deliverability)

1. **Konfigurera SMS-tjänster**. Konfigurera en av de tredjepartsleverantörer av SMS som stöds och som erbjuder SMS-tjänster oberoende av varandra, och konfigurera kontoinloggningsuppgifterna i Adobe Journey Optimizer B2B Edition. [Läs mer](../content/sms-authoring.md#create-a-new-api-credentials-for-an-sms-service-provider)

1. **Konfigurera och aktivera användning av Adobe Experience Manager Assets** för team som använder Assets som en Cloud Service för centraliserad hantering av digitala resurser. [Läs mer](../admin/configure-aem-repositories.md)

>[!TAB Komma igång med marknadsföringssnabbtangenten]

Som marknadsförare, eller en _kontoansvarig_, ansvarar du för att utforma resor och skapa innehåll. Du kan börja arbeta med Adobe Journey Optimizer B2B Edition när systemadministratören och datateknikern har förberett miljön och gett dig åtkomst.

Se följande avsnitt för att konfigurera din första resa, lägga till resurser och skicka innehåll:

1. **Lägg till kontomålgrupper**. Med Journey Optimizer B2B Edition kan ni skapa kontomålgrupper genom segmentdefinitioner direkt från programmet och utnyttja dem i era kontoresor. [Läs mer](../audiences/account-audience-overview.md)

1. **Skapa inköpsgrupper**. Definiera nyckelkomponenterna för att uppfylla era affärsmål och -mål och skapa inköpsgrupper som identifierar medlemmarna i era målkonton. [Läs mer](../buying-groups/buying-groups-overview.md)

1. **Skapa och hantera resurser**. Adobe Experience Manager Assets erbjuder en enda central lagringsplats med resurser som du kan använda för att fylla i dina meddelanden. [Läs mer](../content/assets-overview.md)

1. **Lägg till anpassade och dynamiska e-postmallar**. Utnyttja personaliseringen av Journey Optimizer B2B Edition och funktionerna för dynamiskt innehåll för att anpassa budskapet till era målgrupper. [Läs mer](../content/email-templates.md)

1. **Designa kontoresor för att leverera personaliserade, sammanhangsbaserade upplevelser**. Med Journey Optimizer B2B Edition kan du skapa användningsfall för realtidssamordning med kontextuella data lagrade i händelser eller datakällor. Designa avancerade scenarier i flera steg som bygger på följande funktioner:

   * Skicka enhetsleverans i realtid som utlöses när en händelse tas emot, eller i batch med Adobe Experience Platform-målgrupper.

   * Använd sammanhangsbaserade data från händelser, information från Adobe Experience Platform eller data från API-tjänster från tredje part.

   * Använd de inbyggda kanalåtgärderna (e-post och SMS) för att skicka meddelanden som utformats i Journey Optimizer B2B Edition.

   * I kunddesignern kan du bygga upp dina flerstegssituationer, lägga till villkor och skicka personaliserade meddelanden.

[Läs mer](../journeys/journey-overview.md)

>[!ENDTABS]
