---
title: Återgivningsdata
description: Lär dig hur du sammanställer och skickar nyckelord för att generera intent data för Journey Optimizer B2B edition.
feature: Setup, Intent, Account Insights
roles: Admin
exl-id: c7f9f6fe-2275-42a4-af80-b5c3d1a82837
source-git-commit: 4a54548ad061fc778fae3bc4b8499f3716850e4a
workflow-type: tm+mt
source-wordcount: '225'
ht-degree: 0%

---

# Återgivningsdata

I Journey Optimizer B2B edition förutser Intent Detection-modellen en lösning/produkt av intresse med tillräckligt stor tillförsikt utifrån en leads aktivitet. Den utnyttjar även andra kontomedarbetares aktiviteter, tillsammans med taggat innehåll. En persons avsikt kan tolkas som sannolikheten att ha intresse för en produkt.

* Avsiktsnivåer - Tillgängligt på kända leads-, konto- och inköpsgruppsnivåer.
* Typer av avsiktssignal - Nyckelord, produkt och lösning

![Återgivningsdatavisualisering](../data/assets/intent-data-visualization.png){width="700" zoomable="yes"}

Om du vill aktivera den här funktionen kan du skicka en lista med nyckelord i ett kalkylblad till din kontohanterare för Adobe. Dessa nyckelord används för din innehållstaggning.

En uppsättning nyckelord (upp till 20) kan associeras med en produkt. En uppsättning produkter (upp till 20) kan kopplas till en kategori. Du kan ha högst 20 kategorier. Hela den här modellen uppnås genom ett enkelt kalkylblad som importeras. Kalkylbladet kan innehålla en enda flik som motsvarar produktnamnet och kan innehålla en kolumn som motsvarar en lista med nyckelord.

![Återgivningsdatanyckelord - en produktflik](./assets/intent-data-keywords-single-product-tab.png){width="500" zoomable="yes"}

Du kan lägga till flera flikar, där var och en har ett produktnamn och hela kalkylbladet kan korrelera till en kategori.

![Återgivningsdatanyckelord - flera produktflikar](./assets/intent-data-keywords-multiple-product-tabs.png){width="500" zoomable="yes"}
