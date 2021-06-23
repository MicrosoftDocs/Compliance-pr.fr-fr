---
title: Securities and Exchange Commission (SEC) Rule 17a-4(f) United States
description: Une société d’évaluation indépendante a validé qu’Azure et Office 365 peuvent aider les entreprises financières à respecter les exigences de rétention et de stockage immuables des enregistrements de la SEC règle 17a-4(f).
keywords: Offres pour la conformité Microsoft 365
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
ms.openlocfilehash: 6415b50a38d72ba66ede7e58e1b00aad2485ed42
ms.sourcegitcommit: fb379d1110a9a86c7f9bab8c484dc3f4b3dfd6f0
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 06/23/2021
ms.locfileid: "53089043"
---
# <a name="securities-and-exchange-commission-sec-rule-17a-4f-united-states"></a>Securities and Exchange Commission (SEC) Rule 17a-4(f) United States

## <a name="about-sec-rule-17a-4f"></a>À propos de la règle SEC 17a-4(f)

La [SEC (Securities and Exchange Commission)](https://www.sec.gov/) des États-Unis est une agence indépendante du gouvernement fédéral américain et le principal responsable et régulateur des marchés de titres des États-Unis. Il exerce l’autorité d’application sur les lois fédérales sur les valeurs boursières, propose de nouvelles règles sur les titres et supervise la réglementation du marché du secteur des valeurs boursières.

La SEC définit des exigences rigoureuses et explicites pour les entités réglementées qui choisit de conserver des livres et des enregistrements sur des supports de stockage électronique. Il a établi [17 CFR 240.17a-3](https://www.govinfo.gov/app/details/CFR-2012-title17-vol3/CFR-2012-title17-vol3-sec240-17a-3) et [17 CFR 240.17a-4](https://www.ecfr.gov/cgi-bin/text-idx?mc=true&node=pt17.4.240&rgn=div5#se17.4.240_117a_64) pour contrôler l’enregistrement, y compris les périodes de rétention, pour les courtiers en valeurs boursières. Par la suite, la [SEC](https://www.sec.gov/rules/interp/34-47806.htm) a modifié le paragraphe 17 CFR 240.17a-4 (f), en émettant deux releases interprétatives expressément pour autoriser la conservation des livres et des enregistrements sur les supports de stockage électronique tant que certaines conditions ont été remplies.

Un système de stockage électronique répond à ces conditions s’il empêche l’altération ou l’effacement des enregistrements pendant la période de rétention requise. Les périodes de rétention varient de trois à six ans en fonction des types d’enregistrement, avec une accessibilité immédiate imposée pour les deux premières années. En outre, l’une des releases interprétatives nécessite que le système de stockage soit capable de conserver des enregistrements au-delà de la période de rétention établie par la SEC pour se conformer aux exigences de sécurité, de conservation légale ou d’autres exigences de ce type.

## <a name="microsoft-and-sec-rule-17a-4f"></a>Microsoft et la SEC, règle 17a-4(f)

Les clients des services financiers, qui représentent l’un des secteurs les plus réglementés au monde, sont soumis à des dispositions complexes, telles que la conservation des transactions financières et des communications associées dans un état non révisable et non modifiable. La règle 17a-4(f) de la Commission américaine de sécurité et Exchange (SEC) prévoit des exigences strictes pour les entités réglementées qui choisit de conserver des livres et des enregistrements sur des supports de stockage électronique. Les enregistrements stockés doivent être falsifiés sans possibilité de les modifier ou de les supprimer avant la période de rétention désignée.

Microsoft Azure Les Stockage blob non permutables avec verrouillage de stratégie et Microsoft Office 365 avec verrouillage de conservation peuvent aider les institutions financières à répondre aux exigences de stockage immuables de la règle SEC 17a-4(f).

Pour évaluer la conformité d’Azure et de Office 365 avec la règle SEC 17a-4(f), Microsoft a conservé une société d’évaluation indépendante spécialisée dans la gestion des enregistrements et la gouvernance des informations, Cohasset Associates. Dans le rapport résultant pour :

- **Azure**: SEC [17a-4(f) Évaluation](https://servicetrust.microsoft.com/ViewPage/MSComplianceGuide?command=Download&downloadType=Document&downloadId=19b08fd4-d276-43e8-9461-715981d0ea20&docTab=4ce99610-c9c0-11e7-8c2c-f908a777fa4d_GRC_Assessment_Reports)de la conformité : Stockage Microsoft Azure , Cohasset a validé que [Azure Immutable Blob Stockage](/azure/storage/blobs/storage-blob-immutable-storage) avec l’option de verrouillage de stratégie, lorsqu’il est utilisé pour conserver les objets Blob basés sur le temps dans un format non effaçable et non réécritable (VER), répond aux exigences de stockage immuables de la règle SEC. Chaque objet Blob (enregistrement) n’est pas modifié, remplacé ou supprimé tant que la période de rétention requise n’a pas expiré et que les conservations légales associées ont été libérées. Les fournisseurs de logiciels et les partenaires avec des charges de travail sensibles peuvent désormais s’appuyer sur azure Immutable Blob Stockage comme solution cloud onestop-shop pour la rétention des enregistrements et le stockage immuable. Les institutions financières peuvent désormais créer leurs propres applications en profitant de ces fonctionnalités tout en restant conformes.
- **Microsoft 365**: pour les exigences [sec 17a-4(f),](/microsoft-365/compliance/retention-regulatory-requirements#sec-17a-4f-finra-4511c-and-cftc-131c-d) Cohasset a validé que Microsoft 365 inclut des fonctionnalités d’archivage qui permettent aux clients réglementés, y compris les courtiers, de stocker des données d’une manière qui les aide à se conformer aux exigences de la SEC pour la rétention des enregistrements. Les fonctionnalités de rétention Microsoft 365 permettent de conserver un large éventail de données, notamment la messagerie électronique, la messagerie vocale, les documents partagés, les messages instantanés et les données tierces. En particulier, l’archivage dans Microsoft 365 permet aux clients de définir des stratégies de rétention de messagerie globales ou granulaires pour stocker les données pour une période définie et au-delà dans un format non réécritable et non effaçable.

## <a name="microsoft-in-scope-cloud-services"></a>Services Cloud Microsoft concernés

- [Azure](https://gallery.technet.microsoft.com/Overview-of-Azure-c1be3942)
- [Office 365](https://aka.ms/Office365ComplianceOfferings)

## <a name="audits-reports-and-certificates"></a>Audits, rapports et certificats

### <a name="azure--sec-rule-17"></a>Azure & SEC, règle 17

[SEC 17a-4(f) & CFTC 1.31 (c-d) Compliance Assessment of stockage Azure](https://servicetrust.microsoft.com/ViewPage/MSComplianceGuide?command=Download&downloadType=Document&downloadId=19b08fd4-d276-43e8-9461-715981d0ea20&docTab=4ce99610-c9c0-11e7-8c2c-f908a777fa4d_GRC_Assessment_Reports)

### <a name="office-365--sec-rule-17"></a>Office 365 & SEC Règle 17

[Évaluation de la conformité SEC 17a-4(f) : Centre de sécurité & Conformité Microsoft avec SharePoint, OneDrive, Teams, Exchange et Skype Entreprise](https://servicetrust.microsoft.com/ViewPage/TrustDocumentsV3?command=Download&downloadType=Document&downloadId=2dc92867-5f83-49d8-ad04-9e7295c9e40e&tab=7f51cb60-3d6c-11e9-b2af-7bb9f5d2d913&docTab=7f51cb60-3d6c-11e9-b2af-7bb9f5d2d913_FAQ_and_White_Papers)

## <a name="how-to-implement"></a>Modalités de mise en œuvre

### <a name="financial-services-regulation"></a>Règlement sur les services financiers

Carte de conformité des principaux principes réglementaires américains pour le cloud computing et les services en ligne Microsoft. [En savoir plus](https://servicetrust.microsoft.com/ViewPage/TrustDocuments?command=Download&downloadType=Document&downloadId=5b483567-00b0-4d86-96ae-ee887dadb61c&docTab=6d000410-c9e9-11e7-9a91-892aae8839ad_Compliance_Guides)

### <a name="risk-assessment--compliance-guide"></a>Guide de conformité et & évaluation des risques

Créez un modèle de gouvernance pour l’évaluation des risques des services cloud de Microsoft et la notification réglementaire. [En savoir plus](https://servicetrust.microsoft.com/ViewPage/TrustDocuments?command=Download&downloadType=Document&downloadId=edee9b14-3661-4a16-ba83-c35caf672bd7&docTab=6d000410-c9e9-11e7-9a91-892aae8839ad_FAQ_and_White_Papers)

### <a name="financial-use-cases"></a>Cas d’utilisation financière

Utilisez des présentations de cas, des didacticiels et d’autres ressources pour créer des solutions Azure pour les services financiers. [En savoir plus](/azure/industry/financial/)

## <a name="use-microsoft-compliance-manager-to-assess-your-risk"></a>Utilisez le Gestionnaire de Conformité Microsoft pour évaluer vos risques

[Le Gestionnaire de Conformité Microsoft](/microsoft-365/compliance/compliance-manager) est une fonctionnalité dans le [centre de conformité Microsoft 365](/microsoft-365/compliance/microsoft-365-compliance-center) pour vous aider à comprendre la position de la conformité de votre organisation et à prendre des mesures pour réduire les risques. Le Gestionnaire de Conformité offre un modèle Premium pour la création d’une évaluation de ce règlement. Recherchez le modèle sur la page **modèles d’évaluation** dans le Gestionnaire de Conformité. Découvrez comment [créer des évaluations dans le Gestionnaire de Conformité](/microsoft-365/compliance/compliance-manager-assessments).

## <a name="resources"></a>Ressources

- [Archivage dans Microsoft Office 365, rétention des données et règle 17a-4](https://www.microsoft.com/microsoft-365/blog/2015/11/10/office-365-exchange-online-archiving-now-meets-sec-rule-17a-4-requirements/)
- [Conformité des services financiers Microsoft](https://download.microsoft.com/download/6/4/7/64707E3E-6D3E-45D0-8207-A0EA3201B4A6/Microsoft%20Cloud%20-%20Financial%20Services%20Compliance%20Program%20\(Print\).pdf)
- [Programme de conformité Services cloud microsoft business et services financiers](https://servicetrust.microsoft.com/viewpage/financialservicesoverview)
- [Conformité des services financiers dans Azure](https://azure.microsoft.com/resources/videos/azurecon-2015-financial-services-compliance-in-azure/)
- [Outil d’évaluation des risques dans le Cloud Azure Financial Services](https://servicetrust.microsoft.com/ViewPage/FFIECBlueprint?command=Download&downloadType=Document&downloadId=079a1973-711a-428f-9312-9ddd290cff7b&docTab=c726d5c0-2d1e-11e8-a485-57140ec19669_PaaS)
- [Microsoft Office 365 Stratégies de rétention](/office365/securitycompliance/retention-policies)
- [Microsoft Financial Services Community](https://techcommunity.microsoft.com/t5/financial-services/ct-p/FinancialServices)
- [Conformité sur le site Microsoft Trust Center](https://www.microsoft.com/trust-center/compliance/compliance-overview)
