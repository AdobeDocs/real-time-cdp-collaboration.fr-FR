---
title: Présentation des audiences
description: Découvrez les audiences dans Real-Time CDP Collaboration, y compris leur emplacement d’origine.
audience: admin, publisher
badgelimitedavailability: label="Disponibilité limitée" type="Informative" url="https://helpx.adobe.com/legal/product-descriptions/real-time-customer-data-platform-collaboration.html newtab=true"
product_v2:
  - id: fdddec33-c9cb-4459-b8b6-2664395a6f10
topic_v2:
  - id: b5520579-b31f-4df7-9281-f0d9f91e2edc
  - id: e1e0219c-f879-479f-8427-888ed2a6e9c2
source-git-commit: 160bd29d89d1ce828476d68e917e0271d0852eb6
workflow-type: tm+mt
source-wordcount: 707
ht-degree: 3%

---

# Présentation des audiences

{{limited-availability-release-note}}

Dans Adobe Real-Time CDP Collaboration, les audiences sont des groupes d’utilisateurs ou de clients que vous importez dans Collaboration. Après le sourcing, vous pouvez utiliser les audiences pour découvrir le chevauchement avec les collaborateurs, activer les audiences et mesurer les performances de la campagne. Vous pouvez approvisionner les audiences à partir de différents types de sources, notamment Adobe Experience Platform, les systèmes de stockage et de partage dans le cloud, ainsi que les workflows de chargement de fichiers, en fonction de l’emplacement de stockage de vos données d’audience.

## Utilisation des audiences {#audiences-in-collaboration}

Une fois qu’une audience est sourcée dans Collaboration, elle peut être utilisée dans les workflows de collaboration pris en charge.

Utilisez les audiences dans Collaboration pour :

* Comparer votre audience aux audiences de collaborateurs
* Identification des chevauchements et des opportunités
* Activer les audiences
* Mesurer les résultats et les performances de la campagne
* Gérer la visibilité de l’audience et les paramètres associés

## Intégration des audiences dans Collaboration {#conceptual-diagram}

>[!NOTE]
>
> Le diagramme suivant fournit une vue d’ensemble de la manière dont les audiences sources s’intègrent dans Collaboration et sont utilisées dans les projets.

```text
Source → Data connection → Audience → Project
                                         │
                          ┌──────────────┼──────────────┐
                          ▼              ▼              ▼
                      Discover       Activate       Measure
                                         │
                                         ▼
                                    Destination
```

## Concepts de base {#core-concepts}

Les concepts suivants décrivent les objets clés impliqués dans l’approvisionnement des audiences et les workflows de collaboration.

**Source**\
Système ou emplacement d’origine des données de l’audience, tel que Adobe Experience Platform, un emplacement d’espace de stockage dans le cloud ou un téléchargement de fichier.

**Connexion aux données**\
Connexion configurée que Collaboration utilise pour accéder aux données d’audience à partir d’une source. Une connexion aux données comprend des détails de configuration spécifiques à la source tels que l’authentification, le mappage des champs et la planification.

**Audience**\
Groupe d’utilisateurs ou de clients qui a été sourcé dans Collaboration et qui est disponible pour une utilisation dans des projets.

**Connexion**\
La relation de collaboration entre votre organisation et une autre organisation.

**Projet**\
Espace de travail dans lequel les collaborateurs utilisent les audiences ensemble pour les cas d’utilisation pris en charge, tels que la découverte, l’activation et la mesure.

**Destination**\
Plateforme ou système externe sur lequel les audiences activées sont envoyées.

**Clés correspondantes**
Identifiants utilisés par Collaboration pour faire correspondre les enregistrements dans les jeux de données et les collaborateurs. Les clés de correspondance prennent en charge des workflows tels que le chevauchement, l’activation et la mesure des audiences.

## Cycle de vie de l’audience {#audience-lifecycle}

Dans Collaboration, vous approvisionnez les audiences par le biais de connexions de données, les gérez dans **[!UICONTROL Configuration]** et les utilisez dans des projets pour les cas d’utilisation pris en charge.

