---
title: Vue d’ensemble des connexions
description: Découvrez les connexions dans Real-Time CDP Collaboration.
audience: publisher, advertiser
badgelimitedavailability: label="Disponibilité limitée" type="Informative" url="https://helpx.adobe.com/legal/product-descriptions/real-time-customer-data-platform-collaboration.html newtab=true"
source-git-commit: 5c08738cdc8e1e208203ee1f9a1cf1891b5b07cb
workflow-type: tm+mt
source-wordcount: '754'
ht-degree: 0%

---

# Vue d’ensemble des connexions

{{limited-availability-release-note}}

Avant de pouvoir travailler ensemble sur des campagnes, les collaborateurs doivent établir une connexion. Cette connexion leur permet d’activer des audiences, de créer des projets et d’exécuter des rapports sur les performances des campagnes.

Les connexions sont établies en fonction du modèle de collaboration de votre choix. Collaboration prend en charge trois modèles de collaboration principaux : annonceur-à-éditeur, marque-à-marque et annonceur-à-plateforme-publicitaire. Pour en savoir plus sur ces modèles, consultez le guide [modèles de collaboration](/help/guide/overview/collaboration-patterns.md).

Pour savoir comment établir une connexion, lisez la section ci-dessous qui correspond à votre modèle de collaboration :

