---
title: Importer et gérer des audiences
description: Découvrez comment importer et gérer des audiences dans Adobe Real-Time CDP Collaboration
audience: admin, publisher, advertiser
badgelimitedavailability: label="Disponibilité limitée" type="Informative" url="https://helpx.adobe.com/legal/product-descriptions/real-time-customer-data-platform-collaboration.html newtab=true"
exl-id: 0a5158fa-73d3-4406-af20-2b6c7be9934e
source-git-commit: dd1386f9371cb40285315d11e07b139d3115e147
workflow-type: tm+mt
source-wordcount: '2685'
ht-degree: 24%

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

Avant de pouvoir partager des audiences avec des collaborateurs et exécuter des calculs de chevauchement, les audiences doivent être importées dans Real-Time CDP Collaboration. Pour importer des audiences, suivez les étapes du workflow décrites dans la section ci-dessous.

![Mes audiences s’affichent avant que des audiences aient été ajoutées à l’organisation.](/help/assets/setup/add-manage-audiences/org-without-audiences-added.png)

Dans l’onglet **[!UICONTROL Mes audiences]**, sélectionnez le symbole Plus **+**, puis sélectionnez **Audience**.

### Sélectionner la connexion de données {#select-data-connection}

>[!CONTEXTUALHELP]
>id="rtcdp_collaboration_import_audience_marketing_actions"
>title="Actions marketing"
>abstract="<p>Utilisez des actions marketing pour contrôler les données d’audience à importer dans Real-Time CDP Collaboration à partir d’Experience Platform. L’action marketing <strong>Collaboration de données</strong> prend en charge les libellés d’utilisation des données C4, C5 et C9. L’action marketing <strong>Science des données</strong> prend en charge le libellé d’utilisation des données C9.</p> <p> <ul><li> Lorsque la case à cocher est <em>activée</em>, toutes les données marquées avec les libellés mentionnés ci-dessus dans Experience Platform sont exclues et ne sont <strong> pas</strong> importées dans Real-Time CDP Collaboration.</li><li> Lorsque la case à cocher est <em>désactivée</em>, il n’existe aucune restriction sur les données d’Experience Platform qui peuvent être importées dans Real-Time CDP Collaboration.</li></ul></p>"
>additional-url="https://experienceleague.adobe.com/docs/experience-platform/data-governance/labels/overview.html?lang=fr" text="Présentation des libellés d’utilisation des données"
>additional-url="https://experienceleague.adobe.com/docs/experience-platform/data-governance/labels/reference.html?lang=fr" text="Glossaire des étiquettes dʼutilisation des données"

