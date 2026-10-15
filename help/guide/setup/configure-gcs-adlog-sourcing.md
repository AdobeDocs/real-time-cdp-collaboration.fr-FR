---
title: Configurer des [!DNL Google Cloud Storage] pour le sourcing d’exposition publicitaire
description: Découvrez comment connecter un compartiment [!DNL Google Cloud Storage] en tant que source de journal des publicités en libre-service pour les expositions publicitaires dans la mesure Real-Time CDP Collaboration.
audience: admin, publisher, advertiser
badgelimitedavailability: label="Disponibilité limitée" type="Informative" url="https://helpx.adobe.com/legal/product-descriptions/real-time-customer-data-platform-collaboration.html newtab=true"
source-git-commit: 02f344c9fcfff20c84c2e92b5aa4647829dd5d2f
workflow-type: tm+mt
source-wordcount: '1712'
ht-degree: 3%
---

# Configurer des [!DNL Google Cloud Storage] pour le sourcing d’exposition publicitaire

Connectez votre compartiment [!DNL Google Cloud Storage] (GCS) à Adobe Real-Time CDP Collaboration pour obtenir des données d’exposition publicitaire source (journal publicitaire) à des fins de mesure.

Le module Mesure de Real-Time CDP Collaboration connecte les données de conversion des annonceurs aux journaux d’exposition des annonces des éditeurs afin de fournir des rapports de campagne axés sur la confidentialité. Cela ajoute un chemin d’accès en libre-service et sans code pour les annonceurs et les éditeurs. Vous pouvez importer les journaux d’exposition (impressions) d’annonces que vous conservez déjà en [!DNL Google Cloud Storage] dans la mesure pour attribution, sans dépendance Adobe Experience Platform. Vous connectez un compartiment, confirmez que les données détectées correspondent au schéma de journal des publicités attendu par Measurement et terminez en minutes.

Les données ne sont pas extraites au moment de la connexion. L&#39;approvisionnement est déclenché lorsque vous exécutez un rapport de mesure. Pour minimiser le stockage, Adobe supprime automatiquement les journaux d’annonces sources après une période de conservation de 7 jours.

Les règles de gouvernance et de gestion des données pour les journaux publicitaires provenant de [!DNL Google Cloud Storage] correspondent aux règles qui s’appliquent aux données provenant de Adobe Experience Platform.

>[!NOTE]
>
>Ce guide couvre l’approvisionnement des annonceurs et des éditeurs **journaux publicitaires** (expositions publicitaires) à partir de l’espace de stockage dans le cloud. L’approvisionnement des données de conversion à partir de l’espace de stockage cloud est bientôt disponible.

## Conditions préalables {#prerequisites}

Terminez tous les éléments de cette section avant de démarrer le workflow de configuration. Avant de suivre ce guide, vous devez avoir terminé [intégration et configuration du compte](./onboard-account.md).

### Accès et autorisations GCS {#gcs-access-permissions}

