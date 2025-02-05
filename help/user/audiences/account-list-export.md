---
title: Exportera kontolista
description: Lär dig exportera kontolistan baserat på inköpsgruppsfilter.
source-git-commit: c51ee8c8b58e8154c81f6a2ffada3f58a08eb6b4
workflow-type: tm+mt
source-wordcount: '243'
ht-degree: 0%

---

# Exportera kontolista

Använd funktionen _Exportera kontolista_ om du vill exportera alla konton eller en uppsättning konton baserat på den filtrering som du anger. Exportprocessen skapar en CSV-fil och skickar URL:en för den lagrade filen i ett pulsmeddelande. Du kan använda den här funktionen för att flytta konton till tredjepartsplattformar vid behov.

1. I Journey Optimizer B2B edition går du till **[!UICONTROL Accounts]** > **[!UICONTROL Buying groups]** i den vänstra navigeringen.

1. Välj fliken **[!UICONTROL Browse]**.

1. Klicka på **[!UICONTROL Export accounts]** överst till höger.

   ![Redigera kontoinformation](./assets/export-accounts.png){width="800" zoomable="yes"}

1. I dialogrutan definierar du parametrarna för de kontomålgrupper som ska exporteras.

   ![Ange filtrering av kontomepubliken](./assets/export-accounts-dialog.png){width="400"}

   För **[!UICONTROL Engagement score]** är operatorn `Between` inkluderande, liksom procentintervall. 5.1 och 5 är till exempel både _mellan_ 5 och 6.

   Tomma filterparametrar behandlas som `Is Any`.

1. Klicka på **[!UICONTROL Export accounts]** om du vill generera CSV-filen med de angivna filtren.

1. När du får ett meddelande om att exporten är klar klickar du på meddelandelänken för att öppna CSV-filen.

   ![Klicka på meddelandet om du vill hämta CSV-filen för den exporterade kontolistan](./assets/export-accounts-notification.png){width="425"}

   >[!NOTE]
   >
   >Om du har en meddelandeprenumeration för e-postmeddelanden som har konfigurerats i inställningarna för användarkontot i Adobe kan det vara ett e-postmeddelande.

   Programsidan dirigeras om till fliken _Buying Group_ och dialogrutan Spara fil uppmanar dig att spara filen på datorn. Om du behöver dela data kan du använda teamets fildelningssystem.
