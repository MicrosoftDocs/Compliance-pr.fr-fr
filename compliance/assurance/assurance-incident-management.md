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
hideEdit: true
ms.openlocfilehash: bc7021bb7bacf0e4d79228a6a90e6d6f39268305
ms.sourcegitcommit: 48b8ec2dd00e957508e5af82458bf697e1a97ebb
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 07/12/2021
ms.locfileid: "53395594"
---
# <a name="incident-management-overview"></a>Aperçu sur la gestion des incidents

## <a name="what-is-a-security-incident"></a>Qu’est-ce qu’un incident de sécurité ?

Microsoft définit un incident de sécurité dans ses services en ligne comme une violation confirmée de la sécurité donnant lieu à une destruction fortuite ou illégale, à une perte, à une altération, à une divulgation ou à une consultation non autorisée de données client ou de données personnelles lors du traitement par Microsoft. Par exemple, l’accès non autorisé à l’infrastructure des services en ligne de Microsoft et l’exfiltration des données client constituent un incident de sécurité, tandis que les événements de conformité qui n’affectent pas la confidentialité, l’intégrité ou la disponibilité des services ou des données client ne sont pas considérés comme des incidents de sécurité.

## <a name="how-does-microsoft-respond-to-security-incidents"></a>Comment Microsoft répond-il aux incidents de sécurité ?

Chaque fois qu’un incident de sécurité se produit, Microsoft s’efforce de répondre rapidement et efficacement pour protéger services Microsoft données client. Microsoft utilise une stratégie de réponse aux incidents conçue pour examiner, contenir et supprimer rapidement et efficacement les menaces de sécurité.

Les services cloud de Microsoft sont surveillés en permanence pour les signes de compromission. Outre la surveillance et l’alerte de sécurité automatisées, tous les employés reçoivent une formation annuelle pour reconnaître et signaler les signes d’incidents de sécurité potentiels. Toute activité suspecte détectée par les employés, les clients ou les outils de surveillance de la sécurité est recalcalée aux équipes de réponse de sécurité spécifiques au service pour examen. Toutes les équipes d’opérations de service, y compris les équipes de réponse à la sécurité spécifiques au service, maintiennent une rotation d’appel approfondie pour s’assurer que les ressources sont disponibles pour la réponse aux incidents 24 x 7 x 365. Nos rotations d’appel permettent à Microsoft de monter une réponse efficace aux incidents à tout moment ou à l’échelle, y compris les événements étendus ou simultanés.

Lorsque des activités suspectes sont détectées et remontées, les équipes de réponse de sécurité spécifiques au service lancent un processus d’analyse, de **containment, d’éradication et de récupération.** Ces équipes coordonnent l’analyse de l’incident potentiel pour déterminer son étendue, y compris tout impact sur les clients ou les données client. Sur la base de cette analyse, les équipes de réponse à la sécurité spécifiques au service travaillent avec les équipes de service ayant un impact pour développer un plan visant à contenir la menace et à minimiser l’impact de l’incident, à éliminer la menace de l’environnement et à récupérer entièrement à un état de sécurité connu. Les équipes de service pertinentes implémentent le plan avec le support des équipes de réponse de sécurité spécifiques au service pour s’assurer que la menace est correctement éliminée et que les services concernés subissent une récupération complète.

Une fois qu’un incident est résolu, les équipes de service implémentent les leçons tirées de l’incident pour mieux prévenir, détecter et répondre à des incidents similaires à l’avenir. Sélectionnez les incidents de sécurité, en particulier ceux qui ont un impact sur les clients ou qui entraînent une violation de données, subissent un post-mortem d’incident complet. L’examen post-mortem est conçu pour identifier les insuffisances techniques, les procédures défaillantes, les erreurs manuelles et d’autres défaillances de processus susceptibles de contribuer à l’incident ou précédemment identifiées pendant le processus de réponse aux incidents. Les améliorations identifiées au cours de la post-mortem sont implémentées avec la coordination des équipes de réponse de sécurité spécifiques au service afin d’éviter les incidents futurs et d’améliorer les fonctionnalités de détection et de réponse.

## <a name="how-and-when-are-customers-notified-of-security-or-privacy-incidents"></a>Comment et quand les clients sont-ils avertis des incidents de sécurité ou de confidentialité ?

