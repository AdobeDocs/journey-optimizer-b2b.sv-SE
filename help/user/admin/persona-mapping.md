---
title: Personamappning
description: Lär dig hur du konfigurerar profiler för kontobaserad marknadsföring genom att mappa personattribut för att skapa anpassade rollmallar för inköpsgrupper.
feature: Setup, Buying Groups
hide: true
hidefromtoc: true
badgeBeta: label="Beta" type="informative" tooltip="Den här funktionen är för närvarande i en begränsad betaversion"
role: Admin
source-git-commit: e301dfd5ac1421eb73e80b1d772d1b17f9ef3a1e
workflow-type: tm+mt
source-wordcount: '877'
ht-degree: 0%

---

# Personmappning

Personerna är en viktig aspekt av kontobaserad marknadsföring (ABM) eftersom de hjälper marknadsförarna att anpassa sina strategier till specifika behov, preferenser och utmaningar för individer inom målkonton. Marknadsförarna kan skapa detaljerade profiler för varje enskild person, inklusive bakgrund, ansvarsområden, smärtor och önskade kommunikationskanaler. Med dessa definitioner kan administratörer konfigurera profiler utifrån personattribut i Journey Optimizer B2B edition så att rollmallar kan använda effektiva och konsekventa rollvillkor som fångar dessa profiler.

<!-- Currently there is no insight into what persona goes into what role. With buying group agent, when asked questions about, what should be the size of the buying group, what persona should be in that buying group, what role do they play, etc, then agent will analyze all the data, (opportunity data, engagement data, sales conversation, etc) and informs the user that the buying group needs 7 persona, e.g.CMO, VP of marketing, marketing leader, Marketing ops, etc. 

Then based on what agent informed, users can create a template with those personas. -->
Persondefinitioner och användningsbegränsningar:

* Du kan ha upp till 20 personer definierade i listan _[!UICONTROL Persona mapping]_.
* Varje person kan innehålla upp till fem attribut i sin definition.
* För alla definierade profiler kan du använda upp till tio olika personattribut.

>[!BEGINSHADEBOX]

**Använd skiftläge: jobbtitelvariationer**

Många marknadsförings- och säljteam använder befattningar som ett sätt att identifiera olika personer inom ett konto. Men titlar för kontakter kan vara inkonsekventa och använda flera varianter för liknande roller. När du skapar mallar för inköpsgrupproller kan det krävas att du definierar alla möjliga relaterade befattningar för en viss roll. Ni kan förenkla dessa definitioner och ta med personer med liknande befattningar under en viss person, som ni sedan kan använda i olika rollmallar för att köpa grupper.

Du kan till exempel konfigurera en person med namnet _Product Management_ och definiera den med jobstitelattributet för värdena för _Product Manager_, _Sr. Product Manager_, _Senior Product Manager_, _PM_, _Sr. PM_, _Principal PM_ och _Principal Product Manager_. Använd sedan den här personen i en rollmall där villkoret matchar för _Persona är Produkthantering_. När du använder den konfigurerade rollen blir det smidigare att skapa varje rollmall och det behövs inget komplicerat villkor som kan matcha mot alla möjliga befattningar.

>[!ENDSHADEBOX]

## Få åtkomst till konfigurerade profiler

1. Välj **[!UICONTROL Administration]** > **[!UICONTROL Configurations]** i den vänstra navigeringen.

