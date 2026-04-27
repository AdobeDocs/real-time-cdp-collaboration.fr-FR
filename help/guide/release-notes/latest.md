---
title: Latest Real-Time CDP Collaboration Release Notes
description: Follow the latest releases for Real-Time CDP Collaboration
audience: admin, publisher, advertiser
badgelimitedavailability: label="Disponibilité limitée" type="Informative" url="https://helpx.adobe.com/fr/legal/product-descriptions/real-time-customer-data-platform-collaboration.html newtab=true"
exl-id: 8513c648-1cc1-4544-b86d-2ee3193ab60f
TQID: https://experienceleague.adobe.com/re4oFblCLiZpspWIS7D4EEYNh36EDhULEOd2-ccXH28
product_v2:
  - id: fdddec33-c9cb-4459-b8b6-2664395a6f10
feature_v2:
  - id: ba929a52-9339-4154-9487-317dc875a3c7
topic_v2:
  - id: a004cc84-67b9-4a33-a3a7-8ec7273ef4dc
  - id: c1579802-ddd4-4214-8a91-97b2066abe11
  - id: c2be0313-b3ae-45e0-b454-d20bf54b23f2
  - id: e1e0219c-f879-479f-8427-888ed2a6e9c2
  - id: ebde5b41-29c9-4f5e-9ef6-1197e85409e3
source-git-commit: 3ce7e66b31332836fd6cc6137c94622436505cc9
workflow-type: tm+mt
source-wordcount: 1461
ht-degree: 2%

---

# Latest Real-Time CDP Collaboration Release Notes

{{limited-availability-release-note}}

**Last update**: January 2026.

These release notes cover the functionality released in Adobe Real-Time CDP Collaboration. Collaboration releases operate on a continuous delivery model, which allows for an approximate monthly release cadence. These release notes get updated often, so be sure to check them regularly.

## Janvier 2026 {#january-2026}

Real-Time CDP Collaboration now supports CSV file upload as a new method for sourcing audiences, as well as new mobile match keys (IDFA and GAID) for enhanced audience matching and measurement.

**Fonctionnalités nouvelles ou mises à jour**

| Fonctionnalité | Description |
| ------- | ----------- |
| CSV upload for Audience Sourcing | Upload CSV files to source audiences into Collaboration directly from the UI. Ideal for onboarding first-party data for short-term collaboration projects. For more information, see the [upload CSV file for audience sourcing guide](../setup/upload-csv-audience-sourcing.md). |
| Mobile Match Key Support | Collaboration now supports mobile match keys, including IDFA and GAID, for audience matching and measurement. These match keys are selected during account setup and can then be used when configuring connection settings for new connections and in downstream collaboration workflows. See the [Match keys setup guide](../setup/onboard-account.md#set-up-match-keys) for more details. |

{style="table-layout:auto"}

## Décembre 2025 {#december-2025}

Real-Time CDP Collaboration is now available to customers in **Europe, the Middle East, and Africa (EMEA))**. It is automatically available to Real-Time CDP Prime and Ultimate customers in these regions.

## Août 2025 {#august-2025}

Real-Time CDP Collaboration is now available to customers in **Canada**. It is automatically available to Real-Time CDP Prime and Ultimate customers in these regions.

