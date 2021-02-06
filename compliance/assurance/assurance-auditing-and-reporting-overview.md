---
title: Audit et rapports dans les services cloud de Microsoft
description: Vue d’ensemble des fonctionnalités d’audit et de rapport dans Office 365, Microsoft 365 et Service Assurance.
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
- M365-analytics
- SPO_Content
- MS-Compliance
f1.keywords:
- NOCSH
ms.custom: seo-marvel-apr2020
titleSuffix: Microsoft Service Assurance
ms.openlocfilehash: 4cb9f68f2c5861905a4246582a3b4530c30988ca
ms.sourcegitcommit: 21ed42335efd37774ff5d17d9586d5546147241a
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 02/05/2021
ms.locfileid: "50120703"
---
# <a name="auditing-and-reporting-in-microsoft-cloud-services"></a>Audit et rapports dans les services cloud de Microsoft

Les services cloud de Microsoft incluent plusieurs fonctionnalités d’audit et de création de rapports que vous pouvez utiliser pour suivre les activités des utilisateurs et des administrations au sein de leur client, des exemples incluent les modifications apportées aux paramètres de configuration des clients Exchange Online et SharePoint Online, ainsi que les modifications apportées par les utilisateurs aux documents et autres éléments. Vous pouvez utiliser les informations d’audit et les rapports disponibles dans les services cloud de Microsoft pour gérer plus efficacement l’expérience utilisateur, atténuer les risques et respecter les obligations de conformité.

## <a name="security--compliance-centers"></a>Centres de conformité & sécurité

