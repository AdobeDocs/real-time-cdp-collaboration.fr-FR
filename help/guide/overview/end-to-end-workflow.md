---
title: Workflow de bout en bout
description: Understand the end-to-end workflow of using Real-Time CDP Collaboration based on your collaboration pattern.
audience: admin, publisher, advertiser
badgelimitedavailability: label="Disponibilité limitée" type="Informative" url="https://helpx.adobe.com/fr/legal/product-descriptions/real-time-customer-data-platform-collaboration.html newtab=true"
exl-id: 90f9341e-5dd7-4521-a602-edb0263838c5
TQID: https://experienceleague.adobe.com/9edtg5tMbnB3BrdLrDkcHQ-AjBNOqMFGojAja3NCwCs
product_v2:
  - id: fdddec33-c9cb-4459-b8b6-2664395a6f10
feature_v2:
  - id: ba929a52-9339-4154-9487-317dc875a3c7
topic_v2:
  - id: e1e0219c-f879-479f-8427-888ed2a6e9c2
source-git-commit: 3ce7e66b31332836fd6cc6137c94622436505cc9
workflow-type: tm+mt
source-wordcount: 1738
ht-degree: 0%

---

# Workflow de bout en bout

{{limited-availability-release-note}}

In Adobe Real-Time CDP Collaboration, the end-to-end workflow varies based on the collaboration pattern you choose. The workflow outlines the steps involved in setting up and executing a collaboration project, from creating accounts and sourcing audiences to forming connections and creating projects. Understanding this workflow is essential for effectively leveraging the platform&#39;s capabilities to achieve your marketing goals.

## Commencer

Before you begin, ensure you have a solid understanding of these key concepts:

