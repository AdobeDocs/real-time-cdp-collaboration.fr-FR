---
title: Création de rapports de mesure Amazon Marketing Cloud
description: Découvrez comment créer et interpréter des rapports de mesure pour les campagnes Amazon Marketing Cloud dans Real-Time CDP Collaboration.
audience: advertiser
keywords: AMC, Amazon Marketing Cloud, rapports de mesure, résumé de la campagne, attribution, Real-Time CDP Collaboration
solution: Real-Time Customer Data Platform Collaboration
badgelimitedavailability: label="Disponibilité limitée" type="Informative" url="https://helpx.adobe.com/fr/legal/product-descriptions/real-time-customer-data-platform-collaboration.html newtab=true"
source-git-commit: 944914557c10b43abbe4915e061c219aca9f783f
workflow-type: tm+mt
source-wordcount: '1574'
ht-degree: 5%

---


# Création de rapports de mesure [!DNL Amazon Marketing Cloud] {#amc-measurement-reports}

{{limited-availability-release-note}}

Utilisez l’onglet **[!UICONTROL Mesure]** dans un projet [!DNL Amazon Marketing Cloud] ([!DNL AMC]) pour passer en revue la portée de l’audience, la fréquence et les résultats de conversion. Après avoir créé un projet AMC, créez des rapports de mesure pour les campagnes qui ont déjà été exécutées à l’aide des données disponibles dans votre instance [!DNL AMC].

