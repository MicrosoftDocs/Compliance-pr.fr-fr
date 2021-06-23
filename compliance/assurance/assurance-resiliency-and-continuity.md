---
title: Résilience et continuité
description: En savoir plus sur la résilience et la continuité dans Microsoft 365
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
ms.openlocfilehash: 9ac4a87670d1889e9c74e5ec6afe8920b96946fc
ms.sourcegitcommit: fb379d1110a9a86c7f9bab8c484dc3f4b3dfd6f0
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 06/23/2021
ms.locfileid: "53088773"
---
# <a name="resiliency-and-continuity-overview"></a>Aperçu sur la résilience et la continuité

## <a name="how-does-microsoft-ensure-business-continuity-in-the-case-of-a-disaster-or-other-threat-to-service-availability"></a>Comment Microsoft assure-t-il la continuité de l’activité en cas d’urgence ou d’une autre menace pour la disponibilité du service ?

L’équipe Enterprise gestion de la continuité d’activité (EBCM) de Microsoft supervise la gestion de la continuité des opérations et les activités de récupération d’urgence au sein des offres services Microsoft et cloud. Les représentants des unités commerciales Microsoft, telles que Microsoft 365, se coordonnent avec l’équipe EBCM pour développer des plans de continuité d’activité et valider la conformité avec les exigences de continuité d’activité.

Le cycle de vie bcm est au cœur de notre méthodologie de gestion de la continuité d’activité (BCM). Ce processus en trois phases est conçu pour être adaptable afin qu’il puisse être implémenté par un large éventail de modèles métiers dans Microsoft. Elle commence par une **phase** d’évaluation pour identifier les processus et objectifs critiques qui doivent être inclus dans le programme de continuité d’activité. La phase d’évaluation nécessite également une analyse d’impact commercial (BIA). La phase de **Planification** se concentre sur le développement et l’implémentation de stratégies de résilience et de récupération, ainsi que sur leur documentation dans les plans de continuité de l’activité officiel. Enfin, la **validation des fonctionnalités** teste les plans de continuité d’activité et leurs implémentations pour vérifier l’efficacité et identifier les améliorations potentielles.

Microsoft 365 la continuité d’activité de l’entreprise tire parti de la redondance du matériel, du réseau et des centres de données. La réplication des données entre les centres de données fournit une haute disponibilité et une grande fiabilité en cas d’incident catastrophique. Elle augmente également la résilience aux incidents non courants tels que les défaillances matérielles isolées ou l’altération des données.

## <a name="how-does-microsoft-test-business-continuity-and-disaster-recovery-plans"></a>Comment Microsoft teste-t-il les plans de continuité d’activité et de récupération d’urgence ?

La stratégie de gestion de la Enterprise continuité d’activité (EBCM) de Microsoft stipule que tous les plans de continuité d’activité et de récupération d’urgence de Microsoft doivent être testés, mis à jour et examinés sur une base annuelle. Microsoft 365 services testent leurs plans de continuité d’activité au moins une fois par an par stratégie EBCM. Une fois les rapports d’action créés et révisés pour valider, testez les résultats et informez les mises à jour de plan en réponse aux problèmes détectés lors des tests.

Pour valider les stratégies de résilience et de récupération par rapport à divers incidents potentiels, le programme EBCM définit plusieurs catégories de scénarios de test affectant les personnes, les emplacements et les technologies. Le niveau de validation requis pour chaque service est basé sur la criticalité du service, avec des services plus critiques qui reçoivent une validation plus rigoureuse. Chaque Microsoft 365 de service teste son plan de continuité d’activité conformément aux instructions EBCM pour mesurer l’efficacité du plan et la préparation de l’équipe de service à l’exécution du plan.

Selon les recommandations EBCM, les révisions annuelles des plans de continuité d’activité et la validation des fonctionnalités doivent avoir lieu dans les 12 mois suivant la dernière révision. La validation des fonctionnalités doit inclure la révision de la documentation prise en charge, telle que la BIA, pour s’assurer qu’elle reste précise. Microsoft met à la disposition de nos clients les résultats de validation des fonctionnalités pour Microsoft 365 services disponibles via des rapports trimestrielles.

