---
title: Gérer des connexions
description: Découvrez comment gérer vos connexions dans Real-Time CDP Collaboration.
audience: admin, publisher, advertiser
badgelimitedavailability: label="Disponibilité limitée" type="Informative" url="https://helpx.adobe.com/legal/product-descriptions/real-time-customer-data-platform-collaboration.html newtab=true"
exl-id: 50120839-4a20-4ec1-8887-9342bd17c52d
source-git-commit: 46d2596bd0ccdc5da32067493968945c61f8acc4
workflow-type: tm+mt
source-wordcount: '1079'
ht-degree: 1%

---

# Gérer des connexions {#manage-connections}

{{limited-availability-release-note}}

L’espace de travail **[!UICONTROL Mes connexions]** fournit un emplacement centralisé pour gérer vos connexions. Vous pouvez afficher les connexions existantes dans la section **[!UICONTROL Connexions existantes]** et afficher les connexions nécessitant une action dans la section **[!UICONTROL Action requise]**.

## Afficher la connexion {#view-connection}

Pour afficher vos connexions existantes, accédez à l’espace de travail **[!UICONTROL Connect]**. En tant qu’éditeur, votre connexion existante s’affiche. En tant qu’annonceur, vous devez ensuite accéder à **[!UICONTROL Mes connexions]**.

![L’option Afficher la connexion est mise en surbrillance pour une connexion dans l’espace de travail Mes connexions.](/help/assets/connect/manage-connections/view-connection.png){zoomable="yes"}

L’espace de travail de présentation de la connexion s’affiche et affiche des détails sur la connexion et ses projets actifs. Sélectionnez **[!UICONTROL Paramètres de connexion]** pour afficher les paramètres de connexion.

![L’option Paramètres de connexion mise en surbrillance dans l’espace de travail de présentation de la connexion.](/help/assets/connect/manage-connections/connection-overview.png){zoomable="yes"}

