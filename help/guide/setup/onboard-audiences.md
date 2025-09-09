---
title: Source et gestion des audiences
description: Découvrez comment sourcer et gérer des audiences dans Adobe Real-Time CDP Collaboration
audience: admin, publisher, advertiser
badgelimitedavailability: label="Disponibilité limitée" type="Informative" url="https://helpx.adobe.com/legal/product-descriptions/real-time-customer-data-platform-collaboration.html newtab=true"
exl-id: 0a5158fa-73d3-4406-af20-2b6c7be9934e
source-git-commit: 425bcb6b8069dfca17838d05b6a91250293c8308
workflow-type: tm+mt
source-wordcount: '3508'
ht-degree: 13%

---

# Source et gestion des audiences

{{limited-availability-release-note}}

Les audiences sont des groupes spécifiques d’utilisateurs ou de clients segmentés en fonction de divers attributs. Ils permettent aux collaborateurs de travailler ensemble sur des expériences marketing ciblées et personnalisées pour des campagnes publicitaires plus efficaces. Ce guide explique comment sourcer des audiences dans Real-Time CDP Collaboration, afficher le tableau de bord des audiences et gérer des audiences individuelles.

## Audiences Source dans Collaboration {#source-audiences}

>[!IMPORTANT]
>
>Pour approvisionner les audiences, votre utilisateur doit être affecté à un rôle contenant deux autorisations de gestion des profils - **[!UICONTROL Afficher les profils]** et **[!UICONTROL Afficher les segments]**. Pour plus d’informations sur l’attribution des autorisations nécessaires, consultez le guide [Audience sourcing](../permissions/overview.md#audience-sourcing) dans la section autorisations.

Avant de pouvoir activer des audiences avec des collaborateurs et exécuter des calculs de chevauchement, les audiences doivent être sourcées dans Collaboration. Pour approvisionner les audiences, suivez les étapes du workflow dans la section ci-dessous.

Dans l’onglet **[!UICONTROL Mes audiences]** de l’espace de travail **[!UICONTROL Configuration]**, sélectionnez l’icône d’ajout (![icône d’ajout).](/help/assets/icons/plus.png)), puis sélectionnez **[!UICONTROL Audience]**. S’il s’agit de votre première audience, vous pouvez également sélectionner l’option **[!UICONTROL Ajouter]**.

![Espace de travail Mes audiences avec l’option Ajouter et les options Audiences mises en surbrillance.](/help/assets/setup/add-manage-audiences/add-audiences.png){zoomable="yes"}

### Sélectionner la connexion de données {#select-data-connection}

>[!CONTEXTUALHELP]
>id="rtcdp_collaboration_import_audience_marketing_actions"
>title="Actions marketing"
>abstract="<p>Utilisez des actions marketing pour contrôler les données d’audience à importer dans Real-Time CDP Collaboration à partir d’Experience Platform. L’action marketing <strong>Collaboration de données</strong> prend en charge les libellés d’utilisation des données C4, C5 et C9. L’action marketing <strong>Science des données</strong> prend en charge le libellé d’utilisation des données C9.</p> <p> <ul><li> Lorsque la case à cocher est <em>activée</em>, toutes les données marquées avec les libellés mentionnés ci-dessus dans Experience Platform sont exclues et ne sont <strong> pas</strong> importées dans Real-Time CDP Collaboration.</li><li> Lorsque la case à cocher <em>désactivée</em>, il n’existe aucune restriction sur les données d’Experience Platform qui peuvent être sourcées dans Real-Time CDP Collaboration.</li></ul></p>"
>additional-url="https://experienceleague.adobe.com/docs/experience-platform/data-governance/labels/overview.html?lang=fr" text="Présentation des libellés d’utilisation des données"
>additional-url="https://experienceleague.adobe.com/docs/experience-platform/data-governance/labels/reference.html?lang=fr" text="Glossaire des libellés dʼutilisation des données"

