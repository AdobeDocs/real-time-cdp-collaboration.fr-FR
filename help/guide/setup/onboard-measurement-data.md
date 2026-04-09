---
title: Ajouter et gérer des données de mesure
description: Découvrez comment ajouter des données de mesure à Adobe Real-Time CDP Collaboration.
audience: admin, publisher, advertiser
badgelimitedavailability: label="Disponibilité limitée" type="Informative" url="https://helpx.adobe.com/legal/product-descriptions/real-time-customer-data-platform-collaboration.html newtab=true"
exl-id: 739d31b9-3f00-477d-b6be-995c7767c6ca
source-git-commit: e06ee94afdd1edbf86430cbe348dc448419b8f4e
workflow-type: tm+mt
source-wordcount: '2720'
ht-degree: 4%

---

# Ajouter et gérer des données de mesure {#add-and-manage-measurement-data}

>[!CONTEXTUALHELP]
>id="rtcdp_collaboration_onboard_measurement_data"
>title="En savoir plus"
>abstract=""

>[!CONTEXTUALHELP]
>id="rtcdp_collaboration_measurement_data_target_fields"
>title="Champs cibles"
>abstract="Espace réservé pour les champs cibles de mesure."

>[!CONTEXTUALHELP]
>id="rtcdp_collaboration_measurement_data_source_fields"
>title="Champs sources"
>abstract="Espace réservé pour les champs sources de mesure."

>[!CONTEXTUALHELP]
>id="rtcdp_collaboration_import_measurement_mapping_source_fields"
>title="Champs sources de mapping"
>abstract="Espace réservé pour les champs sources de mapping de mesure."

>[!CONTEXTUALHELP]
>id="rtcdp_collaboration_import_measurement_mapping_target_fields"
>title="Champs cibles de mapping"
>abstract="Espace réservé pour les champs cibles de mapping de mesure."

{{limited-availability-release-note}}

Ce document décrit les étapes à suivre pour ajouter des données de mesure de campagne à Adobe Real-Time CDP Collaboration. Les éditeurs peuvent collaborer avec les équipes d’Adobe pour charger les données de mesure des campagnes. Une fois les données chargées et traitées, l’éditeur et l’annonceur pourront afficher des rapports de mesure de campagne [campaign](/help/guide/collaborate/measure.md) complets.

## Ajouter des données de mesure {#add-measurement-data}

En tant qu’annonceur, vous pouvez charger vos données de mesure contenant des événements de conversion vers Collaboration pour les utiliser dans des rapports de mesure de campagne. Les données de conversion comprennent généralement des champs tels que les identifiants d’utilisateur (par exemple, des e-mails ou des identifiants d’appareil hachés), l’horodatage de l’événement de conversion et des détails spécifiques à l’événement de conversion, tels que l’achat ou l’inscription.

Pour générer des données de mesure, accédez à l’onglet **[!UICONTROL Mes données de mesure]** dans l’espace de travail **[!UICONTROL Configuration]**. Sélectionnez l’icône d’ajout (![Ajouter une icône.](/help/assets/icons/plus.png)) puis sélectionnez **[!UICONTROL Données de mesure]**.

S&#39;il s&#39;agit de vos premières données de mesure, vous pouvez également sélectionner l&#39;option **[!UICONTROL Ajouter]**.

![Onglet Mes données de mesure avec l’option Ajouter et l’option Données de mesure en surbrillance.](../../assets/setup/add-manage-measurement-data/add-measurement-data.png){zoomable="yes"}

L’écran **[!UICONTROL Ajouter des données de mesure]** s’affiche, affichant un résumé des étapes pour générer les données de mesure. Sélectionnez **[!UICONTROL Démarrer l’intégration]**.

![L’écran Ajouter des données de mesure affiche un résumé des étapes permettant de générer les données de mesure et l’option d’intégration Démarrer mise en surbrillance.](../../assets/setup/add-manage-measurement-data/add-measurement-data-screen.png){zoomable="yes"}

