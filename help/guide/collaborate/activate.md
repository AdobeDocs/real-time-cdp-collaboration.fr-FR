---
title: Activer les audiences
description: Découvrez comment envoyer des audiences et activer automatiquement ou manuellement les audiences reçues vers les destinations dans Adobe Real-Time CDP Collaboration.
audience: admin, publisher, advertiser
exl-id: fd82fcbf-ab39-48e0-9438-0a9046693431
TQID: https://experienceleague.adobe.com/bfPHtcW8Mf6RhIlg5fKcJmPSEKDyAODjbNRJ5D3SMkQ
product_v2:
  - id: fdddec33-c9cb-4459-b8b6-2664395a6f10
    internal-label: Real-Time Customer Data Platform
feature_v2:
  - id: ba929a52-9339-4154-9487-317dc875a3c7
    internal-label: Use cases
topic_v2:
  - id: c2be0313-b3ae-45e0-b454-d20bf54b23f2
    internal-label: Measurement
  - id: e1e0219c-f879-479f-8427-888ed2a6e9c2
    internal-label: Insights
source-git-commit: df0c7fe0d09203a02a192931135abaa1715e593f
workflow-type: tm+mt
source-wordcount: '2043'
ht-degree: 2%
---
# Activer les audiences

Utilisez l’onglet **[!UICONTROL Activer]** dans un projet pour envoyer des audiences à votre collaborateur, passer en revue les audiences reçues de votre collaborateur et activer les audiences reçues pour diffusion vers une destination configurée. L’activation peut être créée automatiquement à la réception de l’audience ou manuellement par le collaborateur récepteur. Pour configurer et gérer les destinations à partir de l’espace de travail de niveau supérieur **[!UICONTROL Activation]**, consultez la [présentation des destinations](../destinations/overview.md).

