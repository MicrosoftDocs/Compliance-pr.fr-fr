---
title: Vue d’ensemble du chiffrement et de la gestion des clés
description: En savoir plus sur le chiffrement et la gestion des clés dans Microsoft 365
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
ms.openlocfilehash: 96a3871657dc1e6021949ca9fc2376df382fe15b
ms.sourcegitcommit: 626b0076d133e588cd28598c149a7f272fc18bae
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 11/30/2020
ms.locfileid: "49506868"
---
# <a name="encryption-and-key-management-overview"></a>Vue d’ensemble du chiffrement et de la gestion des clés

## <a name="what-role-does-encryption-play-in-protecting-customer-content"></a>Quel est le rôle joué par le chiffrement dans la protection du contenu client ?

La plupart des services Cloud d’entreprise Microsoft sont des services mutualisés, ce qui signifie que le contenu client peut être stocké sur le même matériel physique que celui d’autres clients. Pour protéger la confidentialité du contenu client, Microsoft 365 chiffre toutes les données au repos et en transit à l’aide de certains des protocoles de chiffrement les plus sécurisés disponibles.

Le chiffrement ne remplace pas les contrôles d’accès renforcés. La stratégie de contrôle d’accès de Microsoft 365 en matière d’accès permanent ZSA protège le contenu du client contre les accès non autorisés par les employés de Microsoft. Le chiffrement complète le contrôle d’accès en protégeant la confidentialité du contenu du client où qu’il est stocké et en empêchant le contenu d’être lu pendant le transit entre les systèmes Microsoft 365 ou entre Microsoft 365 et le client.

## <a name="how-does-microsoft-365-encrypt-data-at-rest"></a>Comment Microsoft 365 chiffre-t-il les données au repos ?

Tout le contenu client de Microsoft 365 est protégé par une ou plusieurs formes de chiffrement. Les serveurs Microsoft utilisent BitLocker pour chiffrer les lecteurs de disque contenant le contenu du client au niveau du volume. Le chiffrement fourni par BitLocker protège le contenu du client en cas de chute d’autres processus ou contrôles (par exemple, le contrôle d’accès ou le recyclage du matériel) susceptibles d’entraîner un accès physique non autorisé aux disques contenant du contenu client.

Exchange Online, Microsoft Teams, SharePoint Online et OneDrive entreprise utilisent également le chiffrement de service au niveau de la couche d’application pour chiffrer le contenu du client. Le chiffrement de service fournit des fonctionnalités de protection et de gestion des droits par-dessus la protection de chiffrement élevée. Il permet également la séparation entre les systèmes d’exploitation Windows et les données client stockées ou traitées par ces systèmes d’exploitation.

## <a name="how-does-microsoft-365-encrypt-data-in-transit"></a>Comment Microsoft 365 chiffre-t-il les données en transit ?

Les produits et services Microsoft 365 utilisent des protocoles de transport forts, tels que TLS, pour empêcher les parties non autorisées d’espionner les données client lorsqu’elles transitent sur un réseau. Parmi les exemples de données en transit, citons les messages électroniques qui sont en cours de remise, les conversations qui ont lieu dans une réunion en ligne ou les fichiers répliqués entre centres de données.

Dans Microsoft 365, les données sont considérées « en transit » dès que l’appareil d’un utilisateur communique avec un serveur Microsoft ou si un serveur Microsoft communique avec un autre serveur. Exchange Online, SharePoint Online, Microsoft teams et Office Online utilisent tous le protocole TLS pour garantir la confidentialité des données lors de leur transit.

## <a name="how-does-microsoft-365-manage-the-keys-used-for-encryption"></a>Comment Microsoft 365 gère-t-il les clés utilisées pour le chiffrement ?

