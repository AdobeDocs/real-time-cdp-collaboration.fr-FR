---
title: Charger un fichier CSV pour l’Audience Sourcing
description: Découvrez comment charger votre fichier CSV en tant que source de données en libre-service pour ingérer les données d’audience dans Real-Time CDP Collaboration.
source-git-commit: 96d3f87cedcfde73ce01c2b53c0b2ce4365fd277
workflow-type: tm+mt
source-wordcount: '1084'
ht-degree: 0%

---

# Charger un fichier CSV pour l’audience

Ce guide décrit les étapes à suivre pour charger un fichier CSV dans l’interface utilisateur d’Adobe Real-Time CDP Collaboration afin de générer les données de votre audience pour les utiliser dans des projets de collaboration.

## Vue d’ensemble {#overview}

Le chargement de fichier CSV est une méthode permettant de générer des données d’audience propriétaires pour des projets de collaboration. Il s’agit d’une alternative à la [connexion de votre compartiment AWS S3](./configure-aws-s3-audience-sourcing.md) ou [approvisionnement des audiences à partir d’Experience Platform](./onboard-audiences.md).

Suivez ce workflow pour charger un fichier CSV contenant les données de votre audience dans la source et gérez les audiences propriétaires dans Collaboration. Vous pouvez mapper des champs d’identité pour l’activation et l’analyse de chevauchement. Une fois votre fichier chargé et traité, l’audience source est disponible dans l’espace de travail **[!UICONTROL Mes audiences]**, où vous pouvez vérifier, activer et gérer vos projets de collaboration.

>[!IMPORTANT]
>
>* Les audiences provenant du téléchargement d’un fichier CSV sont disponibles pendant 7 jours **&#x200B;**. Au-delà de cette période, l’audience expire et doit être rechargée pour être utilisée dans vos projets de collaboration.
>
>* Vous pouvez charger un fichier CSV par session à ce stade. Pour ajouter des audiences supplémentaires, effectuez à nouveau le workflow de chargement pour chaque fichier que vous souhaitez approvisionner.

## Conditions préalables {#prerequisites}

Avant de pouvoir charger des fichiers CSV pour l’approvisionnement de l’audience, vérifiez que vous disposez des éléments suivants :

* Intégration du compte terminée dans Real-Time CDP Collaboration. Consultez [Intégration de votre compte](./onboard-account.md) pour obtenir des instructions détaillées.
* Les autorisations nécessaires pour ajouter des audiences dans votre organisation.
* Un fichier CSV contenant les données de votre audience avec des champs d’identité tels que l’e-mail ou le téléphone.

## Chargement d’un fichier CSV {#upload-csv-file}

Dans l’onglet **[!UICONTROL Mes audiences]** de l’espace de travail **[!UICONTROL Configuration]**, sélectionnez l’icône d’ajout (![icône d’ajout).](/help/assets/icons/plus.png)), puis sélectionnez **[!UICONTROL Audience]**.

S’il s’agit de votre première audience, vous pouvez également sélectionner l’option **[!UICONTROL Ajouter]**.

![L’onglet Mes audiences dans l’espace de travail Configuration avec l’icône d’ajout et l’option Ajouter une audience affichées.](../../assets/setup/add-manage-audiences/add-audiences.png)

Le workflow Ajouter une audience s’affiche. Sélectionnez **[!UICONTROL Ajouter une nouvelle connexion de données]** puis sélectionnez **[!UICONTROL Suivant]**.

![L’espace de travail Ajouter des audiences avec l’option Ajouter une nouvelle connexion de données mise en surbrillance.](../../assets/setup/add-manage-audiences/add-data-connection.png){zoomable="yes"}

### Sélectionnez Fichier CSV comme connexion de données {#select-csv-file}

Sélectionnez **[!UICONTROL Fichier CSV]** comme connexion de données, puis **[!UICONTROL Suivant]**.

![Écran de sélection de la connexion aux données avec le fichier CSV disponible sous forme d’option sélectionnable.](../../assets/setup/csv-audience-sourcing/select-csv-data-connection.png)

### Sélectionner un fichier {#select-file}

Choisissez **[!UICONTROL Sélectionner à partir de l’ordinateur]** pour charger un fichier CSV à partir de votre système local. Vous pouvez également faire glisser et déposer le fichier CSV que vous souhaitez charger dans le panneau [!UICONTROL Glisser-déposer un fichier CSV].

>[!IMPORTANT]
>
>Seuls les fichiers CSV sont pris en charge. La taille de fichier maximale est de **2 Go**.

![Sélectionnez un fichier CSV contenant les données d’audience de votre système local.](../../assets/setup/csv-audience-sourcing/select-file.png)

Une fois le chargement effectué, l’interface utilisateur affiche un résumé comprenant le nombre de colonnes, un nombre de lignes estimé, la structure du fichier et un aperçu des 10 premières lignes de données.

Vérifiez le résumé, puis sélectionnez **[!UICONTROL Suivant]**.

![Prévisualisez les exemples de données d’audience à partir de votre fichier CSV.](../../assets/setup/csv-audience-sourcing/preview-sample-data.png)

#### Remplacer le fichier {#replace-file}

Si vous devez charger un autre fichier CSV, choisissez **[!UICONTROL Remplacer le fichier]** et sélectionnez votre nouveau fichier. L’interface s’actualise ensuite pour afficher un résumé mis à jour des nouvelles données.

Après avoir consulté le résumé révisé, sélectionnez **[!UICONTROL Suivant]**.

![Sélectionnez l’option Remplacer le fichier pour charger un autre fichier CSV.](../../assets/setup/csv-audience-sourcing/replace-file.png)

### Confirmer l’accusé de réception du consentement {#confirm-consent}

