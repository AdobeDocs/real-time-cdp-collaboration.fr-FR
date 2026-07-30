---
title: Exigences de connexion de destination
description: Passez en revue les informations de connexion requises pour configurer les destinations prises en charge dans Real-Time CDP Collaboration.
audience: admin, publisher
source-git-commit: c84582bb81289ce761c664af7db177535ff00a00
workflow-type: tm+mt
source-wordcount: '610'
ht-degree: 1%

---

# Exigences de connexion de destination

Avant de configurer une destination dans Real-Time CDP Collaboration, obtenez les informations d’identification et de connexion requises par le fournisseur de destination.

Cette page résume les méthodes d’authentification disponibles dans Collaboration. Pour plus d’informations sur la création d’informations d’identification, l’attribution d’autorisations, la configuration de l’accès réseau ou la préparation du système de destination, consultez la documentation sur la destination Adobe Experience Platform associée.

>[!NOTE]
>
>La documentation Adobe Experience Platform associée décrit le workflow de destination standard. Certaines étapes, certains champs ou certaines options peuvent ne pas s’appliquer lors de la configuration de la destination dans Real-Time CDP Collaboration.

## Aperçu des exigences {#requirements-at-a-glance}

| Destination | Méthode d&#39;authentification ou de connexion | Préparer avant de commencer | Exigences détaillées |
|---|---|---|---|
| [!DNL Amazon S3] | Clé d&#39;accès et clé secrète, ou rôle assumé | Paire de clés d’accès AWS ou ARN du rôle IAM ; informations de compartiment et de dossier | [[!DNL Amazon S3] documentation de destination](https://experienceleague.adobe.com/en/docs/experience-platform/destinations/catalog/cloud-storage/amazon-s3) |
| SFTP | Mot de passe ou clé SSH | Domaine du serveur, port, nom d’utilisateur, informations d’authentification et chemin d’accès au dossier | [Documentation sur la destination SFTP](https://experienceleague.adobe.com/en/docs/experience-platform/destinations/catalog/cloud-storage/sftp) |
| [!DNL Azure Blob Storage] | Chaîne de connexion | Informations sur la chaîne de connexion de stockage, le conteneur et le dossier Azure | [[!DNL Azure Blob Storage] documentation de destination](https://experienceleague.adobe.com/en/docs/experience-platform/destinations/catalog/cloud-storage/azure-blob) |
| [!DNL Google Cloud Storage] | ID de clé d’accès et clé d’accès secrète | Informations d’identification d’interopérabilité [!DNL Google Cloud Storage], compartiment et dossier | [[!DNL Google Cloud Storage] documentation de destination](https://experienceleague.adobe.com/en/docs/experience-platform/destinations/catalog/cloud-storage/google-cloud-storage) |
| [!DNL Snowflake Batch] | Partage de données [!DNL Snowflake] | ID de compte [!DNL Snowflake], région, statut de lien privé et accès aux annonces privées | [[!DNL Snowflake Batch] documentation de destination](https://experienceleague.adobe.com/en/docs/experience-platform/destinations/catalog/warehouse/snowflake-batch) |
| [!DNL Data Landing Zone] | Aucune authentification distincte requise | Préférences de sortie du dossier de destination et du fichier | [[!DNL Data Landing Zone] documentation de destination](https://experienceleague.adobe.com/en/docs/experience-platform/destinations/catalog/cloud-storage/data-landing-zone) |

## Notes du connecteur {#connector-notes}

Examinez les méthodes d’authentification spécifiques au connecteur et les différences de workflow suivantes avant de configurer une destination.

### [!DNL Amazon S3] {#amazon-s3}

Collaboration prend en charge l’authentification **[!UICONTROL Clé d’accès]** et **[!UICONTROL Rôle assumé]**. L’authentification par clé d’accès nécessite une clé d’accès et une clé d’accès secrète. L’authentification par rôle assumé nécessite l’ARN d’un rôle AWS IAM qu’Adobe peut assumer.

Pour la configuration des informations d’identification, des rôles et des autorisations, voir [Authentification à la  [!DNL Amazon S3]  de destination](https://experienceleague.adobe.com/en/docs/experience-platform/destinations/catalog/cloud-storage/amazon-s3#authenticate).

### SFTP {#sftp}

Collaboration prend en charge l’authentification **[!UICONTROL SFTP avec mot de passe]** et **[!UICONTROL SFTP avec clé SSH]**. Les deux méthodes nécessitent le domaine, le port et le nom d’utilisateur du serveur. Le port est défini par défaut sur `22`.

Pour connaître les exigences en matière de format de clé SSH, de serveur, de réseau et de place sur la liste autorisée, voir [Informations d’authentification SFTP](https://experienceleague.adobe.com/en/docs/experience-platform/destinations/catalog/cloud-storage/sftp#authentication-information).

### [!DNL Azure Blob Storage] {#azure-blob-storage}

Collaboration s’authentifie auprès de [!DNL Azure Blob Storage] à l’aide d’une chaîne de connexion de compte de stockage .

Pour obtenir des instructions sur l’obtention de la chaîne de connexion et l’attribution d’autorisations de stockage, voir [S’authentifier à la  [!DNL Azure Blob Storage]  destination](https://experienceleague.adobe.com/en/docs/experience-platform/destinations/catalog/cloud-storage/azure-blob#authenticate).

### [!DNL Google Cloud Storage] {#google-cloud-storage}

Collaboration nécessite un identifiant de clé d’accès [!DNL Google Cloud Storage] et une clé d’accès secrète générées par les paramètres d’interopérabilité [!DNL Google Cloud Storage].

Pour les exigences de génération d’informations d’identification et d’autorisation de compartiment, voir [Authentification à la  [!DNL Google Cloud Storage]  de destination](https://experienceleague.adobe.com/en/docs/experience-platform/destinations/catalog/cloud-storage/google-cloud-storage#authenticate).

### [!DNL Snowflake Batch] {#snowflake-batch}

[!DNL Snowflake Batch] utilise le partage de données [!DNL Snowflake] au lieu d’exporter des fichiers vers un espace de stockage géré par le client. Dans Collaboration, il n’existe pas d’étape d’authentification distincte. Saisissez l’identifiant du compte Snowflake, la région, le statut du lien privé et la confirmation de propriété du compte lors de la création de la destination.

Pour connaître les exigences de préparation de compte et de liste privée, consultez la [[!DNL Snowflake Batch] documentation de destination](https://experienceleague.adobe.com/en/docs/experience-platform/destinations/catalog/warehouse/snowflake-batch).

### [!DNL Data Landing Zone] {#data-landing-zone}

[!DNL Data Landing Zone] est configuré par Adobe et ne nécessite pas d’étape d’authentification distincte dans Collaboration. Pendant la création de la destination, spécifiez le chemin du dossier de destination et les paramètres de sortie de fichier.

Pour plus d’informations sur l’accès à un [!DNL Data Landing Zone] configuré pour AWS, voir [Authentification dans la zone d’atterrissage de données configurée pour AWS](https://experienceleague.adobe.com/en/docs/experience-platform/destinations/catalog/cloud-storage/data-landing-zone#authenticate-dlz-aws).

## Étapes suivantes {#next-steps}

Après avoir obtenu les informations de connexion requises, [configurez et gérez une destination](./manage-destinations.md).
