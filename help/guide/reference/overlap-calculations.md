---
title: Calcul des nombres et des pourcentages de chevauchement
description: Comprendre comment les nombres et pourcentages de chevauchement sont calculés dans les différentes zones d’Adobe Real-Time CDP Collaboration
audience: admin, publisher, advertiser
badgelimitedavailability: label="Disponibilité limitée" type="Informative" url="https://helpx.adobe.com/legal/product-descriptions/real-time-customer-data-platform-collaboration.html newtab=true"
source-git-commit: 23dc33af83366806f7d99161b4b713a33daeec76
workflow-type: tm+mt
source-wordcount: '869'
ht-degree: 1%

---


# Calcul du nombre et des pourcentages de chevauchement

Dans Adobe Real-Time CDP Collaboration, il est essentiel de comprendre le chevauchement des audiences pour optimiser vos stratégies marketing et assurer une collaboration efficace entre les annonceurs et les éditeurs. Ce document explique comment les nombres et les pourcentages de chevauchement dans différentes zones de produit sont calculés à l’aide de données d’exemple.

## Données d’exemple - Nombre d’identités

### Hypothèses de calcul

Pour cet exemple, supposons que :

* L’annonceur a trois audiences (A1, A2, A3).
* L’éditeur a trois audiences (P1, P2, P3).
* Toutes les identités de clé correspondantes s’excluent mutuellement dans toutes les audiences.

>[!NOTE]
>
>En réalité, il y aurait un certain chevauchement entre les identités de clé de correspondance de chaque audience. Par souci de simplicité, cet exemple suppose qu’elles sont exclusives dans ce cas.

### Audiences publicitaires

| Audiences publicitaires | A1 | A2 | A3 | TOUTES |
|----------------------|------|------|------|------|
| Identités d’email hachées | 300 K | 450K | 250K | 1M |
| Identités de l’identifiant Liveramp | 500K | 200 000 | 700K | 1,4 MILLION |
| Nombre total d’identités | 800K | 650K | 950 000 | 2,4 MILLIONS |

### Audiences de l’éditeur

| Audiences de l’éditeur | P1 | P2 | P3 | TOUTES |
|---------------------|------|------|------|------|
| Identités d’e-mail hachées | 150K | 600K | 550K | 1,3 MILLION |
| Identités de l’identifiant Liveramp | 400K | 350 K | 100 000 | 850K |
| Nombre total d’identités | 550K | 950 000 | 800K | 2,3 MILLIONS |

## Calcul des nombres et des pourcentages de chevauchement

### Données D’Exemple - Nombre De Chevauchements

#### Publicitaire et éditeur respectifs

|                     | A1 - P1 | A2 - P2 | A3 - P3 |
|---------------------|---------|---------|---------|
| Chevauchement par e-mail haché | 100 000 | 300K | 150 K |
| Chevauchement par ID Liveramp | 200 000 | 150K | 50K |
| Chevauchement total | 300K | 450K | 200 000 |

#### Advertiser Each vs Publisher ALL

|                     | A1 - P ALL | A2 - P ALL | A3 - P ALL |
|---------------------|------------|------------|------------|
| Chevauchement par e-mail haché | 250K | 400K | 200 000 |
| Chevauchement par ID Liveramp | 350K | 150K | 230K |
| Chevauchement total | 600K | 550K | 430K |

#### Tous les annonceurs par rapport à chacun des éditeurs

|                     | A ALL - P1 | A ALL - P2 | A ALL - P3 |
|---------------------|------------|------------|------------|
| Chevauchement par e-mail haché | 120 000 | 530K | 200 000 |
| Chevauchement par ID Liveramp | 350K | 330K | 50K |
| Chevauchement total | 470K | 860K | 250K |

#### Tout publicitaire contre tout éditeur

|                     | A ALL - P ALL |
|---------------------|---------------|
| Chevauchement par e-mail haché | 850K |
| Chevauchement par ID Liveramp | 730K |
| Chevauchement total | 1,58 M |

## Module Discover

Le module **[!UICONTROL Discover]** d’Adobe Real-Time CDP Collaboration fournit des informations précieuses sur les données de votre audience. En comprenant les chevauchements d’audiences, vous pouvez identifier les opportunités de collaboration potentielles entre les éditeurs et les annonceurs. La section **[!UICONTROL Informations sur les audiences]** du module **[!UICONTROL Découvrir]** vous aide à analyser le nombre et les pourcentages de chevauchement entre différentes audiences.

![Module Discover du workflow de collaboration.](/help/assets/reference/overlap-calculations/discover-module-overlap-calculations.png)

Consultez ci-dessous des exemples de calculs et de formules pour divers scénarios de chevauchement.

### Toutes les audiences d’annonceurs et toutes les audiences d’éditeurs