Avant de poursuivre, vous devez reconnaître que les désinscriptions au consentement ont été supprimées de vos données d’audience. Collaboration requiert des données d’audience propres sans utilisateurs qui se sont opposés au partage de données.

Cochez la case de confirmation suivie de **[!UICONTROL OK]** pour confirmer. La boîte de dialogue se ferme alors et vous passez à l’écran de mappage des champs.

![La boîte de dialogue d’accusé de réception de désinscription au consentement nécessite une confirmation avant de continuer.](../../assets/setup/csv-audience-sourcing/consent-optout-acknowledgment.png)

### Mapper les champs d’identité source {#map-fields}

Le mappage des champs détermine la manière dont Collaboration utilise les données d’audience pour l’activation et l’analyse de chevauchement. Sur l’écran **[!UICONTROL Mapper les champs]**, utilisez les menus déroulants pour mapper chaque champ d’identité source de votre fichier CSV au champ cible approprié dans Collaboration.

Si vous avez besoin d’informations supplémentaires sur un champ cible, y compris le type de données ou la description, sélectionnez **[!UICONTROL Détails des champs cibles]** pour plus d’informations.

![Liste déroulante pour mapper un champ d’identité source de vos données d’audience CSV au champ cible dans Collaboration.](../../assets/setup/csv-audience-sourcing/map-fields.png)

Examinez ensuite les champs mappés, puis sélectionnez **[!UICONTROL Suivant]**.

![Écran de mappage des champs affichant les champs d’identité source et cible mappés.](../../assets/setup/csv-audience-sourcing/confirm-mapped-fields.png)

### Vérifier et terminer le chargement {#review-and-complete}

L’écran **[!UICONTROL Révision]** s’affiche avec un résumé des paramètres d’audience de votre fichier CSV. Consultez les informations dans les sections suivantes :

* **[!UICONTROL Informations sur le fichier]** : affiche le nom du fichier, le nombre de colonnes et le nombre estimé de lignes.
* **[!UICONTROL Mappage]** : répertorie la manière dont les champs sources du fichier d’audience chargé (par exemple, `email`) sont mappés aux champs cibles utilisés dans Collaboration (par exemple, e-mail haché).

Sélectionnez l’icône en forme de crayon si vous devez modifier une section. Sélectionnez **[!UICONTROL Terminé]** pour confirmer toutes les sections.

![Consultez le résumé des paramètres de chargement, y compris les informations sur le fichier CSV et les détails du mappage des champs.](../../assets/setup/csv-audience-sourcing/review-upload-summary.png)

Une barre de progression s’affiche sous les sections de résumé pour indiquer la progression du chargement. Une fois le chargement terminé, une boîte de dialogue de confirmation confirme que votre audience CSV a été créée et que le sourcing de l’audience est en cours.

![Après le chargement du fichier, une boîte de dialogue de confirmation s’affiche indiquant que l’audience CSV a été créée et que le sourcing de l’audience est en cours.](../../assets/setup/csv-audience-sourcing/upload-success-sourcing-in-progress.png)

## Vérifier les audiences sources {#review-sourced-audiences}

Après avoir chargé votre fichier CSV, Collaboration commence à sourcer les audiences à partir du fichier . Ce processus peut prendre plusieurs minutes. Une fois le sourcing terminé, vos audiences sont disponibles dans l’onglet **[!UICONTROL Mes audiences]** avec les mêmes fonctionnalités et informations que les audiences provenant d’Experience Platform.

![L’onglet Audiences affichant une liste des audiences sources dans la vue Grille.](../../assets/setup/csv-audience-sourcing/csv-audiences-list.png)

En mode Grille ou Tableau, sélectionnez un élément de ligne ou **[!UICONTROL Afficher l’audience]** pour afficher un aperçu d’une audience spécifique. Il affiche le statut, la source et le nom de connexion aux données de l’audience, ainsi que des panneaux détaillés pour :

**[!UICONTROL Identités]** : affiche le nombre total d’identités et leur répartition une fois que les données sont disponibles.
**[!UICONTROL Catégories]** : affiche toutes les balises utilisées pour organiser ou filtrer l’audience.
**[!UICONTROL Accès de connexion]** : indique si l’audience est privée, publique ou partagée avec des collaborateurs spécifiques.
**[!UICONTROL Visibilité des métadonnées]** : affiche les informations d’audience (telles que le nombre d’identités, le pourcentage de chevauchement et l’index) visibles par les collaborateurs.

Utilisez cette vue pour confirmer les paramètres de configuration et de visibilité de l’audience avant d’utiliser l’audience dans des projets de collaboration. Pour plus d’informations, voir [Comment afficher une audience individuelle](./onboard-audiences.md#view-individual-audiences).

## Étapes suivantes {#next-steps}

Vous avez chargé votre fichier CSV dans Collaboration. Une fois l’approvisionnement terminé, vous pouvez :

* Créez des projets de collaboration avec vos audiences sources. Voir [Découvrir les audiences](../../guide/collaborate/discover.md).
* Activez les audiences vers des destinations connectées. Voir [&#x200B; Activer les audiences](../../guide/collaborate/activate.md).
* Examinez les chevauchements et les informations sur les audiences. Voir [Mesure des performances de la campagne](../../guide/collaborate/measure.md).
* Gérez les paramètres et la visibilité de votre audience. Voir [Source et gérer les audiences](./onboard-audiences.md).

Pour plus d’informations sur les autres méthodes de sourcing d’audience, consultez [Configuration d’AWS S3 pour le sourcing d’audience](./configure-aws-s3-audience-sourcing.md) ou [Audiences Source à partir d’Experience Platform](./onboard-audiences.md).
