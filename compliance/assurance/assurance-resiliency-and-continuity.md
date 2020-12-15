---
title: Résistance et continuité
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
ms.openlocfilehash: 2cc3f35a9d109a1a84159de8d0518f58270e3fe9
ms.sourcegitcommit: 1dc97ae3f0511cb1a41565da56e725bbe0cb013c
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 12/14/2020
ms.locfileid: "49671179"
---
# <a name="resiliency-and-continuity-overview"></a>Vue d’ensemble de la résilience et de la continuité

## <a name="how-does-microsoft-ensure-business-continuity-in-the-case-of-a-disaster-or-other-threat-to-service-availability"></a>Comment Microsoft garantit-il la continuité des activités en cas de sinistre ou d’autres menaces pour la disponibilité des services ?

L’équipe de gestion de la continuité d’entreprise de Microsoft (EBCM) supervise les activités de gestion de la continuité d’activité et de récupération d’urgence entre les services Microsoft et les offres de Cloud. Les représentants des divisions Microsoft, tels que Microsoft 365, coordonnent avec l’équipe EBCM pour développer des plans de continuité des activités et valider la conformité aux exigences de continuité de l’activité.

Le cycle de vie du BCM est au cœur de notre méthodologie de gestion de la continuité des opérations (BCM). Ce processus en trois phases est conçu pour être adaptable de sorte qu’il puisse être implémenté par un grand nombre de modèles d’entreprise dans Microsoft. Il commence par une phase d' **évaluation** pour identifier les processus et objectifs critiques qui doivent être inclus dans le programme de continuité d’activité. La phase d’évaluation nécessite également une analyse de l’impact commercial (BIA). La phase de **Planification** se concentre sur le développement et l’implémentation de stratégies de résilience et de récupération, ainsi que sur leur documentation dans les plans de continuité de l’activité officiel. Enfin, la **validation des capacités** teste les plans de continuité d’activité et leurs implémentations pour vérifier l’efficacité et identifier les améliorations potentielles.

La stratégie de continuité d’activité de Microsoft 365 tire parti de la redondance du matériel, du réseau et du centre de ressources. La réplication des données entre centres de données offre une haute disponibilité et une grande fiabilité en cas d’incident catastrophique. Elle augmente également la résistance aux incidents banals, tels que les défaillances matérielles isolées ou la corruption des données.

## <a name="how-does-microsoft-test-business-continuity-and-disaster-recovery-plans"></a>Comment Microsoft teste-t-il les plans de continuité d’activité et de récupération d’urgence ?

La stratégie de gestion de la continuité d’entreprise de Microsoft (EBCM) prévoit que tous les plans de continuité d’activité et de récupération d’urgence de Microsoft doivent être testés, mis à jour et vérifiés annuellement. Les services Microsoft 365 testent les plans de continuité des activités au moins une fois par an pour les stratégies EBCM. Une fois que les rapports d’action sont créés et vérifiés pour validation, les résultats des tests et informent les mises à jour du plan en réponse aux problèmes découverts lors des tests.

Pour valider les stratégies de résilience et de récupération par rapport à divers incidents potentiels, le programme EBCM définit plusieurs catégories de scénarios de test affectant les personnes, les emplacements et les technologies. Le niveau de validation requis pour chaque service est basé sur la criticité du service, avec des services plus critiques recevant une validation plus rigoureuse. Chaque équipe de service Microsoft 365 teste son plan de continuité des activités conformément aux directives EBCM pour mesurer l’efficacité du plan et la préparation de l’équipe de service pour exécuter le plan.

Selon les directives EBCM, les évaluations annuelles des plans de continuité d’activité et la validation des capacités doivent avoir lieu dans les 12 mois suivant la dernière révision. La validation de la capacité doit inclure la révision de la documentation de prise en charge, telle que le BIA, afin de s’assurer qu’elle reste précise. Microsoft propose des résultats de validation de fonctionnalité pour les services de sélection Microsoft 365 disponibles auprès de nos clients via des rapports trimestriels.

