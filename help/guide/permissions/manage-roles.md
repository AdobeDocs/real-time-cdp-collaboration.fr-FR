---
title: Gérer les rôles via les autorisations
description: Découvrez toutes les ressources de rôle disponibles qui permettent d’accéder aux différents composants dans l’interface utilisateur de Real-Time CDP Collaboration.
audience: admin
badgelimitedavailability: label="Disponibilité limitée" type="Informative" url="https://helpx.adobe.com/legal/product-descriptions/real-time-customer-data-platform-collaboration.html newtab=true"
exl-id: 59cf5bf2-421b-4ebc-beab-30eafb098649
source-git-commit: dd1386f9371cb40285315d11e07b139d3115e147
workflow-type: tm+mt
source-wordcount: '584'
ht-degree: 1%

---

# Gérer les rôles {#manage-roles}

{{limited-availability-release-note}}

Pour gérer l’accès des utilisateurs et utilisatrices aux différents composants de l’interface utilisateur de Real-Time CDP Collaboration, un [administrateur](./manage-user-access.md#system-admin-gain-access) peut définir et affecter des rôles. Les rôles définissent l’accès d’un administrateur ou d’un utilisateur aux [ressources](https://experienceleague.adobe.com/en/docs/experience-platform/access-control/home#permissions){target="_blank"} de votre organisation. Ce guide fournit des informations sur les rôles standard fournis dans Real-Time CDP Collaboration, ainsi que sur les autorisations individuelles que vous pouvez attribuer aux rôles personnalisés.

Pour commencer à gérer les rôles, un administrateur doit avoir accès au produit Experience Platform. Pour plus d’informations sur l’obtention d’un accès administratif ou sur l’obtention de l’accès à Experience Platform, consultez le guide [gérer l’accès utilisateur](./manage-user-access.md#manage-user-access-through-permissions).

## Rôles standard {#standard-roles}

Deux rôles standard vous sont fournis, lesquels remplissent deux cas d’utilisation courants de contrôle d’accès. Il s’agit de rôles « en lecture seule », ce qui signifie qu’ils ne peuvent pas être personnalisés.

| Nom du rôle | Description du rôle | Autorisations |
| --- | --- | --- | 
| Responsables Collaboration | Il s’agit d’une autorisation d’accès complet, contenant les 15 autorisations. Cela permet à l’utilisateur de lire, créer et modifier toutes les données. Il permet également d’accéder au sandbox **[!UICONTROL Prod]** dans Experience Platform, ce qui vous permet d’importer des audiences dans Real-Time CDP Collaboration. | Tout cela à partir du tableau ci-dessous. |
| Visionneuses Collaboration | Il s’agit d’une autorisation d’accès en lecture seule. Un utilisateur peut lire et découvrir des données, des activités, des connexions, etc. Il permet également d’accéder au sandbox **[!UICONTROL Prod]** dans Experience Platform, ce qui vous permet d’importer des audiences dans Real-Time CDP Collaboration. | Toutes les autorisations de lecture du tableau ci-dessous. |

{style="table-layout:auto"}

## Créer des rôles d’accès spécifiques {#specific-access-roles}

Vous souhaiterez probablement créer des rôles supplémentaires pour fournir différents niveaux d’accès à différents utilisateurs. Lors de la création de rôles, vous pouvez gérer différents niveaux d&#39;accès en sélectionnant des autorisations spécifiques dans la ressource **[!UICONTROL Collaborations]**. Pour savoir comment créer et gérer des rôles, reportez-vous au guide [roles](https://experienceleague.adobe.com/en/docs/experience-platform/access-control/abac/permissions-ui/roles#create-new-role){target="_blank"}.

>[!NOTE]
> Pour accéder à Real-Time CDP Collaboration, un utilisateur ou une utilisatrice doit avoir accès au sandbox **[!UICONTROL Prod]** dans Experience Platform. Pour permettre à un utilisateur d’accéder à ce sandbox, il doit être affecté à un rôle contenant l’autorisation **[!UICONTROL Prod]** dans la ressource **[!UICONTROL Sandbox]**.

Vous trouverez ci-dessous une liste des autorisations disponibles dans la ressource Collaborations :

| Autorisation de haut niveau | Description |
| --- | --- |
| Gestion des instances Collaboration | Afficher, créer, mettre à jour et supprimer les instances de collaboration d’une organisation. Découvrez les instances de collaboration d’autres organisations. |
| Lecture des instances Collaboration | Lisez les instances de collaboration d’une organisation et découvrez les instances de collaboration d’autres organisations. |
| Gérer les invitations à la connexion | Affichez, créez et supprimez des invitations à des connexions lancées par votre organisation. Accepter et refuser l’invitation à une connexion lancée par d’autres organisations. |
| Lire les invitations de connexion | Afficher les invitations à la connexion. |
| Gérer les connexions Collaboration | Un annonceur peut afficher, créer et mettre à jour des paramètres, ainsi qu’envoyer et supprimer des connexions. Un éditeur peut afficher, accepter ou refuser des connexions. |
| Lire les connexions Collaboration | Afficher les connexions. |
| Gérer les données d’audience | Intégrez et découvrez les audiences. Mettez à jour des audiences publiques, privées et personnalisées et gérez les paramètres de métadonnées de l’inventaire des audiences. |
| Lire les données d’audience | Lire et découvrir des audiences. |
| Gérer les données de mesure | Intégrez, mettez à jour et supprimez des données de mesure. |
| Lire les données de mesure | Lire les données de mesure. |
| Gérer les projets | Affichez, créez, mettez à jour et supprimez des projets pour toutes les activités de découverte, de partage, d’activation et de mesure. |
| Lire les projets | Affichez les projets pour n’importe quelle activité de découverte, de partage, d’activation et de mesure. |
| Lire les activités utilisateur | Lire les activités utilisateur. |
| Exporter les activités utilisateur | Exporter les activités utilisateur. |
| Lire la surveillance du crédit Collaboration | Suivi du crédit au niveau de l’organisation et de l’instance. |

{style="table-layout:auto"}

## Étapes suivantes

Après avoir créé des rôles qui définissent l’accès aux collaborations Real-Time CDP, vous devez [affecter les rôles](./manage-user-access.md#assign-a-role) aux administrateurs et aux utilisateurs. Reportez-vous au guide [gestion des autorisations pour un rôle](https://experienceleague.adobe.com/en/docs/experience-platform/access-control/abac/permissions-ui/permissions) pour une présentation complète de la gestion des rôles.
