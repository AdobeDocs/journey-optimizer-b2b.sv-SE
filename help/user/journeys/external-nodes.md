---
title: Externa noder
description: Lär dig hur du använder noder för Extern åtgärd och Extern delad sökväg i kontoresor för att ansluta till externa tjänster och dirigera konton och personer baserat på servicesvaret.
feature: Account Journeys, Integrations
role: User
source-git-commit: c88ea3ce8c17e78b3e48cb3c2f9951358e822618
workflow-type: tm+mt
source-wordcount: '833'
ht-degree: 0%

---

# Externa noder

Använd externa noder för att koppla kontoresan till en extern tjänst. När en kontopublik når någon av dessa noder skickar Journey Optimizer B2B edition asynkront målgruppsattributdata till den externa tjänsten. Tjänsten bearbetar data och svarar med ett återanrop, som returnerar målgruppsinformation och metadata som resan använder för att fortsätta.

>[!NOTE]
>
>Externa åtgärdsnoder är bara tillgängliga för kontoresor. De stöds inte på personresor.
>
>En administratör måste [konfigurera och aktivera den externa åtgärden](../admin/configure-external-actions.md) innan marknadsförare kan lägga till och implementera dessa noder under en resa.

Det finns två externa åtgärdsnodtyper:

* **[Extern åtgärd](#external-action)** - Anropar en extern tjänst och fortsätter längs en enda utgående sökväg. Använd den här noden när du vill utlösa en extern process utan förgreningslogik, till exempel uppdatera en post i ett externt system eller skicka en signal till en tjänst längre fram i kedjan.
* **[Externa delade sökvägar](#external-split-paths)** - Anropar en extern tjänst och utvärderar svaret för att dirigera konton längs en av flera definierade sökvägar. Använd den här noden när den externa tjänsten returnerar ett värde, till exempel poäng, nivå eller klassificering, som bestämmer nästa steg i resan.

## Extern åtgärdsnod {#external-action}

Noden _Extern åtgärd_ anropar en extern tjänst och fortsätter längs en enda utgående sökväg, oavsett svarsinnehåll. Använd den för integreringar där ingen förgrening behövs efter det externa anropet.

1. Navigera till kundresekartan.

1. Klicka på plusikonen ( **+** ) på en bana och välj **[!UICONTROL External action]**.

   ![Lägg till en extern åtgärdsnod](./assets/node-external-action.png){width="400"}

1. I nodegenskaperna till höger anger du kontexten **[!UICONTROL Action on]** för den externa åtgärden:

   * Välj **[!UICONTROL Accounts]** när du vill använda den externa åtgärden för alla personer som är en del av konton på nodsökvägen.
   * Välj **[!UICONTROL People]** när du vill tillämpa en ändring på alla personer i nodsökvägen.

1. Välj det externa **[!UICONTROL Service name]**.

   ![Nod för extern åtgärd - välj extern tjänst](./assets/node-external-action-service-name.png){width="600" zoomable="yes"}

   Listan innehåller alla konfigurerade externa åtgärder som är aktiva och avsedda för typen _Extern åtgärd_ och kontexten.

1. Om tjänsten har globala attribut anger du obligatoriska värden i fälten som visas under tjänstnamnet.

1. Fortsätt bygga resan från nodens utgående banor.

   Sökvägen _[!UICONTROL Timeout or error]_&#x200B;skapas automatiskt. Om timeoutperioden (som konfigurerats i tjänsten) förfaller innan ett svar tas emot, förskjuts kontot eller personen den här sökvägen. Det är detsamma om ett felsvar tas emot. Du kan lägga till resenoder på den här vägen för att hantera dessa scenarier, eller så avslutas resan för målgruppsmedlemmen.

## Nod för externa delade sökvägar {#external-split-paths}

Noden Externa delade sökvägar anropar en extern tjänst och använder svaret för att avgöra vilka sökvägskonton som kommer härnäst. Varje sökväg definieras av ett villkor som baseras på en variabel (accessor) som returneras av den externa tjänsten. Under resan utvärderas svaret mot de definierade villkoren för sökväg och varje konto dirigeras längs den första matchande sökvägen. Sökvägsvillkoren utvärderas i den nedrullningsbara ordningen. Varje konto fortsätter längs den första sökvägen vars villkor matchar det värde som returneras av den externa tjänsten.

1. Navigera till kundresekartan.

1. Klicka på plusikonen ( **+** ) på en bana och välj **[!UICONTROL External split paths]**.

   ![Lägg till en extern delad sökvägsnod](./assets/node-external-split-path.png){width="400"}

1. Välj en **[!UICONTROL Split paths by]**-typ i nodegenskaperna till höger:

   * **[!UICONTROL Accounts]** - För delade sökvägar efter konton kan du lägga till både konto- och personnoder inom de definierade sökvägarna.
   * **[!UICONTROL People]** - För delade sökvägar efter personer kan du bara lägga till personåtgärdsnoder inom de definierade sökvägarna. En personbaserad delning stängs automatiskt med en _[!UICONTROL Merge paths]_-nod så att alla personer kan gå vidare till nästa steg utan att kontextkontexten försvinner.

1. Välj **[!UICONTROL Service name]**.

1. Om tjänstkonfigurationen har _globala attribut_ anger du obligatoriska värden i fälten som visas under tjänstnamnet.

1. Definiera förgreningsvillkoret för _[!UICONTROL Path 1]_:

   * För **[!UICONTROL Label]** ersätter du standardvärdet med en mer beskrivande etikett.
   * För **[!UICONTROL Select variable]** väljer du en accessor. Åtkomstanser är värden som returneras av den externa tjänsten och definieras när åtgärden konfigureras.
   * För **[!UICONTROL Select operator]** väljer du operatorn.
   * Ange det värde som ska matchas mot **[!UICONTROL Enter values]**.

   ![Extern delad sökvägsnod - ange sökvägsvillkor med en tjänstvariabel](./assets/node-external-split-path-properties.png){width="600" zoomable="yes"}

   >[!NOTE]
   >
   >De tillgängliga villkorsvariablerna och den resekontext som stöds (_Konto_, _Personer_ eller _Personer i Konto_) bestäms av konfigurationen för den externa åtgärden. Kontakta administratören om de förväntade tjänsterna eller variablerna inte är tillgängliga.

1. Om du vill lägga till fler sökvägar klickar du på **[!UICONTROL Add path]** och definierar ett villkor för var och en av dem.

1. Fortsätt bygga resan från varje utgående sökväg i noden.

   Sökvägen _[!UICONTROL Timeout or error]_&#x200B;skapas automatiskt. Om timeoutperioden (som konfigurerats i tjänsten) förfaller innan ett svar tas emot, förskjuts kontot eller personen den här sökvägen. Det är detsamma om ett felsvar tas emot. Du kan lägga till resenoder på den här vägen för att hantera dessa scenarier, eller så avslutas resan för målgruppsmedlemmen.

1. För _Dela efter konto_ kan du lägga till en [sammanfogningssökvägsnod](./split-merge-paths-nodes.md#merge-paths) för att kombinera två eller flera sökvägar efter behov.
