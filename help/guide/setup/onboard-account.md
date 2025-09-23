---
title: Configuration et gestion de votre compte
description: Découvrez comment configurer et gérer divers aspects de votre compte dans Real-Time CDP Collaboration
audience: admin, publisher, advertiser
badgelimitedavailability: label="Disponibilité limitée" type="Informative" url="https://helpx.adobe.com/fr/legal/product-descriptions/real-time-customer-data-platform-collaboration.html newtab=true"
exl-id: a95e932a-9681-48f2-bf34-6fe5a50597d7
source-git-commit: f6ba5bb484f296fe5610901bd7b2e542fb9287b0
workflow-type: tm+mt
source-wordcount: '1361'
ht-degree: 13%

---

# Configuration et gestion de votre compte

{{limited-availability-release-note}}

Découvrez comment configurer votre compte dans Real-Time CDP Collaboration pour préparer les connexions avec d’autres collaborateurs. Ce guide couvre la configuration initiale de votre compte, y compris l’ajout des détails du compte, la sélection des clés de correspondance et la gestion des paramètres de votre compte.

![Espace de travail de configuration affichant un compte configuré.](/help/assets/setup/manage-account/my-account.png){zoomable="yes"}

## Configurer votre compte {#set-up-account}

Lorsque vous accédez à Collaboration pour la première fois, vous êtes invité à configurer votre compte. Il s’agit d’un processus unique qui vous permet de configurer les détails de votre compte et de faire correspondre les clés. S’il s’agit du premier compte de votre entreprise, vous serez immédiatement dirigé tout au long du processus d’intégration, en commençant par la configuration de vos [détails de compte](#set-up-details).

Pour ajouter d’autres organisations, accédez à **[!UICONTROL Configuration]** dans le rail de gauche et sélectionnez l’icône d’ajout (![icône d’ajout).](/help/assets/icons/plus.png)) dans le coin supérieur droit. Sélectionnez ensuite **[!UICONTROL Compte]**.

![Espace de travail de configuration avec l’onglet Mon compte et l’option Compte mises en surbrillance.](/help/assets/setup/manage-account/add-new-account.png){zoomable="yes"}

### Configurer des détails {#set-up-details}

>[!CONTEXTUALHELP]
>id="rtcdp_collaboration_setup_contact_email"
>title="E-mail de contact"
>abstract="Fournissez une adresse e-mail basée sur une équipe ou un rôle, comme **collaboration@votresociete.com**. Des adresses e-mail personnelles ou individuelles ne doivent pas être utilisées."

>[!CONTEXTUALHELP]
>id="rtcdp_collaboration_setup_connect_code"
>title="Code de connexion"
>abstract="Le code de connexion est un identifiant unique de votre compte. Il est utilisé pour établir des connexions avec d’autres collaborateurs et collaboratrice dans Real-Time CDP Collaboration."

Pour commencer à configurer votre compte , vous devez d’abord configurer les détails du compte. Pour ce faire, vous devez ajouter les informations suivantes :

* Ajoutez un **[!UICONTROL Nom du compte]** qui représente clairement votre marque.
* Ajoutez une **[!UICONTROL Description]** votre marque. Cette option est facultative, mais elle aide les autres collaborateurs à mieux comprendre votre marque.
* Sélectionnez votre **[!UICONTROL rôle]**. Vous pouvez choisir entre **[!UICONTROL Annonceur]** et **[!UICONTROL Éditeur]**. Lisez le guide [roles](/help/guide/overview/roles.md) pour voir les similitudes et les légères différences de workflow entre les deux types de rôles de compte.
* Sélectionnez le **[!UICONTROL Secteur]** pour votre compte. Par exemple, **[!UICONTROL Vente au détail]**, **[!UICONTROL Télécommunications]** ou **[!UICONTROL Services financiers]**.
* La **[!UICONTROL Région]** est automatiquement définie en fonction de votre compte Adobe Experience Cloud. Cette valeur ne peut pas être modifiée à tout moment.
* Ajoutez un **[!UICONTROL e-mail de contact]** pour votre compte. Il doit s’agir d’une adresse e-mail d’équipe ou basée sur les rôles. Les adresses e-mail personnelles ne doivent pas être fournies.
* Chargez un **[!UICONTROL Logo]** pour votre compte. Actuellement, les images de type SVG sont prises en charge. Cette opération est facultative, mais le chargement d’un logo permet de représenter visuellement votre marque dans l’interface de Collaboration
* Sélectionnez une image pour l’image d’en-tête de votre compte.

>[!NOTE]
>
>Bien que vous puissiez modifier la plupart de ces détails à tout moment, le **[!UICONTROL rôle]** n’est pas modifiable après la configuration initiale. Lorsque vous avez terminé, utilisez **[!UICONTROL Suivant]** pour passer à la page suivante et sélectionner les clés de correspondance que votre organisation utilisera.

![Espace de travail Configurer le compte avec la section Détails affichée et l’option Suivant mise en surbrillance.](/help/assets/setup/manage-account/add-account-details.png){zoomable="yes"}

