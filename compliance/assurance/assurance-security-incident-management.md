---
title: Gestion des incidents de sécurité Microsoft
description: Cet article fournit une vue d’ensemble du processus de gestion des incidents de sécurité dans les services en ligne Microsoft.
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
- MS-Compliance0
titleSuffix: Microsoft Service Assurance
hideEdit: true
ms.openlocfilehash: a2c2a472d911034952814da51db133acc5744288
ms.sourcegitcommit: 8bf2602d56eedee4447ddb374ef95b0587f254e7
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 07/12/2021
ms.locfileid: "53377501"
---
# <a name="microsoft-security-incident-management"></a>Gestion des incidents de sécurité Microsoft

Microsoft travaille en permanence pour fournir des services de qualité entreprise hautement sécurisés aux clients Microsoft, mais les incidents de sécurité sont une réalité inévitable qui doit être gérée de manière approfondie et rapide. Ce document fournit une vue d’ensemble sur la façon dont Microsoft gère les incidents de sécurité à l’aide de méthodes et technologies essayées pour minimiser leur impact potentiel. Un incident de sécurité fait référence à tout accès illégal aux données client stockées sur l’équipement de Microsoft ou dans les installations de Microsoft, ou à un accès non autorisé à ces équipements ou installations qui peuvent entraîner la perte, la divulgation ou l’altération des données client. Les objectifs de Microsoft lors de la réponse aux incidents de sécurité sont de protéger les données client et les services en ligne de Microsoft.

Les équipes de sécurité des services en ligne Microsoft et les différentes équipes de service travaillent conjointement et utilisent la même approche pour les incidents de sécurité :

- Préparation
- Détection et analyse
- Containment, Éradication et Récupération
- Activité post-incident

## <a name="microsoft-approach-to-security-incident-management"></a>Approche De Microsoft en matière de gestion des incidents de sécurité

