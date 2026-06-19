---
title: Présentation des sources
description: En savoir plus sur les connecteurs source dans Adobe Real-Time CDP Collaboration
audience: admin, publisher, advertiser
source-git-commit: b30d1b01e929e586404faac34650c7fd479d071b
workflow-type: tm+mt
source-wordcount: '400'
ht-degree: 6%

---

# Présentation des sources

Dans Adobe Real-Time CDP Collaboration, les données d’audience proviennent d’une source (ou d’une connexion aux données). Vous pouvez vous connecter à différents types de sources tels que des applications Adobe, des stockages dans le cloud ou des fichiers à partir de votre système local pour [sourcer et gérer des audiences](./onboard-audiences.md) pour vos projets Collaboration. Au cours du workflow d’approvisionnement des audiences, vous pouvez choisir et configurer votre source préférée en fonction des besoins de votre entreprise.

## Connecter une source {#connect-a-source}

Pour connecter une source, vous devez entrer dans le workflow de sourcing. Tout d’abord, accédez à l’onglet **[!UICONTROL Mes audiences]** dans l’espace de travail **[!UICONTROL Configuration]**.

Sélectionnez l’icône d’ajout (![Ajouter une icône.](/help/assets/icons/plus.png)) puis sélectionnez **[!UICONTROL Audience]** pour démarrer le workflow de sourcing.

![Espace de travail Mes audiences avec l’option Ajouter et les options Audiences mises en surbrillance.](/help/assets/setup/add-manage-audiences/add-audiences.png)

Au cours du workflow, vous serez invité à ajouter une nouvelle connexion de données en sélectionnant une source. La source que vous choisissez détermine la manière dont les données d’audience sont importées dans Collaboration. Consultez le tableau [sources disponibles](#available-sources) pour obtenir la liste de toutes les sources prises en charge.

![L’espace de travail Ajouter des audiences avec l’option Ajouter une nouvelle connexion de données mise en surbrillance.](/help/assets/setup/add-manage-audiences/add-data-connection.png)

Après avoir sélectionné une source, le workflow vous guide tout au long des étapes de configuration spécifiques à la connexion, notamment l’authentification, le mappage des champs, la planification et la sélection d’audiences.

### Sources disponibles {#available-sources}

Les sources ci-dessous sont disponibles dans Collaboration. Pour afficher le guide d’approvisionnement détaillé pour cette source, sélectionnez le nom de la source dans le tableau ci-dessous. Si vous souhaitez consulter une source qui n’est pas disponible actuellement, contactez votre représentant ou représentante Adobe.

| Source | Description | Disponibilité |
| --- | --- | --- |
| [Adobe Experience Platform](./onboard-audiences.md) | Importez les audiences de votre instance Experience Platform connectée et réutilisez les segments de clients existants. | Disponible |
| [Amazon S3](./configure-aws-s3-audience-sourcing.md) | Connectez vos compartiments S3 à la source de jeux de données propriétaires volumineux à partir de votre infrastructure cloud. | Disponible |
| [[!DNL Snowflake]](./configure-snowflake-audience-sourcing.md) | Connectez votre [!DNL Snowflake Secure Data Share] pour importer des jeux de données d’audience à grande échelle. | Disponible |
| [[!DNL Google Cloud Storage]](./configure-gcs-audience-sourcing.md) | Connectez vos compartiments GCS pour importer les données d’audience stockées dans votre environnement [!DNL Google Cloud]. | Disponible |
| [Chargement de fichier CSV](./upload-csv-audience-sourcing.md) | Chargez un fichier CSV formaté directement depuis votre système local. | Disponible |
| Adobe Audience Manager | Insérez des segments Audience Manager existants dans vos projets Collaboration. | *Bientôt disponible* |
| [[!DNL Azure Blob Storage]](./configure-azure-storage-audience-sourcing.md) | Connectez vos conteneurs [!DNL Azure Blob Storage] aux jeux de données propriétaires sources de votre environnement [!DNL Microsoft Azure]. | Disponible |
| [[!DNL Azure Data Lake Storage]](./configure-azure-storage-audience-sourcing.md) | Connectez votre compte [!DNL Azure Data Lake Storage Gen 2] pour importer les données d’audience stockées dans votre lac de données [!DNL Azure]. | Disponible |

{style="table-layout:auto"}

## Étapes suivantes

Après avoir connecté une source et importé vos audiences, vous pouvez afficher les détails, mettre à jour les configurations ou supprimer des sources existantes. Pour plus d’informations, consultez le guide [Gérer les connexions aux données](./manage-data-connection.md).
