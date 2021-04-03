---
title: Microsoft 365 traitant de l’altération des données
description: Cet article explique l’altération des données dans Microsoft 365 et les efforts déployés par Microsoft pour empêcher et récupérer des données.
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
ms.custom: seo-marvel-apr2020
titleSuffix: Microsoft Service Assurance
hideEdit: true
ms.openlocfilehash: 9e9f0951f7e349cc70bc96bb6a2d62275848cf04
ms.sourcegitcommit: 024137a15ab23d26cac5ec14c36f3577fd8a0cc4
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 04/01/2021
ms.locfileid: "51497594"
---
# <a name="dealing-with-data-corruption-in-microsoft-365"></a><span data-ttu-id="f572e-103">Gestion de l’altération des données dans Microsoft 365</span><span class="sxs-lookup"><span data-stu-id="f572e-103">Dealing with data corruption in Microsoft 365</span></span>

<span data-ttu-id="f572e-104">L’un des aspects complexes de l’exécution d’un service cloud à grande échelle est la gestion de l’altération des données, étant donné le volume important de données et les systèmes indépendants.</span><span class="sxs-lookup"><span data-stu-id="f572e-104">One of the challenging aspects of running a large-scale cloud service is how to handle data corruption, given the large volume of data and independent systems.</span></span> <span data-ttu-id="f572e-105">L’altération des données peut être causée par :</span><span class="sxs-lookup"><span data-stu-id="f572e-105">Data corruption can be caused by:</span></span>

- <span data-ttu-id="f572e-106">Bogues d’application ou d’infrastructure, qui ont endommagé tout ou partie de l’état de l’application</span><span class="sxs-lookup"><span data-stu-id="f572e-106">Application or infrastructure bugs, corrupting some or all of the application state</span></span>
- <span data-ttu-id="f572e-107">Problèmes matériels qui entraînent la perte de données ou l’impossibilité de lire les données</span><span class="sxs-lookup"><span data-stu-id="f572e-107">Hardware issues that result in lost data or an inability to read data</span></span>
- <span data-ttu-id="f572e-108">Erreurs opérationnelles humaines</span><span class="sxs-lookup"><span data-stu-id="f572e-108">Human operational errors</span></span>
- <span data-ttu-id="f572e-109">Pirates malveillants et employés non régrunts</span><span class="sxs-lookup"><span data-stu-id="f572e-109">Malicious hackers and disgruntled employees</span></span>
- <span data-ttu-id="f572e-110">Incidents dans les services externes qui entraînent une perte de données</span><span class="sxs-lookup"><span data-stu-id="f572e-110">Incidents in external services that result in some loss of data</span></span>

<span data-ttu-id="f572e-111">Étant donné qu’une meilleure résilience de l’intégrité des données implique moins d’incidents de corruption de données, Microsoft a intégré des mécanismes de protection Microsoft 365 pour éviter toute altération, ainsi que des systèmes et des processus qui nous permettent de récupérer des données si c’est le cas.</span><span class="sxs-lookup"><span data-stu-id="f572e-111">Because greater resiliency in data integrity means fewer data corruption incidents, Microsoft has built into Microsoft 365 protection mechanisms to prevent corruption from happening, as well as systems and processes that enable us to recover data if it does.</span></span> <span data-ttu-id="f572e-112">Des vérifications et des processus existent au cours des différentes étapes du processus de publication d’ingénierie pour renforcer la résilience contre l’altération des données, notamment :</span><span class="sxs-lookup"><span data-stu-id="f572e-112">Checks and processes exist within the various stages of the engineering release process to increase resiliency against data corruption, including:</span></span>

- <span data-ttu-id="f572e-113">Conception du système</span><span class="sxs-lookup"><span data-stu-id="f572e-113">System Design</span></span>
- <span data-ttu-id="f572e-114">Organisation et structure du code</span><span class="sxs-lookup"><span data-stu-id="f572e-114">Code organization and structure</span></span>
- <span data-ttu-id="f572e-115">Révision du code</span><span class="sxs-lookup"><span data-stu-id="f572e-115">Code review</span></span>
- <span data-ttu-id="f572e-116">Tests unitaires, tests d’intégration et tests système</span><span class="sxs-lookup"><span data-stu-id="f572e-116">Unit tests, integration tests, and system tests</span></span>
- <span data-ttu-id="f572e-117">Tests/portails de câblage de voyage</span><span class="sxs-lookup"><span data-stu-id="f572e-117">Trip wires tests/gates</span></span>

<span data-ttu-id="f572e-118">Dans les environnements de production Microsoft 365, la réplication homologue entre les centres de données garantit qu’il existe toujours plusieurs copies dynamiques de toutes les données.</span><span class="sxs-lookup"><span data-stu-id="f572e-118">Within Microsoft 365 production environments, peer replication between datacenters ensures that there are always multiple live copies of any data.</span></span> <span data-ttu-id="f572e-119">Les images et les scripts standard sont utilisés pour récupérer les serveurs perdus et les données répliquées sont utilisées pour restaurer les données client.</span><span class="sxs-lookup"><span data-stu-id="f572e-119">Standard images and scripts are used to recover lost servers, and replicated data is used to restore customer data.</span></span> <span data-ttu-id="f572e-120">En raison des processus et des vérifications de résilience des données intégrés, Microsoft ne conserve que les sauvegardes de la documentation du système d’information Microsoft 365 (y compris la documentation relative à la sécurité), à l’aide de la réplication intégrée dans SharePoint Online et de notre outil de référentiel de code interne, Source Domaine.</span><span class="sxs-lookup"><span data-stu-id="f572e-120">Because of the built-in data resiliency checks and processes, Microsoft maintains backups only of Microsoft 365 information system documentation (including security-related documentation), using built-in replication in SharePoint Online and our internal code repository tool, Source Depot.</span></span> <span data-ttu-id="f572e-121">La documentation système est stockée dans SharePoint Online, et le Dossier source contient des images système et d’application.</span><span class="sxs-lookup"><span data-stu-id="f572e-121">System documentation is stored in SharePoint Online, and Source Depot contains system and application images.</span></span> <span data-ttu-id="f572e-122">SharePoint Online et source sont tous deux utilisés par le service de version et sont répliqués en temps quasi réel.</span><span class="sxs-lookup"><span data-stu-id="f572e-122">Both SharePoint Online and Source Depot use versioning and are replicated in near real time.</span></span>
