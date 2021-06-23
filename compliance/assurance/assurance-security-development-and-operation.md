---
title: Vue d’ensemble du développement et des opérations de sécurité
description: En savoir plus sur le développement et les opérations de sécurité dans Microsoft 365
ms.author: robmazz
author: robmazz
manager: laurawi
ms.reviewer: sosstah
audience: Admin
ms.topic: article
f1.keywords:
- NOCSH
ms.service: O365-seccomp
localization_priority: Normal
ms.collection:
- Strat_O365_IP
- M365-security-compliance
search.appverid:
- MET150
- MOE150
titleSuffix: Microsoft Service Assurance
hideEdit: true
ms.openlocfilehash: d1cc1473a0478cd516ddfebf37d881174219e0c2
ms.sourcegitcommit: fb379d1110a9a86c7f9bab8c484dc3f4b3dfd6f0
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 06/23/2021
ms.locfileid: "53087603"
---
# <a name="security-development-and-operations-overview"></a>Vue d’ensemble du développement et des opérations de sécurité

## <a name="how-does-microsoft-implement-secure-development-practices"></a>Comment Microsoft implémente-t-il des pratiques de développement sécurisé ?

Le cycle de vie du développement de la sécurité (SDL) de Microsoft est un processus d’assurance sécurité axé sur le développement et le fonctionnement de logiciels sécurisés. SDL fournit des exigences de sécurité détaillées et mesurables pour les développeurs et ingénieurs de Microsoft afin de réduire le nombre et la gravité des vulnérabilités dans nos produits et services. Toutes les équipes de développement de logiciels Microsoft doivent respecter les exigences SDL et nous les mettez à jour en permanence pour refléter l’évolution du paysage des menaces, les meilleures pratiques du secteur et les normes réglementaires en matière de conformité.

## <a name="how-does-microsofts-sdl-improve-application-security"></a>Comment le SDL de Microsoft améliore-t-il la sécurité des applications ?

Le processus SDL chez Microsoft peut être conçu en cinq phases de développement : exigences, conception, implémentation, vérification et publication. Il commence par définir les exigences logicielles en gardant à l’esprit la sécurité. Pour ce faire, vous posez des questions relatives à la sécurité sur ce que l’application doit effectuer. L’application doit-elle collecter des données sensibles ? L’application peut-elle effectuer des tâches sensibles ou importantes ? L’application doit-elle accepter les entrées provenant de sources non fiables ?

Une fois les impératifs de sécurité pertinents identifiés, nous concevons nos logiciels de façon à intégrer des fonctionnalités de sécurité répondant à ces exigences. Nos développeurs implémentent les exigences de SDL et de conception dans le code, que nous vérifions via la révision manuelle du code, l’automatisation automatisée des outils de sécurité et le test de pénétration. Enfin, avant la publication du code, les nouvelles fonctionnalités et modifications matérielles font l’objet d’une révision finale de la sécurité et de la confidentialité afin de s’assurer que toutes les conditions sont remplies.

## <a name="how-does-microsoft-test-source-code-for-common-vulnerabilities"></a>Comment Microsoft teste-t-il le code source pour les vulnérabilités courantes ?

Pour aider nos développeurs à mettre en œuvre les exigences de sécurité pendant le développement du code et après sa publication, Microsoft leur propose une suite d’outils de développement sécurisés qui permettent de vérifier automatiquement le code source et de détecter les failles de sécurité. Microsoft définit et publie une liste d’outils approuvés que nos développeurs peuvent utiliser, tels que les compilateurs et les environnements de développement, ainsi que les vérifications de sécurité intégrées exécutées automatiquement dans les pipelines de build De Microsoft. Nos développeurs utilisent les dernières versions des outils approuvés pour profiter des nouvelles fonctionnalités de sécurité.

