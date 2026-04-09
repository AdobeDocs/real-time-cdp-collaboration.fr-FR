---
title: Gestion des connexions aux données de mesure
description: Découvrez comment gérer les connexions de données de mesure, y compris les détails et les clés de correspondance dans Real-Time CDP Collaboration
audience: administrator, data engineer
badgelimitedavailability: label="Disponibilité limitée" type="Informative" url="https://helpx.adobe.com/legal/product-descriptions/real-time-customer-data-platform-collaboration.html newtab=true"
source-git-commit: 494277f421606eda62b74c254f1fdd29b22e3473
workflow-type: tm+mt
source-wordcount: '1338'
ht-degree: 3%

---

# Gestion des connexions aux données de mesure

{{limited-availability-release-note}}

## Vue d’ensemble

Utilisez les connexions de données de mesure dans Real-Time CDP Collaboration pour générer vos données de conversion à partir de différentes plateformes. Découvrez comment gérer les détails et faire correspondre les clés de vos connexions de données existantes.

## Afficher les connexions aux données de mesure {#view-measurement-data-connections}

Vous pouvez afficher les détails de toute connexion de données de mesure existante, y compris la source des données de conversion, les clés de correspondance utilisées et tous les événements de conversion liés à la connexion.

Dans l’espace de travail **[!UICONTROL Configuration]**, accédez à l’onglet **[!UICONTROL Mes connexions de données]**. Toutes les connexions de données de mesure en cours sont affichées sous la section **[!UICONTROL Mesure]** en vue tabulaire ou grille. Sélectionnez **[!UICONTROL Afficher la connexion de données]** sur la carte de connexion correspondante ou sélectionnez le nom de la connexion de données en mode Tableau pour ouvrir son espace de travail et afficher tous les détails.

![Onglet Mes connexions de données mettant en surbrillance une carte de connexion aux données de mesure et l’option Afficher la connexion aux données](/help/assets/setup/manage-measurement-data-connection/view-measurement-data-connection.png){zoomable="yes"}.

### Détails de la connexion aux données de mesure {#measurement-data-connection-details}

Dans cette section, vous pouvez voir les détails suivants de la connexion de données :

| Champ | Description |
|-------------------|-------------|
| État | État actuel de la connexion de données de mesure, par exemple **[!UICONTROL Active]**. |
| Source | Plateforme ou système fournissant les données de mesure pour cette connexion. |
| Sandbox | Nom du sandbox dans lequel la connexion aux données de mesure est configurée. |
| Jeu de données | Nom du jeu de données utilisé pour sourcer les données de mesure dans la connexion. |
| Dernière mise à jour | Date et heure de la mise à jour la plus récente de la connexion aux données de mesure. |
| Dernière mise à jour effectuée par | Dernier utilisateur à avoir modifié la connexion aux données de mesure. |
| Created | Date et heure de création de la connexion aux données de mesure. |
| Créé par | Utilisateur qui a créé la connexion de données de mesure à l’origine. |

{style="table-layout:auto"}

### Clés correspondantes {#match-keys}

