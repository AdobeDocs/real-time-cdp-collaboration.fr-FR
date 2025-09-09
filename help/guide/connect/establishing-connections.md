---
title: Établissement de connexions
description: Après avoir découvert des collaborateurs potentiels, apprenez à établir des connexions et à commencer à collaborer sur des projets.
audience: admin, publisher, advertiser
badgelimitedavailability: label="Disponibilité limitée" type="Informative" url="https://helpx.adobe.com/fr/legal/product-descriptions/real-time-customer-data-platform-collaboration.html newtab=true"
exl-id: 3fed93f7-1854-440c-802e-6b47e82918c9
source-git-commit: fcf755d5108f1f957808ead6b7022e3b9f6398b1
workflow-type: tm+mt
source-wordcount: '3230'
ht-degree: 6%

---

# Établissement de connexions

{{limited-availability-release-note}}

Avant de pouvoir travailler ensemble sur des campagnes, les collaborateurs doivent établir une connexion. Cette connexion leur permet d’activer des audiences, de créer des projets et d’exécuter des rapports sur les performances des campagnes.

Les connexions sont établies en fonction du modèle de collaboration de votre choix. Collaboration prend en charge deux schémas de collaboration principaux : publicitaire-éditeur et marque-à-marque. Pour en savoir plus sur ces modèles, consultez le guide [cas d’utilisation](/help/guide/overview/use-cases.md).

<!-- REPLACE THE LINK ABOVE WITH THE CORRECT LINK AFTER PAGE IS ESTABLISHED -->

Pour savoir comment établir une connexion, lisez la section ci-dessous qui correspond à votre modèle de collaboration :

