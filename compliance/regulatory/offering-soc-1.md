---
title: Contrôles système et d’organisation (SOC) 1 Type 2
description: Découvrez comment les services de cloud computing Microsoft sont conformes aux normes SOC (System and Organization Controls) 1 Type 2 pour la sécurité opérationnelle.
keywords: Microsoft 365, conformité, offres
localization_priority: Priority
ms.prod: microsoft-365-enterprise
ms.topic: article
f1.keywords:
- NOCSH
ms.author: robmazz
author: robmazz
manager: laurawi
audience: itpro
ms.collection:
- M365-security-compliance
- MS-Compliance
hideEdit: true
titleSuffix: Microsoft Compliance
ms.openlocfilehash: a3431b93e1c8f4b2705a0362114412aa4381143b
ms.sourcegitcommit: 9b0c8852e73e2be54a0f9c6570da67f4964f616c
ms.translationtype: HT
ms.contentlocale: fr-FR
ms.lasthandoff: 07/12/2021
ms.locfileid: "53385742"
---
# <a name="system-and-organization-controls-soc-1-type-2"></a>Contrôles système et d’organisation (SOC) 1 Type 2

## <a name="soc-1-type-2-overview"></a>Vue d’ensemble de SOC 1 Type 2

Les contrôles système et d’organisation (SOC) pour les organisations de services sont des rapports de contrôle interne créés par l’American Institute of Certified Public Accountants ( AICPA). Ils sont destinés à examiner les services fournis par une organisation de services afin que les utilisateurs finaux puissent évaluer et traiter les risques associés à un service externalisé.

Une attestation SOC 1 de type 2 est effectuée sous :

- SSAE No. 18, normes d’attestation : clarification and Recodification, qui inclut la section 320 AT-C, *Rapport sur l'examen des contrôles d'un organisme de services pertinents pour le contrôle interne des entités utilisatrices en matière de rapports financiers* (AICPA, Standards Professionels).
- Rapport SOC 1 sur l’examen des contrôles au sein d’une organisation de service pertinente pour le contrôle interne des entités utilisateur sur les rapports financiers (Guide AICPA).

Outre la déclaration AICPA sur les normes pour les engagements d’attestation 18 (SSAE 18), l’audit Office 365 SOC 1 Type 2 est effectué conformément à la norme internationale sur les engagements d’assurance No. 3402 (ISAE 3402). L’attestation SOC 1 a remplacé SAS 70, et il convient de créer des rapports sur les contrôles au sein d’une organisation de service qui concernent les entités utilisateur qui contrôlent en interne les rapports financiers. Un rapport de Type 2 inclut l’avis de l’auditeur sur l’efficacité du contrôle pour atteindre les objectifs de contrôle associés pendant la période de surveillance spécifiée.

## <a name="microsoft-in-scope-cloud-platforms--services"></a>Plateformes cloud et services Microsoft dans l’étendue

Les services en ligne Microsoft concernés sont indiqués dans le rapport d'attestation Azure SOC 1 Type 2 :

