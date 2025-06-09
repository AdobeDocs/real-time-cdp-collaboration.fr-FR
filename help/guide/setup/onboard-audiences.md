---
title: Importer et gérer des audiences
description: Découvrez comment importer et gérer des audiences dans Adobe Real-Time CDP Collaboration
audience: admin, publisher, advertiser
badgelimitedavailability: label="Disponibilité limitée" type="Informative" url="https://helpx.adobe.com/legal/product-descriptions/real-time-customer-data-platform-collaboration.html newtab=true"
exl-id: 0a5158fa-73d3-4406-af20-2b6c7be9934e
source-git-commit: fda414120decc0c76712616ff85b83febede53e9
workflow-type: tm+mt
source-wordcount: '2961'
ht-degree: 18%

---

# Importer et gérer des audiences

{{limited-availability-release-note}}

Les audiences sont des groupes spécifiques d’utilisateurs ou de clients segmentés en fonction de divers attributs. Ils permettent aux annonceurs et aux éditeurs de collaborer sur des expériences marketing ciblées et personnalisées pour des campagnes publicitaires plus efficaces.

Utilisez cette page comme référence pour comprendre toutes les mesures pertinentes que vous pouvez afficher en rapport avec vos audiences, ainsi que les étapes de workflow pour importer une audience dans Adobe Real-Time CDP Collaboration.

>[!TIP]
>
>Utilisez les informations de cet écran pour obtenir toutes les informations dont vous avez besoin sur vos audiences. Utilisez également les écrans [découvrir et chevauchent](/help/guide/collaborate/discover.md) pour obtenir des informations sur les audiences qui fonctionneraient le mieux pour différents types de campagne, par rapport à l’inventaire des éditeurs.

>[!BEGINSHADEBOX]

Cette page de documentation contient les éléments suivants :

