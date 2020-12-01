---
title: Exigences en russe de localisation des données personnelles
description: Découvrez comment la collecte de données personnelles, l’enregistrement des données personnelles des citoyens russes, l’Systematization, l’accumulation, le stockage, la clarification et l’extraction sont effectués dans des services et bases de données Microsoft situés en Russie.
keywords: Offres pour la conformité Microsoft 365
localization_priority: None
ms.prod: microsoft-365-enterprise
ms.topic: article
f1.keywords:
- NOCSH
ms.author: robmazz
author: robmazz
manager: laurawi
audience: itpro
ms.collection:
- M365-security-compliance
- MS-Compliance
hideEdit: true
titleSuffix: Microsoft Compliance
ms.openlocfilehash: 07dbfce49dc202ed23a4f2fed6336e00dcec95e1
ms.sourcegitcommit: 626b0076d133e588cd28598c149a7f272fc18bae
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 11/30/2020
ms.locfileid: "49507482"
---
# <a name="russian-personal-data-localization-requirements"></a>Exigences en russe de localisation des données personnelles

Depuis le 1er septembre 2015, les organisations qui sont considérées comme des opérateurs de données personnelles doivent s’assurer que lors de la collecte de données personnelles, l’enregistrement des données personnelles des citoyens russes, l’Systematization, l’accumulation, le stockage, la clarification (mise à jour, modification) et l’extraction sont effectués via les bases de données situées en Russie (« exigences de localisation des données personnelles » <sup>1</sup>

Les services Microsoft accessibles aux organisations (y compris mais sans s’y limiter) (ci-après dénommés « client »), y compris ceux permettant le traitement des données personnelles comme Microsoft Azure, Microsoft 365, Dynamics 365 et Power Platform, sont fournis par des centres de traitement de données situés en dehors de Russie (pour plus d’informations, consultez le centre de gestion de la [confidentialité Microsoft](https://www.microsoft.com/trust-center))

Selon le type et le contenu des informations traitées par les systèmes d’information client, ces systèmes, y compris ceux qui utilisent les produits Cloud de Microsoft, peuvent être considérés comme des systèmes d’information sur les données personnelles (« PDIS », « ISPD »). Dans les cas où le client souhaite utiliser les services Microsoft dans un système qui qualifie comme PDIS par le biais de son architecture et des types d’informations traitées, Microsoft invite ses clients à prendre en compte, entre autres choses, les solutions disponibles indiquées ci-dessous. Tous les scénarios fournis sont disponibles pour les clients en tant qu’option supplémentaire pour les offres commerciales standard.

Il convient de noter qu’il s’agit du client en tant qu’opérateur de données personnelles de PDIS responsable de la conformité et qu’il analyse et évalue les exigences juridiques applicables en matière de localisation de données personnelles, et à sa discrétion, détermine indépendamment les mesures suffisantes pour s’assurer que le traitement des données personnelles dans PDIS est conforme à la loi russe sur les données personnelles. <sup>2</sup>

## <a name="subscribing-to-microsoft-services"></a>Abonnement aux services Microsoft

### <a name="microsoft-id-management"></a>Gestion des ID Microsoft

Microsoft invite les clients à envisager de s’abonner aux services Microsoft ; Microsoft Azure, Microsoft 365, Dynamics 365 et Power Platform, via un partenaire de fournisseur de solutions Cloud Microsoft. Pour plus d’informations, reportez-vous à la [liste des partenaires CSP](https://pinpoint.microsoft.com/search?type=services&campaign=691).

### <a name="managing-user-identity-and-access-for-microsoft-services"></a>Gestion de l’identité et de l’accès des utilisateurs pour les services Microsoft

Pour les services Microsoft, tels que Microsoft Azure, Microsoft 365, Dynamics 365 et Power Platform, la gestion des utilisateurs et la vérification de l’accès sont effectuées via [Azure Active Directory (Azure Active Directory)](https://azure.microsoft.com/services/active-directory/). Dans les cas où un client Microsoft utilise un système de gestion des identifications local pour les services de Cloud Computing Microsoft (par exemple, Windows Server Active Directory (AD) ou tout autre système de gestion des ID), le client a la possibilité d’intégrer rapidement ce système à Azure Active Directory (Azure Active Directory) via Azure AD Connect. Pour plus d’informations, reportez-vous à [Azure ad Connect](https://docs.microsoft.com/azure/active-directory/cloud-provisioning/). Les clients Microsoft peuvent également envisager d’utiliser des applications et des solutions de fournisseurs tiers pour gérer leurs utilisateurs et intégrer leur système d’identification local avec Azure AD.

## <a name="use-microsoft-compliance-manager-to-assess-your-risk"></a>Utilisez le Gestionnaire de conformité Microsoft pour évaluer vos risques

Le [Gestionnaire de conformité Microsoft](https://docs.microsoft.com/microsoft-365/compliance/compliance-manager) est une fonctionnalité du [Centre de conformité Microsoft 365](https://docs.microsoft.com/microsoft-365/compliance/microsoft-365-compliance-center) qui vous permet de comprendre l’état de conformité de votre organisation et de prendre des mesures pour réduire les risques. Le Gestionnaire de conformité propose un modèle premium pour créer une évaluation pour ce règlement. Recherchez le modèle dans la page des **modèles d’évaluation** dans le Gestionnaire de conformité. Découvrez comment [créer des évaluations dans le Gestionnaire de conformité](https://docs.microsoft.com/microsoft-365/compliance/compliance-manager-assessments).

## <a name="questions-and-support"></a>Questions et assistance

Pour des questions techniques et de facturation, reportez-vous aux ressources de support Microsoft ci-dessous. Pour plus d’informations ou de clarifications, contactez l' [équipe de confidentialité](https://support.microsoft.com/gp/privacy-page)de Microsoft.

### <a name="microsoft-azure"></a>Microsoft Azure

- **Site Web**: [prise en charge de Microsoft Azure](https://aka.ms/GetAzureSupport)
- **Numéro** gratuit : 8 800 200 8001
- **Appel local**: 495 916 7171
- **Support en ligne**: soumettre des requêtes via le [portail Azure](https://portal.azure.com)

### <a name="microsoft-365"></a>Microsoft 365

- **Numéro** gratuit : 8 10 800 2548 1044
- **Appel local**: 499 922 8623
- **Support en ligne**: soumettre des requêtes via le [Centre d’administration](https://portal.office.com/)

### <a name="dynamics-365"></a>Dynamics 365

- **Numéro** gratuit : 8 10 800 2548 1044
- **Appel local**: 499 922 8623
- **Support en ligne**: soumettre des requêtes via le [portail de prise en charge Dynamics](https://dynamics.microsoft.com/support/)

### <a name="power-platform"></a>Power Platform

- **Numéro** gratuit : 8 10 800 2548 1044
- **Appel local**: 499 922 8623
- **Support en ligne**: soumettre des requêtes via la [prise en charge de Power Platform](https://docs.microsoft.com/power-platform/admin/get-help-support)

> [!NOTE]
> <sup>1</sup> numéro de loi fédérale. 242-FZ (12.31.2014 version datée)» concernant la saisie de modifications apportées à certains actes législatifs de la Fédération de Russie concernant la clarification de la procédure de traitement des données personnelles dans les réseaux d’information et de télécommunications (07.21.2014) <br>
> <sup>2</sup> n ° de loi fédérale 152-FZ sur les données personnelles à 07,27. 2006<br>