## <a name="how-does-microsoft-365-ensure-system-capacity-meets-demand"></a>Comment s’Microsoft 365 s’assurer que la capacité du système répond à la demande ?

La planification de la capacité permet aux équipes de service d’affecter les ressources nécessaires à la prise en charge de la disponibilité du service Microsoft 365. Une planification régulière de la capacité est requise dans le cadre du programme EBCM de Microsoft. Les équipes de service examinent les données de capacité pendant les examens trimestriels, ainsi que les situations d’urgence qui justifient une révision de capacité supplémentaire.

Les données brutes pour la planification de la capacité sont conservées par chaque équipe de service et incluent des mesures telles que le traitement système, la mémoire et la capacité matérielle. Les révisions programmées utilisent un modèle de capacité actuelle du système et le testent par rapport aux besoins prévus dans les situations d’urgence. Si le modèle indique des écarts de capacité, les modifications proposées à la capacité du système sont soumises au leadership des équipes de maintenance pour examen. Les modifications approuvées sont incorporées dans un nouveau modèle avant leur implémentation par les ingénieurs d’équipe de service.

## <a name="how-does-microsoft-365-maintain-service-availability-during-routine-system-failures"></a>Comment maintenir la disponibilité Microsoft 365 service en cas de défaillances système de routine ?

Microsoft 365 une résilience de service par le biais d’une architecture redondante, d’une réplication des données et d’une vérification automatisée de l’intégrité. L’architecture redondante implique le déploiement de plusieurs instances d’un service sur du matériel géographiquement et physiquement distinct, offrant ainsi une tolérance de panne accrue pour Microsoft 365 services. La réplication des données garantit qu’il existe toujours plusieurs copies de données client dans différentes zones d’erreur, ce qui permet de récupérer des données client critiques en cas de corruption, de perte ou même de suppression accidentelle par le client. La vérification automatisée de l’intégrité augmente la disponibilité des données en restaurant automatiquement les données touchées par de nombreux types d’altération physique ou logique.

## <a name="related-external-regulations--certifications"></a>Réglementations externes associées & certifications

Les services en ligne de Microsoft sont régulièrement audités pour assurer la conformité avec les réglementations et certifications externes. Reportez-vous au tableau suivant pour la validation des contrôles liés à la résilience et à la continuité.

