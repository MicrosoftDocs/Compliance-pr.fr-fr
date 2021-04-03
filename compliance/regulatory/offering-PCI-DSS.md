---
title: Norme de sécurité des données (DSS) d’industrie de carte de paiement (PCI)
description: Azure, SharePoint Online et OneDrive Entreprise sont conformes aux normes de sécurité des données de carte de paiement niveau 1 version 3.2.
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
ms.openlocfilehash: feba7b943f04dc0a9470cef23465f1f63fc55ef7
ms.sourcegitcommit: 024137a15ab23d26cac5ec14c36f3577fd8a0cc4
ms.translationtype: HT
ms.contentlocale: fr-FR
ms.lasthandoff: 04/01/2021
ms.locfileid: "51497717"
---
# <a name="payment-card-industry-pci-data-security-standard-dss"></a>Norme de sécurité des données (DSS) d’industrie de carte de paiement (PCI)

## <a name="pci-dss-overview"></a>Présentation du PCI DSS

La PCI DSS (norme de sécurité des données de l’industrie des cartes de paiement) est une norme mondiale de sécurité des informations conçue pour empêcher la fraude via un contrôle accru des données de carte de crédit. Les organisations de toutes tailles doivent se conformer aux normes PCI DSS si elles acceptent les cartes de paiement des cinq principales marques de cartes de crédit : Visa, MasterCard, American Express, Discover et le Japan Credit Bureau (JCB). La conformité avec la norme PCI DSS est requise pour toute organisation qui stocke, traite ou transmet un paiement et les données du titulaire de la carte.

## <a name="microsoft-and-pci-dss"></a>Microsoft et la norme PCI DSS

Microsoft a réalisé une évaluation PCI DSS annuelle en utilisant un évaluateur qualifié approuvé (QSA) en matière de sécurité. Les auditeurs ont consulté les environnements Microsoft Azure, Microsoft OneDrive Entreprise et Microsoft SharePoint Online, qui incluent la validation de l’infrastructure, développement, opérations, gestion, support et services. La norme PCI DSS désigne quatre niveaux de conformité basés sur un volume de transaction. Azure, OneDrive Entreprise et SharePoint Online sont certifiés compatibles aux termes de PCI DSS version 3.2, fournisseur de services Niveau 1 (le volume le plus élevé de transactions, plus de 6 millions par an).

Cette évaluation a abouti à une attestation de conformité (AoC), disponible pour les clients, et à un rapport de conformité (RoC) publié par l’évaluateur QSA. La période d’effet pour la conformité commence au passage de l’audit et à la réception de l’attestation AoC de l’évaluateur, et elle se termine un an après la date de signature de l’attestation AoC par ce dernier. 

Les clients qui veulent développer un environnement du titulaire de la carte ou un service de traitement de la carte peuvent tirer profit de ces validations dans beaucoup des parties sous-jacentes, réduisant ainsi l'effort et les coûts associés à l'acquisition de leur propre certification PCI DSS.

Il est cependant important de comprendre que le statut de conformité PCI DSS d’Azure, OneDrive Entreprise et SharePoint Online ne se traduit pas automatiquement par une certification PCI DSS pour les services que les clients développent ou hébergent sur ces plateformes. Les clients sont responsables de s’assurer de se conformer aux exigences PCI DSS.

## <a name="microsoft-in-scope-cloud-services"></a>Services Cloud Microsoft dans le périmètre

