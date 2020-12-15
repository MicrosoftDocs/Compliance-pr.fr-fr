---
title: Règles de Securities and Exchange Commission (SEC) 17A -4 (f)
description: Une entreprise d’évaluation indépendante a validé que Azure et Office 365 peuvent aider les entreprises financières à respecter la réglementation SEC 17A -4 (f) des enregistrements sur la rétention et le stockage non modifiable.
keywords: Microsoft 365, conformité, offres
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
ms.openlocfilehash: 8f47359d23aa9399f36053e1ea6b1df91e181d59
ms.sourcegitcommit: fc1da22cf40dfd807c182d3f6df967eee192eacd
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 12/14/2020
ms.locfileid: "49669765"
---
# <a name="securities-and-exchange-commission-sec-rule-17a-4f-united-states"></a>Règles de Securities and Exchange Commission (SEC) 17A -4 (f)

## <a name="about-sec-rule-17a-4f"></a>À propos de la règle SEC 17A -4 (f)

La [Securities and Exchange Commission (s)](https://www.sec.gov/) est une agence indépendante du gouvernement fédéral des États-Unis et le principal overseer et régulateur des marchés des valeurs américaines. Il se charge de l’autorité de contrainte sur les lois fédérales sur les titres, propose de nouvelles règles de titres et supervise la réglementation du marché du secteur des valeurs mobilières.

La SEC définit des exigences rigoureuses et explicites pour les entités réglementées qui choisissent de conserver des livres et des enregistrements sur des supports de stockage électroniques. Il a établi [17 CFR 240.17 a-3](https://www.govinfo.gov/app/details/CFR-2012-title17-vol3/CFR-2012-title17-vol3-sec240-17a-3) et [17 CFR 240.17 a-4](https://www.ecfr.gov/cgi-bin/text-idx?mc=true&node=pt17.4.240&rgn=div5#se17.4.240_117a_64) pour réglementer l’archivage, y compris les périodes de rétention, pour le courtier en titres. Plus tard, la SEC a [modifié](https://www.sec.gov/rules/interp/34-47806.htm) 17 CFR 240.17 a-4 paragraphe (f), en émettant deux versions d’interprétation expressément pour permettre la conservation des livres et des enregistrements sur des supports de stockage électroniques tant que certaines conditions ont été remplies.

Un système de stockage électronique remplit ces conditions s’il empêche la modification ou l’effacement des enregistrements pendant la période de rétention requise. Les périodes de rétention varient de trois à six ans en fonction des types d’enregistrements, avec une accessibilité immédiate autorisée pour les deux premières années. De plus, l’une des versions d’interprétation exige que le système de stockage puisse conserver des enregistrements au-delà de la période de rétention SEC pour se conformer aux demandes, à la conservation légale ou à d’autres exigences.

## <a name="microsoft-and-sec-rule-17a-4f"></a>Règles Microsoft et SEC 17A -4 (f)

Les clients des services financiers, représentant l’un des secteurs les plus réglementés du monde, sont soumis à des dispositions complexes telles que la rétention des transactions financières et des communications associées dans un État non effaçable et non modifiable. La règle 17A -4 (f) des États-Unis de sécurité et de la Commission Exchange (SEC) prévoit des exigences rigoureuses pour les entités réglementées qui choisissent de conserver des livres et des enregistrements sur des supports de stockage électroniques. Les enregistrements stockés doivent être inviolable sans possibilité de les modifier ou de les supprimer jusqu’à la fin de la période de rétention désignée.

Le stockage d’objets BLOB Microsoft Azure inaltérables avec verrou de stratégie et Microsoft Office 365 avec verrouillage de la conservation peuvent aider les établissements financiers à respecter les exigences de stockage non modifiables de la règle 17A -4 (f).

Pour évaluer la conformité Azure et Office 365 avec la règle SEC 17A -4 (f), Microsoft a conservé un cabinet d’évaluation indépendant spécialisé dans la gestion des enregistrements et la gouvernance des informations, Cohasset Associates. Dans le rapport obtenu pour :

- **Azure**: [sec 17A -4 (f) évaluation de la conformité : Microsoft Azure Storage](https://servicetrust.microsoft.com/ViewPage/MSComplianceGuide?command=Download&downloadType=Document&downloadId=19b08fd4-d276-43e8-9461-715981d0ea20&docTab=4ce99610-c9c0-11e7-8c2c-f908a777fa4d_GRC_Assessment_Reports), Cohasset validée que le [stockage d’objets BLOB Azure inaltérables](https://docs.microsoft.com/azure/storage/blobs/storage-blob-immutable-storage) avec l’option de verrouillage de stratégie, lorsqu’il est utilisé pour conserver les objets BLOB basés sur l’heure dans un format non effaçable et non réinscriptible (Worm), répond aux exigences de stockage non modifiables de la règle sec. La modification, l’écrasement ou la suppression de chaque objet BLOB (enregistrement) est protégée jusqu’à ce que la période de rétention requise ait expiré et que toutes les suspensions juridiques associées aient été publiées. Les fournisseurs de logiciels et les partenaires avec des charges de travail sensibles peuvent désormais compter sur le stockage d’objets BLOB Azure inaltérables en tant que solution cloud OneStop Shop pour les enregistrements de rétention et de stockage non modifiable. Les établissements financiers peuvent désormais créer leurs propres applications en tirant parti de ces fonctionnalités tout en restant conformes.
- **Microsoft 365**: pour les exigences de la [sec 17A -4 (f)](https://docs.microsoft.com/microsoft-365/compliance/retention-regulatory-requirements#sec-17a-4f-finra-4511c-and-cftc-131c-d) , Cohasset validées que Microsoft 365 inclut des fonctionnalités d’archivage permettant aux clients réglementés, y compris les concessionnaires, de stocker les données de manière à ce qu’elles soient conformes aux exigences de la sec pour la rétention des enregistrements. Les fonctionnalités de rétention de Microsoft 365 contribuent à conserver un large éventail de données, notamment la messagerie électronique, la messagerie vocale, les documents partagés, les messages instantanés et les données tierces. En particulier, l’archivage dans Microsoft 365 permet aux clients de définir des stratégies de rétention de messagerie globales ou granulaires pour stocker des données pendant une période définie et au-delà dans un format non réinscriptible et non effaçable.

## <a name="microsoft-in-scope-cloud-services"></a>Services Cloud Microsoft concernés

- [Azure](https://gallery.technet.microsoft.com/Overview-of-Azure-c1be3942)
- [Office 365](https://aka.ms/Office365ComplianceOfferings)

## <a name="audits-reports-and-certificates"></a>Audits, rapports et certificats

### <a name="azure--sec-rule-17"></a>Règle d’Azure & SEC 17

[SEC 17A -4 (f) & CFTC 1,31 (c-d) évaluation de la conformité d’Azure Storage](https://servicetrust.microsoft.com/ViewPage/MSComplianceGuide?command=Download&downloadType=Document&downloadId=19b08fd4-d276-43e8-9461-715981d0ea20&docTab=4ce99610-c9c0-11e7-8c2c-f908a777fa4d_GRC_Assessment_Reports)

### <a name="office-365--sec-rule-17"></a>Office 365 & SEC 17

[Évaluation de la conformité SEC 17A -4 (f) : Centre de conformité & Microsoft Security avec SharePoint, OneDrive, teams, Exchange et Skype entreprise](https://servicetrust.microsoft.com/ViewPage/TrustDocuments?command=Download&downloadType=Document&downloadId=9fa8349d-a0c9-47d9-93ad-472aa0fa44ec&docTab=6d000410-c9e9-11e7-9a91-892aae8839ad_FAQ_and_White_Papers)

## <a name="how-to-implement"></a>Modalités de mise en œuvre

### <a name="financial-services-regulation"></a>Réglementation des services financiers

Plan de conformité des principes de réglementation des États-Unis pour le Cloud Computing et Microsoft Online Services. [En savoir plus](https://servicetrust.microsoft.com/ViewPage/TrustDocuments?command=Download&downloadType=Document&downloadId=5b483567-00b0-4d86-96ae-ee887dadb61c&docTab=6d000410-c9e9-11e7-9a91-892aae8839ad_Compliance_Guides)

### <a name="risk-assessment--compliance-guide"></a>Guide de conformité & de l’évaluation des risques

Créez un modèle de gouvernance pour l’évaluation des risques des services de Cloud Computing Microsoft et la notification de réglementation. [En savoir plus](https://servicetrust.microsoft.com/ViewPage/TrustDocuments?command=Download&downloadType=Document&downloadId=edee9b14-3661-4a16-ba83-c35caf672bd7&docTab=6d000410-c9e9-11e7-9a91-892aae8839ad_FAQ_and_White_Papers)

### <a name="financial-use-cases"></a>Cas d’utilisation financière

Utilisez des présentations de cas, des didacticiels et d’autres ressources pour créer des solutions Azure pour les services financiers. [En savoir plus](https://docs.microsoft.com/azure/industry/financial/)

## <a name="use-microsoft-compliance-manager-to-assess-your-risk"></a>Utilisez le Gestionnaire de Conformité Microsoft pour évaluer vos risques

[Le Gestionnaire de Conformité Microsoft](https://docs.microsoft.com/microsoft-365/compliance/compliance-manager) est une fonctionnalité dans le [centre de conformité Microsoft 365](https://docs.microsoft.com/microsoft-365/compliance/microsoft-365-compliance-center) pour vous aider à comprendre la position de la conformité de votre organisation et à prendre des mesures pour réduire les risques. Le Gestionnaire de Conformité offre un modèle Premium pour la création d’une évaluation de ce règlement. Recherchez le modèle sur la page **modèles d’évaluation** dans le Gestionnaire de Conformité. Découvrez comment [créer des évaluations dans le Gestionnaire de Conformité](https://docs.microsoft.com/microsoft-365/compliance/compliance-manager-assessments).

## <a name="resources"></a>Ressources

- [Archivage dans Microsoft Office 365, rétention des données et règle 17A -4](https://www.microsoft.com/microsoft-365/blog/2015/11/10/office-365-exchange-online-archiving-now-meets-sec-rule-17a-4-requirements/)
- [Conformité des services financiers Microsoft](https://download.microsoft.com/download/6/4/7/64707E3E-6D3E-45D0-8207-A0EA3201B4A6/Microsoft%20Cloud%20-%20Financial%20Services%20Compliance%20Program%20\(Print\).pdf)
- [Programme de conformité services Cloud d’entreprise Microsoft et services financiers](https://servicetrust.microsoft.com/viewpage/financialservicesoverview)
- [Conformité des services financiers dans Azure](https://azure.microsoft.com/resources/videos/azurecon-2015-financial-services-compliance-in-azure/)
- [Outil d’évaluation des risques dans le Cloud Azure Financial Services](https://servicetrust.microsoft.com/ViewPage/FFIECBlueprint?command=Download&downloadType=Document&downloadId=079a1973-711a-428f-9312-9ddd290cff7b&docTab=c726d5c0-2d1e-11e8-a485-57140ec19669_PaaS)
- [Stratégies de rétention de Microsoft Office 365](https://docs.microsoft.com/office365/securitycompliance/retention-policies)
- [Communauté des services financiers Microsoft](https://techcommunity.microsoft.com/t5/financial-services/ct-p/FinancialServices)
- [Conformité sur le site Microsoft Trust Center](https://www.microsoft.com/trust-center/compliance/compliance-overview)
