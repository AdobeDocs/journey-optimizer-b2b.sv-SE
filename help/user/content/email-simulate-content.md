---
title: Förhandsgranska och testa ditt e-postinnehåll
description: Förhandsgranska e-postmeddelanden med testprofiler, kontrollera datoråtergivning och mobilåtergivning, skicka korrektur till mottagare och validera personaliseringen i Journey Optimizer B2B edition.
feature: Email Authoring
level: Beginner
role: User
exl-id: cf9d7716-b54d-430a-8102-72f9d35cc694
source-git-commit: 79012352c3ae4e2f3d38b632b1f523d262f74f96
workflow-type: tm+mt
source-wordcount: '543'
ht-degree: 0%

---

# Förhandsgranska och testa ditt e-postinnehåll {#preview-simulate}

>[!CONTEXTUALHELP]
>id="ajo-b2b_email_preview_simulate"
>title="Kontrollera hur innehållet renderar"
>abstract="När innehållet är definierat kan du förhandsgranska det och kontrollera att återgivningen är korrekt för den kanal som du använder."

Använd funktionen _Simulera innehåll_ för att förhandsgranska e-postinnehållet och skicka testleveranser till specifika mottagare. De obligatoriska e-postfälten måste definieras, inklusive _[!UICONTROL From name]_,_[!UICONTROL From address]_, _[!UICONTROL Reply-to address]_&#x200B;och&#x200B;_[!UICONTROL Subject line]_, för att du ska kunna komma åt förhandsgransknings- och testfunktionerna.

>[!IMPORTANT]
>
>Du kan inte förhandsgranska e-postmeddelandet om det finns fel. Kontrollera _Varningarna_ för att kontrollera att inga fel blockerar förhandsgranskningsfunktionerna. Varningar blockerar inte förhandsgranskning, men du bör åtgärda dem innan du publicerar den resa som utlöser e-postleveransen.

## Visa förhandsgranskning av e-post

Du kommer åt förhandsgranskningen av återgivningen från [e-postdesignområdet](./email-authoring.md) eller från _[!UICONTROL Summary]_&#x200B;när du [öppnar ett e-postmeddelande från e-postlistan](./emails-list.md#edit-emails).

1. Klicka på **[!UICONTROL Simulate Content]** överst.

   ![Klicka på Simulera innehåll](assets/email-simulate-content.png){width="800" zoomable="yes"}

   >[!NOTE]
   >
   >Den här knappen är inte tillgänglig om det finns fel eller om obligatoriska fält inte har definierats för e-postmeddelandet.

1. På sidan _[!UICONTROL Simulate]_&#x200B;väljer du en personprofil i listan **[!UICONTROL People]**&#x200B;som ska användas för att återge e-postmeddelandet.

   I innehållsförhandsgranskningen fylls anpassade element i enligt den valda personprofilen.

   ![Välj en personprofil för att återge simuleringen](./assets/email-simulate-content-preview.png){width="800" zoomable="yes"}

   Om listan _[!UICONTROL People]_&#x200B;till vänster är tom [lägger du till personer](#add-people-to-the-profiles-list) med kontakter från den anslutna Marketo Engage-instansen.

   >[!TIP]
   >
   >Du kan också använda [Litmus-teståtergivningsintegrationen](./email-test-rendering.md) för att kontrollera återgivningen av e-postmeddelanden i populära skrivbordsklienter, mobilklienter och webbaserade klienter.

## Justera visningsalternativen

Använd visningsverktygen för att ändra förhandsvisningen efter enhetstyp eller zoomnivå:

* Markera ikonen _Skrivbord_ ( ![Skrivbordsvisningsikon](../../assets/do-not-localize/icon-device-desktop.svg) ) om du vill visa förhandsvisningen med skrivbordsformatet och proportionerna.
* Välj ikonen _Mobil_ ( ![Ikon för mobil visning](../../assets/do-not-localize/icon-device-mobile.svg) ) om du vill visa förhandsvisningen med mobilenhetens format och proportioner.
* Klicka på pilen _Zoomnivå_ och välj en zoomningsprocent för att se hur innehållet ändras enligt zoomnivån.

![Justera förhandsvisningen](assets/email-simulate-content-preview-display-options.png){width="600" zoomable="yes"}

## Skicka korrektur

Ett korrektur är ett levererat testmeddelande som gör att du och dina teammedlemmar kan granska ett e-postmeddelande innan det skickas till medlemmar i en målgrupp. Mottagarna av korrekturet kan kontrollera meddelandeåtergivning, innehåll, personaliseringsinställningar och konfiguration. Du kan skicka korrektur med en vald testprofil.

1. Klicka på **[!UICONTROL Send proof]** överst till höger.

   ![Klicka på Skicka bevis](assets/email-simulate-content-preview-send-proof.png){width="500"}

1. Ange den första mottagarens e-postadress på sidan _Skicka korrektur_.

1. För varje ytterligare mottagare som du vill ta med i granskningen klickar du på **[!UICONTROL Add recipient]** och anger deras e-postadress i fältet **[!UICONTROL Send to]**.

   Du kan lägga till upp till tio mottagare för korrekturleveransen.

1. För varje mottagare anger du fältet **[!UICONTROL Simulate as]** genom att välja en testprofil som ska användas för att anpassa meddelandeinnehållet.

   ![Lägg till mottagare och ange testprofiler](assets/email-simulate-content-preview-send-proof-recipients.png){width="700" zoomable="yes"}

1. Klicka på **[!UICONTROL Send proof]**.

## Lägga till personer i profillistan

1. Klicka på _[!UICONTROL People]_&#x200B;högst upp i listan **[!UICONTROL Add People]**.

   ![Justera förhandsvisningen](assets/email-simulate-content-add-people.png){width="500"}

1. Ange kontaktens fullständiga e-postadress i dialogrutan _[!UICONTROL Add people for testing]_.

   Om du vill lägga till flera kontakter anger du flera adresser avgränsade med kommatecken.

1. Markera kryssrutan för varje matchad kontakt som du vill lägga till i listan med testprofiler.

   ![Justera förhandsvisningen](assets/email-simulate-content-add-people-addresses.png){width="700" zoomable="yes"}

1. Klicka på **[!UICONTROL Add]** överst till höger.
