---
title: Testa e-poståtergivning
description: Testa e-poståtergivning på datorer, mobiler och webbklienter med Litmus-integrering för att säkerställa inkorgens kompatibilitet i Journey Optimizer B2B edition.
feature: Email Authoring, Integrations
level: Intermediate
role: User
exl-id: 26d87a56-6bd1-4d4a-8090-71f5b0a7e9f8
source-git-commit: 79012352c3ae4e2f3d38b632b1f523d262f74f96
workflow-type: tm+mt
source-wordcount: '352'
ht-degree: 0%

---

# Testa e-poståtergivning med Litmus

Om du vill testa dina e-postmeddelanden kan du använda ett [Litmus](https://www.litmus.com/email-testing){target="_blank"} Enterprise-konto från Journey Optimizer B2B edition. Med den här integreringen kan du förhandsgranska din e-poståtergivning i vanliga e-postklienter. Med det här verktyget kan du se till att e-postinnehållet ser bra ut och fungerar som det ska i alla inkorgar.

>[!AVAILABILITY]
>
>Den här integreringen är endast tillgänglig för Journey Optimizer B2B edition-användare med Litmus Enterprise-konton. Mer information finns på [lösningssidan på Litmus-webbplatsen](https://www.litmus.com/solutions/esp/adobe-journey-optimizer){target="_blank"}.

1. När din e-postdesign är klar och klar att testas klickar du på **[!UICONTROL Simulate content]** i e-postdesignområdet.

1. Klicka på **[!UICONTROL Render email]** överst till höger.

   ![Återge e-postknapp](./assets/email-simulate-render-button.png){width="700" zoomable="yes"}

   Om du ännu inte har anslutit till ditt Litmus-konto från Journey Optimizer B2B edition kan du välja mellan att starta ett provkonto eller ansluta till ditt befintliga konto.

1. Klicka på **[!UICONTROL Connect your Litmus account]** överst till höger eller använd länken inuti sidan.

   ![Anslut ditt Litmus-konto](./assets/email-simulate-render-litmus-connect.png){width="700" zoomable="yes"}

1. Ange dina inloggningsuppgifter för Litmus-kontot och klicka på **[!UICONTROL Sign in]**.

1. Klicka på **[!UICONTROL Connect]** för att bekräfta anslutningen mellan Litmus och Journey Optimizer B2B edition och skicka e-postinnehållet för återgivning.

   >[!IMPORTANT]
   >
   >När du ansluter ditt Litmus-konto till Journey Optimizer B2B edition godkänner du att testmeddelanden skickas till Litmus. Innehållet hanteras sedan i Litmus och inte i Adobe. Som en följd av detta gäller regeln för lagring av Litmus-data för dessa e-postmeddelanden, inklusive personaliseringsdata som kan inkluderas i testmeddelandena.

1. Klicka på **[!UICONTROL Run test]** längst upp till höger för att generera förhandsgranskningar via e-post.

   ![Kör ett Litmus-återgivningstest](./assets/email-simulate-render-litmus-run-test.png){width="700" zoomable="yes"}

1. Kontrollera e-postinnehållet i vanliga dator-, mobil- och webbaserade klienter.

   Klicka på miniatyrbilden som visas om du vill visa information om något av de återgivna klienttesterna.

   ![Förhandsgranskningar i Litmus-e-post](./assets/email-simulate-render-litmus-previews.png){width="700" zoomable="yes"}

1. När du är klar med granskningen klickar du på bakåtpilen ( ![Visa eller dölj filterikonen](../../assets/do-not-localize/icon_back-arrow.svg) ) längst upp till vänster för att återgå till sidan Simulera innehåll.

   Du kan välja en annan profil och göra ett annat återgivningstest, eller gå tillbaka till e-postdesignområdet och göra nödvändiga justeringar baserat på granskningen.
