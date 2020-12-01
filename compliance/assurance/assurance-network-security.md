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
ms.openlocfilehash: c063460fdfba44265b3a1504a049a4772b484dff
ms.sourcegitcommit: 626b0076d133e588cd28598c149a7f272fc18bae
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 11/30/2020
ms.locfileid: "49506692"
---
# <a name="network-security-overview"></a>Vue d’ensemble de la sécurité réseau

## <a name="how-does-microsoft-365-secure-the-network-boundary"></a>Comment Microsoft 365 sécurise-t-il la limite réseau ?

Microsoft 365 utilise plusieurs stratégies pour sécuriser sa limite réseau, notamment la détection et la prévention automatiques des attaques basées sur le réseau, les périphériques de pare-feu spécialisés et Exchange Online Protection (EOP) pour la protection contre le courrier indésirable et les programmes malveillants. De plus, Microsoft 365 sépare son environnement de production en segments réseau isolés de façon logique, avec uniquement la communication nécessaire entre les segments. Le trafic réseau est sécurisé à l’aide de pare-feu réseau supplémentaires à des points limites pour aider à détecter, prévenir et atténuer les attaques réseau.

## <a name="how-does-microsoft-365-defend-against-ddos-attacks"></a>Comment Microsoft 365 se protège contre les attaques DDoS ?

La présence importante sur Internet de Microsoft isole les effets négatifs de nombreuses attaques par déni de service distribuées. Les instances distribuées de chaque service Microsoft 365 et plusieurs itinéraires vers chaque service limitent l’impact des attaques DDoS contre le système. Cette redondance améliore la capacité de Microsoft 365 à absorber les attaques DDoS et augmente le temps disponible pour détecter et réduire les attaques DDoS avant qu’elles n’affectent la disponibilité du service.

En plus de l’architecture système redondante de Microsoft, Microsoft utilise des outils de détection et d’atténuation sophistiqués pour répondre aux attaques DDoS. Les pare-feu spécialisés surveillent et suppriment le trafic indésirable avant qu’il n’entre la limite sur le réseau, réduisant ainsi la contrainte sur les systèmes situés à l’intérieur de la limite réseau. Pour mieux protéger nos services Cloud, Microsoft utilise un système de défense DDoS déployé dans le cadre de Microsoft Azure. Le système de la protection contre les attaques Azure est conçu pour résister aux attaques provenant de l’extérieur, ainsi que d’autres clients Azure.

## <a name="how-does-microsoft-365-protect-users-against-spam-and-malware-being-uploaded-or-sent-through-online-services"></a>Comment Microsoft 365 protège-t-il les utilisateurs contre le courrier indésirable et les programmes malveillants téléchargés ou envoyés via les services en ligne ?

Microsoft 365 crée une protection contre les programmes malveillants dans les services qui peuvent être des vecteurs pour le code malveillant, comme Exchange Online et SharePoint Online. Exchange Online Protection (EOP) analyse tous les courriers électroniques et les pièces jointes des courriers électroniques pour les programmes malveillants lorsqu’ils entrent et quittent le système, ce qui empêche la remise des messages et pièces jointes infectés. Le filtrage du courrier indésirable avancé est automatiquement appliqué aux messages entrants et sortants pour empêcher les organisations clientes de recevoir et d’envoyer du courrier indésirable. Cette couche de protection protège contre les attaques qui tirent parti de messages électroniques non sollicités ou non autorisés, tels que les attaques par hameçonnage. SharePoint Online utilise le même moteur de détection de virus pour analyser de manière sélective les fichiers téléchargés pour les programmes malveillants. Si un fichier est marqué comme infecté, les utilisateurs ne peuvent pas télécharger ou synchroniser le fichier pour protéger les points de terminaison du client.

## <a name="related-external-regulations--certifications"></a>Certifications & des réglementations externes connexes

Les services en ligne de Microsoft sont régulièrement vérifiés pour la conformité aux réglementations et aux certifications externes. Consultez le tableau suivant pour valider les contrôles liés à la sécurité du réseau.

| **Audits externes** | **Section** | **Date du dernier rapport** |
|:--------------------|:------------|:-----------------------|
| [FedRAMP (Office 365)](https://compliance.microsoft.com/compliancemanager) | SC-5 : protection contre les attaques par déni de service <br> SC-7 : protection des limites <br> SI-2 : correction des failles <br> SI-3 : protection contre le code malveillant <br> SI-8 : protection contre le courrier indésirable | 24 septembre 2020 |
| [SOC 1 (Office 365)](https://servicetrust.microsoft.com/ViewPage/MSComplianceGuideV3?command=Download&downloadType=Document&downloadId=b07c0f7b-6bd5-4544-8255-7a5f14bf914a&tab=7027ead0-3d6b-11e9-b9e1-290b1eb4cdeb&docTab=7027ead0-3d6b-11e9-b9e1-290b1eb4cdeb_SOC_/_SSAE_16_Reports) | CA-27 : analyse des vulnérabilités | 30 septembre 2019 |
| [SOC 2 (Office 365)](https://servicetrust.microsoft.com/ViewPage/MSComplianceGuideV3?command=Download&downloadType=Document&downloadId=fa062990-e758-4ddc-ace3-7fb21a301d09&tab=7027ead0-3d6b-11e9-b9e1-290b1eb4cdeb&docTab=7027ead0-3d6b-11e9-b9e1-290b1eb4cdeb_SOC_/_SSAE_16_Rep-11e9-b9e1-290b1eb4cdeb_SOC_/_SSAE_16_Reports) | CA-27 : analyse des vulnérabilités <br> CA-45 : anti-programme malveillant | 30 septembre 2019 |