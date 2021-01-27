---
title: Simulation d’attaques dans Microsoft 365
description: Dans cet article, découvrez comment Microsoft surveille et teste en permanence les limites du client pour Microsoft 365.
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
ms.collection:
- Strat_O365_IP
- M365-security-compliance
- MS-Compliance
f1.keywords:
- NOCSH
ms.custom: seo-marvel-apr2020
titleSuffix: Microsoft Service Assurance
ms.openlocfilehash: 9d38131a6ec8f3213c288d76dc3b176ceaa3aace
ms.sourcegitcommit: b06fa9f1b230fd5e470817486ea51f460f28b691
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/27/2021
ms.locfileid: "50012890"
---
# <a name="attack-simulation-in-microsoft-365"></a>Simulation d’attaques dans Microsoft 365

Microsoft surveille et teste en permanence les faiblesses et les vulnérabilités dans les limites du client, y compris la surveillance des intrusions, des tentatives de violation d’autorisation et de l’insévation des ressources. Nous utilisons également plusieurs systèmes internes pour surveiller en permanence l’utilisation inappropriée des ressources, ce qui, s’il est détecté, déclenche une limitation intégrée.

Microsoft 365 dispose de systèmes de surveillance internes qui surveillent en permanence les défaillances et qui pilotent la récupération automatisée en cas de détection d’une défaillance. Les systèmes Microsoft 365 analysent les écarts dans le comportement du service et lancent des processus de auto-ressource intégrés au système. Microsoft 365 utilise également la surveillance externe dans laquelle la surveillance est effectuée à partir de plusieurs emplacements à la fois à partir de services tiers de confiance (pour la vérification du SLA indépendant) et de nos propres centres de données pour lever des alertes. Pour les diagnostics, nous avons une journalisation, un audit et un suivi complets. Le suivi et la surveillance granulaires nous aident à isoler les problèmes et à effectuer une analyse rapide et efficace des causes premières.

Bien que Microsoft 365 dispose d’actions de récupération automatisées dans la mesure du possible, les ingénieurs microsoft en appel sont disponibles 24 heures sur 24 et 7 jours sur 7 pour examiner toutes les escalades de sécurité de gravité 1, et les examens post-mortem de chaque incident de service contribuent à l’apprentissage continu et à l’amélioration. Cette équipe inclut des ingénieurs de support technique, des développeurs de produits, des responsables de programmes, des responsables de produits et des cadres supérieurs. Nos professionnels de l’appel fournissent une sauvegarde en temps voulu et peuvent souvent automatiser les actions de récupération, de sorte que la prochaine fois qu’un événement se produit, il peut être auto-rétabli.

