---
title: US DoE 10 CFR part 810
description: Les clients soumis aux exigences en matière de contrôle d’exportation de US DoE 10 CFR part 810 peuvent utiliser le gouvernement Azure.
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
ms.openlocfilehash: a09f4f6df73ef09dbbce26afd91704181886dd01
ms.sourcegitcommit: 626b0076d133e588cd28598c149a7f272fc18bae
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 11/30/2020
ms.locfileid: "49507506"
---
# <a name="us-doe-10-cfr-part-810"></a>US DoE 10 CFR part 810

## <a name="microsoft-and-doe-10-cfr-part-810"></a>Microsoft et DoE 10 CFR part 810

Le gouvernement Microsoft Azure peut aider les clients soumis aux exigences de contrôle d’exportation du ministère américain de l’énergie (DoE) 10 CFR part 810 à deux autorisations :

- Autorisation provisoire FedRAMP pour fonctionner (P-ATO) émis par le Forum d’autorisation commun (JAB)
- Les autorisations provisoires de niveau 4 et 5 de la protection des systèmes d’information du ministère de la défense (DoD)

FedRAMP offre une référence appropriée pour fournir des assurances indiquant que les pouvoirs publics Azure fournissent une infrastructure de base et des technologies de virtualisation et des services tels que le calcul, le stockage et la mise en réseau conçus avec des contrôles NIST rigoureux. Ces informations permettent de répondre aux besoins de séparation des données client et permettent de sécuriser les connexions aux environnements locaux des clients.

Par ailleurs, les gouvernements Azure sont un nuage communautaire du gouvernement américain qui est physiquement séparé du Cloud Azure. Elle fournit des assurances supplémentaires concernant des exigences spécifiques en matière de filtrage en arrière-plan par le gouvernement américain, y compris des contrôles spécifiques qui restreignent l’accès aux informations et aux systèmes pour les citoyens américains entre le personnel des opérations Azure.

## <a name="microsoft-in-scope-cloud-services"></a>Services Cloud Microsoft concernés

- [Public Azure](https://aka.ms/AzureCompliance)
- Intune

## <a name="how-to-implement"></a>Modalités de mise en œuvre

- [NERC standards de virement & Cloud Computing](https://aka.ms/AzureNERC): instructions pour les utilitaires électriques et les entités enregistrées déployant des charges de travail sur Azure ou sur des administrations publiques Azure.

## <a name="about-doe-10-cfr-part-810"></a>Environ DoE 10 CFR part 810

Le contrôle d’exportation USA Department of Energy (DoE) Règlement [10 CFR Part 810](https://www.govinfo.gov/content/pkg/FR-2015-02-23/pdf/2015-03479.pdf) régit l’exportation des technologies et des interventions nucléaires non classifiées. Elle permet de s’assurer que les technologies nucléaires exportées à partir des États-Unis ne seront utilisées qu’à des fins pacifiques. La partie révisée 810 (règle finale) a pris effet le 1er mars 2015 et est gérée par l’administration de la [sécurité nucléaire nationale](https://www.energy.gov/nnsa/national-nuclear-security-administration). La section 810,6 indique que l’autorisation spécifique DoE est requise pour les deux dispositions de l’assistance et des transferts de technologies nucléaires sensibles qui sont « généralement autorisées », ainsi que celles nécessitant une autorisation spécifique (par exemple, pour les interventions impliquant des technologies nucléaires sensibles telles que l’enrichissement et la production d’eau lourde).

## <a name="frequently-asked-questions"></a>Foire aux questions

**Les 10 CFR part 110 règlements de la Commission de réglementation nucléaire américaine s’appliquent-ils au gouvernement Azure ?**

Non. La [Commission réglementaire nucléaire américaine](https://www.nrc.gov/) (NRC) réglemente l' [exportation et l’importation](https://www.nrc.gov/about-nrc/ip/export-import.html) des installations nucléaires, ainsi que des matériels et matériaux connexes, sous [10 CFR partie 110](https://www.nrc.gov/reading-rm/doc-collections/cfr/part110/). Le NRC ne réglemente pas la technologie et l’assistance nucléaires concernant ces éléments qui tombent sous la juridiction de l’DoE. Par conséquent, les règlements NRC 10 CFR part 110 ne s’appliquent pas au gouvernement Azure.

**Comment puis-je fournir une preuve que je suis conforme à DoE 10 CFR part 810 ?**

Si votre organisation déploie des données vers le gouvernement Azure, vous pouvez vous appuyer sur le haut P-ATO FedRAMP public Azure pour prouver que vous gérez les données de manière convenablement restreint. Toutefois, vous êtes chargé d’obtenir l’autorisation de votre propre système, y compris l’utilisation des services Cloud.

**Quelles sont les responsabilités de classification des données déployées sur les administrations publiques Azure ?**

Les clients qui déploient des données vers le gouvernement Azure sont responsables de leur propre processus de classification de sécurité. Pour les données client soumises aux contrôles d’exportation DoE, le système de classification est augmenté par les contrôles d’information nucléaire contrôlée (UCNI) non classés établis par la section 148 de la Loi sur l' [énergie atomique américaine](https://www.epa.gov/laws-regulations/summary-atomic-energy-act).

## <a name="resources"></a>Ressources

- [Contrôles de services Cloud Azure et d’exportation US](https://servicetrust.microsoft.com/ViewPage/TrustDocuments?command=Download&downloadType=Document&downloadId=c24c11f2-2cd4-444a-9160-19762855ad3a&docTab=6d000410-c9e9-11e7-9a91-892aae8839ad_FAQ_and_White_Papers)
- [Microsoft et FedRAMP](offering-fedramp.md)
- [Microsoft et DoD](offering-dod-disa-l2-l4-l5.md)
- [Cloud Microsoft Service publique](https://www.microsoft.com/enterprise/government)
- [Conformité sur le site Microsoft Trust Center](https://www.microsoft.com/trust-center/compliance/compliance-overview)
