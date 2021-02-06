---
title: Suppression de données SharePoint Online Microsoft 365
description: Découvrez comment fonctionne la suppression des données dans SharePoint Online, par exemple l’endroit où le contenu supprimé est stocké et pendant combien de temps.
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
- SPO_Content
f1.keywords:
- NOCSH
ms.custom: seo-marvel-apr2020
titleSuffix: Microsoft Service Assurance
ms.openlocfilehash: 89281b32dbc577f935224396fd358ed753348ea1
ms.sourcegitcommit: 21ed42335efd37774ff5d17d9586d5546147241a
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 02/05/2021
ms.locfileid: "50120743"
---
# <a name="sharepoint-online-data-deletion-in-microsoft-365"></a><span data-ttu-id="10a01-103">Suppression de données SharePoint Online dans Microsoft 365</span><span class="sxs-lookup"><span data-stu-id="10a01-103">SharePoint Online data deletion in Microsoft 365</span></span>

<span data-ttu-id="10a01-104">SharePoint Online stocke les objets sous forme de code abstrait dans les bases de données d’application.</span><span class="sxs-lookup"><span data-stu-id="10a01-104">SharePoint Online stores objects as abstracted code within application databases.</span></span> <span data-ttu-id="10a01-105">Lorsqu’un utilisateur télécharge un fichier vers SharePoint Online, ce fichier est désassembler et traduit en code d’application et stocké dans plusieurs tables dans plusieurs bases de données.</span><span class="sxs-lookup"><span data-stu-id="10a01-105">When a user uploads a file to SharePoint Online, that file is disassembled and translated into application code and stored in multiple tables across multiple databases.</span></span> <span data-ttu-id="10a01-106">Dans SharePoint Online, tout le contenu téléchargé par un client est divisé en blocs, chiffré (potentiellement avec plusieurs clés AES 256 bits) et distribué dans le centre de données.</span><span class="sxs-lookup"><span data-stu-id="10a01-106">In SharePoint Online, all content that a customer uploads is broken into chunks, encrypted (potentially with multiple AES 256-bit keys), and distributed across the datacenter.</span></span> <span data-ttu-id="10a01-107">Pour plus d’informations sur le processus de création de blocs et de chiffrement, voir [Chiffrement dans Microsoft Cloud.](/microsoft-365/compliance/office-365-encryption-in-the-microsoft-cloud-overview)</span><span class="sxs-lookup"><span data-stu-id="10a01-107">For specific details about the chunking and encryption process, see [Encryption in the Microsoft Cloud](/microsoft-365/compliance/office-365-encryption-in-the-microsoft-cloud-overview).</span></span> 