- [Connexion publicitaire à éditeur](#advertiser-to-publisher-connection)
- [Connexion de marque à marque](#brand-to-brand-connection)

## Connexion publicitaire à éditeur {#advertiser-to-publisher-connection}

![Diagramme de haut niveau du processus de connexion publicitaire-éditeur.](/help/assets/connect/establish-connection/advertiser-publisher-flow.png){zoomable="yes"}

Dans le modèle d’annonceur à éditeur, un annonceur découvre un éditeur avec lequel il souhaite travailler via l’espace de travail **[!UICONTROL Découvrir les éditeurs]** et envoie une invitation à la connexion. L’éditeur examine ensuite l’invitation et l’accepte, ce qui lui permet de proposer des paramètres de connexion. Une fois que l’éditeur accepte les paramètres de connexion, la connexion est établie et les deux collaborateurs peuvent commencer à travailler ensemble sur des projets.

### Présentation générale

Pour établir une connexion entre un annonceur et un éditeur, les étapes suivantes sont impliquées :

1. [Découvrir les éditeurs](#discover-publishers) : l’annonceur identifie les éditeurs potentiels avec lesquels collaborer.
1. [Envoyer une invitation](#send-invite) : l’annonceur envoie une invitation à la connexion à l’éditeur sélectionné.
1. [Accepter l’invitation](#accept-invite) : l’éditeur examine et accepte l’invitation.
1. [Configurer les paramètres de connexion](#configure-connection-settings) : l’annonceur configure les paramètres de connexion et les envoie à l’éditeur pour révision.
1. [Confirmer les paramètres de connexion](#establish-connection) : l’éditeur vérifie les paramètres de connexion et les accepte ou les rejette. Si elle est acceptée, la connexion est établie. En cas de rejet, l’éditeur peut fournir des commentaires pour les révisions en dehors du produit. L’annonceur peut alors réviser les paramètres et les renvoyer pour révision.

Une fois les paramètres de connexion acceptés, la connexion est établie et les collaborateurs sont prêts à [créer un projet](/help/guide/collaborate/manage-projects.md#create-project) pour commencer à collaborer sur des campagnes.

## Connexion de marque à marque {#brand-to-brand-connection}

![Diagramme de haut niveau du processus de connexion de marque à marque.](/help/assets/connect/establish-connection/brand-to-brand-flow.png){zoomable="yes"}

>[!TIP]
>
>Le terme **marque** est utilisé pour désigner une société ou une marque en dehors de Collaboration. Le terme **collaborateur** fait référence à tout compte pouvant former une connexion dans Collaboration, qu’il s’agisse d’un annonceur ou d’un éditeur.

Dans le modèle de marque à marque, deux marques qui ont communiqué en dehors du produit peuvent se connecter directement dans Collaboration à l’aide d’une [ invitation à une connexion privée ](#private-connection-invite). Une marque peut être soit un annonceur, soit un éditeur. Ce modèle est particulièrement utile pour les marques qui peuvent ne pas correspondre au modèle publicitaire-éditeur traditionnel, telles que deux annonceurs ou deux éditeurs.

Pour commencer, un collaborateur envoie une invitation à une connexion privée à un autre collaborateur. Le destinataire examine l’invitation et l’accepte, ce qui permet au propriétaire de proposer des paramètres de connexion. Une fois que le destinataire accepte les paramètres de connexion, la connexion est établie et les deux collaborateurs peuvent commencer à travailler ensemble sur des projets.

### Présentation générale

>[!TIP]
>
>Lors de la discussion du processus de connexion, il y aura une distinction entre le **propriétaire** et le **destinataire**. Le propriétaire est le collaborateur qui lance la connexion en envoyant l’invitation, tandis que le destinataire est le collaborateur qui reçoit et révise l’invitation.

Le processus de connexion entre deux marques implique plusieurs étapes. Avant que le processus de connexion ne commence, certaines conditions préalables doivent être remplies :

1. Deux marques communiquent en dehors du produit pour discuter de la connexion potentielle.
1. Les marques [créer des comptes](/help/guide/setup/onboard-account.md) dans Collaboration si ce n’est pas déjà fait, en veillant à sélectionner le type de rôle approprié (annonceur ou éditeur).

   Une fois les conditions préalables remplies, le processus de connexion peut commencer. Les étapes suivantes décrivent le processus :

1. [Envoyer une invitation à une connexion privée](#send-private-connection-invite) : un collaborateur envoie une invitation à une connexion privée à un autre collaborateur.
1. [Accepter l’invitation à une connexion privée](#accept-private-connection-invite) : le destinataire vérifie et accepte l’invitation à la connexion privée.
1. [Configurer les paramètres de connexion](#configure-connection-settings) : le propriétaire configure les paramètres de connexion et les envoie au destinataire pour révision et acceptation.
1. [Confirmer les paramètres de connexion](#establish-connection) : le destinataire vérifie les paramètres de connexion et les accepte ou les rejette.

Une fois les paramètres de connexion acceptés, la connexion est établie et les collaborateurs sont prêts à [créer un projet](/help/guide/collaborate/manage-projects.md#create-project) pour commencer à collaborer sur des campagnes.

## Connexion {#connect}

L’espace de travail **[!UICONTROL Connect]** vous permet de gérer vos connexions avec des collaborateurs, d’envoyer des invitations à des connexions et les annonceurs peuvent parcourir le répertoire de l’éditeur. L’espace de travail est divisé en deux onglets principaux :

### Découvrir les éditeurs et éditrices {#discover-publishers}

>[!IMPORTANT]
>
>Seuls les annonceurs peuvent découvrir des éditeurs à l’aide de l’espace de travail **[!UICONTROL Découvrir des éditeurs]**. Pour en savoir plus sur la connexion avec les collaborateurs, quel que soit leur rôle, lisez la section [connexion de marque à marque](#brand-to-brand-connection).

Pour découvrir des éditeurs, accédez à l’espace de travail **[!UICONTROL Découvrir des éditeurs]** dans l’onglet **[!UICONTROL Se connecter]**. Vous pouvez parcourir la liste des éditeurs disponibles à l’aide des commandes de pagination situées au bas de l’espace de travail. Pour en savoir plus sur l’espace de travail **[!UICONTROL Découvrir les éditeurs]**, consultez le guide [Découvrir les éditeurs](/help/guide/connect/discover-publishers.md).

![L’espace de travail Découvrir les éditeurs affiche une liste des éditeurs disponibles.](/help/assets/connect/establish-connection/discover-publishers.png){zoomable="yes"}

### Envoyer une invitation {#send-invite}

>[!IMPORTANT]
>
>Cette section décrit le processus par lequel les annonceurs envoient des invitations de connexion aux éditeurs par le biais de l’espace de travail **[!UICONTROL Découvrir les éditeurs]**. Pour en savoir plus sur la création de connexions entre les marques quel que soit leur rôle, lisez la section [connexion de marque à marque](#brand-to-brand-connection) ou consultez la section [invitation à une connexion privée](#private-connection-invite).

Une fois que vous avez identifié un éditeur avec lequel vous souhaitez collaborer, sélectionnez l’option **[!UICONTROL Se connecter]** sur la vignette de l’éditeur. Cette action lance le processus de connexion.

![L’option Connexion est mise en surbrillance sur un éditeur spécifique dans l’espace de travail Découvrir les éditeurs.](/help/assets/connect/establish-connection/connect-selection.png){zoomable="yes"}

Une boîte de dialogue s’affiche, vous invitant à envoyer une invitation à la connexion à l’éditeur. Sélectionnez **[!UICONTROL Envoyer une invitation]** pour continuer.

![Boîte de dialogue Envoyer l’invitation à la connexion avec le bouton Envoyer une invitation en surbrillance.](/help/assets/connect/establish-connection/send-connection-invite-dialog.png){zoomable="yes"}

>[!NOTE]
>
>Si vous souhaitez vous connecter à un éditeur avec lequel vous avez communiqué en dehors du produit, vous pouvez utiliser l’option d’invitation à une connexion privée. Pour en savoir plus, consultez la section [invitation à une connexion privée](#private-connection-invite).

L’invitation en attente s’affiche dans l’onglet **[!UICONTROL Mes connexions]** de la section **[!UICONTROL Action requise]**. Le statut de la connexion apparaît comme **[!UICONTROL Invitation envoyée]**. Vous pouvez prévisualiser les paramètres de connexion en sélectionnant **[!UICONTROL Prévisualiser la connexion]**, mais vous ne pouvez pas les modifier tant que l’éditeur n’a pas accepté l’invitation.

![ La connexion en attente s’affiche dans l’espace de travail Mes connexions de la section Action requise ](/help/assets/connect/establish-connection/preview-connection.png){zoomable="yes"}.

### Invitation à une connexion privée {#private-connection-invite}

Les invitations à une connexion privée vous permettent de vous connecter à des collaborateurs avec lesquels vous avez communiqué en dehors du produit à l’aide d’un **[!UICONTROL code Connect]**. Pour former une connexion privée, vous devez obtenir le code **[!UICONTROL Connect]** auprès du collaborateur avec lequel vous souhaitez vous connecter en dehors du produit. Vous pouvez ensuite utiliser ce code pour envoyer une invitation à une connexion privée au collaborateur dans l’espace de travail **[!UICONTROL Connect]**.

#### Code de connexion {#connect-code}

Avant d’envoyer une invitation à une connexion privée, le collaborateur de votre choix doit vous fournir son **[!UICONTROL code Connect]** unique. Pour rechercher et copier votre **[!UICONTROL code Connect]**, accédez à l’onglet **[!UICONTROL Mon compte]** dans l’espace de travail **[!UICONTROL Configuration]**. Le **[!UICONTROL code de connexion]** s’affiche dans les détails de votre compte.

![L’onglet Mon compte dans l’espace de travail Configuration avec le code de connexion en surbrillance.](/help/assets/connect/establish-connection/connect-code.png){zoomable="yes"}

Sélectionnez l’icône de copie (![icône de copie](/help/assets/icons/copy.png)) à côté du **[!UICONTROL code Connect]** pour le copier dans le presse-papiers. Vous pouvez ensuite partager ce code avec votre collaborateur en dehors du produit.

![Le code Connect avec l’icône de copie mise en surbrillance.](/help/assets/connect/establish-connection/copy-connect-code.png){zoomable="yes"}

##### Actualisation du code de connexion {#refresh-connect-code}

Vous pouvez actualiser votre **[!UICONTROL code Connect]** à tout moment. L’actualisation du code génère un nouveau code unique que vous pouvez partager avec les collaborateurs. Cela s’avère utile si vous souhaitez invalider le code précédent pour des raisons de sécurité. Toutes les connexions établies à l’aide de l’ancien code resteront actives, mais les nouveaux collaborateurs devront utiliser le nouveau code pour se connecter à vous.

>[!IMPORTANT]
>
>Actualiser votre **[!UICONTROL code Connect]** pendant une invitation en attente peut empêcher l’acceptation de l’invitation. Si vous actualisez votre code, votre collaborateur peut avoir besoin de renvoyer l’invitation à la connexion privée à l’aide du nouveau code.

Pour actualiser votre **[!UICONTROL code de connexion]**, sélectionnez l’icône d’actualisation (![icône d’actualisation](/help/assets/icons/refresh.png)) à côté du **[!UICONTROL code de connexion]**.

![Code Connect avec l’icône d’actualisation mise en surbrillance.](/help/assets/connect/establish-connection/refresh-connect-code.png){zoomable="yes"}

>[!IMPORTANT]
>
>Aucun code de connexion n’est généré pour les comptes créés avant l’introduction de la fonction **[!UICONTROL Code de connexion]** et le champ de connexion indique **[!UICONTROL Indisponible]**. Utilisez l’option d’actualisation pour générer un nouveau code de connexion.

#### Envoyer une invitation à une connexion privée {#send-private-connection-invite}

Une fois que vous disposez du **[!UICONTROL code Connect]** de votre collaborateur, vous pouvez envoyer une invitation à une connexion privée. Pour ce faire, accédez à l’espace de travail **[!UICONTROL Connect]** et sélectionnez l’icône plus (![icône plus](/help/assets/icons/plus.png)) dans le coin supérieur droit.

![L’icône plus mise en surbrillance dans l’espace de travail Connect.](/help/assets/connect/establish-connection/private-connection-invite.png){zoomable="yes"}

La boîte de dialogue **[!UICONTROL Connect]** s’affiche et vous invite à saisir le **[!UICONTROL code Connect]** du collaborateur avec lequel vous souhaitez vous connecter. Collez le code dans le champ de texte et sélectionnez **[!UICONTROL Continuer]** pour continuer.

![La boîte de dialogue Connexion avec le champ Code de connexion renseigné et l’option Continuer mise en surbrillance.](/help/assets/connect/establish-connection/private-connection-invite-connect.png){zoomable="yes"}

La boîte de dialogue **[!UICONTROL Connexion]** affiche alors le collaborateur auquel le code est associé, ce qui vous permet de confirmer que vous vous connectez au bon collaborateur. Si le collaborateur a raison, sélectionnez **[!UICONTROL Se connecter]** pour envoyer l’invitation à la connexion privée.

![La boîte de dialogue Connexion avec les détails du collaborateur affichés et l’option Connexion mise en surbrillance.](/help/assets/connect/establish-connection/private-connection-invite-connect-confirm.png){zoomable="yes"}

### Accepter l’invitation {#accept-invite}

>[!TIP]
>
>Lors de la discussion du processus de connexion, il y aura une distinction entre le **propriétaire** et le **destinataire**. Le propriétaire est le collaborateur qui lance la connexion en envoyant l’invitation, tandis que le destinataire est le collaborateur qui reçoit et révise l’invitation.

Avant que le ou la propriétaire puisse configurer les paramètres de connexion, le ou la destinataire doit accepter l’invitation à la connexion. Pour ce faire, accédez à l’espace de travail **[!UICONTROL Connect]** et recherchez la connexion en attente dans la section **[!UICONTROL Action requise]**. Le statut de la connexion apparaît comme **[!UICONTROL Invitation reçue]**. Sélectionnez **[!UICONTROL Accepter]** pour accepter l’invitation.

![La connexion en attente s’affiche dans la section Action requise de l’espace de travail Connexion avec l’option Accepter mise en surbrillance.](/help/assets/connect/establish-connection/accept-connection.png){zoomable="yes"}

La boîte de dialogue s’affiche et vous invite à accepter l’invitation. Sélectionnez **[!UICONTROL Accepter l’invitation]** pour continuer.

![La boîte de dialogue Accepter l’invitation à la connexion avec l’option Accepter l’invitation mise en surbrillance.](/help/assets/connect/establish-connection/accept-connection-invite.png){zoomable="yes"}

Le statut de la connexion passe à **[!UICONTROL En attente]**. Le propriétaire peut maintenant configurer les paramètres de connexion.

### Configurer les paramètres de connexion {#configure-connection-settings}

Les paramètres de connexion définissent les termes entre deux collaborateurs. Ces paramètres comprennent les cas d’utilisation, les clés de correspondance, le partage du crédit et les contrats juridiques. Les collaborateurs qui se connectent aux annonceurs peuvent également ajouter des noms d’annonceurs aux paramètres de connexion, qui seront utilisés lors de la création de projets.

Une fois que le destinataire a accepté l’invitation, le propriétaire peut configurer les paramètres de connexion. Pour ce faire, accédez à **[!UICONTROL Mes connexions]** et recherchez la connexion en attente dans la section **[!UICONTROL Action requise]**. Sélectionnez **[!UICONTROL Configurer la connexion]** pour configurer les paramètres de connexion.

![Connecter l’espace de travail avec l’option Configurer la connexion mise en surbrillance dans la section Action requise ](/help/assets/connect/establish-connection/pending-connection.png){zoomable="yes"}.

L’espace de travail Paramètres de connexion s’affiche, vous permettant de configurer les différents paramètres de la connexion.

![Espace de travail des paramètres de connexion.](/help/assets/connect/establish-connection/connection-set-up.png){zoomable="yes"}

#### Paramètres de connexion {#connection-settings}

>[!CONTEXTUALHELP]
>id="rtcdp_collaboration_connection_settings_usecases"
>title="Cas d’utilisation"
>abstract="Les cas d’utilisation sont préremplis avec toutes les options. Vous pouvez modifier les cas d’utilisation avant d’envoyer vos paramètres de connexion."

>[!CONTEXTUALHELP]
>id="rtcdp_collaboration_connection_settings_matchkeys"
>title="Clés correspondantes"
>abstract="Les clés de correspondance sont préremplies avec les clés de correspondance communes que vous et votre collaborateur avez sélectionnées au niveau du compte. Vous pouvez désactiver toutes les clés correspondantes que vous ne souhaitez pas utiliser dans cette connexion."
>additional-url="https://experienceleague.adobe.com/fr/docs/real-time-cdp-collaboration/using/setup/onboard-account#set-up-match-keys" text="Clés de correspondance de compte"

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
>id="rtcdp_collaboration_connection_settings_advertisername"
>title="Noms de l’annonceur"
>abstract="<p>Paramètre facultatif. Indique le nom et l’ID par lesquels l’annonceur est connu de l’éditeur.</p><p>Le nom de l’annonceur que vous ajoutez ici sera prérempli à l’étape Créer un projet.</p><ul><li>Si l’éditeur a configuré plusieurs noms, sélectionnez-en un dans la liste.</li><li>Si un seul nom est configuré, il est automatiquement présélectionné.</li><li>Si aucun nom n’est configuré, le champ est prérempli avec le nom du compte de l’annonceur de Collaboration.</li></ul>"
>additional-url="https://experienceleague.adobe.com/fr/docs/real-time-cdp-collaboration/using/collaborate/manage-projects#create-project" text="Créer un projet"

>[!CONTEXTUALHELP]
>id="rtcdp_collaboration_audience_activation"
>title="Activation de l’audience"
>abstract="L’activation de l’audience vous permet de sélectionner le collaborateur ou la collaboratrice qui peut lancer l’activation de l’audience."

Vous pouvez configurer les paramètres de connexion suivants :

##### Activation de l’audience {#audience-activation}

>[!IMPORTANT]
>
>Pour toutes les connexions créées avant l’introduction de la fonction **[!UICONTROL Activation de l’audience]**, le paramètre d’activation de l’audience est automatiquement défini sur le propriétaire de la connexion. Si vous souhaitez permettre aux deux collaborateurs d’activer des audiences, vous devez [supprimer votre connexion actuelle](#delete-connections) et en créer une nouvelle avec les paramètres mis à jour.

L’activation de l’audience vous permet de sélectionner le collaborateur qui peut activer les audiences dans la connexion. L’activation de l’audience n’est une option que si le cas d’utilisation **[!UICONTROL Activation de l’audience]** est sélectionné. Si vous choisissez de supprimer le cas d’utilisation pendant le processus de connexion, le paramètre d’activation de l’audience sera supprimé des paramètres de connexion. Pour en savoir plus sur l’activation des audiences, consultez le guide [activer](/help/guide/collaborate/activate.md) .

Pour configurer l’activation de l’audience, sélectionnez **[!UICONTROL Configurer]** dans la section **[!UICONTROL Activation de l’audience]**. Utilisez le menu déroulant pour spécifier le collaborateur qui peut activer les audiences. Vous pouvez choisir un seul collaborateur ou permettre aux deux collaborateurs d’activer les audiences.

![Boîte de dialogue d’activation de l’audience avec des options dans l’espace de travail des paramètres de connexion.](/help/assets/connect/establish-connection/audience-activation.png){zoomable="yes"}

Lorsque vous avez terminé, sélectionnez **[!UICONTROL Enregistrer]** pour enregistrer vos modifications.

![Boîte de dialogue d’activation de l’audience avec l’option Enregistrer dans l’espace de travail des paramètres de connexion.](/help/assets/connect/establish-connection/audience-activation-confirm.png){zoomable="yes"}

##### Cas d’utilisation {#use-cases}

Les cas d’utilisation sont automatiquement renseignés avec toutes les options disponibles. Les cas d’utilisation sélectionnés déterminent les vues et options disponibles dans vos projets. Pour en savoir plus, consultez le guide [cas d’utilisation de projet](/help/guide/collaborate/manage-projects.md#project-use-cases).

Pour personnaliser vos cas d’utilisation, sélectionnez **[!UICONTROL Modifier]** dans la section **[!UICONTROL Cas d’utilisation]** et désactivez tous ceux que vous ne souhaitez pas inclure dans les projets avec votre collaborateur. Lorsque vous avez terminé, sélectionnez **[!UICONTROL Enregistrer]** pour enregistrer vos modifications.

![Paramètres des cas d’utilisation dans l’espace de travail des paramètres de connexion.](/help/assets/connect/establish-connection/view-use-cases.png){zoomable="yes"}

##### Clés correspondantes {#match-keys}

Les clés de correspondance sont automatiquement renseignées avec les clés de correspondance communes que vous et votre collaborateur avez sélectionnées lors de la [configuration de vos comptes](/help/guide/setup/onboard-account.md#set-up-match-keys). Seules les clés de correspondance que vous et votre collaborateur avez sélectionnées **et** ont en commun s’affichent.

![Espace de travail des paramètres de connexion avec la section Clés de correspondance mise en surbrillance, affichant les clés de correspondance communes.](/help/assets/connect/establish-connection/auto-populated-match-keys.png){zoomable="yes"}

Lorsque le propriétaire de la connexion configure les paramètres de connexion, il peut [modifier les clés de correspondance de compte](../setup/onboard-account.md#edit-match-keys) pour inclure des clés de correspondance supplémentaires. Après avoir activé d’autres clés de correspondance dans les paramètres de votre compte, ces clés de correspondance seront disponibles pour activer les paramètres de connexion si votre collaborateur les a également sélectionnées. Les clés de correspondance ajoutées une fois le processus de connexion démarré ne sont pas automatiquement renseignées et doivent être activées manuellement.

Pour personnaliser vos clés de correspondance, sélectionnez **[!UICONTROL Modifier]** dans la section **[!UICONTROL Clés de correspondance]** et désactivez toutes les clés de correspondance que vous ne souhaitez pas utiliser dans cette connexion. Lorsque vous avez terminé, sélectionnez **[!UICONTROL Enregistrer]** pour enregistrer vos modifications.

![L’espace de travail des paramètres de connexion avec la boîte de dialogue Section Clés de correspondance s’ouvre, affichant une clé de correspondance désactivée.](/help/assets/connect/establish-connection/additional-match-key-selected.png){zoomable="yes"}

>[!IMPORTANT]
>
>Une fois que votre collaborateur a accepté les paramètres de connexion, les clés de correspondance sont verrouillées et ne peuvent plus être modifiées.

##### Partage des crédits {#credit-split}

Utilisez la section fractionnement du crédit pour déterminer laquelle des deux parties collaboratrices couvrira les coûts des activités. Les options de partage du crédit sont déterminées par les cas d’utilisation sélectionnés pour la connexion. Alors que le cas d’utilisation **[!UICONTROL Mesure]** nécessite qu’une partie prenne en charge les coûts, le cas d’utilisation **[!UICONTROL Activation - Correspondance]** offre une option supplémentaire pour que chaque partie prenne en charge ses propres coûts. Pour plus d’informations sur la répartition des coûts, consultez le guide [types d’activités de crédit](/help/guide/setup/my-activity.md#types-of-activities).

>[!NOTE]
>
>Audience : la sortie est toujours couverte par le collaborateur qui reçoit l’audience. Aucune sélection n’est donc requise.

Pour configurer le partage des crédits, sélectionnez **[!UICONTROL Modifier]** dans la section **[!UICONTROL Partage des crédits]**. Vous pouvez ensuite sélectionner les options appropriées pour chaque cas d’utilisation. Lorsque vous avez terminé, sélectionnez **[!UICONTROL Enregistrer]** pour enregistrer vos modifications.

![Boîte de dialogue Partage du crédit avec des options dans l’espace de travail Paramètres de connexion.](/help/assets/connect/establish-connection/credit-split.png){zoomable="yes"}

##### Noms de l’annonceur {#advertiser-names}

>[!NOTE]
>
>Cette option peut apparaître lors de la configuration des paramètres de connexion ou de la révision des paramètres de connexion, selon la personne qui initie la connexion.

Si vous êtes un éditeur qui établit une connexion avec un annonceur, vous pouvez choisir d’ajouter les noms des annonceurs dans les paramètres de connexion. Cela vous permet d’ajouter plusieurs noms par lesquels l’annonceur vous est connu dans vos systèmes. Cela s’avère particulièrement utile si l’annonceur est présent dans plusieurs zones géographiques ou s’il est connu sous des noms différents dans différents contextes. Plus tard, lorsque vous créez un projet, vous pouvez sélectionner le nom d’annonceur approprié dans la liste des noms configurés dans les paramètres de connexion.

![Noms des annonceurs dans l’espace de travail des paramètres de connexion.](/help/assets/connect/establish-connection/advertiser-names.png){zoomable="yes"}

Pour ajouter des noms d’annonceurs, sélectionnez **[!UICONTROL Modifier]** dans la section **[!UICONTROL Noms d’annonceurs]**. Vous pouvez ensuite saisir l’**[!UICONTROL ID de l’annonceur]** que vous connaissez sous le nom de dans votre système, ainsi qu’un **[!UICONTROL nom de l’annonceur]** à associer à cet ID dans Collaboration. Vous pouvez ajouter plusieurs noms d’annonceurs en sélectionnant l’option **[!UICONTROL Ajouter]**.

![Boîte de dialogue Noms des annonceurs avec des options dans l’espace de travail Paramètres de connexion.](/help/assets/connect/establish-connection/advertiser-names-dialog.png){zoomable="yes"}

Lorsque vous avez terminé, sélectionnez **[!UICONTROL Enregistrer]** pour enregistrer vos modifications.

Lors de la création d’un projet, le nom de l’annonceur est prérempli en fonction des paramètres suivants établis lors de la connexion    :

1. **Aucun nom d’annonceur défini** : si aucun nom d’annonceur n’est ajouté, Collaboration utilise par défaut le nom de l’annonceur comme nom d’annonceur.
2. **Un nom d’annonceur défini** : si un seul nom d’annonceur est ajouté, Collaboration utilise automatiquement ce nom comme nom d’annonceur pour le projet.
3. **Plusieurs noms d’annonceur définis** : si plusieurs noms d’annonceur sont ajoutés, vous ou votre collaborateur pouvez sélectionner l’un des noms fournis lors de la création du projet.

>[!NOTE]
>
> Une fois les paramètres de connexion envoyés, vous ne pouvez plus ajouter ni modifier les noms des annonceurs.

![Espace de travail des paramètres de connexion avec la section Noms d’annonceurs renseignée.](/help/assets/connect/establish-connection/add-advertiser-names.png)

Une fois vos sélections effectuées, sélectionnez **[!UICONTROL Envoyer]** pour envoyer les paramètres suggérés au destinataire pour révision.

### Examiner les paramètres de connexion {#review-connection-settings}

Ensuite, le destinataire doit vérifier les paramètres de connexion proposés par le propriétaire. Pour ce faire, le destinataire peut accéder à l’onglet **[!UICONTROL Mes connexions]** dans l’espace de travail **[!UICONTROL Connexion]**. La connexion s’affiche dans la section **[!UICONTROL Action requise]**. Sélectionnez **[!UICONTROL Vérifier les paramètres de connexion]** pour vérifier les paramètres de connexion proposés.

![L’espace de travail Mes connexions avec l’option Vérifier les paramètres de connexion mise en surbrillance.](/help/assets/connect/establish-connection/review-connection-settings.png){zoomable="yes"}

Examinez les paramètres proposés par le collaborateur. Vous pouvez accepter ou refuser les paramètres de connexion. Si vous rejetez les paramètres de connexion, vous devrez communiquer avec le collaborateur au sujet des modifications que vous souhaitez apporter en dehors du produit. Les coordonnées du collaborateur sont affichées dans la section **[!UICONTROL Contact]** de l&#39;espace de travail des paramètres de connexion. Le propriétaire peut ensuite réviser les paramètres de connexion et les renvoyer pour révision.

![Espace de travail des paramètres de connexion avec les options Accepter et Rejeter mises en surbrillance.](/help/assets/connect/establish-connection/accept-connection-settings.png){zoomable="yes"}

De plus, si vous êtes un éditeur qui se connecte à un annonceur, vous pouvez désormais ajouter les noms des annonceurs dans les paramètres de connexion. Pour en savoir plus sur ce processus, consultez la section [Paramètres de connexion](#connection-settings).

>[!NOTE]
>
> Une fois que vous avez accepté les paramètres de connexion, vous ne pouvez plus ajouter ni modifier les noms des annonceurs.

Sélectionnez ensuite **[!UICONTROL Accepter]** pour poursuivre la connexion. Le statut de la connexion va passer à **[!UICONTROL Actif]** et vous pouvez maintenant commencer à collaborer sur des projets.

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
>Une fois la connexion supprimée, tous les projets existants dans la collaboration seront définitivement supprimés et irrécupérables. La demande de connexion reste en attente, mais la connexion et ses configurations ne sont plus actives. Vous devrez rétablir la connexion si vous souhaitez vous reconnecter au collaborateur.

## Étapes suivantes

Après avoir établi une connexion avec votre collaborateur, vous pouvez maintenant [créer des projets](/help/guide/collaborate/manage-projects.md#create-project).
