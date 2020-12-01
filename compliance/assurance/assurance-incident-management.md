---
title: Présentation de la gestion des incidents
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
ms.openlocfilehash: 6b5c77a2a81f8231ad620fbc40205457c6ba1a49
ms.sourcegitcommit: 626b0076d133e588cd28598c149a7f272fc18bae
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 11/30/2020
ms.locfileid: "49506728"
---
# <a name="incident-management-overview"></a>Présentation de la gestion des incidents

## <a name="what-is-a-security-incident"></a>Qu’est-ce qu’un incident de sécurité ?

Microsoft définit un incident de sécurité dans ses services en ligne comme une violation confirmée de la sécurité donnant lieu à une destruction fortuite ou illégale, à une perte, à une altération, à une divulgation ou à une consultation non autorisée de données client ou de données personnelles lors du traitement par Microsoft. Par exemple, un accès non autorisé à l’infrastructure Microsoft 365 et l’exfiltration des données client constitueront un incident de sécurité, tandis que les événements de conformité qui n’ont pas d’incidence sur la confidentialité, l’intégrité ou la disponibilité des services ou des données client ne sont pas considérés comme des incidents de sécurité.

## <a name="how-does-microsoft-respond-to-security-incidents"></a>Comment Microsoft répond-t-il aux incidents de sécurité ?

Chaque fois qu’il existe un incident de sécurité, Microsoft s’efforce de répondre rapidement et efficacement à la protection des services Microsoft et des données client. Microsoft a recours à une stratégie de réponse aux incidents conçue pour examiner, contenir et supprimer les menaces de sécurité rapidement et efficacement.

Les services de Cloud Computing Microsoft sont surveillés en permanence pour les signes de compromission. En plus de l’analyse automatisée de la sécurité et des alertes, tous les employés reçoivent une formation annuelle pour reconnaître et signaler les signes d’incidents de sécurité potentiels. Toutes les activités suspectes détectées par les employés, les clients ou les outils de surveillance de la sécurité sont transmises aux équipes de réponse de sécurité spécifiques aux services pour enquête. Toutes les équipes d’opérations de service, y compris les équipes de réponse de sécurité spécifiques, conservent une rotation de longue expérience pour s’assurer que les ressources sont disponibles pour les services de réponse aux incidents. Nos rotations d’appels en fonction permettent à Microsoft de monter une réponse efficace aux incidents à tout moment ou à une échelle, y compris des événements répandus ou simultanés.

Lorsqu’une activité suspecte est détectée et escaladée, des équipes de réponse spécifiques aux services lancent un processus d' **analyse, de contention, d’éradication et de récupération**. Ces équipes coordonnent l’analyse de l’incident potentiel afin de déterminer son étendue, y compris toute incidence sur les clients ou les données client. En fonction de cette analyse, les équipes de sécurité spécifiques aux services travaillent avec des équipes de service affectées afin de développer un plan pour contenir la menace et de réduire l’impact de l’incident, d’éradiquer la menace de l’environnement et de récupérer entièrement à un état sécurisé connu. Les équipes de service pertinentes implémentent le plan avec prise en charge des équipes de réponse de sécurité spécifiques pour s’assurer que la menace est correctement éliminée et que les services concernés subissent une récupération complète.

Une fois qu’un incident est résolu, les équipes de service implémentent les leçons apprises à partir de l’incident afin de mieux prévenir, détecter et répondre aux incidents similaires à l’avenir. Sélectionnez incidents de sécurité, notamment ceux qui ont un impact sur le client ou qui entraînent une violation de données, sont soumis à un événement complet. L’examen post-mortem est conçu pour identifier les insuffisances techniques, les procédures défaillantes, les erreurs manuelles et d’autres défaillances de processus susceptibles de contribuer à l’incident ou précédemment identifiées pendant le processus de réponse aux incidents. Les améliorations identifiées au cours de l’autopsie sont mises en œuvre avec une coordination des équipes de sécurité spécifiques aux services afin de prévenir les incidents futurs et d’améliorer les capacités de détection et de réponse.

## <a name="how-and-when-are-customers-notified-of-security-or-privacy-incidents"></a>Comment et quand les clients sont-ils avertis des incidents de sécurité ou de confidentialité ?

