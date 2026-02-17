---
title: Configuration  [!DNL Amazon S3]  pour l’approvisionnement auprès d’audiences
description: Découvrez comment configurer et connecter votre stockage  [!DNL Amazon S3]  tant que source de données en libre-service pour ingérer les données d’audience dans Real-Time CDP Collaboration.
exl-id: 566ceb1b-a72a-413d-b07d-409723892616
source-git-commit: 43134d6f334ee500834a6451bdf1a8f7372f8d10
workflow-type: tm+mt
source-wordcount: '1583'
ht-degree: 1%

---

# Configuration des [!DNL Amazon S3] pour l’approvisionnement des audiences

Découvrez comment configurer et connecter votre stockage [!DNL Amazon S3] dans l’interface utilisateur d’Adobe Real-Time CDP Collaboration aux données de l’audience source pour l’activation et l’analyse de chevauchement.

>[!IMPORTANT]
>
>Avant de suivre ce guide, vous devez avoir suivi les étapes d’autorisation du rôle IAM d’Adobe dans votre compte AWS.\
>Consultez le guide **[Configurer les autorisations AWS pour l’approvisionnement des audiences](./configure-aws-permissions-audience-sourcing.md)** pour obtenir des instructions de configuration détaillées.

## Vue d’ensemble {#overview}

Utilisez ce workflow pour sourcer et gérer des audiences propriétaires directement à partir de [!DNL Amazon S3]. Après la configuration, Collaboration source automatiquement les audiences à partir de votre compartiment S3 et les rend disponibles pour les informations et l’activation.

Les audiences provenant de S3 suivent les mêmes règles de gouvernance et de gestion des données que celles provenant de Adobe Experience Platform.

## Conditions préalables {#prerequisites}

Avant de configurer votre connexion de données S3, vérifiez les points suivants :

* Vous avez accès à un compartiment **[!DNL Amazon S3]actif** contenant des fichiers d’audience conformes à la **[Spécification d’approvisionnement de l’audience (v1.1)](../../assets/quick-start/RTCDP_Collaboration_Audience_Sourcing_Spec_v1.2.pdf)**.
* Vous avez créé un **rôle IAM** dans AWS qui accorde à Adobe l’autorisation d’accéder à votre compartiment à l’aide de la méthode **rôle assumé** (et non des clés d’accès/secrètes). Consultez **[Configuration des autorisations AWS pour l’approvisionnement des audiences](./configure-aws-permissions-audience-sourcing.md)** pour des instructions détaillées. Le rôle IAM doit inclure les autorisations suivantes :

   * `ListBucket`
   * `GetBucketLocation`
   * `GetObject`

* Les valeurs suivantes sont prêtes :

   * **Nom de la ressource Amazon (ARN) du rôle IAM**
   * Nom du compartiment **S3**
   * **Chemin du dossier** (préfixe de répertoire contenant les fichiers de votre audience)

>[!NOTE]
>
>Les fichiers d’audience doivent se trouver dans le **chemin d’accès au dossier racine** de votre compartiment S3 autorisé. Les structures de sous-dossiers ne sont pas prises en charge.

## Configurer votre connexion [!DNL Amazon S3] {#configure-aws-s3-connection}

Dans l’onglet **[!UICONTROL Mes audiences]** de l’espace de travail **[!UICONTROL Configuration]**, sélectionnez l’icône d’ajout (![icône d’ajout).](/help/assets/icons/plus.png)), puis sélectionnez **[!UICONTROL Audience]**.

S’il s’agit de votre première audience, vous pouvez également sélectionner l’option **[!UICONTROL Ajouter]**.

![L’onglet Mes audiences dans l’espace de travail Configuration avec l’icône d’ajout et l’option Ajouter une audience affichées.](../../assets/setup/add-manage-audiences/add-audiences.png)

Le workflow Ajouter une audience s’affiche. Sélectionnez **[!UICONTROL Ajouter une nouvelle connexion de données]** puis sélectionnez **[!UICONTROL Suivant]**.

![L’espace de travail Ajouter des audiences avec l’option Ajouter une nouvelle connexion de données mise en surbrillance.](../../assets/setup/add-manage-audiences/add-data-connection.png){zoomable="yes"}

### Sélectionnez [!DNL Amazon S3] comme connexion de données {#select-aws-s3}

Sélectionnez **[!UICONTROL Amazon S3]** comme connexion de données, puis **[!UICONTROL Suivant]**.

![Écran de sélection de la connexion aux données avec [!DNL Amazon S3] disponible sous la forme d’une option sélectionnable.](../../assets/setup/aws-audience-sourcing/select-s3-data-connection.png)