>[!IMPORTANT]
>
>L’onglet **[!UICONTROL Mesure]** affiche « Aucune donnée de mesure disponible » jusqu’à ce que les requêtes de configuration des données d’arrière-plan soient terminées. Ce processus peut prendre jusqu’à 24 heures. Si le message persiste au-delà de 24 heures, consultez la section [Dépannage](#troubleshooting).


## Création d’un rapport {#create-report}

Pour créer un rapport de mesure [!DNL AMC], suivez les étapes décrites dans la section [Créer un rapport de synthèse de campagne](../measure.md#create-campaign-summary-report-create-campaign-summary-report).

![Formulaire de rapport de mesure affichant les champs ID publicitaire, ID de campagne, Période du rapport, Date d’exécution du rapport, Nom du rapport et Type de rapport.](../../../assets/collaborate/advertising-platforms/create-measurement-report.png){zoomable="yes"}

### Détails de la campagne {#campaign}

L’**[!UICONTROL ID publicitaire]** identifie le compte [!DNL Amazon Advertising] associé à l’instance [!DNL AMC]. [!DNL AMC] utilise ce contexte de compte pour récupérer les campagnes pour la mesure.

La liste **[!UICONTROL Identifiant de campagne]** est automatiquement renseignée avec les campagnes disponibles dans l’instance [!DNL AMC] connectée. Une campagne s’affiche uniquement si elle se situe dans l’intervalle de recherche en amont de découverte par défaut et si elle comporte suffisamment d’utilisateurs uniques pour respecter le seuil d’agrégation minimal de [!DNL AMC]. Sélectionnez la campagne dont vous souhaitez mesurer l’activité [!DNL Amazon Ads].

Si la campagne dont vous avez besoin n’est pas répertoriée, vérifiez qu’elle appartient au compte [!DNL Amazon Ads] connecté et consultez la section [Dépannage](#troubleshooting). Pour plus d’informations sur le seuil, consultez la documentation [AMC aggregation threshold](https://advertising.amazon.com/API/docs/en-us/guides/amazon-marketing-cloud/aggregation-threshold).

#### Période, date d’exécution et nom du rapport {#dates}

>[!CONTEXTUALHELP]
>id="rtcdp_collaboration_amc_measure_report_date_range"
>title="Période"
>abstract="Définissez les dates de début et de fin des données de la campagne à inclure dans le rapport. La période est limitée à un intervalle de recherche en amont de 365 jours, avec une durée maximale de 90 jours. Vous pouvez uniquement créer des rapports sur les campagnes précédentes."

>[!CONTEXTUALHELP]
>id="rtcdp_collaboration_amc_measure_report_run_date"
>title="Date d’exécution"
>abstract="Date d&#39;exécution du rapport. Doit être au moins un jour après la date de fin du rapport et peut être jusqu&#39;à 46 jours à l&#39;avenir."

>[!NOTE]
>
>Vous pouvez uniquement créer des rapports sur les campagnes qui ont déjà été exécutées.

Définissez la **[!UICONTROL Période du rapport]** sur la période d’exécution de la campagne [!DNL AMC] sélectionnée. [!DNL AMC] prend en charge un intervalle de recherche en amont de 365 jours avec une durée maximale de 90 jours.

Définissez la **[!UICONTROL date d’exécution du rapport]**. Il s’agit de la date d’exécution du rapport. La date d’exécution doit se situer au moins un jour après la date de fin du rapport et peut atteindre 46 jours à l’avenir. Pour l&#39;ensemble complet des contraintes de date, voir [Référence des contraintes AMC](#constraints).

>[!TIP]
>
>Pour les rapports d’attribution dont la période se situe dans les 30 jours suivant la date actuelle, définissez la date d’exécution à 30 jours dans le futur pour vous assurer que toutes les conversions dans l’intervalle de recherche en amont fixe de 30 jours ont été capturées avant l’exécution du rapport.

#### Type de rapport {#report-type}

Tous les rapports [!DNL AMC] incluent un **[!UICONTROL résumé de la campagne]**. Vous pouvez éventuellement inclure des données **[!UICONTROL Attribution]** pour mesurer si les impressions de campagne ont entraîné des actions des clients, telles que des achats ou des inscriptions, dans une fenêtre de 30 jours après l’exposition de l’annonce publicitaire. L’attribution nécessite que les événements de conversion appropriés soient disponibles dans votre instance [!DNL AMC]. Pour les campagnes axées sur la portée ou la sensibilisation, le **[!UICONTROL résumé de la campagne]** fournit les mesures de diffusion dont vous avez besoin.

| Type de rapport | Description |
| --- | --- |
| **[!UICONTROL Résumé de la campagne]** | Fournit des mesures de portée, de fréquence et d’impression pour la campagne sélectionnée. Toujours inclus. |
| **[!UICONTROL Attribution]** | Ajoute les données de conversion au rapport. Disponible uniquement s’il existe des événements de conversion dans votre instance [!DNL AMC]. Voir [&#x200B; Événements de conversion &#x200B;](#conversion-events). |

#### Événements de conversion (attribution uniquement) {#conversion-events}

>[!CONTEXTUALHELP]
>id="rtcdp_collaboration_amc_attribution_lookback_period"
>title="Période de rétrospection d’attribution"
>abstract="AMC applique une fenêtre d’attribution fixe de 30 jours : les conversions qui se produisent jusqu’à 30 jours après la dernière impression peuvent être attribuées aux impressions à l’intérieur de la période du rapport. Cette valeur n’est pas modifiable. Planifiez la date d’exécution du rapport au moins 30 jours après la fin de la période pour vous assurer que toutes les conversions éligibles sont capturées."

>[!CONTEXTUALHELP]
>id="rtcdp_collaboration_amc_measure_conversion_events"
>title="Événements de conversion"
>abstract="Sélectionnez jusqu’à trois événements de conversion à inclure dans le rapport d’attribution. Les événements disponibles sont découverts automatiquement à partir de votre instance [!DNL AMC]. Si aucun événement n’apparaît, il se peut que votre instance [!DNL AMC] ne contienne aucun événement de conversion enregistré et que l’attribution ne soit pas disponible."

>[!NOTE]
>
>Les données d’attribution nécessitent que les événements de conversion soient configurés dans votre instance [!DNL AMC]. Si [!UICONTROL Attribution] n’est pas disponible ou n’a pas été sélectionné, ignorez cette section et sélectionnez **[!UICONTROL Créer]** pour envoyer le formulaire.

Pour les rapports [!UICONTROL Attribution], [!DNL AMC] applique un intervalle de recherche en amont d’attribution fixe de 30 jours. Impossible d’ajuster ce paramètre.

![La section Événements de conversion du formulaire de rapport de mesure dans son état actif, affichant le champ Intervalle de recherche en amont défini sur 30 jours et la liste à sélection multiple Événements de conversion avec les événements disponibles.](../../../assets/collaborate/advertising-platforms/conversion-events-active.png){zoomable="yes"}

Les événements de conversion représentent les actions client sur site suivies par [!DNL Amazon Ads], telles qu’un achat, un ajout de liste de souhaits, une action de panier ou une vue détaillée de produit. Les rapports d’attribution prennent en charge jusqu’à trois événements. Sélectionnez les événements qui correspondent aux résultats de la campagne que vous souhaitez mesurer. Si l’option [!UICONTROL Attribution] n’est pas disponible, voir [Dépannage](#troubleshooting).

Une fois le rapport créé, il apparaît dans l’onglet **[!UICONTROL Mesure]** avec un statut planifié ou en attente. À la date d’exécution configurée, [!DNL AMC] traite la requête de rapport et renvoie les résultats dans les 24 heures.

![Onglet Mesure affichant une nouvelle carte de rapport de mesure avec un indicateur de statut planifié, le nom du rapport, la date d&#39;exécution et le type de rapport visibles.](../../../assets/collaborate/advertising-platforms/measurement-report-pending.png){zoomable="yes"}


## Affichage d’un rapport {#view-report}

Une fois le rapport exécuté, les résultats sont disponibles dans l’onglet **[!UICONTROL Mesure]** de votre projet [!DNL AMC]. Recherchez votre rapport et sélectionnez **[!UICONTROL Afficher le rapport complet]** pour consulter les résultats.

![Onglet Mesure d’un projet [!DNL AMC] affichant une fiche rapport terminée avec sa date d’exécution, son type de rapport et le bouton Afficher le rapport complet en surbrillance.](../../../assets/collaborate/advertising-platforms/view-full-report.png){zoomable="yes"}

Le rapport affiche les résultats disponibles pour le type de rapport sélectionné. Les rapports **[!UICONTROL Résumé de la campagne]** affichent les résultats des diffusions pour la campagne Amazon sélectionnée.

![Les visualisations du résumé de la campagne affichent les totaux du résumé, la distribution des impressions, la distribution des fréquences, la courbe d’étendue et les impressions par emplacement.](../../../assets/collaborate/advertising-platforms/campaign-summary-widgets.png){zoomable="yes"}

Les rapports qui incluent **[!UICONTROL Attribution]** affichent également l’activité de conversion associée aux événements de conversion Amazon Ads sélectionnés.


![Les visualisations Attribution présentant les conversions et conversions cumulées par graphique journalier.](../../../assets/collaborate/advertising-platforms/attribution-report-conversion-widgets.png){zoomable="yes"}

Pour plus d&#39;informations sur l&#39;interprétation des résultats des rapports, voir [Mesurer les performances](../measure.md#view-reports-view-reports).

## [!DNL AMC] de référence des contraintes {#constraints}

Les contraintes suivantes s&#39;appliquent à tous les rapports de mesure [!DNL AMC].

| Contrainte | Valeur |
| --- | --- |
| Début de la période d&#39;état au plus tôt | 365 jours avant la date actuelle |
| Fin de la dernière période du rapport | 45 jours après la date actuelle. Utilisez cette option pour préconfigurer un rapport pour une campagne toujours en cours d’exécution et qui se terminera dans les 45 prochains jours ; le rapport s’exécute automatiquement à sa date d’exécution planifiée une fois la campagne terminée. |
| Période maximale du rapport | 90 jours |
| Intervalle de recherche en amont d’attribution | 30 jours (fixe pour [!DNL AMC]) |
| Date minimale d’exécution | Au moins 1 jour après la date de fin du rapport |
| Date maximale d’exécution | 46 jours dans le futur |
| Nombre maximal d’événements de conversion par rapport | 3 |
| Sélection de la campagne | Campagne unique par rapport |
| Modification de rapports | Non disponible. Le rapport existant est conservé. [Créer un rapport](#create-report) lorsque des modifications sont requises |

## Dépannage {#troubleshooting}

**Aucune Donnée De Mesure Disponible**

L’onglet **[!UICONTROL Mesure]** indique « Aucune donnée de mesure disponible » jusqu’à ce que les requêtes de configuration des données d’arrière-plan déclenchées lors de la création du projet soient terminées. Cela peut prendre jusqu’à 24 heures. Si le message « Aucune donnée de mesure disponible » persiste après 24 heures, vérifiez que votre instance [!DNL AMC] comporte des campagnes qui se sont exécutées au cours des trois derniers mois, car il s’agit de l’intervalle de recherche en amont par défaut utilisé lors de la découverte de la campagne. Si des campagnes éligibles existent et que le message persiste, vérifiez le statut de votre campagne dans votre compte [Amazon Ads](https://advertising.amazon.com/sign-in){target="_blank"}.

**Aucune campagne n’apparaît dans le menu déroulant [!UICONTROL Identifiant de campagne]**

Les campagnes peuvent être absentes même lorsque l’onglet **[!UICONTROL Mesure]** est visible. [!DNL AMC] applique un seuil utilisateur minimum aux données de la campagne. Les campagnes qui ne respectent pas le seuil minimum d’utilisateurs uniques sont exclues et les requêtes de rapport ne renvoient aucun résultat. Vérifiez que les campagnes pour lesquelles vous souhaitez créer des rapports ont une portée suffisante. Pour plus d’informations sur les seuils d’agrégation de [!DNL AMC], consultez la documentation sur le [seuil d’agrégation de l’AMC](https://advertising.amazon.com/API/docs/en-us/guides/amazon-marketing-cloud/aggregation-threshold){target="_blank"}.

**Les résultats ne sont pas visibles après la date d’exécution**

Patientez jusqu’à 24 heures après la date d’exécution planifiée pour que [!DNL AMC] traite les requêtes de rapport et renvoie les résultats. Si le rapport reste en attente après cette période, vérifiez que la date d’exécution est dépassée et que le statut du rapport ne s’affiche plus comme étant en attente.

**Les événements de conversion ne sont pas disponibles et [!UICONTROL Attribution] est grisé**

Cela peut se produire pour trois raisons :

1. **Le suivi des conversions n’est pas activé.** Le suivi des conversions n’est peut-être pas configuré sur votre compte [!DNL AMC] Advertiser. Accédez à votre compte [Amazon Ads](https://advertising.amazon.com/sign-in){target="_blank"} et vérifiez que les événements de conversion font l’objet d’un suivi pour les campagnes appropriées.
2. **Aucun événement de conversion enregistré.** Même si le suivi est activé, votre instance [!DNL AMC] n’a peut-être pas encore enregistré d’événements de conversion.
3. **Seuil d’agrégation non atteint.** [!DNL AMC] applique un seuil minimum aux données de conversion. Si un type d’événement de conversion ne comporte pas un nombre suffisant d’occurrences, il ne sera pas renvoyé et n’apparaîtra pas dans la liste.

**Les conversions semblent inférieures aux prévisions**

Si la date d’exécution du rapport est inférieure à 30 jours après la fin de la période, [!DNL AMC] n’avez peut-être pas capturé toutes les conversions dans la fenêtre d’attribution. [Créez un rapport](#create-report) avec une date d’exécution postérieure d’au moins 30 jours à la fin de la période.

## Étapes suivantes {#next-steps}

Utilisez les résultats du rapport pour évaluer les performances de la campagne et informer la planification des campagnes à venir en [!DNL Amazon Advertising]. Vous pouvez, par exemple, ajuster le ciblage, supprimer les audiences surexposées identifiées dans la distribution de fréquence ou réaffecter les dépenses à des emplacements hautement performants. Pour analyser une autre campagne ou une autre période de compte rendu des performances, créez un autre rapport de mesure avec les paramètres appropriés.

Pour obtenir un aperçu de toutes les fonctionnalités de collaboration [!DNL AMC] disponibles, voir [[!DNL Amazon Marketing Cloud]](./amc.md).
