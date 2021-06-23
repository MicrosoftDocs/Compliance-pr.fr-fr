---
title: Résilience de service intégrée dans Microsoft 365
description: Description de la résilience Microsoft 365 service
author: robmazz
ms.author: robmazz
manager: laurawi
ms.reviewer: sosstah
f1.keywords:
- NOCSH
audience: ITPro
ms.topic: article
ms.service: o365-solutions
localization_priority: Normal
ms.collection:
- M365-subscription-management
- Strat_O365_Enterprise
- MS-Compliance
titleSuffix: Microsoft Service Assurance
hideEdit: true
ms.openlocfilehash: fc8964f453c5a2924fc9a4b43a2c89aa1dec4271
ms.sourcegitcommit: fb379d1110a9a86c7f9bab8c484dc3f4b3dfd6f0
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 06/23/2021
ms.locfileid: "53088573"
---
# <a name="built-in-service-resiliency-in-microsoft-365"></a>Résilience de service intégrée dans Microsoft 365

En tant que fournisseur de collaboration dans le Cloud, Microsoft reconnaît la nécessité de gagner en permanence votre confiance en fournissant des solutions qui fonctionnent de manière cohérente et que vos utilisateurs apprécient. Lorsqu’un service donné n’est pas disponible, il s’agit d’un temps d’arrêt. La définition d’un temps d’indisponibilité varie pour chaque service Microsoft 365, mais il s’agit généralement de toute période pendant laquelle les utilisateurs ne peuvent pas utiliser les fonctionnalités principales du service. Par exemple, voici la définition d’un temps d’indisponibilité pour SharePoint Online extrait du contrat de niveau de service de Microsoft 365 :

**« Temps d’indisponibilité SharePoint Online** : toute période au cours de laquelle les utilisateurs sont dans l’impossibilité de lire ou d’écrire toute partie d’une collection de sites SharePoint Online pour laquelle ils disposent des autorisations appropriées. »

Vous pouvez trouver les définitions de temps d’indisponibilité pour chaque service dans les [Contrats de niveau de service](https://www.microsoftvolumelicensing.com/DocumentSearch.aspx?Mode=3&DocumentTypeId=37).

Pour réduire les temps d'indisponibilité, qu’ils soient planifiés ou imprévus, les services Microsoft 365 sont conçus et exploités de manière à être hautement disponibles et résistants aux défaillances en se concentrant sur quatre domaines :

## <a name="activeactive-design"></a>Conception active/active

Dans Microsoft 365, nous nous dirigeons vers l’architecture de tous les services et leur fonctionnement dans une conception active/active qui augmente la résilience. Cette conception signifie qu’il existe toujours plusieurs instances d’un service en cours d’exécution qui peuvent répondre aux demandes des utilisateurs et qu’elles sont hébergées dans des centres de données géographiquement dispersés. Tout le trafic utilisateur passe par le service Microsoft Front Door et est automatiquement acheminé vers l'instance du service la plus proche et autour de toute défaillance de service pour prévenir ou réduire son impact pour nos clients.

## <a name="reduce-incident-scope"></a>Réduction de la portée des incidents

L’étendue d’un incident de service est mesurée par sa gravité, sa durée et le nombre de clients touchés. Nous cherchons à limiter la portée de tous les incidents en procédant comme suit :

- disposer de plusieurs instances de chaque service partitionnées les unes des autres
- déployer des mises à jour de manière contrôlée et graduelle à l’aide d’anneaux de validation, afin de détecter les problèmes pouvant découler de la mise à jour et de les éliminer au début du processus de déploiement. Cette conception permet la régression de la mise à jour si nécessaire et se produit d’abord dans un petit groupe à l’intérieur de Microsoft (anneau interne) avant d’être déployée pour des groupes plus importants comme tous les 140 000 employés de Microsoft (anneau 2), puis pour les anneaux d’utilisateur précoce (anneau 3) et finalement pour tous les clients globalement (anneau 4).
- améliorer la surveillance grâce à l’automatisation. Microsoft 365 est un service de grande taille et le temps de travail cible du SLA est élevé. Au début d’un incident de service, si des humains devaient être impliqués dans la détection et l’intervention, nous ne pourrions pas réagir assez rapidement pour respecter les contrats SLA. L’automatisation permet de détecter et de répondre rapidement et efficacement aux incidents de service. Plus vite nous sommes au courant d’un incident, plus vite celui-ci pourra être réparé.

Parallèlement aux fonctionnalités actives/actives intégrées à l’architecture de service Microsoft 365, ces efforts atténuent la gravité, la durée et le nombre de clients touchés au cours d’un incident de service.  

## <a name="fault-isolation"></a>Isolation des pannes

Tout comme les services sont conçus et exploités de façon active/active et sont partitionnés les uns des autres afin d’éviter qu’une défaillance d’un service n’en perturbe un autre, la base de code du service est développée en utilisant des principes de partitionnement similaires appelés isolation des pannes. Les mesures d’isolation des pannes sont des protections incrémentielles intégrées à la base de code elle-même. Ces mesures permettent d'éviter qu'un problème dans un domaine ne se répercute dans d'autres domaines d'activité.
Les mesures d’isolation des pannes sont appliquées à plusieurs étapes du développement et de la livraison d’un service, notamment le développement de code, le déploiement de service, l’équilibrage de charge et la réplication de base de données.

Le cycle de vie de développement de la sécurité Microsoft (SDL) favorise davantage la résilience et se compose d'un ensemble de pratiques qui prennent en charge les exigences de sécurité et de conformité. SDL guide nos développeurs dans le cadre de la création de services fiables, sécurisés et conformes. Les principaux éléments de SDL comprennent les révisions de codes, la modélisation des menaces, les tests d’intrusion et les processus normalisés de réponse aux incidents dans le Cloud Microsoft.

Microsoft 365 services sont hautement interconnectés, mais les systèmes et la technologie derrière eux sont conçus d’une manière qui limite l’impact d’un incident de service sur d’autres services. Par exemple, un problème affectant Exchange Online n’affectera pas les fonctionnalités principales dans Teams ou un problème avec la fonctionnalité de recherche dans SharePoint Online n’affectera pas la capacité des utilisateurs à télécharger ou télécharger des fichiers.

## <a name="continuous-service-improvement"></a>Amélioration continue du service

Lorsqu’un incident survient, nous le prenons au sérieux. Après tout, notre architecture de Cloud redondante et ses processus internes rigoureux visent à maintenir l’accessibilité de nos services. Au cours d’un incident, notre surveillance détecte rapidement les services affectés et, si votre client est affecté, vous êtes averti immédiatement via différents canaux. Parallèlement, les ingénieurs suivent des processus bien définis pour trier le problème et prendre les mesures nécessaires pour rétablir le fonctionnement normal le plus rapidement possible. Une fois que le service fonctionne de nouveau normalement, nous procédons à des révisions post-incident dans le cadre du cycle d'amélioration continue du service. Au cours de la révision post-incident, nous déterminons les causes principales de l'incident et les mesures qui ont dû être prises pour régler les problèmes. Ensuite, nous appliquons ce que nous avons appris sur la situation à la conception et au fonctionnement de l'ensemble de notre suite d’offres. Avec cette connaissance, nous pouvons empêcher la même cause première d’avoir un impact sur d’autres services et d’autres clients.
