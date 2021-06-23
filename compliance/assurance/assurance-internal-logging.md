---
title: Microsoft 365 journalisation interne pour Microsoft 365'ingénierie
description: Dans cet article, trouvez une explication du fonctionnement de la journalisation interne Microsoft 365'équipes d’ingénierie.
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
ms.openlocfilehash: 71b08509ae920ad88ecfa1566b9a11d640b0534f
ms.sourcegitcommit: fb379d1110a9a86c7f9bab8c484dc3f4b3dfd6f0
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 06/23/2021
ms.locfileid: "53088593"
---
# <a name="internal-logging-for-microsoft-365-engineering"></a>Journalisation interne pour Microsoft 365 Engineering

En plus des événements et des données de journal disponibles pour les clients, Microsoft maintient un système interne de collecte de données de journal qui est disponible pour Microsoft 365 ingénieurs. De nombreux types différents de données de journal sont téléchargés à partir de serveurs Microsoft 365 vers une solution de surveillance de la sécurité propriétaire pour l’analyse en temps quasi réel (NRT) et un service interne de big data computing (Cosmos) pour le stockage à long terme. Ce transfert de données se produit via une connexion TLS validée PAR LA FIPS 140-2 sur des ports et protocoles approuvés à l’aide d’un outil d’automatisation propriétaire appelé odl Office Data Loader( ODL). Les outils utilisés dans Microsoft 365 pour collecter et traiter les enregistrements d’audit n’autorisent pas les modifications définitives ou irréversibles apportées au contenu ou à l’ordre des enregistrements d’audit d’origine.

Les équipes de service utilisent Cosmos comme référentiel centralisé pour effectuer une analyse de l’utilisation des applications, pour mesurer les performances système et opérationnelles, et pour rechercher des anomalies et des modèles qui peuvent indiquer des problèmes ou des problèmes de sécurité. Chaque équipe de service charge une ligne de base qui inclut :

- Journaux d’événements
- Journaux AppLocker
- Données de performances
- System Center données
- Enregistrements des détails des appels
- Données de qualité de l’expérience
- Journaux du serveur web IIS
- SQL Server journaux
- Données Syslog
- Journaux d’audit de sécurité

Avant le chargement, l’application ODL utilise un service de nettoyage pour supprimer les champs qui contiennent des données client, telles que les informations client et les informations d’identification de l’utilisateur final, et remplacer ces champs par une valeur de hachage. Les journaux nettoyés sont téléchargés vers Cosmos et vers la solution de surveillance de la sécurité NRT qui analyse les journaux pour les événements de sécurité potentiels et les indicateurs de performances. La période de rétention des données du journal d’audit dans Cosmos est déterminée par les équipes de service ; la plupart des données du journal d’audit sont conservées pendant 90 jours ou plus pour prendre en charge les enquêtes sur les incidents de sécurité et pour répondre aux exigences de rétention réglementaires.

L’accès Microsoft 365 données stockées dans Cosmos est limité au personnel autorisé. Microsoft limite la gestion des journaux d’audit à un sous-ensemble limité de membres de l’équipe de sécurité responsables des fonctionnalités d’audit. L’équipe de sécurité n’a pas d’accès administratif permanent aux Cosmos, et toutes les modifications sont enregistrées et auditées.

Après l’analyse NRT, chaque équipe de service peut utiliser des outils d’analyse et des tableaux de bord pour la corrélation de données, les requêtes interactives et l’analyse des données. Ces rapports sont utilisés pour surveiller et améliorer les performances globales du service.
