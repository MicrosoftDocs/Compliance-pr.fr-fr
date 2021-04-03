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
# <a name="yammer-enterprise-access-controls"></a>Yammer contrôles d’accès d’entreprise 

L’accès physique et logique à l Yammer de production est limité à un petit groupe de personnes (infrastructure et opérations). Comme avec d’autres ingénieurs Microsoft 365, les ingénieurs Yammer n’ont aucun accès permanent aux données client. L’accès doit être demandé à l’aide d’un système de contrôle d’accès juste-à-temps basé sur l’approbation, semblable à Lockbox avec un nombre limité d’approuveurs. Les approuveurs vérifient la demande (par exemple, ils vérifient si la demande est légitime en fonction des besoins, de l’entreprise, de l’heure, etc.), puis approuvent ou refusent la demande. Si la demande est approuvée, l’accès JIT est accordé pour une durée définie et limitée. Une fois le temps d’accès dépassé, l’accès expire automatiquement.

Comme avec d’autres services Microsoft 365, tout accès à l’environnement de production Yammer utilise l’authentification multifacteur. Tout l’accès et l’historique des commandes sont attribués à un utilisateur, et consignés et examinés régulièrement par l Yammer de sécurité.

Pour plus d’informations sur Yammer’administration et de gestion, voir [Yammer’aide de l’administrateur.](/yammer/yammer-landing-page)