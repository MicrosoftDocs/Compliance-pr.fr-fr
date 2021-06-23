---
title: US DoE 10 CFR Part 810
description: Les clients soumis aux exigences de contrôle d’exportation de l’US DoE 10 CFR Partie 810 peuvent utiliser Azure Government.
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
ms.openlocfilehash: 1a16495f5cfe3e293910ebe84e6af566aea17621
ms.sourcegitcommit: fb379d1110a9a86c7f9bab8c484dc3f4b3dfd6f0
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 06/23/2021
ms.locfileid: "53087543"
---
# <a name="us-doe-10-cfr-part-810"></a>US DoE 10 CFR Part 810

## <a name="microsoft-and-doe-10-cfr-part-810"></a>Microsoft et DoE 10 CFR Partie 810

Microsoft Azure Le gouvernement peut aider les clients soumis aux exigences de contrôle d’exportation du département de l’Énergie des États-Unis 10 CFR Partie 810 à deux autorisations :

- L’autorisation d’exploitation provisoire élevée FedRAMP (P-ATO) émise par le Comité d’autorisation commun (JAB)
- Autorisations provisoires de niveau 4 et 5 de l’Agence des systèmes d’information sur la défense du département de la Défense (DoD)

FedRAMP offre une ligne de base appropriée pour garantir qu’Azure Government fournit des technologies et des services de virtualisation de base, tels que le calcul, le stockage et la mise en réseau conçus avec des contrôles NIST stricts. Ceux-ci répondent aux exigences de séparation des données client et permettent de sécuriser les connexions aux environnements locaux des clients.

En outre, Azure Government est un cloud communautaire du gouvernement des États-Unis qui est physiquement séparé du cloud Azure. Il fournit des garanties supplémentaires concernant des exigences spécifiques en matière de filtrage des antécédents par le gouvernement des États-Unis, notamment des contrôles spécifiques qui limitent l’accès aux informations et aux systèmes aux citoyens américains triés parmi le personnel des opérations Azure.

## <a name="microsoft-in-scope-cloud-services"></a>Services Cloud Microsoft concernés

- [Azure Government](https://aka.ms/AzureCompliance)
- Intune

## <a name="how-to-implement"></a>Modalités de mise en œuvre

- Normes CIP de la [NERC & Cloud Computing](https://aka.ms/AzureNERC): conseils pour les utilitaires électriques et les entités inscrites déployant des charges de travail sur Azure ou Azure Government.

## <a name="about-doe-10-cfr-part-810"></a>À propos de DoE 10 CFR Partie 810

Le règlement [10 CFR partie 810](https://www.govinfo.gov/content/pkg/FR-2015-02-23/pdf/2015-03479.pdf) sur le contrôle d’exportation du département de l’Énergie (DoE) des États-Unis régit l’exportation de la technologie et de l’assistance technologiques non classifiées. Cela permet de s’assurer que les technologies existantes exportées depuis les États-Unis ne seront utilisées qu’à des fins commerciales. La révision de la partie 810 (règle finale) est entrée en vigueur en mars 2015 et est administrée par l’Administration nationale de la [sécurité de La Sécurité](https://www.energy.gov/nnsa/national-nuclear-security-administration)nationale . L’article 810.6 indique que l’autorisation DoE spécifique est requise pour les dispositions d’assistance et les transferts de technologies sensibles qui sont « généralement autorisées », ainsi que pour celles nécessitant une autorisation spécifique (par exemple, pour l’assistance impliquant des technologies sensibles telles que l’enrichissement et la production d’eau lourde).

## <a name="frequently-asked-questions"></a>Foire aux questions

**Les 10 réglementations CFR partie 110 de la Commission réglementaire américaine s’appliquent-ils au gouvernement Azure ?**

Non. La [COMMISSION DE RÉGLEMENTATION AMÉRICAINE RÉGULE régule](https://www.nrc.gov/) l’exportation et l’importation des installations et équipements connexes et matériels connexes sous [10 CFR Partie 110](https://www.nrc.gov/reading-rm/doc-collections/cfr/part110/). [](https://www.nrc.gov/about-nrc/ip/export-import.html) Le PROGRAMME DNS ne régule pas la technologie et l’assistance relatives à ces éléments qui relèvent de la juridiction DoE. Par conséquent, les réglementations DE LA PARTIE 110 CFR 10 NE s’appliquent pas à Azure Government.

**Comment puis-je fournir des preuves que je suis conforme à la partie 810 cfr du DoE 10 ?**

Si votre organisation déploie des données dans Azure Government, vous pouvez vous appuyer sur azure Government FedRAMP High P-ATO comme preuve que vous traitez les données d’une manière restreinte appropriée. Toutefois, vous êtes responsable de l’obtention de l’autorisation DoE de vos propres systèmes, y compris l’utilisation des services cloud.

**Quelles sont mes responsabilités en matière de classification des données déployées dans Azure Government ?**

Les clients déployant des données dans Azure Government sont responsables de leur propre processus de classification de la sécurité. Pour les données client soumises aux contrôles d’exportation DoE, le système de classification est augmenté par les contrôles UCNI (Unclassified Controlled Controlled Information) établis par la section 148 de [l’US Atomic Energy Act](https://www.epa.gov/laws-regulations/summary-atomic-energy-act).

## <a name="resources"></a>Ressources

- [Azure Cloud Services et contrôles d’exportation des États-Unis](https://servicetrust.microsoft.com/ViewPage/TrustDocuments?command=Download&downloadType=Document&downloadId=c24c11f2-2cd4-444a-9160-19762855ad3a&docTab=6d000410-c9e9-11e7-9a91-892aae8839ad_FAQ_and_White_Papers)
- [Microsoft et FedRAMP](offering-fedramp.md)
- [Microsoft et DoD](offering-dod-disa-l2-l4-l5.md)
- [Cloud Microsoft Service publique](https://www.microsoft.com/enterprise/government)
- [Conformité sur le site Microsoft Trust Center](https://www.microsoft.com/trust-center/compliance/compliance-overview)