Chaque fois que Microsoft détecte une violation de sécurité impliquant une perte, une divulgation ou une modification non autorisée des données client, Microsoft avertit les clients concernés dans un délai de 72 heures, comme indiqué dans le DPA (Data Protection addendum) des services en ligne (OST). La chronologie de la notification démarre lorsque l’incident de sécurité est officiellement déclaré. Dès la déclaration d’un incident de sécurité, le processus de notification se produit le plus rapidement possible, sans retard injustifié.

Les notifications incluent une description de la nature de la violation, un impact approximatif de l’utilisateur et des étapes d’atténuation (le cas échéant). Si l’enquête de Microsoft n’est pas terminée au moment de la notification initiale, la notification indiquera également les étapes et les chronologies suivantes pour la communication ultérieure.

Si un client connaît un incident susceptible d’avoir un impact sur Microsoft, y compris mais sans s’y limiter, le client est responsable de la notification rapide à Microsoft de l’incident, tel qu’il est défini dans DPA.

## <a name="related-external-regulations--certifications"></a>Certifications & des réglementations externes connexes

Les services en ligne de Microsoft sont régulièrement vérifiés pour la conformité aux réglementations et aux certifications externes. Reportez-vous au tableau suivant pour la validation des contrôles liés à la gestion des incidents.

