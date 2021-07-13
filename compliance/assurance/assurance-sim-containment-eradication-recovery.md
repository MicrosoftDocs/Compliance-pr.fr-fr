---
title: 'Gestion des incidents de sécurité Microsoft : containment, éradication et récupération'
description: Cet article fournit une vue d’ensemble du processus de gestion des incidents de sécurité, d’éradication et de récupération dans les services en ligne Microsoft.
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
f1.keywords:
- NOCSH
ms.collection:
- Strat_O365_IP
- M365-security-compliance
- MS-Compliance
titleSuffix: Microsoft Service Assurance
hideEdit: true
ms.openlocfilehash: 95e52107df2f3e745d393c62929f7c169bcf9a33
ms.sourcegitcommit: 8bf2602d56eedee4447ddb374ef95b0587f254e7
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 07/12/2021
ms.locfileid: "53377551"
---
# <a name="microsoft-security-incident-management-containment-eradication-and-recovery"></a>Gestion des incidents de sécurité Microsoft : containment, éradication et récupération

En fonction de l’analyse effectuée par l’équipe de réponse à la sécurité, l’équipe de service et d’autres personnes, un plan de contrôle et de récupération approprié est développé pour minimiser l’effet de l’incident de sécurité. Les équipes de service appropriées appliquent ensuite ce plan en production avec le support de l’équipe de réponse à la sécurité.

## <a name="containment"></a>Confinement

Après avoir détecté un incident de sécurité, il est important de contenir l’intrusion avant que l’adversaire puisse accéder à plus de ressources ou causer davantage de dommages. L’objectif principal de nos procédures de réponse aux incidents de sécurité est de limiter l’impact sur les clients ou leurs données, ou sur les systèmes, services et applications Microsoft.

## <a name="eradication"></a>Eradication

L’éradication est le processus d’élimination de la cause initiale de l’incident de sécurité avec un niveau de confiance élevé. L’objectif est double :

- pour déloger complètement l’adversaire de l’environnement
- pour atténuer la vulnérabilité (si elle est connue) qui a activé ou peut permettre à l’adversaire de reentre l’environnement.

Selon la nature de l’incident, l’étendue de l’incident de sécurité, la profondeur de pénétration et les limites possibles, l’équipe de réponse à la sécurité recommande aux équipes de service d’adopter des techniques d’éradication. Étant donné l’impact potentiel de ces étapes d’éradication sur l’entreprise, ces décisions sont prises par les équipes de service et l’équipe de réponse à la sécurité après une analyse détaillée et une approbation du responsable exécutif des incidents (si nécessaire).

## <a name="recovery"></a>Récupération

À mesure que l’équipe de réponse gagnera un niveau raisonnable de confiance que l’adversaire a été supprimé de l’environnement et que tous les chemins d’accès vulnérables connus ont été supprimés, les équipes de service individuelles lanceront des étapes de restauration pour mettre le service dans une configuration connue et appropriée. Ces étapes de restauration seront en consultation avec l’équipe de réponse à la sécurité. Cette activité inclut l’identification du dernier bon état connu du service, la restauration à partir des sauvegardes vers cet état, l’inspection des chemins d’attaque vulnérables dans l’état restauré, etc. L’équipe de réponse à la sécurité, en consultation avec les équipes de service, déterminera le meilleur plan de récupération possible pour l’environnement.

L’un des aspects clés de la récupération consiste à mettre en place des contrôles et des contrôles améliorés pour vérifier que le plan de récupération a été correctement exécuté et qu’il n’existe aucun signe de violation dans l’environnement.

## <a name="customer-notification-of-security-incident"></a>Notification client de l’incident de sécurité

Si Microsoft détermine qu’un incident de sécurité s’est produit, nous vous en informerons avec retard indu, et dans le cadre des exigences contractuelles et de conformité que nous avons convenues. Après avoir identifié tous les locataires concernés, l’équipe de communication correspondante travaille à identifier les réglementations pertinentes qui peuvent s’appliquer aux locataires concernés. L’équipe de communication utilise le canal de communication approprié défini dans les réglementations applicables pour avertir le contact client approprié.

La notification inclut des informations détaillées sur l’incident, telles qu’une description de l’incident, l’impact sur les données client, le cas contraire, les actions prises par Microsoft et/ou les actions suggérées pour que les clients prennent des mesures pour résoudre le problème et empêcher la récurrence. La notification est remis à l’administrateur désigné du client des services en ligne Microsoft. Pour vous assurer que les notifications sont reçues, vous devez vous assurer que vos administrateurs fournissent et conservent des informations de contact précises dans leurs profils clients. En outre, en fonction de la nature de l’incident, Microsoft 365 clients peuvent également être avertis via le tableau [de bord d Microsoft 365 d’état du service.](http://status.yammer.com/)

## <a name="related-articles"></a>Articles connexes

- [Gestion des incidents de sécurité Microsoft](assurance-security-incident-management.md)
- [Gestion des incidents de sécurité Microsoft : préparation](assurance-sim-preparation.md)
- [Gestion des incidents de sécurité Microsoft : détection et analyse](assurance-sim-detection-analysis.md)
- [Gestion des incidents de sécurité Microsoft : activité post-incident](assurance-sim-post-incident-activity.md)
- [Comment enregistrer un ticket de support d’événement de sécurité](/azure/security/fundamentals/event-support-ticket)
- [Notification de violation Azure et Dynamics 365 dans le cadre du RGPD](/compliance/regulatory/gdpr-breach-azure-dynamics)
