---
title: Configuration et gestion de votre compte
description: Découvrez comment configurer et gérer divers aspects de votre compte dans Real-Time CDP Collaboration
audience: admin, publisher, advertiser
badgelimitedavailability: label="Disponibilité limitée" type="Informative" url="https://helpx.adobe.com/legal/product-descriptions/real-time-customer-data-platform-collaboration.html newtab=true"
exl-id: a95e932a-9681-48f2-bf34-6fe5a50597d7
source-git-commit: a7215d453021be578a32ce1af4d659845c3b8493
workflow-type: tm+mt
source-wordcount: '936'
ht-degree: 18%

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
<!-- The above will need to be updated when I update things for B2B -->
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
>abstract="Les clés correspondantes sont des identifiants utilisés pour réconcilier des membres d’audiences provenant de différentes sources de données. Incluez toutes les clés correspondantes que votre marque peut utiliser."

>[!CONTEXTUALHELP]
>id="rtcdp_collaboration_organization_onboarding_peopleIDs"
>title="Idenfiants de personnes propriétaires"
>abstract="Les identifiants propriétaires de personnes, tels que des adresses e-mail ou des numéros de téléphone hachés, sont directement liés à un profil individuel. Les identifiants actuellement pris en charge sont des e-mails et des numéros de téléphone hachés."

>[!CONTEXTUALHELP]
>id="rtcdp_collaboration_organization_onboarding_deviceIDs"
>title="Identifiants d’appareils propriétaires"
>abstract="Les identifiants d’appareils propriétaires, tels que les adresses IP ou les ECID, sont directement connectés aux appareils, lesquels peuvent être partagés entre plusieurs personnes. IPv4 est le seul identifiant d’appareil propriétaire actuellement pris en charge."

>[!CONTEXTUALHELP]
>id="rtcdp_collaboration_organization_onboarding_partnerIDs"
>title="ID de partenaire pris en charge"
>abstract="Les identifiants de partenaire associés aux profils étendent la portée d’un profil spécifique."

>[!IMPORTANT]
>
>Les clés de correspondance que vous sélectionnez lors de la configuration du compte déterminent les clés de correspondance disponibles pour les connexions que vous créez avec d’autres collaborateurs. Bien que vous puissiez supprimer des clés de correspondance lors de la configuration de la connexion, vous ne pouvez pas ajouter de nouvelles clés de correspondance. Il est important de sélectionner **toutes** les clés de correspondance que vous prévoyez d’utiliser dans les prochaines campagnes lors de la configuration du compte.

Les clés de correspondance, telles que les adresses e-mail, les identifiants d’appareil ou de client, aident les collaborateurs à travailler ensemble en permettant une synchronisation des données précise et axée sur la confidentialité, ce qui permet un ciblage et une mesure d’audience plus précis.

![Diapositive présentant les identifiants disponibles pour la première version de Collaboration.](/help/assets/setup/manage-account/available-identifiers.png)

<!-- Eventually replace this image above to match branding better. -->

Sélectionnez les clés de correspondance à utiliser lors de la réconciliation des profils d’audience. Incluez toutes les clés de correspondance que vous pouvez utiliser. Planifiez l’avenir et sélectionnez les clés de correspondance que vous prévoyez d’utiliser dans les prochaines campagnes. Si vous devez sélectionner d’autres clés de correspondance pour votre compte ultérieurement, vous pouvez le faire dans le workflow [Modifier le compte](#edit-account).

Sélectionnez jusqu’à cinq clés de correspondance que vous prévoyez d’utiliser. Ultérieurement, lors de la configuration des connexions, vous pouvez supprimer les clés de correspondance indésirables, mais vous ne pouvez pas en ajouter de nouvelles.

Il existe trois types de clés de correspondance disponibles :

* Idenfiants de personnes propriétaires
* Identifiants d’appareils propriétaires
* ID partenaires

>[!IMPORTANT]
>
>Actuellement, la seule clé de correspondance prise en charge est l’e-mail haché.

Une fois prêt, sélectionnez **[!UICONTROL Terminé]** pour terminer le workflow de configuration de l’organisation.

![Configuration de l’espace de travail d’organisation avec la section Clés de correspondance affichée.](/help/assets/setup/manage-account/add-account-match-keys.png){zoomable="yes"}

## Modifier le compte {#edit-account}

Après avoir configuré votre compte, vous modifiez à tout moment certains aspects et détails du compte. Pour modifier votre compte, sélectionnez **[!UICONTROL Modifier]** dans la section **[!UICONTROL Mon compte]** de l’espace de travail **[!UICONTROL Configuration]**.

![Espace de travail de configuration avec l’onglet Mon compte et l’option Modifier en surbrillance.](/help/assets/setup/manage-account/edit-account.png){zoomable="yes"}

Vous pouvez désormais modifier les détails de votre compte, à l’exception du **[!UICONTROL Rôle]**. Notez que la région est automatiquement définie en fonction de votre compte Adobe Experience Cloud et ne peut pas être modifiée à tout moment.

![Boîte de dialogue Modifier les détails du compte.](/help/assets/setup/manage-account/editable-options.png){zoomable="yes"}

Vous pouvez également mettre à jour les clés de correspondance que vous avez initialement sélectionnées lors de l’intégration de votre organisation. Sélectionnez **[!UICONTROL Modifier]** dans la section **[!UICONTROL Clés de correspondance]** pour ajouter d’autres clés de correspondance souhaitées.

![Espace de travail de configuration avec l’option Modifier mise en surbrillance dans la section Clés de correspondance du compte.](/help/assets/setup/manage-account/edit-match-keys.png){zoomable="yes"}

## Étapes suivantes

Une fois vos comptes configurés, vous êtes prêt à [audiences source](/help/guide/setup/onboard-audiences.md) dans Real-Time CDP Collaboration.