### Détails et connexion de données {#data-connection-and-details}

Au cours de cette étape, vous devez configurer votre connexion de données et spécifier les détails de vos données de mesure.

#### Sélectionner le type de données de mesure {#select-measurement-data-type}

Le type de données de mesure définit le type d’événements que vous importez pour la mesure de la campagne. Actuellement, le type de données de conversion est pris en charge.

Sélectionnez **[!UICONTROL Données de conversion]** comme type de données de mesure, suivi de **[!UICONTROL Suivant]**.

![L’étape Connexion aux données et détails mettant en surbrillance le type de données de mesure et l’option Suivant &#x200B;](../../assets/setup/add-manage-measurement-data/select-measurement-data-type.png){zoomable="yes"}.

#### Sélectionner la connexion de données {#select-data-connection}

Une connexion aux données est la source à partir de laquelle vous récupérez les données de mesure dans Collaboration. Une fois que vous avez établi votre connexion de données initiale et sourcé votre premier jeu de données de mesure, vous pouvez continuer à sourcer des données de mesure supplémentaires en utilisant la même connexion de données.

Pour ajouter une connexion de données, sélectionnez **[!UICONTROL Ajouter une nouvelle connexion de données]**, puis sélectionnez **[!UICONTROL Suivant]**.

![L’étape Connexion de données et détails mettant en surbrillance les options Ajouter une nouvelle connexion de données et Suivant &#x200B;](../../assets/setup/add-manage-measurement-data/select-measurement-data-connection.png){zoomable="yes"}.

#### Sélectionner une source de données {#select-data-source}

Choisissez ensuite la source de votre connexion aux données. Actuellement, Adobe Experience Platform est la seule source de données prise en charge.

Sélectionnez votre source de données, puis sélectionnez **[!UICONTROL Suivant]**.

![L’étape Connexion aux données et détails mettant en surbrillance les options Adobe Experience Platform et Suivant &#x200B;](../../assets/setup/add-manage-measurement-data/select-measurement-data-source.png){zoomable="yes"}.

#### Sélectionner un sandbox {#select-sandbox}

Sélectionnez le sandbox qui inclut les données de mesure que vous souhaitez utiliser pour les rapports de mesure de campagne Collaboration. Sélectionnez le sandbox dans la liste des sandbox disponibles, puis sélectionnez **[!UICONTROL Suivant]**.

![L’étape Connexion aux données et détails mettant en surbrillance le sandbox Prod et l’option Suivant](../../assets/setup/add-manage-measurement-data/select-sandbox.png){zoomable="yes"}.

#### Sélectionner un jeu de données de mesure {#select-measurement-dataset}

Une liste de jeux de données dans le sandbox sélectionné s’affiche. Sélectionnez un jeu de données comme données de mesure, puis sélectionnez **[!UICONTROL Suivant]**. Vous pouvez utiliser l’option Rechercher pour filtrer et trouver le jeu de données préféré.

![L’étape Connexion aux données et détails mettant en surbrillance l’option Rechercher , l’exemple de jeu de données d’événement et l’option Suivant &#x200B;](../../assets/setup/add-manage-measurement-data/select-measurement-dataset.png){zoomable="yes"}.

#### Indiquer le nom et les détails {#provide-name-and-details}

Indiquez ensuite un nom et une description pour votre connexion de données. Ces informations vous aideront à identifier la connexion de données ultérieurement.

![L’étape Connexion aux données et détails avec la possibilité de fournir un nom et une description.](../../assets/setup/add-manage-measurement-data/data-connection-name-details.png){zoomable="yes"}

### Mappage {#mapping}

L’étape suivante consiste à mapper les champs de vos données de mesure aux champs cibles correspondants utilisés dans Collaboration. Vous pouvez également choisir d’enrichir votre jeu de données d’événement avec des attributs du profil client en temps réel en mappant les clés de jointure et en utilisant ces attributs pour ventiler les rapports de mesure.

#### Enrichissement des données d’événement {#enrich-event-data}

Pour enrichir vos données d’événement, sélectionnez l’option Clé de jointure de champ **[!UICONTROL Source]**.

![Écran Mappage avec l’option Clé de jointure de champ Source mise en surbrillance.](../../assets/setup/add-manage-measurement-data/select-source-field-join-key.png){zoomable="yes"}

Dans la boîte de dialogue Clé de jointure de champ **&#x200B;**&#x200B;choisissez le champ source, puis **[!UICONTROL Sélectionner]**.

![Boîte de dialogue de clé de jointure de champ Source mettant en surbrillance le champ Source et l’option Suivant.](../../assets/setup/add-manage-measurement-data/source-field-join-key-dialog.png){zoomable="yes"}

Sélectionnez ensuite l’option **[!UICONTROL Clé de jointure du profil]**. Dans la boîte de dialogue **[!UICONTROL Clé de jointure du profil]**, sélectionnez le champ de profil dans la liste. Vous pouvez utiliser l’option Rechercher pour trouver le champ souhaité. Sélectionnez ensuite **[!UICONTROL Sélectionner]** pour confirmer.

![&#x200B; Boîte de dialogue Clé de jointure du profil mettant en surbrillance la clé de recherche, le champ de profil sélectionné et l’option Suivant &#x200B;](../../assets/setup/add-manage-measurement-data/profile-join-key-dialog.png){zoomable="yes"}.

#### Champs de mappage {#mapping-fields}

Pour commencer à mapper les champs source de vos données de mesure aux champs cibles dans Collaboration, sélectionnez le champ source vide dans l’écran **[!UICONTROL Mappage]**.

![Écran Mappage avec le champ source vide en surbrillance.](../../assets/setup/add-manage-measurement-data/mapping-screen.png){zoomable="yes"}

La boîte de dialogue **[!UICONTROL Sélectionner le champ source]** s’affiche. Elle présente une liste des champs source disponibles regroupés sous des options telles que **[!UICONTROL Espace de noms d’identité]** et **[!UICONTROL Schéma d’événement]**. Vous pouvez utiliser l’option de recherche pour filtrer et trouver le champ source dans la liste.

Choisissez le champ source de votre choix, puis **[!UICONTROL Sélectionner]**.

![&#x200B; Boîte de dialogue Sélectionner le champ source mettant en surbrillance le champ source E-mails et l’option Sélectionner &#x200B;](../../assets/setup/add-manage-measurement-data/select-source-field-dialog.png){zoomable="yes"}.

Utilisez ensuite le menu déroulant pour mapper le champ source sélectionné à un champ cible approprié. Tous les champs cibles disponibles sont les clés [correspondance configurées pour votre compte collaborateur](./onboard-account.md#set-up-match-keys).

![Menu déroulant affichant tous les champs cibles disponibles à mapper au champ source sélectionné.](../../assets/setup/add-manage-measurement-data/select-target-field-dropdown.png){zoomable="yes"}

Vous pouvez ajouter ou supprimer des lignes de mappage, si nécessaire. Si vous devez mapper un champ source non haché à un champ cible haché (par exemple, mapper un e-mail en texte brut à [!UICONTROL e-mail haché]), utilisez l’option **[!UICONTROL Appliquer la transformation]** pour appliquer le hachage requis.

Une fois que vous avez terminé, passez en revue les champs mappés et les clés de jointure si l’enrichissement est activé. Sélectionnez ensuite **[!UICONTROL Suivant]**.

![Écran Mappage affichant les champs mappés, les clés de jointure (lorsque l’enrichissement est activé) et l’option Suivant mise en surbrillance.](../../assets/setup/add-manage-measurement-data/review-mapping.png){zoomable="yes"}

### Gérer le consentement {#manage-consent}

Avant de poursuivre, vous devez reconnaître que l’utilisation des données dans Collaboration est conforme à vos politiques de gouvernance des données de Real-Time CDP. Toutes les données doivent être préfiltrées en fonction des exigences de consentement ou des politiques de consentement personnalisées applicables, de sorte qu’aucun traitement supplémentaire n’est nécessaire.

Pour confirmer l’accusé de réception, sélectionnez **[!UICONTROL Suivant]**.

![L’écran Gérer le consentement nécessite une confirmation avec l’option Suivant mise en surbrillance.](../../assets/setup/add-manage-measurement-data/manage-consent.png){zoomable="yes"}

Si vous [activez l’enrichissement du profil lors de l’étape de mappage](#enrich-event-data), vous pouvez configurer des politiques de consentement à partir d’une liste d’options prédéfinies. Cela inclut :

* **Actions marketing** : utilisez ces actions marketing pour contrôler les données d’audience à importer dans Collaboration à partir d’Experience Platform.
* **Règles de consentement** : sélectionnez les règles de consentement à appliquer aux données provenant de Collaboration.
* **Audience** : utilisez le filtre d’audience pour inclure ou exclure des profils d’audience pour le consentement.

>[!NOTE]
>
>**[!UICONTROL Data Collaboration]** prend en charge les libellés d’utilisation des données C4, C5 et C9, tandis que **[!UICONTROL Data Science]** prend uniquement en charge C9. Consultez la documentation d’Experience Platform pour en savoir plus sur les libellés d’utilisation des données :
>
>* [Présentation des libellés d’utilisation des données](https://experienceleague.adobe.com/fr/docs/experience-platform/data-governance/labels/overview){target="_blank"}
>* [Glossaire](https://experienceleague.adobe.com/fr/docs/experience-platform/data-governance/labels/reference){target="_blank"}

Sélectionnez les paramètres souhaités, puis sélectionnez **[!UICONTROL Suivant]**.

![L’écran Gérer le consentement affiche les options de configuration du consentement lorsque l’enrichissement du profil est activé, avec l’option Suivant en surbrillance.](../../assets/setup/add-manage-measurement-data/manage-consent-configuration-options.png){zoomable="yes"}

Avant de poursuivre, vous devez confirmer et accepter les termes de la boîte de dialogue **[!UICONTROL Politique de gouvernance et mesures d’application]**. Cochez la case, puis **[!UICONTROL OK]**.

![Boîte de dialogue Politique de gouvernance et actions d’application affichant la case à cocher et l’option OK mises en surbrillance.](../../assets/setup/add-manage-measurement-data/governance-policy-enforcement-actions-dialog.png){zoomable="yes"}

#### Filtre d’audience {#audience-filter}

Pour inclure ou exclure certains profils d’audience pour le consentement, utilisez le menu déroulant **[!UICONTROL Filtre d’audience]**. Une fois que vous avez sélectionné ce filtre, l’interface utilisateur se met à jour pour afficher l’option **[!UICONTROL Parcourir les audiences]**. Sélectionnez **[!UICONTROL Parcourir les audiences]**.

![Écran Gérer le consentement affichant l’option Parcourir les audiences une fois le filtre d’audience sélectionné.](../../assets/setup/add-manage-measurement-data/browse-audiences.png){zoomable="yes"}

La boîte de dialogue **[!UICONTROL Sélectionner des audiences]** s’affiche. Choisissez une audience dans la liste, puis **[!UICONTROL Sélectionner]**.

![&#x200B; Boîte de dialogue Sélectionner des audiences mettant en surbrillance l’audience sélectionnée et l’option Sélectionner &#x200B;](../../assets/setup/add-manage-measurement-data/select-audiences-dialog.png){zoomable="yes"}.

L’audience choisie s’affiche maintenant et vous avez la possibilité de la supprimer si nécessaire. Vérifiez vos paramètres de consentement, puis sélectionnez **[!UICONTROL Suivant]**.

![L’écran Gérer le consentement mettant en surbrillance l’audience sélectionnée pour le consentement et l’option Suivant &#x200B;](../../assets/setup/add-manage-measurement-data/audience-for-consent.png){zoomable="yes"}.

### Ajouter un événement de conversion {#add-conversion-event}

Définissez ensuite les événements de conversion dont vous souhaitez mesurer l’impact de vos campagnes, par exemple, sur les visites de site, les inscriptions ou les achats terminés. Vous pouvez spécifier jusqu’à **3** événements de conversion distincts pour la mesure.

Indiquez le nom de l’événement de conversion, puis utilisez le menu déroulant pour sélectionner le type de conversion.

![Écran Ajouter un événement de conversion mettant en surbrillance le menu déroulant du type de conversion développé.](../../assets/setup/add-manage-measurement-data/conversion-type-dropdown.png){zoomable="yes"}

Vous pouvez saisir une valeur pour la conversion ou la laisser vide si vous ne souhaitez pas attribuer de valeur pour le moment.

![Écran Ajouter un événement de conversion mettant en surbrillance l’option Valeur de conversion.](../../assets/setup/add-manage-measurement-data/conversion-value.png){zoomable="yes"}

Ensuite, vous devez spécifier la clé de duplication pour indiquer quelles lignes de votre jeu de données d’événement appartiennent au même événement de conversion sous-jacent (par exemple, le même horodatage pendant un processus d’inscription). Cela évite de compter la même conversion plusieurs fois dans les rapports de mesure. Pour ce faire, sélectionnez **[!UICONTROL Clé de duplication]**. Dans la boîte de dialogue **[!UICONTROL Clé de duplication]**, recherchez et choisissez la clé, puis **[!UICONTROL Sélectionner]**.

![&#x200B; Boîte de dialogue Clé de duplication affichant la clé sélectionnée et l’option Sélectionner &#x200B;](../../assets/setup/add-manage-measurement-data/duplication-key-dialog.png){zoomable="yes"}

Après avoir spécifié la clé de duplication, vous pouvez ajouter jusqu’à **5** conditions pour inclure uniquement les lignes pertinentes du jeu de données d’événement pour la conversion. Choisissez d’appliquer l’ensemble ou l’une de ces conditions.

Sélectionnez **[!UICONTROL Ajouter une condition]**, puis sélectionnez l’option de condition.

![Écran Ajouter un événement de conversion mettant en surbrillance l’option de condition après avoir sélectionné l’option Ajouter une condition.](../../assets/setup/add-manage-measurement-data/add-condition.png){zoomable="yes"}

Dans la boîte de dialogue **[!UICONTROL Sélectionner le champ source]**, recherchez et choisissez un champ source pour la règle de condition, suivi de **[!UICONTROL Sélectionner]**.

![Boîte de dialogue Sélectionner le champ source mettant en surbrillance le champ Type d’événement et l’option Sélectionner](../../assets/setup/add-manage-measurement-data/select-condition-field.png){zoomable="yes"}.

Utilisez le menu déroulant pour sélectionner un opérateur logique, puis saisissez la valeur de la règle de configuration.

![Écran Ajouter un événement de conversion mettant en surbrillance la liste déroulante pour l’opérateur logique et l’option Valeur.](../../assets/setup/add-manage-measurement-data/logic-operator-dropdown.png){zoomable="yes"}

Pour ajouter un autre événement de conversion, sélectionnez **[!UICONTROL Ajouter une conversion]**. Vous pouvez inclure jusqu’à 3 **&#x200B;**&#x200B;d’événements de conversion au total. Une fois l’opération terminée, passez en revue les configurations de conversion et sélectionnez **[!UICONTROL Suivant]**.

![Écran Ajouter un événement de conversion affichant les configurations d’événement de conversion et l’option Suivant mise en surbrillance.](../../assets/setup/add-manage-measurement-data/add-conversion-event.png){zoomable="yes"}

### Réviser {#review}

L&#39;écran **[!UICONTROL Révision]** s&#39;affiche avec un résumé des paramètres des données de mesure. Vérifiez que toutes les informations sont correctes. Si vous devez modifier une section, utilisez l’option **[!UICONTROL Modifier]**.

Enfin, sélectionnez **[!UICONTROL Terminé]** pour terminer l’ajout des données de mesure.

![Écran Vérifier affichant un résumé des paramètres des données de mesure et l’option Terminé mise en surbrillance.](../../assets/setup/add-manage-measurement-data/review-measurement-data.png){zoomable="yes"}

Une boîte de dialogue de confirmation confirme la création réussie de vos données de mesure. Vous pouvez voir les nouveaux événements de conversion configurés à partir de vos données de mesure dans l’espace de travail **[!UICONTROL Mes données de mesure]**.

![Espace de travail de mes données de mesure affichant la liste des événements de conversion configurés à partir de vos données de mesure.](../../assets/setup/add-manage-measurement-data/conversion-event-list.png){zoomable="yes"}

En mode Grille ou Tableau, sélectionnez un élément de ligne ou l’option **[!UICONTROL Afficher la conversion]** dans une carte d’événement pour afficher un aperçu d’un événement de conversion spécifique. Il affiche le statut de l’événement, la source et le nom de la connexion de données, ainsi que des panneaux détaillés pour :

* **[!UICONTROL Détails de la conversion]** : affiche des informations clés sur la conversion, y compris son type, la clé de duplication utilisée pour identifier les événements uniques et la valeur de conversion affectée (si spécifiée).
* **[!UICONTROL Conditions]** : affiche les règles de condition appliquées à cet événement de conversion.

![Écran Aperçu affichant les détails d’un événement de conversion.](../../assets/setup/add-manage-measurement-data/conversion-event-overview.png){zoomable="yes"}

## Modifier les données de mesure {#edit-measurement-data}

Après avoir sourcé vos données de mesure, vous pouvez modifier les détails et les règles de condition d’un événement de conversion à tout moment.

Dans l’onglet **[!UICONTROL Mes données de mesure]**, sélectionnez l’option représentant des points de suspension (![icône Plus](/help/assets/icons/more.png)) dans la vignette d’événement de conversion appropriée. Sélectionnez ensuite **[!UICONTROL Afficher la conversion]** dans le menu déroulant pour ouvrir la page détaillée de cet événement de conversion.

![Onglet Mes données de mesure avec le menu représentant des points de suspension ouvert et l’option Afficher la conversion en surbrillance.](/help/assets/setup/add-manage-measurement-data/conversion-event-list.png){zoomable="yes"}

### Modifier le nom et la description {#edit-name-and-description}

Pour mettre à jour le nom et la description de l’événement, sélectionnez l’icône Modifier (![icône Modifier](/help/assets/icons/edit.png)) en haut à droite de la page.

![Page de l’événement de visite du site avec l’icône Modifier en haut à droite mise en surbrillance.](/help/assets/setup/add-manage-measurement-data/edit-name-description.png){zoomable="yes"}

Dans la boîte de dialogue **[!UICONTROL Modifier le nom et la description]**, mettez à jour les champs avec les valeurs souhaitées, puis sélectionnez **[!UICONTROL Enregistrer]** pour appliquer vos modifications.

![Boîte de dialogue Modifier le nom et la description avec l’option Enregistrer mise en surbrillance.](/help/assets/setup/add-manage-measurement-data/edit-name-description-dialog.png){zoomable="yes"}

Une boîte de dialogue de confirmation s’affiche pour confirmer que les détails ont bien été mis à jour.

### Modifier les détails de la conversion {#edit-conversion-details}

Vous pouvez mettre à jour les détails de conversion suivants de l’événement :

| Champ | Description |
|-------------------|-------------|
| Type de conversion | La catégorie de l’événement de conversion, telle qu’une visite du site, un achat ou une inscription. |
| Clé de duplication | Identifiant des lignes du jeu de données d’événement appartenant au même événement de conversion (par exemple, même date et heure). Empêche les doublons. |
| Valeur de conversion | Valeur associée à chaque conversion. |

{style="table-layout:auto"}

Pour commencer la modification, sélectionnez **[!UICONTROL Modifier]** dans le panneau **[!UICONTROL Détails de la conversion]**.

![Page d’événement de visite du site mettant en surbrillance l’option Modifier dans le panneau des détails de conversion.](/help/assets/setup/add-manage-measurement-data/edit-conversion-details.png){zoomable="yes"}

Dans la boîte de dialogue **[!UICONTROL Modifier les détails de conversion]**, utilisez le menu déroulant pour mettre à jour le type de conversion. Vous pouvez saisir une valeur pour la conversion ou la laisser vide si vous ne souhaitez pas lui attribuer de valeur. Pour modifier la clé de duplication, sélectionnez l’option Clé existante .

![Boîte de dialogue Modifier les détails de la conversion avec l’option Exemple d’ID de personne mise en surbrillance.](/help/assets/setup/add-manage-measurement-data/edit-conversion-details-dialog.png){zoomable="yes"}

La boîte de dialogue **[!UICONTROL Clé de duplication]** affiche une liste des champs disponibles regroupés sous des options telles que **[!UICONTROL Espace de noms d’identité]** et **[!UICONTROL Schéma d’événement]**. Recherchez et choisissez la touche souhaitée, puis **[!UICONTROL Sélectionner]**.

![&#x200B; Boîte de dialogue Clé de duplication affichant la clé choisie et l’option Sélectionner &#x200B;](../../assets/setup/add-manage-measurement-data/edit-duplication-key-dialog.png){zoomable="yes"}

Une fois l’opération terminée, passez en revue les mises à jour et sélectionnez **[!UICONTROL Enregistrer]** pour appliquer les modifications.

![Boîte de dialogue Modifier les détails de la conversion avec l’option Enregistrer mise en surbrillance.](/help/assets/setup/add-manage-measurement-data/edit-conversion-details-save.png){zoomable="yes"}

Une boîte de dialogue de confirmation s’affiche pour confirmer que les détails ont bien été mis à jour.

### Modifier les conditions {#edit-conditions}

Les règles de condition spécifient les lignes de données de votre jeu de données d’événement incluses en tant que conversions. Mettez à jour ces règles selon les besoins pour vous assurer que votre mesure reflète uniquement les données les plus pertinentes pour votre analyse.

Pour modifier des conditions, sélectionnez **[!UICONTROL Modifier]** dans le panneau **[!UICONTROL Conditions]**.

![Page d’événement de visite du site mettant en surbrillance l’option Modifier dans le panneau Conditions.](/help/assets/setup/add-manage-measurement-data/edit-conditions.png){zoomable="yes"}

Dans la boîte de dialogue **[!UICONTROL Modifier les règles de conversion]**, vous pouvez afficher les détails actuels de toutes les conditions. Sélectionnez une option de condition existante pour mettre à jour ses détails, y compris le champ source, la règle logique et la valeur.

![Boîte de dialogue Modifier les règles de conversion mettant en surbrillance les options permettant de modifier le champ source, la règle logique et la valeur d’une condition existante.](/help/assets/setup/add-manage-measurement-data/edit-exisiting-condition.png){zoomable="yes"}

Pour inclure des règles de conversion supplémentaires, sélectionnez **[!UICONTROL Ajouter une condition]**. Sélectionnez ensuite l’option Nouvelle condition vide .

![Boîte de dialogue Modifier les règles de conversion affichant la nouvelle option de condition vide après avoir sélectionné l’option Ajouter une condition.](/help/assets/setup/add-manage-measurement-data/edit-conversion-rules-add-condition.png){zoomable="yes"}

Dans la boîte de dialogue **[!UICONTROL Sélectionner le champ source]**, vous pouvez voir les champs disponibles regroupés sous des options telles que **[!UICONTROL Espace de noms d’identité]** et **[!UICONTROL Schéma d’événement]**. Sélectionnez le champ approprié à utiliser pour votre condition, puis choisissez **[!UICONTROL Sélectionner]**. Vous pouvez utiliser l’option **[!UICONTROL Rechercher]** pour trouver rapidement le champ de votre choix.

![&#x200B; La boîte de dialogue Sélectionner le champ source affiche le champ sélectionné et l’option Sélectionner &#x200B;](../../assets/setup/add-manage-measurement-data/edit-condition-source-key.png){zoomable="yes"}.

Ensuite, utilisez le menu déroulant pour sélectionner un opérateur logique dans la liste disponible et saisissez une valeur pour la condition.

![Boîte de dialogue Modifier les règles de conversion mettant en surbrillance le menu déroulant logique.](../../assets/setup/add-manage-measurement-data/edit-condition-logic-dropdown.png){zoomable="yes"}

Utilisez **[!UICONTROL Inclure toutes les conditions]** si toutes les conditions spécifiées sont requises pour chaque conversion, ou utilisez **[!UICONTROL Inclure n’importe laquelle des conditions]** pour autoriser les conversions qui correspondent à au moins une condition. Une fois la mise à jour terminée, vérifiez et sélectionnez **[!UICONTROL Enregistrer]** pour appliquer les modifications.

![Boîte de dialogue Modifier les règles de conversion avec l’option Enregistrer mise en surbrillance.](/help/assets/setup/add-manage-measurement-data/edit-conversion-rules-save.png){zoomable="yes"}

Une boîte de dialogue de confirmation s’affiche pour confirmer que les détails ont bien été mis à jour.

## Suppression des données de mesure {#delete-measurement-data}

La suppression des données de mesure supprime définitivement de votre projet l’événement de conversion associé et tous les détails de mesure liés. Les rapports de mesure qui reposent sur cet événement perdront les mesures de conversion correspondantes et ne pourront plus être mis à jour. Cette action ne peut pas être annulée.

Pour supprimer un événement de conversion existant, accédez à l’onglet **[!UICONTROL Mes données de mesure]** dans l’espace de travail **[!UICONTROL Configuration]**. En mode Grille, sélectionnez **[!UICONTROL Supprimer]** dans la vignette d’événement appropriée. En mode Tableau, sélectionnez l’icône de suppression (![icône de suppression](/help/assets/common/delete.svg)) à côté du nom de l’événement.

![Onglet Mes données de mesure mettant en surbrillance l’option Supprimer dans une ligne d’événement de conversion.](/help/assets/setup/add-manage-measurement-data/delete-measurement-data.png){zoomable="yes"}

La boîte de dialogue **[!UICONTROL Supprimer la mesure]** s’affiche et vous invite à confirmer la suppression de l’événement. Sélectionnez **[!UICONTROL Supprimer]**.

![Boîte de dialogue Supprimer la mesure avec l’option Supprimer mise en surbrillance.](/help/assets/setup/add-manage-measurement-data/delete-measurement-dialog.png){zoomable="yes"}

Une boîte de dialogue de confirmation s’affiche pour confirmer que l’événement de conversion a bien été supprimé.

## Étapes suivantes {#next-steps}

Vous avez terminé l’approvisionnement de vos données de mesure dans Collaboration. En tant qu’annonceur, vous pouvez désormais créer des rapports d’attribution pour découvrir comment vos campagnes génèrent des conversions et mesurent l’impact global. Si vous êtes un éditeur, demandez à votre collaborateur de générer un rapport d’attribution pour vos campagnes. Pour obtenir des instructions détaillées, consultez le guide [Créer un rapport d’attribution](../collaborate/measure.md#create-attribution-report).
