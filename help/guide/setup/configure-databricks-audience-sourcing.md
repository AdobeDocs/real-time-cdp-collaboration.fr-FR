---
title: Configurer [!DNL Databricks Delta Share] pour l’Audience Sourcing
description: Découvrez comment configurer et connecter [!DNL Databricks Delta Share] pour le sourcing d'audience dans Real-Time CDP Collaboration, y compris le partage d'historique.
audience: admin, publisher, advertiser
badgelimitedavailability: label=« Disponibilité limitée » type=« Informative » url=« https://helpx.adobe.com/legal/product-descriptions/real-time-customer-data-platform-collaboration.html » newtab=true
product_v2:
  - id: fdddec33-c9cb-4459-b8b6-2664395a6f10
    internal-label: Real-Time Customer Data Platform
source-git-commit: 2c6b8967566bcb1ea1851763a13d965bddfb9236
workflow-type: tm+mt
source-wordcount: '3294'
ht-degree: 1%
---

# Configurer [!DNL Databricks Delta Share] pour le sourcing d’audience

Utilisez ce guide pour connecter [!DNL Databricks Delta Share] à Adobe Real-Time CDP Collaboration et créer des audiences propriétaires via l&#39;interface utilisateur.

Lorsque vous vous connectez à [!DNL Databricks Delta Share], Collaboration lit les données d’audience directement à partir de votre partage de catalogue Unity. Une fois l’approvisionnement terminé, vous pouvez utiliser les audiences pour l’activation et l’analyse de chevauchement dans les projets de collaboration.

Ce guide explique comment remplir les conditions préalables, connecter votre [!DNL Delta Share], spécifier des tables source, mapper des champs d&#39;identité et vérifier que l&#39;approvisionnement de l&#39;audience démarre correctement.

Les audiences provenant de [!DNL Databricks] suivent les mêmes règles de gouvernance et de gestion des données que les audiences provenant de Adobe Experience Platform et d’autres sources cloud prises en charge.

Les autres méthodes de source disponibles sont les suivantes : [Experience Platform](./onboard-audiences.md), [Amazon S3](./configure-aws-s3-audience-sourcing.md), [Google Cloud Storage](./configure-gcs-audience-sourcing.md), [Snowflake](./configure-snowflake-audience-sourcing.md), [Azure storage](./configure-azure-storage-audience-sourcing.md) et [téléchargement de fichier CSV](./upload-csv-audience-sourcing.md). Pour en savoir plus sur toutes les sources disponibles dans Collaboration, consultez [Présentation des sources](./source-overview.md).

## Conditions préalables {#prerequisites}

Remplissez les conditions préalables décrites dans cette section avant de démarrer le workflow de configuration. Les conditions préalables manquantes sont une raison courante pour laquelle la configuration échoue ou les audiences n’apparaissent pas après le sourcing. Avant de suivre ce guide, terminez l’[intégration et configuration du compte](./onboard-account.md).

Certaines tâches de ce guide nécessitent l&#39;aide d&#39;un administrateur [!DNL Databricks]. Si vous n&#39;administrez pas [!DNL Databricks] pour votre organisation, contactez l&#39;administrateur approprié avant de commencer.

### Accès à [!DNL Databricks Delta Share] {#databricks-delta-share-access}

Avant de poursuivre, vérifiez les points suivants auprès de votre administrateur [!DNL Databricks] :

* Votre organisation a publié un compte [!DNL Delta Share] sur Adobe [!DNL Databricks] à l’aide du partage natif de briques de données à briques de données (catalogue Unity). Collaboration ne prend pas en charge les entrées d’informations d’identification de jeton porteur ou OIDC dans l’interface utilisateur pour ce workflow.
* Vous connaissez le nom du fournisseur tel qu’il est enregistré dans le métastore du catalogue Unity d’Adobe, le nom du partage et le schéma qui contient vos tables d’audience.
* L’approvisionnement de l’audience [!DNL Databricks Delta Share] est disponible pour votre compte Collaboration et votre région. Si l’approvisionnement en briques de données n’est pas encore disponible dans votre région, contactez votre représentant de compte Adobe pour confirmer une chronologie.

