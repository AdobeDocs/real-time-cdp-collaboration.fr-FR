---
title: Créer et gérer des projets
description: Découvrez comment créer et gérer des projets dans Adobe Real-Time CDP Collaboration
audience: admin, publisher, advertiser
badgelimitedavailability: label="Disponibilité limitée" type="Informative" url="https://helpx.adobe.com/legal/product-descriptions/real-time-customer-data-platform-collaboration.html newtab=true"
exl-id: ae492846-bc0a-4422-86ca-577bcc1fa60c
source-git-commit: 0cf888e36ffc4730fc8de4d8adccae0e0fc2caa8
workflow-type: tm+mt
source-wordcount: '680'
ht-degree: 11%

---

# Créer et gérer des projets

{{limited-availability-release-note}}

Les projets sont l’élément central de votre workflow dans Adobe Real-Time CDP Collaboration. Après vous être connecté avec des collaborateurs, créez un projet pour exécuter les calculs de chevauchement des audiences et découvrir les audiences pertinentes pour les campagnes.

>[!TIP]
>
>Les projets doivent généralement être associés à une seule campagne.

![Tableau de bord Collaborer affichant tous les projets actuels.](/help/assets/collaborate/manage-view-projects/projects-overview-page.png){zoomable="yes"}

Vous pouvez utiliser les filtres pour afficher uniquement les projets que vous avez démarrés avec certains collaborateurs, comme illustré ci-dessous :

![Vue filtrée des projets avec un seul collaborateur.](/help/assets/collaborate/manage-view-projects/filtered-project-view.png){zoomable="yes"}

## Créer un projet {#create-project}

>[!CONTEXTUALHELP]
>id="rtcdp_collaboration_create_project_advertisername_amc"
>title="Nom de l’annonceur (Amazon Marketing Cloud)"
>abstract="Pour les connexions Amazon Marketing Cloud (AMC), ce champ représente l’instance AMC à laquelle votre nom d’utilisateur ou d’utilisatrice Amazon Ads a accès. Il ne reflète pas le nom d’un annonceur. Si l’instance requise n’est pas répertoriée, contactez votre administrateur ou administratrice Amazon Marketing Cloud pour demander l’accès."

Pour créer un projet, vous devez d’abord [établir une connexion](/help/guide/connect/establishing-connections.md) avec un collaborateur ou une collaboratrice. Une fois la connexion établie, vous pouvez créer un projet avec ce collaborateur.

>[!CONTEXTUALHELP]
>id="rtcdp_collaboration_manage_projects_advertisername"
>title="Nom de d’annonceur"
>abstract="Sélectionnez le nom de l’annonceur dans le menu déroulant. Les options sont préconfigurées par l’éditeur dans les paramètres de connexion afin d’assurer la compatibilité avec ses systèmes."

