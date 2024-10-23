---
title: Assets
description: Läs om filhantering i Journey Optimizer B2B edition.
feature: Assets, Content
exl-id: f3848e65-3196-4d1f-90cf-7aa6ceeafabb
source-git-commit: 23fb478712f3c6df59e94432bdf16883e6acf70b
workflow-type: tm+mt
source-wordcount: '1018'
ht-degree: 0%

---

# Assets

I Adobe Journey Optimizer B2B edition är resurser vanligtvis de bilder som används för att skapa ditt reseinnehåll. Du kan använda dessa bilder i e-postmeddelanden, e-postmallar och fragment som har skapats i Journey Optimizer B2B edition via en resursväljare eller ett enkelt dra och släpp-gränssnitt i den visuella innehållsredigeraren.

Adobe Journey Optimizer B2B edition ger marknadsförarna tillgång till två typer av mediebibliotek: Adobe Marketo Engage Design Studio och Adobe Experience Manager Assets as a Cloud Service. Du får endast använda Adobe Marketo Engage Design Studio, eller använda båda biblioteken konfigurerade samtidigt (baserat på den AEM Assets-licens du har).

## Resurshantering

Om du har ett Marketo Engage-konto och Adobe Experience Manager som Cloud Service har du tillgång till databaserna för både Marketo Engage DAM och Adobe Experience Manager Assets as a Cloud Service om ditt användarkonto har de behörigheter som krävs. Dessa databaser är separata och inte synkroniserade. Du kan använda bilder från båda källorna, men bara en åt gången kan aktiveras i innehållsredigeraren. En administratör kan göra bytet från Marketo Engage DAM till Adobe Experience Manager Assets as a Cloud Service. Objektet _[!UICONTROL Assets]_i den vänstra navigeringen visar databasen som är inställd.

### Adobe Marketo Engage-resurser

Adobe Marketo Engage Design Studio-resurskatalogen ingår som standard i alla Journey Optimizer B2B edition-prenumerationer. Det innebär att du har tillgång till alla bildresurser som lagras i Adobe Marketo Engage > [!UICONTROL Design Studio] > [!UICONTROL Images & Files]. Du kan använda den här databasen som ditt lokala resursbibliotek, inklusive funktioner för överföring och hämtning av resurser. Du kan också använda dessa resurser i ditt reseinnehåll.

Det finns inbyggda skyddsräcken som förhindrar redigering av Marketo Engage-resurser från Journey Optimizer B2B edition samt borttagning och flytt. Dessa skydd säkerställer att källmaterialet (Marketo Engage Design Studio) bevaras samtidigt som det går att läsa och återanvända i Journey Optimizer B2B edition.

Filformat som stöds: JPG, JPEG, GIF, PNG, EPS, SVG, RGB

### Adobe Experience Manager Assets as a Cloud Service

Samla marknadsförings- och kreativa arbetsflöden med Adobe Experience Manager Assets. Programmet är integrerat med Adobe Journey Optimizer B2B edition så att du enkelt kan hitta och använda digitalt material i Assets as a Cloud Service. Den ger åtkomst till din Assets-databas för resurser som du kan använda för att fylla i dina meddelanden.

Adobe Experience Manager Assets kan ansluta till Adobe Experience Manager Assets as a Cloud Service för centraliserade resurslösningar som utökar ert kreativa system och sammanför digitala resurser för leverans av upplevelser. Adobe Experience Manager Assets as a Cloud Service är en lättanvänd molnlösning för effektiv hantering av digitala resurser och Dynamic Media-åtgärder. Programmet innehåller smidigt avancerade funktioner, bland annat artificiell intelligens och maskininlärning.

