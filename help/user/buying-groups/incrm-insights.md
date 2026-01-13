---
title: Insikter i CRM
description: Få tillgång till Journey Optimizer B2B edition inköpsgrupper direkt i CRM. Säljteammedlemmarna kan visa engagemangsdata och identifiera säljmöjligheter med insikter om In-CRM.
feature: Sales Insights, Buying Groups
role: User
source-git-commit: 2eb5b6226730a1948b480a9dee0c6f2786e01cc5
workflow-type: tm+mt
source-wordcount: '379'
ht-degree: 0%

---


# Insikter i CRM

[!DNL In-CRM Insights] är ett webbbasprogram som integreras med Salesforce och Microsoft Dynamics 365 och ger dig tillgång till [!DNL Journey Optimizer B2B Edition] som köper grupper direkt i CRM. Här samlas datakällor för försäljning, vilket gör det enklare att identifiera möjligheter till ökat engagemang och ökad säljpotential.

## Installation

Installationsprocessen omfattar:

* Konfigurera användarbehörigheter och grupper
* Installera programvarupaketet
* Logga in via CRM

### Ange behörigheter

Användare som installerar programmet måste ha behörighet att installera Salesforce-paket.

Användarna måste ha ett medlemskap i en roll med behörigheten **Sales Insights:View Sales Insights** för att få åtkomst till programmet.

Om du vill begränsa användare till endast [!DNL In-CRM Insights]:

1. Skapa en [anpassad roll](https://experienceleague.adobe.com/sv/docs/journey-optimizer-b2b/user/accounts/buying-groups/default-custom-roles#create-a-custom-role) och tilldela den behörigheten **Försäljningsinsikter: Visa försäljningsinsikter**.
1. Skapa en ny [användargrupp](https://experienceleague.adobe.com/sv/docs/journey-optimizer-b2b/user/admin/user-management#create-user-group).
1. Lägg till en Experience Platform-produktprofil i gruppen.

### Installera paketet

Följ stegen för Salesforce eller Microsoft Dynamics för att installera In-CRM Insights-paketet.

#### Salesforce

1. Hämta installationspaketet [In-CRM Insights](https://experience.adobe.com/solutions/OneAdobe-sales-workflow-optimizer-sales-insight-ui/install/sales-insight?crm=salesforce).
1. När du har loggat in omdirigeras du till paketinstallationssidan.
1. Välj alternativet **[!UICONTROL Install for All Users]** och klicka på **[!UICONTROL Install]**.

   ![Installera In-CRM Insights-paketet](assets/incrm-install-sf.png){width=500}

1. Godkänn åtkomst från tredje part i dialogrutan och klicka sedan på **[!UICONTROL Continue]**.
1. När installationen är klar klickar du på **[!UICONTROL Done]**.

   Den visas nu på sidan **Installerade paket** och **Journey Optimizer B2B edition** visas i appstartaren.

   ![In-CRM-insikter konfigurerade i Salesforce](assets/in-crm-install-sf-done.png){width=800 zoomable="yes"}

#### MS Dynamics

1. Hämta installationspaketet [In-CRM Insights](https://experience.adobe.com/solutions/OneAdobe-sales-workflow-optimizer-sales-insight-ui/install/sales-insight?crm=dynamics).
1. Gå till porten [Power Apps](https://make.powerapps.com/){target=_blank}.
1. När du har loggat in väljer du miljön för paketet och navigerar sedan till **[!UICONTROL Solutions]** på den vänstra menyn.
1. Klicka på **[!UICONTROL Import solution]**.
1. Bläddra till och överför installationspaketet och klicka sedan på **[!UICONTROL Next]**.
1. Verifiera paketinformationen och klicka på **[!UICONTROL Next]**.
1. Under _Miljövariabler_ kontrollerar du att värdet är inställt på `prod` (ändra inte värdet) och klickar på **[!UICONTROL Import]**.
1. När installationen är klar visas **[!UICONTROL Journey Optimizer B2B Edition]** > **[!UICONTROL Buying groups]** i det vänstra navigeringsfältet.

   ![In-CRM-insikter finns i Microsoft Dynamics](assets/incrm-ms-install-done.png){width=800 zoomable="yes"}

## Visa dina inköpsgrupper

Följ instruktionerna för att logga in på ditt Adobe-konto. Dina inköpsgrupper är inlästa och tillgängliga att visa.

När du har valt en inköpsgrupp kan du bläddra bland [gruppinformationen](https://experienceleague.adobe.com/sv/docs/journey-optimizer-b2b/user/accounts/sales-experience/buying-group-details#). Detta är samma som de data och insikter som visas i Journey Optimizer B2B edition, men data är skrivskyddade via [!DNL In-CRM Insights].
