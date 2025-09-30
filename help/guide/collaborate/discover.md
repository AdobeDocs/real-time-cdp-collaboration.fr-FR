---
title: Découvrir les chevauchements et comparer les audiences
description: Découvrez les chevauchements entre vos audiences et celles de vos collaborateurs. Découvrez les meilleures audiences à utiliser dans vos campagnes.
audience: admin, publisher, advertiser
badgelimitedavailability: label="Disponibilité limitée" type="Informative" url="https://helpx.adobe.com/fr/legal/product-descriptions/real-time-customer-data-platform-collaboration.html newtab=true"
exl-id: 38c42ad3-9d01-4d09-b80e-37fb51cbf42b
source-git-commit: 3dd37dff0be104894cdfe42503b60056b25018e3
workflow-type: tm+mt
source-wordcount: '2069'
ht-degree: 17%

---

# Découvrir les chevauchements et comparer les audiences

{{limited-availability-release-note}}

>[!IMPORTANT]
>
>L’espace de travail **[!UICONTROL Discover]** n’est disponible que si le cas d’utilisation **Audience discovery** a été activé [pendant le processus de connexion](../connect/establishing-connections.md#connection-settings). Pour plus d’informations sur les cas d’utilisation, consultez le guide [gestion des projets](./manage-projects.md#project-use-cases).

Après avoir [créé un projet](/help/guide/collaborate/manage-projects.md), vous pouvez comparer vos audiences à vos collaborateurs. Vous pouvez ainsi identifier les audiences pertinentes pour les campagnes et décider lesquelles envoyer aux collaborateurs pour activation.

>[!IMPORTANT]
>
>Tous les [esquisses de données](/help/guide/glossary.md#sketches) qui ne sont pas mis à jour ou actualisés seront supprimés après 7 jours. Dans ce cas, les chiffres affichés dans les différents rapports de chevauchement sur cette page sont nuls et le partage d’audience n’est plus disponible pour ces audiences expirées. Les esquisses de données sont automatiquement actualisées pour les audiences avec un [planning d’actualisation actif](/help/guide/setup/onboard-audiences.md#schedule).

Les clés de correspondance utilisées pour découvrir et comparer des audiences sont configurées [pendant le processus de connexion](/help/guide/connect/establishing-connections.md#connection-settings). Les clés de correspondance sont utilisées pour calculer le chevauchement entre vos audiences. Elles peuvent être activées et désactivées. Pour modifier les clés de correspondance, sélectionnez l’option **[!UICONTROL Modifier les clés de correspondance]**.

![Espace de travail de l’onglet Découverte , présentant les informations sur l’audience.](/help/assets/collaborate/discover/discover-overview.png)

La boîte de dialogue **[!UICONTROL Modifier les clés de correspondance]** s’ouvre et vous pouvez activer/désactiver les clés de correspondance que vous ne souhaitez pas utiliser. Sélectionnez **[!UICONTROL Enregistrer]** pour enregistrer vos modifications.

![Boîte de dialogue Modifier les clés de correspondance dans l’espace de travail Discover.](/help/assets/collaborate/discover/edit-match-keys.png)

## Conditions préalables {#prerequisites}

Pour commencer à utiliser l’onglet **[!UICONTROL Découvrir]** dans votre projet, vous devez disposer des éléments suivants :

* [Audiences sources](/help/guide/setup/onboard-audiences.md) dans votre compte
* [Connecté](/help/guide/connect/establishing-connections.md) avec un collaborateur avec le cas d’utilisation **découverte d’audience** activé
* [Création d’un projet](/help/guide/collaborate/manage-projects.md) entre vous et un collaborateur

Une fois ces conditions préalables remplies, vous pouvez commencer à explorer et à comparer les chevauchements entre vous et les audiences de votre collaborateur.

## Comparer des audiences {#compare-audiences}

>[!CONTEXTUALHELP]
>id="rtcdp_collaboration_discover_compare_audiences"
>title="Comparer des audiences"
>abstract="Découvrez les chevauchements entre vos audiences et celles de vos collaborateurs et collaboratrices. Vous pouvez ajuster les paramètres du sélecteur de liste déroulante pour détecter les chevauchements entre une ou plusieurs de vos audiences et une ou plusieurs audiences de vos collaborateurs et collaboratrices."

>[!CONTEXTUALHELP]
>id="rtcdp_collaboration_discover_your_identity_count"
>title="Le nombre de vos identités"
>abstract="Nombre d’identifiants uniques dans l’audience sélectionnée, en fonction des clés de correspondance convenues entre vous et votre collaborateur ou collaboratrice pour le projet."

>[!CONTEXTUALHELP]
>id="rtcdp_collaboration_discover_collaborator_identity_count"
>title="Nombre d’identités du collaborateur ou de la collaboratrice"
>abstract="Nombre d’identifiants uniques dans l’audience de votre collaborateur ou collaboratrice, en fonction des clés de correspondance convenues entre vous et votre collaborateur ou collaboratrice pour le projet."

>[!CONTEXTUALHELP]
>id="rtcdp_collaboration_discover_overlapping_identities_count"
>title="Nombre d’identités qui se chevauchent."
>abstract="Nombre d’identifiants uniques présents dans vos audiences et dans celles de votre collaborateur ou collaboratrice, en fonction des clés de correspondance convenues entre vous et votre collaborateur ou collaboratrice pour le projet."

>[!CONTEXTUALHELP]
>id="rtcdp_collaboration_discover_overlapping_identities_percentage"
>title="Pourcentage d’identités qui se chevauchent."
>abstract="Pourcentage des identités qui se chevauchent entre votre audience et l’audience sélectionnée de votre collaborateur ou collaboratrice."

Utilisez la section Comparer les audiences pour obtenir de riches informations sur le chevauchement entre vos audiences et celles de votre collaborateur. Pour modifier la sélection de l’audience, utilisez le sélecteur de liste déroulante en haut de la section **[!UICONTROL Comparer les audiences]**. Vous pouvez sélectionner une ou toutes vos audiences et une ou toutes les audiences de votre collaborateur pour les comparer.

![L’espace de travail Discover avec le sélecteur d’audience mis en surbrillance dans la section Comparer les audiences.](/help/assets/collaborate/discover/compare-audiences-selector.png)

Dans la section Comparer les audiences , vous pouvez voir les mesures suivantes, qui sont basées sur les clés de correspondance convenues entre vous et votre collaborateur pour le projet :

| Mesure | Description |
|---------|----------|
| **[!UICONTROL Nombre d’identités]** (vôtre) | Nombre d’identifiants uniques dans votre ou vos audience(s) sélectionnée(s). |
| **[!UICONTROL Nombre d’identités]** (votre collaborateur) | Nombre d’identifiants uniques dans l’audience de votre collaborateur ou de vos collaboratrices. |
| **[!UICONTROL Identités qui se chevauchent]** | Nombre d’identifiants uniques présents dans votre audience et dans celle de votre collaborateur ou collaboratrice. |
| **[!UICONTROL Chevaucher %]** | Pourcentage de profils qui se chevauchent entre votre audience et l’audience sélectionnée de votre collaborateur ou collaboratrice. |
| **[!UICONTROL Index d’audience]** | Un score qui indique l’importance de la relation d’une audience avec une autre en fonction du nombre d’audiences sous-jacentes et des chevauchements. Pour en savoir plus sur la signification des scores, lisez la section [score de l’index d’audience](#audience-index-score). Les scores de l’index d’audience ne sont pas disponibles lors de la comparaison avec la ligne de base de votre collaborateur (toutes les audiences). |
| **[!UICONTROL Répartition des identités par clé de correspondance]** | Répartition des identités correspondantes pour chaque clé de correspondance choisie dans le projet, en fonction des audiences sélectionnées pour chaque collaborateur. |

{style="table-layout:auto"}

>[!NOTE]
>
>Le pourcentage de chevauchement et le score de l’index d’audience peuvent ne pas toujours être disponibles pour toutes les audiences. La visibilité du pourcentage de chevauchement et du score de l’index d’audience dépend du paramètre que votre collaborateur a choisi pour une audience dans la [section de visibilité des métadonnées](/help/guide/setup/onboard-audiences.md#metadata-visibility).

Si votre collaborateur n’a activé ni l’index d’audience ni le pourcentage de chevauchement, l’audience ne dispose d’aucune donnée de comparaison.

## Audiences pertinentes {#relevant-audiences}

>[!CONTEXTUALHELP]
>id="rtcdp_collaboration_discover_relevant_audiences"
>title="Audiences pertinentes"
>abstract="En fonction des pourcentages de chevauchement, ces audiences pourraient être adaptées à votre campagne. <br><br> Le <b>nombre d’identités</b> correspond à la taille de l’audience du collaborateur ou de la collaboratrice. <br><br> Les <b>Identités qui se chevauchent</b> représentent le chevauchement entre l’audience recommandée et toutes vos audiences. <br><br> Le <b>% de chevauchement</b> représente le nombre d’identités qui se chevauchent, divisé par la taille de <i>toutes</i> vos audiences."

La section **[!UICONTROL Audiences pertinentes]** de l’onglet **[!UICONTROL Découvrir]** fournit une liste sélectionnée des cinq premières audiences en fonction du pourcentage de chevauchement entre l’audience de votre collaborateur et toutes vos audiences. Cette fonctionnalité vous permet d’identifier rapidement les audiences qui se chevauchent le plus, ce qui vous permet de cibler vos campagnes plus efficacement. Basculez entre les audiences pertinentes à l’aide des sélecteurs de page en haut à droite de la section.

![L’espace de travail Discover avec la section Audiences pertinentes mise en surbrillance.](/help/assets/collaborate/discover/relevant-audiences.png)

>[!NOTE]
>
>La visibilité des audiences de votre collaborateur dépend du paramètre que celui-ci a choisi pour une audience dans la [section d’accès à la connexion](/help/guide/setup/onboard-audiences.md#connection-access) et la [section de visibilité des métadonnées](/help/guide/setup/onboard-audiences.md#metadata-visibility). Si votre collaborateur a défini toutes les audiences sur privées, cette section n’affichera aucune audience.

La section **[!UICONTROL Audiences pertinentes]** affiche les informations suivantes pour chaque audience recommandée :

| Mesure | Description |
|---------|----------|
| **[!UICONTROL Nombre d’identités]** | Nombre d’identifiants uniques dans l’audience. |
| **[!UICONTROL Identités qui se chevauchent]** | Nombre d’identifiants uniques qui se chevauchent entre l’audience recommandée et toutes vos audiences. |
| **[!UICONTROL Chevaucher %]** | Pourcentage d’identités qui se chevauchent entre l’audience recommandée et toutes vos audiences. |
| **[!UICONTROL Index d’audience]** | Un score qui indique l’importance de la relation d’une audience avec une autre en fonction du nombre d’audiences sous-jacentes et des chevauchements. Pour en savoir plus sur la signification des scores, lisez la section [score de l’index d’audience](#audience-index-score). |
| **[!UICONTROL Catégories d’audience]** | Les catégories que votre collaborateur a affectées à l’audience. |
| **[!UICONTROL Clés de correspondance]** | Les clés de correspondance sélectionnées par votre collaborateur pour l’audience. |

{style="table-layout:auto"}

Si la note de l’index d’audience est activée pour l’une des audiences de votre collaborateur, les audiences pertinentes seront basées sur la note de l’index d’audience, et toutes les audiences pour lesquelles l’index d’audience n’a pas été activé ne seront pas incluses. Les audiences pertinentes en fonction du score d&#39;indice d&#39;audience sont triées de sorte que le score d&#39;indice le plus élevé soit affiché en premier. Si l’index d’audience n’est activé pour aucune des audiences de votre collaborateur, les audiences pertinentes seront basées sur le pourcentage de chevauchement.

## Chevauchements de découvertes {#discover-overlaps}

>[!CONTEXTUALHELP]
>id="rtcdp_collaboration_discover_overlaps_collaborator_audiences"
>title="Chevauchements de découvertes avec des audiences individuelles"
>abstract="Obtenez des informations sur les chevauchements entre vos audiences et les audiences de votre collaborateur ou collaboratrice."

Découvrez les chevauchements pour obtenir des informations sur la manière dont vos audiences se comparent aux audiences de vos collaborateurs. Par défaut, cette section compare toutes vos audiences à celles de chacun des collaborateurs. Utilisez le contrôle de pagination au bas de la section pour parcourir les audiences disponibles.

![L’espace de travail Discover avec la section Discover overlaps mise en surbrillance.](/help/assets/collaborate/discover/discover-overlaps.png)

>[!NOTE]
>
>La visibilité des audiences de votre collaborateur dépend du paramètre que celui-ci a choisi pour une audience dans la [section d’accès à la connexion](/help/guide/setup/onboard-audiences.md#connection-access) et la [section de visibilité des métadonnées](/help/guide/setup/onboard-audiences.md#metadata-visibility). Si votre collaborateur a défini toutes les audiences sur privées, cette section n’affichera aucune audience.

Si votre collaborateur n’a activé ni l’index d’audience ni le pourcentage de chevauchement, l’audience ne s’affichera pas.

Pour modifier votre sélection d’audience, sélectionnez **[!UICONTROL Modifier l’audience]**.

![Découvrir l’espace de travail avec l’option Modifier l’audience mise en surbrillance.](/help/assets/collaborate/discover/change-audience.png)

La boîte de dialogue **[!UICONTROL Modifier l’audience]** s’ouvre. Vous pouvez y sélectionner une audience spécifique à comparer aux audiences de votre collaborateur ou de votre collaboratrice. Sélectionnez les audiences souhaitées ou effacez vos sélections pour sélectionner toutes les audiences, puis sélectionnez **[!UICONTROL Enregistrer]**.

![Boîte de dialogue Modifier l’audience dans l’espace de travail Découvrir](/help/assets/collaborate/discover/change-audience-selection.png).

Une fois les audiences sélectionnées, la section **[!UICONTROL Découvrir les chevauchements]** affiche les informations suivantes pour chaque audience :

| Mesure | Description |
|---------|----------|
| **[!UICONTROL Nombre d’identités]** | Nombre d’identifiants uniques dans l’audience. |
| **[!UICONTROL Identités qui se chevauchent]** | Nombre d’identifiants uniques qui se chevauchent entre l’audience recommandée et toutes vos audiences. |
| **[!UICONTROL Chevaucher %]** | Pourcentage d’identités qui se chevauchent entre l’audience recommandée et toutes vos audiences. |
| **[!UICONTROL Index d’audience]** | Un score qui indique l’importance de la relation d’une audience avec une autre en fonction du nombre d’audiences sous-jacentes et des chevauchements. Pour en savoir plus sur la signification des scores, lisez la section [score de l’index d’audience](#audience-index-score). |
| **[!UICONTROL Catégories d’audience]** | Les catégories que votre collaborateur a affectées à l’audience. |
| **[!UICONTROL Clés de correspondance]** | Les clés de correspondance sélectionnées par votre collaborateur pour l’audience. |

{style="table-layout:auto"}

## Score de l’index d’audience {#audience-index-score}

>[!CONTEXTUALHELP]
>id="rtcdp_collaboration_discover_audience_index_score"
>title="Score de l’index d’audience"
>abstract="Les scores de l’index d’audience sont une mesure nuancée qui montre dans quelle mesure une audience est liée à une autre en fonction du nombre d’audiences sous-jacentes et des chevauchements. Le score de l’index brut est traduit en bandes de pertinence, qui catégorisent les scores de l’index d’audience de très faible à très élevé. Cela vous permet d’évaluer rapidement la force de la relation entre votre audience et l’audience de votre collaborateur ou collaboratrice."

Les scores de l’index d’audience sont une mesure nuancée qui montre dans quelle mesure une audience est liée à une autre en fonction du nombre d’audiences sous-jacentes et des chevauchements. Vous pouvez ainsi contextualiser les informations sur les audiences et identifier les audiences à fort potentiel pour la prospection et le ciblage des campagnes.

Le score de l&#39;index est calculé au moyen de la formule suivante :

![Formule de calcul du score de l’index.](/help/assets/collaborate/discover/index-score-formula.png)

Imaginez qu&#39;un constructeur automobile veuille faire une campagne publicitaire auprès d&#39;un grand éditeur de CTV pour un nouveau modèle de SUV. Le constructeur automobile dispose de données sur les propriétaires actuels d&#39;un modèle similaire et souhaite les utiliser pour trouver d&#39;autres prospects pour les convertir en clients. Le constructeur automobile examine les auditoires de l&#39;éditeur de CTV pour trouver un auditoire pertinent qui correspond étroitement aux propriétaires actuels de VUS.

![L&#39;annonceur automobile contre les audiences de l&#39;éditeur de CTV.](/help/assets/collaborate/discover/audience-index-score-example.png)

Les calculs de score d’index sont effectués et peuvent être utilisés pour déterminer le succès probable de la campagne :

| Audience de l’éditeur de CTV | Formule | Score de l’index (i) | Interprétation |
|------------------------|-------------|----------------|----------------|
| Ligne de base (toutes les audiences) | ((1,3 M / 1,3 M) / (50 M / 50 M)) * 100 | 100 | Il s’agit de la référence par rapport à laquelle les autres audiences de votre collaborateur sont comparées. |
| Binge Watchers | ((500 000 / 1,3 M) / (20 M / 50 M)) * 100 | 96 | En ciblant cette audience, vous êtes 4 % moins susceptible d’atteindre les propriétaires de SUV par rapport à la base. |
| Amateurs De Comédie | ((200 000 / 1,3 M) / (6 M / 50 M)) * 100 | 128 | En ciblant cette audience, vous êtes 28 % plus susceptible d’atteindre les propriétaires de SUV par rapport à la base. |
| Hommes 25-34 ans | ((700 000 / 1,3 M) / (12 M / 50 M)) * 100 | 224 | En ciblant cette audience, vous êtes 124 % plus susceptible d’atteindre les propriétaires de SUV par rapport à la base. |
| Amateurs de technologie | ((500 000 / 1,3 M) / (8 M / 50 M)) * 100 | 240 | En ciblant cette audience, vous êtes 140 % plus susceptible d’atteindre les propriétaires de SUV par rapport à la base. |

{style="table-layout:auto"}

Pour mieux comprendre l’impact des scores d’index sur votre campagne, des bandes de pertinence sont fournies avec les scores.

### Bandes de pertinence {#audience-index-relevance-bands}

Pour faciliter la comparaison entre les différentes audiences et campagnes, Collaboration convertit les scores d’index en bandes de pertinence (très faible à très élevé). Cela vous permet d’évaluer rapidement la force de la relation entre votre audience et l’audience de votre collaborateur ou collaboratrice.

| Score de l’index (i) | Bande de pertinence | Description |
|---------------|----------|-----------|
| i &lt; 60 | Très faible | Le chevauchement est beaucoup moins fréquent dans l’audience cible par rapport à votre audience, ce qui indique une relation très faible. Les clients qui utilisent cette audience sont beaucoup moins susceptibles d’atteindre leur audience cible. |
| 60 &lt; i &lt; 80 | Faible | Le chevauchement est un peu moins fréquent dans l’audience cible par rapport à votre audience, ce qui suggère une relation faible. Les clients qui utilisent cette audience sont moins susceptibles d’atteindre leur audience cible. |
| 80 &lt; i &lt; 120 | Méthode | Le chevauchement est à peu près aussi courant dans l’audience cible que dans votre audience, ce qui indique une relation type. Les clients qui utilisent cette audience ont une probabilité moyenne d’atteindre leur audience cible. |
| 120 &lt; i &lt; 140 | Élevé | Le chevauchement est plus courant dans l’audience cible que dans votre audience, ce qui montre une relation forte. Les clients qui utilisent cette audience sont plus susceptibles d’atteindre leur audience cible. |
| i > 140 | Très élevé | Le chevauchement est beaucoup plus courant dans l’audience cible par rapport à votre audience, ce qui reflète une relation très forte. Les clients qui utilisent cette audience sont beaucoup plus susceptibles d’atteindre leur audience cible. |

{style="table-layout:auto"}

Dans la section découvrir les chevauchements , le score de l’index d’audience affiche la bande de pertinence à côté du score. Le score sera codé par couleur pour indiquer la bande de pertinence, ce qui facilite l&#39;identification de la force de la relation en un coup d&#39;œil. Les bandes de très faible et de faible pertinence sont affichées en orange, les bandes de pertinence moyenne en noir et les bandes de pertinence élevée et très élevée en vert.

## Étapes suivantes

Après avoir exploré et découvert les audiences souhaitées, il est temps d’[activer](/help/guide/collaborate/activate.md) les audiences qui doivent être utilisées dans les campagnes.
