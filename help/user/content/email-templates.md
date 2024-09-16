---
title: E-postmallar
description: Lär dig hur du skapar och redigerar e-postmallar som kan användas för att enkelt och effektivt skapa e-postmeddelanden om kontoresan.
feature: Email Authoring, Content
exl-id: 4e146802-e3ef-4528-b581-191e28afe86f
source-git-commit: 5f53f4156c670d1c7b751844ab0bda0aef352973
workflow-type: tm+mt
source-wordcount: '1763'
ht-degree: 0%

---

# E-postmallar

För en snabbare och förbättrad designprocess kan du skapa fristående e-postmallar för att återanvända anpassat innehåll på kontoresor för Adobe Journey Optimizer B2B Edition. Med hjälp av mallar kan era innehållsorienterade teammedlemmar arbeta med e-postinnehåll utanför resor. Marknadsföringsstrateger kan sedan återanvända och anpassa de här fristående mallarna i sina kontoresor. En teammedlem ansvarar till exempel bara för innehåll, utan tillgång till kontoresor. De kan dock skapa en e-postmall som marknadsförarna kan välja som utgångspunkt för e-postkommunikation och anpassa den efter kundresan.

## Få åtkomst till och hantera e-postmallar

Om du vill komma åt e-postmallar i Adobe Journey Optimizer B2B-utgåvan går du till vänster och klickar på **[!UICONTROL Content Management]** > **[!UICONTROL Templates]**. Den här åtgärden öppnar en listsida med alla e-postmallar som har skapats i instansen i en tabell.

Tabellen sorteras efter kolumnen _[!UICONTROL Modified]_, med de senast uppdaterade mallarna överst i listan som standard. Klicka på kolumnrubriken om du vill ändra mellan stigande och fallande.

Om du vill söka efter en mall efter namn anger du en textsträng i sökfältet. Klicka på ikonen _Filter_ längst upp till vänster om du vill filtrera listan efter datum för skapande eller ändring samt mallar som du har skapat eller ändrat.

![Öppna e-postmallsbiblioteket och filtrera efter namn och datum](./assets/templates-list-search-filter.png){width="700" zoomable="yes"}

Anpassa de kolumner som du vill visa i tabellen genom att klicka på ikonen _Anpassa tabell_ längst upp till höger. Markera de kolumner som ska visas och klicka på **[!UICONTROL Apply]**.

På listsidan kan du utföra de åtgärder som beskrivs i följande avsnitt.

## Skapa e-postmallar

Du kan skapa en ny e-postmall från e-postmallens listsida genom att klicka på **[!UICONTROL Create template]** överst till höger.

1. Ange ett användbart **[!UICONTROL Name]** och **[!UICONTROL Description]** (valfritt) i dialogrutan.

   ![Ange initiala egenskaper för den nya e-postmallen](./assets/templates-create-dialog.png){width="400"}

1. Ange startvärdet **[!UICONTROL Image source]**.

   Om du har en prenumeration på Experience Manager Assets as a Cloud Service tillsammans med Adobe Marketo Engage Design Studio som standard kan du välja bildresurser från båda källorna. Om du vill göra det måste du välja bildkällan när du skapar en e-postmall eller ett visuellt fragment. Du kan också välja bildkällan när du redigerar innehållet.

   Mer information om bildkällor finns i [Assets](./assets-overview.md).

1. Klicka på **[!UICONTROL Create]**.

Sidan _[!UICONTROL Design your template]_öppnas och innehåller flera alternativ för att skapa mallen:_[!UICONTROL Design from scratch]_, _[!UICONTROL Import HTML]_eller_[!UICONTROL Select design template]_.

![Välj hur du vill börja med din e-postmallsdesign](./assets/templates-create-design.png){width="800" zoomable="yes"}

### Designa från grunden

Använd den visuella innehållsredigeraren för att definiera strukturen för e-postinnehållet. Genom att lägga till och flytta strukturella komponenter med enkla dra och släpp-åtgärder kan du designa formen på det återanvändbara e-postinnehållet på några sekunder.

>[!NOTE]
>
>De tillgängliga designverktygen motsvarar verktygen som används för att skapa [e-post](./email-authoring.md). Skillnaden är att det här innehållet sedan sparas som en mall som kan återanvändas i flera e-postnoder som skickas via kontoresor.

1. Välj alternativet **[!UICONTROL Design from scratch]** på startsidan för _[!UICONTROL Design your template]_.

