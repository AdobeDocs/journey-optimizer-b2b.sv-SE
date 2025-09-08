---
title: Använd AI-assistenten
description: Ställ frågor om produktkunskaper i AI Assistant och få information om resor, målgrupper och inköpsgrupper i Journey Optimizer B2B edition.
feature: AI Assistant
role: User
level: Beginner
exl-id: 2d642c34-6f6d-4a0f-98c5-4b9ea1cdaa29
source-git-commit: 4fdd89bf32cb9d68b4cdc347f1fd09df8eabe24d
workflow-type: tm+mt
source-wordcount: '949'
ht-degree: 0%

---

# Använd AI-assistenten i Journey Optimizer B2B edition

I Journey Optimizer B2B edition är AI Assistant en funktion i användargränssnittet som du kan använda för att förstå produktkoncept, snabbt navigera och lära dig mer om produktfunktionerna samt få driftsinsikter om din miljö. Det finns också i flera Adobe Experience Cloud-produkter.

>[!IMPORTANT]
>
>Du måste ha ett avtal för Adobe Experience Cloud Generative AI User Guidelines innan du kan använda AI Assistant. Mer information om det här avtalet och riktlinjer för användning finns i [Adobe Experience Cloud Generative AI User Guidelines](https://www.adobe.com/legal/licenses-terms/adobe-dx-gen-ai-user-guidelines.html).

Du öppnar AI Assistant genom att klicka på ikonen i sidhuvudet. AI-assistenten öppnas i en panel till höger.

![Klicka på ikonen för att komma åt AI-assistenten](./assets/ai-assistant-icon-displayed.png){width="420"}

Gränssnittet för AI Assistant visas och du får information om hur du kommer igång direkt. Du kan använda alternativen under _Ideas för att komma igång_ för att svara på frågor och kommandon, som:

* Vilka resor publicerades?
* Vilka lösningsintressen skapades?
* Berätta om huvudfördelarna med Journey Optimizer B2B edition.

I Adobe Journey Optimizer B2B edition har AI Assistant stöd för följande användningsområden:

## Ställ frågor om produktkunskap

Produktkunskapsfrågor handlar om Journey Optimizer B2B edition koncept och instruktionsinformation. Några exempel på frågor om produktkunskap är:

* Hur konfigurerar jag SMS-leverantörskonton?
* Hur skickar jag ett e-postmeddelande under en resa?
* Hur kan jag personalisera mitt e-postinnehåll?

Om du vill ställa en produktfråga anger du den i fältet längst ned på panelen och trycker på Retur. Om du till exempel behöver lära dig hur du använder en inköpsgrupp på en resa. I det här fallet anger du _Hur använder jag en inköpsgrupp under en resa?_ När du har skickat frågan frågar AI Assistant efter sin kunskapsbas och sammanställer ett svar på några sekunder.

![Ange en fråga i textrutan](./assets/ai-assistant-ask-question.png){width="420"}

+++Visa ett exempelsvar

![Ange en fråga i textrutan](./assets/ai-assistant-product-answer.png){width="420"}

+++

## Ställ frågor om driftsinsikter

Frågor om driftsinsikter handlar om reseobjekten i organisationens sandlåda. Du kan ställa frågor om driftfelaktigheter, som kontomepublik, kontoresa, lösningsintresse och inköpsgruppmall. Några exempel på frågor eller frågor om driftsinsikter är:

* Hur många direktresor har jag i Adobe Journey Optimizer B2B edition?
* Ge mig en lista över alla schemalagda resor
* Hur många resor har skapats de senaste 7 dagarna?

Du måste vara i en aktiv sandlåda för att AI Assistant ska kunna svara tillräckligt på en fråga om dina operativa insikter.

>[!NOTE]
>
>De enda Adobe Journey Optimizer B2B edition-objekt som stöds av AI Assistant-frågor om driftsinsikter listas i domäntabellen [driftsinsikter](./ai-assistant-overview.md#operational-insights). Den kan bara komma åt data för den sandlåda som du för närvarande befinner dig i.

Om du vill ställa en fråga om användbara insikter anger du den i fältet längst ned på panelen och trycker på Retur. Om du till exempel vill veta mer om målgrupperna för din sandlåda. I det här fallet anger du _Hur många målgrupper finns det?_.  AI Assistant ger ett antal målgrupper i din sandlåda och en förklaring av hur svaret har beräknats. I följande exempelsvar tillhandahåller AI Assistant en länk för att få tillgång till målgrupperna i användargränssnittet och sammanfattar de åtgärder som vidtagits för att identifiera antalet målgrupper.

![AI Assistant-svar för hur många målgrupper](./assets/ai-assistant-insights-answer.png){width="420"}

Du kan följa din första fråga genom att be om en lista med artefakter, som _Visa de fem översta efter storlek_. AI Assistant returnerar en tabell med de fem främsta objekten i frågan och deras motsvarande ID:n. Klicka på ikonen _Hämta_ ( ![Ikonen Hämta](../assets/do-not-localize/icon-download.svg) ) för att hämta tabellen som en CSV-fil.

![AI Assistant-svar för en lista över direktresor](./assets/ai-assistant-artifacts-query.png){width="420"}

Om du vill visa hela tabellen i AI-assistenten klickar du på ikonen _Maximera_ ( ![Maximera ](../assets/do-not-localize/icon-maximize.svg) ). I den utökade tabellvyn klickar du på **[!UICONTROL Download CSV]** för att spara informationen som en CSV-fil.

![AI Assistant-svar för en lista över direktresor](./assets/ai-assistant-artifacts-maximize.png){width="600" zoomable="yes"}

## Verifiera svar

AI Assistant innehåller verktyg som du kan använda för att verifiera och validera svar.

### Kunskapskällor

När du har fått ett svar på en produktfråga väljer du **[!UICONTROL Show source]** om du vill visa de produktkunskapsbaserade källcitat som används för att generera AI Assistant-svaret.

AI Assistant tillhandahåller länkar till den dokumentation som bekräftar det inledande svaret. Dessutom läggs fotnoter till i svaret för att ange de specifika delar av svaret som refererar till de länkade dokumentationskällorna.

![Resultat från AI Assistant-frågan](./assets/ai-assistant-product-answer-sources.png){width="420"}

### Källor till driftsinsikter

När du har fått ett svar på en fråga om driftsinsikter klickar du på **[!UICONTROL Show source]** och väljer sedan **[!UICONTROL View source query]**.

Du kan verifiera varje svar som rör frågor om driftsinsikter med hjälp av en SQL-fråga som AI Assistant tillhandahåller. När AI Assistant får en fråga om driftsinsikter kan du använda den för att verifiera processen som tog att beräkna svaret. Den här källfrågan är endast avsedd för verifiering och stöds inte av frågetjänsten.

![Resultat från AI Assistant-frågan](./assets/ai-assistant-artifacts-query-source.png){width="550" zoomable="yes"}

## Ge feedback

Använd ikonerna _Tumma upp_ ( ![Tumma upp](../assets/do-not-localize/icon-thumb-up.svg) ) eller _Tumma ned_ ( ![Tumma ned](../assets/do-not-localize/icon-thumb-down.svg) ) för att gradera svarets användbarhet och kvalitet. Fyll i det korta enkätformuläret enligt din erfarenhet och klicka på **[!UICONTROL Submit]**. Informationen du anger används för att förbättra AI Assistant.

Om du märker att något i svaret är problematiskt klickar du på ikonen _Flagga_ ( ![Flagga-ikon](../assets/do-not-localize/icon-flag.svg) ). Använd formuläret för att beskriva problemet och klicka på **[!UICONTROL Submit]** för att rapportera problemet.

![AI Assistant-svar - feedback-ikoner](./assets/ai-assistant-response-feedback-icons.png){width="420"}

+++Visa formulär

>[!BEGINTABS]

>[!TAB Tumma upp]

![AI Assistant-svar - Dra ihop det positiva feedbackformuläret](./assets/ai-assistant-response-feedback-positive-form.png){width="600" zoomable="yes"}

>[!TAB Tumma ned]

![AI Assistant-svar - Tummen gav negativ feedback från formulär](./assets/ai-assistant-response-feedback-negative-form.png){width="600" zoomable="yes"}

>[!TAB Flagga]

![AI Assistant-svar - Flagga problem med feedback-formulär](./assets/ai-assistant-response-feedback-flagged-form.png){width="600" zoomable="yes"}

>[!ENDTABS]

+++
