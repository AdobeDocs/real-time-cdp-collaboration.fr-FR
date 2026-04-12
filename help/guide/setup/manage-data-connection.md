---
title: Gérer les connexions de données
description: Découvrez comment gérer les connexions de données, notamment les clés de correspondance, la planification, les cas d’utilisation et le filtrage d’audience dans Real-Time CDP Collaboration
audience: administrator, data engineer
badgelimitedavailability: label="Disponibilité limitée" type="Informative" url="https://helpx.adobe.com/legal/product-descriptions/real-time-customer-data-platform-collaboration.html newtab=true"
exl-id: d142d3ed-f56a-4150-a885-571728a73ac8
source-git-commit: 4bfa57ba36336dd835551fb846f1d567d6830bf9
workflow-type: tm+mt
source-wordcount: '1168'
ht-degree: 5%

---

# Gérer les connexions de données

{{limited-availability-release-note}}

## Vue d’ensemble

Utilisez les connexions de données dans Real-Time CDP Collaboration pour approvisionner les audiences à partir de différentes plateformes. Découvrez comment gérer les clés de correspondance et planifier l’actualisation des données pour vos connexions de données existantes. De plus, vous pourrez filtrer les audiences en fonction de différents attributs pour obtenir des informations plus granulaires.

## Afficher les connexions de données

Pour afficher les connexions de données existantes, accédez à **[!UICONTROL Configuration]** puis sélectionnez l’onglet **[!UICONTROL Mes connexions de données]**. Toutes vos connexions de données actuelles sont affichées, affichant un bref aperçu pour chaque connexion. Pour obtenir une vue complète des informations d’une connexion de données, y compris ses clés de correspondance, les détails de planification et les audiences, sélectionnez **[!UICONTROL Afficher la connexion de données]** sur la connexion correspondante.

![Configurer l’espace de travail avec la vue de l’onglet Mes connexions de données affichée et mise en surbrillance.](/help/assets/setup/manage-data-connection/my-data-connections.png){zoomable="yes"}

### Clés correspondantes {#match-keys}

>[!CONTEXTUALHELP]
>id="rtcdp_collaboration_manage_dataconnections_matchkeys"
>title="Clés correspondantes"
>abstract="Les clés de correspondance déterminent la manière dont les données provenant de différentes sources seront mises en correspondance. Les clés correspondantes affichées ci-dessous sont les champs cibles auxquels vous avez mappé vos champs sources."

