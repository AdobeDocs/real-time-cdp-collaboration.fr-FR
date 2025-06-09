---
title: Configuration et gestion des destinations
description: Découvrez comment configurer et gérer des destinations dans Real-Time CDP Collaboration.
audience: admin, publisher
badgelimitedavailability: label="Disponibilité limitée" type="Informative" url="https://helpx.adobe.com/legal/product-descriptions/real-time-customer-data-platform-collaboration.html newtab=true"
source-git-commit: f19aff1b7d10a446dd209721e7a6fdf537c9d63e
workflow-type: tm+mt
source-wordcount: '384'
ht-degree: 1%

---

# Configuration et gestion des destinations

{{limited-availability-release-note}}

Les destinations sont des intégrations utilisées pour envoyer des audiences ciblées à des plateformes externes. Ces intégrations vous permettent d’activer des audiences sur divers canaux et plateformes marketing à utiliser dans les campagnes et l’engagement des clients.

Actuellement, les destinations ne sont disponibles que pour les éditeurs dans Real-Time CDP Collaboration. Les éditeurs peuvent configurer des destinations pour envoyer des audiences à des plateformes externes, telles que Adobe Experience Platform, en vue de les utiliser dans des campagnes. Les annonceurs peuvent ensuite [activer des audiences dans un projet](../collaborate/activate.md), qui sont envoyées à la destination configurée de l’éditeur.

![L’onglet Mes destinations de l’espace de travail Configuration affiche une destination Adobe Experience Platform active](/help/assets/setup/manage-destinations/my-destinations-overview.png)

Pour en savoir plus sur les destinations, consultez le guide [présentation des destinations](../destinations/overview.md).

## Configuration des destinations {#configure-destinations}

Les destinations sont configurées dans la section **[!UICONTROL Configuration]** de Real-Time CDP Collaboration. Pour configurer une destination, accédez à **[!UICONTROL Configuration]** puis sélectionnez l’onglet **[!UICONTROL Mes destinations]**. Ici, vous pouvez afficher toutes les destinations disponibles.

>[!IMPORTANT]
>
>Pour configurer et gérer les destinations, votre utilisateur doit disposer d’un rôle avec l’autorisation **Gérer les données d’audience** qui lui est attribuée. Pour plus d’informations sur la gestion des rôles, consultez le guide [gérer les rôles](../permissions/manage-roles.md).

![L’onglet Mes destinations de l’espace de travail Configuration affiche les destinations disponibles.](/help/assets/setup/manage-destinations/my-destinations.png)

Le processus de configuration des destinations dépend de la destination que vous configurez. Consultez le catalogue [destinations disponibles](../destinations/overview.md#available-destinations) pour afficher les destinations disponibles et leurs guides de configuration.

>[!NOTE]
>
>Actuellement, seul Adobe Experience Platform est disponible en tant que destination en libre-service dans Real-Time CDP Collaboration. Si vous souhaitez configurer une autre destination, contactez votre représentant ou représentante Adobe.

## Supprimer les destinations {#delete-destinations}

La suppression d’une destination la supprime de votre organisation, supprime toutes les audiences précédemment envoyées de la destination et empêche toutes les audiences futures d’être envoyées vers cette destination.

Pour supprimer une destination, accédez à l’onglet **[!UICONTROL Mes destinations]** dans la section **[!UICONTROL Configuration]**. Sélectionnez l’option **[!UICONTROL Supprimer]** pour la destination à supprimer.

![Espace de travail Mes destinations avec l’option Supprimer mise en surbrillance pour la destination Adobe Experience Platform.](/help/assets/setup/manage-destinations/delete-destination.png)

Une boîte de dialogue de confirmation s’affiche, dans laquelle vous pouvez confirmer que vous souhaitez supprimer la destination. Sélectionnez **[!UICONTROL Supprimer]** pour supprimer la destination.

![Boîte de dialogue Supprimer la destination avec l’option Supprimer mise en surbrillance.](/help/assets/setup/manage-destinations/delete-destination-confirm.png)

## Étapes suivantes

Une fois la destination configurée, vous pouvez commencer à collaborer avec vos annonceurs pour [activer les audiences ciblées](../collaborate/activate.md) dans vos projets.
