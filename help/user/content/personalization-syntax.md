---
title: Personalization syntax
description: Lär dig mer om hanteringsfältsbaserad personaliseringssyntax i Journey Optimizer B2B edition, inklusive uttryck, handledare, litteraltyper och formateringsregler.
feature: Personalization, Content Design Tools
topic: Personalization
role: Developer
level: Intermediate
keywords: uttryck, redigerare, syntax, personalisering
source-git-commit: fee5bddcce11b3035da6ab93b18bcc7006b4b554
workflow-type: tm+mt
source-wordcount: '349'
ht-degree: 0%

---

# Personalization syntax {#personalization-syntax}

Uttrycken i [!DNL Journey Optimizer B2B Edition] [personaliseringsredigeraren](./personalization.md#personalization-editor) baseras på mallsyntaxen _Handlebars_ . Den använder en mall och ett indataobjekt för att generera HTML eller andra textformat. Mallar för handtag ser ut som vanlig text med inbäddade handtagsuttryck.

Mer information om Handlebars och hur de fungerar finns i [HandlebarsJS-dokumentationen](https://handlebarsjs.com/){target="_blank"}.

## Allmänna regler

Exempel på enkla uttryck:

```
{{account.accountName}}
```

Var:

* `account` är ett namnutrymme.
* `accountName` är en token som består av attribut.

  >[!NOTE]
  >
  >Attributstrukturen definieras i ett [Adobe Experience Platform XDM-schema](https://experienceleague.adobe.com/sv/docs/experience-platform/xdm/home){target="_blank"}.

* Identifierare kan vara vilket Unicode-tecken som helst förutom följande:

  ```
  Whitespace ! " # % & ' ( ) * + , . / ; < = > @ [ \ ] ^ ` { | } ~
  ```

* Syntaxen är skiftlägeskänslig.

* Orden **true**, **false**, **null** och **undefined** tillåts bara i den första delen av ett sökvägsuttryck.

* I Handlebars är värdena som returneras av {\{expression}\} _HTML-escape_. Om uttrycket innehåller `&` genereras returnerade HTML-escape-utdata som `&amp;`. Om du inte vill att Handlebars ska hoppa över ett värde använder du +trippelstash_.

<!-- For example:

    If the value of the field `profile.person.name` is _Mark & Mary_, the `{\{profile.person.name}\}` value generates as `Mark &amp; Mary` and `{\{\{profile.person.name}}}` renders as `Mark & Mary`. -->

* För argument för literala funktioner stöder den mallande språkparsern inte enkel omvänt snedstreck (`\`). Det här tecknet måste föregås av ett ytterligare omvänt snedstreck (`\`). Till exempel:

  ```
  {%= regexGroup("abc@xyz.com","@(\\w+)", 1)%}
  ```

## Hjälpmedel {#helpers-all}

En hjälpfunktion för handtag är en enkel identifierare som kan läggas till med parametrar. Varje parameter är ett Handlebars-uttryck. Dessa hjälpprogram kan nås från alla sammanhang i en e-postmall.

```sql
{{#each account.accountOrganization.annualRevenue.amount}}
    <li>{{this.name}}</li>
{{/each }}
```

<!-- These block helpers are identified with a `#` preceding the helper name and require a matching closing `/`, of the same name. 

Blocks are expressions that have a block opening ( {\{# }\} ) and closing ( {\{/} } ). -->

Mer information om de här funktionerna finns i [Hjälpfunktioner](./personalization-helper-functions.md).

## Literala typer {#literal-types}

[!DNL Adobe Journey Optimizer B2B Edition] stöder följande literaltyper:

| Literal | Definition |
| ------- | ---------- |
| Sträng | En datatyp som består av tecken omgivna av dubbla citattecken. <br>Exempel: `"prospect"`, `"jobs"`, `"articles"` |
| Boolean | En datatyp som är antingen true eller false. |
| Heltal | En datatyp som representerar ett heltal. Den kan vara positiv, negativ eller noll. <br>Exempel: `-201`, `0`, `412` |
| Array | En datatyp som består av en grupp med andra literala värden. Här används hakparenteser för att gruppera och kommatecken för att avgränsa mellan olika värden. <br> **Obs!** Du kan inte komma åt egenskaper direkt för objekt i en array. <br> Exempel: `[1, 4, 7]`, `["US", "FR"]` |

>[!CAUTION]
>
>Det går inte att använda variabeln **xEvent** i personaliseringsuttryck. Alla referenser till xEvent resulterar i valideringsfel.
