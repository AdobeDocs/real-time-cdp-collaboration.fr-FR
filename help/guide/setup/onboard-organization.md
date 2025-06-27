---
title: Intégration et gestion de l’organisation
description: Découvrez comment intégrer et gérer divers aspects de votre organisation dans Real-Time CDP Collaboration
audience: admin, publisher, advertiser
badgelimitedavailability: label="Disponibilité limitée" type="Informative" url="https://helpx.adobe.com/legal/product-descriptions/real-time-customer-data-platform-collaboration.html newtab=true"
exl-id: a95e932a-9681-48f2-bf34-6fe5a50597d7
source-git-commit: 860138b95abc4d6af94bbbf722cf498463570c1b
workflow-type: tm+mt
source-wordcount: '886'
ht-degree: 19%

---

# Intégrer et gérer votre organisation

{{limited-availability-release-note}}

Découvrez comment intégrer votre organisation dans Real-Time CDP Collaboration et gérer divers aspects de votre entreprise. Cette page décrit les étapes d’intégration d’une organisation à Adobe Real-Time CDP Collaboration, y compris la définition de vos clés de correspondance, de vos identités préférées et d’autres options.

![Espace de travail de configuration de l’entreprise présentant ses paramètres actuels.](/help/assets/setup/manage-organization/my-organization.png){zoomable="yes"}

## Configuration initiale de l’organisation

Vous devez d’abord configurer les détails de votre organisation et de votre organisation. S’il s’agit de votre première organisation, vous serez immédiatement dirigé tout au long du processus d’intégration, en commençant par la configuration de vos [détails de compte](#set-up-details).

Pour ajouter d’autres organisations, accédez à **[!UICONTROL Configuration]** dans le rail de gauche et sélectionnez l’icône d’ajout (![icône d’ajout).](/help/assets/icons/plus.png)) dans le coin supérieur droit. Sélectionnez ensuite **[!UICONTROL Compte]**.

![L’espace de travail de configuration avec l’option Compte mise en surbrillance.](/help/assets/setup/manage-organization/add-new-account.png){zoomable="yes"}

### Configurer des détails {#set-up-details}

>[!CONTEXTUALHELP]
>id="rtcdp_collaboration_setup_contact_email"
>title="E-mail de contact"
>abstract="Fournissez une adresse e-mail basée sur une équipe ou un rôle, comme `collaboration@yourcompany.com`. Des adresses e-mail personnelles ou individuelles ne doivent pas être utilisées."

>[!CONTEXTUALHELP]
>id="rtcdp_collaboration_setup_connect_code"
>title="Code de connexion"
>abstract="Le code de connexion est un identifiant unique de votre organisation. Il est utilisé pour établir des connexions avec d’autres organisations dans Real-Time CDP Collaboration."

<!-- Move the above to new section for invite on this page when its created -->

Pour commencer l’intégration de votre organisation, vous devez d’abord configurer les détails de l’organisation. Pour ce faire, vous devez ajouter les informations suivantes :

* Ajoutez un **[!UICONTROL nom de l’organisation]** pour votre société.
* Ajoutez une **[!UICONTROL Description]** à propos de votre entreprise.
* Sélectionnez votre **[!UICONTROL rôle d’entreprise]**. Vous pouvez choisir entre **[!UICONTROL Annonceur]** et **[!UICONTROL Éditeur]**. Lisez le [document sur les workflows de bout en bout](/help/guide/end-to-end-workflow.md) pour voir les similitudes et les légères différences de workflow entre les deux types de rôles organisationnels.
* Sélectionnez le **[!UICONTROL secteur]** de votre organisation. Par exemple, **[!UICONTROL Vente au détail]**, **[!UICONTROL Télécommunications]** ou **[!UICONTROL Services financiers]**.
* Sélectionnez la **[!UICONTROL Région]** de votre organisation. Dans la version actuelle du produit, **[!UICONTROL Amérique du Nord]** est la sélection par défaut prédéfinie.
* Ajoutez un **[!UICONTROL e-mail de contact]** pour votre organisation. Il doit s’agir d’une adresse e-mail d’équipe ou basée sur les rôles. Les adresses e-mail personnelles ne doivent pas être fournies.
* Chargez un **[!UICONTROL Logo]** pour votre entreprise. Actuellement, les images de type SVG sont prises en charge.
* Sélectionnez une image pour l’image d’en-tête de votre société.

>[!NOTE]
>
>Bien que vous puissiez modifier la plupart de ces détails à tout moment, les **[!UICONTROL Rôle]** et **[!UICONTROL Région]** ne sont pas modifiables après la configuration initiale.

![Configurer l’espace de travail d’organisation avec la section Détails affichée.](/help/assets/setup/manage-organization/add-organization-details.png){zoomable="yes"}

