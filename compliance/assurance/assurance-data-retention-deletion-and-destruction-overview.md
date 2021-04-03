---
title: Rétention, suppression et destruction des données dans Microsoft 365
description: Vue d’ensemble des stratégies Microsoft pour Microsoft 365 concernant la rétention, la suppression et la destruction des données.
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
titleSuffix: Microsoft Service Assurance
hideEdit: true
ms.openlocfilehash: f7026d0b9fe27e3818b7b31ed7b4d1e07b62471e
ms.sourcegitcommit: 024137a15ab23d26cac5ec14c36f3577fd8a0cc4
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 04/01/2021
ms.locfileid: "51497611"
---
# <a name="data-retention-deletion-and-destruction-in-microsoft-365"></a>Rétention, suppression et destruction des données dans Microsoft 365

Microsoft a une stratégie standard de gestion des données pour Microsoft 365 qui spécifie la durée de rétention des données client après la suppression. Il existe généralement deux scénarios dans lesquels les données client sont supprimées :

- **Suppression active :** le client dispose d’un abonnement actif et un utilisateur ou un administrateur supprime des données, ou les administrateurs suppriment un utilisateur.
- **Suppression passive :** l’abonnement client se termine.

## <a name="data-retention"></a>Rétention des données

Pour chacun de ces scénarios de suppression, le tableau suivant indique la période maximale de rétention des données, par catégorie et classification de données :

| Catégorie de données | Classification des données | Description | Exemples | Période de rétention |
|-----------------|-----------------|-----------------|----------------------------------|-------------------------------|
| Données client | Contenu client| Contenu directement fourni/créé par les administrateurs et les utilisateurs <br><br> Inclut tous les textes, sons, vidéos, fichiers image et logiciels créés et stockés dans les centres de données Microsoft lors de l’utilisation des services dans Microsoft 365 | Word, Excel, PowerPoint, Outlook et OneNote sont des exemples d’applications Microsoft 365 les plus couramment utilisées qui permettent aux utilisateurs de faire des données <br><br> Le contenu client inclut également les clés secrètes que le client possède/fournit (mots de passe, certificats, clés de chiffrement, clés de stockage) | **Scénario de suppression active :** au maximum 30 jours <br><br> **Scénario de suppression passive :** au maximum 180 jours |
| Données client | Informations d’identification personnelle de l’utilisateur final (EUII) | Données qui identifient ou peuvent être utilisées pour identifier l’utilisateur d’un service Microsoft. L’EUII ne contient pas de contenu client | Nom d’utilisateur ou nom complet (DOMAIN\UserName) <br><br> Nom d’utilisateur principal (name@domain) <br><br>  Adresses IP spécifiques à l’utilisateur | **Scénario de suppression active :** au maximum 180 jours (seule une action de l’administrateur client) <br><br> **Scénario de suppression passive :** au maximum 180 jours |
| Données personnelles <br> (données non incluses dans les données client) | Identificateurs pseudonymes d’utilisateur final (EUPI) | Identificateur créé par Microsoft lié à l’utilisateur d’un service Microsoft. Lorsqu’il est combiné avec d’autres informations, telles qu’une table de mappage, l’EUPI identifie l’utilisateur final <br><br> L’EUPI ne contient pas d’informations téléchargées ou créées par le client | GUID utilisateur, PUID ou SIDs <br><br> ID de session | **Scénario de suppression active :** au maximum 30 jours <br><br> **Scénario de suppression passive :** au maximum 180 jours |

## <a name="subscription-retention"></a>Rétention d’abonnement

Dans le cas d’un abonnement actif, un abonné peut accéder, extraire ou supprimer des données client stockées dans Microsoft 365. Si un abonnement payant se termine ou est résilié, Microsoft conserve les données client stockées dans Microsoft 365 dans un compte à fonction limitée pendant 90 jours pour permettre à l’abonné d’extraire les données. Une fois la période de rétention de 90 jours terminée, Microsoft désactive le compte et supprime les données client. Après un maximum de 180 jours suivant l’expiration ou la résiliation d’un abonnement Microsoft 365, Microsoft désactive le compte et supprime toutes les données client du compte. Une fois la période de rétention maximale des données écoulée, celles-ci sont rendues irrécupérables au plan commercial.

Pour une version d’essai gratuite, votre compte passe à l’état de grâce pendant 30 jours dans la plupart des pays et régions. Au cours de cette période de grâce, vous pouvez acheter Microsoft 365. Si vous décidez de ne pas acheter Microsoft 365, vous pouvez soit annuler votre version d’évaluation, soit laisser l’expiration de la période de grâce, et les informations et les données de votre compte d’évaluation sont supprimées.

## <a name="expedited-deletion"></a>Suppression accélérée

Pour les abonnements, l’abonné peut contacter le support Microsoft et demander une rapide mise hors service de l’abonnement. Dans le cadre de ce processus, toutes les données utilisateur sont supprimées trois jours après la saisie par l’administrateur du code de verrouillage fourni par Microsoft. Cela inclut les données présentes dans SharePoint Online et Exchange Online mises en attente ou stockées dans des boîtes aux lettres inactives.

Pour plus d’informations sur la désapprovisionnement accéléré, voir [Annuler votre abonnement.](/microsoft-365/commerce/subscriptions/cancel-your-subscription)

## <a name="related-links"></a>Liens connexes

- [Destruction de données](assurance-data-destruction.md)
- [Immuabilité dans Office 365](assurance-data-immutability.md)
- [Suppression de données Exchange Online](assurance-exchange-online-data-deletion.md)
- [Suppression de données SharePoint Online](assurance-sharepoint-online-data-deletion.md)
