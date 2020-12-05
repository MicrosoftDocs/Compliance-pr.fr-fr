---
title: Microsoft 365 pour les facteurs atténuants de la gestion de la continuité d’entreprise
description: Voici quelques exemples d’atténuation pour les scénarios d’incident de service Microsoft 365.
author: robmazz
ms.author: robmazz
manager: laurawi
ms.reviewer: sosstah
audience: ITPro
ms.topic: article
f1.keywords:
- NOCSH
ms.service: o365-solutions
localization_priority: Normal
ms.collection:
- M365-subscription-management
- Strat_O365_Enterprise
- MS-Compliance
titleSuffix: Microsoft Service Assurance
ms.openlocfilehash: b31ee58d4e9a60232d7d5df4ff1bf4f16b6266cf
ms.sourcegitcommit: 693bc6b1b51a5a9c9ff1758fa7f7ca3a204f147e
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 12/04/2020
ms.locfileid: "49574746"
---
# <a name="service-incident-mitigation-strategies"></a>Stratégies d’atténuation des incidents de service

Voici quelques stratégies et scénarios qui présentent la façon atténuer l’impact d’un incident de service Microsoft 365 sur votre processus d’entreprise.

## <a name="service-incident-scenarios-and-potential-mitigations"></a>Scénarios d’incident de service et atténuations potentielles

|Dépendance Microsoft 365|atténuations potentielles|
|---------|---------|
|Le système de gestion des incidents s’appuie sur Exchange Online pour impliquer les ingénieurs et responsables d’incident disponibles.|Assurez-vous que le système de gestion des incidents prend en charge les communications multicanaux, telles que la messagerie parallèle, les appels téléphoniques et les notifications par SMS, et des hiérarchies d’arborescence d’appels au cas où l’appel principal ne s’effectuerait pas, le système exécute automatiquement la sauvegarde. Incluez également les méthodes de contact de sauvegarde dans toutes les notifications, de sorte que les méthodes de communication de sauvegarde soient incorporées pour en faciliter la consultation. D’autres méthodes de communication, telles que Yammer, peuvent être utilisées pour la collaboration d’urgence si le service de gestion des incidents n’est pas disponible.|
|Microsoft Teams est utilisé pour stocker les fichiers accessibles via le client.|Teams stocke les fichiers chargés sur le client dans une bibliothèque de documents SharePoint Online. Les fichiers sont encore accessibles via SharePoint Online. Formation des utilisateurs sur l’emplacement des fichiers dans SharePoint Online.|
|La téléconférence Microsoft Teams est utilisée pour la communication générale et le tri de la gestion des incidents.|Établir une solution de conférence de sauvegarde avec un fournisseur tiers.|
|Les téléphones VoIP sont utilisés comme mode de communication secondaire.|Implémentez des téléphones non-VoIP capables d’effectuer des appels PSTN, notamment pour les centres d’opérations de réseau et de service pendant les incidents. Ajoutez les numéros de téléphone mobile des employés à l’annuaire de l’entreprise pour permettre au personnel en détresse d’être contacté via le réseau cellulaire.|
|OneDrive Entreprise est utilisé pour le stockage de fichiers et la productivité des utilisateurs. [Les fichiers à la demande](https://techcommunity.microsoft.com/t5/Microsoft-OneDrive-Blog/OneDrive-Files-On-Demand-For-The-Enterprise/ba-p/117234) sont configurés pour libérer de l’espace sur les lecteurs d’utilisateurs locaux.|La synchronisation avec OneDrive fournit des stratégies de groupe qui permettent aux administrateurs de faire en sorte que le contenu spécifique soit synchronisé en local ou de libérer de l’espace lorsque c’est nécessaire. Pour réduire le risque d’inaccessibilité des documents, configurez cette stratégie de manière à synchroniser localement les documents importants. Formez les utilisateurs à appliquer manuellement le paramètre « Toujours conserver sur cet appareil » pour les documents importants.|
|Exchange Online permet de communiquer les perturbations de productivité aux clients et aux fournisseurs.|Les réseaux sociaux tiers publics peuvent être utilisés comme autres moyens de communication de masse.
|L’utilisation d’une architecture locale hybride, telle que l’ADFS ou l’authentification directe, provoque une perturbation de la possibilité pour l’utilisateur de s’authentifier auprès des services cloud.|Configurer la[synchronisation de hachage de mot de passe](https://docs.microsoft.com/azure/active-directory/authentication/concept-resilient-controls#deploy-password-hash-sync-even-if-you-are-federated-or-use-pass-through-authentication), conjointement avec vos services d’authentification hybrides, comme mécanisme secondaire d’authentification basée sur le cloud afin d’éviter toute perturbation de la connexion pendant la panne. Pour plus d’informations sur la création d’architectures d’authentification et de contrôle d’accès résilients, voir [Créer une stratégie de gestion de contrôle d’accès résiliente avec Azure Active Directory](https://docs.microsoft.com/azure/active-directory/authentication/concept-resilient-controls).|  

## <a name="leveraging-mobile-app-access"></a>Profiter de l'accès aux applications mobiles

Au fur et à mesure de la prolifération des appareils mobiles, il existe de nouveaux moyens de rester connectés et les applications mobiles Microsoft 365 peuvent être un élément clé de votre stratégie de résilience. Dans la mesure où ils se connectent aux services Cloud via le réseau du fournisseur cellulaire, ils ne dépendent pas de l’infrastructure réseau de votre organisation.

Prenons Outlook comme exemple. Les utilisateurs peuvent se connecter à leurs boîtes aux lettres Exchange Online via différents protocoles réseau (HTTPS ou MAPI) en fonction de l’application de messagerie utilisée. En cas d’incident de service impliquant l’un des protocoles (par exemple, MAPI) utilisé par le client de bureau, vos utilisateurs peuvent continuer à utiliser leur boîte aux lettres via l’application Outlook Mobile ou Outlook sur le Web.
  
Si vous décidez d’autoriser les utilisateurs à se connecter aux services Microsoft 365 via leurs appareils mobiles, vous pouvez utiliser Microsoft Intune pour configurer et gérer ces appareils de façon sécurisée. Une fois que les comptes d’utilisateurs et les appareils sont inscrits à votre solution de gestion mobile, assurez-vous que les applications ont été téléchargées et configurées.
