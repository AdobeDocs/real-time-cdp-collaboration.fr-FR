---
title: Configuration des autorisations AWS pour l’approvisionnement auprès d’une audience
description: Découvrez comment configurer les autorisations de gestion des identités et des accès (IAM) d’AWS pour accorder à Adobe un accès sécurisé en lecture seule à votre compartiment pour l [!DNL Amazon S3] approvisionnement des audiences dans Real-Time CDP Collaboration.
source-git-commit: 73f11b7341cf94540dc01f8803291f6dc3cd5038
workflow-type: tm+mt
source-wordcount: '650'
ht-degree: 1%

---

# Configuration des autorisations AWS pour le sourcing d’audience

Utilisez ce guide pour configurer les politiques et rôles de gestion des identités et des accès (IAM) d’AWS qui accordent à Adobe un accès sécurisé en lecture seule à votre compartiment Amazon S3. Cet accès permet à Real-Time CDP Collaboration de s’approvisionner en audiences à partir de votre compartiment S3.

## Conditions préalables {#prerequisites}

Avant de poursuivre, vérifiez que vous répondez aux exigences suivantes et que vous avez accès aux informations requises.

### Autorisations AWS requises

Pour effectuer cette configuration, votre compte doit disposer d’un accès administrateur AWS. L’accès administrateur vous permet de créer et de gérer les politiques et les rôles IAM requis pour autoriser l’accès d’Adobe à votre compartiment S3. Si vous ne disposez pas des privilèges d’administrateur, contactez votre administrateur AWS avant de continuer.

### Informations requises

Au fur et à mesure que vous passez en revue les étapes ci-dessous, notez les informations suivantes. Ces détails sont utilisés dans le [[!DNL Amazon S3] guide de l’interface utilisateur de l’approvisionnement des audiences](./configure-aws-s3-audience-sourcing.md).

* Nom du compartiment S3 où sont stockés vos fichiers d’audience.
* Chemin d’accès au dossier (préfixe) sous lequel se trouvent vos fichiers d’audience.
* Le nom de ressource Amazon (ARN) pour votre rôle IAM nouvellement créé, par exemple : `arn:aws:s3:::my-company-data/audience-files/`

>[!TIP]
>
>Un nom de ressource Amazon (ARN) identifie de manière unique les ressources AWS, telles que les compartiments S3 et les rôles IAM. Utilisez le format suivant pour spécifier votre compartiment et le chemin d’accès au dossier facultatif :
>
>```
>arn:aws:s3:::<bucket-name>/<optional-folder-path>
>```

## Création d’une politique IAM {#create-policy}

Pour commencer la configuration, créez d’abord une politique IAM qui accorde **accès en lecture seule** à votre compartiment S3. Cette politique permet à Adobe de lire les fichiers nécessaires au sourcing d’audience, mais n’accorde pas d’autorisations d’écriture ou de suppression.