- Azure (pour obtenir des informations détaillées, consultez le rapport d’attestation [Offres de conformité Microsoft Azure](https://azure.microsoft.com/resources/microsoft-azure-compliance-offerings/) ou Azure SOC 1 de Type 2)
- Azure DevOps (voir le rapport d'attestation distinct Azure DevOps SOC 1 Type 2)
- Dynamics 365 (pour obtenir des informations détaillées, consultez le rapport d’attestation de Type 1 d’Azure SOC 2)
- Microsoft 365 Defender
- Microsoft Cloud App Security (MCAS)
- Microsoft Defender pour point de terminaison (anciennement Microsoft Protection avancée contre les menaces)
- Microsoft Defender pour Identity (anciennement Azure Protection avancée contre les menaces)
- Microsoft Forms Pro (non inclus dans Azure Government)
- Microsoft Graph
- Microsoft Intune
- Microsoft Managed Desktop (non inclus dans Azure Government)
- Microsoft Stream
- Spécialistes des menaces Microsoft (non inclus dans Azure Government)
- Portail des nominations
- Office 365, Office 365 U.S. Government, Office 365 U.S. Government - Haut, Office 365 U.S. Government Defense
- Power Apps
- Power Automate
- Power BI
- Power Virtual Agents (non inclus dans Azure Government)
- Update Compliance (pas dans l’étendue de Azure Government)

## <a name="azure-dynamics-365-and-soc-1"></a>Azure, Dynamics 365 et SOC 1

Pour plus d’informations sur la conformité à Azure, Dynamics 365 et d’autres services de conformité en ligne, consultez [l’offre Azure SOC 1](/azure/compliance/offerings/offering-soc-1).

## <a name="office-365-and-soc-1"></a>Office 365 et SOC 1

### <a name="office-365-cloud-environments"></a>Environnements cloud Office 365

[!INCLUDE [Office 365 offering intro](../includes/o365-offering-introduction.md)]

### <a name="office-365-applicability-and-in-scope-services"></a>Applicabilité Office 365 et services dans l’étendue

Utilisez le tableau suivant pour déterminer l’applicabilité de vos services et abonnements Office 365 :

| **Applicabilité** | **Services dans l’étendue** |
|:------------------|:----------------------|
| **Office 365** | Gestionnaire de conformité, Customer Lockbox, Delve, Exchange Online Protection, Exchange Online, Forms, Griffin, Identity Manager, Lockbox (Torus), Microsoft Teams, MyAnalytics, Portail client Office 365, Microservices Office 365 (y compris, mais sans s’y limiter, Kaizala, ObjectStore, Sway, PowerPoint Online Document Service, Service d’annotation de requête, School Synchronisation des données, Siphon, Speech, StaffHub, programme d’application eXtensible), Office Online, Office Services Infrastructure, OneDrive Entreprise , Planificateur, PowerApps, Power BI, Project Online, Chiffrement de service avec clé client, SharePoint Online, Skype Entreprise |
| **GCC** | Azure Active Directory, Gestionnaire de conformité, Delve, Exchange Online, Forms, Microsoft Defender pour Office 365, Microsoft Teams, MyAnalytics, module complémentaire Conformité avancée Office 365, Centre de sécurité et conformité Office 365, Office Online, Office Pro Plus, OneDrive Entreprise, Planificateur, PowerApps, Power Automate, Power BI, SharePoint Online, Skype Entreprise, Stream |
| **GCC High** | Azure Active Directory, Exchange Online, Forms, Microsoft Defender pour Office 365, Microsoft Teams, module complémentaire Conformité avancée Office 365, Centre de sécurité et conformité Office 365, Office Online, Office Pro Plus, OneDrive Entreprise, Planificateur, PowerApps, Power Automate, Power BI, SharePoint Online, Skype Entreprise |
| **DOD** | Azure Active Directory, Exchange Online, Forms, Microsoft Defender pour Office 365, Microsoft Teams, module complémentaire Conformité avancée Office 365, Centre de sécurité et conformité Office 365, Office Online, Office Pro Plus, OneDrive Entreprise, Planificateur, Power BI, SharePoint Online, Skype Entreprise |

### <a name="office-365-audit-reports"></a>Rapports d'activité Office 365

- [Office 365 Core : rapport SSAE 18 SOC 1](https://aka.ms/o365SOC-1)
- Voir les lettres de pont et les rapports d’audit supplémentaires

Vous devez disposer d’un abonnement ou d’un compte d’essai gratuit dans Office 365 ou Office 365 U.S. Government pour télécharger les rapports d’attestation SOC 1 et SOC 2 et les lettres de pont si nécessaire.

### <a name="frequently-asked-questions"></a>Questions fréquemment posées

**À quelle fréquence les rapports SOC Office 365 sont-ils émis ?**

Les rapports SOC relatifs à Office 365 et autres services en ligne reposent sur une période de 12 mois glissants (période d’audit) avec de nouveaux rapports émis chaque semestre (les périodes se terminant le 31 mars et le 30 septembre). *Les lettres de pont* sont émises chaque trimestre pour couvrir la période de trois mois précédente. Par exemple, la lettre de janvier couvre le 1er octobre au 31 décembre, la lettre d’avril couvre le 1er janvier au 31 mars, la lettre de juillet couvre le 1er avril au 30 juin et la lettre d’octobre du 1er juillet au 30 septembre.

**Comment les clients peuvent-ils bénéficier de l’attestation office 365 SOC 1 de Type 2 ?**

Les clients peuvent utiliser l’attestation Office 365 SOC 1 de Type 2 pour répondre à leurs propres exigences de conformité propres au secteur financier, telles que Sarbanes-Oxley (SOX), Federal Financial Institutions Examination Council (FFIEC), Gramm-Leach-Bliley Act (GLBA), etc.

**Où puis-je obtenir la documentation d’audit SOC Office 365, y compris les lettres de pont ?**

Pour obtenir des liens vers la documentation d’audit, consultez la section rapport d’audit. Vous devez disposer d’un abonnement ou d’un compte d’essai gratuit dans Office 365 ou Office 365 U.S. Government pour vous connecter. Vous pouvez ensuite télécharger des certificats d’audit, des rapports d’évaluation et d’autres documents applicables pour vous aider à respecter vos propres exigences réglementaires.

**Où puis-je voir les réponses de gestion aux exceptions notées ?**

Les réponses de gestion se trouvent vers la fin du rapport d’attestation SOC. Recherchez « Réponse de gestion » dans le document.

**Où puis-je voir les responsabilités des entités utilisateur ?**

Les responsabilités de l’entité utilisateur se trouvent à la fin du rapport d’attestation SOC. Recherchez « Responsabilités de l’entité utilisateur » dans le document.

### <a name="use-microsoft-compliance-manager-to-assess-your-risk"></a>Utilisez le Gestionnaire de Conformité Microsoft pour évaluer vos risques

[Le Gestionnaire de Conformité Microsoft](/microsoft-365/compliance/compliance-manager) est une fonctionnalité dans le [centre de conformité Microsoft 365](/microsoft-365/compliance/microsoft-365-compliance-center) pour vous aider à comprendre la position de la conformité de votre organisation et à prendre des mesures pour réduire les risques. Le Gestionnaire de Conformité offre un modèle Premium pour la création d’une évaluation de ce règlement. Recherchez le modèle sur la page **modèles d’évaluation** dans le Gestionnaire de Conformité. Découvrez comment [créer des évaluations dans le Gestionnaire de Conformité](/microsoft-365/compliance/compliance-manager-assessments).

### <a name="resources"></a>Ressources

- [Rapports d’audit du portail d’approbation de services](https://servicetrust.microsoft.com/ViewPage/MSComplianceGuideV3)
- [SSAE n° 18, Normes d’attestation : Clarification et recodification](https://www.aicpa.org/Research/Standards/AuditAttest/DownloadableDocuments/SSAE_No_18.pdf)
- [Rapport SOC 1 sur l’examen des contrôles au sein d’une organisation de service pertinente pour le contrôle interne des entités utilisateur sur les rapports financiers (Guide AICPA)](https://future.aicpa.org/cpe-learning/publication/reporting-on-an-examination-of-controls-at-a-service-organization-relevant-to-user-entities-internal-control-over-financial-reporting-soc-1-guide-OPL)(disponible à la vente).
