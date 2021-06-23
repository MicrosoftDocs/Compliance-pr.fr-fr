---
title: Sécurisation de l’infrastructure Microsoft 365 réseau
description: Découvrez comment Microsoft sécurisation l’infrastructure Microsoft 365 réseau.
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
hideEdit: true
ms.openlocfilehash: 224900bd60f2fd5637e7264f1aed98d5ff878b20
ms.sourcegitcommit: fb379d1110a9a86c7f9bab8c484dc3f4b3dfd6f0
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 06/23/2021
ms.locfileid: "53089640"
---
# <a name="securing-the-microsoft-365-infrastructure"></a>Sécurisation de l’infrastructure Microsoft 365 réseau

Microsoft 365 est l’un des plus grands services cloud d’entreprise et grand public au monde et continue de croître rapidement, à la fois dans la base de clients, les produits et les fonctionnalités. Les clients se tournent Microsoft 365 non seulement pour ses solutions de productivité de niveau mondial, mais aussi pour protéger leurs informations les plus sensibles contre l’évolution constante du paysage des cybermenaces. La priorité de Microsoft est de sécuriser les données client et de maintenir la confiance des clients.

La sécurisation d’un système de cette échelle et de cette complexité n’est pas possible si la sécurité est une opération de après, elle n’est efficace que si la sécurité est intégrée au cours du processus de conception initial. Il nécessite un système de détection des menaces robuste avec des réponses rapides de systèmes automatisés et d’ingénieurs hautement qualifiés. L’évaluation et la validation continues de ces systèmes sont essentielles pour garantir que les configurations sécurisées restent intactes et que des vulnérabilités précédemment inconnues sont identifiées.

## <a name="core-security-principles"></a>Principes de sécurité fondamentaux

Sept principes de sécurité sont à  la base de notre infrastructure de protection des services Microsoft 365 contre les  menaces,  de détection et de réponse aux menaces, et d’évaluation continue de la posture de sécurité et de l’amélioration des services en fonction des résultats de ces évaluations.

- **Confidentialité des données**: les clients possèdent leurs données et Microsoft est le dépositaire. Microsoft 365 services sont conçus pour fonctionner sans que les ingénieurs n’accèdent aux données client, à moins d’être explicitement demandés et approuvés par le client.
- **Supposer une violation**: le personnel et les services sont traités comme si la compromission était une possibilité réelle.
- **Privilège minimum**: l’accès et les autorisations aux ressources sont limités à ce qui est nécessaire pour effectuer les tâches nécessaires.
- **Limites de violation :** les identités et l’infrastructure d’une frontière sont isolées des ressources d’autres frontières. La compromission d’une limite ne doit pas conduire à une compromission d’une autre.
- **Sécurité intégrée de** la structure de service : les priorités et exigences en matière de sécurité sont intégrées à la conception de nouvelles fonctionnalités et fonctionnalités, ce qui garantit une forte mise à l’échelle de la posture de sécurité avec chaque service.
- **Automatisé** et automatique : Microsoft se concentre sur le développement de produits et d’architectures durables capables d’appliquer de manière intelligente et automatique la sécurité des services, tout en offrant aux ingénieurs Microsoft la possibilité de gérer en toute sécurité les réponses aux menaces de sécurité à grande échelle.
- **Sécurité adaptative**: les fonctionnalités de sécurité Microsoft s’adaptent aux modèles d’apprentissage automatique, aux tests de pénétration de routine et aux évaluations automatisées et y sont améliorées.

## <a name="protection"></a>Protection

### <a name="access-control"></a>Contrôle d’accès

Par défaut, le personnel responsable du développement et de la maintenance Microsoft 365 services a un accès permanent zéro (ZSA) à l’infrastructure de service. Bien que Microsoft s’efforce d’engager uniquement les meilleurs ingénieurs et que des vérifications rigoureuses des antécédents soient requises, Microsoft ne suppose pas qu’ils sont fiables par défaut dans les services d’exploitation. En outre, lorsque les ingénieurs sont approuvés pour l’accès privilégié, ils ne sont autorisés à accéder que pour une durée limitée afin d’effectuer uniquement les actions nécessaires pour une étendue spécifique de l’infrastructure de service. Microsoft fait référence à ces stratégies comme juste-à-temps (JIT) et JeA (Just-Enough-Access) qui sont implémentées via un système appelé Lockbox.

Pour acquérir des privilèges élevés, les ingénieurs Microsoft envoient une demande pour la tâche spécifique et spécifient la période à exécuter. Une fois approuvé, Lockbox génère un compte JIT spécialisé avec la possibilité d’effectuer uniquement la tâche demandée. Les actions prennent généralement la forme de flux de travail automatisés qui effectuent en toute sécurité les opérations de dépannage ou de récupération requises. Dans de rares cas où l’accès direct à l’infrastructure est nécessaire, des stations de travail à accès privilégié (PAW) strictement surveillées sont requises.

Les utilisateurs non autorisé et les comptes compromis sont une possibilité réelle dans n’importe quelle organisation, et notre système de contrôle d’accès est conçu pour se protéger contre ces menaces.

