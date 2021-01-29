---
title: 'Gestion des incidents de sécurité Microsoft 365 : activité post-incident'
description: Cet article fournit une vue d’ensemble du processus d’activité post-incident de gestion des incidents de sécurité dans Microsoft 365.
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
ms.openlocfilehash: 66c25503ac574de512f5201981112a0e54714968
ms.sourcegitcommit: 2973d25e9e0185b84d281f963553a332eac1c1a3
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/28/2021
ms.locfileid: "50040347"
---
# <a name="microsoft-365-security-incident-management-post-incident-activity"></a><span data-ttu-id="7968b-103">Gestion des incidents de sécurité Microsoft 365 : activité post-incident</span><span class="sxs-lookup"><span data-stu-id="7968b-103">Microsoft 365 security incident management: Post-incident activity</span></span>

## <a name="postmortem"></a><span data-ttu-id="7968b-104">Postmortem</span><span class="sxs-lookup"><span data-stu-id="7968b-104">Postmortem</span></span>

<span data-ttu-id="7968b-105">Certains incidents de sécurité, en particulier ceux qui ont un impact sur le client ou qui entraînent une violation de données, sont soumis à un post-incident complet.</span><span class="sxs-lookup"><span data-stu-id="7968b-105">Some security incidents, especially those incidents that are customer impacting or result in a data breach, are subject to a full incident postmortem.</span></span> <span data-ttu-id="7968b-106">L’équipe de réponse à la sécurité Microsoft 365 effectue un post-mortem détaillé avec toutes les parties impliquées dans la réponse aux incidents de sécurité pour :</span><span class="sxs-lookup"><span data-stu-id="7968b-106">The Microsoft 365 Security Response team conducts a detailed postmortem with all the parties involved in security incident response to:</span></span>

- <span data-ttu-id="7968b-107">Documenter la séquence d’événements à l’origine de l’incident</span><span class="sxs-lookup"><span data-stu-id="7968b-107">Document the sequence of events that caused the incident</span></span>
- <span data-ttu-id="7968b-108">Créez un résumé technique de l’incident tel qu’il est pris en charge par la preuve qui inclut les acteurs impliqués dans la violation (le cas contraire).</span><span class="sxs-lookup"><span data-stu-id="7968b-108">Create a technical summary of the incident as supported by the evidence that includes the actors involved in the breach (if known).</span></span> <span data-ttu-id="7968b-109">Ce résumé inclut la façon dont la réponse a été exécutée et d’autres éléments à prendre en compte.</span><span class="sxs-lookup"><span data-stu-id="7968b-109">This summary will include how the response was executed and other key takeaways.</span></span>
- <span data-ttu-id="7968b-110">Identifiez les échecs techniques, les défaillances procédurales, les erreurs manuelles, les failles de processus et les problèmes de communication, et/ou les vecteurs d’attaque précédemment inconnus identifiés lors de la réponse aux incidents de sécurité.</span><span class="sxs-lookup"><span data-stu-id="7968b-110">Identify technical lapses, procedural failures, manual errors, process flaws, and communication glitches, and/or any previously unknown attack vectors that were identified during the security incident response.</span></span>

<span data-ttu-id="7968b-111">Le post-mortem influence directement l’amélioration du service Microsoft 365, les processus opérationnels et la documentation en fixant de nouvelles priorités dans le cycle de développement d’ingénierie Microsoft 365.</span><span class="sxs-lookup"><span data-stu-id="7968b-111">The postmortem will directly influence Microsoft 365 service improvement, operational processes, and documentation by setting new priorities in the Microsoft 365 engineering development cycle.</span></span>

## <a name="documentation"></a><span data-ttu-id="7968b-112">Documentation</span><span class="sxs-lookup"><span data-stu-id="7968b-112">Documentation</span></span>

<span data-ttu-id="7968b-113">Toutes les principales conclusions techniques du processus post-mortem sont capturées dans un rapport et les investissements ou correctifs de service sous la forme de bogues ou de demandes de modification de développement.</span><span class="sxs-lookup"><span data-stu-id="7968b-113">All key technical findings in the postmortem process are captured in a report and service investments or fixes in the form of bugs or development change requests.</span></span> <span data-ttu-id="7968b-114">Ces résultats sont suivis des équipes d’ingénierie appropriées.</span><span class="sxs-lookup"><span data-stu-id="7968b-114">These findings are followed-up with the appropriate engineering teams.</span></span> <span data-ttu-id="7968b-115">En cas d’échec de processus et de problèmes organisationnels, les problèmes sont documentés dans la base de données de l’équipe de réponse de sécurité Microsoft 365 et suivis avec les groupes appropriés pour les résoudre.</span><span class="sxs-lookup"><span data-stu-id="7968b-115">For process failures and cross-organizational issues, issues are documented in the Microsoft 365 Security Response team's database and followed-up with the appropriate groups to address them.</span></span>

