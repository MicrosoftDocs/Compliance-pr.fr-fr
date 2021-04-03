---
title: Destruction des données dans Microsoft 365
description: Vue d’ensemble des stratégies Microsoft sur le recyclage, l’élimination ou la destruction des disques et serveurs du centre de données Microsoft 365.
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
titleSuffix: Microsoft Service Assurance
hideEdit: true
ms.openlocfilehash: 1b9d410422e22fe67cb27617ba16e2ddbbaec0fd
ms.sourcegitcommit: 024137a15ab23d26cac5ec14c36f3577fd8a0cc4
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 04/01/2021
ms.locfileid: "51497641"
---
# <a name="data-destruction-in-microsoft-365"></a>Destruction des données dans Microsoft 365

## <a name="physical-data-destruction"></a>Destruction des données physiques

Microsoft dispose de stratégies standard de gestion des données qui traitent du recyclage et de l’élimination des lecteurs de disque et des serveurs défaclants ou mis en retrait. Avant de réutiliser des lecteurs de disque Microsoft 365, Microsoft effectue un processus de désinfectation physique cohérent avec la publication spéciale 800-88 du National Institute of Standards and Technology ([NIST SP 800-88 Guidelines for Media Sanitization](https://nvlpubs.nist.gov/nistpubs/SpecialPublications/NIST.SP.800-88r1.pdf)). Étant donné que tous les lecteurs de disque dans Microsoft 365 sont chiffrés à l’aide du chiffrement au niveau du volume BitLocker, l’effacement compatible NIST SP 800-88 n’est pas techniquement nécessaire. Néanmoins, Microsoft effectue ce processus.

Les disques en échec utilisés dans les centres de données Microsoft 365 sont physiquement détruits et audités par le biais du processus ISO. Le type de bien détermine les moyens d’élimination appropriés. Pour les disques durs qui ne peuvent pas être nettoyés, Microsoft utilise un processus de destruction pour détruire les médias et rendre impossible la récupération des informations. Par exemple, les disques sont physiquement détruits, entérés ou insérezés. Microsoft conserve tous les enregistrements de la destruction et effectue un processus de désinfectation similaire sur les serveurs réutilisés dans Microsoft 365. Ces recommandations englobent la désinfectation électronique et physique.

Chaque centre de données utilise un processus de destruction physique sur site pour éliminer ses disques. Les bacs sécurisés pour les supports de stockage désignés pour l’élimination des disques sont dans chaque zone du centre de données. Chaque station bac sécurisée dispose d’une surveillance vidéo. Une fois qu’un bac d’élimination atteint une capacité d’environ 50 %, l’équipe des services de site contacte l’équipe de sécurité physique pour coordonner la suppression. Le personnel des services de site et un bureau de sécurité suppriment le bac d’élimination sécurisé et le placent dans une zone de stockage sécurisée désignée. Les stratégies et procédures régissant la gestion des appareils porteurs de données lors de la destruction sont régulièrement testées, y compris les procédures visant à garantir la condition d’approbation approuvée pour la destruction.

Dans le processus de destruction des données, les disques sont effacés d’une manière conforme à la norme NIST 800-88 (si possible), puis placés dans un broyeur industriel et physiquement effacés. Microsoft conserve la responsabilité des biens quittant le centre de données à l’aide de NIST SP 800-88 nettoyage/purge cohérent, destruction des biens, chiffrement, inventaire précis, suivi et protection de la chaîne de garde pendant le transport. Ce processus est surveillé via une télévision en circuit fermé et un certificat de destruction est émis à la fin de l’opération.

Microsoft utilise des unités d’effacement de données à partir [de solutions de protocole extrême](https://www.enterprisedataerasure.com/) (EPS). Le logiciel EPS prend en charge les exigences NIST SP 800-88 pour nettoyer et purger/sécuriser l’effacement. Avant le nettoyage ou la destruction, un inventaire est créé par le gestionnaire de biens Microsoft. Si un fournisseur est utilisé pour la destruction, il fournit un certificat de destruction pour chaque bien détruit, qui est validé par le gestionnaire de biens.

## <a name="virtual-data-destruction"></a>Destruction de données virtuelles

Microsoft dispose de stratégies et de procédures de gestion des données qui traitent de la destruction virtuelle effective des données afin de se protéger contre le risque de partage inapproprié de données entre les locataires de service ou d’être accessibles après une suppression physique dans le service. Les données supprimées du service dans un client ne sont pas accessibles à un autre client de service, même si l’un des stockages physiques sous-jacents est réassigné. Il s’agit d’un résultat des effets composés de plusieurs technologies de virtualisation et de fragmentation utilisées pour mettre à l’échelle les environnements virtuels, des comportements de suppression actifs des applications au sein de chaque client de service (tels que la mise à zéro des [pages)](/office365/securitycompliance/office-365-exchange-online-data-deletion#page-zeroing)et des processus de chiffrement de contenu multimédia et d’application requis.