| **Audits externes** | **Section** | **Date du dernier rapport** |
|:--------------------|:------------|:-----------------------|
| [FedRAMP (Office 365)](https://compliance.microsoft.com/compliancemanager) | IR-4 : traitement des incidents <br> IR-6 : signalisation des incidents <br> IR-8 : plan de réponse aux incidents | 24 septembre 2020 |
| [ISO 27001/27002 (Office 365)](https://servicetrust.microsoft.com/ViewPage/MSComplianceGuideV3?command=Download&downloadType=Document&downloadId=d7864d4f-e053-4cc4-a964-fa526d07c3be&tab=7027ead0-3d6b-11e9-b9e1-290b1eb4cdeb&docTab=7027ead0-3d6b-11e9-b9e1-290b1eb4cdeb_ISO_Reports) <br><br> [Déclaration de l’applicabilité](https://servicetrust.microsoft.com/ViewPage/MSComplianceGuide?command=Download&downloadType=Document&downloadId=8ee1e46b-2ada-4e7b-bb7d-4c55a8cb6fcd&docTab=4ce99610-c9c0-11e7-8c2c-f908a777fa4d_ISO_Reports) <br> [Certification](https://servicetrust.microsoft.com/ViewPage/MSComplianceGuideV3?command=Download&downloadType=Document&downloadId=1e84a14a-2468-45ac-9412-5e53250d57ec&tab=7027ead0-3d6b-11e9-b9e1-290b1eb4cdeb&docTab=7027ead0-3d6b-11e9-b9e1-290b1eb4cdeb_ISO_Reports) | A. 16.1 : gestion des améliorations et des incidents de sécurité des informations | 22 février 2020 |
| [ISO 27017 (Office 365)](https://servicetrust.microsoft.com/ViewPage/MSComplianceGuideV3?command=Download&downloadType=Document&downloadId=d7864d4f-e053-4cc4-a964-fa526d07c3be&tab=7027ead0-3d6b-11e9-b9e1-290b1eb4cdeb&docTab=7027ead0-3d6b-11e9-b9e1-290b1eb4cdeb_ISO_Reports) <br><br> [Déclaration de l’applicabilité](https://servicetrust.microsoft.com/ViewPage/MSComplianceGuide?command=Download&downloadType=Document&downloadId=8ee1e46b-2ada-4e7b-bb7d-4c55a8cb6fcd&docTab=4ce99610-c9c0-11e7-8c2c-f908a777fa4d_ISO_Reports) <br> [Certification](https://servicetrust.microsoft.com/ViewPage/MSComplianceGuideV3?command=Download&downloadType=Document&downloadId=70de0999-5451-43a3-9ef4-761e8fbfb1a3&tab=7027ead0-3d6b-11e9-b9e1-290b1eb4cdeb&docTab=7027ead0-3d6b-11e9-b9e1-290b1eb4cdeb_ISO_Reports) | A. 16.1 : gestion des améliorations et des incidents de sécurité des informations | 22 février 2020 |
| [ISO 27018 (Office 365)](https://servicetrust.microsoft.com/ViewPage/MSComplianceGuideV3?command=Download&downloadType=Document&downloadId=d7864d4f-e053-4cc4-a964-fa526d07c3be&tab=7027ead0-3d6b-11e9-b9e1-290b1eb4cdeb&docTab=7027ead0-3d6b-11e9-b9e1-290b1eb4cdeb_ISO_Reports) <br><br> [Déclaration de l’applicabilité](https://servicetrust.microsoft.com/ViewPage/MSComplianceGuide?command=Download&downloadType=Document&downloadId=8ee1e46b-2ada-4e7b-bb7d-4c55a8cb6fcd&docTab=4ce99610-c9c0-11e7-8c2c-f908a777fa4d_ISO_Reports) <br> [Certification](https://servicetrust.microsoft.com/ViewPage/MSComplianceGuideV3?command=Download&downloadType=Document&downloadId=43e89534-f48d-42ea-a7a7-3523ff516036&tab=7027ead0-3d6b-11e9-b9e1-290b1eb4cdeb&docTab=7027ead0-3d6b-11e9-b9e1-290b1eb4cdeb_ISO_Reports) | A. 10.1 : notification d’une violation de données impliquant des données personnelles  | 22 février 2020 |
| [SOC 1 (Office 365)](https://servicetrust.microsoft.com/ViewPage/MSComplianceGuideV3?command=Download&downloadType=Document&downloadId=b07c0f7b-6bd5-4544-8255-7a5f14bf914a&tab=7027ead0-3d6b-11e9-b9e1-290b1eb4cdeb&docTab=7027ead0-3d6b-11e9-b9e1-290b1eb4cdeb_SOC_/_SSAE_16_Reports) | CA-26 : création de rapports d’incident de sécurité <br> CA-47 : réponse aux incidents | 30 septembre 2019 |
| [SOC 2 (Office 365)](https://servicetrust.microsoft.com/ViewPage/MSComplianceGuideV3?command=Download&downloadType=Document&downloadId=fa062990-e758-4ddc-ace3-7fb21a301d09&tab=7027ead0-3d6b-11e9-b9e1-290b1eb4cdeb&docTab=7027ead0-3d6b-11e9-b9e1-290b1eb4cdeb_SOC_/_SSAE_16_Rep-11e9-b9e1-290b1eb4cdeb_SOC_/_SSAE_16_Reports) | CA-12 : contrats de niveau de service (SLA) <br> CA-13 : guides de réponse aux incidents <br> CA-15 : notifications d’intégrité de service  <br>  <br> CA-26 : création de rapports d’incident de sécurité <br> CA-29 : ingénieurs sur les appels <br> CA-47 : réponse aux incidents | 30 septembre 2019 |
| [SOC 3 (Office 365)](https://servicetrust.microsoft.com/ViewPage/MSComplianceGuideV3?command=Download&downloadType=Document&downloadId=9df8b99b-96ce-49a9-bff4-268031dcc9a6&tab=7027ead0-3d6b-11e9-b9e1-290b1eb4cdeb&docTab=7027ead0-3d6b-11e9-b9e1-290b1eb4cdeb_SOC_/_SSAE_16_Reports) | CUEC-08 : rapports d’incidents  | 30 septembre 2019  |

## <a name="resources"></a>Ressources

- [Conditions d’utilisation d’Online Services (OTST)](https://www.microsoft.com/licensing/product-licensing/products)
- [Addendum sur la protection des données (DPA)](https://www.microsoft.com/licensing/product-licensing/products)
- [Guide de mise en œuvre de la gestion des incidents dans le Cloud Microsoft pour Azure et Office 365](https://servicetrust.microsoft.com/ViewPage/TrustDocumentsV3?command=Download&downloadType=Document&downloadId=a8a7cb87-9710-4d09-8748-0835b6754e95&tab=7f51cb60-3d6c-11e9-b2af-7bb9f5d2d913&docTab=7f51cb60-3d6c-11e9-b2af-7bb9f5d2d913_FAQ_and_White_Papers)
- [Office 365-évaluation des vulnérabilités tierces d’Office 365-2019](https://servicetrust.microsoft.com/ViewPage/TrustDocumentsV3?command=Download&downloadType=Document&downloadId=e85e478f-2491-435d-9c1b-2f0ad7ca8e56&tab=7f51cb60-3d6c-11e9-b2af-7bb9f5d2d913&docTab=7f51cb60-3d6c-11e9-b2af-7bb9f5d2d913_Pen_Test_and_Security_Assessments)
