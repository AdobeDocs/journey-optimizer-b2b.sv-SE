---
title: Vänta noder
description: Använd väntenoder för att pausa resans förlopp och kontrollera sluttider efter varaktighet, datum eller avancerade inställningar för dag och tid.
feature: Account Journeys, Person Journeys
role: User
exl-id: fecab788-4e8e-490a-bcca-bc3ab43411d9
source-git-commit: 7a05e6aed76d15aa6d0d0a7dd244bf299d549782
workflow-type: tm+mt
source-wordcount: '684'
ht-degree: 0%

---

# Vänta noder

Använd en _Wait_-nod om du vill pausa reseförloppet under en viss tid innan du går vidare till nästa steg.

Du kan definiera väntetiden på två sätt:

* Ett specifikt datum när du vill gå vidare till nästa nod i resan
* En relativ varaktighet (antal minuter, timmar, dagar, veckor eller månader)

## Lägg till väntenoden

1. Navigera till resekartan.

1. Klicka på plusikonen ( **+** ) på en bana och välj **[!UICONTROL Wait]**.

   ![Lägg till resenod - vänta](./assets/add-node-wait.png){width="440"}

1. I nodegenskaperna till höger anger du **[!UICONTROL Type]** tid att vänta innan resan fortsätter till nästa nod i sökvägen.

   * **[!UICONTROL Duration]** - Definiera ett visst antal dagar, timmar eller minuter som ska förflyta mellan inmatning och avslut av väntenoden.
   * **[!UICONTROL Date]** - Ange ett specifikt datum och en speciell tid för avslutningen.

   ![Resensnod - vänta](./assets/node-wait.png){width="500"}

## Avancerade vänteinställningar

Aktivera alternativet **[!UICONTROL Must end on]** om du vill konfigurera ett _avancerat väntesteg_ och se till att dina meddelanden når personer och kontomedlemmar vid rätt tidpunkt. Den här konfigurationen ger dig exakt kontroll över när en person eller ett konto lämnar ett väntesteg och fortsätter till nästa nod på resan. I stället för ett fast antal timmar eller dagar från inträde till avslut kan du schemalägga åtgärder som ska utföras vid specifika tidpunkter och på specifika veckodagar.

Med ett _avancerat väntesteg_ definierar du **_när_** personen eller kontot ska avslutas, inte bara hur länge de ska vänta.

![Resensnod - avancerat väntesteg](./assets/node-wait-advanced.png){width="500"}

>[!AVAILABILITY]
>
>Avancerade vänteinställningar är tillgängliga för [!DNL Journey Optimizer B2B Edition]-miljöer som har etablerats på den [förenklade arkitekturen](../simplified-architecture.md).

### Väntetyper

| Väntetyp | Beskrivning | Konfiguration |
| --------- | ----------- | ------------- |
| **Angiven tid på dagen** | Vänta tills en viss tid (till exempel 09:00):00 | Ange tid (timme och minut). Avslutar vid nästa förekomst av den tiden (för den valda tidszonen). |
| **Specifik veckodag** | Håll kvar till en viss dag (t.ex. tisdag) | Välj en veckodag. Om ingen tid anges avslutas vid midnatt (för den valda tidszonen) på nästa matchande dag. |
| **Dagsintervall eller kombination** | Håll kvar en dag inom ett intervall (t.ex. måndag-fredag) eller någon av de angivna dagarna | Välj måldagar. Om ingen tid anges avslutas vid midnatt (för den valda tidszonen) på nästa matchande dag. |
| **Kombination av tid och dag** | Kombinera båda för exakt schemaläggning (till exempel tisdag klockan 10:00 AM) | Välj måldagar och ange måltid. Avslutar vid nästa dag/tid-förekomst (för den valda tidszonen). |

### Vanliga scenarier

Följande scenarier visar hur du kan använda typiska scenarier för din väntenodskonfiguration:

+++E-postankomst under kontorstid

**Scenario:** Du marknadsför till B2B-kunder som läser e-post på jobbet. Du vill att alla e-postmeddelanden ska anlända under kontorstid.

**Lösning:** Konfigurera väntesteget för att frigöra leads kl. 9:00 på vardagar (måndag-fredag). Oavsett när ett lead går in i väntenoden får de ditt e-postmeddelande under arbetstid.

+++

+++Enhetliga sändningstider för dynamiska målgrupper

**Scenario:** Din målgrupp ändras dagligen när nya konton eller leads kvalificeras. Ni vill att alla leads ska få det första e-postmeddelandet samtidigt, oavsett när de är kvalificerade.

**Lösning:** Ange att väntesteget ska avslutas vid en viss tidpunkt (till exempel 02:00). :00 Alla leads, oavsett om de kvalificerar sig vid midnatt eller tolv, avslutar väntesteget tillsammans klockan 10:00.

+++

+++Uppföljningsuppgifter som följer SLA

**Scenario:** Säljteamet har en SLA som varar i två arbetsdagar för att följa upp marknadsföringskvalificerade leads. Helger räknas inte.

**Lösning:** Konfigurera väntesteget så att leads endast frigörs på arbetsdagar. En lead som är kvalificerad på fredag dirigeras för uppföljning måndag eller tisdag, inte över helgen.

+++

### Exempel på in- och utträde

| Väntekonfiguration | Konto/lead-poster | Konto/lead-utträde |
| ------------------ | ------------------- | ------------------ |
| 09:00 AM, vilken dag som helst | Måndag 11:00 | Tisdag 09:00 |
| 09:00 AM, vilken dag som helst | Måndag 7:00 | Måndag 9:00 |
| Tisdag, ingen tid angiven | Fredag 3:00 | Tisdag 01:00:00:00 |
| 10:00 AM, måndag-fredag | Lördag 2:00 PM | Måndag 10:00 |
| 10:00 AM, måndag-fredag | Onsdag 8:00 AM | Onsdag 10:00 AM |