## <a name="process-improvement"></a><span data-ttu-id="7968b-116">Amélioration des processus</span><span class="sxs-lookup"><span data-stu-id="7968b-116">Process improvement</span></span>

<span data-ttu-id="7968b-117">La réponse à un incident de sécurité dans Microsoft 365 implique la coordination avec plusieurs groupes répartis dans différentes organisations au sein de Microsoft, et potentiellement même des organisations externes appropriées telles que les forces de l’ordre.</span><span class="sxs-lookup"><span data-stu-id="7968b-117">Responding to a security incident in Microsoft 365 involves coordination with multiple groups spread across different organizations within Microsoft, and potentially even appropriate external organizations such as law enforcement.</span></span> <span data-ttu-id="7968b-118">Nous savons qu’il est essentiel d’évaluer nos réponses après chaque incident de sécurité pour des raisons de niveau d’efficacité et d’intégralité.</span><span class="sxs-lookup"><span data-stu-id="7968b-118">We know that it is critical to evaluate our responses after every security incident for both sufficiency and completeness.</span></span> <span data-ttu-id="7968b-119">Pour toutes les améliorations ou modifications identifiées, l’équipe de réponse de sécurité Microsoft 365 évalue les suggestions en consultation avec les équipes et les parties prenantes appropriées, et, le cas échéant, les intègre dans les procédures de fonctionnement standard.</span><span class="sxs-lookup"><span data-stu-id="7968b-119">For any identified improvements or changes, the Microsoft 365 Security Response team evaluates the suggestions in consultation with the appropriate teams and stakeholders, and where appropriate incorporates them into standard operating procedures.</span></span> <span data-ttu-id="7968b-120">Toutes les modifications, bogues ou améliorations de service requises identifiés lors de la réponse aux incidents de sécurité ou de l’activité post-mortem sont consignés et suivis dans une base de données d’ingénierie Microsoft 365 interne.</span><span class="sxs-lookup"><span data-stu-id="7968b-120">All required changes, bugs, or service improvements identified during the security incident response or postmortem activity are logged and tracked in an internal Microsoft 365 engineering database.</span></span> <span data-ttu-id="7968b-121">Tous les bogues ou fonctionnalités potentiels sont affectés au propriétaire approprié.</span><span class="sxs-lookup"><span data-stu-id="7968b-121">All potential bugs or features are assigned to the appropriate owner.</span></span> <span data-ttu-id="7968b-122">L’équipe de réponse de sécurité Microsoft 365 examine toutes les entrées jusqu’à ce que le problème soit résolu.</span><span class="sxs-lookup"><span data-stu-id="7968b-122">The Microsoft 365 Security Response team reviews all entries until the issue is resolved.</span></span>

## <a name="related-articles"></a><span data-ttu-id="7968b-123">Articles connexes</span><span class="sxs-lookup"><span data-stu-id="7968b-123">Related articles</span></span>

- [<span data-ttu-id="7968b-124">Gestion des incidents de sécurité de Microsoft 365</span><span class="sxs-lookup"><span data-stu-id="7968b-124">Microsoft 365 security incident management</span></span>](assurance-security-incident-management.md)
- [<span data-ttu-id="7968b-125">Préparation de la gestion des incidents de sécurité Microsoft 365</span><span class="sxs-lookup"><span data-stu-id="7968b-125">Microsoft 365 security incident management preparation</span></span>](assurance-sim-preparation.md)
- [<span data-ttu-id="7968b-126">Détection et analyse de la gestion des incidents de sécurité Microsoft 365</span><span class="sxs-lookup"><span data-stu-id="7968b-126">Microsoft 365 security incident management detection and analysis</span></span>](assurance-sim-detection-analysis.md)
- [<span data-ttu-id="7968b-127">Contenu, éradication et récupération de la gestion des incidents de sécurité Microsoft 365</span><span class="sxs-lookup"><span data-stu-id="7968b-127">Microsoft 365 security incident management containment, eradication, and recovery</span></span>](assurance-sim-containment-eradication-recovery.md)
