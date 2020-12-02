---
title: Attestation CSA (Cloud Security Alliance) STAR
description: Azure et Intune ont obtenu l’attestation CSA (Cloud Security Alliance) STAR basée sur un audit indépendant.
keywords: Offres pour la conformité Microsoft 365
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
ms.openlocfilehash: 3eb2343767911c7844bf9e9c27ef41a4c4e30952
ms.sourcegitcommit: 626b0076d133e588cd28598c149a7f272fc18bae
ms.translationtype: HT
ms.contentlocale: fr-FR
ms.lasthandoff: 11/30/2020
ms.locfileid: "49507657"
---
# <a name="cloud-security-alliance-csa-star-attestation"></a>Attestation CSA (Cloud Security Alliance) STAR

## <a name="csa-star-attestation-overview"></a>Présentation de l’attestation CSA STAR

La Cloud Security Alliance (CSA) tient à jour le registre STAR (Security, Trust &amp; Assurance Registry), un registre gratuit et public dans lequel les fournisseurs de services Cloud (CSP) peuvent publier leurs évaluations relatives à la CSA. Le registre STAR se compose de trois niveaux d'assurance alignés sur les objectifs de contrôle de la matrice CCM (Cloud Controls Matrix). (La matrice CCM englobe les principes de sécurité fondamentaux en 16 domaines et permettant aux clients cloud d'évaluer le risque de sécurité global d'un service cloud.) :

- Niveau 1 : Auto-évaluation STAR
- Niveau 2 : Attestation STAR, Certification STAR et Évaluation C-STAR (basées sur des audits tiers)
- Niveau 3 : Surveillance continue STAR (les exigences du programme sont toujours en cours d’élaboration par la CSA)

L'Attestation STAR implique un audit indépendant rigoureux de la situation de sécurité du fournisseur de cloud basé sur un audit SOC 2 de type 2 avec les critères de CCM. L'auditeur indépendant qui évalue les offres d'un fournisseur de cloud pour une Attestation STAR doit être un comptable public certifié (CPA) et doit disposer du certificat de la CSA en Cloud Security Knowledge (CCSK).  
  
Un audit SOC 2 type 2 est basé sur les principes et critères d'approbation de services de l'AICPA (American Institute of Certified Public Accountants), notamment la sécurité, la disponibilité, la confidentialité et l'intégrité du traitement, ainsi que les critères de la matrice CCM. L’attestation STAR fournit les résultats d’un auditeur concernant les possibilités de conception et l’efficacité du fonctionnement des contrôles SOC 2 dans les services cloud Microsoft. L’objectif consiste à satisfaire les critères de l’AICPA mentionnés ci-dessus et les exigences figurant dans la matrice CCM.

## <a name="microsoft-in-scope-cloud-services"></a>Services Cloud Microsoft dans le périmètre

Microsoft Azure et Microsoft Intune ont obtenu l’attestation CSA STAR. L’attestation STAR fournit les résultats d’un auditeur concernant les possibilités de conception et l’efficacité du fonctionnement des contrôles SOC 2 dans les services cloud Microsoft.

