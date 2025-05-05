---
title: Intégration et gestion de l’organisation
description: Découvrez comment intégrer et gérer divers aspects de votre organisation dans Real-Time CDP Collaboration
audience: admin, publisher, advertiser
badgelimitedavailability: label="Disponibilité limitée" type="Informative" url="https://helpx.adobe.com/legal/product-descriptions/real-time-customer-data-platform-collaboration.html newtab=true"
exl-id: a95e932a-9681-48f2-bf34-6fe5a50597d7
source-git-commit: 0de6ab9af8152975f8e0b0f75b1ee0116ed73584
workflow-type: tm+mt
source-wordcount: '853'
ht-degree: 14%

---

# Intégration et gestion de l’organisation

{{limited-availability-release-note}}

Découvrez comment intégrer votre organisation dans Real-Time CDP Collaboration et gérer divers aspects de votre entreprise. Cette page décrit les étapes d’intégration d’une organisation à Adobe Real-Time CDP Collaboration, y compris la définition de vos clés de correspondance, de vos identités préférées et d’autres options.

![Page de configuration](/help/assets/setup/manage-organization/my-organization.png){zoomable="yes"}

## Configuration initiale de l’organisation

Vous devez d’abord configurer les détails de votre organisation et de votre organisation. Accédez à **[!UICONTROL Configuration]** dans le rail de gauche, sélectionnez le symbole **+** dans le coin supérieur droit, puis sélectionnez **[!UICONTROL Compte]**.

>[!TIP]
>
>Après avoir configuré un compte initial, vous pouvez utiliser le même workflow pour configurer des comptes supplémentaires au sein de la même organisation.

![Sélectionnez Compte pour ajouter une nouvelle organisation à Real-Time CDP Collaboration](/help/assets/setup/manage-organization/add-new-account.png){zoomable="yes"}

Le workflow de configuration de votre organisation comprend les deux pages ci-dessous :

