---
title: Activer les audiences
description: Découvrez comment envoyer des audiences à des collaborateurs et activer manuellement les audiences reçues vers des destinations dans Adobe Real-Time CDP Collaboration.
audience: admin, publisher, advertiser
exl-id: fd82fcbf-ab39-48e0-9438-0a9046693431
TQID: https://experienceleague.adobe.com/bfPHtcW8Mf6RhIlg5fKcJmPSEKDyAODjbNRJ5D3SMkQ
product_v2:
  - id: fdddec33-c9cb-4459-b8b6-2664395a6f10
feature_v2:
  - id: ba929a52-9339-4154-9487-317dc875a3c7
topic_v2:
  - id: c2be0313-b3ae-45e0-b454-d20bf54b23f2
  - id: e1e0219c-f879-479f-8427-888ed2a6e9c2
source-git-commit: 5d12a5004a6854392c130fd6b93a841fb22cf6ab
workflow-type: tm+mt
source-wordcount: 1565
ht-degree: 2%

---

# Activer les audiences

Utilisez l’onglet **[!UICONTROL Activer]** dans un projet pour envoyer des audiences à votre collaborateur, passer en revue les audiences reçues de votre collaborateur et activer les audiences reçues pour diffusion vers une destination configurée. Pour configurer et gérer les destinations à partir de l’espace de travail de niveau supérieur **[!UICONTROL Activation]**, consultez la [présentation des destinations](../destinations/overview.md).

