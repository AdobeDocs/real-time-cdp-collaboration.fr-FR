---
title: Configuration et gestion des destinations de stockage dans le cloud
description: Découvrez comment configurer, afficher et supprimer une destination d’espace de stockage dans Real-Time CDP Collaboration.
audience: admin, publisher
badgelimitedavailability: label="Disponibilité limitée" type="Informative" url="https://helpx.adobe.com/fr/legal/product-descriptions/real-time-customer-data-platform-collaboration.html newtab=true"
product_v2:
  - id: fdddec33-c9cb-4459-b8b6-2664395a6f10
topic_v2:
  - id: b5520579-b31f-4df7-9281-f0d9f91e2edc
  - id: e1e0219c-f879-479f-8427-888ed2a6e9c2
source-git-commit: 60124235569ca9b17b3bb1cef502d57d39e82e1f
workflow-type: tm+mt
source-wordcount: 885
ht-degree: 1%

---

# Configuration et gestion des destinations de stockage dans le cloud

Utilisez ce guide pour configurer, afficher et supprimer des destinations d’espace de travail d’**[!UICONTROL activation]** de stockage dans le cloud. Utilisez l’onglet **[!UICONTROL Catalogue]** pour configurer les destinations, l’onglet **[!UICONTROL Destinations]** pour les gérer et l’onglet **[!UICONTROL Audiences activées]** pour passer en revue les audiences activées vers les destinations.

