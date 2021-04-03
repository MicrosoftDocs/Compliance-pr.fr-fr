---
title: Aperçu sur la gestion des identités et des accès
description: En savoir plus sur la gestion des identités et des accès dans Microsoft 365
ms.author: robmazz
author: robmazz
manager: laurawi
ms.reviewer: sosstah
audience: Admin
ms.topic: article
f1.keywords:
- NOCSH
ms.service: O365-seccomp
localization_priority: Normal
ms.collection:
- Strat_O365_IP
- M365-security-compliance
- MS-Compliance
search.appverid:
- MET150
- MOE150
titleSuffix: Microsoft Service Assurance
hideEdit: true
ms.openlocfilehash: d431a7f04b156b003f5f4e213aef9bb9792874fe
ms.sourcegitcommit: 024137a15ab23d26cac5ec14c36f3577fd8a0cc4
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 04/01/2021
ms.locfileid: "51497157"
---
# <a name="identity-and-access-management-overview"></a>Aperçu sur la gestion des identités et des accès

## <a name="how-does-microsoft-365-protect-production-systems-from-unauthorized-or-malicious-access"></a>Comment Microsoft 365 protège-t-il les systèmes de production contre tout accès non autorisé ou malveillant ?

Microsoft 365 est conçu pour permettre aux ingénieurs de Microsoft d’exploiter le service sans accéder au contenu client. Par défaut, les ingénieurs Microsoft 365 ont un accès permanent zéro (ZSA) au contenu client et aucun accès privilégié à l’environnement de production. Microsoft 365 utilise un modèle juste-à-temps (JIT), Just-Enough-Access (JEA) pour fournir aux ingénieurs d’équipe de service un accès privilégié temporaire aux environnements de production lorsque cet accès est requis pour prendre en charge Microsoft 365. Le modèle d’accès JIT remplace l’accès administratif traditionnel et persistant avec un processus permettant aux ingénieurs de demander une élévation temporaire des rôles privilégiés lorsque nécessaire.

Les ingénieurs affectés à une équipe de service pour prendre en charge les services de production demandent l’éligibilité à un compte d’équipe de service via l’outil de gestion des identités (IDM). La demande d’éligibilité déclenche une série de vérifications du personnel pour s’assurer que l’ingénieur a réussi toutes les exigences de filtrage cloud, suivi la formation nécessaire et reçu l’approbation de gestion appropriée avant la création du compte. Une fois que toutes les conditions d’éligibilité ont été respectées, un compte d’équipe de service peut être créé pour l’environnement demandé.

Les comptes d’équipe de service n’accordent pas de privilèges d’administrateur permanent ni d’accès au contenu client. Lorsqu’un ingénieur a besoin d’un accès supplémentaire pour prendre en charge son service Microsoft 365, il demande un accès élevé temporaire aux ressources dont il a besoin à l’aide d’un outil de gestion des accès appelé Lockbox. La boîte de saisie sécurisée restreint l’accès élevé aux privilèges, ressources et temps nécessaires à l’exécution de la tâche attribuée. Si un réviseur autorisé approuve la demande d’accès JIT, l’ingénieur se voit accorder un compte temporaire avec uniquement les privilèges nécessaires pour effectuer le travail qui lui est affecté. Ce compte temporaire nécessite une authentification multifacteur et est automatiquement supprimé à l’expiration de la période approuvée.

## <a name="how-does-microsoft-365-handle-remote-access-to-production-systems"></a>Comment Microsoft 365 gère-t-il l’accès à distance aux systèmes de production ?

Les composants système Microsoft 365 sont hébergés dans des centres de données répartis géographiquement par rapport aux équipes d’exploitation. Le personnel du centre de données n’a pas d’accès logique aux systèmes Microsoft 365. Par conséquent, le personnel de l’équipe du service Microsoft 365 gère l’environnement via l’accès à distance. Le personnel de l'équipe de service qui a besoin d'un accès à distance pour prendre en charge Microsoft 365 ne se voit accorder un accès à distance qu'après approbation d'un responsable autorisé. Tout accès à distance utilise un TLS compatible FIPS 140-2 pour les connexions à distance sécurisées.

