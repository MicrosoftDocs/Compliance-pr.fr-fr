---
title: Résilience de service intégrée dans Microsoft 365
description: Description de la résilience de service Microsoft 365
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
ms.openlocfilehash: ee9c7d898af13b9a1db95913a98be09eea8cd27f
ms.sourcegitcommit: 693bc6b1b51a5a9c9ff1758fa7f7ca3a204f147e
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 12/04/2020
ms.locfileid: "49574756"
---
# <a name="built-in-service-resiliency-in-microsoft-365"></a>Résilience de service intégrée dans Microsoft 365

En tant que fournisseur de collaboration dans le Cloud, Microsoft reconnaît la nécessité de gagner en permanence votre confiance en fournissant des solutions qui fonctionnent de manière cohérente et que vos utilisateurs apprécient. Lorsqu’un service donné est indisponible, il s’agit d’un temps d’indisponibilité. La définition d’un temps d’indisponibilité varie pour chaque service Microsoft 365, mais il s’agit généralement de toute période pendant laquelle les utilisateurs ne peuvent pas utiliser les fonctionnalités principales du service. Par exemple, voici la définition d’un temps d’indisponibilité pour SharePoint Online extrait du contrat de niveau de service de Microsoft 365 :

**« Temps d’indisponibilité SharePoint Online** : toute période au cours de laquelle les utilisateurs sont dans l’impossibilité de lire ou d’écrire toute partie d’une collection de sites SharePoint Online pour laquelle ils disposent des autorisations appropriées. »

Vous pouvez trouver les définitions de temps d’indisponibilité pour chaque service dans les [Contrats de niveau de service](https://www.microsoftvolumelicensing.com/DocumentSearch.aspx?Mode=3&DocumentTypeId=37).

Pour réduire les temps d'indisponibilité, qu’ils soient planifiés ou imprévus, les services Microsoft 365 sont conçus et exploités de manière à être hautement disponibles et résistants aux défaillances en se concentrant sur quatre domaines :

## <a name="activeactive-design"></a>Conception active/active

Dans Microsoft 365, nous faisons en sorte que tous les services soient conçus et exploités dans une conception active/active qui augmente la résistance. Cela signifie qu’il existe toujours plusieurs instances d’un service en cours d’exécution hébergées dans des centres de données dispersés géographiquement, capables de répondre aux demandes des utilisateurs. Tout le trafic utilisateur passe par le service Microsoft Front Door et est automatiquement acheminé vers l'instance du service la plus proche et autour de toute défaillance de service pour prévenir ou réduire son impact pour nos clients.

## <a name="reduce-incident-scope"></a>Réduction de la portée des incidents

L’étendue d’un incident de service est mesurée par sa gravité, sa durée et le nombre de clients touchés. Nous cherchons à limiter la portée de tous les incidents en procédant comme suit :

- disposer de plusieurs instances de chaque service partitionnées les unes des autres
- déployer des mises à jour de manière contrôlée et graduelle à l’aide d’anneaux de validation, afin de détecter les problèmes pouvant découler de la mise à jour et de les éliminer au début du processus de déploiement. Cela permet d’effectuer une régression de la mise à jour si nécessaire et d’abord se produire dans un petit groupe au sein de Microsoft (anneau intérieur) avant d’être déployé pour des groupes plus importants comme tous les employés de Microsoft 140 000 (Ring 2), puis pour les sonneries précoces (Ring 3) et finalement pour tous les clients globalement (Ring 4).
- améliorer la surveillance grâce à l’automatisation. Microsoft 365 est un grand service et la durée de fonctionnement de la cible SLA est élevée. Au début d’un incident de service, si des humains devaient être impliqués dans la détection et l’intervention, nous ne pourrions pas réagir assez rapidement pour respecter les contrats SLA. L’automatisation permet de détecter et de répondre rapidement et efficacement aux incidents de service. Plus vite nous sommes au courant d’un incident, plus vite celui-ci pourra être réparé.

Outre les capacités actives/actives intégrées à l’architecture de service de Microsoft 365, ces efforts réduisent la gravité, la durée et le nombre de clients affectés lors d’un incident de service.  

## <a name="fault-isolation"></a>Isolation des pannes

Tout comme les services sont conçus et exploités de façon active/active et sont partitionnés les uns des autres afin d’éviter qu’une défaillance d’un service n’en perturbe un autre, la base de code du service est développée en utilisant des principes de partitionnement similaires appelés isolation des pannes. Les mesures d’isolation des pannes sont des protections incrémentielles intégrées à la base de code elle-même. Ces mesures permettent d'éviter qu'un problème dans un domaine ne se répercute dans d'autres domaines d'activité.
Les mesures d’isolation des pannes sont appliquées à plusieurs stades du développement et de la fourniture d’un service, y compris le développement du code, le déploiement du service, l’équilibrage de charge et la réplication des bases de données.

Le cycle de vie de développement de la sécurité Microsoft (SDL) favorise davantage la résilience et se compose d'un ensemble de pratiques qui prennent en charge les exigences de sécurité et de conformité. SDL guide nos développeurs dans le cadre de la création de services fiables, sécurisés et conformes. Les principaux éléments de SDL comprennent les révisions de codes, la modélisation des menaces, les tests d’intrusion et les processus normalisés de réponse aux incidents dans le Cloud Microsoft.

Les services M365 sont étroitement connectés, mais les systèmes et la technologie sur lesquels ils reposent sont conçus de manière à limiter l'impact d'un incident de service sur les autres services. Par exemple, un problème affectant Exchange Online n’affectera pas les principales fonctionnalités de Teams, ou un problème lié à la fonctionnalité de recherche dans SharePoint Online n’affectera pas la possibilité pour les utilisateurs de télécharger des fichiers.

## <a name="continuous-service-improvement"></a>Amélioration continue du service

Lorsqu’un incident survient, nous le prenons au sérieux. Après tout, notre architecture de Cloud redondante et ses processus internes rigoureux visent à maintenir l’accessibilité de nos services. Lors d’un incident, notre système de surveillance détecte rapidement les services affectés et, si votre client est concerné, vous recevez immédiatement une notification par différents canaux. Parallèlement, les ingénieurs suivent des processus bien définis pour trier le problème et prendre les mesures nécessaires pour rétablir le fonctionnement normal le plus rapidement possible. Une fois que le service fonctionne de nouveau normalement, nous procédons à des révisions post-incident dans le cadre du cycle d'amélioration continue du service. Au cours de la révision post-incident, nous déterminons les causes principales de l'incident et les mesures qui ont dû être prises pour régler les problèmes. Ensuite, nous appliquons ce que nous avons appris sur la situation à la conception et au fonctionnement de l'ensemble de notre suite d’offres. En procédant de la sorte, nous pouvons empêcher que la même cause initiale affecte d’autres services et d’autres clients.