## <a name="how-does-microsoft-365-ensure-system-capacity-meets-demand"></a>Comment Microsoft 365 garantit que la capacité du système répond à la demande ?

La planification de la capacité permet aux équipes de service d’affecter les ressources nécessaires à la prise en charge de la disponibilité du service Microsoft 365. La planification de capacité normale est requise dans le cadre du programme EBCM de Microsoft. Les équipes de service examinent les données de capacité pendant les examens trimestriels, ainsi que les situations d’urgence qui justifient une révision de capacité supplémentaire.

Les données brutes pour la planification de la capacité sont gérées par chaque équipe de service et incluent des métriques telles que le traitement du système, la mémoire et la capacité matérielle. Les révisions planifiées utilisent un modèle de la capacité actuelle du système et les testent par rapport aux besoins prévus dans les situations d’urgence. Si le modèle indique des écarts de capacité, les modifications proposées à la capacité du système sont soumises au leadership des équipes de maintenance pour examen. Les modifications approuvées sont incorporées dans un nouveau modèle avant leur implémentation par les ingénieurs d’équipe de service.

## <a name="how-does-microsoft-365-maintain-service-availability-during-routine-system-failures"></a>Comment Microsoft 365 maintient-t-il la disponibilité des services pendant les défaillances du système de routine ?

Microsoft 365 atteint la résilience de service via une architecture redondante, une réplication de données et un contrôle d’intégrité automatisé. L’architecture redondante implique le déploiement de plusieurs instances d’un service sur un matériel géographiquement et physiquement distinct, ce qui permet une tolérance de panne accrue pour les services Microsoft 365. La réplication des données permet de s’assurer qu’il y a toujours plusieurs copies des données des clients dans des zones d’erreur différentes, ce qui permet de récupérer les données client critiques si elles sont endommagées, perdues, voire accidentellement supprimées par le client. La vérification de l’intégrité automatisée augmente la disponibilité des données en restaurant automatiquement les données affectées par de nombreux types d’altération physique ou logique.

## <a name="related-external-regulations--certifications"></a>Certifications & des réglementations externes connexes

Les services en ligne de Microsoft sont régulièrement vérifiés pour la conformité aux réglementations et aux certifications externes. Reportez-vous au tableau suivant pour la validation des contrôles liés à la résilience et à la continuité.