Microsoft 365 utilise des stations de travail d’administration sécurisées (SAW) pour l’accès à distance de l’équipe de service afin de protéger les environnements Microsoft 365 contre la compromission. Ces stations de travail sont spécifiquement conçues pour empêcher la perte intentionnelle ou involontaire de données de production, notamment le verrouillage des ports USB et la limitation du logiciel disponible sur le SAW à ce qui est requis pour la prise en charge de l’environnement. Les professionnels de l’assistance à la sécurité sont suivis et surveillés de près pour détecter et empêcher toute compromission malveillante ou accidentelle des données client par les ingénieurs Microsoft.

## <a name="how-does-customer-lockbox-add-additional-protection-for-customer-content"></a>Comment Customer Lockbox ajoute-t-il une protection supplémentaire pour le contenu client ?

Les clients peuvent ajouter un niveau supplémentaire de contrôle d’accès à leur contenu en activant Customer Lockbox. Lorsqu’une demande d’élévation lockbox implique l’accès au contenu du client, Customer Lockbox requiert l’approbation du client comme dernière étape du flux de travail d’approbation. Cela permet aux organisations d’approuver ou de refuser ces demandes et fournit un contrôle d’accès direct au client. Si le client rejette une demande Customer Lockbox, l’accès au contenu demandé est refusé. Si le client ne rejette pas ou n’approuve pas la demande dans un certain délai, la demande expirera automatiquement sans que Microsoft n’obtienne l’accès au contenu du client. Si le client approuve la demande, l’accès temporaire de Microsoft au contenu du client sera enregistré, auditable et révoqué automatiquement après l’expiration du délai d’expiration de l’opération de dépannage.

## <a name="related-external-regulations--certifications"></a>Réglementations externes associées & certifications

Les services en ligne de Microsoft sont régulièrement audités pour assurer la conformité avec les réglementations et certifications externes. Reportez-vous au tableau suivant pour la validation des contrôles liés au contrôle d’identité et d’accès.

