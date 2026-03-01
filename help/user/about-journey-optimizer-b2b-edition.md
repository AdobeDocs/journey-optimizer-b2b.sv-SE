---
title: Adobe Journey Optimizer B2B edition - översikt
description: Läs om Adobe Journey Optimizer B2B edition - samordna kontoresor med inköpsgrupper, AI-insikter och Experience Platform-integrering för B2B-marknadsföring.
exl-id: fdfbafdf-826f-44e9-bbb6-5e729d0e18ef
source-git-commit: d3247a48ff1fbda54c559fa03580865da7252935
workflow-type: tm+mt
source-wordcount: '840'
ht-degree: 0%

---

# Adobe Journey Optimizer B2B edition - översikt

Med Adobe Journey Optimizer B2B edition kan ni samordna konton och köpa gruppresor med hjälp av inbyggd generativ AI och branschledande automatisering för att maximera efterfrågan på specifika erbjudanden med hjälp av marknadsföringskvalificerade inköpsgrupper.

## Kontoresor med inköpsgrupper

När man jämför Adobe Journey Optimizer B2B edition med Marketo Engage och Adobe Journey Optimizer är den viktigaste skillnaden att kontoresor rör konton genom resan, inte människor. En person som är kopplad till ett konto har vanligtvis en icke-linjär progression som baseras på hur kontot fortskrider under resan, inte baserat på deras individuella åtgärder. Om ett konto till exempel befinner sig i ett tidigt skede av köpresan kan den information som skickas handla om allmänna funktioner eller funktioner för lösningar. Under köpprocessen kan innehållet bli mer inriktat på vissa erbjudanden eller andra objekt som är inriktade på att avsluta en försäljning. När lösningen har köpts kan informationen ändras igen för att ge handledningar, bästa praxis eller information om kommande evenemang, eller för innehåll om ytterligare merförsäljning. Även om en individ inte har interagerat med innehållet i den tidiga fasen vill du ändå gå vidare till den aktuella fasen baserat inte på deras egna åtgärder, utan på åtgärder från andra personer på deras konto eller i deras inköpsgrupp.

## Arkitektur på hög nivå

Adobe Journey Optimizer B2B edition använder _Account Audiences_ och _People Audiences_ från Adobe Experience Platform för att styra en kontoresa som körs inuti Marketo Engage. Experience Platform är alltid källan till sanning för dessa data, men all körning och bearbetning av kontoresan sker inuti Marketo Engage B2B-marknadsföringsinfrastruktur. Orchestration återför data till Experience Platform i nära realtid med den befintliga Marketo Engage - Adobe Real-Time CDP B2B edition-källkontakten som strömmar dataändringar från Marketo Engage till Experience Platform.

![Dataarkitektur på hög nivå](./assets/high-level-data-architecture.png){width="500" zoomable="yes"}

>[!NOTE]
>
>Kontrollera dina licensrättigheter och motsvarande [produktbeskrivning](https://helpx.adobe.com/se/legal/product-descriptions/adobe-journey-optimizer-b2b.html){target="_blank"} om prestandaskydd och statiska begränsningar.

### Prenumerationsmodell

En Journey Optimizer B2B edition-prenumeration definieras av ett par Experience Platform-sandlådor (AEP) med en Marketo Engage _Munchkin_ -prenumeration. Det går inte att kombinera en enstaka Marketo Engage-prenumeration med mer än en AEP-sandlåda. Om du inte väljer att koppla en befintlig Marketo Engage-prenumeration till Journey Optimizer B2B edition får du en ny, tom Marketo Engage-prenumeration som du kan använda med Journey Optimizer B2B edition.

Syftet med Experience Platform i den här konfigurationen är att ge en enhetlig bild av data från Marketo Engage-instanserna (och eventuella tillhörande CRM-system) och sedan kunna agera på enhetliga data med hjälp av en kontoresa.

### Åtgärder för kontoresa

Kontoresor skapas i Journey Optimizer B2B edition och lagras i den Marketo Engage-instans som är kopplad till prenumerationen. Även om den lagras i Marketo Engage datalager är den inte synlig från Marketo Engage användargränssnitt och kan bara användas från Journey Optimizer B2B edition.

En kontoresa börjar alltid med att ett kontosegment väljs som målgrupp för kundresan. Väljaren av målgrupp använder Experience Platform standardkomponent för målgruppsväljare. Marknadsförarna kan sedan implementera kontoresan genom att dela upp kundresan enligt sina egna kriterier, som kan innehålla kontokriterier, personkriterier eller köpgruppskriterier. På varje gren kan åtgärder vidtas för att implementera resan, som att skicka ett e-postmeddelande eller vänta på att en händelse ska inträffa.

När kontoresan har skapats måste den publiceras. Vid publicering valideras kontoresan och konverteras till en serie Marketo Engage-kampanjer som implementerar upplevelsen. Dataintegreringstjänsterna kontaktas för att starta dataflödet som i sin tur startar kontoresan. Det första steget är att skapa segment för kontots personer.

### Dataflöde

Journey Optimizer B2B edition använder Real-Time CDP kontosegmentering för att både definiera och verkställa kontonegment och närliggande kundsegment som resorna kräver. När en publicerad resa körs kan data om människor och konton ändras, och data samlas in om de personer som interagerar med resan. Journey Optimizer B2B edition förlitar sig på Marketo Engage källanslutning för Real-Time CDP B2B edition för att flöda dataändringar tillbaka till Experience Platform-sandlådan, som är sanningens källa.  Dessa data levereras till AEP i nära realtid.

Endast de datatyper som stöds av Marketo Engage källanslutning (konton, människor och affärsmöjligheter) flödar tillbaka till Real-Time CDP. Detta innebär att data från inköpsgrupper inte flödar till AEP utan i stället finns i den Marketo Engage-instans som används av Journey Optimizer B2B edition-prenumerationen.
