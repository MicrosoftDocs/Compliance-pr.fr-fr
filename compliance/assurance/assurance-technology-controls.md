---
title: Contrôles technologiques dans Microsoft 365
description: Cet article fournit une vue d’ensemble des outils et technologies utilisés par Microsoft pour le contrôle des technologies dans Microsoft 365.
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
ms.custom:
- seo-marvel-apr2020
titleSuffix: Microsoft Service Assurance
ms.openlocfilehash: c3b443505c78832af47719e6840c8b7011f9dfe1
ms.sourcegitcommit: 2b347c9b778ac9b6450daf20fdf8eb74ed14cbbd
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 03/23/2021
ms.locfileid: "51002164"
---
# <a name="technology-controls-in-microsoft-365"></a>Contrôles technologiques dans Microsoft 365 

Microsoft utilise plusieurs outils et technologies pour contrôler, gérer et auditer l’accès aux données client dans ses services en ligne. Ceux-ci s’appliquent à Exchange Online, SharePoint Online, Lockbox et Customer Lockbox, l’authentification multifacteur, etc. Yammer utilise des contrôles similaires décrits dans [Yammer contrôles d’accès d’entreprise.](assurance-yammer-enterprise-access-controls.md)

Les ingénieurs Microsoft 365 n’ont aucun accès permanent aux données client microsoft 365. Les ingénieurs doivent passer par un processus d’approbation Microsoft avant d’accéder aux données client pour les opérations de service. Si le client licence la fonctionnalité Customer Lockbox pour Exchange Online et SharePoint Online, l’accès aux données client nécessite l’approbation du client. Une fois approuvés, les comptes d’administration spécifiques au service sont provisionés pour l’accès juste-à-temps pour les tâches requises par la demande de service.

## <a name="lockbox-and-customer-lockbox"></a>Lockbox et Customer Lockbox

Bien que cela soit rare, un client peut demander de l’aide de Microsoft qui expose du contenu client à un ingénieur Microsoft. Pour contrôler l’accès à Exchange Online, Microsoft utilise un système de contrôle d’accès appelé Lockbox. Avant qu’un ingénieur Microsoft accède à des systèmes ou données Exchange Online ou SharePoint Online, il doit envoyer une demande d’accès à l’aide de Lockbox. Toutes les demandes de service pour Exchange Online et SharePoint Online sont gérées par le système Lockbox. Avec Lockbox et Customer Lockbox, tous les accès approuvés sont accessibles à un utilisateur unique, ce qui rend les ingénieurs responsables de leur gestion des données client.

> [!NOTE]
> Exchange Online inclut toutes les données Skype Entreprise stockées dans les boîtes aux lettres des utilisateurs. La couverture Skype Entreprise n’inclut pas les enregistrements de diffusion de réunion Skype ou le contenu téléchargé vers les réunions par les utilisateurs. SharePoint Online inclut OneDrive Entreprise.

Lockbox traite les demandes d’autorisations qui accordent aux ingénieurs la possibilité d’effectuer des fonctions opérationnelles et administratives au sein du service. Les ingénieurs envoient des demandes via Lockbox et un responsable Microsoft doit approuver la demande avant que l’ingénieur puisse accéder aux données client. Après l’approbation du responsable, l’ingénieur dispose d’un accès limité au temps et à l’étendue aux données client pour travailler sur le problème du client.

Customer Lockbox pour Microsoft 365 vous aide à respecter les obligations de conformité si vous avez besoin de procédures en place pour l’autorisation d’accès aux données explicite. Il s’agit d’une condition requise pour certaines normes de conformité, telles que FedRAMP et HIPAA. Customer Lockbox vous insère dans le processus d’approbation lockbox et vous permet de contrôler l’autorisation d’accès de Microsoft à votre contenu Exchange Online ou SharePoint Online pour les opérations de service.

Dans les rares cas où un ingénieur de service Microsoft a besoin d’accéder à vos données, vous n’accordez l’accès qu’aux données requises pour résoudre le problème et pour une durée limitée. Si vous rejetez une demande d’accès, les ingénieurs Microsoft n’ont pas accès à votre contenu et ne pourront pas effectuer les opérations de service. Si vous approuvez la demande, les ingénieurs Microsoft disposent d’un accès limité juste-à-temps à votre contenu par le biais d’interfaces de gestion contrôlées et limitées.