>[!IMPORTANT]
>
>Après vous être connecté à votre première connexion de données et avoir importé votre première audience, vous pouvez choisir d’importer plusieurs audiences à partir de cette connexion de données existante. Dans ce cas, le workflow vous mènera directement à l’étape [sélectionner l’audience](#select-audience), car toutes les informations préalables des autres étapes seront importées à partir de la connexion existante.

Une connexion aux données est la source de données à partir de laquelle vous importez des audiences dans Real-Time CDP Collaboration. Pour la première version de Real-Time CDP Collaboration, la seule connexion de données prise en charge est Adobe Experience Platform.

Tous les paramètres tels que le mappage d’identité ou la planification que vous configurez pour votre connexion de données sont appliqués à toutes les audiences importées à partir de cette connexion de données.

>[!TIP]
>
>Il existe un workflow distinct où vous pouvez toujours afficher et modifier toutes les connexions de données que vous avez ajoutées à cette étape. En savoir plus sur la [gestion des connexions de données](/help/guide/setup/manage-data-connection.md).

![Écran de sélection de la source de l’audience affichant les options pour AEP RTCDP, le fichier CSV, Amazon S3 et Snowflake.](/help/assets/setup/add-manage-audiences/Step-Select-Audience-Source.png)

#### Sélectionner une source de données

Au cours de cette étape, vous allez choisir la source des données de votre audience. Les sources disponibles sont les suivantes :

* **Adobe Experience Platform** : sélectionnez cette option pour importer vos audiences depuis Adobe Experience Platform Real-Time CDP.
* **Fichier CSV** (version ultérieure) : chargez un fichier CSV contenant les données de votre audience pour une ingestion de données simple et rapide.
* **Amazon Web Services** (version ultérieure) : connectez-vous à votre stockage Amazon S3 pour importer les données d’audience directement à partir de vos compartiments S3.
* **Snowflake** (version ultérieure) : utilisez votre entrepôt de données Snowflake pour extraire facilement les données d’audience.

#### Sélectionner un sandbox

Après avoir sélectionné **Adobe Experience Platform** comme source de données, vous devez sélectionner le sandbox qui inclut les audiences que vous importerez.

![Sélectionner un sandbox pour importer des audiences](/help/assets/setup/add-manage-audiences/import-audiences-select-sandbox.png)

Sélectionnez **[!UICONTROL Suivant]** après avoir sélectionné la sandbox de votre choix.

#### Politique de gouvernance et mesures d’application {#governance-policy-and-enforcement-actions}

Ensuite, vous devez vous assurer que les actions marketing correctes sont définies sur les données importées. Vous devez également donner votre consentement pour que les données importées depuis Real-Time CDP soient utilisées pour la collaboration sur les données.

Utilisez des actions marketing pour contrôler les données d’audience à importer dans Real-Time CDP Collaboration à partir d’Experience Platform. L’action marketing **Collaboration de données** prend en charge les libellés d’utilisation des données C4, C5 et C9. L’action marketing **Science des données** prend en charge le libellé d’utilisation des données C9.

En savoir plus sur les libellés d’utilisation des données [C4, C5 et C9](https://experienceleague.adobe.com/en/docs/experience-platform/data-governance/labels/reference#contract){target="_blank"}.

* Lorsque la case à cocher est *activée*, toutes les données marquées avec les libellés mentionnés ci-dessus dans Experience Platform sont exclues et ne sont *pas* importées dans Real-Time CDP Collaboration.
* Lorsque la case à cocher est *désactivée*, il n’existe aucune restriction sur les données d’Experience Platform qui peuvent être importées dans Real-Time CDP Collaboration.

Consultez la documentation d’Experience Platform pour en savoir plus sur les libellés d’utilisation des données :

* [Présentation des libellés d’utilisation des données](https://experienceleague.adobe.com/en/docs/experience-platform/data-governance/labels/overview){target="_blank"}
* [Glossaire des libellés d’utilisation des données](https://experienceleague.adobe.com/en/docs/experience-platform/data-governance/labels/reference){target="_blank"}

![Actions marketing requises pour la collaboration sur les données.](/help/assets/setup/add-manage-audiences/data-collaboration-consent.png)

### Fournir des détails

Ensuite, fournissez un nom et une description pour que vous puissiez reconnaître cette connexion de données à l’avenir.

<!--

>[!IMPORTANT]
>
>Note a difference in terminology where the sandbox selected from Real-Time CDP is considered a dataset in the UI in Real-Time CDP Collaboration.

-->

### Champs de mappage {#map-fields}

>[!CONTEXTUALHELP]
>id="rtcdp_collaboration_import_audience_mapping_source_fields"
>title="Champs sources"
>abstract="Les champs Source sont des espaces de noms d’identité et des attributs de votre implémentation existante de Real-Time CDP. Vous pouvez les mapper à des champs cibles définis dans Real-Time CDP Collaboration."

>[!CONTEXTUALHELP]
>id="rtcdp_collaboration_import_audience_mapping_target_fields"
>title="Champs cibles"
>abstract="Les champs cibles sont liés aux clés correspondantes que vous avez sélectionnées lors de l’intégration de votre entreprise. Actuellement, les e-mails hachés sont les seules clés correspondantes prises en charge."

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

>[!CONTEXTUALHELP]
>id="rtcdp_collaboration_destinations_target_namespaces"
>title="Espaces de noms cibles"
>abstract="Cette partie sera complétée d’une description appropriée."

![Écran Mapper les champs affichant les champs source mappés aux champs cibles.](/help/assets/setup/add-manage-audiences/Step-Map-Fields.png)

Dans l’étape Mapper les champs , vous pouvez sélectionner le mappage des champs d’identité pour les profils importés à partir de la connexion aux données aux clés de correspondance que vous avez sélectionnées dans votre organisation.

>[!TIP]
>
>Vous pouvez mapper plusieurs champs sources au même champ cible. Par exemple, si des adresses e-mail se trouvent dans deux champs distincts d’Experience Platform, vous pouvez les mapper tous les deux au champ cible **[!UICONTROL E-mail haché]** sous la forme de deux lignes distinctes.

>[!BEGINSHADEBOX]

Les champs **[!UICONTROL Source]** indiquent la manière dont les identités sont référencées dans la source à partir de laquelle vous importez des données.

**[!UICONTROL Champs cibles]** indiquez comment les identités sont référencées dans Real-Time CDP Collaboration. Les valeurs que vous pouvez sélectionner ici correspondent aux clés de correspondance que vous configurez dans le workflow d’intégration de l’entreprise.

Utilisez l’option **[!UICONTROL Appliquer la transformation]** lorsque vous importez des champs *non hachés* de votre source. Dans ce cas, Real-Time CDP Collaboration effectue le hachage et transforme les champs. L’algorithme de hachage utilisé par Adobe est SHA256.

>[!ENDSHADEBOX]

Ajoutez autant de paires de mappage que nécessaire et sélectionnez **[!UICONTROL Suivant]** pour passer à l’étape suivante.

<!--

In this step, you can also add any identity crosswalks that you would like to use.

Identity crosswalks will be supported after the beta release.

#### Add identity crosswalk

Use identity crosswalks to connect different identifiers across datasets to enrich your audience data with additional attributes or dimensions. 

TODO add GIF Identity crosswalks screen showing a list of available identity crosswalks with details.

Select **[!UICONTROL Add identity crosswalk]** to see a screen where you can choose from various identity crosswalks that you have previously [imported into Real-Time CDP Collaboration](/help/guide/setup/identity-crosswalk.md#import-crosswalk). Each entry includes details such as the table name, type, description, and creation date.

After selecting the desired crosswalk, use a source field join key to map to the crosswalk table join key. 

>[!NOTE]
>
>After selecting an identity crosswalk, the **[!UICONTROL Add identity crosswalk]** control is greyed out. 

For further reading about identity crosswalks, refer to the [glossary](/help/guide/glossary.md).

-->


<!-- will uncomment this part when Manage use cases part becomes available

### Manage use cases {#manage-use-cases}

>[!CONTEXTUALHELP]
>id="rtcdp_collaboration_import_audience_usecases"
>title="Use cases for identities"
>abstract="This control is disabled in the initial release of Real-Time CDP Collaboration"

![Manage use cases screen.](/help/assets/setup/add-manage-audiences/Step-manage-use-cases.png)

For every identity selected in the mapping step, select the use cases that you can use the identity for. Available use cases are: 

* Discover
* Share
* Activate
* Measure

Note that this control is disabled in the initial release of Real-Time CDP Collaboration.

After selecting the desired use cases for each identity, proceed to the next step. 

-->›

### Planning {#schedule}

>[!CONTEXTUALHELP]
>id="rtcdp_collaboration_destinations_audience_expiration"
>title="Expiration de l’audience"
>abstract="Détails à venir concernant l’expiration de l’audience."

Planifiez les dates de début et de fin du remplissage et de l’actualisation des audiences. L’appartenance à l’audience sera actualisée conformément à ce planning.

![Écran de planification affichant les dates de début et de fin pour renseigner les audiences.](/help/assets/setup/add-manage-audiences/Step-Schedule.png)

Sélectionnez le taux d’actualisation des audiences. Les options disponibles sont des taux d’actualisation de un à six jours.

>[!IMPORTANT]
>
>Le réglage de la fréquence des mises à jour de l’audience permet de gérer l’[activité de crédit Gestion de l’audience](/help/guide/setup/my-activity.md#types-of-activities), qui est calculée par actualisation de l’appartenance à l’audience. Il peut en résulter moins de données récentes disponibles pour les rapports de découverte d’audience, le partage d’audience et l’activation.

![Écran de planification affichant différents intervalles de fréquence pour la mise à jour de l’appartenance à l’audience.](/help/assets/setup/add-manage-audiences/Step-Schedule-Set-Frequency.png)

>[!IMPORTANT]
>
>Après la date de fin dans la période, toutes les audiences importées à partir de cette connexion de données cesseront de s’actualiser. Pour renouveler la connexion, accédez à [Gérer la connexion de données](/help/guide/setup/manage-data-connection.md) et définissez une nouvelle date de fin.

### Sélectionner des audiences {#select-audience}

Après avoir sélectionné la source de l’audience, vous choisirez des audiences spécifiques à inclure. Utilisez les options de recherche et de filtrage de la page pour trouver les audiences appropriées à partir de la source de données sélectionnée.

![Écran Sélection de l’audience présentant une liste des audiences disponibles avec des cases à cocher pour les sélectionner.](/help/assets/setup/add-manage-audiences/Step-Select-Audience.png)

### Réviser

Passez en revue toutes les configurations et tous les paramètres avant de finaliser l’ajout de l’audience. Assurez-vous que tous les détails sont corrects et sélectionnez **[!UICONTROL Terminé]** pour finaliser le processus.

## Afficher le tableau de bord des audiences {#view-audiences-dashboard}

>[!CONTEXTUALHELP]
>id="rtcdp_collaboration_view_audience_missing_identities"
>title="Identités manquantes"
>abstract="Le nombre d’identités sera disponible après la prochaine actualisation de la connexion de données suivant le planning configuré. L’actualisation initiale se produit généralement dans les 24 heures suivant la configuration de la connexion aux données. Les actualisations en cours suivront le planning configuré. "

Après avoir importé des audiences dans Real-Time CDP Collaboration, vous pouvez obtenir des informations à leur sujet dans une vue de tableau de bord. La vue par défaut de la page **[!UICONTROL Mes audiences]** affiche toutes les audiences actuellement importées par votre organisation dans Real-Time CDP Collaboration.

![Page d’aperçu des audiences présentant toutes les audiences importées par un annonceur](/help/assets/setup/add-manage-audiences/audiences-overview.png)

Vous pouvez afficher les informations pertinentes suivantes sur chaque audience :

| Élément | Description |
|----------|---------|
| **[!UICONTROL Identités]** | Indique le nombre d’identités présentes dans cette audience. Notez que si le même profil possède plusieurs identités et que ces identités sont utilisées comme clés de correspondance dans le projet, le profil s’affichera deux fois dans le décompte. |
| **[!UICONTROL Statut]** | Indique si l’audience est active et peut être utilisée dans des projets. Un statut En attente indique que l’audience vient d’être importée et que les membres de l’audience doivent encore être renseignés. Les audiences importées seront renseignées avec des profils après la prochaine actualisation de la connexion aux données suivant le planning configuré. L’actualisation initiale se produit généralement dans les 24 heures suivant la configuration de la connexion aux données                                         . |
| **[!UICONTROL Source]** | Indique la source à partir de laquelle cette audience a été importée. Dans la version actuelle de Real-Time CDP Collaboration, Adobe Experience Platform est la seule source prise en charge. |
| **[!UICONTROL Connexion aux données]** | D’autres informations d’exploration vers le bas sur l’emplacement d’importation de cette audience. Par exemple, lors de l’importation d’audiences à partir de la source Experience Platform, les sandbox individuels auxquels votre organisation a accès sont considérés comme des connexions de données. |
| **[!UICONTROL Accès à la connexion]** | Définit si cette audience est privée ou publique. Les audiences publiques sont détectables dans les rapports de chevauchement et peuvent être partagées avec les collaborateurs. |
| **[!UICONTROL Créé]** | Indique la date à laquelle cette audience a été importée dans Real-Time CDP Collaboration. |
| **[!UICONTROL Dernière mise à jour]** | Indique la date et l’heure de la dernière mise à jour d’un aspect de cette audience. |

Sélectionnez **[!UICONTROL Gérer les connexions de données]** pour afficher et modifier toutes les connexions de données que vous avez configurées.
Sélectionnez les points de suspension et **[!UICONTROL Supprimer]** pour supprimer l’audience.
Sélectionnez les points de suspension et **[!UICONTROL Modifier les catégories]** pour ajouter différentes balises de catégorie à l’audience. Pour plus d’informations, consultez la section [catégories](/#categories) ci-dessous.
Sélectionnez le nom de l’audience à inspecter ou à modifier.

## Affichage d’audiences individuelles {#view-individual-audiences}

La vue Audience affiche des informations supplémentaires sur votre audience.

![Affichage et inspection d’une audience individuelle.](/help/assets/setup/add-manage-audiences/view-inspect-audience.png)

Les mesures que vous pouvez afficher dans cet écran sont décrites ci-dessous :

| Élément | Description |
|----------|---------|
| **[!UICONTROL Statut]** | Indique si l’audience est active et peut être utilisée dans des projets. |
| **[!UICONTROL Source]** | Indique la source à partir de laquelle cette audience a été importée. Dans la version actuelle de Real-Time CDP Collaboration, Adobe Experience Platform est la seule source prise en charge. |
| **[!UICONTROL Connexion aux données]** | D’autres informations d’exploration vers le bas sur l’emplacement d’importation de cette audience. Par exemple, lors de l’importation d’audiences à partir de la source Experience Platform, les sandbox individuels auxquels votre organisation a accès sont considérés comme des connexions de données. |
| **[!UICONTROL Dernière mise à jour]** | Indique la date et l’heure de la dernière mise à jour d’un aspect de cette audience. |
| **[!UICONTROL Dernière mise à jour par]** | Indique le dernier utilisateur à avoir mis à jour cette audience. |
| **[!UICONTROL Créé]** | Indique la date à laquelle cette audience a été importée dans Real-Time CDP Collaboration. |
| **[!UICONTROL Créé par]** | Indique l’utilisateur qui a importé l’audience dans Real-Time CDP Collaboration. |


Vous pouvez utiliser deux autres commandes sur la page pour modifier ou supprimer des audiences :

* **[!UICONTROL Supprimer]** : supprimez l’audience de votre inventaire.
* **[!UICONTROL Modifier]** : modifiez les métadonnées de l’audience, telles que son nom ou sa description.

![Affichage et inspection d’une audience individuelle.](/help/assets/setup/add-manage-audiences/audiences-edit-delete-controls.png)

Des informations supplémentaires sur l’audience sont disponibles et partiellement modifiables dans les widgets ci-dessous :

![Affichage et inspection d’une audience individuelle.](/help/assets/setup/add-manage-audiences/audiences-further-info-boxes.png)

* [Identités](#identities)
* [Catégories](#categories)
* [Accès à la connexion](#connection-access)
* [Visibilité des métadonnées](#metadata-visibility)

### Identités {#identities}

>[!CONTEXTUALHELP]
>id="rtcdp_collaboration_view_audience_identities"
>title="Identités"
>abstract="Obtenez une vue répartie des identités qui composent cette audience, ainsi que le nombre total de profils avec les identités respectives."

Cette section indique le nombre de profils présents dans l’audience avec l’une des identités que vous avez spécifiées lors de l’importation des audiences. La section contient également une répartition des identités afin que vous puissiez identifier les identités qui constituent le plus de la population de l’audience.

### Catégories {#categories}

>[!CONTEXTUALHELP]
>id="rtcdp_collaboration_view_audience_categories"
>title="Catégories"
>abstract="Balisez vos audiences pour une organisation, un filtrage et une récupération faciles. Vous pouvez baliser une audience avec plusieurs catégories, puis utiliser ces balises de catégorie pour filtrer les audiences de votre choix dans d’autres zones du produit."

Pour une organisation, un filtrage et une récupération faciles des audiences, vous pouvez baliser vos audiences. Vous pouvez baliser une audience avec plusieurs catégories, puis utiliser ces balises de catégorie pour filtrer les audiences souhaitées dans la zone de produit [Discover](/help/guide/collaborate/discover.md) lors de l’exécution de rapports de chevauchement d’audiences.

### Accès à la connexion {#connection-access}

>[!CONTEXTUALHELP]
>id="rtcdp_collaboration_view_audience_connection_access"
>title="Accès à la connexion"
>abstract="<p>Les audiences peuvent être de trois types : publiques, privées et personnalisées.</p><p> Leur disponibilité pour une utilisation dans des projets avec des collaborateurs et collaboratrices diffère en fonction du paramètre d’accès à la connexion. Vous pouvez toujours modifier l’accès à la connexion de privé à public, mais vous ne pouvez pas revenir en arrière une fois qu’une audience est partagée avec des collaborateurs et collaboratrices.</p>"

Choisissez si l’audience doit être privée pour vous ou utilisable et détectable dans les connexions. Les trois options disponibles sont les suivantes :

* **[!UICONTROL Public audience]**. Ces audiences peuvent être utilisées dans les rapports de chevauchement ainsi que pour le partage et l’activation dans les connexions avec n’importe quel collaborateur ou collaboratrice.
* **[!UICONTROL Audience privée]**. Ces audiences ne sont *pas* disponibles pour une utilisation dans les rapports de chevauchement et pour le partage et l’activation dans les connexions avec des collaborateurs. Bien que les collaborateurs ne puissent pas l’afficher ou l’utiliser, la population de cette audience contribue toujours à la population totale dans la vue **[!UICONTROL Toutes les audiences]** de la section [Découvrir et chevaucher](/help/guide/collaborate/discover.md#compare-audiences). Définissez le paramètre sur public ou personnalisé pour utiliser les audiences dans les connexions avec les collaborateurs.
* **[!UICONTROL Audience personnalisée]**. Ces audiences peuvent uniquement être utilisées dans les rapports de chevauchement et pour le partage et l’activation dans des connexions spécifiées. Bien que tous les collaborateurs ne puissent pas l’afficher ou l’utiliser, la population de cette audience contribue toujours à la population totale dans la vue **[!UICONTROL Toutes les audiences]** de la section [découvrir et chevauchements](/help/guide/collaborate/discover.md).

>[!IMPORTANT]
>
>Quel que soit le statut d’accès (public, privé ou personnalisé), la population de toute audience contribue à la population **[!UICONTROL Toutes les audiences]** dans la vue d’analyse de chevauchement Découverte d’audience. <br> ![L’audience **Toutes les audiences** générée par le système dans l’analyse de chevauchement de la découverte d’audiences inclut les audiences avec tous les statuts d’accès aux connexions (publique, privée, personnalisée).](/help/assets/setup/add-manage-audiences/all-audiences-view.png "L’audience générée par le système **Toutes les audiences** dans l’analyse de chevauchement **Découverte d’audiences** inclut les audiences avec tous les statuts d’accès aux connexions (publique, privée, personnalisée)."){width="100" zoomable="yes"}

La disponibilité de l’audience à utiliser dans les projets avec des collaborateurs diffère selon le paramètre d’accès à la connexion. Vous pouvez toujours modifier l’accès à la connexion de privé à public, mais vous ne pouvez pas revenir en arrière une fois qu’une audience est partagée avec des collaborateurs et collaboratrices.

### Visibilité des métadonnées {#metadata-visibility}

>[!CONTEXTUALHELP]
>id="rtcdp_collaboration_view_audience_metadata_visibility"
>title="Visibilité des métadonnées"
>abstract="<p>Précise les informations de métadonnées d’audience qui sont visibles pour d’autres organisations avant qu’elles ne se connectent à votre organisation. </p> <p> Le **Nombre d’identités** vérifie si votre partenaire peut afficher les chiffres des identités de vos audiences lors de l’affichage des rapports de chevauchement dans l’onglet de découverte. Le **Pourcentage de chevauchement des audiences** contrôle si les collaborateurs et collaboratrices sont en mesure de découvrir des pourcentages de chevauchement entre leurs audiences et les vôtres."

>[!NOTE]
>
>Si toutes les audiences de votre collaborateur sont définies sur privées, la vue **[!UICONTROL Audiences pertinentes]** dans les informations sur l’audience sera vide. [En savoir plus](/help/guide/collaborate/discover.md#relevant-audiences).

Indique laquelle des informations de métadonnées d’audience est visible par d’autres organisations avant qu’elles ne se connectent à votre organisation ou dans différentes vues de projet.

**[!UICONTROL Afficher le nombre d’identités]** : ce paramètre contrôle si votre partenaire peut afficher le nombre d’identités de vos audiences lors de l’[affichage de rapports de chevauchement dans l’onglet Détection](/help/guide/collaborate/discover.md#discover-overlaps).

![Images côte à côte avec l’option Afficher le nombre d’identités désélectionnée et sélectionnée.](/help/assets/setup/add-manage-audiences/show-identity-count.png)

**[!UICONTROL Afficher le chevauchement des audiences %]** : lorsque ce paramètre est défini sur true, les collaborateurs peuvent [découvrir des pourcentages de chevauchement](/help/guide/collaborate/discover.md#compare-audiences) entre leurs audiences et l’audience qui vous appartient. Par exemple, dans l’enregistrement ci-dessous, la configuration de l’audience `agora-advertiser-aud3` est définie sur true et un collaborateur peut afficher des pourcentages de chevauchement avec cette audience. Ce paramètre est défini sur false pour l’audience `agora-advertiser-aud1`, de sorte que le collaborateur ne peut pas afficher les pourcentages de chevauchement.

![Pourcentage de chevauchement des audiences pour deux audiences différentes.](/help/assets/setup/add-manage-audiences/audience-overlap-percentage.gif)

## Étapes suivantes

Après avoir importé des audiences, utilisez la section [Connect](/help/guide/connect/establishing-connections.md) pour découvrir les éditeurs avec lesquels vous connecter et commencer à collaborer sur des projets.
