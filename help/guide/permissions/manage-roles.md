---
title: Gérer les rôles via les autorisations
description: Comprendre toutes les ressources de rôle disponibles qui permettent d’accéder aux différents composants de l’interface utilisateur de collaboration CDP en temps réel.
audience: admin
badgelimitedavailability: label="Disponibilité limitée" type="Informative" url="https://helpx.adobe.com/legal/product-descriptions/real-time-customer-data-platform-collaboration.html newtab=true"
exl-id: 59cf5bf2-421b-4ebc-beab-30eafb098649
source-git-commit: 56872a2cd91ae040aba51ed5784c86b055f88756
workflow-type: tm+mt
source-wordcount: '584'
ht-degree: 1%

---

# Gérer les rôles {#manage-roles}

{{limited-availability-release-note}}

Pour gérer l’accès des utilisateurs et utilisatrices aux différents composants de l’interface utilisateur de Real-Time CDP Collaboration, un [administrateur](./manage-user-access.md#system-admin-gain-access) peut définir et affecter des rôles. Les rôles définissent l’accès d’un administrateur ou d’un utilisateur aux [ressources](https://experienceleague.adobe.com/en/docs/experience-platform/access-control/home#permissions){target="_blank"} de votre organisation. Ce guide fournit des informations sur les rôles standard fournis dans Real-Time CDP Collaboration, ainsi que sur les autorisations individuelles que vous pouvez attribuer aux rôles personnalisés.

Pour commencer à gérer les rôles, un administrateur devra avoir accès au produit Experience Platform. Pour plus d’informations sur l’obtention d’un accès administratif ou sur l’accès à Experience Platform, lisez le guide de gestion de l’accès [](./manage-user-access.md#manage-user-access-through-permissions) utilisateur.

## Rôles standard {#standard-roles}

Deux rôles standard vous sont fournis qui remplissent deux cas d’utilisation courants du contrôle d’accès. Il s’agit de rôles « en lecture seule », ce qui signifie qu’ils ne peuvent pas être personnalisés.

| Nom du rôle | Description du rôle | Autorisations |
| --- | --- | --- | 
| Gestionnaires de collaboration | Il s’agit d’une autorisation d’accès total, qui contient les 15 autorisations. Cela permet à l’utilisateur de lire, de créer et de modifier toutes les données. Il permet également d’accéder au bac à **[!UICONTROL sable Prod]** en Experience Platform, ce qui vous permet d’importer des audiences dans Real-Time CDP Collaboration. | Tous issus du tableau ci-dessous. |
| Visionneuses Collaboration | Il s’agit d’une autorisation d’accès en lecture seule. Un utilisateur peut lire et découvrir des données, des activités, des connexions, etc. Il permet également d’accéder au sandbox **[!UICONTROL Prod]** dans Experience Platform, ce qui vous permet d’importer des audiences dans Real-Time CDP Collaboration. | Toutes les autorisations de lecture du tableau ci-dessous. |

{style="table-layout:auto"}

## Création de rôles d’accès spécifiques {#specific-access-roles}

Vous souhaiterez probablement créer des rôles supplémentaires pour fournir différents niveaux d’accès à différents utilisateurs. Lors de la création de rôles, vous pouvez gérer différents niveaux d&#39;accès en sélectionnant des autorisations spécifiques dans la ressource **[!UICONTROL Collaborations]**. Pour savoir comment créer et gérer des rôles, reportez-vous au guide [roles](https://experienceleague.adobe.com/en/docs/experience-platform/access-control/abac/permissions-ui/roles#create-new-role){target="_blank"}.

>[!NOTE]
> Pour accéder à Real-Time CDP Collaboration, un utilisateur ou une utilisatrice doit avoir accès au sandbox **[!UICONTROL Prod]** dans Experience Platform. Pour permettre à un utilisateur d’accéder à ce sandbox, il doit être affecté à un rôle contenant l’autorisation **[!UICONTROL Prod]** dans la ressource **[!UICONTROL Sandbox]**.

Vous trouverez ci-dessous une liste des autorisations disponibles dans la ressource Collaborations :

| Autorisation de haut niveau | Description |
| --- | --- |
| Gérer les instances de collaboration | Affichez, créez, mettez à jour et supprimez des instances de collaboration d’une société. Discover les instances de collaboration d’autres entreprises. |
| Lire des instances de collaboration | Lisez les instances de collaboration d’une organisation et découvrez les instances de collaboration d’autres organisations. |
| Gérer les invitations à la connexion | Affichez, créez et supprimez des invitations de connexion initiées par votre entreprise. Acceptez et refusez l’invitation à la connexion initiée par d’autres organisations. |
| Lire les invitations à la connexion | Afficher les invitations à la connexion. |
| Gérer les connexions de collaboration | Un annonceur peut afficher, créer et mettre à jour des paramètres, ainsi qu’envoyer et supprimer des connexions. Un éditeur peut afficher, accepter ou refuser des connexions. |
| Lire les connexions Collaboration | Afficher les connexions. |
| Gérer les données d’audience | Intégrez et découvrez les audiences. Mettez à jour les audiences publiques, privées et personnalisées et gérez les paramètres de métadonnées de l’inventaire des audiences. |
| Lire les données d’audience | Lecture et découverte des audiences. |
| Gestion des données de mesure | Intégrer, mettre à jour et supprimer les données de mesure. |
| Lire les données de mesure | Lire les données de mesure. |
| Gérer les projets | Affichez, créez, mettez à jour et supprimez des projets pour toutes les activités de découverte, de partage, d’activation et de mesure. |
| Lire les projets | Affichez les projets pour toutes les activités de découverte, de partage, d’activation et de mesure. |
| Lire les activités de l’utilisateur | Lire les activités utilisateur. |
| Exporter les activités utilisateur | Exporter les activités utilisateur. |
| Lire la surveillance du crédit Collaboration | Suivi du crédit au niveau de l’organisation et de l’instance. |

{style="table-layout:auto"}

## Étapes suivantes

Après avoir créé des rôles qui définissent l’accès aux collaborations Real-Time CDP, vous devez [affecter les rôles](./manage-user-access.md#assign-a-role) aux administrateurs et aux utilisateurs. Reportez-vous au guide [gestion des autorisations pour un rôle](https://experienceleague.adobe.com/en/docs/experience-platform/access-control/abac/permissions-ui/permissions) pour une présentation complète de la gestion des rôles.