Les actions entreprises par l’ingénieur du support technique sont enregistrées à des fins d’audit et sont accessibles via l’API Activité de gestion [Office 365](/office/office-365-management-api/get-started-with-office-365-management-apis) et le Centre de sécurité [et conformité.](https://protection.office.com/)

>[!NOTE]
> Customer Lockbox est disponible dans [Microsoft 365 E5](https://products.office.com/business/office-365-enterprise-e5-business-software) en tant qu’achat de modules. Pour plus d’informations, voir Demandes d’accès au Customer Lockbox de [Microsoft 365.](https://support.office.com/article/Office-365-Customer-Lockbox-Requests-36f9cdd1-e64c-421b-a7e4-4a54d16440a2)

## <a name="just-in-time-access"></a>Accès juste-à-temps

Microsoft utilise le principe d’accès juste-à-temps (JIT) pour Microsoft 365 pour atténuer les risques de falsification des informations d’identification et les attaques latérales. JIT supprime l’accès administratif persistant aux services et remplace les droits par la possibilité d’accéder à ces rôles à la demande. La suppression des droits d’accès persistants des administrateurs garantit que les informations d’identification sont disponibles uniquement lorsqu’elles sont nécessaires et réduit les risques de vol d’informations d’identification.

Le modèle d’accès JIT exige que les ingénieurs demandent des privilèges élevés pendant une période limitée pour effectuer des tâches administratives. En outre, les ingénieurs utilisent des comptes temporaires créés avec des mots de passe complexes générés par l’ordinateur et n’ont accordé que les rôles qui leur permettent d’effectuer les tâches nécessaires. Par exemple, l’accès administratif accordé par Lockbox est limité dans le temps et le temps accordé dépend du rôle demandé. Un ingénieur spécifie la durée d’accès au temps nécessaire dans la demande au système Lockbox. Le système Lockbox rejette les demandes lorsque le temps demandé dépasse la durée maximale autorisée pour l’élévation. Après expiration, l’accès administratif est supprimé et le compte temporaire expire.

Lorsqu’ils sont autorisés et approuvés pour l’accès, les ingénieurs reçoivent un mot de passe administratif d’utilisation unique généré par le système d’autorisation. De nouveaux mots de passe sont générés chaque fois qu’une demande d’accès élevé est approuvée. Le mot de passe est copié dans un mot de passe sécurisé, est distinct des informations d’identification de l’ingénieur pour l’environnement d’entreprise Microsoft et s’utilise uniquement pour la session d’accès élevé approuvée.

## <a name="constrained-management-interfaces"></a>Interfaces de gestion contraintes

Les ingénieurs utilisent deux interfaces de gestion pour effectuer des tâches administratives : Bureau à distance via des passerelles de service Terminal Service sécurisées (TSG) et Remote PowerShell. Dans ces interfaces de gestion, les stratégies logicielles et les contrôles d’accès imposent des restrictions importantes quant aux applications exécutées et aux commandes et cmdlets disponibles.

Les serveurs Microsoft 365 limitent les sessions simultanées à une seule session par administrateur d’équipe de service, par serveur. Les TSG n’autorisent qu’une seule session simultanée pour les utilisateurs et n’autorisent pas plusieurs sessions. À l’aide d’une seule session par serveur, les TSG permettent aux administrateurs d’équipes de service Microsoft 365 de se connecter simultanément à plusieurs serveurs afin que les administrateurs peuvent effectuer efficacement leurs tâches. Les administrateurs d’équipe de service n’ont pas d’autorisations sur les TSG eux-mêmes. Le TSG est utilisé uniquement pour appliquer l’authentification multifacteur (MFA) et les exigences de chiffrement. Une fois que l’administrateur de l’équipe de service se connecte à un serveur spécifique via un TSG, le serveur spécifique applique une limite de session d’un par administrateur.

Les restrictions d’utilisation et les exigences de connexion et de configuration pour le personnel Microsoft 365 sont établies par les stratégies de groupe Active Directory. Ces stratégies incluent les caractéristiques suivantes :

- Les TSG utilisent uniquement le chiffrement [VALIDÉ FIPS](https://www.microsoft.com/TrustCenter/Compliance/FIPS) 140-2.
- Les sessions TSG se déconnectent après 30 minutes d’inactivité.
- Les sessions TSG se déconnectent automatiquement après 24 heures.

Les connexions aux TSG nécessitent également l’utilisation d’une carte à puce physique distincte et d’un compte distinct des informations d’identification de l’entreprise Microsoft de l’ingénieur. Différentes cartes à puce sont émises pour les différentes plateformes et plateformes de gestion des secrets, ce qui garantit un stockage sécurisé des informations d’identification. Les groupes de sécurité sociale utilisent des stratégies de groupe Active Directory pour contrôler qui peut se connecter aux serveurs distants, le nombre de sessions autorisées et les paramètres de délai d’inactivité. Des stratégies supplémentaires limitent l’accès aux applications autorisées et limitent l’accès à Internet.

En plus de l’accès à distance à l’aide de groupes de sécurité TSG spécialement configurés, Exchange Online permet aux utilisateurs ayant le rôle Service Engineer Operations d’accéder à certaines fonctionnalités d’administration sur les serveurs de production à l’aide de Remote PowerShell. Pour ce faire, l’utilisateur doit être autorisé à accéder en lecture seule (débogage) à l’environnement de production Microsoft 365. L’escalade de privilège est activée de la même manière que pour les TSG à l’aide du processus Lockbox.

Pour l’accès à distance, chaque centre de données dispose d’une adresse IP virtuelle à charge équilibrée qui sert de point d’accès unique. Les cmdlets Remote PowerShell disponibles sont basées sur le niveau de privilège identifié dans la revendication d’accès obtenue lors de l’authentification. Ces cmdlets offrent la seule fonctionnalité d’administration accessible par les utilisateurs qui se connectent à l’aide de cette méthode. PowerShell à distance limite l’étendue des commandes disponibles pour l’ingénieur et est basé sur le niveau d’accès accordé via le processus Lockbox. Par exemple, dans Exchange Online, Get-Mailbox peut être disponible, mais Set-Mailbox ne le ferait pas.
