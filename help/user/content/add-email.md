---
title: Lägg till ett e-postmeddelande till din resa
description: Lär dig att lägga till, definiera och optimera e-poståtgärder i Adobe Journey Optimizer B2B. Förbättra era kontoresor med riktade e-postmeddelanden.
feature: Email Authoring, Content
source-git-commit: 6517a953692a56bd31c5b0f2fa5f15f40c6743b5
workflow-type: tm+mt
source-wordcount: '882'
ht-degree: 0%

---

# Lägg till ett e-postmeddelande till din resa

Använd Adobe Journey Optimizer B2B edition för att skicka e-postmeddelanden till dina kunder via kontoresor. Du kan välja att skapa, anpassa och förhandsgranska meddelanden i e-postdesignområdet. Du kan också välja att skicka ett e-postmeddelande som redan är definierat i den anslutna Marketo Engage-instansen.

>[!NOTE]
>
>Om du skickar ett e-postmeddelande för första gången kontrollerar du att e-postkanalen har konfigurerats inifrån Adobe Marketo Engage. Mer information finns i [Protokoll för spårning och e-postleverans](../start/email-protocols.md).

## Lägg till en e-poståtgärdsnod i en resa

Du kan konfigurera e-postleveranser under en resa när du [lägger till en _[!UICONTROL Take an action]_nod](../journeys/action-nodes.md) och gör följande:

1. Välj **[!UICONTROL People]** för målet _[!UICONTROL Action on]_.

1. Välj **[!UICONTROL Send email]** för _[!UICONTROL Action on people]_.

