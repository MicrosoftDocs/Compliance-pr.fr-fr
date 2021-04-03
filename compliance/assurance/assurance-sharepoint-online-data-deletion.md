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
hideEdit: true
ms.openlocfilehash: e89a261e44ef4eb4a1399027b70be88fffb82036
ms.sourcegitcommit: 024137a15ab23d26cac5ec14c36f3577fd8a0cc4
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 04/01/2021
ms.locfileid: "51497412"
---
# <a name="sharepoint-online-data-deletion-in-microsoft-365"></a>Suppression de données SharePoint Online dans Microsoft 365

SharePoint Online stocke les objets sous forme de code abstrait dans les bases de données d’application. Lorsqu’un utilisateur télécharge un fichier vers SharePoint Online, ce fichier est désassembler et traduit en code d’application et stocké dans plusieurs tables dans plusieurs bases de données. Dans SharePoint Online, tout le contenu téléchargé par un client est divisé en blocs, chiffré (potentiellement avec plusieurs clés AES 256 bits) et distribué dans le centre de données. Pour plus d’informations sur le processus de création de blocs et de chiffrement, voir [Chiffrement dans Microsoft Cloud.](/microsoft-365/compliance/office-365-encryption-in-the-microsoft-cloud-overview) 

Dans SharePoint Online, les éléments sont conservés pendant 93 jours à partir du moment où vous les supprimez de leur emplacement d’origine. Ils restent tout le temps dans la Corbeille du site, sauf si quelqu’un les supprime de là ou vide cette Corbeille. Dans ce cas, les éléments sont ajoutés à la Corbeille de la collection de sites, où ils restent pendant 93 jours. Pour plus d’informations sur la restauration des éléments supprimés, voir Restaurer des éléments dans la Corbeille d’un [site SharePoint](https://support.office.com/article/6df466b6-55f2-4898-8d6e-c0dff851a0be#ID0EAADAAA=Online
) et Restaurer les éléments supprimés de la Corbeille [de la collection de sites.](https://support.office.com/article/5fa924ee-16d7-487b-9a0a-021b9062d14b) La durée de rétention de la Corbeille n’est pas configurable dans SharePoint Online.

Lorsque vous supprimez une collection de sites, vous supprimez également la hiérarchie des sites de la collection et tout le contenu qu’elle contient :

- les documents et bibliothèques de documents ;
- Listes et données de liste
- Paramètres de configuration de site
- Informations de rôle et de sécurité relatives au site ou à ses sous-sites
- Sous-sites du site web de niveau supérieur, leur contenu et les informations utilisateur

Si vous supprimez accidentellement une collection de sites, elle peut être restaurée par un administrateur global ou SharePoint à l’aide du Centre d’administration SharePoint.

Les collections de sites supprimées sont conservées pendant 93 jours. Après 93 jours, les sites et tous leurs contenus et paramètres sont supprimés définitivement, y compris les listes, bibliothèques, pages et tous les sous-sites.

La suppression définitive se produit lorsqu’un utilisateur purge les éléments supprimés de la Corbeille de la collection de sites, lorsque les périodes de rétention et de sauvegarde expirent ou lorsqu’un administrateur supprime définitivement une collection de sites à l’aide de la [cmdlet Remove-SPODeletedSite.](/powershell/module/sharepoint-online/remove-spodeletedsite) Lorsqu’un utilisateur supprime (définitivement ou purge) le contenu de SharePoint Online, toutes les clés de chiffrement des blocs supprimés sont également supprimées. Les blocs sur les disques qui stockaient précédemment les blocs supprimés sont marqués comme inutilisés et peuvent être réutilisés.
