---
title: Vue d’ensemble de la surveillance de la sécurité
description: En savoir plus sur la surveillance de la sécurité dans Microsoft 365
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
search.appverid:
- MET150
- MOE150
titleSuffix: Microsoft Service Assurance
ms.openlocfilehash: f3eae0aa5ba79372a7ce0d9a34d4dd35fe83a36b
ms.sourcegitcommit: 626b0076d133e588cd28598c149a7f272fc18bae
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 11/30/2020
ms.locfileid: "49507282"
---
# <a name="security-monitoring-overview"></a>Vue d’ensemble de la surveillance de la sécurité

## <a name="what-is-microsofts-strategy-for-monitoring-security"></a>Quelle est la stratégie de Microsoft en matière de surveillance de la sécurité ?

Microsoft 365 est engagé dans la surveillance continue de la sécurité de ses systèmes pour détecter les menaces contre les services Microsoft 365 et y répondre. Nos principes clés en matière de surveillance de la sécurité et d’alerte sont les suivants :

- Robustesse : signaux et logiques pour détecter divers comportements d’attaque
- Précision : alertes significatives pour éviter les distractions du bruit
- Speed : possibilité d’intercepter suffisamment rapidement les attaquants pour les arrêter

L’automatisation, l’évolutivité et les solutions basées sur le cloud constituent les piliers de notre stratégie de surveillance et de réponse. Pour que nous puissions intercepter et arrêter efficacement les attaques au niveau de certains des services principaux Microsoft 365, nos systèmes de surveillance doivent déclencher automatiquement des alertes extrêmement précises en quasi temps réel. De même, lorsqu’un problème est détecté, nous avons besoin de pouvoir réduire le risque à l’horizontale, mais nous ne pouvons pas compter sur notre équipe pour résoudre manuellement les problèmes machine par ordinateur. Pour limiter les risques à grande échelle, nous utilisons des outils basés sur le cloud afin d’appliquer automatiquement des contre-mesures et d’offrir aux ingénieurs des outils qui permettent d’appliquer rapidement des mesures d’atténuation approuvées au sein de l’environnement.

## <a name="how-does-microsoft-365-perform-security-monitoring"></a>Comment Microsoft 365 effectue-t-il la surveillance de la sécurité ?

Microsoft 365 utilise la journalisation centralisée pour collecter et analyser les événements de journal pour les activités susceptibles d’indiquer un incident de sécurité. Les outils de journalisation centralisée regroupent les journaux de tous les composants système, y compris les journaux des événements, les journaux des applications, les journaux de contrôle d’accès et les systèmes de détection d’intrusion basés sur le réseau. Outre la journalisation du serveur et les données au niveau de l’application, l’infrastructure principale de notre service est équipée d’agents de sécurité personnalisés qui génèrent une télémétrie détaillée et fournissent une détection d’intrusion basée sur l’hôte. Nous utilisons cette télémétrie pour la surveillance et l’investigation.

Les données de journalisation et de télémétrie collectées activent les alertes de sécurité 24/7. Notre système d’alertes analyse les données de journal à mesure qu’elles sont chargées, générant des alertes en temps quasi réel. Il s’agit notamment d’alertes basées sur des règles et d’alertes plus sophistiquées basées sur les modèles de machine learning. Nos logiques de surveillance vont au-delà des scénarios d’attaques génériques et intègrent une connaissance approfondie de l’architecture des services et de leurs activités. Nous utilisons les données de surveillance de la sécurité pour améliorer continuellement nos modèles afin de détecter d’autres types d’attaques et d’améliorer la précision de notre surveillance.

## <a name="how-does-microsoft-365-respond-to-security-monitoring-alerts"></a>Comment Microsoft 365 répond-il aux alertes de surveillance de la sécurité ?

Lorsque nous devons effectuer une action en réponse à une alerte ou pour étudier de façon plus approfondie des preuves sur l’ensemble du service, nos outils basés sur le cloud nous permettent de répondre rapidement dans tout l’environnement. Ces outils incluent des agents entièrement automatisés et intelligents qui répondent aux menaces détectées à l’aide de contre-mesures de sécurité. Dans de nombreux cas, ces agents déploient des contre-mesures automatiques afin d’atténuer les détections de sécurité à grande échelle sans intervention humaine. Lorsque ce n’est pas possible, le système de surveillance de la sécurité avertit automatiquement les techniciens concernés qui disposent d’un groupe d’outils qui leur permettent d’agir en temps réel afin d’atténuer les menaces détectées à grande échelle. Les incidents potentiels transmis à l’équipe de réponse de sécurité Microsoft 365 sont résolus à l’aide du processus de réponse aux incidents de sécurité.

## <a name="how-does-microsoft-365-monitor-system-availability"></a>Comment Microsoft 365 surveille-t-il la disponibilité du système ?

Microsoft 365 surveille activement ses systèmes pour des indicateurs d’utilisation excessive des ressources et d’utilisation anormale. La surveillance des ressources est complétée par des redondances de service afin d’éviter les temps morts inattendus et de fournir aux clients un accès fiable aux produits et services. Les problèmes d’État du service sont communiqués rapidement aux clients via le tableau de bord d’État du service (validation).

## <a name="related-external-regulations--certifications"></a>Certifications & des réglementations externes connexes

Les services en ligne de Microsoft sont régulièrement vérifiés pour la conformité aux réglementations et aux certifications externes. Consultez le tableau suivant pour valider les contrôles liés à la surveillance de la sécurité.

