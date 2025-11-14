---
title: Innehållspersonalisering
description: Anpassa B2B-mejl med konto-, person- och systemtokens i Journey Optimizer B2B edition. Lär dig använda personaliseringsredigeraren och syntaxen.
feature: Personalization, Content Design Tools, Email Authoring
topic: Personalization
role: User, Developer
level: Intermediate
keywords: uttryck, redigerare, start, personalisering
source-git-commit: fee5bddcce11b3035da6ab93b18bcc7006b4b554
workflow-type: tm+mt
source-wordcount: '602'
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

>[!NOTE]
>
>Följande information för anpassningsredigeraren återspeglar de ändringar som är tillgängliga för Journey Optimizer B2B edition-miljöer som har etablerats i den [förenklade arkitekturen](../simplified-architecture.md).

Lägg till personalisering i alla fält- eller innehållskomponenter genom att klicka på ikonen _Lägg till personalisering_ ( ![Lägg till personaliseringsikon](../../assets/do-not-localize/icon-personalization-field.svg) ).

![Personalization-redigerare](./assets/personalization-editor.png){width="800" zoomable="yes"}

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

<!-- ## Personalization experimentation {#playground}

**[!DNL Adobe Journey Optimizer]** includes an interactive tool designed to help you learn and experiment with personalization capabilities.

This playground provides a simulated environment to write and test personalization code using sample data without requiring live datasets. You can leverage predefined code samples, edit dummy profile payloads, and preview the output of your personalization code in real-time. 

![personalization playground](assets/playground.png)

➡️ [Access the personalization playground](https://experienceleague.adobe.com/sv/apps/journey-optimizer/ajo-personalization){target="_blank"} 

## How-to videos{#video-perso}

Learn how to use contextual event information from a journey to personalize a message.

>[!VIDEO](https://video.tv.adobe.com/v/334165?quality=12)

Learn how to add profile-based personalization to a message and how to use audience membership as a pre-condition to a personalization block.

>[!VIDEO](https://video.tv.adobe.com/v/334078?quality=12)

Learn how to leverage the personalization editor playground to write and test personalization code using sample data.

>[!VIDEO](https://video.tv.adobe.com/v/3457868?quality=12) -->