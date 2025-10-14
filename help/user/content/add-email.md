---
title: Lägg till ett e-postmeddelande till din resa
description: Lägg till e-poståtgärdsnoder för att redovisa resor - skapa nya e-postmeddelanden eller använd befintliga e-postmeddelanden från Marketo Engage för riktad kommunikation i Journey Optimizer B2B edition.
feature: Email Authoring, Account Journeys
role: User
exl-id: 21a6ce0f-b59d-4be2-abc3-fda5c6a6334f
source-git-commit: 79012352c3ae4e2f3d38b632b1f523d262f74f96
workflow-type: tm+mt
source-wordcount: '1230'
ht-degree: 0%

---

# Lägg till ett e-postmeddelande till din resa

Använd Adobe Journey Optimizer B2B edition för att skicka e-postmeddelanden till dina kunder via kontoresor. Du kan välja att skapa, anpassa och förhandsgranska meddelanden i e-postdesignområdet. Du kan också välja att skicka ett e-postmeddelande som redan är definierat i den anslutna Marketo Engage-instansen.

>[!NOTE]
>
>Om du skickar ett e-postmeddelande för första gången kontrollerar du att e-postkanalen har konfigurerats inifrån Adobe Marketo Engage. Mer information finns i [Protokoll för spårning och e-postleverans](../start/email-protocols.md).

## Lägg till en e-poståtgärdsnod i en resa

