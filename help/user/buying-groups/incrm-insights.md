---
title: Insikter i CRM
description: Gå till Journey Optimizer B2B edition inköpsgrupper direkt i Salesforce. Säljteammedlemmarna kan visa engagemangsdata och identifiera säljmöjligheter med insikter om In-CRM.
feature: Sales Insights, Buying Groups
role: User
source-git-commit: de7f5620556a48fe6f12ed1c70e925e11ec770f1
workflow-type: tm+mt
source-wordcount: '272'
ht-degree: 0%

---


# Insikter i CRM

In-CRM Insights är ett webbaserat program som integreras med Salesforce och ger er tillgång till era inköpsgrupper i Journey Optimizer B2B edition direkt inifrån Salesforce. Ni kan identifiera möjligheter för ökat engagemang och ökad säljpotential.

In-CRM Insights-programmet är tillgängligt i [Marketo Sales Insights-paketet](https://experienceleague.adobe.com/en/docs/marketo/using/product-docs/marketo-sales-insight/msi-for-salesforce/installation/install-marketo-sales-insight-package-in-salesforce-appexchange).

## Behörigheter

För att få åtkomst till programmet måste användarna ha ett medlemskap i en roll med behörigheten **Sales Insights:View Sales Insights** .

Om du vill begränsa en grupp användare till InCRM-Insights använder du följande riktlinjer för att skapa en anpassad roll specifikt för InCRM-Insights:

* Skapa en anpassad roll med bara behörighetsgruppen **Sales Insights:View Sales Insights** .
* Skapa en ny användargrupp utan att lägga till produktprofiler.
* Skapa en annan användargrupp och lägg till en AEP-produktprofil eller lägg till en befintlig AEP-profil i användargruppen som du just skapade.
* Tilldela de nya användargrupperna till den nya rollen och lägg till nya användare i de nya användargrupperna.

## Använda insikter i InCRM

In-CRM Insights-programmet är tillgängligt i Salesforce via App Launcher.

1. Klicka på App Launcher i Salesforce.
1. Välj eller sök efter `Journey Optimizer B2B Edition`.
1. Logga in med dina Adobe-inloggningsuppgifter på den flik som visas.
1. Välj en sandlåda som är värd för dina kontoresor.

Dina inköpsgrupper är inlästa och tillgängliga. Data är skrivskyddade via In-CRM-insikter.

>[!NOTE]
>
>Det krävs medlemskap i produktrollen [B2B-säljanvändare](../admin/user-management.md#b2b-built-in-roles) för att få tillgång till In-CRM-insikter.

När du har valt en inköpsgrupp kan du bläddra bland [gruppinformationen](https://experienceleague.adobe.com/en/docs/journey-optimizer-b2b/user/accounts/sales-experience/buying-group-details#), precis som i Journey Optimizer B2B edition.
