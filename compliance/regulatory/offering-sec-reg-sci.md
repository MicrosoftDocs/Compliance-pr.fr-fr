---
title: Securities and Exchange Commission - Regulation Systems Compliance and Integrity (SCI)
description: Les règles SCI s’appliquent aux entités SCI, qui incluent les organisations auto-réglementaires (SROs) comme les échanges de stock et d’options, les agences de compensation inscrites et les systèmes de commerce alternatifs ( ATS).
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
ms.openlocfilehash: 049f0516598209411b0c5ca47eea39140762fd3d
ms.sourcegitcommit: 21ed42335efd37774ff5d17d9586d5546147241a
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 02/05/2021
ms.locfileid: "50119873"
---
# <a name="securities-and-exchange-commission-regulation-systems-compliance-and-integrity-sci"></a>Securities and Exchange Commission: Regulation Systems Compliance and Integrity (SCI)

## <a name="about-regulation-sci"></a>À propos du règlement SCI

La SEC (Securities and Exchange Commission) des États-Unis est une agence indépendante du gouvernement fédéral américain et le principal responsable et régulateur des marchés de titres des États-Unis. Il exerce l’autorité d’application sur les lois fédérales sur les valeurs boursières, propose de nouvelles règles sur les titres et supervise la réglementation du marché du secteur des valeurs boursières.

