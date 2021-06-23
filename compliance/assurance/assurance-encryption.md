---
title: Aperçu sur le chiffrement et la gestion des clés
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
hideEdit: true
ms.openlocfilehash: 5e46fdb5ddc3b1b80df0bcadf9054b9353a0dc8e
ms.sourcegitcommit: fb379d1110a9a86c7f9bab8c484dc3f4b3dfd6f0
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 06/23/2021
ms.locfileid: "53088643"
---
# <a name="encryption-and-key-management-overview"></a>Aperçu sur le chiffrement et la gestion des clés

## <a name="what-role-does-encryption-play-in-protecting-customer-content"></a>Quel rôle le chiffrement joue-t-il dans la protection du contenu client ?

La plupart des services cloud de Microsoft Business sont multi-clients, ce qui signifie que le contenu client peut être stocké sur le même matériel physique que celui des autres clients. Pour protéger la confidentialité du contenu client, Microsoft 365 chiffre toutes les données au repos et en transit avec certains des protocoles de chiffrement les plus forts et les plus sécurisés disponibles.

Le chiffrement ne remplace pas les contrôles d’accès forts. Microsoft 365 de contrôle d’accès ZSA (Zero Standing Access) protège le contenu des clients contre tout accès non autorisé par les employés de Microsoft. Le chiffrement complète le contrôle d’accès en protégeant la confidentialité du contenu client où qu’il soit stocké et en empêchant la lecture du contenu en transit entre les systèmes Microsoft 365 ou entre Microsoft 365 et le client.

## <a name="how-does-microsoft-365-encrypt-data-at-rest"></a>Comment chiffrer Microsoft 365 données au repos ?

Tout le contenu client Microsoft 365 est protégé par une ou plusieurs formes de chiffrement. Les serveurs Microsoft utilisent BitLocker pour chiffrer les lecteurs de disque contenant le contenu client au niveau du volume. Le chiffrement fourni par BitLocker protège le contenu client en cas de défaillances dans d’autres processus ou contrôles (par exemple, le contrôle d’accès ou le recyclage du matériel) qui pourraient entraîner un accès physique non autorisé aux disques contenant du contenu client.

Exchange Online, Microsoft Teams, SharePoint Online et OneDrive Entreprise également utiliser le chiffrement de service au niveau de la couche application pour chiffrer le contenu client. Le chiffrement de service fournit des fonctionnalités de protection et de gestion des droits en plus d’une protection de chiffrement forte. Il permet également la séparation entre les Windows d’exploitation et les données client stockées ou traitées par ces systèmes d’exploitation.

## <a name="how-does-microsoft-365-encrypt-data-in-transit"></a>Comment chiffrer Microsoft 365 données en transit ?

Microsoft 365 et services utilisent des protocoles de transport forts, tels que TLS, pour empêcher les personnes non autorisées d’espionner des données client lors de leur déplacement sur un réseau. Les messages électroniques en cours de livraison, les conversations en cours dans une réunion en ligne ou les fichiers répliqués entre des centres de données sont des exemples de données en transit.

Dans Microsoft 365, les données sont considérées comme « en transit » chaque fois que l’appareil d’un utilisateur communique avec un serveur Microsoft ou qu’un serveur Microsoft communique avec un autre serveur. Exchange Online, SharePoint Online, Microsoft Teams et Office Online utilisent toutes TLS pour s’assurer que les données restent confidentielles pendant leur transit.

## <a name="how-does-microsoft-365-manage-the-keys-used-for-encryption"></a>Comment gérer Microsoft 365 clés utilisées pour le chiffrement ?

Le chiffrement fort est aussi sécurisé que les clés utilisées pour chiffrer les données. Microsoft utilise ses propres certificats de sécurité pour chiffrer les connexions TLS pour les données en transit. Pour les données au repos, les volumes protégés par BitLocker sont chiffrés avec une clé de chiffrement de volume complète, qui est chiffrée avec une clé principale de volume, qui est à son tour liée au module de plateforme approuvé (TPM) sur le serveur. BitLocker utilise des algorithmes conformes FIPS pour s’assurer que les clés de chiffrement ne sont jamais stockées ou envoyées sur le réseau en clair.