Une fois la destination configurée, elle devient disponible lorsque vous activez des audiences. Pour afficher la liste complète des destinations prises en charge, reportez-vous au tableau [destinations disponibles](./overview.md#available-destinations).

>[!NOTE]
>
> Ce guide utilise une destination **[!DNL Amazon S3]** comme exemple. Le workflow de configuration guidée est partagé entre les types de destination d’espace de stockage pris en charge, mais les méthodes d’authentification, les champs obligatoires et les fonctionnalités du connecteur peuvent varier. Avant de configurer une destination, passez en revue les [exigences de destination de l’espace de stockage](./cloud-storage-destination-requirements.md), qui renvoient à la documentation de destination Adobe Experience Platform correspondante.
>
> Adobe Experience Platform dispose d’un workflow de configuration distinct dans Real-Time CDP Collaboration. Pour le configurer, voir [Configurer Adobe Experience Platform en tant que destination](./experience-platform.md).

## Conditions préalables {#prerequisites}

Avant de configurer une destination, vérifiez les points suivants :

* Vous avez accès à l’espace de travail **[!UICONTROL Activation]**.
* Vous disposez des informations de connexion requises par votre fournisseur d’espace de stockage dans le cloud.
* Si vous devez créer un compte, vous disposez des informations d’identification ou des autorisations requises.
* Vous avez examiné les exigences [requises pour votre destination d’espace de stockage](./cloud-storage-destination-requirements.md).

## Configuration d’une destination {#configure-destination}

Lorsque vous configurez une destination, vous connectez un compte d’espace de stockage à Real-Time CDP Collaboration et définissez la manière dont les données d’audience y sont exportées.

Accédez à **[!UICONTROL Activation]** > **[!UICONTROL Catalogue]**.

L’onglet **[!UICONTROL Catalogue]** affiche les fournisseurs de destination disponibles. Chaque destination s’affiche sous forme de carte. Selon la destination, sa carte peut afficher des comptes et des actions configurés pour afficher des informations supplémentaires.

![Onglet Catalogue affichant les cartes de fournisseur de destination.](/help/assets/destinations/manage-destinations/destination-provider-catalog.png)

Recherchez le fournisseur de destination à configurer et sélectionnez **[!UICONTROL Configurer]**.

La configuration de destination guidée s’ouvre et vous guide tout au long des quatre étapes suivantes : **[!UICONTROL Authentifier]**, **[!UICONTROL Créer une destination]**, **[!UICONTROL Mapper des champs]** et **[!UICONTROL Réviser]**.

### Authentifier {#authenticate}

L’étape **[!UICONTROL Authentifier]** établit une connexion entre Real-Time CDP Collaboration et votre compte de destination.

Si un compte existant est disponible, sélectionnez-le dans le sélecteur de comptes. Pour créer un compte, sélectionnez **[!UICONTROL Nouveau compte]**.

Sélectionnez une méthode d’authentification et fournissez les informations de compte requises. Les méthodes et champs d’authentification disponibles dépendent du fournisseur de destination sélectionné. Pour connaître les exigences spécifiques au connecteur, voir [Exigences de destination de l’espace de stockage dans le cloud](./cloud-storage-destination-requirements.md).

Sélectionnez **[!UICONTROL Connexion à Amazon S3]**. Pour les autres fournisseurs de destination, le bouton affiche le nom du fournisseur correspondant.

Une fois le compte validé, sélectionnez **[!UICONTROL Suivant]**.

![L’étape Authentifier présentant la sélection du compte et la création d’un compte.](/help/assets/destinations/manage-destinations/authenticate-destination-account.png)

### Créer une destination {#create-destination}

L’étape **[!UICONTROL Créer une destination]** définit où et comment les fichiers d’exportation d’audience sont diffusés.

Saisissez un nom de destination et renseignez les paramètres de stockage et d’exportation requis. Les champs disponibles dépendent du fournisseur de destination sélectionné. Pour les définitions et les exigences spécifiques aux connecteurs, reportez-vous à la documentation de destination liée à [Exigences de destination de l’espace de stockage](./cloud-storage-destination-requirements.md).

Une fois tous les champs obligatoires renseignés, sélectionnez **[!UICONTROL Suivant]**. La configuration guidée passe à l’étape de mappage des champs.

![L’étape Créer une destination affichant les champs de configuration de destination.](/help/assets/destinations/manage-destinations/configure-new-destination.png)

### Champs de mappage {#map-fields}

L’étape **[!UICONTROL Mapper les champs]** définit la manière dont les clés de correspondance d’audience sont mappées aux champs d’identité attendus par la destination.

Contrairement au workflow des destinations Real-Time CDP standard, Real-Time CDP Collaboration configure ces mappages pendant la création de la destination. Les clés de correspondance d’audience apparaissent sous la forme de champs sources. Mappez chaque champ source à l’identité cible correspondante afin que la destination puisse reconnaître les identifiants exportés et les associer aux utilisateurs prévus.

Sélectionnez **[!UICONTROL Ajouter un champ]** pour ajouter un autre mappage de clé de correspondance, ou sélectionnez l’icône de suppression pour supprimer un mappage. Examinez et configurez tous les mappages requis.

Une fois les mappages terminés, sélectionnez **[!UICONTROL Suivant]**. La configuration guidée passe à l’étape de révision.

![L’étape Mapper des champs affiche la configuration de mappage des clés d’activation.](/help/assets/destinations/manage-destinations/map-destination-fields.png)

### Réviser {#review-destination}

L’étape **[!UICONTROL Révision]** résume la configuration de destination avant sa création.

Vérifiez les paramètres de destination. Pour apporter des modifications, sélectionnez l’icône en forme de crayon ![Icône en forme de crayon.](../../assets/icons/edit.png) pour la section applicable et mettez à jour la configuration.

Lorsque la configuration est correcte, sélectionnez **[!UICONTROL Terminé]**. La destination est créée et devient disponible pour l’activation de l’audience.

![Étape de révision affichant le résumé de la configuration de destination avant la fin.](/help/assets/destinations/manage-destinations/review-destination-configuration.png)

## Afficher les destinations configurées {#view-configured-destinations}

Une fois une destination configurée, elle apparaît dans votre inventaire de destinations. Dans l’inventaire, vous pouvez consulter son statut et les audiences qui y sont activées.

Accédez à **[!UICONTROL Activation]** > **[!UICONTROL Destinations]**. L’onglet **[!UICONTROL Destinations]** affiche un tableau des destinations configurées.

![L’onglet Destinations affiche les destinations configurées.](/help/assets/destinations/manage-destinations/configured-destinations-list.png)

## Supprimer une destination {#delete-destination}

Supprimez une destination lorsqu’elle n’est plus nécessaire à l’activation de l’audience. La suppression d’une destination la supprime de votre inventaire de destination et empêche l’activation d’audiences vers cette destination à l’avenir.

>[!IMPORTANT]
>
>La suppression d’une destination ne supprime pas les données d’audience qui y ont été précédemment exportées. Supprimez les données précédemment exportées directement du magasin de données de destination.

Accédez à **[!UICONTROL Activation]** > **[!UICONTROL Destinations]**.

Recherchez la destination à supprimer, sélectionnez l’icône représentant des points de suspension dans la colonne **[!UICONTROL Action]**, puis sélectionnez **[!UICONTROL Supprimer]**.

![Onglet Destinations de l’espace de travail Activation avec l’icône représentant des points de suspension et l’action Supprimer mise en surbrillance.](/help/assets/destinations/manage-destinations/delete-configured-destination.png)

Une boîte de dialogue de confirmation s’affiche. Vérifiez la destination qui sera supprimée, puis sélectionnez **[!UICONTROL Supprimer]** pour confirmer.

La destination est supprimée de votre inventaire de destination et n’est plus disponible pour l’activation des audiences.

## Étapes suivantes {#next-steps}

Une fois la destination configurée, vous pouvez commencer [l’activation des audiences](../collaborate/activate.md) dans vos projets.
