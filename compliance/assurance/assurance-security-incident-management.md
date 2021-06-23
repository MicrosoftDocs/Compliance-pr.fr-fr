---
title: Gestion des incidents de sécurité de Microsoft 365
description: Cet article fournit une vue d’ensemble du processus de gestion des incidents de sécurité Microsoft 365.
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
ms.openlocfilehash: 5f3123d4b4ef853357c0b98f1b6973cc8ba4d1e8
ms.sourcegitcommit: fb379d1110a9a86c7f9bab8c484dc3f4b3dfd6f0
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 06/23/2021
ms.locfileid: "53088886"
---
# <a name="microsoft-365-security-incident-management"></a>Gestion des incidents de sécurité de Microsoft 365

Microsoft travaille en permanence pour fournir des services hautement sécurisés et de qualité Microsoft 365 clients. Ce document décrit comment Microsoft gère les incidents de sécurité dans Microsoft 365. Un incident de sécurité fait référence à tout accès illégal aux données client stockées sur l’équipement de Microsoft ou dans les installations de Microsoft, ou à un accès non autorisé à ces équipements ou installations qui peuvent entraîner la perte, la divulgation ou l’altération des données client. Les objectifs de Microsoft lors de la réponse aux incidents de sécurité sont de protéger les données client et les services Microsoft 365 client.

L Microsoft 365 de sécurité et les différentes équipes de service travaillent conjointement et ont la même approche pour les incidents de sécurité :

- Préparation
- Détection et analyse
- Confinement
- Eradication
- Récupération
- Activité post-incident

## <a name="microsoft-approach-to-security-incident-management"></a>Approche De Microsoft en matière de gestion des incidents de sécurité