* [Configurer les détails](#set-up-details)
* [Configurer les clés de correspondance](#set-up-match-keys)

>[!IMPORTANT]
>
>Toutes les *clés de correspondance* que vous sélectionnez au niveau de l’organisation se propagent ensuite au niveau du [projet](/help/guide/collaborate/manage-projects.md) dans la collaboration entre les annonceurs et les éditeurs. Au niveau du projet, vous pouvez ensuite supprimer toutes les clés de correspondance, mais vous ne pouvez *pas* ajouter d’autres clés qui n’ont pas été sélectionnées au niveau de l’organisation dans cet écran.

### Configurer les détails {#set-up-details}

>[!CONTEXTUALHELP]
>id="rtcdp_collaboration_setup_contact_email"
>title="E-mail de contact"
>abstract="Indiquez un e-mail basé sur une équipe ou un rôle, tel que `collaboration@yourcompany.com`. Les adresses électroniques personnelles ou individuelles ne doivent pas être utilisées."

![Étapes de détails et de cas d’utilisation pour configurer une organisation](/help/assets/setup/manage-organization/add-organization-details.png){zoomable="yes"}

1. Ajoutez un **[!UICONTROL nom de l’organisation]** pour votre société.
2. Ajoutez une **[!UICONTROL Description]** à propos de votre entreprise.
3. Sélectionnez votre **[!UICONTROL rôle d’entreprise]**. Vous pouvez choisir entre **[!UICONTROL Annonceur]** et **[!UICONTROL Éditeur]**. Lisez le [document sur les workflows de bout en bout](/help/guide/end-to-end-workflow.md) pour voir les similitudes et les légères différences de workflow entre les deux types de rôles organisationnels.
4. Sélectionnez le **[!UICONTROL secteur]** de votre organisation. Par exemple, **[!UICONTROL Vente au détail]**, **[!UICONTROL Télécommunications]** ou **[!UICONTROL Services financiers]**.
5. Sélectionnez la **[!UICONTROL Région]** de votre organisation. Dans la version actuelle du produit, **[!UICONTROL Amérique du Nord]** est la sélection par défaut prédéfinie.
6. Ajoutez un **[!UICONTROL e-mail de contact]** pour votre organisation. Il doit s’agir d’une adresse e-mail d’équipe ou basée sur les rôles. Les adresses e-mail personnelles ne doivent pas être fournies.
7. <span class="preview"> Publisher-only </span> : lors de la configuration d&#39;une organisation d&#39;éditeur, vous devez lire et reconnaître que vous serez détectable par les annonceurs dans le catalogue de l&#39;éditeur.
   ![Message d’accord préalable spécifique à l’éditeur.](/help/assets/setup/manage-organization/publisher-specific-optin-message.png){zoomable="yes"}
8. Chargez un **[!UICONTROL Logo]** pour votre entreprise. Actuellement, les images de type SVG sont prises en charge.
9. Sélectionnez une image pour l’image d’en-tête de votre société.

Lorsque vous êtes satisfait(e) de votre sélection, utilisez **[!UICONTROL Suivant]** pour passer à la page suivante et sélectionner les clés de correspondance que votre entreprise doit utiliser.

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

Les clés de correspondance, telles que les adresses e-mail, les identifiants d’appareil ou de client, aident les annonceurs et les éditeurs à travailler ensemble en permettant une synchronisation des données précise et axée sur la confidentialité, ce qui permet un ciblage et une mesure d’audience plus précis.

![Diapositive présentant les identifiants disponibles pour la première version de Real-Time CDP Collaboration.](/help/assets/setup/manage-organization/available-identifiers.png)

Sélectionnez les clés de correspondance à utiliser pour réconcilier les membres des audiences de l’éditeur et de l’annonceur. Incluez toutes les clés de correspondance que votre entreprise peut utiliser. Planifiez pour l’avenir et sélectionnez les clés de correspondance que vous prévoyez d’utiliser dans les futures campagnes éditeur-annonceur. Si vous devez sélectionner des clés de correspondance supplémentaires pour votre organisation, vous pouvez également le faire ultérieurement, dans le workflow [modifier l’organisation](#edit-organization).

![Étape de sélection des clés de correspondance.](/help/assets/setup/manage-organization/add-organization-match-keys.png){zoomable="yes"}

Sélectionnez jusqu’à cinq clés de correspondance que vous prévoyez d’utiliser. Ultérieurement, lors de la configuration des connexions, vous pouvez supprimer les clés de correspondance indésirables, mais vous ne pouvez pas en ajouter de nouvelles.

Les clés de correspondance disponibles dans Real-Time CDP Collaboration peuvent être de trois types :

* Identifiants propriétaires de personnes
* Identifiants d’appareils propriétaires
* ID partenaires

Les clés de correspondance disponibles pour la première version de Real-Time CDP Collaboration sont les suivantes :

* E-mail haché

<!--

not available in the Limited GA release

* Hashed phone
* IPv4

-->

Une fois prêt, sélectionnez **[!UICONTROL Terminé]** pour terminer le workflow de configuration de l’organisation.

## Modifier l’organisation {#edit-organization}

Après avoir configuré votre organisation, vous pouvez à tout moment modifier certains aspects et détails de l’organisation. Pour modifier votre organisation, sélectionnez **[!UICONTROL Modifier]** dans la vue **[!UICONTROL Mon organisation]**.

![Modifier le contrôle d’organisation mis en surbrillance.](/help/assets/setup/manage-organization/edit-organization.png){zoomable="yes"}

À ce stade, vous pouvez mettre à jour le nom, la description, le logo et la photo de profil de l’organisation.

![Options modifiables pour les organisations.](/help/assets/setup/manage-organization/editable-options.png){zoomable="yes"}

Vous pouvez également mettre à jour les clés de correspondance que vous avez sélectionnées initialement lors de l’intégration de votre organisation, ainsi que le seuil minimal pour que les identités correspondant aux clés de correspondance soient visibles et utilisables dans les chevauchements d’audience et d’autres zones de produits. Sélectionnez **[!UICONTROL Modifier]** dans l’onglet **[!UICONTROL Clés de correspondance]** pour ajouter d’autres clés de correspondance souhaitées ou mettre à jour les seuils d’identité.

![Modifier les clés de correspondance](/help/assets/setup/manage-organization/edit-match-keys.png){zoomable="yes"}

## Étapes suivantes

Une fois votre organisation configurée, vous êtes prêt à [importer des audiences](/help/guide/setup/onboard-audiences.md) dans Real-Time CDP Collaboration.
