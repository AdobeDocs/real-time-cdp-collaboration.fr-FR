---
title: Se connecter avec des annonceurs ou des éditeurs
description: Après avoir découvert des collaborateurs potentiels, apprenez à établir des connexions et à commencer à collaborer sur des projets.
audience: admin, publisher, advertiser
badgelimitedavailability: label="Disponibilité limitée" type="Informative" url="https://helpx.adobe.com/legal/product-descriptions/real-time-customer-data-platform-collaboration.html newtab=true"
exl-id: 3fed93f7-1854-440c-802e-6b47e82918c9
source-git-commit: eed99cfafd5ffad5a468741f7258c162454769b7
workflow-type: tm+mt
source-wordcount: '1400'
ht-degree: 16%

---

# Se connecter avec des annonceurs ou des éditeurs

{{limited-availability-release-note}}

Avant de pouvoir travailler ensemble sur des campagnes, les collaborateurs doivent établir une connexion. Cette connexion leur permet d’activer des audiences, de créer des projets et d’exécuter des rapports sur les performances des campagnes.

## Workflow de haut niveau

Pour établir une connexion entre un annonceur et un éditeur, les étapes suivantes sont requises :

1. L’annonceur [parcourt les éditeurs et découvre](/help/guide/connect/discover-publishers.md) un éditeur avec lequel il aimerait travailler.
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

Pour configurer une connexion, sélectionnez **[!UICONTROL Connexion]** lors de la navigation dans l’inventaire des éditeurs dans l’espace de travail **[!UICONTROL Découvrir les éditeurs]**.

![Le tableau de bord de connexion avec l’option Se connecter mise en surbrillance sur un éditeur spécifique.](/help/assets/connect/establish-connection/connect-selection.png){zoomable="yes"}

Une fois l’invitation envoyée, vous pouvez prévisualiser (mais pas modifier) les paramètres de connexion. L’affichage de l’invitation en attente s’affiche dans l’onglet **[!UICONTROL Mes connexions]**. Le statut de la connexion apparaît comme **[!UICONTROL Invitation envoyée]**.

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
>abstract="Cette section détermine l’identité de la personne qui paie les activités correspondantes dans Collaboration."

>[!CONTEXTUALHELP]
>id="rtcdp_collaboration_connection_settings_creditsplit_audiencesharing"
>title="Partage d’audiences"
>abstract="Les crédits d’activation de l’audience sont consommés en fonction du nombre d’identifiants correspondants préparés pour l’activation."

>[!CONTEXTUALHELP]
>id="rtcdp_collaboration_connection_settings_creditsplit_measurement"
>title="Mesure"
>abstract="Exécutez des activités pour générer des rapports et des informations sur les performances de la campagne. Les crédits sont consommés en fonction du nombre de lignes dans les rapports de campagne sur toutes les campagnes et de la fréquence de création des rapports (quotidienne, tous les trois jours ou hebdomadaire)."

>[!CONTEXTUALHELP]
>id="rtcdp_collaboration_connection_settings_legalagreement"
>title="Accord juridique"
>abstract="Vérifiez qu’il existe un accord de partage de données entre les deux parties."

>[!CONTEXTUALHELP]
>id="rtcdp_collaboration_connection_settings_advertisername"
>title="Noms de l’annonceur"
>abstract="<p>Paramètre facultatif. Indique le nom et l’ID par lesquels l’annonceur est connu de l’éditeur.</p><p>Le nom de l’annonceur que vous ajoutez ici sera prérempli à l’étape Créer un projet.</p><ul><li>Si l’éditeur a configuré plusieurs noms, sélectionnez-en un dans la liste.</li><li>Si un seul nom est configuré, il est automatiquement présélectionné.</li><li>Si aucun nom n’est configuré, le champ est prérempli avec le nom du compte de l’annonceur de Collaboration.</li></ul>"
>additional-url="https://experienceleague.adobe.com/fr/docs/real-time-cdp-collaboration/using/collaborate/manage-projects#create-project" text="Créer un projet"

>[!CONTEXTUALHELP]
>id="rtcdp_collaboration_audience_activation"
>title="Activation de l’audience"
>abstract="L’activation de l’audience vous permet de sélectionner le collaborateur ou la collaboratrice qui peut lancer l’activation de l’audience."

<!-- Move and update the above popover when bidirectional is active. -->

Une fois l’invitation envoyée, vous pouvez prévisualiser les paramètres de connexion. L’invitation doit être acceptée avant que vous puissiez terminer la configuration de la connexion.

