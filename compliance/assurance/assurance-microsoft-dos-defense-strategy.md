---
title: Stratégie de défense par déni de service Microsoft 365
description: Dans cet article, vous trouverez une vue d’ensemble de la stratégie de défense Microsoft pour les attaques par déni de service (DoS).
ms.author: robmazz
author: robmazz
manager: laurawi
ms.reviewer: sosstah
audience: ITPro
ms.topic: article
ms.service: O365-seccomp
localization_priority: None
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
hideEdit: true
ms.openlocfilehash: 5776b3eb6c0b79b5f272d6e24dd8680967ca2eb4
ms.sourcegitcommit: 024137a15ab23d26cac5ec14c36f3577fd8a0cc4
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 04/01/2021
ms.locfileid: "51496953"
---
# <a name="microsoft-365-denial-of-service-defense-strategy"></a>Stratégie de défense par déni de service Microsoft 365

## <a name="core-principles-of-defense-against-denial-of-service-attacks"></a>Principes fondamentaux de défense contre les attaques par déni de service

Il existe trois principes fondamentaux lors de la défense contre les attaques par déni de service (DoS) basées sur le réseau : les attaques par déni de service, la détection et l’atténuation. Cette situation se produit avant la détection et la détection doit avoir lieu avant que l’atténuation puisse commencer. Si même une petite attaque DoS ne peut pas être assimilée, les services ne survivront pas suffisamment longtemps pour que l’attaque soit détectée. En détectant une attaque avant que le système ne soit submergé, les défenseurs peuvent implémenter un plan de réponse.

La formule suivante vous aide à approximativement le temps d’impact d’une attaque par dos :

  **Capacité maximale (en octets/s) / Taux de croissance (en octets/s) = temps d’impact (en secondes)**

Si le délai de détection est plus long que le délai d’impact, l’attaque par le système DoS réussira probablement. Si le délai de détection est inférieur à l’impact dans le temps, les services attaquants doivent rester en ligne et accessibles si les stratégies d’atténuation réussissent.

Par conséquent, il existe deux stratégies principales pour la défense contre les attaques DoS :

- Augmenter la capacité pour augmenter le plafond de capacité maximale (ce qui permet à son tour de détecter une attaque) ; ou
- Diminuer le temps de détection d’une attaque.

L’un des avantages en matière de sécurité de l’utilisation des services cloud de Microsoft est la façon dont les services Microsoft à grande échelle fournissent une protection réseau renforcée aux clients cloud d’une manière rentable. Même à grande échelle, il doit y avoir un équilibre entre l’équipement, la détection et l’atténuation. Pour trouver cet équilibre, Microsoft étudie les taux de croissance des attaques pour estimer la quantité de services Microsoft à assimiler.

## <a name="denial-of-service-defense-strategy"></a>Stratégie de refus d’attaque de service

La stratégie de Microsoft pour se défendre contre les attaques DoS basées sur le réseau est unique en raison de notre échelle et de notre empreinte globale. Cette échelle permet à Microsoft d’utiliser des stratégies et des techniques qui ne sont pas disponibles pour la plupart des autres organisations. La base de notre stratégie DoS est notre présence globale. Microsoft s’engage auprès de fournisseurs Internet, de fournisseurs d’homologues (publics et privés) et de sociétés privées dans le monde entier. Cet engagement offre à Microsoft une présence Internet importante et permet à Microsoft d’assimiler les attaques sur une grande surface.

À mesure que la capacité des serveurs Edge de Microsoft s’est accrue au fil du temps, l’importance des attaques contre les bords individuels a considérablement diminué. En raison de cette diminution, Microsoft a séparé les composants de détection et d’atténuation de son système de prévention DoS. Microsoft déploie des systèmes de détection à plusieurs niveaux dans les centres de données régionaux pour détecter les attaques plus proches de leurs points de saturation tout en conservant l’atténuation globale sur les serveurs edge. Cette stratégie garantit que les services Microsoft peuvent gérer plusieurs attaques simultanées.

L’une des défenses les plus efficaces et les moins coûteuses employées par Microsoft contre les attaques dos consiste à réduire les surfaces d’attaque de service. Le trafic indésirable est abandonné au niveau du réseau au lieu d’analyser, de traiter et de nettoyer les données en ligne.

