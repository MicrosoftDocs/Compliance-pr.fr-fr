---
title: Fonctionnalités de rapport Microsoft 365
description: Découvrez les différentes fonctionnalités de création de rapports dans Microsoft 365, notamment Azure Active Directory et Exchange Online.
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
- M365-analytics
f1.keywords:
- NOCSH
ms.custom: seo-marvel-apr2020
titleSuffix: Microsoft Service Assurance
ms.openlocfilehash: a745c470dc30703f438258985169431c1053e65d
ms.sourcegitcommit: 21ed42335efd37774ff5d17d9586d5546147241a
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 02/05/2021
ms.locfileid: "50120783"
---
# <a name="microsoft-365-reporting-features"></a>Fonctionnalités de rapport Microsoft 365

Les fonctionnalités de création de rapports dans Microsoft 365 fournissent différents rapports d’audit pour Azure Active Directory (Azure AD), Exchange Online, la gestion des appareils, la vérification de surveillance et la protection contre la perte de données (DLP). Ces rapports sont différents et distincts des rapports d’activité Microsoft 365.

## <a name="microsoft-365-reports-dashboard"></a>Tableau de bord rapports Microsoft 365

Le tableau de bord Rapports de la prévisualisation du Centre d’administration Microsoft 365 affiche l’activité d’utilisation dans Microsoft 365. Les administrateurs globaux Microsoft 365, ou un administrateur Exchange Online, SharePoint Online ou Skype Entreprise, peuvent obtenir des informations granulaires sur l’utilisation de ce service. Par exemple, le nombre d’utilisateurs dans un service Microsoft 365 particulier, le nombre d’utilisateurs qui ont activé Microsoft 365 Apps pour entreprise (précédemment nommé Office 365 ProPlus) et la quantité de courrier qui circule dans l’organisation. Les rapports sont disponibles pour les 7, 30, 90 et 180 derniers jours.

Les rapports suivants sont disponibles :

