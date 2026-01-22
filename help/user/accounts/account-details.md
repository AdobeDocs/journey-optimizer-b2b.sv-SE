---
title: Kontoinformation
description: Ta del av kontoinsikter med AI-sammanfattningar, intent detection, kontaktdisponeringsanalys och e-postkommunikation i Journey Optimizer B2B edition.
feature: Account Insights
role: User
exl-id: 12be33de-0a43-43d9-90b8-fe4411a50599
source-git-commit: 2a676f3cbeb43616a75fa3fa6eb9106230b9fb40
workflow-type: tm+mt
source-wordcount: '618'
ht-degree: 1%

---

# Kontoinformation

När du klickar på ett kontonamn var som helst i Journey Optimizer B2B edition visas sidan _Kontoinformation_. Den här sidan innehåller användbar information om kontot, inklusive generativa AI-sammanfattningar. Det finns också [åtgärder](#account-actions) som du kan utföra för kontakter som är kopplade till kontot.

![Åtkomst till kontoinformationen](./assets/account-details.png){width="700" zoomable="yes"}

Använd fliken **[!UICONTROL Overview]** om du vill granska information om kontot och fliken **[!UICONTROL Contacts]** om du vill visa en lista över kontokontakterna.

## Fliken [!UICONTROL Overview]

Sidan med kontoinformation består av tre primära avsnitt:

### Kontoöversikt

![Kontoöversikt](./assets/details-page-account-overview.png){zoomable="yes"}

Avsnittet för kontoöversikt innehåller följande kontoinformation:

* Kontonamn
* Antal personer i kontot
* Bransch
* Öppna affärsmöjligheter
* De tre senaste kontoresorna där kontot används (klicka på resenamnet för att öppna [reseöversikten](../journeys/journeys-overview.md))
* Generativ AI-sammanfattning av kontot, som innehåller information om de mest engagerade inköpsgrupperna.

### Återgivningsdata

I Journey Optimizer B2B edition förutser Intent Detection-modellen en lösning/produkt av intresse med tillräcklig tillförlitlighet baserat på kontaktaktivitet. Avsikten med kontokontakter kan tolkas som sannolikheten att ha intresse för en produkt.

{{intent-data-note}}

![Återgivningsdata - kontoinformation](./assets/intent-data-panel.png){width="700" zoomable="yes"}

* Avsiktsnivåer
* Typer av avsiktssignal - Nyckelord, produkt och lösning


### Kontakttäckning

![Kontokontaktens täckning](./assets/details-page-contact-coverage.png){width="800" zoomable="yes"}

Avsnittet _[!UICONTROL Contact coverage]_visar antalet kontakter från kontot med en specifik roll som är associerad med ett lösningsintresse. Tilldelningen av roll och lösningsintresse baseras på mallen för inköpsgruppsroller. Klicka på en cell för att visa följande information:

* Beskrivning, i följande format: _x personer har min roll för z-lösningens intresse_
* Kolumner
* Namn
* Konto
* Befattning
* Köpgrupp
* Personengagemangspoäng
* Senaste aktivitet
* Information

Klicka på ikonen _Filter_ ( ![Filterikon](../assets/do-not-localize/icon-filter.svg) ) längst upp till vänster om du vill filtrera datavisningen med något av dessa attribut:

* Intresse av lösningar
* Tidsperiod

### Kontaktöverlappning

![Kontokontaktöverlappning](./assets/details-page-contact-overlap.png){width="800" zoomable="yes"}

Avsnittet _[!UICONTROL Contact overlap]_visar kontakter från kontot som är en del av mer än en inköpsgrupp som ett resultat av att de är kopplade till flera lösningsintressen. Den här informationen är i form av en tabell med följande kolumner:

* Namn
* Befattning
* Konto
* Intresse av lösningar

Klicka på _Informationsikonen_ ( ![Informationsikonen](../assets/do-not-localize/icon-info.svg) ) bredvid kontaktnamnet för att visa en tabell med följande information:

* Buying group (klicka på namnet för att öppna [information om inköpsgrupp](../buying-groups/buying-group-details.md))
* Roll
* Intresse av lösningar
* Produktåtergivning (om [konfigurerats](../admin/intent-data.md))
* Produkt

Klicka på ikonen _Filter_ ( ![Filterikon](../assets/do-not-localize/icon-filter.svg) ) längst upp till vänster om du vill filtrera datavisningen med något av dessa attribut:

* Intresse av lösningar
* Roller

## Fliken [!UICONTROL Contacts]

Välj fliken **[!UICONTROL Contacts]** om du vill visa en lista över alla personer som är associerade med kontot, som synkroniseras till Experience Platform. Varje kontaktperson i listan innehåller namn, e-postadress och poängställning.

![Kontoinformation - fliken Kontakter](./assets/account-details-contacts-tab.png){width="700" zoomable="yes"}

## Skicka e-post

Du kan skicka ett e-postmeddelande som godkänts av en marknadsförare till en eller flera valda kontakter (upp till 50 i taget) eller till alla kontakter för kontot. Listan över tillgängliga e-postmeddelanden är begränsad till godkända e-postmeddelanden från den anslutna Marketo Engage-instansen.

>[!BEGINTABS]

>[!TAB Alla kontokontakter]

1. Klicka på _[!UICONTROL Overview]_överst till höger på fliken **[!UICONTROL Send email]**.

   ![Kontoinformation - Välj e-post](../accounts/assets/account-details-send-email.png){width="700" zoomable="yes"}

1. I dialogrutan _[!UICONTROL Send email]_markerar du arbetsytan i Marketo Engage och markerar sedan kryssrutan för det e-postmeddelande som du vill skicka.

   ![Välj ett e-postmeddelande som ska skickas till medlemmar i inköpsgruppen](../accounts/assets/account-details-send-email-dialog.png){width="700" zoomable="yes"}

1. Klicka på **[!UICONTROL Send]**.

>[!TAB Markerade kontakter]

1. Markera kryssrutorna för de kontakter som du vill ta emot e-postmeddelandet på fliken _[!UICONTROL Contacts]_.

1. Klicka på **[!UICONTROL Send email]** längst upp till höger eller i markeringsfältet längst ned.

   ![Fliken Medlemmar - skicka e-post](../accounts/assets/account-details-send-email-selections.png){width="700" zoomable="yes"}

1. I dialogrutan _[!UICONTROL Send email]_markerar du arbetsytan i Marketo Engage och markerar sedan kryssrutan för det e-postmeddelande som du vill skicka.

   ![Välj ett e-postmeddelande som ska skickas till medlemmar i inköpsgruppen](../accounts/assets/account-details-send-email-dialog.png){width="700" zoomable="yes"}

1. Klicka på **[!UICONTROL Send]**.

>[!ENDTABS]
