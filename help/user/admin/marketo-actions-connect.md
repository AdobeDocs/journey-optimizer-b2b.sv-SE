---
title: Aktivera Marketo Engage för att stödja reseåtgärder
description: Aktivera Marketo Engage-anslutningar för att stödja kundresor så att marknadsförarna kan samordna kampanjer mellan Marketo Engage och Journey Optimizer B2B edition.
feature: Integrations, Audiences, Buying Groups
role: User, Admin
source-git-commit: de7f5620556a48fe6f12ed1c70e925e11ec770f1
workflow-type: tm+mt
source-wordcount: '390'
ht-degree: 0%

---


# Aktivera Marketo Engage-instanser för att stödja åtgärder

Marketo Engage-åtgärder är _personbaserade_-åtgärder som gör att du kan koordinera din _kontobaserade_ marknadsföringssamordning mellan Journey Optimizer B2B edition och dina _lead-baserade_ marknadsföringssatsningar i Marketo Engage. Använd dessa åtgärder för att samordna statiskt listmedlemskap och för att placera personer i kampanjer.

Om du vill använda Marketo Engage-åtgärder skapar en administratör först en [anpassad tjänst](https://experienceleague.adobe.com/sv/docs/marketo-developer/marketo/rest/custom-services#) i Marketo Engage, som tillhandahåller de autentiseringsuppgifter som krävs för autentisering.
Sedan skapar en produktadministratör för Journey Optimizer B2B edition en anslutning till Marketo Engage genom att ange inloggningsuppgifterna.
Journey Optimizer B2B edition-användare kan sedan referera till anslutningen för att konfigurera Marketo Engage-åtgärder på <!-- Person and -->kontoresor, som att lägga till eller ta bort personer från Marketo Engage-listor eller lägga till dem i kampanjförfrågningar.

Synligheten för Marketo Engage-arbetsytan för resurser, som listor och kampanjer, styrs av rollbehörigheterna som tilldelats i den anpassade tjänsten.

Samma anslutning kan användas flera gånger under en resa, och olika Marketo Engage-anslutningar kan samexistera under en och samma resa.

När en åtgärd körs används markeringsprincipen för att avgöra vilka personposter i Marketo Engage som ska användas för att välja om det finns flera identifierare i den enhetliga personprofilen. Du kan välja den äldsta, senaste eller alla matchande Marketo Engage-poster. Folk går igenom resan oavsett vilken matchning de har, förutom när ett fel inträffar.

## Konfigurera en Marketo Engage-anslutning

Konfigurera en Marketo Engage-fjärrinstans för användning med Marketo Engage reseåtgärder.

### Skapa Marketo Engage anpassade tjänst

1. Logga in på Marketo Engage som administratör och skapa en anpassad tjänst.
1. Registrera följande värden som ska användas för anslutningen:

   * MUNCHKIN ID
   * Klient-ID
   * Klienthemlighet

### Lägg till integreringen

![Lägg till integreringsinformation](assets/integration-connection-details.png)

1. I Journey Optimizer B2B edition går du till **Administration** > **Konfigurationer**.
1. Välj på fliken **Integrationer**.
1. Klicka på **[!UICONTROL Create a connection]**.
1. Ange ett namn (obligatoriskt) och en beskrivning (valfritt).
1. Välj en **markeringsprincip** för matchande personposter.
1. Ange ditt Munchkin-ID, klient-ID och klienthemlighet.
1. Klicka på **[!UICONTROL Connect to Marketo]**.
1. Klicka på **[!UICONTROL Create]**.

När en marknadsförare använder en Marketo Engage-åtgärd under en resa kan de konfigurera noden med hjälp av anslutningsnamnet.

Med den slutförda integreringen är Marketo Engage-åtgärder tillgängliga från **Åtgärder på:** i nodegenskaperna.

![Marketo-åtgärdslista](assets/marketo-actions-list.png)