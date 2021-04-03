---
title: 'Gestion des incidents de sécurité Microsoft 365 : détection et analyse'
description: Cet article fournit une vue d’ensemble du processus de détection et d’analyse de la gestion des incidents de sécurité dans Microsoft 365.
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
ms.openlocfilehash: 433b8da98e25c4f465473143074eda055419234d
ms.sourcegitcommit: 024137a15ab23d26cac5ec14c36f3577fd8a0cc4
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 04/01/2021
ms.locfileid: "51497404"
---
# <a name="microsoft-365-security-incident-management-detection-and-analysis"></a>Gestion des incidents de sécurité Microsoft 365 : détection et analyse

Pour détecter les activités malveillantes, Microsoft 365 enregistre de manière centralisée les événements de sécurité et d’autres données et effectue différentes techniques analytiques pour rechercher des activités anormales ou suspectes. Les fichiers journaux sont collectés à partir des serveurs et périphériques d’infrastructure Microsoft 365 et stockés dans une base de données centrale et consolidée.

Microsoft utilise une approche basée sur les risques pour détecter les activités malveillantes. Nous utilisons les données d’incident et la veille contre les menaces pour définir et hiérarchiser nos détections.

L’emploi d’une équipe de personnes expérimentées, compétents et qualifiées est l’un des piliers les plus importants de la réussite de la phase de détection et d’analyse. Microsoft 365 emploie plusieurs équipes de service et ces équipes incluent des employés ayant des compétences sur tous les composants de la pile, y compris le réseau, les routeurs, les pare-feu, les équilibreurs de charge, les systèmes d’exploitation et les applications.

Les mécanismes de détection de sécurité dans Microsoft 365 incluent également des notifications et des alertes initiées par différentes sources. L’équipe de réponse aux incidents de sécurité Microsoft 365 est l’orchestrateur clé du processus d’escalade des incidents de sécurité. Cette équipe reçoit toutes les escalades et est responsable de l’analyse et de la confirmation de la validité de l’incident de sécurité.

L’un des principaux piliers de la détection est la notification :

- Chaque équipe de service est responsable du journal de toute action ou événement à l’intérieur du service en fonction des exigences de l’équipe de sécurité Microsoft 365. Tous les journaux créés par les différentes équipes de service sont traitées par une solution SIEM (Security Information and Event Management) avec des règles de sécurité et de détection prédéfinës. Ces règles évoluent en fonction des recommandations de l’équipe de sécurité Microsoft 365, sur les informations acquises à partir des incidents de sécurité précédents, afin de déterminer s’il existe des activités suspectes ou malveillantes.
- Si un client détermine qu’un incident de sécurité est en cours, il peut ouvrir un dossier de support auprès de Microsoft, qui est affecté à l’équipe de communications de Microsoft 365 Customer Experience (CxP) et transformé en escalade à toutes les équipes appropriées.

Les équipes de service Microsoft 365 utilisent également les renseignements obtenus dans l’analyse de tendance par le biais de la surveillance et de la journalisation de la sécurité pour détecter les attaques dans les systèmes d’information Microsoft 365 qui peuvent indiquer une attaque ou un incident de sécurité. Les serveurs Microsoft 365 regroupent la sortie de ces journaux dans l’environnement de production dans un serveur de journalisation centralisée. À partir de ce serveur de journalisation centralisée, les journaux sont examinés pour repérer les tendances dans l’environnement de production. Les données agrégées sur le serveur centralisé sont transmises en toute sécurité dans un service de journalisation pour l’interrogation avancée, la création et la détection d’activités anormales et malveillantes. Le service utilise également l’apprentissage automatique pour détecter les anomalies avec la sortie du journal.

Pendant la phase d’escalade et en fonction de la nature de l’incident de sécurité, l’équipe de réponse de sécurité Microsoft 365 peut impliquer un ou plusieurs experts techniques de différentes équipes chez Microsoft :

