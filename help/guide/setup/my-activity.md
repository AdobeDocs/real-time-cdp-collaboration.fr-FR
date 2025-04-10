---
title: Suivre votre activité de consommation de crédit
description: Découvrez comment effectuer le suivi de l’activité de consommation du crédit de votre organisation dans Real-Time CDP Collaboration.
audience: admin, publisher, advertiser
badgelimitedavailability: label="Disponibilité limitée" type="Informative" url="https://helpx.adobe.com/legal/product-descriptions/real-time-customer-data-platform-collaboration.html newtab=true"
exl-id: b24d63e7-60f4-4cdb-ab1b-77c284543486
source-git-commit: 1e8c2fdb3294111562f206ac141cfa39d5193c6c
workflow-type: tm+mt
source-wordcount: '520'
ht-degree: 1%

---

# Suivre votre activité de consommation de crédit

{{limited-availability-release-note}}

Utilisez l’onglet **[!UICONTROL Mon activité]** pour surveiller et suivre la consommation de crédit estimée de votre organisation pour toutes les activités de collaboration. Cette fonctionnalité fournit des informations détaillées sur l’utilisation des crédits dans les différentes connexions et activités, ce qui vous aide à gérer efficacement vos ressources.

>[!IMPORTANT]
>
>Le tableau de la consommation du crédit est arrondi et agrégé par jour pour le suivi. Les chiffres du tableau de bord **[!UICONTROL Mon activité]** représentent une consommation de crédit *estimée*. La consommation de crédit *réelle* utilisée pour la facturation est suivie dans les systèmes internes et vous pouvez y accéder sur demande. Contactez votre représentant Adobe pour obtenir ces informations.

Pour accéder à votre activité de consommation de crédit estimée, accédez à **[!UICONTROL Configuration]** dans la navigation principale, puis sélectionnez l’onglet **[!UICONTROL Mon activité]**.

![Tableau de bord Mon activité affichant les détails de la consommation du crédit](/help/assets/setup/my-activity-credits/activity-dashboard.png)

>[!TIP]
>
>La vue **[!UICONTROL Mon activité]** n’inclut pas d’informations sur les actions des utilisateurs dans différentes parties de l’interface utilisateur de Real-Time Collaboration CDP. Utilisez la fonctionnalité [journaux d’audit](/help/guide/setup/audit-logs.md) pour obtenir ces informations.

## Présentation du tableau de bord d’activité

Le tableau de bord des activités affiche une liste complète de toutes les opérations consommatrices de crédit au sein de votre organisation. Chaque ligne représente une activité distincte et fournit des informations clés sur l’utilisation du crédit :

>[!NOTE]
>
>Les activités **[!UICONTROL Gestion de l’audience]** ne sont pas associées à un autre collaborateur. Par conséquent, les colonnes **[!UICONTROL ID de connexion]** et **[!UICONTROL Nom de connexion]** pour ces types d’activités indiquent une valeur **[!UICONTROL N/A]**.

| Colonne | Description |
|--------|-------------|
| **[!UICONTROL Date]** | Date à laquelle l’activité s’est produite, affichée au format MM/JJ/AAAA. |
| **[!UICONTROL Identifiant de connexion]** | Identifiant unique pour chaque connexion associée à une activité consommatrice de crédit, représenté sous la forme d’une chaîne alphanumérique. |
| **[!UICONTROL Nom de la connexion]** | Nom du collaborateur associé à la connexion et à l’activité consommatrice de crédit. |
| **[!UICONTROL Activité]** | Le type d’activité effectuée, tel que **Activation - Partage**, **Activation - Sortie** ou **Gestion de l’audience**. |
| **[!UICONTROL Total des crédits utilisés]** | Nombre total de crédits consommés par l’activité. |
| **[!UICONTROL Mon avoir]** | Portion des crédits de votre entreprise utilisés pour l’activité. |

{style="table-layout:auto"}

## Types d&#39;activités {#types-of-activities}

La colonne **[!UICONTROL Activité]** affiche différents types d’opérations consommatrices de crédit.

* **[!UICONTROL Gestion de l’audience]** : les crédits sont consommés lorsque les audiences sont importées dans Real-Time CDP Collaboration. Les crédits sont consommés en fonction du nombre d’identifiants (en millions) indexés dans Real-Time CDP Collaboration sur toutes les audiences, et de la fréquence de cette indexation (quotidienne, tous les trois jours ou hebdomadaire) tout au long de la période de facturation. En savoir plus sur [l’importation et la gestion des audiences](/help/guide/setup/onboard-audiences.md).
* **[!UICONTROL Activation - Partage]** - Les crédits sont consommés en fonction du nombre d’identifiants activés depuis Real-Time CDP Collaboration tout au long de la période de facturation. En savoir plus sur le [partage](/help/guide/collaborate/share.md) et l’[activation d’audiences](/help/guide/collaborate/activate.md) dans Real-Time CDP Collaboration.
* **[!UICONTROL Activation - Sortie]** - Les crédits sont consommés en fonction du nombre d’identifiants activés depuis Real-Time CDP Collaboration tout au long de la période de facturation. En savoir plus sur le [partage](/help/guide/collaborate/share.md) et l’[activation d’audiences](/help/guide/collaborate/activate.md) dans Real-Time CDP Collaboration.


<!--

**[!UICONTROL Audience Overlaps]** – Credits are consumed as a function of the number of matched IDs across 2 or more shared audiences throughout the billing period. Read more about [audience overlaps in the discover tab](/help/guide/collaborate/discover.md).

Collaboration Measurement – Credits are consumed as a function of the number of rows existing in campaign reports across all campaigns, and the frequency of that reporting (daily, every three days, or weekly).

-->


## Gérer votre consommation de crédit {#manage-credit-consumption}

Pour gérer efficacement votre consommation de crédit :

1. **comprendre** la consommation du crédit associée à chaque activité ; Consultez la description du produit [Real-Time CDP Collaboration](https://helpx.adobe.com/legal/product-descriptions/real-time-customer-data-platform-collaboration.html){target=_blank} pour obtenir un tableau des crédits de collaboration utilisés par activité.
2. **Surveiller régulièrement** : consultez fréquemment votre tableau de bord d’activité pour comprendre les schémas d’utilisation.
3. **Suivi par connexion** : utilisez le nom de la connexion pour identifier les partenariats qui consomment le plus de crédits.

<!--

## Pagination and navigation

The activity list is paginated to improve performance and readability. Use the navigation controls at the bottom of the table to move between pages and adjust how many records you can view at once.

-->
