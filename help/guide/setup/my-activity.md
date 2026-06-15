---
title: Suivre votre activité de consommation de crédit
description: Découvrez comment afficher le portefeuille de crédit de votre entreprise et suivre l’activité de consommation de crédit dans Real-Time CDP Collaboration.
audience: admin, publisher, advertiser
badgelimitedavailability: label="Disponibilité limitée" type="Informative" url="https://helpx.adobe.com/fr/legal/product-descriptions/real-time-customer-data-platform-collaboration.html newtab=true"
exl-id: b24d63e7-60f4-4cdb-ab1b-77c284543486
TQID: https://experienceleague.adobe.com/hDvkKFUCBYvsX8wntcYFrL6qZTxOo5CZOWAbxNwk7mw
product_v2:
  - id: fdddec33-c9cb-4459-b8b6-2664395a6f10
topic_v2:
  - id: aa2f3246-cb95-4b30-8899-fdf7d73550cc
  - id: c2be0313-b3ae-45e0-b454-d20bf54b23f2
  - id: e1e0219c-f879-479f-8427-888ed2a6e9c2
source-git-commit: 681f4af47a58a2ce66b25b09d793d0b5b127df39
workflow-type: tm+mt
source-wordcount: 726
ht-degree: 2%

---

# Suivre votre activité de consommation de crédit {#track-credit-consumption-activity}

>[!CONTEXTUALHELP]
>id="rtcdp_collaboration_organization_my_activity"
>title="En savoir plus"
>abstract=""

{{limited-availability-release-note}}

>[!BEGINSHADEBOX]

**Période sans dépassement de 90 jours** : les clients des régions éligibles bénéficient d’une période sans dépassement de 90 jours à compter de la date de disponibilité dans leur région. Pendant cette période, les clients n’encourent pas de frais supplémentaires pour avoir dépassé leur droit de crédit.

>[!ENDSHADEBOX]

Pour accéder à votre portefeuille de crédit et à votre activité de consommation de crédit, accédez à **[!UICONTROL Configuration]** dans la navigation principale, puis sélectionnez l’onglet **[!UICONTROL Mon activité]**.

![Onglet Mon activité affichant le portefeuille de crédits avec les crédits configurés, les crédits consommés, les crédits disponibles et la table d’activité de consommation de crédits.](/help/assets/setup/my-activity-credits/activity-dashboard.png)

>[!TIP]
>
>La vue **[!UICONTROL Mon activité]** n’inclut pas les actions des utilisateurs d’autres zones de l’interface de Real-Time CDP Collaboration. Utilisez la fonctionnalité [journaux d’audit](/help/guide/setup/audit-logs.md) pour obtenir ces informations.

## Comprendre la vue Mon activité {#understand-dashboard}

Utilisez la vue **[!UICONTROL Mon activité]** pour surveiller votre utilisation du crédit et consulter les activités qui consomment des crédits. La vue inclut le portefeuille de crédit et une table d’activités.

Le portefeuille de crédit affiche vos crédits provisionnés, les crédits consommés et les crédits disponibles.

| Mesure | Description |
|---------|-------------|
| **[!UICONTROL Crédits configurés]** | Nombre de crédits configurés pour votre compte. |
| **[!UICONTROL Crédits consommés]** | Nombre de crédits consommés par votre compte à la dernière actualisation quotidienne. |
| **[!UICONTROL Crédits disponibles]** | Nombre de crédits disponibles sur votre compte, calculé à partir des crédits provisionnés moins les crédits consommés. |

{style="table-layout:auto"}

Le tableau des activités répertorie les enregistrements de consommation de crédit journalière par date, type d&#39;activité, entrées traitées et crédits utilisés :

>[!NOTE]
>
>Les activités **[!UICONTROL Gestion de l’audience]** ne sont pas associées à un autre collaborateur. Par conséquent, les colonnes **[!UICONTROL Identifiant de connexion]** et **[!UICONTROL Nom de connexion]** pour ces types d’activités affichent une valeur **[!UICONTROL -]**.

