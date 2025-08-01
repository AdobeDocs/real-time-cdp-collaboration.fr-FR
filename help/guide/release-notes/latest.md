---
title: Dernières notes de mise à jour de Real-Time CDP Collaboration
description: Suivez les dernières versions de Real-Time CDP Collaboration
audience: admin, publisher, advertiser
badgelimitedavailability: label="Disponibilité limitée" type="Informative" url="https://helpx.adobe.com/fr/legal/product-descriptions/real-time-customer-data-platform-collaboration.html newtab=true"
exl-id: 8513c648-1cc1-4544-b86d-2ee3193ab60f
source-git-commit: 697a822eb02d42e2fad46c09232ce569a675c032
workflow-type: tm+mt
source-wordcount: '946'
ht-degree: 1%

---

# Dernières notes de mise à jour de Real-Time CDP Collaboration

{{limited-availability-release-note}}

**Dernière mise à jour** : juillet 2025.

Ces notes de mise à jour présentent les fonctionnalités disponibles dans Adobe Real-Time CDP Collaboration. Les versions de Collaboration fonctionnent sur un modèle de diffusion continu, ce qui permet une cadence de publication mensuelle approximative. Ces notes de mise à jour sont souvent mises à jour. Veillez donc à les consulter régulièrement.

## Juillet 2025 {#july-2025}

Real-Time CDP Collaboration prend désormais en charge la collaboration de marque à marque. Les collaborateurs peuvent désormais se connecter, qu’ils soient annonceurs ou éditeurs. Cela permet des opportunités de collaboration plus flexibles et permet aux marques d’exploiter les données et informations des unes et des autres. Pour en savoir plus sur les différences entre la collaboration de marque à marque et la collaboration d’annonceur à éditeur, consultez le guide [modèles de collaboration](../overview/collaboration-patterns.md).

