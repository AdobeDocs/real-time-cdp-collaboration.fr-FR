---
title: Guide de démarrage rapide de Real-Time CDP Collaboration
description: Découvrez comment intégrer votre organisation dans Real-Time CDP Collaboration, notamment la configuration des rôles et des organisations, l’approvisionnement des audiences, l’activation et la mesure. Ce guide aide les collaborateurs à configurer les paramètres de connexion pour commencer à utiliser leurs audiences de manière sécurisée et efficace.
audience: admin, publisher, advertiser
badgelimitedavailability: label="Disponibilité limitée" type="Informative" url="https://helpx.adobe.com/fr/legal/product-descriptions/real-time-customer-data-platform-collaboration.html newtab=true"
exl-id: 68e5095e-ece5-4f64-9056-10f3b216cf0c
source-git-commit: a7215d453021be578a32ce1af4d659845c3b8493
workflow-type: tm+mt
source-wordcount: '1408'
ht-degree: 0%

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
- Une [ stratégie de clé de correspondance définie ](./setup/onboard-account.md#set-up-match-keys) (actuellement, l’e-mail haché est la seule clé de correspondance prise en charge).
- (Facultatif) Accès à une source cloud prise en charge (Amazon S3 ou Snowflake) si vous n’utilisez pas Experience Platform pour la gestion de l’audience.

## Étape 1 : terminer la configuration basée sur les rôles {#complete-role-based-setup}

Les rôles d’accès de votre organisation déterminent ce que les utilisateurs peuvent voir et faire dans Collaboration. Avant de poursuivre, assurez-vous que les autorisations basées sur les rôles sont correctement configurées pour garantir un accès et une visibilité appropriés dans la plateforme.

**Ressources:**

- [Documentation d’accès utilisateur](./permissions/manage-user-access.md)
- [Documentation sur la configuration des rôles](./permissions/manage-roles.md)


Regardez cette vidéo pour savoir comment attribuer des accès et des autorisations de produit pour Collaboration à l’aide d’Admin Console et d’Experience Platform.

>[!VIDEO](https://video.tv.adobe.com/v/3452232/?learn=on&enablevpops&captions=fre_fr)

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
- **Configurer les clés de correspondance** - Sélectionnez les identifiants utilisés pour la correspondance d’audience (actuellement, l’e-mail haché est la seule clé de correspondance prise en charge).

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
- **Planification des actualisations** - Définissez la fréquence de mise à jour (par exemple, quotidienne).
- **Configurer les paramètres de consentement** - Déterminez les profils pouvant être inclus dans les connexions en sélectionnant un mode de consentement : opt-in, opt-out ou aucun.

>[!NOTE]
>
>Vous pouvez ajouter ou supprimer des audiences et mettre à jour le planning d’actualisation directement dans Collaboration. Pour modifier d’autres paramètres, tels que les clés de correspondance ou le mode de consentement, vous devez supprimer et recréer la connexion aux données.

>[!IMPORTANT]
>
>**Nombre maximal d’audiences par rôle de collaborateur :**
>
>- **Annonceurs** peut sélectionner jusqu’à 25 audiences.
>- **Les éditeurs** peuvent approvisionner jusqu’à 250 audiences (chacune avec un minimum de 5 000 identifiants).

>[!IMPORTANT]
>
>**Respectez les principales exigences :**
>
>Toutes les clés de correspondance doivent être **tronquées**, **en minuscules** et **SHA256-hachées**.\
>Si vous fournissez des valeurs hachées qui utilisent des caractères majuscules, Collaboration les convertit automatiquement en minuscules.\
>Si votre source contient des **identifiants en texte brut**, utilisez l’option **[!UICONTROL Appliquer la transformation]** pour appliquer le hachage. Cette option est disponible uniquement lors de l’approvisionnement d’audiences à partir d’Experience Platform et n’est pas prise en charge pour les sources cloud.
>
>Pour plus d’informations, consultez la section [mapper des champs](./setup/onboard-audiences.md#map-fields) du guide de source et de gestion des audiences.

Pour découvrir une présentation complète de la source des audiences à l’aide de Collaboration, regardez la vidéo ci-dessous.

>[!VIDEO](https://video.tv.adobe.com/v/3452217/?learn=on&enablevpops)

Vous pouvez également consulter le document sur le [sourcing d’audiences dans Collaboration](./setup/onboard-audiences.md#source-and-manage-audiences).

### Option B : Source de Snowflake ou Amazon S3

Pour configurer une source cloud (par exemple, [!DNL AWS S3] ou [!DNL Snowflake]), préparez les données de votre audience à l’aide de la [PDF de spécification d’audience](../assets/quick-start/RTCDP_Collaboration_Audience_Onboarding_Spec_v1.0.pdf) suivante. Une fois l’opération terminée ou si vous avez des questions, contactez votre représentant de compte Adobe pour finaliser la configuration. Cette méthode n’est pas en libre-service et nécessite l’assistance d’Adobe.

>[!IMPORTANT]
>
>Les fichiers d’audience basés sur le cloud doivent suivre le schéma requis décrit dans le PDF de spécification d’audience. Les fichiers doivent inclure des identifiants hachés (SHA256 en minuscules), les champs de métadonnées requis tels que `segment_name` et `activation_id`, et utiliser des formats pris en charge tels que CSV ou Parquet. Adobe ne normalise pas les données avant l’activation. La durée de vie est appliquée en fonction de la durée de vie de l’audience.
>
>Toutes les audiences du fichier chargé sont entièrement sourcées à ce stade. Le [ paramètre de visibilité de l’audience ](/help/guide/setup/onboard-audiences.md#metadata-visibility) détermine si vos collaborateurs peuvent afficher votre audience. Il est géré via l’interface utilisateur de Collaboration.

## Étape 4 : activer les audiences (vers Experience Platform ou une destination cloud) {#activate-audiences}

Ensuite, activez les audiences vers votre instance Experience Platform ou une destination cloud.

### Option A : activer dans Experience Platform

Suivez les étapes décrites dans le guide [configurer Adobe Experience Platform en tant que destination](/help/guide/destinations/experience-platform.md).

- **Créer une destination** - Utilisez l’interface utilisateur pour configurer une destination Experience Platform (au niveau du sandbox).
- **Mapper les clés de correspondance** - Sélectionnez l’identifiant (par exemple, `hashedEmail`).
- **Définir une durée de vie** - Définir l’expiration (1-30 jours).
- **Vérification dans Audience Portal** - Une fois qu’un collaborateur vous envoie une audience, vérifiez qu’elle apparaît dans Audience Portal sous l’origine « [!UICONTROL Real-Time CDP Collaboration]. »

### Option B : Activer vers le cloud

Pour configurer une destination cloud (par exemple, [!DNL AWS S3] ou [!DNL Snowflake]), contactez votre représentant de compte Adobe pour lancer le processus de configuration. Selon la destination cloud, vous devrez fournir des détails de destination cloud tels que le chemin d’accès au fichier, les informations d’identification, les localisateurs de compte, etc. Une fois les informations requises fournies, Adobe configure la configuration de destination dans le cloud.

Les données d’audience envoyées à une destination cloud suivent un schéma prédéfini. Pour une description détaillée des champs et du format requis, téléchargez le [Guide Collaboration Audience Activation](../assets/quick-start/RTCDP_Collaboration_Audience_Activation_Spec_v1.0.pdf).

## Étape 5 : configurer la mesure (facultatif) {#set-up-measurement}

>[!AVAILABILITY]
>
>Cette fonctionnalité est en version **bêta** et disponible exclusivement pour les clients et clientes du programme à disponibilité limitée. Contactez votre représentant Adobe pour demander l’accès.

>[!IMPORTANT]
>
>L’espace de travail **[!UICONTROL Mesure]** n’est disponible que si le cas d’utilisation **[!UICONTROL Mesure]** a été activé [pendant le processus de connexion](./connect/establishing-connections.md#connection-settings). Pour plus d’informations sur les cas d’utilisation, consultez le guide [gestion des projets](./collaborate/manage-projects.md#project-use-cases).

Collaboration propose divers rapports pour analyser la portée, la fréquence et l’efficacité des campagnes. Bien que l’espace de travail **[!UICONTROL Mesure]** soit disponible dans l’interface utilisateur, une fonctionnalité de création de rapports complète peut nécessiter l’activation du serveur principal.

Pour savoir comment afficher et interpréter les rapports de mesure, consultez le [Guide des mesures](./collaborate/measure.md). Elle couvre l’attribution, les mesures de résumé de la campagne et les tableaux de bord tels que les courbes de portée et la distribution fréquentielle.

<!-- Commenting out the below information as this workflow is not yet in Beta but will be imminently. A guided measurement configuration workflow will be available in a future release."
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
   - Submit the report. It will run on the selected date and populate within 24 hours. -->

## Étape 6 : Se connecter avec les collaborateurs {#connect-with-collaborators}

Une fois la configuration terminée, votre organisation est prête à se connecter à ses collaborateurs en envoyant ou en acceptant des invitations et en envoyant les paramètres du projet pour approbation. Ce processus de connexion implique l’envoi ou la réception d’invitations, la révision et l’envoi des paramètres de connexion (tels que les cas d’utilisation et la consommation de crédit), ainsi que la confirmation de la connexion.

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
