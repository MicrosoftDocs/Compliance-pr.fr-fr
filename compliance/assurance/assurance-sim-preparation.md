---
title: 'Gestion des incidents de sécurité Microsoft 365 : préparation'
description: Cet article fournit une vue d’ensemble du processus de préparation de la gestion des incidents de sécurité dans Microsoft 365.
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
ms.openlocfilehash: b14a9fa236cd71cff7dd02baf04a30c249bc4346
ms.sourcegitcommit: 2973d25e9e0185b84d281f963553a332eac1c1a3
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/28/2021
ms.locfileid: "50040337"
---
# <a name="microsoft-365-security-incident-management-preparation"></a>Gestion des incidents de sécurité Microsoft 365 : préparation

## <a name="training-and-background-checks"></a>Formation et vérifications des antécédents

Chaque employé travaillant sur Microsoft 365 est fourni avec une formation sur les incidents de sécurité et les procédures de réponse appropriées à son rôle. Chaque employé de Microsoft 365 reçoit une formation chaque année après s’être joint à l’équipe, puis à une formation d’actualisation annuelle. La formation est conçue pour fournir à l’employé une compréhension de base de l’approche de Microsoft en matière de sécurité afin qu’une fois la formation terminée, tous les employés comprennent :

- Définition d’un incident de sécurité
- Responsabilité de tous les employés de signaler les incidents de sécurité
- Comment faire pour faire escalader un incident de sécurité potentiel à l’équipe de réponse de sécurité Microsoft 365
- Réponse de l’équipe de réponse aux incidents de sécurité Microsoft 365 aux incidents de sécurité
- Problèmes particuliers concernant la confidentialité, en particulier la confidentialité des clients
- Où trouver des informations supplémentaires sur la sécurité et la confidentialité et les contacts d’escalade
- Tout autre domaine de sécurité pertinent (selon les besoins)

Les employés appropriés reçoivent une formation d’actualisation sur la sécurité annuellement. La formation annuelle sur l’actualisation se concentre sur :

- Toutes les modifications apportées aux procédures d’exploitation standard de l’année précédente
- Responsabilité de chacun de signaler les incidents de sécurité et comment le faire
- Où trouver des informations supplémentaires sur la sécurité et la confidentialité et les contacts d’escalade
- Tous les autres domaines de sécurité qui peuvent être pertinents chaque année

Chaque employé travaillant sur Microsoft 365 passe également par une vérification des antécédents appropriée et approfondie qui inclut l’éducation, l’emploi, le antécédents judiciaires du candidat et d’autres informations spécifiques selon les réglementations américaines telles que la loi HIPAA (Health Insurance Portability and Accountability Act), la réglementation itar (International Traffic in Arms Regulations), le programme fedrAMP (Federal Risk and Authorization Management Program) et d’autres.

Les vérifications des antécédents sont obligatoires pour tous les employés travaillant au sein de l’ingénierie Microsoft 365. Certains environnements et rôles d’opérateur Microsoft 365 peuvent également nécessiter une empreinte digitale complète, des exigences de nationalité, des exigences d’habilitation gouvernementale et d’autres contrôles plus stricts. En outre, certaines équipes de service et certains rôles peuvent faire l’aide d’une formation spécialisée en matière de sécurité si nécessaire. Enfin, les membres de l’équipe de sécurité eux-mêmes obtiennent une formation spécialisée et une participation aux conférences directement liées à la sécurité. Cette formation varie selon les besoins de l’équipe et des employés, mais inclut des choses telles que des conférences du secteur, des conférences internes sur la sécurité Microsoft et des cours de formation externes par le biais de fournisseurs de formation en matière de sécurité connus dans le secteur. Nous avons également des articles de formation dédiés à la sécurité publiés tout au long de l’année pour la communauté de la sécurité au sein de Microsoft et spécialisés régulièrement dans Microsoft 365.

## <a name="penetration-testing--assessment"></a>Test de pénétration &'évaluation

Microsoft collabore avec différents organismes du secteur et experts en sécurité pour comprendre les nouvelles menaces et les tendances en constante évolution. Microsoft évalue en permanence ses propres systèmes pour les vulnérabilités et les contrats avec divers experts externes indépendants qui en font de même.

Les tests effectués pour le renforcement du service dans Microsoft 365 peuvent être regroupés en quatre catégories générales :

