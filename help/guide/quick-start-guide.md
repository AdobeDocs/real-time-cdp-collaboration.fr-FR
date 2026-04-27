---
title: Guide de démarrage rapide et de configuration de Real-Time CDP Collaboration
description: Découvrez comment paramétrer Real-Time CDP Collaboration, configurer des rôles et des comptes, des audiences sources, activer des données et communiquer avec des partenaires en toute sécurité.
audience: admin, publisher, advertiser
badgelimitedavailability: label="Disponibilité limitée" type="Informative" url="https://helpx.adobe.com/fr/legal/product-descriptions/real-time-customer-data-platform-collaboration.html newtab=true"
exl-id: 68e5095e-ece5-4f64-9056-10f3b216cf0c
TQID: https://experienceleague.adobe.com/rhIArZZm0Thkj3E-qiHtVHO6qxpr1vd-Qs4hWt4tf1U
product_v2:
  - id: fdddec33-c9cb-4459-b8b6-2664395a6f10
feature_v2:
  - id: ba929a52-9339-4154-9487-317dc875a3c7
topic_v2:
  - id: a004cc84-67b9-4a33-a3a7-8ec7273ef4dc
  - id: aa2f3246-cb95-4b30-8899-fdf7d73550cc
  - id: c2be0313-b3ae-45e0-b454-d20bf54b23f2
  - id: c7d04a2c-412a-4c9d-9d7a-4456eaa5adeb
  - id: e1e0219c-f879-479f-8427-888ed2a6e9c2
  - id: f4e6943a-c91a-4134-a2c7-f4f20cfff2f0
source-git-commit: 3ce7e66b31332836fd6cc6137c94622436505cc9
workflow-type: tm+mt
source-wordcount: 1417
ht-degree: 2%

---

# Guide de démarrage rapide de Real-Time CDP Collaboration

{{limited-availability-release-note}}

Commencez avec Real-Time CDP Collaboration en configurant votre organisation, en approvisionnant les audiences et en activant l’activation et la mesure axées sur la confidentialité.

## Conditions préalables

Avant de commencer, vérifiez que vous disposez des éléments suivants :

