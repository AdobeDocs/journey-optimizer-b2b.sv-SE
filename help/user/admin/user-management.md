---
title: Användarhantering
description: Lär dig hur du tilldelar teammedlemmar till produktprofiler för Journey Optimizer B2B edition.
feature: Setup
roles: Admin
exl-id: ddbdc6a5-49bc-46cd-8d9b-1d37223dffe2
source-git-commit: 44a3bb6d986726dbbd9d2854e4fce321eac56824
workflow-type: tm+mt
source-wordcount: '1221'
ht-degree: 0%

---

# Användarhantering

När etableringen är klar och sandlådorna är bundna utför du följande steg för att ge ditt team och dina användare tillgång till Adobe Journey Optimizer B2B edition.

1. [Skapa en produktprofil ](#marketo-engage-profile) för Marketo Engage i Admin Console (endast för den nya instansen Marketo Engage).
1. [Skapa en användargrupp](#create-user-group) i Admin Console.
1. [Redigera inbyggda roller](#edit-roles) eller [skapa en anpassad roll](#create-a-custom-role) med Journey Optimizer B2B edition-behörigheter.
1. [Lägg till användare](#add-users) eller [grupper](#add-user-groups-to-a-role) i roller.

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

Mer information om hur du använder produktprofiler för användarberättiganden finns i [Hantera produktprofiler för företagsanvändare](https://helpx.adobe.com/enterprise/using/manage-product-profiles.html){target="_blank"} i Admin Console-dokumentationen.
<!--
>[!BEGINSHADEBOX]

When you add a user to the Marketo Engage product profile, they are subsequently added to the _Standard User_ role within the Default workspace of the Marketo Engage subscription. This role grants them all _Standard User_ permissions for Marketo Engage in that workspace. Currently, all Journey Optimizer B2B Edition users are required to be Marketo Engage users. A Marketo Engage administrator can restrict access by updating the permissions for the _Standard User_ role or by moving the user to a different Marketo Engage user role with more restrictive permissions.

For more information about managing these permissions within Marketo Engage, see [Managing User Roles and Permissions](https://experienceleague.adobe.com/en/docs/marketo/using/product-docs/administration/users-and-roles/managing-user-roles-and-permissions){target="_blank"} in the Marketo Engage documentation.

>[!ENDSHADEBOX]-->

>[!NOTE]
>
>En systemadministratör för Admin Console eller en produktadministratör för Marketo Engage kan utföra dessa steg.

1. Logga in på [https://adminconsole.adobe.com](https://adminconsole.adobe.com).

1. Välj fliken **[!UICONTROL Products]**.

1. Öppna den Marketo Engage-instans där du vill lägga till profilen och klicka på **[!UICONTROL New profile]**.

   ![Admin Console - Marketo Engage - instans - ny profil](./assets/admin-console-marketo-engage-instance-new-profile.png){width="700" zoomable="yes"}

1. Ange ett produktprofilnamn, till exempel _Standardanvändare_.

1. Klicka på **Nästa** och sedan på **Spara**.

## Skapa en användargrupp {#create-user-group}

En användargrupp är en samling användare som tilldelas en delad uppsättning behörigheter. Du kan lägga till eller ta bort användare i din användargrupp. Gruppbehörigheterna förblir desamma medan användarna i gruppen ändras.

Mer information om hur användargrupper används för att hantera behörigheter finns i [Hantera användargrupper](https://helpx.adobe.com/enterprise/using/user-groups.html){target="_blank"} i Admin Console-dokumentationen.

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

## Lägga till användare i en grupp

>[!NOTE]
>
>En Admin Console-systemadministratör kan utföra dessa steg.

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

## Redigera roller för produktbehörigheter {#edit-roles}

Behörigheter är enhetsbehörigheter som gör att du kan definiera de behörigheter som tilldelats en produktprofil. Varje tillstånd samlas in med en funktion, till exempel resor eller köpgrupper, som representerar olika funktioner eller objekt i Journey Optimizer B2B edition.

Under _Behörigheter_ i Adobe Experience Platform kan administratörer definiera användarroller och åtkomstprinciper för att hantera åtkomstbehörigheter för funktioner och objekt i ett produktprogram. I det här programmet kan du skapa och hantera roller samt tilldela önskade resursbehörigheter för rollerna. Med behörigheter kan du också hantera sandlådor och användare som är associerade med en viss roll.

Mer information om rollbehörigheter i Experience Platform finns i [Hantera behörigheter för en roll](https://experienceleague.adobe.com/en/docs/experience-platform/access-control/abac/permissions-ui/permissions){target="_blank"} i dokumentationen för Experience Platform.
<!-- 
### B2B product permissions

The following permissions govern access to Journey Optimizer B2B Edition capabilities:

| Category | Description | Permissions |
| -------- | ----------- | ---------- |
| B2B Account Lists | Configure, manage, view, and publish permissions for B2B account lists. These permissions include actions such as add, remove, import, and delete accounts from account lists. | <li>Manage B2B Account Lists |
| B2B Admin Configurations | Configure, manage, and view permissions for B2B administrative configurations. These permissions include digital asset management connections, asset repositories, and events. | <li>Manage B2B Admin Configurations |
| B2B Assets | Configure, manage, and view permissions for B2B assets. These permissions include emails, SMS, landing pages, fragments, templates, and images. | <li>Manage B2B Assets <li>Manage B2B Templates <li>Manage B2B Fragments|
| B2B Buying Groups | Configure, manage, and view permissions for B2B buying groups. These permissions include solution interests, roles templates, and buying group status. | <li>Manage B2B Buying Groups |
| B2B Channel Configurations | Configure, manage, and view permissions for B2B channel configurations. These permissions include settings for communication limits, API credentials, and security settings. | <li>Manage B2B Channels Configurations |
| B2B Dashboards |Configure and view permissions for B2B dashboards. These permissions include account engagement, buying group stages, surging accounts, and contact coverage. | <li>Manage B2B Dashboards |
| B2B Journeys | Configure manage, view, and publish permissions for B2B journeys. These permissions include account and person actions, event listeners, and split paths | <li>Manage B2B Journeys |

### B2B built-in roles

When your organization has the Journey Optimizer B2B Edition product provisioned, Experience Platform includes a set of built-in (default) roles that you can use to manage access to the product capabilities:

| Role | Permissions |
| ---- | ----------- |
| B2B Journey Manager | <li>Manage B2B Journeys <li>Manage B2B Buying Groups <li>Manage B2B Account Lists <li>View B2B Intelligent Dashboard <li>View B2B Insights Dashboard |
| B2B Channel Manager | <li>Manage B2B Assets <li>Manage B2B Templates <li>Manage B2B Fragments |
| B2B System Administrator | <li>Manage B2B Channels Configurations <li>Manage B2B Admin Configurations |
| B2B Sales User | <li>View Intelligent Dashboard |

### Edit role permissions

For built-in or custom roles, you can decide at any time to add or delete permissions. If you modify a default or custom role, it impacts every user assigned to the role.

In the following example, you want to add permissions related to the B2B Journeys resource for users assigned to the B2B Channel Manager role. This change enables users for that role to manage account journeys also.

>[!NOTE]
>
>An Admin Console system administrator can perform these steps.

_To change the permissions for a role:_

1. Go to [experience.adobe.com](https://experience.adobe.com/).

1. In the _[!UICONTROL Quick access]_ panel, select **[!UICONTROL Permissions]**.

   >[!NOTE]
   >
   >If you don't see _[!UICONTROL Permissions]_, you may need to click **[!UICONTROL View all]** and select it from the available applications.

   ![Experience Platform - access Permissions](./assets/aep-permissions.png){width="700" zoomable="yes"}

1. Select **[!UICONTROL Roles]** in the left navigation.

1. Click the **_B2B Channel Manager_** role name.

1. In the details page, click **[!UICONTROL Edit]** at the top right.

   ![Experience Platform - edit the role](./assets/aep-permissions-role-edit.png){width="700" zoomable="yes"}

   In the role editor, the _[!UICONTROL Resources]_ menu displays the list of resources that apply to the Experience Cloud - Platform powered applications products.

   You can enter _B2B_ in the search tool to filter the list for the B2B product permissions. 
   
1. Click the _Add_ icon (**+**) for the B2B Journeys resource.

   ![Experience Platform - edit the role](./assets/aep-permissions-role-edit-b2b-journeys-add.png){width="700" zoomable="yes"}

1. In the _[!UICONTROL B2B Journeys]_ permissions card, select **[!UICONTROL Manage B2B Account Journeys]**.

1. Click **[!UICONTROL Save]**.

   ![Experience Platform - edit the role](./assets/aep-permissions-role-edit-b2b-journeys-done.png){width="700" zoomable="yes"}

1. Click **[!UICONTROL Close]** to return to the details page. -->

### Lägga till användare i en roll

>[!NOTE]
>
>En Admin Console-systemadministratör kan utföra dessa steg.

1. Öppna rollinformationen och välj fliken **[!UICONTROL Users]**.

   På den här fliken visas en lista med alla användare som tilldelats rollen.

1. Klicka på **[!UICONTROL Add users]**.

   ![Experience Platform - lägg till användare i rollen](./assets/aep-permissions-role-add-users.png){width="700" zoomable="yes"}

1. I dialogrutan _[!UICONTROL Add users]_letar du reda på och väljer de användare som du vill lägga till i rollen.

   * Du kan använda sökverktyget för att filtrera listan med användare.

   * Markera kryssrutan för varje användare.

   ![Experience Platform - Dialogrutan Lägg till användare](./assets/aep-permissions-role-add-users-dialog.png){width="600" zoomable="yes"}

1. Klicka på **[!UICONTROL Save]** när du har markerat alla användare som du vill lägga till.

### Lägga till användargrupper i en roll

>[!NOTE]
>
>En Admin Console-systemadministratör kan utföra dessa steg.

Mer information om användarhantering finns i [Admin Console-användare](https://helpx.adobe.com/enterprise/using/user-groups.html) i dokumentationen för Admin Console.

1. Öppna rollinformationen och välj fliken **[!UICONTROL User groups]**.

   På den här fliken visas en lista med alla användargrupper som tilldelats rollen.

1. Klicka på **[!UICONTROL Add Groups]**.

   ![Experience Platform - lägg till användare i rollen](./assets/aep-permissions-role-add-groups.png){width="700" zoomable="yes"}

1. I dialogrutan _[!UICONTROL Add groups]_letar du reda på och markerar de grupper som du vill lägga till i rollen.

   * Du kan använda sökverktyget för att filtrera listan med användargrupper.

   * Markera kryssrutan för varje användargrupp.

   ![Experience Platform - Dialogrutan Lägg till grupper](./assets/aep-permissions-role-add-groups-dialog.png){width="600" zoomable="yes"}

1. Klicka på **[!UICONTROL Save]** när du har markerat alla användare som du vill lägga till.

## Skapa en anpassad roll

>[!NOTE]
>
>En Admin Console-systemadministratör kan utföra dessa steg.

1. Välj **[!UICONTROL Roles]** i den vänstra navigeringen och välj **[!UICONTROL Create role]**.

1. I dialogrutan _[!UICONTROL Create new role]_anger du ett namn för rollen, till exempel_ B2B-marknadsförare _, och en beskrivning (valfritt).

1. Klicka på **[!UICONTROL Confirm]**.

1. Markera dina sandlådor.

   ![Experience Platform - lägg till sandlådor för den nya rollen](./assets/aep-permissions-role-sandboxes.png){width="700" zoomable="yes"}

1. Lägg till profilbehörigheter:

   * Leta reda på objektet **[!UICONTROL Profile Management]** i listan _[!UICONTROL Resources]_till vänster och klicka på ikonen_ Lägg till _(**+**) för att lägga till attributet.

   * Lägg till följande behörigheter för attributet:
      * [!UICONTROL View segments]
      * [!UICONTROL Manage segments]
      * [!UICONTROL View profiles]
      * [!UICONTROL Manage profiles]
      * [!UICONTROL View B2B profile]
      * [!UICONTROL Manage B2B profile]

   ![Experience Platform - lägg till profiler för den nya rollen](./assets/aep-permissions-role-profiles.png){width="700" zoomable="yes"}

1. Lägg till produktbehörigheter för B2B:

   Se listan över [B2B-produktbehörigheter](#b2b-product-permissions) för att ta reda på vilka produktfunktioner du vill använda för rollen.

   Leta reda på **[!UICONTROL B2B]**-objekten i listan _[!UICONTROL Resources]_till vänster och klicka på ikonen_ Lägg till _(**+**) för att lägga till varje attribut som du vill aktivera för rollen.

   Du kan ange _B2B_ i sökverktyget för att filtrera listan över B2B-produktbehörigheter.

1. Klicka på **[!UICONTROL Save]** överst till höger.

1. Gå till rollinformationen och välj fliken **[!UICONTROL User groups]**.

1. Klicka på **[!UICONTROL Add Groups]**.

   ![Experience Platform - lägg till profiler för den nya rollen](./assets/aep-permissions-role-add-groups.png){width="700" zoomable="yes"}

1. Markera kryssrutan bredvid användargruppen som du skapade tidigare i Admin Console.

1. Klicka på **[!UICONTROL Save]**.
