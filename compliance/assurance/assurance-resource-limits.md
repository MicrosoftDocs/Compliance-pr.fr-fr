---
title: Limites de ressources de Microsoft 365
description: Dans cet article, vous trouverez des informations sur les limites de ressources pour les différentes applications dans Microsoft 365.
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
ms.openlocfilehash: 632a0b78c5c5ba02a59f8863c2e751f009cc968e
ms.sourcegitcommit: 21ed42335efd37774ff5d17d9586d5546147241a
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 02/05/2021
ms.locfileid: "50120753"
---
# <a name="service-resource-limits"></a><span data-ttu-id="6276d-103">Limitation des ressources des services</span><span class="sxs-lookup"><span data-stu-id="6276d-103">Service resource limits</span></span>

<span data-ttu-id="6276d-104">Les limites de ressources sont appliquées à l’aide de quotas (limites) et de limitation.</span><span class="sxs-lookup"><span data-stu-id="6276d-104">Resource limits are enforced using quotas (limits) and throttling.</span></span> <span data-ttu-id="6276d-105">Azure Active Directory (Azure AD) et les services Microsoft 365 individuels utilisent les deux.</span><span class="sxs-lookup"><span data-stu-id="6276d-105">Azure Active Directory (Azure AD) and the individual Microsoft 365 services use both.</span></span> <span data-ttu-id="6276d-106">Les limites sont spécifiques au service et changent au fil du temps à mesure que de nouvelles fonctionnalités sont ajoutées.</span><span class="sxs-lookup"><span data-stu-id="6276d-106">Limits are service-specific and change over time as new capabilities are added.</span></span> <span data-ttu-id="6276d-107">Pour plus d’informations sur les limites actuelles des différents services, consultez les rubriques suivantes :</span><span class="sxs-lookup"><span data-stu-id="6276d-107">For details on the current limits for the various services, see the following topics:</span></span>

- [<span data-ttu-id="6276d-108">Limites et restrictions du service Azure AD</span><span class="sxs-lookup"><span data-stu-id="6276d-108">Azure AD service limits and restrictions</span></span>](/azure/azure-resource-manager/management/azure-subscription-service-limits)
- [<span data-ttu-id="6276d-109">Limites d’Exchange Online</span><span class="sxs-lookup"><span data-stu-id="6276d-109">Exchange Online Limits</span></span>](/office365/servicedescriptions/exchange-online-service-description/exchange-online-limits)
- [<span data-ttu-id="6276d-110">Limites et frontières logicielles SharePoint Online</span><span class="sxs-lookup"><span data-stu-id="6276d-110">SharePoint Online software boundaries and limits</span></span>](https://support.office.com/article/SharePoint-Online-software-boundaries-and-limits-8F34FF47-B749-408B-ABC0-B605E1F6D498)
- [<span data-ttu-id="6276d-111">Limites de Skype Entreprise</span><span class="sxs-lookup"><span data-stu-id="6276d-111">Skype for Business Limits</span></span>](https://technet.microsoft.com/library/skype-for-business-online-limits.aspx)
- [<span data-ttu-id="6276d-112">Yammer API REST et limites de taux</span><span class="sxs-lookup"><span data-stu-id="6276d-112">Yammer REST API and Rate Limits</span></span>](https://developer.yammer.com/docs/rest-api-rate-limits)
- [<span data-ttu-id="6276d-113">Limites de taille de fichier dans Sway</span><span class="sxs-lookup"><span data-stu-id="6276d-113">File Size Limits in Sway</span></span>](https://support.office.com/article/File-size-limits-in-Sway-4db21bc6-b42b-499f-9272-66e089db109f)

<span data-ttu-id="6276d-114">En plus de ces limites, plusieurs mécanismes de limitation sont utilisés dans Azure AD et Microsoft 365.</span><span class="sxs-lookup"><span data-stu-id="6276d-114">In addition to these limits, several throttling mechanisms are used throughout Azure AD and Microsoft 365.</span></span> <span data-ttu-id="6276d-115">La limitation au sein du service est particulièrement importante, étant donné que les ressources réseau dans les centres de données de Microsoft sont optimisées pour le large éventail de clients qui utilisent les services.</span><span class="sxs-lookup"><span data-stu-id="6276d-115">Throttling within the service is especially important, given that network resources in Microsoft's datacenters are optimized for the broad set of customers that use the services.</span></span> <span data-ttu-id="6276d-116">Les mécanismes de limitation sont les suivants :</span><span class="sxs-lookup"><span data-stu-id="6276d-116">Throttling mechanisms include:</span></span>

- <span data-ttu-id="6276d-117">Azure AD et Microsoft 365 offrent des fonctionnalités de limitation au niveau de l’utilisateur, qui limitent le nombre de transactions ou d’appels simultanés (par script ou code) qui peuvent être effectués par un seul utilisateur.</span><span class="sxs-lookup"><span data-stu-id="6276d-117">Azure AD and Microsoft 365 feature user-level throttling, which limit the number of transactions or concurrent calls (by script or code) that can be performed by a single user.</span></span>
- <span data-ttu-id="6276d-118">Une stratégie de limitation PowerShell par défaut est attribuée à chaque client lors de la création du client.</span><span class="sxs-lookup"><span data-stu-id="6276d-118">A default PowerShell throttling policy is assigned to each tenant at tenant creation.</span></span> <span data-ttu-id="6276d-119">Ces paramètres affectent d’autres éléments, tels que le nombre maximal de sessions PowerShell simultanées qui peuvent être ouvertes par un seul administrateur.</span><span class="sxs-lookup"><span data-stu-id="6276d-119">These settings affect other items, such as the maximum number of simultaneous PowerShell sessions that can be opened by a single administrator.</span></span>
- <span data-ttu-id="6276d-120">Chaque client Exchange Online dispose d’une stratégie par défaut des services web Exchange (EWS) qui est mise au point pour les opérations clientes EWS et de la limitation qui s’applique à tous les clients Outlook.</span><span class="sxs-lookup"><span data-stu-id="6276d-120">Each Exchange Online customer has a default Exchange Web Services (EWS) policy that is tuned for EWS client operations, and throttling that applies to all Outlook clients.</span></span>
