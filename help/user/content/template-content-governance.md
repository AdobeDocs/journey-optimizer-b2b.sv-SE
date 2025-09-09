---
title: Styrning av mallinnehåll
description: Lås e-postmallskomponenter för varumärkeskompatibilitet - ange styrningslägen, kontrollera redigering av innehåll och hantera behörigheter för kontouppsättare i Journey Optimizer B2B edition.
feature: Templates, Email Authoring, Content
role: User
exl-id: 0cf852cd-491c-4478-8d5e-51fd2cc2625a
source-git-commit: 79012352c3ae4e2f3d38b632b1f523d262f74f96
workflow-type: tm+mt
source-wordcount: '729'
ht-degree: 0%

---

# Mallinnehållshantering

Inom många marknadsföringsorganisationer finns det kreatörer som utformar e-postkampanjer. En viss design kan användas som grund för kundresor i hela organisationen. Om du vill vara säker på att du följer godkända innehållsdesigner kan du använda funktioner för innehållsstyrning för att låsa mallkomponenter. När innehållslåsning är aktiverat i e-postmallen kan marknadsförarna bara ändra de tillåtna elementen för att den ska vara anpassad till innehållsstrategin.

Du kan till exempel låsa sidhuvudet och sidfoten som är utformad för kontinuitet i varumärkeskommunikationen. Du kan också låsa kolumnen som innehåller huvudavsnittet, men tillåta författare att ändra texten så att den passar deras syfte i utformningen av kontoresan.

## Aktivera innehållsstyrning för mallen

När du har använt det visuella designområdet för att [redigera struktur- och innehållskomponenterna](./email-template-authoring.md) för din e-postmall aktiverar du styrning och tillämpar specifikt innehåll som låses efter behov.

1. I det visuella designområdet kan du komma åt lager/behållare och element med hjälp av _navigeringsträdet_.

   Klicka på ikonen _Navigeringsträd_ ( ![länkikon](../assets/do-not-localize/icon-navigation-tree.svg) ) till vänster om arbetsytan för att visa trädet.

1. Markera rotkomponenten **[!UICONTROL Body]** i trädet.

   Egenskapspanelen till höger om arbetsytan visar fliken _[!UICONTROL Settings]_&#x200B;som standard.

1. Aktivera alternativet **[!UICONTROL Governance]**.

   ![Aktivera styrning för en e-postmall](./assets/governance-template-enable.png){width="800" zoomable="yes"}

   När det här alternativet är aktiverat är standardvärdet _[!UICONTROL Mode]_&#x200B;**[!UICONTROL Read only]**. När det här läget är inställt på rotnivån är alla element i mallen låsta. Trädstrukturen till vänster visar ikonen_ Skrivskyddad _( ![Skrivskyddad ikon](../assets/do-not-localize/icon-tree-lock.svg) ) bredvid roten och alla underordnade element.

1. Om du vill aktivera specifikt innehåll som låses i mallen ändrar du **[!UICONTROL Mode]** till **[!UICONTROL Content locking]**.

   När det här läget är inställt på rotnivån är alla element i mallen upplåsta. Trädstrukturen till vänster visar ikonen _Lås innehåll_ ( ![Ikonen Lås innehåll](../assets/do-not-localize/icon-tree-content-lock.svg) ) bredvid rotelementet. Använd innehållslås för innehållskomponenter (strukturella) och enskilda innehållskomponenter efter behov.

   Aktivera **[!UICONTROL Enable content addition]** om du vill tillåta e-postförfattare för resan att lägga till strukturelement eller innehållselement. Välj vilken typ av tillägg du vill tillåta:

   * **[!UICONTROL Allow structure & content addition]** - Välj det här alternativet om du vill tillåta författare att lägga till både strukturelement och innehållselement.

   * **[!UICONTROL Allow content addition only]** - Välj det här alternativet om du vill tillåta författare att endast lägga till innehållselement.

   ![Aktivera innehållstillägg](./assets/governance-template-content-additions.png){width="600" zoomable="yes"}

   När det här läget är inställt på rotnivån är alla element i mallen låsta. Trädstrukturen till vänster visar ikonen _Skrivskyddad_ ( ![Skrivskyddad ikon](../assets/do-not-localize/icon-tree-lock.svg) ) bredvid roten och alla underordnade element.
<!-- 

   
- ![Link icon](../assets/do-not-localize/icon-navigation-tree.svg)
- ![Read only icon](../assets/do-not-localize/icon-tree-lock.svg)
- ![Content edit icon](../assets/do-not-localize/icon-tree-content-lock.svg)
- ![Content edit icon](../assets/do-not-localize/icon-tree-edit-text.svg)
- ![Edit element](../assets/do-not-localize/icon-edit.svg) -->

## Tillämpa låsning på en struktur

Med hjälp av den strukturella arvsmodellen kan du planera layouten och strukturen för din e-postmall enligt den styrning som du vill använda. Använd de strukturella komponenterna som behållare för att gruppera objekt på ett sätt som gör dem enkla att ange som låsta eller redigerbara. När e-postmallens design är på plats granskar du strukturen och använder låsningsfunktioner enligt din plan.

Om du använder en låstyp på strukturnivån får du en standardinställning för dess underordnade komponenter. Du kan sedan tillämpa en specifik låsinställning på kolumn- eller innehållselementnivå efter behov.

1. Klicka på ikonen _Navigeringsträd_ ( ![länkikon](../assets/do-not-localize/icon-navigation-tree.svg) ) till vänster om arbetsytan för att visa trädet.

1. Markera strukturen i trädet.

   Egenskapspanelen till höger om arbetsytan visar fliken _[!UICONTROL Settings]_&#x200B;som standard.

1. Ange **[!UICONTROL Lock type]**:

   * **[!UICONTROL Locked]** - Med den här inställningen är alla underordnade komponenter låsta som standard. Trädstrukturen till vänster visar ikonen _Skrivskyddad_ ( ![Skrivskyddad ikon](../assets/do-not-localize/icon-tree-lock.svg) ) bredvid alla underordnade komponenter.

   * **[!UICONTROL Editable]** - Med den här inställningen är alla underordnade komponenter redigerbara som standard. Trädstrukturen till vänster visar inte ikoner bredvid de underordnade komponenterna.

   ![Använda innehållslås för en strukturell komponent](./assets/governance-template-structure-locking.png){width="800" zoomable="yes"}

## Ange låsning för en underordnad komponent

1. Markera komponenten i trädet.

   Egenskapspanelen till höger om arbetsytan visar fliken _[!UICONTROL Settings]_&#x200B;som standard.

1. Aktivera alternativet **[!UICONTROL Use specific locking]**.

1. Välj vilken typ av styrning som ska användas:

   * **[!UICONTROL Editable]** - Tillåter fullständig redigeringskontroll av komponenten under e-postredigering.
   * **[!UICONTROL Editable content only]** - Gör att e-postförfattare kan ändra innehållet, men inte själva komponenten.
   * **[!UICONTROL Locked]** - Förhindrar ändringar i komponenten vid e-postredigering.

     För en låst komponent kan du tillåta att komponenten tas bort under e-postredigering genom att aktivera alternativet **[!UICONTROL Allow delete]**.

   ![Tillämpa innehållslåsning på en underordnad komponent](./assets/governance-template-component-locking.png){width="800" zoomable="yes"}
