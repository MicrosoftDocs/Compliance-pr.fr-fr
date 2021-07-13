---
title: Financial Industry Regulatory Authority (FINRA) Rule 4511(c) United States
description: Une société d’évaluation indépendante a validé qu’Azure et Office 365 peuvent aider les entreprises financières à respecter les exigences de rétention et de stockage immuables des enregistrements de la RÈGLE 4511 de la FINRA.
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
ms.openlocfilehash: 5db72902615eef26b45b5d4eeaa52132ee3703b1
ms.sourcegitcommit: 9b0c8852e73e2be54a0f9c6570da67f4964f616c
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 07/12/2021
ms.locfileid: "53385024"
---
# <a name="financial-industry-regulatory-authority-finra-rule-4511c-united-states"></a>Financial Industry Regulatory Authority (FINRA) Rule 4511(c) United States

## <a name="about-finra-rule-4511"></a>À propos de la règle FINRA 4511

L’Autorité de régulation financière [(FINRA)](https://www.finra.org/#/) est le plus grand organisme indépendant qui contrôle les sociétés de titres avec la supervision de plus de 4 500 sociétés de courtier aux États-Unis. Il a été autorisé par le Gouvernement américain à « protéger les investisseurs américains en s’assurer que l’industrie broker-industry fonctionne de façon équitable et intègre ».

En 2011, la Commission de sécurité et d’Exchange (SEC) des États-Unis a approuvé l’adoption par la FINRA des règles sec régissant la conservation des livres et des enregistrements sur les supports de stockage électronique. La règle [4511(c)](https://www.finra.org/sites/default/files/NoticeDocument/p123548.pdf) de la FINRA spécifie que « tous les livres et enregistrements qui doivent être effectués conformément aux règles de la FINRA doivent être conservés dans un format et un média conformes à la règle 17a-4 de la SEA (Securities Exchange Act) ».

En outre, la règle 4511(c) de la FINRA exige que les entreprises conservent pendant une période d’au moins six ans ces livres et enregistrements pour lesquels il n’existe aucune période de rétention spécifiée en vertu des règles FINRA ou SEA applicables. En fait, si les livres et les enregistrements concernent un compte, la période de rétention est obligatoire pour être de six ans après la fermeture du compte. Sinon, la période de rétention est de six ans après la création de ces livres et enregistrements.

## <a name="microsoft-and-finra-rule-4511c"></a>Microsoft et la RÈGLE FINRA 4511(c)

Les clients des services financiers, qui représentent l’un des secteurs les plus réglementés au monde, sont soumis à des dispositions complexes telles que la conservation des transactions financières et des communications associées dans un état non révolu et non modifiable. Parmi celles-ci figure la règle 4511 de l’Autorité de régulation financière (FINRA) qui prévoit des exigences strictes pour les entités réglementées qui choisient de conserver des livres et des enregistrements sur des supports de stockage électronique. Les enregistrements stockés doivent être falsifiés sans possibilité de les modifier ou de les supprimer avant la période de rétention désignée.

Microsoft Azure Les Stockage blob non permutables avec verrouillage de stratégie et Microsoft Office 365 avec verrouillage de conservation peuvent aider les institutions financières à répondre aux exigences de stockage immuables de la règle FINRA 4511(c).

## <a name="microsoft-azure"></a>Microsoft Azure

Pour évaluer la conformité Azure avec la règle FINRA 4511(c), Microsoft a conservé une société d’évaluation indépendante spécialisée dans la gestion des enregistrements et la gouvernance des informations, Cohasset Associates. Le rapport résultant, [SEC 17a-4(f) & CFTC 1.31 (c-d) Évaluation](https://servicetrust.microsoft.com/ViewPage/MSComplianceGuide?command=Download&downloadType=Document&downloadId=19b08fd4-d276-43e8-9461-715981d0ea20&docTab=4ce99610-c9c0-11e7-8c2c-f908a777fa4d_GRC_Assessment_Reports)de la conformité : Stockage Microsoft Azure , englobe la conformité Azure avec la règle FINRA 4511(c), qui se reporte aux exigences de format et de média de la règle SEC 17a-4(f).

Cohasset a validé que les [Stockage blob immuables Azure](/azure/storage/blobs/storage-blob-immutable-storage) avec l’option Verrouillage de stratégie, lorsqu’elles sont utilisées pour conserver des objets Blob basés sur le temps dans un format NON effaçable et non réécritable ,répondent aux exigences de stockage FINRA pertinentes. Chaque objet Blob (enregistrement) n’est pas modifié, remplacé ou supprimé tant que la période de rétention requise n’a pas expiré et que les conservations légales associées ont été libérées.

Les fournisseurs de logiciels et les partenaires avec des charges de travail sensibles peuvent désormais s’appuyer sur Azure Immutable Blob Stockage comme solution cloud d’un magasin unique pour la rétention des enregistrements et le stockage immuable. Les institutions financières peuvent désormais créer leurs propres applications en profitant de ces fonctionnalités tout en restant conformes.

## <a name="microsoft-365"></a>Microsoft 365

Pour les exigences de la [RÈGLE 4511(c)](/microsoft-365/compliance/retention-regulatory-requirements#sec-17a-4f-finra-4511c-and-cftc-131c-d) de la FINRA, Cohasset a validé que Microsoft 365 inclut des fonctionnalités d’archivage qui permettent aux clients réglementés, y compris les courtiers, de stocker des données d’une manière qui les aide à se conformer aux exigences de la SEC pour la rétention des enregistrements. Les fonctionnalités de rétention Microsoft 365 permettent de conserver un large éventail de données, notamment la messagerie électronique, la messagerie vocale, les documents partagés, les messages instantanés et les données tierces. En particulier, l’archivage dans Microsoft 365 permet aux clients de définir des stratégies de rétention de messagerie globales ou granulaires pour stocker les données pour une période définie et au-delà dans un format non réécritable et non effaçable.

## <a name="microsoft-in-scope-cloud-platforms--services"></a>Plateformes cloud microsoft dans l’étendue & services

- [Azure](https://gallery.technet.microsoft.com/Overview-of-Azure-c1be3942)
- [Office 365](https://aka.ms/Office365ComplianceOfferings)

## <a name="audits-reports-and-certificates"></a>Audits, rapports et certificats

### <a name="azure--finra-rule-4511c"></a>Azure & FINRA Règle 4511(c)

[SEC 17a-4(f) & CFTC 1.31 (c-d) Compliance Assessment of stockage Azure](https://servicetrust.microsoft.com/ViewPage/MSComplianceGuide?command=Download&downloadType=Document&downloadId=19b08fd4-d276-43e8-9461-715981d0ea20&docTab=4ce99610-c9c0-11e7-8c2c-f908a777fa4d_GRC_Assessment_Reports)

### <a name="office-365--finra-rule-4511c"></a>Office 365 & FINRA Règle 4511(c)

[Archivage dans le Office 365, la rétention des données et la conformité à la règle SEC 17a-4](https://www.microsoft.com/microsoft-365/blog/2015/11/10/office-365-exchange-online-archiving-now-meets-sec-rule-17a-4-requirements/)

## <a name="how-to-implement"></a>Modalités de mise en œuvre

- **Réglementation des services financiers**: carte de conformité des principaux principes réglementaires américains pour le cloud computing et les services en ligne Microsoft. [En savoir plus](https://servicetrust.microsoft.com/ViewPage/TrustDocuments?command=Download&downloadType=Document&downloadId=5b483567-00b0-4d86-96ae-ee887dadb61c&docTab=6d000410-c9e9-11e7-9a91-892aae8839ad_Compliance_Guides)
- **Guide d'évaluation des risques et de la conformité**: créez un modèle de gouvernance pour l'évaluation des risques des services de cloud computing Microsoft et la notification aux autorités de régulation. [En savoir plus](https://servicetrust.microsoft.com/ViewPage/TrustDocuments?command=Download&downloadType=Document&downloadId=edee9b14-3661-4a16-ba83-c35caf672bd7&docTab=6d000410-c9e9-11e7-9a91-892aae8839ad_FAQ_and_White_Papers)
- **Cas d'utilisation financière** : utilisez des aperçus de cas, des didacticiels et d'autres ressources pour créer des solutions Azure pour services financiers. [En savoir plus](/azure/industry/financial/)

## <a name="resources"></a>Ressources

- [Programme de mise en conformité destiné au secteur des services financiers Microsoft](https://download.microsoft.com/download/6/4/7/64707E3E-6D3E-45D0-8207-A0EA3201B4A6/Microsoft%20Cloud%20-%20Financial%20Services%20Compliance%20Program%20\(Print\).pdf)
- [Services commerciaux cloud computing et services financiers Microsoft](https://servicetrust.microsoft.com/viewpage/financialservicesoverview)
- [Conformité des services financiers dans Azure](https://azure.microsoft.com/resources/videos/azurecon-2015-financial-services-compliance-in-azure/)
- [Outil d’évaluation des risques dans le Cloud Azure Financial Services](https://servicetrust.microsoft.com/ViewPage/FFIECBlueprint?command=Download&downloadType=Document&downloadId=079a1973-711a-428f-9312-9ddd290cff7b&docTab=c726d5c0-2d1e-11e8-a485-57140ec19669_PaaS)
- [Microsoft Office 365 Stratégies de rétention](/office365/securitycompliance/retention-policies)
- [Blog Microsoft Financial Services](https://techcommunity.microsoft.com/t5/Financial-Services-Blog/bg-p/FinancialServicesBlog)
- [Conformité sur le site Microsoft Trust Center](https://www.microsoft.com/trust-center/compliance/compliance-overview)
