---
title: Suivre votre activité de consommation de crédit
description: Découvrez comment effectuer le suivi de l’activité de consommation du crédit de votre organisation dans Real-Time CDP Collaboration.
audience: admin, publisher, advertiser
badgelimitedavailability: label="Disponibilité limitée" type="Informative" url="https://helpx.adobe.com/fr/legal/product-descriptions/real-time-customer-data-platform-collaboration.html newtab=true"
exl-id: b24d63e7-60f4-4cdb-ab1b-77c284543486
source-git-commit: eed99cfafd5ffad5a468741f7258c162454769b7
workflow-type: tm+mt
source-wordcount: '554'
ht-degree: 5%

---

# Suivre votre activité de consommation de crédit

{{limited-availability-release-note}}

>[!BEGINSHADEBOX]

**Période sans dépassement de 90 jours** : les clients des régions éligibles bénéficient d’une période sans dépassement de 90 jours à compter de la date de disponibilité dans leur région. Pendant cette période, les clients n’encourent pas de frais supplémentaires pour avoir dépassé leur droit de crédit.

>[!ENDSHADEBOX]

>[!IMPORTANT]
>
>Le tableau de la consommation du crédit est arrondi et agrégé par jour pour le suivi. Les chiffres du tableau de bord **[!UICONTROL Mon activité]** représentent une consommation de crédit *estimée*. La consommation de crédit *réelle* utilisée pour la facturation est suivie dans les systèmes internes et vous pouvez y accéder sur demande. Contactez votre représentant Adobe pour obtenir ces informations.

Pour accéder à votre activité de consommation de crédit estimée, accédez à **[!UICONTROL Configuration]** dans la navigation principale, puis sélectionnez l’onglet **[!UICONTROL Mon activité]**.

![Tableau de bord Mon activité affichant les détails de la consommation du crédit](/help/assets/setup/my-activity-credits/activity-dashboard.png)

>[!TIP]
>
>La vue **[!UICONTROL Mon activité]** n’inclut pas d’informations sur les actions des utilisateurs dans différentes parties de l’interface utilisateur de Collaboration. Utilisez la fonctionnalité [journaux d’audit](/help/guide/setup/audit-logs.md) pour obtenir ces informations.

## Présentation du tableau de bord d’activité {#understand-dashboard}

Le tableau de bord des activités affiche une liste complète de toutes les opérations consommatrices de crédit au sein de votre compte. Chaque ligne représente une activité distincte et fournit des informations clés sur l’utilisation du crédit :

>[!NOTE]
>
>Les activités **[!UICONTROL Gestion de l’audience]** ne sont pas associées à un autre collaborateur. Par conséquent, les colonnes **[!UICONTROL ID de connexion]** et **[!UICONTROL Nom de connexion]** pour ces types d’activités indiquent une valeur **[!UICONTROL -]**.

| Colonne | Description |
|------------|--------------|
| **[!UICONTROL Date]** | Date à laquelle l’activité s’est produite, affichée au format MM/JJ/AAAA. |
| **[!UICONTROL Identifiant de connexion]** | Identifiant unique pour chaque connexion associée à une activité consommatrice de crédit, représenté sous la forme d’une chaîne alphanumérique. |
| **[!UICONTROL Nom de la connexion]** | Nom du collaborateur associé à la connexion et à l’activité consommatrice de crédit. |
| **[!UICONTROL Activité]** | Le type d’activité effectuée, tel que **Activation - Correspondance**, **Activation - Sortie** ou **Gestion de l’audience**. |
| **[!UICONTROL Entrées traitées]** | Nombre total d’entrées (par exemple, identifiants ou lignes) traitées pour l’activité. |
| **[!UICONTROL Total des crédits utilisés]** | Nombre total de crédits consommés par l’activité. |
| **[!UICONTROL Mon avoir]** | La partie des crédits utilisés pour l&#39;activité correspondant à votre compte. |

{style="table-layout:auto"}

## Types d&#39;activités {#types-of-activities}

La colonne **[!UICONTROL Activité]** affiche différents types d’opérations consommatrices de crédit.

* **[!UICONTROL Gestion de l’audience]** : les crédits sont consommés lorsque les audiences sont sourcées dans Collaboration. Les crédits sont consommés en fonction du nombre d’identifiants (en millions) indexés dans Collaboration sur toutes les audiences, et de la fréquence de cette indexation (quotidienne, tous les trois jours ou hebdomadaire). Pour en savoir plus, consultez le guide [sourcing et gestion des audiences](/help/guide/setup/onboard-audiences.md) .
* **[!UICONTROL Activation - Correspondance]** - Les crédits sont consommés en fonction du nombre d’identifiants correspondants et préparés pour l’activation. Pour en savoir plus, consultez le guide [Activation des audiences](/help/guide/collaborate/activate.md).
* **[!UICONTROL Activation - Sortie]** - Les crédits sont consommés en fonction du nombre d’identifiants envoyés à une destination. Cela est toujours facturé au collaborateur qui reçoit l’audience. Pour en savoir plus, consultez le guide [Activation des audiences](/help/guide/collaborate/activate.md).
* **[!UICONTROL Mesure]** - Exécutez des activités dans Collaboration pour générer des rapports et des informations sur les performances des campagnes. Les crédits sont consommés en fonction du nombre de lignes dans les rapports de campagne sur toutes les campagnes et de la fréquence de création des rapports (quotidienne, tous les trois jours ou hebdomadaire).

## Gérer votre consommation de crédit {#manage-credit-consumption}

Pour gérer efficacement votre consommation de crédit :

1. **comprendre** la consommation du crédit associée à chaque activité ; Consultez la description du produit [Collaboration](https://helpx.adobe.com/fr/legal/product-descriptions/real-time-customer-data-platform-collaboration.html){target=_blank} pour obtenir un tableau des crédits utilisés par activité.
2. **Surveiller régulièrement** : consultez fréquemment votre tableau de bord d’activité pour comprendre les schémas d’utilisation.
3. **Suivi par connexion** : utilisez le nom de la connexion pour identifier les connexions qui consomment le plus de crédits.