>[!IMPORTANT]
>
>L’onglet **[!UICONTROL Activer]** n’est disponible que si le cas d’utilisation **Activation de l’audience** a été activé [pendant le processus de connexion](../connect/establishing-connections.md#connection-settings). Pour plus d’informations sur les cas d’utilisation, voir [Gestion de projets](./manage-projects.md#project-use-cases).

Utilisez l’onglet [Découvrir](./discover.md) pour identifier les audiences qui correspondent le mieux à votre campagne, puis envoyez-les à votre collaborateur ou collaboratrice.

Si le destinataire configure une destination d’activation automatique dans les paramètres de connexion, l’expéditeur sélectionne un planning d’activation lors de l’envoi de l’audience. La destination est en lecture seule pour l’expéditeur. Lorsque l’audience est reçue, elle est automatiquement activée vers la destination configurée du destinataire selon le planning d’activation de l’expéditeur. Pour obtenir des instructions de configuration de la connexion, voir [Configurer une destination d’activation automatique](../connect/manage-connections.md#configure-auto-activation-destination).

Si le destinataire n’a pas configuré de destination d’activation automatique, l’envoi et l’activation restent des actions distinctes. L’envoi donne au destinataire l’accès à une audience, et celui-ci sélectionne une destination et un planning lors de son activation manuelle. Seules les destinations préconfigurées peuvent être sélectionnées pour l’activation dans un projet. Pour obtenir des instructions sur la configuration des destinations, voir [ Gérer les destinations ](../destinations/manage-destinations.md).

Les sections et actions disponibles varient selon que votre organisation envoie ou reçoit des audiences dans le projet. L&#39;onglet **[!UICONTROL Activer]** contient les sections suivantes :

| Section | Description |
|---|---|
| **[!UICONTROL Audiences envoyées à [collaborateur]]** | Audiences que vous avez envoyées à votre collaborateur. |
| **[!UICONTROL Audiences reçues]** | Audiences que votre collaborateur vous a envoyées et qui sont disponibles pour activation. |
| **[!UICONTROL Audiences activées]** | Audiences reçues avec activations créées automatiquement ou manuellement. |

![Onglet Activer au niveau du projet avec des comptes de synthèse en haut des sections Audiences envoyées et étendues, Audiences reçues et Audiences activées . Chaque section affiche le nombre de statuts et un tableau des détails de l’audience.](/help/assets/collaborate/activate/activate-dashboard.png){zoomable="yes"}

## Conditions préalables {#prerequisites}

Avant d’envoyer ou d’activer des audiences, assurez-vous des points suivants :

- Les audiences sont sourcées et disponibles pour l’envoi. Pour plus d&#39;informations, voir [Source et gérer les audiences](../setup/onboard-audiences.md).
- Les audiences atteignent le seuil minimum de 1 000 identités de chevauchement requis pour l’envoi et l’activation.
- Les audiences sont configurées avec les clés de correspondance requises lors de l’utilisation d’audiences à clés de correspondance multiples.
- Au moins une destination est configurée si vous devez activer les audiences reçues. Pour plus d’informations, voir la [présentation des destinations](../destinations/overview.md).
- Pour l’activation automatique, le destinataire possède une destination active et l’a sélectionnée comme [destination d’activation automatique](../connect/manage-connections.md#configure-auto-activation-destination) de la connexion.

## Envoyer les audiences {#send-audiences}

Envoyez une audience pour permettre à votre collaborateur d’y accéder. Une fois l’audience envoyée, elle apparaît dans votre section **[!UICONTROL Envoi d’audiences à [collaborateur]]** et dans la section **[!UICONTROL Audiences reçues]** de votre collaborateur.

Accédez à **[!UICONTROL Collaborer]**, ouvrez un projet, puis sélectionnez l’onglet **[!UICONTROL Activer]**.

Dans la section **[!UICONTROL Audiences envoyées à [collaborateur]]**, sélectionnez l’icône d’ajout (![Ajouter une icône.](/help/assets/icons/plus.png)). Si aucune audience n’a été envoyée, sélectionnez **[!UICONTROL Envoyer l’audience]** dans l’affichage vide à la place.

![Onglet Activer au niveau du projet lorsqu’aucune audience n’a été envoyée. Le message d’affichage vide explique que vous n’avez pas envoyé d’audience et affiche un bouton Envoyer une audience ](/help/assets/collaborate/activate/activate-new-audiences.png){zoomable="yes"}.

Le workflow **[!UICONTROL Envoyer des audiences]** s’ouvre. Utilisez le sélecteur d’audiences pour trouver une audience ou sélectionnez **[!UICONTROL Parcourir les audiences]** pour comparer les audiences disponibles.

>[!IMPORTANT]
>
>Seules les audiences avec plus de 1 000 identités qui se chevauchent sont disponibles pour l’activation. Si les chevauchements d’audiences sont proches du seuil d’identité de 1 000, l’activation peut échouer.

![Workflow Envoyer des audiences avec un sélecteur d’audience et un bouton Parcourir les audiences. Le workflow permet à l’expéditeur de choisir une audience avant de configurer les clés de correspondance et les paramètres d’accès.](/help/assets/collaborate/activate/audience-activation.png){zoomable="yes"}

Dans la boîte de dialogue **[!UICONTROL Parcourir les audiences]**, passez en revue les **[!UICONTROL Nombre d’identités]**, **[!UICONTROL Chevauchement des identités]** et **[!UICONTROL Chevauchement de %]** pour chaque audience.

![La boîte de dialogue Parcourir les audiences répertoriant les audiences disponibles avec leur nombre d’identités, leur nombre d’identités qui se chevauchent et leur pourcentage de chevauchement.](/help/assets/collaborate/activate/browse-audiences.png){zoomable="yes"}

>[!IMPORTANT]
>
>Si une audience utilise plusieurs clés de correspondance, chaque clé de correspondance sélectionnée doit respecter le seuil de chevauchement requis. Utilisez l’onglet [Découvrir](./discover.md) pour vérifier que l’audience répond aux exigences de chevauchement avant de l’envoyer.

Sélectionnez l’audience à envoyer, puis sélectionnez **[!UICONTROL Enregistrer]**.

L’audience sélectionnée apparaît dans le workflow avec son identité et ses informations de chevauchement.

![Le workflow Envoyer des audiences avec une audience sélectionnée affichant son nombre d’identités, le nombre d’identités qui se chevauchent, le pourcentage de chevauchement, les clés de correspondance et l’option Modifier les clés de correspondance.](/help/assets/collaborate/activate/audience-selected.png){zoomable="yes"}

### Modifier les clés correspondantes {#edit-match-keys}

Utilisez les clés de correspondance configurées pour la connexion du collaborateur ou supprimez les clés de correspondance qui ne s’appliquent pas à l’audience.

Sélectionnez **[!UICONTROL Modifier les clés de correspondance]** dans l’audience sélectionnée.

![Audience sélectionnée dans le workflow Envoyer les audiences avec l’option Modifier les clés de correspondance mise en surbrillance.](/help/assets/collaborate/activate/edit-match-keys.png){zoomable="yes"}

La boîte de dialogue **[!UICONTROL Modifier les clés de correspondance]** s’affiche. Désactivez toutes les clés de correspondance que vous ne souhaitez pas utiliser, puis sélectionnez **[!UICONTROL Enregistrer]**.

>[!NOTE]
>
>Au moins une clé de correspondance doit rester sélectionnée.

![La boîte de dialogue Modifier les clés de correspondance avec des commandes de basculement pour les clés de correspondance disponibles via la connexion du collaborateur et un bouton Enregistrer.](/help/assets/collaborate/activate/edit-match-keys-selection.png){zoomable="yes"}

### Configuration de l’accès aux audiences {#configure-audience-access}

Configurez la manière dont l’audience est envoyée et la durée pendant laquelle votre collaborateur peut y accéder.

Utilisez le contrôle **[!UICONTROL Durée d&#39;accès]** pour sélectionner l&#39;une des options suivantes :

- **[!UICONTROL Envoyer maintenant (une seule fois)]** : envoyez l’audience une fois. Le collaborateur récepteur peut l’activer une fois.
- **[!UICONTROL Planifier l’envoi d’audience récurrente]** : actualisez l’audience pendant une période d’accès spécifiée. Utilisez le contrôle **[!UICONTROL Période]** pour sélectionner les dates de début et de fin.

![L’étape Durée d’accès du workflow Envoyer les audiences avec des options pour envoyer l’audience une seule fois ou planifier l’envoi d’une audience récurrente. L&#39;option récurrente affiche des contrôles de date pour définir la période d&#39;accès.](/help/assets/collaborate/activate/activation-frequency.png)

### Choisir un planning d’activation automatique {#auto-activation-schedule}

Si votre collaborateur a configuré une destination d’activation automatique pour la connexion, la section **[!UICONTROL Activation]** indique que l’option **[!UICONTROL Activation automatique]** est activée. La destination sélectionnée par le destinataire s&#39;affiche en lecture seule. En tant qu’expéditeur, utilisez **[!UICONTROL Fréquence]** pour choisir le moment où l’activation s’exécute :

- **[!UICONTROL Activer maintenant (une seule fois)]** : exécutez l’activation une fois lorsque l’audience est reçue.
- **[!UICONTROL Planifier l’activation d’audience unique]** : exécutez l’activation une seule fois à la date et à l’heure futures que vous sélectionnez.
- **[!UICONTROL Planifier une activation récurrente]** : exécutez l’activation selon le planning que vous configurez pendant la période sélectionnée.

![Le workflow Envoyer les audiences avec l’activation automatique activée et le menu Fréquence affichant les options d’activation immédiate, future, ponctuelle et récurrente.](/help/assets/collaborate/activate/choose-auto-activation-schedule.png){zoomable="yes"}

Pour une activation récurrente, configurez le planning d’activation, l’heure de début et la période. L’activation automatique prend en charge des plannings immédiats, futurs, ponctuels ou récurrents ; les plannings récurrents ne sont pas requis.

![Le workflow Envoyer les audiences est configuré avec un planning d’activation récurrent quotidien, l’heure de début et la période.](/help/assets/collaborate/activate/configure-recurring-auto-activation.png){zoomable="yes"}

Une fois l’audience et les paramètres d’accès définis, sélectionnez **[!UICONTROL Envoyer]**.

L’audience s’affiche dans votre section **[!UICONTROL Audiences envoyées à [collaborateur]]**. Votre collaborateur peut le consulter dans sa section **[!UICONTROL Audiences reçues]**. Si l’activation automatique est activée, Collaboration crée également l’activation pour le récepteur, et l’activation s’exécute selon le planning que vous avez sélectionné.

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

![Section Audiences envoyées avec l’icône de suppression affichée en regard d’une ligne d’audience.](/help/assets/collaborate/activate/delete-sent-audiences.png){zoomable="yes"}

Une boîte de dialogue de confirmation s’affiche. Sélectionnez **[!UICONTROL Supprimer]** pour confirmer.

![Boîte de dialogue de confirmation de suppression de l’audience envoyée expliquant que l’audience sera supprimée et que le collaborateur n’y aura plus accès, avec les boutons Annuler et Supprimer.](/help/assets/collaborate/activate/delete-sent-audiences-confirmation.png)

L’audience est supprimée de la section et votre collaborateur n’y a plus accès.

## Afficher les audiences reçues {#received-audiences}

Utilisez la section **[!UICONTROL Audiences reçues]** pour passer en revue les audiences que votre collaborateur vous a envoyées. Si une destination d’activation automatique a été configurée avant l’envoi de l’audience, Collaboration crée automatiquement une activation à la réception de l’audience. Pour les activations automatiques récurrentes, vous pouvez également créer une activation manuelle supplémentaire vers une autre destination. Voir [ Activer manuellement une audience reçue ](#activate-received-audience) pour plus d’informations. Si aucune destination d’activation automatique n’a été configurée, activez l’audience manuellement.

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

![La section Audiences reçues avec les nombres de profils des audiences actifs et expirés. Chaque ligne d’audience affiche son nom, son statut, des informations d’identité, la dernière exécution du flux de données, la durée d’accès, les clés de correspondance et une icône d’ajout utilisée pour commencer l’activation.](/help/assets/collaborate/activate/received-audiences-section.png){zoomable="yes"}

### Activer manuellement une audience reçue {#activate-received-audience}

Activez manuellement une audience reçue pour envoyer ses données à l’une de vos destinations configurées.

Dans la section **[!UICONTROL Audiences reçues]**, sélectionnez l’icône d’ajout (![Ajouter une icône.](/help/assets/icons/plus.png)) à côté de l’audience à activer.

La boîte de dialogue **[!UICONTROL Activer l’audience]** s’affiche.

Utilisez **[!UICONTROL Destination]** pour sélectionner la destination qui reçoit les données d’audience. Si la liste de destinations est vide, configurez une destination avant de continuer. Pour obtenir des instructions, consultez la [présentation des destinations](../destinations/overview.md).

Configurez la **[!UICONTROL Fréquence]** et les commandes de planification disponibles pour choisir quand et à quelle fréquence l’activation s’exécute. Sélectionnez ensuite **[!UICONTROL Activer]**.

L’exemple suivant illustre le workflow d’activation manuelle avec la destination **[!UICONTROL Exportations d’audiences Northstar]** sélectionnée.

![Exemple de la boîte de dialogue manuelle Activer l’audience pour les clients Northstar Fall Campaign, avec l’option Exportations d’audience Northstar sélectionnée et un planning quotidien, une heure de début et une période configurés.](/help/assets/collaborate/activate/manually-activate-received-audience.png){zoomable="yes"}

>[!NOTE]
>
>Pour une audience reçue avec une activation automatique récurrente, vous pouvez créer manuellement une activation supplémentaire pour cette audience vers une autre destination. L’activation automatique récurrente se poursuit indépendamment.

La boîte de dialogue se ferme et l’activation s’affiche dans la section **[!UICONTROL Audiences activées]**. L’audience reçue reste disponible dans la section **[!UICONTROL Audiences reçues]** tandis que son accès reste actif.

## Afficher les audiences activées {#activated-audiences}

Utilisez la section **[!UICONTROL Audiences activées]** pour confirmer quelles audiences reçues ont créé automatiquement ou manuellement des activations et consulter leur destination et leur statut de diffusion. Les activations créées automatiquement apparaissent ici sans que le destinataire ait à terminer le workflow d’activation manuelle.

![Onglet Activer affichant les clients Northstar Fall Campaign dans les audiences reçues et son activation quotidienne créée automatiquement vers les exportations d’audiences Northstar dans les audiences activées.](/help/assets/collaborate/activate/view-auto-activated-audience.png){zoomable="yes"}

Chaque audience activée affiche les informations suivantes :

| Colonne | Description |
|---|---|
| **[!UICONTROL Nom de l’audience]** | Nom de l’audience activée. |
| **[!UICONTROL Statut]** | Statut d’activation actuel. |
| **[!UICONTROL Nombre d’activations]** | Nombre d’identités activées vers la destination. |
| **[!UICONTROL Dernière actualisation]** | Date et heure de la dernière actualisation de l’audience activée. |
| **[!UICONTROL Destination]** | Destination qui reçoit les données d’audience. |
| **[!UICONTROL Fréquence]** | Fréquence d’activation, par exemple planification unique ou récurrente. |
| **[!UICONTROL Date]** | Date ou période d’exécution de l’activation. |
| **[!UICONTROL Clés de correspondance]** | Les clés de correspondance incluses dans l’audience activée. |

![La section Audiences activées avec les nombres d’activations actives, archivées et en pause. Chaque ligne affiche le nom de l’audience, le statut, le nombre activé, la date de dernière actualisation, la destination, la fréquence, la date d’activation, les clés de correspondance et une icône de suppression](/help/assets/collaborate/activate/activated-audiences-section.png){zoomable="yes"}.

### Supprimer une audience activée {#delete-activated-audience}

Supprimez une audience activée pour supprimer l’activation de la section **[!UICONTROL Audiences activées]**.

Sélectionnez l’icône de suppression (![icône de suppression.](/help/assets/icons/delete.png)). en regard de l’audience activée.

Une boîte de dialogue de confirmation s’affiche. Sélectionnez **[!UICONTROL Supprimer]** pour confirmer.

![ Boîte de dialogue de confirmation de suppression de l’audience activée expliquant que l’audience sera supprimée de la liste des audiences activées et peut être activée à nouveau plus tard, avec les boutons Annuler et Supprimer ](/help/assets/collaborate/activate/delete-activated-audience-confirmation.png).

L’activation est supprimée de la liste. Vous pouvez activer à nouveau l’audience reçue tant que son accès reste actif.

## Étapes suivantes {#next-steps}

Après l’envoi ou l’activation des audiences, surveillez leur statut dans les sections **[!UICONTROL Envoyer des audiences à [collaborateur]]** et **[!UICONTROL Audiences activées]**. Une fois les campagnes terminées, travaillez avec l’équipe d’activation et d’ingénierie d’Adobe pour charger les données de mesure et afficher les [rapports de mesure](./measure.md) correspondants.