1. För _[!UICONTROL Email source]_väljer du hur du vill hämta e-postmeddelandet som ska skickas.

   ![Vidta en åtgärd - skicka ett e-postmeddelande](assets/journey-node-send-email.png){width="700" zoomable="yes"}

   * Välj **[!UICONTROL Create new email]** om du vill redigera e-postmeddelandet internt i Journey Optimizer B2B edition.

     Med det här alternativet kan du hantera e-postinnehållet direkt i Journey Optimizer B2B edition. Klicka på **[!UICONTROL Create email]** för att öppna dialogrutan _Skapa ny e-post_. Du kan skapa en ny e-postinnehållsresurs <!-- or duplicate an existing email content asset-->.

     Ange en unik **[!UICONTROL Name]** för e-postmeddelandet och en **[!UICONTROL Subject line]** i dialogrutan och klicka sedan på **[!UICONTROL Create]**.

     ![Skapa ny e-postdialogruta - ny e-post](assets/create-new-email-no-duplicate.png){width="400"}

     Fälten _[!UICONTROL From email]_och_[!UICONTROL Reply to address]_ är redan konfigurerade i avsnittet _[!UICONTROL Email properties]_på sidan för e-postinnehåll. Du kan ange värden för fälten_[!UICONTROL From name]_ och _[!UICONTROL Description]_(valfritt).

     Definiera e-postinställningarna för [och klicka på ](#define-the-email-settings) för att [utforma innehållet](./email-authoring.md).**[!UICONTROL Edit email content]**

     <!-- +++New email {#new-email}
     When you want to create an email using an empty canvas or an email template, use the _[!UICONTROL New email]_ option. 

     1. In the dialog, choose **[!UICONTROL New email]**.

     1. Enter a unique **[!UICONTROL Name]** for the email and a **[!UICONTROL Subject line]**.

        ![Create new email dialog - new email](assets/create-new-email.png){width="400"}

     1. Click **[!UICONTROL Create]**.

       In the _[!UICONTROL Email properties]_ section of the email content page, the _[!UICONTROL From email]_ and _[!UICONTROL Reply to address]_ fields are already configured. You can enter values for the _[!UICONTROL From name]_ and _[!UICONTROL Description]_ (optional) fields.

     1. Click **[!UICONTROL Edit email]** to define the email [settings](#define-the-email-settings) and design the [content](./email-authoring.md).

     +++

     +++Duplicate existing email {#duplicate-email}
     When you want to create an email using an existing email from the current journey or from another journey, use the Duplicate existing journey option. You can make changes to the duplicated email according to your objective for the journey node.

     1. In the dialog, choose **[!UICONTROL Duplicate existing email]**.

     1. For **[!UICONTROL Existing email to duplicate]**, click the _Select email_ icon and select the email you want to duplicate and use for the journey node.

      You can filter the list of emails by entering a text string in the search field to match the email name.

      ![Select email](assets/create-new-email-duplicate-select-email.png){width="600" zoomable="yes"}

      Select the checkbox for the email that you want to duplicate and click **[!UICONTROL Select]**. 

     1. Enter a unique **[!UICONTROL Name]** for the email and a **[!UICONTROL Subject line]**.

        ![Create new email dialog - duplciate existing email](assets/create-new-email.png){width="400"}

     1. Click **[!UICONTROL Create]**.

        In the _[!UICONTROL Email properties]_ section of the email content page, the _[!UICONTROL From email]_ and _[!UICONTROL Reply to address]_ fields are already configured. You can enter values for the _[!UICONTROL From name]_ and _[!UICONTROL Description]_ (optional) fields.

     1. If needed, click **[!UICONTROL Edit email]** to modify the email [settings](#define-the-email-settings) and [content](./email-authoring.md).

     +++
   —>
   * Välj **[!UICONTROL Select email from Adobe Marketo Engage]** om du vill använda ett av de förvalda e-postmeddelandena i Marketo Engage och skicka det som en del av resan.

     ![Välj Marketo Engage-e-post](./assets/email-select-marketo.png){width="500" zoomable="yes"}

     Med det här alternativet anges noden och e-postinnehållet behöver inte definieras ytterligare under resan.

## Definiera e-postinställningarna

Med fliken **[!UICONTROL Details]** markerad på panelen _Sammanfattning_ till höger rullar du längst ned för att visa och ange e-postalternativen.

![E-postinställningar](./assets/email-summary-details-settings.png){width="600" zoomable="yes"}

| Alternativ | Beskrivning |
| ------ | ----------- |
| [!UICONTROL From name] | Avsändarnamnet som används i e-posthuvudet. Ange namnet på avsändaren så som du vill att den ska visas för mottagaren. Klicka på ikonen _Anpassa_ ( ![Ikonen Anpassa ](../assets/do-not-localize/icon-personalize.svg) ) om du vill använda en personaliseringstoken i fältet. |
| [!UICONTROL From email] | Avsändaradressen som används i e-posthuvudet. Standardvärdet fylls i från leveransinställningarna för [e-postkanal](../admin/configure-channels-emails.md#delivery-settings). Klicka på ikonen _Anpassa_ ( ![Ikonen Anpassa ](../assets/do-not-localize/icon-personalize.svg) ) om du vill använda en personaliseringstoken i fältet. |
| [!UICONTROL Reply-to address] | Avsändaradressen som används i e-posthuvudet. Standardvärdet fylls i från leveransinställningarna för [e-postkanal](../admin/configure-channels-emails.md#delivery-settings) ([!UICONTROL From Label]). Ange den e-postadress som du vill fylla i om mottagaren använder svarsfunktionen (den kan vara en annan eller samma som avsändaradressen). Klicka på ikonen _Anpassa_ ( ![Ikonen Anpassa ](../assets/do-not-localize/icon-personalize.svg) ) om du vill använda en personaliseringstoken i fältet. |
| [!UICONTROL Subject line] | Texten som visas i ämnesfältet för e-postmeddelandet. Standardvärdet fylls i från texten som du angav i dialogrutan _[!UICONTROL Create new email]_. Du kan ändra texten om det behövs. Klicka på ikonen_ Anpassa _( ![Ikonen Anpassa ](../assets/do-not-localize/icon-personalize.svg) ) om du vill använda en personaliseringstoken i fältet.<!-- Click the AI Assistant button ( ![AI Assistant icon](../../assets/do-not-localize/icon-gen-ai.svg){width="30" zoomable="no"} ) to generate the subject line based on the current email content.--> |
| [!UICONTROL Operational email] | Markera kryssrutan om du vill ange att e-postmeddelandet ska fungera. Operativa e-postmeddelanden undantas från avanmälnings-/avanmälningslistor och från kommunikationsbegränsningar. Välj bara det här alternativet om mottagaren inte kan betrakta e-postmeddelandet som ett oombett kommersiellt meddelande (SPAM). |
| [!UICONTROL Include view as web page] | Markera kryssrutan om du vill inkludera en länk till en webbsida som genereras från e-postmeddelandeinnehållet. E-postmeddelanden har mer begränsade funktioner än webbsidor, så de är användbara för JavaScript, utökad CSS och formulär. Den text som används för att generera länken har konfigurerats i leveransinställningarna för [e-postkanal](../admin/configure-channels-emails.md#delivery-settings) ([!UICONTROL View as web page HTML] och [!UICONTROL View as web page text]). |
| [!UICONTROL Disable open tracking] | Markera kryssrutan när du inte vill spåra e-postöppningsaktivitet. När funktionen är inaktiverad ökas antalet aktiviteter för e-postöppning bara när en unik person öppnar e-postmeddelandet. Du kan [hantera spårning för e-postinnehållslänkar](./email-authoring.md#content-authoring---link-tracking) när du utformar e-postinnehållets innehåll. |
| [!UICONTROL Preheader] | Markera kryssrutan om du vill ta med en förrubrik. En preheader är den korta sammanfattningstexten som visas efter ämnesraden i vissa e-postklienter. Det ger vanligtvis en kort sammanfattning av e-postmeddelandet och är vanligtvis en enda mening. Ange sammanfattningstexten i fältet <!-- , or click the AI Assistant button ( ![AI Assistant icon](../../assets/do-not-localize/icon-gen-ai.svg){width="30" zoomable="no"} ) to generate summary text based on the current email content -->. |
| [!UICONTROL Fields used as CC addresses] | Om det är tillgängligt väljer du upp till 25 lead- eller företagsfält som har konfigurerats i Marketo Engage med typen `Email`. |

## Kontrollera aviseringar

När du utformar innehållet i e-postmeddelanden visas varningar i gränssnittet (längst upp till höger på sidan) när nyckelinställningarna saknas. Om knappen inte visas finns det inga identifierade problem.

![E-postaviseringar](./assets/email-alerts.png){width="600" zoomable="yes"}

Det finns två typer av varningar:

* **_Varningar_** som hänvisar till rekommendationer och bästa praxis, som:

   * `The opt-out link is not present in the email body`: det är bäst att lägga till en länk för att avbryta prenumerationen i e-postmeddelandet.

     >[!NOTE]
     >
     >E-postmeddelanden i marknadsföringsstil måste innehålla en länk för avanmälan, vilket inte krävs för transaktionsmeddelanden.

   * `Text version of HTML is empty`: glöm inte att definiera en textversion av e-postbrödtexten, som används när HTML-innehåll inte kan visas.

   * `Empty link is present in email body`: Kontrollera att alla länkar i e-postmeddelandet är korrekta.

   * `Email size has exceeded the limit of 100KB`: Kontrollera att e-postmeddelandets storlek inte överstiger 100 kB för optimal leverans.

* **_Fel_** som hindrar dig från att testa eller aktivera resan/kampanjen så länge de inte är lösta, till exempel:

   * `The subject line is missing`: Ämnesraden för e-post är obligatorisk.

   * `The email version of the message is empty`: Det här felet visas när e-postinnehållet inte har konfigurerats.
