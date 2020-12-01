---
title: Vue d’ensemble de la journalisation d’audit
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
ms.openlocfilehash: 3714a5df73253d0814e1d4067248116cb6e10a40
ms.sourcegitcommit: 626b0076d133e588cd28598c149a7f272fc18bae
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 11/30/2020
ms.locfileid: "49507114"
---
# <a name="audit-logging-overview"></a>Vue d’ensemble de la journalisation d’audit

## <a name="how-does-microsoft-365-employ-audit-logging"></a>Comment Microsoft 365 utilise-t-il la journalisation d’audit ?

Microsoft 365 utilise la journalisation d’audit pour détecter les activités non autorisées dans ses produits et services et fournir des responsabilités aux employés de Microsoft. Les journaux d’audit comportent des détails sur les modifications de configuration système et les événements d’accès, avec des détails pour identifier les responsables de l’activité, le moment et l’endroit où l’activité a eu lieu, ainsi que le résultat de l’activité. L’analyse de journal automatisé prend en charge la détection en temps réel de comportement suspect. Les incidents potentiels sont transmis à l’équipe de réponse de sécurité Microsoft 365 pour une meilleure étude.

La journalisation d’audit interne de Microsoft 365 capture les données du journal à partir de plusieurs sources, telles que :

- Journaux des événements
- Journaux AppLocker
- Données de performances
- Données System Center
- Enregistrements des détails des appels
- Données de qualité de l’expérience
- Journaux de serveur Web IIS
- Journaux SQL Server
- Données syslog
- Journaux d’audit de sécurité

## <a name="how-does-microsoft-365-centralize-and-report-on-audit-logs"></a>Comment Microsoft 365 centraliser et rendre compte des journaux d’audit ?

De nombreux types de données de journal sont téléchargés à partir des serveurs Microsoft 365 vers un service informatique interne et de grande taille appelé Cosmos. Chaque équipe de service télécharge les journaux d’audit de leurs serveurs respectifs dans la base de données Cosmos pour l’agrégation et l’analyse. Ce transfert de données se produit sur une connexion TLS validée par FIPS 140-2 sur les ports et protocoles approuvés à l’aide d’un outil Automation propriétaire appelé le chargeur de données Office (ODL).

Les équipes de service exécutent des requêtes délimitées par rapport à leurs données dans Cosmos pour la corrélation des journaux, les alertes et la création de rapports. Par exemple, l’équipe de sécurité de Microsoft 365 utilise les données de Cosmos avec un analyseur de journal des événements propriétaire pour corréler les données du journal, envoyer des alertes et générer des rapports actionnables sur les éventuelles activités suspectes dans l’environnement de production Microsoft 365. Les rapports de ces données sont utilisés pour corriger les vulnérabilités et améliorer les performances globales du service.

## <a name="how-does-microsoft-365-protect-audit-logs"></a>Comment Microsoft 365 protège-t-il les journaux d’audit ?

Les outils utilisés dans Microsoft 365 pour collecter et traiter des enregistrements d’audit n’autorisent pas les modifications permanentes ou irréversibles du contenu des enregistrements d’audit d’origine ou de l’ordre des heures. L’accès aux données Microsoft 365 stockées dans Cosmos est limité au personnel autorisé. Microsoft 365 limite la gestion de la fonctionnalité d’audit au sous-ensemble limité des membres de l’équipe de service qui sont responsables de la fonctionnalité d’audit. Ces membres de l’équipe n’ont pas la possibilité de modifier ou de supprimer des données de Cosmos, et toutes les modifications apportées aux mécanismes de journalisation pour Cosmos sont enregistrées et auditées. Les journaux d’audit sont conservés suffisamment longtemps pour prendre en charge les recherches d’incidents et répondre aux exigences réglementaires. La période exacte de rétention des données du journal d’audit dans Cosmos est déterminée par les équipes de service ; la plupart des données du journal d’audit sont conservées pendant 90 jours ou plus.

## <a name="how-does-microsoft-365-protect-end-user-identifiable-information-that-may-be-captured-in-audit-logs"></a>Comment Microsoft 365 protège-t-il les informations identifiables de l’utilisateur final pouvant être capturées dans les journaux d’audit ?

Avant de télécharger des données dans Cosmos, l’application ODL utilise un service de nettoyage pour brouiller les champs contenant des données client, tels que les informations client et les informations identifiables de l’utilisateur final, et remplacer ces champs par une valeur de hachage. Les journaux hachés et iranonymes sont réécrits, puis téléchargés dans Cosmos.

## <a name="related-external-regulations--certifications"></a>Certifications & des réglementations externes connexes

