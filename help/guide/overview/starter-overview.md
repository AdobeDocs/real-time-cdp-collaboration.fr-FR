---
title: Présentation du démarrage de RTCDP Collaboration
description: Découvrez comment Adobe Real-Time CDP Collaboration Starter vous permet d’étendre et d’améliorer la collaboration axée sur la confidentialité avec un partenaire sous licence sans avoir à obtenir votre propre licence Real-Time CDP complète.
audience: publisher, advertiser, invited users to Real-Time CDP Collaboration Starter
badgelimitedavailability: label="Disponibilité limitée" type="Informative" url="https://helpx.adobe.com/legal/product-descriptions/real-time-customer-data-platform-collaboration.html newtab=true"
exl-id: 7ae0bd3d-eee9-48c0-9f18-a56033fee52d
source-git-commit: c759496b528ed6c1e173f1ca1f1469da572c85df
workflow-type: tm+mt
source-wordcount: '843'
ht-degree: 3%

---

# Présentation d’Adobe Real-Time CDP Collaboration [!DNL Starter]

Utilisez Adobe Real-Time CDP Collaboration [!DNL Starter] pour collaborer avec un partenaire sous licence sur des projets de données axés sur la confidentialité. Vous n’avez pas besoin de votre propre licence Collaboration pour participer.

Votre partenaire sous licence vous invite dans Collaboration et utilise ses crédits pour financer vos workflows conjoints, à la fois entre annonceurs et éditeurs et entre marques. Pour en savoir plus sur ces modèles et leur fonctionnement, consultez les guides [modèles de collaboration](./collaboration-patterns.md) et [workflow de bout en bout](./end-to-end-workflow.md).

En tant qu’utilisateur [!DNL Starter] invité, vous pouvez :

* Intégrez et gérez les données de collaboration dans un compte [!DNL Starter].
* Source et gestion des audiences à utiliser dans des projets conjoints.
* Obtenez des informations sur les chevauchements d’audience avec votre partenaire afin de prendre en charge un ciblage et une mesure de campagne efficaces.
* Activez les audiences et renvoyez-les à votre partenaire pour une activation et un engagement conjoints de la campagne.

## Conditions préalables {#prerequisites}

Pour commencer à utiliser Collaboration [!DNL Starter], assurez-vous que votre entreprise et votre partenaire sous licence se trouvent dans la même région. Vous devez être invité par un partenaire titulaire d’une licence Real-Time CDP Prime, Ultimate ou Collaboration.

Pour lancer l’invitation, fournissez les informations suivantes à votre partenaire sous licence :

* Nom du contact
* E-mail de contact
* Société
* Rôle (Annonceur/Éditeur) : Annonceur
* Secteur industriel