Dans l’interface avec le réseau public, Microsoft utilise des périphériques de sécurité à usage spécial pour les fonctions de pare-feu, de traduction d’adresses réseau et de filtrage IP. Microsoft utilise également le routage ECMP (Equal-Cost Multi-Path) global. Le routage ECMP global est une infrastructure réseau permettant de s’assurer qu’il existe plusieurs chemins globaux pour atteindre un service. Avec plusieurs chemins d’accès à chaque service, les attaques DoS sont limitées à la région d’où provient l’attaque. Les autres régions ne doivent pas être affectées par l’attaque, car les utilisateurs finaux utilisent d’autres chemins d’accès pour accéder au service dans ces régions. Microsoft a également développé des systèmes de corrélation et de détection DoS internes qui utilisent des données de flux, des mesures de performances et d’autres informations pour détecter rapidement les attaques dos.

Pour protéger davantage nos services cloud, Microsoft 365 utilise un système de défense par déni de service distribué intégré aux processus de surveillance et de test de pénétration continus de Microsoft Azure. Le système de défense Azure DDoS est conçu non seulement pour résister aux attaques externes, mais aussi aux attaques d’autres locataires Azure. Azure utilise des techniques standard de détection et d’atténuation telles que les cookies SYN, la limite de débit et les limites de connexion pour se protéger contre les attaques DDoS. Pour prendre en charge nos protections automatisées, une équipe de réponse aux incidents DoS entre charges de travail identifie les rôles et responsabilités au sein des équipes, les critères d’escalade et les protocoles de gestion des incidents entre les équipes concernées.

La plupart des attaques DoS lancées contre des cibles se font au niveau des couches Réseau (L3) et Transport (L4) du modèle OSI [(Open Systems Interconnection).](/windows-hardware/drivers/network/windows-network-architecture-and-the-osi-model) Les attaques dirigées vers les couches L3 et L4 sont conçues pour inonder une interface réseau ou un service avec un trafic d’attaque pour submerger les ressources et refuser la possibilité de répondre au trafic légitime. Pour se prémunir contre les attaques L3 et L4, les solutions DoS de Microsoft utilisent les données d’échantillonnage du trafic des routeurs de centres de données pour protéger l’infrastructure et les cibles des clients. Les données d’échantillonnage du trafic sont analysées par un service de surveillance du réseau pour détecter les attaques. Lorsqu’une attaque est détectée, des mécanismes de défense automatisés sont lancés pour atténuer l’attaque et s’assurer que le trafic d’attaques dirigé vers un client n’entraîne pas de dommages collatéraux ni de dégradation de la qualité de service du réseau pour les autres clients.

## <a name="application-level-defenses"></a>Défenses au niveau de l’application

Les équipes d’ingénierie Microsoft suivent les normes rigoureuses définies par [Microsoft Operational Security Assurance](https://www.microsoft.com/SDL/OperationalSecurityAssurance) pour protéger les données client. Les services cloud de Microsoft sont intentionnellement conçus pour prendre en charge des charges élevées, ce qui permet de se protéger contre les attaques DoS au niveau de l’application. L’architecture avec montée en charge de Microsoft 365 distribue des services dans plusieurs centres de données globaux avec une isolation régionale et des fonctionnalités de limitation spécifiques à la charge de travail pour les charges de travail pertinentes.

Le pays ou la région de chaque client, que l’administrateur du client identifie pendant la configuration initiale des services, détermine l’emplacement de stockage principal pour les données de ce client. Les données client sont répliquées entre des centres de données redondants conformément à une stratégie principale/de sauvegarde. Un centre de données principal héberge le logiciel d’application ainsi que toutes les données client principales en cours d’exécution sur le logiciel. Un centre de données de sauvegarde fournit leover automatique. Si le centre de données principal cesse de fonctionner pour une raison quelconque, les demandes sont redirigées vers la copie du logiciel et des données client dans le centre de données de sauvegarde. À tout moment, les données client peuvent être traitées dans le centre de données principal ou de sauvegarde. La répartition des données entre plusieurs centres de données réduit la surface concernée au cas où un centre de données serait concerné. En outre, les services dans le centre de données affecté peuvent être rapidement redirigés vers le centre de données secondaire pour maintenir la disponibilité pendant une attaque et redirigés vers le centre de données principal une fois qu’une attaque a été atténuée.

En tant qu’autre prévention contre les attaques DoS, les charges de travail individuelles incluent des fonctionnalités intégrées qui gèrent l’utilisation des ressources. Par exemple, les mécanismes de limitation dans Exchange Online et SharePoint Online font partie d’une approche à plusieurs couches pour la défense contre les attaques par dos.
