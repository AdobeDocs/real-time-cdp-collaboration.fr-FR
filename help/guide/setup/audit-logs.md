---
title: Journaux d’audit
description: Découvrez comment utiliser la fonctionnalité Journaux d’audit dans Real-Time CDP Collaboration pour effectuer le suivi des activités et des modifications des utilisateurs et utilisatrices.
audience: admin
badgelimitedavailability: label="Disponibilité limitée" type="Informative" url="https://helpx.adobe.com/legal/product-descriptions/real-time-customer-data-platform-collaboration.html newtab=true"
exl-id: 3af1ac47-dc3d-4f19-a6b9-9e4e835977c0
source-git-commit: ff22dde9730fab89481338753b1dc4a0adf1d57e
workflow-type: tm+mt
source-wordcount: '921'
ht-degree: 1%

---

# Journaux d’audit

{{limited-availability-release-note}}

Afin d’accroître la transparence et la visibilité des activités exécutées dans le système, vous pouvez auditer l’activité des utilisateurs pour divers services et fonctionnalités sous la forme de journaux d’audit dans Adobe Real-Time Customer Data Platform (CDP). Ces journaux constituent un journal d’audit qui peut vous aider à résoudre les problèmes dans Real-Time CDP Collaboration et à respecter efficacement les politiques de gestion des données d’entreprise et les exigences réglementaires.

Pour faire simple, un journal d’audit indique *qui* effectué *quelle* action et *quand*. Chaque action enregistrée dans un journal contient des métadonnées qui indiquent le type d’action, la date et l’heure, l’ID d’e-mail de l’utilisateur ou de l’utilisatrice qui a exécuté l’action et des attributs supplémentaires liés au type d’action.

Utilisez la fonctionnalité de journaux d’audit de Real-Time CDP Collaboration pour effectuer le suivi des activités et des modifications des utilisateurs et utilisatrices dans la plateforme. Cette fonctionnalité est intégrée au service d’audit Adobe Experience Platform et l’interface utilisateur de cette fonctionnalité réside dans Experience Platform.

![Écran de présentation de haut niveau de la fonctionnalité des journaux d’audit](/help/assets/setup/audit-logs/audit-logs-overview.png)

