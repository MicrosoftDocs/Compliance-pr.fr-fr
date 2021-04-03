---
title: Classification des données & taxonomie des étiquettes de sensibilité
description: Dans cet article, vous trouverez une vue d’ensemble de l’utilisation de la classification des & la taxonomie des étiquettes de sensibilité avec Microsoft 365.
ms.author: robmazz
author: robmazz
manager: laurawi
ms.reviewer: sosstah
audience: ITPro
ms.topic: article
ms.service: O365-seccomp
localization_priority: Normal
search.appverid:
- MET150
ms.collection:
- Strat_O365_IP
- M365-security-compliance
- MS-Compliance
f1.keywords:
- NOCSH
ms.custom: seo-marvel-apr2020
titleSuffix: Microsoft Service Assurance
hideEdit: true
ms.openlocfilehash: fcfe98116f4d0629f322383f2992605d2dcf19de
ms.sourcegitcommit: 024137a15ab23d26cac5ec14c36f3577fd8a0cc4
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 04/01/2021
ms.locfileid: "51497794"
---
# <a name="data-classification--sensitivity-label-taxonomy"></a>Classification des données & taxonomie des étiquettes de sensibilité

Les données sensibles présentent un risque important pour une entreprise si elles sont volées, partagées par inadvertance ou exposées par le biais d’une violation. Les facteurs de risque incluent les dommages de réputation, l’impact financier et la perte de l’avantage concurrentiel. La protection des données et des informations que votre entreprise gère est une priorité absolue pour votre organisation, mais il peut vous être difficile de savoir si vos efforts sont réellement efficaces, étant donné la quantité de contenu détenue par votre entreprise.

En plus du volume, votre contenu peut avoir une importance très sensible et impactante à triviale et passagère. Il peut également être sous le contrôle de diverses exigences de conformité réglementaire. Il peut être difficile de savoir quoi hiérarchiser et où appliquer des contrôles. Lisez la suite pour en savoir plus sur la *classification* des données, un outil important pour protéger votre contenu contre le vol, le sabotage ou la destruction accidentelle, et comment Microsoft 365 peut vous aider à atteindre vos objectifs de sécurité des informations.

## <a name="what-is-data-classification"></a>Qu’est-ce que la classification des données ?

La [classification](/microsoft-365/compliance/data-classification-overview) des données est un terme spécialisé utilisé dans les domaines de la cybersécurité et de la gouvernance des informations pour décrire le processus d’identification, de catégorisation et de protection du contenu en fonction de son niveau de sensibilité ou d’impact. Dans sa forme la plus élémentaire, la classification des données est un moyen de protéger vos données contre toute divulgation, altération ou destruction non autorisée en fonction de leur sensibilité ou de leur impact.

## <a name="what-is-a-data-classification-framework"></a>Qu’est-ce qu’une infrastructure de classification des données ?

Souvent codifié dans une stratégie formelle à l’échelle de l’entreprise, une infrastructure de classification des données (parfois appelée « stratégie de classification des données » ) se compose généralement de 3 à 5 niveaux de classification. Il s’agit généralement de trois éléments : un nom, une description et des exemples réels. Microsoft ne recommande pas plus de cinq étiquettes parentes de niveau supérieur, chacune avec cinq sous-étiquettes (25 au total) pour que l’interface utilisateur reste gérable. Les niveaux sont généralement organisés du moins au plus sensible comme *public,* *interne,* confidentiel *et* *hautement* 
 *confidentiel*. Les autres variantes de nom de niveau que vous pouvez rencontrer sont *Restricted,* *Unrestricted* et *Consumer Protected*. Microsoft recommande les noms d’étiquettes qui sont auto-descriptifs et qui mettent clairement en évidence leur sensibilité relative. Par exemple, *confidentiel et* *restreint* peuvent laisser les utilisateurs  deviner l’étiquette appropriée, tandis que confidentiel et hautement confidentiel sont plus clairs sur ce qui est plus sensible.  Le tableau suivant présente des exemples de niveaux d’infrastructure de classification des données.

|**Niveau de classification**|**Description**|**Exemples**|
|:-----------------------|:--------------|:-----------|
| Hautement confidentiel | Les données hautement confidentielles sont le type de données le plus sensible stocké ou géré par l’entreprise et peuvent nécessiter des notifications juridiques en cas de violation ou de divulgation. <br><br> Les données restreintes nécessitent le niveau de contrôle et de sécurité le plus élevé, et l’accès doit être limité à « besoin de savoir ». | Informations d’identification personnelle sensibles (PII sensibles) <br> Données de l’espace réservé de carte <br> Informations de santé protégées (PHI) <br> Données de compte bancaire |

>[!TIP]
>L’infrastructure de classification des données d’entreprise de Microsoft utilisait à l’origine une catégorie et une étiquette nommées « Internal » lors de la phase pilote, mais a constaté qu’il existe des raisons légitimes de partager un document en externe et de passer à l’utilisation de « Général ».

Un autre composant important d’une infrastructure de classification des données est les contrôles associés à chaque niveau. Les niveaux de classification des données sont simplement des étiquettes (ou des balises) qui indiquent la valeur ou la sensibilité du contenu. Pour *protéger ce* contenu, les infrastructure de classification des données définissent les contrôles qui doivent être en place pour chacun de vos niveaux de classification des données. Ces contrôles peuvent inclure des exigences liées aux éléments suivants :

- Type et emplacement de stockage
- Chiffrement
- Contrôle d’accès
- Destruction des données
- Protection contre la perte de données
- Divulgation publique
- Journalisation et suivi de l’accès
- Autres objectifs de contrôle, selon les besoins

Vos contrôles de sécurité varient en fonction du niveau de classification des données, afin que les mesures de protection définies dans votre infrastructure augmentent en fonction de la sensibilité de votre contenu. Par exemple, vos exigences en matière de contrôle de stockage de données varient en fonction du média utilisé, ainsi que du niveau de classification appliqué à un élément de contenu donné. Le tableau suivant présente un exemple de contrôles de classification des données pour un type de stockage spécifique :

|**Type de stockage**|**Confidentiel**|**Interne**|**Non restreint**|
|:---------------|:---------------|:-----------|:---------------|
| Stockage amovible | Interdit | Interdit sauf chiffrement | Aucun contrôle requis |

L’application correcte du niveau de classification des données peut être complexe dans des situations réelles et parfois submerger les utilisateurs finaux. Une fois qu’une stratégie ou une norme a été créée qui définit les niveaux requis de classification des données, il est important de guider les utilisateurs finaux sur la façon de donner vie à cette infrastructure dans leur travail quotidien. C’est dans ce domaine que les règles ou recommandations de gestion de la classification des données entrent en vigueur.

Les instructions de gestion de la classification des données aideront les utilisateurs finaux à donner des instructions spécifiques sur la gestion appropriée de chaque niveau de données, pour différents supports de stockage tout au long de leur cycle de vie. Ces recommandations aident les utilisateurs finaux à appliquer correctement des règles en pratique, par exemple lors du partage de documents, de l’envoi de courriers électroniques ou de la collaboration sur différentes plateformes et organisations.

Les clients Microsoft indiquent qu’environ 50 % d’un projet de protection des informations est axé sur l’entreprise plutôt que sur la technique. Par conséquent, la formation et la communication des utilisateurs finals sont essentielles à la réussite.