| **Audits externes** | **Section** | **Date de rapport la plus récente** |
|:--------------------|:------------|:-----------------------|
| [FedRAMP (Office 365)](https://compliance.microsoft.com/compliancemanager) | CP-2 : plan d’urgence <br> CP-3 : Formation d’urgence <br> CP-4 : Test du plan d’urgence <br> CP-6 : autre site de stockage <br> CP-7 : Autre site de traitement <br> CP-9 : Sauvegarde du système d’information <br> CP-10 : récupération et reconstruction du système d’information | 24 septembre 2020 |
| [ISO 27001/27002 (Office 365)](https://servicetrust.microsoft.com/ViewPage/MSComplianceGuideV3?command=Download&downloadType=Document&downloadId=8d625374-4f2d-49f8-9d37-a4281ba98222&tab=7027ead0-3d6b-11e9-b9e1-290b1eb4cdeb&docTab=7027ead0-3d6b-11e9-b9e1-290b1eb4cdeb_ISO_Reports) <br><br> [Déclaration d’applicabilité](https://servicetrust.microsoft.com/ViewPage/MSComplianceGuideV3?command=Download&downloadType=Document&downloadId=c0df4ce8-c77e-4183-84eb-c8688470d8b1&tab=7027ead0-3d6b-11e9-b9e1-290b1eb4cdeb&docTab=7027ead0-3d6b-11e9-b9e1-290b1eb4cdeb_ISO_Reports) <br> [Certification](https://servicetrust.microsoft.com/ViewPage/MSComplianceGuideV3?command=Download&downloadType=Document&downloadId=1e84a14a-2468-45ac-9412-5e53250d57ec&tab=7027ead0-3d6b-11e9-b9e1-290b1eb4cdeb&docTab=7027ead0-3d6b-11e9-b9e1-290b1eb4cdeb_ISO_Reports) | A.17.1 : Continuité de la sécurité des informations <br> A.17.2 : Redondances | 20 avril 2021 |
| [ISO 22301 (Office 365)](https://servicetrust.microsoft.com/ViewPage/MSComplianceGuideV3?command=Download&downloadType=Document&downloadId=13951eb3-6339-4629-b80d-dd0d43812fe7&tab=7027ead0-3d6b-11e9-b9e1-290b1eb4cdeb&docTab=7027ead0-3d6b-11e9-b9e1-290b1eb4cdeb_ISO_Reports) <br><br> [Certification](https://servicetrust.microsoft.com/ViewPage/MSComplianceGuideV3?command=Download&downloadType=Document&downloadId=2bb29cc0-53e7-4a53-a9de-871316e1b80c&tab=7027ead0-3d6b-11e9-b9e1-290b1eb4cdeb&docTab=7027ead0-3d6b-11e9-b9e1-290b1eb4cdeb_ISO_Reports) | Tous les contrôles | 18 mars 2019 |
| [SOC 1 (Office 365)](https://servicetrust.microsoft.com/ViewPage/MSComplianceGuideV3?command=Download&downloadType=Document&downloadId=90df3f9c-3aaf-4dbf-99d0-ca9f2991721b&tab=7027ead0-3d6b-11e9-b9e1-290b1eb4cdeb&docTab=7027ead0-3d6b-11e9-b9e1-290b1eb4cdeb_SOC_%2F_SSAE_16_Reports) | CA-49 : Stratégies de sauvegarde <br> CA-50 : continuité d’activité <br> CA-51 : Réplication des données | 24 décembre 2020 |
| [SOC 2 (Office 365)](https://servicetrust.microsoft.com/ViewPage/MSComplianceGuideV3?command=Download&downloadType=Document&downloadId=a73c1738-7892-42b7-acd3-87b6371c53f6&tab=7027ead0-3d6b-11e9-b9e1-290b1eb4cdeb&docTab=7027ead0-3d6b-11e9-b9e1-290b1eb4cdeb_SOC_%2F_SSAE_16_Reports) | CA-49 : Stratégies de sauvegarde <br> CA-50 : continuité d’activité <br> CA-51 : Réplication des données | 24 décembre 2020 |
| [SOC 3 (Office 365)](https://servicetrust.microsoft.com/ViewPage/MSComplianceGuideV3?command=Download&downloadType=Document&downloadId=274054e5-4968-48d2-bf94-9a8eda5d7a93&tab=7027ead0-3d6b-11e9-b9e1-290b1eb4cdeb&docTab=7027ead0-3d6b-11e9-b9e1-290b1eb4cdeb_SOC_%2F_SSAE_16_Reports) | CUEC-09 : restauration de la messagerie EXO | 24 décembre 2020 |

## <a name="resources"></a>Ressources

- [Livre blanc Enterprise du programme de gestion de la continuité d’activité de Microsoft](https://servicetrust.microsoft.com/ViewPage/TrustDocumentsV3?command=Download&downloadType=Document&downloadId=64f922a6-d624-40dd-a8ae-6f996b5186f3&tab=7f51cb60-3d6c-11e9-b2af-7bb9f5d2d913&docTab=7f) 
- [Microsoft Cloud EBCM and Disaster Recovery Plan Validation Report: FY21 Q3](https://servicetrust.microsoft.com/ViewPage/TrustDocumentsV3?command=Download&downloadType=Document&downloadId=c072d11c-9cc9-42e1-b1cf-7281572fb1dd&tab=7f51cb60-3d6c-11e9-b2af-7bb9f5d2d913&docTab=7f51cb60-3d6c-11e9-b2af-7bb9f5d2d913_FAQ_and_White_Papers)

## <a name="legal-disclaimer"></a>Clause d’exclusion de responsabilité légale

- [Exclusion de responsabilité légale de continuité d’activité pour les entreprises](assurance-ebcm-legal-disclaimer.md)