Les clés de correspondance sont les champs cibles auxquels vous avez mappé vos champs sources lorsque vous [&#x200B; les données de mesure](./onboard-measurement-data.md). Pour en savoir plus sur le fonctionnement des clés de correspondance, consultez le guide [match keys](./onboard-account.md#set-up-match-keys).

![Espace de travail de connexion aux données de mesure avec la section Touches de correspondance mise en surbrillance.](/help/assets/setup/manage-measurement-data-connection/view-match-keys.png){zoomable="yes"}

### Événements de conversion {#conversion-events}

Une liste des événements de conversion associés à la connexion de données s’affiche au bas de l’espace de travail. La liste affiche un bref aperçu de chaque événement, y compris son statut, son type de conversion et sa source. Vous pouvez sélectionner le nom de l’événement pour afficher et modifier ses configurations, ou supprimer l’événement de conversion à l’aide de l’option de suppression (![icône de suppression](/help/assets/common/delete.svg)). Pour obtenir un guide complet sur la gestion d’un événement de conversion, reportez-vous au guide [ajouter et gérer des données de mesure](./onboard-measurement-data.md).

![Espace de travail de connexion aux données de mesure avec la section des événements de conversion mise en surbrillance.](/help/assets/setup/manage-measurement-data-connection/view-conversion-events.png){zoomable="yes"}

## Modifier la connexion aux données de mesure {#edit-measurement-data-connection}

Vous pouvez mettre à jour à tout moment les détails et les clés de correspondance d’une connexion de données de mesure existante afin de vous assurer que vos rapports et analyses restent exacts. Pour commencer, accédez à l’onglet **[!UICONTROL Mes connexions de données]** et sélectionnez la connexion de données de mesure à modifier. L’espace de travail de connexion aux données s’ouvre, où vous pouvez suivre les étapes ci-dessous pour apporter les modifications nécessaires.

### Modifier le nom et la description {#edit-name-and-description}

Pour mettre à jour le nom et la description de la connexion de données, sélectionnez l’icône Modifier (![icône Modifier](/help/assets/icons/edit.png)) à côté du nom de la connexion actuelle.

![Espace de travail de connexion aux données de mesure mettant en surbrillance l’icône Modifier à côté du nom de la connexion aux données.](/help/assets/setup/manage-measurement-data-connection/edit-name-description.png){zoomable="yes"}

Dans la boîte de dialogue **[!UICONTROL Modifier la connexion aux données]**, mettez à jour les champs avec les valeurs souhaitées, puis sélectionnez **[!UICONTROL Enregistrer]** pour appliquer vos modifications.

![Boîte de dialogue Modifier la connexion de données avec l’option Enregistrer mise en surbrillance.](/help/assets/setup/manage-measurement-data-connection/edit-name-description-dialog.png){zoomable="yes"}

Une boîte de dialogue de confirmation s’affiche pour confirmer que les détails ont bien été mis à jour.

### Modifier les clés correspondantes {#edit-match-keys}

>[!IMPORTANT]
>
>Avant de modifier les clés de correspondance pour une connexion de données, notez ce qui suit :
>
>* Seules les clés de correspondance configurées pour votre compte peuvent être utilisées pour les connexions aux données.
>* Actuellement, vous pouvez ajouter des clés de correspondance supplémentaires à une connexion de données, mais une fois qu’une clé de correspondance est activée, elle ne peut pas être supprimée.

Dans l’espace de travail des connexions de données, sélectionnez **[!UICONTROL Modifier]** dans le panneau **[!UICONTROL Correspondre aux clés]**.

![Section Correspondance des clés avec l’option Modifier mise en surbrillance.](/help/assets/setup/manage-measurement-data-connection/edit-match-keys.png){zoomable="yes"}

Une boîte de dialogue de confirmation s’affiche, expliquant que toute modification apportée à la connexion de données s’appliquera à toutes les conversions associées. Sélectionnez **[!UICONTROL OK]** pour confirmer. Vous pouvez choisir d’ignorer cette confirmation à l’avenir.

![Boîte de dialogue de confirmation indiquant que toute modification apportée à la connexion de données s’appliquera à toutes les conversions associées.](/help/assets/setup/manage-measurement-data-connection/confirm-data-connection-changes.png){zoomable="yes"}

Dans la boîte de dialogue **[!UICONTROL Clés de correspondance]**, vous pouvez consulter les paramètres d’enrichissement et voir les mappages actuels entre vos champs sources et les champs cibles (clés de correspondance).

![Boîte de dialogue Correspondance des clés présentant les paramètres d’enrichissement et les mappages existants entre les champs sources et les champs cibles correspondants.](/help/assets/setup/manage-measurement-data-connection/edit-match-keys-dialog.png){zoomable="yes"}

#### Enrichissement {#enrichment}

Si l’enrichissement n’a pas été activé lorsque vous [avez sourcé vos données de mesure](./onboard-measurement-data.md), vous avez la possibilité d’enrichir votre jeu de données d’événement avec des attributs du profil client en temps réel. Notez qu’une fois l’enrichissement activé pour les données de mesure, il ne peut pas être désactivé. Vous pouvez toujours mettre à jour les clés de jointure d’enrichissement si nécessaire.

Lorsque vous activez l’enrichissement dans la boîte de dialogue **[!UICONTROL Clés de correspondance]**, l’interface utilisateur se développe pour afficher d’autres options de configuration sous la section **[!UICONTROL Enrichir vos données d’événement avec les identifiants de profils]**.

Sélectionnez l’option Clé de jointure de champ **[!UICONTROL Source]** .

![La boîte de dialogue Correspondance des clés avec l’option Clé de jointure de champ Source mise en surbrillance.](../../assets/setup/manage-measurement-data-connection/enrich-event-data.png){zoomable="yes"}

Dans la boîte de dialogue Clé de jointure de champ **&#x200B;**&#x200B;choisissez le champ source, puis **[!UICONTROL Sélectionner]**.

![&#x200B; Boîte de dialogue Clé de jointure de champ Source mettant en surbrillance le champ source sélectionné et l’option Suivant &#x200B;](../../assets/setup/manage-measurement-data-connection/source-field-join-key-dialog.png){zoomable="yes"}.

Sélectionnez ensuite l’option **[!UICONTROL Clé de jointure du profil]**. Dans la boîte de dialogue **[!UICONTROL Clé de jointure du profil]**, sélectionnez le champ de profil dans la liste. Vous pouvez utiliser l’option Rechercher pour trouver le champ souhaité. Sélectionnez ensuite **[!UICONTROL Sélectionner]** pour confirmer.

![Boîte de dialogue Clé de jointure de profil mettant en surbrillance le champ de profil sélectionné et l’option Sélectionner.](../../assets/setup/manage-measurement-data-connection/profile-join-key-dialog.png){zoomable="yes"}

#### Modifier le mapping {#edit-mapping}

Pour modifier une clé de correspondance existante, mettez à jour son champ source et son champ cible associés dans la boîte de dialogue **[!UICONTROL Clés de correspondance]**. Si vous souhaitez inclure une nouvelle clé de correspondance, sélectionnez **[!UICONTROL Ajouter un champ]**. Cela crée une ligne vide où vous pouvez définir un mappage supplémentaire entre les champs source et cible.

![Après avoir sélectionné Ajouter un champ, la boîte de dialogue Correspondance des clés affiche une nouvelle ligne de mappage vide prête pour la saisie.](/help/assets/setup/manage-measurement-data-connection/add-new-field.png){zoomable="yes"}

Sélectionnez ensuite le champ source vide. La boîte de dialogue **[!UICONTROL Sélectionner le champ source]** s’affiche avec une liste des champs source disponibles regroupés sous des options telles que **[!UICONTROL Espaces de noms d’identité]** et **[!UICONTROL Attributs de profil]**. Vous pouvez filtrer la liste et trouver le champ source de votre choix à l’aide de l’option de recherche.

Choisissez le champ source de votre choix, puis **[!UICONTROL Sélectionner]**.

![&#x200B; La boîte de dialogue Sélectionner le champ source mettant en surbrillance l’option Rechercher , le champ Source téléphonique et l’option Sélectionner &#x200B;](/help/assets/setup/manage-measurement-data-connection/select-source-field.png){zoomable="yes"}.

Dans la boîte de dialogue **[!UICONTROL Touches de correspondance]**, utilisez le menu déroulant pour mapper le nouveau champ source à un champ cible. Tous les champs cibles disponibles correspondent aux clés configurées pour votre compte collaborateur. Si vous ne voyez pas le champ cible dont vous avez besoin, [modifiez les clés de correspondance de votre compte](./onboard-account.md#edit-match-keys) pour l’ajouter.

Utilisez l’option **[!UICONTROL Appliquer la transformation]** si vous souhaitez générer un champ non haché en un champ cible haché, par exemple, lors du mappage d’un champ source de téléphone en texte brut au champ cible **[!UICONTROL Téléphone haché]**.

![Menu déroulant affichant tous les champs cibles disponibles à mapper au nouveau champ source.](/help/assets/setup/manage-measurement-data-connection/target-field-dropdown.png){zoomable="yes"}

Une fois les champs de mappage terminés, passez en revue vos mises à jour et sélectionnez **[!UICONTROL Confirmer]** pour appliquer les modifications.

![Boîte de dialogue Correspondance des clés présentant le mappage de champs mis à jour avec l’option Confirmer mise en surbrillance.](/help/assets/setup/manage-measurement-data-connection/confirm-edit-match-keys.png){zoomable="yes"}

Une boîte de dialogue de confirmation confirme que les clés de correspondance ont bien été mises à jour.

## Supprimer la connexion de données

La suppression d’une connexion aux données supprime toutes les conversions sous-jacentes, les paramètres associés et l’utilisation dans Collaboration. Cette action ne peut pas être annulée.

Pour supprimer une connexion de données existante, sélectionnez l’icône de suppression (![icône Supprimer](/help/assets/common/delete.svg)) dans l’espace de travail d’une connexion de données individuelle.

![Un espace de travail des connexions de données avec l’option de suppression mise en surbrillance.](/help/assets/setup/manage-measurement-data-connection/delete-measurement-data-connection.png){zoomable="yes"}

Une boîte de dialogue de confirmation s’affiche. Sélectionnez **[!UICONTROL Supprimer]** pour terminer la suppression de la connexion de données.

![Boîte de dialogue Supprimer la connexion de données avec l’option Supprimer mise en surbrillance.](/help/assets/setup/manage-measurement-data-connection/delete-measurement-data-connection-confirm.png){zoomable="yes"}

Une boîte de dialogue de confirmation confirme la suppression réussie de la connexion de données.

## Étapes suivantes {#next-steps}

Après avoir géré les connexions aux données de mesure, vous pouvez :

* Ajoutez d’autres événements de conversion liés à votre connexion de données, si nécessaire. Pour obtenir des instructions détaillées, consultez la documentation [ajouter et gérer des données de mesure](./onboard-measurement-data.md).
* Générez des rapports de mesure pour obtenir des informations sur les performances et l’impact de votre campagne. Pour plus d’informations sur les types de rapports disponibles et sur la manière de les créer, consultez le guide [mesurer les performances](/help/guide/collaborate/measure.md).