- [Rapport d’activité de messagerie](https://support.office.com/article/Office-365-Reports-in-the-admin-center-preview--Email-activity-1cbe2c00-ca65-4fb9-9663-1bbfa58ebe44)
- [rapport Microsoft Office activations de la clé](https://support.office.com/article/Office-365-Reports-in-the-admin-center-preview--Microsoft-Office-activations-87c24ae2-82e0-4d1e-be01-c3bcc3f18c60)
- [Rapport d’utilisation du site SharePoint Online](https://support.office.com/article/Office-365-Reports-in-the-admin-center-preview--SharePoint-site-usage-4ecfb843-e5d5-464d-8bf6-7ed512a9b213)
- [Rapport d’utilisation de OneDrive Entreprise](https://support.office.com/article/Office-365-Reports-in-the-Admin-Center-Preview--OneDrive-for-Business-usage-0de3b312-c4e8-4e4b-a02d-32b2f726a680)
- [Rapport d’activité Yammer](https://support.office.com/article/View-the-Yammer-Activity-report-in-the-Office-365-admin-center-preview-c7c9f938-5b8e-4d52-b1a2-c7c32cb2312a)
- [Rapport d’activité Skype Entreprise](/SkypeForBusiness/skype-for-business-online-reporting/activity-report)
- [Rapport d’activité P2D Skype Entreprise](/SkypeForBusiness/skype-for-business-online-reporting/peer-to-peer-activity-report)
- [Rapport sur l’organisateur de conférences Skype Entreprise](/SkypeForBusiness/skype-for-business-online-reporting/conference-organizer-activity-report)
- [Rapport d’activité des participants aux conférences Skype Entreprise](/SkypeForBusiness/skype-for-business-online-reporting/conference-participant-activity-report)

Pour plus d’informations, voir Rapports d’activité dans le [Centre d’administration Microsoft 365.](https://support.office.com/article/activity-reports-in-the-office-365-admin-center-0d6dfb17-8582-4172-a9a9-aed798150263)

## <a name="azure-ad-reports"></a>Rapports Azure AD

Microsoft 365 utilise Azure AD pour l’authentification et la gestion des identités. Les administrateurs Microsoft 365 utilisent des rapports générés par Azure pour identifier les activités inhabituelles et l’accès non autorisé à leurs données. Vous pouvez utiliser les rapports d’accès et d’utilisation dans Azure AD pour obtenir une visibilité sur l’intégrité et la sécurité de l’annuaire pour votre organisation. Grâce à ces informations, vous pouvez identifier et atténuer les risques de sécurité possibles.

Les rapports Azure AD peuvent être exportés vers Microsoft Excel et corrélés avec d’autres données de Microsoft 365. Par exemple, les résultats d’une recherche dans le journal d’audit peuvent fournir des informations sur l’accès, l’authentification et les activités au niveau de l’application. Des rapports d’utilisation avancée des anomalies et des ressources sont disponibles avec Azure AD Premium. Ces rapports avancés vous aident à améliorer votre posture de sécurité et à répondre aux menaces potentielles en appliquant des analyses sur l’accès aux appareils et l’utilisation des applications. Pour plus d’informations, [voir rapports Azure Active Directory.](/azure/active-directory/reports-monitoring/overview-reports/)

## <a name="exchange-online-audit-reports"></a>Rapports d’audit Exchange Online

Les rapports d’audit Exchange Online incluent des détails sur l’accès aux boîtes aux lettres et les modifications apportées par les administrateurs à votre client Exchange Online. Avec l’audit de boîte aux lettres, vous pouvez utiliser les tâches du tableau suivant pour exécuter des rapports et exporter des journaux d’audit Exchange Online.

> [!NOTE]
> Vous devez activer l’enregistrement d’audit de boîte aux lettres pour chaque boîte aux lettres afin que les événements audités soient enregistrés dans le journal d’audit de cette boîte aux lettres. Si l’enregistrement d’audit de boîte aux lettres n’est pas activé pour une boîte aux lettres, les événements de cette boîte aux lettres ne sont pas enregistrés dans le journal d’audit et n’apparaissent pas dans les rapports d’audit de boîte aux lettres. Pour plus d’informations, voir [activer l’audit de boîte aux lettres.](https://support.office.com/article/Enable-mailbox-auditing-in-Office-365-aaca8987-5b62-458b-9882-c28476a66918)

| Tâche | Description |
|----------------------------------------------|----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [Exécuter un rapport d’accès aux boîtes aux lettres par des non-propriétaires](/exchange/security-and-compliance/exchange-auditing-reports/non-owner-mailbox-access-report) | Affiche la liste des boîtes aux lettres accessibles par une personne autre que le propriétaire de la boîte aux lettres. Le rapport contient des informations sur les personnes ayant accédé à la boîte aux lettres, les actions qu’elles ont prises dans la boîte aux lettres et si les actions ont réussi. |
| [Exporter les journaux d’audit de boîte aux lettres](/exchange/security-and-compliance/exchange-auditing-reports/export-mailbox-audit-logs) | Les journaux d’audit de boîte aux lettres contiennent des informations sur l’accès et les actions dans une boîte aux lettres prise par un utilisateur autre que le propriétaire de la boîte aux lettres. Les administrateurs peuvent spécifier des boîtes aux lettres avec une plage de dates pour générer des rapports. Les journaux sont exportés en XML, joints à un message et envoyés à des utilisateurs spécifiques, comme déterminé par l’administrateur. |
| [Exécuter un rapport de groupe de rôles d'administrateur](/Office365/SecurityCompliance/eop/run-an-administrator-role-group-report-in-eop-eop) | Le groupe de rôles d’administrateur attribue des privilèges d’administration aux utilisateurs. Ces privilèges permettent aux utilisateurs d’effectuer des tâches administratives telles que la réinitialisation des mots de passe, la création ou la modification de boîtes aux lettres et l’attribution de privilèges d’administrateur à d’autres utilisateurs. Le rapport de groupe de rôles d’administrateur affiche les modifications apportées aux groupes de rôles, notamment l’ajout ou la suppression de membres. |
| [Afficher le journal d’audit de l’administrateur](/exchange/security-and-compliance/exchange-auditing-reports/view-administrator-audit-log) | Le rapport du journal d’audit de l’administrateur répertorie toutes les fonctions de création, de mise à jour et de suppression effectuées par les administrateurs dans Exchange Online. Les entrées de journal fournissent des informations sur la cmdlet qui a été exécuté, les paramètres utilisés, l’ayant exécuté et les objets affectés. |
| [Recherche et attente de contenu de boîte aux lettres](/exchange/security-and-compliance/in-place-ediscovery/in-place-ediscovery) | Fournit des détails sur les modifications apportées aux paramètres In-Place eDiscovery ou In-Place de la boîte aux lettres. |
| [Exporter le journal d’audit de l’administrateur](/exchange/security-and-compliance/exchange-auditing-reports/search-role-group-changes) | Le journal d’audit de l’administrateur enregistre des actions administratives spécifiques telles que créer, mettre à jour et supprimer dans Exchange Online. Les résultats du journal sont exportés au XML et les administrateurs peuvent choisir d’envoyer ce journal à un ensemble d’utilisateurs. |
| [Exécuter un rapport de conservation pour litige par boîte aux lettres](/exchange/security-and-compliance/exchange-auditing-reports/per-mailbox-litigation-hold-report) | Fournit des détails sur les modifications apportées aux paramètres de mise en attente pour litige sur les boîtes aux lettres. |
| [Afficher et exporter le journal d’audit de l’administrateur externe](/exchange/security-and-compliance/exchange-auditing-reports/view-external-admin-audit-log) | Contient les détails des actions effectuées par les administrateurs externes. Les entrées fournissent des informations sur la cmdlet qui a été exécuté, les paramètres utilisés et toutes les actions qui créent, modifient ou suppriment des objets dans Exchange Online. |

## <a name="device-compliance-reports"></a>Rapports de conformité des appareils

Vous gérez et sécurisationz les appareils mobiles connectés à votre abonnement à l’aide de Basic Mobility and Security pour Microsoft 365. Les appareils mobiles utilisés pour accéder à la messagerie électronique, au calendrier, aux contacts et aux documents professionnels jouent un rôle important dans la façon de s’assurer que les employés peuvent travailler à tout moment et en tout lieu. Il est essentiel de protéger les informations de votre organisation. Vous utilisez Basic Mobility and Security pour Microsoft 365 pour définir des stratégies de sécurité des appareils et des règles d’accès. En cas de perte ou de vol, vous utilisez également Basic Mobility and Security pour Microsoft 365 pour effacer les appareils mobiles.

Les rapports de conformité de sécurité et de mobilité de base fournissent une vue d’ensemble des stratégies définies par une organisation pour sécuriser les appareils mobiles qui accèdent aux données Microsoft 365. Le rapport permet le filtrage des appareils par état de conformité, violations signalées, appareils bloqués et nombre d’appareils effacés suite aux stratégies de sécurité. Pour plus d’informations, voir [Vue d’ensemble de la mobilité et de la sécurité de base pour Microsoft 365.](https://support.microsoft.com/office/overview-of-basic-mobility-and-security-for-microsoft-365-faa7d8e5-645d-4d59-839c-c8d4c1869e4a)

## <a name="data-loss-prevention"></a>Protection contre la perte de données

Les stratégies DLP permettent de gérer la sécurité et le flux des informations dans une organisation. Vous pouvez configurer des stratégies pour bloquer l’accès au contenu, chiffrer des données ou informer les utilisateurs des violations de stratégie et de stratégie à l’aide de conseils de stratégie DLP dans l’application. Les rapports DLP fournissent un aperçu du nombre de correspondances de stratégie et de règle, de remplacements et de faux positifs.

Vous utilisez le Centre d’administration Microsoft 365 pour afficher des informations sur le nombre de messages détectés par vos stratégies DLP. Les rapports DLP fournissent des informations sur les correspondances de stratégie et de règle pour les messages envoyés et reçus. Vous pouvez également afficher le nombre de correspondances, de remplacements et de faux positifs pour chaque stratégie au cours des dernières 24 heures à l’aide du Centre d’administration Exchange. Si vous téléchargez un rapport Excel, vous pouvez afficher encore plus de détails, tels que la personne qui a envoyé le message, le jour où il a été envoyé et les correspondances de stratégie déclenchées. Pour plus d’informations, voir [Afficher les rapports sur les détections de stratégies DLP.](/previous-versions/exchange-server/exchange-150/jj889415(v=exchg.150))

## <a name="auditing-in-yammer-enterprise"></a>Audit dans Yammer Entreprise

Yammer Entreprise permet aux administrateurs d’exporter des données d’activité utilisateur à partir de leur réseau Yammer via [l’API](https://support.office.com/article/export-data-from-yammer-enterprise-b303d8f3-007d-4ad4-81f8-54fb1ecfb3f2)d’exportation de données Yammer ou manuellement via la page d’administration Yammer réseau. La possibilité d’exporter des journaux est limitée aux administrateurs réseau dans Yammer. (Tous les administrateurs globaux Microsoft 365 sont Yammer administrateurs réseau.)

Les données suivantes peuvent être exportées :

| Filename | Description |
|----------------------------|-------------------------------------------------------------------------|
| Utilisateurs.csv | Tous les nouveaux utilisateurs, en attente et suspendus dans le réseau |
| Messages.csv | Tous les messages du réseau |
| Files.csv (métadonnées) | Métadonnées telles que le nom de fichier, l’URL de l’API de fichier, l’ID du téléchargeur, téléchargée sur, etc. |
| Files.csv (fichiers d’origine) | Fichier zip des fichiers d’origine chargés par les utilisateurs dans Yammer |
| Topics.csv | Rubriques créées sur le réseau |
| Pages.csv | Pages (notes) créées par les utilisateurs du réseau |
| Admins.csv | Tous les administrateurs vérifiés sur le réseau |
| Networks.csv | Tous les Yammer externes |

Yammer Données d’entreprise sont également disponibles via les rapports d’activité Microsoft 365. En outre, Yammer travaille activement sur l’exposition de la journalisation supplémentaire via l’API Activité de gestion Microsoft 365 et sur la possibilité de raisonner les données à l’aide de Power BI. Pour plus [d’informations](https://fasttrack.microsoft.com/roadmap?filters=yammer) sur ces fonctionnalités, voir la feuille de route Office.
