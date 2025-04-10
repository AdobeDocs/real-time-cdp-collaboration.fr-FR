---
title: Découvrir les chevauchements et comparer les audiences
description: Découvrez les chevauchements entre vos audiences et celles de vos collaborateurs. Découvrez les meilleures audiences à utiliser dans vos campagnes.
audience: admin, publisher, advertiser
badgelimitedavailability: label="Disponibilité limitée" type="Informative" url="https://helpx.adobe.com/legal/product-descriptions/real-time-customer-data-platform-collaboration.html newtab=true"
exl-id: 38c42ad3-9d01-4d09-b80e-37fb51cbf42b
source-git-commit: acaaaa1e1fab981d874210639c16e76e48fc3394
workflow-type: tm+mt
source-wordcount: '882'
ht-degree: 1%

---

# Découvrir les chevauchements et comparer les audiences

{{limited-availability-release-note}}

>[!IMPORTANT]
>
>L’espace de travail **[!UICONTROL Discover]** n’est disponible que si le cas d’utilisation **Audience discovery** a été activé [pendant le processus de connexion](../connect/establishing-connections.md#connection-settings). Pour plus d’informations sur les cas d’utilisation, consultez le guide [gestion des projets](./manage-projects.md#project-use-cases).

Après avoir [créé un projet](/help/guide/collaborate/manage-projects.md) dans un espace de collaboration entre un annonceur et un éditeur, vous pouvez maintenant comparer vos audiences aux audiences de votre collaborateur. Ainsi, vous pouvez découvrir des chevauchements entre les audiences et obtenir des informations réparties par clés de correspondance ou identités. Cela permet aux annonceurs de décider quelles audiences partager avec les éditeurs pour activation.

>[!IMPORTANT]
>
>Tous les [esquisses de données](/help/guide/glossary.md#sketches) qui ne sont pas mis à jour ou actualisés seront supprimés après 7 jours. Dans ce cas, les chiffres affichés dans les différents rapports de chevauchement sur cette page sont nuls et le partage d’audience n’est plus disponible pour ces audiences expirées. Les esquisses de données sont automatiquement actualisées pour les audiences avec un [planning d’actualisation actif](/help/guide/setup/onboard-audiences.md#schedule).

![Découvrir les chevauchements](/help/assets/collaborate/discover-overlaps/discover-overlaps.png)

Les clés de correspondance utilisées pour découvrir et comparer des audiences sont définies lorsque vous vous [connectez avec un éditeur](/help/guide/connect/establishing-connections.md#connection-settings). Pour modifier les pourcentages de chevauchement indiqués en préparation de l’exécution de campagnes, vous pouvez supprimer des clés de correspondance, mais vous ne pouvez pas en ajouter de nouvelles à ce stade. Pour ce faire, accédez à la [paramètres de connexion](/help/guide/connect/establishing-connections.md#connection-settings) entre les collaborateurs.

![Écran Modifier les clés de correspondance](/help/assets/collaborate/discover-overlaps/edit-match-keys.png)

## Conditions préalables {#prerequisites}

Pour utiliser pleinement la fonctionnalité de l’onglet **[!UICONTROL Découvrir]** du workflow **[!UICONTROL Collaborer]**, vous avez déjà :

* [Audiences importées](/help/guide/setup/onboard-audiences.md)
* [Connecté](/help/guide/connect/establishing-connections.md) à un annonceur ou un éditeur souhaité avec le cas d’utilisation **découverte d’audience** activé
* [Création d’un projet](/help/guide/collaborate/manage-projects.md) entre vous et un collaborateur

Une fois les conditions préalables mentionnées ci-dessus remplies, vous pouvez commencer à explorer et à comparer le chevauchement entre votre audience et celle de votre collaborateur.

## Comparer des audiences {#compare-audiences}

>[!CONTEXTUALHELP]
>id="rtcdp_collaboration_discover_compare_audiences"
>title="Comparer des audiences"
>abstract="Découvrez les chevauchements entre vos audiences et celles de vos collaborateurs. Vous pouvez ajuster les paramètres du sélecteur de liste déroulante pour détecter les chevauchements entre une ou plusieurs de vos audiences et une ou plusieurs audiences de vos collaborateurs."

>[!CONTEXTUALHELP]
>id="rtcdp_collaboration_discover_your_identity_count"
>title="Votre nombre d’identités"
>abstract="Nombre de profils avec cette identité sélectionnée qui font partie de votre audience sélectionnée"

>[!CONTEXTUALHELP]
>id="rtcdp_collaboration_discover_collaborator_identity_count"
>title="Nombre d’identités du collaborateur"
>abstract="Nombre de profils avec cette identité sélectionnée qui font partie de l’audience sélectionnée par votre collaborateur ou votre collaboratrice"

>[!CONTEXTUALHELP]
>id="rtcdp_collaboration_discover_overlapping_identities_count"
>title="Nombre d’identités qui se chevauchent"
>abstract="Nombre de profils avec cette identité sélectionnée qui sont présents dans votre audience et dans celle de votre collaborateur"

>[!CONTEXTUALHELP]
>id="rtcdp_collaboration_discover_overlapping_identities_percentage"
>title="Pourcentage d’identités qui se chevauchent"
>abstract="Pourcentage de profils qui se chevauchent entre votre audience et l’audience sélectionnée de votre collaborateur."

Utilisez la carte Comparer les audiences pour obtenir de riches informations sur le chevauchement entre vos audiences et celles de votre collaborateur. Vous pouvez choisir de comparer l’une des combinaisons d’audience suivantes :

* Une de vos audiences par rapport à l’une des audiences de votre collaborateur
* Une de vos audiences par rapport à toutes les audiences de vos collaborateurs
* Toutes vos audiences par rapport à une audience de votre collaborateur
* Toutes vos audiences par rapport à toutes les audiences de vos collaborateurs

Les informations affichées concernent :

| Mesure | Description |
|---------|----------|
| **[!UICONTROL Nombre d’identités]** (vôtre) | Nombre de profils avec une identité sélectionnée qui font partie de votre audience sélectionnée. |
| **[!UICONTROL Nombre d’identités]** (votre collaborateur) | Nombre de profils avec une identité sélectionnée qui font partie de l’audience sélectionnée par votre collaborateur. |
| **[!UICONTROL Identités qui se chevauchent]** | Nombre de profils avec une identité sélectionnée qui sont présents à la fois dans votre audience et dans celle de votre collaborateur. |
| **[!UICONTROL Pourcentage de chevauchement]** | Pourcentage de profils qui se chevauchent entre votre audience et l’audience sélectionnée de votre collaborateur. |
| **[!UICONTROL Répartition des identités par clé de correspondance]** | En fonction des clés de correspondance convenues entre vous et votre collaborateur pour le projet, afficher la composition des identités dans les calculs de chevauchement par clés de correspondance individuelles. |

{style="table-layout:auto"}

>[!TIP]
>
>Le pourcentage de chevauchement peut ne pas toujours être disponible pour toutes les audiences. La visibilité de l’indicateur de pourcentage de chevauchement dépend du paramètre que votre collaborateur a choisi pour une audience dans la [section de visibilité des métadonnées](/help/guide/setup/onboard-audiences.md#metadata-visibility).

## Audiences concernées {#relevant-audiences}

>[!CONTEXTUALHELP]
>id="rtcdp_collaboration_discover_relevant_audiences"
>title="Audiences concernées"
>abstract="En fonction des pourcentages de chevauchement, ces audiences d’éditeur peuvent être adaptées à votre campagne. <br><br> Le <b> nombre d’identités </b> correspond à la taille de l’audience de l’éditeur. <br><br> <b>Identités qui se chevauchent</b> représente le chevauchement entre l’audience recommandée de l’éditeur et toutes les audiences de l’annonceur. <br><br> Le <b>chevauchement %</b> représente le nombre d’identités qui se chevauchent divisé par la taille de <i>toutes</i> les audiences de l’annonceur."

La vue **[!UICONTROL Audiences pertinentes]** du module **[!UICONTROL Découvrir]** fournit une liste sélectionnée des cinq premières audiences en fonction du pourcentage de chevauchement. Cette fonctionnalité vous permet d’identifier rapidement les audiences qui chevauchent le plus vos données actuelles, ce qui vous permet de cibler vos campagnes plus efficacement.

* **[!UICONTROL Nombre d’identités]** correspond à la taille de l’audience de l’éditeur.
* **[!UICONTROL Identités qui se chevauchent]** représente le chevauchement entre l’audience recommandée de l’éditeur et toutes les audiences de l’annonceur.
* **[!UICONTROL Chevauchement %]** représente le nombre d’identités qui se chevauchent divisé par la taille de *toutes* les audiences de l’annonceur.

![Vue des audiences pertinentes](/help/assets/collaborate/discover-overlaps/relevant-audiences-highlighted.png)

## Découvrir les chevauchements {#discover-overlaps}

>[!CONTEXTUALHELP]
>id="rtcdp_collaboration_discover_overlaps_collaborator_audiences"
>title="Découvrir les chevauchements avec des audiences individuelles"
>abstract="Obtenez des informations sur la population de ce public et ses recoupements avec l&#39;univers des identités du collaborateur."

![Découvrir les chevauchements avec différentes vues d’audiences](/help/assets/collaborate/discover-overlaps/discover-overlaps-cards-view.png)

Obtenez des informations détaillées sur n’importe laquelle des audiences de votre collaborateur et consultez des informations de chevauchement en comparant ces audiences par rapport à l’ensemble de votre population, pour toutes vos audiences, ou par rapport à certaines de vos audiences.

>[!TIP]
>
>Certains des nombres indiqués dans la capture d’écran peuvent ne pas toujours être disponibles pour toutes les audiences. Leur visibilité dépend du paramètre que votre collaborateur a choisi pour une audience dans la [section de visibilité des métadonnées](/help/guide/setup/onboard-audiences.md#metadata-visibility).

## Étapes suivantes

Après avoir exploré et découvert les audiences souhaitées, il est temps de [partager](/help/guide/collaborate/share.md) les audiences qui doivent être utilisées dans les campagnes avec l’éditeur.