1. [Lägg till struktur och innehåll](#add-structure-and-content) i mallen.

### Importera HTML

Med Adobe Journey Optimizer B2B Edition kan du importera befintligt HTML-innehåll för att utforma e-postmallar.

{{$include /help/_includes/content-design-import.md}}

![importera html-innehåll i en ZIP-fil](./assets/templates-import-zip-file.png){width="500"}

>[!NOTE]
>
>Om du använder en `<table>`-tagg som det första lagret i en HTML-fil kan du förlora stilar, inklusive inställningar för bakgrund och bredd i den översta lagertaggen.

Du kan anpassa det importerade innehållet efter behov med de visuella redigeringsverktygen för e-post.

### Välj en designmall

{{$include /help/_includes/content-design-select-template.md}}

## Lägga till struktur och innehåll {#structure-content}

>[!CONTEXTUALHELP]
>id="ajo-b2b_structure_components_template"
>title="Lägg till strukturkomponenter"
>abstract="Strukturkomponenter definierar mallens layout. Dra och släpp en **Struktur**-komponent på arbetsytan för att börja designa innehållet för mallen."

>[!CONTEXTUALHELP]
>id="ajo-b2b_content_components_template"
>title="Om innehållskomponenter"
>abstract="Innehållskomponenter är tomma platshållare för innehåll som du kan använda för att skapa layouten för en mall."

{{$include /help/_includes/content-design-components.md}}

### Lägg till fragment

Ikonen _Fragments_ visas till vänster i den visuella innehållsredigeraren. I följande exempel beskrivs stegen för att lägga till fragment i mallinnehållet.

1. Om du vill öppna fragmentlistan klickar du på ikonen _Fragment_ .

   Du kan:

   * Sortera listan.
   * Bläddra, sök eller filtrera listan.
   * Växla mellan miniatyr- och listvy.
   * Uppdatera listan så att den återspeglar något av de nyligen skapade fragmenten.

   ![Välj ett fragment i listan](./assets/visual-designer-fragments.png){width="700" zoomable="yes"}

1. Dra och släpp något av fragmenten i platshållaren för strukturelement.

   Redigeraren återger fragmentet i avsnittet/elementet i e-poststrukturen.

Fragmentets innehåll uppdateras dynamiskt i strukturen för att visa hur innehållet visas i e-postmeddelandet.

>[!TIP]
>
>Om du vill lägga till fragmentet så att det upptar hela den vågräta layouten i e-postmeddelandet lägger du till en 1:1-kolumnstruktur och drar och släpper fragmentet i den.

När e-postmeddelandet har sparats visas det på fragmentinformationssidan när du väljer fliken _[!UICONTROL Used By]_i sammanfattningen. Fragment som läggs till i en e-postmall kan inte redigeras i mallen. Innehållet definieras av källfragmentet.

### Lägga till resurser

{{$include /help/_includes/content-design-assets.md}}

### Navigera mellan lager, inställningar och format

{{$include /help/_includes/content-design-navigation.md}}

### Anpassa innehåll

{{$include /help/_includes/content-design-personalization.md}}

### Redigera länkad URL-spårning

{{$include /help/_includes/content-design-links.md}}

### Visningsalternativ

Utnyttja de alternativ för visning och innehållsvalidering som finns i den visuella e-postredigeraren.

* Zooma in/ut i innehållet genom förinställda zoomalternativ.

* Växla mellan att visa innehållet på datorer, mobiler eller endast text/normal text.
   * Klicka på ikonen _Ögon_ om du vill förhandsgranska innehåll på olika enheter.
   * Välj en av de färdiga enheterna eller ange anpassade dimensioner för att förhandsgranska innehållet.

### Fler alternativ

Från väljaren _Fler alternativ_ i redigeraren för visuellt innehåll kan du utföra följande åtgärder:

![Klicka på Mer för att komma åt mallåtgärder](./assets/visual-designer-more-menu.png){width="500"}

* **Återställ mall** - Klicka på det här alternativet om du vill rensa den visuella e-postdesignerns arbetsyta till en tom plats och starta om skapandet av innehåll.
* **Spara som fragment** - Spara hela eller delar av den som ett fragment som kan återanvändas i flera e-postmallar eller e-postmallar. Du anger ett namn och en beskrivning för fragmenten och den till listan med tillgängliga fragment.
* **Ändra din design** - Återgå till sidan _Designa din mall_. Härifrån kan du vidta vilken åtgärd som helst enligt anvisningarna i avsnittet Skapa e-postmallar.
* **Exportera HTML** - Hämta innehåll på den visuella arbetsytan till ditt lokala system i HTML-format som paketerats som en zip-fil.

## Visa information om e-postmallar

På malllistsidan klickar du på namnet på en e-postmall för att öppna informationssidan för e-postmallen. Härifrån kan du visa grundläggande egenskaper för e-postmallen och komma åt den visuella innehållsredigeraren för att göra ändringar i mallinnehållet.

![Öppna e-postmallsbiblioteket och filtrera efter namn och datum](./assets/template-details.png){width="700" zoomable="yes"}

* Visa information om e-postmallen, till exempel namn och beskrivning. Dessa inställningar kan redigeras. Klicka utanför beskrivningsrutan om du vill spara ändringarna automatiskt.

* Visa egenskaper för e-postmallar, t.ex. skapade av, senast uppdaterade av och ändrade av.

* Klicka på **[!UICONTROL More]** överst till höger för att utföra snabba åtgärder på e-postmallen, till exempel _Duplicera_ och _Ta bort_.

* Om det finns aktiva aviseringar (fel och varningar för e-postmallen) klickar du på **[!UICONTROL Alerts]** längst upp till höger för att visa informationen.

  Dessa aviseringar förhindrar inte att e-postmallen används för att skapa e-post, men den här informationen ger marknadsförarna i teamet insyn i vad som kanske inte fungerar och i de nödvändiga uppdateringarna innan den kan användas för leverans.

## Visa e-postmall som används av referenser

På informationssidan för e-postmallar klickar du på fliken **[!UICONTROL Used By]** för att visa information om var den här e-postmallen används i e-postmeddelanden mellan kontoresor.

![Klicka på fliken Används av för att kontrollera mallanvändning](./assets/template-details-used-by.png){width="400"}

E-postmeddelanden i Journey Optimizer B2B Edition är inbäddade och redigerade inom resorna, så den överordnade resan för det e-postmeddelande som använder mallen visas i referenser.

* När du klickar på länken skickas du till motsvarande e-postmeddelande för resan där e-postmallen används.

* Avsluta vyn när som helst genom att klicka på bakåtpilen, som återgår till listsidan.

## Redigera e-postmallar

Den här åtgärden kan utföras från:

* Informationssidan - Klicka på **[!UICONTROL Edit email template]**.
* Listsidan - Klicka på ellipsen (**..**) bredvid en e-postmall och välj **[!UICONTROL Edit]**.

Den här åtgärden tar dig till sidan _Designa din mall_ eller den visuella innehållets redigeringssida baserat på den senast sparade statusen för e-postmallen. Härifrån kan du redigera e-postmallens innehåll efter behov. Mer information om redigeringsalternativen finns i [Skapa e-postmallar](#create-email-templates).

## Duplicera e-postmallar

Du kan duplicera en e-postmall på något av följande sätt:

* Expandera **[!UICONTROL More]** från e-postmallsinformationen till höger och klicka på **[!UICONTROL Duplicate]**.

  ![Klicka på Mer för att komma åt åtgärderna Ta bort och Duplicera](./assets/template-details-more-menu.png){width="400"}

* Klicka på ellipsen (..) bredvid mallen på listsidan _E-postmallar_ och välj **[!UICONTROL Duplicate]**.

Ange ett användbart namn (unikt) och en beskrivning i dialogrutan. Klicka på **[!UICONTROL Duplicate]** för att slutföra åtgärden.

Den duplicerade (nya) e-postmallen visas sedan i listan _E-postmallar_ .

## Ta bort e-postmallar

Det går inte att ångra borttagningen av en e-postmall, så kontrollera innan du startar en borttagningsåtgärd. Du kan ta bort en e-postmall på något av följande sätt:

* Expandera **[!UICONTROL More]** från mallinformationen till höger och klicka på **[!UICONTROL Delete]**.
* Klicka på ellipsen (..) bredvid mallen på listsidan _E-postmallar_ och välj **[!UICONTROL Delete]**.

  ![Klicka på ... för att komma åt åtgärderna Duplicera och Ta bort](./assets/templates-list-more-menu.png){width="500"}

Åtgärden öppnar en bekräftelsedialogruta. Du kan avbryta processen genom att klicka på **[!UICONTROL Cancel]** eller klicka på **[!UICONTROL Delete]** för att bekräfta borttagningen.

## Ta massåtgärder

På listsidan för e-postmallar markerar du flera mallar åt gången genom att markera kryssrutorna till vänster. En banderoll visas längst ned när du väljer flera mallar.

![En banderoll visar antalet valda mallar och ikonen Ta bort ](./assets/templates-multi-select-banner.png){width="600"}

**[!UICONTROL Delete]** - Du kan ta bort upp till 20 mallar samtidigt. I en bekräftelsedialogruta kan du avbryta åtgärden eller bekräfta borttagningen av mallarna.

## Skapa ett e-postmeddelande från en sparad mall

Från skärmen _Skapa e-post_ kan du använda avsnittet _Välj designmall_ för att börja skapa innehåll från en mall.

Gör så här för att börja skapa innehåll med någon av e-postmallarna:

1. Öppna e-postmeddelandet för Designer från sidan _Redigera innehåll_.

   Fliken _Exempelmallar_ är markerad som standard på sidan _Skapa e-post_.

1. Om du vill använda en anpassad e-postmall väljer du fliken **[!UICONTROL Saved templates]**.

   På den här fliken visas en lista med alla e-postmallar som skapats i sandlådan. Du kan sortera dem _efter namn_, _Senast ändrat_ och _Senast skapat_.

1. Välj önskad mall i listan.

   När du har valt mallen visas en förhandsvisning av den. I förhandsgranskningsläget kan du navigera mellan alla mallar i en kategori (exempel eller sparat, beroende på vad du har valt) med höger- och vänsterpilarna.

1. Klicka på **[!UICONTROL Use this template]** överst till höger.

1. Från den visuella designern kan du redigera ditt innehåll efter behov.
