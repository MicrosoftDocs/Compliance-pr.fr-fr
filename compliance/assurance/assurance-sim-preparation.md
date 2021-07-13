---
title: 'Gestion des incidents de sécurité Microsoft : préparation'
description: Cet article fournit une vue d’ensemble du processus de préparation de la gestion des incidents de sécurité dans les services en ligne Microsoft.
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
ms.openlocfilehash: 12a3c657528dd367a475c3db40c09f50bb3aa38a
ms.sourcegitcommit: 8bf2602d56eedee4447ddb374ef95b0587f254e7
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 07/12/2021
ms.locfileid: "53377541"
---
# <a name="microsoft-security-incident-management-preparation"></a>Gestion des incidents de sécurité Microsoft : préparation

## <a name="training-and-background-checks"></a>Formation et vérifications des antécédents

Chaque employé travaillant sur les services en ligne Microsoft est fourni avec une formation sur les incidents de sécurité et les procédures de réponse appropriées à son rôle. Chaque employé de Microsoft reçoit une formation chaque année après s’être joint à l’équipe, puis à une formation d’actualisation annuelle. La formation est conçue pour fournir à l’employé une compréhension de base de l’approche de Microsoft en matière de sécurité afin qu’une fois la formation terminée, tous les employés comprennent :

- Définition d’un incident de sécurité
- Responsabilité de tous les employés de signaler les incidents de sécurité
- Comment faire pour faire revenir un incident de sécurité potentiel à l’équipe de réponse de sécurité Microsoft appropriée
- Réponse des équipes de réponse aux incidents de sécurité Microsoft aux incidents de sécurité
- Problèmes particuliers concernant la confidentialité, en particulier la confidentialité des clients
- Où trouver des informations supplémentaires sur la sécurité et la confidentialité, et les contacts d’escalade
- Tout autre domaine de sécurité pertinent (selon les besoins)

Les employés appropriés reçoivent une formation d’actualisation sur la sécurité annuellement. La formation annuelle sur l’actualisation se concentre sur :

- Toutes les modifications apportées aux procédures d’exploitation standard de l’année précédente
- Responsabilité de chacun de signaler les incidents de sécurité et comment le faire
- Où trouver des informations supplémentaires sur la sécurité et la confidentialité, et les contacts d’escalade
- Tous les autres domaines de sécurité qui peuvent être pertinents chaque année

Chaque employé travaillant sur les services en ligne Microsoft est soumis à une vérification approfondie et appropriée qui inclut l’éducation, l’emploi, les antécédents judiciaires du candidat et d’autres informations spécifiques selon les réglementations des États-Unis telles que la loi HIPAA (Health Insurance Portability and Accountability Act), la réglementation itar (International Traffic in Arms Regulations), le programme fedRAMP (Federal Risk and Authorization Management Program), etc.

Les vérifications des antécédents sont obligatoires pour tous les employés travaillant au sein de l’ingénierie Microsoft. Certains environnements de service en ligne microsoft et rôles d’opérateur peuvent également nécessiter une empreinte digitale complète, des exigences en matière de nationalité, des exigences d’habilitation gouvernementale et d’autres contrôles plus stricts. En outre, certaines équipes et rôles de service peuvent passer par une formation spécialisée en matière de sécurité si nécessaire. Enfin, les membres de l’équipe de sécurité eux-mêmes obtiennent une formation spécialisée et une participation à des conférences directement liées à la sécurité. Cette formation varie selon les besoins de l’équipe et des employés, mais inclut des choses telles que des conférences du secteur, des conférences internes sur la sécurité Microsoft et des cours de formation externes par le biais de fournisseurs de formation en matière de sécurité connus dans le secteur. Nous avons également des articles de formation dédiés à la sécurité publiés tout au long de l’année pour la communauté de la sécurité au sein de Microsoft et spécialisés dans les services en ligne Microsoft régulièrement.

## <a name="penetration-testing--assessment"></a>Tests de pénétration &'évaluation

Microsoft collabore avec différents organismes du secteur et experts en sécurité pour comprendre les nouvelles menaces et les tendances en constante évolution. Microsoft évalue en permanence ses propres systèmes pour les vulnérabilités et les contrats avec divers experts externes indépendants qui en font de même.

Les tests effectués pour le renforcement de la sécurité des services au sein des services en ligne Microsoft peuvent être regroupés en quatre catégories générales :

