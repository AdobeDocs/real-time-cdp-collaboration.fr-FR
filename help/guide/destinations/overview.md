---
title: Présentation des destinations
description: En savoir plus sur les destinations dans Real-Time CDP Collaboration.
audience: admin, publisher
badgelimitedavailability: label="Disponibilité limitée" type="Informative" url="https://helpx.adobe.com/legal/product-descriptions/real-time-customer-data-platform-collaboration.html newtab=true"
exl-id: 5cbbf5c4-4caa-40da-97be-690d95c1201c
TQID: https://experienceleague.adobe.com/1VvnSt3Z65dfQBfXnjJJi3H0Oj9BxFStexq3icVKxkY
product_v2:
  - id: fdddec33-c9cb-4459-b8b6-2664395a6f10
topic_v2:
  - id: b5520579-b31f-4df7-9281-f0d9f91e2edc
  - id: e1e0219c-f879-479f-8427-888ed2a6e9c2
source-git-commit: 7ab1bc21a4d644e2e6a481d8de594d6a509a92a5
workflow-type: tm+mt
source-wordcount: 273
ht-degree: 7%

---

# Présentation des destinations

{{limited-availability-release-note}}

>[!NOTE]
>
>Cette page couvre les destinations vers lesquelles les audiences sont activées **vers**, telles que les plateformes de stockage dans le cloud. Pour activer des audiences **vers un collaborateur** dans un projet partagé, reportez-vous au guide [Activation des audiences](/help/guide/collaborate/activate.md).

Les destinations sont des intégrations utilisées pour envoyer des audiences ciblées à des plateformes externes. Ces intégrations vous permettent d’activer des audiences sur divers canaux et plateformes marketing à utiliser dans les campagnes et l’engagement des clients.

Les collaborateurs peuvent configurer des destinations pour envoyer des audiences à des plateformes externes, telles que Adobe Experience Platform ou une plateforme de stockage dans le cloud, en vue de les utiliser dans des campagnes. Les collaborateurs peuvent ensuite [activer des audiences dans un projet](../collaborate/activate.md), qui sont envoyées à la destination configurée de leur connexion. L’activation peut être effectuée par l’un des collaborateurs en fonction des paramètres d’activation de l’audience [configurés dans la connexion](/help/guide/connect/establishing-connections.md#configure-connection-settings).

>[!IMPORTANT]
>
>Actuellement, lorsque les collaborateurs activent des audiences dans un projet, elles sont automatiquement envoyées à la destination configurée de leur connexion. Vous **devez** configurer une destination avant que votre collaborateur puisse activer des audiences dans un projet.

## Destinations disponibles {#available-destinations}

Les destinations suivantes peuvent être configurées dans Collaboration. Pour afficher le guide de configuration de cette destination, sélectionnez le nom de la destination dans le tableau ci-dessous.

| Destination | Disponibilité |
| --- | --- |
| [Adobe Experience Platform](./experience-platform.md) | Disponible |
| [[!DNL Amazon S3]](./manage-destinations.md) | Disponible |
| [[!DNL Snowflake]](./manage-destinations.md) | Disponible |
| [[!DNL Google Cloud Storage]](./manage-destinations.md) | Disponible |
| [[!DNL Azure Blob Storage]](./manage-destinations.md) | Disponible |
| [[!DNL SFTP]](./manage-destinations.md) | Disponible |
| [[!DNL Data Landing Zone]](./manage-destinations.md) | Disponible |

>[!NOTE]
>
>**[!DNL Google Cloud Storage]** dans ce tableau fait référence aux **destinations** (où Collaboration envoie des audiences lors de l’activation). Pour **approvisionner les audiences à partir de** un compartiment GCS dans l’espace de travail **[!UICONTROL Configuration]**, consultez [Configurer GCS pour l’approvisionnement des audiences](../setup/configure-gcs-audience-sourcing.md).

## Étapes suivantes

Pour configurer une destination, reportez-vous au guide [configurer et gérer une destination](./manage-destinations.md). Une fois la destination configurée, vous pouvez commencer à [activer les audiences ciblées](../collaborate/activate.md) dans vos projets.
