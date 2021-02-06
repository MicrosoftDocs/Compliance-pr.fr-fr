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
# <a name="monitoring-and-auditing-access-controls-in-microsoft-365"></a><span data-ttu-id="853ac-103">Surveillance et audit des contrôles d’accès dans Microsoft 365</span><span class="sxs-lookup"><span data-stu-id="853ac-103">Monitoring and auditing access controls in Microsoft 365</span></span>

<span data-ttu-id="853ac-104">Microsoft effectue une surveillance et un audit étendus de toutes les délégations, privilèges et opérations qui ont lieu dans Microsoft 365.</span><span class="sxs-lookup"><span data-stu-id="853ac-104">Microsoft performs extensive monitoring and auditing of all delegation, privileges, and operations that occur within Microsoft 365.</span></span> <span data-ttu-id="853ac-105">Le contrôle d’accès Microsoft 365 est un processus automatisé qui repose sur le principe des privilèges minimum et incorporant des contrôles et des audits d’accès aux données :</span><span class="sxs-lookup"><span data-stu-id="853ac-105">Microsoft 365 access control is an automated process built on the principle of least privilege and incorporating data access controls and audits:</span></span>

- <span data-ttu-id="853ac-106">Tous les accès autorisés sont accessibles à un utilisateur unique.</span><span class="sxs-lookup"><span data-stu-id="853ac-106">All permitted access is traceable to a unique user.</span></span> <span data-ttu-id="853ac-107">Les administrateurs sont responsables de leur gestion du contenu client.</span><span class="sxs-lookup"><span data-stu-id="853ac-107">Administrators are accountable for their handling of customer content.</span></span>
- <span data-ttu-id="853ac-108">Les demandes de contrôle d’accès, les approbations et les journaux des opérations administratives sont capturés pour l’analyse des événements de sécurité et malveillants.</span><span class="sxs-lookup"><span data-stu-id="853ac-108">Access control requests, approvals, and administrative operations logs are captured for analysis of security and malicious events.</span></span>
- <span data-ttu-id="853ac-109">Les niveaux d’accès sont examinés en temps quasi réel en fonction de l’appartenance à un groupe de sécurité pour s’assurer que seuls les utilisateurs qui ont des justifications professionnelles autorisées et qui répondent aux exigences d’éligibilité ont accès aux systèmes.</span><span class="sxs-lookup"><span data-stu-id="853ac-109">Access levels are reviewed in near real-time based on security group membership to ensure that only users who have authorized business justifications and meet the eligibility requirements have access to the systems.</span></span>
- <span data-ttu-id="853ac-110">Microsoft 365, ses contrôles d’accès et les services de prise en charge, y compris Azure Active Directory et les centres de données physiques, sont régulièrement audités par des tiers indépendants pour assurer la conformité avec [la norme ISO/IEC 27001,](https://www.microsoft.com/TrustCenter/Compliance/iso-iec-27001) [ISO/IEC 27018,](https://www.microsoft.com/TrustCenter/Compliance/iso-iec-27018) [SOC,](https://www.microsoft.com/TrustCenter/Compliance/SOC) [FedRAMP (Office 365)](https://www.microsoft.com/TrustCenter/Compliance/FedRAMP)et d’autres [normes.](https://www.microsoft.com/TrustCenter/Compliance?service=Office#Icons)</span><span class="sxs-lookup"><span data-stu-id="853ac-110">Microsoft 365, its access controls, and supporting services, including Azure Active Directory and physical datacenters, are regularly audited by independent third-parties for compliance with [ISO/IEC 27001](https://www.microsoft.com/TrustCenter/Compliance/iso-iec-27001), [ISO/IEC 27018](https://www.microsoft.com/TrustCenter/Compliance/iso-iec-27018), [SOC](https://www.microsoft.com/TrustCenter/Compliance/SOC), [FedRAMP (Office 365)](https://www.microsoft.com/TrustCenter/Compliance/FedRAMP), and other [standards](https://www.microsoft.com/TrustCenter/Compliance?service=Office#Icons).</span></span>
- <span data-ttu-id="853ac-111">Les ingénieurs Microsoft 365 doivent suivre une formation sur la sécurité chaque année, examiner les meilleures procédures d’accès élevé et reconnaître les stratégies de sécurité et de confidentialité de Microsoft pour conserver les droits au service.</span><span class="sxs-lookup"><span data-stu-id="853ac-111">Microsoft 365 engineers must take yearly security training, review elevated access best procedures, and acknowledge Microsoft's security and privacy policies to maintain entitlements to the service.</span></span>

<span data-ttu-id="853ac-112">Les alertes automatisées se déclenchent lorsque des activités suspectes sont détectées, telles que plusieurs connexions qui ont échoué sur une courte période.</span><span class="sxs-lookup"><span data-stu-id="853ac-112">Automated alerts trigger when suspicious activity is detected, such as multiple failed logins within a short period.</span></span> <span data-ttu-id="853ac-113">L’équipe de réponse de sécurité Microsoft 365 utilise l’apprentissage automatique et l’analyse de big data pour examiner et analyser l’activité, rechercher des modèles d’accès non autorisé et répondre de manière proactive aux activités anormales et illicites.</span><span class="sxs-lookup"><span data-stu-id="853ac-113">The Microsoft 365 Security Response team uses machine learning and big data analysis to review and analyze activity, look for irregular access patterns, and proactively respond to anomalous and illicit activities.</span></span> <span data-ttu-id="853ac-114">Microsoft emploie également une équipe dédiée de testeurs de pénétration et s’engage dans des exercices périodiques d’équipe rouge et d’équipe bleue pour rechercher les problèmes de sécurité et de contrôle d’accès dans le service.</span><span class="sxs-lookup"><span data-stu-id="853ac-114">Microsoft also employs a dedicated team of penetration testers and engages in periodic Red Team and Blue Team exercises to find security and access control issues in the service.</span></span> <span data-ttu-id="853ac-115">Les clients peuvent vérifier l’efficacité des systèmes de contrôle d’accès à l’aide de rapports d’audit et de l’API d’activité de gestion fournie par Microsoft 365.</span><span class="sxs-lookup"><span data-stu-id="853ac-115">Customers can verify the effectiveness of access control systems by using audit reports and the management activity API provided by Microsoft 365.</span></span>

<span data-ttu-id="853ac-116">Pour plus d’informations, voir référence de l’API Activité de gestion [Office 365](/office/office-365-management-api/office-365-management-activity-api-reference) et Audit et rapports [dans Microsoft 365.](assurance-auditing-and-reporting-overview.md)</span><span class="sxs-lookup"><span data-stu-id="853ac-116">For more information, see [Office 365 Management Activity API reference](/office/office-365-management-api/office-365-management-activity-api-reference) and [Auditing and reporting in Microsoft 365](assurance-auditing-and-reporting-overview.md).</span></span>