Läs mer i [Adobe Experience Manager as a Cloud Service-dokumentationen](https://experienceleague.adobe.com/en/docs/experience-manager-cloud-service/content/assets/overview).

Adobe Experience Manager Assets kan nås direkt inifrån Adobe Journey Optimizer B2B edition från **[!UICONTROL Assets]**-objektet i den vänstra navigeringen. Du kan också komma åt resurser och mappar när du utformar ett e-postinnehåll.

>[!NOTE]
>
>AEM Assets som Cloud Service och Dynamic Media-licenser krävs för den här integreringen.<br/>
>Beroende på ditt kontrakt och din konfiguration kan du nå Adobe Experience Manager Assets as a Cloud Service direkt från Adobe Journey Optimizer B2B edition via den vänstra menydelen i Assets. Du kan också komma åt resurser och mappar när du utformar ett e-postinnehåll.

För närvarande kan du bara använda bilder från Adobe Experience Manager Assets i Adobe Journey Optimizer B2B edition.

## Använda resurser för att skapa innehåll

Använd resurser när du skapar e-postmeddelanden, e-postmallar och visuella fragment. Användargränssnittet för den visuella innehållsredigeraren ger åtkomst till bilderna i dina anslutna resurskataloger.

### Välj en resurskälla

Om du har en prenumeration på Experience Manager Assets as a Cloud Service tillsammans med Adobe Marketo Engage Design Studio som standard kan du välja bildresurser från båda källorna. Om du vill göra det måste du välja bildkällan när du skapar ett nytt e-postmeddelande, en ny e-postmall eller ett visuellt fragment. Du kan också välja bildkällan när du redigerar innehållet. Markeringen gäller bara för redigeringsupplevelsen, och du kan ändra bildkällan för att komma åt resurser från ett annat bibliotek när det behövs.

_**Skapa en innehållsresurs**_ - Om du vill välja en bildkälla när du skapar ett e-postmeddelande, en e-postmall eller ett fragment anger du **[!UICONTROL Image source]** i dialogrutan.

_**Redigera en innehållsresurs**_ - Om du vill välja en bildresurskälla i den visuella förhandsvisningen använder du inställningen **[!UICONTROL Image source]** i panelen till höger.

### Lägg till resurser i ditt innehåll

Du kan lägga till en bildresurs när du redigerar innehållet, beroende på den valda bildresurskällan.

>[!BEGINTABS]

>[!TAB Lägg till bildresurser i Marketo Engage]

Du kan lägga till Marketo Engage-resurser på något av följande sätt:

* Lägg till ett strukturelement och dra och släpp sedan resurser från den vänstra navigeringen på arbetsytan.
* Lägg till ett strukturelement och dra och släpp innehållstypen _image_ i strukturen. I egenskapsinställningarna till höger finns det två sätt att ange bilden:
   * Klicka på **[!UICONTROL Browse]** för att öppna resursväljaren, där du kan välja en bild från Adobe Marketo Engage Design Studio-biblioteket.
   * Klicka på **[!UICONTROL Import media]** om du vill importera en resurs från ditt lokala system. Den importerade resursen lagras i Assets rotmapp i ditt Adobe Marketo Engage Design Studio-bibliotek.

Mer information finns i [Använd resurser i ditt innehåll](./marketo-engage-design-studio.md#use-assets-in-your-content).

Om du vill ändra bilden kan du uppdatera bildens käll-URL i egenskaperna till höger.

>[!TAB Lägg till Experience Manager Assets-bilder]

1. När du redigerar e-postinnehåll i e-postdesignern drar du ett bildelement till arbetsytan.

   Egenskaperna till höger återspeglar markeringen av bildelementet.

1. Klicka på **[!UICONTROL Select an asset]** för att öppna resursväljaren i Experience Manager.

   Här kan du söka efter, filtrera och få tillgång till önskad innehållsresurs som du kan lägga till i marknadsföringsmaterialet. På den här sidan finns mer information om hur du använder väljaren.

   >[!NOTE]
   >
   >Om mer än en databas är konfigurerad kan du använda databasväljaren i resursväljaren

1. Välj den resurs som ska infogas i e-postmeddelandet.

>[!ENDTABS]