Avant que le code puisse être vérifié dans une branche de publication, le SDL nécessite une révision manuelle du code par un réviseur distinct. Les analystes de code vérifient les erreurs de codage et vérifient que les modifications de code répondent aux exigences SDL et de conception, réussissent les tests fonctionnels et de sécurité et fonctionnent de manière fiable. Ils examinent également la documentation, les configurations et les dépendances associées pour s’assurer que les modifications de code sont correctement documentées et ne provoqueront pas d’effets secondaires inattendus. Si un analyste trouve des problèmes lors de la révision du code, il peut demander à l’auteur de soumettre à nouveau le code avec les modifications suggérées et des tests supplémentaires. Les analystes de code peuvent également décider de bloquer entièrement l’archivage du code qui ne répond pas aux exigences. Une fois que le code a été considéré comme satisfaisant par le réviseur, il fournit une approbation, qui est requise pour que le code puisse passer à la phase de déploiement suivante.

En plus des outils de développement sécurisés et de la révision manuelle du code, Microsoft applique les exigences SDL à l’aide d’outils de sécurité automatisés. La plupart de ces outils sont intégrés au pipeline de validation et analysent automatiquement le code pour les failles de sécurité lors de son analyse et au cours de la compilation des nouvelles builds. Les exemples incluent l’analyse de code statique pour les failles de sécurité courantes et les scanneurs d’informations d’identification qui analysent le code pour les secrets incorporés. Les problèmes découverts par les outils de sécurité automatisés doivent être résolus pour que les nouvelles builds passent l’examen de sécurité et soient approuvées pour publication.

## <a name="how-does-microsoft-manage-open-source-software"></a>Comment Microsoft gère-t-il les logiciels open source ?

Microsoft a adopté une stratégie de haut niveau pour la gestion de la sécurité open source, qui tire parti des outils et des flux de travail conçus pour :

- Comprendre les composants Open source utilisés dans nos produits et services.
- Suivez l’emplacement et la façon dont ces composants sont utilisés.
- Déterminez si ces composants présentent des vulnérabilités.
- Répondre correctement lorsque des vulnérabilités sont découvertes et qui affectent ces composants.

Les équipes Microsoft Engineering sont responsables de la sécurité de tous les logiciels open source inclus dans un produit ou un service. Pour y parvenir à l’échelle, Microsoft a intégré les fonctionnalités essentielles aux systèmes d’ingénierie via CG, ce qui permet d’automatiser la détection des sources ouvertes, les flux de travail de besoins juridiques et les alertes pour les composants exposés. Les outils CG automatisés analysent les builds de Microsoft pour les composants open source et les vulnérabilités de sécurité associées ou les obligations légales. Les composants découverts sont enregistrés et envoyés aux équipes appropriées pour les avis d’entreprise et de sécurité. Ces examens sont conçus pour évaluer les obligations légales ou les vulnérabilités de sécurité associées aux composants Open source et les résoudre avant d’approuver les composants à des fins de déploiement.

## <a name="related-external-regulations--certifications"></a>Réglementations externes associées & certifications

Les services en ligne de Microsoft sont régulièrement audités pour assurer la conformité avec les réglementations et certifications externes. Reportez-vous au tableau suivant pour la validation des contrôles liés au développement et au fonctionnement de la sécurité.

