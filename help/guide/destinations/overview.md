---
title: Présentation des destinations
description: En savoir plus sur les destinations dans Real-Time CDP Collaboration.
audience: admin, publisher
badgelimitedavailability: label="Disponibilité limitée" type="Informative" url="https://helpx.adobe.com/fr/legal/product-descriptions/real-time-customer-data-platform-collaboration.html newtab=true"
source-git-commit: f19aff1b7d10a446dd209721e7a6fdf537c9d63e
workflow-type: tm+mt
source-wordcount: '352'
ht-degree: 6%

---

# Présentation des destinations

{{limited-availability-release-note}}

Les destinations sont des intégrations utilisées pour envoyer des audiences ciblées à des plateformes externes. Ces intégrations vous permettent d’activer des audiences sur divers canaux et plateformes marketing à utiliser dans les campagnes et l’engagement des clients.

Actuellement, les destinations ne sont disponibles que pour les éditeurs dans Real-Time CDP Collaboration. Les éditeurs peuvent configurer des destinations pour envoyer des audiences à des plateformes externes, telles que Adobe Experience Platform, en vue de les utiliser dans des campagnes. Les annonceurs peuvent ensuite [activer des audiences dans un projet](../collaborate/activate.md), qui sont envoyées à la destination configurée de l’éditeur.

>[!IMPORTANT]
>
>Actuellement, lorsque les annonceurs activent des audiences dans votre projet, elles sont automatiquement envoyées à la destination configurée par l’éditeur. En tant qu’éditeur, vous **devez** configurer une destination *avant* que votre collaborateur active une audience. Si aucune destination n’est configurée, l’audience vous sera envoyée et visible dans l’onglet **[!UICONTROL Activer]** au sein d’un projet, mais elle ne sera pas activée.

## Configuration des destinations {#configure-destinations}

Pour configurer une destination, accédez à **[!UICONTROL Configuration]** puis sélectionnez l’onglet **[!UICONTROL Mes destinations]**. Ici, vous pouvez afficher toutes les destinations disponibles.

>[!NOTE]
>
> Actuellement, seul Adobe Experience Platform est disponible en tant que destination en libre-service dans Real-Time CDP Collaboration. Si vous souhaitez configurer une destination telle qu’Amazon S3 ou Snowflake, contactez votre représentant ou représentante Adobe.

![L’onglet Mes destinations de l’espace de travail Configuration affiche les destinations disponibles.](/help/assets/destinations/overview/my-destinations-overview.png)

Pour commencer à configurer une destination, sélectionnez l’option **[!UICONTROL Configurer]** dans la destination de votre choix. Pour plus d’informations sur la configuration de destinations spécifiques, reportez-vous aux guides dans le tableau [destinations disponibles](#available-destinations).

![L’espace de travail Mes destinations avec l’option Configurer mise en surbrillance pour la destination Adobe Experience Platform.](/help/assets/destinations/overview/my-destinations-set-up.png)

### Destinations disponibles {#available-destinations}

Les destinations suivantes peuvent être configurées dans Real-Time CDP Collaboration. Pour afficher le guide de configuration de cette destination, sélectionnez le nom de la destination dans le tableau ci-dessous. Si vous souhaitez configurer une destination qui n’est pas actuellement disponible, contactez votre représentant ou représentante Adobe.

| Destination | Disponibilité |
| --- | --- |
| [Adobe Experience Platform](./experience-platform.md) | Disponible |
| Amazon S3 | Bientôt disponible. |
| Snowflake | Bientôt disponible. |
| Google Cloud Storage | Bientôt disponible. |
| Stockage Azure Blob | Bientôt disponible. |

## Étapes suivantes

Une fois la destination configurée, vous pouvez commencer à [activer les audiences ciblées](../collaborate/activate.md) dans vos projets.
