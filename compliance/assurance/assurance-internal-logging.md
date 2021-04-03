---
title: Journalisation interne de Microsoft 365 pour l’ingénierie Microsoft 365
description: Dans cet article, découvrez une explication du fonctionnement de la journalisation interne pour les équipes d’ingénierie Microsoft 365.
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
hideEdit: true
ms.openlocfilehash: 110a61c27a00380eede4d4f2303acfb025a27a1f
ms.sourcegitcommit: 024137a15ab23d26cac5ec14c36f3577fd8a0cc4
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 04/01/2021
ms.locfileid: "51497072"
---
# <a name="internal-logging-for-microsoft-365-engineering"></a>Journalisation interne pour Microsoft 365 Engineering

Outre les événements et les données de journal disponibles pour les clients, il existe également un système interne de collecte de données de journal qui est disponible pour les ingénieurs Microsoft 365 chez Microsoft. De nombreux types de données de journal sont téléchargés à partir de serveurs Microsoft 365 vers un service de calcul de big data interne appelé Cosmos. Chaque équipe de service charge les journaux d’audit de leurs serveurs respectifs dans la base de données Cosmos pour l’agrégation et l’analyse. Ce transfert de données se produit via une connexion TLS validée par FIPS 140-2 sur des ports et protocoles spécifiquement approuvés à l’aide d’un outil d’automatisation propriétaire appelé OdL (Office Data Loader). Les outils utilisés dans Microsoft 365 pour collecter et traiter les enregistrements d’audit n’autorisent pas les modifications définitives ou irréversibles apportées au contenu ou à l’ordre des enregistrements d’audit d’origine.

Les équipes de service utilisent Cosmos comme référentiel centralisé pour effectuer une analyse de l’utilisation des applications, pour mesurer les performances système et opérationnelles, et pour rechercher des anomalies et des modèles qui peuvent indiquer des problèmes ou des problèmes de sécurité. Chaque équipe de service charge une ligne de base des journaux dans Cosmos, en fonction de ce qu’elle cherche à analyser, qui incluent souvent :

- Journaux des événements
- Journaux AppLocker
- Données de performances
- Données System Center
- Enregistrements des détails des appels
- Données de qualité de l’expérience
- Journaux du serveur web IIS
- SQL Server journaux
- Données Syslog
- Journaux d’audit de sécurité

Avant de télécharger des données dans Cosmos, l’application ODL utilise un service de nettoyage pour obscurcir tous les champs qui contiennent des données client, telles que les informations client et les informations d’identification de l’utilisateur final, et remplace ces champs par une valeur de hachage. Les journaux anonymisés et hachés sont réécrits, puis chargés dans Cosmos. Les équipes de service exécutent des requêtes limitées sur leurs données dans Cosmos pour la corrélation, les alertes et les rapports. La période de rétention des données du journal d’audit dans Cosmos est déterminée par les équipes de service ; la plupart des données du journal d’audit sont conservées pendant 90 jours ou plus pour prendre en charge les enquêtes sur les incidents de sécurité et pour répondre aux exigences de rétention réglementaires.

L’accès aux données Microsoft 365 stockées dans Cosmos est limité au personnel autorisé. Microsoft limite la gestion des fonctionnalités d’audit au sous-ensemble limité de membres de l’équipe de service responsables des fonctionnalités d’audit. Ces membres d’équipe n’ont pas la possibilité de modifier ou de supprimer des données de Cosmos, et toutes les modifications apportées aux mécanismes de journalisation de Cosmos sont enregistrées et auditées.

Chaque équipe de service accède à ses données de journal pour analyse en autorisant certaines applications à effectuer une analyse spécifique. Par exemple, l’équipe de sécurité Microsoft 365 utilise les données de Cosmos via un analyseur propriétaire du journal des événements pour corréler, alerter et générer des rapports actionnables sur les activités suspectes possibles dans l’environnement de production Microsoft 365. Les rapports issus de ces données sont utilisés pour corriger les vulnérabilités et améliorer les performances globales du service. Si une alerte ou un rapport spécifique nécessite un examen plus approfondie, le personnel du service peut demander que les données soient importées dans le service Microsoft 365. Étant donné que le journal spécifique importé à partir de Cosmos est chiffré et que le personnel du service n’a pas accès aux clés de déchiffrement, le journal cible est transmis par programme par le biais d’un service de déchiffrement qui renvoie les résultats d’étendue au personnel du service autorisé. Les vulnérabilités trouvées dans cet exercice sont signalées et escalades à l’aide des canaux de gestion des incidents de sécurité standard de Microsoft.