Les services en ligne de Microsoft sont régulièrement vérifiés pour la conformité aux réglementations et aux certifications externes. Consultez le tableau suivant pour valider les contrôles liés à l’enregistrement d’audit.

| **Audits externes** | **Section** | **Date du dernier rapport** |
|:--------------------|:------------|:-----------------------|
| [FedRAMP (Office 365)](https://compliance.microsoft.com/compliancemanager) | Au-2 : événements d’audit <br> Au-3 : contenu des enregistrements d’audit <br> Au-4 : capacité de stockage d’audit <br> Au-5 : réponse aux échecs de traitement d’audit <br> Au-6 : analyse, analyse et création de rapports d’audit <br> Au-7 : réduction d’audit et génération de rapports <br> Au-8 : horodatage <br> Au-9 : protection des informations d’audit  <br> Au-10 : non-répudiation <br> Au-11 : auditer la rétention des enregistrements <br> Au-12 : génération d’audit  | 24 septembre 2020 | 
| [ISO 27001/27002 (Office 365)](https://servicetrust.microsoft.com/ViewPage/MSComplianceGuideV3?command=Download&downloadType=Document&downloadId=d7864d4f-e053-4cc4-a964-fa526d07c3be&tab=7027ead0-3d6b-11e9-b9e1-290b1eb4cdeb&docTab=7027ead0-3d6b-11e9-b9e1-290b1eb4cdeb_ISO_Reports) <br><br> [Déclaration de l’applicabilité](https://servicetrust.microsoft.com/ViewPage/MSComplianceGuide?command=Download&downloadType=Document&downloadId=8ee1e46b-2ada-4e7b-bb7d-4c55a8cb6fcd&docTab=4ce99610-c9c0-11e7-8c2c-f908a777fa4d_ISO_Reports) <br> [Certification](https://servicetrust.microsoft.com/ViewPage/MSComplianceGuideV3?command=Download&downloadType=Document&downloadId=1e84a14a-2468-45ac-9412-5e53250d57ec&tab=7027ead0-3d6b-11e9-b9e1-290b1eb4cdeb&docTab=7027ead0-3d6b-11e9-b9e1-290b1eb4cdeb_ISO_Reports) | A. 12.4 : journalisation et surveillance | 22 février 2020 |
| [ISO 27017 (Office 365)](https://servicetrust.microsoft.com/ViewPage/MSComplianceGuideV3?command=Download&downloadType=Document&downloadId=d7864d4f-e053-4cc4-a964-fa526d07c3be&tab=7027ead0-3d6b-11e9-b9e1-290b1eb4cdeb&docTab=7027ead0-3d6b-11e9-b9e1-290b1eb4cdeb_ISO_Reports) <br><br> [Déclaration de l’applicabilité](https://servicetrust.microsoft.com/ViewPage/MSComplianceGuide?command=Download&downloadType=Document&downloadId=8ee1e46b-2ada-4e7b-bb7d-4c55a8cb6fcd&docTab=4ce99610-c9c0-11e7-8c2c-f908a777fa4d_ISO_Reports) <br> [Certification](https://servicetrust.microsoft.com/ViewPage/MSComplianceGuideV3?command=Download&downloadType=Document&downloadId=70de0999-5451-43a3-9ef4-761e8fbfb1a3&tab=7027ead0-3d6b-11e9-b9e1-290b1eb4cdeb&docTab=7027ead0-3d6b-11e9-b9e1-290b1eb4cdeb_ISO_Reports) | A. 12.4 : journalisation et surveillance | 22 février 2020 |
| [SOC 1 (Office 365)](https://servicetrust.microsoft.com/ViewPage/MSComplianceGuideV3?command=Download&downloadType=Document&downloadId=b07c0f7b-6bd5-4544-8255-7a5f14bf914a&tab=7027ead0-3d6b-11e9-b9e1-290b1eb4cdeb&docTab=7027ead0-3d6b-11e9-b9e1-290b1eb4cdeb_SOC_/_SSAE_16_Reports) | CA-48 : journalisation du centre de session <br> CA-60 : journalisation d’audit | 30 septembre 2019 |
| [SOC 2 (Office 365)](https://servicetrust.microsoft.com/ViewPage/MSComplianceGuideV3?command=Download&downloadType=Document&downloadId=fa062990-e758-4ddc-ace3-7fb21a301d09&tab=7027ead0-3d6b-11e9-b9e1-290b1eb4cdeb&docTab=7027ead0-3d6b-11e9-b9e1-290b1eb4cdeb_SOC_/_SSAE_16_Rep-11e9-b9e1-290b1eb4cdeb_SOC_/_SSAE_16_Reports) | CA-48 : journalisation du centre de session <br> CA-60 : journalisation d’audit | 30 septembre 2019 |