| Audiences publicitaires | Audiences de l’éditeur | Nombre D’Identités (A) | Chevauchement Des Identités (B) | Pourcentage de chevauchement | Ventilation de clés de correspondance | % de répartition de la clé correspondante |
|----------------------|---------------------|--------------------|----------------------------|-----------------|---------------------|-----------------------|
| TOUTES | TOUTES | Nombre total d’identités de TOUTES les audiences d’annonceurs <br> Nombre d’identités = 1 M + 1,4 M = 2,4 M | Chevauchement total entre TOUTES les audiences d’annonceurs et TOUTES les audiences d’éditeurs pour toutes les clés de correspondance <br> Identités qui se chevauchent = 1,58 million | Pourcentage d’identités qui se chevauchent par rapport au nombre total d’identités de TOUTES les audiences d’annonceurs <br> Pourcentage de chevauchement = (B / A) * 100 = (1,58 M / 2,4 M) * 100 = 65,83 % <br> Pourcentage de chevauchement = 65,83 % | Chevauchement des identités par clé <br> de correspondance Chevauchement par e-mail haché = 850 K <br> Chevauchement par ID Liveramp = 730 K | Pourcentage de chevauchement des clés de correspondance sur le nombre total d’identités qui se chevauchent <br> % de clé de correspondance pour les e-mails hachés = (850 000 / 1,58 M) * 100 = 53,8 % <br> pour l’ID Liveramp = (730 000 / 1,58 M) * 100 = 46,2 % |

### Toutes les audiences d’annonceurs et une audience d’éditeur

| Audiences publicitaires | Audiences de l’éditeur | Nombre d’identités (A) | Identités qui se chevauchent (B) | Pourcentage de chevauchement | Ventilation de clés de correspondance | Ventilation par clé correspondante % |
|----------------------|---------------------|--------------------|----------------------------|-----------------|---------------------|-----------------------|
| TOUTES | 1 P2 | Nombre total d’identités de toutes les audiences d’annonceurs <br> Nombre d’identités = 1 M + 1,4 M = 2,4 M | Chevauchement total entre TOUTES les audiences d’annonceurs et l’audience d’éditeur sélectionnée P2 pour toutes les clés de correspondance <br> Identités qui se chevauchent = 860 000 | Pourcentage d’identités qui se chevauchent par rapport au nombre total d’identités de TOUTES les audiences d’annonceurs <br> Pourcentage de chevauchement = (B / A) * 100 = (860 000 / 2,4 M) * 100 = 35,83 % <br> Pourcentage de chevauchement = 35,83 % | Chevauchement des identités par clé de correspondance <br> Chevauchement par e-mail haché = 530 000 <br> Chevauchement par ID Liveramp = 330 000 | Pourcentage de chevauchement des clés de correspondance sur le nombre total d’identités qui se chevauchent <br> % de clé de correspondance pour les e-mails hachés = (530K / 860K) * 100 = 61,62 % <br> pour l’ID Liveramp = (330K / 860K) * 100 = 38,38 % |

### Une audience d’annonceurs et toutes les audiences d’éditeurs

| Audiences publicitaires | Audiences de l’éditeur | Nombre D’Identités (A) | Chevauchement Des Identités (B) | Pourcentage de chevauchement | Ventilation de clés de correspondance | Ventilation par clé correspondante % |
|----------------------|---------------------|--------------------|----------------------------|-----------------|---------------------|-----------------------|
| 1 A1 | TOUTES | Nombre total d’identités de l’audience sélectionnée par l’annonceur Nombre d’identités A1 <br> = 300 K + 500 K = 800 K | Chevauchement total entre l’audience de l’annonceur A1 et TOUTES les audiences de l’éditeur pour toutes les clés de correspondance <br> Identités qui se chevauchent = 600 000 | Pourcentage d’identités qui se chevauchent par rapport au nombre d’identités de l’audience sélectionnée par l’annonceur (A1) <br> % de chevauchement = (B / A) * 100 = (600 000 / 800 000) * 100 = 75 % <br> pourcentage de chevauchement = 75 % | Chevauchement des identités par clé de correspondance <br> Chevauchement par e-mail haché = 250 000 <br> Chevauchement par ID Liveramp = 350 000 | Pourcentage de chevauchement des clés de correspondance sur le nombre total d’identités qui se chevauchent <br> % de clé de correspondance pour les e-mails hachés = (250 000 / 600 000) * 100 = 41,67 % <br> pour l’ID Liveramp = (350 000 / 600 000) * 100 = 58,33 % |

### Une audience publicitaire et une audience publicitaire

| Audiences publicitaires | Audiences de l’éditeur | Nombre D’Identités (A) | Chevauchement Des Identités (B) | Pourcentage de chevauchement | Répartition de la clé de correspondance | % de répartition de la clé correspondante |
|----------------------|---------------------|--------------------|----------------------------|-----------------|---------------------|-----------------------|
| 1 A2 | 1 P2 | Nombre total d’identités de l’audience sélectionnée par l’annonceur A2 <br> Nombre d’identités = 450 000 + 200 000 = 650 000 | Chevauchement total entre l’audience publicitaire sélectionnée A2 et l’audience publicitaire sélectionnée P2 pour toutes les clés de correspondance <br> Identités qui se chevauchent = 450 000 | Pourcentage d’identités qui se chevauchent par rapport au nombre d’identités de mon audience sélectionnée (A2) <br> Pourcentage de chevauchement = (B / A) * 100 = (450K / 650K) * 100 = 69,23 % <br> Pourcentage de chevauchement = 69,23 % | Chevauchement des identités par clé de correspondance <br> Chevauchement par e-mail haché = 300 000 <br> Chevauchement par ID Liveramp = 150 000 | Pourcentage de chevauchement des clés de correspondance sur le nombre total d’identités qui se chevauchent <br> % de clé de correspondance pour les e-mails hachés = (300 000 / 450 000) * 100 = 66,67 % <br> pour l’ID Liveramp = (150 000 / 450 000) * 100 = 33,33 % |
