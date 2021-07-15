---
title: ISO/IEC 27017:2015 Code de pratique international des contrôles de sécurité des informations
description: Les services Cloud Microsoft ont mis en œuvre ce code de pratique pour les contrôles de sécurité des informations.
keywords: Offres pour la conformité Microsoft 365
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
ms.openlocfilehash: 6c431d856fc03f328148722c14dfc558082aacb5
ms.sourcegitcommit: 9b0c8852e73e2be54a0f9c6570da67f4964f616c
ms.translationtype: HT
ms.contentlocale: fr-FR
ms.lasthandoff: 07/12/2021
ms.locfileid: "53384724"
---
# <a name="isoiec-270172015-code-of-practice-for-information-security-controls"></a>ISO/IEC 27017:2015 Code de pratique international des contrôles de sécurité des informations

## <a name="iso-iec-27017-overview"></a>Présentation d’ISO-IEC 27017

Le code de pratique ISO/IEC 27017:2015 est conçu comme une référence permettant aux entreprises de sélectionner les contrôles de sécurité des informations des services Cloud lors de la mise en œuvre d’un système de gestion de la sécurité des informations de Cloud computing basé sur la norme ISO/IEC 27002:2013. Il peut être également utilisé par les fournisseurs de services cloud comme document de référence pour l'implémentation des contrôles de protection communément admis.

Cette norme internationale fournit des conseils d'implémentation supplémentaires spécifiques au cloud basés sur la norme ISO/IEC 27002, et fournit des contrôles supplémentaires pour traiter les menaces et les risques de sécurité des informations spécifiques au cloud conformément aux clauses 5-18 de la norme ISO/IEC 27002: 2013 pour les contrôles, les conseils d'implémentation, ainsi que d'autres informations. Plus précisément, cette norme fournit des conseils sur les 37 contrôles de la norme ISO/IEC 27002 et contient également 7 nouveaux contrôles non dupliqués dans la norme ISO/IEC 27002. Ces nouvelles commandes traitent des aspects importants suivants :

- Rôles et responsabilités partagés dans un environnement de cloud computing
- Retrait et restitution des biens des clients des services cloud à la fin du contrat
- Protection et séparation de l’environnement virtuel d'un client de celui des autres clients
- Durcissement des exigences des machines virtuelles pour répondre aux besoins des entreprises
- Procédures pour les opérations administratives d'un environnement de cloud computing
- Possibilité donnée aux clients de surveiller les activités pertinentes dans un environnement de cloud computing
- Alignement de la gestion de la sécurité pour les réseaux virtuels et physiques

## <a name="microsoft-and-isoiec-27017"></a>Microsoft et la norme ISO/IEC 27017

La norme ISO/IEC 27017 est la seule à fournir des conseils à la fois aux fournisseurs et aux clients des services Cloud. Elle fournit également aux clients des services cloud des informatiques pratiques sur ce à quoi ils doivent s'attendre de la part des fournisseurs de services cloud. Les clients peuvent tirer parti directement de la norme ISO/IEC 27017 en s’assurant qu’ils ont bien compris les responsabilités partagées dans le Cloud.

## <a name="microsoft-in-scope-cloud-platforms--services"></a>Plateformes et services du cloud computing de Microsoft dans le champ d’application