>[!IMPORTANT]
>
>Après avoir établi à votre première connexion de données et sourcé votre première audience, vous pouvez ensuite sourcer plusieurs audiences à partir de la connexion de données existante. Lors de l’ajout d’audiences supplémentaires, vous commencerez à partir de l’étape [sélectionner une audience](#select-audiences), puisque la connexion aux données a déjà été établie.

Une connexion aux données est la source de données à partir de laquelle vous approvisionnez les audiences. Actuellement, la seule connexion de données prise en charge est Adobe Experience Platform.

Tous les paramètres que vous configurez pour votre connexion de données sont appliqués à toutes les audiences provenant de cette connexion de données.

>[!TIP]
>
>Il existe un workflow distinct où vous pouvez afficher et modifier vos connexions de données. Pour plus d’informations, consultez le guide [gestion des connexions aux données](/help/guide/setup/manage-data-connection.md).

Pour commencer à ajouter votre connexion de données, sélectionnez **[!UICONTROL Ajouter une nouvelle connexion de données]** puis sélectionnez **[!UICONTROL Suivant]**.

![L’espace de travail Ajouter des audiences avec l’option Ajouter une nouvelle connexion de données mise en surbrillance.](/help/assets/setup/add-manage-audiences/add-data-connection.png){zoomable="yes"}

#### Sélectionner une source de données

Vous allez ensuite choisir la source de votre connexion aux données. Les sources disponibles sont les suivantes :

* **Adobe Experience Platform** : sélectionnez cette option pour importer vos audiences depuis Adobe Experience Platform.
* **Fichier CSV** (version ultérieure) : chargez un fichier CSV contenant les données de votre audience pour une ingestion de données simple et rapide.
* **Amazon Web Services** (version ultérieure) : connectez-vous à votre stockage Amazon S3 pour obtenir des données d’audience source directement à partir de vos compartiments S3.
* **Snowflake** (version ultérieure) : utilisez votre entrepôt de données Snowflake pour extraire facilement les données d’audience.
* **Google Cloud Platform** (version future) : connectez-vous à votre espace de stockage dans le cloud Google pour obtenir des données d’audience directement à partir de vos compartiments GCS.

Sélectionnez votre source de données, puis sélectionnez **[!UICONTROL Suivant]**.

![Espace de travail Ajouter des audiences avec l’option Adobe Experience Platform mise en surbrillance.](/help/assets/setup/add-manage-audiences/select-data-connection-source.png){zoomable="yes"}

#### Sélectionner un sandbox

Après avoir sélectionné votre source de données, vous devez sélectionner le sandbox qui inclut les audiences que vous souhaitez utiliser pour Collaboration. Sélectionnez le sandbox dans la liste des sandbox disponibles, puis sélectionnez **[!UICONTROL Suivant]**

![Espace de travail Ajouter des audiences avec un sandbox sélectionné.](/help/assets/setup/add-manage-audiences/select-sandbox.png){zoomable="yes"}

#### Politique de gouvernance et mesures d’application {#governance-policy-and-enforcement-actions}

Ensuite, vous devez vous assurer que les actions marketing correctes sont définies sur les données sources. Vous devez également fournir un consentement pour que les données provenant d’Experience Platform soient utilisées pour la collaboration en matière de données.

Utilisez des actions marketing pour contrôler les données d’audience à importer dans Collaboration à partir d’Experience Platform. L’action marketing **[!UICONTROL Collaboration de données]** prend en charge les libellés d’utilisation des données C4, C5 et C9. L’action marketing **[!UICONTROL Science des données]** prend en charge le libellé d’utilisation des données C9.

En savoir plus sur les libellés d’utilisation des données [C4, C5 et C9](https://experienceleague.adobe.com/en/docs/experience-platform/data-governance/labels/reference#contract){target="_blank"}.

* Lorsque la case à cocher est ***activée***, toutes les données libellées dans Experience Platform comme décrit ci-dessus sont exclues et **pas** importées dans Collaboration.
* Lorsque la case à cocher ***désactivée***, il n’existe aucune restriction sur les données provenant d’Experience Platform.

Consultez la documentation d’Experience Platform pour en savoir plus sur les libellés d’utilisation des données :

* [Présentation des libellés d’utilisation des données](https://experienceleague.adobe.com/fr/docs/experience-platform/data-governance/labels/overview){target="_blank"}
* [Glossaire des libellés d’utilisation des données](https://experienceleague.adobe.com/fr/docs/experience-platform/data-governance/labels/reference){target="_blank"}

En outre, vous souhaiterez sélectionner vos règles de consentement à appliquer aux données provenant de Collaboration.

![Espace de travail Ajouter des audiences à la section Politique de gouvernance et application des actions ](/help/assets/setup/add-manage-audiences/data-collaboration-consent.png){zoomable="yes"}.

Une fois que vous avez sélectionné les actions marketing et les règles de consentement, sélectionnez **[!UICONTROL Suivant]** pour passer à l’étape suivante. Une boîte de dialogue de confirmation s’affiche, vous demandant d’accepter les conditions. Cochez la case, puis sélectionnez **[!UICONTROL OK]** pour confirmer.

![La boîte de dialogue Politique de gouvernance et appliquer des actions avec la case à cocher et l’option OK mises en surbrillance.](/help/assets/setup/add-manage-audiences/data-collaboration-consent-confirmation.png){zoomable="yes"}

### Fournir des détails

Indiquez ensuite un nom et une description pour votre connexion de données. Ces informations vous aideront à identifier la connexion de données ultérieurement.

![Espace de travail Ajouter des audiences avec la possibilité de fournir un nom et une description.](/help/assets/setup/add-manage-audiences/data-connection-details.png){zoomable="yes"}

### Champs de mappage {#map-fields}

>[!CONTEXTUALHELP]
>id="rtcdp_collaboration_import_audience_mapping_source_fields"
>title="Champs sources"
>abstract="Les champs sources sont des espaces de noms d’identité et des attributs de votre implémentation d’Experience Platform. Vous pouvez les mapper à des champs cibles définis dans Collaboration."

>[!CONTEXTUALHELP]
>id="rtcdp_collaboration_import_audience_mapping_target_fields"
>title="Champs cibles"
>abstract="Les champs cibles sont les clés de correspondance choisies lors de la configuration du compte. Par défaut, toutes les clés de correspondance sélectionnées sont disponibles."

>[!CONTEXTUALHELP]
>id="rtcdp_collaboration_import_audience_mapping_apply_transformation"
>title="Appliquer la transformation"
>abstract="Lors de la récupération de champs *non hachés* à partir de votre source, utilisez cette option pour que Collaboration applique le hachage et transforme les champs simples en champs hachés."

>[!CONTEXTUALHELP]
>id="rtcdp_collaboration_import_audience_mapping_identity_namespaces"
>title="Espaces de noms d’identité"
>abstract="Sélectionnez un espace de noms d’identité dans les espaces de noms d’identité standard et personnalisés disponibles dans votre organisation Experience Platform."
>additional-url="https://experienceleague.adobe.com/docs/experience-platform/identity/features/namespaces.html#standard?lang=fr" text="Espaces de noms standard et d’identité dans Experience Platform"

>[!CONTEXTUALHELP]
>id="rtcdp_collaboration_import_audience_mapping_profile_attributes"
>title="Attributs de profil"
>abstract="Sélectionnez des attributs dans le schéma d’union pour la classe Profil dans Experience Platform. Cette vue affiche les attributs présents dans le schéma d’union et appartenant à la classe XDM Individual Profile."
>additional-url="https://experienceleague.adobe.com/docs/experience-platform/profile/union-schemas/union-schema.html?lang=fr" text="Schéma d’union dans Experience Platform"

Vous allez ensuite sélectionner les champs sources à mapper aux champs cibles dans Collaboration. Les champs cibles disponibles seront basés sur les clés de correspondance que vous avez sélectionnées lors de la configuration du compte.

>[!IMPORTANT]
>
>Actuellement, vous ne pouvez pas modifier les connexions de données pour inclure de nouveaux champs de mappage. Si vous ajoutez de nouvelles clés de correspondance à votre compte après la création de votre connexion de données, vous devrez créer une nouvelle connexion de données pour les mapper.

![Espace de travail Ajouter des audiences avec la possibilité de mapper les champs sources aux champs cibles.](/help/assets/setup/add-manage-audiences/add-map-fields.png){zoomable="yes"}

>[!TIP]
>
>Vous pouvez mapper plusieurs champs sources au même champ cible. Par exemple, si des adresses e-mail se trouvent dans deux champs distincts d’Experience Platform, vous pouvez les mapper au champ cible **[!UICONTROL E-mail haché]** sous la forme de deux lignes distinctes. Utilisez l’option **[!UICONTROL Ajouter un champ]** pour ajouter des lignes de mappage supplémentaires.

>[!BEGINSHADEBOX]

Les **[!UICONTROL champs Source]** sont des espaces de noms d’identité et des attributs d’Experience Platform. Il s’agit des espaces de noms d’identité [standard](https://experienceleague.adobe.com/docs/experience-platform/identity/features/namespaces.html#standard?lang=fr){target="_blank"} et [personnalisés](https://experienceleague.adobe.com/docs/experience-platform/identity/features/namespaces.html#create-namespaces){target="_blank"}. Ils incluent également les attributs de profil présents dans le [schéma d’union](https://experienceleague.adobe.com/docs/experience-platform/profile/union-schemas/union-schema.html?lang=fr){target="_blank"} et appartenant à la classe XDM Individual Profile.

Les champs Source sont mappés sur les champs cibles définis dans Collaboration.

**[!UICONTROL Champs cibles]** indiquez comment les identités sont référencées dans Collaboration. Les champs cibles sont les clés de correspondance choisies lors de la configuration du compte. Par défaut, toutes les clés de correspondance sélectionnées sont disponibles.

Utilisez l’option **[!UICONTROL Appliquer la transformation]** lorsque vous sourcez des champs *non hachés* vers des champs hachés. Collaboration appliquera le hachage et transformera les champs. L’algorithme de hachage utilisé par Adobe est SHA256.

>[!ENDSHADEBOX]

Pour commencer à mapper des champs, sélectionnez le champ source vide en regard du champ cible. La boîte de dialogue **[!UICONTROL Sélectionner le champ source]** s’affiche. Sélectionnez entre les options **[!UICONTROL Espaces de noms d’identité]** et **[!UICONTROL Attributs de profil]** pour trouver le champ source souhaité, puis sélectionnez le champ dans la liste. Vous pouvez également utiliser l’option de recherche pour trouver le champ souhaité.

![La boîte de dialogue Sélectionner le champ source avec les options d’e-mail affichées.](/help/assets/setup/add-manage-audiences/select-source-field.png){zoomable="yes"}

Pour gérer l’origine d’un champ non haché vers un champ cible haché, utilisez l’option **[!UICONTROL Appliquer la transformation]**. Par exemple, pour ajouter un deuxième champ d’e-mail, sélectionnez l’option **[!UICONTROL Ajouter un champ]** afin d’ajouter une nouvelle ligne, puis sélectionnez **[!UICONTROL E-mail haché]** pour le champ cible. Sélectionnez un champ source d’e-mail non haché, puis sélectionnez **[!UICONTROL Appliquer la transformation]**.

![L’espace de travail Ajouter des audiences avec les champs sources d’e-mail mappés au champ cible, avec l’option Appliquer la transformation activée pour l’un.](/help/assets/setup/add-manage-audiences/apply-transformation.png){zoomable="yes"}

Continuez à ajouter des paires de mappage pour chaque champ cible. Si vous ne souhaitez pas utiliser de clé de correspondance, vous pouvez la supprimer à l’aide de l’icône de suppression (![icône Supprimer](/help/assets/icons/delete.png)) située en regard du champ. Si la clé de correspondance est supprimée, vous ne pourrez pas l’utiliser lors de l’approvisionnement d’audiences à partir de la connexion.

![Espace de travail Ajouter des audiences avec l’option Supprimer en surbrillance à côté d’un champ cible.](/help/assets/setup/add-manage-audiences/remove-target-field.png){zoomable="yes"}

Lorsque vous avez terminé de mapper les champs, sélectionnez **[!UICONTROL Suivant]** pour continuer.

![Espace de travail Ajouter des audiences avec les champs de mappage renseignés et l’option Suivant mise en surbrillance.](/help/assets/setup/add-manage-audiences/confirm-field-mapping.png){zoomable="yes"}

### Planning {#schedule}

Ensuite, planifiez les dates de début et de fin du remplissage des audiences. L’audience sera actualisée selon ce planning.

![L’espace de travail Ajouter une audience avec les options de planification affichées.](/help/assets/setup/add-manage-audiences/audience-scheduling.png){zoomable="yes"}

>[!IMPORTANT]
>
>Le réglage de la fréquence des mises à jour de l’audience permet de gérer l’[activité de crédit Gestion de l’audience](/help/guide/setup/my-activity.md#types-of-activities), qui est calculée par actualisation de l’audience. La sélection d’une fréquence plus élevée peut avoir un impact sur l’actualisation des données disponibles pour les rapports de découverte d’audience et l’activation d’audience.

Sélectionnez la fréquence d’actualisation de l’audience dans le menu déroulant **[!UICONTROL Fréquence]**.

![L’espace de travail Ajouter des audiences de planification avec la liste déroulante Fréquence ouverte.](/help/assets/setup/add-manage-audiences/audience-scheduling-frequency.png){zoomable="yes"}

Sélectionnez ensuite la **[!UICONTROL Période]**. La date de début est la date à laquelle l’audience commencera à remplir avec des profils, et la date de fin est la date à laquelle l’audience cessera de s’actualiser.

![L’espace de travail de planification Ajouter des audiences avec l’option Période affichée.](/help/assets/setup/add-manage-audiences/audience-scheduling-date-range.png){zoomable="yes"}

>[!IMPORTANT]
>
>Après la date de fin dans la période, toutes les audiences provenant de cette connexion de données cesseront de s’actualiser. Pour renouveler la connexion, suivez le guide [Gérer la connexion aux données](/help/guide/setup/manage-data-connection.md).

### Sélectionner des audiences {#select-audiences}

Après avoir sélectionné la source de l’audience, vous choisirez des audiences spécifiques à inclure. Utilisez les options de recherche et de filtrage pour trouver les audiences appropriées à partir de votre connexion de données. Sélectionnez les audiences souhaitées, puis sélectionnez **[!UICONTROL Suivant]**.

![Espace de travail Ajouter des audiences avec une liste des audiences disponibles.](/help/assets/setup/add-manage-audiences/select-audience.png){zoomable="yes"}

### Réviser

Passez en revue toutes les configurations et tous les paramètres avant de finaliser l’ajout de l’audience. Assurez-vous que tous les détails sont corrects, puis sélectionnez **[!UICONTROL Terminé]** pour terminer la création de votre connexion aux données.

![L’espace de travail Ajouter des audiences avec toutes les configurations sélectionnées affichées.](/help/assets/setup/add-manage-audiences/review-connection.png){zoomable="yes"}

## Afficher le tableau de bord des audiences {#view-audiences-dashboard}

>[!CONTEXTUALHELP]
>id="rtcdp_collaboration_view_audience_missing_identities"
>title="Identités manquantes"
>abstract="Le nombre d’identités sera disponible après la prochaine actualisation de la connexion de données suivant le planning configuré. L’actualisation initiale se produit généralement dans les 24 heures suivant la configuration de la connexion aux données. Les actualisations en cours suivront le planning configuré."

Après le sourcing des audiences, l’espace de travail **[!UICONTROL Mes audiences]** affiche toutes les audiences actuellement sourcées dans Collaboration.

![Espace de travail Mes audiences affichant toutes les audiences sourcées.](/help/assets/setup/add-manage-audiences/audiences-workspace.png)

Chaque audience contient un aperçu des informations suivantes :

| Élément | Description |
|----------|---------|
| **[!UICONTROL Nom]** | Nom de l’audience. |
| **[!UICONTROL Identités]** | Indique le nombre d’identités présentes dans cette audience. Notez que si le même profil possède plusieurs identités et que ces identités sont utilisées comme clés de correspondance dans le projet, le profil s’affichera deux fois dans le décompte. |
| **[!UICONTROL Statut]** | Indique si l’audience est active et peut être utilisée dans des projets. Un statut **[!UICONTROL En attente]** indique que l’audience vient d’être sourcée et que les identités doivent encore être renseignées. Les audiences sources sont renseignées avec des profils après l’actualisation initiale, qui se produit généralement dans les 24 heures suivant la configuration de la connexion aux données. |
| **[!UICONTROL Source]** | Indique l’origine de l’audience. Dans la version actuelle de Collaboration, Experience Platform est la seule source prise en charge. |
| **[!UICONTROL Connexion aux données]** | Connexion de données à partir de laquelle l’audience est sourcée. Vous pouvez sélectionner le nom pour afficher la connexion de données. |
| **[!UICONTROL Accès à la connexion]** | Définit si l’audience est privée ou publique. Les audiences publiques sont détectables dans les rapports de chevauchement et peuvent être activées dans un projet. |
| **[!UICONTROL Créé]** | Indique la date à laquelle l’audience a été initialement sourcée dans Collaboration. |
| **[!UICONTROL Dernière mise à jour]** | Indique la date et l’heure de la dernière mise à jour de l’audience dans Collaboration. Il ne s’agit pas de la date de la dernière actualisation de l’audience, mais plutôt de la date de la dernière modification de la configuration ou des métadonnées de l’audience. |

![Espace de travail Mon audience affichant toutes les audiences sourcées.](/help/assets/setup/add-manage-audiences/audiences-workspace.png){zoomable="yes"}

Pour effectuer des actions rapides sur une audience, sélectionnez les points de suspension **...** en regard du nom de l’audience. Les options disponibles sont les suivantes :

* **[!UICONTROL Modifier les catégories]** vous permet d’ajouter différentes balises de catégorie à l’audience. Pour plus d’informations, reportez-vous à la section [catégories](#categories) ci-dessous.
* **[!UICONTROL Supprimer]** supprimera l’audience de la connexion aux données.

![L’espace de travail Mes audiences avec le menu représentant des points de suspension ouvert et les options Modifier les catégories et Supprimer mises en surbrillance.](/help/assets/setup/add-manage-audiences/audiences-ellipsis-menu.png){zoomable="yes"}

## Affichage d’audiences individuelles {#view-individual-audiences}

Pour afficher et mettre à jour les informations d’une audience individuelle, sélectionnez l’audience dans l’espace de travail **[!UICONTROL Mes audiences]**. L’espace de travail des audiences affiche des informations détaillées sur l’audience sélectionnée, notamment ses détails, ses identités, ses catégories, son accès à la connexion et ses paramètres de visibilité des métadonnées.

### Détails de l’audience

Les informations suivantes s’affichent pour chaque audience :

| Élément | Description |
|----------|---------|
| **[!UICONTROL Statut]** | Indique si l’audience est active et peut être utilisée dans des projets. |
| **[!UICONTROL Source]** | Indique l’origine de l’audience. Dans la version actuelle de Collaboration, Experience Platform est la seule source prise en charge. |
| **[!UICONTROL Connexion aux données]** | Connexion de données à partir de laquelle l’audience est sourcée. |
| **[!UICONTROL Dernière mise à jour]** | Indique la date et l’heure de la dernière mise à jour de l’audience dans Collaboration. Il ne s’agit pas de la date de la dernière actualisation de l’audience, mais plutôt de la date de la dernière modification de sa configuration ou de ses métadonnées |
| **[!UICONTROL Dernière mise à jour par]** | Indique le dernier utilisateur à avoir mis à jour l’audience. |
| **[!UICONTROL Créé]** | Indique la date à laquelle l’audience a été initialement sourcée dans Collaboration. |
| **[!UICONTROL Créé par]** | Indique l’utilisateur qui a sourcé l’audience dans Collaboration. |

![Espace de travail d’une audience individuelle.](/help/assets/setup/add-manage-audiences/audience-details.png){zoomable="yes"}

#### Identités {#identities}

>[!CONTEXTUALHELP]
>id="rtcdp_collaboration_view_audience_identities"
>title="Identités"
>abstract="Une vue de répartition des identités qui constituent cette audience, séparées par une clé de correspondance."

La section **[!UICONTROL Identités]** indique le nombre d’identités présentes dans l’audience. La section contient également une répartition des identités par clé de correspondance pour vous aider à comprendre la composition de l’audience.

![Section Identités de l’espace de travail d’une audience individuelle.](/help/assets/setup/add-manage-audiences/audience-details-identities.png){zoomable="yes"}

Placer le pointeur de la souris sur les sections individuelles de la répartition de la clé de correspondance fournit un nombre d’identités précis pour la clé correspondante.

![Section Identités de l’espace de travail d’une audience individuelle avec une répartition de clé de correspondance affichée.](/help/assets/setup/add-manage-audiences/audience-details-identities.png)

#### Catégories {#categories}

>[!CONTEXTUALHELP]
>id="rtcdp_collaboration_view_audience_categories"
>title="Catégories"
>abstract="Balisez vos audiences pour une organisation, un filtrage et une récupération faciles. Vous pouvez baliser une audience avec plusieurs catégories, puis utiliser ces balises de catégorie pour filtrer les audiences de votre choix dans d’autres zones du produit."

Pour une organisation, un filtrage et une récupération faciles des audiences, vous pouvez baliser vos audiences. Vous pouvez baliser une audience avec plusieurs catégories, puis utiliser ces balises de catégorie pour filtrer les audiences souhaitées dans la zone de produit [Discover](/help/guide/collaborate/discover.md) lors de l’exécution de rapports de chevauchement d’audiences.

Pour ajouter des catégories, sélectionnez l’option **[!UICONTROL Modifier]** dans la section **[!UICONTROL Catégories]**.

![Section Catégories de l’espace de travail d’une audience individuelle.](/help/assets/setup/add-manage-audiences/audience-details-categories.png){zoomable="yes"}

La boîte de dialogue **[!UICONTROL Catégories]** s’affiche, vous permettant de sélectionner les catégories que vous souhaitez ajouter à l’audience. Pour sélectionner une catégorie individuelle, cochez la case en regard du nom de la catégorie.

![La boîte de dialogue Catégories avec les catégories disponibles affichées.](/help/assets/setup/add-manage-audiences/audience-details-categories-select.png){zoomable="yes"}

#### Accès à la connexion {#connection-access}

>[!CONTEXTUALHELP]
>id="rtcdp_collaboration_view_audience_connection_access"
>title="Accès à la connexion"
>abstract="<p>Les audiences peuvent être de trois types : publiques, privées et personnalisées.</p><p> Leur disponibilité pour une utilisation dans des projets avec des collaborateurs diffère en fonction du paramètre d’accès à la connexion.</p>"

La disponibilité d’une audience à utiliser dans des projets avec des collaborateurs diffère en fonction du paramètre d’accès à la connexion. Dans la section **[!UICONTROL Accès à la connexion]** , vous pouvez choisir si l’audience doit être privée, publique ou disponible uniquement pour des connexions spécifiques. Les audiences publiques sont utilisables et détectables dans les connexions.

Pour mettre à jour l’accès à la connexion de l’audience, sélectionnez l’option **[!UICONTROL Modifier]** dans la section **[!UICONTROL Accès à la connexion]**.

![Section Accès à la connexion de l’espace de travail d’une audience individuelle.](/help/assets/setup/add-manage-audiences/audience-details-connection-access.png){zoomable="yes"}

La boîte de dialogue **[!UICONTROL Accès de connexion]** s’affiche, avec trois options d’accès de connexion disponibles :

* **[!UICONTROL Audience privée]**. Ces audiences ne sont *pas* disponibles pour une utilisation dans les rapports de chevauchement ou pour une activation dans les connexions avec des collaborateurs. Bien que les audiences ne soient pas disponibles pour les collaborateurs, la population des audiences contribue toujours à la population totale dans la vue **[!UICONTROL Toutes les audiences]** dans la section [Comparer les audiences](/help/guide/collaborate/discover.md#compare-audiences). Définissez le paramètre sur public ou personnalisé pour utiliser les audiences dans les connexions avec les collaborateurs.
* **[!UICONTROL Public audience]**. Ces audiences peuvent être utilisées dans les rapports de chevauchement et pour l’activation dans les connexions avec des collaborateurs.
* **[!UICONTROL Audience personnalisée]**. Ces audiences peuvent uniquement être utilisées dans les rapports de chevauchement et pour l’activation dans des connexions spécifiées. Bien que les audiences ne soient pas disponibles pour les collaborateurs, la population des audiences contribue toujours à la population totale dans la vue **[!UICONTROL Toutes les audiences]** dans la section [Comparer les audiences](/help/guide/collaborate/discover.md#compare-audiences).

Sélectionnez l’option d’accès à la connexion souhaitée, puis sélectionnez **[!UICONTROL Enregistrer]** pour appliquer les modifications.

![La boîte de dialogue Accès à la connexion avec les options disponibles s’affiche.](/help/assets/setup/add-manage-audiences/audience-details-connection-access-dialog.png){zoomable="yes"}

>[!IMPORTANT]
>
>Quel que soit le statut d’accès (public, privé ou personnalisé), la population de toute audience contribue à la population **[!UICONTROL Toutes les audiences]** dans la section **[!UICONTROL Comparer les audiences]** d’un projet.

La disponibilité de l’audience à utiliser dans les projets avec des collaborateurs diffère selon le paramètre d’accès à la connexion.

#### Visibilité des métadonnées {#metadata-visibility}

>[!CONTEXTUALHELP]
>id="rtcdp_collaboration_view_audience_metadata_visibility"
>title="Visibilité des métadonnées"
>abstract="<p>Précise les métadonnées d’audience qui sont visibles pour d’autres collaborateurs et collaboratrices avant qu’ils ne se connectent à vous ou dans les vues du projet.</p> <p> Le **Nombre d’identités** vérifie si vos collaborateurs ou collaboratrices peuvent afficher le nombre d’identités de vos audiences lors de l’affichage des rapports de chevauchement dans l’onglet de découverte.</p><p> Le **% de chevauchement d’audiences** vérifie si les collaborateurs et collaboratrices sont en mesure de découvrir des pourcentages de chevauchement entre leurs audiences et les vôtres.</p><p> L’**[!UICONTROL Index d’audience]** contrôle si les collaborateurs et les collaboratrices peuvent afficher l’index d’audience dans un projet. Cette fonctionnalité n’est disponible que lorsque vous avez trois audiences actives ou plus.</p> <br> Pour que les paramètres de visibilité des métadonnées prennent effet, l’audience doit être définie sur publique ou personnalisée."

>[!NOTE]
>
>Si toutes les audiences de votre collaborateur sont définies sur privées, la section **[!UICONTROL Audiences pertinentes]** d’un projet dans l’espace de travail **[!UICONTROL Découvrir]** sera vide. Pour plus d’informations, consultez le guide [discover](/help/guide/collaborate/discover.md#relevant-audiences).

La visibilité des métadonnées indique la visibilité des métadonnées d’une audience sur d’autres collaborateurs avant qu’ils ne se connectent avec vous ou dans différentes vues de projet. Pour mettre à jour la visibilité des métadonnées de l’audience, sélectionnez l’option **[!UICONTROL Modifier]** dans la section **[!UICONTROL Visibilité des métadonnées]**.

![Section Visibilité des métadonnées de l’espace de travail d’une audience individuelle.](/help/assets/setup/add-manage-audiences/audience-details-metadata-visibility.png){zoomable="yes"}

La boîte de dialogue **[!UICONTROL Visibilité des métadonnées]** s’affiche, vous permettant de configurer les paramètres de visibilité de l’audience. Vous pouvez configurer deux paramètres de visibilité des métadonnées pour chaque audience :

**[!UICONTROL Afficher le nombre d’identités]** : ce paramètre contrôle si votre collaborateur peut afficher le nombre d’identités de vos audiences lors de l’[affichage de rapports de chevauchement dans l’onglet Détection](/help/guide/collaborate/discover.md#discover-overlaps) au sein d’un projet.

**[!UICONTROL Afficher le chevauchement des audiences %]** : ce paramètre contrôle si les collaborateurs sont en mesure de [découvrir des pourcentages de chevauchement](/help/guide/collaborate/discover.md#compare-audiences) entre leurs audiences et vos audiences.

**[!UICONTROL Index d’audience]** : lorsqu’il est défini sur true, vos collaborateurs peuvent afficher l’[index d’audience](/help/guide/collaborate/discover.md#audience-index-score) dans un projet. Cette fonctionnalité n’est disponible que lorsque vous avez trois audiences actives ou plus.

>[!NOTE]
>
>Pour que les paramètres de visibilité des métadonnées prennent effet, l’audience doit être définie sur publique ou personnalisée.

![La boîte de dialogue Visibilité des métadonnées avec les options disponibles s’affiche.](/help/assets/setup/add-manage-audiences/audience-details-metadata-dialog.png){zoomable="yes"}

## Modification de plusieurs audiences {#edit-audiences}

Dans le tableau de bord des audiences, vous pouvez modifier plusieurs audiences à la fois. Pour ce faire, sélectionnez les audiences que vous souhaitez modifier en cochant les cases en regard de leur nom. Une fois les audiences sélectionnées, vous pouvez effectuer des actions à l’aide des options disponibles dans le menu d’édition.

![Espace de travail Mes audiences avec deux audiences sélectionnées et le menu Modifier mis en surbrillance.](/help/assets/setup/add-manage-audiences/audiences-bulk-edit.png)

### Modification en masse de la visibilité des métadonnées {#bulk-edit-metadata-visibility}

Une fois vos audiences sélectionnées dans le tableau de bord d’audience, sélectionnez **[!UICONTROL Modifier la visibilité des métadonnées]** dans le menu de modification.

![Espace de travail Mes audiences avec l’option Modifier la visibilité des métadonnées mise en surbrillance.](/help/assets/setup/add-manage-audiences/audiences-bulk-edit-metadata.png)

La boîte de dialogue **[!UICONTROL Visibilité des métadonnées]** s’affiche, vous permettant de configurer les paramètres de visibilité des audiences sélectionnées. Par défaut, aucune option n’est sélectionnée. Choisissez les options à appliquer à toutes les audiences sélectionnées, puis sélectionnez **[!UICONTROL Enregistrer]**.

![La boîte de dialogue Visibilité des métadonnées avec les options disponibles s’affiche.](/help/assets/setup/add-manage-audiences/audience-details-metadata-dialog.png)

### Modifier en bloc l’accès à la connexion {#bulk-edit-connection-access}

Une fois vos audiences sélectionnées dans le tableau de bord des audiences, sélectionnez **[!UICONTROL Modifier l’accès à la connexion]** dans le menu de modification.

![Espace de travail Mes audiences avec l’option Modifier l’accès à la connexion mise en surbrillance.](/help/assets/setup/add-manage-audiences/audiences-bulk-edit-connection-access.png)

La boîte de dialogue **[!UICONTROL Accès à la connexion]** s’affiche, vous permettant de configurer les paramètres d’accès pour les audiences sélectionnées. Par défaut, l’option **[!UICONTROL Audience privée]** est sélectionnée. Choisissez les options à appliquer à toutes les audiences sélectionnées, puis sélectionnez **[!UICONTROL Enregistrer]**.

![La boîte de dialogue Accès à la connexion avec les options disponibles s’affiche.](/help/assets/setup/add-manage-audiences/audience-details-connection-access-dialog.png)

### Modifier en masse les noms et les descriptions des audiences {#bulk-edit-audience-names-descriptions}

Une fois vos audiences sélectionnées dans le tableau de bord d’audience, sélectionnez **[!UICONTROL Modifier le nom et la description]** dans le menu de modification.

![Espace de travail Mes audiences avec l’option Modifier le nom et la description mise en surbrillance.](/help/assets/setup/add-manage-audiences/audiences-bulk-edit-name-description.png)

La boîte de dialogue **[!UICONTROL Nom et description]** s’affiche, vous permettant de configurer le nom et la description de chaque audience sélectionnée. Par défaut, les noms et descriptions actuels s’affichent pour chaque audience. Apportez vos modifications, puis sélectionnez **[!UICONTROL Enregistrer]**.

![La boîte de dialogue Nom et description avec les options disponibles affichées.](/help/assets/setup/add-manage-audiences/audiences-bulk-edit-name-description-dialog.png)

### Modification en masse de catégories {#bulk-edit-categories}

Une fois vos audiences sélectionnées dans le tableau de bord d’audience, sélectionnez **[!UICONTROL Modifier les catégories]** dans le menu de modification.

![Espace de travail Mes audiences avec l’option Modifier les catégories mise en surbrillance.](/help/assets/setup/add-manage-audiences/audiences-bulk-edit-categories.png)

La boîte de dialogue **[!UICONTROL Catégories]** s’affiche, vous permettant de configurer les catégories pour chaque audience sélectionnée. Par défaut, aucune catégorie ne sera sélectionnée. Pour sélectionner une catégorie, sélectionnez d’abord la catégorie principale, puis sélectionnez les sous-catégories à inclure. Apportez vos modifications, puis sélectionnez **[!UICONTROL Enregistrer]**.

![La boîte de dialogue Catégories avec les options disponibles s’affiche.](/help/assets/setup/add-manage-audiences/audiences-bulk-edit-categories-dialog.png)

## Étapes suivantes

Après avoir sourcé des audiences, il est temps de découvrir des éditeurs avec lesquels [se connecter](/help/guide/connect/establishing-connections.md) et collaborer sur des projets.
