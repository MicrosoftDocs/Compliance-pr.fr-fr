---
title: Sécurité réseau
description: En savoir plus sur la sécurité réseau dans Microsoft 365
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
ms.openlocfilehash: e246cc3c84a17fe697baea29eda285599832b0fa
ms.sourcegitcommit: 7a5b6bc58fc4613b38f3fda20aebee5cec6a5730
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/08/2021
ms.locfileid: "49787426"
---
# <a name="network-security-overview"></a>Aperçu sur la sécurité réseau

## <a name="how-does-microsoft-365-secure-the-network-boundary"></a>Comment Microsoft 365 sécurisation-t-il la limite du réseau ?

Microsoft 365 utilise plusieurs stratégies pour sécuriser ses limites réseau, notamment la détection et la prévention automatisées des attaques basées sur le réseau, les périphériques de pare-feu spécialisés et Exchange Online Protection (EOP) pour la protection contre le courrier indésirable et les programmes malveillants. En outre, Microsoft 365 sépare son environnement de production en segments réseau logiquement isolés, avec uniquement les communications nécessaires autorisées entre les segments. Le trafic réseau est sécurisé à l’aide de pare-feu réseau supplémentaires aux points de limite pour vous aider à détecter, prévenir et atténuer les attaques réseau.

## <a name="how-does-microsoft-365-defend-against-ddos-attacks"></a>Comment Microsoft 365 se défendre contre les attaques DDoS ?

La présence Internet importante de Microsoft l’isole des effets négatifs de nombreuses attaques par déni de service distribué (DDoS). Les instances distribuées de chaque service Microsoft 365 et plusieurs itinéraires vers chaque service limitent l’impact des attaques DDoS contre le système. Cette redondance améliore la capacité de Microsoft 365 à assimiler les attaques DDoS et augmente le temps disponible pour détecter et atténuer les attaques DDoS avant qu’elles n’impactent la disponibilité du service.

Outre l’architecture système redondante de Microsoft, Microsoft utilise des outils sophistiqués de détection et d’atténuation pour répondre aux attaques DDoS. Les pare-feu à usage spécial surveillent et larmentent le trafic indésirable avant de traverser la frontière dans le réseau, ce qui réduit la contrainte sur les systèmes situés à l’intérieur de la limite réseau. Pour protéger davantage nos services cloud, Microsoft utilise un système de défense DDoS déployé dans le cadre de Microsoft Azure. Le système de défense Azure DDoS est conçu pour résister aux attaques en provenance de l’extérieur et d’autres locataires Azure.

## <a name="how-does-microsoft-365-protect-users-against-spam-and-malware-being-uploaded-or-sent-through-online-services"></a>Comment Microsoft 365 protège-t-il les utilisateurs contre le courrier indésirable et les programmes malveillants téléchargés ou envoyés via des services en ligne ?

Microsoft 365 crée une protection contre les programmes malveillants dans des services qui peuvent être des vecteurs de code malveillant, tels qu’Exchange Online et SharePoint Online. Exchange Online Protection (EOP) analyse tous les messages électroniques et pièces jointes des messages électroniques à la recherche de programmes malveillants lors de leur entrée et de leur sortie du système, empêchant ainsi la livraison des messages infectés et des pièces jointes. Le filtrage avancé du courrier indésirable est automatiquement appliqué aux messages entrants et sortants pour empêcher les organisations clientes de recevoir et d’envoyer du courrier indésirable. Cette couche de protection protège contre les attaques qui tirez parti de messages électroniques non sollicités ou non autorisés, tels que les attaques par hameçonnage. SharePoint Online utilise le même moteur de détection de virus pour analyser de manière sélective les fichiers téléchargés à la recherche de programmes malveillants. Si un fichier est marqué comme infecté, les utilisateurs ne peuvent pas télécharger ou synchroniser le fichier pour protéger les points de terminaison du client.

## <a name="related-external-regulations--certifications"></a>Réglementations externes associées & certifications

Les services en ligne de Microsoft sont régulièrement audités pour assurer la conformité avec les réglementations et certifications externes. Reportez-vous au tableau suivant pour la validation des contrôles liés à la sécurité du réseau.

| **Audits externes** | **Section** | **Date de rapport la plus récente** |
|:--------------------|:------------|:-----------------------|
| [FedRAMP (Office 365)](https://compliance.microsoft.com/compliancemanager) | SC-5 : protection contre les dénis de service <br> SC-7 : Protection des frontières <br> SI-2 : correction des failles <br> SI-3 : Protection contre le code malveillant <br> SI-8 : Protection contre le courrier indésirable | 24 septembre 2020 |
| [SOC 1 (Office 365)](https://servicetrust.microsoft.com/ViewPage/MSComplianceGuideV3?command=Download&downloadType=Document&downloadId=90df3f9c-3aaf-4dbf-99d0-ca9f2991721b&tab=7027ead0-3d6b-11e9-b9e1-290b1eb4cdeb&docTab=7027ead0-3d6b-11e9-b9e1-290b1eb4cdeb_SOC_%2F_SSAE_16_Reports) | CA-27 : Analyse des vulnérabilités | 24 décembre 2020 |
| [SOC 2 (Office 365)](https://servicetrust.microsoft.com/ViewPage/MSComplianceGuideV3?command=Download&downloadType=Document&downloadId=a73c1738-7892-42b7-acd3-87b6371c53f6&tab=7027ead0-3d6b-11e9-b9e1-290b1eb4cdeb&docTab=7027ead0-3d6b-11e9-b9e1-290b1eb4cdeb_SOC_%2F_SSAE_16_Reports) | CA-27 : Analyse des vulnérabilités <br> CA-45 : Anti-programme malveillant | 24 décembre 2020 |