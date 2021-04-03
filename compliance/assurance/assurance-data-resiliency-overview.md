---
title: Résilience des données dans Microsoft 365
description: Dans cet article, découvrez la conception et les principes de résilience et de récupération des données dans Microsoft 365.
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
ms.openlocfilehash: 6e990facde47b07d50f594afb55353a5ef81dd78
ms.sourcegitcommit: 024137a15ab23d26cac5ec14c36f3577fd8a0cc4
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 04/01/2021
ms.locfileid: "51497625"
---
# <a name="data-resiliency-in-microsoft-365"></a>Résilience des données dans Microsoft 365

Étant donné la nature complexe du cloud computing, Microsoft n’oublie pas qu’il ne s’agit pas de savoir si les choses vont mal se passer, mais plutôt quand. Nous concevons nos services cloud pour optimiser la fiabilité et minimiser les effets négatifs sur les clients en cas de problème. Nous avons dépassé la stratégie traditionnelle qui consiste à s’appuyer sur une infrastructure physique complexe et nous avons intégré la redondance directement dans nos services cloud. Nous utilisons une combinaison d’infrastructure physique moins complexe et de logiciels plus intelligents qui renforcent la résilience des données dans nos services et offrent une haute disponibilité à nos clients.

## <a name="resiliency-and-recoverability-are-built-in"></a>La résilience et la récupérabilité sont intégrées

La création d’une résilience et d’une récupération commence par l’hypothèse que l’infrastructure et les processus sous-jacents échoueront à un moment donné : le matériel (infrastructure) échouera, les humains commeront des erreurs et les logiciels auront des bogues. Bien qu’il soit incorrect de dire que les développeurs de logiciels ne réfléchissaient pas à ces éléments avant le cloud, la façon dont ces problèmes étaient traités dans une implémentation informatique classique était différente avant le cloud :

- Tout d’abord, les protections matérielles et d’infrastructure étaient importantes. Cette structure nécessitait que des centres de données avec une fiabilité de 99,99 % nécessitaient une puissance et une redondance réseau importantes, et que les serveurs étaient implémentés avec le clustering matériel, les deux alimentations, les interfaces réseau doubles, etc.
- Ensuite, le processus a été essentiel. Les équipes opérationnelles ont maintenu des procédures rigoureuses, des fenêtres de modification ont été employées et il y a souvent eu une surcharge de gestion de projet importante.
- Troisièmement, le déploiement s’est déroulée à un rythme très élevé. Le déploiement de code sans propriétaire de la source implique l’attente de versions de correctifs, et les versions majeures impliquent un remplacement matériel et une dépense importante en capital. En outre, la seule façon de corriger un problème était de revenir en arrière. Par conséquent, la plupart des organisations de l’it doivent déployer uniquement les principales publications afin d’éviter que le travail ne soit à jour.
- Enfin, l’échelle des systèmes déployés et le niveau de leur interconnectivité étaient historiquement beaucoup plus petits qu’aujourd’hui.

Aujourd’hui, les clients s’attendent à une innovation continue de Microsoft sans compromettre la qualité, et c’est l’une des raisons pour lesquelles les services et logiciels de Microsoft sont conçus avec résilience et récupérabilité à l’esprit.

## <a name="microsoft-365-data-resiliency-principles"></a>Principes de résilience des données Microsoft 365

La résilience fait référence à la capacité d’un service basé sur le cloud à résister à certains types d’échecs tout en maintenant une fonctionnalité complète du point de vue des clients. La résilience des données signifie que, quelles que soit les défaillances qui se produisent dans Microsoft 365, les données client critiques restent intactes et non affectées. À cette fin, les services Microsoft 365 ont été conçus autour de cinq principes de résilience spécifiques :

- Il existe des données critiques et non critiques. Les données non critiques (par exemple, si un message a été lu) peuvent être abandonnées dans de rares scénarios d’échec. Les données critiques (par exemple, les données client telles que les messages électroniques) doivent être protégées à un coût extrême. En tant qu’objectif de conception, les messages électroniques remis sont toujours essentiels et des éléments tels que la lecture d’un message ne sont pas essentiels.
- Les copies des données client doivent être séparées en différentes zones d’erreur ou autant de domaines d’erreur que possible (par exemple, des centres de données, accessibles par des informations d’identification simples (processus, serveur ou opérateur)) pour assurer l’isolation des défaillances. 
- Les données client critiques doivent être surveillées pour les défaillances d’une partie de l’atomicité, de la cohérence, de l’isolation, de la délation (UMA).
- Les données client doivent être protégées contre l’altération. Il doit être analysé ou surveillé activement, réparable et récupérable.
- La plupart des pertes de données résultent d’actions des clients. Autorisez donc les clients à récupérer eux-mêmes à l’aide d’une interface utilisateur graphique qui leur permet de restaurer des éléments supprimés accidentellement.

Grâce à la création de nos services cloud à ces principes, couplés à des tests et une validation robustes, Microsoft 365 est en mesure de répondre aux exigences des clients et de les dépasser tout en garantissant une plateforme d’innovation et d’amélioration continue.

## <a name="related-articles"></a>Articles connexes

- [Gérer l’altération des données](assurance-dealing-with-data-corruption.md)
- [Protection contre les ransomware et programmes malveillants](assurance-malware-and-ransomware-protection.md)
- [Surveillance et auto-adaptation](assurance-monitoring-and-self-healing.md)
- [Résilience des données Exchange](assurance-exchange-data-resiliency.md)