- **Collaboration patterns**: These patterns define how collaborators work together. There are five distinct patterns:
   - [advertiser-to-publisher](./collaboration-patterns.md#advertiser-to-publisher)
   - [brand-to-brand](./collaboration-patterns.md#brand-to-brand)
   - [advertiser-to-data partner](./collaboration-patterns.md#advertiser-to-data-partner)
   - [agency-to-publisher](./collaboration-patterns.md#agency-to-publisher)
   - [advertiser-to-agency platform](./collaboration-patterns.md#advertiser-to-agency-platform)
- **Account roles**: Account roles determine your capabilities within the platform. They should align with your organization&#39;s objectives, brand, and goals. There are four account roles: [advertiser](./roles.md#advertiser), [publisher](./roles.md#publisher), [agency](./roles.md#agency) and [data partner](./roles.md#data-partner).
- **Use cases**: Uses cases define the ways you can leverage Collaboration to achieve your marketing objectives. There are three collaboration use cases: [Discover](./use-cases.md#discover), [Activate](./use-cases.md#activate), and [Measure](./use-cases.md#measure).

This guide will use three mock collaborators to illustrate the end-to-end workflow:

- **[!UICONTROL Luma]**: An athletic apparel brand. They are an advertiser that wants to reach specific audiences through targeted marketing campaigns.
- **[!UICONTROL TV Tube]**: A digital streaming provider. They are a publisher that provides audience data for use by advertisers.
- **[!UICONTROL Fit Apparel]** : Une autre marque de vêtements de sport. Il s’agit d’un second annonceur qui souhaite collaborer pour partager des données et des informations relatives à l’audience afin d’améliorer les efforts marketing.
- **[!UICONTROL Agency99]** : agence de presse. Ils gèrent plusieurs comptes clients dans leur espace de travail et se connectent aux éditeurs et aux annonceurs.
- **[!UICONTROL DataM8]** : fournisseur de données tiers. Ils fournissent des données d’audience à l’usage des annonceurs.
- **[!UICONTROL Holdco]** : plateforme de services publicitaires et marketing d’une société holding d’agence utilisée par les équipes internes de l’agence pour gérer les campagnes client.

## Workflow publicitaire-éditeur {#advertiser-to-publisher-workflow}

[!UICONTROL Luma], une société de vente au détail sportive, souhaite établir une connexion avec [!UICONTROL TV Tube], un fournisseur de streaming numérique, pour atteindre des audiences spécifiques par le biais de campagnes marketing ciblées.

Pour commencer, [!UICONTROL Luma] doit [créer un compte](../setup/onboard-account.md) avec le rôle d’annonceur, tandis que [!UICONTROL TV Tube] crée un compte avec le rôle d’éditeur.

Après avoir établi leurs comptes, [!UICONTROL Luma] et [!UICONTROL TV Tube] doivent [&#x200B; créer une connexion de données et des audiences sources](../setup/onboard-audiences.md). Seule [!UICONTROL TV Tube] active les audiences pour les campagnes marketing. Elles doivent donc [configurer une destination](../setup/manage-destinations.md).

Une fois que les comptes des deux collaborateurs sont configurés, ils sont prêts à [former une connexion](../connect/establishing-connections.md) au sein de la plateforme. [!UICONTROL Luma] utilise la fonctionnalité [découvrir les collaborateurs](../connect/discover-collaborators.md) pour rechercher [!UICONTROL TV Tube] et lancer une demande de connexion. Une fois que [!UICONTROL TV Tube] a accepté la demande de connexion, [!UICONTROL Luma] configure les paramètres de connexion pour définir comment ils vont collaborer. [!UICONTROL TV Tube] accepte la demande de connexion pour établir un lien sécurisé entre les deux marques.

Une fois la connexion établie, [!UICONTROL Luma] [crée un projet](../collaborate/manage-projects.md) pour lancer leur collaboration avec [!UICONTROL TV Tube]. Pendant la configuration du projet, ils choisissent les cas d’utilisation de collaboration qui correspondent le mieux à leurs objectifs : [Découvrir](../collaborate/discover.md), [Activer](../collaborate/activate.md) et [Mesurer](../collaborate/measure.md).

[!UICONTROL Luma] exploite le cas d’utilisation [Discover](../collaborate/discover.md) pour obtenir des informations sur les données d’audience de [!UICONTROL TV Tube]. Une fois que [!UICONTROL Luma] a identifié les segments d’audience cibles, ils [Activer](../collaborate/activate.md) ces audiences.

Après avoir activé les audiences, [!UICONTROL TV Tube] exécute des campagnes marketing ciblées et charge les données dans [Mesurer](../collaborate/measure.md) afin d’évaluer l’efficacité de leur campagne.

## Workflow de marque à marque {#brand-to-brand-workflow}

[!UICONTROL Fit Apparel], une marque de vêtements de sport, souhaite collaborer avec [!UICONTROL Luma], une autre marque de vêtements de sport, pour partager des données d’audience et des informations afin d’améliorer les efforts de marketing.

Après avoir établi leurs comptes, [!UICONTROL Fit Apparel] et [!UICONTROL Luma] doivent [créer une connexion de données et des audiences sources](../setup/onboard-audiences.md). Les options [!UICONTROL Ajuster les vêtements] et [!UICONTROL Luma] activent toutes deux les audiences pour les campagnes marketing. Elles doivent donc [configurer une destination](../setup/manage-destinations.md).

After sourcing their audiences, [!UICONTROL Fit Apparel] and [!UICONTROL Luma] [form a connection](../connect/establishing-connections.md) within the platform to securely share audience data. To do so, they must make use of the [private connection invite](../connect/establishing-connections.md#private-connection-invite) feature. [!UICONTROL Luma] shares their connect code with [!UICONTROL Fit Apparel], who then uses it to initiate a connection request. After [!UICONTROL Luma] accepts the connection request, [!UICONTROL Fit Apparel] configures the connection settings to define how they will collaborate. In the configuration, [!UICONTROL Fit Apparel] specifies that both collaborators can activate audiences for marketing campaigns. To complete the connection, [!UICONTROL Luma] accepts the request to establish a secure link between the two brands.

After the connection is established, [!UICONTROL Fit Apparel] [creates a project](../collaborate/manage-projects.md) to kick off their collaboration with [!UICONTROL Luma]. Pendant la configuration du projet, ils choisissent les cas d’utilisation de collaboration qui correspondent le mieux à leurs objectifs : [Découvrir](../collaborate/discover.md), [Activer](../collaborate/activate.md) et [Mesurer](../collaborate/measure.md).

[!UICONTROL Fit Apparel] and [!UICONTROL Luma] can both use the [Discover](../collaborate/discover.md) use case to gain insights into each other&#39;s audience data. Once they have identified valuable audience segments, they [Activate](../collaborate/activate.md) their chosen audiences for marketing campaigns.

Finally, after executing their campaigns, both brands upload data to [Measure](../collaborate/measure.md) the results and evaluate the effectiveness of their collaboration.

## Advertiser-to-advertising platform workflow {#advertiser-to-advertising-platform-workflow}

[!UICONTROL Luma], an athletic retail company, wants to connect with [!DNL Amazon Marketing Cloud] ([!DNL AMC]) to enhance their marketing capabilities by leveraging [!DNL AMC]&#39;s identity resolution and targeting tools. Luma already has an active [!DNL Amazon Advertising] account and is approved to use [!DNL AMC].

To begin, [!UICONTROL Luma] needs to [create an account](../setup/onboard-account.md) with the advertiser role. After establishing their account, [!UICONTROL Luma] must [create a data connection and source audiences](../setup/onboard-audiences.md). Since [!UICONTROL Luma] will activate audiences for marketing campaigns, they need to [configure a destination](../setup/manage-destinations.md).

Once [!UICONTROL Luma] has their account set up, they&#39;re ready to [form a connection](../connect/establishing-connections.md) with [!DNL AMC] within the platform. [!UICONTROL Luma] uses the [discover collaborators](../connect/discover-collaborators.md) feature to find [!UICONTROL Amazon Marketing Cloud] and [initiate a connection request](../connect/advertising-platforms/amc.md). After authenticating and authorizing the connection through the [!DNL Amazon] sign-in page, the connection with [!DNL AMC] is established.

After the connection is established, [!UICONTROL Luma] [creates a project](../collaborate/manage-projects.md) to kick off their collaboration with [!DNL AMC]. Connection settings, including use cases, are pre-configured depending on the advertising platform. For [!DNL AMC], the available use case is [Discover](../collaborate/advertising-platforms/amc.md#discover).

[!UICONTROL Luma] leverages the [Discover](../collaborate/advertising-platforms/amc.md#discover) use case to gain insights and audience data from [!DNL AMC]. Using these insights, [!UICONTROL Luma] can optimize their marketing strategies and improve campaign effectiveness.

## Advertiser-to-data partner workflow {#advertiser-to-data-partner-workflow}

[!UICONTROL Luma], an athletic retail company, wants to collaborate with [!UICONTROL DataM8], a third-party data provider, to enrich customer profiles and improve audience targeting.

To begin, [!UICONTROL Luma] needs to [create an account](../setup/onboard-account.md) with the advertiser role, while [!UICONTROL DataM8] creates an account with the data partner role.

After establishing their accounts, both [!UICONTROL Luma] and [!UICONTROL DataM8] must [create a data connection and source audiences](../setup/onboard-audiences.md). Both collaborators may activate audiences for marketing campaigns, so they each need to [configure a destination](../setup/manage-destinations.md).

Once both collaborators have their accounts set up, they&#39;re ready to [form a connection](../connect/establishing-connections.md) within the platform. [!UICONTROL Luma] uses the [discover collaborators](../collaborate/discover.md) feature to find [!UICONTROL DataM8] and initiate a connection request. After [!UICONTROL DataM8] accepts the connection request, [!UICONTROL Luma] configures the connection settings to define how they will collaborate. [!UICONTROL DataM8] accepts the connection request to establish a secure link between the two collaborators.

After the connection is established, [!UICONTROL Luma] [creates a project](../collaborate/manage-projects.md) to kick off their collaboration with [!UICONTROL DataM8]. During the project setup, they choose the collaboration use cases that best fit their objectives: [Discover](../collaborate/discover.md), [Activate](../collaborate/activate.md), and [Measure](../collaborate/measure.md).

[!UICONTROL Luma] leverages the [Discover](../collaborate/discover.md) use case to gain insights into [!UICONTROL DataM8]&#39;s audience data. Once [!UICONTROL Luma] has identified the target audience segments, they [activate](../collaborate/activate.md) these audiences.

[!UICONTROL DataM8] can also [activate](../collaborate/activate.md) their audiences to [!UICONTROL Luma]. [!UICONTROL Luma] uses these capabilities to append third-party attributes to its customer profiles and analyze audience composition. With enriched data available directly in its CDP, [!UICONTROL Luma] can build more precise audiences and activate them to paid media destinations without moving data outside its governed environment.

## Agency-to-publisher workflow {#agency-to-publisher-workflow}

[!UICONTROL Agency99], a media agency, wants to collaborate with [!UICONTROL TV Tube], a digital streaming provider, to reach specific audiences through targeted marketing campaigns.

To begin, [!UICONTROL Agency99] needs to [create an account](../setup/onboard-account.md) with the agency role, while [!UICONTROL TV Tube] creates an account with the publisher role.

After establishing their accounts, both [!UICONTROL Agency99] and [!UICONTROL TV Tube] must [create a data connection and source audiences](../setup/onboard-audiences.md). [!UICONTROL Agency99] will set up client sub-accounts and source client data within its workspace. Only [!UICONTROL TV Tube] will activate audiences for marketing campaigns, so they need to [configure a destination](../setup/manage-destinations.md).

Once both collaborators have their accounts set up, they&#39;re ready to [form a connection](../connect/establishing-connections.md) within the platform. [!UICONTROL Agency99] uses the [discover collaborators](../collaborate/discover.md) feature to find [!UICONTROL TV Tube] and initiate a connection request. [!UICONTROL Agency99] will do this for one or multiple clients that want to collaborate with [!UICONTROL TV Tube]. Une fois que [!UICONTROL TV Tube] a accepté la ou les demandes de connexion, [!UICONTROL Agency99] configure les paramètres de connexion pour définir comment chaque collaboration doit se dérouler. [!UICONTROL TV Tube] accepte la ou les demandes de connexion pour établir une liaison sécurisée entre les deux marques.

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
