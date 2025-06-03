---
title: Se connecter avec des annonceurs ou des éditeurs
description: Après avoir découvert des collaborateurs potentiels, apprenez à établir des connexions et à commencer à collaborer sur des projets.
audience: admin, publisher, advertiser
badgelimitedavailability: label="Disponibilité limitée" type="Informative" url="https://helpx.adobe.com/legal/product-descriptions/real-time-customer-data-platform-collaboration.html newtab=true"
exl-id: 3fed93f7-1854-440c-802e-6b47e82918c9
source-git-commit: dd1386f9371cb40285315d11e07b139d3115e147
workflow-type: tm+mt
source-wordcount: '1272'
ht-degree: 17%

---

# Se connecter avec des annonceurs ou des éditeurs

{{limited-availability-release-note}}

L’établissement d’une connexion entre deux parties d’une collaboration (le plus souvent un annonceur et un éditeur) est la condition préalable dans Real-Time CDP Collaboration pour que les sociétés travaillent ensemble sur des campagnes. Les éditeurs comme les annonceurs peuvent configurer des connexions. La partie qui initie la connexion sera ensuite le *propriétaire de la connexion*.

## Workflow de haut niveau

À un niveau élevé, pour établir une connexion entre un annonceur et un éditeur, le workflow ressemble à ce qui suit :

1. L’annonceur [parcourt les éditeurs et découvre](/help/guide/connect/discover-publishers.md) l’un d’eux avec lequel il souhaite travailler
2. L’annonceur envoie une invitation à la connexion.
3. L’éditeur accepte l’invitation.
4. L’annonceur envoie les paramètres de connexion, y compris les clés de correspondance et autres. Ces paramètres de connexion représentent les conditions internes au produit de la collaboration.
5. L’éditeur accepte les paramètres de connexion. Si vous le souhaitez, l’éditeur peut rejeter les paramètres de connexion initiaux et demander à l’annonceur d’envoyer les paramètres de connexion révisés.

![Diagramme de haut niveau du processus de connexion publicitaire-éditeur.](/help/assets/connect/establish-connection/advertiser-publisher-connection-process.png){zoomable="yes"}

