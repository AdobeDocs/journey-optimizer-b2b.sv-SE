---
title: Konvertera en bild till en e-postmall
description: Förvandla bildfiler till HTML e-postmallar med Journey Optimizer B2B edition. Ladda upp PNG-/JPEG-filer och generera automatiskt återanvändbart e-postinnehåll.
feature: Email Authoring, Content
source-git-commit: b27b4485e5d778f0d4cbcad7392ab19c42a79e14
workflow-type: tm+mt
source-wordcount: '505'
ht-degree: 0%

---

# Konvertera en bild till en e-postmall

Att skapa och uppdatera e-postmallar är en grundläggande komponent i leveranskedjan för marknadsföringsmaterial, men dessa uppgifter kräver ofta mycket tid och resurser på grund av manuell HTML-kodning. Marknadsföringsteamen har traditionellt förlitat sig på byråer eller IT-team för att ta fram dessa mallar. Det nya Image-to-HTML-verktyget för e-postmallar förenklar processen genom att marknadsförarna kan konvertera designfiler till HTML-kodmallar. Den konverterade HTML är klar för redigering i e-postdesignområdet. Det här verktyget har stöd för både filtyperna JPEG och PNG och har ett dra och släpp-gränssnitt.

Du kan enkelt konvertera designfiler som sparats som bilder (PNG eller JPEG) till HTML som är färdigt för e-postmallar, vilket sparar värdefull tid och resurser för webbteamet. Den intuitiva mallgeneratorn konverterar bilder till HTML-kodade e-postmallar som är klara att ändras med e-postdesignverktygen. Marknadsförare kan ladda upp bilder och snabbt generera e-postmallar utan att behöva skriva kod manuellt från HTML. Det här verktyget stöder konvertering från JPEG- och PNG-filer till HTML-kodade e-postmallar.

>[!BEGINSHADEBOX]

**Använda ett varumärkestema**

Om din organisation har [varumärkesteman](./brand-themes.md) definierade i Journey Optimizer B2B edition kan du välja ett varumärkestema som indata så att den genererade utdata från HTML formateras enligt parametrarna för varumärkestemat. Med den här inmatningen används format som bakgrundsfärg, knappfärg, teckensnitt, radavstånd, marginaler och utfyllnad på den genererade mallen.  Genom att använda ett varumärkestema slipper du ytterligare designarbete för formatering och formatering och skapar en mall som är klar att användas med minimala redigeringar.

>[!ENDSHADEBOX]

1. Gå till **[!UICONTROL Content Management]** > **[!UICONTROL Templates]** i den vänstra navigeringen.

   Den här åtgärden öppnar en listsida med alla skapade e-postmallar för instansen som listas i en tabell.

1. Klicka på **[!UICONTROL Convert Image to Template]** i sidhuvudet ovanför listan.

   ![Öppna e-postmallsbiblioteket och generera en mall från en bild](./assets/email-template-convert-image-select.png){width="800" zoomable="yes"}

1. Ange ett användbart **[!UICONTROL Template name]** och **[!UICONTROL Description]** (valfritt) för den genererade e-postmallen i dialogrutan.

1. (Valfritt) Välj en **[!UICONTROL Brand theme]** om du vill använda en specifik formatering på den genererade HTML-filen enligt temaspecifikationerna.

1. Använd någon av följande metoder för att överföra bildfilen:

   * Dra och släpp bildfilen i dialogrutans filområde.
   * Klicka på **[!UICONTROL Upload image]** om du vill använda ditt lokala filsystem för att leta upp och välja bildfilen.

1. Kontrollera att bildfilen inte innehåller någon personligt identifierbar information eller personuppgifter och markera kryssrutan längst ned i dialogrutan för att bekräfta.

   Klicka på länken **[!UICONTROL Adobe Experience Cloud Generative AI User Guidelines]** om du vill granska riktlinjerna.

   ![Slutför parametrar för att konvertera en bildfil till en e-postmall](./assets/email-template-convert-image-dialog.png){width="400" zoomable="yes"}

1. Klicka på **[!UICONTROL Convert]**.

   Dialogrutan stängs och det nya mallnamnet visas i listan med statusen _[!UICONTROL converting to template...]_. Konverteringsprocessen kan ta en stund, beroende på hur komplex källbilden är och det använda varumärkestemat (om det används).

1. När processen är klar klickar du på mallnamnet för att förhandsgranska det återgivna e-postinnehållet och göra nödvändiga ändringar.
