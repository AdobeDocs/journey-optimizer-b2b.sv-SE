---
title: Arbeta med Marketo Engage Assets
description: Läs om hur du använder Marketo Engage Design Studio-mediehanteringsintegrering i Journey Optimizer B2B Edition.
feature: Assets, Content
exl-id: 430ae5b7-2691-454c-bbd2-5a0b7a8843fb
source-git-commit: 78d82aa8b3bb8b8d432eeb187d75e2354dbff3ee
workflow-type: tm+mt
source-wordcount: '1604'
ht-degree: 0%

---

# Arbeta med resurser i Marketo Engage

Marketo Engage Design Studio är standardresurskällan för Journey Optimizer B2B Edition och du kan enkelt hantera och använda de tillgängliga resurserna i innehåll för dina kontoresor.

## Bläddra bland och få tillgång till resurser

Om du vill få åtkomst till Adobe Marketo Engage Design Studio-resurser inifrån Journey Optimizer B2B Edition går du till vänster och klickar på **[!UICONTROL Content Management]** > **[!UICONTROL Assets]**. Den här åtgärden öppnar en listsida med alla resurser listade.

![Bläddra bland Marketo Engage-resurser](assets/assets-list-page.png){width="600" zoomable="yes"}

* Om du vill visa resurserna efter mapp öppnar du mappstrukturen genom att klicka på ikonen _Visa mappar_ längst upp till vänster.

* Om du vill sortera tabellen efter någon av kolumnerna klickar du på kolumnrubriken.

* Om du vill söka efter en bildresurs i den valda mappen anger du en textsträng i sökfältet.

* Om du vill anpassa kolumnerna som visas i tabellen klickar du på ikonen _Anpassa tabell_ längst upp till höger.

  Markera de kolumner som du vill visa i listan och klicka på **[!UICONTROL Apply]**.

## Visa tillgångsinformation

Klicka på namnet på en resurs för att öppna sidan med resursinformation.

## Visa tillgångar som används som referenser

Klicka på fliken **[!UICONTROL Used By]** på sidan med tillgångsinformation för att visa information om var resursen för närvarande används i Journey Optimizer B2B Edition, för e-postmeddelanden, e-postmallar och fragment.

>[!IMPORTANT]
>
>Alla resurser som för närvarande är _IN USE_ i något av e-postmeddelandena, e-postmallarna eller fragmenten **kan inte** tas bort.

Referenser visas per kategori: _E-post_, _E-postmall_ eller _fragment_. E-postmeddelanden i Journey Optimizer B2B Edition är inbäddade och redigerade inom resorna, så den överordnade resan för det e-postmeddelande som använder resursen visas i referenser.

När du klickar på länken dirigeras du till motsvarande e-post, e-postmall eller fragment där resursen används.

## Lägga till resurser

På listsidan för Assets kan du lägga till bildresurser i Adobe Marketo Engage Design Studio.

1. Klicka på **[!UICONTROL Add Assets]** överst till höger.

