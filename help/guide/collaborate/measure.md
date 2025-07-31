---
title: Mesurer les performances
description: Mesurez les performances de vos campagnes sur différents canaux. Découvrez comment utiliser et interpréter divers rapports.
audience: admin, publisher, advertiser
badgelimitedavailability: label="Disponibilité limitée" type="Informative" url="https://helpx.adobe.com/legal/product-descriptions/real-time-customer-data-platform-collaboration.html newtab=true"
exl-id: c92b263e-1f96-49f1-841a-ef2e97a4cb9a
source-git-commit: a7215d453021be578a32ce1af4d659845c3b8493
workflow-type: tm+mt
source-wordcount: '575'
ht-degree: 19%

---

# Mesurer les performances

{{limited-availability-release-note}}

>[!IMPORTANT]
>
>L’espace de travail **[!UICONTROL Mesure]** n’est disponible que si le cas d’utilisation **Mesure** a été activé [pendant le processus de connexion](../connect/establishing-connections.md#connection-settings). Pour plus d’informations sur les cas d’utilisation, consultez le guide [gestion des projets](./manage-projects.md#project-use-cases).

Découvrez les rapports disponibles dans Adobe Real-Time CDP Collaboration et comment mesurer et analyser les performances de vos campagnes marketing sur différents canaux.

## Conditions préalables

Avant de pouvoir accéder aux rapports de mesure dans Collaboration, vous avez déjà :

* [Connecté](/help/guide/connect/establishing-connections.md) avec un collaborateur avec le cas d’utilisation **Measurement** activé et a commencé à collaborer sur [projets](/help/guide/collaborate/manage-projects.md)
* Exécutez une campagne et [téléchargez les données de mesure](/help/guide/setup/onboard-measurement-data.md) dans Collaboration.

<!--

## Create a report {#create-report}

Hidden until functionality is live. At that point, move the contextualhelp from below into this section. 

The syntax rtcdp_collaboration_measurement_create_report is currently implemented in the UI. However, a preference would be to imlement the other contextualhelp ID from below instead, since that explicitly includes campaignID in the syntax. Need to sync up with UI team. More details in CORE-116991.

-->

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

![Comment accéder à l’onglet Mesure dans un projet ](/help/assets/collaborate/measure/measurement.gif).

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