* [Importer des audiences dans Real-Time CDP Collaboration](#import-audiences)
* [Afficher le tableau de bord des audiences](#view-audiences-dashboard)
* [Affichage d’audiences individuelles](#view-individual-audiences)

>[!ENDSHADEBOX]

## Importer des audiences dans Real-Time CDP Collaboration {#import-audiences}

>[!IMPORTANT]
>
>Pour importer des audiences, votre utilisateur doit être affecté à un rôle contenant deux autorisations de gestion des profils - Affichage des profils et Affichage des segments. Pour plus d’informations sur l’attribution des autorisations nécessaires, consultez le guide [importation d’audience](../permissions/overview.md#audience-importation).

Avant de pouvoir activer des audiences avec des collaborateurs et exécuter des calculs de chevauchement, les audiences doivent être importées dans Real-Time CDP Collaboration. Pour importer des audiences, suivez les étapes du workflow décrites dans la section ci-dessous.

Dans l’onglet **[!UICONTROL Mes audiences]** de l’espace de travail **[!UICONTROL Configuration]**, sélectionnez l’icône d’ajout (![icône d’ajout).](/help/assets/icons/plus.png)) ou l’option **[!UICONTROL Ajouter]** puis sélectionnez **Audience**.

![Espace de travail Mes audiences avec l’option Ajouter et les options Audiences mises en surbrillance.](/help/assets/setup/add-manage-audiences/add-audiences.png)

### Sélectionner la connexion de données {#select-data-connection}

>[!CONTEXTUALHELP]
>id="rtcdp_collaboration_import_audience_marketing_actions"
>title="Actions marketing"
>abstract="<p>Utilisez des actions marketing pour contrôler les données d’audience à importer dans Real-Time CDP Collaboration à partir d’Experience Platform. L’action marketing <strong>Collaboration de données</strong> prend en charge les libellés d’utilisation des données C4, C5 et C9. L’action marketing <strong>Science des données</strong> prend en charge le libellé d’utilisation des données C9.</p> <p> <ul><li> Lorsque la case à cocher est <em>activée</em>, toutes les données marquées avec les libellés mentionnés ci-dessus dans Experience Platform sont exclues et ne sont <strong> pas</strong> importées dans Real-Time CDP Collaboration.</li><li> Lorsque la case à cocher est <em>désactivée</em>, il n’existe aucune restriction sur les données d’Experience Platform qui peuvent être importées dans Real-Time CDP Collaboration.</li></ul></p>"
>additional-url="https://experienceleague.adobe.com/docs/experience-platform/data-governance/labels/overview.html?lang=fr" text="Présentation des libellés d’utilisation des données"
>additional-url="https://experienceleague.adobe.com/docs/experience-platform/data-governance/labels/reference.html?lang=fr" text="Glossaire des étiquettes dʼutilisation des données"

>[!IMPORTANT]
>
>Après avoir établi à votre première connexion de données et importé votre première audience, vous pouvez importer plusieurs audiences à partir de la connexion de données existante. Lors de l’ajout d’audiences supplémentaires, vous commencerez à partir de l’étape [sélectionner une audience](#select-audience), car toutes les informations préalables des autres étapes seront importées à partir de la connexion existante.

Une connexion aux données est la source de données à partir de laquelle vous importez des audiences dans Real-Time CDP Collaboration. Actuellement, la seule connexion de données prise en charge est Adobe Experience Platform.

Tous les paramètres tels que la planification que vous configurez pour votre connexion de données sont appliqués à toutes les audiences importées à partir de cette connexion de données.

>[!TIP]
>
>Il existe un workflow distinct où vous pouvez afficher et modifier vos connexions de données. Pour plus d’informations, consultez le guide [gestion des connexions aux données](/help/guide/setup/manage-data-connection.md).

Pour commencer à ajouter votre connexion de données, sélectionnez **[!UICONTROL Ajouter une nouvelle connexion de données]** puis sélectionnez **[!UICONTROL Suivant]**.

![L’espace de travail Ajouter des audiences avec l’option Ajouter une nouvelle connexion de données mise en surbrillance.](/help/assets/setup/add-manage-audiences/add-data-connection.png)

#### Sélectionner une source de données

Vous allez ensuite choisir la source de votre connexion aux données. Les sources disponibles sont les suivantes :

* **Adobe Experience Platform** : sélectionnez cette option pour importer vos audiences depuis Adobe Experience Platform Real-Time CDP.
* **Fichier CSV** (version ultérieure) : chargez un fichier CSV contenant les données de votre audience pour une ingestion de données simple et rapide.
* **Amazon Web Services** (version ultérieure) : connectez-vous à votre stockage Amazon S3 pour importer les données d’audience directement à partir de vos compartiments S3.
* **Snowflake** (version ultérieure) : utilisez votre entrepôt de données Snowflake pour extraire facilement les données d’audience.

Sélectionnez votre source de données, puis sélectionnez **[!UICONTROL Suivant]**.

![Espace de travail Ajouter des audiences avec l’option Adobe Experience Platform mise en surbrillance.](/help/assets/setup/add-manage-audiences/select-data-connection-source.png)

#### Sélectionner un sandbox

Après avoir sélectionné votre source de données, vous devez sélectionner le sandbox qui inclut les audiences que vous importerez. Sélectionnez le sandbox dans la liste des sandbox disponibles, puis sélectionnez **[!UICONTROL Suivant]**

![Espace de travail Ajouter des audiences avec un sandbox sélectionné.](/help/assets/setup/add-manage-audiences/select-sandbox.png)

#### Politique de gouvernance et mesures d’application {#governance-policy-and-enforcement-actions}

Ensuite, vous devez vous assurer que les actions marketing correctes sont définies sur les données importées. Vous devez également donner votre consentement pour que les données importées depuis Real-Time CDP soient utilisées pour la collaboration sur les données.

Utilisez des actions marketing pour contrôler les données d’audience à importer dans Real-Time CDP Collaboration à partir d’Experience Platform. L’action marketing **Collaboration de données** prend en charge les libellés d’utilisation des données C4, C5 et C9. L’action marketing **Science des données** prend en charge le libellé d’utilisation des données C9.

En savoir plus sur les libellés d’utilisation des données [C4, C5 et C9](https://experienceleague.adobe.com/en/docs/experience-platform/data-governance/labels/reference#contract){target="_blank"}.

* Lorsque la case à cocher est *activée*, toutes les données marquées avec les libellés mentionnés ci-dessus dans Experience Platform sont exclues et ne sont *pas* importées dans Real-Time CDP Collaboration.
* Lorsque la case à cocher est *désactivée*, il n’existe aucune restriction sur les données d’Experience Platform qui peuvent être importées dans Real-Time CDP Collaboration.

Consultez la documentation d’Experience Platform pour en savoir plus sur les libellés d’utilisation des données :

* [Présentation des libellés d’utilisation des données](https://experienceleague.adobe.com/fr/docs/experience-platform/data-governance/labels/overview){target="_blank"}
* [Glossaire des libellés d’utilisation des données](https://experienceleague.adobe.com/en/docs/experience-platform/data-governance/labels/reference){target="_blank"}

En outre, vous souhaiterez sélectionner vos règles de consentement à appliquer aux données importées dans Real-Time CDP Collaboration.

![Espace de travail Ajouter des audiences à la section Politique de gouvernance et application des actions ](/help/assets/setup/add-manage-audiences/data-collaboration-consent.png).

Une fois que vous avez sélectionné les actions marketing et les règles de consentement, sélectionnez **[!UICONTROL Suivant]** pour passer à l’étape suivante. Une boîte de dialogue de confirmation s’affiche, vous demandant d’accepter les conditions. Cochez la case, puis sélectionnez **[!UICONTROL OK]** pour confirmer.

![La boîte de dialogue Politique de gouvernance et appliquer des actions avec la case à cocher et l’option OK mises en surbrillance.](/help/assets/setup/add-manage-audiences/data-collaboration-consent-confirmation.png)

### Fournir des détails

Indiquez ensuite un nom et une description pour votre connexion de données. Ces informations vous aideront à identifier la connexion de données ultérieurement.

![Espace de travail Ajouter des audiences avec la possibilité de fournir un nom et une description.](/help/assets/setup/add-manage-audiences/data-connection-details.png)

### Champs de mappage {#map-fields}

>[!CONTEXTUALHELP]
>id="rtcdp_collaboration_import_audience_mapping_source_fields"
>title="Champs sources"
>abstract="Les champs Source sont des espaces de noms d’identité et des attributs de votre implémentation existante de Real-Time CDP. Vous pouvez les mapper à des champs cibles définis dans Real-Time CDP Collaboration."

>[!CONTEXTUALHELP]
>id="rtcdp_collaboration_import_audience_mapping_target_fields"
>title="Champs cibles"
>abstract="Actuellement, les e-mails hachés sont les seules clés correspondantes prises en charge."

>[!CONTEXTUALHELP]
>id="rtcdp_collaboration_import_audience_mapping_apply_transformation"
>title="Appliquer la transformation"
>abstract="Lors de l’import de champs *non hachés* à partir de votre source, utilisez cette option pour que Real-Time CDP Collaboration applique le hachage et transforme les champs simples en champs hachés."

>[!CONTEXTUALHELP]
>id="rtcdp_collaboration_import_audience_mapping_identity_namespaces"
>title="Espaces de noms d’identité"
>abstract="Sélectionnez un espace de noms d’identité dans les espaces de noms d’identité standard et personnalisés disponibles dans votre organisation Experience Platform."
>additional-url="https://experienceleague.adobe.com/docs/experience-platform/identity/features/namespaces.html#standard?lang=fr" text="Espaces de noms standard et d’identité dans Experience Platform"

>[!CONTEXTUALHELP]
>id="rtcdp_collaboration_import_audience_mapping_profile_attributes"
>title="Attributs de profil"
>abstract="Sélectionnez des attributs dans le schéma d’union pour la classe Profil dans Experience Platform. Cette vue affiche les attributs présents dans le schéma d’union et appartenant à la classe XDM Profil individuel."
>additional-url="https://experienceleague.adobe.com/docs/experience-platform/profile/union-schemas/union-schema.html?lang=fr" text="Schéma d’union dans Experience Platform"

Vous allez ensuite sélectionner les champs sources à mapper aux champs cibles dans Real-Time CDP Collaboration.

![Espace de travail Ajouter des audiences avec la possibilité de mapper les champs sources aux champs cibles.](/help/assets/setup/add-manage-audiences/add-map-fields.png)

>[!TIP]
>
>Vous pouvez mapper plusieurs champs sources au même champ cible. Par exemple, si des adresses e-mail se trouvent dans deux champs distincts d’Experience Platform, vous pouvez les mapper tous les deux au champ cible **[!UICONTROL E-mail haché]** sous la forme de deux lignes distinctes.

>[!BEGINSHADEBOX]

Les **[!UICONTROL champs Source]** sont des espaces de noms d’identité et des attributs de votre implémentation existante de Real-Time CDP. Voici comment les identités existent dans la source à partir de laquelle vous importez des données. Les champs Source sont mappés sur les champs cibles définis dans Real-Time CDP Collaboration.

**[!UICONTROL Champs cibles]** indiquez comment les identités sont référencées dans Real-Time CDP Collaboration. Actuellement, les e-mails hachés sont les seules clés correspondantes prises en charge.

Utilisez l’option **[!UICONTROL Appliquer la transformation]** lorsque vous importez des champs *non hachés* de votre source. Dans ce cas, Real-Time CDP Collaboration effectue le hachage et transforme les champs. L’algorithme de hachage utilisé par Adobe est SHA256.

>[!ENDSHADEBOX]

Sélectionnez le champ source vide en regard du champ cible. La boîte de dialogue **[!UICONTROL Sélectionner le champ source]** s’affiche. Sélectionnez entre les options **[!UICONTROL Espaces de noms d’identité]** et **[!UICONTROL Attributs de profil]** pour trouver le champ source souhaité, puis sélectionnez le champ source dans la liste à l’aide de l’option de recherche pour trouver le champ souhaité.

![La boîte de dialogue Sélectionner le champ source avec les options d’e-mail affichées.](/help/assets/setup/add-manage-audiences/select-source-field.png)

Pour gérer plusieurs champs d’e-mail, mappez le champ source d’e-mail non haché à l’aide de **[!UICONTROL Apply transformation]**.

![L’espace de travail Ajouter des audiences avec les champs sources d’e-mail mappés au champ cible, avec l’option Appliquer la transformation activée pour l’un.](/help/assets/setup/add-manage-audiences/apply-transformation.png)

Continuez à ajouter des paires de mappage si nécessaire, puis sélectionnez **[!UICONTROL Suivant]**.

### Planning {#schedule}

Ensuite, planifiez les dates de début et de fin du remplissage des audiences. L’audience sera actualisée selon ce planning.

![L’espace de travail Ajouter une audience avec les options de planification affichées.](/help/assets/setup/add-manage-audiences/audience-scheduling.png)

>[!IMPORTANT]
>
>Le réglage de la fréquence des mises à jour de l’audience permet de gérer l’[activité de crédit Gestion de l’audience](/help/guide/setup/my-activity.md#types-of-activities), qui est calculée par actualisation de l’audience. La sélection d’une fréquence plus élevée peut avoir un impact sur l’actualisation des données disponibles pour les rapports de découverte d’audience et l’activation d’audience.

Sélectionnez la fréquence d’actualisation de l’audience dans le menu déroulant **[!UICONTROL Fréquence]**.

![L’espace de travail Ajouter des audiences de planification avec la liste déroulante Fréquence ouverte.](/help/assets/setup/add-manage-audiences/audience-scheduling-frequency.png)

Sélectionnez ensuite la **[!UICONTROL Période]**. La date de début est la date à laquelle l’audience commencera à remplir avec des profils, et la date de fin est la date à laquelle l’audience cessera de s’actualiser.

![L’espace de travail de planification Ajouter des audiences avec l’option Période affichée.](/help/assets/setup/add-manage-audiences/audience-scheduling-date-range.png)

>[!IMPORTANT]
>
>Après la date de fin dans la période, toutes les audiences importées à partir de cette connexion de données cesseront de s’actualiser. Pour renouveler la connexion, accédez à [Gérer la connexion de données](/help/guide/setup/manage-data-connection.md) et définissez une nouvelle date de fin.

### Sélectionner des audiences {#select-audience}

Après avoir sélectionné la source de l’audience, vous choisirez des audiences spécifiques à inclure. Utilisez les options de recherche et de filtrage pour trouver les audiences appropriées à partir de votre source de données. Sélectionnez les audiences de votre choix, puis sélectionnez **[!UICONTROL Suivant]**.

![L’espace de travail Ajouter des audiences avec une liste des audiences disponibles.](/help/assets/setup/add-manage-audiences/select-audience.png)

### Réviser

Passez en revue toutes les configurations et tous les paramètres avant de finaliser l’ajout de l’audience. Assurez-vous que tous les détails sont corrects, puis sélectionnez **[!UICONTROL Terminé]** pour terminer la création de votre connexion aux données.

![L’espace de travail Ajouter des audiences avec toutes les configurations sélectionnées affichées.](/help/assets/setup/add-manage-audiences/review-connection.png)

## Afficher le tableau de bord des audiences {#view-audiences-dashboard}

>[!CONTEXTUALHELP]
>id="rtcdp_collaboration_view_audience_missing_identities"
>title="Identités manquantes"
>abstract="Le nombre d’identités sera disponible après la prochaine actualisation de la connexion de données suivant le planning configuré. L’actualisation initiale se produit généralement dans les 24 heures suivant la configuration de la connexion aux données. Les actualisations en cours suivront le planning configuré. "

Après avoir importé des audiences dans Real-Time CDP Collaboration, l’espace de travail **[!UICONTROL Mes audiences]** affiche toutes les audiences actuellement importées dans Real-Time CDP Collaboration par votre organisation.


Chaque audience contient un aperçu des informations suivantes :

| Élément | Description |
|----------|---------|
| **[!UICONTROL Identités]** | Indique le nombre d’identités présentes dans cette audience. Notez que si le même profil possède plusieurs identités et que ces identités sont utilisées comme clés de correspondance dans le projet, le profil s’affichera deux fois dans le décompte. |
| **[!UICONTROL Statut]** | Indique si l’audience est active et peut être utilisée dans des projets. Un statut **[!UICONTROL En attente]** indique que l’audience vient d’être importée et que les membres de l’audience doivent encore être renseignés. Les audiences importées sont renseignées avec des profils après l’actualisation initiale, qui se produit généralement dans les 24 heures suivant la configuration de la connexion aux données. |
| **[!UICONTROL Source]** | Indique la source à partir de laquelle l’audience a été importée. Dans la version actuelle de Real-Time CDP Collaboration, Adobe Experience Platform est la seule source prise en charge. |
| **[!UICONTROL Connexion aux données]** | Connexion de données à partir de laquelle l’audience est sourcée. Vous pouvez sélectionner le nom pour afficher la connexion de données. |
| **[!UICONTROL Accès à la connexion]** | Définit si l’audience est privée ou publique. Les audiences publiques sont détectables dans les rapports de chevauchement et peuvent être activées dans un projet. |
| **[!UICONTROL Créé]** | Indique la date à laquelle l’audience a été importée dans Real-Time CDP Collaboration. |
| **[!UICONTROL Dernière mise à jour]** | Indique la date et l’heure de la dernière mise à jour d’un aspect de l’audience. |

![Espace de travail Mon audience affichant toutes les audiences importées.](/help/assets/setup/add-manage-audiences/audiences-workspace.png)

Pour effectuer des actions rapides sur une audience, sélectionnez les points de suspension **...** en regard du nom de l’audience. Les options disponibles sont les suivantes :

* **[!UICONTROL Modifier les catégories]** vous permet d’ajouter différentes balises de catégorie à l’audience. Pour plus d’informations, reportez-vous à la section [catégories](#categories) ci-dessous.
* **[!UICONTROL Supprimer]** supprimera l’audience de la connexion aux données.

![L’espace de travail Mes audiences avec le menu représentant des points de suspension ouvert et les options Modifier les catégories et Supprimer mises en surbrillance.](/help/assets/setup/add-manage-audiences/audiences-ellipsis-menu.png)

## Affichage d’audiences individuelles {#view-individual-audiences}

Pour afficher plus d’informations et modifier des configurations pour une audience individuelle, sélectionnez l’audience dans l’espace de travail **[!UICONTROL Mes audiences]**. L’espace de travail des audiences affiche des informations détaillées sur l’audience sélectionnée, notamment ses détails, identités, catégories, accès à la connexion et paramètres de visibilité des métadonnées.

### Détails de l’audience

Les informations suivantes s’affichent pour chaque audience :

| Élément | Description |
|----------|---------|
| **[!UICONTROL Statut]** | Indique si l’audience est active et peut être utilisée dans des projets. |
| **[!UICONTROL Source]** | Indique la source à partir de laquelle l’audience a été importée. Dans la version actuelle de Real-Time CDP Collaboration, Adobe Experience Platform est la seule source prise en charge. |
| **[!UICONTROL Connexion aux données]** | Connexion de données à partir de laquelle l’audience est sourcée. |
| **[!UICONTROL Dernière mise à jour]** | Indique la date et l’heure de la dernière mise à jour de l’audience. |
| **[!UICONTROL Dernière mise à jour par]** | Indique le dernier utilisateur à avoir mis à jour l’audience. |
| **[!UICONTROL Créé]** | Indique la date à laquelle l’audience a été importée dans Real-Time CDP Collaboration. |
| **[!UICONTROL Créé par]** | Indique l’utilisateur qui a importé l’audience dans Real-Time CDP Collaboration. |

![Espace de travail d’une audience individuelle.](/help/assets/setup/add-manage-audiences/audience-details.png)

De plus, les commandes suivantes sont disponibles dans l’espace de travail des audiences :

* **[!UICONTROL Supprimer]** : supprimez l’audience de votre connexion aux données.
* **[!UICONTROL Modifier]** : modifiez le nom ou la description de l’audience.

![Espace de travail d’une audience individuelle avec l’option Modifier et supprimer mise en surbrillance.](/help/assets/setup/add-manage-audiences/audience-details-edit-delete.png)

Vous pouvez ensuite mettre à jour les sections suivantes dans l’espace de travail de l’audience :

* [Identités](#identities)
* [Catégories](#categories)
* [Accès à la connexion](#connection-access)
* [Visibilité des métadonnées](#metadata-visibility)

### Identités {#identities}

>[!CONTEXTUALHELP]
>id="rtcdp_collaboration_view_audience_identities"
>title="Identités"
>abstract="Une vue de répartition des identités qui composent cette audience, ainsi qu’un nombre total de profils avec les identités respectives."

La section **[!UICONTROL Identités]** indique le nombre de profils présents dans l’audience avec l’une des identités que vous avez sélectionnées lors de l’importation de l’audience. La section contient également une répartition des identités afin que vous puissiez identifier les identités qui constituent le plus de la population de l’audience.

![Section Identités de l’espace de travail d’une audience individuelle.](/help/assets/setup/add-manage-audiences/audience-details-identities.png)

### Catégories {#categories}

>[!CONTEXTUALHELP]
>id="rtcdp_collaboration_view_audience_categories"
>title="Catégories"
>abstract="Balisez vos audiences pour une organisation, un filtrage et une récupération faciles. Vous pouvez baliser une audience avec plusieurs catégories, puis utiliser ces balises de catégorie pour filtrer les audiences de votre choix dans d’autres zones du produit."

Pour une organisation, un filtrage et une récupération faciles des audiences, vous pouvez baliser vos audiences. Vous pouvez baliser une audience avec plusieurs catégories, puis utiliser ces balises de catégorie pour filtrer les audiences souhaitées dans la zone de produit [Discover](/help/guide/collaborate/discover.md) lors de l’exécution de rapports de chevauchement d’audiences.

Pour ajouter des catégories, sélectionnez l’option **[!UICONTROL Modifier]** dans la section **[!UICONTROL Catégories]**.

![Section Catégories de l’espace de travail d’une audience individuelle.](/help/assets/setup/add-manage-audiences/audience-details-categories.png)

La boîte de dialogue **[!UICONTROL Catégories]** s’affiche, vous permettant de sélectionner les catégories que vous souhaitez ajouter à l’audience. Pour sélectionner une catégorie individuelle, cochez la case en regard du nom de la catégorie.

![La boîte de dialogue Catégories avec les catégories disponibles affichées.](/help/assets/setup/add-manage-audiences/audience-details-categories-select.png)

### Accès à la connexion {#connection-access}

>[!CONTEXTUALHELP]
>id="rtcdp_collaboration_view_audience_connection_access"
>title="Accès à la connexion"
>abstract="<p>Les audiences peuvent être de trois types : publiques, privées et personnalisées.</p><p> Leur disponibilité pour une utilisation dans des projets avec des collaborateurs et collaboratrices diffère en fonction du paramètre d’accès à la connexion. Vous pouvez toujours modifier l’accès à la connexion de privé à public, mais vous ne pouvez pas revenir en arrière une fois qu’une audience est activée avec des collaborateurs.</p>"

La disponibilité d’une audience à utiliser dans des projets avec des collaborateurs diffère en fonction du paramètre d’accès à la connexion. Dans la section **[!UICONTROL Accès à la connexion]**, vous pouvez choisir si l’audience doit être privée ou utilisable et détectable dans les connexions.

Pour mettre à jour l’accès à la connexion de l’audience, sélectionnez l’option **[!UICONTROL Modifier]** dans la section **[!UICONTROL Accès à la connexion]**.

![Section Accès à la connexion de l’espace de travail d’une audience individuelle.](/help/assets/setup/add-manage-audiences/audience-details-connection-access.png)

La boîte de dialogue **[!UICONTROL Accès de connexion]** s’affiche, avec trois options d’accès de connexion disponibles :

* **[!UICONTROL Audience privée]**. Ces audiences ne sont *pas* disponibles pour une utilisation dans les rapports de chevauchement ou pour une activation dans les connexions avec des collaborateurs. Bien que les audiences ne soient pas disponibles pour les collaborateurs, la population des audiences contribue toujours à la population totale dans la vue **[!UICONTROL Toutes les audiences]** dans la section [Comparer les audiences](/help/guide/collaborate/discover.md#compare-audiences). Définissez le paramètre sur public ou personnalisé pour utiliser les audiences dans les connexions avec les collaborateurs.
* **[!UICONTROL Public audience]**. Ces audiences peuvent être utilisées dans les rapports de chevauchement et pour l’activation dans les connexions avec des collaborateurs.
* **[!UICONTROL Audience personnalisée]**. Ces audiences peuvent uniquement être utilisées dans les rapports de chevauchement et pour l’activation dans des connexions spécifiées. Bien que les audiences ne soient pas disponibles pour les collaborateurs, la population des audiences contribue toujours à la population totale dans la vue **[!UICONTROL Toutes les audiences]** dans la section [Comparer les audiences](/help/guide/collaborate/discover.md#compare-audiences).

Sélectionnez l’option d’accès à la connexion souhaitée, puis sélectionnez **[!UICONTROL Enregistrer]** pour appliquer les modifications.

![La boîte de dialogue Accès à la connexion avec les options disponibles s’affiche.](/help/assets/setup/add-manage-audiences/audience-details-connection-access-dialog.png)

>[!IMPORTANT]
>
>Quel que soit le statut d’accès (public, privé ou personnalisé), la population de toute audience contribue à la population **[!UICONTROL Toutes les audiences]** dans la section **[!UICONTROL Comparer les audiences]** d’un projet.<br>

La disponibilité de l’audience à utiliser dans les projets avec des collaborateurs diffère selon le paramètre d’accès à la connexion. Vous pouvez toujours modifier l’accès à la connexion de privé à public, mais vous ne pouvez pas revenir en arrière une fois qu’une audience est activée.

### Visibilité des métadonnées {#metadata-visibility}

>[!CONTEXTUALHELP]
>id="rtcdp_collaboration_view_audience_metadata_visibility"
>title="Visibilité des métadonnées"
>abstract="<p>Indique laquelle des métadonnées de l’audience est visible par d’autres organisations avant qu’elles ne se connectent à votre organisation. </p> <p> Le **Nombre d’identités** vérifie si votre partenaire peut afficher les chiffres des identités de vos audiences lors de l’affichage des rapports de chevauchement dans l’onglet de découverte. Le **Pourcentage de chevauchement des audiences** contrôle si les collaborateurs et collaboratrices sont en mesure de découvrir des pourcentages de chevauchement entre leurs audiences et les vôtres."

>[!NOTE]
>
>Si toutes les audiences de votre collaborateur sont définies sur privées, la section **[!UICONTROL Audiences pertinentes]** d’un projet dans l’espace de travail **[!UICONTROL Découvrir]** sera vide. Pour plus d’informations, lisez le [Discover](/help/guide/collaborate/discover.md#relevant-audiences). guide.

La visibilité des métadonnées indique la visibilité des métadonnées d’une audience sur d’autres organisations avant qu’elles ne se connectent à votre organisation ou dans différentes vues de projet. Pour mettre à jour la visibilité des métadonnées de l’audience, sélectionnez l’option **[!UICONTROL Modifier]** dans la section **[!UICONTROL Visibilité des métadonnées]**.

![Section Visibilité des métadonnées de l’espace de travail d’une audience individuelle.](/help/assets/setup/add-manage-audiences/audience-details-metadata.png)

La boîte de dialogue **[!UICONTROL Visibilité des métadonnées]** s’affiche, vous permettant de configurer les paramètres de visibilité de l’audience. Vous pouvez configurer deux paramètres de visibilité des métadonnées pour chaque audience :

**[!UICONTROL Afficher le nombre d’identités]** : ce paramètre contrôle si votre collaborateur peut afficher le nombre d’identités de vos audiences lors de l’[affichage de rapports de chevauchement dans l’onglet Détection](/help/guide/collaborate/discover.md#discover-overlaps) au sein d’un projet.

**[!UICONTROL Afficher le chevauchement des audiences %]** : lorsque ce paramètre est défini sur true, les collaborateurs peuvent [découvrir des pourcentages de chevauchement](/help/guide/collaborate/discover.md#compare-audiences) entre leurs audiences et vos audiences.

![La boîte de dialogue Visibilité des métadonnées avec les options disponibles s’affiche.](/help/assets/setup/add-manage-audiences/audience-details-metadata-dialog.png)

## Étapes suivantes

Après l’importation des audiences, il est temps de découvrir les éditeurs avec lesquels [se connecter](/help/guide/connect/establishing-connections.md) et commencer à collaborer sur des projets.
