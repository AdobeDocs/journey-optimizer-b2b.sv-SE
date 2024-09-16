---
title: Skapa innehåll - personalisering
description: Återanvänt avsnitt om att använda personalisering för innehållsutveckling
source-git-commit: 0a9c05ac2ddd95e1fa5321f44f5cbe8cfa595007
workflow-type: tm+mt
source-wordcount: '137'
ht-degree: 1%

---

# Skapa innehåll - personalisering

Journey Optimizer B2B Edition använder en infogad enkel syntax som gör att du kan skapa uttryck med anpassat innehåll omgivet av dubbla klammerparenteser `{}`. Du kan lägga till flera uttryck i samma innehåll eller fält utan begränsningar.

Exempel:

* `Hello {{profile.person.name.firstName}} {{profile.person.name.lastName}}`

* `Hello {{profile.person.name.fullName}}`

När du bearbetar meddelandet (e-post och SMS) ersätter Journey Optimizer B2B Edition uttrycket med data som finns i Experience Platform-databasen. Det första exemplet blir _Hello John Doe_.

I följande exempel beskrivs stegen för att anpassa innehåll med hjälp av lead-/kontoattribut och systemtokens.

1. Markera textkomponenten och klicka på ikonen _Lägg till anpassning_ i verktygsfältet.

   ![Klicka på ikonen Anpassa ](../assets/content-design-shared/visual-designer-personalize-icon.png){width="600"}

   Den här åtgärden öppnar dialogrutan _Redigera Personalization_.

1. Klicka på **+** eller **..** för att lägga till en token i det tomma utrymmet.

   ![Skapa personlig text med hjälp av variabler](../assets/content-design-shared/visual-designer-personalize-dialog.png){width="700" zoomable="yes"}

1. Klicka på **[!UICONTROL Save]**.
