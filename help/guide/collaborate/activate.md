---
title: Activer les audiences
description: Découvrez comment activer des audiences dans Adobe Real-Time CDP Collaboration.
audience: admin, publisher
badgelimitedavailability: label="Disponibilité limitée" type="Informative" url="https://helpx.adobe.com/legal/product-descriptions/real-time-customer-data-platform-collaboration.html newtab=true"
exl-id: fd82fcbf-ab39-48e0-9438-0a9046693431
source-git-commit: f19aff1b7d10a446dd209721e7a6fdf537c9d63e
workflow-type: tm+mt
source-wordcount: '795'
ht-degree: 1%

---

# Activer les audiences

{{limited-availability-release-note}}

>[!IMPORTANT]
>
>L’espace de travail **[!UICONTROL Activer]** n’est disponible que si le cas d’utilisation **Activation de l’audience** a été activé [pendant le processus de connexion](../connect/establishing-connections.md#connection-settings). Pour plus d’informations sur les cas d’utilisation, consultez le guide [gestion des projets](./manage-projects.md#project-use-cases).

L’activation des audiences vous permet d’activer des audiences dans les campagnes. Le processus d&#39;activation est une collaboration entre les annonceurs et les éditeurs. Après avoir [découvert les meilleures audiences pour votre campagne](./discover.md), les audiences peuvent activer les audiences ciblées. Les audiences activées sont envoyées à la destination préconfigurée de l’éditeur, telle que Adobe Experience Platform, pour être utilisées dans les campagnes. Pour plus d’informations sur la configuration de la destination, reportez-vous au guide [présentation des destinations](../destinations/overview.md).

>[!IMPORTANT]
>
>Actuellement, lorsque les annonceurs activent des audiences, elles sont alors automatiquement activées vers la destination que l’éditeur a configurée pour leur organisation. L’éditeur **doit** configurer une destination *avant* l’annonceur active une audience. Si aucune destination n’est configurée, l’audience sera envoyée à l’éditeur, mais ne pourra être activée dans aucune campagne.

## Activer de nouvelles audiences

Pour commencer à activer les audiences, accédez à l’onglet **[!UICONTROL Activer]** dans l’espace de travail de votre projet.

Sélectionnez l’icône d’ajout (![ Icône Ajouter .](/help/assets/icons/plus.png)) ou l’option **[!UICONTROL Activer l’audience]** si aucune audience précédente n’a été envoyée pour activation.

![Activer l’espace de travail dans un projet sans audience ajoutée.](/help/assets/collaborate/activate/activate-new-audiences.png)

Le workflow d’activation des audiences s’ouvre et vous pouvez sélectionner l’audience à envoyer à votre collaborateur ou votre collaboratrice. Utilisez la liste déroulante pour sélectionner une audience ou recherchez une audience spécifique. Pour afficher plus d’informations sur les audiences avant d’effectuer votre sélection, sélectionnez **[!UICONTROL Parcourir les audiences]**

![Workflow d’activation de l’audience avec les options de liste déroulante et de Parcourir les audiences mises en surbrillance.](/help/assets/collaborate/activate/audience-activation.png)

Dans le **[!UICONTROL Parcourir les audiences]**, vous pouvez voir le **[!UICONTROL Nombre d’identités]**, le **[!UICONTROL Chevauchement des identités]** et le **[!UICONTROL Chevauchement %]** pour chaque audience.

![Boîte de dialogue Parcourir les audiences affichant les audiences disponibles.](/help/assets/collaborate/activate/browse-audiences.png)

Sélectionnez l’audience à activer dans les campagnes, puis sélectionnez **[!UICONTROL Enregistrer]**. L’audience est maintenant affichée et vous pouvez voir le **[!UICONTROL nombre d’identités]**, le **[!UICONTROL chevauchement d’identités]** et le **[!UICONTROL chevauchement %]** pour l’audience sélectionnée.

![Workflow d’activation de l’audience avec l’audience sélectionnée affichée.](/help/assets/collaborate/activate/audience-selected.png)

### Modifier les clés correspondantes

Vous pouvez ensuite modifier les clés de correspondance de l’audience en sélectionnant **[!UICONTROL Modifier les clés de correspondance]** dans l’audience sélectionnée. Ces options sont héritées de vos sélections de clés de correspondance lors de la configuration initiale de la connexion entre les collaborateurs. Vous pouvez supprimer les clés de correspondance sélectionnées si elles ne s’appliquent pas à une campagne spécifique, mais vous ne pouvez pas ajouter de nouvelles clés de correspondance.

![Workflow d’activation de l’audience avec l’option Modifier les clés de correspondance mise en surbrillance.](/help/assets/collaborate/activate/edit-match-keys.png)

La boîte de dialogue **[!UICONTROL Modifier les clés de correspondance]** s’ouvre et vous pouvez activer/désactiver les clés de correspondance que vous ne souhaitez pas utiliser. Sélectionnez **[!UICONTROL Enregistrer]** pour enregistrer vos modifications.

>[!NOTE]
>
>Au moins une clé de correspondance doit être sélectionnée. Dans la version actuelle, la seule clé de correspondance disponible est **[!UICONTROL e-mail haché]**. Vous ne pouvez donc pas supprimer cette clé de correspondance.

![Boîte de dialogue Modifier les clés de correspondance dans le workflow d’activation de l’audience.](/help/assets/collaborate/activate/edit-match-keys-selection.png)

### Définir la fréquence et l’intervalle d’actualisation de l’audience

Enfin, définissez la fréquence et la période souhaitées pour l’actualisation de l’audience. Dans la version actuelle, la seule option de fréquence prise en charge est **[!UICONTROL Une fois]**. La fréquence **[!UICONTROL Une fois]** signifie que les audiences sont activées une seule fois et ne sont pas actualisées. L’option **[!UICONTROL Date]** est automatiquement renseignée avec la date actuelle.

![Workflow d’activation de l’audience avec la section Fréquence mise en surbrillance.](/help/assets/collaborate/activate/audience-frequency.png)

Une fois vos sélections effectuées, sélectionnez **[!UICONTROL Activer]** pour terminer le workflow. L’audience est maintenant activée et vous pouvez la visualiser dans l’onglet **[!UICONTROL Activer]**. Elle sera également disponible pour votre collaborateur dans son onglet **[!UICONTROL Activer]**, où il peut l&#39;utiliser dans des campagnes.

Vous pouvez modifier l’icône de modification du nom de l’audience (![icône de crayon.](/help/assets/icons/edit.png)) ou désactivez l’audience en sélectionnant **[!UICONTROL Désactiver]**.

![L’onglet Activer avec l’audience activée affichée et les options Modifier et Désactiver mises en surbrillance.](/help/assets/collaborate/activate/edit-activate-audience.png)

## Afficher les audiences activées

Dans l’onglet **[!UICONTROL Activer]**, les éditeurs et les annonceurs peuvent afficher les audiences actuellement activées. Actuellement, les audiences sont automatiquement envoyées à la destination configurée de l’éditeur après leur activation par l’annonceur.

![Aperçu de l’onglet Activer, présentant une audience activée.](/help/assets/collaborate/activate/activate-overview.png)

Dans chaque audience activée, vous pouvez voir les mesures suivantes :

| Mesure | Description |
|---------|----------|
| **[!UICONTROL Identités activées]** | Indique le nombre d’identités activées dans l’audience. |
| **[!UICONTROL Identités qui se chevauchent]** | Indique le nombre d’identités qui se chevauchent entre cette audience et la population totale des profils dans l’inventaire du collaborateur. |
| **[!UICONTROL Répartition des clés de correspondance]** | Affiche le nombre d’identités pour chaque identité utilisée dans l’audience. Par exemple, un nombre total d’identités de 500 000 utilisateurs peut se composer de 400 000 utilisateurs ayant saisi l’identité d’e-mail hachée et de 100 000 utilisateurs ayant saisi une identité d’identifiant mobile. Notez que dans l’exemple décrit ici, la même personne peut être présente deux fois dans l’audience avec son adresse e-mail et son identifiant mobile. |

## Étapes suivantes {#next-steps}

Après avoir activé les données et exécuté des campagnes, travaillez avec l’équipe d’activation et d’ingénierie d’Adobe pour charger les données de mesure et afficher les [rapports de mesure](/help/guide/collaborate/measure.md) correspondants.