Du kan konfigurera e-postleveranser under en resa när du [lägger till en _[!UICONTROL Take an action]_&#x200B;nod](../journeys/action-nodes.md) och gör följande:

1. Välj _[!UICONTROL Action on]_&#x200B;för målet **[!UICONTROL People]**.

1. Välj _[!UICONTROL Action on people]_&#x200B;för **[!UICONTROL Send email]**.

1. För _[!UICONTROL Email source]_&#x200B;väljer du hur du vill hämta e-postmeddelandet som ska skickas.

   ![Vidta en åtgärd - skicka ett e-postmeddelande](assets/journey-node-send-email.png){width="700" zoomable="yes"}

   * Välj **[!UICONTROL Create new email]** om du vill redigera e-postmeddelandet internt i Journey Optimizer B2B edition.

     Med det här alternativet kan du hantera e-postinnehållet direkt i Journey Optimizer B2B edition. Klicka på **[!UICONTROL Create email]** för att öppna dialogrutan _Skapa ny e-post_. Du kan skapa en ny resurs för e-postinnehåll eller duplicera en befintlig resurs för e-postinnehåll.

     +++Nytt e-postmeddelande

     När du vill skapa ett e-postmeddelande med en tom arbetsyta eller en e-postmall använder du alternativet _[!UICONTROL New email]_.

      1. Välj **[!UICONTROL New email]** i dialogrutan.

      1. Ange en unik **[!UICONTROL Name]** för e-postmeddelandet och en **[!UICONTROL Subject line]**.

         ![Skapa ny e-postdialogruta - ny e-post](assets/create-new-email.png){width="400"}

      1. Klicka på **[!UICONTROL Create]**.

         Fälten _[!UICONTROL Email properties]_&#x200B;och&#x200B;_[!UICONTROL From email]_ är redan konfigurerade i avsnittet _[!UICONTROL Reply to address]_&#x200B;på sidan för e-postinnehåll. Du kan ange värden för fälten&#x200B;_[!UICONTROL From name]_ och _[!UICONTROL Description]_(valfritt).

      1. Klicka på **[!UICONTROL Edit email]** för att definiera e-postinställningarna [för &#x200B;](#define-the-email-settings) och utforma [innehållet](./email-authoring.md).

     +++

     +++Duplicera befintlig e-post

     När du vill skapa ett e-postmeddelande med hjälp av ett befintligt e-postmeddelande från den aktuella resan eller från en annan resa använder du alternativet _[!UICONTROL Duplicate existing email]_. Du kan ändra den duplicerade e-postadressen enligt ditt mål för kundnoden.

      1. Välj _[!UICONTROL Create new email]_&#x200B;i dialogrutan **[!UICONTROL Duplicate existing email]**.

      1. För **[!UICONTROL Existing email to duplicate]** klickar du på ikonen _Markering_ ( ![Markeringsikon](../assets/do-not-localize/icon-email-select.svg) ) och markerar det e-postmeddelande som du vill duplicera och använda för kundnoden.

         Du kan filtrera listan med e-postmeddelanden genom att ange en textsträng i sökfältet så att den matchar e-postnamnet.

         ![Välj e-post](assets/create-new-email-duplicate-select-email.png){width="600" zoomable="yes"}

         Markera kryssrutan för e-postmeddelandet som du vill duplicera och klicka på **[!UICONTROL Select]**.

      1. Ange en unik **[!UICONTROL Name]** för e-postmeddelandet och en **[!UICONTROL Subject line]**.

         ![Skapa ny e-postdialogruta - duplicera befintlig e-post](assets/create-new-email-duplicate.png){width="400"}

      1. Klicka på **[!UICONTROL Create]**.

         Fälten _[!UICONTROL Email properties]_&#x200B;och&#x200B;_[!UICONTROL From email]_ är redan konfigurerade i avsnittet _[!UICONTROL Reply to address]_&#x200B;på sidan för e-postinnehåll. Du kan ange värden för fälten&#x200B;_[!UICONTROL From name]_ och _[!UICONTROL Description]_(valfritt).

      1. Om det behövs klickar du på **[!UICONTROL Edit email]** för att ändra e-postinställningarna [för &#x200B;](#define-the-email-settings) och [innehållet](./email-authoring.md).

     +++

   * Välj **[!UICONTROL Select email from Adobe Marketo Engage]** om du vill använda ett av de förvalda e-postmeddelandena i Marketo Engage och skicka det som en del av resan.

     Om du har fler än en arbetsyta tillgänglig i den anslutna Market Engage-instansen markerar du arbetsytan. Välj sedan det godkända e-postmeddelande som du vill skicka som kundresa.

     ![Välj Marketo Engage-e-post](./assets/email-select-marketo.png){width="500" zoomable="yes"}

     Med det här alternativet anges noden och e-postinnehållet behöver inte definieras ytterligare under resan.

## Definiera e-postinställningarna

Med fliken **[!UICONTROL Details]** markerad på panelen _Sammanfattning_ till höger rullar du längst ned för att visa och definiera e-postinställningarna.

![E-postinställningar](./assets/email-summary-details-settings.png){width="700" zoomable="yes"}

| Alternativ | Beskrivning |
| ------ | ----------- |
| [!UICONTROL From name] | Avsändarnamnet som används i e-posthuvudet. Ange namnet på avsändaren så som du vill att den ska visas för mottagaren. Klicka på ikonen _Anpassa_ ( ![Ikonen Anpassa &#x200B;](../assets/do-not-localize/icon-personalize.svg) ) om du vill använda en personaliseringstoken i fältet. |
| [!UICONTROL From email] | Avsändaradressen som används i e-posthuvudet. Standardvärdet fylls i från leveransinställningarna för [e-postkanal](../admin/configure-channels-emails.md#delivery-settings). Klicka på ikonen _Anpassa_ ( ![Ikonen Anpassa &#x200B;](../assets/do-not-localize/icon-personalize.svg) ) om du vill använda en personaliseringstoken i fältet. |
| [!UICONTROL Reply-to address] | Avsändaradressen som används i e-posthuvudet. Standardvärdet fylls i från leveransinställningarna för [e-postkanal](../admin/configure-channels-emails.md#delivery-settings) ([!UICONTROL From Label]). Ange den e-postadress som du vill fylla i om mottagaren använder svarsfunktionen (den kan vara en annan eller samma som avsändaradressen). Klicka på ikonen _Anpassa_ ( ![Ikonen Anpassa &#x200B;](../assets/do-not-localize/icon-personalize.svg) ) om du vill använda en personaliseringstoken i fältet. |
| [!UICONTROL Subject line] | Texten som visas i ämnesfältet för e-postmeddelandet. Standardvärdet fylls i från texten som du angav i dialogrutan _[!UICONTROL Create new email]_. Du kan ändra texten om det behövs. Klicka på ikonen_ Anpassa _( ![Ikonen Anpassa &#x200B;](../assets/do-not-localize/icon-personalize.svg) ) om du vill använda en personaliseringstoken i fältet.<!-- Click the AI Assistant button ( ![AI Assistant icon](../../assets/do-not-localize/icon-gen-ai.svg){width="30" zoomable="no"} ) to generate the subject line based on the current email content.--> |
| [!UICONTROL Branding domain] | Om du har fler än en [varumärkesdomän](../admin/configure-channels-emails.md#branding-domains) definierad i systemet väljer du den varumärkesdomän som ska användas för att skicka e-postmeddelandet. Använd en specifik varumärkesdomän för att skicka e-postmeddelanden som verkar komma från ert varumärke i stället för från företaget som helhet. Det bygger upp förtroende för varumärket, personaliserar e-postupplevelsen och ökar öppnings- och svarsfrekvensen. |
| [!UICONTROL Dedicated IP] | Om du har definierat fler än en dedikerad IP-adress väljer du en dedikerad IP-adress som ska användas för att skicka e-postmeddelandet. När ni använder en specifik dedikerad IP-adress för era program kan ni spåra och övervaka leveransen noggrannare och snabbt reagera på eventuella förändringar i leveransstatistiken. Mer information om hur du lägger till en dedikerad IP-adress för den anslutna Marketo Engage-instansen finns i [Marketo Engage-dokumentationen](https://experienceleague.adobe.com/sv/docs/marketo/using/product-docs/email-marketing/deliverability/use-your-dedicated-ip-addresses-to-send-emails){target="_blank"}. |
| [!UICONTROL Operational email] | Markera kryssrutan om du vill ange att e-postmeddelandet ska fungera. Operativa e-postmeddelanden undantas från avanmälnings-/avanmälningslistor och från kommunikationsbegränsningar. Välj bara det här alternativet om mottagaren inte kan betrakta e-postmeddelandet som ett oombett kommersiellt meddelande (SPAM). |
| [!UICONTROL Include view as web page] | Markera kryssrutan om du vill inkludera en länk till en webbsida som genereras från e-postmeddelandeinnehållet. E-postmeddelanden har mer begränsade funktioner än webbsidor, så de är användbara för JavaScript, utökad CSS och formulär. Den text som används för att generera länken har konfigurerats i leveransinställningarna för [e-postkanal](../admin/configure-channels-emails.md#delivery-settings) ([!UICONTROL View as web page HTML] och [!UICONTROL View as web page text]). |
| [!UICONTROL Disable open tracking] | Markera kryssrutan när du inte vill spåra e-postöppningsaktivitet. När funktionen är inaktiverad ökas antalet aktiviteter för e-postöppning bara när en unik person öppnar e-postmeddelandet. Du kan [hantera länkspårning för e-postinnehåll](./email-authoring.md#content-authoring---link-tracking) när du utformar e-postinnehållets innehåll. |
| [!UICONTROL Preheader] | Markera kryssrutan om du vill ta med en förrubrik. En preheader är den korta sammanfattningstexten som visas efter ämnesraden i vissa e-postklienter. Det ger vanligtvis en kort sammanfattning av e-postmeddelandet och är vanligtvis en enda mening. Ange sammanfattningstexten i fältet <!-- , or click the AI Assistant button ( ![AI Assistant icon](../../assets/do-not-localize/icon-gen-ai.svg){width="30" zoomable="no"} ) to generate summary text based on the current email content -->. |
| [!UICONTROL Fields used as CC addresses] | Om det är tillgängligt väljer du upp till 25 lead- eller företagsfält som har konfigurerats i Marketo Engage med typen `Email`. |

## Kontrollera aviseringar

När du utformar innehållet i e-postmeddelanden visas varningar i gränssnittet (längst upp till höger på sidan) när nyckelinställningarna saknas. Om knappen inte visas finns det inga identifierade problem.

![E-postaviseringar](./assets/email-alerts.png){width="600" zoomable="yes"}

Det finns två typer av varningar:

* **_Varningar_** som hänvisar till rekommendationer och bästa praxis, som:

   * `The opt-out link is not present in the email body`: Det är bäst att lägga till en länk för att avbryta prenumerationen i e-postmeddelandet.

     >[!NOTE]
     >
     >E-postmeddelanden i marknadsföringsstil måste innehålla en länk för avanmälan, vilket inte krävs för transaktionsmeddelanden.

   * `Text version of HTML is empty`: Glöm inte att definiera en textversion av e-postbrödtexten, som används när HTML-innehåll inte kan visas.

   * `Empty link is present in email body`: Kontrollera att alla länkar i e-postmeddelandet är korrekta.

   * `Email size has exceeded the limit of 100KB`: Kontrollera att e-postmeddelandets storlek inte överstiger 100 kB för optimal leverans.

* **_Fel_** som hindrar dig från att testa eller aktivera resan/kampanjen så länge de inte är lösta, till exempel:

   * `From name is empty`: Fältet _Från_ (obligatoriskt) har inte definierats.

   * `The subject line is missing`: Ämnesraden (obligatoriskt) för e-post har inte definierats.

   * `The email version of the message is empty`: E-postinnehållet har inte definierats.
