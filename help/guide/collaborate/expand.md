---
title: Créez des audiences d’extension dans Développer .
description: Découvrez comment créer des audiences d’extension à partir d’une audience source à l’aide de la population d’audiences d’un collaborateur dans Adobe Real-Time CDP Collaboration.
source-git-commit: d2585628407acf10ad8388231259c77991a9a0b0
workflow-type: tm+mt
source-wordcount: '872'
ht-degree: 2%
---
# (Beta) Création d’audiences d’extension dans l’onglet Développer

Utilisez l’onglet **[!UICONTROL Développer]** dans un projet pour créer une audience d’extension à partir de l’une de vos audiences. Collaboration utilise la population d’audiences de votre collaborateur pour trouver des profils qui ressemblent à votre audience initiale, ce qui vous permet d’atteindre de nouveaux prospects sans exposer les données d’audience sous-jacentes de votre collaborateur. L’audience d’extension résultante est envoyée à votre collaborateur pour activation.

## Conditions préalables {#prerequisites}

Avant de pouvoir utiliser l’onglet **[!UICONTROL Développer]**, vous devez disposer des éléments suivants :

* [Source ](/help/guide/setup/onboard-audiences.md) au moins une audience à utiliser comme audience source
* [Connecté](/help/guide/connect/establishing-connections.md) avec un collaborateur
* [A créé un projet](/help/guide/collaborate/manage-projects.md) avec ce collaborateur
* Si vous recevez une audience d’extension, une [destination](/help/guide/destinations/overview.md) configurée pour recevoir des audiences activées

## Développer la vue d’ensemble {#expand-overview}

Accédez à **[!UICONTROL Collaborer]** > **[!UICONTROL Mes projets]**, ouvrez un projet, puis sélectionnez l’onglet **[!UICONTROL Développer]**.

La page **[!UICONTROL Développer]** affiche les audiences d&#39;extension créées pour ce collaborateur et la possibilité d&#39;en créer une nouvelle.

![Onglet Développer affichant le tableau Audiences de développement avec les colonnes Nom, Statut, Taille du modèle, Portée de l’audience et Dernière mise à jour.](/help/assets/collaborate/expand/expand-overview.png){zoomable="yes"}

Le tableau **[!UICONTROL Audiences d’extension]** répertorie toutes les audiences d’extension créées dans le projet :

