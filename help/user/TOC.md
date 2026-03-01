---
user-guide-title: Journey Optimizer B2B edition Documentation
user-guide-description: Läs om Adobe Journey Optimizer B2B edition och hur du kan använda det för att skapa konto och köpa gruppresor med hjälp av inbyggd generativ AI och branschledande automatisering.
source-git-commit: 696d3a57a1c086a25670ffb41cd095d4da011615
workflow-type: tm+mt
source-wordcount: '405'
ht-degree: 2%

---


# Användarhandbok för Journey Optimizer B2B edition {#user}

+ [Adobe Journey Optimizer B2B edition Documentation](guide-overview.md)
+ [Versionsinformation](./release-notes/release-notes.md)
+ Kom igång {#get-started}
   + [Journey Optimizer B2B edition - översikt](about-journey-optimizer-b2b-edition.md)
   + [Inloggning och hemsida](home-page.md)
   + [Vägledning om introduktion](./start/get-started.md)
   + [Spårnings- och e-postprotokoll](./start/email-protocols.md)
+ AI-assistenten {#ai-assistant}
   + [Ökning](./ai-assistant/ai-assistant-overview.md)
   + [Aktivera åtkomst till AI Assistant](./ai-assistant/enable-ai-assistant-access.md)
   + [Frågevägledning](./ai-assistant/question-guidance.md)
   + [Använd AI-assistenten](./ai-assistant/use-ai-assistant.md)
   + Agenter {#ai-agents}
      + [Audience Agent](./agents/audience-agent-b2b.md)
      + [Journey Build Agent B2B](./agents/journey-agent.md)
      + [Försäljningskvalificerare](./agents/sales-qualifier.md)
+ Resehantering {#journeys}
   + [Konto- och personresor](./journeys/journeys-overview.md)
   + [Skapa och publicera en resa](./journeys/create-publish-journey.md)
   + [Reseåterinträde](./journeys/journey-re-entry.md)
   + [Resensnoder](./journeys/journey-nodes.md)
   + Resensnoder {#journey-nodes}
      + [Målgrupp](./journeys/account-audience-nodes.md)
      + [Målgrupp (Beta)](./journeys/person-audience-nodes.md)
      + [Agera](./journeys/action-nodes.md)
      + [Lyssna efter en händelse](./journeys/listen-for-event-nodes.md)
      + [Dela och sammanfoga banor](./journeys/split-merge-paths-nodes.md)
      + [Vänta](./journeys/wait-nodes.md)
   + [Resedetaljer](./journeys/journey-details.md)
+ Reseinnehåll {#journey-content}
   + [SMS-kanal](./content/sms-authoring.md)
   + E-postkanal {#email-channel}
      + [Lägg till ett e-postmeddelande](./content/add-email.md)
      + [Framtagning av e-post](./content/email-authoring.md)
      + [AI-assistenten för att skapa e-post](./content/ai-assistant-emails.md)
      + [GenStudio arbetsflöden](./content/genstudio-email-workflow.md)
      + [Mörkt läge för e-postdesign](./content/email-dark-mode.md)
      + [Styrda mallar](./content/email-authoring-governance.md)
      + [E-postmeddelande om försäljning](./content/sales-alert-email.md)
      + [Deduplicering av e-post](./content/email-deduplication.md)
   + Webbkanal (Beta) {#web-channel}
      + [Ökning](./content/web-experiences.md)
      + [Design av webbupplevelser](./content/web-experience-design.md)
      + [Single-page applications](./content/web-single-page-applications.md)
   + [Anpassade personaliseringstoken](./content/personalization-my-tokens.md)
+ Målgrupper {#audiences}
   + [Experience Platform målgrupper](./audiences/account-audience-overview.md)
   + [Målgrupper externt](./audiences/target-external-audience.md)
   + [LinkedIn Account - matchade målgrupper](./data/linkedin-account-matched-audiences.md)
+ Konton {#accounts}
   + Köpgrupper {#buying-groups}
      + [Ökning](./buying-groups/buying-groups-overview.md)
      + [Lösningsintressen](./buying-groups/solution-interests.md)
      + [Rollmallar](./buying-groups/buying-groups-role-templates.md)
      + [Standardroller och anpassade roller](./buying-groups/default-custom-roles.md)
      + [Rollinsikter](./buying-groups/buying-group-role-insights.md)
      + Köpa grupppoäng {#scoring}
         + [Engagemangsmoment](./buying-groups/engagement-scores.md)
         + [Slutförandepoäng](./buying-groups/completeness-scores.md)
      + [Köpgruppsfaser](./buying-groups/buying-group-stages.md)
      + [Skapa inköpsgrupper](./buying-groups/buying-groups-create.md)
      + [Exportera konton](./audiences/account-list-export.md)
      + [Köpa gruppfilter i Marketo Engage](./buying-groups/marketo-engage-smart-list-buying-group-filters.md)
      + [Insikter i CRM](./buying-groups/incrm-insights.md)
   + Kontolistor {#account-lists}
      + [Ökning](./accounts/account-lists.md)
      + [Användning under resor och program](./accounts/account-lists-journeys.md)
   + Försäljningsupplevelse {#sales-experience}
      + [Kontoinformation](./accounts/account-details.md)
      + [Information om inköpsgrupp](./buying-groups/buying-group-details.md)
      + [Personinformation](./accounts/person-details.md)
      + [CRM-länkning](./accounts/crm-linking.md)
+ Innehållshantering {#content-management}
   + E-post {#emails}
      + [Arbeta med e-postinnehåll](./content/emails-list.md)
      + [Utforma tillgängligt innehåll](./content/email-accessible-content.md)
      + Förhandsgranska och validera {#preview}
         + [Simulera innehåll](./content/email-simulate-content.md)
         + [Testa e-poståtergivning](./content/email-test-rendering.md)
         + [Rapport om skräppost](./content/email-spam-report.md)
      + [E-postsamarbete](./content/email-collaboration-tools.md)
   + Resurser {#assets}
      + [Ökning](./content/assets-overview.md)
      + Interna tillgångar {#internal-dam}
         + [Arbeta med interna resurser](./content/internal-image-assets.md)
         + [Redigera bilder med Adobe Express](./content/image-edit-adobe-express.md)
      + [Experience Manager bildresurser](./content/aem-assets.md)
   + Mallar {#templates}
      + [Innehållsstyrning](./content/template-content-governance.md)
      + E-postmallar {#email-templates}
         + [Ökning](./content/email-templates.md)
         + [Framtagning av e-postmallar](./content/email-template-authoring.md)
         + [Konvertera bild till mall](./content/email-template-image-convert.md)
      + Landningssidmallar (Beta) {#landing-page-templates}
         + [Ökning](./content/landing-page-templates.md)
         + [Design av mall för landningssida](./content/landing-page-template-design.md)
   + Fragment {#visual-fragments}
      + [Ökning](./content/fragments.md)
      + [Skapa fragment](./content/fragment-authoring.md)
   + Forms (Beta) {#forms}
      + [Ökning](./content/forms.md)
      + [Formulärdesign](./content/form-design.md)
   + Landningssidor (Beta) {#landing-pages}
      + [Översikt](./content/landing-pages.md)
      + [Landningssiddesign](./content/landing-page-design.md)
   + Verktyg för innehållsdesign {#content-design}
      + [Strukturkomponenter](./content/structure-components.md)
      + [Innehållskomponenter](./content/content-components.md)
      + [Anpassad CSS](./content/design-custom-css.md)
   + Varumärken (Beta) {#brands}
      + [Ökning](./content/brands-overview.md)
      + [Hantera och skapa](./content/brands-manage-create.md)
      + [Märkesjustering](./content/brand-alignment.md)
   + [Varumärkesteman](./content/brand-themes.md)
   + [Villkorligt innehåll](./content/conditional-content.md)
   + Personalisering {#personalization}
      + [Ökning](./content/personalization.md)
      + [Personalization syntax](./content/personalization-syntax.md)
      + [Hjälpfunktionslista](./content/personalization-helper-functions.md)
+ Intelligenta instrumentpaneler {#dashboards}
   + [Instrumentpanel för insikter](./dashboards/intelligent-dashboard.md)
   + [Instrumentpanel för engagemang](./dashboards/engagement-dashboard.md)
   + [Kontrollpanel för webbengagemang](./dashboards/web-engagement-dashboard.md)
   + [Instrumentpanel för inköpsgrupper](./dashboards/buying-groups-dashboard.md)
   + [Kontrollpanel för kontoresor](./dashboards/journeys-dashboard.md)
+ Administration {#admin}
   + [Styrning](./admin/governance.md)
   + [Konfiguration av Marketo Actions](./admin/marketo-actions-connect.md)
   + [Personmappning](./admin/persona-mapping.md)
   + [Användarhantering](./admin/user-management.md)
   + XDM-fälthantering {#xdm-field-management}
      + [XDM-klasser](admin/xdm-field-management.md)
      + [Experience Events och fields](./admin/configure-aep-events.md)
      + [XDM-standardfält](./admin/field-mapping.md)
   + Kanaler {#channels}
      + [E-postkonfigurationer](./admin/configure-channels-emails.md)
      + [SMS-konfiguration](./admin/configure-channels-sms.md)
      + [Konfigurationer av webbkanaler (Beta)](./admin/configure-channels-web.md)
      + [Inställningar för landningssida (Beta)](./admin/landing-page-settings.md)
      + [Konfigurera datastreams för händelsesamling](./data/aep-event-collection.md)
   + Konfigurationer {#configurations}
      + [AEM Assets-databaser](./admin/configure-aem-repositories.md)
      + [Återgivningsdata](./admin/intent-data.md)
      + [Vägning av engagemangsmusik](./admin/engagement-score-weighting.md)
   + [Förenklad arkitekturkonfiguration](simplified-architecture.md)
