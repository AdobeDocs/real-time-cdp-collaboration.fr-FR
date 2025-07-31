---
title: Présentation des destinations
description: En savoir plus sur les destinations dans Real-Time CDP Collaboration.
audience: admin, publisher
badgelimitedavailability: label="Disponibilité limitée" type="Informative" url="https://helpx.adobe.com/fr/legal/product-descriptions/real-time-customer-data-platform-collaboration.html newtab=true"
exl-id: 5cbbf5c4-4caa-40da-97be-690d95c1201c
source-git-commit: 4ef7f8c7c27935f0e5b3620da63e7129f2714b37
workflow-type: tm+mt
source-wordcount: '328'
ht-degree: 7%

---

# Présentation des destinations

{{limited-availability-release-note}}

Les destinations sont des intégrations utilisées pour envoyer des audiences ciblées à des plateformes externes. Ces intégrations vous permettent d’activer des audiences sur divers canaux et plateformes marketing à utiliser dans les campagnes et l’engagement des clients.

Les collaborateurs peuvent configurer des destinations pour envoyer des audiences à des plateformes externes, telles que Adobe Experience Platform, en vue de les utiliser dans des campagnes. Les collaborateurs peuvent ensuite [activer des audiences dans un projet](../collaborate/activate.md), qui sont envoyées à la destination configurée de leur connexion. L’activation peut être effectuée par l’un des collaborateurs en fonction des paramètres d’activation de l’audience [configurés dans la connexion](/help/guide/connect/establishing-connections.md#configure-connection-settings).

>[!IMPORTANT]
>
>Actuellement, lorsque les collaborateurs activent des audiences dans un projet, elles sont automatiquement envoyées à la destination configurée de leur connexion. Vous **devez** configurer une destination avant que votre collaborateur puisse activer des audiences dans un projet.

## Configuration des destinations {#configure-destinations}

Pour configurer une destination, accédez à **[!UICONTROL Configuration]** puis sélectionnez l’onglet **[!UICONTROL Mes destinations]**. Ici, vous pouvez afficher toutes les destinations disponibles.

>[!NOTE]
>
> Actuellement, seul Adobe Experience Platform est disponible en tant que destination en libre-service dans Collaboration. Si vous souhaitez configurer une destination telle qu’Amazon S3 ou Snowflake, contactez votre représentant ou représentante Adobe.

![L’onglet Mes destinations de l’espace de travail Configuration affiche les destinations disponibles.](/help/assets/destinations/overview/my-destinations-overview.png)

Pour commencer à configurer une destination, sélectionnez l’option **[!UICONTROL Configurer]** dans la destination de votre choix. Pour plus d’informations sur la configuration de destinations spécifiques, reportez-vous aux guides dans le tableau [destinations disponibles](#available-destinations).

![L’espace de travail Mes destinations avec l’option Configurer mise en surbrillance pour la destination Adobe Experience Platform.](/help/assets/destinations/overview/my-destinations-set-up.png)

### Destinations disponibles {#available-destinations}

Les destinations suivantes peuvent être configurées dans Collaboration. Pour afficher le guide de configuration de cette destination, sélectionnez le nom de la destination dans le tableau ci-dessous. Si vous souhaitez configurer une destination qui n’est pas actuellement disponible, contactez votre représentant ou représentante Adobe.

| Destination | Disponibilité |
| --- | --- |
| [Adobe Experience Platform](./experience-platform.md) | Disponible |
| Amazon S3 | Bientôt disponible. |
| Snowflake | Bientôt disponible. |
| Google Cloud Storage | Bientôt disponible. |
| Stockage Azure Blob | Bientôt disponible. |

## Étapes suivantes

Une fois la destination configurée, vous pouvez commencer à [activer les audiences ciblées](../collaborate/activate.md) dans vos projets.