Lorsque vous avez terminé, utilisez **[!UICONTROL Suivant]** pour passer à la page suivante et sélectionner les clés de correspondance que votre organisation utilisera.

### Configurer des clés correspondantes {#set-up-match-keys}

>[!CONTEXTUALHELP]
>id="rtcdp_collaboration_organization_onboarding_matchkeys"
>title="Clés correspondantes"
>abstract="Les clés correspondantes sont des identifiants utilisés pour réconcilier des membres d’audiences provenant de différentes sources de données. Incluez toutes les clés correspondantes que votre entreprise peut utiliser."

>[!CONTEXTUALHELP]
>id="rtcdp_collaboration_organization_onboarding_peopleIDs"
>title="Identifiants propriétaires de personnes"
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
>Les clés de correspondance que vous sélectionnez lors de la configuration de l’organisation déterminent les clés de correspondance disponibles pour les connexions que vous créez avec d’autres organisations. Bien que vous puissiez supprimer des clés de correspondance lors de la configuration de la connexion, vous ne pouvez pas ajouter de nouvelles clés de correspondance ultérieurement. Il est important de sélectionner toutes les clés de correspondance que vous prévoyez d’utiliser dans les prochaines campagnes lors de la configuration de l’organisation.

Les clés de correspondance, telles que les adresses e-mail, les identifiants d’appareil ou de client, aident les annonceurs et les éditeurs à travailler ensemble en permettant une synchronisation des données précise et axée sur la confidentialité, ce qui permet un ciblage et une mesure d’audience plus précis.

![Diapositive présentant les identifiants disponibles pour la première version de Real-Time CDP Collaboration.](/help/assets/setup/manage-organization/available-identifiers.png)

Sélectionnez les clés de correspondance à utiliser pour réconcilier les membres des audiences de l’éditeur et de l’annonceur. Incluez toutes les clés de correspondance que votre entreprise peut utiliser. Planifiez pour l’avenir et sélectionnez les clés de correspondance que vous prévoyez d’utiliser dans les futures campagnes éditeur-annonceur. Si vous devez sélectionner des clés de correspondance supplémentaires pour votre organisation, vous pouvez également le faire ultérieurement, dans le workflow [modifier l’organisation](#edit-organization).

![Configuration de l’espace de travail d’organisation avec la section Clés de correspondance affichée.](/help/assets/setup/manage-organization/add-organization-match-keys.png){zoomable="yes"}

Sélectionnez jusqu’à cinq clés de correspondance que vous prévoyez d’utiliser. Ultérieurement, lors de la configuration des connexions, vous pouvez supprimer les clés de correspondance indésirables, mais vous ne pouvez pas en ajouter de nouvelles.

Les clés de correspondance disponibles dans Real-Time CDP Collaboration peuvent être de trois types :

* Identifiants propriétaires de personnes
* Identifiants d’appareils propriétaires
* ID partenaires

Les clés de correspondance disponibles pour la première version de Real-Time CDP Collaboration sont les suivantes :

* E-mail haché

Une fois prêt, sélectionnez **[!UICONTROL Terminé]** pour terminer le workflow de configuration de l’organisation.

## Modifier l’organisation {#edit-organization}

Après avoir configuré votre organisation, vous pouvez à tout moment modifier certains aspects et détails de l’organisation. Pour modifier votre organisation, sélectionnez **[!UICONTROL Modifier]** dans la section **[!UICONTROL Mon organisation]** de l’espace de travail **[!UICONTROL Configuration]**.

![Espace de travail de configuration avec l’onglet Mon organisation et l’option Modifier mises en surbrillance.](/help/assets/setup/manage-organization/edit-organization.png){zoomable="yes"}

Vous pouvez désormais modifier les détails de votre organisation, à l’exception des **[!UICONTROL Rôle]** et **[!UICONTROL Région]**.

![Boîte de dialogue Modifier les détails de l’organisation.](/help/assets/setup/manage-organization/editable-options.png){zoomable="yes"}

Vous pouvez également mettre à jour les clés de correspondance que vous avez initialement sélectionnées lors de l’intégration de votre organisation. Sélectionnez **[!UICONTROL Modifier]** dans la section **[!UICONTROL Clés de correspondance]** pour ajouter d’autres clés de correspondance souhaitées.

![Espace de travail de configuration avec l’option Modifier mise en surbrillance dans la section Clés de correspondance de l’entreprise.](/help/assets/setup/manage-organization/edit-match-keys.png){zoomable="yes"}

## Étapes suivantes

Une fois votre organisation configurée, vous êtes prêt à [importer des audiences](/help/guide/setup/onboard-audiences.md) dans Real-Time CDP Collaboration.
