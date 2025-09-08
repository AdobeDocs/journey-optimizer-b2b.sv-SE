---
title: Konfiguration av landningssida
description: Konfigurera underdomäner för landningssidor, inställningar för förifyllnad av formulär och datastreams för att möjliggöra publicering av kampanjwebbsidor i Journey Optimizer B2B edition.
feature: Setup, Landing Pages, Content
role: Admin
hide: true
hidefromtoc: true
badgeBeta: label="Beta" type="informative" tooltip="Den här funktionen är för närvarande i en begränsad betaversion"
exl-id: 54b812cb-0129-4253-8e9e-538c25fc4709
source-git-commit: 9ed2d2a36dbdaf39c107a18632d951003c86197b
workflow-type: tm+mt
source-wordcount: '483'
ht-degree: 0%

---

# Konfiguration av landningssida

Administratörer bör se till att inställningarna för landningssidan är konfigurerade för marknadsförare som redigerar och publicerar dessa sidor.

## Inställningar

Gå till **[!UICONTROL Administration]** > **[!UICONTROL Channels]** om du vill granska landningssidans konfiguration. Välj _[!UICONTROL Landing Pages]_under **[!UICONTROL Settings]**i navigeringspanelen.

![Inställningar för landningssida](./assets/config-landing-pages-settings.png){width="800" zoomable="yes"}

### Kontosträng {#account-string}

>[!CONTEXTUALHELP]
>id="ajo-b2b_landing_pages_account_string"
>title="Kontosträng för landningssidor"
>abstract="Kontosträngen identifierar den Adobe Journey Optimizer B2B edition-instans som är värd för landningssidorna."

Kontosträngen identifierar den Adobe Journey Optimizer B2B edition-instans som är värd för landningssidorna. Kontrollera att ditt systemteam lägger till och konfigurerar DNS-posten.

### Formulärförifyllning {#form-prefill}

>[!CONTEXTUALHELP]
>id="ajo-b2b_landing_pages_form_prefill"
>title="Inställningar för förifyllning av landningssidformulär"
>abstract="Du kan aktivera alternativet för förifyllnad av formulär så att formulär på landningssidorna kan använda förfylld information för kända användare."

Aktivera alternativet **[!UICONTROL Form prefill]** om du vill tillåta att formulär på dina landningssidor använder förfylld information för kända användare. När det här alternativet är inaktiverat kan inte författare av landningssidor inkludera förifyllda formulärfält.

### Datastream {#datastream}

>[!CONTEXTUALHELP]
>id="ajo-b2b_landing_pages_datastream"
>title="Datastreams-krav"
>abstract="Datastream krävs för att samla in sidhändelser från landningssidorna på den här domänen."

>[!CONTEXTUALHELP]
>id="ajo-b2b_landing_pages_missing_datastream"
>title="DataStream-ID saknas"
>abstract="Underdomänen saknar ett DataStream ID, vilket krävs för korrekt routning. Konfigurera den i Inställningar för att fortsätta"

Ange alternativet **[!UICONTROL Datastream]** för att konfigurera ett datastream för händelsesamling på landningssidan.

## Underdomäner {#add-subdomain}

>[!CONTEXTUALHELP]
>id="ajo-b2b_landing_pages_add_subdomain"
>title="Lägg till underdomän för landningssida"
>abstract="Du kan lägga till högst 50 underdomäner. Skapa en ny underdomän för varje unik varumärkes-URL som du vill ha på Adobe Journey Optimizer B2B edition."

>[!CONTEXTUALHELP]
>id="ajo-b2b_landing_pages_configure_subdomain"
>title="Konfigurera underdomän för landningssida"
>abstract="En konfigurerad underdomän krävs för att publicera landningssidor. Du kan använda en underdomän som redan har delegerats till Adobe eller skapa en ny underdomän."

En deldomän på en landningssida ska hjälpa till att identifiera innehållstyp, produktnamn eller kampanj och förstärka sidans autenticitet. Innan du konfigurerar underdomänerna definierar du en eller flera CNAME som ska användas för dina landningssidor. Exempel:

* **product**.[CompanyDomain].com
* **go**.[CompanyDomain].com
* **signup**.[CompanyDomain].com

I de här exemplen är den första delen (i fet stil) `LandingPageCNAME`.

Lägg till en ny underdomän för varje unik varumärkes-URL som du vill ha på Adobe Journey Optimizer B2B edition. Du kan lägga till maximalt 50 underdomäner.

>[!IMPORTANT]
>
>Det är inte tillåtet att delegera en ogiltig underdomän till Adobe. Se till att du anger en giltig underdomän som din organisation äger, till exempel _marketing.dincompany.com_.

Om du vill granska dina underdomäner och lägga till nya går du till **[!UICONTROL Administration]** > **[!UICONTROL Channels]**. Välj _[!UICONTROL Landing Pages]_under **[!UICONTROL Subdomains]**i navigeringspanelen.

![Underdomäner för landningssidor](./assets/config-landing-pages-settings.png){width="800" zoomable="yes"}

_Lägga till en underdomän för landningssida :_

1. Klicka på **[!UICONTROL Add subdomain]** överst till höger.

1. I _[!UICONTROL Subdomain details]_anger du information om underdomäner:

   * **[!UICONTROL Subdomain]** - Den underdomän-URL som ska användas, till exempel `marketing.yourcompany.com`
   * **[!UICONTROL Default page]** - URL:en för standardunderdomänsidan, till exempel `marketing.yourcompany.com/products`
   * **[!UICONTROL Fallback page]** - URL:en för reservsidan som ska användas om en landningssida på underdomänen inte är aktiv, till exempel `marketing.yourcompany.com/expired`

   ![Lägg till underdomän för landningssida](./assets/config-landing-pages-add-subdomain.png){width="700" zoomable="yes"}

1. Klicka på **[!UICONTROL Save]**.
