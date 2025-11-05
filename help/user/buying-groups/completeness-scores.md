---
title: Slutförandepoäng för inköpsgrupper
description: Beräkna kundgruppernas fullständighetspoäng med rollbaserade trösklar, anpassningsbara medlemskrav och inställningar för fullständighet i Journey Optimizer B2B edition.
feature: Buying Groups
role: User
source-git-commit: 1ebc27a709e1b82029c22950897505f3945a507f
workflow-type: tm+mt
source-wordcount: '884'
ht-degree: 2%

---


# Slutförandepoäng {#completeness-scores}

>[!CONTEXTUALHELP]
>id="ajo-b2b_buying_group_completeness_score"
>title="Slutförandepoäng"
>abstract="Slutförandepoängen visar hur väl köpgruppsmedlemskapet är anpassat för en säljklar inköpsgrupp."

Ett slutresultat är en procentandel som anger hur väl en inköpsgrupp fylls med de obligatoriska medlemmarna i sina definierade roller. Poängen baseras på tröskelvärden för rollmedlemmar som du konfigurerar i rollmallen och det faktiska antalet medlemmar som tilldelats till varje roll i inköpsgruppen. Resultatet hjälper marknadsförarna att utvärdera säljberedskapen och identifiera luckor i köpgruppssammansättningen. Resultatberäkning sker automatiskt när köpgruppsmedlemskapet ändras.

![Buying group complete scores](./assets/buying-group-details-page-completeness-scores.png){width="800" zoomable="yes"}

Det finns två typer av fullständighetspoäng:

* **Slutgiltigt resultat för köp av grupp** - Poängen för slutförande av inköpsgrupp är en procentandel mellan 0 % och 100 % och representerar den övergripande fullständigheten för inköpsgruppen baserat på beräkningar av fullständighetsnivån för roll.

  Slutgiltigt poängvärde för inköpsgrupp visas på sidan [Information om inköpsgrupp](./buying-group-details.md). Den här poängen ger en överblick över om köpgruppen har de intressenter som krävs för säljengagemang.

* **Kompletteringspoäng för roll** - Poängen för rollens fullständighet är en procentandel för varje enskild roll i en inköpsgrupp, baserat på antalet medlemmar som tilldelats den rollen.

  När du redigerar roller och justerar slutresultatet visas poängen för varje roll på informationssidan för inköpsgrupper. Med dessa poäng kan du identifiera vilka specifika roller som behöver ytterligare medlemmar för att nå det säljklara tröskelvärdet.

  På informationssidan visas de två första rollernas fullständighetspoäng med en n_+-länk för eventuella ytterligare roller. Klicka på länken om du vill visa de extra poängen för rollslutförande.

Slutpoängen återspeglar det aktuella läget för medlemskap i inköpsgrupper och uppdateras automatiskt när medlemmar läggs till eller tas bort. Visade bakgrundsmusik visas som hela procenttal (poängen 66,67 % visas till exempel som 67 %).

## Utvärdera säljberedskap

Adobe Journey Optimizer B2B edition förser marknadsförarna med verktyg som säkerställer att köpgrupperna är i linje med de verkliga beslutsprocesserna. Du kan definiera hela inköpsgrupper med anpassningsbara tröskelvärden för rollmedlemmar som återspeglar organisationens försäljningsmetod. Genom att ställa in lägsta och högsta medlemskrav för varje roll kan ni fastställa tydliga kriterier för vad som utgör en försäljningsfärdig inköpsgrupp.

Poängen för slutförande av inköpsgrupp ger ett korrekt mått på gruppens försäljningsberedskap. För att t.ex. kunna slutföra en viss lösning kan du behöva minst två beslutsfattare, en påverkare och minst en läkare. Beräkningen av fullständighetspoäng redovisar för var och en av dessa rollspecifika krav och ger en bild av den övergripande beredskapen för inköpsgrupper.

## Mät reseeffektiviteten

Att köpa hela grupper fungerar som en nyckelresultatindikator för att uppnå en effektiv kundresa. Målet för en viss resa kan vara att öka slutförandet av inköpsgrupper med en viss procentandel eller att uppnå en minimitröskel innan säljklara varningar utlöses.

I ett stort företag kan du identifiera en person per roll. Den personen kanske inte är den rätta kontakten för försäljningen eller så behöver du flera kontakter i viktiga roller. En stor organisation kan t.ex. ha flera IT-beslutsfattare fördelade över olika avdelningar eller affärsenheter. Att identifiera en beslutsfattare räcker kanske inte för en komplex företagsförsäljning.

När du har analyserat den aktuella inköpsgruppens fullständighet kan du justera antalet kontakter som krävs för varje roll i rollmallen. Dessa justeringar gör att ni kan anpassa er strategi för inköpsgrupper utifrån verkliga mönster och försäljningsresultat.

<!-- ## Analyze audiences for journey optimization

Marketers can view the starting buying group completeness score of target account audiences to find the best performance indicators for a solution. This visibility enables marketers to:

