---
title: Frågvägledning för AI-assistenten
description: Platshållare
feature: AI Assistant
level: Beginner
exl-id: 65541246-7f4f-442f-8293-df036ea1c4ac
source-git-commit: f09f3f5b7d4419ead5308e4c5be3b518b4e16ff5
workflow-type: tm+mt
source-wordcount: '871'
ht-degree: 0%

---

# Frågevägledning för AI Assistant i Journey Optimizer B2B edition

Se följande exempelfrågor för frågor om AI Assistant i Journey Optimizer B2B edition. Den här informationen innehåller även tips om hur du kan ge dina frågor en optimal svarsbeskrivning från AI Assistant.

## Målsättningsbaserade frågor

Följande exempelfrågor grupperas efter mål som du kan uppnå med AI Assistant:

| Syfte | Beskrivning | Exempel |
| --- | --- | --- |
| Utbildningsbegrepp och fortsatta arbetsflöden | Som nybörjare kan du använda AI Assistant för att lära dig Real-Time CDP- och Adobe Journey Optimizer B2B edition-koncept och själv ta till vara produkter och funktioner som du inte känner till. <br>Som erfaren användare kan du använda AI Assistant för att lösa ett edge-fall som kan blockera ditt arbetsflöde. | <li>Berätta några användningsfall för Real-Time CDP. <li>Förklara Buying Group för mig. |
| Felsökning | Använd AI Assistant för att lära dig hur du felsöker grundläggande fel som kan uppstå i arbetsflödet. | <li>Vad betyder det här felet &lt;ERROR_MESSAGE>? <li>Varför kan jag inte ta bort målgruppen med namnet &quot;..&quot;? |
| Sandlådehygien | Använd AI Assistant för att identifiera eventuella dubbletter eller oanvända objekt så att du effektivt kan underhålla sandlådan. | <li>Kan du visa mig vilka målgrupper som är lika? <li>Finns det några scheman som inte har någon associerad datauppsättning? |
| Värdeanalys | Använd AI Assistant för att identifiera dina mest använda dataobjekt och utvärdera eventuella prestandaindikatorer eller hitta de värdefullaste dataobjekten. | <li>Hur många konton finns i segmentdefinitionen &quot;..&quot;? <li>När aktiverades målgrupper på Experience Cloud målgrupper? |
| Sök | Använd AI Assistant för att hitta Experience Platform- och Adobe Journey Optimizer B2B edition-objekt som stöds, t.ex. kontomålgrupper, dataset, destinationer, scheman, källor, kontoresor, inköpsgruppmallar och lösningsintressen | <li>Ange de målgrupper som innehåller&quot;Luma&quot; i namnet som användes vid kontoresor. <li>Vilka attribut finns i XDM-schemat&quot;Luma: Custom Actions&quot;? |
| Effektanalys | Använd AI Assistant för att identifiera dataobjekt som har använts i vissa arbetsflöden, så att du kan bedöma effekten av eventuella ändringar. | <li>Vilka kontomålgrupper använder `workEmail.address` i B2B-personschemat? <li>Vilka datauppsättningar lagras i ... `jobTitle`? |

## Tar hand om dina frågor

Du måste ge AI Assistant tydliga och kontextuella svar på dina frågor för att få ett så korrekt svar som möjligt. Se följande lista med tips om hur du ställer en tydlig fråga i sitt sammanhang:

* Ange din uppgift och/eller fråga kortfattat.
* Undvik tvetydigt språk och alltför komplex syntax för att underlätta förståelsen.
* Ange relevant sammanhang för dina uppgifter och/eller frågor eftersom kontexten kan hjälpa AI Assistant att generera mer relevanta svar.

I följande tabeller beskrivs några metodtips som du kan följa när du använder AI Assistant:

| Gör | Exempel |
| --- | --- |
| <li>Var tydlig med objektet eller informationen som du vill hämta eller analysera. <li>Försök att ange dataobjektens namn inom citattecken. <li>Om du bara känner till en del av objektnamnet kan du även ange det i frågan. | <li>Vilka datauppsättningar använder schemat &quot;B2B-konto&quot;? <li>Visa de aktiva målgrupperna som har &quot;Konto&quot; i sina namn. Rangordna dem efter antal medlemmar. |
| <li>Undvik tvetydighet och använd tydligt språk. <li>Använd exakt terminologi för att få bättre tydlighet i frågan. <li>När du ställer frågor om Adobe Experience Platform och Adobe Journey Optimizer B2B edition kan du försöka använda terminologi som är specifik för Experience Platform eller Adobe Journey Optimizer B2B edition för att förbättra relevansen i svaren. | <li>Hur många medlemmar har jag i&quot;Målgrupp för mitt konto&quot;? <li>Hur många kontoresor använder kontomålgruppen&quot;Min kontomålgrupp&quot;? |
| <li>Ange sammanhang eller ange ett villkor för att filtrera resultaten. <li>Använd ett filtervillkor i frågorna för att begränsa mängden data i svaret. | <li>Visa målgrupper som inte har aktiverats och som skapats för mer än sex månader sedan och som aldrig har ändrats. <li>Visa kontoresor som har publicerats de senaste 7 dagarna och använder en kontopublik som har fler än 1 000 medlemmar |

| Gör det inte | Exempel |
| --- | --- |
| Använd oklart eller tvetydigt språk. | <li>Ge mig information om datauppsättningar. <li>Vad gör resan x? <li>Hur många användare har jag i&quot;ACME Audience&quot;? <li>Visa segment. <li>Listattribut. |
| Gör ofullständiga förfrågningar. | <li>&quot;Luma - lojalitetsdatauppsättning&quot; |
| Anta kunskap utan kontext. | <li>Målgrupper de senaste sex månaderna. <li>Bygg en fråga åt mig. <li>Skapa en resa åt mig |
| Formge alltför komplexa frågor. | <li>Gör en omfattande analys av datalinjer för alla objekt och deras beroenden. |
| Utelämna villkor eller parametrar. | <li>Visa datauppsättningar. |

## Exempel på frågor som inte stöds

Följande lista innehåller exempel på frågor som AI Assistant i Journey Optimizer B2B edition inte stöder:

* Vilka målgrupper använder fältet workEmail.address i fältgruppen ... i sitt skick? 
* Visa mig antalet aktiva resor med kontomålgrupper som är större än 10 000, 5 000-10 000, 1 000-5 000 och mindre än 1 000, i en visuell distribution
* Vem gjorde den senaste uppdateringen av kontoresan x?
* Hur många aktiva resor lägger till medlemmar i inköpsgrupper för lösningsränta x?
* Vilka aktiva resor lägger till medlemmar i inköpsgrupper för lösningsränta x?
* Vilken är den vanligaste beslutsfattartiteln för att köpa gruppmallar?
* Vilka är beslutsfattarna när det gäller att köpa gruppmall x?

## Nästa steg

Mer information om hur du använder AI Assistant-funktionerna under arbetsflöden finns i [Använd AI Assistant i Journey Optimizer B2B edition](./use-ai-assistant.md).
