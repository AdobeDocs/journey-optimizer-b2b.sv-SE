---
title: Konfigurationer av webbkanaler
description: Lär dig hur du konfigurerar inställningar för webbkanaler för att definiera webbegenskaper och sidmatchningsregler för innehållsleverans i Journey Optimizer B2B edition.
feature: Setup, Channels
role: Admin
badgeBeta: label="Beta" type="informative" tooltip="Den här funktionen är för närvarande i en begränsad betaversion"
source-git-commit: 2f9b007df233cf8a233c3646bf691b7cff139f86
workflow-type: tm+mt
source-wordcount: '983'
ht-degree: 0%

---

# Konfigurationer av webbkanaler

En webbkonfiguration är en webbegenskap som identifieras av en URL där innehållet levereras. Den kan matcha en eller flera sidor på en sida så att webbupplevelsen kan leverera ändringar på en eller flera webbsidor. Dessa konfigurationer krävs för att marknadsförare ska kunna [lägga till åtgärdsnoder för webbanpassning på resor](../content/web-experiences.md#create-a-web-experience) och för att [utforma upplevelseändringarna](../content/web-experience-design.md) för en kampanj.

>[!BEGINSHADEBOX]

**Förutsättningar**

Om du vill använda webbkanaler måste din webbplats ha [Adobe Experience Platform Web SDK](https://experienceleague.adobe.com/en/docs/experience-platform/collection/js/js-overview) (`alloy.js`) implementerat för besöksidentifiering och innehållsleverans. Kontrollera att Adobe Experience Platform Web SDK version är 2.16 eller senare.

Webbkanalskonfigurationen i Journey Optimizer B2B edition kräver följande [behörigheter](../admin/user-management.md#b2b-product-permissions):

* _[!UICONTROL Channel Configurations]_>_[!UICONTROL Manage Messages Presets]_ - Krävs för att skapa, uppdatera och ta bort webbkanalskonfigurationer.
* _[!UICONTROL Channel Configurations]_>_[!UICONTROL View Messages Presets]_ - krävs för att visa webbkanalskonfigurationer.

>[!ENDSHADEBOX]

## Skapa en webbkanalskonfiguration

1. Gå till **[!UICONTROL Administration]** > **[!UICONTROL Channels]** i den vänstra navigeringen.

1. Välj _[!UICONTROL Web]_&#x200B;under **[!UICONTROL Channel configurations]**&#x200B;i navigeringspanelen.

   ![Få åtkomst till webbkanalskonfigurationerna](./assets/config-web-channels.png){width="800" zoomable="yes"}

1. Klicka på **[!UICONTROL Create channel configuration]** överst till höger.

1. Ange **[!UICONTROL Name]** (obligatoriskt) och **[!UICONTROL Description]** (valfritt) för konfigurationen.

   >[!NOTE]
   >
   >Namn måste börja med en bokstav (A-Z) och får bara innehålla alfanumeriska tecken. Du kan också använda understreck `_`, punkt `.` och bindestreck `-`.

1. Välj något av följande alternativ i avsnittet **[!UICONTROL Web settings]**:

   * **[!UICONTROL Single page]** - Om du vill tillämpa ändringarna på endast en sida anger eller väljer du **[!UICONTROL Page URL]**.

     ![Välja en sidadress för en enkelsidig webbkanalskonfiguration](./assets/config-web-channel-create-single-page.png){width="600" zoomable="yes"}

   * **[!UICONTROL Pages matching rule]** - Om du vill ha flera URL:er som matchar samma regel som mål skapar du en [sida som matchar regeln](#build-a-pages-matching-rule) och anger en **[!UICONTROL Default authoring and preview URL]**.

1. Klicka på **[!UICONTROL Submit]** om du vill spara ändringarna.

När du har sparat konfigurationen har den statusen _Utkast_ och är tillgänglig för marknadsförare när de använder en webbkanal på sina resor. Du kan fortsätta redigera konfigurationen så länge den är i utkastläge. Du kan också ta bort ett utkast till en webbkanalskonfiguration genom att klicka på ikonen _Mer_ (**..**) bredvid namnet och välja **[!UICONTROL Delete]**.

Så snart webbkanalen används i en resa, flyttas den till statusen _Aktiv_. I det här läget kan du redigera namnet och beskrivningen för konfigurationen. Du kan inte ändra webbinställningarna eller ta bort konfigurationen.

## Sidmatchningsregler {#pages-matching-rule}

När du skapar en webbkonfiguration kan du skapa en _[!UICONTROL Pages matching rule]_&#x200B;som mål för flera URL:er som matchar samma regel. Med de här reglerna kan du tillämpa samma innehållsändringar på flera sidor.

Du kan till exempel lägga till ändringar i en hjältebanderoll på en hel webbplats, eller lägga till en toppbild som visas på alla produktsidor.

### Bygg en regel

1. Välj [&#x200B; när du &#x200B;](#create-a-web-channel-configuration)skapar en webbkanalskonfiguration **[!UICONTROL Page matching rule]**.

1. Definiera dina villkor för fälten **[!UICONTROL Domain]** och **[!UICONTROL Page]** med hjälp av de olika operatorerna i varje avsnitt för att skapa regeln.

   +++Domänoperatörer

   Använd följande operatorer för att matcha domäner enligt strängvärdet som du anger:

   | Operator | Beskrivning | Exempel |
   | --- | --- | --- |
   | [!UICONTROL Equals] | Exakt domänmatchning. | |
   | [!UICONTROL Starts with] | Matchar alla domäner (inklusive underdomäner) som börjar med den angivna strängen. | `Starts with: dev` matchar alla domäner och underdomäner som börjar med `dev`, till exempel `dev.example.com`, `dev.products.example.com` och `developer.example.com` |
   | [!UICONTROL Ends with] | Matchar alla domäner (inklusive underdomäner) som slutar med den angivna strängen. | `Ends with: example.com` matchar alla domäner och underdomäner som slutar med `example.com`, till exempel `stage.example.com`, `prod.example.com` och `myexample.com` |
   | [!UICONTROL Wildcard matching] | Gör att du kan definiera en jokerteckenmatchning mitt i strängen, till exempel `dev.*.example.com`. Valideringsreglerna kräver att värdet innehåller ett och endast ett jokertecken (asterisk) när operatorn är _jokerteckenmatchning_. | `Wildcard matching: dev.*.example.com` matchar domäner som `dev.products.example.com`, `dev.mytest.products.example.com` och `dev.blog.example.com` |
   | [!UICONTROL Any] | Matchar alla domäner. Det är användbart när du testar en viss sökväg över domäner. | |

   +++

   +++Banoperatorer

   Använd följande operatorer för att matcha sökvägar enligt strängvärdet som du anger:

   | Operator | Beskrivning | Exempel |
   | --- | --- | --- |
   | [!UICONTROL Equals] | Exakt matchning av sökvägen. | |
   | [!UICONTROL Starts with] | Matchar alla sökvägar (inklusive delsökvägar) som börjar med strängen. | |
   | [!UICONTROL Ends with] | Matchar alla sökvägar (inklusive delsökvägar) som slutar med strängen. | |
   | [!UICONTROL Any] | Matchar alla sökvägar. Det är användbart när du riktar in dig på alla banor under en eller flera domäner. | |
   | [!UICONTROL Wildcard matching] | Gör att du kan definiera ett internt jokertecken i sökvägen, till exempel `/products/*/detail`. Jokertecknet `*` i sökvägskomponenten matchar alla teckensekvenser fram till det första `/`-tecknet.  Och `/*/` matchar alla teckensekvenser (inklusive delbanor). | `Wildcard matching: /products/*/detail` matchar sökvägar som `example.com/products/yoga/detail`, `example.com/products/surf/detail`, `example.com/products/tennis/detail` och `example.com/products/yoga/pants/detail` |
   | [!UICONTROL Contains] | Värdet översätts till ett jokertecken, till exempel `*mystring*`, och matchar alla sökvägar som innehåller teckensekvensen. | `Contains: product` matchar alla sökvägar som innehåller strängen `product`, till exempel `example.com/products`, `example.com/yoga/perfproduct`, `example.com/surf/productdescription` och `example.com/home/product/page` |

   +++

   Om du till exempel vill ha stöd för innehållsändringar på alla _LumaSecure_ -lösningssidor på din _Bodea_ -webbplats väljer du **[!UICONTROL Domain]** > **[!UICONTROL Starts with]** > `bodea` och **[!UICONTROL Page]** > **[!UICONTROL Contains]** > `lumasecure` .

   ![Definierar en sidmatchningsregel för en webbkanalskonfiguration](./assets/config-web-channel-pages-matching-rules.png){width="600" zoomable="yes"}

1. Om ditt användningsfall kräver flera regler klickar du på **[!UICONTROL Add another page rule]** och upprepar föregående steg.

   * Du kan definiera upp till 10 regler.

   * Använd operatorerna **[!UICONTROL Or]** eller **[!UICONTROL Exclude]** mellan de olika reglerna.

     _[!UICONTROL Or]_&#x200B;är standardoperator för att definiera flera regler och är användbar när du vill lägga till flera villkorsdefinitioner som kan matchas.

     _[!UICONTROL Exclude]_&#x200B;är användbart när en av sidorna som matchar den definierade regeln inte ska ha något mål. Du kan till exempel ange alla `bodea.com` sidor som innehåller `lumasecure` som mål, men inte bloggsidor (till exempel `bodea.com/blogs/lumasecure/latest-release`).

   ![Sidor som matchar regler med undantag](./assets/config-web-channel-pages-matching-rules-exclude.png){width="600" zoomable="yes"}

1. Ange **[!UICONTROL Default authoring and preview URL]**.

   Det här steget ser till att de sidor som genereras eller matchas av regeln har en angiven URL-adress för design av webbupplevelseinnehåll och förhandsgranskning.

## Duplicera en webbkanal

Du kan duplicera en befintlig webbkanalskonfiguration och ändra den för att skapa en ny webbkanal baserad på en befintlig. Det går inte att ändra en aktiv webbkanalskonfiguration som har sparats i biblioteket.

1. Klicka på ikonen _Mer meny_ (**..**) för varianten och välj **[!UICONTROL Duplicate]**.

   ![Klicka på ikonen för fler nya för att duplicera en befintlig webbkanalskonfiguration](./assets/config-web-channels-more-menu.png){width="450"}

   Den här åtgärden skapar en duplicerad webbkanal med `_Copy_nnn` som tillägg till namnet.

1. Klicka på namnet på den duplicerade webbkanalen för att redigera parametrarna.

   * Ändra namnet och beskrivningen så att de matchar syftet eller objekten i regeln.
   * Ändra URL:en för en sida om det behövs.
   * Ändra vid behov sidmatchningsregeln enligt dina önskemål.

1. När konfigurationen är klar klickar du på **[!UICONTROL Submit]**.