- Équipe sécurité et conformité des services en ligne
- Microsoft Threat Intelligence Center (MSTIC)
- Centre de réponse de sécurité Microsoft (MSRC)
- Affaires d’entreprise, externes et juridiques (CELA)
- Azure Security
- Microsoft 365 engineering, etc.

Avant toute escalade vers l’équipe de réponse de sécurité Microsoft 365, l’équipe de service est chargée de déterminer et de définir le niveau de gravité de l’incident de sécurité en fonction de critères définis, tels que :

- Confidentialité
- Impact
- Portée
- Nombre de locataires affectés
- Région
- Service
- Détails de l’incident
- Réglementations spécifiques du secteur ou du marché des clients.

La priorisation des incidents est déterminée à l’aide de facteurs distincts, y compris, mais sans s’y limiter, l’impact fonctionnel de l’incident, l’impact informationnel de l’incident et la récupération de l’incident.

Après avoir reçu une escalade concernant un incident de sécurité, l’équipe de sécurité Microsoft 365 organise une équipe virtuelle (v-team) composée de membres de l’équipe de réponse de sécurité Microsoft 365, des équipes de service et de l’équipe de communication des incidents Microsoft 365. La partie la plus complexe des activités de cette équipe v consiste à confirmer l’incident de sécurité et à éliminer les faux positifs. La précision des informations fournies par les indicateurs déterminés dans la phase de préparation est essentielle. En analysant ces informations par catégorie d’attaque vectorielle, l’équipe v peut déterminer si l’incident de sécurité est une préoccupation légitime.

Au début de l’enquête, l’équipe de réponse aux incidents de sécurité Office enregistre toutes les informations sur l’incident conformément à nos stratégies de gestion des cas. Au fur et à mesure de la progression du cas, nous suivons les actions en cours et suivons les normes de gestion des preuves pour collecter, conserver et sécuriser ces données tout au long du cycle de vie de l’incident.

Voici quelques exemples de ces actions :

- Résumé, qui est une brève description de l’incident et de son impact potentiel
- Gravité et priorité de l’incident, qui sont dérivées en évaluant l’impact potentiel
- Liste de tous les indicateurs identifiés qui ont conduit à la détection de l’incident
- Liste des incidents associés
- Liste de toutes les actions entreprises par l’équipe v
- Toutes les preuves recueillies, qui seront également conservées pour l’analyse post-mortem et les enquêtes d’investigation ultérieures
- Étapes et actions suivantes recommandées

Après la confirmation des incidents de sécurité, les principaux objectifs de l’équipe de réponse de sécurité Microsoft 365 et de l’équipe de service appropriée sont de contenir l’attaque, de protéger les services en cas d’attaque et d’éviter un impact global plus important. En même temps, les équipes d’ingénierie appropriées travaillent pour déterminer la cause première et préparer le premier plan de récupération.

Dans la phase suivante, l’équipe de réponse de sécurité Microsoft 365 identifie le ou les clients concernés par l’incident de sécurité, le caser. L’étendue de l’effet peut prendre un certain temps pour déterminer, en fonction de la région, du centre de données, du service, de la batterie de serveurs, du serveur, etc. La liste des clients concernés est compilée par l’équipe de service et l’équipe microsoft 365 CxP Communications, qui gèrent ensuite le processus de notification des clients dans le cadre des obligations contractuelles et de conformité.

## <a name="related-articles"></a>Articles connexes

- [Gestion des incidents de sécurité de Microsoft 365](assurance-security-incident-management.md)
- [Préparation de la gestion des incidents de sécurité Microsoft 365](assurance-sim-preparation.md)
- [Contenu, éradication et récupération de la gestion des incidents de sécurité Microsoft 365](assurance-sim-containment-eradication-recovery.md)
- [Activité post-incident de gestion des incidents de sécurité Microsoft 365](assurance-sim-post-incident-activity.md)