| **Audits externes** | **Section** | **Date de rapport la plus récente** |
|:--------------------|:------------|:-----------------------|
| [FedRAMP (Office 365)](https://compliance.microsoft.com/compliancemanager) | SA-3 : Cycle de vie du développement système | 24 septembre 2020 |
| [ISO 27001/27002 (Office 365)](https://servicetrust.microsoft.com/ViewPage/MSComplianceGuideV3?command=Download&downloadType=Document&downloadId=8d625374-4f2d-49f8-9d37-a4281ba98222&tab=7027ead0-3d6b-11e9-b9e1-290b1eb4cdeb&docTab=7027ead0-3d6b-11e9-b9e1-290b1eb4cdeb_ISO_Reports) <br><br> [Déclaration d’applicabilité](https://servicetrust.microsoft.com/ViewPage/MSComplianceGuideV3?command=Download&downloadType=Document&downloadId=c0df4ce8-c77e-4183-84eb-c8688470d8b1&tab=7027ead0-3d6b-11e9-b9e1-290b1eb4cdeb&docTab=7027ead0-3d6b-11e9-b9e1-290b1eb4cdeb_ISO_Reports) <br> [Certification](https://servicetrust.microsoft.com/ViewPage/MSComplianceGuideV3?command=Download&downloadType=Document&downloadId=1e84a14a-2468-45ac-9412-5e53250d57ec&tab=7027ead0-3d6b-11e9-b9e1-290b1eb4cdeb&docTab=7027ead0-3d6b-11e9-b9e1-290b1eb4cdeb_ISO_Reports) | A.12.1.2 : Contrôles de gestion des changements <br> A.14.2 : Sécurité dans les processus de développement et de support | 20 avril 2021 |
| [ISO 27017 (Office 365)](https://servicetrust.microsoft.com/ViewPage/MSComplianceGuideV3?command=Download&downloadType=Document&downloadId=8d625374-4f2d-49f8-9d37-a4281ba98222&tab=7027ead0-3d6b-11e9-b9e1-290b1eb4cdeb&docTab=7027ead0-3d6b-11e9-b9e1-290b1eb4cdeb_ISO_Reports) <br><br> [Déclaration d’applicabilité](https://servicetrust.microsoft.com/ViewPage/MSComplianceGuideV3?command=Download&downloadType=Document&downloadId=c0df4ce8-c77e-4183-84eb-c8688470d8b1&tab=7027ead0-3d6b-11e9-b9e1-290b1eb4cdeb&docTab=7027ead0-3d6b-11e9-b9e1-290b1eb4cdeb_ISO_Reports) <br> [Certification](https://servicetrust.microsoft.com/ViewPage/MSComplianceGuideV3?command=Download&downloadType=Document&downloadId=70de0999-5451-43a3-9ef4-761e8fbfb1a3&tab=7027ead0-3d6b-11e9-b9e1-290b1eb4cdeb&docTab=7027ead0-3d6b-11e9-b9e1-290b1eb4cdeb_ISO_Reports) | A.12.1.2 : Contrôles de gestion des changements <br> A.14.2 : Sécurité dans les processus de développement et de support | 20 avril 2021 |
| [SOC 1 (Office 365)](https://servicetrust.microsoft.com/ViewPage/MSComplianceGuideV3?command=Download&downloadType=Document&downloadId=90df3f9c-3aaf-4dbf-99d0-ca9f2991721b&tab=7027ead0-3d6b-11e9-b9e1-290b1eb4cdeb&docTab=7027ead0-3d6b-11e9-b9e1-290b1eb4cdeb_SOC_%2F_SSAE_16_Reports) | CA-03 : Gestion des risques <br> CA-18 : Gestion des changements <br> CA-19 : Analyse des changements <br> CA-21 : Test des changements <br> CA-38 : Configurations de référence <br> CA-46 : Révision de sécurité | 24 décembre 2020 |
| [SOC 2 (Office 365)](https://servicetrust.microsoft.com/ViewPage/MSComplianceGuideV3?command=Download&downloadType=Document&downloadId=a73c1738-7892-42b7-acd3-87b6371c53f6&tab=7027ead0-3d6b-11e9-b9e1-290b1eb4cdeb&docTab=7027ead0-3d6b-11e9-b9e1-290b1eb4cdeb_SOC_%2F_SSAE_16_Reports) | CA-03 : Gestion des risques <br> CA-18 : Gestion des changements <br> CA-19 : Analyse des changements <br> CA-21 : Test des changements <br> CA-38 : Configurations de référence <br> CA-46 : Révision de sécurité | 24 décembre 2020 |

## <a name="resources"></a>Ressources

- [Cycle de vie du développement de la sécurité de Microsoft](https://www.microsoft.com/securityengineering/sdl)
