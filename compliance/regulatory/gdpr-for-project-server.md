---
title: RGPD pour Project Server
description: Découvrez comment répondre aux exigences en matière de Règlement général sur la protection des données (RGPD) dans un serveurs Project local.
f1.keywords:
- NOCSH
ms.author: mikeplum
author: MikePlumleyMSFT
manager: pamgreen
audience: ITPro
ms.topic: article
ms.service: O365-seccomp
localization_priority: Priority
titleSuffix: Microsoft GDPR
ms.custom: seo-marvel-apr2020
ms.collection: MS-Compliance
hideEdit: true
ms.openlocfilehash: ddbf22523caf1869d0253599216fff07ee14f751
ms.sourcegitcommit: 024137a15ab23d26cac5ec14c36f3577fd8a0cc4
ms.translationtype: HT
ms.contentlocale: fr-FR
ms.lasthandoff: 04/01/2021
ms.locfileid: "51495956"
---
# <a name="gdpr-for-project-server"></a><span data-ttu-id="3552a-103">RGPD pour Project Server</span><span class="sxs-lookup"><span data-stu-id="3552a-103">GDPR for Project Server</span></span>

<span data-ttu-id="3552a-p101">Project Server utilise des scripts personnalisés pour exporter et supprimer des données utilisateur dans Project Web App. Le processus de base est le suivant :</span><span class="sxs-lookup"><span data-stu-id="3552a-p101">Project Server uses custom scripts to export and redact user data in Project Web App. The basic process is:</span></span>

1.  <span data-ttu-id="3552a-106">Recherchez les sites Project Web App dans votre batterie de serveurs.</span><span class="sxs-lookup"><span data-stu-id="3552a-106">Find the Project Web App sites in your farm.</span></span>

2.  <span data-ttu-id="3552a-107">Recherchez les projets dans chaque site contenant l’utilisateur.</span><span class="sxs-lookup"><span data-stu-id="3552a-107">Find the projects in each site that contain the user.</span></span>

3.  <span data-ttu-id="3552a-108">Exportez et passez en revue les types de données que vous voulez examiner.</span><span class="sxs-lookup"><span data-stu-id="3552a-108">Export and review the types of data that you want to review.</span></span>

4.  <span data-ttu-id="3552a-109">Supprimez des données si nécessaire.</span><span class="sxs-lookup"><span data-stu-id="3552a-109">Redact data as needed.</span></span>

<span data-ttu-id="3552a-110">Ces étapes sont expliquées en détail dans les articles suivants :</span><span class="sxs-lookup"><span data-stu-id="3552a-110">These steps are covered in detail in the following articles:</span></span>

- [<span data-ttu-id="3552a-111">Exportation de données utilisateur depuis Project Server</span><span class="sxs-lookup"><span data-stu-id="3552a-111">Export user data from Project Server</span></span>](/Project/export-user-data-from-project-server?toc=/Office365/Enterprise/toc.json)

- [<span data-ttu-id="3552a-112">Suppression de données utilisateur de Project Server</span><span class="sxs-lookup"><span data-stu-id="3552a-112">Delete user data from Project Server</span></span>](/Project/delete-user-data-from-project-server?toc=/Office365/Enterprise/toc.json)


<span data-ttu-id="3552a-p102">Notez que Project Server est basé sur SharePoint Server et consigne les événements dans les journaux ULS de SharePoint et dans la base de données d’utilisation. Pour en savoir plus, consultez l’article qui traite du [RGPD dans SharePoint Server](gdpr-for-sharepoint-server.md).</span><span class="sxs-lookup"><span data-stu-id="3552a-p102">Note that Project Server is built on top of SharePoint Server and logs events to the SharePoint ULS logs and Usage database. See [GDPR for SharePoint Server](gdpr-for-sharepoint-server.md) for more information.</span></span>