Le Centre de sécurité et conformité [Microsoft 365 &,](https://protection.office.com)le Centre de sécurité [Microsoft 365](https://security.microsoft.com)et le Centre de conformité [Microsoft 365](https://compliance.microsoft.com) sont des portails uniques pour la protection des données dans votre organisation. Ils incluent de nombreuses fonctionnalités d’audit et de rapport. Ces centres vous aident à répondre à vos besoins en matière de protection ou de conformité des données, ainsi qu’à auditer l’activité des utilisateurs et des administrateurs. Vous pouvez accéder à ces centres à l’aide de votre compte d’administrateur d’abonnement.

Ces centres incluent des volets de navigation pour accéder à plusieurs fonctionnalités :

- **Alertes :** Permet de gérer les alertes, d’afficher les alertes liées à la sécurité et de gérer les alertes avancées à l’aide [de Cloud App Security.](/cloud-app-security/what-is-cloud-app-security)
- **Autorisations :** Vous permet d’attribuer des [autorisations telles](/microsoft-365/security/office-365-security/grant-access-to-the-security-and-compliance-center) que l’administrateur de conformité, le Gestionnaire eDiscovery et d’autres personnes à des personnes de votre organisation afin qu’elles peuvent effectuer des tâches dans ces centres. Vous attribuez des autorisations pour la plupart des fonctionnalités dans chaque centre, mais d’autres autorisations doivent être configurées à l’aide du Centre d’administration Exchange et du Centre d’administration SharePoint.
- **Gestion des menaces :** Vous permet de créer et d’appliquer des stratégies de gestion des appareils à l’aide de Basic Mobility and Security pour [Microsoft 365,](https://support.microsoft.com/office/overview-of-basic-mobility-and-security-for-microsoft-365-faa7d8e5-645d-4d59-839c-c8d4c1869e4a)de configurer des stratégies de protection contre la perte de données (DLP) pour votre organisation, de configurer le filtrage du courrier électronique, les logiciels anti-programme malveillant, DKIM (DomainKeys Identified Mail), les pièces jointes sécurisées, les liens sécurisés et les applications OAuth. [](/microsoft-365/compliance/data-loss-prevention-policies)
- **Gouvernance des données :** Permet d’importer du courrier électronique ou des données SharePoint à partir d’autres [](/microsoft-365/compliance/retention-policies) systèmes dans [Microsoft 365,](https://support.office.com/article/Import-PST-files-or-SharePoint-data-to-Office-365-ba688e0a-0fcb-4bd7-8e57-2b669564ea84)de configurer des boîtes aux lettres [d’archivage](https://support.office.com/article/Enable-archive-mailboxes-in-the-Office-365-Security-Compliance-Center-268a109e-7843-405b-bb3d-b9393b2342ce)et de définir des stratégies de rétention pour le courrier électronique et d’autres contenus au sein de votre organisation.
- **Recherche et & recherche :** Fournit [](https://support.office.com/article/Run-a-Content-Search-in-the-Office-365-Security-Compliance-Center-61852fd9-fe8a-4880-a339-cb19ed3bff4a)des outils de recherche de contenu, de journal [d’audit,](https://support.office.com/article/Search-the-audit-log-in-the-Office-365-Security-Compliance-Center-0d4d0f35-390b-4518-800e-0c7ec95e946c)de mise en quarantaine et de gestion des cas [eDiscovery](https://support.office.com/article/Manage-eDiscovery-cases-in-the-Office-365-Security-Compliance-Center-edea80d6-20a7-40fb-b8c4-5e8c8395f6da) pour découvrir rapidement l’activité dans les boîtes aux lettres, les groupes et les dossiers publics Exchange Online, SharePoint Online et OneDrive Entreprise.
- **Rapports :** Vous permet d’accéder rapidement aux [rapports](https://support.office.com/article/Reports-in-the-Office-365-Security-Compliance-Center-7acd33ce-1ec8-49fb-b625-43bac7b58c5a) pour SharePoint Online, OneDrive Entreprise, Exchange Online et Azure AD.
- **Assurance de service :** Fournit des informations sur la façon dont Microsoft maintient la sécurité, la confidentialité et la conformité avec les normes globales pour Microsoft 365, Azure, Microsoft Dynamics CRM Online, Microsoft Intune et d’autres services cloud. Inclut également l’accès à des rapports d’audit tiers ISO, SOC et autres, ainsi que des contrôles audités, qui fournissent des détails sur les différents contrôles qui ont été testés et vérifiés par des auditeurs tiers de Microsoft 365.

## <a name="service-assurance"></a>Service Assurance

De nombreuses organisations dans les secteurs réglementés sont soumises à des exigences de conformité étendues. Pour effectuer leurs propres évaluations des risques, les clients ont souvent besoin d’informations détaillées sur la façon dont Microsoft 365 maintient la sécurité et la confidentialité de leurs données. Microsoft s’engage à assurer la sécurité et la confidentialité des données client dans ses services cloud et à gagner la confiance des clients en fournissant une vue transparente de ses opérations et un accès facile aux rapports et évaluations de conformité indépendants.

Service Assurance assure la transparence des opérations et des informations sur la façon dont Microsoft maintient la sécurité, la confidentialité et la conformité des données client dans Microsoft 365. Il inclut des rapports d’audit tiers, ainsi qu’une bibliothèque de livres blancs, de faq et d’autres documents sur microsoft 365, tels que le chiffrement des données, la résilience des données, la gestion des incidents de sécurité, etc. Les clients peuvent utiliser ces informations pour effectuer leurs propres évaluations des risques réglementaires. Les responsables de la mise en conformité peuvent attribuer le rôle « Utilisateur de l’assurance service » pour donner aux utilisateurs l’accès à Service Assurance. L’administrateur client peut également fournir aux utilisateurs externes, tels que des auditeurs indépendants, l’accès aux informations du tableau de bord Service Assurance via le Portail d’confiance des services Cloud [Microsoft](https://aka.ms/STP) (STP).

## <a name="onedrive-for-business-admin-center"></a>Centre d’administration OneDrive Entreprise

Le Centre d’administration Microsoft OneDrive vous permet de gérer rapidement et facilement les paramètres OneDrive Entreprise de votre organisation au même endroit. Pour utiliser le Centre d’administration OneDrive, l’accès à onedrive.com est requis. Vous devez également être un administrateur général de votre organisation ou un administrateur personnalisé avec le rôle d’administrateur SharePoint. Accédez au Centre d’administration OneDrive Entreprise à [https://admin.onedrive.com](https://admin.onedrive.com/) l’adresse .

Les fonctionnalités clés incluent une zone de conformité qui fournit aux administrateurs des liens vers le centre de gestion approprié pour les scénarios clés, tels que la recherche dans le journal d’audit, l’emploi de la DLP, la rétention, la découverte électronique et les alertes.

## <a name="related-links"></a>Liens connexes

- [Fonctionnalités de création de rapports Microsoft 365](assurance-reporting-features.md)
- [Journalisation interne pour Microsoft 365 Engineering](assurance-internal-logging.md)
