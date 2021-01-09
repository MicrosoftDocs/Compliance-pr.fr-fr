---
title: Aperçu sur la gestion des incidents
description: En savoir plus sur la gestion des incidents dans Microsoft 365
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
ms.openlocfilehash: 24ecad99115705f293f765edb84345dad8ff8c93
ms.sourcegitcommit: 7a5b6bc58fc4613b38f3fda20aebee5cec6a5730
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/08/2021
ms.locfileid: "49787313"
---
# <a name="incident-management-overview"></a>Aperçu sur la gestion des incidents

## <a name="what-is-a-security-incident"></a>Qu’est-ce qu’un incident de sécurité ?

Microsoft définit un incident de sécurité dans ses services en ligne comme une violation confirmée de la sécurité donnant lieu à une destruction fortuite ou illégale, à une perte, à une altération, à une divulgation ou à une consultation non autorisée de données client ou de données personnelles lors du traitement par Microsoft. Par exemple, l’accès non autorisé à l’infrastructure Microsoft 365 et l’exfiltration de données client constituent un incident de sécurité, tandis que les événements de conformité qui n’affectent pas la confidentialité, l’intégrité ou la disponibilité des services ou des données client ne sont pas considérés comme des incidents de sécurité.

## <a name="how-does-microsoft-respond-to-security-incidents"></a>Comment Microsoft répond-il aux incidents de sécurité ?

Chaque fois qu’un incident de sécurité se produit, Microsoft s’efforce de répondre rapidement et efficacement afin de protéger les services microsoft et les données client. Microsoft utilise une stratégie de réponse aux incidents conçue pour examiner, contenir et supprimer rapidement et efficacement les menaces de sécurité.

Les services cloud de Microsoft sont surveillés en permanence pour les signes de compromission. Outre la surveillance et l’alerte de sécurité automatisées, tous les employés reçoivent une formation annuelle pour reconnaître et signaler les signes d’incidents de sécurité potentiels. Toute activité suspecte détectée par les employés, les clients ou les outils de surveillance de la sécurité est recalcalée aux équipes de réponse de sécurité spécifiques au service pour examen. Toutes les équipes d’opérations de service, y compris les équipes de réponse à la sécurité spécifiques au service, maintiennent une rotation d’appel approfondie pour s’assurer que les ressources sont disponibles pour la réponse aux incidents 24 x 7 x 365. Nos rotations d’appel permettent à Microsoft de monter une réponse efficace aux incidents à tout moment ou à l’échelle, y compris les événements étendus ou simultanés.

Lorsque des activités suspectes sont détectées et remontées, les équipes de réponse de sécurité spécifiques au service lancent un processus d’analyse, de **containment, d’éradication et de récupération.** Ces équipes coordonnent l’analyse de l’incident potentiel pour déterminer son étendue, y compris tout impact sur les clients ou les données client. Sur la base de cette analyse, les équipes de réponse à la sécurité spécifiques au service travaillent avec les équipes de service ayant un impact pour développer un plan visant à contenir la menace et à minimiser l’impact de l’incident, à éliminer la menace de l’environnement et à récupérer entièrement à un état de sécurité connu. Les équipes de service pertinentes implémentent le plan avec le support des équipes de réponse de sécurité spécifiques au service pour s’assurer que la menace est correctement éliminée et que les services concernés subissent une récupération complète.

Une fois qu’un incident est résolu, les équipes de service implémentent les leçons tirées de l’incident pour mieux prévenir, détecter et répondre à des incidents similaires à l’avenir. Sélectionnez les incidents de sécurité, en particulier ceux qui ont un impact sur le client ou qui entraînent une violation de données, subissent un post-mortem d’incident complet. L’examen post-mortem est conçu pour identifier les insuffisances techniques, les procédures défaillantes, les erreurs manuelles et d’autres défaillances de processus susceptibles de contribuer à l’incident ou précédemment identifiées pendant le processus de réponse aux incidents. Les améliorations identifiées au cours de la post-mortem sont implémentées avec la coordination des équipes de réponse de sécurité spécifiques au service afin d’éviter les incidents futurs et d’améliorer les fonctionnalités de détection et de réponse.

## <a name="how-and-when-are-customers-notified-of-security-or-privacy-incidents"></a>Comment et quand les clients sont-ils avertis des incidents de sécurité ou de confidentialité ?

