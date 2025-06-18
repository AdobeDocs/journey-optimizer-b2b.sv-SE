---
title: Användarhantering
description: Lär dig hur du tilldelar teammedlemmar till produktprofiler för Journey Optimizer B2B edition.
feature: Setup, Permissions
roles: Admin
exl-id: ddbdc6a5-49bc-46cd-8d9b-1d37223dffe2
source-git-commit: ae2acbde4fbabb5d49a532e8060005acf04f8b26
workflow-type: tm+mt
source-wordcount: '693'
ht-degree: 0%

---

# Användarhantering

När etableringen är klar och sandlådorna är bundna utför du följande steg för att ge ditt team och dina användare tillgång till Adobe Journey Optimizer B2B edition.

1. [Skapa en Marketo Engage-produktprofil](#marketo-engage-profile) i Admin Console (endast ny Marketo Engage-instans).
1. [Skapa en användargrupp](#create-user-group) i Admin Console.
<!-- 1. [Edit built-in roles](#edit-roles) or [create a custom role](#create-a-custom-role) with Journey Optimizer B2B Edition permissions. 
1. [Add users](#add-users) or [groups](#add-user-groups-to-a-role) to roles. -->

Som administratör kan du utföra dessa uppgifter i Adobe Admin Console, som är en central plats för att administrera och hantera dina Adobe produktlicenser och användare. I Admin Console kan du skapa och hantera användare på en och samma plats i stället för i de olika individuella lösningarna. På sidan [Admin Console - översikt](https://helpx.adobe.com/se/enterprise/using/admin-console.html) finns mer information om funktioner och funktioner.

## Öppna Admin Console

Innan du kan använda Admin Console för att administrera användare i ditt team måste du se till att du har tillgång till Admin Console och rätt behörigheter.

1. Som systemadministratör bör du få flera e-postmeddelanden från Adobe som en del av introduktionsprocessen.

   Leta efter det välkomstmeddelande som innehåller information om organisationens namn som du har beviljats åtkomst till.

1. Klicka på länken **[!UICONTROL Get started]** i ditt välkomstmeddelande för att navigera till Admin Console.

   Om du inte hittar e-postmeddelandet kan du öppna en webbläsare direkt till Admin Console på [https://adminconsole.adobe.com](https://adminconsole.adobe.com).

1. Logga in med din Adobe ID.

   När inloggningen är klar visas sidan _Översikt_ i Adobe Admin Console.

1. Om du har tillgång till flera organisationer måste du se till att du har loggat in i rätt organisation.

   Om du vill ändra din organisation klickar du på organisationens namn i det övre högra hörnet och väljer den organisation som du behöver åtkomst till.

1. Välj **[!UICONTROL Administrators]** från _[!UICONTROL Users]_-kortet för att verifiera att du är systemadministratör.

   ![Admin Console - översikt - klicka på Administratörer](./assets/admin-console-overview-administrators.png){width="700" zoomable="yes"}

1. Sök genom att ange Adobe ID e-postadress, användarnamn, för- eller efternamn.

   * Om din åtkomst är korrekt konfigurerad returnerar sökningen din post.

   * Om värdet i kolumnen **[!UICONTROL ADMIN ROLE]** visar `System` vet du att du (eller den användare som visas) är systemadministratör.

## Skapa Marketo Engage produktprofil {#marketo-engage-profile}

När du ger användare tillgång till en Adobe-lösning behöver du inte nödvändigtvis ge dem fullständig åtkomst. Med produktprofiler kan varje lösning ha en egen uppsättning användarbehörigheter. Använd Admin Console för att tilldela produktprofiler.

Mer information om hur du använder produktprofiler för användarrättigheter finns i [Hantera produktprofiler för företagsanvändare](https://helpx.adobe.com/enterprise/using/manage-product-profiles.html){target="_blank"} i Admin Console-dokumentationen.
<!--
>[!BEGINSHADEBOX]

When you add a user to the Marketo Engage product profile, they are subsequently added to the _Standard User_ role within the Default workspace of the Marketo Engage subscription. This role grants them all _Standard User_ permissions for Marketo Engage in that workspace. Currently, all Journey Optimizer B2B Edition users are required to be Marketo Engage users. A Marketo Engage administrator can restrict access by updating the permissions for the _Standard User_ role or by moving the user to a different Marketo Engage user role with more restrictive permissions.

For more information about managing these permissions within Marketo Engage, see [Managing User Roles and Permissions](https://experienceleague.adobe.com/en/docs/marketo/using/product-docs/administration/users-and-roles/managing-user-roles-and-permissions){target="_blank"} in the Marketo Engage documentation.

>[!ENDSHADEBOX]-->

![Administratörsrollkrav](../../assets/do-not-localize/icon-admin-user.svg){width="30"} En systemadministratör eller Marketo Engage produktadministratör kan utföra följande steg.

1. Logga in på [https://adminconsole.adobe.com](https://adminconsole.adobe.com).

1. Välj fliken **[!UICONTROL Products]**.

1. Öppna Marketo Engage-instansen där du vill lägga till profilen och klicka på **[!UICONTROL New profile]**.

   ![Admin Console - Marketo Engage-instans - ny profil](./assets/admin-console-marketo-engage-instance-new-profile.png){width="700" zoomable="yes"}

1. Ange ett produktprofilnamn, till exempel _Standardanvändare_.

1. Klicka på **Nästa** och sedan på **Spara**.

## Skapa en användargrupp {#create-user-group}

En användargrupp är en samling användare som tilldelas en delad uppsättning behörigheter. Du kan lägga till eller ta bort användare i din användargrupp. Gruppbehörigheterna förblir desamma medan användarna i gruppen ändras.

Mer information om hur användargrupper används för att hantera behörigheter finns i [Hantera användargrupper](https://helpx.adobe.com/enterprise/using/user-groups.html){target="_blank"} i Admin Console-dokumentationen.

![Administratörsrollkrav](../../assets/do-not-localize/icon-admin-user.svg){width="30"} En systemadministratör kan utföra följande steg.

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

Mer information om användarhantering finns i [Admin Console-användare](https://helpx.adobe.com/enterprise/using/user-groups.html) i Admin Console-dokumentationen.

![Administratörsrollkrav](../../assets/do-not-localize/icon-admin-user.svg){width="30"} En systemadministratör eller produktadministratör kan utföra följande steg. En produktadministratör kan bara lägga till användare som redan finns i organisationen.

1. Gå till [https://adminconsole.adobe.com](https://adminconsole.adobe.com).

1. Klicka på **[!UICONTROL Add users]** under _[!UICONTROL Quick links]_.

1. Lägg till varje användare:

   * Ange användarens e-postadress, förnamn och efternamn.

     ![Experience Platform - lägg till profiler för den nya rollen](./assets/admin-console-add-users.png){width="600" zoomable="yes"}

   * För **[!UICONTROL User groups]** klickar du på **+**.

   * Markera användargruppen som du skapade tidigare.

   * Klicka på **[!UICONTROL Apply]**.

1. Klicka på **[!UICONTROL Save]**.

<!-- ## Edit roles for product permissions {#edit-roles}

Permissions are unitary rights that allow you to define the authorizations assigned to a product profile. Each permission is gathered under a capability, such as journeys or buying groups, which represents the different functionalities or objects in Journey Optimizer B2B Edition.

The _Permissions_ area of Adobe Experience Platform is where administrators can define user roles and access policies to manage access permissions for features and objects within a product application. In this app, you can create and manage roles, as well as assign the desired resource permissions for these roles. Permissions also allow you to manage the sandboxes and users associated with a specific role.

For more information about role permissions in Experience Platform, see [Manage permissions for a role](https://experienceleague.adobe.com/en/docs/experience-platform/access-control/abac/permissions-ui/permissions){target="_blank"} in the Experience Platform documentation.

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
| B2B Journey Manager | <li>Manage B2B Journeys <li>Manage B2B Buying Groups <li>Manage B2B Account Lists <li>View B2B Engagement Dashboard <li>View B2B Insights Dashboard |
| B2B Channel Manager | <li>Manage B2B Assets <li>Manage B2B Templates <li>Manage B2B Fragments |
| B2B System Administrator | <li>Manage B2B Channels Configurations <li>Manage B2B Admin Configurations |
| B2B Sales User | <li>View B2B Engagement Dashboard |

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

1. Click **[!UICONTROL Close]** to return to the details page.

### Add users to a role

![Administrator role requirements](../../assets/do-not-localize/icon-admin-user.svg){width="30"} A system administrator or AEP product administrator can perform the following steps. 

1. Open the role details and select the **[!UICONTROL Users]** tab.

   This tab displays a list of all users assigned to the role.

1. Click **[!UICONTROL Add users]**.

   ![Experience Platform - add users to the role](./assets/aep-permissions-role-add-users.png){width="700" zoomable="yes"}

1. In the _[!UICONTROL Add users]_ dialog, locate and select the users that you want to add to the role.

   * You can use the Search tool to filter the list of users. 

   * Select the checkbox for each user.

   ![Experience Platform - Add users dialog](./assets/aep-permissions-role-add-users-dialog.png){width="600" zoomable="yes"}

1. Click **[!UICONTROL Save]** when you have selected all the users that you want to add.

### Add user groups to a role

For information about user management, see [Admin Console users](https://helpx.adobe.com/enterprise/using/user-groups.html) in the Admin Console documentation.

![Administrator role requirements](../../assets/do-not-localize/icon-admin-user.svg){width="30"} A system administrator or AEP product administrator can perform the following steps. 

1. Open the role details and select the **[!UICONTROL User groups]** tab.

   This tab displays a list of all user groups assigned to the role. 

1. Click **[!UICONTROL Add Groups]**.

   ![Experience Platform - add users to the role](./assets/aep-permissions-role-add-groups.png){width="700" zoomable="yes"}

1. In the _[!UICONTROL Add groups]_ dialog, locate and select the groups that you want to add to the role.

   * You can use the Search tool to filter the list of user groups. 

   * Select the checkbox for each user group.

   ![Experience Platform - Add groups dialog](./assets/aep-permissions-role-add-groups-dialog.png){width="600" zoomable="yes"}

1. Click **[!UICONTROL Save]** when you have selected all the users that you want to add.

## Create a custom role

![Administrator role requirements](../../assets/do-not-localize/icon-admin-user.svg){width="30"} A system administrator or AEP product administrator can perform the following steps. 

1. Select **[!UICONTROL Roles]** in the left navigation and select **[!UICONTROL Create role]**.

1. In the _[!UICONTROL Create new role]_ dialog, enter a name for the role, such as _B2B Marketers_, and a description (optional).

1. Click **[!UICONTROL Confirm]**.

1. Select your sandboxes.

   ![Experience Platform - add sandboxes for the new role](./assets/aep-permissions-role-sandboxes.png){width="700" zoomable="yes"}

1. Add the profile permissions:

   * In the _[!UICONTROL Resources]_ list on the left, locate the **[!UICONTROL Profile Management]** item and click the _Add_ (**+**) icon to add the attribute.

   * For the attribute, add the following permissions:
      * [!UICONTROL View segments]
      * [!UICONTROL Manage segments]
      * [!UICONTROL View profiles]
      * [!UICONTROL Manage profiles]
      * [!UICONTROL View B2B profile]
      * [!UICONTROL Manage B2B profile]

   ![Experience Platform - add profiles for the new role](./assets/aep-permissions-role-profiles.png){width="700" zoomable="yes"}

1. Add B2B product permissions:

   Refer to the list of [B2B product permissions](#b2b-product-permissions) to determine which product capabilities that you want for the role.

   In the _[!UICONTROL Resources]_ list on the left, locate the **[!UICONTROL B2B]** items and click the _Add_ (**+**) icon to add each attribute that you want to enable for the role.

   You can enter _B2B_ in the search tool to filter the list for the B2B product permissions.

1. Click **[!UICONTROL Save]** at the top right.

1. Go to the role details and select the **[!UICONTROL User groups]** tab.

1. Click **[!UICONTROL Add Groups]**.

   ![Experience Platform - add profiles for the new role](./assets/aep-permissions-role-add-groups.png){width="700" zoomable="yes"}

1. Select the checkbox next to the user group that you created previously in the Admin Console.

1. Click **[!UICONTROL Save]**.
-->