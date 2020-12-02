---
title: North American Electric Reliability Corporation (NERC)
description: Azure et Azure Government conviennent aux personnes morales déployant un volume de travail dans le Cloud soumis aux standards CIP de la NERC.
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
ms.openlocfilehash: ff7d22396efc6dcac52c029b2929d77717289c9e
ms.sourcegitcommit: 626b0076d133e588cd28598c149a7f272fc18bae
ms.translationtype: HT
ms.contentlocale: fr-FR
ms.lasthandoff: 11/30/2020
ms.locfileid: "49506982"
---
# <a name="north-american-electric-reliability-corporation-nerc"></a>North American Electric Reliability Corporation (NERC)

## <a name="about-the-nerc"></a>À propos de la NERC

La [North American Electric Reliability Corporation](https://www.nerc.com/) (NERC) est une autorité de réglementation à but non lucratif, dont la mission est de garantir la fiabilité du réseau de distribution d’électricité en Amérique du Nord. La NERC est supervisée par l’agence Federal Energy Regulatory Commission (FERC) des Etats-Unis et par les autorités gouvernementales du Canada. En 2006, la FERC a accordé le label Electric Reliability Organization (ERO) à la NERC conformément à la Loi de 2005 sur l'énergie (US Public Law 109-58). La NERC développe et applique des normes de fiabilité connues sous le nom de [standards Critical Infrastructure Protection (CIP)](https://www.nerc.com/pa/Stand/Pages/CIPStandards.aspx) de la NERC.

## <a name="microsoft-and-the-nerc-cip-standard"></a>Microsoft et le standard CIP NERC

La North American Electric Reliability Corporation (NERC) est une autorité de réglementation à but non lucratif, dont la mission est de garantir la fiabilité du réseau de distribution d’électricité en Amérique du Nord. La NERC est supervisée par l’agence Federal Energy Regulatory Commission (FERC) des Etats-Unis et par les autorités gouvernementales du Canada. En 2006, la FERC a accordé le label Electric Reliability Organization (ERO) à la NERC conformément à la Loi de 2005 sur l'énergie (US Public Law 109-58). La NERC développe et applique des normes de fiabilité connues sous le nom de [standards Critical Infrastructure Protection (CIP)](https://www.nerc.com/pa/Stand/Pages/CIPStandards.aspx) de la NERC.

Tous les propriétaires, opérateurs et utilisateurs d’énergie en gros doivent [se conformer aux standards CIP de la NERC](https://www.nerc.com/pa/comp/Pages/default.aspx). Ces entités doivent s’inscrire auprès de la NERC. Les fournisseurs de services Cloud et les fournisseurs tiers ne sont pas soumis aux standards CIP de la NERC. Toutefois, les normes CIP incluent des objectifs qui doivent être pris en considération pour les [personnes morales](https://www.nerc.com/pa/comp/Pages/Registration.aspx) qui utilisent des fournisseurs du réseau de production et transport d’électricité (BES). Les clients Microsoft exploitant des réseaux de production et transport d’électricité sont entièrement responsables de leur conformité aux standards CIP de la NERC. Ni Microsoft Azure, ni Microsoft Azure Government ne sont des actifs de BES ou de BES Cyber.

Comme stipulé par la NERC dans les [standards CIP](https://www.nerc.com/pa/Stand/Reliability%20Standards%20Complete%20Set/RSCompleteSet.pdf) actuels et dans le [Glossaire des termes](https://www.nerc.com/pa/Stand/Glossary%20of%20Terms/Glossary_of_Terms.pdf) de la NERC, les ressources de BES Cyber permettent d’effectuer des surveillances et des contrôles du BES en temps réel, et peuvent affecter l’exploitation fiable du BES dans les 15 minutes après sa détérioration. Pour assurer correctement la prise en charge des ressources de BES Cyber et de Protected Cyber dans le Cloud Computing, les définitions existantes dans les standards CIP de la NERC [doivent être révisées](https://www.nerc.com/pa/Stand/Pages/Project%202016-02%20Modifications%20to%20CIP%20Standards.aspx). Toutefois, il existe de nombreuses charges de travail qui traitent des données CIP sensibles et ne tombent pas sous la règle de 15 minutes, y compris la grande catégorie des BES Cyber System Information (BCSI).

Azure et Azure Government conviennent aux personnes morales déployant un volume de travail soumis aux standards CIP de la NERC, y compris des charges de travail BCSI. Microsoft met les documents suivants à la disposition des personnes morales intéressées par le déploiement des données et des charges de travail soumises à des obligations de conformité au CIP de la NERC dans Azure ou Azure Government :

- [Les standards CIP de la NERC et le Cloud Computing](https://aka.ms/AzureNERC) est un livre blanc qui traite des exigences en matière de conformité pour les CIP de la NERC basées sur des audits établis par des tiers reconnus qui s’appliquent aux fournisseurs de service Cloud tels que FedRAMP. Il traite du filtrage en arrière-plan pour le personnel des opérations de Cloud et répond aux questions fréquentes sur l’isolation logique et l’architecture mutualisée qui sont intéressantes pour les personnes morales. Il traite également des aspects relatifs à la sécurité pour le déploiement local par rapport à celui sur le Cloud.
- [Le guide de mise en œuvre dans le Cloud pour les audits NERC](https://aka.ms/AzureNERCGuide) est un document d’aide qui fournit le mappage de contrôle entre la série actuelle d’exigences en matière de normalisation CIP de la NERC et la série de contrôles [NIST SP 800-53 Rev 4](https://nvd.nist.gov/800-53/Rev4) qui forme la base pour FedRAMP. Il est conçu pour aider techniquement les personnes morales à respecter les exigences de conformité CIP de la NERC pour les ressources déployées dans le Cloud. Le document contient des [feuilles de calcul préremplies de RSAWs (Reliability Standard Audit)](https://www.nerc.com/pa/comp/Pages/Reliability-Standard-Audit-Worksheets-\(RSAWs\).aspx) pour expliquer la manière dont les contrôles Azure répondent aux exigences CIP de la NERC et des instructions pour les personnes morales sur l’utilisation des services Azure pour implémenter les contrôles qu’ils possèdent.

L’entreprise NERC ERO [a publié](https://www.nerc.com/pa/comp/guidance/Pages/default.aspx) un Programme de Suivi et d’Application de la Conformité (CMEP),[guide pratique](https://www.nerc.com/pa/comp/guidance/CMEPPracticeGuidesDL/ERO%20Enterprise%20CMEP%20Practice%20Guide%20_%20BCSI%20-%20v0.2%20CLEAN.pdf) pour aider le personnel CMEP de l’Entreprise ERO dans le cadre de l’évaluation du processus d’une Personne Morale afin d’autoriser l’accès à des emplacements de stockage BSCI désignés, ainsi que les contrôles d’accès qui ont été implémentés par la Personne Morale. De plus, NERC a revu les détails de l’implémentation d’un contrôle Azure et les preuves d’audit FedRamp relatives aux standards NERC CIP-004-6 et CIP-011-2 applicables au BCSI. Sur la base du guide pratique publié par ERO et des contrôles FedRAMP revus pour s’assurer que les personnes morales chiffrent leurs données, aucune recommandation supplémentaire ou clarification n’est requise auprès des personnes morales pour déployer BCSI et les charges de travail associées dans le Cloud. Toutefois, les personnes morales sont responsables du respect des standards CIP de la NERC en fonction de leurs propres faits et circonstances. Les personnes morales doivent passer en revue le [Guide de mise en œuvre dans le Cloud pour les audits NERC](https://aka.ms/AzureNERCGuide) pour obtenir de l’aide sur la documentation des processus et des preuves utilisés pour autoriser l’accès électronique à des emplacements de stockage BCSI, notamment la gestion des clés de chiffrement utilisées pour le chiffrement BCSI dans Azure et Azure Government.

## <a name="microsoft-in-scope-cloud-services"></a>Services Cloud Microsoft dans le périmètre

- [Azure et Azure Government](https://aka.ms/AzureCompliance)

## <a name="audits-reports-and-certificates"></a>Audits, rapports et certificats

Microsoft doit certifier à nouveau ses services Cloud chaque année pour conserver ses P-ATO et ATO. Pour ce faire, Microsoft doit constamment surveiller et évaluer ses contrôles de sécurité, et prouver qu’ils restent conforme.

- [Autorisations des services de cloud computing Microsoft](https://marketplace.fedramp.gov/?sort=productName&productNameSearch=azure#/product/azure-government)
- [Rapports d’audit FedRAMP de Microsoft](https://aka.ms/MicrosoftFedRAMPAuditDocuments)

## <a name="how-to-implement"></a>Modalités de mise en œuvre

### <a name="nerc-cip-standards-and-cloud-computing"></a>Standards CIP de la NERC et Cloud Computing

Traite la conformité des personnes morales qui envisagent d’adopter le Cloud pour les charges de travail soumises aux standards CIP de la NERC.

[En savoir plus](https://aka.ms/AzureNERC)

### <a name="cloud-implementation-guide-for-nerc-audits"></a>Guide de mise en œuvre dans le Cloud pour les audits NERC

Une aide technique accompagne les personnes morales sur les audits NERC d’actifs déployés dans Azure ou Azure Government. 

[En savoir plus](https://aka.ms/AzureNERCGuide)

## <a name="frequently-asked-questions"></a>Questions fréquentes (FAQ)

**Qui est responsable de la conformité aux standards CIP de la NERC ?**

Tous les propriétaires, opérateurs et utilisateurs d’énergie en gros doivent [se conformer aux standards CIP de la NERC](https://www.nerc.com/pa/comp/Pages/default.aspx). Ces entités doivent s’inscrire auprès de la NERC. Les fournisseurs de services Cloud et les fournisseurs tiers ne sont pas soumis aux standards CIP de la NERC. Toutefois, les normes CIP incluent des objectifs qui doivent être pris en considération pour les [personnes morales](https://www.nerc.com/pa/comp/Pages/Registration.aspx) qui utilisent des fournisseurs du réseau de production et transport d’électricité (BES). Les clients Microsoft exploitant des réseaux de production et transport d’électricité sont entièrement responsables de leur conformité aux standards CIP de la NERC. Ni Azure, ni Azure Government ne sont des actifs de BES ou de BES Cyber.

Pour évaluer l’aptitude d’Azure et de Azure Government pour les données et charges de travail soumises aux standards CIP de la NERC, les personnes morales doivent consulter leur propre responsable de la conformité et des audits NERC. Ils doivent examiner le [Guide de mise en œuvre de Cloud pour les audits NERC](https://aka.ms/AzureNERCGuide) pour obtenir de l’aide sur la documentation des processus et des preuves pour les ressources déployées dans le Cloud.

**Quelles charges de travail les personnes morales peuvent-elles déployer sur Azure et Azure Government ?**

Les [standards CIP](https://www.nerc.com/pa/Stand/Reliability%20Standards%20Complete%20Set/RSCompleteSet.pdf) et le [Glossaire des termes](https://www.nerc.com/pa/Stand/Glossary%20of%20Terms/Glossary_of_Terms.pdf) de la NERC stipulent que les ressources de BES Cyber permettent d’effectuer des surveillances et des contrôles du BES en temps réel, et qu’elles pourraient, en cas de détérioration dans les 15 minutes, affecter l’exploitation fiable du BES. Pour assurer correctement la prise en charge des ressources de BES Cyber et de Protected Cyber dans le Cloud Computing, les définitions existantes dans les standards CIP de la NERC [doivent être révisées](https://www.nerc.com/pa/Stand/Pages/Project%202016-02%20Modifications%20to%20CIP%20Standards.aspx). Toutefois, il existe de nombreuses charges de travail qui traitent des données CIP sensibles et ne tombent pas sous la règle de 15 minutes, y compris la grande catégorie des BES Cyber System Information (BCSI).

L’entreprise NERC ERO [a publié](https://www.nerc.com/pa/comp/guidance/Pages/default.aspx) un Programme de Suivi et d’Application de la Conformité (CMEP),[guide pratique](https://www.nerc.com/pa/comp/guidance/CMEPPracticeGuidesDL/ERO%20Enterprise%20CMEP%20Practice%20Guide%20_%20BCSI%20-%20v0.2%20CLEAN.pdf) pour aider le personnel CMEP de l’Entreprise ERO dans le cadre de l’évaluation du processus d’une Personne Morale afin d’autoriser l’accès à des emplacements de stockage BSCI désignés, ainsi que les contrôles d’accès qui ont été implémentés par la Personne Morale. De plus, NERC a revu les détails de l’implémentation d’un contrôle Azure et les preuves d’audit FedRamp relatives aux standards NERC CIP-004-6 et CIP-011-2 applicables au BCSI. Sur la base du guide pratique publié par ERO et des contrôles FedRAMP revus pour s’assurer que les personnes morales chiffrent leurs données, aucune recommandation supplémentaire ou clarification n’est requise auprès des personnes morales pour déployer BCSI et les charges de travail associées dans le Cloud. Toutefois, les personnes morales sont responsables du respect des standards CIP de la NERC en fonction de leurs propres faits et circonstances.

## <a name="use-microsoft-compliance-manager-to-assess-your-risk"></a>Utilisez le Gestionnaire de conformité Microsoft pour évaluer vos risques

Le [Gestionnaire de conformité Microsoft](https://docs.microsoft.com/microsoft-365/compliance/compliance-manager) est une fonctionnalité du [Centre de conformité Microsoft 365](https://docs.microsoft.com/microsoft-365/compliance/microsoft-365-compliance-center) qui vous permet de comprendre l’état de conformité de votre organisation et de prendre des mesures pour réduire les risques. Le Gestionnaire de conformité propose un modèle premium pour créer une évaluation pour ce règlement. Recherchez le modèle dans la page des **modèles d’évaluation** dans le Gestionnaire de conformité. Découvrez comment [créer des évaluations dans le Gestionnaire de conformité](https://docs.microsoft.com/microsoft-365/compliance/compliance-manager-assessments).

## <a name="resources"></a>Ressources

- [Conseils de la NERC en matière de conformité](https://www.nerc.com/pa/comp/guidance/)
- [Cybersécurité NERC – Gestion des risques de la chaîne d’approvisionnement](https://www.nerc.com/pa/Stand/Pages/CIP0131RI.aspx)
- [Conformité et application NERC](https://www.nerc.com/pa/comp/Pages/default.aspx)
- [Organisation et certification de la NERC](https://www.nerc.com/pa/comp/Pages/Registration.aspx)
- [Microsoft et FedRAMP](offering-fedramp.md)
- [Attestation](offering-csa-star-attestation.md) et [certification](offering-csa-star-certification.md) Microsoft et CSA STAR
- [Microsoft et les rapports SOC 2](offering-soc.md)
- [Conformité sur le site Microsoft Trust Center](https://www.microsoft.com/trust-center/compliance/compliance-overview)