Le chiffrement fort est sécurisé uniquement comme les clés utilisées pour chiffrer les données. Microsoft utilise ses propres certificats de sécurité pour chiffrer les connexions TLS pour les données en transit. Pour les données au repos, les volumes protégés par BitLocker sont chiffrés avec une clé de chiffrement de volume complet, qui est chiffrée avec une clé principale de volume, qui est à son tour liée au module de plateforme sécurisée (TPM) du serveur. BitLocker utilise des algorithmes conformes à FIPS pour s’assurer que les clés de chiffrement ne sont jamais stockées ou envoyées sur le réseau en clair.

Le chiffrement de service fournit une couche supplémentaire de chiffrement pour les données client-inactives dans Exchange Online, Microsoft Teams, SharePoint Online et OneDrive entreprise. Le chiffrement de service offre aux clients deux options pour la gestion des clés de chiffrement : clés gérées par Microsoft ou clé client. Lors de l’utilisation de clés gérées par Microsoft, les services Microsoft 365 génèrent et stockent automatiquement les clés racines utilisées pour le chiffrement de service.

Les clients ayant besoin de contrôler leurs propres clés de chiffrement racines peuvent tirer parti du chiffrement de service avec la clé client. À l’aide de la clé client, les clients peuvent générer leurs propres clés de chiffrement à l’aide d’un module de service matériel (HSM) local ou d’un coffre-fort de clés Azure (AKV). Les clés racines du client sont stockées dans AKV, où elles peuvent être utilisées comme racine de l’une des clés qui chiffre les fichiers ou les données de la boîte aux lettres du client. Les clés racines du client ne sont accessibles qu’indirectement par le code de service Microsoft 365 pour le chiffrement des données et ne sont pas accessibles directement par les employés de Microsoft.

## <a name="related-external-regulations--certifications"></a>Certifications & des réglementations externes connexes

Les services en ligne de Microsoft sont régulièrement vérifiés pour la conformité aux réglementations et aux certifications externes. Reportez-vous au tableau suivant pour la validation des contrôles liés au chiffrement et à la gestion des clés.