* Collaboration now supports the following [match keys](../setup/onboard-account.md#supported-match-keys):
   * E-mail haché
   * Hashed phone number
   * ID de CRM
   * ID de fidélité
   * IPv4 haché
   * ID AdFixus
* Multiple match keys are now available across Collaboration, giving you the ability to expand your audience size and improve match rates. Multiple match keys can be used when sourcing audiences, establishing connections, and activating audiences. To learn more about using multiple match keys, read the [set up match keys](../setup/onboard-account.md) and [sourcing audiences](../setup/onboard-audiences.md#map-fields) guides.

>[!IMPORTANT]
>
>Lors de l’activation des audiences où plusieurs clés de correspondance sont utilisées, si une ou plusieurs clés de correspondance ne se chevauchent pas, ne génèrent aucun nombre de profils des audiences ou se situent sous le seuil, l’activation entière échoue. Assurez-vous que vos audiences disposent d’un chevauchement suffisant et respectent le seuil minimum de 1 000 identifiants sur toutes les clés de correspondance avant d’activer.

* The Adobe Experience Platform destination now supports activating audiences with multiple match keys. Additionally, you can now used a linked key when configuring your destination&#39;s mapping to specify which match key is sent during activation. To learn more, read the [Experience Platform destination](../destinations/experience-platform.md#linked-keys) guide.
* Collaborators can now edit multiple audiences at once. You can now edit audience metadata, connection access, names, descriptions, and categories for multiple audiences using the bulk edit tool. To learn more about editing audiences, read the [manage audiences](../setup/onboard-audiences.md#edit-audiences) guide.

## Juillet 2025 {#july-2025}

Real-time CDP Collaboration now supports brand-to-brand collaboration. Collaborators can now form connections, regardless of whether they are an advertiser or publisher. This allows for more flexible collaboration opportunities and enables brands to leverage each other&#39;s data and insights. To learn more about the differences between brand-to-brand collaboration and advertiser-to-publisher collaboration, read the [collaboration patterns](../overview/collaboration-patterns.md) guide.

* Collaborators can now connect to each other using [private connection invites](../connect/establishing-connections.md#private-connection-invites). Share your account&#39;s unique connect code with a collaborator who can then use it to connect with you directly. This is a core feature of brand-to-brand collaboration, allowing collaborators to establish connections beyond advertisers exploring the **[!UICONTROL Discover collaborators]** directory.
* [Self-serve destinations](../setup/manage-destinations.md) are now available to both advertisers and publishers.
* Audience activation is now available for both collaborators in a connection, regardless of their [account role](../overview/roles.md). Audience activation settings are configured while [establishing connections](../connect/establishing-connections.md#configure-connection-settings), allowing you to specify which collaborator can activate audiences. To learn more about audience activation, read the [activate audiences](../collaborate/activate.md) guide.
* The **[!UICONTROL Activate]** use case has been reconfigured to support brand-to-brand collaboration. The **[!UICONTROL Activate]** tab within a project now displays the audiences that have been sent to your collaborator, and the audiences activated to your destination by your collaborator. To learn more, read the [activate audiences](../collaborate/activate.md) guide. <br> ![Tableau de bord d’activation avec les sections Audiences envoyées à et Audiences activées.](/help/assets/release-notes/2025/activate-dashboard.png){zoomable="yes"}
* Les scores d’index d’audience sont désormais disponibles dans l’onglet **[!UICONTROL Découvrir]** d’un projet. Le score de l’index d’audience est une mesure de la façon dont une audience correspond à l’audience de votre collaborateur. Ce score est calculé en fonction des nombres de profils des audiences et des chevauchements sous-jacents. Pour en savoir plus sur les scores d’index d’audience, consultez le guide [score d’index d’audience](../collaborate/discover.md#audience-index-score) .

## Mai 2025 {#may-2025}

* Real-Time CDP Collaboration est désormais disponible pour les clients en **Australie** et **Nouvelle-Zélande**. Il est automatiquement disponible pour les clients Real-Time CDP Prime et Ultimate dans ces régions.
* Real-Time CDP Collaboration propose désormais des [destinations en libre-service](../setup/manage-destinations.md) par le biais de l’onglet **[!UICONTROL Mes destinations]** dans la section **[!UICONTROL Configuration]**. Les destinations vous permettent d’activer des audiences dans des plateformes tierces, telles que des réseaux publicitaires ou des plateformes de gestion de données, afin d’atteindre vos clients sur divers canaux. Actuellement, seules les destinations Adobe Experience Platform sont prises en charge. Si vous souhaitez configurer une autre destination, contactez votre représentant ou représentante Adobe. Pour en savoir plus sur les destinations, consultez le guide [présentation des destinations](../destinations/overview.md).
   * Les destinations prennent également en charge l’affichage des audiences Collaboration dans le portail d’audiences [Adobe Experience Platform](https://experienceleague.adobe.com/fr/docs/experience-platform/segmentation/ui/audience-portal.md#manage-audiences).
* Vous pouvez désormais modifier la fréquence d’actualisation de l’audience pour les connexions de données existantes dans Collaboration. Actuellement, vous pouvez choisir d’actualiser vos audiences tous les jours ou tous les deux à six jours. Pour en savoir plus sur la modification de la fréquence d’actualisation de l’audience, consultez le guide [gérer les connexions de données](../setup/manage-data-connection.md#scheduling).
* Les répartitions de crédit entre collaborateurs sont désormais définies pour chaque cas d’utilisation sélectionné dans la connexion. Vous pouvez définir différentes règles de consommation de crédit pour chaque cas d’utilisation afin de mieux contrôler l’utilisation de vos crédits. Pour en savoir plus sur la fonctionnalité de partage du crédit, consultez le guide [Paramètres de connexion](../connect/establishing-connections.md#connection-settings). Pour en savoir plus sur la manière dont les crédits sont consommés, lisez le guide [types d’activité de crédit](../setup/my-activity.md#types-of-activities). <br> ![Écran des paramètres de connexion affichant la fonctionnalité de répartition du crédit.](/help/assets/release-notes/2025/credit-split.png){zoomable="yes"}
* Les éditeurs peuvent désormais définir les noms et identifiants des annonceurs avant d’accepter les paramètres de connexion d’un annonceur. Les éditeurs peuvent définir des noms et des identifiants qui s’alignent sur leurs systèmes internes, qui peuvent être différents des noms et des identifiants de l’annonceur. Pour en savoir plus sur l’ajout de noms et d’identifiants d’annonceurs, consultez le guide [Paramètres de connexion](../connect/establishing-connections.md#connection-settings.md). <br> ![Écran des paramètres de connexion affichant le paramètre de l’éditeur, les noms et identifiants des annonceurs.](/help/assets/release-notes/2025/add-advertiser-names-modal.png){zoomable="yes"}

## Avril 2025 {#april-2025}

* Une nouvelle colonne **[!UICONTROL Entrées traitées]** a été ajoutée au tableau des activités de consommation de crédit. Cette colonne affiche le nombre total d’entrées (par exemple, les identifiants ou les lignes) traitées pour chaque activité. [En savoir plus](/help/guide/setup/my-activity.md#inputs-processed). <br> ![Colonne traitée des entrées mise en surbrillance dans la vue Mon activité.](/help/assets/release-notes/2025/inputs-processed-column.png){zoomable="yes"}
* Une nouvelle option d’e-mail de contact a été ajoutée lors de la création du compte. Cela permet aux collaborateurs partenaires de vous contacter si nécessaire pendant le processus de connexion. [En savoir plus](../setup/onboard-account.md).

## Mars 2025 {#march-2025}

* Lorsque vous [approvisionnez des audiences](/help/guide/setup/onboard-audiences.md) dans Collaboration, vous pouvez désormais définir une fréquence d’actualisation de l’audience comprise entre **tous les un et six jours** afin de mieux gérer l’activité de crédit [Gestion de l’audience](/help/guide/setup/my-activity.md#types-of-activities). Pour plus d’informations, consultez le guide [gérer les audiences](https://experienceleague.adobe.com/fr/docs/experience-platform/segmentation/ui/audience-portal.md#manage-audiences). <br> ![Écran de planification affichant différents intervalles de fréquence pour la mise à jour de l’appartenance à l’audience.](/help/assets/setup/add-manage-audiences/audience-scheduling-frequency.png "Écran de planification affichant différents intervalles de fréquence pour la mise à jour de l’appartenance à l’audience."){width="250" align="center" zoomable="yes"}
* Lors de l’établissement d’une connexion avec un collaborateur, vous pouvez désormais effectuer une sélection parmi des **cas d’utilisation** prédéfinis. Le cas d’utilisation sélectionné détermine les sections de projet et les fonctionnalités de produit qui deviennent disponibles. Pour plus d’informations, consultez le guide [gérer les projets](/help/guide/collaborate/manage-projects.md#project-use-cases).
   * *Mesure* active la section de projet **Mesure**.
   * *Découverte d’audiences* active la section de projet **Découverte**.
   * *Activation de l’audience* active les sections de projet **Activer** <br>
* Vous pouvez désormais supprimer des connexions avec des collaborateurs avec lesquels vous ne souhaitez plus travailler. Pour savoir comment supprimer des connexions, consultez le guide [suppression de connexions](/help/guide/connect/establishing-connections.md#delete-connections).

## Février 2025 {#february-2025}

Adobe Real-Time CDP Collaboration, conçu pour permettre aux annonceurs et aux éditeurs de découvrir, d’activer et de mesurer des audiences à forte valeur ajoutée sans cookies tiers, est désormais disponible en général aux États-Unis.

### Commencer

1. **Configuration des accès** : les administrateurs système configurent les autorisations d’accès pour les utilisateurs. Pour en savoir plus sur la configuration des autorisations d’accès, consultez le guide [gérer l’accès des utilisateurs](/help/guide/permissions/manage-user-access.md#RTCDP-collaboration-access).
2. **Connexion aux sources de données** : audiences Source à utiliser dans Collaboration. Pour commencer à approvisionner les audiences, lisez le guide [source et gestion des audiences](/help/guide/setup/onboard-audiences.md) .
3. **Établir des connexions** : commencez à collaborer avec des annonceurs ou des éditeurs approuvés. Pour en savoir plus sur la création de connexions, consultez le guide [établissement de connexions](/help/guide/connect/establishing-connections.md).
4. **Découvrir et activer** : créez des projets pour identifier les audiences importantes à activer dans les campagnes. Pour en savoir plus sur la création de projets, consultez le guide [gérer les projets](/help/guide/collaborate/manage-projects.md).

### Disponibilité

* Adobe Real-Time CDP Collaboration est actuellement disponible uniquement pour les clients américains.
* Il est automatiquement disponible pour les clients Adobe Real-Time CDP Prime et Ultimate

Pour plus d’informations, consultez :

* [Présentation de Collaboration](/help/guide/home.md)
* [Workflow de bout en bout](/help/guide/overview/end-to-end-workflow.md)
* [Présentation des autorisations](/help/guide/permissions/overview.md)