L’approche de Microsoft en matière de gestion d’un incident de sécurité est conforme au National [Institute of Standards and Technology (NIST)](https://www.nist.gov/) Special Publication (SP) 800-61. Microsoft dispose de plusieurs équipes dédiées qui travaillent ensemble pour prévenir, surveiller, détecter et répondre aux incidents de sécurité.

|**Équipe/zone**|**Description**|
|:------------|:--------------|
| Centre de réponse aux problèmes de sécurité Microsoft | Identifie, surveille, résout et répond aux incidents de sécurité et aux vulnérabilités de sécurité des logiciels Microsoft. |
| Centre des opérations de cyber-défense | Le Centre des opérations de cybersécurité est l’emplacement physique qui regroupe les équipes de réponse à la sécurité et les experts de toute l’entreprise pour vous aider à protéger, détecter et répondre aux menaces en temps réel. |
| Affaires d’entreprise, externes et juridiques | Fournit des conseils juridiques et réglementaires pour un incident de sécurité suspecté. |
| Microsoft 365 Équipe de réponse à la sécurité | Partenaires avec des Microsoft 365 service pour créer le processus de gestion des incidents de sécurité approprié et pour piloter toute réponse aux incidents de sécurité. |
| Office 365 Confiance | Fournit des conseils sur les exigences réglementaires, la conformité et la confidentialité. |
| Microsoft 365 Équipe de sécurité du centre de données | Équipe qui se concentre sur les différents services sur les investissements communs en matière d’ingénierie de sécurité pour protéger, détecter et répondre aux menaces et Microsoft 365'architecture de service. |
| Équipes de service | Équipes d’ingénierie pour les services Microsoft 365, tels que Exchange, SharePoint et Microsoft Teams, qui sont chargés de prendre des décisions et des stratégies liées à la sécurité pour chaque service. |
| Microsoft Threat Intelligence Center (MSTIC) | Fournit l’état actuel des menaces de sécurité numérique contre les ressources et l’infrastructure Microsoft, aide les équipes partenaires au sein de Microsoft à hiérarchiser les plans d’action de prévention et d’atténuation, et augmente la protection en adoptant la surveillance/détection des incidents en temps quasi réel. |
| Équipes de sécurité des partenaires | Autres équipes de sécurité partenaires au sein de Microsoft qui fournissent des services clés ou qui sont responsables des dépendances clés dans Microsoft 365, telles que l’équipe Azure Security Response, identity security response et Microsoft Corporate Security Response teams. |
| Microsoft 365 Communications d’expérience client | Équipe d’ingénierie responsable de toutes les communications client sur les incidents de sécurité et de service. |

## <a name="response-management-process"></a>Processus de gestion des réponses

L’équipe de sécurité Microsoft 365 et les équipes de service travaillent ensemble et ont la même approche des incidents de sécurité, qui est basée sur les phases de gestion des réponses NIST 800-61 :

- **Préparation**: fait référence à la préparation organisationnelle nécessaire pour pouvoir répondre, y compris les outils, les processus, les compétences et la préparation.
- **Analyse &** détection : fait référence à l’activité pour détecter un incident de sécurité dans un environnement de production et analyser tous les événements afin de confirmer l’authenticité de l’incident de sécurité.
- **Containment, éradication, récupération**: fait référence aux actions requises et appropriées prises pour contenir l’incident de sécurité en fonction de l’analyse effectuée au cours de la phase précédente. Une analyse plus approfondie peut également être nécessaire dans cette phase pour une récupération complète à partir de l’incident de sécurité.
- **Activité post-incident**: fait référence à l’analyse post-mortem effectuée après la récupération d’un incident de sécurité. Les actions opérationnelles effectuées au cours du processus sont examinées pour déterminer si des modifications doivent être apportées lors des phases de préparation ou de détection et d’analyse.

![Phases de gestion des incidents de sécurité](../media/assurance-sim-phases.png)

## <a name="federated-security-response-model"></a>Modèle de réponse de sécurité fédérée

les services Microsoft 365 incluent les services en ligne Microsoft principaux (Exchange, SharePoint et Microsoft Teams, etc.) et d’autres services cloud De Microsoft, tels que Azure Active Directory, microsoft Commerce Platform et MSTIC. Ces services sont gérés par des équipes distinctes avec leurs propres processus opérationnels de sécurité. D’autres équipes chez Microsoft sont également engagées dans différents aspects de la sécurité Microsoft 365. En raison de la multitude d’équipes qui travaillent sur la gestion des opérations de sécurité dans tous les différents services qui Microsoft 365, Microsoft a implémenté un modèle de réponse de sécurité fédérée.

Ce tableau présente les limites opérationnelles entre les différentes équipes Microsoft 365 opérations de sécurité et les équipes Microsoft 365 service :

|**Activité**|**Microsoft 365 Opérations de l’équipe de sécurité**|**Microsoft 365 Opérations de l’équipe de service**|
|:-----------|:-----------------------------------------|:----------------------------------------|
| Détection et analyse | - Exigences de détection <br> - Analyse et surveillance de la sécurité <br> - Indicateur de compromission (IOC) <br> - Recherche de violation <br> - 24 h/24 et 7 j/7, responsable de la sécurité à l’appel et de la réponse aux incidents | - Exigences de détection <br> - Surveillance du déploiement de l’infrastructure <br> - Analyse et aperçu du service <br> - Tri des événements et des alertes <br> - 24 h/24, 7 j/7, ingénierie de service à l’appel  |
| Containment, éradication, récupération | - Chef de réponse aux incidents <br> - Investigation d’investigation légale <br> - Expertise et conseil en matière de sécurité <br> - Conseils sur la récupération | - Propriétaire de l’incident de sécurité <br> - Informations et expertise sur les services <br> - Exécuter l’endiguement, l’éradication et la récupération |
| Activité post-incident | - Chef de l’analyse post-incident <br> - Collecte et archivage des données <br> - Leçons apprises et demandes de bogues <br> - Rapport d’incident | - Analyse des incidents côté service <br> - Hiérarchiser les activités de suivi <br> - Investissements en matière de sécurité de mise en œuvre <br> - Préparation de la sécurité du service |

## <a name="related-articles"></a>Articles connexes

- [Microsoft 365 de gestion des incidents de sécurité](assurance-sim-preparation.md)
- [Microsoft 365 détection et analyse de la gestion des incidents de sécurité](assurance-sim-detection-analysis.md)
- [Microsoft 365 de gestion des incidents de sécurité, l’éradication et la récupération](assurance-sim-containment-eradication-recovery.md)
- [Microsoft 365 gestion des incidents de sécurité après incident](assurance-sim-post-incident-activity.md)
