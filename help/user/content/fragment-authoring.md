---
title: Fragmentredigering
description: Skapa återanvändbara innehållsfragment med visuella designverktyg - lägg till komponenter, personalisering, villkorsstyrt innehåll och anpassningsbara fält för e-post och mallar i Journey Optimizer B2B edition.
feature: Fragments, Content Design Tools
role: User
exl-id: d29754cf-6721-489c-bff8-cde034456db2
source-git-commit: 79012352c3ae4e2f3d38b632b1f523d262f74f96
workflow-type: tm+mt
source-wordcount: '383'
ht-degree: 0%

---

# Skapa fragment

När du har [skapat ett fragment](./fragments.md#create-fragments) använder du det visuella designområdet för att skapa struktur- och innehållskomponenterna i fragmentet.

## Lägga till struktur och innehåll {#design-fragment}

{{$include /help/_includes/content-design-components.md}}

## Lägga till resurser

{{$include /help/_includes/content-design-assets.md}}

## Navigera mellan lager, inställningar och format

{{$include /help/_includes/content-design-navigation.md}}

## Anpassa innehåll

{{$include /help/_includes/content-design-personalization.md}}

## Villkorligt innehåll

Om du vill lägga till villkorligt innehåll som anpassar innehållet till målprofilerna baserat på regler, markerar du en innehållskomponent och klickar på knappen **[!UICONTROL Enable conditional content]** i komponentens verktygsfält. När det publicerade fragmentet inkluderas i ett e-postmeddelande avgör de villkorliga reglerna varianten för en villkorlig komponent som återges i e-postmeddelandet.

Mer information finns i [_Villkorligt innehåll_](./conditional-content.md).

## Aktivera fragmentanpassning

När en författare lägger till ett fragment i en [e-postmall](./email-authoring.md#content-authoring---use-visual-fragments) eller [e-postmall](./email-template-authoring.md#content-authoring---use-visual-fragments) låses fragmentinnehållet som standard. Alla ändringar i det publicerade fragmentet sprids automatiskt till alla innehållsresurser där fragmentet används. När du anger en parameter för en komponent i fragmentet som redigerbar kan e-postförfattaren eller mallskaparen ange ett anpassat fältvärde som är specifikt för deras behov. Den här anpassningsflaggan är begränsad till visuella komponenter för bild, text och knappar.

Om du till exempel utformar en återanvändbar banderoll som innehåller en klickbar knapp, kan du ange att URL-parametern för knappen är redigerbar. E-postförfattare kan sedan använda en URL som är mer specifik för deras e-postkampanj. Med dessa anpassningsbara fält kan marknadsförarna hantera och personalisera återanvändbart innehåll utan att behöva skapa helt nya innehållsblock eller störa de ärvda uppdateringarna från det ursprungliga fragmentet.

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
