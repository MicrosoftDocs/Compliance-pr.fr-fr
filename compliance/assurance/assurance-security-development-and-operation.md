---
title: Vue d’ensemble des opérations et du développement de la sécurité
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
ms.openlocfilehash: 7c6752b84470eebbdb6ad78c212361156dea957b
ms.sourcegitcommit: 626b0076d133e588cd28598c149a7f272fc18bae
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 11/30/2020
ms.locfileid: "49506827"
---
# <a name="security-development-and-operations-overview"></a>Vue d’ensemble des opérations et du développement de la sécurité

## <a name="how-does-microsoft-implement-secure-development-practices"></a>Comment Microsoft implémente-t-il les pratiques de développement sécurisé ?

Le cycle de vie de développement de sécurité de Microsoft (SDL) est un processus d’assurance de sécurité axé sur le développement et l’exploitation de logiciels sécurisés. SDL fournit des exigences de sécurité détaillées et mesurables pour les développeurs et ingénieurs de Microsoft afin de réduire le nombre et la gravité des vulnérabilités dans nos produits et services. Toutes les équipes de développement de logiciels Microsoft doivent respecter les exigences de SDL et nous mettons à jour le SDL pour refléter le paysage des menaces, les meilleures pratiques du secteur et les normes réglementaires en matière de conformité.

## <a name="how-does-microsofts-sdl-improve-application-security"></a>Comment SDL améliore-t-elle la sécurité des applications ?

Le processus de SDL chez Microsoft peut être imaginé en cinq phases de développement : configuration requise, conception, implémentation, vérification et publication. Il commence par définir les exigences logicielles en gardant à l’esprit la sécurité. Pour ce faire, vous posez des questions relatives à la sécurité sur ce que l’application doit effectuer. L’application doit-elle collecter des données sensibles ? L’application peut-elle effectuer des tâches sensibles ou importantes ? L’application doit-elle accepter les entrées provenant de sources non fiables ?

Une fois les impératifs de sécurité pertinents identifiés, nous concevons nos logiciels de façon à intégrer des fonctionnalités de sécurité répondant à ces exigences. Nos développeurs implémentent les exigences de SDL et de conception dans le code, que nous vérifions via la révision manuelle du code, l’automatisation automatisée des outils de sécurité et le test de pénétration. Enfin, avant que le code puisse être publié, de nouvelles fonctionnalités et modifications de matériel sont soumises à la vérification de la sécurité et de la confidentialité finales afin de s’assurer que toutes les conditions sont remplies.

## <a name="how-does-microsoft-test-source-code-for-common-vulnerabilities"></a>Comment le code source de test Microsoft est-il destiné aux vulnérabilités courantes ?

Pour aider nos développeurs à mettre en œuvre les exigences de sécurité pendant le développement du code et après sa publication, Microsoft leur propose une suite d’outils de développement sécurisés qui permettent de vérifier automatiquement le code source et de détecter les failles de sécurité. Microsoft définit et publie une liste d’outils approuvés que les développeurs peuvent utiliser, tels que les compilateurs et les environnements de développement, ainsi que les vérifications de sécurité intégrées exécutées automatiquement dans les pipelines Microsoft Build. Nos développeurs utilisent les dernières versions des outils approuvés pour profiter des nouvelles fonctionnalités de sécurité.

Avant que le code puisse être archivé dans une branche de publication, le SDL requiert une vérification manuelle du code par un réviseur distinct. Les analystes de code vérifient les erreurs de codage et vérifient que les modifications de code répondent aux exigences SDL et de conception, réussissent les tests fonctionnels et de sécurité et fonctionnent de manière fiable. Ils examinent également la documentation, les configurations et les dépendances associées pour s’assurer que les modifications de code sont correctement documentées et ne provoqueront pas d’effets secondaires inattendus. Si un analyste trouve des problèmes lors de la révision du code, il peut demander à l’auteur de soumettre à nouveau le code avec les modifications suggérées et des tests supplémentaires. Les analystes de code peuvent également décider de bloquer entièrement l’archivage du code qui ne répond pas aux exigences. Une fois que le code a été jugé satisfaisant par le réviseur, le réviseur fournit une approbation, qui est requise avant que le code puisse passer à la phase de déploiement suivante.

En plus des outils de développement sécurisés et de la révision manuelle du code, Microsoft applique les exigences de SDL à l’aide d’outils de sécurité automatisés. Un grand nombre de ces outils sont intégrés au pipeline de validation et analysent automatiquement le code pour les failles de sécurité lors de l’archivage et la compilation de nouvelles builds. Les exemples incluent l’analyse de code statique pour les failles de sécurité courantes et les analyseurs d’informations d’identification qui analysent le code pour les secrets incorporés. Les problèmes non couverts par les outils de sécurité automatisés doivent être résolus avant que les nouvelles builds puissent transmettre la vérification de la sécurité et être approuvées pour la publication.

## <a name="how-does-microsoft-manage-open-source-software"></a>Comment Microsoft gère-t-il les logiciels open source ?

Microsoft a adopté une stratégie de haut niveau pour la gestion de la sécurité Open source, qui exploite les outils et les flux de travail conçus pour :

- Comprendre les composants Open source utilisés dans nos produits et services.
- Suivez l’emplacement et la façon dont ces composants sont utilisés.
- Déterminez si ces composants présentent des vulnérabilités.
- Répondre correctement lorsque des vulnérabilités sont découvertes et qui affectent ces composants.

