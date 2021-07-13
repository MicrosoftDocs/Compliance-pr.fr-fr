---
title: Département de la Défense (DoD) Impact Niveau 2 (IL2)
description: Découvrez comment Microsoft répond aux normes d’impact de niveau 2 (IL2) du département de la Défense (DoD).
keywords: Offres pour la conformité Microsoft 365
localization_priority: None
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
ms.openlocfilehash: 77e8cb50f815c167e50293d495b4a548a73d022e
ms.sourcegitcommit: 9b0c8852e73e2be54a0f9c6570da67f4964f616c
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 07/12/2021
ms.locfileid: "53385722"
---
# <a name="department-of-defense-dod-impact-level-2-il2"></a>Département de la Défense (DoD) Impact Niveau 2 (IL2)

## <a name="dod-il2-overview"></a>Vue d’ensemble de DoD IL2

La Defense Information Systems Agency (DISA) est une agence du département américain de la Défense (DoD) qui est responsable du développement et de la maintenance du Guide dod cloud computing [security requirements (SRG)](https://dl.dod.cyber.mil/wp-content/uploads/cloud/SRG/index.html). Le SRG définit les exigences de sécurité de base utilisées par DoD pour évaluer la posture de sécurité d’un fournisseur de services cloud (CSP), en appuyant la décision d’accorder une autorisation provisoire DoD (PA) qui permet à un fournisseur CSP d’héberger des missions DoD. Il incorpore, annule et annule le modèle CSM (DoD Cloud Security Model) publié précédemment et se mappe sur DoD Risk Management Framework (RMF).

DISA guide les agences et services DoD dans la planification et l’autorisation de l’utilisation d’un programme CSP. Il évalue également les offres de CSP pour la conformité avec le SRG, un processus d’autorisation dans lequel les CSP peuvent fournir de la documentation sur leur conformité aux normes DoD. Les autorisations provisoires DoD sont émises le cas échéant, de sorte que les agences DoD et les organisations de support peuvent utiliser les services cloud sans avoir à passer par un processus d’approbation complet, ce qui permet de gagner du temps et des efforts.

Le mémo DoD CIO du [15 décembre 2014](https://www.esi.mil/contentview.aspx?id=585) concernant les conseils mis à jour sur l’acquisition et l’utilisation des services cloud *computing* commerciaux indique que « FedRAMP servira de base de sécurité minimale pour tous les services cloud DoD ». Le SRG utilise la ligne de base modéré FedRAMP à tous les niveaux d’impact sur les informations (IL) et prend en compte la ligne de base élevée à certains niveaux.

La [section SRG 5.1.1](https://dl.dod.cyber.mil/wp-content/uploads/cloud/SRG/index.html#5SECURITYREQUIREMENTS) Utilisation dod des contrôles de sécurité *FedRAMP* indique que les informations IL2 peuvent être hébergées dans un CSP qui contient au minimum une pa modéré FedRAMP et une autorité de sécurité DoD Level 2, sous réserve de conformité avec les exigences de sécurité du personnel décrites à la section 5.6.2. Toutefois, cette approche ne permet pas au programme CSP de répondre aux autres exigences de sécurité et d’intégration requises par le propriétaire de la mission. Conformément à la [section SRG 5.2.2.1](https://dl.dod.cyber.mil/wp-content/uploads/cloud/SRG/index.html#5.2LegalConsiderations) IL2 Location *and Separation Requirements,* DoD IL2 PA est correctement couvert par une pa modéré FedRAMP de telle manière que les exigences ne seront pas évaluées en plus pour une pa IL2.

## <a name="microsoft-in-scope-cloud-platforms--services"></a>Plateformes cloud microsoft dans l’étendue & services

- Azure
- Dynamics 365
- Microsoft Cloud App Security
- Microsoft Defender pour point de terminaison
- Microsoft Graph
- Microsoft Intune
- Microsoft Stream
- Office 365 Gouvernement américain, Office 365 pour le gouvernement américain - Élevé
- Power Apps
- Power Automate
- Power BI

## <a name="azure-dynamics-365-and-dod-il2"></a>Azure, Dynamics 365 et DoD IL2

Pour plus d’informations sur Azure, Dynamics 365 et d’autres services en ligne, voir l’offre [Azure DoD IL2.](/azure/compliance/offerings/offering-dod-il2)

## <a name="office-365-and-dod-il2"></a>Office 365 et DoD IL2

### <a name="office-365-cloud-environments"></a>Office 365 cloud

[!INCLUDE [Office 365 offering intro](../includes/o365-offering-introduction.md)]

### <a name="office-365-applicability-and-in-scope-services"></a>Office 365 applicabilité et services dans l’étendue

Utilisez le tableau suivant pour déterminer l’applicabilité de vos services Office 365 et de votre abonnement :

| **Applicabilité** | **Services dans l’étendue** |
|:------------------|:----------------------|
| **GCC** | Service Informations sur les activités, services Bing, Delve, Exchange Online Protection, Exchange Online, Services intelligents, Microsoft Teams, portail client Office 365, Office Online, infrastructure de service Office, rapports d’utilisation Office, OneDrive Entreprise, carte de visite, SharePoint Online, Skype Entreprise, Windows Ink |
| **GCC High** | Service Informations sur les activités, services Bing, Delve, Exchange Online Protection, Exchange Online, Services intelligents, Microsoft Teams, portail client Office 365, Office Online, infrastructure de service Office, rapports d’utilisation Office, OneDrive Entreprise, carte de visite, SharePoint Online, Skype Entreprise, Windows Ink |

### <a name="resources"></a>Ressources

- [Solutions microsoft pour le gouvernement](https://www.microsoft.com/enterprise/government)
- [Guide des conditions requises pour la sécurité dans le Cloud Computing DoD](https://dl.dod.cyber.mil/wp-content/uploads/cloud/SRG/index.html)
- [Documents FedRAMP](https://www.fedramp.gov/documents/)
- [NIST SP 800-37](https://csrc.nist.gov/publications/detail/sp/800-37/rev-2/final) *Risk Management Framework for Information Systems and Organizations: A System Life-Cycle Approach for Security and Privacy*
- Contrôles de sécurité et de confidentialité [NIST SP 800-53](https://csrc.nist.gov/Projects/risk-management/sp800-53-controls/release-search#!/800-53) *pour les systèmes d’information et les organisations*
- [Instruction DoD 8510.01](https://www.esd.whs.mil/Portals/54/Documents/DD/issuances/dodi/851001p.pdf) *DoD Risk Management Framework (RMF) pour* les technologies de l’information DoD
