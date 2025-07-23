---
title: Gérer l’accès des utilisateurs et utilisatrices via les autorisations
description: Gérez les autorisations et l’accès des utilisateurs aux différents composants de l’interface utilisateur de Real-Time CDP Collaboration.
audience: admin
badgelimitedavailability: label="Disponibilité limitée" type="Informative" url="https://helpx.adobe.com/legal/product-descriptions/real-time-customer-data-platform-collaboration.html newtab=true"
exl-id: 0155f6a6-5e67-4415-af96-1848345842e4
source-git-commit: eed99cfafd5ffad5a468741f7258c162454769b7
workflow-type: tm+mt
source-wordcount: '1336'
ht-degree: 1%

---

# Gérer l’accès des utilisateurs et utilisatrices via les autorisations {#manage-user-access}

{{limited-availability-release-note}}

Gérez les autorisations et l’accès des utilisateurs et utilisatrices à des composants individuels dans Adobe Real-Time CDP Collaboration via l’interface Experience Cloud [Autorisations](https://experienceleague.adobe.com/en/docs/experience-platform/access-control/abac/permissions-ui/browse){target="_blank"}. Les autorisations permettent aux administrateurs et administratrices système et produit de définir des [rôles](./manage-roles.md) afin de gérer l’accès des utilisateurs et utilisatrices à des fonctionnalités et ressources spécifiques.

## Configuration de l&#39;accès aux autorisations {#permissions-access}

Pour accéder aux autorisations, vous devez disposer d’un accès administrateur de produit et d’un accès utilisateur au produit Adobe Experience Platform. Un administrateur système est requis pour configurer les privilèges d’administrateur de produit, tandis que les privilèges d’utilisateur peuvent être configurés par un administrateur système ou de produit. Pour plus d’informations sur les rôles administratifs, consultez le guide [hiérarchie du contrôle d’accès](./overview.md#hierarchy).

>[!TIP]
>
>Tout au long de ce guide, un **administrateur** se réfère à **administrateurs système et administrateurs de produit**.

### Administrateurs système : configuration de l’accès administrateur de produit {#admin-access}

Accordez à un utilisateur ou une utilisatrice l’accès administrateur de produit pour lui donner des capacités administratives au sein du produit Experience Platform par le biais des étapes suivantes :

>[!IMPORTANT]
>
>En tant qu’administrateur système, vous disposez d’un accès prêt à l’emploi à des produits Experience Cloud spécifiques, tels que Adobe Admin Console. Toutefois, pour utiliser les autorisations, vous devez vous accorder un accès administrateur de produit et utilisateur au produit Experience Platform. Suivez le guide détaillé ci-dessous pour vous accorder l’accès en tant qu’administrateur système.

Connectez-vous à [Adobe Experience Cloud](https://experience.adobe.com/){target="_blank"} à l&#39;aide de vos identifiants. La vue d’accueil s’affiche avec une liste de vos produits disponibles dans la section **[!UICONTROL Accès rapide]**. Sélectionnez lʼ&#x200B;**[!UICONTROL Admin Console]**.

![Vue d’accueil d’Experience Cloud avec Admin Console mis en surbrillance.](../../assets/permissions/experience-cloud.png){zoomable="yes"}

Le tableau de bord de présentation de [Adobe Admin Console](https://adminconsole.adobe.com/) s&#39;affiche. Sélectionnez **[!UICONTROL Adobe Experience Platform]** dans la liste **[!UICONTROL Produits]** sous **[!UICONTROL Produits et services]**.

![Tableau de bord de présentation d’Admin Console avec le produit Adobe Experience Platform mis en surbrillance.](../../assets/permissions/admin-console.png){zoomable="yes"}

Le tableau de bord Adobe Experience Platform s’affiche. Sélectionnez l’onglet **[!UICONTROL Administrateurs]** puis sélectionnez **[!UICONTROL Ajouter un administrateur]**.

Tableau de bord du produit ![Adobe Experience Platform avec l’onglet Administrateurs sélectionné et Ajouter un administrateur en surbrillance.](../../assets/permissions/add-admin.png){zoomable="yes"}

La boîte de dialogue **[!UICONTROL Ajouter des administrateurs de produit]** s’affiche. Saisissez l’adresse e-mail ou le nom d’utilisateur dans le champ de texte **[!UICONTROL E-mail ou nom d’utilisateur]**, puis sélectionnez le compte approprié dans la liste déroulante. Sélectionnez **[!UICONTROL Enregistrer]** pour terminer l’ajout de l’utilisateur en tant qu’administrateur de produit.

![La boîte de dialogue Ajouter des administrateurs de produit avec les informations d’utilisateur renseignées et l’option Enregistrer sélectionnée.](../../assets/permissions/add-product-administrators.png){zoomable="yes"}

L’utilisateur dispose désormais des privilèges d’administrateur de produit et peut effectuer des fonctions administratives, comme ajouter des utilisateurs ou d’autres administrateurs au produit dans Admin Console. Ils auront ensuite besoin d’un accès utilisateur au produit Experience Platform pour accéder et exécuter des fonctions dans le cadre des autorisations.

### Administrateurs : configuration de l’accès des utilisateurs à Experience Platform {#user-access}

Maintenant que vous avez accordé à l’utilisateur ou à l’utilisatrice un accès d’administrateur de produit, vous devez lui fournir un accès d’utilisateur au produit Experience Platform. Dans le cadre des configurations d’accès, vous affecterez des [profils de produit](https://helpx.adobe.com/fr/enterprise/using/manage-product-profiles.html) spécifiques à l’utilisateur.

>[!TIP]
>
>Si vous procédez comme indiqué dans la section précédente, vous vous trouvez déjà dans la catégorie Adobe Experience Platform et vous pouvez ignorer la première étape.

Accédez à [Admin Console](https://adminconsole.adobe.com/){target="_blank"} et sélectionnez **[!UICONTROL Adobe Experience Platform]** dans la liste **[!UICONTROL Produits]** sous **[!UICONTROL Produits et services]**.

![Vue d’accueil d’Experience Cloud avec Admin Console mis en surbrillance.](../../assets/permissions/experience-cloud.png){zoomable="yes"}

Sélectionnez l’onglet **[!UICONTROL Utilisateurs]** puis sélectionnez **[!UICONTROL Ajouter des utilisateurs]**.

Tableau de bord du produit ![Adobe Experience Platform avec l’onglet Utilisateurs sélectionné et Ajouter des utilisateurs en surbrillance.](../../assets/permissions/add-users.png){zoomable="yes"}

La boîte de dialogue **[!UICONTROL Ajouter des utilisateurs à ce produit]** s’affiche. Saisissez le nom ou l’adresse e-mail de l’utilisateur dans le champ de texte **[!UICONTROL Nom, groupe d’utilisateurs ou adresse e-mail]**, puis sélectionnez le compte approprié dans la liste déroulante. Sélectionnez ensuite l’option d’ajout **[!UICONTROL Produits]**.

![La boîte de dialogue Ajouter des utilisateurs à ce produit avec des informations d’utilisateur renseignées et l’option Ajouter des produits sélectionnée.](../../assets/permissions/add-users-to-product.png){zoomable="yes"}

La boîte de dialogue **[!UICONTROL Sélectionner des profils de produit]** s’affiche. Sélectionnez **[!UICONTROL AEP-Default-All-Users]** et **[!UICONTROL Default Production All Access]** puis sélectionnez **[!UICONTROL Appliquer]**.

![La boîte de dialogue Sélectionner des profils de produit avec les options AEP-Default-All-Users et Tous les accès de production par défaut sélectionnées et Appliquer en surbrillance.](../../assets/permissions/select-product-profiles.png){zoomable="yes"}

Vérifiez que les informations sont correctes, puis sélectionnez **[!UICONTROL Enregistrer]**.

![La boîte de dialogue Ajouter des utilisateurs aux produits avec les informations sur les utilisateurs et les profils de produit affichés et Enregistrer en surbrillance.](../../assets/permissions/save-selections.png){zoomable="yes"}

L’utilisateur doit maintenant disposer d’un accès administrateur de produit et de produit à Experience Platform, lui permettant ainsi d’accéder aux autorisations. Ensuite, vous devez attribuer à l’utilisateur deux rôles fondamentaux pour lui donner accès à l’interface utilisateur d’Experience Platform.

### Administrateurs : configurer l’accès à l’interface utilisateur d’Experience Platform {#product-access}

Dans Real-Time CDP Collaboration, les administrateurs et les utilisateurs finaux utiliseront les données d’Experience Platform, telles que les audiences et les journaux d’audit. Ces données sont conservées dans des instances d’Experience Platform appelées sandbox. Pour que les utilisateurs puissent interagir avec ces données, vous devez affecter des [rôles par défaut](https://experienceleague.adobe.com/en/docs/experience-platform/access-control/home#default-roles){target="_blank"} à l’utilisateur.

Pour commencer, accédez à [Adobe Experience Cloud](https://experience.adobe.com/). Vous devriez maintenant voir **[!UICONTROL Experience Platform]** et **[!UICONTROL Autorisations]** dans **[!UICONTROL Accès rapide]**.

![Vue d’accueil d’Experience Cloud avec Experience Platform et autorisations mises en surbrillance.](../../assets/permissions/experience-cloud-products.png){zoomable="yes"}

>[!NOTE]
>
> L’accès aux produits peut prendre plusieurs minutes et vous recevrez un e-mail vous informant que vous y avez accès. Si vous ne voyez pas Experience Platform ou Autorisations dans Adobe Experience Cloud après avoir reçu l’e-mail, déconnectez-vous, puis reconnectez-vous à votre compte.

À ce stade, vous pouvez désormais accéder à **[!UICONTROL Autorisations]**. Si vous tentez d’accéder à **[!UICONTROL Experience Platform]**, un avertissement s’affiche indiquant qu’aucun sandbox n’est activé, comme illustré ci-dessous. Pour résoudre ce problème, vous devez affecter les rôles par défaut à votre utilisateur. Pour commencer, sélectionnez **[!UICONTROL Autorisations]**.

![Affichage de l’accueil d’Experience Cloud avec un avertissement affiché et les autorisations mises en surbrillance.](../../assets/permissions/experience-cloud-warning.png){zoomable="yes"}

Le tableau de bord **[!UICONTROL Autorisations]** s’affiche. Sélectionnez **Utilisateurs** dans le panneau de gauche, puis sélectionnez le nom de l’utilisateur.

![Tableau de bord des autorisations avec l’espace de travail Utilisateurs affiché et un utilisateur en surbrillance.](../../assets/permissions/permissions-user.png){zoomable="yes"}

Sélectionnez l’onglet **[!UICONTROL Rôles]** puis sélectionnez **[!UICONTROL Ajouter des rôles]**.

![Espace de travail de l’utilisateur avec l’onglet Rôles affiché et Ajouter des rôles en surbrillance.](../../assets/permissions/user-roles.png){zoomable="yes"}

La boîte de dialogue **[!UICONTROL Ajouter des rôles]** s’affiche. Sélectionnez **[!UICONTROL Tous les accès de production par défaut]** et **[!UICONTROL Administrateurs Sandbox]**, puis sélectionnez **[!UICONTROL Enregistrer]**.

![La boîte de dialogue Ajouter des rôles avec les Administrateurs d’accès Tous les environnements de production et Sandbox par défaut sélectionnés et Enregistrer en surbrillance.](../../assets/permissions/add-roles.png){zoomable="yes"}

Vous avez désormais accès à Experience Platform et aux autorisations. Lors de la dernière étape, vous allez accorder l’accès à Real-Time CDP Collaboration.

### Administrateurs : configuration de l’accès à Real-Time CDP Collaboration {#RTCDP-collaboration-access}

Pour accorder aux utilisateurs l’accès à Collaboration, vous allez utiliser un concept de contrôle d’accès appelé rôles. Les rôles définissent le niveau d’accès d’un administrateur ou d’un utilisateur aux [ressources](https://experienceleague.adobe.com/en/docs/experience-platform/access-control/home#permissions) de votre organisation.

Lors de la configuration de l&#39;accès individuel à Collaboration, vous attribuerez aux utilisateurs des rôles contenant des autorisations provenant de la ressource Collaborations. Vous pouvez utiliser le guide [gérer les rôles](./manage-roles.md) pour obtenir des informations sur :

- les [deux rôles standard](./manage-roles.md#standard-roles) et les niveaux d’accès qu’ils accordent à Collaboration
- création de [rôles personnalisés](./manage-roles.md#specific-access-roles) à l’aide de la ressource Collaboration
- la liste des autorisations incluses dans la ressource Collaborations

>[!NOTE]
>
>En outre, un utilisateur doit être affecté à un rôle contenant l’autorisation **[!UICONTROL Prod]** dans les ressources **[!UICONTROL Sandbox]**. Les deux rôles standard contiennent cette autorisation. Si vous choisissez d’attribuer à un utilisateur un rôle personnalisé au lieu d’un rôle standard, vous devez vous assurer que l’un des rôles qui lui sont attribués contient cette autorisation.

Une fois que vous avez choisi ou créé un rôle qui englobe le niveau d’accès dont votre utilisateur a besoin, vous devez affecter l’utilisateur à ce rôle.

#### Attribuer un rôle

Vous pouvez affecter plusieurs rôles à un seul utilisateur ou affecter plusieurs utilisateurs à un seul rôle. Le premier cas a été abordé précédemment lors de l’[affectation des rôles par défaut](#product-access) pour donner à un utilisateur l’accès à Experience Platform. Dans les étapes suivantes, vous affecterez directement des utilisateurs au rôle que vous avez sélectionné.

Dans **[!UICONTROL Autorisations]** sélectionnez **[!UICONTROL Rôles]** dans le panneau de gauche, puis sélectionnez votre rôle dans la liste.

![Tableau de bord des autorisations avec l’espace de travail Rôles affiché et un rôle en surbrillance.](../../assets/permissions/select-role.png){zoomable="yes"}

La page de détails du rôle s’affiche. Sélectionnez l’onglet **[!UICONTROL Utilisateurs]** puis sélectionnez **[!UICONTROL Ajouter des utilisateurs]**.

![Espace de travail détaillé du rôle avec l’onglet Utilisateurs affiché et Ajouter des utilisateurs en surbrillance.](../../assets/permissions/role-users.png){zoomable="yes"}

La boîte de dialogue **[!UICONTROL Ajouter des utilisateurs]** s’affiche. Sélectionnez le ou les utilisateurs dans la liste, puis sélectionnez **[!UICONTROL Enregistrer]**.

![La boîte de dialogue Ajouter des utilisateurs avec une sélection d’utilisateurs et l’option Enregistrer mise en surbrillance.](../../assets/permissions/add-users-to-role.png){zoomable="yes"}

L’utilisateur doit maintenant voir **[!UICONTROL RTCDP Collaboration]** répertorié en tant que produit sous **[!UICONTROL Accès rapide]** dans Experience Cloud.

![Experience Cloud avec RTCDP Collaboration mis en surbrillance sous Accès rapide](../../assets/permissions/rtcdp-experience-cloud.png)

## Étapes suivantes

Maintenant que les utilisateurs ont accès à Real-Time CDP Collaboration, ils peuvent commencer à utiliser le produit. Pour en savoir plus sur le produit dans son ensemble, consultez le [guide de présentation](../home.md).
