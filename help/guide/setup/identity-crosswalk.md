---
title: Croisements d’identités
description: Découvrez les passerelles d’identité dans Real-Time CDP Collaboration, notamment comment les importer de différentes sources et comment les gérer.
audience: admin, publisher, advertiser
badgelimitedavailability: label="Disponibilité limitée" type="Informative" url="https://helpx.adobe.com/legal/product-descriptions/real-time-customer-data-platform-collaboration.html newtab=true"
hidefromtoc: true
hide: true
exl-id: a51f112d-3da7-4482-a24a-6d9f269d28d1
source-git-commit: 23dc33af83366806f7d99161b4b713a33daeec76
workflow-type: tm+mt
source-wordcount: '514'
ht-degree: 22%

---

# Croisements d’identités

{{limited-availability-release-note}}

Découvrez les passages piétons d’identité dans Real-Time CDP Collaboration, notamment comment les importer de différentes sources et comment les gérer.

Les passerelles d’identité facilitent la liaison sécurisée et conforme à la confidentialité des identités des clients sur plusieurs jeux de données et plateformes. En utilisant des identifiants hachés, Real-Time CDP Collaboration garantit que les utilisateurs peuvent synchroniser et réconcilier des identités sans exposer des informations d’identification personnelle (PII). Cela permet d’obtenir une vue unifiée du client pour une meilleure collaboration et des efforts de marketing ciblés.

<!--
In Real-Time CDP Collaboration, use identity crosswalks alongside your audiences by [TODO] insert material here. 
-->


Dans un premier temps, vous devez importer les passages pour piétons d’identité dans Real-Time CDP Collaboration. Pour importer des passerelles d’identité dans Real-Time CDP Collaboration, lisez la section ci-dessous :

>[!NOTE]
>
>Dans la version Beta de Real-Time CDP Collaboration, vous pouvez importer des passages à niveau d’identité à partir de vos jeux de données dans Real-Time CDP. D’autres options seront disponibles dans les versions ultérieures.

## Importer les passages croisés d’identités dans Real-Time CDP Collaboration {#import-crosswalk}

Accédez à l’onglet **[!UICONTROL Configuration]** > **[!UICONTROL Passages croisés d’identité]**, sélectionnez le symbole Plus **+**, puis sélectionnez **[!UICONTROL Passage croisé d’identité]**

![Enregistrement de la manière d’accéder à l’écran pour ajouter des passerelles d’identité](/help/assets/setup/identity-crosswalks/import-identity-crosswalk.gif)

### Sélectionner la source des croisements

Sélectionnez une source à partir de laquelle vous allez importer le tableau de concordance d&#39;identité. Dans la première version de Real-Time CDP Collaboration, Experience Platform est la seule source prise en charge pour l’importation de passages pour piétons.

>[!TIP]
>
>Les passages piétons que vous importez depuis Experience Platform sont appelés *jeux de données* dans Platform.

Après avoir sélectionné Experience Platform comme source de vos passages pour croisés, sélectionnez le [sandbox Experience Platform](https://experienceleague.adobe.com/en/docs/experience-platform/sandbox/home) à partir duquel vous importez le passage pour croisé d’identité.

![Enregistrement de la façon de sélectionner une source de passage piétons](/help/assets/setup/identity-crosswalks/select-crosswalk-source.gif)

### Sélectionner le croisement

Après avoir sélectionné Experience Platform comme source de vos passages pour piétons,

### Fournir des détails

Attribuez un nom et une description au passage d&#39;identité que vous importez dans le produit.

### Sélectionner une clé de jointure {#select-join-key}

>[!CONTEXTUALHELP]
>id="rtcdp_collaboration_import_crosswalk_join_key"
>title="Clé de jointure"
>abstract="Une clé de jointure est un identifiant unique utilisé pour faire correspondre et relier des enregistrements de différents jeux de données. Cela permet de s’assurer que les données provenant de diverses sources puissent être associées avec précision à la même personne ou entité. L’un des en-têtes de colonne du croisement sélectionné peut servir de clé de jointure."

Une clé de jointure est un identifiant unique utilisé pour faire correspondre et relier des enregistrements de différents jeux de données. Cela permet de s’assurer que les données provenant de diverses sources puissent être associées avec précision à la même personne ou entité. En sélectionnant la clé de jointure appropriée, vous pouvez fusionner et réconcilier efficacement les données, ce qui améliore la précision et l’exhaustivité de vos campagnes.

L’un des en-têtes de colonne du croisement sélectionné peut servir de clé de jointure.

Sélectionnez la clé de jointure souhaitée pour la table de passage pour piétons et sélectionnez **[!UICONTROL Suivant]** pour passer à l&#39;étape suivante.

### Réviser

Passez en revue toutes les sélections effectuées dans les écrans précédents. Lorsque vous êtes satisfait(e) de votre sélection, sélectionnez **[!UICONTROL Suivant]** pour terminer le workflow.

## Étapes suivantes

Après avoir appris à importer des passerelles d’identité dans Real-Time CDP, vous pouvez afficher toutes les passerelles d’identité que vous avez ajoutées jusqu’à présent à Real-Time CDP Collaboration. Vous pouvez également utiliser les passages pour piétons d’identité que vous avez importés lors de l’importation d’audiences dans Real-Time CDP Collaboration.