### Configurer des clés correspondantes {#set-up-match-keys}

>[!CONTEXTUALHELP]
>id="rtcdp_collaboration_organization_onboarding_matchkeys"
>title="Clés correspondantes"
>abstract="Les clés correspondantes sont des identifiants utilisés pour réconcilier les profils des audiences provenant de différentes sources de données. Incluez toutes les clés correspondantes que votre marque peut utiliser."

>[!CONTEXTUALHELP]
>id="rtcdp_collaboration_organization_onboarding_peopleIDs"
>title="Identifiants propriétaires de personnes"
>abstract="Les identifiants propriétaires de personnes, tels que les adresses e-mail, les numéros de téléphone hachés ou les ID de CRM, sont directement liés à un profil individuel."

>[!CONTEXTUALHELP]
>id="rtcdp_collaboration_organization_onboarding_deviceIDs"
>title="Identifiants d’appareils propriétaires"
>abstract="Les identifiants propriétaires d’appareil, tels que les adresses IP ou les ECID, sont directement liés aux appareils, lesquels peuvent être partagés entre plusieurs personnes. IPv4 est le seul identifiant d’appareil propriétaire actuellement pris en charge."

>[!CONTEXTUALHELP]
>id="rtcdp_collaboration_organization_onboarding_partnerIDs"
>title="ID de partenaire pris en charge"
>abstract="Les identifiants de partenaire sont des identifiants fournis par des partenaires externes pour la réconciliation des audiences. Les identifiants de partenaire ne sont pas directement liés à un profil individuel."

![Clés de correspondance prises en charge.](/help/assets/setup/manage-account/match-keys.png){zoomable="yes"}

