---
title: Workflow de bout en bout
description: Découvrez le workflow de bout en bout de l’utilisation de Real-Time CDP Collaboration en fonction de votre modèle de collaboration.
audience: admin, publisher, advertiser
badgelimitedavailability: label="Disponibilité limitée" type="Informative" url="https://helpx.adobe.com/legal/product-descriptions/real-time-customer-data-platform-collaboration.html newtab=true"
exl-id: 90f9341e-5dd7-4521-a602-edb0263838c5
source-git-commit: 901b17c7493e76b17e780b6f7b05a69fa22303d2
workflow-type: tm+mt
source-wordcount: '1738'
ht-degree: 0%

---

# Workflow de bout en bout

{{limited-availability-release-note}}

Dans Adobe Real-Time CDP Collaboration, le workflow de bout en bout varie en fonction du modèle de collaboration que vous choisissez. Le workflow décrit les étapes de configuration et d’exécution d’un projet de collaboration, depuis la création de comptes et d’audiences d’approvisionnement jusqu’à la création de connexions et de projets. Il est essentiel de comprendre ce workflow pour tirer efficacement parti des fonctionnalités de la plateforme afin d’atteindre vos objectifs marketing.

## Commencer

Avant de commencer, assurez-vous de bien comprendre ces concepts clés :

