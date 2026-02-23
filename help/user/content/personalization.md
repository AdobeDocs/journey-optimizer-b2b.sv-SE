---
title: Innehållspersonalisering
description: Anpassa B2B-mejl med konto-, person- och systemtokens i Journey Optimizer B2B edition. Lär dig använda personaliseringsredigeraren och syntaxen.
feature: Personalization, Content Design Tools, Email Authoring
topic: Personalization
role: User, Developer
level: Intermediate
keywords: uttryck, redigerare, start, personalisering
exl-id: 60bf2e06-8d6e-4cc4-8aff-5c5ca11f05ab
source-git-commit: 10e02b821609c48b82ea0248501daa60de6daa12
workflow-type: tm+mt
source-wordcount: '744'
ht-degree: 0%

---

# Innehållspersonalisering {#add-personalization}

>[!CONTEXTUALHELP]
>id="aj-b2b_personalization"
>title="Personalisera innehållsupplevelser"
>abstract="Använd **Adobe Journey Optimizer B2B edition** för att anpassa dina meddelanden till varje specifik mottagare genom att utnyttja de data och den information du har om dem. Det kan vara deras förnamn, bransch, titel med mera."

Med personaliseringsfunktionerna i [!DNL Adobe Journey Optimizer B2B Edition] kan du anpassa dina e-postmeddelanden till varje specifik mottagare genom att utnyttja de data och den information du har om dem. Det kan vara deras förnamn, bransch, titel med mera.

Med _anpassningsredigeraren_ kan du välja, ordna, anpassa och validera alla data för att skapa en anpassad personalisering för ditt innehåll. Använd olika verktyg, till exempel hjälpfunktioner, för att skräddarsy meddelanden. Redigeraren använder en infogad personaliseringssyntax som baseras på _Handlebars_, där uttryck konstrueras med innehåll omslutet av dubbla klammerparenteser `{{}}`.

När du bearbetar meddelandet ersätter Journey Optimizer B2B edition uttrycket med data som finns i Adobe Experience Platform datamängd och lokala systemvärden. Till exempel blir `Hello {{profile.person.name.firstName}} {{profile.person.name.lastName}}` dynamiskt `Hello John Doe`.

Med den här syntaxen kan du personalisera meddelanden i flera fält, inklusive ämnesrader, meddelandetexter och avsändarinformation.

## Personalization tokens

I [!DNL Journey Optimizer B2B Edition] kan du skapa ditt dynamiska e-postinnehåll med hjälp av personaliseringstoken:

* **Kontotoken** - Dessa token baseras på kontoattributen, till exempel _kontonamn_, _bransch_ och _antalet anställda_. Använd dessa token för att fylla i attributdata som hanteras av schemat **_XDM Business Account Details_** , som definieras i Adobe Experience Platform.

* **Persontoken** - Dessa token baseras på affärspersonsattribut, till exempel _förnamn_, _jobbtitel_ och _företagsnamn_. Använd dessa token för att fylla i attributdata som hanteras av schemat **_XDM Business Person Details_** , som definieras i Adobe Experience Platform.

* **Systemtokens** - Dessa tokens baseras på systemfältets värden, till exempel _date_, _time_ och _unsubscribe link_.

* **Mina tokens** (när de har definierats för resan) - De [anpassade tokens som har definierats för resan](./personalization-my-tokens.md) där e-postmeddelandet finns.

>[!NOTE]
>
>Läs mer om XDM-scheman i [dokumentationen för Adobe Experience Platform datamodell (XDM)](https://experienceleague.adobe.com/sv/docs/experience-platform/xdm/home){target="_blank"}.

## Personalization editor

Anpassningsredigeraren är tillgänglig i alla sammanhang där du behöver definiera personalisering i e-postinnehåll. I redigeraren kan du välja, ordna, anpassa och validera alla data för att skapa en anpassad personalisering för ditt innehåll.

Lägg till personalisering i alla fält- eller innehållskomponenter genom att klicka på ikonen _Lägg till personalisering_ ( ![Lägg till personaliseringsikon](../../assets/do-not-localize/icon-personalization-field.svg) ).

![Personalization-redigerare](./assets/personalization-editor.png){width="800" zoomable="yes"}

>[!NOTE]
>
>Följande information om anpassningsredigeraren återspeglar de ändringar som är tillgängliga för [!DNL Journey Optimizer B2B Edition]-miljöer som har etablerats i den [förenklade arkitekturen](../simplified-architecture.md).

### Tokens och hjälpfunktioner

Om du vill använda en personaliseringstoken eller hjälpfunktion letar du reda på den i den vänstra navigeringsrutan och klickar på **+** för att lägga till den i uttrycket.

Klicka på ikonen _Mer meny_ ( **..** ) (bredvid ikonen _Lägg till_ ( **+** )) om du vill visa mer information för varje attribut och lägga till de attribut som du använder mest i _favoriterna_. Attribut som läggs till i favoriter är tillgängliga på menyn **[!UICONTROL Favorites]** i den vänstra navigeringen i redigeraren.

![Personalization-redigerare - menyn Mer om token](./assets/personalization-editor-token-more-menu.png){width="800" zoomable="yes"}

<!-- >>[!NOTE]
>
>By default, the attributes list shows only populated attributes. To display all attributes, click the _Settings_ icon above the search field and toggle off the **[!UICONTROL Show only populated attributes]** option.
-->
Du kan också definiera en standardtextsträng som visas om ett profilattribut av strängtyp är tomt. Klicka på ikonen _Mer meny_ ( **..** ) för attributet och välj **[!UICONTROL Insert with fallback text]**. Ange den text som ska visas när attributets värde är tomt för en profil och klicka sedan på **[!UICONTROL Add]**.

Det är en god vana att validera uttrycket innan du infogar det i innehållet. Klicka på **[!UICONTROL Validate]** längst ned i redigeraren för att kontrollera din syntax och se till att det inte finns några fel.

![Personalization-redigeraren har verifierat koden](./assets/personalization-editor-validated.png){width="500"}

När uttrycket är klart och felfritt klickar du på **[!UICONTROL Save]**.

### Anpassade datamängder

[!BADGE Beta]{type=Informative tooltip="Funktionen Beta"}

Du kan använda relationsscheman för e-postpersonalisering. De anpassade objekten definieras i _relationsscheman_, och en produktadministratör kan [konfigurera relationsschemafält &#x200B;](../admin/xdm-field-management.md#relational-schemas) i [!DNL Journey Optimizer B2B Edition]. Dessa fält är tillgängliga i personaliseringsredigeraren. Endast anpassade objekt som har en 1:N-relation (1:M) till personer eller konto är tillgängliga.

>[!IMPORTANT]
>
>Innan du använder anpassade objekt för skriptad personalisering måste du kontrollera och förstå [Handlebars som mallar språk](https://handlebarsjs.com/guide/), [personaliseringssyntax](./personalization-syntax.md) och de inbyggda [hjälpfunktionerna](./personalization-helper-functions.md).

När du definierar personalisering med anpassade objekt kan du komma åt alla variabler i skripttillgängliga objekt i **[!UICONTROL Personalization tokens]** (person/lead, konto, system och Mina token) och **[!UICONTROL Custom objects]** (relationsscheman). När du har markerat anpassade objekt kan du visa fälten genom att klicka på den anpassade objektmappen. Klicka på **+** för varje fält som du vill lägga till i uttrycket.

![Personalization-redigerare - Modellbaserade klasser - lägg till anpassade objektfält](./assets/personalization-editor-custom-object-fields.png){width="700" zoomable="yes"}