- [Azure, Azure Gouvernement et Azure Allemagne](https://aka.ms/AzureCompliance)
- Microsoft Cloud App Security
- [Dynamics 365, Dynamics 365 et Dynamics 365 Allemagne](https://aka.ms/d365-compliance-list)
- Intune
- Microsoft Defender pour point de terminaison
- Microsoft Graph
- Microsoft Healthcare Bot
- [Microsoft Managed Desktop](/microsoft-365/managed-desktop/intro/compliance)
- Office 365, Office 365 U.S. Government, Office 365 U.S. Government Defense et Office 365 Allemagne
- Service Cloud Power Automate (anciennement Microsoft Flow), soit en service autonome, soit inclus dans un plan ou une suite Office 365 ou Dynamics 365
- Service Cloud PowerApps, soit en service autonome, soit inclus dans un plan ou une suite Office 365 ou Dynamics 365
- Service Cloud Power BI soit en service autonome, soit inclus dans un plan ou une suite Office 365
- Power BI intégré

## <a name="azure-dynamics-365-and-iso-270172015"></a>Azure, Dynamics 365 et ISO 27017:2015

Pour plus d’informations sur la conformité à Azure, Dynamics 365 et d’autres services en ligne, consultez [l’offre ISO/IEC 27017 Azure](/azure/compliance/offerings/offering-iso-27017).

## <a name="office-365-and-iso-270172015"></a>Office 365 et ISO 27017:2015

### <a name="office-365-cloud-environments"></a>Office 365 dans le cloud

[!INCLUDE [Office 365 offering intro](../includes/o365-offering-introduction.md)]

### <a name="office-365-applicability-and-in-scope-services"></a>L’applicabilité d’Office 365 et des services dans l’étendue

Utilisez le tableau suivant pour déterminer l’applicabilité de vos services et abonnements Office 365 :

| **L’applicabilité** | **Les Services dans l’étendue** |
|:------------------|:----------------------|
| **Office 365** | Access Online, Azure Active Directory, Azure Communications Service, Gestionnaire de conformité, Customer Lockbox, Delve, Exchange Online Protection, Exchange Online, Forms, Windows, Identity Manager, Lockbox (Torus), Microsoft Defender pour Office 365, Microsoft Teams, MyAnalytics, Module complémentaire Conformité avancée Office 365, Portail client Office 365, Microservices Office 365 (y compris mais non limité à Kaizala, ObjectStore, Sway, Service de document Power Automate, PowerPoint Online , Service d’annotation de requête, Synchronisation des données scolaires, Siphon, Speech, StaffHub, Programme d’application eXtensible), Office 365 Centre de sécurité et de conformité, Office Online, Office Pro Plus, Infrastructure office Services, OneDrive Entreprise, Planificateur, PowerApps, Power BI, Project Online, Chiffrement de service avec clé client, SharePoint Online, Skype Entreprise, Stream |
| **GCC** | Azure Active Directory, Azure Communications Service, Gestionnaire de conformité, Delve, Exchange Online, Forms, Microsoft Defender pour Office 365, Microsoft Teams, MyAnalytics, module complémentaire Conformité avancée Office 365, Centre de sécurité et conformité Office 365, Office Online, Office Pro Plus, OneDrive Entreprise, Planificateur, PowerApps, Power Automate, Power BI, SharePoint Online, Skype Entreprise, Stream |
| **GCC High** | Azure Active Directory, Azure Communications Service, Exchange Online, Forms, Microsoft Defender pour Office 365, Microsoft Teams, module complémentaire Conformité avancée Office 365, Centre de sécurité et conformité Office 365, Office Online, Office Pro Plus, OneDrive Entreprise, Planificateur, PowerApps, Power Automate, Power BI, SharePoint Online, Skype Entreprise |
| **DOD** | Azure Active Directory, Azure Communications Service, Exchange Online, Formulaires, Microsoft Defender pour Office 365, Microsoft Teams, module complémentaire Conformité avancée Office 365, Centre de sécurité et conformité Office 365, Office Online, Office Pro Plus, OneDrive Entreprise, Planificateur, Power BI, SharePoint Online, Skype Entreprise |

### <a name="office-365-audits-reports-and-certificates"></a>Audits, rapports et certificats Office 365

Les services Cloud Microsoft font l’objet d’un audit une fois par an pour le code de pratique ISO/IEC 27017:2015 dans le cadre du processus de certification pour ISO/IEC 27001:2013.

- [Office 365 : rapport d’évaluation d’audit ISO 27001, 27018 et 27017](https://aka.ms/o365isoreport)

### <a name="frequently-asked-questions"></a>Foire aux questions

**À qui la norme s'applique-t-elle ?**

Ce code de pratique fournit des contrôles et des conseils de mise en œuvre aux fournisseurs de services Cloud et à leurs clients. Il se présente sous la même forme que la norme ISO/IEC 27002:2013.

**Où puis-je consulter les informations de conformité de Microsoft concernant la norme ISO/IEC 27017:2015?**

Vous pouvez télécharger le certificat [ISO/IEC 27017:2015](https://aka.ms/azureiso27017) pour Azure, Intune et Power BI.

**Puis-je utiliser la conformité ISO/IEC 27017 des services Microsoft dans le processus de certification de mon entreprise?**

Oui. Si votre entreprise cherche une certification pour des implémentations déployées sur les services Enterprise Cloud de Microsoft, vous pouvez utiliser les certifications pertinentes de Microsoft dans votre évaluation de la conformité. Il vous incombe néanmoins d’engager un évaluateur pour mesurer votre mise en œuvre de la conformité, ainsi que des contrôles et des processus au sein de votre propre organisation.

**Comment puis-je me procurer des copies des rapports d’audit applicables ?**

Le [portail d'approbation de services](https://aka.ms/stphelp) fournit des rapports d'audit indépendants et tiers, ainsi que toute autre documentation. Vous pouvez utiliser le portail pour télécharger et examiner cette documentation afin d’obtenir de l’aide concernant vos propres exigences légales et réglementaires.

### <a name="use-microsoft-compliance-manager-to-assess-your-risk"></a>Utilisez le Gestionnaire de Conformité Microsoft pour évaluer vos risques

[Le Gestionnaire de Conformité Microsoft](/microsoft-365/compliance/compliance-manager) est une fonctionnalité dans le [centre de conformité Microsoft 365](/microsoft-365/compliance/microsoft-365-compliance-center) pour vous aider à comprendre la position de la conformité de votre organisation et à prendre des mesures pour réduire les risques. Le Gestionnaire de Conformité offre un modèle Premium pour la création d’une évaluation de ce règlement. Recherchez le modèle sur la page **modèles d’évaluation** dans le Gestionnaire de Conformité. Découvrez comment [créer des évaluations dans le Gestionnaire de Conformité](/microsoft-365/compliance/compliance-manager-assessments).

### <a name="resources"></a>Ressources

- [Code de pratique ISO/IEC 27017:2015](https://www.iso.org/iso/iso_catalogue/catalogue_tc/catalogue_detail.htm?csnumber=43757)
- [Conditions de Microsoft Online Services](https://aka.ms/Online-Services-Terms)
- [Conformité sur le site Microsoft Trust Center](https://www.microsoft.com/trust-center/compliance/compliance-overview)