<span data-ttu-id="10a01-108">Dans SharePoint Online, les éléments sont conservés pendant 93 jours à partir du moment où vous les supprimez de leur emplacement d’origine.</span><span class="sxs-lookup"><span data-stu-id="10a01-108">In SharePoint Online, items are retained for 93 days from the time you delete them from their original location.</span></span> <span data-ttu-id="10a01-109">Ils restent tout le temps dans la Corbeille du site, sauf si quelqu’un les supprime de là ou vide cette Corbeille.</span><span class="sxs-lookup"><span data-stu-id="10a01-109">They stay in the site Recycle Bin the entire time, unless someone deletes them from there or empties that Recycle Bin.</span></span> <span data-ttu-id="10a01-110">Dans ce cas, les éléments sont ajoutés à la Corbeille de la collection de sites, où ils restent pendant 93 jours.</span><span class="sxs-lookup"><span data-stu-id="10a01-110">In that case, the items go to the site collection Recycle Bin, where they stay for the remainder of the 93 days.</span></span> <span data-ttu-id="10a01-111">Pour plus d’informations sur la restauration des éléments supprimés, voir Restaurer des éléments dans la Corbeille d’un [site SharePoint](https://support.office.com/article/6df466b6-55f2-4898-8d6e-c0dff851a0be#ID0EAADAAA=Online
) et Restaurer les éléments supprimés de la Corbeille [de la collection de sites.](https://support.office.com/article/5fa924ee-16d7-487b-9a0a-021b9062d14b)</span><span class="sxs-lookup"><span data-stu-id="10a01-111">For info about restoring deleted items, see [Restore items in the Recycle Bin of a SharePoint site](https://support.office.com/article/6df466b6-55f2-4898-8d6e-c0dff851a0be#ID0EAADAAA=Online
) and [Restore deleted items from the site collection recycle bin](https://support.office.com/article/5fa924ee-16d7-487b-9a0a-021b9062d14b).</span></span> <span data-ttu-id="10a01-112">La durée de rétention de la Corbeille n’est pas configurable dans SharePoint Online.</span><span class="sxs-lookup"><span data-stu-id="10a01-112">The Recycle Bin retention time is not configurable in SharePoint Online.</span></span>

<span data-ttu-id="10a01-113">Lorsque vous supprimez une collection de sites, vous supprimez également la hiérarchie des sites de la collection et tout le contenu qu’elle contient :</span><span class="sxs-lookup"><span data-stu-id="10a01-113">When you delete a site collection, you're also deleting the hierarchy of sites in the collection, and all content within them:</span></span>

- <span data-ttu-id="10a01-114">les documents et bibliothèques de documents ;</span><span class="sxs-lookup"><span data-stu-id="10a01-114">Documents and document libraries</span></span>
- <span data-ttu-id="10a01-115">Listes et données de liste</span><span class="sxs-lookup"><span data-stu-id="10a01-115">Lists and list data</span></span>
- <span data-ttu-id="10a01-116">Paramètres de configuration de site</span><span class="sxs-lookup"><span data-stu-id="10a01-116">Site configuration settings</span></span>
- <span data-ttu-id="10a01-117">Informations de rôle et de sécurité relatives au site ou à ses sous-sites</span><span class="sxs-lookup"><span data-stu-id="10a01-117">Role and security information that is related to the site or its subsites</span></span>
- <span data-ttu-id="10a01-118">Sous-sites du site web de niveau supérieur, leur contenu et les informations utilisateur</span><span class="sxs-lookup"><span data-stu-id="10a01-118">Subsites of the top-level website, their contents, and user information</span></span>

<span data-ttu-id="10a01-119">Si vous supprimez accidentellement une collection de sites, elle peut être restaurée par un administrateur global ou SharePoint à l’aide du Centre d’administration SharePoint.</span><span class="sxs-lookup"><span data-stu-id="10a01-119">If you accidentally delete a site collection, it can be restored by a global or SharePoint admin using the SharePoint admin center.</span></span>

<span data-ttu-id="10a01-120">Les collections de sites supprimées sont conservées pendant 93 jours.</span><span class="sxs-lookup"><span data-stu-id="10a01-120">Deleted site collections are retained for 93 days.</span></span> <span data-ttu-id="10a01-121">Après 93 jours, les sites et tous leurs contenus et paramètres sont supprimés définitivement, y compris les listes, bibliothèques, pages et tous les sous-sites.</span><span class="sxs-lookup"><span data-stu-id="10a01-121">After 93 days, sites and all their content and settings are permanently deleted, including lists, libraries, pages, and any subsites.</span></span>

<span data-ttu-id="10a01-122">La suppression définitive se produit lorsqu’un utilisateur purge les éléments supprimés de la Corbeille de la collection de sites, lorsque les périodes de rétention et de sauvegarde expirent ou lorsqu’un administrateur supprime définitivement une collection de sites à l’aide de la [cmdlet Remove-SPODeletedSite.](/powershell/module/sharepoint-online/remove-spodeletedsite)</span><span class="sxs-lookup"><span data-stu-id="10a01-122">Hard deletion occurs when a user purges deleted items from the site collection Recycle Bin, when the retention and backup periods expire, or when an administrator permanently deletes a site collection using the [Remove-SPODeletedSite cmdlet](/powershell/module/sharepoint-online/remove-spodeletedsite).</span></span> <span data-ttu-id="10a01-123">Lorsqu’un utilisateur supprime (définitivement ou purge) le contenu de SharePoint Online, toutes les clés de chiffrement des blocs supprimés sont également supprimées.</span><span class="sxs-lookup"><span data-stu-id="10a01-123">When a user hard deletes (permanently deletes, or purges) content from SharePoint Online, all encryption keys for the deleted chunks are also deleted.</span></span> <span data-ttu-id="10a01-124">Les blocs sur les disques qui stockaient précédemment les blocs supprimés sont marqués comme inutilisés et peuvent être réutilisés.</span><span class="sxs-lookup"><span data-stu-id="10a01-124">The blocks on the disks that previously stored the deleted chunks are marked as unused and available for re-use.</span></span>