Vous ou votre administrateur [!DNL Google Cloud] devez accorder à Adobe un accès en lecture seule à votre compartiment GCS avant de démarrer l’assistant. Pour obtenir des instructions détaillées, voir [Configuration des autorisations de l’espace de stockage dans le cloud Google](#setup-gcs-permissions).


### Préparation des données du journal des publicités {#prepare-adlog-data}

Vos fichiers journaux des publicités doivent être conformes au schéma [journal des publicités](#ad-log-schema) avant que l’approvisionnement ne commence. Les principales exigences sont les suivantes :

* **Format de fichier :** CSV uniquement.
* **En-têtes de colonne canoniques :** les fichiers doivent utiliser les en-têtes de colonne canoniques définis dans le schéma [journal des publicités](#ad-log-schema). Cette version ne prend pas en charge le remappage par colonne ni le mappage de schéma automatisé.
* **Champs obligatoires :** tous les champs obligatoires doivent être présents, ainsi qu’au moins une clé de correspondance.
* **Hachage de la clé de correspondance :** les valeurs de hachage de la clé de correspondance doivent être des SHA hexadécimaux en minuscules-256.
* **Cohérence des colonnes :** chaque fichier situé à votre chemin d’accès configuré doit partager une disposition de colonne identique.
* **Sous-dossiers :** les fichiers doivent se trouver directement au chemin spécifié. Collaboration ne parcourt pas les sous-dossiers.

## Connexion et journaux dans l’assistant {#connect-adlogs}

Suivez les étapes ci-après pour connecter vos journaux publicitaires GCS à partir de Collaboration.

1. Dans l’espace de travail **[!UICONTROL Configuration]**, sélectionnez **[!UICONTROL Mes données de mesure]**, puis sélectionnez l’icône d’ajout et choisissez **[!UICONTROL Données de mesure]**.

   ![Espace de travail Configurer dans l’onglet Mes données de mesure, affichant l’icône d’ajout et l’option Données de mesure dans le menu.](../../assets/setup/gcs-adlog-sourcing/add-measurement-data-entry-point.png){zoomable="yes"}

2. Dans le workflow **[!UICONTROL Ajouter des données de mesure]**, sélectionnez **[!UICONTROL Expositions Advertising]** comme type de données de mesure, puis sélectionnez **[!UICONTROL Suivant]**.

   ![Le workflow Ajouter des données de mesure présentant la sélection du type de données de mesure, avec les expositions Advertising sélectionnées.](../../assets/setup/gcs-adlog-sourcing/select-adlog-data-type.png){zoomable="yes"}

3. Pour importer vos données de mesure, sélectionnez **[!UICONTROL Ajouter une nouvelle connexion de données]**, puis sélectionnez **[!UICONTROL Suivant]**.

   ![Le workflow Ajouter des données de mesure présentant l’étape de sélection de la connexion de données, avec l’option Ajouter une nouvelle connexion de données sélectionnée.](../../assets/setup/gcs-adlog-sourcing/add-new-data-connection.png){zoomable="yes"}

4. Choisissez la source de données de votre nouvelle connexion de données : **[!UICONTROL Google Cloud Storage]**. Sélectionnez **[!UICONTROL Suivant]**.

   ![Le workflow Ajouter des données de mesure présentant l’étape de sélection de la source de données, avec les options Google Cloud Storage, Azure Blob Storage et Azure Data Lake Storage Gen 2 et Google Cloud Storage sélectionnées.](../../assets/setup/gcs-adlog-sourcing/gcs-adlog-source-selection.png){zoomable="yes"}

5. L’assistant **[!UICONTROL Ajouter une connexion de données]** s’ouvre. À l’étape **[!UICONTROL Connecter Google Cloud Storage]**, indiquez le **[!UICONTROL compartiment]** et le **[!UICONTROL chemin]** où se trouvent vos fichiers journaux des publicités. Les deux champs sont obligatoires et tous les fichiers du chemin d’accès configuré sont traités comme un seul jeu de données.

   ![Assistant d’ajout de connexion aux données à l’étape Connexion à Google Cloud Storage, affichant les champs Compartiment et Chemin requis.](../../assets/setup/gcs-adlog-sourcing/gcs-adlog-connection-details.png){zoomable="yes"}

6. À l’étape **[!UICONTROL Nom et description]**, fournissez un **[!UICONTROL Nom de la connexion de données]** obligatoire et un **[!UICONTROL Description]** facultatif pour la connexion de données.

   ![l’étape Nom et description, affichant le nom de la connexion de données et les champs Description.](../../assets/setup/gcs-adlog-sourcing/gcs-adlog-name-description.png){zoomable="yes"}

7. Dans l’étape **[!UICONTROL Mapper les champs]**, prévisualisez les colonnes détectées pour confirmer que l’assistant lit les fichiers appropriés, puis passez en revue le schéma du journal des publicités [ad](#ad-log-schema) qui répertorie chaque champ que la mesure comprend, les champs obligatoires et facultatifs, et les colonnes détectées reconnues comme clés d’identité/de correspondance. Cette étape est une validation en lecture seule : le système confirme la présence des en-têtes requis et vous bloque si un champ obligatoire est manquant. Cette version ne comporte aucun remappage par colonne.

   ![l’étape Mapper les champs qui affiche la prévisualisation des colonnes détectées et la révision du schéma du journal des publicités.](../../assets/setup/gcs-adlog-sourcing/gcs-adlog-map-fields.png){zoomable="yes"}

8. À l’étape **[!UICONTROL Réviser]**, révisez et terminez. La connexion apparaît dans la zone de données de mesure avec son état, qui reste **en attente** jusqu&#39;à ce que le premier rapport de mesure exécute les données de la source.

## Fonctionnement de l’approvisionnement des journaux d’annonces {#how-it-works}

L’approvisionnement des journaux publicitaires depuis [!DNL Google Cloud Storage] reflète le flux de haut niveau utilisé pour l’approvisionnement des audiences :

1. **Connexion de stockage dans le cloud :** vous configurez l’accès en lecture seule à un compartiment qui contient vos journaux publicitaires.
2. **Révision et validation des schémas :** le système valide les fichiers par rapport au schéma du journal des publicités (vérifications de dossier, de fichier et d’en-tête requis ; lecture seule).
3. **Mappage de champs :** champs d’identité source sont automatiquement mappés à des champs canoniques en fonction des noms de colonne canoniques. Il n’existe aucun remappage manuel.
4. **Ingestion et normalisation :** événements sont normalisés à une ligne par exposition. L’approvisionnement des journaux d’annonces démarre lorsque vous exécutez un rapport de mesure.

### Schéma des Ad Logs (format CSV canonique) {#ad-log-schema}

Les champs obligatoires doivent être présents et au moins un champ marqué **Clé de jointure (un des obligatoires)** dans le tableau suivant doit également être présent. Les valeurs de hachage de clé de correspondance sont des SHA-256 hexadécimaux en minuscules.

| Champ | Type de données | Requis | Description |
| --- | --- | --- | --- |
| `EVENT_DATETIME` | Chaîne (ISO 8601) | Requis | Date et heure de l’événement |
| `EVENT_ID` | Chaîne | Facultatif | ID unique de l’événement |
| `EVENT_TYPE` | Chaîne (énumération) | Requis | Type d’événement. Un de `{impression, click}` |
| `HASHED_EMAIL_SHA_256` | Chaîne (hexadécimale de 64 caractères) | Clé de jointure (une seule requise) | Sha-256 hexadécimal inférieur de l’e-mail |
| `HASHED_IPV4_SHA_256` | Chaîne (hexadécimale de 64 caractères) | Clé de jointure (une seule requise) | SHA-256 hexadécimal en minuscules d’IPv4 |
| `DEVICE_ID` | Chaîne (hexadécimale de 64 caractères) | Clé de jointure (une seule requise) | Identifiant publicitaire de l’appareil |
| `DEVICE_ID_TYPE` | Chaîne (énumération) | Facultatif | Un de `{idfa, gaid, aaid, rida, afai, msai, vida, lgudid, tifa}` |
| `ECID` | Chaîne (hexadécimale de 64 caractères) | Clé de jointure (une seule requise) | ECID basé sur Demdex |
| `CUSTOM_ID` | Chaîne | Facultatif | ID persistant de l’éditeur/du partenaire (par exemple, PPID, RampID, Core ID) |
| `ADVERTISER_ID` | Chaîne | Requis | Identifiant unique de l’annonceur |
| `ADVERTISER_NAME` | Chaîne | Facultatif | Publicitaire/nom de marque |
| `CAMPAIGN_ID` | Chaîne | Requis | Identifiant de campagne spécifique à la plateforme |
| `CAMPAIGN_NAME` | Chaîne | Facultatif | Nom de campagne lisible par l’utilisateur |
| `PLACEMENT_ID` | Chaîne | Requis | Identifiant unique de l’emplacement |
| `PLACEMENT_NAME` | Chaîne | Facultatif | Nom d’emplacement descriptif |
| `CREATIVE_ID` | Chaîne | Facultatif | Identifiant unique du contenu publicitaire |
| `CREATIVE_NAME` | Chaîne | Facultatif | Nom créatif lisible par l’utilisateur |
| `AUDIENCE_ID` | Chaîne | Facultatif | Identifiant du segment ciblé |
| `AUDIENCE_NAME` | Chaîne | Facultatif | Nom de l’audience lisible par l’utilisateur |
| `DEVICE_TYPE` | Chaîne (énumération) | Facultatif | Un de `{mobile, desktop, tablet, ctv, dooh, car, in_store, other}` |
| `AD_FORMAT` | Chaîne (énumération) | Facultatif | Un de `{display, video, native, audio, search, commerce, dooh, other}` |
| `SITE_NAME` | Chaîne | Facultatif | Propriété réseau/site/application/éditeur sur laquelle l’impression s’est produite. |
| `TEST_GROUP` | Chaîne | Facultatif | Regroupement pour les études de portance, les essais/contrôles, les groupes d&#39;exclusion |
| `CUSTOM_DIM` | Chaîne | Facultatif | Dimension d’éditeur supplémentaire |

{style="table-layout:auto"}

>[!NOTE]
>
>`MATCH_KEY_TYPE` est inclus dans le schéma sous la forme d’un champ facultatif afin que, au fil du temps, plusieurs types d’ID puissent être pris en charge en parallèle et que la provenance des clés de correspondance (e-mail, téléphone ou CRM) puisse être conservée sans rompre le contrat v1.

### Exigences de validation (v1) {#validation-requirements}

Le système valide et consigne les données sources avant la fin du workflow de configuration. Contrôles de validation :

* Le dossier source doit contenir au moins un fichier.
* Les fichiers ne peuvent pas être vides.
* Les en-têtes de schéma requis doivent être présents.
* Les champs de schéma facultatifs peuvent être omis.
* Les fichiers contenant uniquement les champs obligatoires sont valides.

Les échecs de validation vous empêchent de continuer. Le système ne valide **pas** les types de données, les valeurs de champ, l’exhaustivité des enregistrements, la qualité des données ou le mappage automatisé des schémas. La validation est limitée aux contrôles de dossiers, de fichiers et d’en-têtes obligatoires pour cette version initiale.

## Limites connues {#known-limitations}

Tenez compte des contraintes suivantes lors de la configuration et de l’utilisation de l’approvisionnement des journaux d’annonces [!DNL Google Cloud Storage] :

* **Journaux publicitaires uniquement :** cette connexion fournit les journaux publicitaires de l’annonceur ou de l’éditeur (expositions publicitaires). Les données de conversion ne sont pas encore prises en charge.
* **Sources prises en charge :** [!DNL Google Cloud Storage] et [!DNL Azure Data Lake Storage] ou [!DNL Azure Blob Storage].
* **Format de fichier :** CSV uniquement.
* **En-têtes canoniques requis :** il n’existe aucun remappage par colonne ni aucun mappage intelligent/automatisé dans cette version. Vos fichiers doivent utiliser les noms de colonne canoniques.
* **Aucune validation de valeur/type :** seuls les en-têtes de colonne obligatoires sont validés. Au départ, il peut n’y avoir aucune ligne de données.
* **Aucune modification apportée à une connexion après sa création :** toute modification, y compris la modification des clés de correspondance actives, nécessite la création d’une nouvelle connexion.
* **Une disposition par chemin d’accès :** tous les fichiers du chemin d’accès doivent partager une disposition de colonne identique. Des dispositions mixtes peuvent entraîner des échecs de sourcing partiel.
* **Sous-dossiers non parcourus :** les fichiers doivent se trouver directement au chemin spécifié.
* **Pas de planification ni d’analyse lors de la configuration :** l’approvisionnement des journaux d’annonces commence lorsque vous exécutez un rapport de mesure. Définissez la période d’analyse lorsque vous configurez le rapport.
* **Une connexion aux données du journal des publicités :** configurer une seule connexion aux données du journal des publicités à la fois. Les rapports de mesure utilisent automatiquement la connexion configurée.

## Dépannage {#troubleshooting}

* **La connexion apparaît en attente/aucune donnée :** attendu jusqu’à la première exécution du rapport de mesure. Aucune donnée n’est générée au moment de la connexion.
* **« Aucune donnée trouvée » à l’étape source :** Le dossier est vide. Ajoutez les fichiers avant de continuer.
* **L’aperçu n’affiche aucune colonne :** le fichier est présent mais vide (aucun en-tête ni contenu).
* **Impossible d’obtenir une validation ultérieure :** un en-tête de colonne obligatoire est manquant. Vérifiez les champs obligatoires et la présence d’au moins une clé de correspondance, à l’aide de noms canoniques.
* **Colonnes non reconnues :** les noms de colonne non canoniques ne sont pas sélectionnés en tant que champs connus. Renommez-les au format canonique. Il n’existe aucun remappage dans cette version.
* **L’approvisionnement échoue après la configuration :** vérifiez qu’Adobe n’a pas modifié l’accès en lecture au compartiment et que les fichiers existent toujours au chemin configuré au format canonique.
* **Période du rapport non entièrement couverte :** mémorisez l’expiration automatique des données de 7 jours. Les journaux de plus de 7 jours peuvent ne pas être disponibles pour la plage demandée.

## Configurer les autorisations [!DNL Google Cloud Storage] {#setup-gcs-permissions}

Pour permettre à Adobe de lire à partir de votre compartiment GCS, créez un rôle IAM personnalisé avec les autorisations suivantes :

| Autorisation | Rôle |
| ------------- | --------------- |
| `storage.buckets.get` | Lire les métadonnées du compartiment. |
| `storage.objects.get` | Lire des données et des métadonnées d’objet. |
| `storage.objects.list` | Répertorier les objets dans un compartiment. |

{style="table-layout:auto"}

Accordez ce rôle personnalisé au compte de service Adobe Google pour votre région (Amérique du Nord, EMEA ou Australie). Pour effectuer cette configuration, vous devez disposer des privilèges **Administrateur de compte Google Cloud**.

## Considérations relatives à la mise à niveau ou à la migration {#upgrade-migration}

* Les clients précédemment intégrés via Experience Platform ou une configuration assistée par Adobe peuvent passer au chemin de stockage dans le cloud en libre-service. Les rapports et flux de mesure existants restent inchangés.
* Les clés de correspondance présentes dans les fichiers journaux des publicités doivent être activées pour le compte Collaboration, comme pour l’approvisionnement des audiences.
* Les règles de gouvernance et de gestion des données correspondent aux données provenant d’Experience Platform.

## Étapes suivantes {#next-steps}

Une fois l’approvisionnement terminé, vos journaux publicitaires sont disponibles pour le compte rendu des performances.

Pour d’autres méthodes de source d’exposition publicitaire, voir [Configurer le stockage Azure pour la source d’exposition publicitaire](./configure-azure-adlog-sourcing.md).