Accédez à **[!UICONTROL Collaborer]** puis à **[!UICONTROL Mes projets]**. S’il s’agit de votre premier projet, vous pouvez sélectionner **[!UICONTROL Créer un projet]**. Sinon, vous pouvez sélectionner l’icône d’ajout (![&#x200B; Ajouter une icône &#x200B;](/help/assets/icons/plus.png)) pour créer un projet à tout moment.

![Sélectionnez le symbole plus ou Créez un projet pour configurer un nouveau projet.](/help/assets/collaborate/manage-view-projects/create-project.png){zoomable="yes"}

La boîte de dialogue **[!UICONTROL Créer un projet]** s’affiche. Sélectionnez la **[!UICONTROL Collaborateur]** avec laquelle vous créez le projet dans la liste déroulante. Si vous êtes un éditeur et que vous définissez des noms d’annonceurs lors de la configuration de votre connexion, vous pouvez sélectionner le **[!UICONTROL Nom de l’annonceur]**.

>[!NOTE]
>
> Si vous avez configuré un nom d’annonceur unique dans les paramètres de connexion, il s’affiche par défaut. Si aucun nom d’annonceur n’a été configuré, le **[!UICONTROL nom]** de l’annonceur est présélectionné comme **[!UICONTROL nom de l’annonceur]**.

![Boîte de dialogue Créer un projet avec le collaborateur sélectionné et le nom de l’annonceur mis en surbrillance.](/help/assets/collaborate/manage-view-projects/create-project-advertiser-names.png){zoomable="yes"}

Ajoutez ensuite un **[!UICONTROL Nom du projet]** et un **[!UICONTROL Description]** pour votre projet. Sélectionnez ensuite une image pour représenter le projet. Cette image permet de distinguer le projet sur la page de présentation du projet. Une fois que vous avez terminé, sélectionnez **[!UICONTROL Créer]** pour créer le projet.

![Options requises pour configurer un nouveau projet](/help/assets/collaborate/manage-view-projects/create-project-required-info.png){zoomable="yes"}

Vous pouvez maintenant afficher votre nouveau projet, ses détails et les sections disponibles en fonction des cas d’utilisation sélectionnés lors de la configuration de la connexion.

![Espace de travail de présentation du projet.](/help/assets/collaborate/manage-view-projects/project-overview.png){zoomable="yes"}

## Gérer l’identifiant de campagne {#manage-campaign-id}

Un **Identifiant de campagne** associe votre projet à une campagne spécifique. Il est nécessaire pour [générer des rapports de mesure](./measure.md#create-measurement-report). Vous pouvez ajouter plusieurs identifiants de campagne à un projet si vous exécutez plusieurs campagnes avec le même collaborateur. Toutes ces campagnes peuvent être sélectionnées dans les rapports.

- **Éditeurs** : saisissez ou mettez à jour les identifiants de campagne et les noms associés dans l’interface utilisateur de Collaboration avant d’exécuter des rapports.
- **Annonceurs** : demandez à votre collaborateur (éditeur) d’ajouter des identifiants de campagne si nécessaire.

Pour ajouter ou mettre à jour des identifiants de campagne, accédez à l’espace de travail **[!UICONTROL Collaborer]**, puis sélectionnez **[!UICONTROL Afficher]** dans la vignette de projet appropriée.

![Espace de travail de collaboration mettant en surbrillance l’option Afficher dans une carte de projet.](/help/assets/collaborate/manage-view-projects/view-project.png){zoomable="yes"}

L’espace de travail **[!UICONTROL Présentation du projet]** correspondant s’affiche avec une section **[!UICONTROL Identifiant et nom de la campagne]** qui répertorie toutes les campagnes liées au projet. Si vous n’avez pas encore ajouté de campagne, sélectionnez **[!UICONTROL Ajouter]**. Si des campagnes sont déjà présentes, sélectionnez **[!UICONTROL Modifier]** pour mettre à jour les détails ou en ajouter d’autres.

![Espace de travail de présentation du projet affichant la section Identifiant et nom de la campagne avec l’option Modifier mise en surbrillance.](/help/assets/collaborate/manage-view-projects/edit-campaign-id.png){zoomable="yes"}

Dans la boîte de dialogue **[!UICONTROL Identifiant et nom de la campagne]**, sélectionnez **[!UICONTROL Ajouter un identifiant de campagne]** pour ajouter une nouvelle ligne dans laquelle vous pouvez saisir les détails de la campagne.

![La boîte de dialogue Identifiant et nom de la campagne affiche la ligne de campagne vide après avoir sélectionné l’option Ajouter un identifiant de campagne &#x200B;](/help/assets/collaborate/manage-view-projects/add-campaign-row.png){zoomable="yes"}.

Indiquez les **[!UICONTROL Identifiant de campagne]** et **[!UICONTROL Nom de la campagne]**, puis sélectionnez **[!UICONTROL Enregistrer]**.

![La boîte de dialogue Identifiant et nom de la campagne affiche les nouveaux détails de la campagne et l’option Enregistrer mise en surbrillance.](/help/assets/collaborate/manage-view-projects/save-campaign-id.png){zoomable="yes"}

Vérifiez la section **[!UICONTROL Identifiant et nom de la campagne]** pour afficher vos dernières campagnes et vos dernières modifications. Vous pouvez désormais utiliser les nouveaux identifiants de campagne pour générer des rapports de mesure.

![Espace de travail de présentation du projet affichant la section ID et nom de campagne mis à jour.](/help/assets/collaborate/manage-view-projects/view-updated-campaigns.png){zoomable="yes"}
