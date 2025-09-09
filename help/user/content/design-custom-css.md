---
title: Lägg till anpassad CSS för ditt innehåll
description: Lägg in anpassad CSS i e-post och landningssidor för avancerad formatering och exakt designkontroll utöver standardkomponenterna i Journey Optimizer B2B edition.
feature: Content Design Tools, Email Authoring, Landing Pages
role: User
exl-id: 5a961190-8a65-41b0-90d0-5dd44e5cdf8a
source-git-commit: 79012352c3ae4e2f3d38b632b1f523d262f74f96
workflow-type: tm+mt
source-wordcount: '539'
ht-degree: 0%

---

# Lägg till anpassad CSS för ditt innehåll

Du kan lägga till egen anpassad CSS direkt i designutrymmet för e-post- eller landningssidor. Använd anpassad CSS för att använda avancerad och specifik formatering, vilket ger större flexibilitet och kontroll över utseendet på innehållet.

Den anpassade CSS-koden läggs till i avsnittet `<head>` i en `<style>` -tagg med attributet `data-name="global-custom"`. Den här strukturen ser till att de anpassade formaten används globalt på innehållet.

+++ Exempel på implementering

```html
<!DOCTYPE html>
<html>
  <head>
    <meta charset="utf-8">
    <meta name="content-version" content="3.3.31">
    <meta name="x-apple-disable-message-reformatting">
    <meta name="viewport" content="width=device-width,initial-scale=1.0">
    <style data-name="default" type="text/css">
      td { padding: 0; }
      th { font-weight: normal; }
    </style>
    <style data-name="grid" type="text/css">
      .acr-grid-table { width: 100%; }
    </style>
    <style data-name="acr-theme" type="text/css" data-theme="default" data-variant="0">
      body { margin: 0; font-family: Arial; }
    </style>
    <style data-name="media-default-max-width-500px" type="text/css">
      @media screen and (max-width: 500px) {
        body { width: 100% !important; }
      }
    </style>
    <style data-name="global-custom" type="text/css">
      /* Add you custom CSS here */
    </style>
  </head>
  <body>
    <!-- Minimal content -->
  </body>
</html>
```

+++

>[!NOTE]
>
>Den anpassade CSS-koden visas eller valideras inte på panelen _[!UICONTROL Styles]_&#x200B;för en vald komponent. Den är helt oberoende och kan bara ändras med alternativet [!UICONTROL Add Custom CSS] på komponentnivån Body.

## Lägg till anpassad CSS

1. Markera **[!UICONTROL Body]**-komponenten i den vänstra navigeringen när minst en innehållskomponent har lagts till på arbetsytan.

1. Välj fliken _Format_ till höger och klicka på **[!UICONTROL Add custom CSS]**.

   ![Få åtkomst till brödtextformaten](./assets/email-body-styles.png){width="800" zoomable="yes"}

   >[!NOTE]
   >
   >Knappen _[!UICONTROL Add custom CSS]_&#x200B;är bara tillgänglig när komponenten&#x200B;_[!UICONTROL Body]_ är markerad. Du kan dock använda anpassade CSS-format på alla komponenter i det.

   Popup-redigeraren _[!UICONTROL Add custom CSS]_&#x200B;visas med platshållarkodkommentarer.

