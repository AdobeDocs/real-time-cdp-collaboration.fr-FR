---
title: Workflow de bout en bout
description: Découvrez le workflow de bout en bout de l’utilisation de Real-Time CDP Collaboration en fonction de votre modèle de collaboration.
audience: admin, publisher, advertiser
badgelimitedavailability: label="Disponibilité limitée" type="Informative" url="https://helpx.adobe.com/fr/legal/product-descriptions/real-time-customer-data-platform-collaboration.html newtab=true"
exl-id: 90f9341e-5dd7-4521-a602-edb0263838c5
source-git-commit: 36f43d9d34ce7851a1c7093e0891f9c87e56387c
workflow-type: tm+mt
source-wordcount: '727'
ht-degree: 0%

---

# Workflow de bout en bout

{{limited-availability-release-note}}

Dans Adobe Real-Time CDP Collaboration, le workflow de bout en bout varie en fonction du modèle de collaboration que vous choisissez. Le workflow décrit les étapes de configuration et d’exécution d’un projet de collaboration, depuis la création de comptes et d’audiences d’approvisionnement jusqu’à la création de connexions et de projets. Il est essentiel de comprendre ce workflow pour tirer efficacement parti des fonctionnalités de la plateforme afin d’atteindre vos objectifs marketing.

## Commencer

Avant de commencer, assurez-vous de bien comprendre ces concepts clés :

- **Modèles Collaboration** : ces modèles définissent la façon dont les collaborateurs travaillent ensemble. Il existe deux modèles distincts : [annonceur-éditeur](./collaboration-patterns.md#advertiser-to-publisher) et [marque-à-marque](./collaboration-patterns.md#brand-to-brand).
- **Rôles de compte** : les rôles de compte déterminent vos fonctionnalités au sein de la plateforme. Ils doivent s’aligner sur les objectifs, la marque et les buts de votre entreprise. Il existe deux rôles de compte : [annonceur](./roles.md#advertiser) et [éditeur](./roles.md#publisher).
- **Cas d’utilisation** : les cas d’utilisation définissent les manières dont vous pouvez tirer parti de Collaboration pour atteindre vos objectifs marketing. Il existe trois cas d’utilisation de collaboration : [Découvrir](./use-cases.md#discover), [Activer](./use-cases.md#activate) et [Mesurer](./use-cases.md#measure).

Ce guide utilise trois collaborateurs simulés pour illustrer le workflow de bout en bout :

- **[!UICONTROL Luma]** : une marque de vêtements de sport. Il s’agit d’un annonceur qui souhaite atteindre des audiences spécifiques par le biais de campagnes marketing ciblées.
- **[!UICONTROL TV Tube]** : un fournisseur de streaming numérique. Il s’agit d’un éditeur qui fournit des données d’audience utilisables par les annonceurs.
- **[!UICONTROL Fit Apparel]** : Une autre marque de vêtements de sport. Il s’agit d’un second annonceur qui souhaite collaborer pour partager des données et des informations relatives à l’audience afin d’améliorer les efforts marketing.

## Workflow publicitaire-éditeur {#advertiser-to-publisher-workflow}

[!UICONTROL Luma], une société de vente au détail sportive, souhaite établir une connexion avec [!UICONTROL TV Tube], un fournisseur de streaming numérique, pour atteindre des audiences spécifiques par le biais de campagnes marketing ciblées.

Pour commencer, [!UICONTROL Luma] doit [créer un compte](../setup/onboard-account.md) avec le rôle d’annonceur, tandis que [!UICONTROL TV Tube] crée un compte avec le rôle d’éditeur.

Après avoir établi leurs comptes, [!UICONTROL Luma] et [!UICONTROL TV Tube] doivent [ créer une connexion de données et des audiences sources](../setup/onboard-audiences.md). Seule [!UICONTROL TV Tube] active les audiences pour les campagnes marketing. Elles doivent donc [configurer une destination](../setup/manage-destinations.md).

Une fois que les comptes des deux collaborateurs sont configurés, ils sont prêts à [former une connexion](../connect/establishing-connections.md) au sein de la plateforme. [!UICONTROL Luma] utilise la fonctionnalité [découvrir les collaborateurs](../connect/discover-collaborators.md) pour rechercher [!UICONTROL TV Tube] et lancer une demande de connexion. Une fois que [!UICONTROL TV Tube] a accepté la demande de connexion, [!UICONTROL Luma] configure les paramètres de connexion pour définir la manière dont la collaboration s’effectuera. [!UICONTROL TV Tube] accepte la demande de connexion pour établir un lien sécurisé entre les deux marques.

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
