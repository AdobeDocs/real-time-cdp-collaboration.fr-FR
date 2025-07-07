---
title: Démarrage rapide de l’intégration à Real-Time CDP Collaboration
description: Découvrez comment intégrer votre organisation dans Real-Time CDP Collaboration, notamment la configuration des rôles et des organisations, l’approvisionnement des audiences, l’activation et la mesure. Ce guide aide les annonceurs et les éditeurs à configurer les paramètres de collaboration et à commencer à utiliser les audiences partagées de manière sécurisée et efficace.
audience: admin, publisher, advertiser
exl-id: 68e5095e-ece5-4f64-9056-10f3b216cf0c
source-git-commit: 5b17bcfbab02e8d24009a875ddea15cbd49c1506
workflow-type: tm+mt
source-wordcount: '1605'
ht-degree: 0%

---

# démarrage rapide de l’intégration à Real-Time CDP Collaboration

Commencez avec Real-Time CDP Collaboration en configurant votre organisation, en approvisionnant les audiences et en activant l’activation et la mesure axées sur la confidentialité.

## Conditions préalables

Avant de commencer, vérifiez que vous disposez des éléments suivants :

- Une licence Real-Time CDP Collaboration active.
- [Accès de l’administrateur système ou produit à Adobe Experience Platform](./permissions/overview.md#use-cases).
- [Accès configuré pour les utilisateurs finaux](./permissions/manage-user-access.md).
- [Rôles créés pour votre organisation et affectés aux utilisateurs](./permissions/manage-roles.md).
- Accès aux ressources de marque, telles que le nom, le logo et la bannière de votre organisation.
- Une [ stratégie de clé de correspondance définie ](./setup/onboard-organization.md#set-up-match-keys) (actuellement, l’e-mail haché est la seule clé de correspondance prise en charge).
- (Facultatif) Accès à une source cloud prise en charge (Amazon S3 ou Snowflake) si vous n’utilisez pas Experience Platform comme destination.

## Étape 1 : terminer la configuration basée sur les rôles {#complete-role-based-setup}

>[!NOTE]
>
>Cette étape s’applique à la fois aux annonceurs et aux éditeurs.

Les rôles d’accès de votre organisation déterminent ce que les utilisateurs peuvent voir et faire dans Real-Time CDP Collaboration. Avant de poursuivre, assurez-vous que les autorisations basées sur les rôles sont correctement configurées pour garantir un accès et une visibilité appropriés dans la plateforme.

**Ressources:**

- [Documentation d’accès utilisateur](./permissions/manage-user-access.md)
- [Documentation sur la configuration des rôles](./permissions/manage-roles.md)


Regardez cette vidéo pour savoir comment attribuer des accès et des autorisations de produit pour Collaboration à l’aide d’Admin Console et de l’interface utilisateur d’Experience Platform.

>[!VIDEO](https://video.tv.adobe.com/v/3452232/?learn=on&enablevpops&captions=fre_fr)

## Étape 2 : configurer votre organisation Real-Time CDP Collaboration {#set-up-your-organization}

>[!NOTE]
>
>Cette étape s’applique à la fois aux annonceurs et aux éditeurs.

Avant de pouvoir ajouter des audiences, vous devez configurer votre organisation dans Collaboration. Cela régit la manière dont votre organisation apparaît et se comporte dans l’interface.

Si vous ne disposez pas d’un accès administrateur à Experience Platform, contactez l’administrateur de votre organisation pour obtenir de l’aide sur la réalisation de cette configuration.

Définissez le rôle de votre organisation dans Collaboration, fournissez des ressources de marque et configurez des clés de correspondance pour aligner les audiences sur les connexions. Suivez ensuite les étapes ci-dessous pour finaliser la configuration et préparer votre organisation à interagir avec vos connexions.

>[!NOTE]
>
>Vous pouvez créer un ou plusieurs collaborateurs (tels que des profils d’annonceurs ou d’éditeurs) lors de la configuration. Certains champs, tels que les ressources de marque et l’e-mail du contact, peuvent être mis à jour ultérieurement dans l’espace de travail **[!UICONTROL Paramètres]**. Les clés de correspondance peuvent être supprimées au niveau du projet, mais pas ajoutées, alors planifiez-les avec soin.

- **Attribuer un rôle** - Détermine si votre organisation agit en tant qu’annonceur, éditeur ou les deux. Votre rôle définit les fonctionnalités de collaboration dont vous disposez, par exemple le lancement du partage d’audience (annonceur) ou la mise à disposition d’audiences (éditeur). Pour en savoir plus sur l’impact des rôles sur le workflow de collaboration, consultez le [guide de workflow de bout en bout](./end-to-end-workflow.md).
- **Valorisation de marque des ressources** - Ajoutez les éléments suivants à votre compte :
   - Nom de la marque (100 caractères max.)
   - Description de la marque (1 000 caractères max.)
   - Logo de la marque (SVG &lt;20KB, idéalement carré)
   - Bannière de marque (JPG 2688x1536 ou similaire)
- **E-mail de contact** - Fournissez un e-mail professionnel que les collaborateurs peuvent utiliser une fois la connexion établie.

  >[!NOTE]
  >
  >Si vous créez un compte d’éditeur et souhaitez qu’il soit visible publiquement dans le catalogue des connexions de Collaboration, contactez le représentant de votre compte Adobe. Les comptes d’éditeur nécessitent une bannière de marque personnalisée (JPG 2 688 x 1 536). Ce fichier peut être partagé directement avec votre représentant.

- **Configurer les clés de correspondance** - Sélectionnez les identifiants utilisés pour la correspondance d’audience (actuellement, l’e-mail haché est la seule clé de correspondance prise en charge).

Une fois votre organisation créée et vos clés de branding et de correspondance configurées, votre organisation est prête à commencer à approvisionner les audiences et à activer les données.

Pour en savoir plus sur la configuration initiale de l’organisation, notamment sur la définition des rôles, le chargement de ressources de marque et la configuration des clés de correspondance, consultez le document [configuration initiale de l’organisation](./setup/onboard-organization.md#initial-organization-setup){target="_blank"}.

Regardez une présentation détaillée de la configuration de l’annonceur, y compris la création de compte, le branding et la configuration des clés de correspondance.

>[!VIDEO](https://video.tv.adobe.com/v/3452264/?learn=on&enablevpops)

## Étape 3 : Audiences Source (à partir d’Experience Platform ou d’une source cloud) {#source-audiences}

Sélectionnez l’un des magasins de données suivants, ou les deux, pour approvisionner les audiences. Utilisez l’interface utilisateur de Collaboration ou coordonner avec Adobe pour approvisionner les audiences dans un format qui protège la confidentialité.

### Option A : Source à partir d’Experience Platform

[Utilisez l’interface utilisateur des destinations Collaboration pour lier un sandbox qui contient des audiences](./setup/onboard-audiences.md). Utilisez cette méthode en libre-service pour référencer des segments d’audience existants à partir de votre instance Experience Platform.

### Option B : Source de Snowflake ou Amazon S3

Pour configurer une source cloud (par exemple, [!DNL AWS S3] ou [!DNL Snowflake]), préparez les données de votre audience à l’aide de la [PDF de spécification d’audience](../assets/quick-start/RTCDP_Collaboration_Audience_Onboarding_Spec_v1.0.pdf) suivante. Une fois l’opération terminée ou si vous avez des questions, contactez votre représentant de compte Adobe pour finaliser la configuration. Cette méthode n’est pas en libre-service et nécessite l’assistance d’Adobe.

>[!IMPORTANT]
>
>Les fichiers d’audience basés sur le cloud doivent suivre le schéma requis décrit dans le PDF de spécification d’audience. Les fichiers doivent inclure des identifiants hachés (SHA256 en minuscules), les champs de métadonnées requis tels que `segment_name` et `activation_id`, et utiliser des formats pris en charge tels que CSV ou Parquet. Adobe ne normalise pas les données avant l’activation. La durée de vie est appliquée en fonction de la durée de vie de l’audience.
>
>Toutes les audiences du fichier chargé sont entièrement sourcées à ce stade. L’accès à des organisations partenaires spécifiques est configuré séparément via l’interface utilisateur de Collaboration.

### Configuration des audiences

Configurez la manière dont les audiences sont préparées, appariées et gouvernées pour une utilisation dans les connexions.

- **Sélectionner des audiences** *(Experience Platform uniquement)* - Choisissez des segments d’audience avec des identifiants pris en charge.
- **Mapper les clés de correspondance** - Alignez les champs d’audience avec les clés de correspondance configurées.
- **Appliquer des transformations** - Hachage de valeurs en texte brut (par exemple, e-mail) si nécessaire.
- **Planification des actualisations** - Définissez la fréquence de mise à jour (par exemple, quotidienne).
- **Configurer les paramètres de consentement** - Déterminez les profils pouvant être inclus dans les connexions en sélectionnant un mode de consentement : opt-in, opt-out ou aucun.

>[!NOTE]
>
>Vous pouvez ajouter ou supprimer des audiences et mettre à jour le planning d’actualisation directement dans l’interface utilisateur de Collaboration. Pour modifier d’autres paramètres, tels que les clés de correspondance ou le mode de consentement, vous devez supprimer et recréer la connexion aux données.

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
>Si votre source contient des **identifiants en texte brut**, utilisez l’option **[!UICONTROL Appliquer la transformation]** dans l’interface utilisateur pour appliquer le hachage. Cette option est disponible uniquement lors de l’approvisionnement d’audiences à partir d’Experience Platform et n’est pas prise en charge pour les sources cloud.
>
>Pour plus d’informations, consultez la section [mapper des champs](./setup/onboard-audiences.md#map-fields) du guide d’importation et de gestion des audiences.

Pour découvrir une présentation complète de la manière de référencer des audiences à l’aide de l’interface utilisateur de Collaboration, regardez la vidéo de démonstration Référencement d’audience Collaboration ci-dessous.

>[!VIDEO](https://video.tv.adobe.com/v/3452217/?learn=on&enablevpops)

Vous pouvez également consulter le document sur la [mise à disposition des audiences dans Real-Time CDP Collaboration](https://experienceleague.adobe.com/fr/docs/real-time-cdp-collaboration/using/setup/onboard-audiences#import-audiences).

## Étape 4 : activer les audiences (vers Experience Platform ou une destination cloud) {#activate-audiences}

>[!NOTE]
>
>Cette étape s’applique à la fois aux annonceurs et aux éditeurs.

Utilisez l’interface utilisateur de Collaboration pour activer des audiences vers votre instance Experience Platform ou une destination cloud.

### Option A : activer dans Experience Platform

Suivez les étapes décrites dans le guide [Configurer Adobe Experience Platform en tant que destination](https://experienceleague.adobe.com/fr/docs/real-time-cdp-collaboration/using/destinations/experience-platform).

- **Créer une destination** - Utilisez l’interface utilisateur pour configurer une destination Experience Platform (au niveau du sandbox).
- **Mapper les clés de correspondance** - Sélectionnez l’identifiant (par exemple, `hashedEmail`).
- **Définir une durée de vie** - Définir l’expiration (1-30 jours).
- **Vérification dans Audience Portal** - Une fois qu’un collaborateur vous envoie une audience, vérifiez qu’elle apparaît dans Audience Portal sous l’origine « [!UICONTROL Real-Time CDP Collaboration]. »

### Option B : Activer vers le cloud

Pour activer des audiences vers une destination cloud (telle que [!DNL AWS S3] ou [!DNL Snowflake]), contactez votre représentant de compte Adobe pour lancer le processus de configuration. Vous devez fournir les détails de destination tels que le chemin d’accès au fichier, les informations d’identification et le format de fichier attendu. Lors de la configuration, vous devez également spécifier une clé de correspondance (par exemple, `hashedEmail`) et définir la durée de vie et la fréquence d’actualisation souhaitées. Une fois la configuration terminée, Adobe approvisionne la destination et garantit la diffusion correcte des données.

Les données d’audience envoyées à une destination cloud suivent un schéma prédéfini. Pour une description détaillée des champs et du format requis, téléchargez le [Guide Collaboration Audience Activation](../assets/quick-start/RTCDP_Collaboration_Audience_Activation_Spec_v1.0.pdf).

### Principales différences

La liste suivante met en évidence les différences entre les options d’activation d’Experience Platform et du cloud :

- Les activations vers Experience Platform sont entièrement en libre-service et visibles dans le portail Audience.
- Les destinations cloud nécessitent une coordination Adobe et ne sont pas visibles dans l’interface utilisateur.

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

## Vérification

Après l’activation, vérifiez que les audiences ont été correctement diffusées ou mises à disposition dans la destination appropriée.

- Vérifiez que vos audiences s’affichent dans le Portail d’audiences (pour l’activation d’Experience Platform).
- Confirmez la réussite de la diffusion dans le cloud via des logs de destination externes ou confirmez.

## Étape 6 : Se connecter avec les collaborateurs {#connect-with-collaborators}

Une fois la configuration et l’approvisionnement des données terminés, votre organisation est prête à se connecter à ses collaborateurs en envoyant ou en acceptant des invitations et en envoyant les paramètres du projet pour approbation. Ce processus de connexion implique l’envoi ou la réception d’invitations, la révision et l’envoi des paramètres de connexion (tels que les cas d’utilisation et la consommation de crédit) et la confirmation de la relation.

En tant qu’annonceur, utilisez l’espace de travail **[!UICONTROL Connect]** dans le menu de navigation de gauche de l’interface utilisateur de Collaboration pour parcourir les éditeurs disponibles.

>[!NOTE]
>
>Actuellement, seuls les annonceurs peuvent parcourir les éditeurs. Les éditeurs ne peuvent pas parcourir ni établir de connexions avec les annonceurs.

Pour obtenir un aperçu de ce flux, consultez le guide [Se connecter aux annonceurs ou aux éditeurs](./connect/establishing-connections.md){target="_blank"}. Pour une présentation visuelle du processus de connexion, y compris la navigation des collaborateurs et la gestion des paramètres de connexion, regardez la vidéo [configuration du compte d’annonceur](https://experienceleague.adobe.com/fr/docs/platform-learn/tutorials/collaboration/connect-with-publishers){target="_blank"}.

## Étapes suivantes

Vous avez maintenant terminé la configuration initiale et configuré votre organisation pour une collaboration sécurisée. Explorez ensuite les ressources suivantes pour mieux comprendre l’activation, la mesure et la gouvernance des données :

- [Documentation sur le workflow d’activation de l’audience](./collaborate/activate.md)
- [Cas d’utilisation de Measurement](./collaborate/measure.md)
- [Bonnes pratiques de gouvernance de Collaboration](./setup/onboard-audiences.md#governance-policy-and-enforcement-actions)