Microsoft effectue un examen approfondi après incident chaque fois qu’un incident de sécurité Microsoft 365 se produit, quelle que soit l’ampleur de l’impact. Un examen post-incident se compose d’une analyse de ce qui s’est passé, de la façon dont nous avons répondu et de la façon dont nous avons empêché des incidents similaires à l’avenir. Dans un souci de transparence et de responsabilité, nous partageons la révision post-incident pour les incidents de service majeurs avec les clients concernés. Pour plus d’informations, voir Gestion des incidents de sécurité [Office 365.](https://aka.ms/Office365SIM)

## <a name="assume-breach-methodology"></a>Supposer une méthodologie de violation

Sur la base d’une analyse détaillée des tendances de sécurité, Microsoft recommande et met en évidence la nécessité d’autres investissements dans des processus et technologies de sécurité réactifs qui se concentrent sur la détection et la réponse aux menaces émergentes, plutôt que sur la prévention de ces menaces uniquement. En raison des modifications apportées au paysage des menaces et de l’analyse approfondie, Microsoft a affiné sa stratégie de sécurité au-delà de la simple prévention des violations de sécurité en une personne mieux dotée pour traiter les violations lorsqu’elles se produisent ; une stratégie qui considère les événements de sécurité majeurs non pas pour savoir si, mais quand.

Bien que [](https://www.microsoft.com/TrustCenter/Security/default.aspx) les pratiques de violation de l’hypothèse de Microsoft soient en place depuis de nombreuses années, de nombreux clients ignorent que le travail en arrière-plan est effectué pour renforce le cloud Microsoft. Supposons que la violation est un état d’esprit qui guide les investissements en matière de sécurité, les décisions de conception et les pratiques de sécurité opérationnelles. Supposons que la violation limite l’confiance placée dans les applications, les services, les identités et les réseaux en les traitant toutes (internes et externes) comme non sécurisées et déjà compromises. Bien que la stratégie d’hypothèse de violation n’a pas été portée à partir d’une violation réelle d’une entreprise Microsoft ou de services cloud, il a été reconnu que de nombreuses organisations, dans le secteur, ont été enfreintes malgré toutes les tentatives pour l’empêcher. Bien que la prévention des violations soit un élément essentiel des opérations de toute organisation, ces pratiques doivent être continuellement testées et augmentées pour répondre efficacement aux adversaires modernes et aux menaces persistantes avancées. Pour que toute organisation se prépare à une violation, elle doit d’abord créer et maintenir des procédures de réponse de sécurité robustes, extensibles et minutieusement testées.

Bien que les processus de sécurité de prévention des violations, tels que la modélisation des menaces, les révisions de code et les tests de sécurité soient très utiles dans le cadre du cycle de vie du développement de la [sécurité,](https://www.microsoft.com/securityengineering/sdl/)supposons que la violation offre de nombreux avantages qui permettent de prendre en compte la sécurité globale en faisant des exercices et en mesurant les fonctionnalités réactives en cas de violation.

Chez Microsoft, nous nous sommes fixés pour objectif d’y parvenir par le biais d’exercices de conflit en cours et de tests de pénétration de site en direct de nos plans de réponse de sécurité dans le but d’améliorer nos fonctionnalités de détection et de réponse. Microsoft simule régulièrement des violations réelles, effectue une surveillance continue de la sécurité et pratique la gestion des incidents de sécurité pour valider et améliorer la sécurité de Microsoft 365, Azure et d’autres services cloud Microsoft.

Microsoft exécute sa stratégie d’hypothèse de sécurité de violation à l’aide de deux groupes principaux :

- Équipes rouges (attaquants)
- Équipes bleues (défenseurs)

Les équipes Microsoft Azure et Microsoft 365 séparent les équipes rouges à temps plein et les équipes bleues.

Appelée « équipe[](https://go.microsoft.com/fwlink/?linkid=518599)rouge », l’approche consiste à tester les systèmes et opérations Azure et Microsoft 365 à l’aide des mêmes tactiques, techniques et procédures que les adversaires réels, par rapport à l’infrastructure de production en direct, sans le savoir-faire des équipes techniques ou opérationnelles. Cela teste les fonctionnalités de détection et de réponse de sécurité de Microsoft, et permet d’identifier les vulnérabilités de production, les erreurs de configuration, les hypothèses non valides et d’autres problèmes de sécurité de manière contrôlée. Chaque violation d’équipe rouge est suivie d’une divulgation complète entre les deux équipes afin d’identifier les lacunes, de corriger les résultats et d’améliorer la réponse aux violations.

**REMARQUE**: aucune donnée client n’est délibérément ciblée lors de l’équipe rouge ou des tests de pénétration de site en direct. Les tests sont effectués sur l’infrastructure et les plateformes Microsoft 365 et Azure, ainsi que sur les propres clients, applications et données de Microsoft. Les clients, les applications et le contenu hébergés dans Microsoft 365 ou Azure ne sont jamais ciblés.

## <a name="red-teams"></a>Équipes rouges

L’équipe rouge est un groupe d’employés à plein temps au sein de Microsoft qui se concentre sur la violation de l’infrastructure, de la plateforme et des propres clients et applications de Microsoft. Ils sont l’adversaire dédié (un groupe de pirates informatiques éthiques) qui effectuent des attaques ciblées et persistantes contre les services en ligne (infrastructure, plateformes et applications Microsoft, mais pas les applications ou le contenu des clients finaux).

Le rôle de l’équipe rouge consiste à attaquer et à attaquer des environnements en utilisant les mêmes étapes qu’un adversaire :

![Étapes de violation](../media/office-365-isolation-breach-stages.png)

Entre autres fonctions, les équipes rouges tentent spécifiquement d’enfreindr les limites de l’isolation des clients pour trouver des bogues ou des lacunes dans notre conception d’isolation.

## <a name="blue-teams"></a>Équipes bleues

L’équipe bleue est composée d’un ensemble dédié de répondeurs de sécurité ou de membres de l’ensemble des organisations de réponse aux incidents de sécurité, d’ingénierie et d’opérations. Quel que soit leur make-up, ils sont indépendants et fonctionnent séparément de l’équipe rouge. L’équipe bleue suit les processus de sécurité établis et utilise les outils et technologies les plus récents pour détecter les attaques et les intrusions et y répondre. Tout comme les attaques réelles, l’équipe bleue ne sait pas quand, comment les attaques de l’équipe rouge se produisent ou quelles méthodes peuvent être utilisées. Leur travail, qu’il s’agit d’une attaque d’équipe rouge ou d’une attaque réelle, consiste à détecter tous les incidents de sécurité et à y répondre. Pour cette raison, l’équipe bleue est en permanence en appel et doit réagir aux violations de l’équipe rouge de la même manière que pour toute autre violation.

Lorsqu’un adversaire, tel qu’une équipe rouge, a enfreint un environnement, l’équipe bleue doit :

- Recueillir les preuves laissées par l’adversaire
- Détecter les preuves comme indication de compromission
- Alerter les équipes techniques et d’exploitation appropriées
- Trier les alertes pour déterminer s’ils justifient un examen plus approfondie
- Collecter le contexte de l’environnement pour la portée de la violation
- Créer un plan de correction pour contenir ou évincer l’adversaire
- Exécuter le plan de correction et récupérer d’une violation

Ces étapes forment la réponse aux incidents de sécurité parallèle à celle de l’adversaire, comme illustré ci-dessous :

![Étapes de réponse aux violations](../media/office-365-isolation-breach-response-stages.png)

Les violations d’équipe rouge permettent d’exercer la capacité de l’équipe bleue à détecter les attaques réelles et à y répondre de bout en bout. Plus important encore, il permet une réponse pratique aux incidents de sécurité avant une violation authentique. En outre, en raison de violations de l’équipe rouge, l’équipe bleue améliore sa connaissance de la situation, ce qui peut être utile lors de futures violations (qu’il s’agit de l’équipe rouge ou d’un autre adversaire). Tout au long du processus de détection et de réponse, l’équipe bleue produit des renseignements actionnables et obtient une visibilité sur les conditions réelles de l’environnement qu’elle tente de défendre. Souvent, cela s’effectue via l’analyse des données et les enquêtes légales, effectuées par l’équipe bleue, lors de la réponse aux attaques d’équipe rouge et en établissant des indicateurs de menace, tels que des indicateurs de compromission. Tout comme l’équipe rouge identifie les lacunes dans l’article de sécurité, les équipes bleues identifient les lacunes dans leur capacité à détecter et à répondre. En outre, étant donné que les équipes rouges modélisent des attaques réelles, l’équipe bleue peut être évaluée avec précision sur sa capacité ou son incapacité à gérer des adversaires déterminés et persistants. Enfin, les violations d’équipe rouge mesurent à la fois la préparation et l’impact de notre réponse aux violations.