* Les collaborateurs peuvent désormais se connecter les uns aux autres à l’aide d’[invitations à une connexion privée](../connect/establishing-connections.md#private-connection-invites). Partagez le code de connexion unique de votre compte avec un collaborateur qui peut ensuite l’utiliser pour se connecter directement avec vous. Il s’agit d’une fonctionnalité clé de la collaboration de marque à marque, qui permet aux collaborateurs d’établir des connexions au-delà des annonceurs qui explorent le répertoire **[!UICONTROL Découvrir les éditeurs]**.
* [Destinations en libre-service](../setup/manage-destinations.md) sont désormais disponibles pour les annonceurs et les éditeurs.
* L’activation de l’audience est désormais disponible pour les deux collaborateurs dans une connexion, quel que soit leur rôle [ compte](../overview/roles.md). Les paramètres d’activation des audiences sont configurés lors de l’[établissement de connexions](../connect/establishing-connections.md#configure-connection-settings), ce qui vous permet de spécifier quel collaborateur peut activer les audiences. Pour en savoir plus sur l’activation des audiences, consultez le guide [ Activer les audiences ](../collaborate/activate.md).
* Le cas d’utilisation **[!UICONTROL Activer]** a été reconfiguré pour prendre en charge la collaboration de marque à marque. L’onglet **[!UICONTROL Activer]** d’un projet affiche désormais les audiences qui ont été envoyées à votre collaborateur et les audiences activées vers votre destination par votre collaborateur. Pour en savoir plus, consultez le guide [Activer les audiences](../collaborate/activate.md). <br> ![Tableau de bord d’activation avec les sections Audiences envoyées à et Audiences activées.](/help/assets/release-notes/2025/activate-dashboard.png){zoomable="yes"}

## Mai 2025 {#may-2025}

* Real-Time CDP Collaboration est désormais disponible pour les clients en **Australie** et **Nouvelle-Zélande**. Il est automatiquement disponible pour les clients Real-Time CDP Prime et Ultimate dans ces régions.
* Real-Time CDP Collaboration propose désormais des [destinations en libre-service](../setup/manage-destinations.md) par le biais de l’onglet **[!UICONTROL Mes destinations]** dans la section **[!UICONTROL Configuration]**. Les destinations vous permettent d’activer des audiences dans des plateformes tierces, telles que des réseaux publicitaires ou des plateformes de gestion de données, afin d’atteindre vos clients sur divers canaux. Actuellement, seules les destinations Adobe Experience Platform sont prises en charge. Si vous souhaitez configurer une autre destination, contactez votre représentant ou représentante Adobe. Pour en savoir plus sur les destinations, consultez le guide [présentation des destinations](../destinations/overview.md).
   * Les destinations prennent également en charge l’affichage des audiences Collaboration dans le portail d’audiences [Adobe Experience Platform](https://experienceleague.adobe.com/fr/docs/experience-platform/segmentation/ui/audience-portal.md#manage-audiences).
* Vous pouvez désormais modifier la fréquence d’actualisation de l’audience pour les connexions de données existantes dans Collaboration. Actuellement, vous pouvez choisir d’actualiser vos audiences tous les jours ou tous les deux à six jours. Pour en savoir plus sur la modification de la fréquence d’actualisation de l’audience, consultez le guide [gérer les connexions de données](../setup/manage-data-connection.md#scheduling).
* Les répartitions de crédit entre collaborateurs sont désormais définies pour chaque cas d’utilisation sélectionné dans la connexion. Vous pouvez définir différentes règles de consommation de crédit pour chaque cas d’utilisation afin de mieux contrôler l’utilisation de vos crédits. Pour en savoir plus sur la fonctionnalité de partage du crédit, consultez le guide [Paramètres de connexion](../connect/establishing-connections.md#connection-settings). Pour en savoir plus sur la manière dont les crédits sont consommés, lisez le guide [types d’activité de crédit](../setup/my-activity.md#types-of-activities). <br> ![Écran des paramètres de connexion affichant la fonctionnalité de répartition du crédit.](/help/assets/release-notes/2025/credit-split.png){zoomable="yes"}
* Les éditeurs peuvent désormais définir les noms et identifiants des annonceurs avant d’accepter les paramètres de connexion d’un annonceur. Les éditeurs peuvent définir des noms et des identifiants qui s’alignent sur leurs systèmes internes, qui peuvent être différents des noms et des identifiants de l’annonceur. Pour en savoir plus sur l’ajout de noms et d’identifiants d’annonceurs, consultez le guide [Paramètres de connexion](../connect/establishing-connections.md#connection-settings.md). <br> ![Écran des paramètres de connexion affichant le paramètre de l’éditeur, les noms et identifiants des annonceurs.](/help/assets/release-notes/2025/add-advertiser-names-modal.png){zoomable="yes"}

## Avril 2025 {#april-2025}

* Une nouvelle colonne **[!UICONTROL Entrées traitées]** a été ajoutée au tableau des activités de consommation de crédit. Cette colonne affiche le nombre total d’entrées (par exemple, les identifiants ou les lignes) traitées pour chaque activité. [En savoir plus](/help/guide/setup/my-activity.md#inputs-processed). <br> ![Colonne traitée des entrées mise en surbrillance dans la vue Mon activité.](/help/assets/release-notes/2025/inputs-processed-column.png){zoomable="yes"}
* Une nouvelle option d’e-mail de contact a été ajoutée lors de la création du compte. Cela permet aux collaborateurs partenaires de vous contacter si nécessaire pendant le processus de connexion. [En savoir plus](../setup/onboard-account.md).

## Mars 2025 {#march-2025}

* Lorsque vous [approvisionnez des audiences](/help/guide/setup/onboard-audiences.md) dans Collaboration, vous pouvez désormais définir une fréquence d’actualisation de l’audience comprise entre **tous les un et six jours** afin de mieux gérer l’activité de crédit [Gestion de l’audience](/help/guide/setup/my-activity.md#types-of-activities). Pour plus d’informations, consultez le guide [gérer les audiences](https://experienceleague.adobe.com/fr/docs/experience-platform/segmentation/ui/audience-portal.md#manage-audiences). <br> ![Écran de planification affichant différents intervalles de fréquence pour la mise à jour de l’appartenance à l’audience.](/help/assets/setup/add-manage-audiences/audience-scheduling-frequency.png "Écran de planification affichant différents intervalles de fréquence pour la mise à jour de l’appartenance à l’audience."){width="250" align="center" zoomable="yes"}
* Lors de l’établissement d’une connexion avec un collaborateur, vous pouvez désormais effectuer une sélection parmi des **cas d’utilisation** prédéfinis. Le cas d’utilisation sélectionné détermine les sections de projet et les fonctionnalités de produit qui deviennent disponibles. Pour plus d’informations, consultez le guide [gérer les projets](/help/guide/collaborate/manage-projects.md#project-use-cases).
   * *Mesure* active la section de projet **Mesure**.
   * *Découverte d’audiences* active la section de projet **Découverte**.
   * *Activation de l’audience* active les sections de projet **Activer** <br>
* Vous pouvez désormais supprimer des connexions avec des collaborateurs avec lesquels vous ne souhaitez plus travailler. Pour savoir comment supprimer des connexions, consultez le guide [suppression de connexions](/help/guide/connect/establishing-connections.md#delete-connections).

## Février 2025 {#february-2025}

Adobe Real-Time CDP Collaboration, conçu pour permettre aux annonceurs et aux éditeurs de découvrir, d’activer et de mesurer des audiences à forte valeur ajoutée sans cookies tiers, est désormais disponible en général aux États-Unis.

### Commencer

1. **Configuration des accès** : les administrateurs système configurent les autorisations d’accès pour les utilisateurs. Pour en savoir plus sur la configuration des autorisations d’accès, consultez le guide [gérer l’accès des utilisateurs](/help/guide/permissions/manage-user-access.md#RTCDP-collaboration-access).
2. **Connexion aux sources de données** : audiences Source à utiliser dans Collaboration. Pour commencer à approvisionner les audiences, lisez le guide [source et gestion des audiences](/help/guide/setup/onboard-audiences.md) .
3. **Établir des connexions** : commencez à collaborer avec des annonceurs ou des éditeurs approuvés. Pour en savoir plus sur la création de connexions, consultez le guide [établissement de connexions](/help/guide/connect/establishing-connections.md).
4. **Découvrir et activer** : créez des projets pour identifier les audiences importantes à activer dans les campagnes. Pour en savoir plus sur la création de projets, consultez le guide [gérer les projets](/help/guide/collaborate/manage-projects.md).

### Disponibilité

* Adobe Real-Time CDP Collaboration est actuellement disponible uniquement pour les clients américains.
* Il est automatiquement disponible pour les clients Adobe Real-Time CDP Prime et Ultimate

Pour plus d’informations, consultez :

* [Présentation de Collaboration](/help/guide/home.md)
* [Workflow de bout en bout](/help/guide/overview/end-to-end-workflow.md)
* [Présentation des autorisations](/help/guide/permissions/overview.md)
