---
title: Contrôles d’accès Microsoft 365 Yammer entreprise
description: Cet article contient un bref résumé sur Yammer contrôles d’accès d’entreprise dans l’environnement de production.
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
f1.keywords:
- NOCSH
ms.custom: seo-marvel-apr2020
titleSuffix: Microsoft Service Assurance
hideEdit: true
ms.openlocfilehash: df345d922bbd0c9106cf0714377803a9c0870d82
ms.sourcegitcommit: 024137a15ab23d26cac5ec14c36f3577fd8a0cc4
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 04/01/2021
ms.locfileid: "51497354"
---
# <a name="yammer-enterprise-access-controls"></a><span data-ttu-id="30664-103">Yammer contrôles d’accès d’entreprise</span><span class="sxs-lookup"><span data-stu-id="30664-103">Yammer enterprise access controls</span></span> 

<span data-ttu-id="30664-104">L’accès physique et logique à l Yammer de production est limité à un petit groupe de personnes (infrastructure et opérations).</span><span class="sxs-lookup"><span data-stu-id="30664-104">Physical and logical access to the Yammer production environment is restricted to a small set of people (infrastructure and operations).</span></span> <span data-ttu-id="30664-105">Comme avec d’autres ingénieurs Microsoft 365, les ingénieurs Yammer n’ont aucun accès permanent aux données client.</span><span class="sxs-lookup"><span data-stu-id="30664-105">As with other Microsoft 365 engineers, Yammer engineers have zero standing access to customer data.</span></span> <span data-ttu-id="30664-106">L’accès doit être demandé à l’aide d’un système de contrôle d’accès juste-à-temps basé sur l’approbation, semblable à Lockbox avec un nombre limité d’approuveurs.</span><span class="sxs-lookup"><span data-stu-id="30664-106">Access must be requested using an approval-based just-in-time access control system similar to Lockbox with a limited number of approvers.</span></span> <span data-ttu-id="30664-107">Les approuveurs vérifient la demande (par exemple, ils vérifient si la demande est légitime en fonction des besoins, de l’entreprise, de l’heure, etc.), puis approuvent ou refusent la demande.</span><span class="sxs-lookup"><span data-stu-id="30664-107">Approvers verify the request (for example, they verify whether the request is legitimate based on need, business case, time, etc.), and then approve or deny the request.</span></span> <span data-ttu-id="30664-108">Si la demande est approuvée, l’accès JIT est accordé pour une durée définie et limitée.</span><span class="sxs-lookup"><span data-stu-id="30664-108">If the request is approved, JIT access is granted for a defined and limited time.</span></span> <span data-ttu-id="30664-109">Une fois le temps d’accès dépassé, l’accès expire automatiquement.</span><span class="sxs-lookup"><span data-stu-id="30664-109">After access time is exceeded, the access automatically expires.</span></span>

<span data-ttu-id="30664-110">Comme avec d’autres services Microsoft 365, tout accès à l’environnement de production Yammer utilise l’authentification multifacteur.</span><span class="sxs-lookup"><span data-stu-id="30664-110">As with other Microsoft 365 services, all access to the Yammer production environment uses multi-factor authentication.</span></span> <span data-ttu-id="30664-111">Tout l’accès et l’historique des commandes sont attribués à un utilisateur, et consignés et examinés régulièrement par l Yammer de sécurité.</span><span class="sxs-lookup"><span data-stu-id="30664-111">All access and command history is attributed to a user, and logged and reviewed regularly by the Yammer security team.</span></span>

<span data-ttu-id="30664-112">Pour plus d’informations sur Yammer’administration et de gestion, voir [Yammer’aide de l’administrateur.](/yammer/yammer-landing-page)</span><span class="sxs-lookup"><span data-stu-id="30664-112">For more information about Yammer administration and management, see [Yammer admin help](/yammer/yammer-landing-page).</span></span>