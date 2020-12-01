---
title: Securities and Exchange Commission-réglementation sur la conformité et l’intégrité des systèmes (SIC)
description: Les règles du SIC s’appliquent aux entités SCI, qui incluent de telles organisations d’autoréglementation (SROs) en tant qu’échanges boursiers et d’options, de prestataires de services de compensation et autres systèmes commerciaux (ATSs).
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
ms.openlocfilehash: 9d833cfde69d9cb2c76ee49b600f3defb49fa1ac
ms.sourcegitcommit: 626b0076d133e588cd28598c149a7f272fc18bae
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 11/30/2020
ms.locfileid: "49507474"
---
# <a name="securities-and-exchange-commission-regulation-systems-compliance-and-integrity-sci"></a>Securities and Exchange Commission : réglementation sur la conformité et l’intégrité des systèmes (SIC)

## <a name="about-regulation-sci"></a>À propos de la réglementation SIC

La Securities and Exchange Commission (s) est une agence indépendante du gouvernement fédéral des États-Unis et le principal overseer et régulateur des marchés des valeurs américaines. Il se charge de l’autorité de contrainte sur les lois fédérales sur les titres, propose de nouvelles règles de titres et supervise la réglementation du marché du secteur des valeurs mobilières.

En novembre 2014, les SEC ont adopté la réglementation des systèmes de réglementation [(SIC)](https://www.sec.gov/rules/final/2014/34-73639.pdf) (et formulaire SCI pour la création de rapports sur les événements SCI) pour renforcer l’infrastructure technologique sur les marchés des valeurs américaines. Le règlement est conçu pour réduire la fréquence des pannes système, améliorer la résilience lorsque de tels incidents surviennent, et augmenter la supervision de la technologie du marché des valeurs mobilières et l’application de ses réglementations.

Les règles du SIC s’appliquent aux entités SCI, qui incluent de telles organisations d’autoréglementation (SROs) en tant qu’échanges boursiers et d’options, de prestataires de services de compensation et autres systèmes commerciaux (ATSs). Les règles réglementent principalement les systèmes qui prennent directement en charge les fonctions clés du marché des valeurs mobilières : les opérations de commerce, de dédouanement et de règlement, le routage des commandes, les données sur le marché, la réglementation du marché et la surveillance du marché

## <a name="microsoft-and-sec-regulation-sci"></a>Microsoft et SEC règlement SIC

La Securities and Exchange Commission (s) a adopté le SIC de la réglementation pour renforcer l’infrastructure technologique des organisations financières qui exploitent et prennent en charge les marchés des valeurs américaines. Sous la section s supervision, ses exigences sont conçues pour garantir que ces systèmes bénéficient d’une haute disponibilité, d’une résistance élevée et d’une faible latence (volume élevé de messages avec peu de retard).

Pour vous aider à guider les clients des services financiers qui doivent se conformer à la présente réglementation, Microsoft a publié le [Guide de mise en œuvre de la conformité et de l’intégrité des systèmes de réglementation Microsoft Azure sec](https://servicetrust.microsoft.com/ViewPage/TrustDocumentsV3?command=Download&downloadType=Document&downloadId=a69ce0c1-7b7e-44e9-9143-867241e6b2f9&tab=7f51cb60-3d6c-11e9-b2af-7bb9f5d2d913&docTab=7f51cb60-3d6c-11e9-b2af-7bb9f5d2d913_FAQ_and_White_Papers). Les conseils fournis dans ce document sont les suivants :

- Fournit une vue d’ensemble des fonctionnalités Azure globales qui prennent en charge une résistance élevée, une haute disponibilité et une faible latence.
- Indique clairement les zones de contrôle et les aspects réglementaires des adresses. Ce mappage point par point des fonctionnalités et services Azure aux exigences de SCI mesure la conformité d’Azure à l’infrastructure réglementaire. Elle permet également aux clients de savoir où ils peuvent décaler les responsabilités de sécurité vers Azure, qu’ils avaient entièrement détenues lorsqu’ils étaient exploités sur site. Ces fonctionnalités sont suivies par les promesses que Microsoft effectue dans les SLA Azure.
- Spécifie chaque exigence de SIC relative à la responsabilité du client, et offre une documentation et des services Azure pour les aider à répondre à ces responsabilités.

Ce document fournit une liste de contrôle approfondie des zones ciblées du SIC sur la réglementation. Cette liste de vérification permet aux organisations financières de comprendre comment elles peuvent adopter Azure pour s’assurer que leurs organismes de réglementation, leurs clients et leur direction peuvent se conformer aux exigences réglementaires applicables.

## <a name="microsoft-in-scope-cloud-services"></a>Services Cloud Microsoft concernés

- [Azure](https://aka.ms/AzureCompliance)

## <a name="how-to-implement"></a>Modalités de mise en œuvre

- [Guide de mise en œuvre de la réglementation SIC](https://servicetrust.microsoft.com/ViewPage/TrustDocumentsV3?command=Download&downloadType=Document&downloadId=a69ce0c1-7b7e-44e9-9143-867241e6b2f9&tab=7f51cb60-3d6c-11e9-b2af-7bb9f5d2d913&docTab=7f51cb60-3d6c-11e9-b2af-7bb9f5d2d913_FAQ_and_White_Papers): mappe les fonctionnalités Azure sur le règlement et détaille la responsabilité partagée de la conformité.
- [Conception d’applications Azure fiables](https://docs.microsoft.com/azure/architecture/resiliency/): présentation succincte de la façon de créer la fiabilité à chaque étape de la conception d’une application Azure.
- [Conception d’applications à haut niveau de disponibilité](https://docs.microsoft.com/azure/storage/common/storage-designing-ha-apps-with-ragrs): les développeurs peuvent s’assurer que leurs applications de stockage Azure sont hautement disponibles.
- [Guide d'évaluation des risques et de la conformité](https://aka.ms/RiskGovernanceGuide): créez un modèle de gouvernance pour l'évaluation des risques des services de cloud computing Microsoft et la notification aux autorités de régulation.

## <a name="frequently-asked-questions"></a>Foire aux questions

**Que signifie les responsabilités partagées lors de l’utilisation de la technologie Cloud ?**

À mesure que les environnements informatiques passent des centres de ressources en local à ceux du Cloud, la responsabilité de la sécurité est également déplacée, le fournisseur de services Cloud et le client partagent désormais cette responsabilité. Pour chaque application et solution, la part de cette responsabilité sur le client et la proportion sur le fournisseur de services de chiffrement dépendent du modèle Azure déployé par un client : IaaS, SaaS ou PaaS. Il incombe au client de savoir quel degré il est responsable de l’implémentation des contrôles de sécurité requis. Toutefois, Microsoft fournit des conseils pour aider les clients à accéder à cette dynamique complexe. Pour plus d’informations, consultez la en savoir plus sur [les responsabilités partagées pour le Cloud Computing](https://gallery.technet.microsoft.com/Shared-Responsibilities-81d0ff91).

**Quels établissements financiers peuvent tirer parti d’Azure pour répondre aux exigences en matière de réglementation du SIC ?**

Les organismes financiers ou les entités SCI, soumis à cette réglementation, peuvent déployer Azure. Le SEC indique que son règlement s’applique aux «organisations d’autoréglementation (SROs), y compris les échanges de stocks et d’options, les agences de compensation inscrites, les FINRA et les MSRB, les systèmes de commerce alternatifs (ATSs), les stocks de services de région commerciale et de non-NMS qui dépassent les seuils de volume spécifiés, les disséminateurs de données

## <a name="resources"></a>Ressources

- [Réponses SEC aux questions fréquemment posées concernant la réglementation SIC](https://www.sec.gov/divisions/marketreg/regulation-sci-faq.shtml)
- [Continuité de l’activité et récupération d’urgence (BCDR) : régions couplées Azure](https://docs.microsoft.com/azure/best-practices-availability-paired-regions)
- [Plan de conformité des principes de réglementation de l’informatique en nuage et de Microsoft Online Services](https://aka.ms/FinServ-Guide-US)
- [Programme de conformité des services financiers de Microsoft Cloud](https://aka.ms/FSCP-Print)
- [Conformité destinée au secteur des services financiers dans Azure](https://aka.ms/FinServ-Compliance-Azure)
- [Services financiers Microsoft](https://aka.ms/FinServ-Compliance)
- [Règles Microsoft et SEC 17A -4](offering-SEC-17a-4.md)
- [Conformité sur le site Microsoft Trust Center](https://www.microsoft.com/trust-center/compliance/compliance-overview)