Après avoir reçu et accepté l’invitation, votre entreprise doit vérifier et signer une commande client gratuite avec Adobe pour accéder à Collaboration [!DNL Starter]. Pour plus d’informations sur le processus d’invitation, consultez le guide [inviter un collaborateur à Collaboration [!DNL Starter]](../connect/establishing-connections.md#invite-collaborator).

## Mécanismes de sécurisation {#guardrails}

Lisez le tableau suivant pour comprendre les principaux mécanismes de sécurisation qui s’appliquent à votre compte [!DNL Starter]. Il s’agit notamment des limites sur l’approvisionnement des audiences, le volume des données, la fréquence d’actualisation, les chevauchements d’audiences et les fonctionnalités d’activation.

| Mécanisme de sécurisation | Description |
|----------| ------------|
| Audience source | Vous pouvez importer des données d’audience dans Collaboration avec **[!DNL Amazon S3]** comme source. Pour obtenir des instructions détaillées, voir [comment configurer [!DNL Amazon S3] pour l’approvisionnement des audiences](../setup/configure-aws-s3-audience-sourcing.md). |
| Audience | Votre compte [!DNL Starter] a droit à un maximum de :<ul><li>10 audiences provenant d’un compartiment [!DNL AWS S3]</li><li>50 millions d’identités totales (calculées par le nombre de lignes dans vos données d’audience)</li><li>1 actualisation par audience tous les 6 jours</li></ul> |
| Chevauchements d’audience et informations | Il n’existe aucune limite d’utilisation sur la fréquence à laquelle vous pouvez exécuter des chevauchements d’audiences et des informations sur vos audiences. Découvrez comment [découvrir des chevauchements et comparer des audiences](../collaborate/discover.md). |
| Activation | En tant qu’utilisateur [!DNL Starter], vous ne pouvez activer et partager des audiences qu’avec le partenaire qui vous a invité. La configuration des destinations vers des plateformes externes n’est pas disponible. En savoir plus sur l’[activation de vos audiences](../collaborate/activate.md). |

{style="table-layout:auto"}

## Prise en main {#getting-started}

Après avoir [accepté votre invitation et accepté les conditions](../connect/establishing-connections.md#accept-invitation-sign-terms), connectez-vous à [Adobe Experience Cloud](https://experience.adobe.com/){target="_blank"} avec vos informations d’identification. Avant de pouvoir utiliser Collaboration, vous devez disposer des droits d’accès et des rôles appropriés sur votre compte.

Utilisez ce workflow pour configurer votre compte [!DNL Starter] et commencer à collaborer avec votre partenaire.

### Configurer l’accès administrateur {#setup-admin-access}

Tout d’abord, utilisez l’espace de travail **Accès administrateur** pour vous accorder l’accès nécessaire. Vous disposez ainsi à la fois de droits d’administration et d’un accès utilisateur aux produits Experience Platform. Pour obtenir des instructions détaillées sur la configuration de l’accès initial, reportez-vous aux [instructions d’accès administrateur](../setup/starter-admin-access.md).

Une fois l’opération terminée, vous devriez voir **[!UICONTROL Autorisations]**, **[!UICONTROL Experience Platform]** et **[!UICONTROL Real-Time CDP Collaboration]** dans la section **[!UICONTROL Accès rapide]** de votre page d’accueil [Adobe Experience Cloud](https://experience.adobe.com/){target="_blank"}.

![L’espace de travail Adobe Experience Cloud affichant les autorisations, Experience Platform et Real-Time CDP Collaboration après la configuration de l’accès administrateur de produit.](/help/assets/overview/starter/setup-admin-access.png){zoomable="yes"}

Pour plus d’informations sur les rôles d’accès et les différents produits Adobe Experience Cloud, consultez la [présentation du contrôle d’accès](../permissions/overview.md).

### Configuration des autorisations {#configure-permissions}

Maintenant que vous disposez des privilèges d’administrateur, vous pouvez vous attribuer des rôles et des autorisations ainsi qu’aux autres utilisateurs de votre organisation. Cette étape est nécessaire avant de pouvoir accéder à Real-Time CDP Collaboration ou de permettre à d’autres personnes de l’utiliser. Pour obtenir des instructions détaillées, voir [comment configurer des autorisations](../setup/starter-permission-controls.md). Pour plus d’informations sur les différents rôles et autorisations disponibles dans Collaboration, consultez la documentation [gérer les rôles](../permissions/manage-roles.md).

Une fois les rôles et les autorisations attribués, vérifiez que vous pouvez accéder à Collaboration. Accédez à [&#128279;](https://experience.adobe.com/){target="_blank"}, puis sélectionnez **[!UICONTROL Real-Time CDP Collaboration]** dans la section **[!UICONTROL Accès rapide]**. L’espace de travail **&#x200B;**&#x200B;s’ouvre, où vous pouvez commencer à utiliser les fonctionnalités de Collaboration.

### Configurer des connexions {#set-up-connections}

Suivez ensuite les étapes des guides suivants pour configurer une connexion et commencer à collaborer avec votre partenaire :

* [Configuration de votre compte Collaboration](../setup/onboard-account.md)
* [Établir un lien avec votre collaborateur invité](../connect/overview.md)
* [Créez un projet et commencez à collaborer avec votre partenaire](../collaborate/overview.md)

### Comprendre l’utilisation du crédit {#understand-credit-usage}

Toutes les activités Collaboration [!DNL Starter] utilisent des crédits. Cependant, en tant qu’utilisateur invité, vous n’avez pas besoin d’acheter ni de gérer ces crédits. Le collaborateur qui vous a invité couvre toutes les utilisations de crédit associées à vos activités. Pour en savoir plus, consultez la documentation [utilisation et consommation du crédit dans Collaboration [!DNL Starter]](../setup/starter-credit-usage.md).

## Étapes suivantes {#next-steps}

Vous avez maintenant terminé la configuration initiale et configuré votre organisation pour une collaboration sécurisée. Consultez ensuite les ressources suivantes pour en savoir plus sur l’approvisionnement des audiences et les différents cas d’utilisation de projets dans Collaboration :

* [Source et gestion des audiences](../setup/onboard-audiences.md)
* [Cas d’utilisation de projet](../collaborate/overview.md#project-use-cases) :
   * [Découvrir les chevauchements et comparer les audiences](../collaborate/discover.md)
   * [Activer les audiences](../collaborate/activate.md)
   * [Mesurer les performances de la campagne](../collaborate/measure.md)