- [Azure et Azure Government](https://aka.ms/AzureCompliance)
- Microsoft Cloud App Security
- Service cloud Flow, soit en service autonome, soit tel qu’inclus dans un plan ou une suite Office 365 ou Dynamics 365
- Microsoft Graph
- Intune
- [Microsoft Defender pour point de terminaison](/windows/security/threat-protection/microsoft-defender-atp/microsoft-defender-advanced-threat-protection)
- Service Cloud PowerApps, soit en service autonome, soit inclus dans un plan ou une suite Office 365 ou Dynamics 365
- Service Cloud Power BI soit en service autonome, soit inclus dans un plan ou une suite Office 365
- OneDrive Entreprise et SharePoint Online (États-Unis uniquement)

## <a name="audit-reports-and-certificates"></a>Rapports, audit et certificats

- [Attestation de conformité (AoC) Azure PCI DSS](https://aka.ms/azure-pci)
- [Attestation de conformité (AoC)PCI DSS OneDrive Entreprise et SharePoint Online ](https://aka.ms/spo-pci)

## <a name="get-your-pci-dss-solution-running-on-azure"></a>Obtenir votre solution DSS PCI exécutée sur Azure

Créez et déployez votre solution DSS PCI dans le Cloud plus rapidement avec le modèle sécurité et conformité Azure PCI DSS. Obtenez des architectures de référence, des instructions de déploiement, des mappages d’implémentation de contrôle, des scripts automatisés et bien plus encore. [Commencez à utiliser le standard Azure PCI DSS](https://aka.ms/pciblueprint).

## <a name="frequently-asked-questions"></a>Questions fréquemment posées

**Pourquoi la page de couverture de l’Attestation de Conformité (AoC) indique t-elle «juin 2018»?**

La date de juin 2018 sur la page d’accueil correspond au moment où le modèle AoC a été publié. Reportez-vous à la Section 2 pour obtenir la date de l’évaluation.

**Pourquoi existe-t-il deux attestations de conformité Azure (AoC) ?**

Le package Azure AoC inclut des AoCs correspondant au Cloud Azure Public, Allemagne et Gouvernement. Les clients doivent utiliser la AoC qui correspond à leur environnement Azure.  

**Quelle est la relation entre PA DSS et PCI DSS ?**

La PA DSS (Payment Application Data Security Standard) est un ensemble d’exigences qui sont conformes à la PCI DSS et remplace les Meilleures Pratiques de la Demande de Paiement du Visa, tout en consolidant également les exigences de conformité des autres principaux émetteurs de carte. PA DSS aide les fournisseurs de logiciel à développer des applications tierces qui stockent, traitent ou transmettent des données de paiement de détenteur de carte dans le cadre d’un processus de règlement ou d’autorisation de carte. Afin d’atteindre efficacement leur conformité PCI DSS, les détaillants doivent utiliser des applications certifiées PA DSS. PA DSS ne s’applique pas à Azure.

**Qu'est-ce qu'un acquéreur et Azure en utilise-t-il un ?**

Un acquéreur est une banque ou autre entité qui traite des transactions de carte de paiement. Azure n’offre pas de traitement de carte de paiement en tant que service et n’utilise donc pas un acquéreur.

**À quelles organisations et à quels marchands la PCI DSS s'applique-t-elle ?**

Cela s’applique à toute société, quelle que soit la taille ou le nombre des transactions, qui accepte, transmet ou stocke des données de détenteur de carte. Cela signifie que si un client vient à payer une société en utilisant une carte de débit ou de crédit, alors les exigences PCI DSS s’appliquent. Les sociétés sont validées à un des quatre niveaux basés sur le volume total de transactions sur une période de 12 mois. Le Niveau 1 s’adresse aux sociétés qui traitent plus de 6 millions de transactions par an, le Niveau 2 pour 1 à 6 millions de transactions et le Niveau 3 pour 20 000 à 1 million de transactions, enfin le Niveau 4 concerne un nombre de transactions inférieur à 20 000.

**Où dois-je commencer les efforts de conformité PCI DSS de mon organisation pour une solution déployée sur Azure?**

Les informations que le PCI Security Standards Council met à disposition sont un bon moyen de découvrir les exigences de conformité spécifiques. Le Conseil publie le[Guide de référence rapide PCI DSS (PCI DSS Quick Reference Guide)](https://www.pcisecuritystandards.org/documents/PCISSC%20QRG%20August%202014%20-print.pdf)pour les commerçants et autres personnes impliquées dans le traitement de cartes de paiement. Le guide explique comment la norme PCI DSS peut aider à protéger un environnement de transaction de carte de paiement et comment l'appliquer.

La conformité implique plusieurs facteurs, dont l’évaluation des systèmes et des processus qui ne sont pas hébergés sur Azure. Les exigences individuelles varient en fonction des services Azure utilisés et de la manière dont ils sont employés dans la solution.

**Existe-t-il des offres pour OneDrive Entreprise et SharePoint Online compatibles avec la norme PCI DSS en dehors des États-Unis ?**

Pour l’instant, OneDrive Entreprise et SharePoint Online sont compatibles avec la norme PCI-DSS uniquement aux États-Unis (États-Unis). Microsoft évalue la configuration requise et les chronologies pour les régions en dehors des États-Unis et fournit des mises à jour lorsque d’autres régions sont ajoutées à la feuille de route.

**Quelle est l’étendue de OneDrive Entreprise et de SharePoint Online ?**

Pour l’instant, seuls les fichiers et documents téléchargés sur OneDrive Entreprise et SharePoint Online seront conformes au standard PCI DSS.

## <a name="use-microsoft-compliance-manager-to-assess-your-risk"></a>Utilisez le Gestionnaire de Conformité Microsoft pour évaluer vos risques

[Le Gestionnaire de Conformité Microsoft](/microsoft-365/compliance/compliance-manager) est une fonctionnalité dans le [centre de conformité Microsoft 365](/microsoft-365/compliance/microsoft-365-compliance-center) pour vous aider à comprendre la position de la conformité de votre organisation et à prendre des mesures pour réduire les risques. Le Gestionnaire de Conformité offre un modèle Premium pour la création d’une évaluation de ce règlement. Recherchez le modèle sur la page **modèles d’évaluation** dans le Gestionnaire de Conformité. Découvrez comment [créer des évaluations dans le Gestionnaire de Conformité](/microsoft-365/compliance/compliance-manager-assessments).

## <a name="resources"></a>Ressources

- [Conseil normes de sécurité PCI](https://www.pcisecuritystandards.org/)
- [Norme de sécurité des données PCI](https://www.pcisecuritystandards.org/documents/PCI_DSS_v3-1.pdf)
- [Blueprint Azure PCI DSS 3.2.1](/azure/governance/blueprints/samples/pci-dss-3.2.1/)
- [Guide de référence rapide PCI DSS](https://www.pcisecuritystandards.org/documents/PCISSC%20QRG%20August%202014%20-print.pdf)
- [Conformité sur le site Microsoft Trust Center](https://www.microsoft.com/trust-center/compliance/compliance-overview)
