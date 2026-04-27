---
title: Journaux d’audit
description: Découvrez comment utiliser la fonctionnalité Journaux d’audit dans Real-Time CDP Collaboration pour effectuer le suivi des activités et des modifications des utilisateurs et utilisatrices.
audience: admin
badgelimitedavailability: label="Disponibilité limitée" type="Informative" url="https://helpx.adobe.com/legal/product-descriptions/real-time-customer-data-platform-collaboration.html newtab=true"
exl-id: 3af1ac47-dc3d-4f19-a6b9-9e4e835977c0
TQID: https://experienceleague.adobe.com/zb09-bUpxJ2VPDknETHeayMuLpNRCaQ2VTnV9QnTRgE
product_v2:
  - id: fdddec33-c9cb-4459-b8b6-2664395a6f10
topic_v2:
  - id: a004cc84-67b9-4a33-a3a7-8ec7273ef4dc
  - id: c1579802-ddd4-4214-8a91-97b2066abe11
  - id: c7d04a2c-412a-4c9d-9d7a-4456eaa5adeb
  - id: d095671a-1355-40aa-8b5f-06c33c68080b
  - id: e1e0219c-f879-479f-8427-888ed2a6e9c2
  - id: f4e6943a-c91a-4134-a2c7-f4f20cfff2f0
source-git-commit: 3ce7e66b31332836fd6cc6137c94622436505cc9
workflow-type: tm+mt
source-wordcount: 950
ht-degree: 4%

---

# Journaux d’audit

{{limited-availability-release-note}}

Afin d’accroître la transparence et la visibilité des activités exécutées dans le système, vous pouvez auditer l’activité des utilisateurs et utilisatrices pour divers services et fonctionnalités sous la forme de journaux d’audit dans Adobe Experience Platform. Ces journaux constituent un journal d’audit qui peut vous aider à résoudre les problèmes dans Adobe Real-Time CDP Collaboration et à respecter efficacement les politiques de gestion des données d’entreprise et les exigences réglementaires.

Pour faire simple, un journal d’audit indique *qui* effectué *quelle* action et *quand*. Chaque action enregistrée dans un journal contient des métadonnées qui indiquent le type d’action, la date et l’heure, l’ID d’e-mail de l’utilisateur ou de l’utilisatrice qui a exécuté l’action et des attributs supplémentaires liés au type d’action.

Utilisez la fonctionnalité de journaux d’audit de Collaboration pour effectuer le suivi des activités et des modifications des utilisateurs et utilisatrices dans la plateforme. Cette fonctionnalité est intégrée au service d’audit Experience Platform et l’interface utilisateur de cette fonctionnalité réside dans Experience Platform.

![Écran de présentation de haut niveau de la fonctionnalité des journaux d’audit.](/help/assets/setup/audit-logs/audit-logs-overview.png)

