---
title: E-postborttagning
description: Lär dig hur du använder borttagning av dubbletter via e-post i kontoresor för att förhindra att samma e-post skickas flera gånger till samma e-postadress.
feature: Account Journeys, Channels
topic: Content Management
role: User
level: Beginner, Intermediate
keywords: e-post, borttagning av dubbletter, resa, duplicera
source-git-commit: 89dcfae6293fc2bd1eefb58943bee354c57bc73a
workflow-type: tm+mt
source-wordcount: '334'
ht-degree: 0%

---

# Deduplicering av e-post

Använd deduplicering av e-post i kontoresor för att säkerställa att samma e-post inte skickas flera gånger till samma e-postadress under en resa. När du aktiverar den här funktionen blockeras dubblettadresser tills den första posten med den e-postadressen slutför resan. När ett konto har avslutat en resa kan en person kvalificera sig för att få e-post igen som en del av ett nytt konto som förs in på resan.

## När borttagning av e-post ska användas

Det finns några viktiga scenarier där du bör överväga att aktivera borttagning av e-post:

* **E-postadressen används inte som en identitet i Real-Time CDP** - samma e-postadress kan visas för flera personprofiler. Aktivera den här funktionen om dessa dubblettprofiler kvalificerar sig för samma resa och du vill förhindra att e-postmeddelandet skickas mer än en gång.

* **En person som är associerad med flera konton** - Om din Real-Time CDP-datamodell tillåter att en person kan associeras med flera konton, och du vill undvika att skicka samma e-postadress två gånger till den personen när flera konton (inklusive profiler med samma e-postadress) kvalificerar för samma resa, aktiverar du den här funktionen.

>[!NOTE]
>
>Borttagning av dubbletter via e-post gäller på kundresenivå. Om en person med samma e-postadress kvalificerar sig för olika resor kan de fortfarande få e-post från varje resa.

## Aktivera deduplicering av e-post för en resa

Så här aktiverar du deduplicering av e-post för en kontoresa:

1. Öppna en kontoresa.

1. Klicka på **[!UICONTROL More]** (**..**) i det övre högra hörnet av arbetsytan för resan.

   ![Researbetsyta med Mer-menyn utökad med alternativet E-postborttagning &#x200B;](./assets/email-deduplication-more-menu.png){width="450"}

1. Välj **[!UICONTROL Email Deduplication]**.

1. Markera kryssrutan **[!UICONTROL Email Deduplication]** i dialogrutan.

   ![Dialogrutan Deduplicering av e-post med växling aktiverat](./assets/email-deduplication-dialog.png){width="400"}

1. Klicka på **[!UICONTROL Save]**.

När borttagning av e-post är aktiverat kontrolleras varje e-postadress innan e-postmeddelandet skickas. Om en post med samma e-postadress redan har angetts för den resan blockeras den nya posten tills den första posten slutför resan.