Chaque fois que Microsoft prend connaissance d’une violation de la sécurité impliquant une perte, une divulgation ou une modification non autorisée de données client, Microsoft informe les clients concernés dans les 72 heures, comme indiqué dans la DPA (Data Protection Addendum) des conditions d’utilisation des services en ligne (OST). La chronologie de la notification démarre lorsque l’incident de sécurité est officiellement déclaré. Dès la déclaration d’un incident de sécurité, le processus de notification se produit le plus rapidement possible, sans retard injustifié.

Les notifications incluent une description de la nature de la violation, de l’impact approximatif sur l’utilisateur et des étapes d’atténuation (le cas échéant). Si l’enquête de Microsoft n’est pas terminée au moment de la notification initiale, la notification indiquera également les étapes et les chronologies suivantes pour la communication ultérieure.

Si un client est informé d’un incident qui pourrait avoir un impact sur Microsoft, y compris, mais sans s’y limiter, une violation de données, le client est responsable d’avertir rapidement Microsoft de l’incident tel que défini dans la DPA.

## <a name="related-external-regulations--certifications"></a>Réglementations externes associées & certifications

Les services en ligne de Microsoft sont régulièrement audités pour assurer la conformité avec les réglementations et certifications externes. Reportez-vous au tableau suivant pour la validation des contrôles liés à la gestion des incidents.

### <a name="azure-and-dynamics-365"></a>Azure et Dynamics 365