| Colonne | Description |
|---|---|
| **[!UICONTROL Nom]** | Nom de l’audience d’extension. La valeur par défaut est le nom de l’audience source jusqu’à sa modification. |
| **[!UICONTROL Statut]** | Statut actuel de l’audience d’extension. Voir [statut de l’audience d’extension](#expansion-audience-status) pour plus d’informations. |
| **[!UICONTROL Taille du modèle]** | Taille de l’audience d’extension générée. Non disponible tant que le modèle n’a pas terminé le traitement. |
| **[!UICONTROL Audience reach]** | Paramètre de portée d’audience utilisé pour l’audience d’extension. |
| **[!UICONTROL Dernière mise à jour]** | Date et heure de la dernière mise à jour de l’audience d’extension. |

{style="table-layout:auto"}

### Statut de l’audience d’extension {#expansion-audience-status}

Une audience d’extension passe par les statuts suivants :

| État | Description |
|---|---|
| **[!UICONTROL En cours de traitement]** | Le modèle d’extension génère toujours l’audience d’extension. |
| **[!UICONTROL Brouillon]** | Le modèle est terminé et l’audience d’extension est prête à être examinée et envoyée à votre collaborateur ou votre collaboratrice. |
| **[!UICONTROL Actif]** | Vous avez envoyé l’audience d’extension à votre collaborateur. |

{style="table-layout:auto"}

>[!NOTE]
>
>Le statut n’est pas mis à jour en temps réel. Rouvrez ou actualisez l’onglet **[!UICONTROL Développer]** pour afficher le dernier statut.

## Création d’une audience d’extension {#create-expansion-audience}

Pour créer une audience d’extension, sélectionnez l’icône d’ajout (![Ajouter une icône.](/help/assets/icons/plus.png)) sur la page **[!UICONTROL Développer]**, puis sélectionnez **[!UICONTROL Créer une audience développée]**.


La boîte de dialogue **[!UICONTROL Générer une audience d’extension]** s’affiche. Renseignez chaque champ pour générer l’audience d’extension.

![La boîte de dialogue Générer l’extension d’audience avec les champs Audience de départ, Portée de l’audience, Clé de correspondance et Membres de l’audience de départ ](/help/assets/collaborate/expand/generate-expansion-audience-dialog.png){zoomable="yes"}.

### Sélectionner l’audience source {#select-seed-audience}

Sélectionnez l’une de vos propres audiences dans le menu déroulant **[!UICONTROL Sélectionner l’audience source]**. Collaboration utilise cette audience comme base pour trouver des profils similaires dans la population de votre collaborateur.

![Le champ Audience de base dans la boîte de dialogue Générer une extension d’audience.](/help/assets/collaborate/expand/select-seed-audience.png){zoomable="yes"}

### Sélectionner une clé de correspondance {#select-match-key}

Activez une clé de correspondance pour l’audience d’extension. Vous ne pouvez pas en activer plusieurs.

| ID de personnes | ID d’appareils |
|---|---|
| **[!UICONTROL E-mail haché]** | **[!UICONTROL IPv4 haché]** |
| **[!UICONTROL Téléphone haché]** | **[!UICONTROL GAID]** |
| **[!UICONTROL Identifiant de fidélité]** | **[!UICONTROL IDFA]** |
| **[!UICONTROL ID CRM]** | **[!UICONTROL ID Demdex]** |

{style="table-layout:auto"}

>[!NOTE]
>
>Si votre audience source n’inclut pas une clé de correspondance donnée, cette option apparaît désactivée et ne peut pas être sélectionnée.

![Section Clé de correspondance de la boîte de dialogue Générer une extension d’audience avec les options de clé de correspondance disponibles.](/help/assets/collaborate/expand/select-match-key.png){zoomable="yes"}

### Sélectionner la portée de votre audience {#select-audience-reach}

Utilisez le menu déroulant **[!UICONTROL Portée de l’audience]** pour équilibrer la similarité avec votre audience source avec la portée globale. Sélectionnez **[!UICONTROL Équilibré]** pour trouver un juste milieu entre la similitude avec l’audience source et la portée globale.

![Le champ Portée de l’audience dans la boîte de dialogue Générer l’extension d’audience avec l’option Équilibrée sélectionnée et le texte de description en dessous.](/help/assets/collaborate/expand/select-audience-reach.png){zoomable="yes"}

### Inclure ou exclure l’audience source {#include-exclude-seed-audience}

Utilisez les boutons radio **[!UICONTROL Audience de départ]** pour choisir si votre audience de départ originale est incluse ou exclue de l’audience d’extension finale.

![Le champ Membres de l’audience de contrôle dans la boîte de dialogue Générer une extension d’audience avec les boutons radio Oui et Non.](/help/assets/collaborate/expand/include-exclude-seed-audience.png){zoomable="yes"}

### Générer l’audience d’extension {#generate-expansion-audience}

Une fois tous les champs renseignés, sélectionnez **[!UICONTROL Générer l’audience d’extension]**. Un message de confirmation confirme que Collaboration crée l’audience d’extension et que vous pouvez suivre sa progression sur la page **[!UICONTROL Développer]**.

## Vérifier et envoyer une audience d’extension {#review-send-expansion-audience}

Une fois que le statut d’une audience d’extension est mis à jour sur **[!UICONTROL Brouillon]**, sélectionnez son nom dans le tableau **[!UICONTROL Audiences d’extension]** pour l’ouvrir.

![Audience d’extension Page de détails affichant les métadonnées de l’audience, la taille du modèle, la taille de l’audience d’amorçage et le bouton Envoyer.](/help/assets/collaborate/expand/expansion-audience-detail.png){zoomable="yes"}

À partir de cette vue, vous pouvez :

* Modifier le nom de l’audience d’extension
* Afficher la date et l’heure de création
* Comparez la taille de l’audience source à la taille de l’audience d’extension générée
* Examinez la clé de correspondance utilisée pour générer l’audience

Lorsque vous êtes prêt, sélectionnez **[!UICONTROL Envoyer au partenaire]** pour envoyer l’audience d’extension à votre collaborateur. L’audience reste à l’état **[!UICONTROL Brouillon]** jusqu’à ce que vous l’envoyiez, puis se met à jour vers l’état **[!UICONTROL Actif]**.

>[!NOTE]
>
>Si aucune destination n&#39;est configurée pour votre collaborateur, l&#39;option **[!UICONTROL Envoyer au partenaire]** n&#39;est pas disponible. Un message explique que votre collaborateur doit d’abord configurer une destination.

>[!IMPORTANT]
>
>Une audience d’extension expire 7 jours après avoir été générée si elle n’est pas envoyée à votre collaborateur.

## Recevoir et activer une audience d’extension {#receive-activate-expansion-audience}

Lorsque vous envoyez une audience d’extension, Collaboration la diffuse à votre collaborateur en fonction du paramètre d’activation configuré pour la connexion :

* Si l’option **activation automatique** est activée, Collaboration active automatiquement l’audience d’extension vers la destination configurée de votre collaborateur et elle apparaît dans son [onglet Activer](./activate.md#activated-audiences).
<!-- Beta release: automatic activation is the only available activation setting. Uncomment the manual activation guidance below when manual activation is introduced with the GA release. -->
<!-- * If **manual activation** is enabled, the expansion audience appears in your collaborator's [Received audiences](./activate.md#received-audiences) section of the **[!UICONTROL Activate]** tab, and your collaborator must manually activate it. -->

## Étapes suivantes

Une fois que vous avez envoyé votre audience d’extension, utilisez l’onglet [Découvrir](./discover.md) pour la comparer à d’autres audiences, ou l’onglet [Activer](./activate.md) pour suivre son activation.
