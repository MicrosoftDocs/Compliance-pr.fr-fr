---
title: Commodity Futures Trading Commission (CFTC) Rule 1.31(c-d) United States
description: Une société d’évaluation indépendante a validé qu’Azure et Office 365 peuvent aider les entreprises financières à respecter les exigences de rétention et de stockage immuable des enregistrements de la règle CFTC 1.31.
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
ms.openlocfilehash: 72a849b369f2d72c9b2546d73158ee9237c18b93
ms.sourcegitcommit: 8af471ad10420ee5fce98d2eb0d69a6d2b992f08
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/22/2021
ms.locfileid: "49937039"
---
# <a name="commodity-futures-trading-commission-cftc-rule-131c-d-united-states"></a>Commodity Futures Trading Commission (CFTC) Rule 1.31(c-d) United States

## <a name="about-cftc-rule-13c-d"></a>À propos de la règle CFTC 1.3(c-d)

La [Commodity Futures Trading Commission](https://www.cftc.gov/) (CFTC), une agence fédérale indépendante des États-Unis, régule les marchés de futures et d’options des produits et, plus récemment, le marché des permutations.  
  
La règle CFTC de longue date 1.31 définit les exigences de rétention des enregistrements établies par la règle SEC 17a-4(f). En outre, il spécifie que les enregistrements électroniques doivent être conservés pendant cinq ans et que les originaux doivent être conservés « facilement accessibles » pendant les deux premières années et mis à disposition pour inspection par la Commission ou le département de la Justice des États-Unis pendant toute la période de rétention.  
  
En 2017, la [CFTC](https://www.cftc.gov/sites/default/files/idc/groups/public/@lrfederalregister/documents/file/2017-11014a.pdf)a révisé sa règle, en modifiant et en modernisant son règlement sur la gestion des enregistrements afin d’adopter des normes moins normatives basées sur des principes qui offrent une plus grande flexibilité dans la façon dont les enregistrements peuvent être conservés. Cette révision rend la règle plus neutre en matière de technologie, ce qui permet aux entités réglementées de choisir la technologie la plus appropriée à leur activité tout en conservant les dispositifs de protection qui « garantissent la fiabilité du processus de gestion des registres ». La règle révisée supprime l’exigence selon laquelle les organisations conservent les enregistrements d’origine pendant deux ans, mais conserve la période de maintenance de cinq ans, qui a pour effet d’harmoniser les pratiques pour les entreprises réglementées par la CFTC et la SEC.

## <a name="microsoft-and-cftc-rule-131c-d"></a>Microsoft et la règle CFTC 1.31(c-d)

Les clients des services financiers, qui représentent l’un des secteurs les plus réglementés au monde, sont soumis à des dispositions complexes, telles que la conservation des transactions financières et des communications associées dans un état non révisable et non modifiable. L’une des plus normatives est la règle 1.31 de la CFTC (Commodity Futures Trading Commission) des États-Unis qui prévoit des exigences strictes pour les entités réglementées qui choisit de conserver des livres et des enregistrements sur des supports de stockage électronique. Les enregistrements stockés doivent être falsifiés sans possibilité de les modifier ou de les supprimer avant la période de rétention désignée. Microsoft Azure Immutable Blob Storage with Policy Lock and Microsoft Office 365 with Preservation Lock can help financial institutions meet the storage requirements of CFTC Rule 1.31(c-d).

### <a name="microsoft-azure"></a>Microsoft Azure

Pour évaluer la conformité d’Azure avec la règle CFTC 1.31(c-d), Microsoft a conservé une société d’évaluation indépendante spécialisée dans la gestion des enregistrements et la gouvernance des informations, Cohasset Associates. Dans le rapport résultant, l’évaluation de la conformité [CFTC 1.31 (c)–(d)](https://servicetrust.microsoft.com/ViewPage/MSComplianceGuide?command=Download&downloadType=Document&downloadId=19b08fd4-d276-43e8-9461-715981d0ea20&docTab=4ce99610-c9c0-11e7-8c2c-f908a777fa4d_GRC_Assessment_Reports): Microsoft Azure Storage , Cohasset a validé que le stockage [blob immuable Azure](https://docs.microsoft.com/azure/storage/blobs/storage-blob-immutable-storage) avec l’option de verrouillage de stratégie, lorsqu’il est utilisé pour conserver les objets Blob basés sur le temps dans un format NON effacessable et non réécritable (WORM), répond aux exigences basées sur les principes de la règle CFTC. Chaque objet Blob (enregistrement) n’est pas modifié, remplacé ou supprimé tant que la période de rétention requise n’a pas expiré et que les conservations légales associées ont été libérées. Les fournisseurs de logiciels et les partenaires avec des charges de travail sensibles peuvent désormais s’appuyer sur le stockage d’objets blob immuables Azure comme solution cloud à un arrêt pour la rétention des enregistrements. Les institutions financières peuvent désormais créer leurs propres applications en profitant de ces fonctionnalités tout en restant conformes.

### <a name="microsoft-365"></a>Microsoft 365

Pour les exigences [CFTC 1.31(c)-(d),](https://docs.microsoft.com/microsoft-365/compliance/retention-regulatory-requirements#sec-17a-4f-finra-4511c-and-cftc-131c-d) Cohasset a validé que Microsoft 365 inclut des fonctionnalités d’archivage qui permettent aux clients réglementés, y compris les courtiers, de stocker des données d’une manière qui les aide à se conformer aux exigences de la SEC pour la rétention des enregistrements. Les fonctionnalités de rétention de Microsoft 365 permettent de préserver un large éventail de données, notamment la messagerie électronique, la messagerie vocale, les documents partagés, les messages instantanés et les données tierces. En particulier, l’archivage dans Microsoft 365 permet aux clients de définir des stratégies de rétention de messagerie globales ou granulaires pour stocker les données pour une période définie et au-delà dans un format non réécritable et non effaçable.

## <a name="microsoft-in-scope-cloud-services"></a>Services Cloud Microsoft concernés

- [Azure](https://aka.ms/AzureCompliance)
- [Office 365](https://aka.ms/o365-compliance-framework)

## <a name="audits-reports-and-certificates"></a>Audits, rapports et certificats

[Azure & CFTC Rule 1.31 : SEC 17a-4(f) & CFTC 1.31(c-d) Compliance Assessment of Azure Storage

[Office 365 & CFTC Rule 1.31: Archiving in Office 365, data retention, and SEC Rule 17a-4 compliance

## <a name="how-to-implement"></a>Modalités de mise en œuvre

- [Réglementation des services financiers](https://servicetrust.microsoft.com/ViewPage/TrustDocuments?command=Download&downloadType=Document&downloadId=5b483567-00b0-4d86-96ae-ee887dadb61c&docTab=6d000410-c9e9-11e7-9a91-892aae8839ad_Compliance_Guides): carte de conformité des principaux principes réglementaires américains pour le cloud computing et les services en ligne Microsoft.
- [Guide d'évaluation des risques et de la conformité](https://aka.ms/RiskGovernanceGuide): créez un modèle de gouvernance pour l'évaluation des risques des services de cloud computing Microsoft et la notification aux autorités de régulation.
- [Cas d'utilisation financière](https://docs.microsoft.com/azure/industry/financial/) : utilisez des aperçus de cas, des didacticiels et d'autres ressources pour créer des solutions Azure pour services financiers.

## <a name="resources"></a>Ressources

- [Programme de mise en conformité destiné au secteur des services financiers Microsoft](https://aka.ms/FSCP-Print)
- [Services commerciaux cloud computing et services financiers Microsoft](https://www.microsoft.com/trustcenter/cloudservices/financialservices)
- [Conformité des services financiers dans Azure](https://azure.microsoft.com/resources/videos/azurecon-2015-financial-services-compliance-in-azure/)
- [Microsoft Office stratégies de rétention 365](https://docs.microsoft.com/office365/securitycompliance/retention-policies)
- [Blog Microsoft Financial Services](https://techcommunity.microsoft.com/t5/Financial-Services-Blog/bg-p/FinancialServicesBlog)
- [Conformité sur le site Microsoft Trust Center](https://www.microsoft.com/trust-center/compliance/compliance-overview)
