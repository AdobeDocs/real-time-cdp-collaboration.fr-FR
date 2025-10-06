---
title: Amazon Marketing Cloud
description: Découvrez comment collaborer avec Amazon Marketing Cloud dans Real-Time CDP Collaboration.
audience: publisher, advertiser
badgelimitedavailability: label="Disponibilité limitée" type="Informative" url="https://helpx.adobe.com/legal/product-descriptions/real-time-customer-data-platform-collaboration.html newtab=true"
source-git-commit: 57b847c25edbf88f4708bda74be41fe6141472a7
workflow-type: tm+mt
source-wordcount: '644'
ht-degree: 20%

---

# Amazon Marketing Cloud

{{limited-availability-release-note}}

Après avoir établi une connexion avec [!DNL Amazon Marketing Cloud] ([!DNL AMC]), les annonceurs peuvent [créer un projet](../manage-projects.md#create-project) collaborer avec [!DNL AMC] pour tirer parti de ses fonctionnalités d’analyse avancées. Après avoir créé un projet, vous pouvez utiliser la section **[!UICONTROL Découvrir]** pour comparer les informations sur les audiences et découvrir les audiences pertinentes pour vos campagnes.

>[!IMPORTANT]
>
>Les seuls cas d’utilisation pris en charge avec [!DNL AMC] sont **découverte d’audience** et **mesure**. Actuellement, seule la section **[!UICONTROL Discover]** est disponible dans votre projet avec [!DNL AMC].

## Découvrir {#discover}

>[!CONTEXTUALHELP]
>id="rtcdp_collaboration_amc_discover_compare_audiences"
>title="Comparer des audiences"
>abstract="Comparez votre audience à toute la clientèle atteinte par vos publicités Amazon Ads."

>[!CONTEXTUALHELP]
>id="rtcdp_collaboration_amc_discover_relevant_audiences"
>title="Audiences pertinentes"
>abstract="Segments de ciblage Amazon pour lesquels votre audience présente les chevauchements les plus importants, en ne prenant en compte que les impressions DSP (ces segments ne peuvent être ciblés que dans DSP)."

>[!CONTEXTUALHELP]
>id="rtcdp_collaboration_amc_discover_resolved_ids"
>title="ID résolus"
>abstract="Le nombre d’identifiants que la résolution d’identité d’Amazon a pu résoudre à l’aide des données de votre audience."

>[!CONTEXTUALHELP]
>id="rtcdp_collaboration_amc_discover_overlapping_ad_exposed_ids"
>title="Chevauchement des ID exposés aux publicités"
>abstract="Cela représente le nombre d’« identifiants résolus » de l’audience chargée qui ont également été exposés à une publicité via Amazon Ads."

>[!CONTEXTUALHELP]
>id="rtcdp_collaboration_amc_discover_overlap_percentage"
>title="% de chevauchement"
>abstract="Proportion d’« ID résolus » qui ont été exposés à une publicité via Amazon Ads."

>[!CONTEXTUALHELP]
>id="rtcdp_collaboration_amc_discover_amazon_breakdown"
>title="Répartition par produit publicitaire Amazon"
>abstract="Répartition des « ID exposés à des publicités avec chevauchement » atteints par le produit sponsorisé par Amazon Ads et/ou Amazon Ads DSP."

Dans la section **[!UICONTROL Découvrir]**, vous pouvez comparer votre audience AMC à tous les consommateurs atteints par vos publicités Amazon. Vous pouvez également afficher les segments de ciblage Amazon avec lesquels votre audience a les chevauchements les plus importants, en ne prenant en compte que les impressions DSP (ces segments ne peuvent être ciblés que dans DSP).

>[!IMPORTANT]
>
>Les données d’audience sont traitées à partir des audiences chargées dans votre compte [!DNL Amazon Ads]. Pour savoir comment envoyer et utiliser la fonctionnalité Destinations Experience Platform pour envoyer vos audiences à votre compte [!DNL Amazon Ads], lisez le guide [Connexion Amazon Ads](https://experienceleague.adobe.com/en/docs/experience-platform/destinations/catalog/advertising/amazon-ads) .

![Section Découverte d’un projet avec Amazon Marketing Cloud.](/help/assets/collaborate/advertising-platforms/amc-discover.png){zoomable="yes"}

### Comparer des audiences {#compare-audiences}

La section **[!UICONTROL Comparer les audiences]** fournit des informations sur la manière dont votre audience [!DNL AMC] chevauche les consommateurs atteints par vos publicités Amazon. Dans la section **[!UICONTROL Comparer les audiences]**, vous pouvez afficher les mesures suivantes :

| Mesure | Description |
|--------------------------------|---------------------------------------------------------------------------------------------------|
| [!UICONTROL ID résolus] | Le nombre d’identifiants [!DNL Amazon’s Identity Resolution] a pu être résolu à l’aide des données de votre audience. |
| [!UICONTROL Chevauchement des ID exposés à la publicité] | Le nombre d’identifiants [!UICONTROL Résolus] de l’audience chargée qui ont également été exposés à une publicité via [!DNL Amazon Ads]. |
| [!UICONTROL Chevaucher %] | La proportion d’[!UICONTROL ID résolus] qui ont été exposés à une publicité via [!DNL Amazon Ads]. |
| [!UICONTROL Répartition par produit publicitaire Amazon] | Répartition des [!UICONTROL ID exposés à des publicités avec chevauchement] atteints par [!UICONTROL Produit sponsorisé] et/ou [!UICONTROL DSP]. Chaque est représenté sous la forme d’un pourcentage individuel par rapport au nombre total d’identifiants exposés à la publicité. Comme un ID peut appartenir à la fois à [!UICONTROL Produits sponsorisés] et à [!UICONTROL DSP], la somme des pourcentages peut ne pas être égale à 100 %. |


### Audiences pertinentes {#relevant-audiences}

La section **[!UICONTROL Audiences pertinentes]** fournit des informations sur [!DNL Amazon] segments de ciblage, ou audiences, avec lesquels votre audience a les chevauchements les plus importants, en ne prenant en compte que les impressions DSP (ces segments ne peuvent être ciblés que dans DSP). Vous pouvez parcourir toutes les audiences pertinentes à l’aide du bouton (bascule). Dans chaque section, vous pouvez afficher les mesures suivantes :

| Mesure | Description |
|--------------------------------|---------------------------------------------------------------------------------------------------|
| [!UICONTROL ID résolus] | Le nombre d’identifiants [!DNL Amazon’s Identity Resolution] a pu être résolu à l’aide des données de votre audience. |
| [!UICONTROL Chevauchement des ID exposés à la publicité] | Cela représente le nombre d’identifiants [!UICONTROL Résolus] de l’audience chargée qui ont également été exposés à une publicité via [!DNL Amazon Ads]. Cela ne prend en compte que les impressions DSP. |
| [!UICONTROL Chevaucher %] | La proportion d’[!UICONTROL ID résolus] qui ont été exposés à une publicité via [!DNL Amazon Ads]. |
| [!UICONTROL Catégories] | La ou les catégories auxquelles l’audience appartient. Une audience peut appartenir à plusieurs catégories. |

### Découvrir les chevauchements avec les [!DNL Amazon Marketing Cloud] {#discover-overlaps}

La section **[!UICONTROL Discover chevauche Amazon Marketing Cloud]** fournit des informations sur la façon dont vos audiences se chevauchent avec [!DNL Amazon] segments de ciblage, ou audiences. Vous pouvez afficher les mesures suivantes :

| Mesure | Description |
|--------------------------------|---------------------------------------------------------------------------------------------------|
| [!UICONTROL ID résolus] | Le nombre d’identifiants [!DNL Amazon’s Identity Resolution] a pu être résolu à l’aide des données de votre audience. |
| [!UICONTROL Chevauchement des ID exposés à la publicité] | Cela représente le nombre d’identifiants [!UICONTROL Résolus] de l’audience chargée qui ont également été exposés à une publicité via [!DNL Amazon Ads]. Cela ne prend en compte que les impressions DSP. |
| [!UICONTROL Chevaucher %] | La proportion d’[!UICONTROL ID résolus] qui ont été exposés à une publicité via [!DNL Amazon Ads]. |