En novembre 2014, la SEC a adopté la conformité et l’intégrité des systèmes de réglementation [(SCI)](https://www.sec.gov/rules/final/2014/34-73639.pdf) (et Form SCI pour la rapports d’événements SCI) pour améliorer l’infrastructure technologique sur les marchés de titres américains. La réglementation est conçue pour réduire la fréquence des pannes du système, améliorer la résilience lorsque de tels incidents se produisent et renforcer la supervision de la SEC sur la technologie du marché des titres et l’application de ses réglementations.

Les règles SCI s’appliquent aux entités SCI, qui incluent les organisations auto-réglementaires (SROs) comme les échanges de stock et d’options, les agences de compensation inscrites et les systèmes de commerce alternatifs ( ATS). Les règles régulent principalement les systèmes qui s’appuient directement sur les principales fonctions du marché des titres : commerce, habilitation et règlement, routage des commandes, données de marché, réglementation du marché et surveillance du marché.

## <a name="microsoft-and-sec-regulation-sci"></a>Microsoft et la SEC Regulation SCI

La SEC (Securities and Exchange Commission) des États-Unis a adopté le règlement SCI pour renforcer l’infrastructure technologique des organisations financières qui exploitent et gèrent les marchés de titres américains. Sous supervision de la SEC, ses exigences sont conçues pour s’assurer que ces systèmes ont une haute disponibilité, une résilience forte et une faible latence (volume élevé de messages avec peu de délai).

Pour guider les clients des services financiers américains qui doivent se conformer à cette réglementation, Microsoft a publié le Guide de mise en œuvre du cloud conformité et intégrité des systèmes de réglementation [SEC Microsoft Azure.](https://servicetrust.microsoft.com/ViewPage/TrustDocumentsV3?command=Download&downloadType=Document&downloadId=a69ce0c1-7b7e-44e9-9143-867241e6b2f9&tab=7f51cb60-3d6c-11e9-b2af-7bb9f5d2d913&docTab=7f51cb60-3d6c-11e9-b2af-7bb9f5d2d913_FAQ_and_White_Papers) Les instructions de ce document :

- Fournit une vue d’ensemble des fonctionnalités Azure globales qui assurent une résilience élevée, une haute disponibilité et une faible latence.
- Précise les domaines de contrôle et les aspects réglementaires des adresses Azure. Ce mappage point par point des fonctionnalités et services Azure aux exigences sci mesure la conformité d’Azure par rapport à l’infrastructure réglementaire. Il permet également aux clients de comprendre où ils peuvent déplacer les responsabilités de sécurité vers Azure qu’ils possédaient entièrement lorsqu’ils fonctionnaient sur site. Ces fonctionnalités sont dosées par les promesses que Microsoft fait dans les SSL Azure.
- Spécifie chaque exigence de l’sci de règlement qui est la responsabilité du client à traiter, et offre la documentation et les services Azure pour l’aider à répondre à ces responsabilités.

Ce document fournit une liste de contrôle complète des domaines essentiels de l’sci du règlement. Cette liste de contrôle aide les organisations financières à comprendre comment elles peuvent adopter Azure pour garantir à leurs autorités de réglementation, clients et direction qu’elles peuvent se conformer aux exigences réglementaires applicables.

## <a name="microsoft-in-scope-cloud-services"></a>Services Cloud Microsoft dans le périmètre

- [Azure](https://aka.ms/AzureCompliance)

## <a name="how-to-implement"></a>Modalités de mise en œuvre

- [Guide de mise en œuvre sci](https://servicetrust.microsoft.com/ViewPage/TrustDocumentsV3?command=Download&downloadType=Document&downloadId=a69ce0c1-7b7e-44e9-9143-867241e6b2f9&tab=7f51cb60-3d6c-11e9-b2af-7bb9f5d2d913&docTab=7f51cb60-3d6c-11e9-b2af-7bb9f5d2d913_FAQ_and_White_Papers)du règlement : mase les fonctionnalités Azure à la réglementation et détaille la responsabilité partagée en matière de conformité.
- [Conception d’applications Azure fiables](/azure/architecture/resiliency/): vue d’ensemble de la création de la fiabilité à chaque étape de la conception d’applications Azure.
- [Conception d’applications hautement disponibles](/azure/storage/common/storage-designing-ha-apps-with-ragrs): comment les développeurs peuvent s’assurer que leurs applications de stockage Azure sont hautement disponibles.
- [Guide d'évaluation des risques et de la conformité](https://aka.ms/RiskGovernanceGuide): créez un modèle de gouvernance pour l'évaluation des risques des services de cloud computing Microsoft et la notification aux autorités de régulation.

## <a name="frequently-asked-questions"></a>Questions fréquemment posées

**Que signifie la responsabilité partagée lors de l’utilisation de la technologie cloud ?**

À mesure que les environnements informatiques se déplacent des centres de données locaux vers ceux du cloud, la responsabilité de la sécurité change également : le fournisseur de services cloud (CSP) et le client partagent désormais cette responsabilité. Pour chaque application et solution, le niveau de responsabilité du client et du programme CSP dépend du modèle Azure déployé par un client (IaaS, SaaS ou PaaS). Il est de l’obligation du client de comprendre dans quelle mesure il est responsable de l’implémentation des contrôles de sécurité requis. Toutefois, Microsoft fournit des conseils pour aider les clients à naviguer dans cette dynamique complexe. Pour plus d’informations, [voir Responsabilités partagées pour le cloud computing.](https://gallery.technet.microsoft.com/Shared-Responsibilities-81d0ff91)

**Quelles institutions financières peuvent tirer parti d’Azure pour répondre aux exigences de l’SCI du règlement ?**

Les organisations financières, ou entités SCI, qui sont soumises au règlement peuvent déployer Azure. La SEC indique que sa réglementation s’applique aux « organisations auto-réglementaires ( SROs), y compris les échanges de stock et d’options, les organismes d’échanges inscrits, la FINRA et le MSRB, les systèmes de commerce alternatifs (ATS), qui échangent des stocks NMS et non-NMS dépassant les seuils de volume spécifiés, les diffuseurs de données de marché consolidées (processeurs de plan) et certains organismes de compensation exemptés. »

## <a name="resources"></a>Ressources

- [Réponses SEC aux questions fréquemment posées concernant le règlement SCI](https://www.sec.gov/divisions/marketreg/regulation-sci-faq.shtml)
- [Continuité d’activité et récupération d’urgence (BCDR) : régions couplées Azure](/azure/best-practices-availability-paired-regions)
- [Carte de conformité des principes et des principes de réglementation cloud computing Microsoft Online Services](https://aka.ms/FinServ-Guide-US)
- [Programme de conformité des services financiers de Microsoft Cloud](https://aka.ms/FSCP-Print)
- [Conformité des services financiers dans Azure](https://aka.ms/FinServ-Compliance-Azure)
- [Services financiers Microsoft](https://aka.ms/FinServ-Compliance)
- [Microsoft et la SEC, règle 17a-4](offering-SEC-17a-4.md)
- [Conformité sur le site Microsoft Trust Center](https://www.microsoft.com/trust-center/compliance/compliance-overview)