Pour obtenir des instructions détaillées sur la publication d’un partage dans Adobe, consultez la section [Publier votre partage Delta dans Adobe](#publish-delta-share) de ce guide.

### Préparation des données d’audience {#prepare-audience-data}

Structurez vos tableaux d’audience afin que Collaboration puisse découvrir des audiences et mapper correctement les identités.

* **Table d’appartenance (obligatoire) :** table de votre schéma partagé qui contient une ligne par paire profil-audience. Ce tableau doit inclure une colonne `AUDIENCE_ID` et au moins une colonne de clé de correspondance prise en charge. Collaboration utilise cette table pour l’aperçu des données sources et le mappage des champs.
* **Table de métadonnées (facultative) :** si vous conservez un catalogue distinct d’audiences (une ligne par audience avec un ID d’audience, un nom, des nombres ou des métadonnées similaires), vous pouvez fournir cette table afin que Collaboration lise les définitions d’audience à partir de celle-ci au lieu de déduire des ID d’audience distincts à partir de la table d’appartenance seule.
* **Clés de correspondance prises en charge :** `HASHED_EMAIL_SHA_256`, `HASHED_PHONE_SHA_256`, `HASHED_IPV4_SHA_256`, `CRM_ID`, `LOYALTY_ID`, `ADFIXUS_ID` et autres clés de correspondance activées pour votre compte Collaboration.
* **Exigences de hachage :** toutes les valeurs de clé correspondantes doivent être tronquées, mises en minuscules et SHA256-hachées avant d’être stockées dans [!DNL Databricks]. Collaboration ne hache ni ne normalise les données avant l’ingestion.
* **Cohérence des colonnes :** la table des abonnements doit exposer des noms de colonnes stables que Collaboration peut mapper à vos clés de correspondance activées.
* **Partage de l&#39;historique (recommandé) :** Pour améliorer les performances de sourcing, en particulier pour les tables volumineuses, activez le partage de l&#39;historique lors du partage des tables d&#39;audience. Le partage d’historique permet à Collaboration de lire les données en parallèle à l’aide d’une version de tableau cohérente. Sans partage d’historique, l’approvisionnement des audiences se termine à l’aide d’un processus de requête unique plus lent. Pour plus d&#39;informations, voir [Activer le partage d&#39;historique](#enable-history-sharing).

Toutes les clés de correspondance présentes dans votre table d’abonnement doivent également être activées pour votre compte Collaboration. Pour ajouter ou activer des clés de correspondance, voir [Configurer des clés de correspondance](./onboard-account.md#set-up-match-keys).

### Valeurs requises avant de commencer {#required-values}

Préparez les valeurs suivantes avant de démarrer le workflow de configuration.


| Valeur | Description |
| ----- | ----------- |
| Nom du fournisseur | Identifiant de fournisseur qu’Adobe utilise dans le catalogue Unity pour accéder à votre [!DNL Delta Share]. Votre administrateur [!DNL Databricks] ou votre contact d’intégration Adobe peut fournir cette valeur. Cette valeur n’est pas identique à l’URL de votre espace de travail [!DNL Databricks]. |
| Partager le nom | Nom de l’entité [!DNL Delta Share] publiée sur Adobe. |
| Schéma | Le schéma dans le partage qui contient vos tableaux d’audience. |
| Table des appartenances | Nom de la table dans le schéma qui contient les lignes d’appartenance à l’audience (une ligne par profil dans une audience). |
| Table de métadonnées (facultatif) | Nom de la table dans le schéma qui répertorie les audiences (une ligne par audience), si vous utilisez un catalogue d’audiences piloté par les métadonnées. |

{style="table-layout:auto"}

## Configurer votre connexion [!DNL Databricks] {#configure-databricks-connection}

Le workflow de configuration comprend plusieurs étapes dans l’espace de travail **[!UICONTROL Installation]**. Effectuez chaque étape dans l’ordre.

### Ajouter une nouvelle connexion de données {#add-data-connection}

Dans l’onglet **[!UICONTROL Mes audiences]** de l’espace de travail **[!UICONTROL Configuration]**, sélectionnez l’icône d’ajout (![Icône d’ajout.](/help/assets/icons/plus.png)) puis sélectionnez **[!UICONTROL Audience]**.

S’il s’agit de votre première audience, vous pouvez également sélectionner l’option **[!UICONTROL Ajouter]**.

![L’onglet Mes audiences dans l’espace de travail Configuration avec l’icône d’ajout et l’option Ajouter une audience affichées.](../../assets/setup/add-manage-audiences/add-audiences.png)

Le workflow Ajouter une audience s’affiche. Sélectionnez **[!UICONTROL Ajouter une nouvelle connexion de données]**, puis **[!UICONTROL Suivant]**.

![L’espace de travail Ajouter des audiences avec l’option Ajouter une nouvelle connexion de données mise en surbrillance.](../../assets/setup/add-manage-audiences/add-data-connection.png){zoomable="yes"}

### Sélectionner [!DNL Databricks Delta Share] comme source de données {#select-databricks-delta-share}

L’écran de sélection de la source de données répertorie tous les types de connexion disponibles. Sélectionnez **[!UICONTROL Partage Delta des briques de données]**, puis **[!UICONTROL Suivant]**.

![Le workflow Ajouter une audience affichant l’écran de sélection de la source de données avec le Partage Delta des briques de données sélectionné et Suivant en surbrillance.](../../assets/setup/databricks-audience-sourcing/databricks-data-source-selection.png)

### Connecter votre [!DNL Delta Share] {#connect-delta-share}

>[!CONTEXTUALHELP]
>id="rtcdp_collaboration_audience_sharing_databricks"
>title="Experience League"
>abstract="Pour obtenir des instructions sur la configuration de votre partage pour le sourcing d’audience, consultez le guide de sourcing [!DNL Databricks Delta Share]."

Fournissez les détails requis pour permettre à Collaboration d’accéder à votre [!DNL Delta Share]. Saisissez les détails du fournisseur, du partage, du schéma et de la table de votre [!DNL Databricks Delta Share]. La table d’appartenance requise doit être disponible dans le schéma partagé. Si vous utilisez une table de métadonnées, elle doit également être disponible dans le même schéma partagé.
Après avoir saisi les informations requises, sélectionnez **[!UICONTROL Connexion]**.

Collaboration valide le partage et le monte dans l’espace de travail Adobe. Cette étape peut prendre jusqu’à une minute. Un indicateur de progression s’affiche lorsque la connexion est établie.

| Champ | Description |
| --- | --- |
| **[!UICONTROL Nom du fournisseur]** | Le nom du fournisseur de catalogues Unitaires utilisé par Adobe pour consommer votre partage. Consultez les [valeurs requises avant de commencer](#required-values). |
| **[!UICONTROL Partager le nom]** | Nom de l’entité [!DNL Delta Share] publiée sur Adobe. |
| **[!UICONTROL Schéma]** | Le schéma dans le partage qui contient vos tableaux d’audience. |
| **[!UICONTROL Table des membres]** | Nom de la table dans le schéma qui contient les lignes d’appartenance à l’audience (une ligne par profil dans une audience). |
| **[!UICONTROL Table de métadonnées]** | Le tableau qui répertorie les audiences (une ligne par audience). |


![Le workflow Ajouter une audience affichant le formulaire de partage de connexion des briques de données avec le nom du fournisseur, le nom du partage, le schéma, la table d&#39;appartenance et les champs de table de métadonnées, ainsi que le bouton Suivant disponible.](../../assets/setup/databricks-audience-sourcing/databricks-connect-share-successful.png)

Si le partage est introuvable ou si le schéma n’est pas encore visible, un message d’erreur s’affiche. Vérifiez les valeurs avec votre administrateur [!DNL Databricks] et réessayez.

### Confirmer le consentement et la confirmation d’utilisation des données {#confirm-consent}

Avant de poursuivre, vérifiez que vous avez appliqué les désinscriptions requises par la loi aux données d’audience que vous envoyez à Collaboration. Si vous ne savez pas si vos données répondent à cette exigence, consultez le guide [politique de gouvernance et mesures d’application](./onboard-audiences.md#governance-policy-and-enforcement-actions) avant de continuer. Cochez la case de confirmation, puis sélectionnez **[!UICONTROL OK]** pour continuer.

![La boîte de dialogue d&#39;accusé de réception de désinscription au consentement nécessite une confirmation avant de continuer.](../../assets/setup/aws-audience-sourcing/consent-optout-acknowledgment.png)

### Fournir les détails de la connexion {#provide-connection-details}

Saisissez un nom et une description facultative pour cette connexion de données. Le nom que vous indiquez apparaît dans l’onglet **[!UICONTROL Mes connexions de données]** et permet de distinguer cette source si vous gérez plusieurs connexions de données.

* **[!UICONTROL Nom de la connexion de données]** (obligatoire)
* **[!UICONTROL Description de la connexion de données]** (facultatif)

Sélectionnez **[!UICONTROL Suivant]** pour continuer.

![Workflow Ajouter une audience à l’étape « Fournir des détails » affichant les champs pour le nom et la description de la connexion de données, avec « Suivant » visible dans le coin supérieur droit.](../../assets/setup/databricks-audience-sourcing/databricks-connection-details.png)

### Mapper les champs d’identité {#map-identity-fields}

L’écran **[!UICONTROL Mappage]** montre comment Collaboration mappe les colonnes sources de votre table d’appartenance aux champs d’identité cibles. Collaboration mappe automatiquement les champs en fonction des noms de colonne et des clés de correspondance activées pour votre compte.

>[!TIP]
>
>Sélectionnez **[!UICONTROL Prévisualiser les données sources]** pour consulter un exemple de votre table d’abonnement au format tabulaire, puis sélectionnez **[!UICONTROL Fermer]** pour revenir à l’écran de mappage.

![La boîte de dialogue « Aperçu des données des briques de données » affichant un exemple de tableau de données d’audience avec des colonnes telles que AUDIENCE_ID et HASHED_EMAIL_SHA_256, ainsi qu’un bouton Fermer dans le coin inférieur droit.](../../assets/setup/databricks-audience-sourcing/databricks-source-data-preview.png)

Vérifiez que les mappages affichés reflètent les colonnes de votre tableau d’appartenance. Sélectionnez **[!UICONTROL Suivant]** pour continuer.

![Workflow Ajouter une audience à l’étape « Mapper les champs » affichant les champs sources mappés aux champs d’identité cibles, avec l’option « Prévisualiser les données sources » visible et le bouton Suivant dans le coin supérieur droit.](../../assets/setup/databricks-audience-sourcing/databricks-field-mapping.png)

### Planifier la fréquence d’actualisation et la période {#schedule-refresh}

La vue **[!UICONTROL Planification]** s&#39;affiche. Utilisez le menu déroulant pour sélectionner une fréquence d’actualisation comprise entre un et six jours, puis définissez la période active. Utilisez l’icône de calendrier pour spécifier les dates de début et de fin.

>[!IMPORTANT]
>
>Pour gérer efficacement vos crédits Collaboration, définissez la fréquence d’actualisation pour qu’elle corresponde ou dépasse la fréquence de mise à jour de votre actualisation des données sous-jacentes.

![Écran des paramètres de planification avec options de fréquence d&#39;actualisation et configuration des périodes.](../../assets/setup/databricks-audience-sourcing/databricks-schedule-refresh-frequency.png)

### Vérifier et terminer la connexion {#review-and-complete}

Consultez le résumé de la configuration avant de créer la connexion. L’écran de résumé affiche les sections suivantes :

* **[!UICONTROL Connexion de données]** : nom de la connexion, nom du fournisseur, nom du partage et schéma que vous avez configurés.
* **[!UICONTROL Mappage]** : mappages des champs d’identité source et cible.
* **[!UICONTROL Planification]** : fréquence d’actualisation et période active.

![Ajoutez un workflow d’audience à l’étape « Vérifier » présentant un résumé des sections de partage de connexion, de détails et de mappage avec les valeurs configurées, ainsi que le bouton Terminer visible dans le coin supérieur droit.](../../assets/setup/databricks-audience-sourcing/databricks-review.png)

Vérifiez que toutes les sections sont correctes, puis sélectionnez **[!UICONTROL Terminé]**.

Une boîte de dialogue de confirmation s’affiche, indiquant que Collaboration a créé la connexion de données et que l’approvisionnement de l’audience est en cours.

## Vérifier les audiences sources {#review-sourced-audiences}

Une fois le workflow de configuration terminé, Collaboration commence à sourcer les audiences de vos tables [!DNL Databricks] de manière asynchrone. Accédez à **[!UICONTROL Configurer] > [!UICONTROL Mes audiences]** pour surveiller la progression. L’approvisionnement n’est pas terminé immédiatement ; le temps nécessaire dépend de la taille de vos données.

### Surveiller la progression de l’approvisionnement des audiences {#monitor-sourcing-progress}

Pendant que Collaboration récupère les données de votre audience, une bannière en haut de l’espace de travail **[!UICONTROL Mes audiences]** indique que le sourcing est en cours. Les audiences individuelles apparaissent dans la liste uniquement une fois l’approvisionnement terminé pour chaque audience.

![Configurez l’espace de travail dans l’onglet Mes audiences avec une bannière « Audience sourcing in progress » indiquant que les audiences sont sourcées à partir d’une connexion de données Databricks, avec la liste d’audiences affichée ci-dessous.](../../assets/setup/databricks-audience-sourcing/databricks-audience-sourcing-in-progress-banner.png)

>[!TIP]
>
>Pour améliorer les performances d&#39;approvisionnement des audiences, en particulier pour les tables volumineuses, activez le partage d&#39;historique. Cela permet à Collaboration de lire les données en parallèle à partir d’une version de tableau cohérente. Cependant, les partages entre cloud utilisent un processus de requête unique, même lorsque le partage d’historique est activé.
>
>Le temps d’approvisionnement de l’audience dépend également de facteurs tels que la taille de la table d’appartenance et la découverte d’audience pilotée par les métadonnées. Les jeux de données volumineux peuvent prendre plus de temps à apparaître dans **[!UICONTROL Mes audiences]**. Pour plus d&#39;informations, voir [Activer le partage d&#39;historique](#enable-history-sharing).

### Afficher les détails de l’audience source {#view-audience-details}

Une fois l’approvisionnement terminé, vos [!DNL Databricks] audiences apparaissent dans l’onglet **[!UICONTROL Mes audiences]** aux côtés des audiences provenant d’autres connexions. Sélectionnez un élément de ligne ou **[!UICONTROL Afficher l&#39;audience]** pour ouvrir la vue détaillée pour une audience spécifique.

![L&#39;onglet « Mes audiences » dans l&#39;espace de travail Configuration affiche un tableau des audiences, dont une provenant du partage Delta des briques de données, avec des cases à cocher sélectionnables et des actions de ligne disponibles.](../../assets/setup/databricks-audience-sourcing/databricks-my-audiences-row-actions.png)

La vue détaillée affiche le statut de l’audience, la source et le nom de la connexion aux données, ainsi que les panneaux suivants :

* **[!UICONTROL Identités]** : nombre total d’identités et répartition de l’audience, une fois que les données sont disponibles.
* **[!UICONTROL Catégories]** : toute balise appliquée pour organiser ou filtrer l’audience.
* **[!UICONTROL Accès à la connexion]** : que l’audience soit privée, publique ou partagée avec des collaborateurs spécifiques.
* **[!UICONTROL Visibilité des métadonnées]** : informations sur l’audience, telles que le nombre d’identités, le pourcentage de chevauchement et l’index, visibles par les collaborateurs.

![Vue détaillée d&#39;audience individuelle affichant le statut : Actif, le système source et le nom de la connexion de données en haut, avec quatre panneaux ci-dessous : Identités, Catégories, Accès à la connexion et Visibilité des métadonnées.](../../assets/setup/databricks-audience-sourcing/databricks-audience-detail-view.png)

Consultez ces paramètres avant d’utiliser l’audience dans un projet de collaboration. Pour mettre à jour les catégories, l’accès à la connexion ou la visibilité des métadonnées, consultez [Afficher et gérer des audiences individuelles](./onboard-audiences.md#view-individual-audiences).

### Modifier les paramètres d’audience {#edit-audience-settings}

Vous pouvez modifier les métadonnées d’audience directement à partir de la vue Liste **[!UICONTROL Mes audiences]** sans ouvrir la vue détaillée. Cochez la case d’une audience pour afficher la barre d’outils d’actions, puis sélectionnez une action : **[!UICONTROL Modifier la visibilité des métadonnées]**, **[!UICONTROL Modifier l’accès à la connexion]**, **[!UICONTROL Modifier le nom et la description]**, **[!UICONTROL Modifier les catégories]** ou **[!UICONTROL Supprimer]**.

![La vue Liste Mes audiences affiche les audiences provenant de différents systèmes, avec une ligne sélectionnée à l&#39;aide d&#39;une case à cocher, affichant une barre d&#39;outils inférieure avec des options de modification et de suppression.](../../assets/setup/databricks-audience-sourcing/databricks-edit-audience-settings.png)

### Afficher votre connexion de données [!DNL Databricks] {#view-databricks-connection}

Pour vérifier la connexion elle-même, y compris ses clés de correspondance, accédez à **[!UICONTROL Configuration]** > **[!UICONTROL Mes connexions de données]**. Votre nouvelle connexion [!DNL Databricks] y est disponible. La source de l&#39;audience s&#39;affiche sous la forme **[!UICONTROL Partage Delta des briques de données]**.

![L’onglet Mes connexions de données affiche la connexion de données [!DNL Databricks Delta Share] avec les informations de statut de source.](../../assets/setup/databricks-audience-sourcing/databricks-my-data-connections-tab.png)

## Limites connues {#known-limitations}

Tenez compte des contraintes suivantes lors de la configuration et de l’utilisation de l’approvisionnement des audiences [!DNL Databricks Delta Share] :

* **Partage natif uniquement :** L’interface utilisateur prend uniquement en charge les briques de données natives à l’adresse [!DNL Delta Sharing]. Les flux d’authentification de jeton porteur et OIDC ne sont pas disponibles dans le workflow de configuration.
* **Saisie manuelle du nom de la table :** Vous devez saisir les noms de la table manuellement. Collaboration valide les noms des tableaux lorsque vous les prévisualisez ; il ne répertorie pas automatiquement tous les tableaux de votre partage.
* **Limite de lignes du tableau de métadonnées :** lorsque vous utilisez un tableau de métadonnées pour la découverte d’audiences, Collaboration importe jusqu’à 100 000 lignes d’audience de ce tableau. Contactez l’assistance Adobe si votre catalogue dépasse cette limite.
* **Contraintes de clé de correspondance :** Une fois qu’une clé de correspondance est activée pour une connexion de données, elle ne peut pas être supprimée. Vous pouvez ajouter des clés de correspondance à une connexion existante, mais vous ne pouvez pas les désactiver ni les supprimer. Pour modifier les clés de correspondance actives, vous devez [supprimer la connexion de données](./manage-data-connection.md#delete-data-connection) et en créer une nouvelle.
* **Table d’appartenance requise :** même lorsque vous utilisez une table de métadonnées pour la découverte d’audiences, vous devez spécifier une table d’appartenance. Collaboration lit les lignes d’identité de la table d’appartenance lors de l’ingestion.
* **Partage d&#39;historique recommandé pour les tables volumineuses :** Pour améliorer les performances de sourcing pour les tables volumineuses, activez le partage d&#39;historique. Cela permet à Collaboration de lire les données en parallèle. Sans partage d’historique, le sourcing utilise un processus de requête unique plus lent. Pour plus d&#39;informations, voir [Activer le partage d&#39;historique](#enable-history-sharing).
* **Partages entre cloud :** lorsque votre fournisseur [!DNL Databricks] et l’espace de travail Adobe utilisent différents environnements cloud, l’approvisionnement utilise un processus de requête unique, que le partage d’historique soit activé ou non. Par exemple, cela s’applique lorsque votre fournisseur utilise [!DNL Azure] et que l’espace de travail Adobe utilise AWS. Aucune configuration supplémentaire n’est requise.

## Dépannage {#troubleshooting}

Utilisez cette section pour résoudre les problèmes qui se produisent pendant ou après la configuration. Pour détecter les erreurs lors du partage de la connexion, vérifiez le nom de votre fournisseur, le nom du partage et le schéma avec votre administrateur [!DNL Databricks].

**La connexion de partage échoue ou expire**

* Vérifiez que votre [!DNL Delta Share] est publié sur le compte Adobe [!DNL Databricks] et que le nom du fournisseur, le nom du partage et le schéma sont corrects.
* Vérifiez que le schéma est visible dans le partage. Les partages nouvellement publiés peuvent prendre du temps à se propager.
* Si la connexion échoue toujours au bout de quelques minutes, redémarrez la configuration et réessayez, ou contactez l’assistance clientèle d’Adobe et fournissez le nom du fournisseur, le nom du partage, le schéma et tous les détails d’erreur pertinents. N’incluez pas d’informations d’identification sensibles.

**Échec de l&#39;aperçu du tableau**

* Vérifiez que le nom de la table est orthographié correctement et existe dans le schéma que vous avez spécifié.
* Assurez-vous que le tableau est inclus dans le [!DNL Delta Share] publié sur Adobe.
* Pour la découverte pilotée par les métadonnées, prévisualisez le tableau des abonnements et le tableau des métadonnées avant de continuer.

**La validation du mappage des champs bloque la progression**

* Confirmez que votre tableau d’appartenance comprend une colonne `AUDIENCE_ID` et au moins une colonne de clé de correspondance prise en charge.
* Vérifiez qu’au moins une clé de correspondance prise en charge possède un champ source et un champ cible mappés.
* Utilisez **[!UICONTROL Prévisualiser les données sources]** pour vérifier que les noms des colonnes correspondent à vos clés de correspondance activées.

**Les audiences n’apparaissent pas ou l’approvisionnement prend plus de temps que prévu**

* Vérifiez que vos tableaux sont partagés avec l’historique. Exécutez `SHOW ALL IN SHARE <share_name>;` et vérifiez que `history_sharing` est `ENABLED`. Si le partage d&#39;historique est désactivé, ajoutez à nouveau le tableau avec `WITH HISTORY`. Pour plus d&#39;informations, voir [Activer le partage d&#39;historique](#enable-history-sharing).
* Le temps d’approvisionnement est proportionnel au volume des données. Un temps de traitement étendu est attendu pour les tables d’appartenance volumineuses.
* Si les audiences ne s’affichent pas dans les 24 heures, recherchez les indicateurs d’erreur sur la connexion dans l’onglet **[!UICONTROL Mes connexions de données]**.
* Vérifiez que la structure de votre table d&#39;appartenance et les mappages de champs correspondent aux exigences de la section [Préparer les données d&#39;audience](#prepare-audience-data).
* Si le problème persiste, contactez l’assistance clientèle d’Adobe et fournissez le nom de la connexion de données et les détails de la table.

**Échec de l&#39;activation du partage de l&#39;historique**

Si votre espace de travail rejette la commande `ALTER TABLE`, supprimez le tableau du partage et ajoutez le tableau avec l’historique. Remplacez `<share_name>`, `<catalog>`, `<schema>` et `<table>` par votre nom de partage et vos identifiants de table.

>[!IMPORTANT]
>
> Ne supprimez pas et n’ajoutez pas à nouveau une table lorsqu’une exécution de sourcing Adobe est en cours.

```sql
ALTER SHARE <share_name> REMOVE TABLE <catalog>.<schema>.<table>;
ALTER SHARE <share_name> ADD TABLE <catalog>.<schema>.<table> WITH HISTORY;
```

Après avoir rajouté la table, [vérifiez que le partage d&#39;historique est activé](#enable-history-sharing).

**La connexion de données affiche le statut En échec après avoir réussi**

* Vérifiez que les tableaux [!DNL Delta Share] et n&#39;ont pas été supprimés ou renommés dans [!DNL Databricks] depuis que vous avez créé la connexion.
* Vérifiez que l’accès Adobe au partage n’a pas été révoqué.
* Si le problème persiste, contactez l’assistance clientèle d’Adobe.

## Publier votre [!DNL Delta Share] dans Adobe {#publish-delta-share}

[!DNL Databricks] Le catalogue Unity [!DNL Delta Sharing] vous permet de partager des tables en toute sécurité avec d’autres comptes [!DNL Databricks] sans copier de données. Pour permettre à Collaboration de lire vos données d’audience, votre administrateur [!DNL Databricks] doit publier un [!DNL Delta Share] sur le compte client [!DNL Databricks] d’Adobe.

### Avant la publication {#before-you-publish}

Contactez votre représentant de compte Adobe ou votre contact d’intégration pour obtenir :

* Confirmation qu’Adobe est prêt à recevoir votre part dans votre région.
* Nom du fournisseur qu’Adobe utilise dans sa métastore de catalogue Unity pour identifier votre organisation en tant que fournisseur de partages.

Préparez les éléments suivants dans votre espace de travail [!DNL Databricks] :

* Un [!DNL Delta Share] contenant le schéma et les tables que Collaboration lira.
* Une table des appartenances avec une ligne par paire profil-audience et des colonnes pour **`AUDIENCE_ID`** et des clés de correspondance.
* Un tableau de métadonnées facultatif si vous prévoyez d’utiliser la découverte d’audience pilotée par les métadonnées.
* Partage de l&#39;historique activé pour chaque table du partage (recommandé).

### Publier le partage {#publish}

Suivez les procédures [!DNL Databricks Delta Sharing] de votre organisation pour accorder l’accès au partage à un compte client Adobe. Les étapes exactes dépendent de votre déploiement [!DNL Databricks] et de votre modèle de gouvernance. En général :

1. Dans le catalogue Unity, créez ou identifiez le partage contenant le schéma et les tableaux de votre audience.
2. Ajoutez le schéma ou les tables individuelles à votre partage de briques de données. Adobe vous recommande d&#39;activer le partage d&#39;historique pour chaque table. Pour plus d&#39;informations, voir [Activer le partage d&#39;historique](#enable-history-sharing).
3. Octroyez le partage au compte client [!DNL Databricks] d’Adobe à l’aide du partage natif de briques de données à briques de données.
4. Vérifiez auprès de votre contact Adobe que le partage est visible du côté du client et notez le nom du fournisseur et le nom du partage pour le workflow de configuration de Collaboration.

>[!NOTE]
>
> Pour obtenir des instructions sur le produit, consultez la [documentation sur le partage Delta des briques de données](https://docs.databricks.com/aws/en/delta-sharing){target="_blank"}.

### Activer le partage d&#39;historique {#enable-history-sharing}

Pour améliorer les performances de sourcing pour les tableaux volumineux, activez le partage d’historique pour chaque tableau d’audience. Cela permet à Collaboration de lire les données en parallèle à l’aide d’une version de tableau cohérente. Sans partage d’historique, Collaboration utilise un processus de requête unique plus lent.

Les partages entre cloud utilisent l’événement de lecture de requête unique avec l’historique activé. Pour plus d&#39;informations, voir [Limites connues](#known-limitations).

Le partage d&#39;historique permet à Adobe d&#39;accéder aux versions précédentes des tables partagées, mais pas aux autres tables. Vous n’avez pas besoin d’accorder un accès supplémentaire lorsque vous activez le partage d’historique pour une table que vous partagez déjà avec Adobe.

Utilisez les commandes SQL suivantes dans votre espace de travail [!DNL Databricks]. Remplacez `<share_name>`, `<catalog>`, `<schema>` et `<table>` par votre nom de partage et vos identifiants de table.

Pour ajouter un tableau avec un historique, exécutez :

```sql
ALTER SHARE <share_name> ADD TABLE <catalog>.<schema>.<table> WITH HISTORY;
```

Pour activer le partage d&#39;historique pour une table déjà dans le partage, exécutez :

```sql
ALTER SHARE <share_name> ALTER TABLE <catalog>.<schema>.<table> WITH HISTORY;
```

Pour vérifier le partage de l’historique, exécutez :

```sql
SHOW ALL IN SHARE <share_name>;
```

Vérifiez que `history_sharing` est `ENABLED` pour chaque table d’audience, y compris la table de métadonnées si vous en utilisez une. Le partage de l’historique prend effet lors de la prochaine exécution de sourcing.

### Collecter [!DNL Databricks] détails pour Collaboration {#collect-databricks-details}

Après avoir publié le partage, assurez-vous que le nom du fournisseur, le nom du partage, le schéma et les noms des tables sont disponibles pour le workflow de configuration de Collaboration.

Rassemblez les détails ci-dessous avant de démarrer le workflow de configuration Collaboration.

| Champ | Description | Exemple |
| ------ | ----------- | ------- |
| Nom du fournisseur | Identifiant du fournisseur dans la métastore du catalogue Adobe Unity (provenant de l’intégration à Adobe) | `your_org_provider` |
| Partager le nom | Nom du [!DNL Delta Share] publié | `audience_share_prod` |
| Schéma | Schéma dans le partage contenant vos tableaux d’audience. | `collaboration_audiences` |
| Table des appartenances | Tableau avec lignes d’appartenance à une audience de profil | `audience_members` |
| Table de métadonnées (facultatif) | Tableau répertoriant les audiences (une ligne par audience) | `audience_catalog` |

{style="table-layout:auto"}

## Étapes suivantes {#next-steps}

Vous avez configuré [!DNL Databricks Delta Share] en tant que source de données dans Collaboration. Une fois l’approvisionnement terminé, vos audiences sont disponibles dans l’espace de travail **[!UICONTROL Mes audiences]** et prêtes à être utilisées dans des projets de collaboration.

Plusieurs possibilités sʼoffrent alors à vous :

* [Créer et gérer des projets de collaboration](../collaborate/manage-projects.md)
* [Activer des audiences dans un projet](../collaborate/activate.md)
* [Vérifier les chevauchements et mesurer les performances](../collaborate/measure.md)
* [Gérer les paramètres et la visibilité de l’audience](./onboard-audiences.md#view-individual-audiences)
* [Afficher et gérer les connexions de données](./manage-data-connection.md)

Pour d’autres méthodes d’approvisionnement d’audience, voir :

* [Configurer [!DNL Google Cloud Storage] pour l&#39;approvisionnement de l&#39;audience](./configure-gcs-audience-sourcing.md)
* [Configurer [!DNL Amazon S3] pour l&#39;approvisionnement de l&#39;audience](./configure-aws-s3-audience-sourcing.md)
* [Configurer [!DNL Snowflake] pour l&#39;approvisionnement de l&#39;audience](./configure-snowflake-audience-sourcing.md)
* [Audiences Source à partir d’Experience Platform](./onboard-audiences.md)
* [Chargement d’un fichier CSV pour l’audience](./upload-csv-audience-sourcing.md)
