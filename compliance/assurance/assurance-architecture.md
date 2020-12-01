---
title: Vue d’ensemble de l’architecture
description: En savoir plus sur l’architecture dans Microsoft 365
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
ms.openlocfilehash: 7ceceb59d0afcbc72fac9758f3de500082b8b365
ms.sourcegitcommit: 626b0076d133e588cd28598c149a7f272fc18bae
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 11/30/2020
ms.locfileid: "49507119"
---
# <a name="architecture-overview"></a>Vue d’ensemble de l’architecture

## <a name="what-is-microsoft-365"></a>Qu’est-ce que Microsoft 365 ?

Microsoft 365 est la version en nuage, basée sur les abonnements d’Office, Windows 10, Enterprise Mobility + Security et la conformité. Les clients Microsoft 365 obtiennent des clients tels qu’Outlook et Windows, et ils bénéficient également des services hébergés par Microsoft pour leur compte, comme Exchange Online, Microsoft teams et SharePoint Online. Tous les composants du service sont régulièrement mis à jour dans le cadre du modèle d’abonnement, afin que nos clients aient un produit « persistant ». Microsoft gère l’infrastructure de service pour le compte de clients, ce qui signifie que Microsoft est responsable de la sécurisation de l’infrastructure qui stocke les données client.

En ce qui concerne l’envergure, nous utilisons actuellement près d’un million d’ordinateurs pour alimenter les services Microsoft 365. L’infrastructure qui alimente ces services varie largement en fonction du matériel et des environnements virtualisés spécifiques aux services dans Azure, Windows et Linux, ainsi qu’aux plateformes mutualisées et dédiées. Microsoft 365 est une entreprise internationale et notre infrastructure est distribuée dans des centres de données dans le monde entier, ce qui permet à nos clients de répondre aux exigences de résidence et de souveraineté.

En bref, le service est complexe, s’exécute à un incroyable niveau d’envergure et nécessite des milliers d’ingénieurs Microsoft pour créer et gérer. Notre priorité principale est de maintenir la sécurité de toute cette infrastructure.

## <a name="how-does-microsoft-365-ensure-isolation-between-customer-tenants"></a>Comment Microsoft 365 garantit-il l’isolation entre les locataires des clients ?

Les services Cloud de Microsoft sont construits en partant du principe que tous les clients sont potentiellement hostiles à tous les autres clients. Pour isoler correctement les clients les uns des autres, Microsoft implémente plusieurs contrôles et technologies d’isolation. Ces contrôles sont conçus pour vous protéger contre la fuite d’informations ou l’accès non autorisé aux données client sur les différents clients et pour empêcher les actions d’un client d’affecter le service à un autre client.

Le contenu client est logiquement isolé au sein des clients Microsoft 365 utilisant Azure Active Directory (Azure AD). L'authentification des utilisateurs dans Microsoft 365 vérifie non seulement l'identité de l'utilisateur, mais aussi celle du locataire dont le compte utilisateur fait partie, ce qui empêche les utilisateurs d'accéder aux données en dehors de leur environnement de locataire. Pour compléter l’isolation logique d’Azure AD, le contenu du client est toujours chiffré au repos et en transit. Les services individuels peuvent également fournir des couches supplémentaires d’isolation de client, telles que l’isolation SharePoint Online des données client dans des bases de données séparées et chiffrées.

## <a name="how-does-microsoft-365-engineer-resilient-services-that-avoid-single-points-of-failure"></a>Comment Microsoft 365 Engineer a-t-il des services résistants qui évitent les points de défaillance uniques ?

Microsoft conçoit et crée des services Cloud pour optimiser la fiabilité et réduire les effets négatifs sur les pannes et les défis liés aux opérations normales. Cette stratégie commence par la conception du réseau qui connecte nos centres de distribution géographiquement dispersés. L’architecture réseau de Microsoft comprend des interconnexions directes et plusieurs chemins d’accès réseau. Les services Microsoft 365 tirent parti de cette redondance pour acheminer automatiquement le trafic entourant les défaillances afin d’améliorer la qualité du service.

Au niveau du service, la stratégie de résilience de Microsoft 365 accorde la priorité à la résilience logicielle. Dans la mesure du possible, nos services sont déployés dans des configurations actives/actives avec surveillance automatisée de l’état du service, ce qui permet au service de détecter et de résoudre de nombreuses défaillances et échecs courants sans intervention humaine. En plus des configurations actives/actives, les services Microsoft 365 augmentent la tolérance de panne en s’assurant que le service est déployé dans des zones d’erreur distinctes, ce qui empêche une erreur dans une zone d’affecter la disponibilité d’autres zones.

La résilience des données complète la résilience du service en protégeant l’intégrité et la disponibilité des données dans les services Microsoft 365. Nos services utilisent la redondance de stockage local et la redondance géographique pour répliquer des copies des données des clients dans différentes zones d’erreur. Si des données sont endommagées ou perdues dans une zone de défaillance, elles peuvent être accessibles dans une autre zone de défaillance sans perte de disponibilité. La vérification de l’intégrité automatique restaure automatiquement les données affectées par de nombreux types d’altération physique ou logique. Microsoft 365 fournit également aux clients des outils permettant de restaurer des données accidentellement supprimées ou modifiées par le client dans Exchange Online et SharePoint Online.

## <a name="how-does-microsoft-365-track-dependencies-and-prevent-unauthorized-external-system-connections"></a>Comment Microsoft 365 effectue le suivi des dépendances et empêche les connexions système externes non autorisées ?