1. I dialogrutan _[!UICONTROL Add assets]_drar och släpper du en eller flera filer från systemet till filrutan.

   ![Lägg till resurser i Marketo Engage Design Studio](./assets/assets-add-dialog.png){width="500" zoomable="yes"}

   Du kan också klicka på länken _[!UICONTROL Select a file from your computer]_om du vill använda ditt lokala filsystem för att söka efter och välja filer.

   Du kan överföra resurser från ditt lokala system på upp till 10 filer i taget. Den maximala filstorleken är 100 MB.

   De markerade bildernas filnamn visas i dialogrutan. Resursfilnamn måste vara unika (i olika mappar), och om det redan finns en fil med det namnet visas ett meddelande. Namn kan innehålla högst 100 tecken och får inte innehålla specialtecken (som `;`, `:`, `\` och `|`).

1. Markera målmappen där resurserna ska lagras med hjälp av mappväljaren.

1. Om du vill skriva över (ersätta) filer när du överför en eller flera filer med ett befintligt filnamn markerar du kryssrutan **[!UICONTROL Overwrite existing files]**.

1. Klicka på **[!UICONTROL Add]**.

## Ta bort resurser

Det går inte att ta bort resurser som används i e-postmeddelanden, e-postmallar eller fragment. Kontrollera de använda referenserna innan du påbörjar en resursborttagning. En borttagningsåtgärd kan inte ångras, så kontrollera innan du startar en borttagningsåtgärd.

Du kan ta bort en resurs på något av följande sätt:

* Gå till resursinformationen, klicka på **[!UICONTROL ... More]** längst upp till höger och välj **[!UICONTROL Delete]** bland alternativen.

  ![Åtkomståtgärder för resursen](./assets/assets-details-more-menu.png){width="500" zoomable="yes"}

* Klicka på _Ellipsen_ (**[!UICONTROL ...]**) bredvid resursobjektet på listsidan _[!UICONTROL Assets]_och välj **[!UICONTROL Delete]**bland alternativen.

  ![Åtkomståtgärder för resursen](./assets/assets-list-file-more-menu.png){width="500" zoomable="yes"}

Åtgärden öppnar en bekräftelsedialogruta. Du kan avbryta processen genom att klicka på **[!UICONTROL Cancel]** eller klicka på **[!UICONTROL Delete]** för att bekräfta borttagningen.

Om resursen används för närvarande öppnas en informationsdialogruta där du får en varning om att den inte kan tas bort. Klicka på **[!UICONTROL OK]** som avbryter borttagningen.

## Ersätt resurser

Du kan ersätta en resurs på något av följande sätt:

* Gå till resursinformationen, klicka på **[!UICONTROL ... More]** längst upp till höger och välj **[!UICONTROL Replace]** bland alternativen.

* Klicka på _Ellipsen_ (**[!UICONTROL ...]**) bredvid resursobjektet på listsidan _[!UICONTROL Assets]_och välj **[!UICONTROL Replace]**bland alternativen.

I dialogrutan _[!UICONTROL Replace asset]_drar och släpper du ersättningsfilen från systemet till filrutan. Du kan också klicka på länken_[!UICONTROL Select a file from your computer]_ om du vill använda det lokala filsystemet för att välja en fil. (Om du markerar flera filer i det lokala systemet används den första filen som är markerad för att ersätta dem.)

![Dialogrutan Ersätt resurs](./assets/assets-replace-dialog.png){width="520" zoomable="yes"}

Klicka på **[!UICONTROL Replace]** om du vill fortsätta. Du kan avbryta processen genom att klicka på **[!UICONTROL Cancel]**.

Om den fil som ska ersättas används för närvarande visas en informationsdialogruta om att den nya bildfilen ersätter bilden på alla platser där den används (e-post, e-postmallar och fragment).

## Hämta resurser

Du kan hämta en resurs på något av följande sätt:

* Gå till resursinformationen och klicka på **[!UICONTROL Download]** längst upp till höger.

* Klicka på _Ellipsen_ (**[!UICONTROL ...]**) bredvid resursobjektet på listsidan _[!UICONTROL Assets]_och välj **[!UICONTROL Download]**bland alternativen.

I bekräftelsedialogrutan klickar du på **[!UICONTROL Download]** för att påbörja hämtningen av resursen till ditt lokala system. Du kan avbryta processen genom att klicka på **[!UICONTROL Cancel]**.

## Använda massåtgärder på valda resurser

På listsidan (_[!UICONTROL Content Management]_>_[!UICONTROL Assets]_) markerar du flera resurser åt gången genom att markera varje kryssruta till vänster. En meddelandebanderoll visas längst ned när du väljer flera resurser.

![Markerade resurser](./assets/assets-list-selected.png){width="700" zoomable="yes"}

Du kan utföra följande gruppåtgärder:

+++Flytta resurser

1. Klicka på **Flytta** på markeringsbanderollen.

   Den här åtgärden öppnar dialogrutan _[!UICONTROL Move Assets]_, där namnen på de markerade resurserna visas och där kan du välja den_ målmapp _där du vill flytta resurserna.

1. Välj en mapp.

   Sökvägen uppdateras intill _[!UICONTROL Selected assets will move to:]_.

1. Klicka på **[!UICONTROL Move]**.

+++

+++Ta bort resurser

>[!NOTE]
>
>Du kan använda massborttagning för högst 20 markerade resurser.

1. Klicka på **[!UICONTROL Delete]** på markeringsbanderollen.

1. Klicka på **[!UICONTROL Delete]** i bekräftelsedialogrutan.

   Om någon av de markerade resurserna används för närvarande avbryts borttagningen av resursen och ett varningsmeddelande visas.

+++

## Skapa en mapp

1. Klicka på **[!UICONTROL Create Folder]** överst till höger på listsidan _[!UICONTROL Assets]_.

1. Ange mappnamnet i dialogrutan och välj målmappen (överordnad) för den nya mappen.

   Mappnamn måste vara unika, med högst 100 tecken, och får inte innehålla specialtecken som `;`, `:`, `\`, `|`.

   ![Dialogrutan Skapa mapp](./assets/assets-create-folder-dialog.png){width="500"}

1. Klicka på **[!UICONTROL Add]**.

## Använda åtgärder på mappnivå

Du kan använda åtgärder på en mapp eller resurser i mappen. Klicka på ikonen för ovaler (**..**) för mappen för att visa alternativen för åtgärder på den.

![Tillämpa åtgärder på en mapp eller resurser i mappen](./assets/assets-folder-menu-options.png){width="500"}

Du kan utföra följande åtgärder på mappnivå:

+++Lägg till resurser

1. Välj **[!UICONTROL Add assets]** om du vill överföra bildfiler till mappen.

1. Dra och släpp filerna från datorn i dialogrutan _[!UICONTROL Add assets]_. Du kan också klicka på länken om du vill använda filsystemet för att markera filerna.

   Du kan lägga till resurser från ditt lokala system på upp till 10 filer i taget. Du kan skriva över filer när du överför en eller flera filer med ett befintligt filnamn.

   De markerade bildernas filnamn visas i dialogrutan. Resursfilnamn måste vara unika (i olika mappar), och om det redan finns en fil med det namnet visas ett felmeddelande. Namn kan innehålla högst 100 tecken och får inte innehålla specialtecken (som `;`, `:`, `\` och `|`).

1. Klicka på **[!UICONTROL Add]**.

+++

+++Skapa en undermapp

1. Välj **[!UICONTROL Create folder]**.

1. Ange mappnamnet i dialogrutan.

   Mappnamn måste vara unika, med högst 100 tecken, och får inte innehålla specialtecken som `;`, `:`, `\`, `|`.

1. Klicka på **[!UICONTROL Add]**.

+++

+++Byt namn på mappen

1. Välj **[!UICONTROL Rename]**.

1. Ange det nya mappnamnet i dialogrutan.

   Mappnamn måste vara unika, med högst 100 tecken, och får inte innehålla specialtecken som `;`, `:`, `\`, `|`.

1. Klicka på **[!UICONTROL Save]**.

+++

+++Flytta mappen

1. Om du vill flytta mappen till en annan överordnad mapp väljer du **[!UICONTROL Move]**.

1. I dialogrutan väljer du målmappen som ny överordnad för undermappen.

1. Klicka på **[!UICONTROL Move]**.

   Om du försöker flytta en mapp till en av dess egna undermappar (inom strukturen för den valda mappen) visas ett felmeddelande och flyttningen avbryts.

+++

+++Ta bort mappen

1. Välj **[!UICONTROL Delete]**.

1. Klicka på **[!UICONTROL Delete]** i bekräftelsedialogrutan.

Om något av resurserna i mappen används för närvarande, öppnas en varningsdialogruta som informerar dig om att det inte går att ta bort. Klicka på **[!UICONTROL OK]**, som avbryter borttagningen.

+++

+++Konvertera till en arkivmapp

Om du arkiverar en mapp blir filerna i den inte sökbara. Använd arkivfunktionen för resursfiler som du inte vill att teammedlemmen ska kunna använda framgent, till exempel ett gammalt kampanjmärke eller säsongsinnehåll. Du kan senare avarkivera en mapp om du vill att innehållet ska vara tillgängligt igen.

* Välj **[!UICONTROL Convert to archive folder]**. En bekräftelsebanderoll visas som bekräftar att mappens status har ändrats till arkiverad.

* Välj **[!UICONTROL Unarchive folder]**. En bekräftelsebanderoll visas som bekräftar att mappens status har ändrats till Oarkiverad.

+++

## Använd resurser i e-postinnehåll

Assets kan användas i teamets e-post, e-postmall eller visuella fragmentredigering från den visuella innehållsredigeraren.

I det visuella redigeringsgränssnittet väljer du ikonen _Resursväljare_ i det vänstra sidofältet.

![Markerade resurser](./assets/content-assets-selector-icon.png){width="700" zoomable="yes"}

Den här åtgärden ändrar verktygspanelen som visar en lista med tillgängliga resurser. Det finns flera metoder för att lägga till en bildresurs på den visuella arbetsytan:

* Dra och släpp en miniatyrbild från den vänstra navigeringen.

* Lägg till en bildkomponent på arbetsytan och klicka på **[!UICONTROL Browse]** för att öppna dialogrutan _[!UICONTROL Select Asset from Adobe Marketo Engage]_.

  ![Använd filtren och sökfältet för att hitta den resurs du behöver](./assets/assets-select-dialog-marketo.png){width="700" zoomable="yes"}

  I dialogrutan kan du välja en bild från den valda databasen. Klicka på **[!UICONTROL Select]** för att lägga till resursen.

  Det finns verktyg som hjälper dig att hitta den resurs du behöver:

   * Klicka på ikonen _Filter_ längst upp till vänster om du vill filtrera de visade objekten enligt dina kriterier.

   * Ange text i fältet _Sök_ om du vill filtrera de visade objekten så att de matchar resursnamnet.

  ![Använd filtren och sökfältet för att hitta den resurs du behöver](./assets/assets-select-dialog-marketo-filtered.png){width="600" zoomable="yes"}