Le chiffrement de service fournit une couche supplémentaire de chiffrement pour les données client au repos dans Exchange Online, Microsoft Teams, SharePoint Online et OneDrive Entreprise. Le chiffrement de service offre aux clients deux options de gestion des clés de chiffrement : les clés gérées par Microsoft ou la clé client. Lorsque vous utilisez des clés gérées par Microsoft, Microsoft 365 services génèrent et stockent automatiquement en toute sécurité les clés racine utilisées pour le chiffrement de service.

Les clients ayant besoin de contrôler leurs propres clés de chiffrement racine peuvent tirer parti du chiffrement de service avec la clé client. À l’aide de la clé client, les clients peuvent générer leurs propres clés de chiffrement à l’aide d’un module de service matériel (HSM) local ou d’Azure Key Vault (AKV). Les clés racine du client sont stockées dans AKV, où elles peuvent être utilisées comme racine de l’un des chaînes de clés qui chiffre les données ou fichiers de boîte aux lettres du client. Les clés racine client ne sont accessibles qu’indirectement par Microsoft 365 code de service pour le chiffrement des données et ne sont pas accessibles directement par les employés de Microsoft.

## <a name="related-external-regulations--certifications"></a>Réglementations externes associées & certifications

Les services en ligne de Microsoft sont régulièrement audités pour assurer la conformité avec les réglementations et certifications externes. Reportez-vous au tableau suivant pour la validation des contrôles liés au chiffrement et à la gestion des clés.

