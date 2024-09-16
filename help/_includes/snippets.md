---
title: Fragment
description: Återanvända anteckningar och visuella element för att anteckna en funktion eller sida som gäller en viss utgåva
source-git-commit: 4facd14886cb21371ebbc3e0032cbf14cc322586
workflow-type: tm+mt
source-wordcount: '387'
ht-degree: 0%

---

# Fragment

<!-- Content authoring steps for reuse -->

## Skapa innehåll - komponenter - struktursteg {#structures-step}

1. Om du vill starta innehållsdesignen drar du ett objekt från **[!UICONTROL Structures]** och släpper det på arbetsytan.

   Lägg till så många objekt från _[!UICONTROL Structures]_som du behöver och redigera inställningarna för varje objekt i rutan till höger.

   >[!TIP]
   >
   >Välj komponenten _[!UICONTROL n:n column]_för att definiera antalet kolumner som du vill använda (mellan tre och 10). Du kan också definiera bredden på varje kolumn genom att flytta pilarna under kolumnen.

   ![Dra en struktur till arbetsytan och justera inställningarna](../assets/content-design-shared/content-design-add-structure.png){width="800" zoomable="yes"}

   Varje kolumnstorlek får inte vara mindre än 10 % av strukturkomponentens totala bredd. Endast tomma kolumner kan tas bort.

## Skapa innehåll - komponenter - innehållssteg {#contents-step}

1. Expandera avsnittet **[!UICONTROL Contents]** och lägg till så många element du behöver i en eller flera strukturkomponenter.

   ![Dra ett innehållselement till arbetsytan och justera inställningarna](../assets/content-design-shared/content-design-add-content.png){width="800" zoomable="yes"}
   <!--
   reference to the contents elements--->

## Skapa innehåll - komponenter - inställningssteg {#settings-step}

1. Om det behövs kan du göra ytterligare anpassningar för varje komponent på flikarna _[!UICONTROL Settings]_eller_[!UICONTROL Style]_.

   Du kan till exempel ändra textstil, utfyllnad eller marginal för varje komponent.

## Skapa innehåll - steg för resurser {#assets-step}

1. Från _Resursväljaren_ kan du välja resurser som lagras direkt i resursbiblioteket.

   Dubbelklicka på mappen som innehåller dina resurser. Dra och släpp objekten i en strukturkomponent.

   >[!NOTE]
   >
   >Om du har en prenumeration på Experience Manager Assets as a Cloud Service tillsammans med standardversionen av Adobe Marketo Engage Design Studio måste du välja [bildkällan](../user/content/assets-overview.md#choose-an-asset-source) när du skapar ett e-postmeddelande, en e-postmall eller ett visuellt fragment. Du kan också välja bildkällan innan du öppnar innehållsdesignern för redigering.

   Mer information om hur du använder resurser från din källtyp finns i [Lägg till resurser i ditt innehåll](../user/content/assets-overview.md#add-assets-to-your-content).

   ![Dra en Marketo Engage-resurs till arbetsytan och justera inställningarna](../assets/content-design-shared/content-design-add-asset.png){width="800" zoomable="yes"}

## Skapa innehåll - personaliseringssteg {#personalization-step}

1. Infoga anpassningsfält för att anpassa innehållet utifrån profilattribut, målgruppsmedlemskap, kontextuella attribut med mera.

## Skapa innehåll - aktivera steg för villkorsinnehåll {#dynamic-content-step}

1. Klicka på **[!UICONTROL Enable condition content]** om du vill lägga till dynamiskt innehåll och anpassa innehållet till målprofilerna baserat på villkorliga regler.

## Framtagning av innehåll - steg för spårning av länkar {#links-tracking-step}

1. Välj fliken **[!UICONTROL Links]** i den vänstra rutan för att visa alla URL:er för ditt innehåll som spåras.

   Du kan ändra _spårningstypen_ eller _etiketten_ och lägga till taggar om det behövs.
