---
title: Användarhantering
description: Lär dig hur du tilldelar teammedlemmar till produktprofiler för Journey Optimizer B2B Edition.
feature: Setup
roles: Admin
source-git-commit: dcd8ab2820d60654e8970944054142fc296ed54f
workflow-type: tm+mt
source-wordcount: '811'
ht-degree: 0%

---

# Användarhantering

När etableringen är klar och sandlådorna är bundna utför du följande steg för att ge ditt team och dina användare tillgång till Adobe Journey Optimizer B2B Edition.

1. [Skapa en produktprofil ](#marketo-engage-profile) för Marketo Engage i Admin Console (endast för den nya instansen Marketo Engage).
1. [Skapa en användargrupp](#create-user-group) i Admin Console.
1. [Skapa en roll](#create-role) i AEP-behörigheter.
1. [Lägg till användare](#add-users) i Admin Console.

Som administratör kan du utföra dessa uppgifter i Adobe Admin Console, som är en central plats för att administrera och hantera produktlicenser och användare för Adobe. På Admin Console kan du skapa och hantera användare på en och samma plats i stället för i de olika individuella lösningarna. Mer information om funktioner och funktioner finns på [Admin Console-översiktssidan](https://helpx.adobe.com/se/enterprise/using/admin-console.html).

## Gå till Admin Console

Innan du kan använda Admin Console för att administrera användare i ditt team måste du se till att du har tillgång till Admin Console och rätt behörigheter.

1. Som systemadministratör bör du få flera e-postmeddelanden från Adobe som en del av introduktionsprocessen.

   Leta efter det välkomstmeddelande som innehåller information om organisationens namn som du har beviljats åtkomst till.

1. Klicka på länken **[!UICONTROL Get started]** i ditt välkomstmeddelande för att navigera till Admin Console.

   Om du inte kan hitta e-postmeddelandet öppnar du en webbläsare direkt till Admin Console på [https://adminconsole.adobe.com](https://adminconsole.adobe.com).

1. Logga in med din Adobe ID.

   När inloggningen är klar visas sidan Översikt i Adobe Admin Console.

1. Om du har tillgång till flera organisationer måste du se till att du har loggat in i rätt organisation.

   Om du vill ändra din organisation klickar du på organisationens namn i det övre högra hörnet och väljer den organisation som du behöver åtkomst till.

1. Välj Administratörer på användarkortet för att verifiera att du är systemadministratör.

1. Sök genom att ange Adobe ID e-postadress, användarnamn, för- eller efternamn.

   * Om din åtkomst är korrekt konfigurerad returnerar sökningen din post.

   * Om värdet i kolumnen **[!UICONTROL ADMIN ROLE]** visar `System` vet du att du (eller den användare som visas) är systemadministratör.

## Skapa produktprofilen för Marketo Engage {#marketo-engage-profile}

När du ger användare åtkomst till en Adobe-lösning behöver du inte nödvändigtvis ge dem full åtkomst. Med produktprofiler kan varje lösning ha en egen uppsättning användarbehörigheter. Använd Admin Console för att tilldela produktprofiler.

>[!NOTE]
>
>Dessa steg kan bara utföras av systemadministratören eller produktadministratören i Marketo Engage. Admin Console.

1. Logga in på [https://adminconsole.adobe.com](https://adminconsole.adobe.com).

1. Välj Produkter > Marketo Engage.

1. Klicka på Ny profil och ange ett produktprofilnamn, till exempel _Standardanvändare_.

1. Klicka på Nästa > Spara

## Skapa en användargrupp {#create-user-group}

En användargrupp är en samling användare som tilldelas en delad uppsättning behörigheter. Du kan lägga till eller ta bort användare i din användargrupp. Gruppbehörigheterna förblir desamma medan användarna i gruppen ändras.

>[!NOTE]
>
>Dessa steg kan bara utföras av en systemadministratör i Admin Console.

1. Logga in på [https://adminconsole.adobe.com](https://adminconsole.adobe.com).

1. Välj **[!UICONTROL Users]** > **[!UICONTROL User Groups]** > **[!UICONTROL New user group]**.

1. Ange ett namn för användargruppen, till exempel _Standardanvändare_, och klicka på **[!UICONTROL Save]**.

1. Klicka på användargruppen som du nyss skapade.

1. Klicka på **[!UICONTROL Assigned product profiles]** > **[!UICONTROL Assign profile]**.

1. Välj följande produkter:
   * [!UICONTROL Marketo Engage - Standard User]
   * [!UICONTROL Adobe Experience Platform - AEP-Default-All-Users]
   * [!UICONTROL Adobe Experience Platform Data Collection - Default]
   * [!UICONTROL Data Collection All Access]

1. Klicka på **[!UICONTROL Save]**.

## Skapa en roll i AEP-behörigheter {#create-role}

Behörigheter är enhetsbehörigheter som gör att du kan definiera de behörigheter som tilldelats en produktprofil. Varje tillstånd samlas in med en funktion, till exempel resor eller köpgrupper, som representerar de olika funktionerna eller objekten i Journey Optimizer B2B Edition.

_Behörigheter_ är det område i Adobe Experience Platform där administratörer kan definiera användarroller och åtkomstprinciper för att hantera åtkomstbehörigheter för funktioner och objekt i ett produktprogram. I det här programmet kan du skapa och hantera roller samt tilldela önskade resursbehörigheter för rollerna. Med behörigheter kan du också hantera etiketter, sandlådor och användare som är kopplade till en viss roll.

>[!NOTE]
>
>För att kunna utföra följande steg måste du vara produktadministratör för Adobe Experience Platform.

1. Gå till [experience.adobe.com](https://experience.adobe.com/).

1. Välj **[!UICONTROL Permissions]**.

   >[!NOTE]
   >
   >Om du inte ser behörigheterna kan du behöva klicka på Visa alla och välja det bland de tillgängliga programmen.

1. Välj **[!UICONTROL Roles]** i den vänstra navigeringen och välj **[!UICONTROL Create role]**.

1. I dialogrutan _[!UICONTROL Create new role]_anger du ett namn för rollen, till exempel_ Standardanvändare _, och en beskrivning (valfritt).

1. Klicka på **[!UICONTROL Confirm]**.

1. Markera dina sandlådor.

1. Lägg till profilbehörigheter:

   * Leta reda på objektet **[!UICONTROL Profile Management]** i listan _[!UICONTROL Resources]_till vänster och klicka på plusikonen (**+**) för att lägga till attributet.

   * Lägg till följande behörigheter för attributet:
      * [!UICONTROL View segments]
      * [!UICONTROL Manage segments]
      * [!UICONTROL View profiles]
      * [!UICONTROL Manage profiles]
      * [!UICONTROL View B2B profile]
      * [!UICONTROL Manage B2B profile]

1. Klicka på **[!UICONTROL Save]** överst till höger.

1. Välj **[!UICONTROL User groups]** > **[!UICONTROL Add Groups]**.

1. Markera kryssrutan bredvid användargruppen som du skapade tidigare i Admin Console.

1. Klicka på **[!UICONTROL Save]**.

## Lägga till användare i Admin Console

>[!NOTE]
>
>Dessa steg kan bara utföras av en systemadministratör eller en produktadministratör i Admin Console.

1. Gå till [https://adminconsole.adobe.com](https://adminconsole.adobe.com).

1. Klicka på **[!UICONTROL Add users]**.

1. Lägg till varje användare:

   * Ange användarens e-postadress, förnamn och efternamn.
   * Klicka på [!UICONTROL User groups].
   * Markera användargruppen som du skapade tidigare.

1. Klicka på **[!UICONTROL Apply]**.

1. Klicka på **[!UICONTROL Save]**.
