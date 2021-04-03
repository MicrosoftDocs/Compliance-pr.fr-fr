---
title: Contrôles d’accès administratif dans Microsoft 365
description: Cet article fournit une vue d’ensemble des contrôles d’accès administratifs et de la catégorisation des données dans Microsoft 365.
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
f1.keywords:
- NOCSH
ms.collection:
- Strat_O365_IP
- M365-security-compliance
- MS-Compliance
ms.custom: seo-marvel-apr2020
titleSuffix: Microsoft Service Assurance
hideEdit: true
ms.openlocfilehash: e7dc9d73b6eb1961387d85910bb558e85498ffae
ms.sourcegitcommit: 024137a15ab23d26cac5ec14c36f3577fd8a0cc4
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 04/01/2021
ms.locfileid: "51497703"
---
# <a name="administrative-access-controls-in-microsoft-365"></a>Contrôles d’accès administratif dans Microsoft 365 

Microsoft a lourdement investi dans des systèmes et des contrôles qui automatisent la plupart des opérations De Microsoft 365 tout en limitant intentionnellement l’accès au contenu client par Microsoft. Les humains régissent le service et les logiciels le gèrent. Cette structure permet à Microsoft de gérer Microsoft 365 à grande échelle et de gérer les risques de menaces internes sur le contenu des clients.

Par défaut, les ingénieurs Microsoft n’ont aucun privilège administratif permanent et aucun accès permanent au contenu client dans Microsoft 365. Un ingénieur Microsoft peut avoir un accès limité, audité et sécurisé au contenu d’un client pendant une durée limitée. L’accès est uniquement nécessaire pour les opérations de service et uniquement lorsqu’il est approuvé par un membre de la direction de Microsoft. Pour les clients titulaires d’une licence Customer Lockbox, le client donne accès à son contenu hébergé sur Microsoft 365.

Microsoft fournit des services en ligne à l’aide de plusieurs formes de distribution cloud :

- **Clouds publics :** Inclut des versions multi-clients de Microsoft 365, Azure et d’autres services hébergés en Amérique du Nord, en Amérique du Sud, en Europe, en Asie, en Australie, etc.
- **Clouds nationaux :** Inclut tous les clouds souverains et tiers gérés en dehors des États-Unis (à l’exception de ceux mentionnés précédemment), tels que Microsoft 365 en Chine (géré par 21Vianet) et Microsoft 365 en Allemagne (géré par Microsoft, mais selon un modèle dans lequel un tiers de confiance allemand, Deutsche Telekom, contrôle et surveille l’accès de Microsoft aux données client et aux systèmes qui contiennent des données client).
- **Clouds pour le gouvernement :** Inclut les services Microsoft 365 et Azure disponibles pour les clients du gouvernement des États-Unis.

Dans le cadre de cet article, les services Microsoft 365 incluent :

- [Exchange Online](/Exchange/exchange-online)
- [Exchange Online Protection](/Office365/SecurityCompliance/eop/exchange-online-protection-overview)
- [SharePoint Online](/sharepoint/sharepoint-online)
- [OneDrive Entreprise](/OneDrive/onedrive)
- [Skype Entreprise](/SkypeForBusiness/skype-for-business-online)
- [Microsoft Teams](/MicrosoftTeams/Teams-overview)
- [Yammer](/yammer/yammer-landing-page)

## <a name="microsoft-365-access-controls"></a>Contrôles d’accès Microsoft 365

À des fins de contrôle d’accès, Microsoft classe les données Microsoft 365 en tant que données client ou d’autres types de données.

### <a name="customer-data"></a>Données client

Les données client sont toutes les données fournies par ou pour le compte d’un client lors de l’utilisation des services Microsoft 365. Ces données sont du contenu client directement créé ou téléchargé par les utilisateurs de Microsoft 365, notamment :

- Messages électroniques
- Contenu SharePoint Online
- Messages instantanés
- Éléments de calendrier
- Documents
- Contacts
- Informations d’identification de l’utilisateur final (EUII) (données qui sont propres à un utilisateur ou qui sont accessibles à un utilisateur individuel, mais qui n’incluent pas de contenu client)

### <a name="other-types-of-data"></a>Autres types de données

Les autres types de données sont les suivants :

- **Données de compte :** Inclut les données administratives (informations fournies par les administrateurs lors de l’inscription ou de l’achat de services) et les données de paiement (informations sur les instrument de paiement, telles que les détails de carte de crédit).
- **Informations d’identification organisationnelle :** Inclut les données utilisées pour identifier un client, les données d’utilisation et non accessibles à un utilisateur individuel ou incluses dans le contenu client.
- **Métadonnées système :** Inclut les journaux de service qui contiennent les paramètres de configuration, l’état du système, les adresses IP Microsoft et des informations techniques sur les abonnements et les clients.

Microsoft a mis en place des mécanismes de contrôle d’accès pour s’assurer que personne n’a un accès non autorisé aux données client ou aux données de contrôle d’accès. Les données de contrôle d’accès gèrent l’accès à d’autres types de données ou de fonctions au sein de l’environnement, y compris l’accès au contenu client ou à l’EUII, aux mots de passe Microsoft, aux certificats de sécurité et à d’autres données relatives à l’authentification. Les mécanismes de contrôle d’accès se prémunir également contre l’accès physique, logique ou distant non autorisé à l’environnement de production Microsoft 365.

Il existe trois catégories de contrôles d’accès utilisées par Microsoft pour l’exploitation de Microsoft 365 :

- Contrôles d’isolation
- Contrôles du personnel
- Contrôles de technologie

Lorsqu’ils sont combinés, ces contrôles permettent de prévenir et de détecter les actions malveillantes dans Microsoft 365. Outre les contrôles d’isolation, de personnel et de technologie utilisés par Microsoft, il existe une quatrième catégorie de contrôles : ces contrôles implémentés par les clients.

Microsoft 365 vous permet de gérer les données de la même façon que dans les environnements locaux. La personne qui signe une organisation pour Microsoft 365 devient automatiquement un administrateur général. L’administrateur global a accès à toutes les fonctionnalités des portails de gestion et peut :

- Créer ou modifier des utilisateurs
- Attribuer des rôles d’administrateur à d’autres personnes
- Réinitialiser les mots de passe des utilisateurs
- Gérer les licences utilisateur
- Gérer les domaines
- Approuver les demandes Customer Lockbox

Il est recommandé que chaque organisation configure au moins deux comptes d’administrateur. Pour les grandes entreprises, nous recommandons des comptes d’administrateur spécialisés qui servent différentes fonctions.

Pour plus d’informations sur l’attribution de rôles d’administrateur et d’autorisations, voir Attribuer des rôles [d’administrateur](/microsoft-365/admin/add-users/assign-admin-roles) et [À propos des rôles d’administrateur.](/microsoft-365/admin/add-users/about-admin-roles)

## <a name="related-links"></a>Liens connexes

- [Isolation dans Microsoft 365](assurance-isolation-in-microsoft-365.md)
- [Filtrage avant l’embauche chez Microsoft Corporation](assurance-pre-employment-screening.md)
- [Vérification des antécédents de Microsoft Cloud](assurance-cloud-background-check.md)
- [Surveillance et audit des contrôles d’accès](assurance-monitoring-and-auditing-access-controls.md)
- [Contrôles d’accès de Yammer Entreprise](assurance-yammer-enterprise-access-controls.md)