Chaque fois que Microsoft prend connaissance d’une violation de la sécurité impliquant une perte, une divulgation ou une modification non autorisée de données client, Microsoft informe les clients concernés dans les 72 heures comme indiqué dans la DPA (Data Protection Addendum) des conditions d’utilisation des services en ligne (OST). La chronologie de la notification démarre lorsque l’incident de sécurité est officiellement déclaré. Dès la déclaration d’un incident de sécurité, le processus de notification se produit le plus rapidement possible, sans retard injustifié.

Les notifications incluent une description de la nature de la violation, de l’impact approximatif sur l’utilisateur et des étapes d’atténuation (le cas échéant). Si l’enquête de Microsoft n’est pas terminée au moment de la notification initiale, la notification indiquera également les étapes suivantes et les chronologies pour la communication suivante.

Si un client prend connaissance d’un incident qui pourrait avoir un impact sur Microsoft, y compris, mais sans s’y limiter, une violation de données, le client est responsable d’avertir rapidement Microsoft de l’incident tel que défini dans la DPA.

## <a name="related-external-regulations--certifications"></a>Réglementations externes associées & certifications

Les services en ligne de Microsoft sont régulièrement audités pour assurer la conformité avec les réglementations et certifications externes. Reportez-vous au tableau suivant pour la validation des contrôles liés à la gestion des incidents.

