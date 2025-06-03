---
title: Glossaire
description: Comprendre la terminologie clé de Real-Time CDP Collaboration
audience: admin, publisher, advertiser
badgelimitedavailability: label="Disponibilité limitée" type="Informative" url="https://helpx.adobe.com/legal/product-descriptions/real-time-customer-data-platform-collaboration.html newtab=true"
exl-id: 870c45d0-df68-487f-bbe2-d9862a8ea62e
source-git-commit: dd1386f9371cb40285315d11e07b139d3115e147
workflow-type: tm+mt
source-wordcount: '815'
ht-degree: 3%

---

# Glossaire

{{limited-availability-release-note}}

Ce glossaire fournit des définitions des termes clés identifiés dans la documentation et les produits Adobe Real-Time CDP Collaboration. La compréhension de ces termes vous aidera à mieux utiliser le produit et ses fonctionnalités.

## A

### Société d’annonceurs

Toute entité qui dépensera un budget marketing pour atteindre les audiences des éditeurs ou d’autres partenaires de marque afin d’atteindre les objectifs de sensibilisation à la marque, de prospection, de réengagement et de conversions.

## C

### Stockage cloud

Le stockage dans le cloud est une solution de cloud computing qui permet de stocker des données et des fichiers sur Internet par le biais d’un fournisseur de cloud computing. Il fait presque toujours partie de la pile de données d’une organisation. Il s’agit par exemple de Amazon Web Services (AWS), Microsoft Azure et Google Cloud Platform (GCP).

### Demande de connexion

Une demande de connexion est une demande formelle envoyée d’une organisation à une autre pour établir une connexion de partage de données. Une fois acceptée, elle permet aux deux parties de collaborer et de partager des données d’audience en toute sécurité.

### Paramètres de connexion

Une fois qu&#39;une demande de connexion est acceptée, l&#39;initiateur de cette demande envoie les paramètres de connexion au collaborateur pour approbation. Ces paramètres de connexion régissent la façon dont les collaborateurs travaillent ensemble sur les projets et incluent les clés de correspondance à utiliser, la propriété de la facturation, etc.

<!--

### Crosswalk

An identity crosswalk is a tool used to connect different identifiers across datasets to enrich your audience data with additional attributes or dimensions. It creates a bridge between different data points, allowing for a more comprehensive and cohesive view of the data.

-->

## D

### Salle de nettoyage des données

Un environnement de collaboration sécurisé qui permet à deux participants ou plus d&#39;exploiter des ressources de données pour des utilisations spécifiques convenues mutuellement, tout en garantissant l&#39;application de limites strictes d&#39;accès aux données. Cette couche d’infrastructure est souvent fournie par les fournisseurs de stockage dans le cloud et/ou par des entrepôts de données tels que Snowflake et Databricks. Elle est mieux adaptée aux utilisateurs techniques tels que les ingénieurs de données et les spécialistes des données maîtrisant des compétences telles que SQL.

### Collaboration de données

La collaboration en matière de données implique de combiner et d’analyser des données au sein d’une entreprise ou avec des partenaires à diverses fins, telles que le ciblage des audiences, la mesure et les informations. Les plateformes de collaboration de données offrent des environnements sécurisés pour partager des données en toute sécurité tout en respectant la confidentialité et la sécurité.

### Connexion de données

Une connexion aux données est la source à partir de laquelle vous pouvez importer des données dans Real-Time CDP Collaboration. Actuellement, Experience Platform est la seule connexion de données disponible. En savoir plus sur la [gestion des connexions de données](/help/guide/setup/manage-data-connection.md).

### Accord de partage de données

Un accord de partage de données est un contrat formel entre deux parties ou plus définissant les termes et conditions du partage de données. Il garantit que toutes les parties se conforment aux exigences légales et de confidentialité et établit des directives pour l’utilisation et la protection des données.

### Identifiant de l’appareil

Un identifiant d’appareil est un numéro unique associé à un appareil, tel qu’un smartphone ou une tablette. Il est utilisé pour suivre et identifier l’appareil sur différentes plateformes et services, ce qui permet d’offrir des expériences utilisateur personnalisées et de la publicité ciblée.

## I

### Inviter

Une invitation dans Adobe Real-Time CDP Collaboration fait référence à une demande envoyée à un autre utilisateur ou à une autre organisation pour rejoindre un projet ou un effort de collaboration sur les données. Le service invite à faciliter un accès sécurisé et contrôlé aux données et ressources partagées.

<!--

## J

### Join key

In the context of identity crosswalks, a join key is a unique identifier used to match and link different identifiers across datasets, enabling the integration and unification of audience data from various sources. For example, a hashed email (HEM) can be a join key.

-->

## M

### Clés correspondantes

Les clés de correspondance sont des identifiants uniques utilisés pour lier des enregistrements dans différents jeux de données. Elles permettent de s’assurer que les données provenant de différentes sources peuvent être correctement appariées et intégrées, ce qui facilite une meilleure analyse des données et une segmentation de l’audience.

## O

### Chevaucher

Un chevauchement (ou chevauchement d’audience) fait référence aux segments d’audience communs qui existent entre différents jeux de données. Comprendre le chevauchement des audiences permet d’identifier les opportunités de collaboration potentielles et de cibler les efforts marketing en exploitant les données d’audience partagées.

## P

### Projet

Un projet dans Adobe Real-Time CDP Collaboration est un espace de travail dans lequel les utilisateurs peuvent collaborer sur des tâches spécifiques d’intégration de données et de segmentation d’audience. Les projets aident à organiser et à gérer les efforts de partage de données, rendant la collaboration plus efficace et rationalisée.

### Public audience

Dans le contexte des projets, il s’agit d’une audience que votre collaborateur peut découvrir. Les audiences peuvent être privées, personnalisées ou publiques. Les audiences privées ne sont détectables par aucun autre collaborateur. Les audiences personnalisées ne peuvent être découvertes que par certains collaborateurs, et les audiences publiques peuvent être découvertes par tous les collaborateurs.

### Éditeur ou éditrice

Un éditeur est propriétaire ou exploitant de contenu ou de services en ligne où des données personnelles sont collectées avec consentement et sont disponibles pour être utilisées par d&#39;autres entités pour la publicité numérique et la mesure d&#39;audience.

## S

### Esquisses {#sketches}

Les esquisses (ou esquisses de données) sont des résumés simplifiés des données d’audience utilisées dans Real-Time CDP Collaboration. Ils permettent aux marques et aux éditeurs d’analyser les chevauchements d’audiences et les informations sans partager les données réelles des clients. Considérez-les comme des effectifs anonymes plutôt que comme des profils clients détaillés.
Dans Adobe Real-Time CDP Collaboration, les schémas de données :

* Aidez à déterminer à quel point deux audiences sont similaires
* Préserver la confidentialité tout en permettant la collaboration
* Doit être actualisé au moins tous les 7 jours pour rester valide

Si les esquisses ne sont pas actualisées régulièrement, les rapports de chevauchement d’audience n’afficheront aucune valeur et le partage d’audience peut devenir temporairement indisponible. Les esquisses de données sont automatiquement actualisées chaque fois que l’appartenance à une audience est mise à jour dans Real-Time CDP Collaboration.

## U

### Cas d’utilisation

Un cas d’utilisation définit un scénario ou un problème d’entreprise spécifique qui peut être résolu à l’aide d’Adobe Real-Time CDP Collaboration. Dans Real-Time CDP Collaboration, des exemples de cas d’utilisation, tels que la découverte d’audience ou la mesure de campagne, sont disponibles pour vous aider à atteindre un objectif particulier.
