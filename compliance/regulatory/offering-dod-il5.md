---
title: Impact sur le Niveau d’impact 5 (IL5) du département de la Défense (DoD)
description: Découvrez comment Microsoft répond aux normes d’impact de niveau 5 (IL5) du département de la Défense (DoD).
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
ms.openlocfilehash: 9f92ed19a22b7eff8a7e9988e66c51aea90d42ab
ms.sourcegitcommit: 9b0c8852e73e2be54a0f9c6570da67f4964f616c
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 07/12/2021
ms.locfileid: "53385729"
---
# <a name="department-of-defense-dod-impact-level-5-il5"></a>Impact sur le Niveau d’impact 5 (IL5) du département de la Défense (DoD)

## <a name="dod-il5-overview"></a>Vue d’ensemble de DoD IL5

La Defense Information Systems Agency (DISA) est une agence du département américain de la Défense (DoD) qui est responsable du développement et de la maintenance du Guide dod cloud computing [security requirements (SRG)](https://dl.dod.cyber.mil/wp-content/uploads/cloud/SRG/index.html). Le SRG définit les exigences de sécurité de base utilisées par DoD pour évaluer la posture de sécurité d’un fournisseur de services cloud (CSP), en appuyant la décision d’accorder une autorisation provisoire DoD (PA) qui permet à un fournisseur CSP d’héberger des missions DoD. Il incorpore, annule et annule le modèle CSM (DoD Cloud Security Model) publié précédemment et se mappe sur DoD Risk Management Framework (RMF).

DISA guide les agences et services DoD dans la planification et l’autorisation de l’utilisation d’un programme CSP. Il évalue également les offres de CSP pour la conformité avec le SRG, un processus d’autorisation dans lequel les CSP peuvent fournir de la documentation sur leur conformité aux normes DoD. Les autorisations provisoires DoD sont émises le cas échéant, de sorte que les agences DoD et les organisations de support peuvent utiliser les services cloud sans avoir à passer par un processus d’approbation complet, ce qui permet de gagner du temps et des efforts.

Conformément aux niveaux *d’impact* sur les informations de [la section 3.2 du SRG,](https://dl.dod.cyber.mil/wp-content/uploads/cloud/SRG/index.html#3.2InformationImpactLevels) IL5 couvre les informations suivantes :

- Informations non classifiées contrôlées (CUI) nécessitant un niveau de protection supérieur à celui d’IL4
    - Le Registre de l’interface utilisateur de la [CUI](https://www.archives.gov/cui) fournit des catégories spécifiques d’informations qui sont protégées par le pouvoir exécutif, par exemple, plus de 20 regroupements de catégories sont inclus dans la liste des catégories de l’interface [utilisateur utilisateur.](https://www.archives.gov/cui/registry/category-list)
    - [NIST SP 800-171](https://csrc.nist.gov/publications/detail/sp/800-171/rev-2/final) *Protecting Controlled Unclassified Information in Nonfederal Systems and Organizations* is intended to use by federal agencies in contracts or other agreements established with non-federal organizations.

- Systèmes de sécurité nationaux (NSS)
    - [La directive NIST SP 800-59](https://nvlpubs.nist.gov/nistpubs/Legacy/SP/nistspecialpublication800-59.pdf) pour l’identification d’un système *d’information* en tant que système de sécurité national fournit des définitions de NSS.
    - [CnSSI 1253](https://www.dcsa.mil/portals/91/documents/ctp/nao/CNSSI_No1253.pdf) Security *Categorization and Control Selection for National Security Systems* provides guidance on the security standards that federal agencies should apply to categorize national security information.

Le mémo DoD CIO du [15 décembre 2014](https://www.esi.mil/contentview.aspx?id=585) concernant les conseils mis à jour sur l’acquisition et l’utilisation des services cloud *computing* commerciaux indique que « FedRAMP servira de base de sécurité minimale pour tous les services cloud DoD ». Le SRG utilise la ligne de base modéré FedRAMP à tous les niveaux d’impact sur les informations (IL) et prend en compte la ligne de base élevée à certains niveaux.

La [section SRG 5.1.1](https://dl.dod.cyber.mil/wp-content/uploads/cloud/SRG/index.html#5SECURITYREQUIREMENTS) Utilisation dod des contrôles de sécurité *FedRAMP* indique qu’une autorité de sécurité FedRAMP Haute pa, complétée par les contrôles DoD FedRAMP+ et les améliorations de contrôle (C/CEs) et les exigences dans le SRG, sont utilisées pour évaluer les CSP en vue de l’attribution d’une pa DoD pa à IL5. Quelle que soit la référence C/CE utilisée comme base pour une pa pa élevée FedRAMP, des considérations supplémentaires et/ou des exigences doivent être évaluées et approuvées pour qu’une autorité de configuration DoD puisse être attribuée à IL5. Plus précisément, la [section SRG 5.1.2](https://dl.dod.cyber.mil/wp-content/uploads/cloud/SRG/index.html#5SECURITYREQUIREMENTS) *DoD FedRAMP+ Security Controls/Enhancements* indique dans le tableau 2 que 10 C/CEs supplémentaires au-delà de la ligne de base FedRAMP High sont requises pour une autorité de configuration DoD IL5.

En outre, conformément à la [section 5.2.2.3](https://dl.dod.cyber.mil/wp-content/uploads/cloud/SRG/index.html#5.2LegalConsiderations) *IL5 et* aux exigences de séparation des espaces, les conditions suivantes (entre autres) doivent être en place pour une autorité de sécurité de niveau 5 :

- La séparation virtuelle/logique entre les locataires/missions DoD et le gouvernement fédéral est suffisante. Une séparation virtuelle/logique entre les systèmes client/mission est requise.
- La séparation physique des locataires non DoD/non fédéraux (c’est-à-dire, les locataires publics, locaux/publics) est requise.
- Le programme CSP limite l’accès potentiel aux données de DoD et des informations de la communauté aux employés des CSP qui sont citoyens américains.

## <a name="microsoft-in-scope-cloud-platforms--services"></a>Plateformes cloud microsoft dans l’étendue & services

- Azure
- Service clientèle Dynamics 365
- Microsoft Defender pour le point de terminaison (anciennement Microsoft Defender - Protection avancée contre les menaces)
- Microsoft Graph
- Microsoft Stream
- Office 365 U.S. Government Defense
- Power Automate (anciennement Microsoft Flow)
- Power BI

## <a name="azure-dynamics-365-and-dod-il5"></a>Azure, Dynamics 365 et DoD IL5

Pour plus d’informations sur Azure, Dynamics 365 et d’autres services en ligne, voir l’offre [Azure DoD IL5.](/azure/compliance/offerings/offering-dod-il5)

## <a name="office-365-and-dod-il5"></a>Office 365 et DoD IL5

### <a name="office-365-cloud-environments"></a>Office 365 cloud

[!INCLUDE [Office 365 offering intro](../includes/o365-offering-introduction.md)]

### <a name="office-365-applicability-and-in-scope-services"></a>Office 365 applicabilité et services dans l’étendue

Utilisez le tableau suivant pour déterminer l’applicabilité de vos services Office 365 et de votre abonnement :

| **Applicabilité** | **Services dans l’étendue** |
|:------------------|:----------------------|
| **DOD** | Service informations sur les activités, services Bing, Exchange Online, Exchange Online Protection, services intelligents, Microsoft Teams, portail client Office 365, Office Online, infrastructure de service Office, rapports d’utilisation Office, OneDrive Entreprise, carte de visite, SharePoint Online, Skype Entreprise, Windows Ink |

### <a name="attestation-documents"></a>Documents d’attestation

Les clients du gouvernement américain peuvent demander Office 365 documentation FedRAMP pour le gouvernement américain Defense FedRAMP directement à partir de [FedRAMP Marketplace](https://marketplace.fedramp.gov/#!/products?sort=productName&productNameSearch=azure) en envoyant un formulaire de demande d’accès au package. Vous devez avoir une adresse de messagerie .gov ou .pack pour accéder à un package de sécurité FedRAMP directement à partir de FedRAMP.

Sélectionnez la documentation FedRAMP et DoD, y compris le Plan de sécurité système (SSP), les rapports de surveillance continue, le plan d’action et les jalons (POA M), etc., est disponible pour les clients sous NDA et en attente d’autorisation d’accès à partir de la section Rapports d’audit du portail d’approbation de services \& [- Rapports FedRAMP.](https://servicetrust.microsoft.com/ViewPage/MSComplianceGuideV3) Contactez votre représentant de compte Microsoft pour obtenir de l’aide.

### <a name="resources"></a>Ressources

- [Solutions microsoft pour le gouvernement](https://www.microsoft.com/enterprise/government)
- [Guide des conditions requises pour la sécurité dans le Cloud Computing DoD](https://dl.dod.cyber.mil/wp-content/uploads/cloud/SRG/index.html)
- [Documents FedRAMP](https://www.fedramp.gov/documents/)
- [Instruction DoD 8510.01](https://www.esd.whs.mil/Portals/54/Documents/DD/issuances/dodi/851001p.pdf) *DoD Risk Management Framework (RMF) pour* les technologies de l’information DoD
- [NIST SP 800-37](https://csrc.nist.gov/publications/detail/sp/800-37/rev-2/final) *Risk Management Framework for Information Systems and Organizations: A System Life-Cycle Approach for Security and Privacy*
- Contrôles de sécurité et de confidentialité [NIST SP 800-53](https://csrc.nist.gov/Projects/risk-management/sp800-53-controls/release-search#!/800-53) *pour les systèmes d’information et les organisations*
- [Recommandations NIST SP 800-59 pour](https://nvlpubs.nist.gov/nistpubs/Legacy/SP/nistspecialpublication800-59.pdf) l’identification d’un système *d’information en tant que système de sécurité national*
- Catégorisation et sélection des contrôles [CNSSI 1253](https://www.dcsa.mil/portals/91/documents/ctp/nao/CNSSI_No1253.pdf) pour les *systèmes de sécurité nationaux*
- [NIST SP 800-171](https://csrc.nist.gov/publications/detail/sp/800-171/rev-2/final) *Protecting Controlled Unclassified Information in Nonfederal Systems and Organizations*
- Controlled Unclassified Information (CUI) [Registry](https://www.archives.gov/cui) and CUI [category list](https://www.archives.gov/cui/registry/category-list).
