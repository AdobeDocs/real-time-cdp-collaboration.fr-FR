---
title: Partager les audiences
description: Découvrez comment partager des audiences avec vos collaborateurs pour les campagnes publicitaires.
audience: admin, publisher, advertiser
badgelimitedavailability: label="Disponibilité limitée" type="Informative" url="https://helpx.adobe.com/legal/product-descriptions/real-time-customer-data-platform-collaboration.html newtab=true"
exl-id: 0fdf0598-89c9-452d-a2e3-ce868df0b9d2
source-git-commit: acaaaa1e1fab981d874210639c16e76e48fc3394
workflow-type: tm+mt
source-wordcount: '755'
ht-degree: 1%

---

# Partager les audiences

{{limited-available-release-note}}

>[!IMPORTANT]
>
>L’espace de travail **[!UICONTROL Partage]** n’est disponible que si le cas d’utilisation **Partage et activation d’audiences** a été activé [pendant le processus de connexion](../connect/establishing-connections.md#connection-settings). Pour plus d’informations sur les cas d’utilisation, consultez le guide [gestion des projets](./manage-projects.md#project-use-cases).

En tant qu’annonceur, apprenez à partager des audiences avec vos éditeurs afin qu’ils puissent exécuter des campagnes. Si votre collaboration a activé le cas d’utilisation **Découvrir des audiences**, commencez par exécuter des rapports de chevauchement dans l’onglet [Découvrir](/help/guide/collaborate/discover.md) pour identifier les meilleures audiences à partager.

## Partager de nouvelles audiences

Pour commencer à partager des audiences, accédez à l’onglet **[!UICONTROL Partager]** dans l’espace de travail de votre projet. Seules les **organisations d’annonceurs** peuvent partager des audiences pour les campagnes. Dans cet onglet, vous pouvez vérifier et gérer les audiences partagées.

Sélectionnez le symbole **Plus (+)** ou l’option **[!UICONTROL Partager l’audience]** si aucune audience précédente n’a été partagée, pour lancer le processus de partage d’audience.

![Affichage par défaut sans audiences partagées.](/help/assets/collaborate/share/share-new-audiences.png)

Un nouveau panneau s’affiche, dans lequel vous pouvez sélectionner les audiences que vous souhaitez partager avec votre collaborateur.

![Workflow de partage de nouvelles audiences.](/help/assets/collaborate/share/share-audiences-workflow.png)

### Sélectionner les audiences à partager

Dans la fenêtre de sélection de l’audience, vous pouvez rechercher des audiences spécifiques à partager en saisissant le nom de l’audience dans la barre de recherche. Sélectionnez **[!UICONTROL Parcourir les audiences]** et utilisez les options de tri disponibles pour trouver les audiences exactes dont vous avez besoin.

![Parcourir la vue des audiences avec les audiences sélectionnées.](/help/assets/collaborate/share/browse-audiences-view.png)

### Modification des clés de correspondance et définition des options de ciblage

Après avoir sélectionné les audiences souhaitées à partager, vous pouvez maintenant sélectionner d’autres options de configuration pour l’activité de partage.

![Modifier les touches de correspondance et cibler ou supprimer le sélecteur mis en surbrillance](/help/assets/collaborate/share/match-keys-and-targeting.png)

Sélectionnez **[!UICONTROL Modifier les clés de correspondance]** pour indiquer quelles clés de correspondance doivent être utilisées pour les identités dans l’audience. Ces options sont héritées des paramètres sélectionnés lors de la configuration initiale de la connexion entre collaborateurs. Vous pouvez supprimer les clés de correspondance sélectionnées à ce stade si elles ne s’appliquent pas à cette campagne spécifique, mais vous ne pouvez pas ajouter de nouvelles clés de correspondance à ce stade.

![Modifier les clés de correspondance.](/help/assets/collaborate/share/update-match-keys.png)

Pour chaque audience, choisissez si vous souhaitez que les membres de cette audience soient ciblés ou supprimés dans la campagne. Les profils supprimés ne feront spécifiquement pas partie de l’audience activée par l’éditeur.

### Définir la fréquence et l’intervalle d’actualisation de l’audience

Enfin, définissez la fréquence et la période souhaitées pour l’actualisation de l’audience. Les modes actuellement pris en charge pour l’actualisation de l’audience sont **[!UICONTROL Une fois]** et **[!UICONTROL Quotidien]**.

Lors de la sélection de **[!UICONTROL Une fois]**, l’adhésion à l’audience n’est pas actualisée tout au long d’une campagne. En sélectionnant **[!UICONTROL Quotidien]**, l’adhésion à l’audience est actualisée une fois par jour pendant toute la durée d’une campagne.

![Options de fréquence mises en surbrillance.](/help/assets/collaborate/share/audience-refresh-frequency.png)

Une fois vos sélections effectuées, sélectionnez **[!UICONTROL Partager]** pour terminer le workflow.

>[!SUCCESS]
>
>Une nouvelle activité de partage d’audience apparaît désormais dans l’onglet **[!UICONTROL Partage]**. Si vous le souhaitez, vous pouvez revenir en arrière et modifier l’une des sélections que vous avez effectuées.

## Afficher les audiences actuellement partagées

Dans l’onglet **[!UICONTROL Partage]**, vous pouvez afficher les audiences actuellement partagées entre les collaborateurs, regroupées dans des activités de partage d’audience.

![Présentation de l’onglet Partage.](/help/assets/collaborate/share/share-tab-overview.png)

<!--

The banner at the top of the page shows figures across all audience sharing activities. 

![The hero banner in the sharing tab.](/help/assets/collaborate/share/share-hero-banner.png)


|Metric | Description |
|---------|----------|
| **[!UICONTROL Shared audiences]** | Indicates the number of audiences shared between collaborators in this project, across all audience sharing modules. |
| **[!UICONTROL Estimated addressable reach]** | Indicates the approximate number of profiles that you can reach across all the audiences that are currently shared in the project. [TODO: ADD INFORMATION ABOUT HOW THIS IS CALCULATED] |
| **[!UICONTROL Target identities]** | The number of identities across all audiences shared in this project for which you selected to target the profiles. |
| **[!UICONTROL Suppress identities]** | The number of identities across all audiences shared in this project for which you selected to suppress the profiles and thereby not target them in campaigns. |

-->

Au sein de chaque activité de partage d’audience, vous pouvez obtenir des informations sur chaque audience partagée.

| Mesure | Description |
|---------|----------|
| **[!UICONTROL Nombre d’identités]** | Indique le nombre de profils sur toutes les identités liées à cette audience, en fonction de la dernière évaluation du nombre d’identités. Ces nombres sont actualisés toutes les 24 heures. |
| **[!UICONTROL Identités qui se chevauchent]** | Indique le nombre d’identités qui se chevauchent entre les membres de cette audience et la population totale des profils dans l’inventaire du collaborateur. |
| **[!UICONTROL Répartition des clés de correspondance]** | Affiche le nombre d’identités pour chaque identité utilisée dans l’audience. Par exemple, un nombre total d’identités de 500 000 utilisateurs peut se composer de 400 000 utilisateurs ayant saisi l’identité d’e-mail hachée et de 100 000 utilisateurs ayant saisi une identité d’identifiant mobile. Notez que dans l’exemple décrit ici, la même personne peut être présente deux fois dans l’audience avec son adresse e-mail et son identifiant mobile. |
| **[!UICONTROL Objectif]** | **[!UICONTROL Supprimer]** ou **[!UICONTROL Cible]**. Indique si les membres d’une audience doivent être ciblés ou exclus des campagnes. |

La page fournit également des commandes vous permettant de **[!UICONTROL Suspendre le partage]** et **[!UICONTROL Modifier les audiences]**.

## Modifier des audiences {#edit-audiences}

>[!CONTEXTUALHELP]
>id="rtcdp_collaboration_share_edit_audiences_usecases"
>title="Cibler ou supprimer un cas d’utilisation"
>abstract="<p>Sélectionnez **Cible** si vous souhaitez que les profils de l’audience soient affichés dans les publicités de la campagne.</p> <p>Sélectionnez **Supprimer** si vous souhaitez exclure les profils de l’audience des messages de la campagne.</p>"

Sélectionnez **[!UICONTROL Modifier les audiences]** pour modifier les audiences partagées dans un module de partage d’audiences, ainsi que pour modifier plusieurs configurations liées à la manière dont les audiences sont partagées.

![Affichage de la fenêtre modale de modification des audiences](/help/assets/collaborate/share/edit-audiences-modal.png)

<!--

Search for audiences that you want to add to the sharing module. 

For each audience, you can select whether you'd like to target or suppress those profiles in campaigns. 

To remove an audience from the sharing module, select the trash can icon [TODO: add spectrum icon and folder].

Select how often you would like the audience membership to be refreshed and the date range within which you want the membership of the audience to be refreshed. 

TODO: are there any limitations for frequency in the M1 release?

-->

## Étapes suivantes

Une fois que l’éditeur a reçu les audiences partagées, il les [active](/help/guide/collaborate/activate.md) dans les campagnes publicitaires numériques.
