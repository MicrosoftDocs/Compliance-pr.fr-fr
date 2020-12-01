---
title: Vue d’ensemble de la gestion des identités et des accès
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
ms.openlocfilehash: b62219faa5bc55ef4bef9557d953caf1a2f95fc7
ms.sourcegitcommit: 626b0076d133e588cd28598c149a7f272fc18bae
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 11/30/2020
ms.locfileid: "49506723"
---
# <a name="identity-and-access-management-overview"></a>Vue d’ensemble de la gestion des identités et des accès

## <a name="how-does-microsoft-365-protect-production-systems-from-unauthorized-or-malicious-access"></a>Comment Microsoft 365 protège-t-il les systèmes de production des accès non autorisés ou malveillants ?

Microsoft 365 est conçu pour permettre aux ingénieurs de Microsoft de faire fonctionner le service sans accéder au contenu client. Par défaut, les ingénieurs Microsoft 365 ont un accès permanent à zéro (ZSA) au contenu du client et aucun accès privilégié à l’environnement de production. Microsoft 365 utilise un modèle juste-à-temps (JIT), juste-suffisant-Access (JEA) pour fournir aux ingénieurs de l’équipe de service un accès privilégié temporaire aux environnements de production lorsqu’un tel accès est requis pour prendre en charge Microsoft 365. Le modèle d’accès JIT remplace l’accès administratif traditionnel et persistant avec un processus permettant aux ingénieurs de demander une élévation temporaire des rôles privilégiés lorsque nécessaire.

Ingénieurs affectés à une équipe de service pour prendre en charge l’éligibilité des demandes de services de production pour un compte d’équipe de service via l’outil de gestion des identités (IDM). La demande d’éligibilité déclenche une série de vérifications de personnel afin de s’assurer que l’ingénieur a passé toutes les conditions requises en matière de filtrage dans le Cloud, qu’il a effectué la formation nécessaire et a reçu une approbation de gestion appropriée avant la création de compte. Une fois que toutes les conditions d’éligibilité ont été respectées, un compte d’équipe de service peut être créé pour l’environnement demandé.

Les comptes d’équipe de service n’accordent pas de privilèges d’administrateur permanent ni d’accès au contenu client. Lorsqu’un ingénieur requiert un accès supplémentaire pour prendre en charge son service Microsoft 365, il demande un accès à des ressources élevées à l’aide d’un outil de gestion des accès appelé Lockbox. La boîte de saisie sécurisée restreint l’accès élevé aux privilèges, ressources et temps nécessaires à l’exécution de la tâche attribuée. Si un relecteur autorisé approuve la demande d’accès JIT, l’ingénieur dispose d’un compte temporaire disposant uniquement des privilèges nécessaires pour terminer son travail affecté. Ce compte temporaire nécessite une authentification multifacteur et est automatiquement supprimé après l’expiration de la période approuvée.

## <a name="how-does-microsoft-365-handle-remote-access-to-production-systems"></a>Comment Microsoft 365 gère-t-il l’accès à distance aux systèmes de production ?

Les composants système Microsoft 365 sont hébergés dans des centres de données répartis géographiquement par rapport aux équipes d’exploitation. Le personnel du centre de connaissances ne dispose pas d’un accès logique aux systèmes Microsoft 365. Par conséquent, le personnel de l’équipe du service Microsoft 365 gère l’environnement par le biais de l’accès à distance. Le personnel de l'équipe de service qui a besoin d'un accès à distance pour prendre en charge Microsoft 365 ne se voit accorder un accès à distance qu'après approbation d'un responsable autorisé. Tout accès à distance utilise un TLS compatible FIPS 140-2 pour les connexions à distance sécurisées.

Microsoft 365 utilise des stations de travail d’administration sécurisée (scie) pour l’accès distant de l’équipe de service afin de protéger les environnements Microsoft 365 contre toute compromission. Ces stations de travail sont spécialement conçues pour empêcher la perte intentionnelle ou involontaire des données de production, y compris le verrouillage des ports USB et la limitation du logiciel disponible sur la présentation de ce qui est nécessaire pour la prise en charge de l’environnement. Les scies sont étroitement suivies et surveillées pour détecter et empêcher la compromission malveillante ou involontaire des données client par les ingénieurs Microsoft.

## <a name="how-does-customer-lockbox-add-additional-protection-for-customer-content"></a>Comment le référentiel sécurisé du client ajoute-t-il une protection supplémentaire pour le contenu client ?

Les clients peuvent ajouter un niveau de contrôle d’accès supplémentaire à leur contenu en activant le référentiel sécurisé du client. Lorsqu’une demande d’élévation de bte post-zone implique l’accès au contenu client, le référentiel sécurisé du client demande une approbation du client en tant que dernière étape du flux de travail approbation. Les organisations peuvent ainsi approuver ou refuser ces demandes et fournir un contrôle d’accès direct au client. Si le client rejette une demande de référentiel sécurisé du client, l’accès au contenu demandé est refusé. Si le client ne rejette pas ou n’approuve pas la demande au cours d’une période donnée, la demande expire automatiquement sans que Microsoft n’accède au contenu client. Si le client approuve la demande, l’accès temporaire de Microsoft au contenu du client sera journalisé, audité et révoqué automatiquement après l’expiration du délai imparti pour l’exécution de l’opération de dépannage.

## <a name="related-external-regulations--certifications"></a>Certifications & des réglementations externes connexes

Les services en ligne de Microsoft sont régulièrement vérifiés pour la conformité aux réglementations et aux certifications externes. Consultez le tableau suivant pour valider les contrôles liés à l’identité et au contrôle d’accès.

