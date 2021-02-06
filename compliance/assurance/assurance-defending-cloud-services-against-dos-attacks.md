---
title: Défense des services cloud Microsoft 365 contre les attaques par déni de service
description: Dans cet article, découvrez comment Microsoft défendre ses services cloud contre les attaques par déni de service (DoS).
ms.author: robmazz
author: robmazz
manager: laurawi
ms.reviewer: sosstah
audience: ITPro
ms.topic: article
ms.service: O365-seccomp
localization_priority: Normal
search.appverid:
- MET150
ms.collection:
- Strat_O365_IP
- M365-security-compliance
- MS-Compliance
f1.keywords:
- NOCSH
ms.custom: seo-marvel-apr2020
titleSuffix: Microsoft Service Assurance
ms.openlocfilehash: e632c1524d5cc8c21aec9dab3d95d285a3b8801e
ms.sourcegitcommit: 21ed42335efd37774ff5d17d9586d5546147241a
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 02/05/2021
ms.locfileid: "50120573"
---
# <a name="defending-microsoft-365-cloud-services-against-denial-of-service-attacks"></a>Défense des services cloud Microsoft 365 contre les attaques par déni de service

Les centres de données Microsoft sont protégés par une sécurité renforcée qui inclut l’périmètre de périmètre, les caméras vidéo, le personnel de sécurité et les entrées sécurisées qui utilisent la biométrie, la carte à puce et l’authentification multifacteur. La sécurité de défense en profondeur continue dans chaque zone de l’installation et à chaque unité de serveur physique. Microsoft [Cloud Infrastructure and Operations Group](https://www.microsoft.com/cloud-platform/global-datacenters) fournit l’infrastructure de base et les technologies fondamentales pour nos services cloud. Nos centres de données sont conformes aux normes du secteur pour la sécurité physique et la fiabilité et sont gérés, surveillés et administrés par le personnel des opérations de Microsoft.

Pour protéger davantage nos services cloud, Microsoft fournit un système de défense DDoS qui fait partie des processus de surveillance et de test de pénétration continus de Microsoft Azure. Le système de défense Azure DDoS est conçu non seulement pour résister aux attaques en provenance de l’extérieur, mais aussi d’autres locataires Azure. Azure utilise des techniques standard de détection et d’atténuation telles que les cookies SYN, la limite de débit et les limites de connexion pour se protéger contre les attaques DDoS.

Les services cloud de Microsoft sont soumis à la menace d’attaques provenant de plusieurs sources. Pour atténuer et protéger contre les diverses menaces DoS, un système de détection et d’atténuation des menaces Azure hautement évolutif et dynamique a été développé et implémenté dans le but principal de protéger l’infrastructure sous-jacente contre les attaques DoS et d’empêcher les interruptions de service pour les clients des services cloud. Le système de prévention Azure DoS protège le trafic entrant, sortant et de région à région.

La plupart des attaques DoS lancées contre des cibles au niveau des couches Réseau (L3) et Transport (L4) du modèle OSI [(Open Systems Interconnection).](/windows-hardware/drivers/network/windows-network-architecture-and-the-osi-model) Les attaques dirigées vers les couches L3 et L4 sont conçues pour inonder une interface réseau ou un service avec un trafic d’attaque pour submerger les ressources et refuser la possibilité de répondre au trafic légitime. Plus précisément, les attaques L3 et L4 tentent soit de saturer la capacité des liaisons réseau, des périphériques ou des services, soit de saturer les processeurs des serveurs ou des machines virtuelles qui prend en charge une application.

Pour se prémunir contre les attaques L3 et L4, Microsoft a conçu, développé et déployé une solution visant spécifiquement à protéger l’infrastructure et les cibles des clients qui sont la cible d’attaques en protégeant ces couches. La protection de l’infrastructure garantit que le trafic d’attaque destiné à un client n’entraîne pas de dommages collatéraux ni de dégradation de la qualité de service réseau pour d’autres clients. La solution utilise les données d’échantillonnage du trafic des routeurs de centres de données. Ces données sont analysées par un service de surveillance réseau pour détecter les attaques. Lorsqu’une attaque est détectée, des mécanismes de défense automatisés démarrent.

## <a name="application-level-defenses"></a>Application-Level défenses
Les équipes d’ingénierie Microsoft suivent les normes rigoureuses définies par [Microsoft Operational Security Assurance](https://www.microsoft.com/SDL/OperationalSecurityAssurance) pour protéger les données client. Les services cloud de Microsoft sont intentionnellement conçus pour prendre en charge une charge très élevée, ainsi que pour protéger et atténuer contre les attaques DoS au niveau de l’application. Nous avons implémenté une architecture mise à l’échelle dans laquelle les services sont distribués dans plusieurs centres de données globaux avec des fonctionnalités d’isolation et de limitation régionales dans certaines charges de travail.

Le pays ou la région de chaque client, que l’administrateur du client identifie pendant la configuration initiale des services, détermine l’emplacement de stockage principal pour les données de ce client. Les données client sont répliquées entre des centres de données redondants conformément à une stratégie principale/de sauvegarde. Un centre de données principal héberge le logiciel d’application ainsi que toutes les données client principales en cours d’exécution sur le logiciel. Un centre de données de sauvegarde fournit leover automatique. Si le centre de données principal cesse de fonctionner pour une raison quelconque, les demandes sont redirigées vers la copie du logiciel et des données client dans le centre de données de sauvegarde. À tout moment, les données client peuvent être traitées dans le centre de données principal ou de sauvegarde. La répartition des données entre plusieurs centres de données réduit la surface concernée au cas où un centre de données serait concerné. En outre, les services du centre de données affecté peuvent être rapidement redirigés vers le centre de données secondaire comme l’un des mécanismes de récupération, et inversement (redirigés vers le centre de données principal une fois le service restauré).

Les charges de travail individuelles incluent des fonctionnalités intégrées qui gèrent l’utilisation des ressources. Par exemple, les mécanismes de limitation dans Exchange Online et SharePoint Online font partie d’une approche à plusieurs couches pour la défense contre les attaques par dos. La limitation pour les utilisateurs d’Exchange Online est basée sur le niveau de ressources consommées par l’utilisateur final, que les ressources soient dans Active Directory, dans la boutique d’informations Exchange Online ou ailleurs. Un budget est alloué à chaque client pour limiter les ressources consommées par un utilisateur. La limitation d’Exchange Online pour l’activité des utilisateurs et les composants système est basée sur la gestion de la charge [de travail.](https://technet.microsoft.com/library/jj150503(v=exchg.150).aspx) Une charge de travail Exchange Online est une fonctionnalité, un protocole ou un service Exchange Online qui a été explicitement défini à des fins de gestion des ressources système Exchange Online. Chaque charge de travail Exchange Online nécessite des ressources système telles que le processeur, les opérations de base de données de boîtes aux lettres ou les demandes Active Directory pour effectuer des demandes utilisateur ou un travail en arrière-plan. Parmi les exemples de charges de travail Exchange Online, citons Outlook sur le web, Exchange ActiveSync, la migration de boîtes aux lettres et les assistants de boîte aux lettres. Les administrateurs clients peuvent gérer les paramètres de limitation de la gestion de la charge de travail Exchange pour les utilisateurs avec l’Environnement de ligne de ligne de contrôle Exchange Management Shell. Plusieurs formes de limitation ont été implémentées dans Exchange Online, notamment PowerShell, les services web Exchange, POP et IMAP, Exchange ActiveSync, les connexions d’appareils mobiles, les destinataires, etc. Bien que les administrateurs de déploiements Exchange locaux peuvent configurer des stratégies de limitation, les administrateurs ne peuvent pas configurer de stratégies de limitation pour Exchange Online.

Le déclencheur le plus courant de limitation dans SharePoint Online est le code de modèle objet côté client (CSOM) qui effectue trop d’actions à une fréquence trop élevée. Avec le CSOM, de nombreuses actions peuvent être effectuées avec une seule demande, ce qui peut dépasser les limites d’utilisation et provoquer une limitation par utilisateur.

Quelle que soit l’activité qui peut entraîner une limitation, lorsqu’un utilisateur dépasse les limites d’utilisation, SharePoint Online limite les autres demandes provenant de ce compte d’utilisateur, généralement pendant une courte période. Pendant qu’une limitation utilisateur est en vigueur, toutes les actions de cet utilisateur sont limitées jusqu’à l’expiration de la limitation, selon les critères suivants :
- Pour les demandes effectuées par l’utilisateur directement dans un navigateur, SharePoint Online redirige vers une page d’informations de limitation et les demandes échouent.
- Pour toutes les autres demandes, y compris les appels CSOM, SharePoint Online renvoie le code d’état HTTP 429 (« trop de demandes ») et les demandes échouent.

Si le processus en cause continue de dépasser les limites d’utilisation, SharePoint Online peut bloquer complètement le processus et renvoyer le code d’état HTTP 503 ( « service indisponible »).

## <a name="vulnerability-and-penetration-testing"></a>Test de vulnérabilité et de pénétration
Microsoft utilise de nombreuses [technologies](https://www.microsoft.com/trustcenter/security/threatmanagement) et pratiques de sécurité pour protéger son [infrastructure cloud](https://blogs.technet.microsoft.com/hybridcloud/2015/05/05/protecting-your-datacenter-and-cloud-from-emerging-threats/) et ses réseaux locaux contre les menaces modernes et sophistiquées, notamment l’utilisation de composants et de services anti-programme malveillant pour les services cloud, les machines virtuelles (VM) et d’autres systèmes. L’analyse avancée des menaces, qui surveille les modèles d’utilisation normaux pour les réseaux, les systèmes et les utilisateurs, et utilise l’apprentissage automatique pour faire état de tout comportement hors de l’ordinaire et des tests de pénétration réguliers.

En plus d’effectuer nos propres tests de pénétration et d’offrir à nos clients un programme de test de pénétration unifié microsoft [Cloud,](https://technet.microsoft.com/mt784683)nous nous engageons également avec des professionnels de la sécurité tiers qui effectuent régulièrement des évaluations de vulnérabilité et des tests de pénétration sur nos services cloud. Les rapports de ces évaluations de vulnérabilité tiers sont [](https://aka.ms/STP) disponibles pour téléchargement à partir des portails d’confiance de service et [d’assurance](https://aka.ms/ServiceAssurance) service.