| **Audits externes** | **Section** | **Date de rapport la plus récente** |
|:--------------------|:------------|:-----------------------|
| [ISO 27001/27002](https://servicetrust.microsoft.com/ViewPage/MSComplianceGuideV3?command=Download&downloadType=Document&downloadId=e9116047-f327-430c-a83f-166b7e561ad6&tab=7027ead0-3d6b-11e9-b9e1-290b1eb4cdeb&docTab=7027ead0-3d6b-11e9-b9e1-290b1eb4cdeb_ISO_Reports) <br><br> [Déclaration d’applicabilité](https://servicetrust.microsoft.com/ViewPage/MSComplianceGuideV3?command=Download&downloadType=Document&downloadId=00af6c3e-7f3e-4e0d-8b0e-79f45ef2cef1&tab=7027ead0-3d6b-11e9-b9e1-290b1eb4cdeb&docTab=7027ead0-3d6b-11e9-b9e1-290b1eb4cdeb_ISO_Reports) <br> [Certification](https://servicetrust.microsoft.com/ViewPage/MSComplianceGuideV3?command=Download&downloadType=Document&downloadId=d7af5304-3a31-40e6-9abb-e26352305d41&tab=7027ead0-3d6b-11e9-b9e1-290b1eb4cdeb&docTab=7027ead0-3d6b-11e9-b9e1-290b1eb4cdeb_ISO_Reports) | A.16.1 : Gestion des améliorations et des incidents de sécurité des informations | 2 décembre 2021 |
| [ISO 27017](https://servicetrust.microsoft.com/ViewPage/MSComplianceGuideV3?command=Download&downloadType=Document&downloadId=e9116047-f327-430c-a83f-166b7e561ad6&tab=7027ead0-3d6b-11e9-b9e1-290b1eb4cdeb&docTab=7027ead0-3d6b-11e9-b9e1-290b1eb4cdeb_ISO_Reports) <br><br> [Déclaration d’applicabilité](https://servicetrust.microsoft.com/ViewPage/MSComplianceGuideV3?command=Download&downloadType=Document&downloadId=a3bca0ac-867d-4204-b66b-13665f5f1e8d&tab=7027ead0-3d6b-11e9-b9e1-290b1eb4cdeb&docTab=7027ead0-3d6b-11e9-b9e1-290b1eb4cdeb_ISO_Reports) <br> [Certification](https://servicetrust.microsoft.com/ViewPage/MSComplianceGuideV3?command=Download&downloadType=Document&downloadId=25718a8a-f34d-41e1-a95a-c49246508787&tab=7027ead0-3d6b-11e9-b9e1-290b1eb4cdeb&docTab=7027ead0-3d6b-11e9-b9e1-290b1eb4cdeb_ISO_Reports) | A.16.1 : Gestion des améliorations et des incidents de sécurité des informations | 2 décembre 2021 |
| [ISO 27018](https://servicetrust.microsoft.com/ViewPage/MSComplianceGuideV3?command=Download&downloadType=Document&downloadId=e9116047-f327-430c-a83f-166b7e561ad6&tab=7027ead0-3d6b-11e9-b9e1-290b1eb4cdeb&docTab=7027ead0-3d6b-11e9-b9e1-290b1eb4cdeb_ISO_Reports) <br><br> [Déclaration d’applicabilité](https://servicetrust.microsoft.com/ViewPage/MSComplianceGuideV3?command=Download&downloadType=Document&downloadId=00af6c3e-7f3e-4e0d-8b0e-79f45ef2cef1&tab=7027ead0-3d6b-11e9-b9e1-290b1eb4cdeb&docTab=7027ead0-3d6b-11e9-b9e1-290b1eb4cdeb_ISO_Reports) <br> [Certification](https://servicetrust.microsoft.com/ViewPage/MSComplianceGuideV3?command=Download&downloadType=Document&downloadId=56904fc3-0942-4ff5-9eef-7cabc751a25c&tab=7027ead0-3d6b-11e9-b9e1-290b1eb4cdeb&docTab=7027ead0-3d6b-11e9-b9e1-290b1eb4cdeb_ISO_Reports) | A.9.1 : Notification d’une violation de données impliquant des données personnelles  | 2 décembre 2021 |
| [SOC 1](https://servicetrust.microsoft.com/ViewPage/MSComplianceGuideV3?command=Download&downloadType=Document&downloadId=b8721ebd-af20-42fe-b22f-8332b0a19517&tab=7027ead0-3d6b-11e9-b9e1-290b1eb4cdeb&docTab=7027ead0-3d6b-11e9-b9e1-290b1eb4cdeb_SOC_%2F_SSAE_16_Reports) | IM-1 : infrastructure de gestion des incidents <br> IM-2 : Mécanismes de détection et alertes <br> IM-3 : exécution de la réponse aux incidents <br> IM-4 : post-mortems d’incident <br> IM-6 : test de réponse aux incidents <br> OA-7 : accès de l’ingénieur d’appel | 31 mars 2021 |
| [SOC 2](https://servicetrust.microsoft.com/ViewPage/MSComplianceGuideV3?command=Download&downloadType=Document&downloadId=234a0f57-83c1-4afc-a586-a0e7a59592f7&tab=7027ead0-3d6b-11e9-b9e1-290b1eb4cdeb&docTab=7027ead0-3d6b-11e9-b9e1-290b1eb4cdeb_SOC_%2F_SSAE_16_Reports) <br> [SOC 3](https://servicetrust.microsoft.com/ViewPage/MSComplianceGuideV3?command=Download&downloadType=Document&downloadId=75c8cbf6-e456-473c-a05e-34fea888ec2a&tab=7027ead0-3d6b-11e9-b9e1-290b1eb4cdeb&docTab=7027ead0-3d6b-11e9-b9e1-290b1eb4cdeb_SOC_%2F_SSAE_16_Reports) | CCM-9 : Procédures d’investigation <br> CUEC : signalement des incidents <br> IM-1 : infrastructure de gestion des incidents <br> IM-2 : Mécanismes de détection et alertes <br> IM-3 : exécution de la réponse aux incidents <br> IM-4 : post-mortems d’incident <br> IM-6 : test de réponse aux incidents <br> OA-7 : accès de l’ingénieur d’appel <br> SOC2-6 : site web du support technique <br> SOC2-9 : Tableaux de bord de service | 31 mars 2021 |

### <a name="office-365"></a>Office 365

| **Audits externes** | **Section** | **Date de rapport la plus récente** |
|:--------------------|:------------|:-----------------------|
| [FedRAMP](https://compliance.microsoft.com/compliancemanager) | IR-4 : gestion des incidents <br> IR-6 : rapport d’incident <br> IR-8 : plan de réponse aux incidents | 24 septembre 2020 |
| [ISO 27001/27002/27017](https://servicetrust.microsoft.com/ViewPage/MSComplianceGuideV3?command=Download&downloadType=Document&downloadId=8d625374-4f2d-49f8-9d37-a4281ba98222&tab=7027ead0-3d6b-11e9-b9e1-290b1eb4cdeb&docTab=7027ead0-3d6b-11e9-b9e1-290b1eb4cdeb_ISO_Reports) <br><br> [Déclaration d’applicabilité](https://servicetrust.microsoft.com/ViewPage/MSComplianceGuideV3?command=Download&downloadType=Document&downloadId=c0df4ce8-c77e-4183-84eb-c8688470d8b1&tab=7027ead0-3d6b-11e9-b9e1-290b1eb4cdeb&docTab=7027ead0-3d6b-11e9-b9e1-290b1eb4cdeb_ISO_Reports) | A.16.1 : Gestion des améliorations et des incidents de sécurité des informations | 20 avril 2021 |
| [ISO 27018](https://servicetrust.microsoft.com/ViewPage/MSComplianceGuideV3?command=Download&downloadType=Document&downloadId=8d625374-4f2d-49f8-9d37-a4281ba98222&tab=7027ead0-3d6b-11e9-b9e1-290b1eb4cdeb&docTab=7027ead0-3d6b-11e9-b9e1-290b1eb4cdeb_ISO_Reports) <br><br> [Déclaration d’applicabilité](https://servicetrust.microsoft.com/ViewPage/MSComplianceGuideV3?command=Download&downloadType=Document&downloadId=c0df4ce8-c77e-4183-84eb-c8688470d8b1&tab=7027ead0-3d6b-11e9-b9e1-290b1eb4cdeb&docTab=7027ead0-3d6b-11e9-b9e1-290b1eb4cdeb_ISO_Reports) | A.9.1 : Notification d’une violation de données impliquant des données personnelles  | 20 avril 2021 |
| [SOC 1](https://servicetrust.microsoft.com/ViewPage/MSComplianceGuideV3?command=Download&downloadType=Document&downloadId=90df3f9c-3aaf-4dbf-99d0-ca9f2991721b&tab=7027ead0-3d6b-11e9-b9e1-290b1eb4cdeb&docTab=7027ead0-3d6b-11e9-b9e1-290b1eb4cdeb_SOC_%2F_SSAE_16_Reports) | CA-26 : Rapports d’incident de sécurité <br> CA-47 : Réponse aux incidents | 24 décembre 2020 |
| [SOC 2](https://servicetrust.microsoft.com/ViewPage/MSComplianceGuideV3?command=Download&downloadType=Document&downloadId=a73c1738-7892-42b7-acd3-87b6371c53f6&tab=7027ead0-3d6b-11e9-b9e1-290b1eb4cdeb&docTab=7027ead0-3d6b-11e9-b9e1-290b1eb4cdeb_SOC_%2F_SSAE_16_Reports) | CA-12 : contrats de niveau de service (SSL) <br> CA-13 : Guides de réponse aux incidents <br> CA-15 : Notifications d’état du service  <br>  <br> CA-26 : Rapports d’incident de sécurité <br> CA-29 : ingénieurs en appel <br> CA-47 : Réponse aux incidents | 24 décembre 2020 |
| [SOC 3](https://servicetrust.microsoft.com/ViewPage/MSComplianceGuideV3?command=Download&downloadType=Document&downloadId=274054e5-4968-48d2-bf94-9a8eda5d7a93&tab=7027ead0-3d6b-11e9-b9e1-290b1eb4cdeb&docTab=7027ead0-3d6b-11e9-b9e1-290b1eb4cdeb_SOC_%2F_SSAE_16_Reports) | CUEC-08 : Signalement des incidents  | 24 décembre 2020  |

## <a name="resources"></a>Ressources

- [Conditions d’utilisation d’Online Services (OTST)](https://www.microsoft.com/licensing/product-licensing/products)
- [Data Protection Addendum (DPA)](https://www.microsoft.com/licensing/product-licensing/products)
- [Conseils de mise en œuvre de la gestion des incidents Microsoft Cloud pour Azure et Office 365](https://servicetrust.microsoft.com/ViewPage/TrustDocumentsV3?command=Download&downloadType=Document&downloadId=a8a7cb87-9710-4d09-8748-0835b6754e95&tab=7f51cb60-3d6c-11e9-b2af-7bb9f5d2d913&docTab=7f51cb60-3d6c-11e9-b2af-7bb9f5d2d913_FAQ_and_White_Papers)
- [Office 365 - Évaluation des vulnérabilités tierces de Office 365 - 2019](https://servicetrust.microsoft.com/ViewPage/TrustDocumentsV3?command=Download&downloadType=Document&downloadId=e85e478f-2491-435d-9c1b-2f0ad7ca8e56&tab=7f51cb60-3d6c-11e9-b2af-7bb9f5d2d913&docTab=7f51cb60-3d6c-11e9-b2af-7bb9f5d2d913_Pen_Test_and_Security_Assessments)
