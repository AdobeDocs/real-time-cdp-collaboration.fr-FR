---
title: Mesurer les performances
description: Mesurez les performances de vos campagnes sur différents canaux. Découvrez comment utiliser et interpréter divers rapports.
audience: admin, publisher, advertiser
badgelimitedavailability: label="Disponibilité limitée" type="Informative" url="https://helpx.adobe.com/legal/product-descriptions/real-time-customer-data-platform-collaboration.html newtab=true"
exl-id: c92b263e-1f96-49f1-841a-ef2e97a4cb9a
source-git-commit: 0cf888e36ffc4730fc8de4d8adccae0e0fc2caa8
workflow-type: tm+mt
source-wordcount: '1949'
ht-degree: 6%

---

# Mesurer les performances

{{limited-availability-release-note}}

>[!IMPORTANT]
>
>L’espace de travail **[!UICONTROL Mesure]** n’est disponible que si le cas d’utilisation **Mesure** a été activé [pendant le processus de connexion](../connect/establishing-connections.md#connection-settings). Pour plus d’informations sur les cas d’utilisation, consultez le guide [gestion des projets](./manage-projects.md#project-use-cases).

Découvrez les rapports disponibles dans Adobe Real-Time CDP Collaboration et comment mesurer et analyser les performances de vos campagnes marketing sur différents canaux.

## Conditions préalables {#prerequisites}

Avant de pouvoir accéder aux rapports de mesure dans Collaboration, vous devez :

* [Se connecter](/help/guide/connect/establishing-connections.md) avec un collaborateur avec le cas d’utilisation **Measurement** activé
* Collaborez à au moins un projet avec votre collaborateur. Découvrez comment [&#x200B; créer un projet &#x200B;](/help/guide/collaborate/manage-projects.md#create-project).
* Exécutez votre campagne et assurez-vous qu’un [identifiant de campagne est fourni pour la campagne](../collaborate/manage-projects.md#manage-campaign-id) :
   * Si vous êtes un éditeur, saisissez l’identifiant de campagne associé à la campagne de votre annonceur.
   * Si vous êtes un annonceur, demandez à votre collaborateur (éditeur) de fournir l’identifiant de la campagne. Cela est nécessaire pour [générer des rapports dans l’espace de travail Mesure](#create-measurement-report).
* [Chargez les données de mesure](/help/guide/setup/onboard-measurement-data.md) dans Collaboration pour [créer des rapports d’attribution](#create-attribution-report).

## Afficher les rapports {#view-reports}

>[!CONTEXTUALHELP]
>id="rtcdp_collaboration_measurement_create_report_campaignID"
>title="Identifiants de campagne"
>abstract="Espace réservé pour ajouter des informations pertinentes dans l’interface d’utilisation sur les identifiants de campagne."

>[!CONTEXTUALHELP]
>id="rtcdp_collaboration_measurement_create_report"
>title="Identifiants de campagne"
>abstract="Espace réservé pour ajouter des informations pertinentes dans l’interface d’utilisation sur les identifiants de campagne."

Pour visualiser les rapports disponibles dans l&#39;onglet Mesure :

1. Accédez à **[!UICONTROL Collaborer]** > **[!UICONTROL Mes projets]**.
2. Pour le projet souhaité, sélectionnez **[!UICONTROL Afficher]**.
3. Dans le projet, sélectionnez l’onglet **[!UICONTROL Mesure]**.

Sélectionnez **[!UICONTROL Afficher le rapport complet]** pour accéder aux différents rapports disponibles, détaillés ci-dessous.

![Comment accéder à l’onglet Mesure dans un projet &#x200B;](/help/assets/collaborate/measure/measurement.gif).

### Vue récapitulative

L’affichage du haut de la page dans l’onglet Mesure affiche un résumé de la campagne avec des chiffres généraux à titre de référence :

**[!UICONTROL Impressions]** : nombre total d’affichages de la création.
**[!UICONTROL Portée unique]** : nombre d’identités individuelles ayant vu le contenu créatif.
**[!UICONTROL Fréquence moyenne totale]** : nombre d’impressions divisé par les identités uniques atteintes. Cette figure indique la fréquence à laquelle chaque identité a été présentée dans la création.

![Vue récapitulative de la campagne](/help/assets/collaborate/measure/campaign-summary.png)

### Mesures au fil du temps {#metrics-over-time}

>[!CONTEXTUALHELP]
>id="rtcdp_collaboration_measure_metricsovertime"
>title="Mesures au fil du temps"
>abstract="Utilisez la vue Mesures au fil du temps pour comprendre le nombre total d’impressions affichées pour votre contenu créatif tout au long de la campagne. Vous pouvez sélectionner deux dimensions au maximum à afficher dans le rapport."

Utilisez la vue Mesures au fil du temps pour comprendre le nombre total d’impressions affichées pour votre contenu créatif tout au long de la campagne. Notez que vous pouvez sélectionner un maximum de deux mesures à afficher et à analyser dans le rapport.

![Vue Mesures au fil du temps.](/help/assets/collaborate/measure/metrics-over-time.png)

### Répartition des fréquences {#frequency-distribution}

Utilisez le mode Distribution de fréquence pour comprendre la répartition du nombre d’impressions présentées à chaque utilisateur unique. Cette vue peut vous aider dans les futures campagnes à décider à partir de quel point vous souhaitez commencer à supprimer des audiences. Par exemple, vous pouvez supprimer des profils qui ont déjà vu un contenu créatif trois fois.

![Vue de répartition de la fréquence.](/help/assets/collaborate/measure/frequency-distribution.gif)

### Mesure par dimension {#metric-by-dimension}

Analysez différentes mesures telles que les impressions, les impressions visibles, la portée unique, le coût, etc. dans le contexte du support d’emplacement. Analysez les médias (par exemple, diffusion en continu mobile, CTV programmatique ou autres) qui génèrent les meilleurs résultats pour vos campagnes.

![Mesure par dimension.](/help/assets/collaborate/measure/metric-by-dimension.png)

### Courbe de portée cumulée {#cumulative-reach-curve}

Au fur et à mesure que la campagne avançait et que le nombre d’impressions augmentait, comprenez si le nombre d’utilisateurs que vous avez pu atteindre a également augmenté. Une tendance courante dans les campagnes est qu&#39;après un certain point, un plateau est atteint où la création est présentée aux mêmes personnes encore et encore. Cette vue peut vous aider à ajuster la durée des futures campagnes, en fonction du moment où de nouvelles personnes n’ont plus été atteintes.

![Courbe de portée cumulée.](/help/assets/collaborate/measure/cumulative-reach-curve.png)

### Impressions par placement {#impressions-by-placement}

Identifiez le support qui génère des impressions pour votre contenu créatif. Cela peut vous aider à décider où investir vos dépenses publicitaires dans les campagnes futures.

![Impressions par emplacement.](/help/assets/collaborate/measure/impressions-by-placement.png)

### Conversions cumulées {#cumulative-conversions}

Cette vue fournit une répartition détaillée des événements de conversion que vous choisissez de mesurer sous la forme d’un tableau. Le tableau comprend :

* **Événement de conversion** : nom de chaque événement de conversion dont vous effectuez le suivi.
* **Nombre de conversions** : nombre total de conversions qui se sont produites pour chaque événement.
* **Revenu estimé** : valeur estimée attribuée à chaque événement de conversion.

Consultez ce tableau pour évaluer l’efficacité de votre campagne à générer les actions souhaitées.

![Conversions cumulées.](/help/assets/collaborate/measure/cumulative-conversions.png)

### Conversions par jour {#conversions-by-day}

Ce graphique fournit une répartition quotidienne des conversions pour chaque événement configuré lors de la création d’un rapport d’attribution. Utilisez cette vue pour découvrir des modèles quotidiens, identifier les périodes d’activité de conversion élevée ou faible, et comparer l’exécution de différents événements de conversion sur la chronologie de votre campagne.

![Conversions par jour.](/help/assets/collaborate/measure/conversions-by-day.gif)

## Créer un rapport de mesure {#create-measurement-report}

Dans Collaboration, vous pouvez créer deux principaux types de rapports de mesure :

* **Résumé de la campagne** : fournit des mesures de haut niveau telles que la portée, les impressions, la fréquence moyenne et la diffusion par canal, ce qui donne un aperçu rapide des performances globales de la campagne.
* **Attribution** : mesure la manière dont les expositions des campagnes génèrent des actions en aval telles que des conversions ou des achats, ce qui vous aide à comprendre l’efficacité des campagnes.

Vous pouvez exécuter le rapport de synthèse de la campagne seul, tandis que le rapport d&#39;attribution nécessite que les deux types de rapports soient sélectionnés ensemble.

### Créer un rapport de synthèse de campagne {#create-campaign-summary-report}

Les éditeurs et les annonceurs peuvent générer des rapports **Résumé de la campagne** pour évaluer les performances de la campagne. Utilisez ces rapports pour obtenir des informations sur les mesures clés telles que [portée](#cumulative-reach-curve), [fréquence](#frequency-distribution) et [impressions](#impressions-by-placement) et comprendre comment votre campagne a été diffusée et son impact global.

Pour générer un rapport **Résumé de la campagne**, accédez à l’espace de travail du projet à partir de l’espace de travail **[!UICONTROL Collaborateur]**. Dans l’onglet **[!UICONTROL Mesure]**, sélectionnez l’icône Ajouter (![Ajouter une icône.](/help/assets/icons/plus.png)) puis sélectionnez **[!UICONTROL Mesure]**.

S’il s’agit de votre premier rapport, vous pouvez également sélectionner l’option **[!UICONTROL Exécuter le rapport]**.

![Onglet Mesure mettant en surbrillance les options Exécuter le rapport et Mesure](/help/assets/collaborate/measure/run-measure-report.png).

L’écran **[!UICONTROL Créer un rapport de mesure]** s’affiche avec des informations et des champs de saisie regroupés sous les sections **[!UICONTROL Détails de facturation]**, **[!UICONTROL Détails de la campagne]** et **[!UICONTROL Détails du rapport]**.

#### Détails de facturation {#billing-details}

Cette section explique comment les crédits sont utilisés lors de la génération des rapports de mesure. La responsabilité du crédit est établie lors de la [configuration de la connexion](../connect/establishing-connections.md#credit-split). Avant d’exécuter des rapports, vérifiez et confirmez les paramètres de répartition du crédit et les rôles de reporting avec votre collaborateur.

#### Détails de la campagne {#campaign-details}

Dans la section **[!UICONTROL Détails de la campagne]**, sélectionnez l’**ID publicitaire** approprié à associer à votre rapport. Ces noms ou identifiants publicitaires ont été ajoutés lors de la [configuration de la connexion](../connect/establishing-connections.md#advertiser-names). Si un seul nom a été configuré, il s’affiche par défaut. Si aucun nom n’a été configuré, le champ **[!UICONTROL ID de l’annonceur (nom)]** est désactivé et prérempli avec le nom du compte de l’annonceur.

![Écran Créer un rapport de mesure affichant l’option ID de l’annonceur (nom) désactivée.](/help/assets/collaborate/measure/advertiser-id.png)

Sélectionnez ensuite la campagne souhaitée dans le menu déroulant **[!UICONTROL Identifiant de campagne]**. Ce menu répertorie tous les identifiants de campagne saisis par l’éditeur pour votre projet. Si la campagne dont vous avez besoin n’est pas disponible, [ajoutez-la dans l’interface utilisateur](./manage-projects.md#manage-campaign-id) avant de générer le rapport.

![Écran Créer un rapport de mesure affichant le menu déroulant de l’identifiant de campagne développé.](/help/assets/collaborate/measure/campaign-id.png)

Indiquez ensuite la période sur laquelle vous souhaitez que le rapport porte. Sélectionnez **[!UICONTROL Période du rapport]**, puis utilisez le calendrier pour choisir les dates de début et de fin.

![Écran Créer un rapport de mesure affichant le calendrier de la période du rapport.](/help/assets/collaborate/measure/report-date-range.png)

#### Détails du rapport {#report-details}

**Date d’exécution du rapport**

Dans la section **[!UICONTROL Détails du rapport]**, choisissez la date d’exécution du rapport. Sélectionnez **[!UICONTROL Date d’exécution de l’état]** et choisissez la date souhaitée dans le calendrier.

* Si vous choisissez la date d’aujourd’hui ou une date dans le passé, le rapport **Résumé de la campagne** s’exécute immédiatement.
* Si vous choisissez une date ultérieure, l&#39;exécution du rapport **Synthèse de la campagne** est planifiée ce jour-là.

![Écran Créer un état de mesure affichant le calendrier de date d&#39;exécution de l&#39;état.](/help/assets/collaborate/measure/report-run-date.png)

**Type de rapport**

* Si vous êtes un annonceur, vous pouvez sélectionner le type de rapport **[!UICONTROL Résumé de la campagne]** parmi les options disponibles. Seuls les annonceurs peuvent générer des rapports d’attribution.
* Si vous êtes un éditeur, le type de rapport **[!UICONTROL Résumé de la campagne]** est présélectionné et ne peut pas être modifié. Actuellement, les éditeurs ne peuvent pas exécuter de rapports d’attribution.

![Écran Créer un rapport de mesure affichant l’option Résumé de la campagne en tant que type de rapport présélectionné et non modifiable.](/help/assets/collaborate/measure/cs-report-type.png)

Enfin, vérifiez vos paramètres et sélectionnez **[!UICONTROL Créer]**. Le rapport de synthèse de la campagne est généré immédiatement si la date d&#39;exécution est aujourd&#39;hui ou antérieure, ou à la date future choisie. Vous pouvez modifier le rapport planifié avant sa date d’exécution. Pour obtenir des instructions détaillées, reportez-vous à la section [Modifier le rapport de mesure].

Une fois disponible, vous pouvez afficher votre rapport à tout moment dans l’onglet **[!UICONTROL Mesure]** de l’espace de travail du projet.

![Écran Créer un rapport de mesure affichant les informations et l’option Créer mise en surbrillance.](/help/assets/collaborate/measure/cs-review.png)

### Créer un rapport d’attribution {#create-attribution-report}

En tant qu’annonceur, vous pouvez générer des rapports **Attribution** pour évaluer la manière dont l’exposition à vos campagnes contribue aux résultats clés, tels que les inscriptions ou les achats. Utilisez ces rapports pour comprendre les interactions des utilisateurs avec votre campagne, identifier les points de contact qui génèrent le plus d’impact et éclairer des stratégies marketing plus efficaces.

>[!IMPORTANT]
>
> Vous devez [générer vos données de mesure](../setup/onboard-measurement-data.md#add-measurement-data) dans Collaboration avant de générer des rapports d’attribution.
>![L’onglet Mesure avec les exigences relatives aux données de mesure et l’option Mesure désactivée.](/help/assets/collaborate/measure/require-measurement-data.png)

Pour générer un rapport **Attribution**, accédez à l’espace de travail du projet à partir de l’espace de travail **[!UICONTROL Collaborateur]**. Dans l’onglet **[!UICONTROL Mesure]**, sélectionnez l’icône Ajouter (![Ajouter une icône.](/help/assets/icons/plus.png)) puis sélectionnez **[!UICONTROL Mesure]**.

S’il s’agit de votre premier rapport, vous pouvez également sélectionner l’option **[!UICONTROL Exécuter le rapport]**.

![Onglet Mesure mettant en surbrillance les options Exécuter le rapport et Mesure](/help/assets/collaborate/measure/run-measure-report-attribution.png).

L’écran **[!UICONTROL Créer un rapport de mesure]** s’affiche avec des informations et des champs de saisie regroupés sous les sections **[!UICONTROL Détails de facturation]**, **[!UICONTROL Détails de la campagne]** et **[!UICONTROL Détails du rapport]**.

Lisez et suivez les étapes de la section [Créer un rapport de synthèse de campagne](#create-campaign-summary-report) pour configurer les paramètres suivants :

* [Détails de facturation](#billing-details)
* [Détails de la campagne](#campaign-details)

#### Détails des rapports pour les rapports d’attribution {#report-details-attribution}

**Date d’exécution du rapport**

>[!IMPORTANT]
>
> Pour les rapports d’attribution, la date d’exécution du rapport doit être une date ultérieure et doit se produire au moins un jour après la date de fin de votre période de rapport, plus la durée complète de l’intervalle de recherche en amont défini.
> **Date d’exécution du rapport ≥ date de fin du rapport + intervalle de recherche en amont + 1**
> 
> Par exemple, si votre période de rapport se termine le 15 juin et que l’intervalle de recherche en amont est de 14 jours, la date d’exécution du rapport est le 30 juin ou une date ultérieure.

Dans la section **[!UICONTROL Détails du rapport]**, choisissez la date d’exécution du rapport. Sélectionnez **[!UICONTROL Date d’exécution de l’état]** et choisissez la date souhaitée dans le calendrier.

**Type de rapport**

En tant qu’annonceur, vous pouvez sélectionner **[!UICONTROL Attribution]** comme type de rapport en plus du **[!UICONTROL Résumé de la campagne]**. Lorsque vous choisissez le rapport d’attribution, vos résultats incluent les mesures standard de résumé de la campagne et l’analyse d’attribution détaillée, fournissant ainsi une vue complète des performances de la campagne.

![Écran Créer un rapport de mesure mettant en surbrillance les types de rapports Synthèse de la campagne et Attribution sélectionnés.](/help/assets/collaborate/measure/attribution-report-type.png)

Lorsque vous sélectionnez **[!UICONTROL Attribution]** comme type de rapport, une section de configuration **[!UICONTROL Attribution]** s’affiche avec les paramètres supplémentaires requis :

* **Intervalle de recherche en amont en jours** : définit la durée pendant laquelle le rapport prend en compte les impressions de campagne avant chaque conversion. Seules les impressions au cours de cette période sont éligibles au crédit d’attribution.
* **Événements de conversion** : indique les actions de conversion que vous souhaitez mesurer, par exemple les achats ou les inscriptions. Ces événements doivent être configurés à l’avance lorsque vous [source des données de mesure](../setup/onboard-measurement-data.md#add-conversion-event) dans Collaboration.

Tout d’abord, saisissez une valeur pour le champ **[!UICONTROL Intervalle de recherche en amont en jours]** ou ajustez-le à l’aide des options d’incrémentation/décrémentation.

![Écran Créer un rapport de mesure mettant en surbrillance la valeur de l’intervalle de recherche en amont en jours.](/help/assets/collaborate/measure/lookback-window-in-days.png)

Sélectionnez ensuite jusqu’à **3** événements de conversion dans la liste disponible. Pour plus d’informations sur un événement particulier, sélectionnez l’icône **[!UICONTROL i]** pour en afficher les détails.

![Écran Créer un rapport de mesure mettant en surbrillance les événements de conversion sélectionnés et les informations de l’événement d’achat.](/help/assets/collaborate/measure/attribution-conversion-events.png)

Enfin, passez en revue vos paramètres et sélectionnez **[!UICONTROL Créer]** pour planifier le rapport. Votre rapport d’attribution sera généré à la date d’exécution spécifiée. Vous pouvez modifier le rapport planifié avant sa date d’exécution. Pour obtenir des instructions détaillées, reportez-vous à la section [Modifier le rapport de mesure].

Une fois disponible, vous pouvez afficher votre rapport à tout moment dans l’onglet **[!UICONTROL Mesure]** de l’espace de travail du projet.

![Écran Créer un rapport de mesure affichant les informations et l’option Créer mise en surbrillance.](/help/assets/collaborate/measure/attribution-review.png)
