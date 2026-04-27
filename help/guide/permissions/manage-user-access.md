---
title: Gérer l’accès des utilisateurs et utilisatrices via les autorisations
description: Gérez les autorisations et l’accès des utilisateurs aux différents composants de l’interface utilisateur de Real-Time CDP Collaboration.
audience: admin
badgelimitedavailability: label="Disponibilité limitée" type="Informative" url="https://helpx.adobe.com/legal/product-descriptions/real-time-customer-data-platform-collaboration.html newtab=true"
exl-id: 0155f6a6-5e67-4415-af96-1848345842e4
TQID: https://experienceleague.adobe.com/uPFss3qIstJmeVFF1YpQQJ0V848SiDEfy6BYyEcgPZw
product_v2: id: fdddec33-c9cb-4459-b8b6-2664395a6f10
topic_v2: id: e1e0219c-f879-479f-8427-888ed2a6e9c2
source-git-commit: 3ce7e66b31332836fd6cc6137c94622436505cc9
workflow-type: tm+mt
source-wordcount: 1406
ht-degree: 2%

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

The Adobe Experience Platform dashboard displays. Select the **[!UICONTROL Admins]** tab and then select **[!UICONTROL Add admin]**.

![Adobe Experience Platform product dashboard with the Admins tab selected and Add admin highlighted.](../../assets/permissions/add-admin.png){zoomable="yes"}

The **[!UICONTROL Add product administrators]** dialog appears. Enter the user email or username into the **[!UICONTROL Email or username]** text field and then select the correct account from the dropdown. Select **[!UICONTROL Save]** to finish adding the user as a product administrator.

![The Add product administrators dialog with a users information filled in and the Save option selected.](../../assets/permissions/add-product-administrators.png){zoomable="yes"}

The user now has product administrator privileges and can perform administrative functions, such as adding users or other admins, to the product within the Admin Console. Next they&#39;ll need user access to the Experience Platform product to access and perform functions within Permissions.

### Administrators: configure user access to Experience Platform {#user-access}

Now that you&#39;ve granted the user product administrator access, you need to provide them user access to the Experience Platform product. As part of the access configurations, you&#39;ll assign the user specific [product profiles](https://helpx.adobe.com/fr/enterprise/using/manage-product-profiles.html).

>[!TIP]
>
>If you&#39;re following along from the previous section, you&#39;ll already be within the Adobe Experience Platform product and you may skip the first step.

Navigate to the [Admin Console](https://adminconsole.adobe.com/){target="_blank"} and select **[!UICONTROL Adobe Experience Platform]** from the **[!UICONTROL Products]** list under **[!UICONTROL Products and services]**.

![Vue d’accueil d’Experience Cloud avec Admin Console mis en surbrillance.](../../assets/permissions/experience-cloud.png){zoomable="yes"}

Select the **[!UICONTROL Users]** tab and then select **[!UICONTROL Add users]**.

![Adobe Experience Platform product dashboard with the Users tab selected and Add users highlighted.](../../assets/permissions/add-users.png){zoomable="yes"}

The **[!UICONTROL Add users to this product]** dialog appears. Enter the user&#39;s name or email into the **[!UICONTROL Name, user group or email address]** text field and then select the correct account from the dropdown. Next, select the **[!UICONTROL Products]** add option.

![The Add users to this product dialog with a users information filled in and the Products add option selected.](../../assets/permissions/add-users-to-product.png){zoomable="yes"}

The **[!UICONTROL Select product profiles]** dialog appears. Select **[!UICONTROL AEP-Default-All-Users]** and **[!UICONTROL Default Production All Access]** and then select **[!UICONTROL Apply]**.

![The Select product profiles dialog with the AEP-Default-All-Users and Default Production All Access options selected and Apply highlighted.](../../assets/permissions/select-product-profiles.png){zoomable="yes"}

Confirm the information is correct and then select **[!UICONTROL Save]**.

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

### Administrateurs et administratrices : configurer l’accès à la Collaboration Real-Time CDP {#RTCDP-collaboration-access}

>[!CONTEXTUALHELP]
>id="rtcdp_collaboration_organization_permissions"
>title="guide de gestion des accès utilisateur"
>abstract=""

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
