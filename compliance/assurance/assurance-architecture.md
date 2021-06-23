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
hideEdit: true
ms.openlocfilehash: 9af5296cce34db6362638f025f38315f2e1d7b05
ms.sourcegitcommit: fb379d1110a9a86c7f9bab8c484dc3f4b3dfd6f0
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 06/23/2021
ms.locfileid: "53088533"
---
# <a name="architecture-overview"></a>Vue d’ensemble de l’architecture

## <a name="what-is-microsoft-365"></a>Qu’est-ce que Microsoft 365 ?

Microsoft 365 est la version basée sur le cloud basée sur un abonnement de Office, Windows 10, Enterprise Mobility + Security et conformité. Microsoft 365 clients obtiennent des clients tels que Outlook et Windows, et ils bénéficient également des services que Microsoft héberge en leur nom, tels que Exchange Online, Microsoft Teams et SharePoint Online. Tous les composants du service sont régulièrement mis à jour dans le cadre du modèle d’abonnement, afin que nos clients utilisent un produit « persistant ». Microsoft gère l’infrastructure de service pour le compte des clients, ce qui signifie que Microsoft est responsable de la sécurisation de l’infrastructure qui stocke les données client.

En termes d’échelle, nous utilisons actuellement près d’un million d’ordinateurs pour Microsoft 365 services. L’infrastructure qui permet d’alimenter ces services varie considérablement selon le matériel propre au service et les environnements virtualisés dans Azure, Windows et Linux, ainsi que les plateformes multi-clients et dédiées. Microsoft 365 est une entreprise internationale et notre infrastructure est distribuée dans des centres de données dans le monde entier, ce qui permet à nos clients de répondre aux exigences de résidence et de souveraineté.

En bref, le service est complexe, s’exécute à grande échelle et nécessite des milliers d’ingénieurs Microsoft pour créer et maintenir. Nous avons pour priorité de préserver la sécurité de toute cette infrastructure.

## <a name="how-does-microsoft-365-ensure-isolation-between-customer-tenants"></a>Comment garantir Microsoft 365 isolation entre les clients ?

Les services cloud de Microsoft reposent sur l’hypothèse que tous les clients sont potentiellement présupposants pour tous les autres clients. Pour isoler correctement les clients les uns des autres, Microsoft implémente diverses technologies et contrôles d’isolation. Ces contrôles sont conçus pour protéger contre les fuites d’informations ou l’accès non autorisé aux données client entre les clients et pour empêcher que les actions d’un client n’affectent le service pour un autre client.

Le contenu client est logiquement isolé au sein Microsoft 365 clients utilisant Azure Active Directory (Azure AD). L'authentification des utilisateurs dans Microsoft 365 vérifie non seulement l'identité de l'utilisateur, mais aussi celle du locataire dont le compte utilisateur fait partie, ce qui empêche les utilisateurs d'accéder aux données en dehors de leur environnement de locataire. Pour compléter l’isolation logique d’Azure AD, le contenu client est toujours chiffré au repos et en transit. Les services individuels peuvent également fournir des couches supplémentaires d’isolation du client, telles que SharePoint isolation en ligne des données client dans des bases de données chiffrées distinctes.

## <a name="how-does-microsoft-365-engineer-resilient-services-that-avoid-single-points-of-failure"></a>Comment Microsoft 365 des services résilients qui évitent des points de défaillance simples ?

Microsoft conçoit et crée des services cloud pour optimiser la fiabilité et minimiser les effets négatifs sur les clients en cas de pannes et de défis liés aux opérations normales. Cette stratégie commence par la conception du réseau qui connecte nos centres de données distribués géographiquement. L’architecture réseau de Microsoft inclut des interconnexions directes et plusieurs chemins d’accès réseau. Microsoft 365 services tirent parti de cette redondance pour router automatiquement le trafic autour des défaillances afin d’améliorer la qualité du service.

Au niveau du service, la stratégie Microsoft 365 la résilience des logiciels hiérarchise la résilience des logiciels. Dans la mesure du possible, nos services sont déployés dans des configurations actives/actives avec une surveillance automatisée de l’état du service, ce qui permet au service de détecter et de récupérer de nombreux défauts et défaillances courants sans intervention humaine. Outre les configurations actives/actives, les services Microsoft 365 augmentent la tolérance de pannes en s’assurant que le service est déployé dans des zones d’erreur distinctes, ce qui empêche une panne dans une zone d’affecter la disponibilité des autres zones.

La résilience des données complète la résilience du service en protégeant l’intégrité et la disponibilité des données dans les services Microsoft 365. Nos services utilisent la redondance du stockage local et la redondance géographique pour répliquer des copies de données client dans différentes zones d’erreur. Si des données sont endommagées ou perdues dans une zone de défaillance, elles peuvent être accessibles dans une autre zone de défaillance sans perte de disponibilité. La vérification automatisée de l’intégrité restaure automatiquement les données touchées par de nombreux types d’altération physique ou logique. Microsoft 365 fournit également aux clients des outils pour restaurer des données supprimées ou modifiées accidentellement par le client dans Exchange Online et SharePoint Online.

## <a name="how-does-microsoft-365-track-dependencies-and-prevent-unauthorized-external-system-connections"></a>Comment suivre Microsoft 365 dépendances et empêcher les connexions système externe non autorisées ?

Microsoft 365 service identifient les composants système critiques et leurs dépendances dans le cadre de la gestion de la continuité d’activité. En outre, Microsoft 365 documents et suit toutes les connexions du système externe pour s’assurer que seules les connexions autorisées sont autorisées dans les configurations de pare-feu réseau. Microsoft 365 systèmes, dépendances et connexions externes sont documentés dans l’architecture de sécurité Microsoft 365 informations de l’Microsoft 365' L’architecture de sécurité des informations et les diagrammes de flux de données correspondants sont examinés et mis à jour chaque année au minimum, ainsi que chaque fois que des modifications importantes sont apportées au système.