Les clés de correspondance sont les champs cibles auxquels vous [avez mappé vos champs sources](./onboard-audiences.md#map-fields). Pour en savoir plus sur le fonctionnement des clés de correspondance, consultez le guide [match keys](./onboard-account.md#set-up-match-keys).

![Un espace de travail des connexions de données avec la section Clés de correspondance mise en surbrillance.](/help/assets/setup/manage-data-connection/view-data-connection-match-keys.png){zoomable="yes"}

### Planification {#scheduling}

>[!CONTEXTUALHELP]
>id="rtcdp_collaboration_manage_dataconnections_scheduling"
>title="Planification"
>abstract="Affichez les détails de la planification de votre connexion de données et modifiez les configurations si nécessaire."

Afficher et gérer les paramètres de planification de vos connexions de données. La planification détermine la fréquence d’actualisation de l’audience.

Une fois une connexion de données créée, vous pouvez mettre à jour sa fréquence d’actualisation, sa date de début et sa date de fin directement à partir de la section **[!UICONTROL Planification]** de l’espace de travail de connexion de données.

>[!NOTE]
>
>Lorsque vous sourcez des audiences à partir de Adobe Experience Platform, les audiences sont disponibles dans les 24 heures suivant l’établissement de la connexion aux données. Après le sourcing initial, les données d’audience sont actualisées selon la fréquence définie.

Pour plus d’informations sur la planification, consultez la [section de planification](/help/guide/setup/onboard-audiences.md#schedule) dans le guide de configuration des audiences.

![Espace de travail d’une connexion de données avec la section Planification mise en surbrillance.](/help/assets/setup/manage-data-connection/view-data-connection-scheduling.png){zoomable="yes"}

## Modifier la connexion de données {#edit-data-connection}

Lisez les sections suivantes pour savoir comment mettre à jour les clés de correspondance et les paramètres de planification d’une connexion de données existante.

### Modifier les clés correspondantes {#edit-match-keys}

>[!CONTEXTUALHELP]
>id="rtcdp_collaboration_edit_measurement_data_connection_enrichment"
>title="Enrichissement"
>abstract="Désactiver l’enrichissement n’est pas pris en charge. Vous pouvez modifier les clés de jointure d’enrichissement à la place."
>additional-url="https://www.adobe.com/go/rtcdp-collaboration-manage-dataconnections" text="Enrichissement"

>[!IMPORTANT]
>
>Avant de modifier les clés de correspondance pour une connexion de données, notez ce qui suit :
>
>* Seules les clés de correspondance configurées pour votre compte peuvent être utilisées pour les connexions aux données.
>* Actuellement, vous pouvez ajouter des clés de correspondance supplémentaires à une connexion de données, mais une fois qu’une clé de correspondance est activée, elle ne peut pas être supprimée.

Sélectionnez **[!UICONTROL Modifier]** dans la section **[!UICONTROL Clés de correspondance]**.

![Section Correspondance des clés avec l’option Modifier mise en surbrillance.](/help/assets/setup/manage-data-connection/edit-match-keys.png){zoomable="yes"}

Une boîte de dialogue de confirmation s’affiche, expliquant que toute modification de la connexion aux données s’appliquera à toutes les audiences associées. Sélectionnez **[!UICONTROL OK]** pour confirmer. Vous pouvez choisir d’ignorer cette confirmation à l’avenir.

![Boîte de dialogue de confirmation indiquant que toute modification apportée à la connexion de données s’appliquera à toutes les audiences associées.](/help/assets/setup/manage-data-connection/confirm-data-connection-changes.png){zoomable="yes"}

Dans la boîte de dialogue **[!UICONTROL Clés de correspondance]**, vous pouvez afficher les mappages existants entre les champs sources et leurs champs cibles correspondants (clés de correspondance). Vous pouvez modifier une clé de correspondance en mettant à jour le champ source mappé ou ajouter des lignes de champ de mappage supplémentaires pour renseigner de nouvelles clés de correspondance.

![Boîte de dialogue Correspondance des clés présentant les mappages existants entre les champs sources et les champs cibles correspondants.](/help/assets/setup/manage-data-connection/match-keys-dialog.png){zoomable="yes"}

#### Ajouter des clés de correspondance {#add-match-keys}

Sélectionnez **[!UICONTROL Ajouter un champ]** pour ajouter une nouvelle ligne de champ.

![Après avoir sélectionné Ajouter un champ, la boîte de dialogue Correspondance des clés affiche un nouveau champ de mappage vide prêt pour la saisie.](/help/assets/setup/manage-data-connection/add-new-field.png){zoomable="yes"}

Sélectionnez ensuite le champ source vide. La boîte de dialogue **[!UICONTROL Sélectionner le champ source]** s’affiche avec les options **[!UICONTROL Espaces de noms d’identité]** et **[!UICONTROL Attributs de profil]**. Vous pouvez filtrer la liste et trouver le champ source de votre choix à l’aide de l’option de recherche.

Choisissez le champ source de votre choix, puis **[!UICONTROL Sélectionner]**.

![La boîte de dialogue Sélectionner le champ source avec l’option GAID sélectionnée.](/help/assets/setup/manage-data-connection/select-source-field.png){zoomable="yes"}

Dans la boîte de dialogue **[!UICONTROL Touches de correspondance]**, utilisez le menu déroulant pour mapper le nouveau champ source à un champ cible. Tous les champs cibles disponibles correspondent aux clés configurées pour votre compte collaborateur. Si vous ne voyez pas le champ cible dont vous avez besoin, [modifiez les clés de correspondance de votre compte](./onboard-account.md#edit-match-keys) pour l’ajouter.

Utilisez l’option **[!UICONTROL Appliquer la transformation]** si vous souhaitez générer un champ non haché en champ cible haché, par exemple, lors du mappage d’un champ source d’e-mail en texte brut au champ cible **[!UICONTROL E-mail haché]**.

![Menu déroulant affichant tous les champs cibles disponibles à mapper au nouveau champ source.](/help/assets/setup/manage-data-connection/select-target-field.png){zoomable="yes"}

Une fois les champs de mappage terminés, passez en revue vos mises à jour et sélectionnez **[!UICONTROL Confirmer]** pour appliquer les modifications.

![Boîte de dialogue Correspondance des clés présentant le mappage de champs mis à jour avec l’option Confirmer mise en surbrillance.](/help/assets/setup/manage-data-connection/review-and-confirm.png){zoomable="yes"}

Une boîte de dialogue de confirmation confirme que les clés de correspondance ont bien été mises à jour.

### Modifier la planification {#edit-scheduling}

Une fois une connexion de données créée, vous pouvez mettre à jour sa fréquence d’actualisation, sa date de début et sa date de fin directement à partir de la section **[!UICONTROL Planification]** de l’espace de travail de connexion de données.

Vous pouvez modifier la fréquence d’une connexion de données existante pour mieux contrôler la fréquence d’actualisation des audiences. Pour modifier le planning, sélectionnez **[!UICONTROL Modifier]** depuis la connexion de données dans la carte de planification.

![Section Planification avec l’option Modifier mise en surbrillance.](/help/assets/setup/manage-data-connection/edit-scheduling.png){zoomable="yes"}

Une boîte de dialogue de confirmation s’affiche, expliquant que toute modification de la connexion aux données s’appliquera à toutes les audiences associées. Sélectionnez **[!UICONTROL OK]** pour confirmer. Vous pouvez choisir d’ignorer cette confirmation à l’avenir.

![Boîte de dialogue de confirmation indiquant que toute modification apportée à la connexion de données s’appliquera à toutes les audiences associées.](/help/assets/setup/manage-data-connection/confirm-data-connection-changes.png){zoomable="yes"}

Dans la boîte de dialogue **[!UICONTROL Planification]**, sélectionnez le menu déroulant pour mettre à jour la **[!UICONTROL Fréquence]**. Définissez la fréquence d’actualisation pour qu’elle s’exécute tous les jours ou tous les deux à six jours.

![La boîte de dialogue Planification avec la liste déroulante Fréquence développée pour afficher les options de fréquence d’actualisation de l’audience.](../../assets/setup/manage-data-connection/edit-frequency.png){zoomable="yes"}

Sélectionnez ensuite **[!UICONTROL Période]** si vous souhaitez mettre à jour la période pendant laquelle les audiences sont renseignées et actualisées.

![La boîte de dialogue Planification affichant le menu déroulant Période s’est développée pour modifier les dates de début et de fin du remplissage et de l’actualisation de l’audience.](../../assets/setup/manage-data-connection/edit-date-range.png){zoomable="yes"}

Lorsque vous avez terminé, passez en revue les mises à jour et sélectionnez **[!UICONTROL Enregistrer]** pour appliquer vos modifications.

![Boîte de dialogue Planification mettant en surbrillance les options Mises à jour et Enregistrer.](../../assets/setup/manage-data-connection/scheduling-dialog.png){zoomable="yes"}

## Supprimer la connexion de données

La suppression d’une connexion aux données supprimera toutes les audiences sous-jacentes, les paramètres associés et l’utilisation dans Collaboration. Cette action ne peut pas être annulée.

Pour supprimer une connexion de données existante, sélectionnez l’icône de suppression (![icône Supprimer](/help/assets/common/delete.svg)) dans l’espace de travail d’une connexion de données individuelle.

![Un espace de travail des connexions de données avec l’option de suppression mise en surbrillance.](/help/assets/setup/manage-data-connection/delete-data-connection.png){zoomable="yes"}

Une boîte de dialogue de confirmation s’affiche. Sélectionnez **[!UICONTROL Supprimer]** pour terminer la suppression de la connexion de données.

![Boîte de dialogue Supprimer la connexion de données avec l’option Supprimer mise en surbrillance.](/help/assets/setup/manage-data-connection/delete-data-connection-confirm.png){zoomable="yes"}

## Gérer des audiences {#manage-audiences}

Une liste des audiences associées à la connexion de données s’affiche au bas de l’espace de travail. La liste affiche un bref aperçu de chaque audience, y compris son statut, sa source et son accès à la connexion. Pour modifier les catégories d’une audience, l’accès à la connexion ou la visibilité des métadonnées, sélectionnez le nom de l’audience. Pour obtenir un guide complet sur la gestion d’une audience, reportez-vous au guide [Afficher des audiences individuelles](./onboard-audiences.md#view-individual-audiences) .

![Espace de travail des connexions de données avec les audiences en surbrillance.](/help/assets/setup/manage-data-connection/view-data-connection-manage-audiences.png){zoomable="yes"}

## Étapes suivantes

Après avoir géré vos connexions de données, vous pouvez [découvrir des chevauchements](/help/guide/collaborate/discover.md) entre vos audiences et les audiences que votre collaborateur a rendues détectables.
