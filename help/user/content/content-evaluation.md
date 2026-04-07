---
title: Innehållsbedömning
description: Utvärdera e-postinnehåll med bedömning av varumärkesjustering - validera färger, teckensnitt, logotyper och skriva stil mot varumärkesriktlinjer i Journey Optimizer B2B edition.
badge: label="Beta" type="Informative"
feature: Content, Brand Identity
role: User
level: Beginner, Intermediate
exl-id: 686d5ce0-c597-48e1-a51f-e91e95a942d5
source-git-commit: 37e4a7976d716f24edf2c2e92cbfa4c149aa66ec
workflow-type: tm+mt
source-wordcount: '730'
ht-degree: 6%

---

# Innehållsbedömning {#content-scoring}

Utvärderingen och poängsättningen av innehållet hjälper dig att skapa, granska och hantera innehåll som följer riktlinjerna [som definierats i det valda varumärket](./brands-manage-create.md#brand-definitions) och de allmänna kvalitetsstandarderna. Genom att köra en utvärdering säkerställs enhetlighet i fråga om ton, meddelanden och visuell identitet i alla e-postkampanjer, samtidigt som det fungerar som en kvalitetskontroll innan innehållet publiceras.

>[!AVAILABILITY]
>
>Ett [användaravtal](https://www.adobe.com/legal/licenses-terms/adobe-dx-gen-ai-user-guidelines.html){target="_blank"} krävs innan du kan använda AI-baserade funktioner i Adobe Journey Optimizer B2B edition. Kontakta Adobe om du vill ha mer information.
>
>Mer information om hur produktadministratörer kan aktivera de här funktionerna finns i [varumärkesrelaterade behörigheter](./brands-overview.md#brand-related-permissions).

## Utvärdera

1. När du har skapat e-postinnehållet klickar du på ikonen _Varumärkesjustering_ ( ![Varumärkesjusteringsikon](../assets/do-not-localize/icon-brand-compliance.svg) ) till höger för att öppna den högra panelen för _Varumärkesjustering_ i e-postdesignområdet.

   [Standardvarumärket](./brands-manage-create.md#default-brand) markeras automatiskt.

   ![Få åtkomst till varumärkesjusteringsverktygen](./assets/brands-alignment-sidebar.png){width="600" zoomable="yes"}

   Du kan klicka på ikonen _Helskärm_ ( ![Helskärmsikon](../assets/do-not-localize/icon-full-screen.svg) ) längst upp på panelen om du vill visa varumärkesjusteringsverktygen i helskärmsläge.

1. Om det behövs klickar du på **[!UICONTROL Brand]**-menypilen ( ![ nedpil ](../assets/do-not-localize/icon-down-menu.svg) ) för att välja ett annat publicerat varumärke.

1. Klicka på **[!UICONTROL Evaluate score]** om du vill få innehållets justering med det valda varumärket.

   Systemet utvärderar innehållet mot riktlinjerna för det valda varumärket och visar resultatet.

   ![Utvärderingsresultat i den högra panelen](./assets/brands-alignment-evaluation.png){width="600" zoomable="yes"}

## Poäng för varumärkesjustering {#brand-score}

>[!CONTEXTUALHELP]
>id="ajo-b2b_brand_score_overview"
>title="Märkesmarkering"
>abstract="Välj ert varumärke för att säkerställa att ert innehåll utformas i enlighet med dess specifika riktlinjer, standarder och identitet, samtidigt som ni upprätthåller enhetlighet och varumärkesintegritet."

>[!CONTEXTUALHELP]
>id="ajo-b2b_brand_score"
>title="Poäng för varumärkesjustering"
>abstract="Poängen för varumärkesanpassning mäter hur väl ert innehåll följer varumärkesriktlinjerna för att säkerställa enhetlighet i färger, teckensnitt, logotyp, bilder och skrivstil."

>[!CONTEXTUALHELP]
>id="ajo-b2b_brand_colors_score"
>title="Färgskala"
>abstract="Färgskala"

>[!CONTEXTUALHELP]
>id="ajo-b2b_brand_fonts_score"
>title="Teckensnittsmusik"
>abstract="Teckensnittsmusik"

>[!CONTEXTUALHELP]
>id="ajo-b2b_brand_logos_score"
>title="Logos score"
>abstract="Logos score"

>[!AVAILABILITY]
>
>Den här funktionen är för närvarande tillgänglig som en betaversion.

När ert varumärke är väldefinierat och publicerat kan ni bedöma ert varumärkeskoncentrationsmoment direkt i e-postdesignområdet för att säkerställa att innehållet följer varumärkesriktlinjerna:

Poängen beräknas enligt identifierade fel i det utvärderade e-postinnehållet:

* 100 = Perfekt - Inga överträdelser hittades
* 80-99 = Bra - Endast mindre överträdelser
* 60-79 = Rättvis - vissa allvarliga överträdelser
* Under 60 = Dålig - allvarliga överträdelser måste åtgärdas

Du kan granska utvärderingsresultaten i detalj för att hjälpa dig att identifiera överträdelser och förbättra dina poängvärden för kategorijustering (_Hög_, _Medium_ och _Låg_) och granska informationen.

För **[!UICONTROL Writing style]** eller **[!UICONTROL Visual content]** klickar du på pilen _Expandera_ ( ![Expandera pil](../assets/do-not-localize/icon-expand-right.svg) ) för att visa information för utvärderingen.

![Utvärderingsinformation för varumärkesjustering](./assets/brands-alignment-evaluation-details.png){width="600" zoomable="yes"}

Klicka på ikonen _Helskärm_ ( ![Helskärmsikonen för detaljerade insikter](../assets/do-not-localize/icon-full-screen.svg) ) om du vill se en detaljerad vy över varje bakgrundsmusik.

Välj en flaggad stödlinje om du vill visa specifik feedback och förslag.

![Utvärderingsinformation för varumärkesjustering i helskärmsläge](./assets/brands-alignment-evaluation-details-full-screen.png){width="700" zoomable="yes"}

Du kan ändra innehållet och klicka på **[!UICONTROL Re-evaluate score]** för att köra en annan utvärdering och kontrollera om resultatet har förbättrats.

## Innehållskvalitetspoäng {#quality-score}

>[!CONTEXTUALHELP]
>id="ajo-b2b_quality_score_overview"
>title="Innehållskvalitet"
>abstract="Utvärdera den allmänna innehållskvaliteten för att identifiera potentiella problem med läsbarhet, innehållskonsekvens och effektivitet. Kvalitetsbedömningen är oberoende av varumärkesriktlinjerna."

>[!NOTE]
>
>Utvärderingen av innehållskvaliteten är oberoende av varumärkesriktlinjerna. Även om ett varumärke väljs tillämpas inte dess riktlinjer på kvalitetskontrollen. Varumärkesvalet är endast relevant för bedömning av varumärkesanpassning.

Förutom varumärkesanpassning kan ni utvärdera den allmänna innehållskvaliteten för att identifiera potentiella problem med läsbarhet, innehållets enhetlighet och effektivitet, oberoende av varumärkesriktlinjerna.

Bläddra till avsnittet **[!UICONTROL Content quality]** för att granska kvalitetsinsikter och rekommendationer.

![Utvärdering av innehållskvalitet](./assets/content-scoring-quality-insights.png){width="600" zoomable="yes"}

Markera ett flaggat objekt om du vill visa specifik feedback och förslag till åtgärder som kan förbättras. Poängen baseras på följande kategorier:

* **[!UICONTROL CTA effectiveness]**: Utvärderar hur väl din call-to-action motiverar läsarna att vidta den önskade åtgärden.
* **[!UICONTROL Subject Line]**: Utvärderar klarhet, relevans och kvalitet som får tittarna att tappa intresset för att uppmuntra e-postöppningar.
* **[!UICONTROL Readability]**: Mäter hur enkelt och engagerande ditt innehåll är för läsarna att förstå.
* **[!UICONTROL Spam Check]**: Identifierar vanliga skräppostutlösare som kan påverka leveransen.
* **[!UICONTROL Content Cohesiveness]**: Ser till att ditt innehåll flyter smidigt och hålls kvar i ämnet.
* **[!UICONTROL Proofreading]**: Kontrollerar stavning, grammatik och klarhetsproblem.

Klicka på ikonen _Helskärm_ ( ![Helskärmsikon för detaljerade insikter](../assets/do-not-localize/icon-full-screen.svg) ) om du vill se en detaljerad bild av din kvalitetspoäng.

![Helskärmsläge av utvärderingen av innehållskvalitet](./assets/content-scoring-quality-full-screen.png){width="700" zoomable="yes"}

Baserat på rekommendationerna kan du redigera innehållet för att förbättra läsbarheten, innehållets enhetlighet och övergripande kvalitet. Klicka på **[!UICONTROL Re-evaluate score]** när du har gjort ändringar för att uppdatera kvalitetspoängen.