- Une licence Real-Time CDP Collaboration active.
- [Accès de l’administrateur système ou produit à Adobe Experience Platform](./permissions/overview.md).
- [Accès configuré pour les utilisateurs finaux](./permissions/manage-user-access.md).
- [Rôles créés pour votre organisation et affectés aux utilisateurs](./permissions/manage-roles.md).
- Accès aux ressources de marque, telles que le nom, le logo et la bannière de votre organisation.
- Une stratégie de clé de correspondance [&#x200B; définie](./setup/onboard-account.md#set-up-match-keys)
- (Facultatif) Accès à une source cloud prise en charge (Amazon S3, Google Cloud Storage ou Snowflake) si vous n’utilisez pas Experience Platform pour la gestion de l’audience.

## Étape 1 : terminer la configuration basée sur les rôles {#complete-role-based-setup}

Les rôles d’accès de votre organisation déterminent ce que les utilisateurs peuvent voir et faire dans Collaboration. Avant de poursuivre, assurez-vous que les autorisations basées sur les rôles sont correctement configurées pour garantir un accès et une visibilité appropriés dans la plateforme.

**Ressources:**

- [Documentation d’accès utilisateur](./permissions/manage-user-access.md)
- [Documentation sur la configuration des rôles](./permissions/manage-roles.md)


Regardez cette vidéo pour savoir comment attribuer des accès et des autorisations de produit pour Collaboration à l’aide d’Admin Console et d’Experience Platform.

>[!VIDEO](https://video.tv.adobe.com/v/3452232/?captions=fre_fr&learn=on&enablevpops)

## Étape 2 : configurer votre compte Collaboration {#set-up-your-account}

Avant de pouvoir approvisionner des audiences, vous devez configurer votre compte dans Collaboration. Cela régit votre apparence et ce à quoi vous avez accès dans l’interface.

Si vous ne disposez pas de l’accès nécessaire, reportez-vous à l’étape 1 ou contactez l’administrateur de votre organisation pour obtenir de l’aide sur la réalisation de cette configuration.

Définissez le rôle de votre compte dans Collaboration, fournissez des ressources de marque et configurez des clés de correspondance pour aligner les audiences sur les connexions.

>[!NOTE]
>
>Vous pouvez créer un ou plusieurs comptes (tels qu’un annonceur et un éditeur) lors de la configuration. Certains champs, tels que les ressources de marque et l’e-mail du contact, peuvent être mis à jour ultérieurement dans l’espace de travail **[!UICONTROL Paramètres]**.

- **Attribuer un rôle** - Détermine si votre compte est un annonceur ou un éditeur. Votre rôle définit les fonctionnalités dont vous disposez dans Collaboration. Pour en savoir plus sur l’impact des rôles sur le workflow de collaboration, consultez le guide [rôles](./overview/roles.md).
- **Valorisation de marque des ressources** - Ajoutez les éléments suivants à votre compte :
   - Nom du compte (100 caractères max.)
   - Description (1 000 caractères max.)
   - Logo (SVG &lt;20KB, idéalement carré)

>[!NOTE]
>
>Si vous créez un compte d’éditeur et souhaitez être visible publiquement dans le catalogue des connexions de Collaboration, contactez votre représentant de compte Adobe. Les comptes d’éditeur nécessitent une bannière de marque personnalisée (JPG 2 688 x 1 536). Ce fichier peut être partagé directement avec votre représentant.

- **E-mail de contact** - Fournissez un e-mail professionnel que les collaborateurs peuvent utiliser une fois la connexion établie.
- **Configurer les clés de correspondance** - Sélectionnez les identifiants utilisés pour la correspondance d’audience.

Pour en savoir plus sur la configuration initiale du compte, notamment sur la définition des rôles, le chargement de ressources de marque et la configuration des clés de correspondance, consultez le guide [configuration initiale du compte](./setup/onboard-account.md#initial-account-setup){target="_blank"}.

Regardez cette vidéo pour une présentation détaillée de la configuration d’un annonceur, y compris la création de compte, l’image de marque et la configuration de la clé de correspondance.

>[!VIDEO](https://video.tv.adobe.com/v/3452264/?learn=on&enablevpops)

## Étape 3 : Audiences Source (à partir d’Experience Platform ou d’une source cloud) {#source-audiences}

Une fois votre compte créé et vos clés de branding et de correspondance configurées, vous êtes prêt à commencer à approvisionner les audiences. Choisissez l’une des méthodes de sourcing suivantes en fonction de votre magasin de données et des besoins de votre entreprise.

### Option A : Source à partir d’Experience Platform

[Utilisez Collaboration pour lier un sandbox contenant des audiences](./setup/onboard-audiences.md). Utilisez cette méthode en libre-service pour référencer des segments d’audience existants à partir de votre instance Experience Platform.

#### Configuration des audiences

Configurez la manière dont les audiences sont préparées, appariées et gouvernées pour une utilisation dans les connexions.

- **Sélectionner des audiences** *(Experience Platform uniquement)* - Choisissez des segments d’audience avec des identifiants pris en charge.
- **Mapper les clés de correspondance** - Alignez les champs d’audience avec les clés de correspondance configurées.
- **Appliquer des transformations** - Hachage de valeurs en texte brut (par exemple, e-mail) si nécessaire.
- **Schedule refreshes** – Define update frequency (for example, daily).
- **Configure consent settings** – Determine which profiles are eligible to be included in connections by selecting a consent mode: opt-in, opt-out, or none.

>[!NOTE]
>
>You can add or remove audiences and update the refresh schedule directly in Collaboration. To change other settings, such as match keys or consent mode, you must delete and recreate the data connection.

>[!IMPORTANT]
>
>**Maximum number of audiences per collaborator role:**
>
>- **Advertisers** can source up to 25 audiences.
>- **Publishers** can source up to 250 audiences (each with a minimum of 1,000 IDs).

>[!IMPORTANT]
>
>**Match key requirements:**
>
>All match keys must be **trimmed**, **lowercased**
>Les clés de correspondance hachées doivent être **SHA256-hachées**.\
>Si vous fournissez des valeurs hachées qui utilisent des caractères majuscules, Collaboration les convertit automatiquement en minuscules.\
>If your source contains **plaintext identifiers**, use the **[!UICONTROL Apply transformation]** option to apply hashing. Cette option est disponible uniquement lors de l’approvisionnement d’audiences à partir d’Experience Platform et n’est pas prise en charge pour les sources cloud.
>
>For more information, see the [map fields](./setup/onboard-audiences.md#map-fields) section of the source and manage audiences guide.

To see a full walkthrough of how to source audiences using Collaboration, watch the video below.

>[!VIDEO](https://video.tv.adobe.com/v/3452217/?learn=on&enablevpops)

Alternatively, see the document on [sourcing audiences in Collaboration](./setup/onboard-audiences.md#source-and-manage-audiences).

### Option B: Source from Snowflake, Amazon S3, or Google Cloud Storage

To configure a cloud source, such as [!DNL Snowflake], [!DNL Amazon S3], or [!DNL Google Cloud Storage], prepare your audience data using the [Audience Specification PDF](../assets/quick-start/RTCDP_Collaboration_Audience_Sourcing_Spec_v1.2.pdf)

You can configure [!DNL Amazon S3], [!DNL Google Cloud Storage], or [!DNL Snowflake] as self-service data sources. For setup instructions, see the [Amazon S3 sourcing guide](./setup/configure-aws-s3-audience-sourcing.md), the [GCS sourcing guide](./setup/configure-gcs-audience-sourcing.md), or the [Snowflake sourcing guide](./setup/configure-snowflake-audience-sourcing.md).

For other cloud service providers, contact your Adobe account representative to finalize the setup.

>[!IMPORTANT]
>
>Cloud-based audience files must follow the required schema outlined in the Audience Specification PDF. Files must include hashed identifiers (lowercased SHA256), required metadata fields such as `segment_name` and `activation_id`, and use supported formats such as CSV or Parquet. Adobe does not normalize data before activation. TTL is enforced based on the audience&#39;s lifespan.
>
>All audiences in the uploaded file are fully sourced at this stage. The [audience visibility setting](/help/guide/setup/onboard-audiences.md#metadata-visibility) determines whether your collaborators can view your audience and is managed through the Collaboration UI.

## Step 4: Activate audiences (to Experience Platform or a cloud destination) {#activate-audiences}

Next, activate audiences to either your Experience Platform instance or a cloud destination.

### Option A: Activate to Experience Platform

Complete the following steps outlined in the [configure Adobe Experience Platform as a destination](/help/guide/destinations/experience-platform.md) guide.

- **Create a destination** – Use the UI to set up an Experience Platform destination (sandbox-level).
- **Map match keys** – Select the identifier (e.g., `hashedEmail`).
- **Define TTL** – Set expiration (1–30 days).
- **Verify in Audience Portal** – Once a collaborator sends you an audience, verify that it appears in the Audience Portal under the origin &quot;[!UICONTROL Real-Time CDP Collaboration].&quot;

### Option B: Activate to cloud

To configure a cloud destination (for example, [!DNL AWS S3] or [!DNL Snowflake]), contact your Adobe account representative to initiate the setup process. Depending on the cloud destination, you will need to provide cloud destination details such as file path, credentials, account locators etc. Once required information is provided, Adobe will configure the cloud destination setup.

Audience data sent to a cloud destination follows a predefined schema. For a detailed description of the required fields and format, download the [Collaboration Audience Activation Guide](../assets/quick-start/RTCDP_Collaboration_Audience_Activation_Spec_v1.0.pdf).

## Step 5: Set up measurement (optional) {#set-up-measurement}

>[!IMPORTANT]
>
>The **[!UICONTROL Measure]** workspace is only available if the **[!UICONTROL Measurement]** use case was enabled [during the connection process](./connect/establishing-connections.md#connection-settings). Pour plus d’informations sur les cas d’utilisation, consultez le guide [gestion des projets](./collaborate/manage-projects.md#project-use-cases).

Collaboration offers a variety of reports to analyze campaign reach, frequency, and effectiveness. While the **[!UICONTROL Measure]** workspace is available in the UI, full reporting functionality may require backend enablement.

To learn how to view and interpret measurement reports, see the [Measurement guide](./collaborate/measure.md). It covers attribution, campaign summary metrics, and dashboards such as reach curves and frequency distribution.

<!-- 
Commenting out the below information as this workflow is not yet in Beta but will be imminently. A guided measurement configuration workflow will be available in a future release."

### Configure measurement workflow

Collaboration supports two measurement workflows:

- **Attribution using Adobe Experience Platform datasets**
- **Campaign summary using only partner-provided data**

Choose the appropriate workflow below based on your campaign measurement goals.

#### Option A: Attribution using Experience Platform datasets

Use this workflow to measure conversion activity using datasets stored in Experience Platform.

1. **Create a measurement data connection**
   - Select the dataset that contains your conversion events.
   - Map identity fields from your dataset to the match keys used in Collaboration.
   - Manage consent and governance settings.
   - Define one or more conversion events to measure.
   - Review and confirm your setup.

2. **Run a measurement report**
   - Go to the **[!UICONTROL Measure]** workspace within the associated project.
   - Input the report name, date range, and report run date.
   - Select **[!UICONTROL Attribution]** as the report type.
   - Select the defined conversion event(s).
   - Submit the report. It will run on the specified date and populate within 24 hours.

#### Option B: Campaign summary using partner-provided data

Use this workflow to generate campaign summary insights based on advertiser-supplied identifiers (for example, campaign ID).

1. **Set up the connection**
   - In the connection settings, ensure **[!UICONTROL Measurement]** is selected as a use case.
   - Create a project under the connection with **[!UICONTROL Measurement]** as an activity.

2. **Provide campaign context**
   - Input required campaign identifiers (for example, **Campaign ID**) for the partner to reference.
   - Align with your partner on campaign scope and reporting timeline.

3. **Run a measurement report**
   - Navigate to the **[!UICONTROL Measure]** workspace within the project.
   - Input the report name, date range, and report run date.
   - Select **[!UICONTROL Campaign summary]** as the report type.
   - Submit the report. It will run on the selected date and populate within 24 hours. 
-->

## Step 6: Connect with collaborators {#connect-with-collaborators}

With setup complete, your organization is now ready to connect with collaborators by sending or accepting invitations and submitting project settings for approval. This connection process involves sending or receiving invitations, reviewing and submitting connection settings (such as use cases and credit consumption), and confirming the connection.

En tant qu’annonceur, utilisez l’espace de travail **[!UICONTROL Connect]** dans le menu de navigation de gauche pour parcourir les éditeurs disponibles. Les collaborateurs peuvent également communiquer directement entre eux par le biais d’[invitations à des connexions privées](./connect/establishing-connections.md#private-connection-invite){target="_blank"}.

>[!NOTE]
>
>Actuellement, seuls les annonceurs peuvent parcourir les éditeurs. Les éditeurs ne peuvent pas parcourir ni établir de connexions avec les annonceurs.

Pour une présentation de ce flux, consultez le [guide d’établissement de connexions](./connect/establishing-connections.md){target="_blank"}. Pour une présentation visuelle du processus de connexion, y compris la navigation des collaborateurs et la gestion des paramètres de connexion, regardez la vidéo [configuration du compte d’annonceur](https://experienceleague.adobe.com/fr/docs/platform-learn/tutorials/collaboration/connect-with-publishers){target="_blank"}.

## Étapes suivantes

Vous avez maintenant terminé la configuration initiale et configuré votre organisation pour une collaboration sécurisée. Explorez ensuite les ressources suivantes pour mieux comprendre l’activation, la mesure et la gouvernance des données :

- [Documentation sur le workflow d’activation de l’audience](./collaborate/activate.md)
- [Cas d’utilisation de Measurement](./collaborate/measure.md)
- [Bonnes pratiques de gouvernance de Collaboration](./setup/onboard-audiences.md#governance-policy-and-enforcement-actions)
