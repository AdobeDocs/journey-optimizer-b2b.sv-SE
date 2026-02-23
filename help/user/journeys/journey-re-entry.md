---
title: Reseåterinträde
description: Styr när och hur ofta konton kan återföras till samma kontoresa.
feature: Account Journeys
role: User
level: Intermediate
source-git-commit: 696d3a57a1c086a25670ffb41cd095d4da011615
workflow-type: tm+mt
source-wordcount: '406'
ht-degree: 0%

---


# Reseåterinträde

_Endast kontoresor_

När du aktiverar återregistrering för en kontoresa kan du styra när och hur ofta ett konto kan återkomma till samma resa. Använd inställningarna för ny registrering för att ställa in villkor, begränsningar och väntetider så att konton kan kvalificeras på ett kontrollerat sätt.

Ett konto kan begära en resa när följande saker är sanna:

* Kontot är inom det tillåtna antalet återregistreringar för resan.
* Kontot har uppnått väntetiden (den kortaste väntetiden innan det anropas).
* Kontot befinner sig för närvarande inte på resan.

## Aktivera återregistrering för en kontoresa

Du kan aktivera återinträde och ändra inställningarna för återinträde när resan är i statusen _Utkast_.

1. Öppna utkastet till kontoresa.

1. Klicka på menyn **[!UICONTROL More...]** längst upp till höger och välj **[!UICONTROL Re-entry]**.

   ![Klicka på Mer längst upp till höger](./assets/account-journey-draft-more-menu.png){width="450"}

1. I dialogrutan _[!UICONTROL Journey re-entry]_&#x200B;växlar du till alternativet **[!UICONTROL Enable re-entry]**.

   När funktionen är aktiverad visas alternativen för timing, delay och limits.

   ![Dialogrutan för återinträde på resan med den aktiverade funktionen](./assets/journey-re-entry-dialog-enabled.png){width="450"}

1. Välj hur väntetiden ska beräknas för **[!UICONTROL Re-entry timing]**:

   * **[!UICONTROL Wait from end of journey]** - Vänteperioden börjar när kontot avslutar eller slutför resan. Exempel:&quot;30 dagar efter att kontot har slutfört resan kan de registrera sig igen.&quot;

   * **[!UICONTROL Wait from start of journey]** - Vänteperioden baseras på när kontot först gick in på resan. Exempel:&quot;30 dagar från det att kontot startade resan kan de registrera sig igen.&quot;

1. Ange **[!UICONTROL Re-entry delay]**, som är väntetiden i timmar eller dagar.

   Den här inställningen avgör hur länge ett konto måste vänta efter att resan har avslutats eller påbörjats innan det kan gå in igen.

1. Ange **[!UICONTROL Entry limit]** för att definiera det maximala antal gånger som ett konto tillåts gå in på resan.

   När ett konto når gränsen är det inte längre kvalificerat för registrering förrän gränsen har återställts eller tills resan publiceras på nytt med en ny gräns.

   Denna gräns gäller per konto för den resan.

1. Klicka på **[!UICONTROL Save]**.

## Kontoutveckling och aktivitet

För en publicerad kontoresa visas [kontoförloppet](./journeys-overview.md#review-account-progression) för resenoderna på färdkartan. Varje nod på kartan visar antalet konton som ska nå den noden och, för direktresor, antalet konton på den noden. Varje gång ett konto återförs till en resa räknas det som en separat post.
<!-- You can see how many times accounts have entered the journey. ?? -->

När du fördjupar dig i [kontoinformation](../accounts/account-details.md) visas kontoaktiviteten varje gång som kontot registreras på resan. Den innehåller explicit aktivitet och ett antal återkommande så att du kan se nya poster tydligt.
