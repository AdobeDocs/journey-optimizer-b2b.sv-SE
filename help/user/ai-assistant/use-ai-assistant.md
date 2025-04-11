---
title: Använd AI-assistenten
description: Se hur AI Assistant kan hjälpa dig att få ut det mesta av Journey Optimizer B2B edition-funktionerna.
feature: AI Assistant
level: Beginner
exl-id: 2d642c34-6f6d-4a0f-98c5-4b9ea1cdaa29
source-git-commit: d19ed2bbe850a14cb0563f6e3563cd8f1c8d3226
workflow-type: tm+mt
source-wordcount: '494'
ht-degree: 0%

---

# Använd AI-assistenten i Journey Optimizer B2B edition

I Journey Optimizer B2B edition är AI Assistant en funktion i användargränssnittet som du kan använda för att förstå produktkoncept, snabbt navigera och lära dig mer om funktionerna i Journey Optimizer B2B edition samt få driftsinsikter för just din miljö. Det finns också i flera Adobe Experience Cloud-produkter.

>[!IMPORTANT]
>
>Du måste ha ett avtal för Adobe Experience Cloud Generative AI User Guidelines innan du kan använda AI Assistant. Mer information om det här avtalet och riktlinjer för användning finns i [Adobe Experience Cloud Generative AI User Guidelines](https://www.adobe.com/legal/licenses-terms/adobe-dx-gen-ai-user-guidelines.html).

Du öppnar AI Assistant genom att klicka på ikonen i sidhuvudet. AI-assistenten öppnas i en panel till höger.

![Klicka på ikonen för att komma åt AI-assistenten](./assets/ai-assistant-icon-displayed.png){width="420" zoomable="yes"}

Gränssnittet för AI Assistant visas och du får information om hur du kommer igång direkt. Du kan använda alternativen under _Ideas för att komma igång_ för att svara på frågor och kommandon, som:

* Vilka av mina kontoresor har publicerats?
* Vilka lösningsintressen skapades?
* Berätta om huvudfördelarna med Journey Optimizer B2B edition.

I Adobe Journey Optimizer B2B edition har AI Assistant stöd för följande användningsområden:

## Produktkunskap

Produktkunskapsfrågor handlar om Journey Optimizer B2B edition koncept som gäller aspekter av Adobe Journey Optimizer. Några exempel på frågor om produktkunskap är:

* Hur konfigurerar jag SMS-leverantörskonton?
* Hur skickar jag ett e-postmeddelande under en kontoresa?
* Hur kan jag personalisera mitt e-postinnehåll?

Om du vill ställa en produktfråga anger du den i fältet längst ned på panelen och trycker på Retur.

![Ange en fråga i textrutan](./assets/ai-assistant-ask-question.png){width="420" zoomable="yes"}

Du kan verifiera svaren som skickats in av AI Assistant genom att granska de citat som finns i varje produktinformationssvar.

Om du vill visa citat och validera AI Assistants svar väljer du **[!UICONTROL Show sources]**.

![Resultat från AI Assistant-frågan](./assets/ai-assistant-answer.png){width="420" zoomable="yes"}

AI Assistant uppdaterar gränssnittet och ger dig länkar till dokumentation som bekräftar det ursprungliga svaret. När citat är aktiverat uppdaterar AI Assistant svaret så att det innehåller fotnoter som anger vilka delar av svaret som refererar till den angivna dokumentationen.

Använd reglaget uppåt eller nedåt för att bedöma svarets kvalitet.

## Driftsinsikter

Frågor om driftsinsikt handlar om reseobjekten i organisationens sandlåda. Några exempel på frågor eller frågor om driftsinsikter är:

* Hur många direktresor har jag i Adobe Journey Optimizer B2B edition?
* Ge mig en lista över alla schemalagda resor
* Hur många resor har skapats de senaste 7 dagarna?

Du måste vara i en aktiv sandlåda för att AI Assistant ska kunna svara tillräckligt på en fråga om dina operativa insikter.

>[!NOTE]
>
>De enda Adobe Journey Optimizer B2B edition-objekt som stöds av AI Assistant-frågor om driftsinsikter listas i domäntabellen [driftsinsikter](./ai-assistant-overview.md#operational-insights). Den kan bara komma åt data för den sandlåda som du för närvarande befinner dig i.

<!-- Select to view an example of an operational insights question.

In the following example, AI Assistant receives the following query: _Show me dataflows that were created using the Amazon S3 source._

screen

AI Assistant responds with a table list of your dataflows and their corresponding IDs. Click the _Download_ icon ( Download icon ) to download the table as a CSV file. To view the entire table, click the _Expand_ icon ( Expand icon ).

screen

An expanded view of the table appears, providing you with a more comprehensive list of dataflows based on the parameters of your query.

screen

When prompted with an operational insights question, AI Assistant provides an explanation of how it computed the answer. In the following example, AI Assistant outlines the steps it took in order to identify the dataflows that were created using the Amazon S3 source.

screen

You can also provide filters and modifications to your questions, and you can instruct AI Assistant to render its findings based on the filters that you include. For example, you can ask AI Assistant to show you a trend of the count of segment definitions in the order of their created date, remove segment definitions with zero total profiles, and use month names instead of integers when displaying the data.

### Verify operational insights responses

You can verify each response related to operational insights questions using an SQL query that AI Assistant provides.

Select to view example of verifying operational insights responses

After receiving an answer for an operational insights question, click **[!UICONTROL Show sources]** and then select **[!UICONTROL View source query]**.

screen

When queried with an operational insights question, AI Assistant provides an SQL query that you can use to verify the process that it took to compute its answer. This source query is for verification purposes only and is not supported on Query Service.

screen  

 -->