* Determine if they need to adjust the completeness score requirements for each role to make journeys more effective.
* Identify which buying groups are closest to sales-ready status and prioritize them for acceleration campaigns.
* Segment buying groups by completeness score ranges and create tailored nurture strategies for different maturity levels.

>[!BEGINSHADEBOX]

The buying group completeness score is available to use for filtering in [journey split-path-by-account nodes](../journeys/split-merge-paths-nodes.md#account-path-filters) and for audience segmentation. Role completeness can be used to create personalized content that addresses specific gaps in buying group composition.

>[!ENDSHADEBOX] -->

## Beräkning av rollfullständighet {#role-completeness-calculation}

>[!CONTEXTUALHELP]
>id="ajo-b2b_buying_group_role_completeness_calculation"
>title="Beräkning av rollfullständighet"
>abstract="Poängen för rollens fullständighet beräknas som en procentandel baserat på antalet medlemmar som tilldelats en roll."

Journey Optimizer B2B edition beräknar slutresultatet för varje enskild inköpsgruppsroll i procent. Basera detta poängvärde på hur många medlemmar som tilldelas rollen, jämfört med [det antal som krävs i rollmallen](./buying-groups-role-templates.md#change-the-completeness-score-settings) för slutförande.

Rollens fullständighetsberäkning är en linjär procentandel mellan noll och det angivna tröskelvärdet (medlemmar krävs):

* Om antalet tilldelade medlemmar är **noll** är rollens fullständighet **0%**.
* Om antalet tilldelade medlemmar är **vid eller över tröskelvärdet** är rollens fullständighet **100 %**.
* Om antalet tilldelade medlemmar är **mellan ett och tröskeln** beräknas fullständigheten proportionellt.

### Formel för rollfullständighet

Procentvärdet för rollens fullständighet beräknas med följande formel:

```text
Role Completeness % = ((Assigned Members - Threshold) / (Threshold)) × 100
```

Var:

* `Assigned Members` = Aktuellt antal medlemmar i rollen
* `Threshold` = Obligatoriskt medlemsvärde angivet i rollmallen

### Exempel på rollfullständighet

I följande exempel visas beräkningar av rollernas fullständighet med olika tröskelkonfigurationer:

| Roll | Obligatoriska medlemmar | Tilldelade medlemmar | Beräkning | Fullständighet för roll |
|------|------------------|------------------|-------------|-------------------|
| Beslutsfattare | 3 | 0 | Ingen | 0 % |
|  |  | 1 | 1/3 × 100 | 33 % |
|  |  | 2 | 2/3 × 100 | 66 % |
|  |  | 3 | Vid tröskelvärde | 100 % |
|  |  | 4 | Över tröskelvärdet | 100 % |
| Påverkande | 5 | 0 | Ingen | 0 % |
|  |   | 1 | 1/5 × 100 | 20% |
|  |   | 2 | 2/5 × 100 | 40 % |
|  |   | 3 | 3/5 × 100 | 60 % |
|  |   | 4 | 4/5 × 100 | 80% |
|  |   | 5 | Vid tröskelvärde | 100 % |
|  |   | 6 | Över tröskelvärdet | 100 % |

## Beräkning av slutförande av inköpsgrupp {#buying-group-completeness-calculation}

Poängen för slutförandegrad för inköpsgrupper aggregerar poängen för den enskilda rollens fullständighet. Den här beräkningen ger en helhetsbild av hur du kan köpa grupper för alla definierade roller.

### Slutgiltig inköpsgrupp

Procentuell fullständighet för inköpsgruppen beräknas med hjälp av följande formel:

```text
Buying Group Completeness % = Σ(Role Completeness %) / Number of defined roles
```

Var:

* `Role Completeness %` = Procent för slutförande av enskild roll (0-100 %)
* `Σ` = Summan av alla roller i inköpsgruppen

<!--

## Use completeness scores in journeys

Use buying group completeness scores and role-level completeness scores to optimize your account journeys and personalize engagement strategies.

### Split paths by completeness

Use completeness thresholds in [journey split-path-by-account nodes](../journeys/split-merge-paths-nodes.md#account-path-filters) to route buying groups through different journey paths based on their readiness. For example:

* **High completeness path** (≥70%) - Buying groups that are nearly sales-ready can be routed to sales teams or receive call-to-action campaigns
* **Medium completeness path** (40-69%) - Buying groups in active development receive nurture campaigns focused on filling specific role gaps
* **Low completeness path** (<40%) - Newly formed buying groups receive awareness and education content to build initial engagement

### Trigger actions based on completeness milestones

Set up journey events that trigger specific actions when buying groups reach completeness milestones. FOr example:

* Alert sales teams when a buying group reaches 70% completeness.
* Send a _stakeholder alignment_ campaign when completeness increases by 20% or more within a defined timeframe.
* Trigger an automated assessment when a buying group stalls at the same completeness level for an extended period.

By leveraging completeness scores throughout the journey, you create more targeted, efficient campaigns that align with the actual composition and maturity of your buying groups.

-->