| **Audits externes** | **Section** | **Date de rapport la plus récente** |
|:--------------------|:------------|:-----------------------|
| [FedRAMP (Office 365)](https://compliance.microsoft.com/compliancemanager) | SC-8 : Confidentialité et intégrité de la transmission <br> SC-13 : Utilisation du chiffrement <br> SC-28 : Protection des informations au repos <br>  | 24 septembre 2020 |
| [ISO 27001/27002 (Office 365)](https://servicetrust.microsoft.com/ViewPage/MSComplianceGuideV3?command=Download&downloadType=Document&downloadId=8d625374-4f2d-49f8-9d37-a4281ba98222&tab=7027ead0-3d6b-11e9-b9e1-290b1eb4cdeb&docTab=7027ead0-3d6b-11e9-b9e1-290b1eb4cdeb_ISO_Reports) <br><br> [Déclaration d’applicabilité](https://servicetrust.microsoft.com/ViewPage/MSComplianceGuideV3?command=Download&downloadType=Document&downloadId=c0df4ce8-c77e-4183-84eb-c8688470d8b1&tab=7027ead0-3d6b-11e9-b9e1-290b1eb4cdeb&docTab=7027ead0-3d6b-11e9-b9e1-290b1eb4cdeb_ISO_Reports) <br> [Certification](https://servicetrust.microsoft.com/ViewPage/MSComplianceGuideV3?command=Download&downloadType=Document&downloadId=1e84a14a-2468-45ac-9412-5e53250d57ec&tab=7027ead0-3d6b-11e9-b9e1-290b1eb4cdeb&docTab=7027ead0-3d6b-11e9-b9e1-290b1eb4cdeb_ISO_Reports) | A.10.1 : Contrôles de chiffrement <br> A.18.1.5 : Contrôles de chiffrement | 20 avril 2021 |
| [ISO 27017 (Office 365)](https://servicetrust.microsoft.com/ViewPage/MSComplianceGuideV3?command=Download&downloadType=Document&downloadId=8d625374-4f2d-49f8-9d37-a4281ba98222&tab=7027ead0-3d6b-11e9-b9e1-290b1eb4cdeb&docTab=7027ead0-3d6b-11e9-b9e1-290b1eb4cdeb_ISO_Reports) <br><br> [Déclaration d’applicabilité](https://servicetrust.microsoft.com/ViewPage/MSComplianceGuideV3?command=Download&downloadType=Document&downloadId=c0df4ce8-c77e-4183-84eb-c8688470d8b1&tab=7027ead0-3d6b-11e9-b9e1-290b1eb4cdeb&docTab=7027ead0-3d6b-11e9-b9e1-290b1eb4cdeb_ISO_Reports) <br> [Certification](https://servicetrust.microsoft.com/ViewPage/MSComplianceGuideV3?command=Download&downloadType=Document&downloadId=70de0999-5451-43a3-9ef4-761e8fbfb1a3&tab=7027ead0-3d6b-11e9-b9e1-290b1eb4cdeb&docTab=7027ead0-3d6b-11e9-b9e1-290b1eb4cdeb_ISO_Reports) | A.10.1 : Contrôles de chiffrement <br> A.18.1.5 : Contrôles de chiffrement | 20 avril 2021 |
| [ISO 27018 (Office 365)](https://servicetrust.microsoft.com/ViewPage/MSComplianceGuideV3?command=Download&downloadType=Document&downloadId=8d625374-4f2d-49f8-9d37-a4281ba98222&tab=7027ead0-3d6b-11e9-b9e1-290b1eb4cdeb&docTab=7027ead0-3d6b-11e9-b9e1-290b1eb4cdeb_ISO_Reports) <br><br> [Déclaration d’applicabilité](https://servicetrust.microsoft.com/ViewPage/MSComplianceGuideV3?command=Download&downloadType=Document&downloadId=c0df4ce8-c77e-4183-84eb-c8688470d8b1&tab=7027ead0-3d6b-11e9-b9e1-290b1eb4cdeb&docTab=7027ead0-3d6b-11e9-b9e1-290b1eb4cdeb_ISO_Reports) <br> [Certification](https://servicetrust.microsoft.com/ViewPage/MSComplianceGuideV3?command=Download&downloadType=Document&downloadId=43e89534-f48d-42ea-a7a7-3523ff516036&tab=7027ead0-3d6b-11e9-b9e1-290b1eb4cdeb&docTab=7027ead0-3d6b-11e9-b9e1-290b1eb4cdeb_ISO_Reports) | A.11.6 : Chiffrement des données personnelles transmises sur les réseaux de transmission de données publics | 20 avril 2021 |
| [SOC 2 (Office 365)](https://servicetrust.microsoft.com/ViewPage/MSComplianceGuideV3?command=Download&downloadType=Document&downloadId=a73c1738-7892-42b7-acd3-87b6371c53f6&tab=7027ead0-3d6b-11e9-b9e1-290b1eb4cdeb&docTab=7027ead0-3d6b-11e9-b9e1-290b1eb4cdeb_SOC_%2F_SSAE_16_Reports) | CA-44 : Chiffrement des données en transit <br> CA-54 : chiffrement des données au repos <br> CA-62 : Chiffrement de boîte aux lettres de clé client <br> CA-63 : suppression des données de clé client <br> CA-64 : Clé client | 24 décembre 2020 |
| [SOC 3 (Office 365)](https://servicetrust.microsoft.com/ViewPage/MSComplianceGuideV3?command=Download&downloadType=Document&downloadId=274054e5-4968-48d2-bf94-9a8eda5d7a93&tab=7027ead0-3d6b-11e9-b9e1-290b1eb4cdeb&docTab=7027ead0-3d6b-11e9-b9e1-290b1eb4cdeb_SOC_%2F_SSAE_16_Reports) | CUEC-16 : Clés de chiffrement client <br> CUEC-17 : coffre de clés client <br>  CUEC-18 : rotation des clés client| 24 décembre 2020 |
