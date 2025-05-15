---
title: Gérer les connexions de données
description: Découvrez comment gérer les connexions de données, notamment les clés de correspondance, la planification, les cas d’utilisation et le filtrage d’audience dans Real-Time CDP Collaboration
audience: administrator, data engineer
badgelimitedavailability: label="Disponibilité limitée" type="Informative" url="https://helpx.adobe.com/fr/legal/product-descriptions/real-time-customer-data-platform-collaboration.html newtab=true"
exl-id: d142d3ed-f56a-4150-a885-571728a73ac8
source-git-commit: 8d620828bb0fb0bf116396f884b1bbd35d7c5d69
workflow-type: tm+mt
source-wordcount: '439'
ht-degree: 18%

---

# Gérer les connexions de données

{{limited-availability-release-note}}

## Vue d’ensemble

Utilisez les connexions de données dans Real-Time CDP Collaboration pour importer des audiences provenant de diverses sources. Découvrez comment gérer les clés de correspondance et planifier des importations de données pour vos connexions de données existantes. De plus, vous pourrez filtrer les audiences en fonction de différents attributs pour obtenir des informations plus granulaires.

## Afficher les connexions de données

Pour afficher les connexions de données existantes, accédez à **[!UICONTROL Configuration]** puis sélectionnez l’onglet **[!UICONTROL Mes connexions de données]**. Toutes vos connexions de données actuelles sont affichées, affichant un bref aperçu pour chaque connexion. Pour obtenir une vue complète des informations d’une connexion de données, y compris ses clés de correspondance, les détails de planification et les audiences, sélectionnez **[!UICONTROL Afficher la connexion de données]** sur la connexion correspondante.

![Configurer l’espace de travail avec la vue de l’onglet Mes connexions de données affichée et mise en surbrillance.](/help/assets/setup/manage-data-connection/my-data-connections.png){zoomable="yes"}

### Clés correspondantes {#match-keys}

>[!CONTEXTUALHELP]
>id="rtcdp_collaboration_manage_dataconnections_matchkeys"
>title="Clés correspondantes"
>abstract="Les clés de correspondance déterminent la manière dont les données provenant de différentes sources seront mises en correspondance. Sélectionnez les clés correspondantes les plus pertinentes pour vos cas d’utilisation et vos directives de confidentialité."

Les clés correspondantes sont des identifiants utilisés pour réconcilier des membres d’audiences provenant de différentes sources de données. Vous ne pouvez pas modifier les clés de correspondance que vous avez initialement sélectionnées pour votre connexion aux données.

Les clés de correspondance disponibles sont les suivantes :

- **E-mail haché**

![Un espace de travail des connexions de données avec la section Clés de correspondance mise en surbrillance.](/help/assets/setup/manage-data-connection/view-data-connection-match-keys.png){zoomable="yes"}

### Planification {#scheduling}

>[!CONTEXTUALHELP]
>id="rtcdp_collaboration_manage_dataconnections_scheduling"
>title="Planification"
>abstract="Cette vue affiche les options de planification que vous avez sélectionnées au départ pour votre connexion aux données."

Vous ne pouvez pas modifier les options de planification que vous avez sélectionnées initialement pour votre connexion aux données. Pour plus d’informations sur les options de planification, consultez la [section de planification](/help/guide/setup/onboard-audiences.md#schedule) dans le document du workflow d’importation d’audience.

![Espace de travail des connexions de données avec la section Planification mise en surbrillance.](/help/assets/setup/manage-data-connection/view-data-connection-scheduling.png){zoomable="yes"}

## Supprimer la connexion de données

La suppression d’une connexion de données supprimera toutes les audiences sous-jacentes, les paramètres associés et l’utilisation sur la plateforme. Cette action ne peut pas être annulée.

Pour supprimer une connexion de données existante, sélectionnez l’icône de suppression (![icône Supprimer](/help/assets/common/delete.svg)) dans l’espace de travail d’une connexion de données individuelle.

![Un espace de travail des connexions de données avec l’option de suppression mise en surbrillance.](/help/assets/setup/manage-data-connection/delete-data-connection.png){zoomable="yes"}

Une boîte de dialogue de confirmation s’affiche. Sélectionnez **[!UICONTROL Supprimer]** pour terminer la suppression de la connexion de données.

![Boîte de dialogue Supprimer la connexion de données avec l’option Supprimer mise en surbrillance.](/help/assets/setup/manage-data-connection/delete-data-connection-confirm.png){zoomable="yes"}

## Gérer des audiences {#manage-audiences}

Une liste des audiences associées à la connexion de données s’affiche au bas de l’espace de travail. La liste affiche un bref aperçu de chaque audience, y compris son statut, sa source et son accès à la connexion. Pour modifier les catégories d’une audience, l’accès à la connexion ou la visibilité des métadonnées, sélectionnez le nom de l’audience. Pour obtenir un guide complet sur la gestion d’une audience, reportez-vous au guide [Afficher des audiences individuelles](./onboard-audiences.md#view-individual-audiences) .

![Espace de travail des connexions de données avec les audiences en surbrillance.](/help/assets/setup/manage-data-connection/view-data-connection-manage-audiences.png){zoomable="yes"}

## Étapes suivantes

Après avoir géré vos connexions de données, vous pouvez [découvrir des chevauchements](/help/guide/collaborate/discover.md) entre vos audiences et les audiences que votre collaborateur a rendues détectables.
