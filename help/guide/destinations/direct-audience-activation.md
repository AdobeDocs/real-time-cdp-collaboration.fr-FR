---
title: Activation Directe Des Audiences (Audience Activation 1P) - Beta
description: Découvrez comment activer vos propres audiences propriétaires ou partagées sans projet, sélectionner une destination, vérifier les mappages de champs et définir un planning d’activation.
badgeBeta: label="Beta" type="Informative"
source-git-commit: 5f823194a18468b9205f64853551719ae8a3752f
workflow-type: tm+mt
source-wordcount: '650'
ht-degree: 1%
---

# Activer les audiences directement (Audience Activation 1P) {#activate-audiences-directly}

Utilisez l’activation directe de l’audience propriétaire (1P) dans [!DNL Adobe Real-Time CDP Collaboration] pour envoyer des audiences vers une destination sans créer de projet. Activez les audiences que vous possédez ou les audiences partagées avec vous pour une utilisation propriétaire.

Commencez à partir d’une destination configurée ou de **[!UICONTROL Audiences activées]**, puis sélectionnez des audiences et définissez le planning d’activation.

Pour envoyer et activer des audiences dans un projet de collaboration, consultez [Envoyer et activer des audiences dans un projet](/help/guide/collaborate/activate.md).

## Accès de l’audience pour l’activation {#audience-access-for-activation}

Vérifiez la source de l’audience pour déterminer si vous avez besoin d’une subvention avant l’activation.

| Audience source | Exigence d’accès |
| --- | --- |
| Vos propres audiences | Les audiences vous appartiennent. |
| Audiences partagées avec vous | Vous avez besoin d’une subvention active avec une autorisation d’activation directe. Le fournisseur conserve la propriété. |

{style="table-layout:auto"}

Une audience virtuelle vous donne accès à une audience partagée par référence sans déplacer ses données. Vous pouvez ensuite activer l’audience pour envoyer ses données à la destination sélectionnée.

Pour plus d’informations sur les autorisations et les contrôles des fournisseurs, consultez [Accès aux audiences virtuelles (autorisations d’audience)](/help/guide/setup/virtual-audience-access.md).

## Conditions préalables {#prerequisites}

Avant de commencer, vérifiez que vous disposez des éléments suivants :

* Audience que vous possédez ou que vous partagez par le biais d’une subvention propriétaire éligible (1P).
* Une destination configurée que vous contrôlez et qui prend en charge l’activation directe.
* Au moins un mappage des champs de clé de correspondance pour la destination.

Pour activer une audience partagée, vérifiez que son octroi actif de portée connexion remplit les [conditions d’éligibilité](#check-shared-audience-access). Utilisez l’espace de travail **[!UICONTROL Activation]**. Vous n’avez pas besoin de projet.

### Éligibilité de l’audience partagée {#check-shared-audience-access}

La subvention doit remplir chaque condition pour permettre l&#39;activation directe.

| Exigence | Condition |
| --- | --- |
| Autorisation Audience | L’octroi inclut l’autorisation d’activation directe. |
| Durée de l’accès | L&#39;octroi est actif, indéfiniment ou dans la période spécifiée. |

{style="table-layout:auto"}

L’autorisation distincte **[!UICONTROL Créer une nouvelle audience]** vous permet d’utiliser une audience partagée pour la création d’une audience de cohorte. Vous n’avez pas besoin de cette autorisation pour l’activation directe.

### Mappages de champs de destination {#review-destination-field-mappings}

L’activation directe utilise les mappages de clé de correspondance configurés pour votre destination. Vous ne sélectionnez pas les clés de correspondance lors de l’activation.

Pour configurer des destinations, consultez [présentation des destinations](../destinations/overview.md).

## Démarrer l’activation directe {#start-direct-activation}

Commencez à partir d’une destination configurée pour la liste des audiences activées. Les destinations Adobe Experience Platform ne prennent pas en charge l’activation propriétaire.

### Démarrer à partir d’une destination {#start-from-a-destination}

Pour ouvrir le workflow avec une destination sélectionnée, commencez à partir de cette destination configurée. Tout d’abord, ouvrez l’espace de travail **[!UICONTROL Activation]** et sélectionnez **[!UICONTROL Destinations]**.

Sélectionnez ensuite **[!UICONTROL Activer les audiences]** parmi les actions pour la destination que vous souhaitez utiliser.

Le workflow s’ouvre avec la destination sélectionnée. Continuez ensuite avec [Configurer l&#39;activation](#configure-the-activation).

### Démarrer à partir des audiences activées {#start-from-activated-audiences}

Pour choisir une destination dans le workflow, commencez dans la liste audiences activées . Tout d’abord, ouvrez l’espace de travail **[!UICONTROL Activation]** et sélectionnez **[!UICONTROL Audiences activées]**.

Démarrez ensuite le workflow en sélectionnant **[!UICONTROL Activer l’audience]** sur la page ou en sélectionnant l’icône d’ajout (![Ajouter une activation d’audience.](/help/assets/icons/plus.png)) puis **[!UICONTROL Activer l’audience]**.

Le workflow s’ouvre sans sélection de destination. Continuez ensuite avec [Configurer l&#39;activation](#configure-the-activation).

## Configurer l’activation {#configure-the-activation}

Sélectionnez une audience par activation à partir de vos propres audiences ou audiences partagées avec vous. Utilisez la destination présélectionnée ou choisissez une destination configurée si aucune destination n’est sélectionnée. Le workflow applique les [mappages existants](#review-destination-field-mappings) configurés pour cette destination.

Choisissez quand exécuter l’activation, puis passez en revue l’audience, la destination et le planning sélectionnés avant l’envoi.

## Accès aux modifications et exécutions planifiées {#access-changes-and-scheduled-runs}

Activez une audience partagée uniquement lorsque le fournisseur autorise l’accès.

| Modification de l’accès | Effet |
| --- | --- |
| La subvention expire | Le système traite l’expiration toutes les heures. Le destinataire perd l’accès à l’audience virtuelle après le traitement de l’expiration. |
| Le fournisseur révoque la subvention | Le destinataire perd immédiatement l’accès à l’audience virtuelle. |
| Une activation planifiée s’exécute | Le système vérifie la subvention. Les audiences avec des subventions révoquées ou expirées ne sont pas éligibles à l’activation. |

{style="table-layout:auto"}

L’expiration ou la révocation ne suppriment pas les données d’audience déjà diffusées vers une destination.

## Étapes suivantes {#next-steps}

Une fois les audiences activées, utilisez ces guides pour gérer les destinations ou les connexions des collaborateurs.

* [Configuration et gestion des destinations](/help/guide/destinations/manage-destinations.md)
* [Gérer les connexions des collaborateurs](/help/guide/connect/manage-connections.md)