>[!IMPORTANT]
>
>Les clés de correspondance que vous sélectionnez lors de la configuration du compte déterminent les clés de correspondance disponibles dans vos connexions. Bien que vous puissiez [supprimer les clés de correspondance indésirables](../connect/establishing-connections.md#connection-settings) lors de la configuration de la connexion, les clés de correspondance ne peuvent pas être ajoutées une fois la connexion établie. Il est important de sélectionner **toutes** les clés de correspondance que vous prévoyez d’utiliser dans les prochaines campagnes lors de la configuration du compte.

Les clés de correspondance aident les collaborateurs à travailler ensemble en permettant une synchronisation des données précise et axée sur la confidentialité, ce qui permet un ciblage et une mesure d’audience plus précis. Les clés de correspondance sélectionnées lors de la configuration du compte détermineront quelles clés de correspondance sont disponibles dans les connexions futures. Ils sont également utilisés pour [mapper des champs](./onboard-audiences.md#map-fields) de votre connexion de données aux champs cibles dans Collaboration lors de l’approvisionnement des audiences.

Sélectionnez les clés de correspondance à utiliser lors de la réconciliation des profils d’audience. Planifiez l’avenir et incluez toutes les clés de correspondance que vous pouvez utiliser et anticiper en les utilisant dans les prochaines campagnes. Si vous devez sélectionner d’autres clés de correspondance pour votre compte ultérieurement, vous pouvez le faire dans le workflow [Modifier le compte](#edit-account). Toutefois, les clés de correspondance ajoutées après la configuration initiale ne seront pas disponibles pour une utilisation dans les connexions existantes.

#### Clés correspondantes prises en charge {#supported-match-keys}

Collaboration prend en charge trois types de clés de correspondance : les identifiants de personnes propriétaires, les identifiants d’appareils propriétaires et les identifiants de partenaires. Toutes les clés de correspondance doivent répondre aux exigences suivantes :

* Les clés de correspondance doivent être **rognées**, **en minuscules**
* Les clés de correspondance hachées doivent être **SHA256-hachées**.
* Si vous fournissez des valeurs hachées qui utilisent des caractères majuscules, Collaboration les convertit automatiquement en minuscules.
* Si votre source contient des **identifiants en texte brut**, utilisez l’option **[!UICONTROL Appliquer la transformation]** lors de la [configuration de la connexion aux données](./manage-data-connection.md#match-keys) pour appliquer le hachage. Cette option est disponible uniquement lors de l’approvisionnement d’audiences à partir d’Experience Platform et n’est pas prise en charge pour les sources cloud.

##### Identifiants propriétaires de personnes

Les identifiants de personnes propriétaires sont directement connectés à un profil individuel. Les identifiants actuellement pris en charge sont les suivants :

* **[!UICONTROL E-mail haché]**
* **[!UICONTROL Téléphone haché]**
* **[!UICONTROL Identifiants CRM]**
* **[!UICONTROL Identifiants de fidélité]**
<!-- * **[!UICONTROL Custom ID]**: Custom identifiers -->

##### Identifiants d’appareils propriétaires

Les identifiants d’appareils propriétaires sont des identifiants connectés à un appareil spécifique. Les identifiants actuellement pris en charge sont les suivants :

* **[!UICONTROL IPv4 haché]** : adresses IPv4 hachées

##### ID partenaires

Les identifiants de partenaire sont des identifiants fournis par des partenaires externes pour la réconciliation des audiences. Les identifiants actuellement pris en charge sont les suivants :

* **[!UICONTROL Adfixus ID]**

>[!NOTE]
>
>L’intégration d’Adobe à [!DNL Adfixus] mappe les [!UICONTROL identifiants Adfixus] uniques pour chaque compte à un format codé Adobe commun. Ces mappages sont utilisés pour identifier les chevauchements entre les collaborateurs. Lors de l’activation d’audiences à l’aide de **[!UICONTROL Adfixus ID]**, les identifiants d’origine sont utilisés. Le format codé Adobe ne quitte jamais Collaboration.

Lors de la sélection de **[!UICONTROL Adfixus ID]**, vous devez fournir l’identifiant correspondant de votre partenaire externe dans la section **[!UICONTROL Informations d’identification du compte]**. Cette option n’est disponible qu’*après* le basculement sur **[!UICONTROL Adfixus ID]**. Saisissez votre Adfixus ID dans le champ **[!UICONTROL ID de compte]**, en veillant à vérifier la précision de la valeur.

![La boîte de dialogue Correspondance des clés avec l’Adfixus ID activée et la section Informations d’identification du compte mise en surbrillance.](/help/assets/setup/manage-account/adfixus-settings.png){zoomable="yes"}

Après avoir sélectionné toutes les clés de correspondance souhaitées, sélectionnez **[!UICONTROL Terminer]** pour terminer le workflow de configuration du compte.

![L’espace de travail Configurer le compte avec la section Clés de correspondance affichée.](/help/assets/setup/manage-account/add-account-match-keys.png){zoomable="yes"}

## Modifier le compte {#edit-account}

Après avoir configuré votre compte , vous pouvez modifier les détails et faire correspondre les clés à tout moment.

### Modifier les détails {#edit-details}

Vous pouvez modifier la plupart des détails de votre compte à tout moment, à l’exception du **[!UICONTROL Rôle]**. La région est automatiquement définie en fonction de votre compte Adobe Experience Cloud et ne peut pas être modifiée.

Pour modifier votre compte, sélectionnez **[!UICONTROL Modifier]** dans la section **[!UICONTROL Mon compte]** de l’espace de travail **[!UICONTROL Configuration]**.

![Espace de travail de configuration avec l’onglet Mon compte et l’option Modifier en surbrillance.](/help/assets/setup/manage-account/edit-account.png){zoomable="yes"}

Vous pouvez maintenant modifier les détails de votre compte. Mettez à jour les champs à modifier, puis sélectionnez **[!UICONTROL Enregistrer]** pour confirmer les modifications.

![Boîte de dialogue Modifier les détails du compte.](/help/assets/setup/manage-account/editable-options.png){zoomable="yes"}

### Modifier les clés correspondantes {#edit-match-keys}

>[!IMPORTANT]
>
>La modification des clés de correspondance n’affecte pas vos connexions existantes. Une fois la connexion établie, les clés de correspondance que vous sélectionnez lors de la configuration de la connexion sont corrigées. Il est important de sélectionner **toutes** les clés de correspondance que vous prévoyez d’utiliser dans les prochaines campagnes lors de la configuration du compte.

Vous pouvez également mettre à jour les clés de correspondance que vous avez initialement sélectionnées lors de la création de votre compte. Ces clés de correspondance déterminent les clés de correspondance disponibles pour les connexions futures.

Sélectionnez **[!UICONTROL Modifier]** dans la section **[!UICONTROL Clés de correspondance]**.

![Espace de travail de configuration avec l’option Modifier mise en surbrillance dans la section Clés de correspondance du compte.](/help/assets/setup/manage-account/edit-match-keys.png){zoomable="yes"}

La boîte de dialogue **[!UICONTROL Correspondance des clés]** s’affiche. Activez et désactivez toutes les clés de correspondance ou mettez à jour votre **[!UICONTROL ID de compte]** pour vos [!UICONTROL ID d’adfixus], puis sélectionnez **[!UICONTROL Enregistrer]** pour confirmer les modifications.

>[!IMPORTANT]
>
>La modification de votre [!UICONTROL Adfixus ID] ne déclenche pas d’actualisation de l’[esquisse de données](../glossary.md#sketches) pour vos connexions de données existantes à l’aide de la clé de correspondance. Une fois vos données esquissées, les modifications apportées à votre [!UICONTROL Adfixus ID] ne seront pas répercutées jusqu’à la prochaine actualisation de l’audience suivant les paramètres de votre [planning de connexion aux données](./manage-data-connection.md#scheduling). Si vous avez besoin de modifications avant votre prochaine actualisation, vous pouvez supprimer et recréer votre connexion de données.

![Boîte de dialogue Correspondance des clés avec l’option Enregistrer mise en surbrillance.](/help/assets/setup/manage-account/match-key-dialog.png){zoomable="yes"}

## Étapes suivantes

Une fois vos comptes configurés, vous êtes prêt à [audiences source](/help/guide/setup/onboard-audiences.md) dans Real-Time CDP Collaboration.