1. **Audiences Source** : importez les données d’audience dans Collaboration par le biais d’une connexion aux données.
2. **Gérer les audiences** : vérifiez et gérez les détails de l’audience, la visibilité et les paramètres associés.
3. **Utiliser des audiences dans les projets** : utilisez des audiences sources dans les projets pour les cas d’utilisation pris en charge, y compris **Découvrir**, **Activer** et **Mesurer**.

Toutes les audiences ne sont pas utilisées dans tous les cas d’utilisation. Par exemple, une audience peut être sourcée et utilisée pour **Discover** sans être activée, ou elle peut être utilisée dans des workflows **Measure** sans être envoyée à une destination.

Pour plus d’informations sur l’approvisionnement et la gestion des audiences, voir [Source et gérer les audiences](./onboard-audiences.md). Pour plus d’informations sur la gestion des connexions de données, voir [Gestion des connexions de données](./manage-data-connection.md).

## D’où proviennent les audiences {#supported-sources}

Collaboration prend en charge plusieurs types de sources d’audience. La source que vous choisissez détermine le flux de configuration, les conditions préalables, les exigences d’authentification, le format de données, le mappage des champs, le comportement d’actualisation et les options de configuration disponibles pour importer les audiences dans Collaboration.

* Adobe Experience Platform
* Stockage dans le cloud, y compris Amazon S3, Google Cloud Storage et le stockage Azure
* Services de partage de données, y compris Snowflake et Databricks Delta Share
* Adobe Audience Manager
* Chargement du fichier CSV

Pour obtenir la liste des sources prises en charge et des étapes de configuration spécifiques à une source, voir [Présentation des sources](./source-overview.md#available-sources).

## En quoi consistent les audiences ? {#match-keys}

Dans RTCDP Collaboration, les audiences sont composées de clés de correspondance. Selon la configuration de votre compte, les clés de correspondance prises en charge peuvent inclure **ID de personne**, **ID d’appareil** et **ID de partenaire**. Les clés de correspondance prennent en charge des workflows tels que **chevauchement des audiences**, **activation** et **mesure**.

Pour en savoir plus, consultez [Configuration des clés de correspondance](../setup/onboard-account.md#set-up-match-keys) et [Gestion des connexions de données](../setup/manage-data-connection.md#match-keys)

## Utilisation des audiences dans les projets {#audiences-in-projects}

Les projets fournissent le contexte nécessaire à la collaboration avec une autre organisation. Dans un projet, vous pouvez utiliser des audiences pour les cas d’utilisation de collaboration pris en charge :

* **Découvrir** : comparez les audiences et examinez les informations de chevauchement. Voir [Découvrir le chevauchement des audiences](../collaborate/discover.md).
* **Activer** : activez les audiences sélectionnées pour une utilisation de campagne. L’activation est lancée à partir de l’onglet [!UICONTROL &#x200B; Activer &#x200B;] dans l’espace de travail du projet et envoie des audiences vers la destination configurée de la connexion. Voir [&#x200B; Activer les audiences](../collaborate/activate.md).
* **Mesure** : consultez les rapports de conversion et de diffusion de la campagne associés au projet. Voir [Mesure des performances](../collaborate/measure.md).

Pour plus d’informations sur la création et la gestion de projets, voir [Créer et gérer des projets](../collaborate/manage-projects.md). Pour plus d’informations sur la configuration des destinations, voir [Présentation des destinations](../destinations/overview.md).

## Étapes suivantes {#next-steps}

* [Vérifier les sources d’audience disponibles](./source-overview.md)
* [Source et gestion des audiences](./onboard-audiences.md)
* [Créer et gérer des projets](../collaborate/manage-projects.md)
* [Découvrir le chevauchement des audiences](../collaborate/discover.md)
* [Activer les audiences](../collaborate/activate.md)
* [Mesurer les performances](../collaborate/measure.md)
* [Présentation des destinations](../destinations/overview.md)