| **Audits externes** | **Section** | **Date du dernier rapport** |
|:--------------------|:------------|:-----------------------|
| [FedRAMP (Office 365)](https://compliance.microsoft.com/compliancemanager) | SC-8 : confidentialité et intégrité de la transmission <br> SC-13 : utilisation du chiffrement <br> SC-28 : protection des informations au repos <br>  | 24 septembre 2020 |
| [ISO 27001/27002 (Office 365)](https://servicetrust.microsoft.com/ViewPage/MSComplianceGuideV3?command=Download&downloadType=Document&downloadId=d7864d4f-e053-4cc4-a964-fa526d07c3be&tab=7027ead0-3d6b-11e9-b9e1-290b1eb4cdeb&docTab=7027ead0-3d6b-11e9-b9e1-290b1eb4cdeb_ISO_Reports) <br><br> [Déclaration de l’applicabilité](https://servicetrust.microsoft.com/ViewPage/MSComplianceGuide?command=Download&downloadType=Document&downloadId=8ee1e46b-2ada-4e7b-bb7d-4c55a8cb6fcd&docTab=4ce99610-c9c0-11e7-8c2c-f908a777fa4d_ISO_Reports) <br> [Certification](https://servicetrust.microsoft.com/ViewPage/MSComplianceGuideV3?command=Download&downloadType=Document&downloadId=1e84a14a-2468-45ac-9412-5e53250d57ec&tab=7027ead0-3d6b-11e9-b9e1-290b1eb4cdeb&docTab=7027ead0-3d6b-11e9-b9e1-290b1eb4cdeb_ISO_Reports) | A. 10.1 : contrôles de chiffrement <br> A. 18.1.5 : contrôles de chiffrement | 22 février 2020 |
| [ISO 27017 (Office 365)](https://servicetrust.microsoft.com/ViewPage/MSComplianceGuideV3?command=Download&downloadType=Document&downloadId=d7864d4f-e053-4cc4-a964-fa526d07c3be&tab=7027ead0-3d6b-11e9-b9e1-290b1eb4cdeb&docTab=7027ead0-3d6b-11e9-b9e1-290b1eb4cdeb_ISO_Reports) <br><br> [Déclaration de l’applicabilité](https://servicetrust.microsoft.com/ViewPage/MSComplianceGuide?command=Download&downloadType=Document&downloadId=8ee1e46b-2ada-4e7b-bb7d-4c55a8cb6fcd&docTab=4ce99610-c9c0-11e7-8c2c-f908a777fa4d_ISO_Reports) <br> [Certification](https://servicetrust.microsoft.com/ViewPage/MSComplianceGuideV3?command=Download&downloadType=Document&downloadId=70de0999-5451-43a3-9ef4-761e8fbfb1a3&tab=7027ead0-3d6b-11e9-b9e1-290b1eb4cdeb&docTab=7027ead0-3d6b-11e9-b9e1-290b1eb4cdeb_ISO_Reports) | A. 10.1 : contrôles de chiffrement <br> A. 18.1.5 : contrôles de chiffrement | 22 février 2020 |
| [ISO 27018 (Office 365)](https://servicetrust.microsoft.com/ViewPage/MSComplianceGuideV3?command=Download&downloadType=Document&downloadId=d7864d4f-e053-4cc4-a964-fa526d07c3be&tab=7027ead0-3d6b-11e9-b9e1-290b1eb4cdeb&docTab=7027ead0-3d6b-11e9-b9e1-290b1eb4cdeb_ISO_Reports) <br><br> [Déclaration de l’applicabilité](https://servicetrust.microsoft.com/ViewPage/MSComplianceGuide?command=Download&downloadType=Document&downloadId=8ee1e46b-2ada-4e7b-bb7d-4c55a8cb6fcd&docTab=4ce99610-c9c0-11e7-8c2c-f908a777fa4d_ISO_Reports) <br> [Certification](https://servicetrust.microsoft.com/ViewPage/MSComplianceGuideV3?command=Download&downloadType=Document&downloadId=43e89534-f48d-42ea-a7a7-3523ff516036&tab=7027ead0-3d6b-11e9-b9e1-290b1eb4cdeb&docTab=7027ead0-3d6b-11e9-b9e1-290b1eb4cdeb_ISO_Reports) | A. 11.6 : chiffrement des données personnelles transmises via des réseaux de transmission de données publiques | 22 février 2020 |
| [SOC 2 (Office 365)](https://servicetrust.microsoft.com/ViewPage/MSComplianceGuideV3?command=Download&downloadType=Document&downloadId=fa062990-e758-4ddc-ace3-7fb21a301d09&tab=7027ead0-3d6b-11e9-b9e1-290b1eb4cdeb&docTab=7027ead0-3d6b-11e9-b9e1-290b1eb4cdeb_SOC_/_SSAE_16_Rep-11e9-b9e1-290b1eb4cdeb_SOC_/_SSAE_16_Reports) | CA-44 : chiffrement des données en transit <br> CA-54 : chiffrement des données au repos <br> CA-62 : chiffrement de boîte aux lettres du client <br> CA-63 : suppression des données de clé client <br> CA-64 : clé client | 30 septembre 2019 |
| [SOC 3 (Office 365)](https://servicetrust.microsoft.com/ViewPage/MSComplianceGuideV3?command=Download&downloadType=Document&downloadId=9df8b99b-96ce-49a9-bff4-268031dcc9a6&tab=7027ead0-3d6b-11e9-b9e1-290b1eb4cdeb&docTab=7027ead0-3d6b-11e9-b9e1-290b1eb4cdeb_SOC_/_SSAE_16_Reports) | CUEC-16 : clés de chiffrement client <br> CUEC-17 : coffre-fort de clés client <br>  CUEC-18 : rotation des clés client| 30 septembre 2019 |