![La vue des paramètres de connexion dans l’état d’aperçu.](/help/assets/connect/establish-connection/preview-connection-settings.png){zoomable="yes"}

<!-- The sections below will be updated in B2B and have not been addressed yet. -->

### Paramètres de connexion de l’annonceur {#advertiser-connection-settings}

Une fois que votre collaborateur a accepté la connexion, configurez les paramètres de connexion. Ces paramètres définissent vos termes de collaboration, y compris les cas d’utilisation sur lesquels vous travaillerez, les clés de correspondance pour les projets et d’autres configurations.

Pour commencer, accédez à **[!UICONTROL Mes connexions]**. Pour toutes les connexions dont le statut est **[!UICONTROL En attente]**, vous pouvez sélectionner **[!UICONTROL Configurer la connexion]** pour configurer les paramètres de connexion.

![L’espace de travail Mes connexions avec une connexion en attente et son option Configurer la connexion sont mis en surbrillance.](/help/assets/connect/establish-connection/pending-connection.png){zoomable="yes"}

Vous pouvez modifier et définir les champs ci-dessous :

![Espace de travail des paramètres de connexion avant qu’il ne soit rempli.](/help/assets/connect/establish-connection/connection-view.png){zoomable="yes"}

+++Cas d’utilisation

Les cas d’utilisation sont préremplis avec toutes les options disponibles. Pour les personnaliser, sélectionnez **[!UICONTROL Modifier]** dans la section **[!UICONTROL Cas d’utilisation]** et désactivez ceux que vous ne souhaitez pas. Les cas d’utilisation sélectionnés déterminent les vues et options [disponibles dans vos projets](../collaborate/manage-projects.md#project-use-cases).

![Paramètres des cas d’utilisation dans l’espace de travail des paramètres de connexion.](/help/assets/connect/establish-connection/view-use-cases.png){zoomable="yes"}

+++

+++Clés de correspondance

Les clés de correspondance sont préremplies avec celles que vous avez sélectionnées lors de la [configuration de votre organisation](/help/guide/setup/onboard-account.md#set-up-match-keys). Vous pouvez désactiver toutes les clés de correspondance que vous ne souhaitez pas utiliser, mais vous ne pouvez pas ajouter de clés de correspondance qui n’ont pas été sélectionnées lors de la configuration de l’organisation.

![Paramètres de clé de correspondance dans l’espace de travail des paramètres de connexion.](/help/assets/connect/establish-connection/match-keys.png){zoomable="yes"}

+++

+++Répartition des crédits

Utilisez la section fractionnement du crédit pour déterminer laquelle des deux parties collaboratrices couvrira les coûts des activités. Les options de partage du crédit sont déterminées par les cas d’utilisation sélectionnés pour la connexion. Alors que le cas d’utilisation **[!UICONTROL Mesure]** nécessite qu’une partie prenne en charge les coûts, le cas d’utilisation **[!UICONTROL Activation - Correspondance]** offre une option supplémentaire pour que chaque partie prenne en charge ses propres coûts. Pour plus d’informations sur la répartition des coûts, consultez le guide [types d’activités de crédit](/help/guide/setup/my-activity.md#types-of-activities).

>[!NOTE]
>
>Audience : la sortie est toujours couverte par le collaborateur qui reçoit l’audience. Aucune sélection n’est donc requise.

![Boîte de dialogue Partage du crédit avec des options dans l’espace de travail de connexion.](/help/assets/connect/establish-connection/credit-split.png){zoomable="yes"}
+++

+++Accords

Avant de pouvoir procéder à cette connexion, vous devez reconnaître qu’il existe un accord de partage de données entre les deux parties.

![La section Accord juridique met en surbrillance et est confirmée dans l’espace de travail de connexion.](/help/assets/connect/establish-connection/legal-agreement.png){zoomable="yes"}

+++

Une fois vos sélections effectuées, sélectionnez **[!UICONTROL Envoyer]** pour envoyer les paramètres suggérés à votre collaborateur pour révision.

### Paramètres de connexion de l’éditeur {#publisher-connection-settings}

L’éditeur doit ensuite vérifier les paramètres de connexion et les accepter ou les refuser. Pour vérifier les paramètres de connexion, accédez à **[!UICONTROL Mes connexions]** et sélectionnez **[!UICONTROL Vérifier les paramètres de connexion]** dans la carte de connexion.

![l’option Vérifier les paramètres de connexion mise en surbrillance dans la vue Mes connexions](/help/assets/connect/establish-connection/review-connection-settings.png){zoomable="yes"}.

Examinez les paramètres proposés par le collaborateur. Avant d’accepter les paramètres de connexion, vous devez reconnaître qu’un accord juridique a été conclu entre vous et le collaborateur. En outre, vous pouvez ajouter les noms d’annonceurs par lesquels l’annonceur vous est connu dans vos systèmes.

![Espace de travail des paramètres de connexion avec les paramètres proposés par le collaborateur et les sections Noms et contrats de l’annonceur mises en surbrillance.](/help/assets/connect/establish-connection/publisher-connection-settings.png){zoomable="yes"}

+++Noms d’annonceurs

En tant qu’éditeur travaillant sur les paramètres de connexion, vous pouvez choisir d’ajouter les noms d’annonceurs par lesquels l’annonceur vous est connu dans vos systèmes. En tant qu’éditeur, vous pouvez ajouter plusieurs noms d’annonceurs à une connexion, par exemple dans les cas où l’annonceur avec lequel vous travaillez est présent dans plusieurs zones géographiques. Plus tard dans le processus, lors de la [création d’un projet](/help/guide/collaborate/manage-projects.md#create-project) pour collaborer, vous ou votre collaborateur pourrez sélectionner le nom de l’annonceur à associer au projet.

![Boîte de dialogue Noms d’annonceurs dans l’espace de travail Paramètres de connexion.](/help/assets/connect/establish-connection/add-advertiser-names-modal.png)

Voici comment fonctionne la sélection du nom de l’annonceur lors de la création d’un projet :

1. **Aucun nom d’annonceur défini** : si aucun nom d’annonceur n’est ajouté, Real-Time CDP Collaboration utilise par défaut le nom de l’annonceur comme nom d’annonceur.
2. **Un nom d’annonceur défini** : si un seul nom d’annonceur est ajouté, Real-Time CDP Collaboration utilise automatiquement ce nom comme nom d’annonceur pour le projet.
3. **Plusieurs noms d’annonceur définis** : si plusieurs noms d’annonceur sont ajoutés, vous ou votre collaborateur pouvez sélectionner l’un des noms fournis lors de la création du projet.

![Espace de travail des paramètres de connexion avec la section Noms d’annonceurs renseignée.](/help/assets/connect/establish-connection/advertiser-names.png)

+++

>[!NOTE]
>
> Une fois que vous avez accepté les paramètres de connexion, vous ne pouvez plus ajouter ni modifier les noms des annonceurs.

Si les paramètres de connexion proposés vous conviennent, sélectionnez **[!UICONTROL Accepter]** pour établir la connexion. Si vous souhaitez demander des modifications des paramètres de connexion, sélectionnez **[!UICONTROL Rejeter]**. Le collaborateur peut ensuite réviser les paramètres de connexion et les renvoyer pour révision.

<!-- The end of the sections needing updates still. -->

## Suppression des connexions {#delete-connections}

Vous pouvez supprimer toutes les connexions avec des collaborateurs avec lesquelles vous ne souhaitez plus travailler. Pour supprimer des connexions existantes, accédez à **[!UICONTROL Connexion]**. En tant qu’éditeur, votre connexion existante s’affiche. En tant qu’annonceur, vous devez ensuite accéder à **[!UICONTROL Mes connexions]**.

Sélectionnez **[!UICONTROL Afficher la connexion]** sur la carte de connexion à supprimer.

![L’option Afficher la connexion est mise en surbrillance dans la vue Mes connexions.](/help/assets/connect/establish-connection/delete-view-connection.png){zoomable="yes"}

Sélectionnez l’icône de suppression ![icône de suppression](/help/assets/common/delete.svg) dans l’espace de travail de connexion pour supprimer la connexion.

![Icône de suppression mise en surbrillance dans l’espace de travail de connexion.](/help/assets/connect/establish-connection/delete-option.png){zoomable="yes"}

Une boîte de dialogue de confirmation s’affiche, vous demandant de confirmer la suppression de la connexion. Sélectionnez **[!UICONTROL Supprimer]** pour confirmer la suppression.

![Boîte de dialogue de confirmation permettant de supprimer une connexion.](/help/assets/connect/establish-connection/delete-confirmation-dialog.png){zoomable="yes"}

>[!WARNING]
>
>Une fois la connexion supprimée, vous ne serez plus connecté au collaborateur et tous les projets existants qui font partie de la collaboration seront définitivement supprimés et irrécupérables.

## Étapes suivantes

Après avoir établi une connexion avec votre collaborateur, vous pouvez maintenant [créer des projets](/help/guide/collaborate/manage-projects.md#create-project).
