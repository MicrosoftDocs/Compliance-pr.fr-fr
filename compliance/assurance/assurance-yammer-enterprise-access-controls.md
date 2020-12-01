---
title: Contrôles d’accès Yammer Enterprise de Microsoft 365
description: Cet article contient un bref résumé des contrôles d’accès à l’entreprise Yammer dans l’environnement de production.
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
ms.openlocfilehash: d44bead3627ed9b99c93bcffc9f29f87731f7407
ms.sourcegitcommit: 626b0076d133e588cd28598c149a7f272fc18bae
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 11/30/2020
ms.locfileid: "49506951"
---
# <a name="yammer-enterprise-access-controls"></a>Contrôles d’accès à l’entreprise Yammer 

L’accès physique et logique à l’environnement de production Yammer est limité à un petit ensemble de personnes (infrastructure et opérations). Comme avec d’autres ingénieurs Microsoft 365, les ingénieurs Yammer disposent d’un accès permanent aux données client. L’accès doit être demandé à l’aide d’un système de contrôle d’accès juste-à-temps basé sur l’approbation, comme le Lockbox avec un nombre limité d’approbateurs. Les approbateurs vérifient la demande (par exemple, ils vérifient si la demande est légitime en fonction de la demande, du cas client, du temps, etc.), puis approuvez ou refusez la demande. Si la demande est approuvée, l’accès JIT est accordé pour un temps défini et limité. Une fois le temps d’accès dépassé, l’accès expire automatiquement.

Tout comme les autres services Microsoft 365, tout accès à l’environnement de production Yammer utilise l’authentification multifacteur. Tous les accès et historique des commandes sont attribués à un utilisateur et sont consignés et révisés régulièrement par l’équipe de sécurité Yammer.

Pour plus d’informations sur l’administration et la gestion de Yammer, consultez [l’aide de l’administrateur de Yammer](https://docs.microsoft.com/yammer/yammer-landing-page).