Une fois les éléments ci-dessus terminés, les collaborateurs peuvent passer à [créer un projet](/help/guide/collaborate/manage-projects.md#create-project) pour [exécuter des rapports de chevauchement](/help/guide/collaborate/discover.md) et lancer des campagnes publicitaires.

>[!IMPORTANT]
>
>Une fois la connexion entre deux collaborateurs établie, les paramètres de connexion ne peuvent plus être modifiés.

## Envoyer une invitation {#send-invite}

Pour configurer une connexion, sélectionnez **[!UICONTROL Connexion]** lors de la navigation dans l’inventaire des éditeurs dans l’écran Découvrir les éditeurs.

![Sélecteur Connect](/help/assets/connect/establish-connection/connect-selection.png){zoomable="yes"}

À ce stade, l’invitation est fermée et vous pouvez prévisualiser les paramètres de connexion, mais vous ne pouvez pas les modifier. Vous pouvez afficher l’invitation en attente dans l’onglet **[!UICONTROL Mes connexions]**. Le statut de la connexion est **[!UICONTROL Invitation envoyée]**.

![Invitation en attente envoyée à l&#39;éditeur affichée dans la vue Mes connexions.](/help/assets/connect/establish-connection/pending-invite-sent.png){zoomable="yes"}

Une fois que le collaborateur accepte l’invitation, vous pouvez configurer les paramètres de connexion et les envoyer au collaborateur pour révision et acceptation.

## Paramètres de connexion {#connection-settings}

>[!CONTEXTUALHELP]
>id="rtcdp_collaboration_connection_settings_usecases"
>title="Cas d’utilisation"
>abstract="Les cas d’utilisation sont préremplis avec toutes les options. Vous pouvez modifier les cas d’utilisation avant d’envoyer vos paramètres de connexion."

>[!CONTEXTUALHELP]
>id="rtcdp_collaboration_connection_settings_matchkeys"
>title="Clés correspondantes"
>abstract="Les clés correspondantes sont préremplies avec celles que vous avez sélectionnées au niveau de votre organisation. Vous pouvez désactiver toutes les clés correspondantes que vous ne souhaitez pas utiliser dans cette connexion."

>[!CONTEXTUALHELP]
>id="rtcdp_collaboration_connection_settings_creditsplit"
>title="Partage des crédits"
>abstract="Cette section détermine l’identité de la personne qui paie les activités correspondantes dans Real-Time CDP Collaboration. Actuellement, seul le cas d’utilisation du partage d’audience est configurable."

>[!CONTEXTUALHELP]
>id="rtcdp_collaboration_connection_settings_creditsplit_audiencesharing"
>title="Partage d’audiences"
>abstract="Le partage d’audience est l’activité qu’une partie entreprend lorsqu’elle demande que ses données correspondantes soient activées par son partenaire de collaboration."

>[!CONTEXTUALHELP]
>id="rtcdp_collaboration_connection_settings_creditsplit_measurement"
>title="Mesure"
>abstract="Ce cas pratique vous permet d’exécuter des activités dans Real-Time CDP Collaboration afin de générer des rapports et des informations sur les performances de la campagne."

>[!CONTEXTUALHELP]
>id="rtcdp_collaboration_connection_settings_legalagreement"
>title="Accord juridique"
>abstract="Vérifiez qu’il existe un accord de partage de données entre les deux parties."

>[!CONTEXTUALHELP]
>id="rtcdp_collaboration_connection_settings_advertisername"
>title="Noms de l’annonceur"
>abstract="<p>Paramètre facultatif. Indique le nom et l’ID par lesquels l’annonceur est connu de l’éditeur.</p><p>Le nom de l’annonceur que vous ajoutez ici sera prérempli à l’étape Créer un projet.</p><ul><li>Si l’éditeur a configuré plusieurs noms, sélectionnez-en un dans la liste.</li><li>Si un seul nom est configuré, il est automatiquement présélectionné.</li><li>Si aucun nom n’est configuré, le champ est prérempli avec le nom du compte de l’annonceur de Real-Time CDP Collaboration.</li></ul>"
>additional-url="https://experienceleague.adobe.com/fr/docs/real-time-cdp-collaboration/using/collaborate/manage-projects#create-project" text="Créer un projet"

Une fois l’invitation envoyée, vous pouvez prévisualiser les paramètres de connexion. L’invitation doit être acceptée avant que vous puissiez terminer la configuration de la connexion.

![La vue des paramètres de connexion dans l’état d’aperçu.](/help/assets/connect/establish-connection/preview-connection-settings.png){zoomable="yes"}

Une fois la connexion acceptée par votre collaborateur, vous pouvez commencer à configurer les paramètres de connexion pour la connexion. Les paramètres de connexion définissent les termes de votre collaboration, tels que les cas d’utilisation que vous accomplirez ensemble, les clés de correspondance que vous utiliserez dans les projets, etc.

Pour configurer et partager les paramètres de connexion avec votre collaborateur, accédez à **[!UICONTROL Mes connexions]**. Pour toutes les connexions dont le statut est **[!UICONTROL En attente]**, vous pouvez sélectionner **[!UICONTROL Configurer la connexion]** pour configurer les paramètres de connexion.

![La vue Mes connexions avec une connexion en attente et son option Configurer la connexion sont mises en surbrillance.](/help/assets/connect/establish-connection/pending-connection.png){zoomable="yes"}

Vous pouvez modifier et définir les champs ci-dessous :

![Configurer la vue de connexion](/help/assets/connect/establish-connection/connection-view.png){zoomable="yes"}

+++Cas d’utilisation

Les cas d’utilisation sont préremplis avec tous les cas d’utilisation disponibles. Vous pouvez choisir les cas d’utilisation que votre connexion utilisera en sélectionnant **[!UICONTROL Modifier]** et en désactivant les cas d’utilisation que vous ne souhaitez pas. Les cas d’utilisation sélectionnés affecteront les vues et options [disponibles dans vos projets](../collaborate/manage-projects.md#project-use-cases).

![Cas d&#39;utilisation](/help/assets/connect/establish-connection/view-use-cases.png){zoomable="yes"}

+++

+++Clés de correspondance

Les clés de correspondance sont préremplies avec celles que vous [avez sélectionnées au niveau de votre organisation](/help/guide/setup/onboard-organization.md#set-up-match-keys). Vous pouvez désactiver toutes les clés de correspondance que vous ne souhaitez pas utiliser dans cette connexion, mais vous ne pouvez pas ajouter de clés de correspondance qui n’ont pas été sélectionnées lors de la configuration de l’organisation.

![Clés de correspondance](/help/assets/connect/establish-connection/match-keys.png){zoomable="yes"}

+++

+++Répartition des crédits

Utilisez la section fractionnement du crédit pour déterminer laquelle des deux parties collaboratrices couvrira les coûts des activités. Les options de partage du crédit sont déterminées par les cas d’utilisation sélectionnés pour la connexion. Alors que le cas d’utilisation **[!UICONTROL Mesure]** nécessite qu’une partie prenne en charge les coûts, le cas d’utilisation **[!UICONTROL Activation de l’audience]** offre une option supplémentaire pour que chaque partie prenne en charge ses propres coûts. Pour plus d’informations sur la répartition des coûts, consultez le guide [types d’activités de crédit](/help/guide/setup/my-activity.md#types-of-activities).

>[!NOTE]
>
>Audience : la sortie est toujours couverte par le collaborateur qui reçoit l’audience. Aucune sélection n’est donc requise.

![Boîte de dialogue Partage du crédit avec des options dans l’espace de travail de connexion.](/help/assets/connect/establish-connection/credit-split.png){zoomable="yes"}
+++

+++Accords

Avant de pouvoir procéder à cette connexion, vous devez reconnaître qu’il existe un accord de partage de données entre les deux parties.

![Accords juridiques.](/help/assets/connect/establish-connection/legal-agreement.png){zoomable="yes"}

+++

+++Noms d’annonceurs

En tant qu’éditeur travaillant sur les paramètres de connexion, vous pouvez choisir d’ajouter les noms d’annonceurs par lesquels l’annonceur vous est connu dans vos systèmes. En tant qu’éditeur, vous pouvez ajouter plusieurs noms d’annonceurs à une connexion, par exemple dans les cas où l’annonceur avec lequel vous travaillez est présent dans plusieurs zones géographiques. Plus tard dans le processus, lors de la [création d’un projet](/help/guide/collaborate/manage-projects.md#create-project) pour collaborer, vous ou votre collaborateur pourrez sélectionner le nom de l’annonceur à associer au projet.

![Ajout de noms d’annonceurs modal.](/help/assets/connect/establish-connection/add-advertiser-names-modal.png)

Voici comment fonctionne la sélection du nom de l’annonceur lors de la création d’un projet :

1. **Aucun nom d’annonceur défini** : si aucun nom d’annonceur n’est ajouté, Real-Time CDP Collaboration utilise par défaut le nom de l’annonceur comme nom d’annonceur.
2. **Un nom d’annonceur défini** : si un seul nom d’annonceur est ajouté, Real-Time CDP Collaboration utilise automatiquement ce nom comme nom d’annonceur pour le projet.
3. **Plusieurs noms d’annonceur définis** : si plusieurs noms d’annonceur sont ajoutés, vous ou votre collaborateur pouvez sélectionner l’un des noms fournis lors de la création du projet.

![Noms d’annonceurs.](/help/assets/connect/establish-connection/advertiser-names.png)

+++

Une fois votre sélection effectuée, sélectionnez **[!UICONTROL Envoyer]** pour envoyer les paramètres suggérés à votre collaborateur pour révision.

Si vous recevez les paramètres de connexion proposés par votre collaborateur, vous pouvez choisir entre **[!UICONTROL Accepter]** ou **[!UICONTROL Rejeter]** ces paramètres. Avant d&#39;accepter les paramètres de connexion, vous devez reconnaître et confirmer qu&#39;un accord juridique a été conclu entre vous et le collaborateur. Si vous rejetez les paramètres de connexion, contactez votre collaborateur en dehors du produit et discutez de la manière dont il doit réviser les paramètres de connexion pour que vous les acceptiez.

## Suppression des connexions {#delete-connections}

Vous pouvez supprimer toutes les connexions avec des collaborateurs avec lesquelles vous ne souhaitez plus travailler. Pour supprimer des connexions existantes :

1. Accédez à **[!UICONTROL Connexion]** > **[!UICONTROL Mes connexions]**.
2. Sélectionnez **[!UICONTROL Afficher la connexion]** sur la carte de connexion pour accéder à la connexion à supprimer.
3. Sélectionnez l’icône de suppression ![icône de suppression](/help/assets/common/delete.svg) pour afficher la boîte de dialogue de confirmation de suppression de la connexion.
   ![Icône Supprimer la connexion mise en surbrillance.](/help/assets/connect/establish-connection/delete-icon-highlighted.png){zoomable="yes"}
4. Confirmez la suppression en sélectionnant **[!UICONTROL Supprimer]**.
   ![Boîte de dialogue pour confirmer la suppression d’une connexion. ](/help/assets/connect/establish-connection/delete-connection-dialog.png){zoomable="yes"}

>[!WARNING]
>
>Une fois la connexion supprimée, vous ne serez plus connecté au collaborateur et tous les projets existants qui font partie de la collaboration seront définitivement supprimés et irrécupérables.

## Étapes suivantes

Après avoir établi une connexion avec votre collaborateur, vous pouvez maintenant [créer des projets](/help/guide/collaborate/manage-projects.md#create-project).
