---
title: Fragmentredigering
description: Lär dig hur du skapar innehållsfragment som kan återanvändas för e-post och malldesigner för att vara effektiv och för att upprätthålla design- och varumärkesstandarder.
feature: Content
source-git-commit: 1f551b636ef347fd65aa39a809dedba8372c3ac4
workflow-type: tm+mt
source-wordcount: '365'
ht-degree: 0%

---

# Skapa fragment

När du har [skapat ett fragment](./fragments.md#create-fragments) använder du den visuella redigeraren för att skapa struktur- och innehållskomponenterna i fragmentet.

## Lägga till struktur och innehåll {#design-fragment}

>[!CONTEXTUALHELP]
>id="ajo-b2b_structure_components_fragment"
>title="Lägg till strukturkomponenter"
>abstract="Strukturkomponenter definierar fragmentets layout. Dra och släpp en **Structure**-komponent på arbetsytan för att börja designa innehållet i fragmentet."

>[!CONTEXTUALHELP]
>id="ajo-b2b_content_components_fragment"
>title="Om innehållskomponenter"
>abstract="Innehållskomponenter är tomma platshållare för innehåll som du kan använda för att skapa layouten för ett fragment."

{{$include /help/_includes/content-design-components.md}}

## Lägga till resurser

{{$include /help/_includes/content-design-assets.md}}

## Navigera mellan lager, inställningar och format

{{$include /help/_includes/content-design-navigation.md}}

## Anpassa innehåll

{{$include /help/_includes/content-design-personalization.md}}

## Aktivera anpassade fält

När en e-postmallskapare eller e-postmallskapare lägger till fragmentet, låses fragmentinnehållet som standard. Alla ändringar i det publicerade fragmentet sprids automatiskt till alla innehållsresurser där fragmentet används. När du anger en parameter för en komponent i fragmentet som redigerbar kan e-postförfattaren eller mallskaparen ange ett anpassat fältvärde som är specifikt för deras behov. Den här anpassningsflaggan är begränsad till visuella komponenter för bild, text och knappar.

Om du till exempel utformar en återanvändbar banderoll som innehåller en klickbar knapp, kan du ange att URL-parametern för knappen är redigerbar. E-postförfattare kan sedan använda en URL som är mer specifik för deras e-postkampanj. Med dessa anpassningsbara fält kan marknadsförarna hantera och personalisera innehåll utan att behöva skapa helt nya innehållsblock eller störa de ärvda uppdateringarna från det ursprungliga fragmentet.

1. I den visuella innehållsredigeraren markerar du bilden, texten eller knappelementet där du vill aktivera anpassning.

1. Välj fliken **[!UICONTROL Editable fields]** i komponentinformationen till höger.

1. Klicka på alternativet **[!UICONTROL Enable edition]** för att växla och ange de redigerbara fälten.

   ![Aktivera redigerbara fält för en fragmentbildkomponent](./assets/fragment-editable-fields-image.png){width="700" zoomable="yes"}

   Du kan aktivera anpassning för de fält som visas, vilket beror på komponenttypen och de parametrar som definieras i fragmentet.

   Ändra växlingen till ett aktiverat läge för varje fält där du vill tillåta anpassning.

1. Klicka på **[!UICONTROL Overview]** om du vill granska alla redigerbara fält och deras standardvärden.

   ![Granska redigerbara fält och deras standardvärden](./assets/fragment-editable-fields-image-overview.png){width="700" zoomable="yes"}

1. Spara ändringarna.

## Redigera länkad URL-spårning

{{$include /help/_includes/content-design-links.md}}