Pour plus d’informations sur le contrôle d’accès, voir [vue d’ensemble de la gestion des identités et des accès.](assurance-identity-and-access-management.md)

### <a name="encryption"></a>Chiffrement

Bien que les contrôles d’accès jouent un rôle vital dans la défense des services Microsoft 365, le chiffrement est utilisé tout au long du cycle de vie des données pour protéger davantage la confidentialité et la confidentialité pour les clients Microsoft.

Les données en transit entre les ordinateurs clients, Microsoft 365 serveurs et les serveurs non Microsoft 365 sont chiffrées à l’aide de TLS 1.2. Nous examinerons régulièrement les chiffrements et les protocoles utilisés, en ajoutant des protocoles améliorés lorsqu’ils sont disponibles et en supprimant les protocoles plus faibles selon les besoins.

Le contenu client au repos sur les serveurs Microsoft est chiffré au niveau du volume à l’aide de BitLocker. Le chiffrement au niveau de l’application peut également être appliqué à l’aide de clés gérées par Microsoft ou le client. L’accès aux clés gérées par Microsoft n’est possible qu’en cas d’autorisation et d’approbation par le biais du processus JIT et JEA.

Pour plus d’informations sur le chiffrement Microsoft 365, voir [la vue d’ensemble du](assurance-encryption.md)chiffrement et de la gestion des clés.

### <a name="network-isolation"></a>Isolation du réseau

En accord avec le principe du moindre privilège, Microsoft 365 limite la communication entre les différentes parties de l’infrastructure de service uniquement à ce qui est nécessaire pour fonctionner. Tout le trafic réseau est refusé par défaut, seules les communications explicitement définies étant autorisées. Cette restriction établit des limites de violation dans toute l’infrastructure. Teams qui souhaitent ajouter de nouveaux chemins d’accès réseau pour prendre en charge une nouvelle fonctionnalité à leur service doivent avoir évalué et approuvé la demande avant de pouvoir être ouverte.

Pour plus d’informations sur l’isolation réseau dans Microsoft 365, voir [Microsoft 365 d’isolation.](/microsoft-365/enterprise/microsoft-365-isolation-controls)

## <a name="detection--response"></a>Réponse & détection

### <a name="security-monitoring"></a>Surveillance de la sécurité

La surveillance de la sécurité à grande échelle de Microsoft n’est possible qu’en générant des alertes très précises à l’aide de solutions informatiques automatisées. Les journaux d’audit de chaque service et données de télémétrie recueillies à partir de l’ensemble de l’infrastructure principale sont envoyés à une solution propriétaire centralisée de traitement et d’alerte en temps quasi réel.

Dans la mesure du possible, les menaces détectées sont corrigés à l’aide d’actions déclenchées automatiquement. Lorsque les solutions automatisées échouent ou sont incapables de résoudre le problème, les ingénieurs Microsoft d’appel prennent immédiatement des mesures pour atténuer la menace.

Pour plus d’informations sur la surveillance de la sécurité dans Microsoft 365, voir [Vue d’ensemble de la surveillance de la sécurité.](assurance-security-monitoring.md)

## <a name="assessment"></a>Évaluation

### <a name="automated-assessments"></a>Évaluations automatisées

Quelle que soit la façon dont un système est conçu, la posture de sécurité peut se dégrader en raison d’une dérive de configuration intentionnelle et involontaire au fil du temps. Les outils automatisés évaluent Microsoft 365 systèmes qui recherchent des services non configurés et mal configurés. Cette évaluation est souvent appelée correction, antivirus, vulnérabilité et analyse de configuration (PAVC).

Notre architecture est également fréquemment validée, en identifiant des instances telles que des comptes et des ports ouverts inutilisés avec un accès administratif permanent. Tous les services qui dérivent d’un état prédéfiny souhaité sont automatiquement de nouveau alignés.

Pour plus d’informations sur la surveillance de la sécurité dans Microsoft 365, voir [vue d’ensemble de la gestion des vulnérabilités.](assurance-vulnerability-management.md)

### <a name="attack-simulation-and-penetration-testing"></a>Simulation d’attaque et test de pénétration

Microsoft 365 la priorité la plus élevée consiste à empêcher les attaques d’introduire des défenses. Microsoft 365 dispose d’une équipe dédiée d’experts en sécurité qui effectuent en permanence des attaques simulées pour identifier les vulnérabilités précédemment inconnues et fournir un flux constant de données enrichies afin d’améliorer les fonctionnalités de surveillance de la sécurité. Ces attaques simulées prennent la forme d’attaques automatisées fréquentes à petite échelle et de profondeurs pilotées par des experts. À partir de ces activités, Microsoft évalue la capacité à détecter, à répondre et à déloger des personnes malveillantes.

Pour plus d’informations sur la surveillance de la sécurité dans Microsoft 365, voir [simulation d’attaque dans Microsoft 365](assurance-monitoring-and-testing.md).

## <a name="resources"></a>Ressources

[Dans les coulisses : sécurisation de l’infrastructure influençant le service Microsoft 365](https://download.microsoft.com/download/c/4/5/c45b197e-f0d9-4f40-bd5f-ed8fc7d0cd8c/M365DCSecurityIntro_Whitepaper.pdf)