| **Audits externes** | **Section** | **Date du dernier rapport** |
|:--------------------|:------------|:-----------------------|
| [FedRAMP (Office 365)](https://compliance.microsoft.com/compliancemanager) | CP-2 : plan d’urgence <br> CP-3 : formation aux mesures d’urgence <br> CP-4 : test du plan d’urgence <br> CP-6 : site de stockage de substitution <br> CP-7 : site de remplacement <br> CP-9 : sauvegarde du système d’information <br> CP-10 : récupération et reconstitution du système d’information | 24 septembre 2020 |
| [ISO 27001/27002 (Office 365)](https://servicetrust.microsoft.com/ViewPage/MSComplianceGuideV3?command=Download&downloadType=Document&downloadId=d7864d4f-e053-4cc4-a964-fa526d07c3be&tab=7027ead0-3d6b-11e9-b9e1-290b1eb4cdeb&docTab=7027ead0-3d6b-11e9-b9e1-290b1eb4cdeb_ISO_Reports) <br><br> [Déclaration de l’applicabilité](https://servicetrust.microsoft.com/ViewPage/MSComplianceGuide?command=Download&downloadType=Document&downloadId=8ee1e46b-2ada-4e7b-bb7d-4c55a8cb6fcd&docTab=4ce99610-c9c0-11e7-8c2c-f908a777fa4d_ISO_Reports) <br> [Certification](https://servicetrust.microsoft.com/ViewPage/MSComplianceGuideV3?command=Download&downloadType=Document&downloadId=1e84a14a-2468-45ac-9412-5e53250d57ec&tab=7027ead0-3d6b-11e9-b9e1-290b1eb4cdeb&docTab=7027ead0-3d6b-11e9-b9e1-290b1eb4cdeb_ISO_Reports) | A. 17.1 : continuité de la sécurité des informations <br> A. 17.2 : redondances | 22 février 2020 |
| [ISO 22301 (Office 365)](https://servicetrust.microsoft.com/ViewPage/MSComplianceGuideV3?command=Download&downloadType=Document&downloadId=13951eb3-6339-4629-b80d-dd0d43812fe7&tab=7027ead0-3d6b-11e9-b9e1-290b1eb4cdeb&docTab=7027ead0-3d6b-11e9-b9e1-290b1eb4cdeb_ISO_Reports) <br><br> [Certification](https://servicetrust.microsoft.com/ViewPage/MSComplianceGuideV3?command=Download&downloadType=Document&downloadId=2bb29cc0-53e7-4a53-a9de-871316e1b80c&tab=7027ead0-3d6b-11e9-b9e1-290b1eb4cdeb&docTab=7027ead0-3d6b-11e9-b9e1-290b1eb4cdeb_ISO_Reports) | Tous les contrôles | 18 mars 2019 |
| [SOC 1 (Office 365)](https://servicetrust.microsoft.com/ViewPage/MSComplianceGuideV3?command=Download&downloadType=Document&downloadId=b07c0f7b-6bd5-4544-8255-7a5f14bf914a&tab=7027ead0-3d6b-11e9-b9e1-290b1eb4cdeb&docTab=7027ead0-3d6b-11e9-b9e1-290b1eb4cdeb_SOC_/_SSAE_16_Reports) | CA-49 : stratégies de sauvegarde <br> CA-50 : continuité des activités <br> CA-51 : réplication des données | 30 septembre 2019 |
| [SOC 2 (Office 365)](https://servicetrust.microsoft.com/ViewPage/MSComplianceGuideV3?command=Download&downloadType=Document&downloadId=fa062990-e758-4ddc-ace3-7fb21a301d09&tab=7027ead0-3d6b-11e9-b9e1-290b1eb4cdeb&docTab=7027ead0-3d6b-11e9-b9e1-290b1eb4cdeb_SOC_/_SSAE_16_Rep-11e9-b9e1-290b1eb4cdeb_SOC_/_SSAE_16_Reports) | CA-49 : stratégies de sauvegarde <br> CA-50 : continuité des activités <br> CA-51 : réplication des données | 30 septembre 2019 |
| [SOC 3 (Office 365)](https://servicetrust.microsoft.com/ViewPage/MSComplianceGuideV3?command=Download&downloadType=Document&downloadId=9df8b99b-96ce-49a9-bff4-268031dcc9a6&tab=7027ead0-3d6b-11e9-b9e1-290b1eb4cdeb&docTab=7027ead0-3d6b-11e9-b9e1-290b1eb4cdeb_SOC_/_SSAE_16_Reports) | CUEC-09 : restauration de la messagerie EXO | 30 septembre 2019 |

## <a name="resources"></a>Ressources

- [Livre blanc sur le programme de gestion de la continuité d’entreprise Microsoft](https://servicetrust.microsoft.com/ViewPage/TrustDocumentsV3?command=Download&downloadType=Document&downloadId=64f922a6-d624-40dd-a8ae-6f996b5186f3&tab=7f51cb60-3d6c-11e9-b2af-7bb9f5d2d913&docTab=7f) 
- [Microsoft Cloud EBCM et le rapport de validation du plan de récupération d’urgence : FY21 Q1 et Q2](https://servicetrust.microsoft.com/ViewPage/TrustDocumentsV3?command=Download&downloadType=Document&downloadId=b4181ab3-b03d-4a62-b396-4bfd1c98ddb0&tab=7f51cb60-3d6c-11e9-b2af-7bb9f5d2d913&docTab=7f51cb60-3d6c-11e9-b2af-7bb9f5d2d913_FAQ_and_White_Papers)

## <a name="legal-disclaimer"></a>Clause d’exclusion de responsabilité légale

- [Exclusion de responsabilité légale de continuité d’activité pour les entreprises](assurance-ebcm-legal-disclaimer.md)