| **Audits externes** | **Section** | **Date de rapport la plus récente** |
|:--------------------|:------------|:-----------------------|
| [FedRAMP (Office 365)](https://compliance.microsoft.com/compliancemanager) | IR-4 : gestion des incidents <br> IR-6 : rapport d’incident <br> IR-8 : plan de réponse aux incidents | 24 septembre 2020 |
| [ISO 27001/27002 (Office 365)](https://servicetrust.microsoft.com/ViewPage/MSComplianceGuideV3?command=Download&downloadType=Document&downloadId=d7864d4f-e053-4cc4-a964-fa526d07c3be&tab=7027ead0-3d6b-11e9-b9e1-290b1eb4cdeb&docTab=7027ead0-3d6b-11e9-b9e1-290b1eb4cdeb_ISO_Reports) <br><br> [Déclaration d’applicabilité](https://servicetrust.microsoft.com/ViewPage/MSComplianceGuide?command=Download&downloadType=Document&downloadId=8ee1e46b-2ada-4e7b-bb7d-4c55a8cb6fcd&docTab=4ce99610-c9c0-11e7-8c2c-f908a777fa4d_ISO_Reports) <br> [Certification](https://servicetrust.microsoft.com/ViewPage/MSComplianceGuideV3?command=Download&downloadType=Document&downloadId=1e84a14a-2468-45ac-9412-5e53250d57ec&tab=7027ead0-3d6b-11e9-b9e1-290b1eb4cdeb&docTab=7027ead0-3d6b-11e9-b9e1-290b1eb4cdeb_ISO_Reports) | A.16.1 : Gestion des améliorations et des incidents de sécurité des informations | 22 février 2020 |
| [ISO 27017 (Office 365)](https://servicetrust.microsoft.com/ViewPage/MSComplianceGuideV3?command=Download&downloadType=Document&downloadId=d7864d4f-e053-4cc4-a964-fa526d07c3be&tab=7027ead0-3d6b-11e9-b9e1-290b1eb4cdeb&docTab=7027ead0-3d6b-11e9-b9e1-290b1eb4cdeb_ISO_Reports) <br><br> [Déclaration d’applicabilité](https://servicetrust.microsoft.com/ViewPage/MSComplianceGuide?command=Download&downloadType=Document&downloadId=8ee1e46b-2ada-4e7b-bb7d-4c55a8cb6fcd&docTab=4ce99610-c9c0-11e7-8c2c-f908a777fa4d_ISO_Reports) <br> [Certification](https://servicetrust.microsoft.com/ViewPage/MSComplianceGuideV3?command=Download&downloadType=Document&downloadId=70de0999-5451-43a3-9ef4-761e8fbfb1a3&tab=7027ead0-3d6b-11e9-b9e1-290b1eb4cdeb&docTab=7027ead0-3d6b-11e9-b9e1-290b1eb4cdeb_ISO_Reports) | A.16.1 : Gestion des améliorations et des incidents de sécurité des informations | 22 février 2020 |
| [ISO 27018 (Office 365)](https://servicetrust.microsoft.com/ViewPage/MSComplianceGuideV3?command=Download&downloadType=Document&downloadId=d7864d4f-e053-4cc4-a964-fa526d07c3be&tab=7027ead0-3d6b-11e9-b9e1-290b1eb4cdeb&docTab=7027ead0-3d6b-11e9-b9e1-290b1eb4cdeb_ISO_Reports) <br><br> [Déclaration d’applicabilité](https://servicetrust.microsoft.com/ViewPage/MSComplianceGuide?command=Download&downloadType=Document&downloadId=8ee1e46b-2ada-4e7b-bb7d-4c55a8cb6fcd&docTab=4ce99610-c9c0-11e7-8c2c-f908a777fa4d_ISO_Reports) <br> [Certification](https://servicetrust.microsoft.com/ViewPage/MSComplianceGuideV3?command=Download&downloadType=Document&downloadId=43e89534-f48d-42ea-a7a7-3523ff516036&tab=7027ead0-3d6b-11e9-b9e1-290b1eb4cdeb&docTab=7027ead0-3d6b-11e9-b9e1-290b1eb4cdeb_ISO_Reports) | A.10.1 : Notification d’une violation de données impliquant des données personnelles  | 22 février 2020 |
| [SOC 1 (Office 365)](https://servicetrust.microsoft.com/ViewPage/MSComplianceGuideV3?command=Download&downloadType=Document&downloadId=90df3f9c-3aaf-4dbf-99d0-ca9f2991721b&tab=7027ead0-3d6b-11e9-b9e1-290b1eb4cdeb&docTab=7027ead0-3d6b-11e9-b9e1-290b1eb4cdeb_SOC_%2F_SSAE_16_Reports) | CA-26 : Rapports d’incident de sécurité <br> CA-47 : Réponse aux incidents | 24 décembre 2020 |
| [SOC 2 (Office 365)](https://servicetrust.microsoft.com/ViewPage/MSComplianceGuideV3?command=Download&downloadType=Document&downloadId=a73c1738-7892-42b7-acd3-87b6371c53f6&tab=7027ead0-3d6b-11e9-b9e1-290b1eb4cdeb&docTab=7027ead0-3d6b-11e9-b9e1-290b1eb4cdeb_SOC_%2F_SSAE_16_Reports) | CA-12 : contrats de niveau de service (SSL) <br> CA-13 : Guides de réponse aux incidents <br> CA-15 : Notifications d’état du service  <br>  <br> CA-26 : Rapports d’incident de sécurité <br> CA-29 : Ingénieurs d’appel <br> CA-47 : Réponse aux incidents | 24 décembre 2020 |
| [SOC 3 (Office 365)](https://servicetrust.microsoft.com/ViewPage/MSComplianceGuideV3?command=Download&downloadType=Document&downloadId=274054e5-4968-48d2-bf94-9a8eda5d7a93&tab=7027ead0-3d6b-11e9-b9e1-290b1eb4cdeb&docTab=7027ead0-3d6b-11e9-b9e1-290b1eb4cdeb_SOC_%2F_SSAE_16_Reports) | CUEC-08 : Signalement des incidents  | 24 décembre 2020  |

## <a name="resources"></a>Ressources

- [Conditions d’utilisation d’Online Services (OTST)](https://www.microsoft.com/licensing/product-licensing/products)
- [Data Protection Addendum (DPA)](https://www.microsoft.com/licensing/product-licensing/products)
- [Conseils d’implémentation de la gestion des incidents microsoft cloud pour Azure et Office 365](https://servicetrust.microsoft.com/ViewPage/TrustDocumentsV3?command=Download&downloadType=Document&downloadId=a8a7cb87-9710-4d09-8748-0835b6754e95&tab=7f51cb60-3d6c-11e9-b2af-7bb9f5d2d913&docTab=7f51cb60-3d6c-11e9-b2af-7bb9f5d2d913_FAQ_and_White_Papers)
- [Office 365 - Évaluation des vulnérabilités tierces d’Office 365 - 2019](https://servicetrust.microsoft.com/ViewPage/TrustDocumentsV3?command=Download&downloadType=Document&downloadId=e85e478f-2491-435d-9c1b-2f0ad7ca8e56&tab=7f51cb60-3d6c-11e9-b2af-7bb9f5d2d913&docTab=7f51cb60-3d6c-11e9-b2af-7bb9f5d2d913_Pen_Test_and_Security_Assessments)