>[!IMPORTANT]
>
>L’onglet **[!UICONTROL Activer]** n’est disponible que si le cas d’utilisation **Activation de l’audience** a été activé [pendant le processus de connexion](../connect/establishing-connections.md#connection-settings). Pour plus d’informations sur les cas d’utilisation, voir [Gestion de projets](./manage-projects.md#project-use-cases).

Utilisez l’onglet [Découvrir](./discover.md) pour identifier les audiences qui correspondent le mieux à votre campagne, puis envoyez-les à votre collaborateur ou collaboratrice. Le collaborateur récepteur sélectionne une destination configurée et planifie l’activation de l’audience reçue.

L’envoi et l’activation sont des actions distinctes. L’envoi de donne à votre collaborateur l’accès à une audience. Le collaborateur récepteur sélectionne ensuite une destination et active manuellement l’audience reçue.

Les sections et actions disponibles varient selon que votre organisation envoie ou reçoit des audiences dans le projet. L&#39;onglet **[!UICONTROL Activer]** contient les sections suivantes :

| Section | Description |
|---|---|
| **[!UICONTROL Audiences envoyées à [collaborateur]]** | Audiences que vous avez envoyées à votre collaborateur. |
| **[!UICONTROL Audiences reçues]** | Audiences que votre collaborateur vous a envoyées et qui sont disponibles pour activation. |
| **[!UICONTROL Audiences activées]** | Audiences reçues que vous avez activées vers une destination. |

![Onglet Activer au niveau du projet avec des comptes de synthèse en haut des sections Audiences envoyées et étendues, Audiences reçues et Audiences activées . Chaque section affiche le nombre de statuts et un tableau des détails de l’audience.](/help/assets/collaborate/activate/activate-dashboard.png)

## Conditions préalables {#prerequisites}

Avant d’envoyer ou d’activer des audiences, assurez-vous des points suivants :

- Les audiences sont sourcées et disponibles pour l’envoi. Pour plus d&#39;informations, voir [Source et gérer les audiences](../setup/onboard-audiences.md).
- Au moins une destination est configurée si vous devez activer les audiences reçues. Pour plus d’informations, voir la [présentation des destinations](../destinations/overview.md).

## Envoyer les audiences {#send-audiences}

Envoyez une audience pour permettre à votre collaborateur d’y accéder. Une fois l’audience envoyée, elle apparaît dans votre section **[!UICONTROL Envoi d’audiences à [collaborateur]]** et dans la section **[!UICONTROL Audiences reçues]** de votre collaborateur.

Accédez à **[!UICONTROL Collaborer]**, ouvrez un projet, puis sélectionnez l’onglet **[!UICONTROL Activer]**.

Dans la section **[!UICONTROL Audiences envoyées à [collaborateur]]**, sélectionnez l’icône d’ajout (![Ajouter une icône.](/help/assets/icons/plus.png)). Si aucune audience n’a été envoyée, sélectionnez **[!UICONTROL Envoyer l’audience]** dans l’affichage vide à la place.

![Onglet Activer au niveau du projet lorsqu’aucune audience n’a été envoyée. Le message d’affichage vide explique que vous n’avez pas envoyé d’audience et affiche un bouton Envoyer une audience &#x200B;](/help/assets/collaborate/activate/activate-new-audiences.png).

Le workflow **[!UICONTROL Envoyer des audiences]** s’ouvre. Utilisez le sélecteur d’audiences pour trouver une audience ou sélectionnez **[!UICONTROL Parcourir les audiences]** pour comparer les audiences disponibles.

![Workflow Envoyer des audiences avec un sélecteur d’audience et un bouton Parcourir les audiences. Le workflow permet à l’expéditeur de choisir une audience avant de configurer les clés de correspondance et les paramètres d’accès.](/help/assets/collaborate/activate/audience-activation.png)

Dans la boîte de dialogue **[!UICONTROL Parcourir les audiences]**, passez en revue les **[!UICONTROL Nombre d’identités]**, **[!UICONTROL Chevauchement des identités]** et **[!UICONTROL Chevauchement de %]** pour chaque audience.

![La boîte de dialogue Parcourir les audiences répertoriant les audiences disponibles avec leur nombre d’identités, leur nombre d’identités qui se chevauchent et leur pourcentage de chevauchement.](/help/assets/collaborate/activate/browse-audiences.png)

>[!IMPORTANT]
>
>Si une audience utilise plusieurs clés de correspondance, chaque clé de correspondance sélectionnée doit respecter le seuil de chevauchement requis. Utilisez l’onglet [Découvrir](./discover.md) pour vérifier que l’audience répond aux exigences de chevauchement avant de l’envoyer.

Sélectionnez l’audience à envoyer, puis sélectionnez **[!UICONTROL Enregistrer]**.

L’audience sélectionnée apparaît dans le workflow avec son identité et ses informations de chevauchement.

![Le workflow Envoyer des audiences avec une audience sélectionnée affichant son nombre d’identités, le nombre d’identités qui se chevauchent, le pourcentage de chevauchement, les clés de correspondance et l’option Modifier les clés de correspondance.](/help/assets/collaborate/activate/audience-selected.png)

### Modifier les clés correspondantes {#edit-match-keys}

Utilisez les clés de correspondance configurées pour la connexion du collaborateur ou supprimez les clés de correspondance qui ne s’appliquent pas à l’audience.

Sélectionnez **[!UICONTROL Modifier les clés de correspondance]** dans l’audience sélectionnée.

![Audience sélectionnée dans le workflow Envoyer les audiences avec l’option Modifier les clés de correspondance mise en surbrillance.](/help/assets/collaborate/activate/edit-match-keys.png)

La boîte de dialogue **[!UICONTROL Modifier les clés de correspondance]** s’affiche. Désactivez toutes les clés de correspondance que vous ne souhaitez pas utiliser, puis sélectionnez **[!UICONTROL Enregistrer]**.

>[!NOTE]
>
>Au moins une clé de correspondance doit rester sélectionnée.

![La boîte de dialogue Modifier les clés de correspondance avec des commandes de basculement pour les clés de correspondance disponibles via la connexion du collaborateur et un bouton Enregistrer.](/help/assets/collaborate/activate/edit-match-keys-selection.png)

### Configuration de l’accès aux audiences {#configure-audience-access}

Configurez la manière dont l’audience est envoyée et la durée pendant laquelle votre collaborateur peut y accéder.

Utilisez le contrôle **[!UICONTROL Durée d&#39;accès]** pour sélectionner l&#39;une des options suivantes :

- **[!UICONTROL Envoyer maintenant (une seule fois)]** : envoyez l’audience une fois. Le collaborateur récepteur peut l’activer une fois.
- **[!UICONTROL Planifier l’envoi d’audience récurrente]** : actualisez l’audience pendant une période d’accès spécifiée. Utilisez le contrôle **[!UICONTROL Période]** pour sélectionner les dates de début et de fin.

![L’étape Durée d’accès du workflow Envoyer les audiences avec des options pour envoyer l’audience une seule fois ou planifier l’envoi d’une audience récurrente. L&#39;option récurrente affiche des contrôles de date pour définir la période d&#39;accès.](/help/assets/collaborate/activate/activation-frequency.png)

Une fois l’audience et les paramètres d’accès définis, sélectionnez **[!UICONTROL Envoyer]**.

L’audience s’affiche dans votre section **[!UICONTROL Audiences envoyées à [collaborateur]]**. Votre collaborateur peut le consulter dans sa section **[!UICONTROL Audiences reçues]**.

## Afficher les audiences envoyées {#view-sent-audiences}

Utilisez la section **[!UICONTROL Audiences envoyées à [collaborateur]]** pour passer en revue les audiences que vous avez envoyées et surveiller leur statut d’accès actuel.

Chaque audience envoyée affiche les informations suivantes :

| Colonne | Description |
|---|---|
| **[!UICONTROL Nom de l’audience]** | Nom de l’audience envoyée. |
| **[!UICONTROL Statut]** | Statut d’accès actuel de l’audience. |
| **[!UICONTROL Nombre d’identités]** | Nombre d’identités dans l’audience. |
| **[!UICONTROL Identités qui se chevauchent]** | Nombre d’identités qui se chevauchent avec l’inventaire de votre collaborateur. |
| **[!UICONTROL Créé]** | Date et heure du premier envoi de l’audience. |
| **[!UICONTROL Dernier envoi]** | Date et heure auxquelles les données d’audience ont été envoyées le plus récemment à votre collaborateur. |
| **[!UICONTROL Durée d&#39;accès]** | Paramètre d’accès configuré lors de l’envoi de l’audience. |
| **[!UICONTROL Clés de correspondance]** | Clés de correspondance utilisées lors de l’envoi de l’audience. |

### Supprimer une audience envoyée {#delete-sent-audience}

Supprimez une audience envoyée pour la supprimer de la liste des audiences envoyées et révoquer l’accès de votre collaborateur ou collaboratrice.

Sélectionnez l’icône de suppression (![icône de suppression.](/help/assets/icons/delete.png)). en regard de l’audience dans la section **[!UICONTROL Envoi d’audiences à [collaborateur]]**.

![Section Audiences envoyées avec l’icône de suppression affichée en regard d’une ligne d’audience.](/help/assets/collaborate/activate/delete-sent-audiences.png)

Une boîte de dialogue de confirmation s’affiche. Sélectionnez **[!UICONTROL Supprimer]** pour confirmer.

![Boîte de dialogue de confirmation de suppression de l’audience envoyée expliquant que l’audience sera supprimée et que le collaborateur n’y aura plus accès, avec les boutons Annuler et Supprimer.](/help/assets/collaborate/activate/delete-sent-audiences-confirmation.png)

L’audience est supprimée de la section et votre collaborateur n’y a plus accès.

## Afficher les audiences reçues {#received-audiences}

Utilisez la section **[!UICONTROL Audiences reçues]** pour passer en revue les audiences que votre collaborateur vous a envoyées. Une audience reçue doit être activée manuellement avant que ses données ne soient envoyées à une destination.

Chaque audience reçue affiche les informations suivantes :

| Colonne | Description |
|---|---|
| **[!UICONTROL Nom de l’audience]** | Nom de l’audience reçue. |
| **[!UICONTROL Statut]** | Statut d’accès actuel de l’audience. |
| **[!UICONTROL Nombre d’identités]** | Nombre d’identités dans l’audience. |
| **[!UICONTROL Identités qui se chevauchent]** | Nombre d’identités qui se chevauchent avec votre inventaire. |
| **[!UICONTROL Dernière exécution du flux de données]** | Date et heure de la dernière exécution du flux de données pour l’audience. |
| **[!UICONTROL Durée d&#39;accès]** | Paramètre d’accès configuré par le collaborateur qui a envoyé l’audience. |
| **[!UICONTROL Clés de correspondance]** | Clés de correspondance utilisées pour l’audience. |

![La section Audiences reçues avec les nombres de profils des audiences actifs et expirés. Chaque ligne d’audience affiche son nom, son statut, des informations d’identité, la dernière exécution du flux de données, la durée d’accès, les clés de correspondance et une icône d’ajout utilisée pour commencer l’activation.](/help/assets/collaborate/activate/received-audiences-section.png)

### Activer une audience reçue {#activate-received-audience}

Activez une audience reçue pour envoyer ses données à l’une de vos destinations configurées.

Dans la section **[!UICONTROL Audiences reçues]**, sélectionnez l’icône d’ajout (![Ajouter une icône.](/help/assets/icons/plus.png)) à côté de l’audience à activer.

La boîte de dialogue **[!UICONTROL Activer l’audience]** s’affiche.

Utilisez **[!UICONTROL Destination]** pour sélectionner la destination qui reçoit les données d’audience. Si la liste de destinations est vide, configurez une destination avant de continuer. Pour obtenir des instructions, consultez la [présentation des destinations](../destinations/overview.md).

Utilisez **[!UICONTROL Date]** pour sélectionner la date d’exécution de l’activation, puis sélectionnez **[!UICONTROL Activer]**.

![La boîte de dialogue Activer l’audience s’est ouverte à partir d’une audience reçue. La boîte de dialogue contient une liste déroulante Destination permettant de sélectionner une destination configurée, un champ Date avec un contrôle Calendrier, ainsi que des boutons Annuler et Activer &#x200B;](/help/assets/collaborate/activate/activate-received-audience.png).

La boîte de dialogue se ferme et l’activation s’affiche dans la section **[!UICONTROL Audiences activées]**. L’audience reçue reste disponible dans la section **[!UICONTROL Audiences reçues]** tandis que son accès reste actif.

## Afficher les audiences activées {#activated-audiences}

Utilisez la section **[!UICONTROL Audiences activées]** pour confirmer quelles audiences reçues ont été activées et consulter leur destination et leur statut de diffusion.

Chaque audience activée affiche les informations suivantes :

| Colonne | Description |
|---|---|
| **[!UICONTROL Nom de l’audience]** | Nom de l’audience activée. |
| **[!UICONTROL Statut]** | Statut d’activation actuel. |
| **[!UICONTROL Nombre d’activations]** | Nombre d’identités activées vers la destination. |
| **[!UICONTROL Dernière actualisation]** | Date et heure de la dernière actualisation de l’audience activée. |
| **[!UICONTROL Destination]** | Destination qui reçoit les données d’audience. |
| **[!UICONTROL Fréquence]** | Fréquence d’activation. Les activations manuelles s’affichent **[!UICONTROL Une fois]**. |
| **[!UICONTROL Date]** | Date d’exécution de l’activation. |
| **[!UICONTROL Clés de correspondance]** | Les clés de correspondance incluses dans l’audience activée. |

![La section Audiences activées avec les nombres d’activations actives, archivées et en pause. Chaque ligne affiche le nom de l’audience, le statut, le nombre activé, la date de dernière actualisation, la destination, la fréquence, la date d’activation, les clés de correspondance et une icône de suppression](/help/assets/collaborate/activate/activated-audiences-section.png).

### Supprimer une audience activée {#delete-activated-audience}

Supprimez une audience activée pour supprimer l’activation de la section **[!UICONTROL Audiences activées]**.

Sélectionnez l’icône de suppression (![icône de suppression.](/help/assets/icons/delete.png)). en regard de l’audience activée.

Une boîte de dialogue de confirmation s’affiche. Sélectionnez **[!UICONTROL Supprimer]** pour confirmer.

![&#x200B; Boîte de dialogue de confirmation de suppression de l’audience activée expliquant que l’audience sera supprimée de la liste des audiences activées et peut être activée à nouveau plus tard, avec les boutons Annuler et Supprimer &#x200B;](/help/assets/collaborate/activate/delete-activated-audience-confirmation.png).

L’activation est supprimée de la liste. Vous pouvez activer à nouveau l’audience reçue tant que son accès reste actif.

## Étapes suivantes {#next-steps}

Après l’envoi ou l’activation des audiences, surveillez leur statut dans les sections **[!UICONTROL Envoyer des audiences à [collaborateur]]** et **[!UICONTROL Audiences activées]**. Une fois les campagnes terminées, travaillez avec l’équipe d’activation et d’ingénierie d’Adobe pour charger les données de mesure et afficher les [rapports de mesure](./measure.md) correspondants.