1. **Tests de sécurité automatisés :** Le personnel interne et externe analyse régulièrement les environnements de service en ligne Microsoft en fonction des pratiques SDL de Microsoft, des 10 principaux risques OWASP (Open Web Application Security Project) et des menaces émergentes signalées par différents organismes du secteur.
2. **Évaluations des vulnérabilités :** Les engagements formels avec des testeurs tiers indépendants valident régulièrement si les contrôles logiques clés fonctionnent efficacement pour respecter les obligations de service de divers organismes de réglementation. Les évaluations sont effectuées par le personnel certifié CREST (Registered Ethical Security Testers) par le Conseil et sont basées sur les 10 principaux risques OWASP et d’autres menaces applicables au service. Toutes les menaces trouvées sont suivis jusqu’à la fermeture.
3. **Test continu des vulnérabilités du système :** Microsoft effectue des tests réguliers dans lesquels les équipes tentent d’enfreinder le système à l’aide de menaces émergentes, de menaces fusion et/ou de menaces persistantes avancées, tandis que d’autres équipes tentent de bloquer ces tentatives de violation.
4. Microsoft Online Services programme de **bogues :** ce programme permet d’autoriser des évaluations de vulnérabilité limitées, d’origine client, sur les services en ligne De Microsoft. Pour plus d’informations, [Microsoft Online Services termes de bogue.](https://www.microsoft.com/msrc/bounty-terms)

Les équipes d’ingénierie des services en ligne De Microsoft publient régulièrement différents documents de conformité. Plusieurs de ces documents sont disponibles dans le cadre d’un accord de non-divulgation à partir du portail d’Microsoft Cloud Service trust [ou](https://aka.ms/STP) de la zone d’assurance de service du [Centre de conformité Microsoft 365](https://compliance.office.com)

>[!NOTE]
>Pour plus d’informations sur la façon d’accéder au portail d’Office 365 pour les entreprises, Azure et Dynamics CRM Online, voir La mise en place du portail d’confiance des services. Un abonnement Microsoft 365 est requis pour accéder au Centre de conformité Microsoft 365.

## <a name="attack-simulation"></a>Simulation d’attaque

Microsoft s’engage dans des exercices de simulation d’attaque en cours et des tests de pénétration de site en direct de nos plans de sécurité et de réponse dans le but d’améliorer la fonctionnalité de détection et de réponse. Microsoft simule régulièrement des violations réelles, effectue une surveillance continue de la sécurité et pratique la réponse aux incidents de sécurité pour valider et améliorer la sécurité des services en ligne Microsoft.

Microsoft exécute une stratégie de sécurité de violation par hypothèse à l’aide de deux équipes principales :

### <a name="red-teams"></a>Équipes rouges

Les équipes Microsoft Red sont des groupes d’employés à plein temps au sein de Microsoft qui se concentrent sur la violation de l’infrastructure, de la plateforme et des propres clients et applications de Microsoft. Il s’agit de l’adversaire dédié (un groupe de pirates informatiques éthiques) qui effectuent des attaques ciblées et persistantes contre les services en ligne (mais pas les applications clientes ou les données). Ils assurent une validation continue de la « gamme complète » (par exemple, contrôles techniques, stratégie papier, réponse humaine, etc.) des fonctionnalités de réponse aux incidents de service.

### <a name="blue-teams"></a>Équipes bleues

Les équipes Microsoft Blue sont composées d’ensembles dédiés de répondeurs de sécurité et de membres issus des équipes de réponse aux incidents de sécurité, d’ingénierie et d’opérations. Ils sont indépendants et fonctionnent séparément des équipes rouges. Les équipes bleues suivent les processus de sécurité établis et utilisent les outils et technologies les plus récents pour détecter les attaques et les tentatives de pénétration et y répondre. Tout comme les attaques réelles, les équipes bleues ne savent pas quand ou comment les attaques de l’équipe rouge se produisent ou quelles méthodes peuvent être utilisées. Leur travail, qu’il s’agit d’une attaque d’équipe rouge ou d’une attaque réelle, consiste à détecter tous les incidents de sécurité et à y répondre. Pour cette raison, les équipes bleues sont continuellement en appel et doivent réagir aux violations de l’équipe rouge de la même manière que pour tout autre adversaire.

Les équipes Microsoft séparent les équipes rouges à temps plein et les équipes bleues au sein de Microsoft dans différentes divisions qui effectuent des opérations à la fois entre les services et au sein de ces équipes. Appelée « équipe rouge » , l’approche consiste à tester les systèmes et opérations de services Microsoft à l’aide des mêmes tactiques, techniques et procédures que les adversaires réels, par rapport à l’infrastructure de production en direct, sans le savoir-faire des équipes d’ingénierie ou d’opérations d’infrastructure et de plateforme. Cela teste les fonctionnalités de détection et de réponse de sécurité et permet d’identifier les vulnérabilités de production, les erreurs de configuration, les hypothèses non valides ou d’autres problèmes de sécurité de manière contrôlée. Chaque violation d’équipe rouge est suivie d’une divulgation complète entre l’équipe rouge et l’équipe bleue, y compris les équipes de service, pour identifier les lacunes, corriger les résultats et améliorer considérablement la réponse aux violations.

>[!NOTE]
>Aucune donnée client n’est ciblée lors des exercices d’équipe rouge ou de pénétration de site en direct. Les tests sont effectués sur Microsoft 365 et l’infrastructure et les plateformes Azure, ainsi que sur les propres clients, applications et données de Microsoft. Les clients, applications et données client hébergés dans Azure, Dynamics 365 ou Microsoft 365 ne sont jamais ciblés selon les règles d’engagement convenues.

### <a name="joint-exercises"></a>Exercices communs

Parfois, les équipes Microsoft Blue et Red effectuent des opérations conjointes où la relation au cours de l’opération est plus partenaire que adversaire avec un groupe sélectionné d’employés de chaque équipe. Ces exercices sont bien coordonnés entre les équipes pour piloter un ensemble plus ciblé de résultats par le biais d’une collaboration en temps réel entre les pirates éthiques et les répondeurs. Ces exercices « d’équipe violet » sont hautement adaptés à chaque opération afin d’optimiser les opportunités, mais chaque opération se base sur le partage d’informations à bande passante élevée et le partenariat pour atteindre les objectifs.

## <a name="related-articles"></a>Articles connexes

- [Gestion des incidents de sécurité Microsoft](assurance-security-incident-management.md)
- [Gestion des incidents de sécurité Microsoft : détection et analyse](assurance-sim-detection-analysis.md)
- [Gestion des incidents de sécurité Microsoft : containment, éradication et récupération](assurance-sim-containment-eradication-recovery.md)
- [Gestion des incidents de sécurité Microsoft : activité post-incident](assurance-sim-post-incident-activity.md)
- [Comment enregistrer un ticket de support d’événement de sécurité](/azure/security/fundamentals/event-support-ticket)
- [Notification de violation Azure et Dynamics 365 dans le cadre du RGPD](/compliance/regulatory/gdpr-breach-azure-dynamics)