---
title: Croisements d’identités
description: Découvrez tous les passages pour piétons d’identité dans Real-Time CDP Collaboration, y compris comment intégrer des passages pour piétons d’identité provenant de différentes sources et comment gérer les passages pour croisés d’identité
audience: admin, publisher, advertiser
badgelimitedavailability: label="Disponibilité limitée" type="Informative" url="https://helpx.adobe.com/legal/product-descriptions/real-time-customer-data-platform-collaboration.html newtab=true"
hidefromtoc: true
hide: true
exl-id: a51f112d-3da7-4482-a24a-6d9f269d28d1
source-git-commit: 23dc33af83366806f7d99161b4b713a33daeec76
workflow-type: tm+mt
source-wordcount: '515'
ht-degree: 4%

---

# Croisements d’identités

{{limited-availability-release-note}}

Découvrez tous les passages pour piétons d’identité dans Real-Time CDP Collaboration, notamment comment intégrer des passages pour piétons d’identité provenant de différentes sources et comment gérer les passages pour piétons d’identité.

Les passages en concordance des identités facilitent la liaison sécurisée et conforme à la confidentialité des identités des clients à travers plusieurs ensembles de données et plates-formes. En utilisant des identifiants hachés, Real-Time CDP Collaboration garantit que les utilisateurs peuvent synchroniser et rapprocher les identités sans exposer d’informations personnelles identifiables (PII). Cela permet une vue unifiée du client pour une meilleure collaboration et des efforts de marketing ciblés.

<!--
In Real-Time CDP Collaboration, use identity crosswalks alongside your audiences by [TODO] insert material here. 
-->


Dans un premier temps, vous devez importer des passages croisés d’identité dans Real-Time CDP Collaboration. Pour importer des passages croisés d’identité dans Real-Time CDP Collaboration, lisez la section ci-dessous :

>[!NOTE]
>
>Dans la version bêta de Real-Time CDP Collaboration, vous pouvez importer des passerelles d’identité à partir de vos jeux de données dans Real-Time CDP. D’autres options seront disponibles dans les versions ultérieures.

## Importer les passages croisés d’identités dans Real-Time CDP Collaboration {#import-crosswalk}

Accédez à l’onglet **[!UICONTROL Configuration]** > **[!UICONTROL Passages croisés d’identité]**, sélectionnez le symbole Plus **+**, puis sélectionnez **[!UICONTROL Passage croisé d’identité]**

![Enregistrement de la manière d’accéder à l’écran pour ajouter des passerelles d’identité](/help/assets/setup/identity-crosswalks/import-identity-crosswalk.gif)

### Sélectionner la source des croisements

Sélectionnez une source à partir de laquelle vous allez importer le tableau de concordance d’identité. Dans la première version de Real-Time CDP Collaboration, Experience Platform est la seule source prise en charge pour l’importation de passages pour piétons.

>[!TIP]
>
>Les passages pour piétons que vous importez depuis Experience Platform sont appelés *jeux de* données dans Platform.

Après avoir sélectionné Experience Platform comme source de vos passages pour piétons, sélectionnez le [bac](https://experienceleague.adobe.com/en/docs/experience-platform/sandbox/home) à sable Experience Platform à partir duquel vous importez le passage pour piétons d’identité.

![Enregistrement de la façon de sélectionner une source de passage pour piétons](/help/assets/setup/identity-crosswalks/select-crosswalk-source.gif)

### Sélectionner le croisement

Après avoir sélectionné Experience Platform comme source de vos passages pour piétons,

### Fournir des détails

Attribuez un nom et une description au passage d&#39;identité que vous importez dans le produit.

### Sélectionner une clé de jointure {#select-join-key}

>[!CONTEXTUALHELP]
>id="rtcdp_collaboration_import_crosswalk_join_key"
>title="Clé de jointure"
>abstract="Une clé de jointure est un identificateur unique utilisé pour faire correspondre et lier des enregistrements entre différents ensembles de données. Il garantit que les données provenant de diverses sources peuvent être associées avec précision à la même personne ou entité. N’importe lequel des en-têtes de colonne du passage pour piétons sélectionné peut servir de clé de jointure."

Une clé de jointure est un identificateur unique utilisé pour faire correspondre et lier des enregistrements entre différents ensembles de données. Il garantit que les données provenant de diverses sources peuvent être associées avec précision à la même personne ou entité. En sélectionnant la clé de jonction appropriée, vous pouvez fusionner et rapprocher efficacement les données, améliorant ainsi la précision et l’exhaustivité de vos campagnes.

N’importe lequel des en-têtes de colonne du passage pour piétons sélectionné peut servir de clé de jointure.

Sélectionnez la clé de jonction souhaitée pour la table de passage pour piétons et sélectionnez **[!UICONTROL Suivant]** pour passer à l’étape suivante.

### Réviser

Passez en revue toutes les sélections effectuées dans les écrans précédents. Lorsque vous êtes satisfait(e) de votre sélection, sélectionnez **[!UICONTROL Suivant]** pour terminer le workflow.

## Étapes suivantes

Après avoir appris à importer des passerelles d’identité dans Real-Time CDP, vous pouvez afficher toutes les passerelles d’identité que vous avez ajoutées jusqu’à présent à Real-Time CDP Collaboration. Vous pouvez également utiliser les passages croisés d’identité que vous avez importés lors de l’importation d’audiences dans Real-Time CDP Collaboration.