L’espace de travail des paramètres de connexion s’affiche, affichant les détails de connexion entre vous et votre collaborateur. Ici, vous pouvez afficher tous les paramètres sélectionnés pendant le processus de connexion, le statut actuel de la connexion, le propriétaire de la connexion et les informations de contact de votre collaborateur. Pour plus d’informations sur les paramètres de connexion spécifiques, consultez le guide [paramètres de connexion](/help/guide/connect/establishing-connections.md#connection-settings).

![Espace de travail des paramètres de connexion affichant les détails de la connexion.](/help/assets/connect/manage-connections/connection-settings.png){zoomable="yes"}

## Supprimer la connexion {#delete-connection}

Vous pouvez supprimer toutes les connexions avec des collaborateurs avec lesquelles vous ne souhaitez plus travailler. Pour supprimer une connexion, accédez à la connexion que vous souhaitez supprimer, puis sélectionnez l’icône de suppression ![icône de suppression](/help/assets/common/delete.svg) dans l’espace de travail de connexion.

![Icône de suppression mise en surbrillance dans l’espace de travail de connexion.](/help/assets/connect/establish-connection/delete-option.png){zoomable="yes"}

Une boîte de dialogue de confirmation s’affiche, vous demandant de confirmer la suppression de la connexion. Sélectionnez **[!UICONTROL Supprimer]** pour confirmer la suppression.

![Boîte de dialogue de confirmation permettant de supprimer une connexion.](/help/assets/connect/establish-connection/delete-confirmation-dialog.png){zoomable="yes"}

>[!WARNING]
>
>Une fois la connexion supprimée, tous les projets existants dans la collaboration seront définitivement supprimés et irrécupérables. La demande de connexion reste en attente dans la section **[!UICONTROL Action requise]** de **[!UICONTROL Mes connexions]**, mais la connexion et ses configurations ne sont plus actives. Vous devrez rétablir la connexion si vous souhaitez vous reconnecter au collaborateur.

## Modifier la connexion {#edit-connection}

En tant que propriétaire d’une connexion de collaboration, vous pouvez modifier les paramètres de connexion avec votre collaborateur une fois la connexion établie. Vous pouvez :

* Ajouter des cas d’utilisation
* Ajoutez des clés de correspondance. La suppression de la clé de correspondance sera prise en charge à l’avenir.
* Mettre à jour les autorisations d’activation des audiences
* Mettre à jour les paramètres de partage des crédits

>[!IMPORTANT]
>
>Une fois qu’un cas d’utilisation ou une clé de correspondance est ajouté à une connexion, il ne peut pas être supprimé.

>[!TIP]
>
>Le **propriétaire** est le collaborateur qui établit la connexion en envoyant l’invitation au **destinataire**. Pour plus d’informations, voir la documentation [établissement de connexions avec des collaborateurs](./establishing-connections.md).

Pour modifier les paramètres de connexion, accédez à l’espace de travail Paramètres de connexion . Sélectionnez l’icône des trois points (![ Icône des trois points.](/help/assets/icons/more.png)) pour afficher les actions disponibles, puis sélectionnez **[!UICONTROL Modifier]**.

![Espace de travail des paramètres de connexion avec l’option Modifier mise en surbrillance.](/help/assets/connect/manage-connections/edit-connection.png){zoomable="yes"}

Une boîte de dialogue s’affiche, vous invitant à modifier et à envoyer les modifications des paramètres pour révision par le collaborateur. Sélectionnez **[!UICONTROL Modifier]**.

![Boîte de dialogue Modifier les paramètres de connexion avec l’option Modifier mise en surbrillance.](/help/assets/connect/manage-connections/edit-connection-settings-dialog.png){zoomable="yes"}

### Modifier l’activation de l’audience {#edit-audience-activation}

Les paramètres d’activation de l’audience déterminent quel collaborateur dans la connexion peut activer les audiences vers les destinations. Pour modifier ces paramètres, sélectionnez **[!UICONTROL Modifier]** dans la section **[!UICONTROL Activation de l’audience]**.

![Écran de modification des paramètres de connexion affichant la section Activation de l’audience et l’option Modifier ](/help/assets/connect/manage-connections/edit-audience-activation.png){zoomable="yes"}.

Dans la boîte de dialogue **[!UICONTROL Activation de l’audience]**, utilisez le menu déroulant pour mettre à jour les autorisations d’activation de l’audience. Vous pouvez choisir un seul collaborateur ou permettre aux deux collaborateurs d’activer les audiences.

![La boîte de dialogue Activation de l’audience mettant en surbrillance le menu déroulant développée pour mettre à jour les autorisations d’activation de l’audience.](/help/assets/connect/manage-connections/audience-activation-dropdown-menu.png){zoomable="yes"}

Lorsque vous avez terminé, sélectionnez **[!UICONTROL Enregistrer]**.

![ Boîte de dialogue d’activation de l’audience affichant les nouvelles autorisations d’activation de l’audience et l’option Enregistrer ](/help/assets/connect/manage-connections/audience-activation-dialog.png){zoomable="yes"}.

### Ajouter des cas d’utilisation {#add-use-cases}

Dans Collaboration, les cas d’utilisation tels que Découvrir, Activer et Mesurer déterminent les sections et fonctionnalités du projet que vous pouvez utiliser avec votre collaborateur. Vous pouvez ajouter des cas d’utilisation supplémentaires à une connexion existante pour des projets futurs. Pour plus d’informations, voir [Cas d’utilisation de collaboration](../overview/use-cases.md).

Pour ajouter de nouveaux cas d’utilisation, sélectionnez **[!UICONTROL Modifier]** dans la section **[!UICONTROL Cas d’utilisation]**.

![Écran Modifier les paramètres de connexion mettant en surbrillance la section Cas d’utilisation et l’option Modifier](/help/assets/connect/manage-connections/edit-use-cases.png){zoomable="yes"}.

Dans la boîte de dialogue **[!UICONTROL Cas d’utilisation]**, activez les nouveaux cas d’utilisation que vous souhaitez ajouter, puis **[!UICONTROL Enregistrer]**.

![Boîte de dialogue Cas d’utilisation présentant l’option Enregistrer mise en surbrillance.](/help/assets/connect/manage-connections/use-cases-dialog.png){zoomable="yes"}

>[!NOTE]
>
>Lorsque vous [ajoutez de nouveaux cas d’utilisation](#add-use-cases) tels que « Activation de l’audience » ou « Mesure », l’écran de modification des paramètres de connexion se met à jour pour inclure les sections **[!UICONTROL Activation de l’audience]** et **[!UICONTROL Partage du crédit]**. Vous devez configurer les paramètres appropriés pour ces nouveaux cas d’utilisation. Pour plus d’informations, consultez les guides [activation de l’audience](../connect/establishing-connections.md#audience-activation) et [partage du crédit](../connect/establishing-connections.md#credit-split).
>
>![L’écran Modifier les paramètres de connexion affiche les sections Activation de l’audience et Partage du crédit après l’ajout de nouveaux cas d’utilisation.](/help/assets/connect/manage-connections/setup-audience-activation-credit-split.png){zoomable="yes"}

### Ajouter des clés de correspondance {#add-match-keys}

Seules les clés de correspondance configurées dans votre compte et également sélectionnées par votre collaborateur sont disponibles pour la connexion. Une fois que vous [ajoutez de nouvelles clés de correspondance à votre compte](../setup/onboard-account.md#edit-match-keys) et que votre collaborateur sélectionne également les mêmes clés, vous pouvez les activer dans vos connexions existantes.

Dans l’écran Modifier les paramètres de connexion, sélectionnez **[!UICONTROL Modifier]** dans la section **[!UICONTROL Touches de correspondance]**.

![Écran Modifier les paramètres de connexion mettant en surbrillance la section Touches de correspondance et l’option Modifier.](/help/assets/connect/manage-connections/edit-connection-match-keys.png){zoomable="yes"}

Une boîte de dialogue **[!UICONTROL Clés de correspondance]** s’affiche, affichant les clés de correspondance existantes configurées pour la connexion. Sélectionnez les clés de correspondance à ajouter, puis **[!UICONTROL Enregistrer]**.

![La boîte de dialogue Touches de correspondance affiche les nouvelles touches de correspondance sélectionnées et l’option Enregistrer.](/help/assets/connect/manage-connections/connection-match-keys-dialog.png){zoomable="yes"}

### Modifier le fractionnement de crédit {#edit-credit-split}

Les paramètres de répartition du crédit indiquent quel collaborateur est responsable des coûts associés à chaque cas d’utilisation dans la connexion. Pour mettre à jour ces paramètres, sélectionnez **[!UICONTROL Modifier]** dans la section **[!UICONTROL Partage du crédit]**.

![Écran Modifier les paramètres de connexion mettant en surbrillance la section Partage du crédit et l’option Modifier](/help/assets/connect/manage-connections/edit-credit-split.png){zoomable="yes"}.

Dans la boîte de dialogue **[!UICONTROL Répartition du crédit]**, sélectionnez les paramètres préférés pour [!UICONTROL Activation-Correspondance] et [!UICONTROL Mesure]. Sélectionnez ensuite **[!UICONTROL Enregistrer]** pour confirmer.

![Boîte de dialogue Fractionnement de crédit affichant les paramètres de fractionnement de crédit et l’option Enregistrer.](/help/assets/connect/manage-connections/credit-split-dialog.png){zoomable="yes"}

### Vérifier et envoyer les modifications {#review-and-submit-changes}

Une fois la modification des paramètres de connexion terminée, vérifiez et sélectionnez **[!UICONTROL Envoyer les modifications]**. Les mises à jour des paramètres de connexion seront envoyées à votre collaborateur pour révision.

![L’écran Modifier les paramètres de connexion affiche les mises à jour et l’option Envoyer les modifications.](/help/assets/connect/manage-connections/review-and-submit-changes.png){zoomable="yes"}

#### Enregistrer les modifications des paramètres de connexion en tant que brouillon

Vous pouvez enregistrer les modifications des paramètres de connexion en tant que brouillon et revenir en arrière pour terminer la mise à jour des paramètres de connexion à tout moment.

Pour enregistrer les modifications en tant que brouillon, sélectionnez **[!UICONTROL Annuler]** en regard de **[!UICONTROL Envoyer les modifications]**. Ensuite, dans la boîte de dialogue **[!UICONTROL Modifications non envoyées]**, sélectionnez **[!UICONTROL Continuer ultérieurement]** pour confirmer.

![Écran Modifier les paramètres de connexion.](/help/assets/connect/manage-connections/unsubmitted-changes-dialog.png){zoomable="yes"}

Vos modifications sont maintenant enregistrées en tant que brouillon. Dans l’espace de travail Paramètres de connexion , une notification s’affiche pour indiquer que des modifications n’ont pas été envoyées. Pour effectuer d’autres mises à jour, sélectionnez **[!UICONTROL Continuer la modification]**.

![Notification dans l’espace de travail des paramètres de connexion indiquant que des modifications non envoyées sont en attente de révision et d’envoi.](/help/assets/connect/manage-connections/continue-editing-connection.png){zoomable="yes"}
