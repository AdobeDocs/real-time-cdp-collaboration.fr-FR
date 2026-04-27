---
title: Configuration et gestion des destinations
description: Learn how to configure and manage destinations in Real-Time CDP Collaboration.
audience: admin, publisher
badgelimitedavailability: label="Disponibilité limitée" type="Informative" url="https://helpx.adobe.com/legal/product-descriptions/real-time-customer-data-platform-collaboration.html newtab=true"
exl-id: b4b26761-46ac-420f-b9f7-6e829d67aec9
TQID: https://experienceleague.adobe.com/3JoqIEJ0ilX3NHYOVersSkaa98kgPzOhqk94UP6Xc50
product_v2:
  - id: fdddec33-c9cb-4459-b8b6-2664395a6f10
topic_v2:
  - id: b5520579-b31f-4df7-9281-f0d9f91e2edc
  - id: e1e0219c-f879-479f-8427-888ed2a6e9c2
source-git-commit: 3ce7e66b31332836fd6cc6137c94622436505cc9
workflow-type: tm+mt
source-wordcount: 401
ht-degree: 1%

---

# Configuration et gestion des destinations

{{limited-availability-release-note}}

Destinations are integrations used to send targeted audiences to external platforms. These integrations enable you to activate audiences across various marketing channels and platforms for use in campaigns and customer engagement.

Collaborators can configure destinations to send audiences to external platforms, such as Adobe Experience Platform, for use in campaigns. Collaborators can then [activate audiences within a project](../collaborate/activate.md), which are sent to their connection&#39;s configured destination. L’activation peut être effectuée par l’un des collaborateurs en fonction des paramètres d’activation de l’audience [configurés dans la connexion](/help/guide/connect/establishing-connections.md#configure-connection-settings).

![The My destinations tab in the Setup workspace showing an active Adobe Experience Platform destinations.](/help/assets/setup/manage-destinations/my-destinations-overview.png)

To learn more about destinations, refer to the [destinations overview](../destinations/overview.md) guide.

## Configure destinations {#configure-destinations}

Desintations are configured in the **[!UICONTROL Setup]** section of Collaboration. To configure a destination, navigate to **[!UICONTROL Setup]** and then select the **[!UICONTROL My destinations]** tab. Here, you can view all available destinations.

>[!IMPORTANT]
>
>To configure and manage desintations, your user must have a role with the **Manage Audience Data** permission assigned to them. For more information about managing roles, refer to the [manage roles](../permissions/manage-roles.md) guide.

![The My destinations tab in the Setup workspace showing the available destinations.](/help/assets/setup/manage-destinations/my-destinations.png)

The set up process for destinations is dependent on the destination you are configuring. Refer to the [available destinations](../destinations/overview.md#available-destinations) catalog to view the available destinations and their configuration guides.

>[!NOTE]
>
>Currently, only Adobe Experience Platform is available as a self-serve destination within Real-Time CDP Collaboration. If you are interested in configuring a different destination, please contact your Adobe representative.

## Supprimer les destinations {#delete-destinations}

Deleting a destination removes it from your account, removes any previously sent audiences from the destination, and prevents any future audiences from being sent to that destination.

To delete a destination, navigate to the **[!UICONTROL My destinations]** tab in the **[!UICONTROL Setup]** section. Select the **[!UICONTROL Delete]** option for the destination that you want to remove.

![Espace de travail Mes destinations avec l’option Supprimer mise en surbrillance pour la destination Adobe Experience Platform.](/help/assets/setup/manage-destinations/delete-destination.png)

Une boîte de dialogue de confirmation s’affiche, dans laquelle vous pouvez confirmer que vous souhaitez supprimer la destination. Sélectionnez **[!UICONTROL Supprimer]** pour supprimer la destination.

![Boîte de dialogue Supprimer la destination avec l’option Supprimer mise en surbrillance.](/help/assets/setup/manage-destinations/delete-destination-confirmation.png)

## Étapes suivantes

Une fois la destination configurée, vous pouvez commencer à collaborer au sein de vos connexions pour [activer les audiences ciblées](../collaborate/activate.md) dans vos projets.
