---
title: Skapa innehåll - personalisering
description: Återanvänt avsnitt om att använda personalisering för innehållsutveckling
source-git-commit: 3791beb98068a56882bb0a96fbc6b192e85130bb
workflow-type: tm+mt
source-wordcount: '134'
ht-degree: 1%

---

# Skapa innehåll - personalisering

Journey Optimizer B2B edition använder en infogad enkel syntax som gör att du kan skapa uttryck med anpassat innehåll omgivet av dubbla klammerparenteser `{}`. Du kan lägga till flera uttryck i samma innehåll eller fält utan begränsningar.

Exempel:

* `Hello {{profile.person.name.firstName}} {{profile.person.name.lastName}}`

* `Hello {{profile.person.name.fullName}}`

När du bearbetar innehållet ersätter Journey Optimizer B2B edition uttrycket med data som finns i Experience Platform-databasen. Det första exemplet blir _Hello John Doe_.

I följande exempel beskrivs stegen för att anpassa innehåll med hjälp av lead-/kontoattribut och systemtokens.

1. Markera textkomponenten och klicka på ikonen _Lägg till anpassning_ i verktygsfältet.

   ![Klicka på ikonen Anpassa ](../assets/content-design-shared/visual-designer-personalize-icon.png){width="600"}

   Den här åtgärden öppnar dialogrutan _Redigera Personalization_.

1. Klicka på **+** eller **..** för att lägga till en token i det tomma utrymmet.

   ![Skapa personlig text med hjälp av variabler](../assets/content-design-shared/visual-designer-personalize-dialog.png){width="700" zoomable="yes"}

1. Klicka på **[!UICONTROL Save]**.