- **Modèles Collaboration** : ces modèles définissent la façon dont les collaborateurs travaillent ensemble. Il existe cinq modèles distincts :
   - [publicitaire à éditeur](./collaboration-patterns.md#advertiser-to-publisher)
   - [de marque à marque](./collaboration-patterns.md#brand-to-brand)
   - [publicitaire partenaire de données](./collaboration-patterns.md#advertiser-to-data-partner)
   - [agence à éditeur](./collaboration-patterns.md#agency-to-publisher)
   - [plateforme publicitaire-agence](./collaboration-patterns.md#advertiser-to-agency-platform)
- **Rôles de compte** : les rôles de compte déterminent vos fonctionnalités au sein de la plateforme. Ils doivent s’aligner sur les objectifs, la marque et les buts de votre entreprise. Il existe quatre rôles de compte : [annonceur](./roles.md#advertiser), [éditeur](./roles.md#publisher), [agence](./roles.md#agency) et [partenaire de données](./roles.md#data-partner).
- **Cas d’utilisation** : les cas d’utilisation définissent les manières dont vous pouvez tirer parti de Collaboration pour atteindre vos objectifs marketing. Il existe trois cas d’utilisation de collaboration : [Découvrir](./use-cases.md#discover), [Activer](./use-cases.md#activate) et [Mesurer](./use-cases.md#measure).

Ce guide utilise trois collaborateurs simulés pour illustrer le workflow de bout en bout :

- **[!UICONTROL Luma]** : une marque de vêtements de sport. Il s’agit d’un annonceur qui souhaite atteindre des audiences spécifiques par le biais de campagnes marketing ciblées.
- **[!UICONTROL TV Tube]** : un fournisseur de streaming numérique. Il s’agit d’un éditeur qui fournit des données d’audience utilisables par les annonceurs.
- **[!UICONTROL Fit Apparel]** : Une autre marque de vêtements de sport. Il s’agit d’un second annonceur qui souhaite collaborer pour partager des données et des informations relatives à l’audience afin d’améliorer les efforts marketing.
- **[!UICONTROL Agency99]** : agence de presse. Ils gèrent plusieurs comptes clients dans leur espace de travail et se connectent aux éditeurs et aux annonceurs.
- **[!UICONTROL DataM8]** : fournisseur de données tiers. Ils fournissent des données d’audience à l’usage des annonceurs.
- **[!UICONTROL Holdco]** : plateforme de services publicitaires et marketing d’une société holding d’agence utilisée par les équipes internes de l’agence pour gérer les campagnes client.

## Workflow publicitaire-éditeur {#advertiser-to-publisher-workflow}

[!UICONTROL Luma], une société de vente au détail sportive, souhaite établir une connexion avec [!UICONTROL TV Tube], un fournisseur de streaming numérique, pour atteindre des audiences spécifiques par le biais de campagnes marketing ciblées.

Pour commencer, [!UICONTROL Luma] doit [créer un compte](../setup/onboard-account.md) avec le rôle d’annonceur, tandis que [!UICONTROL TV Tube] crée un compte avec le rôle d’éditeur.

Après avoir établi leurs comptes, [!UICONTROL Luma] et [!UICONTROL TV Tube] doivent [ créer une connexion de données et des audiences sources](../setup/onboard-audiences.md). Seule [!UICONTROL TV Tube] active les audiences pour les campagnes marketing. Elles doivent donc [configurer une destination](../setup/manage-destinations.md).

Une fois que les comptes des deux collaborateurs sont configurés, ils sont prêts à [former une connexion](../connect/establishing-connections.md) au sein de la plateforme. [!UICONTROL Luma] utilise la fonctionnalité [découvrir les collaborateurs](../connect/discover-collaborators.md) pour rechercher [!UICONTROL TV Tube] et lancer une demande de connexion. Une fois que [!UICONTROL TV Tube] a accepté la demande de connexion, [!UICONTROL Luma] configure les paramètres de connexion pour définir comment ils vont collaborer. [!UICONTROL TV Tube] accepte la demande de connexion pour établir un lien sécurisé entre les deux marques.

Une fois la connexion établie, [!UICONTROL Luma] [crée un projet](../collaborate/manage-projects.md) pour lancer leur collaboration avec [!UICONTROL TV Tube]. Pendant la configuration du projet, ils choisissent les cas d’utilisation de collaboration qui correspondent le mieux à leurs objectifs : [Découvrir](../collaborate/discover.md), [Activer](../collaborate/activate.md) et [Mesurer](../collaborate/measure.md).

[!UICONTROL Luma] exploite le cas d’utilisation [Discover](../collaborate/discover.md) pour obtenir des informations sur les données d’audience de [!UICONTROL TV Tube]. Une fois que [!UICONTROL Luma] a identifié les segments d’audience cibles, ils [Activer](../collaborate/activate.md) ces audiences.

Après avoir activé les audiences, [!UICONTROL TV Tube] exécute des campagnes marketing ciblées et charge les données dans [Mesurer](../collaborate/measure.md) afin d’évaluer l’efficacité de leur campagne.

## Workflow de marque à marque {#brand-to-brand-workflow}

[!UICONTROL Fit Apparel], une marque de vêtements de sport, souhaite collaborer avec [!UICONTROL Luma], une autre marque de vêtements de sport, pour partager des données d’audience et des informations afin d’améliorer les efforts de marketing.

Après avoir établi leurs comptes, [!UICONTROL Fit Apparel] et [!UICONTROL Luma] doivent [créer une connexion de données et des audiences sources](../setup/onboard-audiences.md). Les options [!UICONTROL Ajuster les vêtements] et [!UICONTROL Luma] activent toutes deux les audiences pour les campagnes marketing. Elles doivent donc [configurer une destination](../setup/manage-destinations.md).

Après avoir sourcé leurs audiences, [!UICONTROL Fit Apparel] et [!UICONTROL Luma] [forment une connexion](../connect/establishing-connections.md) dans la plateforme pour partager en toute sécurité les données d’audience. Pour ce faire, ils doivent utiliser la fonctionnalité [invitation à une connexion privée](../connect/establishing-connections.md#private-connection-invite). [!UICONTROL Luma] partage son code de connexion avec [!UICONTROL Fit Apparel], qui l’utilise ensuite pour lancer une demande de connexion. Une fois que [!UICONTROL Luma] a accepté la demande de connexion, [!UICONTROL Fit Apparel] configure les paramètres de connexion pour définir comment ils vont collaborer. Dans la configuration, [!UICONTROL Ajuster les vêtements] indique que les deux collaborateurs peuvent activer des audiences pour les campagnes marketing. Pour terminer la connexion, [!UICONTROL Luma] accepte la demande d’établissement d’un lien sécurisé entre les deux marques.

Une fois la connexion établie, [!UICONTROL Fit Apparel] [crée un projet](../collaborate/manage-projects.md) pour lancer leur collaboration avec [!UICONTROL Luma]. Pendant la configuration du projet, ils choisissent les cas d’utilisation de collaboration qui correspondent le mieux à leurs objectifs : [Découvrir](../collaborate/discover.md), [Activer](../collaborate/activate.md) et [Mesurer](../collaborate/measure.md).

[!UICONTROL Fit Apparel] et [!UICONTROL Luma] peuvent tous deux utiliser le cas d’utilisation [Discover](../collaborate/discover.md) pour obtenir des informations sur les données d’audience de l’autre. Une fois qu’ils ont identifié des segments d’audience importants, ils [Activent](../collaborate/activate.md) les audiences de leur choix pour les campagnes marketing.

Enfin, après l&#39;exécution de leurs campagnes, les deux marques chargent les données vers [Mesurer](../collaborate/measure.md) les résultats et évaluent l&#39;efficacité de leur collaboration.

## Workflow publicitaire vers plateforme publicitaire {#advertiser-to-advertising-platform-workflow}

[!UICONTROL Luma], une société de vente au détail sportive, souhaite se connecter à [!DNL Amazon Marketing Cloud] ([!DNL AMC]) pour améliorer ses fonctionnalités marketing en tirant parti des outils de résolution d’identité et de ciblage d’[!DNL AMC]. Luma dispose déjà d’un compte [!DNL Amazon Advertising] actif et est autorisé à l’utiliser [!DNL AMC].

Pour commencer, [!UICONTROL Luma] doit [créer un compte](../setup/onboard-account.md) avec le rôle d’annonceur. Après avoir établi leur compte, [!UICONTROL Luma] doit [créer une connexion de données et des audiences sources](../setup/onboard-audiences.md). Comme [!UICONTROL Luma] active des audiences pour les campagnes marketing, elles doivent [configurer une destination](../setup/manage-destinations.md).

Une fois que [!UICONTROL Luma] a configuré son compte, il est prêt à [former une connexion](../connect/establishing-connections.md) avec [!DNL AMC] au sein de la plateforme. [!UICONTROL Luma] utilise la fonctionnalité [découvrir les collaborateurs](../connect/discover-collaborators.md) pour rechercher [!UICONTROL Amazon Marketing Cloud] et [lancer une demande de connexion](../connect/advertising-platforms/amc.md). Après l’authentification et l’autorisation de la connexion via la page de connexion [!DNL Amazon], la connexion à [!DNL AMC] est établie.

Une fois la connexion établie, [!UICONTROL Luma] [crée un projet](../collaborate/manage-projects.md) pour lancer leur collaboration avec [!DNL AMC]. Les paramètres de connexion, y compris les cas pratiques, sont préconfigurés en fonction de la plateforme publicitaire. Par [!DNL AMC], le cas d’utilisation disponible est [Découvrir](../collaborate/advertising-platforms/amc.md#discover).

[!UICONTROL Luma] tire parti du cas d’utilisation [Discover](../collaborate/advertising-platforms/amc.md#discover) pour obtenir des informations et des données d’audience de [!DNL AMC]. Grâce à ces informations, [!UICONTROL Luma] peut optimiser ses stratégies marketing et améliorer l’efficacité de ses campagnes.

## Workflow publicitaire-partenaire de données {#advertiser-to-data-partner-workflow}

[!UICONTROL Luma], une société de vente au détail sportive, souhaite collaborer avec [!UICONTROL DataM8], un fournisseur de données tiers, pour enrichir les profils clients et améliorer le ciblage des audiences.

Pour commencer, [!UICONTROL Luma] doit [créer un compte](../setup/onboard-account.md) avec le rôle d’annonceur, tandis que [!UICONTROL DataM8] crée un compte avec le rôle de partenaire de données.

Après avoir établi leurs comptes, [!UICONTROL Luma] et [!UICONTROL DataM8] doivent [créer une connexion de données et des audiences sources](../setup/onboard-audiences.md). Les deux collaborateurs peuvent activer des audiences pour les campagnes marketing. Ils doivent donc chacun [configurer une destination](../setup/manage-destinations.md).

Une fois que les comptes des deux collaborateurs sont configurés, ils sont prêts à [former une connexion](../connect/establishing-connections.md) au sein de la plateforme. [!UICONTROL Luma] utilise la fonctionnalité [découvrir les collaborateurs](../collaborate/discover.md) pour rechercher [!UICONTROL DataM8] et lancer une demande de connexion. Une fois que [!UICONTROL DataM8] a accepté la demande de connexion, [!UICONTROL Luma] configure les paramètres de connexion pour définir comment ils vont collaborer. [!UICONTROL DataM8] accepte la demande de connexion pour établir un lien sécurisé entre les deux collaborateurs.

Une fois la connexion établie, [!UICONTROL Luma] [crée un projet](../collaborate/manage-projects.md) pour lancer leur collaboration avec [!UICONTROL DataM8]. Pendant la configuration du projet, ils choisissent les cas d’utilisation de collaboration qui correspondent le mieux à leurs objectifs : [Découvrir](../collaborate/discover.md), [Activer](../collaborate/activate.md) et [Mesurer](../collaborate/measure.md).

[!UICONTROL Luma] exploite le cas d’utilisation [Discover](../collaborate/discover.md) pour obtenir des informations sur les données d’audience de [!UICONTROL DataM8]. Une fois que [!UICONTROL Luma] a identifié les segments d’audience cibles, ils [activent](../collaborate/activate.md) ces audiences.

[!UICONTROL DataM8] peut également [activer](../collaborate/activate.md) ses audiences vers [!UICONTROL Luma]. [!UICONTROL Luma] utilise ces fonctionnalités pour ajouter des attributs tiers à ses profils clients et analyser la composition de l’audience. Grâce aux données enrichies disponibles directement dans sa plateforme CDP, [!UICONTROL Luma] peut créer des audiences plus précises et les activer vers des destinations de médias payants sans déplacer les données en dehors de son environnement régi.

## Workflow Agence-vers-éditeur {#agency-to-publisher-workflow}

[!UICONTROL Agency99], une agence de médias, souhaite collaborer avec [!UICONTROL TV Tube], un fournisseur de streaming numérique, pour atteindre des audiences spécifiques par le biais de campagnes marketing ciblées.

Pour commencer, [!UICONTROL Agency99] doit [créer un compte](../setup/onboard-account.md) avec le rôle d’agence, tandis que [!UICONTROL TV Tube] crée un compte avec le rôle d’éditeur.

Après avoir établi leurs comptes, [!UICONTROL Agency99] et [!UICONTROL TV Tube] doivent [ créer une connexion de données et des audiences sources](../setup/onboard-audiences.md). [!UICONTROL Agency99] configurera les sous-comptes clients et les données client sources dans son espace de travail. Seule [!UICONTROL TV Tube] active les audiences pour les campagnes marketing. Elles doivent donc [configurer une destination](../setup/manage-destinations.md).

Une fois que les comptes des deux collaborateurs sont configurés, ils sont prêts à [former une connexion](../connect/establishing-connections.md) au sein de la plateforme. [!UICONTROL Agency99] utilise la fonction [découvrir les collaborateurs](../collaborate/discover.md) pour rechercher [!UICONTROL TV Tube] et lancer une demande de connexion. [!UICONTROL Agency99] le fera pour un ou plusieurs clients qui souhaitent collaborer avec [!UICONTROL TV Tube]. Une fois que [!UICONTROL TV Tube] a accepté la ou les demandes de connexion, [!UICONTROL Agency99] configure les paramètres de connexion pour définir comment chaque collaboration doit se dérouler. [!UICONTROL TV Tube] accepte la ou les demandes de connexion pour établir une liaison sécurisée entre les deux marques.

Une fois la connexion établie, [!UICONTROL Agency99] [crée un projet](../collaborate/manage-projects.md) pour lancer leur collaboration avec [!UICONTROL TV Tube] dans chaque sous-compte client. Pendant la configuration du projet, ils choisissent les cas d’utilisation de collaboration qui correspondent le mieux à leurs objectifs : [Découvrir](../collaborate/discover.md), [Activer](../collaborate/activate.md) et [Mesurer](../collaborate/measure.md).

[!UICONTROL Agency99] exploite le cas d’utilisation [Discover](../collaborate/discover.md) pour obtenir des informations sur les données d’audience de [!UICONTROL TV Tube]. Une fois que [!UICONTROL Agency99] a identifié les segments d’audience cibles, ils [activent](../collaborate/activate.md) ces audiences.

Après avoir activé les audiences, [!UICONTROL TV Tube] exécute des campagnes marketing ciblées et charge les données pour [mesurer](../collaborate/measure.md) les résultats afin d’évaluer l’efficacité de leur campagne.

## Workflow de plateforme publicitaire-agence {#advertiser-to-agency-platform-workflow}

[!UICONTROL Luma], une société de vente au détail sportive, souhaite collaborer avec [!UICONTROL Holdco], une plateforme d’agence, pour partager des données et recevoir des informations sur les médias payants.

Pour commencer, [!UICONTROL Luma] doit [créer un compte](../setup/onboard-account.md) avec le rôle d’annonceur, tandis que [!UICONTROL Holdco] crée un compte avec le rôle d’agence. 

Après avoir établi leurs comptes, [!UICONTROL Luma] et [!UICONTROL Holdco] doivent [créer une connexion de données et des audiences sources](../setup/onboard-audiences.md). Les deux collaborateurs peuvent activer des audiences pour les campagnes marketing. Ils doivent donc chacun [configurer une destination](../setup/manage-destinations.md). 

Une fois que les comptes des deux collaborateurs sont configurés, ils sont prêts à [former une connexion](../connect/establishing-connections.md) au sein de la plateforme. [!UICONTROL Luma] utilise la fonctionnalité [découvrir les collaborateurs](../collaborate/discover.md) pour rechercher [!UICONTROL Holdco] et lancer une demande de connexion. Une fois que [!UICONTROL Holdco] a accepté la demande de connexion, [!UICONTROL Luma] configure les paramètres de connexion pour définir comment ils vont collaborer.

[!UICONTROL Holdco] accepte la demande de connexion pour établir un lien sécurisé entre les deux collaborateurs.

Une fois la connexion établie, [!UICONTROL Luma] [crée un projet](../collaborate/manage-projects.md) pour lancer leur collaboration avec [!UICONTROL Holdco]. Pendant la configuration du projet, ils choisissent les cas d’utilisation de collaboration qui correspondent le mieux à leurs objectifs : [Découvrir](../collaborate/discover.md), [Activer](../collaborate/activate.md) et [Mesurer](../collaborate/measure.md).

[!UICONTROL Luma] exploite le cas d’utilisation [Discover](../collaborate/discover.md) pour obtenir des informations sur les données d’audience de [!UICONTROL Holdco]. Une fois que [!UICONTROL Luma] a identifié les segments d’audience cibles, ils [activent](../collaborate/activate.md) ces audiences.

[!UICONTROL Holdco] peut également [activer](../collaborate/activate.md) ses audiences vers [!UICONTROL Luma]. [!UICONTROL Luma] utilise ces fonctionnalités pour recevoir des informations sur les médias payants à partir de campagnes gérées par l’agence pour obtenir des informations, des ajouts de profil CDP et une orchestration des médias propriétaires.