L’approche de Microsoft en matière de gestion d’un incident de sécurité est conforme au National [Institute of Standards and Technology (NIST)](https://www.nist.gov/) Special Publication (SP) 800-61. Microsoft dispose de plusieurs équipes dédiées qui travaillent ensemble pour prévenir, surveiller, détecter et répondre aux incidents de sécurité.

|**Équipe/zone**|**Description**|
|:------------|:--------------|
| Centre de réponse aux problèmes de sécurité Microsoft | Identifie, surveille, résout et répond aux incidents de sécurité et aux vulnérabilités de sécurité des logiciels Microsoft. |
| Centre des opérations de cyber-défense | Le Centre des opérations de cybersécurité est l’emplacement physique qui regroupe les équipes de réponse à la sécurité et les experts de toute l’entreprise pour vous aider à protéger, détecter et répondre aux menaces en temps réel. |
| Affaires d’entreprise, externes et juridiques | Fournit des conseils juridiques et réglementaires pour un incident de sécurité suspecté. |
| Équipe de sécurité du centre de données Microsoft | Équipe qui se concentre sur les différents services sur les investissements communs en matière d’ingénierie de sécurité pour protéger, détecter et répondre aux risques et menaces de l’architecture de service. |
| Microsoft Security Response Teams | Azure, Dynamics 365 et les équipes de sécurité Microsoft 365 indépendantes qui s’associent aux équipes de service pour créer le processus de gestion des incidents de sécurité approprié et pour piloter toute réponse aux incidents de sécurité. |
| Équipes de gouvernance, de risque et de conformité (GRC) Microsoft | Fournir des conseils sur les exigences réglementaires, la conformité et la confidentialité. |
| Équipes de service | Les équipes d’ingénierie pour Azure, Dynamics 365 Microsoft 365 responsables des stratégies et décisions liées à la sécurité pour chaque service. |
| Responsables des opérations Azure | Supervise l’examen et la résolution des incidents de sécurité et de confidentialité liés à Azure. |
| Microsoft Threat Intelligence Center (MSTIC) | Fournit l’état actuel des menaces de sécurité numérique contre les ressources et l’infrastructure Microsoft, aide les équipes partenaires au sein de Microsoft à hiérarchiser les plans d’action de prévention et d’atténuation, et augmente la protection en adoptant la surveillance/détection des incidents en temps quasi réel. |
| Équipes de communication d’expérience client | Équipes d’ingénierie responsables de toutes les communications client sur les incidents de sécurité et de service. Des équipes distinctes sont dédiées à Azure, Dynamics 365 et Microsoft 365. |

## <a name="response-management-process"></a>Processus de gestion des réponses

Les équipes de sécurité des services en ligne microsoft et les équipes de service travaillent ensemble et utilisent la même approche pour les incidents de sécurité, basée sur les phases de gestion des réponses NIST 800-61 :

- **Préparation**: fait référence à la préparation organisationnelle nécessaire pour pouvoir répondre, y compris les outils, les processus, les compétences et la préparation.
- **Analyse &** détection : fait référence à l’activité pour détecter un incident de sécurité dans un environnement de production et analyser tous les événements afin de confirmer l’authenticité de l’incident de sécurité.
- **Containment, éradication, récupération**: fait référence aux actions requises et appropriées prises pour contenir l’incident de sécurité en fonction de l’analyse effectuée au cours de la phase précédente. Une analyse plus approfondie peut également être nécessaire dans cette phase pour une récupération complète à partir de l’incident de sécurité.
- **Activité post-incident**: fait référence à l’analyse post-mortem effectuée après la récupération d’un incident de sécurité. Les actions opérationnelles effectuées au cours du processus sont examinées pour déterminer si des modifications doivent être apportées lors des phases de préparation ou de détection et d’analyse.

![Phases de gestion des incidents de sécurité](../media/assurance-sim-phases.png)

## <a name="federated-security-response-model"></a>Modèle de réponse de sécurité fédérée

Les services en ligne Microsoft comprennent des produits Microsoft de base, notamment Azure, Dynamics 365 et Microsoft 365. Chacun de ces services est géré par des équipes distinctes avec leurs propres processus opérationnels de sécurité. D’autres équipes de Microsoft, telles que MSTIC, sont également engagées dans différents aspects de la sécurité des services en ligne Microsoft. En raison de la multitude d’équipes qui travaillent sur la gestion des opérations de sécurité dans tous les différents services qui font partie des services en ligne Microsoft, Microsoft a implémenté un modèle de réponse de sécurité fédérée.

Ce tableau présente les limites opérationnelles entre les différentes équipes d’opérations de sécurité du service en ligne Microsoft et les équipes de service Microsoft :

|**Activité**|**Opérations de l’équipe de sécurité Microsoft**|**Opérations de l’équipe de service Microsoft**|
|:-----------|:-----------------------------------------|:----------------------------------------|
| Détection et analyse | - Exigences de détection <br> - Analyse et surveillance de la sécurité <br> - Indicateur de compromission (IOC) <br> - Recherche de violation <br> - 24 h/24 et 7 j/7, responsable de la sécurité à l’appel et de la réponse aux incidents | - Exigences de détection <br> - Surveillance du déploiement de l’infrastructure <br> - Analyse et aperçu du service <br> - Tri des événements et des alertes <br> - 24 h/24, 7 j/7, ingénierie de service à l’appel  |
| Containment, éradication, récupération | - Chef de réponse aux incidents <br> - Investigation d’investigation légale <br> - Expertise et conseil en matière de sécurité <br> - Conseils sur la récupération | - Propriétaire de l’incident de sécurité <br> - Informations et expertise sur les services <br> - Exécuter l’endiguement, l’éradication et la récupération |
| Activité post-incident | - Chef de l’analyse post-incident <br> - Collecte et archivage des données <br> - Leçons apprises et demandes de bogues <br> - Rapport d’incident | - Analyse des incidents côté service <br> - Hiérarchiser les activités de suivi <br> - Investissements en matière de sécurité de mise en œuvre <br> - Préparation de la sécurité du service |

## <a name="related-articles"></a>Articles connexes

- [Gestion des incidents de sécurité Microsoft : préparation](assurance-sim-preparation.md)
- [Gestion des incidents de sécurité Microsoft : détection et analyse](assurance-sim-detection-analysis.md)
- [Gestion des incidents de sécurité Microsoft : containment, éradication et récupération](assurance-sim-containment-eradication-recovery.md)
- [Gestion des incidents de sécurité Microsoft : activité post-incident](assurance-sim-post-incident-activity.md)
