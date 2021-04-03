---
title: Microsoft 365 traitant de l’altération des données
description: Cet article explique l’altération des données dans Microsoft 365 et les efforts déployés par Microsoft pour empêcher et récupérer des données.
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
ms.openlocfilehash: 9e9f0951f7e349cc70bc96bb6a2d62275848cf04
ms.sourcegitcommit: 024137a15ab23d26cac5ec14c36f3577fd8a0cc4
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 04/01/2021
ms.locfileid: "51497594"
---
# <a name="dealing-with-data-corruption-in-microsoft-365"></a>Gestion de l’altération des données dans Microsoft 365

L’un des aspects complexes de l’exécution d’un service cloud à grande échelle est la gestion de l’altération des données, étant donné le volume important de données et les systèmes indépendants. L’altération des données peut être causée par :

- Bogues d’application ou d’infrastructure, qui ont endommagé tout ou partie de l’état de l’application
- Problèmes matériels qui entraînent la perte de données ou l’impossibilité de lire les données
- Erreurs opérationnelles humaines
- Pirates malveillants et employés non régrunts
- Incidents dans les services externes qui entraînent une perte de données

Étant donné qu’une meilleure résilience de l’intégrité des données implique moins d’incidents de corruption de données, Microsoft a intégré des mécanismes de protection Microsoft 365 pour éviter toute altération, ainsi que des systèmes et des processus qui nous permettent de récupérer des données si c’est le cas. Des vérifications et des processus existent au cours des différentes étapes du processus de publication d’ingénierie pour renforcer la résilience contre l’altération des données, notamment :

- Conception du système
- Organisation et structure du code
- Révision du code
- Tests unitaires, tests d’intégration et tests système
- Tests/portails de câblage de voyage

Dans les environnements de production Microsoft 365, la réplication homologue entre les centres de données garantit qu’il existe toujours plusieurs copies dynamiques de toutes les données. Les images et les scripts standard sont utilisés pour récupérer les serveurs perdus et les données répliquées sont utilisées pour restaurer les données client. En raison des processus et des vérifications de résilience des données intégrés, Microsoft ne conserve que les sauvegardes de la documentation du système d’information Microsoft 365 (y compris la documentation relative à la sécurité), à l’aide de la réplication intégrée dans SharePoint Online et de notre outil de référentiel de code interne, Source Domaine. La documentation système est stockée dans SharePoint Online, et le Dossier source contient des images système et d’application. SharePoint Online et source sont tous deux utilisés par le service de version et sont répliqués en temps quasi réel.