1. Ange din CSS-kod i redigeraren.

   Kontrollera att den anpassade CSS-koden är giltig och följer rätt syntax. Om angiven CSS är ogiltig visas ett felmeddelande och CSS kan inte sparas. Mer information finns i [CSS-giltighet](#css-validity).

   ![Ange anpassad CSS i redigeraren](./assets/content-design-add-custom-css.png){width="450"}

1. Klicka på **[!UICONTROL Save]** om du vill spara den anpassade CSS-koden.

   Den anpassade formatmallen används för det befintliga innehållet. Du kan kontrollera att din anpassade CSS används efter dina behov. Mer information om hur du gör ändringar och justerar formatmallsprogrammet finns i [Felsökning](#troubleshooting).

   ![Anpassad CSS tillämpad på innehåll](assets/email-body-custom-css-applied.png){width="600" zoomable="yes"}

## CSS-giltighet

>[!CAUTION]
>
>Användarna ansvarar för säkerheten i sina anpassade CSS. Se till att CSS inte medför sårbarheter eller konflikter med det befintliga innehållet.
>
>Undvik att använda CSS som oavsiktligt kan bryta layouten eller funktionaliteten i innehållet.

+++ Exempel på giltig CSS

```css
.acr-component[data-component-id="form"] {
  display: flex;
  justify-content: center;
  background: none;
}

.acr-Form {
  width: 100%;
  padding: 20px 100px;
  border-spacing: 0px 8px;
  box-sizing: border-box;
  margin: 0;
}

.acr-Form .spectrum-FieldLabel {
  width: 20%;
}

.acr-Form.spectrum-Form--labelsAbove .spectrum-FieldLabel,
.acr-Form [data-form-item="checkbox"] .spectrum-FieldLabel {
  width: auto;
}

.acr-Form .spectrum-Textfield {
  width: 100%;
}

#acr-form-error,
#acr-form-confirmation {
  width: 100%;
  padding: var(--spectrum-global-dimension-static-size-500);
  display: flex;
  align-items: center;
  flex-direction: column;
  justify-content: center;
  gap: var(--spectrum-global-dimension-static-size-200);
}

.spectrum-Form-item.is-required .spectrum-FieldLabel:after{
  content: '*';
  font-size: 1.25rem;
  margin-left: 5px;
  position: absolute;
}

/* Error field placeholder */
.spectrum-HelpText {
  display: none !important;
}

.spectrum-HelpText.is-invalid,
.is-invalid ~ .spectrum-HelpText {
  display: flex !important;
}
```

```css
@media only screen and (min-width: 600px) {
  .acr-paragraph-1 {
    width: 100% !important;
  }
}
```

+++

+++ Exempel på ogiltig CSS

Användning av `<style>`-taggar accepteras inte:

```html
<style type="text/css">
  .acr-Form {
    width: 100%;
    padding: 20px 100px;
    border-spacing: 0px 8px;
    box-sizing: border-box;
    margin: 0;
  }
</style>
```

Ogiltig syntax, t.ex. saknade klammerparenteser, accepteras inte:

```css
body {
  background: red;
```

+++

## CSS i importerat innehåll

Om du vill använda anpassad CSS med innehåll som importerats till designutrymmet för e-post- eller landningssidan bör du tänka på följande:

* Om du importerar externt HTML-innehåll inklusive CSS fylls <!-- unless converting that content, -->det i [!UICONTROL Compatibility mode] och [!UICONTROL CSS styles] -avsnittet är inte tillgängligt.

* Om du importerar innehåll som ursprungligen skapades i designutrymmet för e-post eller landningssida med alternativet [!UICONTROL Add custom CSS], är den tillämpade CSS-koden synlig och redigerbar från samma alternativ.

## Felsökning

Om din anpassade CSS inte används som förväntat kan du använda webbläsarutvecklarverktygen för att inspektera innehållet och verifiera att din CSS har rätt väljare som mål. När du granskar formatkoden bör du tänka på följande:

* Kontrollera att CSS-koden är giltig och fri från syntaxfel (t.ex. saknade klammerparenteser, felaktiga egenskapsnamn).

* Kontrollera att din CSS har lagts till i taggen `<style>` med attributet `data-name="global-custom"`.

* Kontrollera om stiltaggen `global-custom` har attributet `data-disabled` inställt på true, till exempel:

  `<style data-name="global-custom" type="text/css" data-disabled="true"> body: { color: red; } </style>`

* Kontrollera att din CSS inte åsidosätts någonstans i innehållet, till exempel när du använder infogad formatering.

* Lägg till `!important` i dina deklarationer för att säkerställa att de har företräde, till exempel:

  ```
  .acr-Form {
  background: red !important;
  }
  ```
