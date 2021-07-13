---
title: 'Gestion des incidents de sécurité Microsoft : activité post-incident'
description: Cet article fournit une vue d’ensemble du processus d’activité post-incident de gestion des incidents de sécurité dans les services en ligne Microsoft.
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
ms.openlocfilehash: 965c7d6d0d469b9eea981252805bda598c92a4c8
ms.sourcegitcommit: 8bf2602d56eedee4447ddb374ef95b0587f254e7
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 07/12/2021
ms.locfileid: "53377531"
---
# <a name="microsoft-security-incident-management-post-incident-activity"></a>Gestion des incidents de sécurité Microsoft : activité post-incident

## <a name="postmortem"></a>Postmortem

Certains incidents de sécurité, en particulier ceux qui ont un impact sur le client ou qui entraînent une violation de données, sont soumis à un post-incident complet. L’équipe de réponse à la sécurité effectue un post-mortem détaillé avec toutes les parties impliquées dans la réponse aux incidents de sécurité pour :

- Documenter la séquence d’événements à l’origine de l’incident.
- Créez un résumé technique de l’incident tel qu’il est pris en charge par la preuve qui inclut les acteurs impliqués dans la violation (le cas contraire). Ce résumé inclut la façon dont la réponse a été exécutée et d’autres éléments à prendre en compte.
- Identifiez les échecs techniques, les défaillances procédurales, les erreurs manuelles, les failles de processus et les problèmes de communication, et/ou les vecteurs d’attaque précédemment inconnus identifiés lors de la réponse aux incidents de sécurité.

Le post-mortem influence directement l’amélioration du service en ligne de Microsoft, les processus opérationnels et la documentation en fixant de nouvelles priorités dans le cycle de développement d’ingénierie des services en ligne Microsoft.

## <a name="documentation"></a>Documentation

Toutes les principales conclusions techniques du processus post-mortem sont capturées dans un rapport et les investissements ou correctifs de service sous la forme de bogues ou de demandes de modification de développement. Ces résultats sont suivis des équipes d’ingénierie appropriées. En cas d’échec de processus et de problèmes organisationnels, les problèmes sont documentés dans la base de données de l’équipe de réponse à la sécurité et suivis avec les groupes appropriés pour les résoudre.

## <a name="process-improvement"></a>Amélioration des processus

La réponse à un incident de sécurité dans les services en ligne Microsoft implique une coordination avec plusieurs groupes répartis dans différentes organisations au sein de Microsoft, et potentiellement même des organisations externes appropriées telles que les forces de l’ordre. Nous savons qu’il est essentiel d’évaluer nos réponses après chaque incident de sécurité à la fois pour la sotivité et l’intégralité. Pour toutes les améliorations ou modifications identifiées, l’équipe de réponse à la sécurité évalue les suggestions en consultation avec les équipes et les parties prenantes appropriées, et, le cas échéant, les intègre dans les procédures de fonctionnement standard. Toutes les modifications, bogues ou améliorations de service requises identifiés lors de la réponse aux incidents de sécurité ou de l’activité post-mortem sont consignés et suivis dans une base de données interne d’ingénierie Microsoft. Tous les bogues ou fonctionnalités potentiels sont affectés au propriétaire approprié. L’équipe de réponse aux problèmes de sécurité de Microsoft examine toutes les entrées jusqu’à ce que le problème soit résolu.

## <a name="related-articles"></a>Articles connexes

- [Gestion des incidents de sécurité Microsoft](assurance-security-incident-management.md)
- [Gestion des incidents de sécurité Microsoft : préparation](assurance-sim-preparation.md)
- [Gestion des incidents de sécurité Microsoft : détection et analyse](assurance-sim-detection-analysis.md)
- [Gestion des incidents de sécurité Microsoft : containment, éradication et récupération](assurance-sim-containment-eradication-recovery.md)
- [Comment enregistrer un ticket de support d’événement de sécurité](/azure/security/fundamentals/event-support-ticket)
- [Notification de violation Azure et Dynamics 365 dans le cadre du RGPD](/compliance/regulatory/gdpr-breach-azure-dynamics)