Microsoft 365 architecture est validée régulièrement et automatiquement à l’aide d’outils basés sur le cloud pour vérifier l’alignement avec nos principes de sécurité et pour tester en permanence les fonctionnalités d’isolation et de résilience. La validation architecturale permet d’identifier automatiquement les instances où l’état actuel du service a dérivé de l’état souhaité, en signalant les écarts à réviser et à atténuer. L’objectif de la validation de l’architecture est de s’assurer que les fonctionnalités de sécurité de notre infrastructure de service continuent de fonctionner comme prévu.

## <a name="related-external-regulations--certifications"></a>Réglementations externes associées & certifications

Les services en ligne de Microsoft sont régulièrement audités pour assurer la conformité avec les réglementations et certifications externes. Reportez-vous au tableau suivant pour la validation des contrôles liés à l’architecture de Microsoft 365.

| **Audits externes** | **Section** | **Date de rapport la plus récente** |
|:--------------------|:------------|:-----------------------|
| [FedRAMP (Office 365)](https://compliance.microsoft.com/compliancemanager) | AC-4 : application du flux d’informations <br> CP-9 : Sauvegarde du système d’information <br> PL-8 : architecture de sécurité des informations <br> SC-7 : Protection des frontières <br> SC-22 : Architecture et approvisionnement | 24 septembre 2020 |
| [ISO 27001/27002 (Office 365)](https://servicetrust.microsoft.com/ViewPage/MSComplianceGuideV3?command=Download&downloadType=Document&downloadId=8d625374-4f2d-49f8-9d37-a4281ba98222&tab=7027ead0-3d6b-11e9-b9e1-290b1eb4cdeb&docTab=7027ead0-3d6b-11e9-b9e1-290b1eb4cdeb_ISO_Reports) <br><br> [Déclaration d’applicabilité](https://servicetrust.microsoft.com/ViewPage/MSComplianceGuideV3?command=Download&downloadType=Document&downloadId=c0df4ce8-c77e-4183-84eb-c8688470d8b1&tab=7027ead0-3d6b-11e9-b9e1-290b1eb4cdeb&docTab=7027ead0-3d6b-11e9-b9e1-290b1eb4cdeb_ISO_Reports) <br> [Certification](https://servicetrust.microsoft.com/ViewPage/MSComplianceGuideV3?command=Download&downloadType=Document&downloadId=1e84a14a-2468-45ac-9412-5e53250d57ec&tab=7027ead0-3d6b-11e9-b9e1-290b1eb4cdeb&docTab=7027ead0-3d6b-11e9-b9e1-290b1eb4cdeb_ISO_Reports) | A.6 : Organisation de la sécurité des informations <br> A.13.1 : Gestion de la sécurité du réseau <br> A.17.2 : Redondances | 20 avril 2021 |
| [ISO 27017 (Office 365)](https://servicetrust.microsoft.com/ViewPage/MSComplianceGuideV3?command=Download&downloadType=Document&downloadId=8d625374-4f2d-49f8-9d37-a4281ba98222&tab=7027ead0-3d6b-11e9-b9e1-290b1eb4cdeb&docTab=7027ead0-3d6b-11e9-b9e1-290b1eb4cdeb_ISO_Reports) <br><br> [Déclaration d’applicabilité](https://servicetrust.microsoft.com/ViewPage/MSComplianceGuideV3?command=Download&downloadType=Document&downloadId=c0df4ce8-c77e-4183-84eb-c8688470d8b1&tab=7027ead0-3d6b-11e9-b9e1-290b1eb4cdeb&docTab=7027ead0-3d6b-11e9-b9e1-290b1eb4cdeb_ISO_Reports) <br> [Certification](https://servicetrust.microsoft.com/ViewPage/MSComplianceGuideV3?command=Download&downloadType=Document&downloadId=70de0999-5451-43a3-9ef4-761e8fbfb1a3&tab=7027ead0-3d6b-11e9-b9e1-290b1eb4cdeb&docTab=7027ead0-3d6b-11e9-b9e1-290b1eb4cdeb_ISO_Reports) | A.6 : Organisation de la sécurité des informations <br> A.13.1 : Gestion de la sécurité du réseau | 20 avril 2021 |
| [SOC 1 (Office 365)](https://servicetrust.microsoft.com/ViewPage/MSComplianceGuideV3?command=Download&downloadType=Document&downloadId=90df3f9c-3aaf-4dbf-99d0-ca9f2991721b&tab=7027ead0-3d6b-11e9-b9e1-290b1eb4cdeb&docTab=7027ead0-3d6b-11e9-b9e1-290b1eb4cdeb_SOC_%2F_SSAE_16_Reports) | CA-37 : isolation du client <br> CA-49 : Stratégies de sauvegarde <br> CA-51 : Réplication des données | 24 décembre 2020 |
| [SOC 2 (Office 365)](https://servicetrust.microsoft.com/ViewPage/MSComplianceGuideV3?command=Download&downloadType=Document&downloadId=a73c1738-7892-42b7-acd3-87b6371c53f6&tab=7027ead0-3d6b-11e9-b9e1-290b1eb4cdeb&docTab=7027ead0-3d6b-11e9-b9e1-290b1eb4cdeb_SOC_%2F_SSAE_16_Reports) | CA-05 : Diagrammes de flux de données <br> CA-37 : isolation du client <br> CA-49 : Stratégies de sauvegarde <br> CA-51 : Réplication des données | 24 décembre 2020 |