---
title: Användarhantering
description: Lär dig hur du tilldelar teammedlemmar till produktprofiler för Journey Optimizer B2B Edition.
feature: Setup
roles: Admin
exl-id: ddbdc6a5-49bc-46cd-8d9b-1d37223dffe2
source-git-commit: f8ae6e51e76ded14316273c8e746ed814e7eb68b
workflow-type: tm+mt
source-wordcount: '976'
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

   När inloggningen är klar visas sidan _Översikt_ i Adobe Admin Console.

1. Om du har tillgång till flera organisationer måste du se till att du har loggat in i rätt organisation.

   Om du vill ändra din organisation klickar du på organisationens namn i det övre högra hörnet och väljer den organisation som du behöver åtkomst till.

1. Välj **[!UICONTROL Administrators]** från _[!UICONTROL Users]_-kortet för att verifiera att du är systemadministratör.

   ![Admin Console - översikt - klicka på Administratörer](./assets/admin-console-overview-administrators.png){width="700" zoomable="yes"}

1. Sök genom att ange Adobe ID e-postadress, användarnamn, för- eller efternamn.

   * Om din åtkomst är korrekt konfigurerad returnerar sökningen din post.

   * Om värdet i kolumnen **[!UICONTROL ADMIN ROLE]** visar `System` vet du att du (eller den användare som visas) är systemadministratör.

## Skapa produktprofilen för Marketo Engage {#marketo-engage-profile}

När du ger användare åtkomst till en Adobe-lösning behöver du inte nödvändigtvis ge dem full åtkomst. Med produktprofiler kan varje lösning ha en egen uppsättning användarbehörigheter. Använd Admin Console för att tilldela produktprofiler.

