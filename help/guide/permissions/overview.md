---
title: Présentation du contrôle d’accès
description: Découvrez comment accéder à Adobe Real-Time Customer Data Platform (CDP) Collaboration.
audience: admin
badgelimitedavailability: label="Disponibilité limitée" type="Informative" url="https://helpx.adobe.com/legal/product-descriptions/real-time-customer-data-platform-collaboration.html newtab=true"
exl-id: af48f5ea-8258-42a6-a39e-f4a4ca5b4a69
source-git-commit: 56872a2cd91ae040aba51ed5784c86b055f88756
workflow-type: tm+mt
source-wordcount: '986'
ht-degree: 2%

---

# Présentation du contrôle d’accès

{{limited-availability-release-note}}

>[!IMPORTANT]
>
> Si vous êtes un utilisateur final souhaitant accéder à Real-Time CDP Collaboration, contactez votre administrateur système ou produit pour vérifier l’existence d’un accès. Si vous ne savez pas qui est votre administrateur système, contactez votre représentant ou représentante Adobe.

Le contrôle d’accès pour Real-Time Customer Data Platform (CDP) Collaboration est fourni via Admin Console et les autorisations dans [Adobe Experience Cloud](https://experience.adobe.com/){target="_blank"}. Dans ce guide, vous apprendrez à donner accès à vous-même ou à d’autres membres de votre équipe, en fonction de votre cas d’utilisation.

## Hiérarchie du contrôle d’accès {#hierarchy}

Pour configurer le contrôle d’accès sur Real-Time CDP Collaboration, vous **devez** disposer de droits d’administrateur système ou produit. Un administrateur système n’a aucune restriction et est configuré pendant le processus d’intégration. En attendant, un administrateur produit peut fournir des fonctions administratives pour tous les produits auxquels il a été affecté. Un administrateur de produit doit disposer d’un accès produit et administratif par un administrateur système.

Ces guides décrivent la configuration de l’accès pour les administrateurs système, les administrateurs de produit et les utilisateurs finaux. Reportez-vous au tableau ci-dessous pour comprendre la principale différence entre les rôles.

| Rôle | Description |
| --- | --- | 
| Administrateur système | Super utilisateur ou super utilisatrice de l’organisation. Ils sont en mesure d’effectuer toutes les tâches administratives dans Admin Console et disposent des autorisations pour déléguer des fonctions administratives à d’autres utilisateurs. |
| Administrateur de produit | Administration des produits qui leur sont affectés et de toutes les fonctions administratives associées, telles que l’ajout d’utilisateurs à des organisations, l’ajout ou la suppression d’utilisateurs de profils de produit et l’ajout ou la suppression d’autres administrateurs de produit d’un produit. |
| Utilisateur final | Utilisateurs de votre entreprise qui utilisent les produits. |

{style="table-layout:auto"}

Pour plus d’informations sur les rôles administratifs, consultez le [Centre d’aide Adobe](https://helpx.adobe.com/fr/enterprise/using/admin-roles.html).

>[!TIP]
>
>L’utilisation de la mention **administrateurs** dans ces guides fait référence à **administrateurs système et produits**.

## Produits supplémentaires {#products}

Avant de pouvoir accorder l’accès à Real-Time CDP Collaboration, vous devez accéder à plusieurs produits, selon votre [cas d’utilisation](#use-cases). Les guides de contrôle d’accès peuvent fonctionner avec plusieurs interfaces utilisateur au fur et à mesure que vous avancez, chacune d’elles répondant à un objectif spécifique dans le processus de configuration des accès. Consultez le tableau ci-dessous pour mieux comprendre à quoi chaque produit servira.

| Produit | Utilise |
| --- | --- |
| [Admin Console](https://adminconsole.adobe.com/) | Les administrateurs l’utilisent pour attribuer aux utilisateurs un accès au produit et/ou aux administrateurs. |
| [Autorisations](https://experience.adobe.com/) | Les administrateurs l’utilisent pour affecter des rôles d’administrateurs ou d’utilisateurs finaux. |
| [Experience Platform](https://platform.adobe.com/) | Les administrateurs et les utilisateurs finaux doivent avoir accès au produit Experience Platform pour les affecter à des rôles. |

## Par où commencer {#use-cases}

Maintenant que vous avez une meilleure compréhension des rôles d’utilisateur et d’administration, ainsi que des différents produits Experience Cloud, vous pouvez commencer à donner accès à Real-Time CDP Collaboration. Deux facteurs principaux influencent les mesures que vous devrez prendre :

- si vous affectez un accès administrateur ou utilisateur final
- si les utilisateurs ont déjà accès au produit Experience Platform

Reportez-vous au tableau ci-dessous pour déterminer qui est nécessaire pour configurer les privilèges et par où commencer en fonction de votre cas d’utilisation du contrôle d’accès. **Assurez-vous de suivre le tutoriel jusqu’à la fin du guide à partir de votre point de départ.**

>[!TIP]
>
> Un super utilisateur fait référence au niveau d’accès le plus élevé obtenu par l’administrateur système. Un super utilisateur peut effectuer toutes les tâches administratives et toutes les fonctionnalités utilisateur. Un administrateur système ne dispose pas des fonctionnalités du produit prêtes à l’emploi et doit se donner l’accès approprié, comme indiqué dans le tableau ci-dessous.

| Cas d’utilisation | Rôle requis | Par où commencer |
| --- | --- | --- | 
| Super utilisateur sans accès existant au produit Experience Platform. | Un administrateur système. | [Configuration de l’accès administrateur de produit](./manage-user-access.md#admin-access) |
| Super utilisateur pour un administrateur système Experience Platform existant **avec accès à**’interface utilisateur d’Experience Platform). | administrateur système. | [Configuration de l’accès à la plateforme CDP en temps réel pour la collaboration](./manage-user-access.md#RTCDP-collab-access) |
| Super utilisateur pour un administrateur système Experience Platform existant **sans accès** à l’interface utilisateur d’Experience Platform. | Un administrateur système. | [Configuration de l’accès administrateur de produit](./manage-user-access.md#admin-access) |
| Privilèges d’administrateur de produit et accès à Real-Time CDP Collaboration pour un nouvel administrateur de produit. | administrateur système. | [Configuration de l’accès administrateur du produit](./manage-user-access.md#admin-access) |
| Accès à la collaboration CDP en temps réel pour un administrateur **produit Experience Platform existant disposant** d’un accès Experience Platform à l’interface utilisateur. | Un administrateur système ou de produit. | [Configuration de l’accès à la plateforme CDP en temps réel pour la collaboration](./manage-user-access.md#RTCDP-collab-access) |
| Accès à Real-Time CDP Collaboration pour un administrateur de produit Experience Platform existant **sans accès** à l’interface utilisateur d’Experience Platform. | Un administrateur système ou produit. | [Configurer l’accès utilisateur](./manage-user-access.md#user-access) |
| Accès à Real-Time CDP Collaboration pour un nouvel utilisateur final. | Un administrateur système ou produit. | [Configurer l’accès utilisateur](./manage-user-access.md#user-access) |
| Accès à Real-Time CDP Collaboration pour un utilisateur existant disposant d’un accès à Experience Platform. | Un administrateur système ou produit. | [Configurer l’accès à Real-Time CDP Collaboration](./manage-user-access.md#RTCDP-collab-access) |

{style="table-layout:auto"}

## Autorisations supplémentaires

Une fois que vous avez obtenu l’accès à Real-Time CDP Collaboration, vous pouvez avoir besoin de certaines autorisations Experience Platform supplémentaires pour une fonctionnalité spécifique.

### Importation d’audiences {#audience-importation}

Avant de pouvoir commencer à partager des audiences avec des collaborateurs, vous devez importer des audiences dans Real-Time CDP Collaboration. Actuellement, la seule connexion aux données prise en charge pour l’importation d’audiences est Experience Platform. Pour commencer, la ou les personnes qui gèrent l’intégration de l’audience devront se voir attribuer un rôle contenant les autorisations de ressources **Gestion des profils** suivantes :

| Autorisation | Description |
| ---- | ---- |
| Afficher les segments | Permet à l’utilisateur de voir la liste des audiences disponibles dans un environnement de test. |
| Affichage des profils | Permet à l’utilisateur de voir les champs disponibles pour le mappage aux champs de collaboration. |

Ci-dessous, vous pouvez voir un exemple de rôle avec les autorisations ci-dessus ajoutées. Pour plus d’informations sur la création ou l’attribution [de rôles, reportez-vous au guide de gestion des rôles](./manage-roles.md) .

![Espace de travail des ressources dans Autorisations avec les autorisations Afficher les segments et Afficher les profils ajoutées à la ressource Gestion des profils.](../../assets/permissions/sample-audience-role.png)

>[!NOTE]
>
>Les utilisateurs peuvent travailler avec des audiences dans Real-Time CDP Collaboration après les avoir importés sans l’une des autorisations ci-dessus.

## Étapes suivantes

Une fois que vous avez déterminé par où commencer, suivez le lien de votre cas d’utilisation pour commencer à configurer l’accès. Si vous souhaitez en savoir plus sur la configuration de l’accès à Real-Time CDP Collaboration en tant qu’administrateur au-delà de ces cas d’utilisation, reportez-vous au guide [gérer l’accès utilisateur](manage-user-access.md). Pour en savoir plus sur les rôles et leur rôle dans la configuration de l’accès aux différents composants de Real-Time CDP Collaboration, reportez-vous au guide [gérer les rôles](manage-roles.md).
