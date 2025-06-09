---
title: Découvrir les chevauchements et comparer les audiences
description: Découvrez les chevauchements entre vos audiences et celles de vos collaborateurs. Découvrez les meilleures audiences à utiliser dans vos campagnes.
audience: admin, publisher, advertiser
badgelimitedavailability: label="Disponibilité limitée" type="Informative" url="https://helpx.adobe.com/fr/legal/product-descriptions/real-time-customer-data-platform-collaboration.html newtab=true"
exl-id: 38c42ad3-9d01-4d09-b80e-37fb51cbf42b
source-git-commit: f19aff1b7d10a446dd209721e7a6fdf537c9d63e
workflow-type: tm+mt
source-wordcount: '1206'
ht-degree: 11%

---

# Découvrir les chevauchements et comparer les audiences

{{limited-availability-release-note}}

>[!IMPORTANT]
>
>L’espace de travail **[!UICONTROL Discover]** n’est disponible que si le cas d’utilisation **Audience discovery** a été activé [pendant le processus de connexion](../connect/establishing-connections.md#connection-settings). Pour plus d’informations sur les cas d’utilisation, consultez le guide [gestion des projets](./manage-projects.md#project-use-cases).

Après avoir [créé un projet](/help/guide/collaborate/manage-projects.md), vous pouvez comparer vos audiences à vos collaborateurs. Vous pouvez ainsi identifier les audiences pertinentes pour les campagnes et décider lesquelles envoyer aux éditeurs pour activation.

>[!IMPORTANT]
>
>Tous les [esquisses de données](/help/guide/glossary.md#sketches) qui ne sont pas mis à jour ou actualisés seront supprimés après 7 jours. Dans ce cas, les chiffres affichés dans les différents rapports de chevauchement sur cette page sont nuls et le partage d’audience n’est plus disponible pour ces audiences expirées. Les esquisses de données sont automatiquement actualisées pour les audiences avec un [planning d’actualisation actif](/help/guide/setup/onboard-audiences.md#schedule).

Les clés de correspondance utilisées pour découvrir et comparer des audiences sont configurées [pendant le processus de connexion](/help/guide/connect/establishing-connections.md#connection-settings). Les clés de correspondance sont utilisées pour calculer le chevauchement entre vos audiences et peuvent être activées et désactivées. Pour modifier les clés de correspondance, sélectionnez l’option **[!UICONTROL Modifier les clés de correspondance]**. Ce(tte)

![Espace de travail de l’onglet Découverte , présentant les informations sur l’audience.](/help/assets/collaborate/discover/discover-overview.png)

La boîte de dialogue **[!UICONTROL Modifier les clés de correspondance]** s’ouvre et vous pouvez activer/désactiver les clés de correspondance que vous ne souhaitez pas utiliser. Sélectionnez **[!UICONTROL Enregistrer]** pour enregistrer vos modifications.

![Boîte de dialogue Modifier les clés de correspondance dans l’espace de travail Discover.](/help/assets/collaborate/discover/edit-match-keys.png)

## Conditions préalables {#prerequisites}

Pour commencer à utiliser l’onglet **[!UICONTROL Découvrir]** dans votre projet, vous devez disposer des éléments suivants :

* [Audiences importées](/help/guide/setup/onboard-audiences.md) dans votre organisation
* [Connecté](/help/guide/connect/establishing-connections.md) avec un collaborateur avec le cas d’utilisation **découverte d’audience** activé
* [Création d’un projet](/help/guide/collaborate/manage-projects.md) entre vous et un collaborateur

Une fois ces conditions préalables remplies, vous pouvez commencer à explorer et à comparer le chevauchement entre vos audiences et celles de votre collaborateur.

## Comparer des audiences {#compare-audiences}

>[!CONTEXTUALHELP]
>id="rtcdp_collaboration_discover_compare_audiences"
>title="Comparer des audiences"
>abstract="Découvrez les chevauchements entre vos audiences et celles de vos collaborateurs et collaboratrices. Vous pouvez ajuster les paramètres du sélecteur de liste déroulante pour détecter les chevauchements entre une ou plusieurs de vos audiences et une ou plusieurs audiences de vos collaborateurs et collaboratrices."

>[!CONTEXTUALHELP]
>id="rtcdp_collaboration_discover_your_identity_count"
>title="Le nombre de vos identités"
>abstract="Nombre d’identifiants uniques dans l’audience sélectionnée, en fonction des clés de correspondance convenues entre vous et votre collaborateur pour le projet."
>
>[!CONTEXTUALHELP]
>id="rtcdp_collaboration_discover_collaborator_identity_count"
>title="Nombre d’identités du collaborateur ou de la collaboratrice"
>abstract="Nombre d’ID uniques dans l’audience de votre collaborateur, en fonction des clés de correspondance convenues entre vous et votre collaborateur pour le projet."

>[!CONTEXTUALHELP]
>id="rtcdp_collaboration_discover_overlapping_identities_count"
>title="Nombre d’identités qui se chevauchent"
>abstract="Nombre d’identifiants uniques présents dans vos audiences et dans celles de votre collaborateur, en fonction des clés de correspondance convenues entre vous et votre collaborateur pour le projet."

>[!CONTEXTUALHELP]
>id="rtcdp_collaboration_discover_overlapping_identities_percentage"
>title="Pourcentage d’identités qui se chevauchent"
>abstract="Pourcentage d’identités qui se chevauchent entre vous et l’audience sélectionnée de votre collaborateur ou collaboratrice."

Utilisez la section Comparer les audiences pour obtenir de riches informations sur le chevauchement entre vos audiences et celles de votre collaborateur. Pour modifier la sélection de l’audience, utilisez le sélecteur de liste déroulante en haut de la section **[!UICONTROL Comparer les audiences]**. Vous pouvez sélectionner une ou toutes vos audiences et une ou toutes les audiences de votre collaborateur pour les comparer.

![L’espace de travail Discover avec le sélecteur d’audience mis en surbrillance dans la section Comparer les audiences.](/help/assets/collaborate/discover/compare-audiences-selector.png)

Dans la section Comparer les audiences , vous pouvez voir les mesures suivantes, qui sont basées sur les clés de correspondance convenues entre vous et votre collaborateur pour le projet :

| Mesure | Description |
|---------|----------|
| **[!UICONTROL Nombre d’identités]** (vôtre) | Nombre d’identifiants uniques dans votre ou vos audience(s) sélectionnée(s). |
| **[!UICONTROL Nombre d’identités]** (votre collaborateur) | Nombre d’identifiants uniques dans l’audience de votre collaborateur ou de vos collaboratrices. |
| **[!UICONTROL Identités qui se chevauchent]** | Nombre d’identifiants uniques présents dans votre audience et dans celle de votre collaborateur ou collaboratrice. |
| **[!UICONTROL Chevaucher %]** | Pourcentage de profils qui se chevauchent entre votre audience et l’audience sélectionnée de votre collaborateur ou collaboratrice. |
| **[!UICONTROL Répartition des identités par clé de correspondance]** | Répartition des identités pour chaque clé de correspondance choisie dans le projet, en fonction des audiences sélectionnées pour chaque collaborateur. |

{style="table-layout:auto"}

>[!TIP]
>
>Le pourcentage de chevauchement peut ne pas toujours être disponible pour toutes les audiences. La visibilité de l’indicateur de pourcentage de chevauchement dépend du paramètre que votre collaborateur a choisi pour une audience dans la [section de visibilité des métadonnées](/help/guide/setup/onboard-audiences.md#metadata-visibility).

## Audiences pertinentes {#relevant-audiences}

>[!CONTEXTUALHELP]
>id="rtcdp_collaboration_discover_relevant_audiences"
>title="Audiences pertinentes"
>abstract="En fonction des pourcentages de chevauchement, ces audiences d’éditeurs pourraient être adaptées à votre campagne. <br><br> Le <b> nombre d’identités</b> correspond à la taille de l’audience de l’éditeur. <br><br> Les <b>Identités qui se chevauchent</b> représentent le chevauchement entre l’audience recommandée de l’éditeur et toutes les audiences de l’annonceur. <br><br> Le <b>Pourcentage de chevauchement</b> représente le nombre d’identités qui se chevauchent, divisé par la taille de <i>toutes</i> les audiences de l’annonceur."

La section **[!UICONTROL Audiences pertinentes]** de l’onglet **[!UICONTROL Découvrir]** fournit une liste sélectionnée des cinq premières audiences en fonction du pourcentage de chevauchement entre l’audience de votre collaborateur et toutes vos audiences. Cette fonctionnalité vous permet d’identifier rapidement les audiences qui se chevauchent le plus, ce qui vous permet de cibler vos campagnes plus efficacement. Basculez entre les audiences pertinentes à l’aide des sélecteurs de page en haut à droite de la section.

![L’espace de travail Discover avec la section Audiences pertinentes mise en surbrillance.](/help/assets/collaborate/discover/relevant-audiences.png)

>[!NOTE]
>
>La visibilité des audiences de votre collaborateur dépend du paramètre que celui-ci a choisi pour une audience dans la [section visibilité des métadonnées](/help/guide/setup/onboard-audiences.md#metadata-visibility). Si votre collaborateur a défini toutes les audiences sur privées, cette section n’affichera aucune audience.

La section **[!UICONTROL Audiences pertinentes]** affiche les informations suivantes pour chaque audience recommandée :

| Mesure | Description |
|---------|----------|
| **[!UICONTROL Nombre d’identités]** | Le nom des ID uniques dans l’audience. |
| **[!UICONTROL Identités qui se chevauchent]** | Nombre d’identifiants uniques qui se chevauchent entre l’audience recommandée et toutes vos audiences. |
| **[!UICONTROL Chevaucher %]** | Pourcentage d’identités qui se chevauchent entre l’audience recommandée et toutes vos audiences. |
| **[!UICONTROL Catégories d’audience]** | Les catégories que votre collaborateur a affectées à l’audience. |
| **[!UICONTROL Clés de correspondance]** | Les clés de correspondance sélectionnées par votre collaborateur pour l’audience. |

{style="table-layout:auto"}

>[!NOTE]
>
>La visibilité des audiences de votre collaborateur dépend du paramètre que celui-ci a choisi pour une audience dans la [section visibilité des métadonnées](/help/guide/setup/onboard-audiences.md#metadata-visibility). Si votre collaborateur a défini toutes les audiences sur privées, cette section n’affichera aucune audience.

## Chevauchements de découvertes {#discover-overlaps}

>[!CONTEXTUALHELP]
>id="rtcdp_collaboration_discover_overlaps_collaborator_audiences"
>title="Chevauchements de découvertes avec des audiences individuelles"
>abstract="Obtenez des informations sur les chevauchements entre vos audiences et les audiences de votre collaborateur."

Découvrez les chevauchements pour obtenir des informations sur la manière dont vos audiences se comparent aux audiences de vos collaborateurs. Par défaut, cette section compare toutes vos audiences à celles de chacun des collaborateurs. Utilisez le contrôle de pagination au bas de la section pour parcourir les audiences disponibles.

![L’espace de travail Discover avec la section Discover overlaps mise en surbrillance.](/help/assets/collaborate/discover/discover-overlaps.png)

>[!NOTE]
>
>La visibilité des audiences de votre collaborateur dépend du paramètre que celui-ci a choisi pour une audience dans la [section visibilité des métadonnées](/help/guide/setup/onboard-audiences.md#metadata-visibility). Si votre collaborateur a défini toutes les audiences sur privées, cette section n’affichera aucune audience.

Pour modifier votre sélection d’audience, sélectionnez **[!UICONTROL Modifier l’audience]**.

![Découvrir l’espace de travail avec l’option Modifier l’audience mise en surbrillance.](/help/assets/collaborate/discover/change-audience.png)

La boîte de dialogue **[!UICONTROL Modifier l’audience]** s’ouvre et vous pouvez comparer une audience spécifique aux audiences de votre collaborateur ou de votre collaboratrice. Sélectionnez les audiences souhaitées ou effacez vos sélections pour sélectionner toutes les audiences, puis sélectionnez **[!UICONTROL Enregistrer]**.

![Boîte de dialogue Modifier l’audience dans l’espace de travail Découvrir](/help/assets/collaborate/discover/change-audience-selection.png).

Une fois les audiences sélectionnées, la section **[!UICONTROL Découvrir les chevauchements]** affiche les informations suivantes pour chaque audience :

| Mesure | Description |
|---------|----------|
| **[!UICONTROL Nombre d’identités]** | Le nom des ID uniques dans l’audience. |
| **[!UICONTROL Identités qui se chevauchent]** | Nombre d’identifiants uniques qui se chevauchent entre l’audience recommandée et toutes vos audiences. |
| **[!UICONTROL Chevaucher %]** | Pourcentage d’identités qui se chevauchent entre l’audience recommandée et toutes vos audiences. |
| **[!UICONTROL Catégories d’audience]** | Les catégories que votre collaborateur a affectées à l’audience. |
| **[!UICONTROL Clés de correspondance]** | Les clés de correspondance sélectionnées par votre collaborateur pour l’audience. |

{style="table-layout:auto"}

## Étapes suivantes

Après avoir exploré et découvert les audiences souhaitées, il est temps d’[activer](/help/guide/collaborate/activate.md) les audiences qui doivent être utilisées dans les campagnes.
