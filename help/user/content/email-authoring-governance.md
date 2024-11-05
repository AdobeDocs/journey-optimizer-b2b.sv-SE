---
title: Skapa från en styrd mall
description: Lär dig hur du använder e-postredigering med en styrd mall som innehåller låsta innehållskomponenter.
feature: Email Authoring, Content
source-git-commit: d7e2b7673b0a6709d2841893d87617e580b62298
workflow-type: tm+mt
source-wordcount: '266'
ht-degree: 0%

---

# Författare från en styrd mall

Innehållsdesigners kan aktivera [styrning (_innehållslås_)](./template-content-governance.md) när de skapar e-postmallar. Styrningsfunktioner gör det möjligt för dem att ange vilka delar av designen som inte kan ändras när de används på en kontoresa. När du [väljer en sparad mall](./email-authoring.md#select-a-template) för att skapa ett e-postmeddelande läser den visuella designern in mallen så att du kan använda den som grund för e-postmeddelandet.

Om mallen har styrning aktiverad visas en varning på egenskapspanelen till höger. Du kan aktivera **[!UICONTROL Highlight editable areas]** högst upp på arbetsytan för att se vilka komponenter och innehållselement som kan redigeras under din resa.

![Visa redigerbara områden i en styrd mall](./assets/email-designer-governed-highlight.png){width="800" zoomable="yes"}

Du kan också avgöra vilka element som är låsta eller redigerbara med _navigeringsträdet_. Klicka på ikonen _Navigeringsträd_ ( ![länkikon](../assets/do-not-localize/icon-navigation-tree.svg) ) till vänster om arbetsytan för att visa trädet.

![Visa redigerbara områden i en styrd mall](./assets/email-designer-governed-tree.png){width="600" zoomable="yes"}

Ikonerna anger inställningarna för innehållslås.

| Ikon | Namn | Beskrivning |
|------|------|-------------|
| ![Skrivskyddad ikon](../assets/do-not-localize/icon-tree-lock.svg) | Skrivskyddad | Komponenten är låst och kan inte redigeras. När det används på rotnivån (_[!UICONTROL Body]_) är alla underordnade komponenter låsta och kan inte redigeras. |
| ![Ikon för innehållsredigering](../assets/do-not-localize/icon-tree-content-lock.svg) | Innehållslås | Lås innehåll används på komponentnivå. |
| ![Redigerbar ikon](../assets/do-not-localize/icon-edit.svg) | Redigerbar | Komponenten är helt redigerbar. Du kanske inte kan ta bort elementet. |
| ![Ikon för innehållsredigering](../assets/do-not-localize/icon-tree-edit-text.svg) | Redigerbar - endast innehåll | Komponenten och formateringen är statiska, men du kan ändra innehållet (till exempel text eller bild). |
