---
title: Testa e-poståtergivning
description: Lär dig hur du använder ditt Litmus-konto för att testa återgivning av e-postmeddelanden i Journey Optimizer B2B edition.
feature: Email Authoring, Integrations
level: Intermediate
role: User
source-git-commit: 23fe51dd0df0b958a61ada25521f35d8acd8bcc4
workflow-type: tm+mt
source-wordcount: '293'
ht-degree: 0%

---

# Testa e-poståtergivning med Litmus

Om du vill testa dina e-postmeddelanden kan du använda ett [Litmus-konto](https://www.litmus.com/email-testing){target="_blank"} i Journey Optimizer B2B edition. Med den här integreringen kan du förhandsgranska din e-poståtergivning i vanliga e-postklienter. Med det här verktyget kan du se till att e-postinnehållet ser bra ut och fungerar som det ska i alla inkorgar.

1. När din e-postdesign är klar och klar att testas klickar du på **[!UICONTROL Simulate content]** i e-postdesignområdet.

1. Klicka på **[!UICONTROL Render email]** överst till höger.

   ![Återge e-postknapp](./assets/email-simulate-render-button.png)

   Om du ännu inte har anslutit till ditt Litmus-konto från Journey Optimizer B2B edition kan du välja mellan att starta ett provkonto eller ansluta till ditt befintliga konto.

1. Klicka på **[!UICONTROL Connect your Litmus account]** överst till höger eller använd länken inuti sidan.

   ![Anslut ditt Litmus-konto](./assets/email-simulate-render-litmus-connect.png)

1. Ange dina autentiseringsuppgifter och klicka på **[!UICONTROL Sign in]**.

   >[!IMPORTANT]
   >
   >När du ansluter ditt Litmus-konto till Journey Optimizer B2B edition godkänner du att testmeddelanden skickas till Litmus. Efter att de skickats hanteras dessa e-postmeddelanden inte längre av Adobe. Som en följd av detta gäller regeln för lagring av Litmus-data för dessa e-postmeddelanden, inklusive personaliseringsdata som kan inkluderas i testmeddelandena.

1. Klicka på **[!UICONTROL Run test]** längst upp till höger för att generera förhandsgranskningar via e-post.

1. Kontrollera e-postinnehållet i vanliga dator-, mobil- och webbaserade klienter.

   ![Förhandsgranskningar i Litmus-e-post](./assets/email-simulate-render-litmus-previews.png)

   Klicka på miniatyrbilden som visas om du vill visa information om något av de återgivna klienttesterna.

1. När du är klar med granskningen klickar du på bakåtpilen ( ![Visa eller dölj filterikonen](../../assets/do-not-localize/icon_back-arrow.svg) ) längst upp till vänster för att återgå till sidan Simulera innehåll.

   Du kan välja en annan profil och göra ett annat återgivningstest, eller gå tillbaka till e-postdesignområdet och göra nödvändiga justeringar baserat på granskningen.

