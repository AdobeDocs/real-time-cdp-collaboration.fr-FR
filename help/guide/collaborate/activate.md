---
title: Activer les audiences
description: Découvrez comment activer des audiences dans Adobe Real-Time CDP Collaboration.
audience: admin, publisher
badgelimitedavailability: label="Disponibilité limitée" type="Informative" url="https://helpx.adobe.com/legal/product-descriptions/real-time-customer-data-platform-collaboration.html newtab=true"
exl-id: fd82fcbf-ab39-48e0-9438-0a9046693431
source-git-commit: a7215d453021be578a32ce1af4d659845c3b8493
workflow-type: tm+mt
source-wordcount: '953'
ht-degree: 2%

---

# Activer les audiences

{{limited-availability-release-note}}

>[!IMPORTANT]
>
>L’espace de travail **[!UICONTROL Activer]** n’est disponible que si le cas d’utilisation **Activation de l’audience** a été activé [pendant le processus de connexion](../connect/establishing-connections.md#connection-settings). Pour plus d’informations sur les cas d’utilisation, consultez le guide [gestion des projets](./manage-projects.md#project-use-cases).

L’activation des audiences vous permet d’activer des audiences à utiliser dans des campagnes. L’activation peut être effectuée par l’un des collaborateurs en fonction des paramètres d’activation de l’audience [configurés dans la connexion](/help/guide/connect/establishing-connections.md#configure-connection-settings). Après avoir [découvert les meilleures audiences pour votre campagne](./discover.md), activez les audiences pour les rendre disponibles. Lorsque vous activez une audience, elle est envoyée à la destination préconfigurée de votre collaborateur, telle que Adobe Experience Platform, où elle peut être utilisée dans les campagnes. Pour plus d’informations sur la configuration des destinations, consultez le guide [présentation des destinations](../destinations/overview.md).

## Activer de nouvelles audiences {#activate-new-audiences}

Pour commencer à activer les audiences, accédez à l’onglet **[!UICONTROL Activer]** dans l’espace de travail de votre projet.

>[!IMPORTANT]
>
>**Avant** vous pouvez activer une audience, votre collaborateur **doit** configurer une destination. Lorsque vous activez une audience, elle est automatiquement envoyée à la destination configurée de votre collaborateur. Si aucune destination n’est configurée, vous ne pouvez pas activer d’audiences.
>
>![Activer l’espace de travail lorsque aucune destination n’est configurée pour le collaborateur.](/help/assets/collaborate/activate/no-destination-configured.png)

Sélectionnez l’icône d’ajout (![ Icône Ajouter .](/help/assets/icons/plus.png)) ou l’option **[!UICONTROL Activer l’audience]** si aucune audience précédente n’a été envoyée pour activation.

![Activer l’espace de travail dans un projet sans audience ajoutée.](/help/assets/collaborate/activate/activate-new-audiences.png)

Le workflow d’activation des audiences s’ouvre et vous pouvez sélectionner l’audience à envoyer à votre collaborateur ou votre collaboratrice. Utilisez la liste déroulante pour sélectionner une audience ou recherchez une audience spécifique. Pour afficher plus d’informations sur les audiences avant d’effectuer votre sélection, sélectionnez **[!UICONTROL Parcourir les audiences]**

![Workflow d’activation de l’audience avec les options de liste déroulante et de Parcourir les audiences mises en surbrillance.](/help/assets/collaborate/activate/audience-activation.png)

Dans le **[!UICONTROL Parcourir les audiences]**, vous pouvez voir le **[!UICONTROL Nombre d’identités]**, le **[!UICONTROL Chevauchement des identités]** et le **[!UICONTROL Chevauchement %]** pour chaque audience.

![Boîte de dialogue Parcourir les audiences affichant les audiences disponibles.](/help/assets/collaborate/activate/browse-audiences.png)

Sélectionnez l’audience à activer dans les campagnes, puis sélectionnez **[!UICONTROL Enregistrer]**. L’audience est maintenant affichée et vous pouvez voir le **[!UICONTROL nombre d’identités]**, le **[!UICONTROL chevauchement d’identités]** et le **[!UICONTROL chevauchement %]** pour l’audience sélectionnée.

![Workflow d’activation de l’audience avec l’audience sélectionnée affichée.](/help/assets/collaborate/activate/audience-selected.png)

### Modifier les clés correspondantes {#edit-match-keys}

Vous pouvez ensuite modifier les clés de correspondance de l’audience en sélectionnant **[!UICONTROL Modifier les clés de correspondance]** dans l’audience sélectionnée. Ces options sont héritées de vos sélections de clés de correspondance lors de la configuration initiale de la connexion entre les collaborateurs. Vous pouvez supprimer les clés de correspondance sélectionnées si elles ne s’appliquent pas à une campagne spécifique, mais vous ne pouvez pas ajouter de nouvelles clés de correspondance.

![Workflow d’activation de l’audience avec l’option Modifier les clés de correspondance mise en surbrillance.](/help/assets/collaborate/activate/edit-match-keys.png)

La boîte de dialogue **[!UICONTROL Modifier les clés de correspondance]** s’ouvre et vous pouvez activer/désactiver les clés de correspondance que vous ne souhaitez pas utiliser. Sélectionnez **[!UICONTROL Enregistrer]** pour enregistrer vos modifications.

>[!NOTE]
>
>Au moins une clé de correspondance doit être sélectionnée. Dans la version actuelle, la seule clé de correspondance disponible est **[!UICONTROL e-mail haché]**. Vous ne pouvez donc pas supprimer cette clé de correspondance.

![Boîte de dialogue Modifier les clés de correspondance dans le workflow d’activation de l’audience.](/help/assets/collaborate/activate/edit-match-keys-selection.png)

### Définir la fréquence d’actualisation de l’audience {#set-audience-refresh-frequency}

Enfin, définissez la fréquence et la période souhaitées pour l’actualisation de l’audience. Dans la version actuelle, la seule option de fréquence prise en charge est **[!UICONTROL Une fois]**. La fréquence **[!UICONTROL Une fois]** signifie que les audiences sont activées une seule fois et ne sont pas actualisées. L’option **[!UICONTROL Date]** est automatiquement renseignée avec la date actuelle.

![Workflow d’activation de l’audience avec la section Fréquence mise en surbrillance.](/help/assets/collaborate/activate/audience-frequency.png)

Une fois vos sélections effectuées, sélectionnez **[!UICONTROL Activer]** pour terminer le workflow.

## Activer le tableau de bord {#activate-dashboard}

Dans l’onglet **[!UICONTROL Activer]**, vous pouvez afficher toutes les audiences envoyées à votre collaborateur, ainsi que toutes les audiences que votre collaborateur a activées vers votre destination.

![Tableau de bord d’activation présentant les sections Audiences envoyées et Audiences activées.](/help/assets/collaborate/activate/activate-dashboard.png)

## Afficher les audiences envoyées {#view-sent-audiences}

Dans la section collaborateur **[!UICONTROL Envoyer des audiences à]**, toutes les audiences que vous avez envoyées seront répertoriées. Actuellement, les audiences sont automatiquement envoyées à la destination configurée de votre collaborateur ou de votre collaboratrice après leur envoi. Dans la vue de votre collaborateur, ces audiences sont affichées dans la section **[!UICONTROL Audiences activées]**.

Dans chaque audience envoyée, vous pouvez voir les mesures suivantes :

| Mesure | Description |
|---------|----------|
| **[!UICONTROL Nom]** | Nom de l’audience. |
| **[!UICONTROL Statut]** | Statut de l’audience envoyée. |
| **[!UICONTROL Nombre d’identités]** | Nombre d’identités dans l’audience. |
| **[!UICONTROL Identités qui se chevauchent]** | Nombre d’identités qui se chevauchent entre cette audience et la population totale des profils de l’inventaire du collaborateur. |
| **[!UICONTROL Créé]** | Date d’envoi initiale de l’audience. |
| **[!UICONTROL Dernier envoi]** | Date à laquelle l’audience a été envoyée pour la dernière fois à votre collaborateur. |
| **[!UICONTROL Clés de correspondance]** | Indique la clé de correspondance utilisée pour l’audience. |

## Afficher les audiences activées {#view-activated-audiences}

Dans la section **[!UICONTROL Audiences activées]**, vous pouvez voir toutes les audiences qui ont été activées vers votre destination.

Dans chaque audience activée, vous pouvez voir les mesures suivantes :

| Mesure | Description |
|---------|----------|
| **[!UICONTROL Nom]** | Nom de l’audience. |
| **[!UICONTROL Statut]** | Statut de l’audience activée. |
| **[!UICONTROL Nombre d’identités]** | Le nombre d’identités activées, en fonction des identités qui se chevauchent lorsque votre collaborateur a envoyé l’audience. |
| **[!UICONTROL Créé]** | Date d’activation de l’audience. |
| **[!UICONTROL Dernière actualisation]** | Date de la dernière actualisation de l’audience, en fonction du planning d’actualisation choisi lors de l’activation. |
| **[!UICONTROL Destination]** | Destination vers laquelle l’audience a été activée. |
| **[!UICONTROL Clés de correspondance]** | Indique la clé de correspondance utilisée pour l’audience. |

## Supprimer les audiences envoyées {#delete-sent-audiences}

Vous pouvez supprimer les audiences envoyées que vous ne souhaitez plus activer. Lorsque vous supprimez une audience envoyée, elle est supprimée de la section **[!UICONTROL Audiences envoyées à]** et elle ne sera plus activée vers la destination de votre collaborateur ou de votre collaboratrice.

Pour supprimer une audience envoyée, sélectionnez l’icône **[!UICONTROL Supprimer]** (![Icône Supprimer).](/help/assets/icons/delete.png)) à côté de l’audience dans la section **[!UICONTROL A envoyé des audiences à]**.

![Option Supprimer dans la section Audiences envoyées à ](/help/assets/collaborate/activate/delete-sent-audiences.png).

Une boîte de dialogue de confirmation s’ouvre, vous demandant de confirmer la suppression. Sélectionnez **[!UICONTROL Supprimer]** pour confirmer.

![Boîte de dialogue de confirmation de suppression.](/help/assets/collaborate/activate/delete-sent-audiences-confirmation.png)

## Étapes suivantes {#next-steps}

Après avoir activé les audiences et exécuté des campagnes, travaillez avec l’équipe d’activation et d’ingénierie d’Adobe pour charger les données de mesure et afficher les [rapports de mesure](/help/guide/collaborate/measure.md) correspondants.