| **Audits externes** | **Section** | **Date du dernier rapport** |
|:--------------------|:------------|:-----------------------|
| [FedRAMP (Office 365)](https://compliance.microsoft.com/compliancemanager) | AC-2 : gestion des comptes <br> AC-3 : application d’une application Access <br> AC-5 : séparation des tâches <br> AC-6 : privilège minimal <br> AC-17 : accès à distance | 24 septembre 2020 |
| [ISO 27001/27002 (Office 365)](https://servicetrust.microsoft.com/ViewPage/MSComplianceGuideV3?command=Download&downloadType=Document&downloadId=d7864d4f-e053-4cc4-a964-fa526d07c3be&tab=7027ead0-3d6b-11e9-b9e1-290b1eb4cdeb&docTab=7027ead0-3d6b-11e9-b9e1-290b1eb4cdeb_ISO_Reports) <br><br> [Déclaration de l’applicabilité](https://servicetrust.microsoft.com/ViewPage/MSComplianceGuide?command=Download&downloadType=Document&downloadId=8ee1e46b-2ada-4e7b-bb7d-4c55a8cb6fcd&docTab=4ce99610-c9c0-11e7-8c2c-f908a777fa4d_ISO_Reports) <br> [Certification](https://servicetrust.microsoft.com/ViewPage/MSComplianceGuideV3?command=Download&downloadType=Document&downloadId=1e84a14a-2468-45ac-9412-5e53250d57ec&tab=7027ead0-3d6b-11e9-b9e1-290b1eb4cdeb&docTab=7027ead0-3d6b-11e9-b9e1-290b1eb4cdeb_ISO_Reports) | A. 9.1 : exigences professionnelles de contrôle d’accès <br> A. 9.2 : gestion de l’accès utilisateur <br> A. 9.3 : responsabilités de l’utilisateur <br> A. 9.4 : contrôle d’accès au système et aux applications <br> A. 15.1 : sécurité des informations dans les relations avec les fournisseurs | 22 février 2020 |
| [ISO 27017 (Office 365)](https://servicetrust.microsoft.com/ViewPage/MSComplianceGuideV3?command=Download&downloadType=Document&downloadId=d7864d4f-e053-4cc4-a964-fa526d07c3be&tab=7027ead0-3d6b-11e9-b9e1-290b1eb4cdeb&docTab=7027ead0-3d6b-11e9-b9e1-290b1eb4cdeb_ISO_Reports) <br><br> [Déclaration de l’applicabilité](https://servicetrust.microsoft.com/ViewPage/MSComplianceGuide?command=Download&downloadType=Document&downloadId=8ee1e46b-2ada-4e7b-bb7d-4c55a8cb6fcd&docTab=4ce99610-c9c0-11e7-8c2c-f908a777fa4d_ISO_Reports) <br> [Certification](https://servicetrust.microsoft.com/ViewPage/MSComplianceGuideV3?command=Download&downloadType=Document&downloadId=70de0999-5451-43a3-9ef4-761e8fbfb1a3&tab=7027ead0-3d6b-11e9-b9e1-290b1eb4cdeb&docTab=7027ead0-3d6b-11e9-b9e1-290b1eb4cdeb_ISO_Reports) | A. 9.2 : gestion de l’accès utilisateur <br> A. 9.4 : contrôle d’accès au système et aux applications <br> A. 15.1 : sécurité des informations dans les relations avec les fournisseurs | 22 février 2020 |
| [SOC 1 (Office 365)](https://servicetrust.microsoft.com/ViewPage/MSComplianceGuideV3?command=Download&downloadType=Document&downloadId=b07c0f7b-6bd5-4544-8255-7a5f14bf914a&tab=7027ead0-3d6b-11e9-b9e1-290b1eb4cdeb&docTab=7027ead0-3d6b-11e9-b9e1-290b1eb4cdeb_SOC_/_SSAE_16_Reports) | CA-33 : modification de compte <br> CA-34 : authentification de l’utilisateur <br> CA-35 : accès privilégié <br> CA-36 : accès à distance <br> CA-57 : approbation de la gestion Microsoft de la bte post. <br> CA-58 : demandes de service de référentiel sécurisé du client <br> CA-59 : notifications bte post. <br> CA-61 : révision et approbation JIT | 30 septembre 2019 |
| [SOC 2 (Office 365)](https://servicetrust.microsoft.com/ViewPage/MSComplianceGuideV3?command=Download&downloadType=Document&downloadId=fa062990-e758-4ddc-ace3-7fb21a301d09&tab=7027ead0-3d6b-11e9-b9e1-290b1eb4cdeb&docTab=7027ead0-3d6b-11e9-b9e1-290b1eb4cdeb_SOC_/_SSAE_16_Rep-11e9-b9e1-290b1eb4cdeb_SOC_/_SSAE_16_Reports) | CA-32 : stratégie de compte partagé <br> CA-33 : modification de compte <br> CA-34 : authentification de l’utilisateur <br> CA-35 : accès privilégié <br> CA-36 : accès à distance <br> CA-53 : analyse de tiers <br> CA-56 : approbation du client bte post. <br> CA-57 : approbation de la gestion Microsoft de la bte post. <br> CA-58 : demandes de service de référentiel sécurisé du client <br> CA-59 : notifications bte post. <br> CA-61 : révision et approbation JIT | 30 septembre 2019 |
| [SOC 3 (Office 365)](https://servicetrust.microsoft.com/ViewPage/MSComplianceGuideV3?command=Download&downloadType=Document&downloadId=9df8b99b-96ce-49a9-bff4-268031dcc9a6&tab=7027ead0-3d6b-11e9-b9e1-290b1eb4cdeb&docTab=7027ead0-3d6b-11e9-b9e1-290b1eb4cdeb_SOC_/_SSAE_16_Reports) | CUEC-15 : demandes de référentiel sécurisé du client | 30 septembre 2019 |