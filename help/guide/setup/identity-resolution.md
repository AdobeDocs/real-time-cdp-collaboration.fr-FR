---
title: Configurer et gérer la résolution d’identité
description: Découvrez comment configurer et gérer la résolution d’identité dans Real-Time CDP Collaboration.
audience: admin, publisher, advertiser, agency
badgelimitedavailability: label="Disponibilité limitée" type="Informative" url="https://helpx.adobe.com/fr/legal/product-descriptions/real-time-customer-data-platform-collaboration.html newtab=true"
product_v2:
  - id: fdddec33-c9cb-4459-b8b6-2664395a6f10
    internal-label: Real-Time Customer Data Platform
source-git-commit: ff233017fb78a63b2e911dc0dc94d67f2b18af04
workflow-type: tm+mt
source-wordcount: '1110'
ht-degree: 1%
---
# Configurer et gérer la résolution d’identité

{{limited-availability-release-note}}

La résolution d’identité vous permet d’identifier les clients que vous avez en commun avec les collaborateurs, même si vos organisations utilisent des identifiants différents. Configurez et gérez la résolution d’identité avec les fournisseurs d’identité pris en charge dans Real-Time CDP Collaboration, sans créer d’intégrations personnalisées pour chaque partenaire.

>[!NOTE]
>
>Les étapes et les captures d’écran de ce guide utilisent [!DNL Epsilon Core ID] comme exemple. Les conditions requises et les options disponibles peuvent varier en fonction de votre fournisseur d’identité.

>[!AVAILABILITY]
>
>Au lancement, seul [!DNL Epsilon Core ID] peut être configuré. La résolution d’identité Epsilon Core ID n’est disponible que pour les comptes Real-Time CDP Collaboration configurés aux États-Unis.

## Conditions préalables {#prerequisites}

Avant de commencer, vérifiez que vous disposez des éléments suivants :