| **Audits externes** | **Section** | **Date du dernier rapport** |
|:--------|:--------|:------|
| [FedRAMP (Office 365)](https://compliance.microsoft.com/compliancemanager) | AC-2 : gestion des comptes <br> AC-17 : accès à distance <br> Au-7 : réduction d’audit et génération de rapports <br> SI-4 : analyse du système d’informations <br> SI-7 : logiciels, microprogrammes et intégrité des informations <br> | 24 septembre 2020 |
| [ISO 27001/27002 (Office 365)](https://servicetrust.microsoft.com/ViewPage/MSComplianceGuideV3?command=Download&downloadType=Document&downloadId=d7864d4f-e053-4cc4-a964-fa526d07c3be&tab=7027ead0-3d6b-11e9-b9e1-290b1eb4cdeb&docTab=7027ead0-3d6b-11e9-b9e1-290b1eb4cdeb_ISO_Reports) <br> <br> [Déclaration de l’applicabilité](https://servicetrust.microsoft.com/ViewPage/MSComplianceGuide?command=Download&downloadType=Document&downloadId=8ee1e46b-2ada-4e7b-bb7d-4c55a8cb6fcd&docTab=4ce99610-c9c0-11e7-8c2c-f908a777fa4d_ISO_Reports) <br> [Certification](https://servicetrust.microsoft.com/ViewPage/MSComplianceGuideV3?command=Download&downloadType=Document&downloadId=70de0999-5451-43a3-9ef4-761e8fbfb1a3&tab=7027ead0-3d6b-11e9-b9e1-290b1eb4cdeb&docTab=7027ead0-3d6b-11e9-b9e1-290b1eb4cdeb_ISO_Reports) | A. 12.1.3 : surveillance de la disponibilité et planification de la capacité | 22 février 2020 |
| [ISO 27017 (Office 365)](https://servicetrust.microsoft.com/ViewPage/MSComplianceGuideV3?command=Download&downloadType=Document&downloadId=d7864d4f-e053-4cc4-a964-fa526d07c3be&tab=7027ead0-3d6b-11e9-b9e1-290b1eb4cdeb&docTab=7027ead0-3d6b-11e9-b9e1-290b1eb4cdeb_ISO_Reports) <br><br> [Déclaration de l’applicabilité](https://servicetrust.microsoft.com/ViewPage/MSComplianceGuide?command=Download&downloadType=Document&downloadId=8ee1e46b-2ada-4e7b-bb7d-4c55a8cb6fcd&docTab=4ce99610-c9c0-11e7-8c2c-f908a777fa4d_ISO_Reports) <br> [Certification](https://servicetrust.microsoft.com/ViewPage/MSComplianceGuideV3?command=Download&downloadType=Document&downloadId=70de0999-5451-43a3-9ef4-761e8fbfb1a3&tab=7027ead0-3d6b-11e9-b9e1-290b1eb4cdeb&docTab=7027ead0-3d6b-11e9-b9e1-290b1eb4cdeb_ISO_Reports) | A. 12.1.3 : surveillance de la disponibilité et planification de la capacité <br> A. 16.1 : gestion des améliorations et des incidents de sécurité des informations | 22 février 2020 |
| [SOC 1 (Office 365)](https://servicetrust.microsoft.com/ViewPage/MSComplianceGuideV3?command=Download&downloadType=Document&downloadId=b07c0f7b-6bd5-4544-8255-7a5f14bf914a&tab=7027ead0-3d6b-11e9-b9e1-290b1eb4cdeb&docTab=7027ead0-3d6b-11e9-b9e1-290b1eb4cdeb_SOC_/_SSAE_16_Reports) | CA-19 : analyse des modifications <br> CA-26 : création de rapports d’incident de sécurité <br> CA-29 : ingénieurs sur les appels <br> CA-48 : journalisation du centre de session | 30 septembre 2019 |
| [SOC 2 (Office 365)](https://servicetrust.microsoft.com/ViewPage/MSComplianceGuideV3?command=Download&downloadType=Document&downloadId=fa062990-e758-4ddc-ace3-7fb21a301d09&tab=7027ead0-3d6b-11e9-b9e1-290b1eb4cdeb&docTab=7027ead0-3d6b-11e9-b9e1-290b1eb4cdeb_SOC_/_SSAE_16_Rep-11e9-b9e1-290b1eb4cdeb_SOC_/_SSAE_16_Reports) | CA-19 : analyse des modifications <br> CA-26 : création de rapports d’incident de sécurité <br> CA-29 : ingénieurs sur les appels <br> CA-30 : surveillance de la disponibilité <br> CA-48 : journalisation du centre de session | 30 septembre 2019 |
| [SOC 3 (Office 365)](https://servicetrust.microsoft.com/ViewPage/MSComplianceGuideV3?command=Download&downloadType=Document&downloadId=9df8b99b-96ce-49a9-bff4-268031dcc9a6&tab=7027ead0-3d6b-11e9-b9e1-290b1eb4cdeb&docTab=7027ead0-3d6b-11e9-b9e1-290b1eb4cdeb_SOC_/_SSAE_16_Reports) | CUEC-08 : rapports d’incidents <br> CUEC-10 : contrats de service | 30 septembre 2019 |

## <a name="resources"></a>Ressources

- [Dans les coulisses : sécurisation de l’infrastructure influençant le service Microsoft 365](https://download.microsoft.com/download/c/4/5/c45b197e-f0d9-4f40-bd5f-ed8fc7d0cd8c/M365DCSecurityIntro_Whitepaper.pdf)
