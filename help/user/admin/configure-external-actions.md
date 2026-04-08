---
title: Konfiguration för externa åtgärder
description: Se hur utvecklare, administratörer och marknadsförare samarbetar för att implementera, konfigurera och använda externa åtgärder som kopplar Journey Optimizer B2B edition till externa tjänster på kontoresor.
feature: Setup, Integrations
role: Admin, Developer
source-git-commit: 6d3967babc1bc868fde0c76ac9068e63156070cd
workflow-type: tm+mt
source-wordcount: '857'
ht-degree: 2%

---

# Konfiguration för externa åtgärder

Externa åtgärder gör det möjligt för kontoresor i Journey Optimizer B2B edition att ansluta till externa system direkt från arbetsytan. När en kontopublik når en extern åtgärdsnod gör systemet ett asynkront utgående anrop till en konfigurerad extern tjänst, skickar målgruppsattributdata för konton, personer eller både och. Den externa tjänsten bearbetar data och svarar med ett återanrop och returnerar målgruppsdata och metadata som kan användas som vägledning vid körning av resan.

Den här funktionen har stöd för två typer av kundnoder:

* **Extern åtgärd** - Anropar en extern tjänst och fortsätter längs en enda utgående sökväg. Idealiskt för _eld-och-glöm_-integreringar, som att uppdatera en CRM-post eller utlösa ett meddelande längre fram i kedjan.
* **Externa delade sökvägar** - Anropar en extern tjänst och utvärderar svaret för att dirigera konton längs en av flera definierade sökvägar.

>[!NOTE]
>
>Externa åtgärdstjänster stöds endast för kontoresor. De här nodtyperna är inte tillgängliga för personresor.

## Implementeringsöversikt

Konfigurering av externa åtgärder kräver samordning mellan tre roller i följd:

