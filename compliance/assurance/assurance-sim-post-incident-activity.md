---
title: 'Gestion des incidents de sécurité Microsoft : activité post-incident'
description: Cet article fournit une vue d’ensemble du processus d’activité post-incident de gestion des incidents de sécurité dans les services en ligne Microsoft.
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
f1.keywords:
- NOCSH
ms.collection:
- Strat_O365_IP
- M365-security-compliance
- MS-Compliance
titleSuffix: Microsoft Service Assurance
hideEdit: true
ms.openlocfilehash: 965c7d6d0d469b9eea981252805bda598c92a4c8
ms.sourcegitcommit: 8bf2602d56eedee4447ddb374ef95b0587f254e7
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 07/12/2021
ms.locfileid: "53377531"
---
# <a name="microsoft-security-incident-management-post-incident-activity"></a><span data-ttu-id="8a9ce-103">Gestion des incidents de sécurité Microsoft : activité post-incident</span><span class="sxs-lookup"><span data-stu-id="8a9ce-103">Microsoft security incident management: Post-incident activity</span></span>

## <a name="postmortem"></a><span data-ttu-id="8a9ce-104">Postmortem</span><span class="sxs-lookup"><span data-stu-id="8a9ce-104">Postmortem</span></span>

<span data-ttu-id="8a9ce-105">Certains incidents de sécurité, en particulier ceux qui ont un impact sur le client ou qui entraînent une violation de données, sont soumis à un post-incident complet.</span><span class="sxs-lookup"><span data-stu-id="8a9ce-105">Some security incidents, especially those incidents that are customer impacting or result in a data breach, are subject to a full incident postmortem.</span></span> <span data-ttu-id="8a9ce-106">L’équipe de réponse à la sécurité effectue un post-mortem détaillé avec toutes les parties impliquées dans la réponse aux incidents de sécurité pour :</span><span class="sxs-lookup"><span data-stu-id="8a9ce-106">The security response team conducts a detailed postmortem with all the parties involved in security incident response to:</span></span>

- <span data-ttu-id="8a9ce-107">Documenter la séquence d’événements à l’origine de l’incident.</span><span class="sxs-lookup"><span data-stu-id="8a9ce-107">Document the sequence of events that caused the incident.</span></span>
- <span data-ttu-id="8a9ce-108">Créez un résumé technique de l’incident tel qu’il est pris en charge par la preuve qui inclut les acteurs impliqués dans la violation (le cas contraire).</span><span class="sxs-lookup"><span data-stu-id="8a9ce-108">Create a technical summary of the incident as supported by the evidence that includes the actors involved in the breach (if known).</span></span> <span data-ttu-id="8a9ce-109">Ce résumé inclut la façon dont la réponse a été exécutée et d’autres éléments à prendre en compte.</span><span class="sxs-lookup"><span data-stu-id="8a9ce-109">This summary will include how the response was executed and other key takeaways.</span></span>
- <span data-ttu-id="8a9ce-110">Identifiez les échecs techniques, les défaillances procédurales, les erreurs manuelles, les failles de processus et les problèmes de communication, et/ou les vecteurs d’attaque précédemment inconnus identifiés lors de la réponse aux incidents de sécurité.</span><span class="sxs-lookup"><span data-stu-id="8a9ce-110">Identify technical lapses, procedural failures, manual errors, process flaws, and communication glitches, and/or any previously unknown attack vectors that were identified during the security incident response.</span></span>

<span data-ttu-id="8a9ce-111">Le post-mortem influence directement l’amélioration du service en ligne de Microsoft, les processus opérationnels et la documentation en fixant de nouvelles priorités dans le cycle de développement d’ingénierie des services en ligne Microsoft.</span><span class="sxs-lookup"><span data-stu-id="8a9ce-111">The postmortem will directly influence Microsoft online service improvement, operational processes, and documentation by setting new priorities in the Microsoft online services engineering development cycle.</span></span>

## <a name="documentation"></a><span data-ttu-id="8a9ce-112">Documentation</span><span class="sxs-lookup"><span data-stu-id="8a9ce-112">Documentation</span></span>

<span data-ttu-id="8a9ce-113">Toutes les principales conclusions techniques du processus post-mortem sont capturées dans un rapport et les investissements ou correctifs de service sous la forme de bogues ou de demandes de modification de développement.</span><span class="sxs-lookup"><span data-stu-id="8a9ce-113">All key technical findings in the postmortem process are captured in a report and service investments or fixes in the form of bugs or development change requests.</span></span> <span data-ttu-id="8a9ce-114">Ces résultats sont suivis des équipes d’ingénierie appropriées.</span><span class="sxs-lookup"><span data-stu-id="8a9ce-114">These findings are followed-up with the appropriate engineering teams.</span></span> <span data-ttu-id="8a9ce-115">En cas d’échec de processus et de problèmes organisationnels, les problèmes sont documentés dans la base de données de l’équipe de réponse à la sécurité et suivis avec les groupes appropriés pour les résoudre.</span><span class="sxs-lookup"><span data-stu-id="8a9ce-115">For process failures and cross-organizational issues, issues are documented in the security response team's database and followed-up with the appropriate groups to address them.</span></span>

