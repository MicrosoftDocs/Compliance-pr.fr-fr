---
title: Contrôles système et d’organisation (SOC) 2 Type 2
description: Découvrez comment les services de cloud computing Microsoft sont conformes aux normes SOC (System and Organization Controls) 2 Type 2 pour la sécurité opérationnelle.
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
ms.openlocfilehash: c20ad27b244825e017d7545e669262ca61202b60
ms.sourcegitcommit: 9b0c8852e73e2be54a0f9c6570da67f4964f616c
ms.translationtype: HT
ms.contentlocale: fr-FR
ms.lasthandoff: 07/12/2021
ms.locfileid: "53385741"
---
# <a name="system-and-organization-controls-soc-2-type-2"></a>Contrôles système et d’organisation (SOC) 2 Type 2

## <a name="soc-2-type-2-overview"></a>Vue d’ensemble de SOC 2 Type 2

Les contrôles système et d’organisation (SOC) pour les organisations de services sont des rapports de contrôle interne créés par l’American Institute of Certified Public Accountants ( AICPA). Ils sont destinés à examiner les services fournis par une organisation de services afin que les utilisateurs finaux puissent évaluer et traiter les risques associés à un service externalisé.

Une attestation SOC 2 de type 2 est effectuée sous :

- SSAE No. 18, Normes d’attestation : Clarification et recodification, qui inclut la section 105 AT-C, *Concepts communs à tous les engagements d’attestation* et la section 205 AT-C, *Engagements d’examen* (AICPA, Normes professionnelles).
- Rapport SOC 2 sur un examen des contrôles au sein d’une organisation de service concernant la sécurité, la disponibilité, l’intégrité du traitement, la confidentialité ou la vie privée (Guide AICPA).
- Section 100 TSP, 2017 Critères de services de confidentialité pour la sécurité, disponibilité, intégrité de traitement, confidentialité et vie privée (AICPA, 2017 Trust Services Criteria).

En outre, le rapport d'attestation Office 365 SOC 2 de type 2 répond aux exigences énoncées dans la matrice des contrôles du Cloud (CCM) de la Cloud Security Alliance (CSA) et dans le catalogue des critères de conformité du Cloud Computing (C5:2020) créé par l'Office fédéral allemand de la sécurité de l'information (BSI).

Les attestations SOC 2 d’Office 365 sont basées sur des audits tiers indépendants rigoureux effectués par une société d’administration d’entreprise reconnue. À la fin d'un audit SOC 2, l'auditeur émet une opinion dans un rapport SOC 2 de type 2, qui décrit le système du fournisseur de services en nuage (FSC) et évalue la justesse de la description de ses contrôles par le FSC. Il évalue également si les contrôles du CSP sont conçus de manière adéquate, étaient en fonctionnement à une date spécifique et fonctionnaient efficacement sur une période donnée. Les rapports Office 365 SOC 2 de type 2 concernent la sécurité, la disponibilité, l'intégrité du traitement, la confidentialité et la vie privée du système.

## <a name="microsoft-in-scope-cloud-platforms--services"></a>Plateformes cloud et services Microsoft dans l’étendue

Les services en ligne Microsoft concernés sont indiqués dans le rapport d'attestation Azure SOC 2 Type 2 :

