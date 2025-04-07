---
title: Skapa innehåll - lägga till formulär
description: Återanvänt avsnitt om att lägga till formulär på landningssidor och mallar
source-git-commit: 97d8e5b366e8786e517c18828236f95304f3f3be
workflow-type: tm+mt
source-wordcount: '331'
ht-degree: 0%

---

# Skapa innehåll - lägga till formulär

Ett formulär är en återanvändbar komponent som kan refereras av flera landningssidor och mallar för landningssidor i Adobe Journey Optimizer B2B edition. Det är ett block med fält och en skicka-knapp som kan skapas i förväg och snabbt infogas för att göra siddesignen snabbare och mer konsekvent.

I följande exempel beskrivs stegen för hur du lägger till ett formulär när du utformar sidan.

1. Under avsnittet **[!UICONTROL Contents]** drar du objektet **[!UICONTROL Form]** och släpper det i en strukturell komponent på siddesignområdet.

   ![Dra en formulärkomponent till den visuella designrymden](../assets/content-design-shared/content-design-add-form.png){width="600"}

   >[!TIP]
   >
   >Om du vill lägga till formuläret så att det upptar hela den vågräta layouten i e-postmeddelandet lägger du till en 1:1-kolumnstruktur och drar och släpper formuläret i den.

1. Klicka på ikonen _Formulär_ i komponentverktygsfältet eller använd egenskaperna **[!UICONTROL Embed Form]** till höger för att välja det publicerade formuläret.

   ![Välj det publicerade formuläret](../assets/content-design-shared/content-design-add-form-properties.png){width="600"}

1. Om du vill åsidosätta standardinställningen **[!UICONTROL Follow up type]** för formuläret ändrar du inställningen enligt kraven för sidan eller mallen.

   Detta kallas även _Tack-sidan_ för formuläret och den här inställningen avgör vad som händer när en besökare skickar formuläret:

   * **[!UICONTROL Stay on page]** - Välj det här alternativet om du vill att besökaren ska vara på samma sida när formuläret skickas.

   * **[!UICONTROL Landing page]** - Välj det här alternativet om du vill välja en Journey Optimizer B2B edition- eller Marketo Engage-landningssida som uppföljning.

   * **[!UICONTROL External URL]** - Välj det här alternativet om du vill ange en URL som uppföljningssida. När besökaren har skickat formuläret läser webbläsaren in den angivna URL:en.

     >[!TIP]
     >
     >Om du vill använda formuläret för att hämta en fil kan du ange en URL för den värdbaserade filen. Med den här konfigurationen fungerar&quot;submit bottom&quot; som en nedladdningsknapp.

   ![Ändra uppföljningsinställningen](../assets/content-design-shared/content-design-add-form-follow-up.png){width="280"}

1. Om du vill begränsa formulärvisningen efter enhetstyp ändrar du inställningen **[!UICONTROL Display Options]**:

   * **[!UICONTROL Show only on desktop devices]**
   * **[!UICONTROL Show only on mobile devices]**
   * **[!UICONTROL Show on all devices]** (standard)

1. Om det behövs väljer du fliken **[!UICONTROL Styles]** på den högra panelen för att ange formulärmarginaler på sidan.