- [Connexion publicitaire à éditeur](#advertiser-to-publisher-connection)
- [Connexion de marque à marque](#brand-to-brand-connection)
- [Connexion publicitaire à plateforme publicitaire](#advertiser-to-advertising-platform-connection)

## Connexion publicitaire à éditeur {#advertiser-to-publisher-connection}

![Diagramme de haut niveau du processus de connexion publicitaire-éditeur.](/help/assets/connect/establish-connection/advertiser-publisher-flow.png){zoomable="yes"}

Dans le modèle d’annonceur à éditeur, un annonceur découvre un éditeur avec lequel il souhaite travailler via l’espace de travail **[!UICONTROL Découvrir les éditeurs]** et envoie une invitation à la connexion. L’éditeur examine ensuite l’invitation et l’accepte, ce qui lui permet de proposer des paramètres de connexion. Une fois que l’éditeur accepte les paramètres de connexion, la connexion est établie et les deux collaborateurs peuvent commencer à travailler ensemble sur des projets.

### Présentation générale

Pour établir une connexion entre un annonceur et un éditeur, les étapes suivantes sont impliquées :

1. [Découvrir les éditeurs](./discover-collaborators.md) : l’annonceur identifie les éditeurs potentiels avec lesquels collaborer.
2. [Envoyer une invitation](./establishing-connections.md#send-invite) : l’annonceur envoie une invitation à la connexion à l’éditeur sélectionné.
3. [Accepter l’invitation](./establishing-connections.md#accept-invite) : l’éditeur examine et accepte l’invitation.
4. [Configurer les paramètres de connexion](./establishing-connections.md#configure-connection-settings) : l’annonceur configure les paramètres de connexion et les envoie à l’éditeur pour révision.
5. [Confirmer les paramètres de connexion](./establishing-connections.md#review-connection-settings) : l’éditeur vérifie les paramètres de connexion et les accepte ou les rejette. Si elle est acceptée, la connexion est établie. En cas de rejet, l’éditeur peut fournir des commentaires pour les révisions en dehors du produit. L’annonceur peut alors réviser les paramètres et les renvoyer pour révision.

Une fois les paramètres de connexion acceptés, la connexion est établie et les collaborateurs sont prêts à [créer un projet](/help/guide/collaborate/manage-projects.md#create-project) pour commencer à collaborer sur des campagnes.

## Connexion de marque à marque {#brand-to-brand-connection}

![Diagramme de haut niveau du processus de connexion de marque à marque.](/help/assets/connect/establish-connection/brand-to-brand-flow.png){zoomable="yes"}

>[!TIP]
>
>Le terme **marque** est utilisé pour désigner une société ou une marque en dehors de Collaboration. Le terme **collaborateur** fait référence à tout compte pouvant former une connexion dans Collaboration, qu’il s’agisse d’un annonceur ou d’un éditeur.

Dans le modèle de marque à marque, deux marques qui ont communiqué en dehors du produit peuvent se connecter directement dans Collaboration à l’aide d’une [&#x200B; invitation à une connexion privée &#x200B;](#private-connection-invite). Une marque peut être soit un annonceur, soit un éditeur. Ce modèle est particulièrement utile pour les marques qui peuvent ne pas correspondre au modèle publicitaire-éditeur traditionnel, telles que deux annonceurs ou deux éditeurs.

Pour commencer, un collaborateur envoie une invitation à une connexion privée à un autre collaborateur. Le destinataire examine l’invitation et l’accepte, ce qui permet au propriétaire de proposer des paramètres de connexion. Une fois que le destinataire accepte les paramètres de connexion, la connexion est établie et les deux collaborateurs peuvent commencer à travailler ensemble sur des projets.

### Présentation générale

>[!TIP]
>
>Lors de la discussion du processus de connexion, il y aura une distinction entre le **propriétaire** et le **destinataire**. Le propriétaire est le collaborateur qui lance la connexion en envoyant l’invitation, tandis que le destinataire est le collaborateur qui reçoit et révise l’invitation.

Le processus de connexion entre deux marques implique plusieurs étapes. Avant que le processus de connexion ne commence, certaines conditions préalables doivent être remplies :

1. Deux marques communiquent en dehors du produit pour discuter de la connexion potentielle.
1. Les marques [créer des comptes](/help/guide/setup/onboard-account.md) dans Collaboration si ce n’est pas déjà fait, en veillant à sélectionner le type de rôle approprié (annonceur ou éditeur).

Une fois les conditions préalables remplies, le processus de connexion peut commencer. Les étapes suivantes décrivent le processus :

1. [Envoyer une invitation à une connexion privée](./establishing-connections.md#private-connection-invite) : un collaborateur envoie une invitation à une connexion privée à un autre collaborateur.
2. [Accepter l’invitation à une connexion privée](./establishing-connections.md#accept-invite) : le destinataire vérifie et accepte l’invitation à la connexion privée.
3. [Configurer les paramètres de connexion](./establishing-connections.md#configure-connection-settings) : le propriétaire configure les paramètres de connexion et les envoie au destinataire pour révision et acceptation.
4. [Confirmer les paramètres de connexion](./establishing-connections.md#review-connection-settings) : le destinataire vérifie les paramètres de connexion et les accepte ou les rejette.

Une fois les paramètres de connexion acceptés, la connexion est établie et les collaborateurs sont prêts à [créer un projet](/help/guide/collaborate/manage-projects.md#create-project) pour commencer à collaborer sur des campagnes.

## Connexion publicitaire à plateforme publicitaire {#advertiser-to-advertising-platform-connection}

Le processus de connexion d’annonceur à plateforme publicitaire permet aux annonceurs de se connecter à des plateformes publicitaires tierces, telles qu’Amazon Marketing Cloud (AMC), afin d’améliorer leurs fonctionnalités marketing.

### Présentation générale

Le processus de connexion entre un annonceur et une plateforme publicitaire comporte plusieurs étapes. Avant de commencer le processus de connexion, vérifiez que vous disposez d’un compte actif sur la plateforme publicitaire et que vous êtes autorisé à utiliser ses services. Les étapes suivantes décrivent le processus de connexion :

1. [Découvrir les plateformes publicitaires](./discover-collaborators.md) : l’annonceur identifie les plateformes publicitaires potentielles avec lesquelles collaborer.
2. [Se connecter à une plateforme publicitaire](./advertising-platforms/overview.md#advertising-platforms-overview) : l’annonceur lance le processus de connexion en sélectionnant la plateforme publicitaire avec laquelle il souhaite se connecter et suit les invites pour authentifier et autoriser la connexion.