1. Klicka på **[!UICONTROL Persona mapping]** på den mellanliggande panelen för att visa listan över profiler.

   ![Få åtkomst till konfigurerade profiler](./assets/configuration-engagement-scoring-list.png){width="800" zoomable="yes"}

   Från den här sidan kan du [skapa](#create-an-engagement-score-model), [redigera](#change-the-engagement-weighting-settings) eller [ta bort](#delete-a-persona) profiler.

   Personmappningslistan. är organiserat som en tabell och visar de senast uppdaterade personerna högst upp (sorterat efter _[!UICONTROL Last update]_). Du kan anpassa den visade tabellen genom att klicka på ikonen_ Kolumninställningar _( ![Kolumninställningar](../assets/do-not-localize/icon-column-settings.svg) ) i det övre högra hörnet och markera eller avmarkera kryssrutorna för kolumner.

![Kolumner att visa i personmappningslistan](./assets/configuration-engagement-scoring-list-columns.png){width="300"}

1. Klicka på namnet om du vill komma åt informationen för en person.

### Standardprofiler

Listan _Personmappning_ innehåller fem standardprofiler som har definierats enligt jobbnamnsattributet. Du kan redigera vilken som helst av dessa standardprofiler beroende på organisationens behov:

| Persona | Jobbtitlar |
| ------- | ---------- |
| CXO/EVP - CXO/Executive Vice President | VD, CIO, CTO, CMO, CFO, Executive Vice President of Strategy |
| SVP/VP - Senior Vice President/Vice President | SVP of Marketing, VP of Sales, SVP of Operations, VP of Product, VP of IT |
| Senior Director/Director - Senior Director/Director | Director of Engineering, Senior Director of Product, Director of Finance, Director of Customer Success |
| Senior Manager/Manager - Senior Manager/Manager | Senior Marketing Manager, IT Manager, Operations Manager, Sales Manager, HR Manager |
| Enskild deltagare - enskild deltagare | Account Executive, Software Engineer, Marketing Specialist, Customer Success Representant |
| Analytiker - analytiker | Business Analyst, Data Analyst, Market Research Analyst, Financial Analyst, Operations Analyst |
| Utvecklare - utvecklare | Front-End Developer, Back-End Developer, Full-Stack Developer, Mobile App Developer, DevOps Engineer |
| Yrkespersonal - Yrkespersonal | HR-specialist, juridisk rådgivare, efterlevnadsansvarig, projektledare, inköpsspecialist |
| Konsult - konsult | Management Consultant, IT Consultant, Business Process Consultant, Marketing Consultant |
| Övrigt - Annat | Branschspecialist, oberoende rådgivare, frilanskonsult, ämnesexpert |

### Listfiltrering

Använd sök- och filterverktygen för att hitta den profil du vill ha:

* Ange en textsträng i sökfältet för att matcha persona efter namn,

  ![Filtrera de händelsedefinitioner som visas](./assets/configuration-events-defs-list-filtered.png){width="700" zoomable="yes"}

* Klicka på ikonen _Filter_ ( ![Filterikon](../assets/do-not-localize/icon-filter.svg) ) längst upp till vänster om du vill filtrera den visade listan med något av dessa attribut:

   * ?
   * ?

## Skapa en persona

1. Välj **[!UICONTROL Administration]** > **[!UICONTROL Configuration]** i den vänstra navigeringen.

1. Klicka på **[!UICONTROL Persona mapping]** i panelen Mellan.

1. Klicka på **[!UICONTROL Create persona]**.

1. Ange en unik **[!UICONTROL Name]** och **[!UICONTROL Description]** (valfritt) för personen.

1. Välj de attribut som ska användas för att matcha persona.

   * Klicka på **[!UICONTROL Select person attributes]**.

   * I dialogrutan _[!UICONTROL Select person attributes]_markerar du kryssrutan för varje attribut som du vill mappa (högst fem).

     Du kan anpassa den visade tabellen genom att klicka på ikonen _Kolumninställningar_ ( ![Kolumninställningar](../assets/do-not-localize/icon-column-settings.svg) ) i det övre högra hörnet.

     Om du vill filtrera attributlistan efter namn anger du en textsträng i sökfältet. Du kan också klicka på ikonen _Filter_ ( ![Filterikon](../assets/do-not-localize/icon-filter.svg) ) längst upp till vänster om du vill filtrera den visade listan efter typ, _Standard_ eller _Egen_.

   * Klicka på **[!UICONTROL Save]**.

     De markerade attributen fylls i i avsnittet _[!UICONTROL Persona attributes]_.

1. För varje attribut anger du de kommaavgränsade värden som du vill matcha för attributet.

   I stället för ett värde kan du också lägga till en fråga som kan användas för att identifiera en matchning. Du kan till exempel skriva

1. Klicka på **[!UICONTROL Create]**.

## Redigera en profil

1. Klicka på namnet för att få tillgång till informationen om den aktuella personen.


## Ta bort en persona

Om du tar bort en profil tas den bort från listan _Personmappning_ och kan inte längre användas i rollmallar.

1. På sidan _[!UICONTROL Persona mapping]_letar du reda på den profil du vill ta bort.

1. Klicka på ellipsikonen (**..**) bredvid namnet för och välj **[!UICONTROL Delete]**.

1. Klicka på **[!UICONTROL Delete]** i bekräftelsedialogrutan.