- Azure (pour obtenir des informations détaillées, consultez le rapport d’attestation [Offres de conformité Microsoft Azure](https://azure.microsoft.com/resources/microsoft-azure-compliance-offerings/) ou Azure SOC 2 De type 2)
- Azure DevOps (voir le rapport d'attestation distinct Azure DevOps SOC 2 Type 2)
- Dynamics 365 (pour obtenir des informations détaillées, consultez le rapport d’attestation de type 2 d’Azure SOC 2)
- Microsoft 365 Defender
- Microsoft Cloud App Security (MCAS)
- Microsoft Defender pour point de terminaison
- Microsoft Defender pour l’identité
- Microsoft Forms Pro (non inclus dans Azure Government)
- Microsoft Graph
- Microsoft Intune
- Microsoft Managed Desktop (non inclus dans Azure Government)
- Microsoft Stream
- Spécialistes des menaces Microsoft(non inclus dans Azure Government)
- Portail des nominations
- Office 365, Office 365 U.S. Government, Office 365 U.S. Government - Haut, Office 365 U.S. Government Defense
- Power Apps
- Power Automate
- Power BI
- Power Virtual Agents (non inclus dans Azure Government)
- Update Compliance (pas dans l’étendue de Azure Government)

## <a name="azure-dynamics-365-and-soc-2"></a>Azure, Dynamics 365 et SOC 2

Pour plus d’informations sur la conformité à Azure, Dynamics 365 et d’autres services de conformité en ligne, consultez [l’offre Azure SOC 2](/azure/compliance/offerings/offering-soc-2).

## <a name="office-365-and-soc-2"></a>Office 365 et SOC 2

### <a name="office-365-cloud-environments"></a>Environnements cloud Office 365

[!INCLUDE [Office 365 offering intro](../includes/o365-offering-introduction.md)]

### <a name="office-365-applicability-and-in-scope-services"></a>Applicabilité Office 365 et services dans l’étendue

Utilisez le tableau suivant pour déterminer l’applicabilité de vos services et abonnements Office 365 :

| **Applicabilité** | **Services dans l’étendue** |
|:------------------|:----------------------|
| **Office 365** | Gestionnaire de conformité, Customer Lockbox, Delve, Exchange Online Protection, Exchange Online, Forms, Griffin, Identity Manager, Lockbox (Torus), Microsoft Teams, MyAnalytics, Portail client Office 365, Microservices Office 365 (y compris, mais sans s’y limiter, Kaizala, ObjectStore, Sway, PowerPoint Online Document Service, Service d’annotation de requête, School Synchronisation des données, Siphon, Speech, StaffHub, programme d’application eXtensible), Office Online, Office Services Infrastructure, OneDrive Entreprise , Planificateur, PowerApps, Power Automate, Power BI, Project Online, Chiffrement de service avec clé client, SharePoint Online, Skype Entreprise |
| **GCC** | Azure Active Directory, Gestionnaire de conformité, Delve, Exchange Online, Forms, Microsoft Defender pour Office 365, Microsoft Teams, MyAnalytics, module complémentaire Conformité avancée Office 365, Centre de sécurité et conformité Office 365, Office Online, Office Pro Plus, OneDrive Entreprise, Planificateur, PowerApps, Power Automate, Power BI, SharePoint Online, Skype Entreprise, Stream |
| **GCC High** | Azure Active Directory, Exchange Online, Forms, Microsoft Defender pour Office 365, Microsoft Teams, module complémentaire Conformité avancée Office 365, Centre de sécurité et conformité Office 365, Office Online, Office Pro Plus, OneDrive Entreprise, Planificateur, PowerApps, Power Automate, Power BI, SharePoint Online, Skype Entreprise |
| **DOD** | Azure Active Directory, Exchange Online, Forms, Microsoft Defender pour Office 365, Microsoft Teams, module complémentaire Conformité avancée Office 365, Centre de sécurité et conformité Office 365, Office Online, Office Pro Plus, OneDrive Entreprise, Planificateur, Power BI, SharePoint Online, Skype Entreprise |

### <a name="office-365-audit-reports"></a>Rapports d’audit Office 365

- [Office 365 Core : rapport SSAE 18 SOC 2](https://aka.ms/o365SOC-2)
- [Office 365 Microservices T1-SSAE 18 SOC2 Type I Rapport](https://aka.ms/o365-MS-SOC-2-type1)
- [Voir les lettres de crédit et les rapports d’audit supplémentaires](https://aka.ms/auditreports)

Vous devez disposer d’un abonnement ou d’un compte d’essai gratuit dans Office 365 ou [Office](https://azure.microsoft.com/global-infrastructure/government/request/) 365 U.S. Government pour télécharger les rapports d’attestation SOC 1 et SOC 2 et les lettres de pont si nécessaire.

### <a name="frequently-asked-questions"></a>Questions fréquemment posées

**À quelle fréquence les rapports SOC Office 365 sont-ils émis ?**

Les rapports SOC relatifs à Office 365 et autres services en ligne reposent sur une période de 12 mois glissants (période d’audit) avec de nouveaux rapports émis chaque semestre (les périodes se terminant le 31 mars et le 30 septembre). *Les lettres de pont* sont émises chaque trimestre pour couvrir la période de trois mois précédente. Par exemple, la lettre de janvier couvre le 1er octobre au 31 décembre, la lettre d’avril couvre le 1er janvier au 31 mars, la lettre de juillet couvre le 1er avril au 30 juin et la lettre d’octobre du 1er juillet au 30 septembre.

**Où puis-je obtenir la documentation d’audit SOC Office 365, y compris les lettres de pont ?**

Pour obtenir des liens vers la documentation d’audit, consultez la section rapport d’audit. Vous devez disposer d’un abonnement ou d’un compte d’essai gratuit dans Office 365 ou [Office](https://azure.microsoft.com/global-infrastructure/government/request/) 365 U.S. Government pour vous connecter. Vous pouvez ensuite télécharger des certificats d’audit, des rapports d’évaluation et d’autres documents applicables pour vous aider à respecter vos propres exigences réglementaires.

**Où puis-je trouver une évaluation de l’implémentation des contrôles CCM cloud Security Alliance ?**

L’audit Office 365 SOC 2 type 2 est basé sur les principes et critères d'approbation de services de l'AICPA (American Institute of Certified Public Accountants), notamment la sécurité, la disponibilité, la confidentialité, la vie privée et l'intégrité du traitement, ainsi que les critères de la matrice CCM de la Cloud Security Alliance (CSA). L’objectif est de répondre aux critères et exigences AICPA définis dans le CCM. L’audit Office 365 SOC 2 Type 2 intègre l’évaluation des contrôles CCM, comme requis par l’attestation CSA STAR. Pour plus d’informations, consultez le rapport d’attestation Office 365 SOC 2 type 2.

**Où puis-je voir les réponses de gestion aux exceptions notées ?**

Les réponses de gestion se trouvent vers la fin du rapport d’attestation SOC. Recherchez « Réponse de gestion » dans le document.

**Où puis-je voir les responsabilités des entités utilisateur ?**

Les responsabilités de l’entité utilisateur se trouvent à la fin du rapport d’attestation SOC. Recherchez « Responsabilités de l’entité utilisateur » dans le document.

### <a name="use-microsoft-compliance-manager-to-assess-your-risk"></a>Utilisez le Gestionnaire de Conformité Microsoft pour évaluer vos risques

[Le Gestionnaire de Conformité Microsoft](/microsoft-365/compliance/compliance-manager) est une fonctionnalité dans le [centre de conformité Microsoft 365](/microsoft-365/compliance/microsoft-365-compliance-center) pour vous aider à comprendre la position de la conformité de votre organisation et à prendre des mesures pour réduire les risques. Le Gestionnaire de Conformité offre un modèle Premium pour la création d’une évaluation de ce règlement. Recherchez le modèle sur la page **modèles d’évaluation** dans le Gestionnaire de Conformité. Découvrez comment [créer des évaluations dans le Gestionnaire de Conformité](/microsoft-365/compliance/compliance-manager-assessments).

### <a name="resources"></a>Ressources

- [Rapports d’audit du portail d’approbation de services](https://servicetrust.microsoft.com/ViewPage/MSComplianceGuideV3)
- [SOC AICPA pour les organisations de service](https://www.aicpa.org/interestareas/frc/assuranceadvisoryservices/socforserviceorganizations.html)
- [SSAE n° 18, Normes d’attestation : Clarification et recodification (normes professionnelles AICPA)](https://www.aicpa.org/Research/Standards/AuditAttest/DownloadableDocuments/SSAE_No_18.pdf)
- [Rapport SOC 2 sur l’examen des contrôles au sein d’une organisation de service relative à la sécurité, à la disponibilité, à l’intégrité du traitement, à la confidentialité ou à la vie privée (Guide AICPA)](https://future.aicpa.org/cpe-learning/publication/soc-2-reporting-on-an-examination-of-controls-at-a-service-organization-relevant-to-security-availability-processing-integrity-confidentiality-or-privacy-OPL) (disponible à l’achat)
- [TSP section 100 (AICPA, 2017 Trust Services Criteria)](https://www.aicpa.org/content/dam/aicpa/interestareas/frc/assuranceadvisoryservices/downloadabledocuments/trust-services-criteria.pdf)
