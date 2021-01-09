---
title: Aperçu sur la journalisation d’audit
description: En savoir plus sur la journalisation d’audit dans Microsoft 365
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
ms.openlocfilehash: 6e32e089a5b42f846a332e32218959fef5103615
ms.sourcegitcommit: 7a5b6bc58fc4613b38f3fda20aebee5cec6a5730
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/08/2021
ms.locfileid: "49787503"
---
# <a name="audit-logging-overview"></a>Aperçu sur la journalisation d’audit

## <a name="how-does-microsoft-365-employ-audit-logging"></a>Comment Microsoft 365 utilise-t-il la journalisation d’audit ?

Microsoft 365 utilise la journalisation d’audit pour détecter les activités non autorisées dans ses produits et services et assurer la responsabilité du personnel Microsoft. Les journaux d’audit capturent des détails sur les modifications de configuration système et les événements d’accès, avec des détails pour identifier qui était responsable de l’activité, quand et où l’activité a eu lieu, et quel était le résultat de l’activité. L’analyse automatisée des journaux prend en charge la détection en temps quasi réel de comportements suspects. Les incidents potentiels sont signalés à l’équipe de réponse de sécurité Microsoft 365 pour examen plus approfondie.

La journalisation d’audit interne microsoft 365 capture les données du journal à partir de diverses sources, telles que :

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

## <a name="how-does-microsoft-365-centralize-and-report-on-audit-logs"></a>Comment Microsoft 365 centralise-t-il et signale-t-il les journaux d’audit ?

De nombreux types de données de journal sont téléchargés à partir de serveurs Microsoft 365 vers un service de calcul de big data interne appelé Cosmos. Chaque équipe de service charge les journaux d’audit de leurs serveurs respectifs dans la base de données Cosmos pour l’agrégation et l’analyse. Ce transfert de données se produit via une connexion TLS validée par FIPS 140-2 sur des ports et protocoles approuvés à l’aide d’un outil d’automatisation propriétaire appelé OdL (Office Data Loader).

Les équipes de service exécutent des requêtes limitées sur leurs données dans Cosmos pour la corrélation de journal, les alertes et les rapports. Par exemple, l’équipe de sécurité Microsoft 365 utilise les données de Cosmos avec un analyseur propriétaire du journal des événements pour corréler les données du journal, envoyer des alertes et générer des rapports actionnables sur une activité suspecte possible dans l’environnement de production Microsoft 365. Les rapports issus de ces données sont utilisés pour corriger les vulnérabilités et améliorer les performances globales du service.

## <a name="how-does-microsoft-365-protect-audit-logs"></a>Comment Microsoft 365 protège-t-il les journaux d’audit ?

Les outils utilisés dans Microsoft 365 pour collecter et traiter les enregistrements d’audit n’autorisent pas les modifications définitives ou irréversibles apportées au contenu ou à l’ordre des enregistrements d’audit d’origine. L’accès aux données Microsoft 365 stockées dans Cosmos est limité au personnel autorisé. Microsoft 365 limite la gestion des fonctionnalités d’audit au sous-ensemble limité de membres de l’équipe de service responsables des fonctionnalités d’audit. Ces membres d’équipe n’ont pas la possibilité de modifier ou de supprimer des données de Cosmos, et toutes les modifications apportées aux mécanismes de journalisation de Cosmos sont enregistrées et auditées. Les journaux d’audit sont conservés suffisamment longtemps pour prendre en charge les enquêtes sur les incidents et répondre aux exigences réglementaires. La période exacte de rétention des données du journal d’audit dans Cosmos est déterminée par les équipes de service ; la plupart des données du journal d’audit sont conservées pendant 90 jours ou plus.

## <a name="how-does-microsoft-365-protect-end-user-identifiable-information-that-may-be-captured-in-audit-logs"></a>Comment Microsoft 365 protège-t-il les informations d’identification de l’utilisateur final qui peuvent être capturées dans les journaux d’audit ?

Avant de télécharger des données dans Cosmos, l’application ODL utilise un service de nettoyage pour obscurcir tous les champs qui contiennent des données client, telles que les informations client et les informations d’identification de l’utilisateur final, et remplace ces champs par une valeur de hachage. Les journaux anonymisés et hachés sont réécrits, puis chargés dans Cosmos.

## <a name="related-external-regulations--certifications"></a>Réglementations externes associées & certifications

Les services en ligne de Microsoft sont régulièrement audités pour assurer la conformité avec les réglementations et certifications externes. Reportez-vous au tableau suivant pour la validation des contrôles liés à la journalisation d’audit.