| Colonne | Description |
|------------|--------------|
| **[!UICONTROL Date]** | Date à laquelle l’activité s’est produite, affichée au format MM/JJ/AAAA. |
| **[!UICONTROL Identifiant de connexion]** | Identifiant unique pour chaque connexion associée à une activité consommatrice de crédit, représenté sous la forme d’une chaîne alphanumérique. |
| **[!UICONTROL Nom de la connexion]** | Nom du collaborateur associé à la connexion et à l’activité consommatrice de crédit. |
| **[!UICONTROL Activité]** | Le type d’activité effectuée, tel que **[!UICONTROL Activation - Accès à l’audience (une fois)]**, **[!UICONTROL Activation - Accès à l’audience (récurrent)]**, **[!UICONTROL Activation - Sortie d’audience (une fois)]**, **[!UICONTROL Activation - Sortie d’audience (récurrente)]** ou **[!UICONTROL Gestion de l’audience]**. |
| **[!UICONTROL Entrées traitées]** | Nombre total d’entrées (par exemple, identifiants ou lignes) traitées pour l’activité. |
| **[!UICONTROL Total des crédits utilisés]** | Total des crédits consommés par l’activité. |
| **[!UICONTROL Mon avoir]** | La partie des crédits utilisés pour l&#39;activité correspondant à votre compte. |

{style="table-layout:auto"}

## Types d&#39;activités {#types-of-activities}

La colonne **[!UICONTROL Activité]** affiche différents types d’opérations consommatrices de crédit.

* **[!UICONTROL Gestion de l’audience]** : les crédits sont consommés lorsque les audiences sont sourcées dans Collaboration. Les crédits sont consommés en fonction du nombre d’identifiants indexés dans Collaboration sur toutes les audiences et de la fréquence de cette indexation, par exemple tous les jours, tous les trois jours ou toutes les semaines. Pour en savoir plus, consultez le guide [sourcing et gestion des audiences](/help/guide/setup/onboard-audiences.md) .
* **[!UICONTROL Activation - Accès à l’audience (une fois)]** : les crédits sont consommés lorsque l’accès à l’audience est traité une fois par le workflow d’activation. Pour en savoir plus, consultez le guide [Activation des audiences](/help/guide/collaborate/activate.md).
* **[!UICONTROL Activation - Accès à l’audience (récurrent)]** : les crédits sont consommés lorsque l’accès à l’audience est traité selon un planning récurrent via le workflow d’activation. Pour en savoir plus, consultez le guide [Activation des audiences](/help/guide/collaborate/activate.md).
* **[!UICONTROL Activation - Sortie d’audience (une fois)]** : les crédits sont consommés lorsque la sortie d’audience vers une destination est traitée une fois par le workflow d’activation. Cette activité est facturée au collaborateur qui reçoit l’audience. Pour en savoir plus, consultez le guide [Activation des audiences](/help/guide/collaborate/activate.md).
* **[!UICONTROL Activation - Sortie d’audience (récurrente)]** : les crédits sont consommés lorsque la sortie d’audience vers une destination est traitée selon un planning récurrent via le workflow d’activation. Cette activité est facturée au collaborateur qui reçoit l’audience. Pour en savoir plus, consultez le guide [Activation des audiences](/help/guide/collaborate/activate.md).
* **[!UICONTROL Mesure]** : les crédits sont consommés lorsque vous générez des rapports et des informations sur les performances de la campagne dans Collaboration. Les crédits sont consommés en fonction du nombre de lignes dans les rapports de campagne pour toutes les campagnes et de la fréquence de création des rapports, par exemple tous les jours, tous les trois jours ou toutes les semaines.

## Gérer votre consommation de crédit {#manage-credit-consumption}

Pour gérer efficacement votre consommation de crédit :

1. **comprendre** la consommation du crédit associée à chaque activité ; Consultez la description du produit [&#128279;](https://helpx.adobe.com/fr/legal/product-descriptions/real-time-customer-data-platform-collaboration.html){target=_blank} pour obtenir un tableau des crédits utilisés par activité.
2. **Surveiller régulièrement l’utilisation** : consultez vos tableaux d’activités et de crédits disponibles pour comprendre les modèles d’utilisation dans les activités de gestion de l’audience, d’accès à l’audience, de sortie d’audience et de mesure.
3. **Suivi par connexion** : utilisez le nom de la connexion pour identifier les connexions qui consomment le plus de crédits.