Mer information om hur du använder produktprofiler för användarrättigheter finns i [Hantera produktprofiler för företagsanvändare](https://helpx.adobe.com/enterprise/using/manage-product-profiles.html) i dokumentationen för Admin Console.

>[!NOTE]
>
>En systemadministratör för Admin Console eller en produktadministratör för Marketo Engage kan utföra dessa steg.

1. Logga in på [https://adminconsole.adobe.com](https://adminconsole.adobe.com).

1. Välj fliken **[!UICONTROL Products]**.

1. Öppna Market Engage-instansen där du vill lägga till profilen och klicka på Ny profil.

   ![Admin Console - Marketo Engage - instans - ny profil](./assets/admin-console-marketo-engage-instance-new-profile.png){width="700" zoomable="yes"}

1. Ange ett produktprofilnamn, till exempel _Standardanvändare_.

1. Klicka på **Nästa** och sedan på **Spara**.

## Skapa en användargrupp {#create-user-group}

En användargrupp är en samling användare som tilldelas en delad uppsättning behörigheter. Du kan lägga till eller ta bort användare i din användargrupp. Gruppbehörigheterna förblir desamma medan användarna i gruppen ändras.

Mer information om hur användargrupper används för att hantera behörigheter finns i [Hantera användargrupper](https://helpx.adobe.com/enterprise/using/user-groups.html) i Admin Console-dokumentationen.

>[!NOTE]
>
>En Admin Console-systemadministratör kan utföra dessa steg.

1. Logga in på [https://adminconsole.adobe.com](https://adminconsole.adobe.com).

1. Välj fliken **[!UICONTROL Users]**.

1. Välj **[!UICONTROL User Groups]** i den vänstra navigeringen.

1. Klicka på **[!UICONTROL New user group]** överst till höger.

1. Ange ett namn för användargruppen, till exempel _Standardanvändare_, och klicka på **[!UICONTROL Save]**.

1. Klicka på användargruppen som du nyss skapade.

1. Välj fliken **[!UICONTROL Assigned product profiles]** och klicka på **[!UICONTROL Assign profile]**.

1. Klicka på **+** och lägg till varje instans av följande produkter:

   * [!UICONTROL Marketo Engage]
   * [!UICONTROL Adobe Experience Platform - AEP-Default-All-Users]
   * [!UICONTROL Adobe Experience Platform Data Collection]
   * [!UICONTROL Data Collection All Access]

   ![Admin Console - användargrupp - lägg till produkter](./assets/admin-console-user-group-add-products.png){width="700" zoomable="yes"}

1. Klicka på **[!UICONTROL Save]**.

## Skapa en roll i AEP-behörigheter {#create-role}

Behörigheter är enhetsbehörigheter som gör att du kan definiera de behörigheter som tilldelats en produktprofil. Varje tillstånd samlas in med en funktion, till exempel resor eller köpgrupper, som representerar de olika funktionerna eller objekten i Journey Optimizer B2B Edition.

Under _Behörigheter_ i Adobe Experience Platform kan administratörer definiera användarroller och åtkomstprinciper för att hantera åtkomstbehörigheter för funktioner och objekt i ett produktprogram. I det här programmet kan du skapa och hantera roller samt tilldela önskade resursbehörigheter för rollerna. Med behörigheter kan du också hantera etiketter, sandlådor och användare som är kopplade till en viss roll.

Mer information finns i [Hantera behörigheter för en roll](https://experienceleague.adobe.com/en/docs/experience-platform/access-control/abac/permissions-ui/permissions) i Experience Platform-dokumentationen.

>[!NOTE]
>
>För att kunna utföra följande steg måste du vara produktadministratör för Adobe Experience Platform.

1. Gå till [experience.adobe.com](https://experience.adobe.com/).

1. Välj **[!UICONTROL Permissions]** på panelen _[!UICONTROL Quick access]_.

   >[!NOTE]
   >
   >Om du inte ser _[!UICONTROL Permissions]_kan du behöva klicka på&#x200B;**[!UICONTROL View all]**och välja det bland de tillgängliga programmen.

   ![Experience Platform - åtkomstbehörigheter](./assets/aep-permissions.png){width="700" zoomable="yes"}

1. Välj **[!UICONTROL Roles]** i den vänstra navigeringen och välj **[!UICONTROL Create role]**.

1. I dialogrutan _[!UICONTROL Create new role]_anger du ett namn för rollen, till exempel_ AJO B2B _, och en beskrivning (valfritt).

1. Klicka på **[!UICONTROL Confirm]**.

1. Markera dina sandlådor.

   ![Experience Platform - lägg till sandlådor för den nya rollen](./assets/aep-permissions-role-sandboxes.png){width="700" zoomable="yes"}

1. Lägg till profilbehörigheter:

   * Leta reda på objektet **[!UICONTROL Profile Management]** i listan _[!UICONTROL Resources]_till vänster och klicka på plusikonen (**+**) för att lägga till attributet.

   * Lägg till följande behörigheter för attributet:
      * [!UICONTROL View segments]
      * [!UICONTROL Manage segments]
      * [!UICONTROL View profiles]
      * [!UICONTROL Manage profiles]
      * [!UICONTROL View B2B profile]
      * [!UICONTROL Manage B2B profile]

   ![Experience Platform - lägg till profiler för den nya rollen](./assets/aep-permissions-role-profiles.png){width="700" zoomable="yes"}

1. Klicka på **[!UICONTROL Save]** överst till höger.

1. Gå till rollinformationen och välj fliken **[!UICONTROL User groups]**.

1. Klicka på **[!UICONTROL Add Groups]**.

   ![Experience Platform - lägg till profiler för den nya rollen](./assets/aep-permissions-role-add-groups.png){width="700" zoomable="yes"}

1. Markera kryssrutan bredvid användargruppen som du skapade tidigare i Admin Console.

1. Klicka på **[!UICONTROL Save]**.

## Lägga till användare i gruppen i Admin Console

>[!NOTE]
>
>En Admin Console-systemadministratör eller en produktadministratör kan utföra dessa steg.

Mer information om användarhantering finns i [Admin Console-användare](https://helpx.adobe.com/enterprise/using/user-groups.html) i dokumentationen för Admin Console.

1. Gå till [https://adminconsole.adobe.com](https://adminconsole.adobe.com).

1. Klicka på **[!UICONTROL Add users]** under _[!UICONTROL Quick links]_.

1. Lägg till varje användare:

   * Ange användarens e-postadress, förnamn och efternamn.

     ![Experience Platform - lägg till profiler för den nya rollen](./assets/admin-console-add-users.png){width="600" zoomable="yes"}

   * För **[!UICONTROL User groups]** klickar du på **+**.

   * Markera användargruppen som du skapade tidigare.

   * Klicka på **[!UICONTROL Apply]**.

1. Klicka på **[!UICONTROL Save]**.
