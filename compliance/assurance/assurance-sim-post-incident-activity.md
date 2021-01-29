---
title: 'Gestion des incidents de sécurité Microsoft 365 : activité post-incident'
description: Cet article fournit une vue d’ensemble du processus d’activité post-incident de gestion des incidents de sécurité dans Microsoft 365.
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
ms.openlocfilehash: 66c25503ac574de512f5201981112a0e54714968
ms.sourcegitcommit: 2973d25e9e0185b84d281f963553a332eac1c1a3
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/28/2021
ms.locfileid: "50040347"
---
# <a name="microsoft-365-security-incident-management-post-incident-activity"></a>Gestion des incidents de sécurité Microsoft 365 : activité post-incident

## <a name="postmortem"></a>Postmortem

Certains incidents de sécurité, en particulier ceux qui ont un impact sur le client ou qui entraînent une violation de données, sont soumis à un post-incident complet. L’équipe de réponse à la sécurité Microsoft 365 effectue un post-mortem détaillé avec toutes les parties impliquées dans la réponse aux incidents de sécurité pour :

- Documenter la séquence d’événements à l’origine de l’incident
- Créez un résumé technique de l’incident tel qu’il est pris en charge par la preuve qui inclut les acteurs impliqués dans la violation (le cas contraire). Ce résumé inclut la façon dont la réponse a été exécutée et d’autres éléments à prendre en compte.
- Identifiez les échecs techniques, les défaillances procédurales, les erreurs manuelles, les failles de processus et les problèmes de communication, et/ou les vecteurs d’attaque précédemment inconnus identifiés lors de la réponse aux incidents de sécurité.

Le post-mortem influence directement l’amélioration du service Microsoft 365, les processus opérationnels et la documentation en fixant de nouvelles priorités dans le cycle de développement d’ingénierie Microsoft 365.

## <a name="documentation"></a>Documentation

Toutes les principales conclusions techniques du processus post-mortem sont capturées dans un rapport et les investissements ou correctifs de service sous la forme de bogues ou de demandes de modification de développement. Ces résultats sont suivis des équipes d’ingénierie appropriées. En cas d’échec de processus et de problèmes organisationnels, les problèmes sont documentés dans la base de données de l’équipe de réponse de sécurité Microsoft 365 et suivis avec les groupes appropriés pour les résoudre.

## <a name="process-improvement"></a>Amélioration des processus

La réponse à un incident de sécurité dans Microsoft 365 implique la coordination avec plusieurs groupes répartis dans différentes organisations au sein de Microsoft, et potentiellement même des organisations externes appropriées telles que les forces de l’ordre. Nous savons qu’il est essentiel d’évaluer nos réponses après chaque incident de sécurité pour des raisons de niveau d’efficacité et d’intégralité. Pour toutes les améliorations ou modifications identifiées, l’équipe de réponse de sécurité Microsoft 365 évalue les suggestions en consultation avec les équipes et les parties prenantes appropriées, et, le cas échéant, les intègre dans les procédures de fonctionnement standard. Toutes les modifications, bogues ou améliorations de service requises identifiés lors de la réponse aux incidents de sécurité ou de l’activité post-mortem sont consignés et suivis dans une base de données d’ingénierie Microsoft 365 interne. Tous les bogues ou fonctionnalités potentiels sont affectés au propriétaire approprié. L’équipe de réponse de sécurité Microsoft 365 examine toutes les entrées jusqu’à ce que le problème soit résolu.

## <a name="related-articles"></a>Articles connexes

- [Gestion des incidents de sécurité de Microsoft 365](assurance-security-incident-management.md)
- [Préparation de la gestion des incidents de sécurité Microsoft 365](assurance-sim-preparation.md)
- [Détection et analyse de la gestion des incidents de sécurité Microsoft 365](assurance-sim-detection-analysis.md)
- [Contenu, éradication et récupération de la gestion des incidents de sécurité Microsoft 365](assurance-sim-containment-eradication-recovery.md)