### Vérifier les exigences relatives aux fichiers d’audience {#review-audience-requirements}

>[!CONTEXTUALHELP]
>id="rtcdp_collaboration_audience_sourcing_specifications"
>title="Préparer vos données pour l’intégration"
>abstract="Lisez le Guide de spécification d’approvisionnement d’audience pour savoir comment formater et structurer les données d’audience à partir d’Amazon S3 pour Collaboration."
>additional-url="https://www.adobe.com/go/rtcdp-collaboration-audience-sourcing" text="Voir le guide"

Une boîte de dialogue s’affiche pour expliquer comment les fichiers d’audience doivent être structurés. Utilisez le lien vers la **[[!UICONTROL Spécification d’approvisionnement d’audience]](../../assets/quick-start/RTCDP_Collaboration_Audience_Sourcing_Spec_v1.2.pdf)** pour savoir comment formater et structurer les données d’audience à partir de [!DNL Amazon S3] pour que Collaboration les lise correctement.

>[!IMPORTANT]
>
>Vous devez disposer de l’autorisation Adobe en tant qu’utilisateur [!DNL Amazon S3] afin qu’Adobe puisse récupérer les données de votre espace de stockage [!DNL Amazon S3] pour le traitement.

Les fichiers d’audience doivent être conformes aux spécifications d’approvisionnement de l’audience. Les clés de correspondance sont automatiquement mappées en fonction du format requis.

Les principales considérations sont les suivantes :

* Les fichiers doivent être au format CSV, avec des virgules comme délimiteurs et barres verticales (`|`) pour plusieurs valeurs.
* Si vous téléchargez plusieurs fichiers, assurez-vous que tous contiennent des colonnes identiques.
* Chaque enregistrement d’audience doit inclure un `AUDIENCE_ID` et au moins une clé de correspondance, telle que `HASHED_EMAIL_SHA_256`, `HASHED_PHONE_SHA_256`, `HASHED_IPV4_SHA_256`, `CRM_ID`, `LOYALTY_ID` ou `ADFIXUS_ID`.
* Les données sont actualisées tous les 1 à 6 jours en fonction de votre sélection lors de la configuration de l’approvisionnement dans Collaboration.