Ouvrez la [console de gestion AWS](https://aws.amazon.com/console/) puis accédez à **[!DNL IAM]** > **[!DNL Policies]** > **[!DNL Create policy]**.

Dans l’espace de travail Créer une politique d’AWS, sélectionnez l’onglet **JSON** et collez l’exemple de politique ci-après.

>[!NOTE]
>
>Remplacez `<Your AWS ARN for bucket folder path>` et `<Your AWS ARN for bucket>` par vos ARN S3 spécifiques. Lors de la spécification du chemin d’accès au dossier de compartiment, incluez `/*` à la fin du ARN (par exemple, `arn:aws:s3:::my-company-data/audience-files/*`). Adobe a ainsi accès à tous les fichiers et sous-dossiers dans le chemin d’accès au dossier spécifié.

```json
{
  "Version": "2012-10-17",
  "Statement": [
    {
      "Sid": "Statement1",
      "Effect": "Allow",
      "Action": [
        "s3:GetObject",
        "s3:ListBucket",
        "s3:GetBucketLocation"
      ],
      "Resource": "<Your AWS ARN for bucket folder path>"
    },
    {
      "Sid": "Statement2",
      "Effect": "Allow",
      "Action": [
        "s3:ListBucket"
      ],
      "Resource": "<Your AWS ARN for bucket>"
    }
  ]
}
```

Vérifiez les paramètres de la politique et sélectionnez **[!DNL Create policy]**. Enregistrez le nom de la politique à utiliser à une étape ultérieure.

>[!TIP]
>
>Pour localiser le nom du compartiment et le chemin d’accès au dossier, ouvrez la **console de gestion Amazon S3**. Sur la page **Compartiments**, sélectionnez le nom de votre compartiment pour l’ouvrir. La vue **Objets** répertorie vos fichiers et dossiers, et le chemin d’accès en haut de la page affiche votre chemin d’accès au dossier actif.

## Créer un rôle IAM {#create-role}

Créez ensuite un rôle IAM et définissez le rôle IAM Real-Time CDP Collaboration AWS en tant qu **entité approuvée**. Cela permet aux services d’Adobe d’assumer le rôle et de lire en toute sécurité les données de votre audience S3.

Dans l’onglet **[!DNL IAM]** de la console de gestion Amazon S3, accédez à **[!DNL Roles]** > **[!DNL Create role]**.

Sous [!DNL Step 1] du workflow [!DNL Create role], dans la section **[!DNL Trusted entity type]**, sélectionnez **[!DNL Custom trust policy]**. Ensuite, dans l’éditeur de **[!DNL Custom trust policy]**, collez l’exemple suivant et remplacez `<Adobe IAM Role ARN>` par la valeur de votre région.

* L’ARN de rôle Adobe IAM approprié pour votre région :

| Région | ARN des rôles Adobe IAM |
|---------|-------------------|
| Amérique du Nord | `arn:aws:iam::590183896800:role/rtcdp-collab-prod-va6-role` |
| Australie | `arn:aws:iam::590183896800:role/rtcdp-collab-prod-aus3-role` |
| EMEA | `arn:aws:iam::590183896800:role/rtcdp-collab-prod-deu1-role` |

Exemple de politique d’approbation :

```json
{
  "Version": "2012-10-17",
  "Statement": [
    {
      "Sid": "Statement1",
      "Effect": "Allow",
      "Principal": {
        "AWS": "<Adobe IAM Role ARN>"
      },
      "Action": "sts:AssumeRole"
    }
  ]
}
```

Vérifiez la politique et sélectionnez **Suivant** pour continuer.

Dans [!DNL Step 2] section **[!DNL Add permissions]** du workflow [!DNL Create role], recherchez et joignez la politique IAM que vous avez créée [précédemment](#create-policy). Sélectionnez la politique suivie de **[!DNL Next]** pour continuer à [!DNL Step 3].

Dans la section [!DNL Step 3] **[!DNL Name review, and create - Role details]** , indiquez un nom de rôle (par exemple, `s3-iam-role`) et une description facultative.

Cette page affiche la politique d’entité de confiance, le résumé de la politique d’autorisations et les balises que vous avez ajoutées pour l’organisation interne et le suivi.

Enfin, sélectionnez **Créer un rôle** pour confirmer la configuration.

>[!IMPORTANT]
>
>Vous devez enregistrer le nom de la ressource Amazon (ARN) après la création du rôle. Vous devrez fournir l’ARN du rôle IAM pendant l’étape **Authentifier votre connexion S3** du workflow [Configurer AWS S3 pour l’approvisionnement de l’audience](./configure-aws-s3-audience-sourcing.md).

## Étapes suivantes {#next-steps}

Cette configuration accorde à Adobe un accès en lecture seule à votre compartiment S3 et établit une connexion approuvée avec le rôle d’IAM d’Adobe.

Ensuite, passez à [Configurer AWS S3 pour le sourcing d’audience](./configure-aws-s3-audience-sourcing.md) pour connecter votre compartiment S3 à Collaboration.

Pour plus d&#39;informations sur l&#39;approvisionnement des audiences, consultez les sections [Source et gérer les audiences](./onboard-audiences.md).
