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
hideEdit: true
ms.openlocfilehash: 54ea001e542cdd1ab078546cf96bd011e27ab1dc
ms.sourcegitcommit: 024137a15ab23d26cac5ec14c36f3577fd8a0cc4
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 04/01/2021
ms.locfileid: "51497499"
---
# <a name="service-resource-limits"></a>Limitation des ressources des services

Les limites de ressources sont appliquées à l’aide de quotas (limites) et de limitation. Azure Active Directory (Azure AD) et les services Microsoft 365 individuels utilisent les deux. Les limites sont spécifiques au service et changent au fil du temps à mesure que de nouvelles fonctionnalités sont ajoutées. Pour plus d’informations sur les limites actuelles des différents services, consultez les rubriques suivantes :

- [Limites et restrictions du service Azure AD](/azure/azure-resource-manager/management/azure-subscription-service-limits)
- [Limites d’Exchange Online](/office365/servicedescriptions/exchange-online-service-description/exchange-online-limits)
- [Limites et frontières logicielles SharePoint Online](https://support.office.com/article/SharePoint-Online-software-boundaries-and-limits-8F34FF47-B749-408B-ABC0-B605E1F6D498)
- [Limites de Skype Entreprise](https://technet.microsoft.com/library/skype-for-business-online-limits.aspx)
- [Yammer API REST et limites de taux](https://developer.yammer.com/docs/rest-api-rate-limits)
- [Limites de taille de fichier dans Sway](https://support.office.com/article/File-size-limits-in-Sway-4db21bc6-b42b-499f-9272-66e089db109f)

En plus de ces limites, plusieurs mécanismes de limitation sont utilisés dans Azure AD et Microsoft 365. La limitation au sein du service est particulièrement importante, étant donné que les ressources réseau dans les centres de données de Microsoft sont optimisées pour le large éventail de clients qui utilisent les services. Les mécanismes de limitation sont les suivants :

- Azure AD et Microsoft 365 offrent des fonctionnalités de limitation au niveau de l’utilisateur, qui limitent le nombre de transactions ou d’appels simultanés (par script ou code) qui peuvent être effectués par un seul utilisateur.
- Une stratégie de limitation PowerShell par défaut est attribuée à chaque client lors de la création du client. Ces paramètres affectent d’autres éléments, tels que le nombre maximal de sessions PowerShell simultanées qui peuvent être ouvertes par un seul administrateur.
- Chaque client Exchange Online dispose d’une stratégie par défaut des services web Exchange (EWS) qui est mise au point pour les opérations clientes EWS et de la limitation qui s’applique à tous les clients Outlook.
