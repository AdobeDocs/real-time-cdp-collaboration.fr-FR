---
title: Configuration de Adobe Experience Platform en tant que destination
description: Découvrez comment configurer et gérer Adobe Experience Platform en tant que destination dans Real-Time CDP Collaboration.
audience: admin, publisher, advertiser
badgelimitedavailability: label="Disponibilité limitée" type="Informative" url="https://helpx.adobe.com/fr/legal/product-descriptions/real-time-customer-data-platform-collaboration.html newtab=true"
exl-id: 594610a0-9102-448a-b59b-ec162ef9dd57
source-git-commit: b79fad9257cfe2aafd27b81346ca45a00fcfdf76
workflow-type: tm+mt
source-wordcount: '878'
ht-degree: 11%

---

# Configuration de Adobe Experience Platform en tant que destination

{{limited-availability-release-note}}

Configurez cette destination pour activer les audiences de votre projet vers Adobe Experience Platform. L’activation des audiences dans Adobe Experience Platform vous permet d’exploiter les fonctionnalités de la plateforme en matière de segmentation, d’analyse et d’activation des audiences sur divers canaux marketing. Pour en savoir plus sur Adobe Experience Platform, consultez la présentation d’[Experience Platform](https://experienceleague.adobe.com/fr/docs/experience-platform/landing/home){target="_blank"}.

>[!NOTE]
>
>Actuellement, seuls les éditeurs peuvent configurer des destinations dans Real-Time CDP Collaboration.

## Configurer la destination {#configure-destination}

Pour configurer Adobe Experience Platform en tant que destination, accédez à **[!UICONTROL Configuration]** puis sélectionnez l’onglet **[!UICONTROL Destinations]**. Sélectionnez **[!UICONTROL Configurer]** pour Adobe Experience Platform.

![L’espace de travail Mes destinations avec l’option Configurer mise en surbrillance pour la destination Adobe Experience Platform.](/help/assets/destinations/adobe-experience-platform/setup-aep.png)

Le workflow **[!UICONTROL Créer une destination]** s’affiche.

![Workflow Créer une destination pour Adobe Experience Platform.](/help/assets/destinations/adobe-experience-platform/create-destination.png)

### Configurer le sandbox {#configure-sandbox}

>[!CONTEXTUALHELP]
>id="rtcdp_collaboration_destinations_audience_expiration"
>title="Expiration de l’audience"
>abstract="Période au bout de laquelle l’audience ne sera plus disponible dans Adobe Experience Platform. L’expiration par défaut est de 30 jours, mais vous pouvez la définir sur une valeur comprise entre 1 et 30 jours."

Tout d’abord, vous devez sélectionner le sandbox dans lequel vos données d’audience seront envoyées.

>
>
>Vous pouvez uniquement sélectionner un sandbox auquel votre utilisateur a accès. Par défaut, tous les utilisateurs de Real-Time CDP Collaboration ont accès au sandbox **Prod**. Pour accéder à d’autres sandbox, un administrateur doit ajouter des sandbox supplémentaires à un rôle affecté à votre utilisateur. Pour plus d’informations sur la gestion des rôles, consultez le guide [gérer les rôles](../permissions/manage-roles.md).

Dans la section **[!UICONTROL Configurer le sandbox]**, sélectionnez la liste déroulante **[!UICONTROL Sandbox]** ou saisissez le nom d’un sandbox.

![Liste déroulante Sandbox mise en surbrillance dans le workflow Créer la destination.](/help/assets/destinations/adobe-experience-platform/select-sandbox.png)

Vous pouvez également sélectionner **[!UICONTROL Parcourir le sandbox]** pour afficher tous les sandbox disponibles, ainsi que leur **[!UICONTROL Type]**, **[!UICONTROL Statut]** et **[!UICONTROL Région]**. Sélectionnez le sandbox à utiliser, puis sélectionnez **[!UICONTROL Enregistrer]**.

Configurez ensuite l’**[!UICONTROL Expiration de l’audience]**. Par défaut, l’expiration de l’audience est définie sur 30 jours. Vous pouvez choisir de définir l’expiration sur une période comprise entre 1 et 30 jours. Après la date d’expiration, l’audience ne sera plus disponible dans Adobe Experience Platform.

![Section Expiration de l’audience mise en surbrillance dans le workflow Créer une destination.](/help/assets/destinations/adobe-experience-platform/audience-expiration.png)

### Créer un mappage d’activation {#create-activation-mapping}

>[!CONTEXTUALHELP]
>id="rtcdp_collaboration_destinations_activation_matchkeys"
>title="Clés de correspondance d’activation"
>abstract="Les clés de correspondance d’activation s’affichent en fonction des clés de correspondance que vous avez sélectionnées lors de la création de votre organisation."

>[!CONTEXTUALHELP]
>id="rtcdp_collaboration_destinations_target_namespaces"
>title="Espaces de noms cibles"
>abstract="Les espaces de noms cibles spécifient l’espace de noms d’identité auquel la clé de correspondance sera mappée dans Adobe Experience Platform. Les clés de correspondance hachées doivent être mappées à un espace de noms cible qui prend en charge les valeurs hachées."

Vous devez ensuite créer un mappage d’activation pour définir comment les données d’audience seront envoyées à Adobe Experience Platform. Vous pouvez mapper chaque clé [correspondance](../setup/onboard-organization.md#set-up-match-keys) sélectionnée lors de la création de votre organisation à un espace de noms cible. Les espaces de noms cibles spécifient l’[espace de noms d’identité](https://experienceleague.adobe.com/fr/docs/experience-platform/identity/features/namespaces#standard){target="_blank"} auquel la clé de correspondance sera mappée dans Adobe Experience Platform.

>
>
>Les clés de correspondance hachées doivent être mappées à un espace de noms cible qui prend en charge les valeurs hachées. Par exemple, la clé de correspondance **[!UICONTROL E-mail haché]** doit être mappée à l’espace de noms d’identité **[!UICONTROL E-mail(SHA256, en minuscules)]** dans Adobe Experience Platform. Vous ne pouvez pas mapper la clé de correspondance **[!UICONTROL E-mail haché]** à l’espace de noms d’identité **[!UICONTROL E-mail]**, car cet espace de noms ne prend pas en charge les valeurs hachées.

Sélectionnez le champ **[!UICONTROL Espaces de noms cibles]** en regard de chaque clé de correspondance. La boîte de dialogue **[!UICONTROL Sélectionner le champ source]** s’affiche. Recherchez l’espace de noms cible dans la liste ou recherchez un espace de noms spécifique. Sélectionnez l’espace de noms cible à utiliser pour la clé de correspondance, puis sélectionnez **[!UICONTROL Sélectionner]**.

![La boîte de dialogue Sélectionner le champ source avec l’option Sélectionner mise en surbrillance](/help/assets/destinations/adobe-experience-platform/select-target-namespace.png)

Une fois que vous avez terminé de mapper toutes les clés de correspondance, passez en revue vos paramètres, puis sélectionnez **[!UICONTROL Créer]** pour terminer la création de la destination.

## Utilisation de Adobe Experience Platform en tant que destination

Une fois que vous avez configuré Adobe Experience Platform en tant que destination, vous pouvez commencer [à activer les audiences](../collaborate/activate.md) à la plateforme par le biais de vos projets. Actuellement, le processus d’activation est un processus en une seule étape lancé par l’annonceur. Lorsque l’annonceur active une audience, elle est envoyée à la destination préconfigurée de l’éditeur (dans ce cas, Adobe Experience Platform). L’éditeur n’a pas besoin de prendre d’autres mesures pour envoyer l’audience à la destination.

>[!IMPORTANT]
>
>Vous **devez** configurer Adobe Experience Platform en tant que destination *avant* que votre collaborateur active une audience. Si la destination n’est pas configurée, l’audience vous sera envoyée et visible dans l’onglet **[!UICONTROL Activer]** au sein d’un projet, mais elle ne sera pas activée dans Adobe Experience Platform.

Une fois l’audience activée, elle est disponible dans [Audience Portal](#audience-portal) dans Experience Platform avec Real-Time CDP Collaboration comme origine.  Ces audiences peuvent ensuite être utilisées dans les campagnes et l’engagement des clients.

### Audience Portal {#audience-portal}

Maintenant que vous avez configuré Adobe Experience Platform en tant que destination, vous pouvez afficher les audiences activées dans le portail d’audiences. Audience Portal est un hub central de Adobe Experience Platform qui vous permet d’afficher et de gérer vos audiences. Audience Portal fournit désormais Real-Time CDP Collaboration comme origine lors du filtrage de vos audiences.

>[!IMPORTANT]
>
>Il vous incombe d’appliquer les libellés d’utilisation des données nécessaires aux audiences que vous activez dans Adobe Experience Platform. Pour plus d’informations, consultez le guide [libellés d’utilisation des données](https://experienceleague.adobe.com/fr/docs/experience-platform/data-governance/labels/overview){target="_blank"}.

![Audience Portal avec Real-Time CDP Collaboration comme origine dans les options de filtrage.](/help/assets/destinations/adobe-experience-platform/audience-portal.png)

Pour en savoir plus sur Audience Portal, consultez le guide [Présentation d’Audience Portal](https://experienceleague.adobe.com/fr/docs/experience-platform/segmentation/ui/audience-portal#manage-audiences){target="_blank"}.
