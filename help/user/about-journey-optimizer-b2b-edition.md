---
title: Adobe Journey Optimizer B2B Edition - översikt
description: Upptäck funktioner för Adobe Journey Optimizer B2B-versionen, användningsfall och arkitekturer.
exl-id: fdfbafdf-826f-44e9-bbb6-5e729d0e18ef
source-git-commit: 78d82aa8b3bb8b8d432eeb187d75e2354dbff3ee
workflow-type: tm+mt
source-wordcount: '805'
ht-degree: 1%

---

# Adobe Journey Optimizer B2B Edition - översikt

Med Adobe Journey Optimizer B2B Edition kan ni samordna konto- och inköpsgruppresor med hjälp av inbyggd generativ AI och branschledande automatisering för att maximera efterfrågan på specifika erbjudanden med hjälp av marknadsföringskvalificerade inköpsgrupper.

## Kontoresor med inköpsgrupper

När man jämför Adobe Journey Optimizer B2B Edition med standarden Marketo Engage och Adobe Journey Optimizer är den viktigaste skillnaden att kontoresor flyttar konton genom resan, inte människor. En person som är kopplad till ett konto har troligen en icke-linjär progression, baserad på hur kontot fortskrider under resan, inte baserat på deras individuella åtgärder. Om ett konto till exempel befinner sig i ett tidigt skede av köpresan kan den information som skickas handla om allmänna funktioner eller funktioner för lösningar. Under köpprocessen kan innehållet bli mer inriktat på vissa erbjudanden eller andra objekt som är inriktade på att avsluta en försäljning. När lösningen har köpts kan informationen ändras igen för att ge handledningar, bästa praxis eller information om kommande evenemang, eller för innehåll om ytterligare merförsäljning. Även om en individ inte har interagerat med innehållet i den tidiga fasen vill du ändå gå vidare till den aktuella fasen baserat inte på deras egna åtgärder, utan på åtgärder från andra personer på deras konto eller i deras inköpsgrupp.

## Arkitektur på hög nivå

Adobe Journey Optimizer B2B Edition använder _kontomåldrar_ och kontots _målgrupper_ från Adobe Experience Platform för att styra en kontoresa som körs innanför Marketo Engage. Experience Platform är alltid källan till sanning för dessa data, men all körning och bearbetning av kontoresan sker inuti marknadsföringsinfrastrukturen för Marketo Engage B2B. Orchestration återför data till Experience Platform i nära realtid med den befintliga källkontakten Marketo Engage - Adobe Real-Time CDP B2B Edition, som strömmar dataändringar från Marketo Engage till Experience Platform.

![Dataarkitektur på hög nivå](./assets/high-level-data-architecture.png){width="500" zoomable="yes"}

### Prenumerationsmodell

En Journey Optimizer B2B Edition-prenumeration definieras av ett par AEP-sandlådor (Experience Platform) med en _munchkin_-prenumeration på Marketo Engage. Det går inte att kombinera en prenumeration på Marketo Engage med mer än en AEP-sandlåda. Om du inte väljer att använda en befintlig Marketo Engage-prenumeration med Journey Optimizer B2B Edition, eller om du inte redan använder Marketo Engage, får du en ny, tom Marketo Engage-prenumeration för användning med Journey Optimizer B2B Edition.

Syftet med Experience Platform i den här konfigurationen är att ge en enhetlig bild av data från instanserna i Marketo Engage (och eventuella tillhörande CRM-system) och sedan kunna agera på enhetliga data med hjälp av en kontoresa.

### Åtgärder för kontoresa

Kontoresor skapas i Journey Optimizer B2B Edition och lagras i den Marketo Engage-instans som är kopplad till prenumerationen. Även om den lagras i datalagret i Marketo Engage är den inte synlig från användargränssnittet i Marketo Engage, och den kan bara användas från Journey Optimizer B2B Edition.

En kontoresa börjar alltid med att ett kontosegment väljs som målgrupp för kundresan. När du väljer målgrupp används standardkomponenten för målgruppsväljare i Experience Platform. Marknadsförarna kan sedan implementera kontoresan genom att dela upp kundresan enligt sina egna kriterier, som kan innehålla kontokriterier, personkriterier eller köpgruppskriterier. På varje gren kan åtgärder vidtas för att implementera resan, som att skicka ett e-postmeddelande eller vänta på att en händelse ska inträffa.

När kontoresan har skapats måste den publiceras. Vid publicering valideras kontoresan och konverteras till en serie Marketo Engage-kampanjer som implementerar upplevelsen, och dataintegreringstjänsterna kontaktas för att starta dataflödet som i sin tur startar kontoresan. Det första steget är att skapa segment för kontots personer.

### Dataflöde

Journey Optimizer B2B Edition använder Real-Time CDP-kontosegmentering för att både definiera och köra kontonegment och närliggande kundsegment som resorna kräver. När en publicerad resa körs kan data om människor och konton ändras, och data samlas in om de personer som interagerar med resan. Journey Optimizer B2B Edition förlitar sig på Marketo Engage-källkopplingen för Real-Time CDP B2B Edition för att flöda dataändringar tillbaka till sandlådan Experience Platform, som är sanningens källa.  Dessa data levereras till AEP i nära realtid.

Endast de datatyper som stöds av Marketo Engage-källkopplingen (konton, människor och affärsmöjligheter) flödar tillbaka till Real-Time CDP. Detta innebär att data från inköpsgrupper inte flödar till AEP utan i stället finns i den Marketo Engage-instans som används av prenumerationen på Journey Optimizer B2B Edition.
