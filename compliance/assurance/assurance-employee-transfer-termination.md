---
title: Transfert et résiliation des employés de Microsoft
description: En savoir plus sur le processus de transfert et de résiliation des employés de Microsoft dans Microsoft 365
ms.author: robmazz
author: robmazz
manager: laurawi
ms.reviewer: sosstah
audience: Admin
ms.topic: article
f1.keywords:
- NOCSH
ms.service: O365-seccomp
localization_priority: Normal
ms.collection:
- Strat_O365_IP
- M365-security-compliance
search.appverid:
- MET150
- MOE150
titleSuffix: Microsoft Service Assurance
hideEdit: true
ms.openlocfilehash: b31dd13f4a6209712a9cc212ab3bcd9c5addf6b7
ms.sourcegitcommit: fb379d1110a9a86c7f9bab8c484dc3f4b3dfd6f0
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 06/23/2021
ms.locfileid: "53089610"
---
# <a name="microsoft-employee-transfer-and-termination"></a>Transfert et résiliation des employés de Microsoft

Les transferts et les résiliations d’employés font partie des opérations normales de chaque organisation. Lorsqu’un employé change de poste ou quitte l’entreprise, il est essentiel de révoquer l’accès inapproprié en temps voulu. Pour faciliter les modifications d’accès efficaces et les révocations d’accès, Microsoft 365 utilise des procédures normalisées et des processus automatisés pour coordonner le système d’information des ressources humaines (HRIS) avec le système de gestion des identités (IDM). L’orchestration automatisée entre ces deux systèmes est essentielle pour maintenir la cohérence opérationnelle, la protection des services et des données de Microsoft 365, la prévention des privilèges et la réduction des risques liés aux menaces internes.

Microsoft 365 sont conçus pour fonctionner sans accès administratif permanent aux environnements de production pour nos ingénieurs. Microsoft utilise un modèle juste-à-temps (JIT), Just-Enough-Access (JEA) pour fournir aux ingénieurs l’accès temporaire nécessaire pour prendre en charge leur service si nécessaire. Pour demander et utiliser un compte d’équipe de service pour l’accès JIT, les ingénieurs doivent demander et maintenir des éligibilités via l’outil IDM. Lorsque les employés sont transférés ou licenciés, leur compte d’équipe de service et les éligibilités associées sont automatiquement modifiés pour empêcher tout accès inapproprié.

## <a name="transfer-and-reassignment"></a>Transfert et réaffectation

Les transferts d’employés sont initiés via une demande de transaction de transfert par le responsable de l’employé. Le responsable crée une demande et s’engage dans l’acquisition de talents global pour le processus de lettre d’offre. Une fois que l’employé accepte l’offre pour le nouveau rôle, les services RH terminent le transfert dans les outils de cœur de ressources humaines, déclenchant IDM pour définir une date d’expiration pour toutes les conditions d’éligibilité de l’employé. L’employé doit envoyer une demande et recevoir l’approbation de son nouveau responsable pour conserver ses éligibilités. Le fait de ne pas envoyer une demande ou de recevoir l’approbation du responsable entraîne la révocation des conditions d’éligibilité de l’employé transféré. Pour les transferts qui incluent des implications spécifiques en matière de sécurité, les accès au système et les appartenances aux groupes de sécurité sont réévalués immédiatement pour refléter leur nouveau rôle.

## <a name="termination"></a>Résiliation

Microsoft utilise des stratégies et des procédures clairement définies pour révoquer rapidement l'accès physique et logique aux systèmes et ressources de Microsoft lorsqu'un employé est licencié. Lorsqu’un employé donne son avis, le responsable de l’employé entre la date de résiliation dans le HRIS. Après le dernier jour oué de travail de l’employé, le HRIS marque l’employé comme licencié et partage les informations à IDM, ce qui supprime automatiquement tous les comptes d’équipe de service et les éligibilités.

Pour les résiliations int gr es, hr travaille avec le responsable de l’employé pour suivre les étapes appropriées pour mettre fin à l’employé et l’en déboarder. Comme pour un arrêt volontaire, les informations de résiliation sont entrées dans le HRIS, ainsi que toutes les étapes nécessaires telles que la coordination de la date d’effet, la suppression de l’accès. et les autres étapes relatives à la transition hors rôle.