Pour obtenir des informations plus complètes sur les journaux d’audit, consultez la documentation sur les journaux d’audit d’[Experience Platform](https://experienceleague.adobe.com/en/docs/experience-platform/landing/governance-privacy-security/audit-logs/overview){target="_blank"}.

## Accéder aux journaux d’audit

Vous pouvez accéder aux journaux d’audit de deux manières, comme décrit dans les sections ci-dessous. Les deux options affichent une liste de journaux d’audit capturant diverses activités effectuées dans Collaboration.

### Accès aux journaux d’audit à partir de l’interface utilisateur de Collaboration

1. Accédez à l’onglet **[!UICONTROL Mon activité]** dans l’espace de travail **[!UICONTROL Configuration]** de Collaboration.
2. Sélectionnez le lien Experience Platform dans le texte en haut de la page.

![Accédez aux journaux d’audit à partir de l’onglet Mon activité dans Collaboration.](/help/assets/setup/audit-logs/access-from-collaboration-ui.png)

### Accès aux journaux d’audit directement dans l’interface utilisateur d’Experience Platform

1. Accédez à [Experience Platform](https://platform.adobe.com/) et sélectionnez la section **[!UICONTROL Audits]** dans le menu de gauche. Contactez les administrateurs système de votre entreprise pour obtenir les autorisations nécessaires si vous ne pouvez pas afficher les journaux d’audit.

![Accéder aux journaux d’audit à partir d’Experience Platform.](/help/assets/setup/audit-logs/access-from-experience-platform-ui.png)

## Affichage et utilisation des journaux d’audit

Pour afficher les journaux d’audit :

1. Navigate to the **[!UICONTROL Audits]** section in Experience Platform.
2. Use the [filters](#filter-audit-logs) to narrow down the logs based on your criteria.
3. Select a log entry to view detailed information, including the timestamp, request ID, resource details, and action status.

![Detailed Audit Log](/help/assets/setup/audit-logs/filters-and-detailed-view.png)

### Captured activities

Audit logs capture detailed information about user activities, including:

* **Timestamp**: The exact date and time of the action performed in a month/day/year hour:minute AM/PM format.
* **Asset name**: The name of the resource on which the action was performed.
* **Category**: The type of resource the action was performed on.
* **Action**: The specific action performed, such as create or delete.
* **User**: The email address of the user who performed the action.

These logs create a comprehensive trail of all activities within your Collaboration instance, which is useful for data governance and regulatory compliance. Read more about [managing audit logs in the UI](https://experienceleague.adobe.com/en/docs/experience-platform/landing/governance-privacy-security/audit-logs/overview#managing-audit-logs-in-the-ui).

### Filter audit logs {#filter-audit-logs}

The audit logs UI provides several filters to help you search for specific logs:

* **Category**: The type of resource the action was performed on, such as Collaboration Instance or Collaboration Connection Invite.
* **Action**: The type of action performed. Available actions depend on the category selected. For example, actions for Collaboration Instance include create, update, and delete.
* **Request ID**: A unique identifier for the request.
* **User**: The email address of the user who performed the action.
* **Status**: The status of the action, such as allow or deny.
* **Date Range**: The range of dates for which you want to view logs.

Read more about [filtering audit logs](https://experienceleague.adobe.com/en/docs/experience-platform/landing/governance-privacy-security/audit-logs/overview#filter-audit-logs).

## Avantages

Audit logs provide several benefits for organizations using Collaboration:

* **Gouvernance des données** : utilisez les journaux d’audit pour vous assurer que toutes les activités au sein de la plateforme sont suivies et auditables.
* **Conformité à la réglementation** : cette fonctionnalité fournit un journal des activités des utilisateurs pour répondre aux exigences réglementaires.
* **Dépannage** : les journaux d’audit permettent d’identifier et de résoudre les problèmes en fournissant des journaux détaillés des actions de l’utilisateur.

## Référence des catégories et actions

Le tableau ci-dessous fournit une référence de toutes les catégories et actions pour Real-Time CDP Collaboration.

![Catégories disponibles mises en surbrillance dans les journaux d’audit Real-Time CDP Collaboration.](/help/assets/setup/audit-logs/available-categories.png)

| Catégorie | Actions | Description |
|-------------------------------|------------------------------------------|-------------|
| **[!UICONTROL Instance Collaboration]** | créer, mettre à jour, supprimer | Gérez les comptes, notamment la création, la mise à jour et la suppression de comptes. Pour en savoir plus sur le modèle, consultez le guide [Configurer vos comptes](/help/guide/setup/onboard-account.md). |
| **[!UICONTROL Invitation À Une Connexion Collaboration]** | créer, mettre à jour, supprimer, approuver, rejeter | Gérer les invitations à la connexion, notamment la création, la mise à jour, la suppression, l’approbation et le rejet des invitations. Pour plus d’informations, consultez le guide [établissement de connexions](/help/guide/connect/establishing-connections.md). |
| **[!UICONTROL Connexion Collaboration]** | créer, mettre à jour, supprimer, approuver, rejeter, demander l’approbation | Gérer les connexions, notamment la création, la mise à jour, la suppression, l’approbation, le rejet et la demande d’approbation des connexions. |
| **[!UICONTROL Connexion aux données Collaboration]** | créer, mettre à jour, supprimer | Gérez les connexions de données à partir desquelles vous créez et gérez les audiences, notamment en créant, mettant à jour et supprimant des connexions de données. Pour plus d’informations, consultez le guide [gestion des connexions aux données](/help/guide/setup/manage-data-connection.md). |
| **[!UICONTROL Entité De Données Collaboration]** | créer, mettre à jour, supprimer | Gérez les entités de données pour Collaboration, notamment la création, la mise à jour et la suppression d’entités de données. Dans ce contexte, les entités de données font référence aux audiences. For more information, read the [sourcing and managing audiences](/help/guide/setup/onboard-audiences.md) guide. |
| **[!UICONTROL Collaboration Project]** | créer, mettre à jour, supprimer | Manage projects within Collaboration, including creating, updating, and deleting projects. For more information, read the [managing projects](/help/guide/collaborate/manage-projects.md) guide. |
| **[!UICONTROL Collaboration Module]** | créer, mettre à jour, supprimer | Manage different modules within projects, including creating, updating, and deleting various modules in the UI. For example, the ability to [activate audiences](/help/guide/collaborate/activate.md). |

{style="table-layout:auto"}

By leveraging the audit logs functionality, you can maintain a clear and detailed record of all activities within Collaboration, ensuring transparency and accountability.