| | Roll | Uppgift |
| ---- | ---- | ---- |
| 1 | Utvecklare | [Implementera och publicera den externa tjänsten](#implement-service) |
| 2 | Administratör | [Konfigurera åtgärden i Journey Optimizer B2B edition](#configure-action) |
| 3 | Marknadsförare | [Lägg till en extern nod till en kontoresa](#add-journey-node) |

## Implementera den externa tjänsten {#implement-service}

Utvecklaren måste skapa och publicera en offentlig webbtjänst som är kompatibel med [Adobe Journey Optimizer B2B edition External Actions Service Provider Interface](https://developer.adobe.com/journey-optimizer-b2b-apis/).

>[!NOTE]
>
>Callback-funktionen kräver en innehavartoken. Hämta detta genom att konfigurera [OAuth Server-till-Server-autentiseringsuppgifter i Adobe Developer Console](https://developer.adobe.com/developer-console/docs/guides/authentication/ServerToServerAuthentication/implementation) för din IMS-organisation.

När tjänsten är aktiv anger du URL:en till OpenAPI-specifikationen och autentiseringsuppgifterna till produktadministratören som ansvarar för att konfigurera åtgärden.

## Konfigurera åtgärden {#configure-action}

En åtgärd måste konfigureras och aktiveras innan marknadsförarna kan använda den på en resa. Åtgärder skapas i läget _Utkast_ och dina ändringar sparas automatiskt. Det förblir som ett utkast tills du aktiverar det.

>[!PREREQUISITES]
>
>Hämta URL:en till OpenAPI-specifikationen och autentiseringsuppgifterna från utvecklaren innan du lägger till konfigurationen.
>
>Om du vill definiera och aktivera en extern åtgärd måste du ha _[!UICONTROL Manage B2B Admin Configurations]_[produktbehörighet](./user-management.md#b2b-product-permissions).

1. Gå till **[!UICONTROL Administration]** > **[!UICONTROL Configurations]**.

1. Klicka på **[!UICONTROL External Actions]** på panelen mellan.

   ![Gå till konfigurationsutrymmet för externa åtgärder](./assets/configuration-external-actions-list.png){width="800" zoomable="yes"}

1. Klicka på **[!UICONTROL Create action]** överst till höger.

1. Ange URL:en till OpenAPI-specifikationen för den externa tjänsten och klicka på **[!UICONTROL Create]**.

   ![Ange tjänst-URL](./assets/configuration-external-actions-create-url.png){width="500"}

   >[!NOTE]
   >
   >Din externa tjänst måste vara tillgänglig och åtkomlig för att det här steget ska lyckas.

1. Granska **[!UICONTROL Service details]** när URL:en har lösts.

   Tjänstinformationen läses direkt från OpenAPI-specifikationen när åtgärden skapas. Du kan inte ändra dessa egenskaper i konfigurationen efter att du har skapat den.

   | Egenskap | Beskrivning | OpenAPI-specifikationsegenskap |
   | -------- | ----------- | --------------------- |
   | [!UICONTROL Name] | Åtgärdens namn | `info.title` |
   | [!UICONTROL Description] | Beskrivning av åtgärden | `info.description` |
   | [!UICONTROL URL] | URL till OpenAPI-specifikationen som definierar den externa tjänsten | `servers.url` |

1. Ange autentiseringsuppgifterna **[!UICONTROL Authentication]** för den externa tjänsten (`components.securitySchemes`).

   >[!NOTE]
   >
   >Vilka inloggningsfält som visas beror på vilken autentiseringsmekanism som har definierats i den externa tjänsten. De typer som stöds är API Key, OAuth2 och HTTP Basic Authentication.

   ![Lägg till autentiseringsuppgifter](./assets/configuration-external-actions-auth-credentials.png){width="600" zoomable="yes"}

   Du kan ändra autentiseringsuppgifterna efter behov när den konfigurerade åtgärden har statusen _Utkast_ eller _Aktiv_.

1. Klicka på **[!UICONTROL Next]**.

1. Ange egenskaperna **[!UICONTROL Configurations]** för att definiera hur åtgärden ska utbyta data med den externa tjänsten.

   >[!NOTE]
   >
   >Egenskaper som har markerats som _Statisk_ kan inte uppdateras vid konfigurationstiden och baseras på tjänstdefinitionen.

   * **[!UICONTROL Action type]** (_Statisk_) - Den typ av resenod som stöds:

      * [!UICONTROL External action] (`enableSplitPath` = false)
      * [!UICONTROL External action split path] (`enableSplitPath` = true)

     Du kan inte ändra åtgärdstypen efter att du har skapat åtgärdskonfigurationen.

   * **[!UICONTROL Accessors]** (_Statisk_) - (Endast delad sökväg för extern åtgärd) Variablerna som returneras av den externa tjänsten som ska vara tillgängliga som sökvägsvillkor i en extern delad sökvägsnod. (`invocationPayloadDef.accessorsMetadata`)

   * **[!UICONTROL Journey context]** (_Statisk_) - Omfånget för målgruppsdata som skickats i begäran (`supportedEntityType`):

      * [!UICONTROL Account] - Skickar endast konton

      * [!UICONTROL People] - Skickar endast personer

      * [!UICONTROL People in Account] - Skickar konton och kontorelaterade personer

   * **[!UICONTROL Outgoing Fields]** - Mappa varje fält i tabellen till ett [XDM-fält](../admin/xdm-field-management.md). Dessa fält skickas i begärandetexten till den externa tjänsten. Tjänstedefinitionsegenskaper: `invocationPayloadDef.accountFields`, `invocationPayloadDef.fields`.

   ![Mappa utgående fält för extern åtgärd](./assets/configuration-external-actions-fields.png){width="600" zoomable="yes"}

   * **[!UICONTROL Incoming Fields]** - Mappa varje fält i tabellen till ett [uppdateringsbart XDM-fält](../admin/xdm-field-management.md#updatable-fields). Dessa fält fylls i från det externa tjänstsvaret. Tjänstedefinitionsegenskaper: `callbackPayloadDef.accountFields`, `callbackPayloadDef.fields`. Uppdateringsbart efter att det har skapats.

   * **[!UICONTROL Header parameters]** - Ange ett värde för varje rad som ska skickas som en HTTP-rubrik i begäran. Tjänstedefinitionsegenskap: `invocationPayloadDef.headers`.

   * **[!UICONTROL Timeout]** - Ange hur många minuter det ska ta att vänta på att den externa tjänsten ska anropa återanropet innan begäran anses vara misslyckad. Tjänstedefinitionsegenskap: `timeout`.

   * **[!UICONTROL Global attributes]** - Ange ett värde för varje rad som ska inkluderas som ett statiskt fält i begärandetexten. Tjänstedefinitionsegenskap: `invocationPayloadDef.globalAttributes`.

   ![Externa åtgärdshuvudesparametrar, timeout och globala attribut](./assets/configuration-external-actions-header-timeout-global.png){width="600" zoomable="yes"}

1. Klicka på _Bakåtpilen_ för att gå tillbaka till listan och behålla åtgärden i läget _Utkast_.

   Du kan också klicka på **[!UICONTROL Activate]** om du vill ändra åtgärdskonfigurationen till läget _Aktiv_. Den konfigurerade externa åtgärden måste vara aktiv för att den ska kunna användas på kontoresor.

## Lägg till en extern nod till en resa {#add-journey-node}

När en åtgärd har aktiverats kan marknadsförarna lägga till en _[!UICONTROL External action]_- eller_[!UICONTROL External split path]_-nod till en kontoresa. Mer information om hur du lägger till och använder de här noderna i kontoresans arbetsyta finns i [Externa noder](../journeys/external-nodes.md).