Les équipes de service Microsoft 365 identifient les composants système critiques et leurs dépendances dans le cadre de la gestion de la continuité des opérations. De plus, Microsoft 365 documente et effectue le suivi de toutes les connexions de systèmes externes pour garantir que seules les connexions autorisées sont autorisées dans les configurations de pare-feu réseau. Les systèmes Microsoft 365, les dépendances et les connexions externes sont documentés dans l’architecture de sécurité des informations de Microsoft 365. L’architecture de sécurité des informations et les diagrammes de flux de données correspondants sont examinés et mis à jour chaque année au minimum, ainsi que chaque fois que des modifications importantes sont apportées au système.

L’architecture de Microsoft 365 est validée régulièrement et automatiquement à l’aide d’outils basés sur le Cloud pour vérifier l’alignement avec nos principes de sécurité et pour tester en continu les fonctionnalités d’isolation et de résilience. La validation de l’architecture permet d’identifier automatiquement les instances dans lesquelles l’état actuel du service est dérivant de l’état souhaité, en marquant les écarts de révision et d’atténuation. L’objectif de la validation de l’architecture est de s’assurer que les fonctionnalités de sécurité de notre infrastructure de service continuent de fonctionner comme prévu.

## <a name="related-external-regulations--certifications"></a>Certifications & des réglementations externes connexes

Les services en ligne de Microsoft sont régulièrement vérifiés pour la conformité aux réglementations et aux certifications externes. Consultez le tableau suivant pour valider les contrôles liés à l’architecture de Microsoft 365.

| **Audits externes** | **Section** | **Date du dernier rapport** |
|:--------------------|:------------|:-----------------------|
| [FedRAMP (Office 365)](https://compliance.microsoft.com/compliancemanager) | AC-4 : application du flux d’informations <br> CP-9 : sauvegarde du système d’information <br> PL-8 : architecture de sécurité des informations <br> SC-7 : protection des limites <br> SC-22 : architecture et mise en service | 24 septembre 2020 |
| [ISO 27001/27002 (Office 365)](https://servicetrust.microsoft.com/ViewPage/MSComplianceGuideV3?command=Download&downloadType=Document&downloadId=d7864d4f-e053-4cc4-a964-fa526d07c3be&tab=7027ead0-3d6b-11e9-b9e1-290b1eb4cdeb&docTab=7027ead0-3d6b-11e9-b9e1-290b1eb4cdeb_ISO_Reports) <br><br> [Déclaration de l’applicabilité](https://servicetrust.microsoft.com/ViewPage/MSComplianceGuide?command=Download&downloadType=Document&downloadId=8ee1e46b-2ada-4e7b-bb7d-4c55a8cb6fcd&docTab=4ce99610-c9c0-11e7-8c2c-f908a777fa4d_ISO_Reports) <br> [Certification](https://servicetrust.microsoft.com/ViewPage/MSComplianceGuideV3?command=Download&downloadType=Document&downloadId=1e84a14a-2468-45ac-9412-5e53250d57ec&tab=7027ead0-3d6b-11e9-b9e1-290b1eb4cdeb&docTab=7027ead0-3d6b-11e9-b9e1-290b1eb4cdeb_ISO_Reports) | A. 6 : Organisation de la sécurité des informations <br> A. 13.1 : gestion de la sécurité réseau <br> A. 17.2 : redondances | 22 février 2020 |
| [ISO 27017 (Office 365)](https://servicetrust.microsoft.com/ViewPage/MSComplianceGuideV3?command=Download&downloadType=Document&downloadId=d7864d4f-e053-4cc4-a964-fa526d07c3be&tab=7027ead0-3d6b-11e9-b9e1-290b1eb4cdeb&docTab=7027ead0-3d6b-11e9-b9e1-290b1eb4cdeb_ISO_Reports) <br><br> [Déclaration de l’applicabilité](https://servicetrust.microsoft.com/ViewPage/MSComplianceGuide?command=Download&downloadType=Document&downloadId=8ee1e46b-2ada-4e7b-bb7d-4c55a8cb6fcd&docTab=4ce99610-c9c0-11e7-8c2c-f908a777fa4d_ISO_Reports) <br> [Certification](https://servicetrust.microsoft.com/ViewPage/MSComplianceGuideV3?command=Download&downloadType=Document&downloadId=70de0999-5451-43a3-9ef4-761e8fbfb1a3&tab=7027ead0-3d6b-11e9-b9e1-290b1eb4cdeb&docTab=7027ead0-3d6b-11e9-b9e1-290b1eb4cdeb_ISO_Reports) | A. 6 : Organisation de la sécurité des informations <br> A. 13.1 : gestion de la sécurité réseau | 22 février 2020 |
| [SOC 1 (Office 365)](https://servicetrust.microsoft.com/ViewPage/MSComplianceGuideV3?command=Download&downloadType=Document&downloadId=b07c0f7b-6bd5-4544-8255-7a5f14bf914a&tab=7027ead0-3d6b-11e9-b9e1-290b1eb4cdeb&docTab=7027ead0-3d6b-11e9-b9e1-290b1eb4cdeb_SOC_/_SSAE_16_Reports) | CA-37 : isolation du client <br> CA-49 : stratégies de sauvegarde <br> CA-51 : réplication des données | 30 septembre 2019 |
| [SOC 2 (Office 365)](https://servicetrust.microsoft.com/ViewPage/MSComplianceGuideV3?command=Download&downloadType=Document&downloadId=fa062990-e758-4ddc-ace3-7fb21a301d09&tab=7027ead0-3d6b-11e9-b9e1-290b1eb4cdeb&docTab=7027ead0-3d6b-11e9-b9e1-290b1eb4cdeb_SOC_/_SSAE_16_Rep-11e9-b9e1-290b1eb4cdeb_SOC_/_SSAE_16_Reports) | CA-05 : diagrammes de flux de données <br> CA-37 : isolation du client <br> CA-49 : stratégies de sauvegarde <br> CA-51 : réplication des données | 30 septembre 2019 |