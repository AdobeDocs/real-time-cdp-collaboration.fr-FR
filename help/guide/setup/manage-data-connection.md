---
title: Gérer les connexions de données
description: Découvrez comment gérer les connexions de données, notamment les clés de correspondance, la planification, les cas d’utilisation et le filtrage d’audience dans Real-Time CDP Collaboration
audience: administrator, data engineer
badgelimitedavailability: label="Disponibilité limitée" type="Informative" url="https://helpx.adobe.com/legal/product-descriptions/real-time-customer-data-platform-collaboration.html newtab=true"
exl-id: d142d3ed-f56a-4150-a885-571728a73ac8
source-git-commit: acaaaa1e1fab981d874210639c16e76e48fc3394
workflow-type: tm+mt
source-wordcount: '428'
ht-degree: 6%

---

# Gérer les connexions de données

{{limited-available-release-note}}

## Vue d’ensemble

Utilisez les connexions de données dans Real-Time CDP Collaboration pour importer des audiences provenant de diverses sources. Découvrez comment gérer les clés de correspondance et planifier des importations de données pour vos connexions de données existantes. De plus, vous pourrez filtrer les audiences en fonction de différents attributs pour obtenir des informations plus granulaires.

Avant de gérer vos connexions de données ici, vous devez d’abord les configurer pendant le [workflow d’intégration d’audience](./onboard-audiences.md). Vous aurez ainsi la garantie que les sources de données appropriées sont connectées pour être utilisées dans Real-Time CDP Collaboration.

## Afficher les connexions de données

>[!IMPORTANT]
>
>La suppression d’une connexion de données n’est actuellement pas prise en charge dans l’interface utilisateur de Real-Time CDP Collaboration. Pour supprimer une connexion de données, contactez votre représentant Adobe ou [créez un ticket de service clientèle](https://experienceleague.adobe.com/home?lang=en&amp;support-tab=open-ticket#support){target="_blank"}{target=« _blank »}.

Pour afficher les connexions de données existantes, accédez à **[!UICONTROL Configuration]** > **[!UICONTROL Mes audiences]**, puis sélectionnez **[!UICONTROL Gérer les connexions de données]**.

![Configurer l’espace de travail avec l’option Gérer les connexions de données mise en surbrillance.](/help/assets/setup/manage-data-connection/manage-data-connection-highlighted.png){zoomable="yes"}{zoomable=&quot;yes&quot;}

Toutes les connexions de données actuellement configurées sont ainsi affichées, avec des informations sur le nombre d’audiences dans chacune d’elles, la source de la connexion de données, etc. Sélectionnez **[!UICONTROL Afficher la connexion de données]** pour afficher des informations sur les clés de correspondance, la planification et les audiences qui font partie de cette connexion de données.

![Espace de travail Gérer les connexions de données avec une connexion Afficher les connexions de données en surbrillance. ](/help/assets/setup/manage-data-connection/view-data-connection-highlighted.png){zoomable="yes"}{zoomable=&quot;yes&quot;}

### Clés de correspondance {#match-keys}

>[!CONTEXTUALHELP]
>id="rtcdp_collaboration_manage_dataconnections_matchkeys"
>title="Clés de correspondance"
>abstract="Les clés de correspondance déterminent la manière dont les données provenant de différentes sources seront mises en correspondance. Sélectionnez les clés de correspondance les plus pertinentes pour vos cas d’utilisation et vos directives de confidentialité."

Les clés de correspondance sont des identifiants utilisés pour réconcilier des membres d’audiences provenant de différentes sources de données. Les clés de correspondance disponibles sont les suivantes :

- **E-mail haché**

Vous ne pouvez pas modifier les clés de correspondance utilisées dans cette connexion de données.

![Un espace de travail des connexions de données avec la section Clés de correspondance mise en surbrillance.](/help/assets/setup/manage-data-connection/view-data-connection-match-keys.png){zoomable="yes"}{zoomable=&quot;yes&quot;}

### Planification {#scheduling}

>[!CONTEXTUALHELP]
>id="rtcdp_collaboration_manage_dataconnections_scheduling"
>title="Planification"
>abstract="Cette vue affiche les options de planification que vous avez sélectionnées initialement pour votre connexion aux données."

Vous ne pouvez pas modifier les options de planification que vous avez sélectionnées initialement pour votre connexion aux données. Pour plus d’informations sur les options de planification, consultez la [section de planification](/help/guide/setup/onboard-audiences.md#schedule) dans le document du workflow d’importation d’audience.

![Espace de travail des connexions de données avec la section Planification mise en surbrillance.](/help/assets/setup/manage-data-connection/view-data-connection-scheduling.png){zoomable="yes"}{zoomable=&quot;yes&quot;}

## Gérer des audiences {#manage-audiences}

Lors de l’affichage de la liste des audiences de votre connexion de données, vous pouvez choisir d’afficher les audiences, de modifier leurs catégories ou de les supprimer de la connexion de données.

![Espace de travail des connexions de données avec les audiences en surbrillance.](/help/assets/setup/manage-data-connection/view-data-connection-manage-audiences.png){zoomable="yes"}{zoomable=&quot;yes&quot;}

## Étapes suivantes

Après avoir géré vos connexions de données, vous pouvez [découvrir des chevauchements](/help/guide/collaborate/discover.md) entre vos audiences et les audiences que votre collaborateur a rendues détectables.