1. **Tests de sécurité automatisés :** Le personnel interne et externe analyse régulièrement l’environnement Microsoft 365 en fonction des pratiques de Microsoft SDL, des 10 principaux risques du projet OWASP (Open Web Application Security Project) et des menaces émergentes signalées par différents organismes du secteur.
2. **Évaluations des vulnérabilités :** Les engagements formels avec des testeurs tiers indépendants valident régulièrement si les contrôles logiques clés fonctionnent efficacement pour respecter les obligations de service de divers organismes de réglementation. Les évaluations sont effectuées par le personnel certifié CREST (Registered Ethical Security Testers) par le Conseil des 10 principaux risques OWASP et d’autres menaces applicables au service. Toutes les menaces trouvées sont suivis jusqu’à la fermeture.
3. **Tests continus de vulnérabilité du système :** Microsoft effectue des tests réguliers dans lesquels les équipes tentent d’enfreindr le système à l’aide de menaces émergentes, de menaces fusion et/ou de menaces persistantes avancées, tandis que d’autres équipes tentent de bloquer ces tentatives de violation.
4. **Microsoft Online Services programme de bogues**: ce programme permet d’autoriser des évaluations limitées de vulnérabilité d’origine client sur Microsoft 365. Pour plus d’informations, [Microsoft Online Services termes de bogue.](https://www.microsoft.com/msrc/bounty-terms)

L’équipe d’ingénierie Microsoft 365 publie régulièrement différents documents de conformité. Plusieurs de ces documents sont disponibles dans le cadre d’un accord de non-divulgation à partir du portail d’confiance des services cloud [microsoft](https://aka.ms/STP) ou de la zone d’assurance service du Centre de conformité [Microsoft 365.](https://compliance.office.com)

>[!NOTE]
>Pour plus d’informations sur l’accès au portail d’confiance des services, voir La mise en place du portail d’confiance des services pour les abonnements Office 365 pour les entreprises, Azure et Dynamics CRM Online. Un abonnement Microsoft 365 est requis pour accéder au Centre de conformité Microsoft 365.

## <a name="attack-simulation"></a>Simulation d’attaque

Microsoft s’engage dans des exercices de simulation d’attaque en cours et des tests de pénétration de site réel de nos plans de sécurité et de réponse dans le but d’améliorer la détection et la fonctionnalité de réponse. Microsoft simule régulièrement des violations réelles, effectue une surveillance continue de la sécurité et pratique la réponse aux incidents de sécurité pour valider et améliorer la sécurité de Microsoft 365 et Azure.

Microsoft exécute une stratégie de sécurité de violation par hypothèse à l’aide de deux équipes principales :

### <a name="red-teams"></a>Équipes rouges

L’équipe rouge de sécurité Microsoft 365 est un groupe d’employés à plein temps au sein de Microsoft qui se concentre sur la violation de l’infrastructure, de la plateforme et des propres clients et applications de Microsoft. Ils sont l’adversaire dédié (un groupe de pirates informatiques éthiques) qui effectuent des attaques ciblées et persistantes contre les services en ligne (mais pas les applications clientes ou les données). Ils assurent une validation continue du « spectre complet » (par exemple, contrôles techniques, stratégie papier, réponse humaine, etc.) des fonctionnalités de réponse aux incidents de service.

### <a name="blue-teams"></a>Équipes bleues

L’équipe bleue de sécurité Microsoft 365 est composée d’un ensemble dédié de répondeurs de sécurité et de membres issus des équipes de réponse aux incidents de sécurité, d’ingénierie et d’opérations. Ils sont indépendants et fonctionnent séparément de l’équipe rouge. L’équipe bleue suit les processus de sécurité établis et utilise les outils et technologies les plus récents pour détecter les attaques et les tentatives de pénétration et y répondre. Tout comme les attaques réelles, l’équipe bleue ne sait pas quand, comment les attaques de l’équipe rouge se produisent ou quelles méthodes peuvent être utilisées. Leur travail, qu’il s’agit d’une attaque d’équipe rouge ou d’une attaque réelle, consiste à détecter tous les incidents de sécurité et à y répondre. Pour cette raison, l’équipe bleue est en permanence en appel et doit réagir aux violations de l’équipe rouge de la même manière que pour tout autre adversaire.

Les équipes Microsoft séparent les équipes rouges à temps plein et les équipes bleues au sein de Microsoft dans différentes divisions qui effectuent des opérations à la fois entre les services et au sein de ces équipes. Appelée « équipe rouge » , l’approche consiste à tester les systèmes et opérations des services Microsoft à l’aide des mêmes tactiques, techniques et procédures que les adversaires réels, par rapport à l’infrastructure de production en direct, sans le savoir-faire des équipes d’ingénierie ou d’exploitation de plateforme et d’infrastructure. Cela teste les fonctionnalités de détection et de réponse de sécurité et permet d’identifier les vulnérabilités de production, les erreurs de configuration, les hypothèses non valides ou d’autres problèmes de sécurité de manière contrôlée. Chaque violation d’équipe rouge est suivie d’une divulgation complète entre l’équipe rouge et l’équipe bleue, y compris les équipes de service, pour identifier les lacunes, corriger les résultats et améliorer considérablement la réponse aux violations.

>[!NOTE]
>Aucune donnée client n’est ciblée lors des exercices d’équipe rouge ou de pénétration de site en direct. Les tests sont effectués sur l’infrastructure et les plateformes Microsoft 365 et Azure, ainsi que sur les propres clients, applications et données de Microsoft. Les clients, applications et données client hébergés dans Microsoft 365 ou Azure ne sont jamais ciblés selon les règles d’engagement convenues.

### <a name="joint-exercises"></a>Exercices communs

Parfois, les équipes De sécurité Microsoft 365 Bleu et Rouge effectuent des opérations conjointes où la relation au cours de l’opération est plus partenaire qu’adversaire avec un groupe sélectionné d’employés de chaque équipe. Ces exercices sont bien coordonnés entre les équipes pour piloter un ensemble plus ciblé de résultats par le biais d’une collaboration en temps réel entre les pirates éthiques et les répondeurs. Ces exercices « d’équipe violet » sont hautement adaptés à chaque opération afin d’optimiser les opportunités, mais chaque opération se base sur le partage d’informations à bande passante élevée et le partenariat pour atteindre les objectifs.

## <a name="related-articles"></a>Articles connexes

- [Gestion des incidents de sécurité de Microsoft 365](assurance-security-incident-management.md)
- [Détection et analyse de la gestion des incidents de sécurité Microsoft 365](assurance-sim-detection-analysis.md)
- [Contenu, éradication et récupération de la gestion des incidents de sécurité Microsoft 365](assurance-sim-containment-eradication-recovery.md)
- [Activité post-incident de gestion des incidents de sécurité Microsoft 365](assurance-sim-post-incident-activity.md)
