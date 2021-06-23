---
title: Exigences de localisation des données personnelles russes
description: Découvrez comment la collecte de données personnelles, l’enregistrement des données personnelles des citoyens russes, la systematisation, l’exploitation, le stockage, la clarification et l’extraction des données personnelles des citoyens russes sont effectuées dans des bases de données et des services Microsoft situées en Russie.
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
ms.openlocfilehash: 1dff74da16ca0a58dd7c11445ee4b435d8737855
ms.sourcegitcommit: fb379d1110a9a86c7f9bab8c484dc3f4b3dfd6f0
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 06/23/2021
ms.locfileid: "53088903"
---
# <a name="russian-personal-data-localization-requirements"></a>Exigences de localisation des données personnelles russes

Depuis le 1er septembre 2015, les organisations considérées comme des opérateurs de données personnelles doivent s’assurer que, lors de la collecte des données personnelles, l’enregistrement, la systematisation, l’utilisation, le stockage, la clarification (mise à jour, modification) et l’extraction des données personnelles des citoyens russes sont effectués via les bases de données situées en Russie (« exigence de localisation des données personnelles »). <sup>1</sup>

les services Microsoft disponibles pour les organisations (y compris, mais sans s’y limiter, les établissements d’enseignement) (appelés « client » ci-dessous), y compris ceux qui permettent le traitement des données personnelles tels que Microsoft Azure, Microsoft 365, Dynamics 365 et Power Platform, sont fournis à partir de centres de traitement de données situés en dehors de la Russie (pour plus d’informations, visitez le Centre de gestion de la gestion de la confiance [Microsoft).](https://www.microsoft.com/trust-center)

En fonction du type et du contenu des informations traitées par les systèmes d’information client, ces systèmes, y compris ceux qui utilisent les produits cloud de Microsoft, peuvent être considérés comme un système d’informations de données personnelles (PDIS, ISPD). Dans les cas où le client souhaite utiliser services Microsoft dans un système éligible en tant que PDIS par le biais de son architecture et des types d’informations traitées, Microsoft invite ses clients à envisager, entre autres choses, les solutions disponibles spécifiées ci-dessous. Tous les scénarios fournis sont disponibles pour les clients en tant qu’option supplémentaire pour les offres commerciales standard.

Notez que c’est le client en tant qu’opérateur de données personnelles de PDIS qui est responsable de la conformité et qui analyse et évalue les exigences légales applicables pour la localisation des données à caractère personnel, et, à sa propre discrétion, détermine de manière indépendante les mesures suffisantes pour s’assurer que le traitement des données à caractère personnel dans PDIS est conforme à la loi russe sur les données personnelles. <sup>2</sup>

## <a name="subscribing-to-microsoft-services"></a>S’abonner à services Microsoft

### <a name="microsoft-id-management"></a>Gestion des ID Microsoft

Microsoft invite les clients à envisager de s’abonner à services Microsoft; Microsoft Azure, Microsoft 365, Dynamics 365 et Power Platform, via un partenaire Fournisseur de solutions Microsoft Cloud (CSP). Pour plus d’informations, consultez la liste des partenaires du programme [CSP.](https://pinpoint.microsoft.com/search?type=services&campaign=691)

### <a name="managing-user-identity-and-access-for-microsoft-services"></a>Gestion de l’identité utilisateur et de l’accès services Microsoft

Pour services Microsoft telles que Microsoft Azure, Microsoft 365, Dynamics 365 et Power Platform, la vérification des utilisateurs et la gestion des accès sont effectuées via Azure Active Directory [(Azure Active Directory).](https://azure.microsoft.com/services/active-directory/) Dans les cas où un client Microsoft utilise un système de gestion de l’identification local pour les services cloud de Microsoft (par exemple, Windows Server Active Directory (AD) ou tout autre système de gestion des ID), le client a la possibilité d’intégrer rapidement ce système au Azure Active Directory (Azure Active Directory) via Azure AD Connecter. Pour plus d’informations, voir la Connecter Azure [AD.](/azure/active-directory/cloud-provisioning/) Les clients Microsoft peuvent également envisager d’utiliser des applications et des solutions de fournisseurs tiers pour gérer leurs utilisateurs et intégrer leur système d’identification local à Azure AD.

## <a name="use-microsoft-compliance-manager-to-assess-your-risk"></a>Utilisez le Gestionnaire de Conformité Microsoft pour évaluer vos risques

[Le Gestionnaire de Conformité Microsoft](/microsoft-365/compliance/compliance-manager) est une fonctionnalité dans le [centre de conformité Microsoft 365](/microsoft-365/compliance/microsoft-365-compliance-center) pour vous aider à comprendre la position de la conformité de votre organisation et à prendre des mesures pour réduire les risques. Le Gestionnaire de Conformité offre un modèle Premium pour la création d’une évaluation de ce règlement. Recherchez le modèle sur la page **modèles d’évaluation** dans le Gestionnaire de Conformité. Découvrez comment [créer des évaluations dans le Gestionnaire de Conformité](/microsoft-365/compliance/compliance-manager-assessments).

## <a name="questions-and-support"></a>Questions et support

Pour des questions techniques et de facturation, reportez-vous aux ressources du support Microsoft ci-dessous. Pour des questions ou des clarifications supplémentaires, contactez l’équipe de [confidentialité](https://support.microsoft.com/gp/privacy-page)de Microsoft.

### <a name="microsoft-azure"></a>Microsoft Azure

- **Site web**: [Microsoft Azure prise en charge](https://aka.ms/GetAzureSupport)
- **Numéro gratuit**: 8 800 200 8001
- **Appel local**: 495 916 7171
- **Support en ligne**: soumettre des requêtes via le [portail Azure](https://portal.azure.com)

### <a name="microsoft-365"></a>Microsoft 365

- **Numéro gratuit**: 8 10 800 2548 1044
- **Appel local**: 499 922 8623
- **Support en ligne**: envoyer des requêtes via le [Centre d’administration](https://portal.office.com/)

### <a name="dynamics-365"></a>Dynamics 365

- **Numéro gratuit**: 8 10 800 2548 1044
- **Appel local**: 499 922 8623
- **Support en ligne**: envoyer des requêtes via le [portail de support Dynamics](https://dynamics.microsoft.com/support/)

### <a name="power-platform"></a>Plateforme d’alimentation

- **Numéro gratuit**: 8 10 800 2548 1044
- **Appel local**: 499 922 8623
- **Support en ligne**: soumettre des requêtes via le support [de plateforme Power Platform](/power-platform/admin/get-help-support)

> [!NOTE]
> <sup>1</sup> Loi fédérale n. 242-FZ (édition 12.31.2014) « Lors de l’entrée de modifications dans certains actes juridiques de la Fédération de Russie concernant la clarification de la procédure de traitement des données personnelles dans les réseaux d’information et de télécommunications » date 07.21.2014 <br>
> <sup>2</sup> Loi fédérale n. 152-FZ sur les données personnelles à partir du 07.27. 2006<br>
