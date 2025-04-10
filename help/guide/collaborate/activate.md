---
title: Activer les audiences
description: En tant qu’éditeur, apprenez à activer dans les campagnes les audiences partagées avec vous par votre collaborateur.
audience: admin, publisher
badgelimitedavailability: label="Disponibilité limitée" type="Informative" url="https://helpx.adobe.com/legal/product-descriptions/real-time-customer-data-platform-collaboration.html newtab=true"
exl-id: fd82fcbf-ab39-48e0-9438-0a9046693431
source-git-commit: acaaaa1e1fab981d874210639c16e76e48fc3394
workflow-type: tm+mt
source-wordcount: '268'
ht-degree: 3%

---

# Activer les audiences

{{limited-availability-release-note}}

>[!IMPORTANT]
>
>L’espace de travail **[!UICONTROL Activer]** n’est disponible que si vous êtes un éditeur et que le cas d’utilisation **Partage et activation d’audience** a été activé [pendant le processus de connexion](../connect/establishing-connections.md#connection-settings). Pour plus d’informations sur les cas d’utilisation, consultez le guide [gestion des projets](./manage-projects.md#project-use-cases).

En tant qu’éditeur, découvrez comment activer des audiences à l’aide d’Adobe Real-Time CDP Collaboration. Actuellement, vous pouvez activer des audiences vers des emplacements Amazon S3. D’autres canaux d’activation sont prévus.

Seules les **organisations d’éditeurs** peuvent activer des audiences pour les campagnes. Les organisations publicitaires peuvent [partager des audiences](/help/guide/collaborate/share.md) avec les éditeurs, qui les activeront dans les projets. En savoir plus sur le [workflow de bout en bout](/help/guide/end-to-end-workflow.md) pour les annonceurs et les éditeurs.

## Conditions préalables {#prerequisites}

En tant qu’éditeur utilisant Real-Time CDP Collaboration, vous devez d’abord travailler avec l’équipe d’activation et d’ingénierie Adobe pour configurer une connexion à l’emplacement Amazon S3 souhaité. Une fois cette configuration terminée, vous pouvez activer ou exporter des audiences de Real-Time CDP Collaboration vers votre emplacement Amazon S3. Contactez votre représentant Adobe pour lancer ce workflow.

En outre, le cas d’utilisation **Partage et activation d’audience** doit être activé pour votre connexion.

## Comportement d’activation {#activation-behavior}

Une fois que la connexion de votre annonceur a partagé une audience pour activation, celle-ci s’affiche immédiatement dans votre vue **[!UICONTROL Activer]**. L’audience sera exportée vers l’emplacement indiqué à l’intervalle défini par l’annonceur dans son écran de partage d’audience.

![Activer le workflow vers une destination Amazon S3.](/help/assets/collaborate/activate/activate-to-amazon-s3.png)

## Étapes suivantes {#next-steps}

Après avoir activé les données et exécuté des campagnes, travaillez avec l’équipe d’activation et d’ingénierie d’Adobe pour charger les données de mesure et afficher les [rapports de mesure](/help/guide/collaborate/measure.md) correspondants.