Les équipes Microsoft Engineering sont responsables de la sécurité de tous les logiciels open source inclus dans un produit ou un service. Pour y parvenir à l’échelle, Microsoft a intégré les fonctionnalités essentielles aux systèmes d’ingénierie via CG, ce qui permet d’automatiser la détection des sources ouvertes, les flux de travail de besoins juridiques et les alertes pour les composants exposés. Outils CG automatisés : analyse des versions de Microsoft pour les composants Open source et les failles de sécurité ou obligations légales associées. Les composants découverts sont enregistrés et envoyés aux équipes appropriées pour les avis d’entreprise et de sécurité. Ces examens sont conçus pour évaluer les obligations légales ou les vulnérabilités de sécurité associées aux composants Open source et les résoudre avant d’approuver les composants à des fins de déploiement.

## <a name="related-external-regulations--certifications"></a>Certifications & des réglementations externes connexes

Les services en ligne de Microsoft sont régulièrement vérifiés pour la conformité aux réglementations et aux certifications externes. Reportez-vous au tableau suivant pour la validation des contrôles liés au développement et à l’exploitation de la sécurité.

| **Audits externes** | **Section** | **Date du dernier rapport** |
|:--------------------|:------------|:-----------------------|
| [FedRAMP (Office 365)](https://compliance.microsoft.com/compliancemanager) | SA-3 : cycle de vie de développement du système | 24 septembre 2020 |
| [ISO 27001/27002 (Office 365)](https://servicetrust.microsoft.com/ViewPage/MSComplianceGuideV3?command=Download&downloadType=Document&downloadId=d7864d4f-e053-4cc4-a964-fa526d07c3be&tab=7027ead0-3d6b-11e9-b9e1-290b1eb4cdeb&docTab=7027ead0-3d6b-11e9-b9e1-290b1eb4cdeb_ISO_Reports) <br><br> [Déclaration de l’applicabilité](https://servicetrust.microsoft.com/ViewPage/MSComplianceGuide?command=Download&downloadType=Document&downloadId=8ee1e46b-2ada-4e7b-bb7d-4c55a8cb6fcd&docTab=4ce99610-c9c0-11e7-8c2c-f908a777fa4d_ISO_Reports) <br> [Certification](https://servicetrust.microsoft.com/ViewPage/MSComplianceGuideV3?command=Download&downloadType=Document&downloadId=1e84a14a-2468-45ac-9412-5e53250d57ec&tab=7027ead0-3d6b-11e9-b9e1-290b1eb4cdeb&docTab=7027ead0-3d6b-11e9-b9e1-290b1eb4cdeb_ISO_Reports) | A. 12.1.2 : contrôles de gestion des modifications <br> A. 14.2 : sécurité dans les processus de développement et de prise en charge | 22 février 2020 |
| [ISO 27017 (Office 365)](https://servicetrust.microsoft.com/ViewPage/MSComplianceGuideV3?command=Download&downloadType=Document&downloadId=d7864d4f-e053-4cc4-a964-fa526d07c3be&tab=7027ead0-3d6b-11e9-b9e1-290b1eb4cdeb&docTab=7027ead0-3d6b-11e9-b9e1-290b1eb4cdeb_ISO_Reports) <br><br> [Déclaration de l’applicabilité](https://servicetrust.microsoft.com/ViewPage/MSComplianceGuide?command=Download&downloadType=Document&downloadId=8ee1e46b-2ada-4e7b-bb7d-4c55a8cb6fcd&docTab=4ce99610-c9c0-11e7-8c2c-f908a777fa4d_ISO_Reports) <br> [Certification](https://servicetrust.microsoft.com/ViewPage/MSComplianceGuideV3?command=Download&downloadType=Document&downloadId=70de0999-5451-43a3-9ef4-761e8fbfb1a3&tab=7027ead0-3d6b-11e9-b9e1-290b1eb4cdeb&docTab=7027ead0-3d6b-11e9-b9e1-290b1eb4cdeb_ISO_Reports) | A. 12.1.2 : contrôles de gestion des modifications <br> A. 14.2 : sécurité dans les processus de développement et de prise en charge | 22 février 2020 |
| [SOC 1 (Office 365)](https://servicetrust.microsoft.com/ViewPage/MSComplianceGuideV3?command=Download&downloadType=Document&downloadId=b07c0f7b-6bd5-4544-8255-7a5f14bf914a&tab=7027ead0-3d6b-11e9-b9e1-290b1eb4cdeb&docTab=7027ead0-3d6b-11e9-b9e1-290b1eb4cdeb_SOC_/_SSAE_16_Reports) | CA-03 : gestion des risques <br> CA-18 : gestion des modifications <br> CA-19 : analyse des modifications <br> CA-21 : test des modifications <br> CA-38 : configurations de base <br> CA-46 : révision de la sécurité | 30 septembre 2019 |
| [SOC 2 (Office 365)](https://servicetrust.microsoft.com/ViewPage/MSComplianceGuideV3?command=Download&downloadType=Document&downloadId=fa062990-e758-4ddc-ace3-7fb21a301d09&tab=7027ead0-3d6b-11e9-b9e1-290b1eb4cdeb&docTab=7027ead0-3d6b-11e9-b9e1-290b1eb4cdeb_SOC_/_SSAE_16_Rep-11e9-b9e1-290b1eb4cdeb_SOC_/_SSAE_16_Reports) | CA-03 : gestion des risques <br> CA-18 : gestion des modifications <br> CA-19 : analyse des modifications <br> CA-21 : test des modifications <br> CA-38 : configurations de base <br> CA-46 : révision de la sécurité | 30 septembre 2019 |

## <a name="resources"></a>Ressources

- [Cycle de vie du développement de la sécurité Microsoft](https://www.microsoft.com/securityengineering/sdl)