* **Autorisations de gestion de compte.** Vous devez disposer des autorisations **[!UICONTROL Gérer le compte]** et **[!UICONTROL Gérer les instances Collaboration]**.
* **Au moins une connexion de données d’audience.** Vous avez besoin d’une connexion de données d’audience existante pour configurer la résolution d’identité. [Configurez le sourcing d’audience](./source-overview.md) si nécessaire. Les connexions aux données de mesure ne sont pas prises en charge.
* **Clés et champs de correspondance pris en charge.** Chaque connexion de données d’audience que vous prévoyez d’utiliser pour la résolution d’identité doit contenir des champs pris en charge par votre fournisseur d’identité. Pour l’Epsilon Core ID, vous pouvez utiliser une adresse e-mail, un numéro de téléphone ou un nom hachés associés à une adresse postale.

  Les clés de correspondance au niveau du compte, telles que l’e-mail et le téléphone hachés, doivent être activées pour votre compte et mappées aux données de votre audience. Les champs Nom et Adresse postale sont mappés lors de la configuration de la connexion aux données d’audience et ne nécessitent pas d’activation au niveau du compte.

  Si vous utilisez le nom et l’adresse postale, mappez au moins un champ de chaque groupe :

  * **Nom :** prénom, nom ou nom complet.
  * **Adresse postale :** adresse postale, ville, code postal, état ou pays.

  Les valeurs de nom et d’adresse postale ne sont pas hachées. Pour obtenir des instructions sur l’activation des clés de correspondance au niveau du compte, telles que les e-mails et les téléphones hachés, voir [Modifier les clés de correspondance](./onboard-account.md#edit-match-keys). Pour mapper les clés de correspondance prises en charge ou les champs de nom et d’adresse postale à vos données d’audience, voir [Mapper les champs](./onboard-audiences.md#map-fields).
* **Numéro de compte Epsilon.** Obtenez votre numéro de compte Epsilon auprès de votre représentant de compte Epsilon.

## Configurer la résolution d’identité {#configure-identity-resolution}

Sélectionnez un fournisseur d’identité pour commencer à configurer la résolution d’identité. Dans cet exemple de [!DNL Epsilon Core ID], vous allez vous authentifier auprès du fournisseur, sélectionner les connexions de données d’audience, définir une période et vérifier votre configuration avant de confirmer.

Pour commencer, sélectionnez **[!UICONTROL Configuration]** dans le volet de navigation de gauche, puis l’onglet **[!UICONTROL Résolution d’identité]** pour afficher les fournisseurs d’identité disponibles.

### Sélectionner un fournisseur d’identité {#select-identity-provider}

Recherchez la carte de votre fournisseur d’identité et vérifiez sa région prise en charge ainsi que les clés de correspondance. Sélectionnez **[!UICONTROL Configuration]** pour commencer.

![Catalogue des fournisseurs d’identité avec la carte d’identité principale Epsilon et son action de configuration.](../../assets/setup/identity-resolution/select-an-identity-provider.png){zoomable="yes"}

Avant de lancer le workflow de configuration, Collaboration recherche une connexion aux données et des clés de correspondance compatibles. Si une exigence est manquante, une boîte de dialogue s’affiche pour guider le processus. Suivez l’action dans la boîte de dialogue :

* **[!UICONTROL Connexion de données requise] :** sélectionnez **[!UICONTROL Configurer la connexion de données]** pour configurer une connexion de données d’audience. Voir [Connexion d’une source](./source-overview.md#connect-a-source).
* **[!UICONTROL Clé de correspondance requise] :** sélectionnez **[!UICONTROL Modifier les clés de correspondance]** pour activer une clé prise en charge. Voir [Modifier les clés de correspondance](./onboard-account.md#edit-match-keys).

Si les deux sont manquants, la boîte de dialogue de connexion aux données s’affiche en premier. Après avoir corrigé les conditions préalables, revenez à **[!UICONTROL Résolution d’identité]** et sélectionnez à nouveau **[!UICONTROL Configuration]**.

### Authentification auprès de votre fournisseur d’identité {#authenticate-with-provider}

À l’étape **[!UICONTROL Authentifier]**, fournissez les informations requises par votre fournisseur d’identité. Pour Epsilon Core ID, saisissez le numéro de compte fourni par votre représentant Epsilon dans le champ **[!UICONTROL Numéro de compte Epsilon]**. Sélectionnez **[!UICONTROL Suivant]** pour continuer.

![Étape d’authentification affichant le champ Numéro de compte Epsilon.](../../assets/setup/identity-resolution/authenticate.png){zoomable="yes"}

### Sélectionner les connexions de données {#select-data-connections}

Choisissez ensuite les connexions de données d’audience à utiliser pour la résolution d’identité. Cela détermine les données d’audience qui seront utilisées pour faire correspondre vos identités client avec votre fournisseur d’identité. La résolution d’identité utilise automatiquement les identifiants pris en charge mappés dans chaque connexion sélectionnée.
Choisissez ensuite les connexions de données d’audience à utiliser pour la résolution d’identité. Les connexions sélectionnées déterminent quelles données d’audience et quels champs mappés sont disponibles pour la résolution d’identité.

La résolution d’identité s’applique à toutes les audiences de chaque connexion de données sélectionnée, y compris les audiences ajoutées ultérieurement. Vous ne pouvez pas sélectionner d’audiences individuelles pour le moment.

Si la connexion que vous souhaitez ne figure pas dans la liste, [configurez la connexion aux données de l’audience](./source-overview.md) avant de continuer.

Sous **[!UICONTROL Source(s) de données)]** cochez la case correspondant à chaque connexion à inclure dans **[!UICONTROL Sources d’audience]**. Vous devez sélectionner au moins une connexion. Sélectionnez **[!UICONTROL Suivant]** pour continuer.

![Cartes de source d’audience affichant les connexions de données sélectionnées et non sélectionnées.](../../assets/setup/identity-resolution/source-selection.png){zoomable="yes"}

### Définir un planning de résolution d’identité {#set-schedule}

Sélectionnez les dates de début et de fin pour définir la période pendant laquelle Adobe actualise les identifiants de partenaire. La fréquence d’actualisation est déterminée par les connexions de données d’audience sélectionnées. Vous ne pouvez donc pas configurer une fréquence d’actualisation distincte pour la résolution des identités.

À l’étape **[!UICONTROL Planifier]**, sélectionnez la commande de calendrier sous **[!UICONTROL Période]** et choisissez vos dates. Sélectionnez **[!UICONTROL Suivant]** pour continuer.

![Étape Planifier avec une période pour la résolution d’identité Epsilon Core ID.](../../assets/setup/identity-resolution/schedule-identity-resolution-job.png){zoomable="yes"}

### Examinez et confirmez la configuration {#review-and-confirm}

À l’étape **[!UICONTROL Révision]**, vérifiez vos détails d’authentification, les connexions de données d’audience sélectionnées et le planning. Pour apporter des modifications, sélectionnez **[!UICONTROL Modifier]** en regard de la section correspondante.

Vous ne pouvez pas modifier la configuration après l’installation. Pour apporter des modifications ultérieurement, vous devez le supprimer et le configurer à nouveau. Une fois vos sélections effectuées, sélectionnez **[!UICONTROL Confirmer et planifier]**.

![Étape de révision affichant l’authentification, les sources de données et le résumé du planning.](../../assets/setup/identity-resolution/review-and-confirm.png){zoomable="yes"}

Une boîte de dialogue de confirmation indique que la résolution d’identité a été configurée avec succès.

<!-- [Question: Does the first identity resolution run happen immediately after setup, or at the next scheduled audience data connection refresh?] -->

## Gestion de la résolution des identités {#manage-identity-resolution}

Après avoir confirmé votre configuration, vous revenez automatiquement à l’onglet **[!UICONTROL Résolution d’identité]**, où vous pouvez afficher ou supprimer votre configuration.

### Afficher les détails de configuration {#view-configuration-details}

Pour vérifier votre configuration, sélectionnez **[!UICONTROL Afficher les détails]** sur la carte de votre fournisseur d’identité configuré.

Passez en revue les détails d’authentification, les connexions de données d’audience sélectionnées et la période. Vous pouvez également afficher les clés de correspondance affichées dans les détails de configuration, ainsi que le statut de la configuration et les informations de création et de mise à jour.

![Détails de la configuration de la résolution d’identité affichant le statut, les clés de correspondance, le planning et la connexion d’audience associée.](../../assets/setup/identity-resolution/view-connection-details.png){zoomable="yes"}

### Modifier une configuration existante {#edit-configuration}

Vous ne pouvez pas modifier une configuration d’identifiant principal après l’installation. Pour modifier le numéro de compte Epsilon, les connexions de données sélectionnées ou la période, [supprimez la configuration](#delete-configuration) et effectuez à nouveau le [workflow de configuration](#configure-identity-resolution).

<!-- Question: Do other providers have the same limitation? -->

### Suppression d’une configuration de résolution d’identité {#delete-configuration}

Pour supprimer une configuration, accédez à **[!UICONTROL Configuration]** > **[!UICONTROL Résolution d’identité]** et sélectionnez **[!UICONTROL Supprimer]** sur la carte de votre fournisseur d’identité configuré. Consultez la boîte de dialogue de confirmation, puis sélectionnez **[!UICONTROL Supprimer]** pour confirmer.

Si vous souhaitez réutiliser ce fournisseur d’identité, vous devez [configurer](#configure-identity-resolution) une nouvelle configuration.

<!-- [UNVERIFIED: Does deletion affect previously resolved identifiers, future processing, or both? Confirm before publication.] -->

## Résolution des problèmes de configuration {#troubleshoot}

Si vous ne pouvez pas démarrer la configuration car une connexion de données ou une clé de correspondance est manquante, suivez les instructions de la section [Sélectionner un fournisseur d’identité](#select-identity-provider).

Pour Epsilon Core ID, vérifiez les éléments suivants :

* **Non disponible dans votre région :** Epsilon Core ID est disponible uniquement pour les comptes Collaboration configurés aux États-Unis.
* **Numéro de compte Epsilon non disponible :** contactez votre représentant Epsilon pour obtenir votre numéro de compte.
