---
title: Kom igång med Journey Optimizer B2B edition
description: Som ny användare av Journey Optimizer B2B-version får du lära dig mer om de viktigaste områdena att komma igång med.
role: Admin, User
exl-id: 83f8e666-0b31-4323-9902-4fdf4446424c
source-git-commit: 4a54548ad061fc778fae3bc4b8499f3716850e4a
workflow-type: tm+mt
source-wordcount: '664'
ht-degree: 6%

---

# Kom igång med Journey Optimizer B2B edition

Vilka funktioner och verktyg du vill använda i Adobe Journey Optimizer B2B edition beror på vilken roll du har i ditt team.

Beroende på din organisation kan administratörer definiera flera typer av användare och ge dem åtkomst till vissa funktioner beroende på deras behörigheter.

>[!TIP]
>
>Kontrollera även dina licensrättigheter och motsvarande [produktbeskrivning](https://helpx.adobe.com/se/legal/product-descriptions/adobe-journey-optimizer-b2b.html){target="_blank"} om prestandaresäkerhetsskydd och statiska begränsningar.

>[!BEGINTABS]

>[!TAB Snabbstart för administratör]

Innan ditt team kan börja använda funktionerna i Adobe Journey Optimizer B2B edition krävs flera steg för att förbereda din miljö. Utför dessa steg så att datateknikern och marknadsföraren kan börja arbeta med Adobe Journey Optimizer B2B edition.

Som systemadministratör måste du förstå produktprofiler och tilldela behörigheter för sandlådeadministration och kanalkonfiguration. Du måste också konfigurera sandlådor och hantera dem för de tillgängliga produktprofilerna. Du kan sedan tilldela teammedlemmar till produktprofilerna. Dessa funktioner kan hanteras av produktadministratörer som har tillgång till Adobe Admin Console. [Läs mer om Adobe Admin Console](https://helpx.adobe.com/se/enterprise/using/admin-console.html).

Lär dig mer om åtkomsthantering på följande sidor:

1. **Skapa sandlådor** för att partitionera dina instanser i separata, isolerade virtuella miljöer. [Läs mer](https://experienceleague.adobe.com/sv/docs/experience-platform/sandbox/home#understanding-sandboxes){target="_blank"}

1. **Konfigurera produktprofilen**. En produktprofil är en uppsättning enhetsrättigheter i Adobe Experience Platform som ger användarna tillgång till vissa funktioner eller objekt i gränssnittet. [Läs mer](../admin/user-management.md#create-the-marketo-engage-product-profile)

1. **Konfigurera användarbehörigheter** för produktprofiler, inklusive sandlådor, och ge teammedlemmarna åtkomst genom att tilldela dem till olika produktprofiler. Den här uppgiften utförs i Admin Console. [Läs mer](../admin/user-management.md#create-a-user-group)

1. **Konfigurera e-postleverans** i Marketo Engage, vilket gör att ditt team kan skicka e-postinnehåll från kontoresor. [Läs mer](https://experienceleague.adobe.com/sv/docs/marketo/using/getting-started/initial-setup/setup-steps#ensure-email-deliverability){target="_blank"}

1. **Konfigurera SMS-tjänster**. Konfigurera en av de tredjepartsleverantörer av SMS som stöds och som erbjuder SMS-tjänster oberoende av varandra, och konfigurera kontoinloggningsuppgifterna i Adobe Journey Optimizer B2B edition. [Läs mer](../admin/configure-channels-sms.md)

1. **Konfigurera och aktivera användning av Adobe Experience Manager Assets** för team som använder Assets as a Cloud Service för centraliserad hantering av digitala resurser. [Läs mer](../admin/configure-aem-repositories.md)

1. **Konfigurera Adobe Experience Platform (AEP) Experience Event-definitioner** för team som ansvarar för att skapa kontoresor som lyssnar på AEP Experience Events. [Läs mer](../admin/configure-aep-events.md)

>[!TAB Komma igång med marknadsföringssnabbtangenten]

Som marknadsförare, eller en _kontoansvarig_, ansvarar du för att utforma resor och skapa innehåll. Du kan börja arbeta med Adobe Journey Optimizer B2B edition när systemadministratören och datateknikern har förberett din miljö och gett dig åtkomst.

Se följande avsnitt för att konfigurera din första resa, lägga till resurser och skicka innehåll:

1. **Lägg till kontomålgrupper**. Med Journey Optimizer B2B edition kan ni skapa kontomålgrupper genom segmentdefinitioner direkt från programmet och utnyttja dem i era kontoresor. [Läs mer](../audiences/account-audience-overview.md)

1. **Skapa inköpsgrupper**. Definiera nyckelkomponenterna för att uppfylla dina affärsmål och -mål och skapa inköpsgrupper som identifierar medlemmarna i dina målkontolistor. [Läs mer](../buying-groups/buying-groups-overview.md)

1. **Skapa och hantera resurser**. Adobe Experience Manager Assets erbjuder en enda central lagringsplats med resurser som du kan använda för att fylla i dina meddelanden. [Läs mer](../content/assets-overview.md)

1. **Lägg till anpassade och dynamiska e-postmallar**. Utnyttja personalisering och dynamiska innehållsfunktioner i Journey Optimizer B2B edition för att anpassa budskapet till er målgrupp. [Läs mer](../content/email-templates.md)

1. **Designa kontoresor för att leverera personaliserade, sammanhangsbaserade upplevelser**. Med Journey Optimizer B2B edition kan du skapa användningsfall för realtidssamordning med kontextuella data som lagras i händelser eller datakällor. Designa avancerade scenarier i flera steg som bygger på följande funktioner:

   * Skicka enhetsleverans i realtid som utlöses när en händelse tas emot, eller i batch med Adobe Experience Platform-målgrupper.

   * Använd sammanhangsbaserade data från händelser, information från Adobe Experience Platform eller data från API-tjänster från tredje part.

   * Använd de inbyggda kanalåtgärderna (e-post och SMS) för att skicka meddelanden som utformats i Journey Optimizer B2B edition.

   * I kunddesignern kan du bygga upp dina flerstegssituationer, lägga till villkor och skicka personaliserade meddelanden.

[Läs mer](../journeys/journey-overview.md)

>[!ENDTABS]