Pour obtenir des informations plus complètes sur les journaux d’audit, consultez la documentation sur les journaux d’audit Adobe Experience Platform [&#128279;](https://experienceleague.adobe.com/en/docs/experience-platform/landing/governance-privacy-security/audit-logs/overview){target="_blank"}.

## Accéder aux journaux d’audit

Vous pouvez accéder aux journaux d’audit de deux manières, comme décrit dans les sections ci-dessous. Les deux options affichent une liste de journaux d’audit capturant diverses activités effectuées dans l’interface utilisateur de Real-Time CDP Collaboration

### Accès aux journaux d’audit à partir de l’interface utilisateur de Real-Time CDP Collaboration

1. Accédez à l’onglet **[!UICONTROL Mon activité]** dans l’interface utilisateur de Real-Time CDP Collaboration.
2. Sélectionnez le lien Experience Platform dans le texte de l’interface utilisateur en haut de la page.

![Accéder aux journaux d’audit à partir de l’interface utilisateur de Real-Time CDP Collaboration](/help/assets/setup/audit-logs/access-from-collaboration-ui.png)

### Accès aux journaux d’audit directement dans l’interface utilisateur d’Experience Platform

1. Accédez à l’interface utilisateur de Adobe Experience Platform et sélectionnez la section **[!UICONTROL Audits]** dans le menu de gauche. Contactez les administrateurs système de votre entreprise pour obtenir les autorisations nécessaires si vous ne pouvez pas afficher les journaux d’audit.

![Accéder aux journaux d’audit à partir de l’interface utilisateur d’Experience Platform](/help/assets/setup/audit-logs/access-from-experience-platform-ui.png)

## Affichage et utilisation des journaux d’audit

Pour afficher les journaux d’audit :

1. Accédez à la section **[!UICONTROL Audits]** dans l’interface utilisateur de Adobe Experience Platform.
2. Utilisez les filtres pour réduire les journaux en fonction de vos critères.
3. Sélectionnez une entrée de journal pour afficher des informations détaillées, notamment la date et l’heure, l’identifiant de requête, les détails de la ressource et le statut de l’action.

![Journal d’audit détaillé](/help/assets/setup/audit-logs/filters-and-detailed-view.png)

### Activités capturées

Les journaux d’audit capturent des informations détaillées sur les activités des utilisateurs, notamment :

* **Identifiant utilisateur** : l’identifiant de l’utilisateur qui a exécuté l’action.
* **Action** : type d’action effectuée (par exemple, création, mise à jour, suppression).
* **Ressource** : ressource qui a été modifiée ou créée.
* **Horodatage** : l’heure à laquelle l’action a été effectuée.

Ces journaux créent un journal complet de toutes les activités au sein de votre instance Real-Time CDP Collaboration, ce qui est utile pour la gouvernance des données et la conformité à la réglementation. En savoir plus sur la [gestion des journaux d’audit dans l’interface utilisateur](https://experienceleague.adobe.com/en/docs/experience-platform/landing/governance-privacy-security/audit-logs/overview#managing-audit-logs-in-the-ui).

### Filtrer les journaux d’audit

L’interface utilisateur des journaux d’audit fournit plusieurs filtres pour vous aider à rechercher des journaux spécifiques :

* **Catégorie** : fait référence au type de ressource (par exemple : instance de collaboration, connexion, projet).
* **Action** : type d’action effectuée (par exemple : créer, supprimer, mettre à jour).
* **ID de la demande** : identifiant unique de la demande.
* **Adresse électronique de l’utilisateur** : adresse électronique de l’utilisateur qui a exécuté l’action.
* **Statut** : statut de l’action (par exemple : autorisée, refusée).
* **Période** : période pour laquelle vous souhaitez afficher les journaux.

En savoir plus sur le [ filtrage des journaux d’audit ](https://experienceleague.adobe.com/en/docs/experience-platform/landing/governance-privacy-security/audit-logs/overview#filter-audit-logs).

### Exemple d’utilisation

Les journaux d’audit sont générés et affichés dans l’interface utilisateur des audits d’Experience Platform lorsque vous effectuez des actions dans l’interface utilisateur de Real-Time CDP Collaboration, telles que la gestion des audiences, l’extension des invitations à la connexion, la création de projets, etc. Par exemple, les opérations de création ou de mise à jour de parties d’un projet sont capturées comme illustré ci-dessous :

![Exemple de journaux d’audit générés lors de la création et de la mise à jour de parties d’un projet.](/help/assets/setup/audit-logs/create-project-audits.png)

## Avantages

Découvrez certains des avantages de l’utilisation des journaux d’audit :

* **Gouvernance des données** : utilisez les journaux d’audit pour vous assurer que toutes les activités au sein de la plateforme sont suivies et auditables.
* **Conformité à la réglementation** : cette fonctionnalité fournit un journal des activités des utilisateurs pour répondre aux exigences réglementaires.
* **Dépannage** : les journaux d’audit permettent d’identifier et de résoudre les problèmes en fournissant des journaux détaillés des actions de l’utilisateur.

## Référence des catégories et actions

Le tableau ci-dessous fournit une référence de toutes les catégories et actions pour Real-Time CDP Collaboration.

![Catégories disponibles mises en surbrillance dans les journaux d’audit Real-Time CDP Collaboration.](/help/assets/setup/audit-logs/available-categories.png)

| Catégorie | Actions | Description |
|-------------------------------|------------------------------------------|-------------|
| **[!UICONTROL Instance Collaboration]** | créer, mettre à jour, supprimer | Gérez les comptes d’organisation, notamment la création, la mise à jour et la suppression d’organisations. En savoir plus sur la [configuration d’organisations](/help/guide/setup/onboard-organization.md). |
| **[!UICONTROL Invitation À Une Connexion Collaboration]** | créer, mettre à jour, supprimer, approuver, rejeter | Gérer les invitations à la connexion, notamment la création, la mise à jour, la suppression, l’approbation et le rejet des invitations. En savoir plus sur les [invitations à une connexion](/help/guide/connect/establishing-connections.md). |
| **[!UICONTROL Connexion Collaboration]** | créer, mettre à jour, supprimer, approuver, rejeter, demander l’approbation | Gérer les connexions de collaboration, notamment la création, la mise à jour, la suppression, l’approbation, le rejet et la demande d’approbation des connexions. |
| **[!UICONTROL Connexion aux données Collaboration]** | créer, mettre à jour, supprimer | Gérez les connexions de données pour la collaboration afin d’importer et de gérer les audiences, y compris la création, la mise à jour et la suppression de connexions de données. En savoir plus sur la [gestion des connexions de données](/help/guide/setup/manage-data-connection.md). |
| **[!UICONTROL Entité De Données Collaboration]** | créer, mettre à jour, supprimer | Gérez les entités de données pour la collaboration, notamment la création, la mise à jour et la suppression des entités de données. Dans ce contexte, les entités de données font référence aux audiences. En savoir plus sur [l’importation et la gestion des audiences](/help/guide/setup/onboard-audiences.md). |
| **[!UICONTROL Projet Collaboration]** | créer, mettre à jour, supprimer | Gérez les projets en collaboration, notamment la création, la mise à jour et la suppression de projets. En savoir plus sur la [gestion de projets](/help/guide/collaborate/manage-projects.md). |
| **[!UICONTROL Module Collaboration]** | créer, mettre à jour, supprimer | Gérez différents modules dans les projets de collaboration, notamment la création, la mise à jour et la suppression de divers modules dans l’interface utilisateur. Par exemple, la possibilité de [partager des audiences](/help/guide/collaborate/share.md). |

{style="table-layout:auto"}

En utilisant la fonctionnalité des journaux d’audit, vous pouvez conserver un enregistrement clair et détaillé de toutes les activités au sein de votre instance Real-Time CDP Collaboration, ce qui garantit la transparence et la responsabilité.
