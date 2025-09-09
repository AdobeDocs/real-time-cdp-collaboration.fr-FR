---
title: Configuration de Adobe Experience Platform en tant que destination
description: Découvrez comment configurer et gérer Adobe Experience Platform en tant que destination dans Real-Time CDP Collaboration.
audience: admin, publisher, advertiser
badgelimitedavailability: label="Disponibilité limitée" type="Informative" url="https://helpx.adobe.com/fr/legal/product-descriptions/real-time-customer-data-platform-collaboration.html newtab=true"
exl-id: 594610a0-9102-448a-b59b-ec162ef9dd57
source-git-commit: 6acf936f50b412147578a70e2369b06c53260f06
workflow-type: tm+mt
source-wordcount: '1487'
ht-degree: 6%

---

# Configuration de Adobe Experience Platform en tant que destination

{{limited-availability-release-note}}

Configurez cette destination pour activer les audiences de votre projet vers Adobe Experience Platform. L’activation des audiences dans Adobe Experience Platform vous permet d’exploiter les fonctionnalités de la plateforme en matière de segmentation, d’analyse et d’activation des audiences sur divers canaux marketing. Pour en savoir plus sur Adobe Experience Platform, consultez la présentation d’[Experience Platform](https://experienceleague.adobe.com/fr/docs/experience-platform/landing/home){target="_blank"}.

>[!WARNING]
>
>Vous ne pouvez pas mettre à jour une destination après sa création. Si vous devez modifier des paramètres, vous devez supprimer la destination existante et en créer une nouvelle.

## Configurer la destination {#configure-destination}

Pour configurer Adobe Experience Platform en tant que destination, accédez à **[!UICONTROL Configuration]** puis sélectionnez l’onglet **[!UICONTROL Mes destinations]**. Sélectionnez **[!UICONTROL Configurer]** pour Adobe Experience Platform.

![L’espace de travail Mes destinations avec l’option Configurer mise en surbrillance pour la destination Adobe Experience Platform.](/help/assets/destinations/adobe-experience-platform/setup-aep.png)

Le workflow **[!UICONTROL Créer une destination]** s’affiche.

![Workflow Créer une destination pour Adobe Experience Platform.](/help/assets/destinations/adobe-experience-platform/create-destination.png)

### Configurer le sandbox {#configure-sandbox}

>[!CONTEXTUALHELP]
>id="rtcdp_collaboration_destinations_audience_expiration"
>title="Expiration de l’audience"
>abstract="Période au bout de laquelle l’audience ne sera plus disponible dans Adobe Experience Platform. L’expiration par défaut est de 30 jours, mais vous pouvez la définir sur une valeur comprise entre 1 et 30 jours."

Tout d’abord, vous devez sélectionner le sandbox dans lequel vos données d’audience seront envoyées.

>[!IMPORTANT]
>
>Vous pouvez uniquement sélectionner un sandbox auquel votre utilisateur a accès. Par défaut, tous les utilisateurs de Collaboration ont accès au sandbox **Prod**. Pour accéder à d’autres sandbox, un administrateur doit ajouter des sandbox supplémentaires à un rôle affecté à votre utilisateur. Pour plus d’informations sur la gestion des rôles, consultez le guide [gérer les rôles](../permissions/manage-roles.md).

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

Toutes les clés de correspondance activées pour votre compte sont incluses par défaut dans le mappage d’activation. Si vous ne souhaitez pas mapper directement une clé de correspondance à un espace de noms cible, vous pouvez utiliser l’option de clé liée pour la remplacer par une clé de correspondance différente. Pour plus d’informations sur les clés liées, consultez la [section ci-dessous](#linked-keys).

#### Mappage des espaces de noms cibles {#map-target-namespaces}

Pour mapper chaque clé de correspondance à un espace de noms cible, sélectionnez le champ **[!UICONTROL Espaces de noms cibles]** en regard de la clé de correspondance. La boîte de dialogue **[!UICONTROL Sélectionner le champ source]** s’affiche. Recherchez l’espace de noms cible dans la liste ou recherchez un espace de noms spécifique. Sélectionnez l’espace de noms cible à utiliser pour la clé de correspondance, puis sélectionnez **[!UICONTROL Sélectionner]**.

>[!IMPORTANT]
>
>Les clés de correspondance hachées doivent être mappées à un espace de noms cible qui prend en charge les valeurs hachées. Par exemple, la clé de correspondance **[!UICONTROL E-mail haché]** doit être mappée à l’espace de noms d’identité **[!UICONTROL E-mail(SHA256, en minuscules)]** dans Adobe Experience Platform. Vous ne pouvez pas mapper la clé de correspondance **[!UICONTROL E-mail haché]** à l’espace de noms d’identité **[!UICONTROL E-mail]**, car cet espace de noms ne prend pas en charge les valeurs hachées.

![La boîte de dialogue Sélectionner le champ source avec l’option Sélectionner mise en surbrillance](/help/assets/destinations/adobe-experience-platform/select-target-namespace.png)

Répétez ce processus pour chaque clé de correspondance que vous souhaitez inclure dans le mappage d’activation. Si vous ne souhaitez pas inclure de clé de correspondance, vous pouvez la supprimer ou utiliser l’option de clé liée pour la remplacer par une autre clé de correspondance.

#### Clés liées {#linked-keys}

>[!CONTEXTUALHELP]
>id="rtcdp_collaboration_destinations_linked_key"
>title="Clé liée"
>abstract="Les clés liées vous permettent de spécifier qu’une clé de correspondance différente doit être utilisée à la place de la clé de correspondance d’origine lors de l’activation. Pour qu’un profil soit activé, il doit avoir des valeurs pour la clé de correspondance d’origine et la clé de correspondance liée."

Les clés liées vous permettent de spécifier qu’une clé de correspondance différente doit être utilisée à la place de la clé de correspondance d’origine lors de l’activation. Pour mieux comprendre le fonctionnement des clés liées, prenons l’exemple suivant :

Un retailer souhaite envoyer les données en cours d’activation à Experience Platform vers son système CRM. Le retailer a activé l’adresse IP hachée comme clé de correspondance pour le compte afin d’augmenter le taux de correspondance lors de l’activation des audiences. Cependant, le système CRM de retailer ne prend pas en charge l’adresse IP hachée comme espace de noms d’identité. Ils souhaitent donc utiliser la clé de correspondance d’identifiant CRM à la place lors de l’activation des audiences dans Experience Platform. Le retailer peut utiliser l’option de clé liée pour activer des audiences vers Experience Platform à l’aide de l’identifiant CRM au lieu de l’adresse IP hachée.

>[!NOTE]
>
>Pour qu’un profil soit activé, il doit avoir des valeurs pour la clé de correspondance d’origine et la clé de correspondance liée. Par exemple, si l’ID haché est lié à un ID CRM, un profil doit posséder des valeurs pour que l’ID haché et l’ID CRM soient activés l’un et l’autre. Si l’une des valeurs est manquante, le profil ne sera pas activé.

Pour utiliser une clé liée, activez/désactivez l’option **[!UICONTROL Clé liée]** en regard de la clé de correspondance que vous souhaitez utiliser à sa place. La section **[!UICONTROL Clé liée]** s’affiche et vous demande de créer le mappage.

![L’option Clé liée et la section mises en surbrillance dans le workflow Créer la destination.](/help/assets/destinations/adobe-experience-platform/linked-key.png)

Sélectionnez la **[!UICONTROL clé liée]** à utiliser dans le menu déroulant. En suivant l’exemple ci-dessus, le retailer sélectionnerait **[!UICONTROL ID CRM]** comme clé liée.

![Liste déroulante Clé liée mise en surbrillance dans le workflow Créer une destination.](/help/assets/destinations/adobe-experience-platform/select-linked-key.png)

Vous devez ensuite spécifier l’espace de noms cible de la clé liée si vous ne l’avez pas déjà fait. Si vous avez déjà sélectionné l’espace de noms cible pour la clé de correspondance dans la section **[!UICONTROL Créer un mapping d’activation]** , celui-ci sera automatiquement renseigné. Si vous n’avez pas encore sélectionné d’espace de noms cible pour la clé liée, vous pouvez le faire maintenant.

Sélectionnez le champ **[!UICONTROL Espaces de noms cibles]** en regard de la clé liée. La boîte de dialogue **[!UICONTROL Sélectionner le champ source]** s’affiche. Recherchez l’espace de noms cible dans la liste ou recherchez un espace de noms spécifique. Sélectionnez l’espace de noms cible à utiliser pour la clé liée, puis sélectionnez **[!UICONTROL Sélectionner]**.

![Boîte de dialogue Sélectionner le champ source.](/help/assets/destinations/adobe-experience-platform/select-linked-key-target-namespace.png)

La clé liée est maintenant configurée.

>[!NOTE]
>
>Vous ne pouvez utiliser qu’un seul espace de noms cible de clé liée par mapping d’activation. Par exemple, si vous liez l’ID haché à l’ID CRM, le fait d’activer l’option de clé liée pour un autre champ le liera également à l’ID CRM.

Lorsque vous avez terminé de mapper toutes les clés de correspondance, vérifiez vos paramètres. La section **[!UICONTROL Aperçu]** fournit un résumé de votre configuration.

![Section Aperçu du workflow Créer une destination.](/help/assets/destinations/adobe-experience-platform/preview.png)

>[!IMPORTANT]
>
>Actuellement, chaque clé de correspondance est activée pour Experience Platform en tant qu’audience distincte. Par exemple, si vous avez [!UICONTROL E-mail haché] et [!UICONTROL Téléphone haché] comme clés de correspondance, deux audiences distinctes sont créées dans Audience Portal lorsqu’une audience est activée.

Lorsque votre configuration vous convient, sélectionnez **[!UICONTROL Créer une destination]**. Un message de confirmation s’affiche indiquant que la destination a été créée avec succès.

## Utilisation de Adobe Experience Platform en tant que destination

Une fois que vous avez configuré Experience Platform en tant que destination, vous pouvez commencer [l’activation des audiences](../collaborate/activate.md) à la plateforme par le biais de vos projets. Actuellement, le processus d’activation est un processus en une seule étape initié par le collaborateur. Par exemple, lorsqu’un annonceur active une audience, elle est envoyée à la destination préconfigurée de l’éditeur (Experience Platform). L’éditeur n’a pas besoin de prendre d’autres mesures pour envoyer l’audience à la destination. Il en va de même pour le modèle de collaboration de marque à marque.

>[!IMPORTANT]
>
>Vous **devez** configurer Experience Platform en tant que destination *avant* que votre collaborateur active une audience. Si la destination n’est pas configurée, l’audience vous sera envoyée et visible dans l’onglet **[!UICONTROL Activer]** au sein d’un projet, mais elle ne sera pas activée dans Experience Platform.

Une fois l’audience activée, elle est disponible dans [Audience Portal](#audience-portal) dans Experience Platform avec Real-Time CDP Collaboration comme origine.  Ces audiences peuvent ensuite être utilisées dans les campagnes et l’engagement des clients.

### Audience Portal {#audience-portal}

Maintenant que vous avez configuré Adobe Experience Platform en tant que destination, vous pouvez afficher les audiences activées dans le portail d’audiences. Audience Portal est un hub central de Adobe Experience Platform qui vous permet d’afficher et de gérer vos audiences. Audience Portal fournit désormais Real-Time CDP Collaboration comme origine lors du filtrage de vos audiences.

>[!IMPORTANT]
>
>Il vous incombe d’appliquer les libellés d’utilisation des données nécessaires aux audiences que vous activez dans Adobe Experience Platform. Pour plus d’informations, consultez le guide [libellés d’utilisation des données](https://experienceleague.adobe.com/fr/docs/experience-platform/data-governance/labels/overview){target="_blank"}.

![Audience Portal avec Real-Time CDP Collaboration comme origine dans les options de filtrage.](/help/assets/destinations/adobe-experience-platform/audience-portal.png)

Pour en savoir plus sur Audience Portal, consultez le guide [Présentation d’Audience Portal](https://experienceleague.adobe.com/fr/docs/experience-platform/segmentation/ui/audience-portal#manage-audiences){target="_blank"}.
