---
title: Contrôles d’accès de surveillance et d’audit Microsoft 365
description: 'Résumé : Résumé des différents contrôles d’accès de surveillance et d’audit disponibles dans Microsoft 365.'
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
titleSuffix: Microsoft Service Assurance
ms.openlocfilehash: 3021ce1dd59d5d071edec22286ae9c63833f1277
ms.sourcegitcommit: 21ed42335efd37774ff5d17d9586d5546147241a
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 02/05/2021
ms.locfileid: "50120443"
---
# <a name="monitoring-and-auditing-access-controls-in-microsoft-365"></a>Surveillance et audit des contrôles d’accès dans Microsoft 365

Microsoft effectue une surveillance et un audit étendus de toutes les délégations, privilèges et opérations qui ont lieu dans Microsoft 365. Le contrôle d’accès Microsoft 365 est un processus automatisé qui repose sur le principe des privilèges minimum et incorporant des contrôles et des audits d’accès aux données :

- Tous les accès autorisés sont accessibles à un utilisateur unique. Les administrateurs sont responsables de leur gestion du contenu client.
- Les demandes de contrôle d’accès, les approbations et les journaux des opérations administratives sont capturés pour l’analyse des événements de sécurité et malveillants.
- Les niveaux d’accès sont examinés en temps quasi réel en fonction de l’appartenance à un groupe de sécurité pour s’assurer que seuls les utilisateurs qui ont des justifications professionnelles autorisées et qui répondent aux exigences d’éligibilité ont accès aux systèmes.
- Microsoft 365, ses contrôles d’accès et les services de prise en charge, y compris Azure Active Directory et les centres de données physiques, sont régulièrement audités par des tiers indépendants pour assurer la conformité avec [la norme ISO/IEC 27001,](https://www.microsoft.com/TrustCenter/Compliance/iso-iec-27001) [ISO/IEC 27018,](https://www.microsoft.com/TrustCenter/Compliance/iso-iec-27018) [SOC,](https://www.microsoft.com/TrustCenter/Compliance/SOC) [FedRAMP (Office 365)](https://www.microsoft.com/TrustCenter/Compliance/FedRAMP)et d’autres [normes.](https://www.microsoft.com/TrustCenter/Compliance?service=Office#Icons)
- Les ingénieurs Microsoft 365 doivent suivre une formation sur la sécurité chaque année, examiner les meilleures procédures d’accès élevé et reconnaître les stratégies de sécurité et de confidentialité de Microsoft pour conserver les droits au service.

Les alertes automatisées se déclenchent lorsque des activités suspectes sont détectées, telles que plusieurs connexions qui ont échoué sur une courte période. L’équipe de réponse de sécurité Microsoft 365 utilise l’apprentissage automatique et l’analyse de big data pour examiner et analyser l’activité, rechercher des modèles d’accès non autorisé et répondre de manière proactive aux activités anormales et illicites. Microsoft emploie également une équipe dédiée de testeurs de pénétration et s’engage dans des exercices périodiques d’équipe rouge et d’équipe bleue pour rechercher les problèmes de sécurité et de contrôle d’accès dans le service. Les clients peuvent vérifier l’efficacité des systèmes de contrôle d’accès à l’aide de rapports d’audit et de l’API d’activité de gestion fournie par Microsoft 365.

Pour plus d’informations, voir référence de l’API Activité de gestion [Office 365](/office/office-365-management-api/office-365-management-activity-api-reference) et Audit et rapports [dans Microsoft 365.](assurance-auditing-and-reporting-overview.md)