![&#x200B; La boîte de dialogue Préparer vos données pour l’approvisionnement avec un lien vers les spécifications d’approvisionnement de l’audience.](../../assets/setup/aws-audience-sourcing/prepare-data-sourcing-dialog.png)

### Authentification de votre connexion S3 {#authenticate-s3-connection}

>[!CONTEXTUALHELP]
>id="rtcdp_collaboration_sources_s3_folderpath"
>title="Format du chemin d’accès au dossier"
>abstract="Saisissez le chemin d’accès au dossier (préfixe) dans votre compartiment [!DNL Amazon S3] où vos fichiers d’audience sont stockés.<br><ul><li>Ne commencez pas les chemins par une barre oblique (/).</li><li>Insérez une barre oblique à la fin du chemin d’accès.</li><ul><br>Exemple valide : `base/path/`<br>Exemple non valide : `/base/path`"

>[!CONTEXTUALHELP]
>id="rtcdp_collaboration_audience_sharing_amazon_s3"
>title="Ajout d’une audience pour Amazon S3"
>abstract="Pour connecter votre stockage Amazon S3, autorisez l’utilisateur du service Adobe à récupérer les données de votre audience pour traitement. Suivez les étapes décrites dans Experience League pour accorder à Adobe l’accès à votre stockage Amazon S3."

Indiquez ensuite vos informations d’identification [!DNL Amazon S3] pour connecter votre compartiment S3 à Collaboration.

Suivez les étapes décrites dans **[Configuration des autorisations AWS pour l’approvisionnement des audiences](./configure-aws-permissions-audience-sourcing.md)** pour accorder à Adobe l’accès à vos
Stockage [!DNL Amazon S3]. Une fois l’opération terminée, saisissez vos valeurs dans les champs suivants de l’interface utilisateur :

* Rôle IAM
* Nom du compartiment S3
* Chemin du dossier

![Formulaire de connexion [!DNL Amazon S3] avec champs pour le rôle IAM, le nom du compartiment S3 et le chemin d’accès au dossier.](../../assets/setup/aws-audience-sourcing/s3-authentication-credentials-form.png)

### Confirmer l’accusé de réception du consentement {#confirm-consent}

Vous devez ensuite reconnaître que les désinscriptions au consentement ont été supprimées avant de continuer. Cochez la case de confirmation suivie de **[!UICONTROL OK]** pour confirmer.

![La boîte de dialogue d’accusé de réception de désinscription au consentement nécessite une confirmation avant de continuer.](../../assets/setup/aws-audience-sourcing/consent-optout-acknowledgment.png)

### Valider les résultats de l’authentification {#validate-authentication}

Une fois connecté, le système valide vos informations d’identification et affiche l’un des messages suivants :

| Statut | Message | Description |
|---| ---|---|
| **Succès** | **[!UICONTROL Authentification réussie]** | Votre connexion à [!DNL Amazon S3] a été établie. |
| **Échec** | **[!UICONTROL Échec de l’authentification]** | Vérifiez vos informations d’identification et réessayez. |
| **Accès refusé** | **[!UICONTROL Accès refusé]** | Vos informations d’identification ne disposent pas des autorisations requises pour accéder à ce compartiment [!DNL Amazon S3]. Vérifiez les paramètres d’accès ou contactez votre administrateur. |
| **Format de fichier non valide** | **[!UICONTROL Format de fichier non valide]** | Les données de l’audience ne correspondent pas à la structure attendue. Veillez à ce que vos fichiers soient conformes aux spécifications d’approvisionnement de l’audience. |
| **Aucun fichier d’audience trouvé** | **[!UICONTROL Aucun fichier d’audience trouvé]** | Veuillez confirmer que les fichiers de votre audience existent dans le chemin d’accès au dossier spécifié et que le chemin d’accès est accessible. |
| **Erreur interne** | **[!UICONTROL Une erreur interne est survenue]** | Veuillez réessayer. Si le problème persiste, contactez le service clientèle. |


### Fournir les détails de la connexion {#provide-connection-details}

Saisissez un nom explicite et une description facultative pour votre connexion de données S3. Saisissez vos valeurs dans les champs d’interface utilisateur suivants :

* **[!UICONTROL Nom de la connexion de données]** (obligatoire)
* **[!UICONTROL Description de la connexion de données]** (facultatif)

![Formulaire des détails de la connexion de données avec des champs pour le nom et la description de la connexion.](../../assets/setup/aws-audience-sourcing/s3-connection-name-description.png)

### Vérifier les champs d’identité mappés automatiquement {#auto-mapped-fields}

L’écran **[!UICONTROL Mappage]** est en lecture seule. Vous ne pouvez pas ajouter, supprimer ou appliquer de transformations. Collaboration mappe automatiquement les champs d’identité source de vos fichiers d’audience vers les champs cibles en fonction de la spécification de l’approvisionnement de l’audience.

Confirmez visuellement les champs mappés et sélectionnez **[!UICONTROL Suivant]** pour continuer.

![Écran de mappage des champs affichant les champs d’identité source et cible mappés automatiquement.](../../assets/setup/aws-audience-sourcing/s3-field-mapping-auto-mapped.png)

### Planifier la fréquence d’actualisation et la période {#schedule-refresh}

La vue **[!UICONTROL Planification]** s’affiche. Utilisez le menu déroulant pour sélectionner une fréquence d’actualisation comprise entre un et six jours, puis définissez la période active. Utilisez l’icône de calendrier pour spécifier les dates de début et de fin.

>[!IMPORTANT]
>
>Pour gérer efficacement vos crédits Collaboration, définissez la fréquence d’actualisation pour qu’elle corresponde ou dépasse la fréquence de mise à jour de vos données S3 sous-jacentes. L’intervalle d’actualisation minimum pris en charge est d’une fois tous les six jours.

![Écran des paramètres de planification avec les options de fréquence d’actualisation et la configuration des périodes.](../../assets/setup/aws-audience-sourcing/s3-schedule-refresh-frequency.png)

### Vérifier et terminer la connexion {#review-and-complete}

Enfin, passez en revue vos paramètres de configuration dans l’écran de résumé. Cette vue contient un résumé des sections suivantes :

* **[!UICONTROL Connexion aux données]** : affiche le rôle IAM, le nom du compartiment S3 et le chemin d’accès au dossier que vous avez configuré.
* **[!UICONTROL Détails]** : affiche le nom et la description facultative de votre connexion de données pour vous aider à l’identifier ultérieurement.
* **[!UICONTROL Mappage]** : répertorie la manière dont les champs sources de vos fichiers d’audience chargés (par exemple, `HASHED_EMAIL`) sont mappés aux champs cibles utilisés dans Collaboration (par exemple, e-mail haché).
* **[!UICONTROL Planification]** : résume la fréquence à laquelle la connexion actualise les données d’audience et la période active pour l’approvisionnement.

Sélectionnez l’icône en forme de crayon si vous devez modifier une section. Sélectionnez **[!UICONTROL Terminé]** pour confirmer toutes les sections.

![Écran de résumé de la révision affichant les sections de connexion aux données, de détails, de mappage et de planification.](../../assets/setup/aws-audience-sourcing/s3-connection-review-summary.png)

Une boîte de dialogue de confirmation s’affiche, indiquant que la connexion de données a été créée avec succès et que l’audience est approvisionnée en cours.

## Vérifier les audiences sources {#review-sourced-audiences}

Une fois la configuration terminée, Collaboration commence à sourcer les audiences à partir de votre compartiment S3. Les audiences provenant d’un compartiment [!DNL Amazon S3] apparaissent dans l’onglet **[!UICONTROL Mes audiences]** et disposent des mêmes fonctionnalités et informations que les audiences provenant d’Experience Platform.

Si le sourcing d’audience est en cours, une bannière s’affiche en haut de l’écran. Les audiences individuelles s’affichent uniquement une fois l’approvisionnement terminé.

![Onglet Audiences indiquant que le sourcing est en cours pour les audiences [!DNL Amazon S3].](../../assets/setup/aws-audience-sourcing/s3-audiences-sourcing-in-progress.png)

Une fois que les audiences S3 sont sourcées, votre liste d’audiences disponibles est fournie dans un affichage tabulé ou en mode Carte.

>[!TIP]
>
>Le temps d’approvisionnement de l’audience varie en fonction de la taille de vos données S3 et de la fréquence d’actualisation que vous avez configurée. L’affichage de jeux de données plus volumineux ou de plannings d’actualisation moins fréquents peut prendre plus de temps dans l’espace de travail **[!UICONTROL Mes audiences]**.

![Onglet Audiences présentant une liste tabulée des audiences sources.](../../assets/setup/aws-audience-sourcing/s3-audiences-list-view.png)

En mode Grille ou Tableau, sélectionnez un élément de ligne ou **[!UICONTROL Afficher l’audience]** pour afficher un aperçu d’une audience spécifique. Il affiche le statut, la source et le nom de connexion aux données de l’audience, ainsi que des panneaux détaillés pour :

**[!UICONTROL Identités]** : affiche le nombre total d’identités et leur répartition une fois que les données sont disponibles.
**[!UICONTROL Catégories]** : répertorie toutes les balises utilisées pour organiser ou filtrer l’audience.
**[!UICONTROL Accès de connexion]** : indique si l’audience est privée, publique ou partagée avec des collaborateurs spécifiques.
**[!UICONTROL Visibilité des métadonnées]** : définit les informations d’audience (telles que le nombre d’identités, le pourcentage de chevauchement et l’index) visibles par les collaborateurs.

Utilisez cette vue pour confirmer les paramètres de configuration et de visibilité de l’audience avant d’utiliser l’audience dans des projets de collaboration.

Consultez la [documentation du tableau de bord Afficher les audiences](https://experienceleague.adobe.com/en/docs/real-time-cdp-collaboration/using/setup/onboard-audiences#view-audiences-dashboard) pour en savoir plus.

## Affichage de la connexion aux données S3 {#view-s3-connection}

La nouvelle connexion [!DNL Amazon S3] est immédiatement disponible dans l’onglet **[!UICONTROL Mes connexions de données]**. La source de l’audience s’affiche sous la forme [!UICONTROL Amazon S3].

Votre connexion de données S3 inclut les mêmes fonctionnalités et détails que les autres connexions de données d’audience, sauf que vous ne pouvez pas ajouter ou modifier des audiences directement à partir de cette vue.

>[!NOTE]
>
>Les connexions de données [!DNL Amazon S3] ne sont pas modifiables. Vous ne pouvez pas modifier des paramètres tels que la fréquence d’actualisation une fois la connexion créée. Pour mettre à jour la configuration, vous devez supprimer la connexion existante et en créer une nouvelle.

![Onglet Mes connexions de données affichant la connexion de données [!DNL Amazon S3] avec les informations de statut de source.](../../assets/setup/aws-audience-sourcing/s3-data-connections-tab.png)

## Étapes suivantes {#next-steps}

Vous avez maintenant correctement configuré et connecté votre stockage [!DNL Amazon S3] en tant que source de données dans Collaboration. En exécutant ce workflow, vous avez activé l’approvisionnement sécurisé des données d’audience propriétaires pour l’activation et l’analyse de chevauchement.

Une fois l’approvisionnement terminé, vos audiences apparaissent dans l’espace de travail **[!UICONTROL Mes audiences]**, prêtes pour la collaboration et l’activation. Pour obtenir des options de gestion détaillées, consultez la documentation [source et gestion des audiences](./onboard-audiences.md).