## <a name="process-improvement"></a><span data-ttu-id="8a9ce-116">Amélioration des processus</span><span class="sxs-lookup"><span data-stu-id="8a9ce-116">Process improvement</span></span>

<span data-ttu-id="8a9ce-117">La réponse à un incident de sécurité dans les services en ligne Microsoft implique une coordination avec plusieurs groupes répartis dans différentes organisations au sein de Microsoft, et potentiellement même des organisations externes appropriées telles que les forces de l’ordre.</span><span class="sxs-lookup"><span data-stu-id="8a9ce-117">Responding to a security incident in Microsoft online services involves coordination with multiple groups spread across different organizations within Microsoft, and potentially even appropriate external organizations such as law enforcement.</span></span> <span data-ttu-id="8a9ce-118">Nous savons qu’il est essentiel d’évaluer nos réponses après chaque incident de sécurité à la fois pour la sotivité et l’intégralité.</span><span class="sxs-lookup"><span data-stu-id="8a9ce-118">We know that it is critical to evaluate our responses after every security incident for both sufficiency and completeness.</span></span> <span data-ttu-id="8a9ce-119">Pour toutes les améliorations ou modifications identifiées, l’équipe de réponse à la sécurité évalue les suggestions en consultation avec les équipes et les parties prenantes appropriées, et, le cas échéant, les intègre dans les procédures de fonctionnement standard.</span><span class="sxs-lookup"><span data-stu-id="8a9ce-119">For any identified improvements or changes, the security response team evaluates the suggestions in consultation with the appropriate teams and stakeholders, and where appropriate incorporates them into standard operating procedures.</span></span> <span data-ttu-id="8a9ce-120">Toutes les modifications, bogues ou améliorations de service requises identifiés lors de la réponse aux incidents de sécurité ou de l’activité post-mortem sont consignés et suivis dans une base de données interne d’ingénierie Microsoft.</span><span class="sxs-lookup"><span data-stu-id="8a9ce-120">All required changes, bugs, or service improvements identified during the security incident response or postmortem activity are logged and tracked in an internal Microsoft engineering database.</span></span> <span data-ttu-id="8a9ce-121">Tous les bogues ou fonctionnalités potentiels sont affectés au propriétaire approprié.</span><span class="sxs-lookup"><span data-stu-id="8a9ce-121">All potential bugs or features are assigned to the appropriate owner.</span></span> <span data-ttu-id="8a9ce-122">L’équipe de réponse aux problèmes de sécurité de Microsoft examine toutes les entrées jusqu’à ce que le problème soit résolu.</span><span class="sxs-lookup"><span data-stu-id="8a9ce-122">The Microsoft security response team reviews all entries until the issue is resolved.</span></span>

## <a name="related-articles"></a><span data-ttu-id="8a9ce-123">Articles connexes</span><span class="sxs-lookup"><span data-stu-id="8a9ce-123">Related articles</span></span>

- [<span data-ttu-id="8a9ce-124">Gestion des incidents de sécurité Microsoft</span><span class="sxs-lookup"><span data-stu-id="8a9ce-124">Microsoft security incident management</span></span>](assurance-security-incident-management.md)
- [<span data-ttu-id="8a9ce-125">Gestion des incidents de sécurité Microsoft : préparation</span><span class="sxs-lookup"><span data-stu-id="8a9ce-125">Microsoft security incident management: Preparation</span></span>](assurance-sim-preparation.md)
- [<span data-ttu-id="8a9ce-126">Gestion des incidents de sécurité Microsoft : détection et analyse</span><span class="sxs-lookup"><span data-stu-id="8a9ce-126">Microsoft security incident management: Detection and analysis</span></span>](assurance-sim-detection-analysis.md)
- [<span data-ttu-id="8a9ce-127">Gestion des incidents de sécurité Microsoft : containment, éradication et récupération</span><span class="sxs-lookup"><span data-stu-id="8a9ce-127">Microsoft security incident management: Containment, eradication, and recovery</span></span>](assurance-sim-containment-eradication-recovery.md)
- [<span data-ttu-id="8a9ce-128">Comment enregistrer un ticket de support d’événement de sécurité</span><span class="sxs-lookup"><span data-stu-id="8a9ce-128">How to Log a Security Event Support Ticket</span></span>](/azure/security/fundamentals/event-support-ticket)
- [<span data-ttu-id="8a9ce-129">Notification de violation Azure et Dynamics 365 dans le cadre du RGPD</span><span class="sxs-lookup"><span data-stu-id="8a9ce-129">Azure and Dynamics 365 breach notification under the GDPR</span></span>](/compliance/regulatory/gdpr-breach-azure-dynamics)