- [Azure et Azure Government](https://aka.ms/AzureCompliance)
- [Azure Germany](https://aka.ms/AzureCompliance)
- Microsoft Cloud App Security
- Microsoft Graph
- Intune
- Bureau géré Microsoft
- Service Cloud Power Automate (anciennement Microsoft Flow), soit en service autonome, soit inclus dans un plan ou une suite Office 365 ou Dynamics 365
- Service Cloud PowerApps, soit en service autonome, soit inclus dans un plan ou une suite Office 365 ou Dynamics 365 
- Power BI

## <a name="audits-reports-and-certificates"></a>Audits, rapports et certificats

- [Attestation et certification CSA STAR](https://cloudsecurityalliance.org/star/registry/microsoft/)

## <a name="frequently-asked-questions"></a>Questions fréquentes (FAQ)

**Sur quelles normes du secteur la CSA CCM est-elle alignée ?**

La matrice CCM correspond aux normes, réglementations et cadres de contrôle de sécurité acceptés par le secteur, tels que ISO/IEC 27001, PCI DSS, HIPAA, AICPA SOC 2, NERC CIP, FedRAMP, NIST, et plus encore. Pour obtenir la liste la plus récente, consultez le [site Web de la CSA](https://cloudsecurityalliance.org/).

**Où puis-je consulter l’attestation CSA STAR pour les services de cloud computing Microsoft ?**

Vous pouvez télécharger l’[attestation CSA STAR](https://aka.ms/CSASTAR-Attestation) pour Azure, qui couvre également Intune, dans le registre de la CSA.

**À quels niveaux d’assurance CSA STAR les services Entreprise Cloud de Microsoft se situent-ils ?**

- **Niveau 1** : **Auto-évaluation CSA STAR** : Azure, Microsoft Dynamics 365 et Microsoft Office 365. L'[autoévaluation](offering-csa-star-self-assessment.md) est une offre gratuite des fournisseurs de service cloud pour documenter leurs contrôles de sécurité afin d'aider les clients à évaluer la sécurité du service.
- **Niveau 2** : **Certification CSA STAR** : Azure, Microsoft Cloud App Security, Intune et Microsoft Power BI. La certification STAR est basée sur l'obtention de la certification ISO/IEC 27001 et la satisfaction des critères spécifiés dans la matrice CCM. Elle est attribuée après une évaluation tierce rigoureuse des contrôles et pratiques de sécurité d'un fournisseur de service cloud.
- **Niveau 2** : **Attestation CSA STAR** : Azure et Intune. La CSA et l'AICPA ont collaboré pour fournir des directives à l'ACP à utiliser lors de missions SOC 2, à l'aide des critères de l'AICPA (principes d'approbation de services, AT 101) et de la CSA CCM. L’[attestation STAR](offering-CSA-STAR-Attestation.md) est basée sur ces directives et est attribuée après des évaluations indépendantes rigoureuses des fournisseurs de Cloud.

## <a name="use-microsoft-compliance-manager-to-assess-your-risk"></a>Utilisez le gestionnaire de conformité de Microsoft pour évaluer votre risque

Le [Gestionnaire de conformité Microsoft](https://docs.microsoft.com/microsoft-365/compliance/compliance-manager) est une fonctionnalité du [Centre de conformité Microsoft 365](https://docs.microsoft.com/microsoft-365/compliance/microsoft-365-compliance-center) qui vous permet de comprendre l’état de conformité de votre organisation et de prendre des mesures pour réduire les risques. Le Gestionnaire de conformité propose un modèle premium pour créer une évaluation pour ce règlement. Recherchez le modèle dans la page des **modèles d’évaluation** dans le Gestionnaire de conformité. Découvrez comment [créer des évaluations dans le Gestionnaire de conformité](https://docs.microsoft.com/microsoft-365/compliance/compliance-manager-assessments).

## <a name="resources"></a>Ressources

- [Réponse standard Azure pour la demande d’informations](https://aka.ms/AzureStandardRequestForInformation)
- [CAIQ Cloud Security Alliance Azure](https://aka.ms/AzureCSACAIQ)
- [Mappage de la matrice de contrôle du cloud de CSA Office 365](https://aka.ms/Office365CSACloudControlMatrix)
- [Cloud Security Alliance](https://cloudsecurityalliance.org/)
- [CSA Security, Trust & Assurance Registry (STAR)](https://cloudsecurityalliance.org/star/)
- [Rapports SOC 1, 2 et 3](offering-soc.md)
- [Cloud Controls Matrix (CCM)](https://cloudsecurityalliance.org/group/cloud-controls-matrix/)
- [Infrastructure de conformité Microsoft Common Controls Hub](https://www.microsoft.com/trust-center/compliance/compliance-overview)
- [Conformité sur le site Microsoft Trust Center](https://www.microsoft.com/trust-center/compliance/compliance-overview)