| **Audits externes** | **Section** | **Date de rapport la plus récente** |
|:--------------------|:------------|:-----------------------|
| [FedRAMP (Office 365)](https://compliance.microsoft.com/compliancemanager) | AC-2 : Gestion des comptes <br> AC-3 : Application de l’accès <br> AC-5 : séparation des tâches <br> AC-6 : privilège minimum <br> AC-17 : Accès à distance | 24 septembre 2020 |
| [ISO 27001/27002 (Office 365)](https://servicetrust.microsoft.com/ViewPage/MSComplianceGuideV3?command=Download&downloadType=Document&downloadId=d7864d4f-e053-4cc4-a964-fa526d07c3be&tab=7027ead0-3d6b-11e9-b9e1-290b1eb4cdeb&docTab=7027ead0-3d6b-11e9-b9e1-290b1eb4cdeb_ISO_Reports) <br><br> [Déclaration d’applicabilité](https://servicetrust.microsoft.com/ViewPage/MSComplianceGuide?command=Download&downloadType=Document&downloadId=8ee1e46b-2ada-4e7b-bb7d-4c55a8cb6fcd&docTab=4ce99610-c9c0-11e7-8c2c-f908a777fa4d_ISO_Reports) <br> [Certification](https://servicetrust.microsoft.com/ViewPage/MSComplianceGuideV3?command=Download&downloadType=Document&downloadId=1e84a14a-2468-45ac-9412-5e53250d57ec&tab=7027ead0-3d6b-11e9-b9e1-290b1eb4cdeb&docTab=7027ead0-3d6b-11e9-b9e1-290b1eb4cdeb_ISO_Reports) | A.9.1 : Exigences professionnelles en matière de contrôle d’accès <br> A.9.2 : Gestion de l’accès des utilisateurs <br> A.9.3 : Responsabilités de l’utilisateur <br> A.9.4 : Contrôle d’accès système et application <br> A.15.1 : Sécurité des informations dans les relations avec les fournisseurs | 22 février 2020 |
| [ISO 27017 (Office 365)](https://servicetrust.microsoft.com/ViewPage/MSComplianceGuideV3?command=Download&downloadType=Document&downloadId=d7864d4f-e053-4cc4-a964-fa526d07c3be&tab=7027ead0-3d6b-11e9-b9e1-290b1eb4cdeb&docTab=7027ead0-3d6b-11e9-b9e1-290b1eb4cdeb_ISO_Reports) <br><br> [Déclaration d’applicabilité](https://servicetrust.microsoft.com/ViewPage/MSComplianceGuide?command=Download&downloadType=Document&downloadId=8ee1e46b-2ada-4e7b-bb7d-4c55a8cb6fcd&docTab=4ce99610-c9c0-11e7-8c2c-f908a777fa4d_ISO_Reports) <br> [Certification](https://servicetrust.microsoft.com/ViewPage/MSComplianceGuideV3?command=Download&downloadType=Document&downloadId=70de0999-5451-43a3-9ef4-761e8fbfb1a3&tab=7027ead0-3d6b-11e9-b9e1-290b1eb4cdeb&docTab=7027ead0-3d6b-11e9-b9e1-290b1eb4cdeb_ISO_Reports) | A.9.2 : Gestion de l’accès des utilisateurs <br> A.9.4 : Contrôle d’accès système et application <br> A.15.1 : Sécurité des informations dans les relations avec les fournisseurs | 22 février 2020 |
| [SOC 1 (Office 365)](https://servicetrust.microsoft.com/ViewPage/MSComplianceGuideV3?command=Download&downloadType=Document&downloadId=90df3f9c-3aaf-4dbf-99d0-ca9f2991721b&tab=7027ead0-3d6b-11e9-b9e1-290b1eb4cdeb&docTab=7027ead0-3d6b-11e9-b9e1-290b1eb4cdeb_SOC_%2F_SSAE_16_Reports) | CA-33 : Modification du compte <br> CA-34 : Authentification des utilisateurs <br> CA-35 : Accès privilégié <br> CA-36 : Accès à distance <br> CA-57 : approbation de gestion de Customer Lockbox Microsoft <br> CA-58 : Demandes de service Customer Lockbox <br> CA-59 : Notifications Customer Lockbox <br> CA-61 : révision et approbation JIT | 24 décembre 2020 |
| [SOC 2 (Office 365)](https://servicetrust.microsoft.com/ViewPage/MSComplianceGuideV3?command=Download&downloadType=Document&downloadId=a73c1738-7892-42b7-acd3-87b6371c53f6&tab=7027ead0-3d6b-11e9-b9e1-290b1eb4cdeb&docTab=7027ead0-3d6b-11e9-b9e1-290b1eb4cdeb_SOC_%2F_SSAE_16_Reports) | CA-32 : stratégie de compte partagé <br> CA-33 : Modification du compte <br> CA-34 : Authentification des utilisateurs <br> CA-35 : Accès privilégié <br> CA-36 : Accès à distance <br> CA-53 : surveillance tierce <br> CA-56 : approbation du client customer Lockbox <br> CA-57 : approbation de gestion de Customer Lockbox Microsoft <br> CA-58 : Demandes de service Customer Lockbox <br> CA-59 : Notifications Customer Lockbox <br> CA-61 : révision et approbation JIT | 24 décembre 2020 |
| [SOC 3 (Office 365)](https://servicetrust.microsoft.com/ViewPage/MSComplianceGuideV3?command=Download&downloadType=Document&downloadId=274054e5-4968-48d2-bf94-9a8eda5d7a93&tab=7027ead0-3d6b-11e9-b9e1-290b1eb4cdeb&docTab=7027ead0-3d6b-11e9-b9e1-290b1eb4cdeb_SOC_%2F_SSAE_16_Reports) | CUEC-15 : Demandes Customer Lockbox | 24 décembre 2020 |