| **Audits externes** | **Section** | **Date de rapport la plus récente** |
|:--------------------|:------------|:-----------------------|
| [FedRAMP (Office 365)](https://compliance.microsoft.com/compliancemanager) | AU-2 : Événements d’audit <br> AU-3 : Contenu des enregistrements d’audit <br> AU-4 : Auditer la capacité de stockage <br> AU-5 : Réponse aux échecs de traitement d’audit <br> AU-6 : vérification, analyse et rapport d’audit <br> AU-7 : Réduction d’audit et génération de rapports <br> AU-8 : horodats <br> AU-9 : Protection des informations d’audit  <br> AU-10 : non-répudiation <br> AU-11 : Rétention d’enregistrement d’audit <br> AU-12 : génération d’audit  | 24 septembre 2020 | 
| [ISO 27001/27002 (Office 365)](https://servicetrust.microsoft.com/ViewPage/MSComplianceGuideV3?command=Download&downloadType=Document&downloadId=d7864d4f-e053-4cc4-a964-fa526d07c3be&tab=7027ead0-3d6b-11e9-b9e1-290b1eb4cdeb&docTab=7027ead0-3d6b-11e9-b9e1-290b1eb4cdeb_ISO_Reports) <br><br> [Déclaration d’applicabilité](https://servicetrust.microsoft.com/ViewPage/MSComplianceGuide?command=Download&downloadType=Document&downloadId=8ee1e46b-2ada-4e7b-bb7d-4c55a8cb6fcd&docTab=4ce99610-c9c0-11e7-8c2c-f908a777fa4d_ISO_Reports) <br> [Certification](https://servicetrust.microsoft.com/ViewPage/MSComplianceGuideV3?command=Download&downloadType=Document&downloadId=1e84a14a-2468-45ac-9412-5e53250d57ec&tab=7027ead0-3d6b-11e9-b9e1-290b1eb4cdeb&docTab=7027ead0-3d6b-11e9-b9e1-290b1eb4cdeb_ISO_Reports) | A.12.4 : Journalisation et surveillance | 22 février 2020 |
| [ISO 27017 (Office 365)](https://servicetrust.microsoft.com/ViewPage/MSComplianceGuideV3?command=Download&downloadType=Document&downloadId=d7864d4f-e053-4cc4-a964-fa526d07c3be&tab=7027ead0-3d6b-11e9-b9e1-290b1eb4cdeb&docTab=7027ead0-3d6b-11e9-b9e1-290b1eb4cdeb_ISO_Reports) <br><br> [Déclaration d’applicabilité](https://servicetrust.microsoft.com/ViewPage/MSComplianceGuide?command=Download&downloadType=Document&downloadId=8ee1e46b-2ada-4e7b-bb7d-4c55a8cb6fcd&docTab=4ce99610-c9c0-11e7-8c2c-f908a777fa4d_ISO_Reports) <br> [Certification](https://servicetrust.microsoft.com/ViewPage/MSComplianceGuideV3?command=Download&downloadType=Document&downloadId=70de0999-5451-43a3-9ef4-761e8fbfb1a3&tab=7027ead0-3d6b-11e9-b9e1-290b1eb4cdeb&docTab=7027ead0-3d6b-11e9-b9e1-290b1eb4cdeb_ISO_Reports) | A.12.4 : Journalisation et surveillance | 22 février 2020 |
| [SOC 1 (Office 365)](https://servicetrust.microsoft.com/ViewPage/MSComplianceGuideV3?command=Download&downloadType=Document&downloadId=90df3f9c-3aaf-4dbf-99d0-ca9f2991721b&tab=7027ead0-3d6b-11e9-b9e1-290b1eb4cdeb&docTab=7027ead0-3d6b-11e9-b9e1-290b1eb4cdeb_SOC_%2F_SSAE_16_Reports) | CA-48 : journalisation du centre de données <br> CA-60 : Journalisation d’audit | 24 décembre 2020 |
| [SOC 2 (Office 365)](https://servicetrust.microsoft.com/ViewPage/MSComplianceGuideV3?command=Download&downloadType=Document&downloadId=a73c1738-7892-42b7-acd3-87b6371c53f6&tab=7027ead0-3d6b-11e9-b9e1-290b1eb4cdeb&docTab=7027ead0-3d6b-11e9-b9e1-290b1eb4cdeb_SOC_%2F_SSAE_16_Reports) | CA-48 : journalisation du centre de données <br> CA-60 : Journalisation d’audit | 24 décembre 2020|