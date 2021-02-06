---
title: Demandes des personnes concernées pour le RGPD et le CCPA
keywords: Microsoft 365, Microsoft 365 Éducation, documentation Microsoft 365, RGPD, CCPA
localization_priority: Priority
ms.prod: microsoft-365-enterprise
ms.topic: article
f1.keywords:
- NOCSH
ms.author: robmazz
author: robmazz
manager: laurawi
audience: itpro
ms.collection:
- GDPR
- M365-security-compliance
- MS-Compliance
titleSuffix: Microsoft GDPR
description: Découvrez comment effectuer des demandes de la personne concernée (DPC) dans le cadre des règlements généraux sur la protection des données (GPDR) et le California Consumer Privacy Act (CCPA) à l’aide de produits et services Microsoft.
ms.custom: seo-marvel-mar2020
ms.openlocfilehash: 83ba52015eeb7aed73cd231ff01f824f75337360
ms.sourcegitcommit: 21ed42335efd37774ff5d17d9586d5546147241a
ms.translationtype: HT
ms.contentlocale: fr-FR
ms.lasthandoff: 02/05/2021
ms.locfileid: "50121033"
---
# <a name="data-subject-requests-and-the-gdpr-and-ccpa"></a>Demandes des personnes concernées et le RGPD et CCPA

Le règlement général sur la protection des données (RGPD) présente de nouvelles règles pour les organisations qui offrent des produits et des services aux membres de l’Union européenne (UE), ou qui collectent et analysent des données pour les résidents de l’UE quel que soit l’endroit où vous vous trouvez et celui où se trouve votre entreprise. Pour plus de détails, consultez la [rubrique Synthèse RGPD](gdpr.md).

De même, le CCPA (California Consumer Privacy Act) prévoit des droits de confidentialité et des obligations pour les consommateurs de la Californie, y compris des droits similaires aux droits des personnes concernées en vertu du RGPD, tels que le droit de supprimer, d’accéder et de recevoir (portabilité) leurs informations personnelles.  Le CCPA prévoit également des publications d’informations, des protections contre la discrimination des personnes faisant usage de leurs droits et la possibilité d’opter pour ou contre certains transferts de données classés en tant que « ventes ». Ce document vous permet d’obtenir des informations sur le traitement des demandes des personnes concernées (DPC) dans le cadre du RGPD et du CCPA à l’aide des produits etdes services Microsoft.

- [Office 365](gdpr-dsr-Office365.md)
- [Azure](gdpr-dsr-Azure.md)
- [Intune](gdpr-dsr-Intune.md)
- [Dynamics 365](gdpr-dsr-Dynamics365.md)
- [Visual Studio Family](gdpr-dsr-visual-studio-family.md)
- [Azure DevOps Services](gdpr-dsr-vsts.md)
- [Support Microsoft et services professionnels](gdpr-dsr-prof-services.md)

## <a name="terminology"></a>Terminologie

Définitions utiles pour les termes RGPD utilisés dans ce document :

- *Contrôleur de données (contrôleur)*  : la personne morale, l’autorité publique, le service ou tout autre organisme qui, seul ou conjointement avec d’autres entités, détermine les finalités et les moyens de traitement des données personnelles.  
- *Données personnelles* et *personne concernée* : toutes les informations relatives à une personne physique identifiée ou identifiable (personne concernée); une personne physique identifiable est une personne qui peut être identifiée, directement ou indirectement.  
- *Responsable du traitement* : la personne physique ou morale, l’autorité publique, le service ou tout autre organisme qui traite des données à caractère personnel pour le compte de l’entité de contrôle.  
- *Données client* : les données produites et stockées dans les opérations quotidiennes dans le cadre du fonctionnement de votre entreprise.

## <a name="what-is-a-dsr"></a>Qu’est-ce qu’une demande de la personne concernée ?

Le Règlement général sur la protection des données (RGPD) accorde le droit aux individus (appelés, dans le règlement, personnes concernées) de gérer les données personnelles qui ont été collectées par un employeur ou tout autre type d’agence ou d’organisation (également appelé responsable du traitement des données ou responsable du traitement). Le RGPD confère aux personnes concernées des droits précis sur leurs données personnelles ; ces droits vous donnent la possibilité d’obtenir des copies de ces données, de les faire modifier, d’en limiter le traitement, de les supprimer ou de les recevoir dans un format électronique afin de pouvoir les transférer à un autre responsable du traitement.

Le CCPA (California Consumer Privacy Act) prévoit des droits de confidentialité et des obligations pour les consommateurs de la Californie, y compris des droits similaires aux droits des personnes concernées en vertu du RGPD, tels que le droit de supprimer, d’accéder et de recevoir (portabilité) leurs informations personnelles.  

En tant que contrôleur, vous avez l’obligation de prendre en compte chaque DPC et de fournir une réponse de fond en effectuant l’action demandée ou en indiquant pourquoi la DPC ne peut pas être traitée par le contrôleur. Un contrôleur doit consulter ses propres conseillers juridiques ou de conformité en relation avec la destruction correcte d’une DSR donnée.

Plusieurs processus peuvent impliquer l’exécution d’une DPC, conformément aux règles de conformité RGPD de votre organisation.
  
- **Découverte**. Processus de détermination des données nécessaires à l’exécution d’une DSR.
- **Accès**. Récupération et transmission potentielle à la personne concernée par les informations découvertes.
- **Rectifier**. Implémentation des modifications ou d’autres modifications de données personnelles demandées.
- **Restreindre**. Modification de l’accès ou du traitement des données de personne en restreignant l’accès ou en supprimant des données du Cloud Microsoft.
- **Exporter**. Fournir un « format structuré, communément utilisé, lisible par l’ordinateur » de données personnelles à la personne concernée, comme fourni par le « droit de portabilité des données » du RGPD.
- **Supprimer** Suppression définitive de données personnelles du Microsoft Cloud.

## <a name="specific-dsr-considerations"></a>Considérations spécifiques concernant une DSR

### <a name="insights-generated-by-microsoft-products-or-services"></a>Analyses générées par les produits ou services Microsoft

[Des analyses](/microsoft-365/compliance/gdpr-dsr-office365#part-2-responding-to-dsrs-with-respect-to-insights-generated-by-office-365) peuvent être générées par les services (MyAnalytics, etc.). Office 365 inclut des services en ligne qui fournissent une analyse aux utilisateurs et organisations qui les utilisent. Les données générées par ces services peuvent produire des données personnelles pertinentes pour une DSR. Suivez le lien dans la liste ci-dessous pour obtenir des informations sur les processus DSR spécifiques aux services.  

### <a name="dsrs-for-system-generated-logs"></a>DSR pour des journaux générés par le système

Les journaux et données associées générés par Microsoft peuvent contenir des données considérées comme personnelles dans le cadre de la définition RGPD des « données personnelles ». Restriction ou rectification des données dans des journaux générés par le système n’est pas prise en charge. Les données contenues dans des journaux générés par le système forment des actions factuelles effectuées dans le cloud Microsoft et les données de diagnostic ; des modifications compromettraient l’enregistrement historique des actions, augmentant ainsi les risques de fraude et de sécurité. Microsoft offre la possibilité d’accéder à des journaux générés par le système, ainsi que de les exporter et de les supprimer, qui peuvent être nécessaires pour effectuer une DSR. Les exemples suivants peuvent inclure les données suivantes :  

- Données relatives à l’utilisation de produits et de services tels que les journaux d’activité des utilisateurs
- Requêtes de recherche et données de requête des utilisateurs
- Données générées par les produits et services comme résultat des fonctionnalités du système et de l’interaction par les utilisateurs ou d’autres systèmes.  

### <a name="yammer-and-kaizala"></a>Yammer et Kaizala

La suppression du compte d'un utilisateur ne supprime pas les journaux générés par le système pour Yammer et Kaizala. Pour supprimer les données contenues dans ces applications, consultez l'une des ressources suivantes :

- [Gérer les demandes des personnes concernées RGPD dans Yammer Entreprise](/yammer/manage-security-and-compliance/gdpr-requests-in-yammer-enterprise)
- [Exporter ou supprimer les données organisationnelles d’un utilisateur dans Kaizala](/office365/kaizala/export-or-delete-a-user-s-data)

### <a name="national-clouds"></a>Clouds nationaux

Dans certains clouds nationaux, un administrateur IT général doit supprimer les journaux générés par le système.

### <a name="microsoft-services"></a>Services Microsoft

Si votre organisation ou vos utilisateurs interagissent avec Microsoft pour bénéficier du support technique lié aux produits et services Microsoft, certaines de ces données peuvent contenir des données personnelles. Pour plus d’informations, reportez-vous à [Demandes des personnes concernées du support Microsoft et des services professionnels concernant le RGPD](gdpr-dsr-prof-services.md).

### <a name="microsoft-controller-products"></a>Produits de contrôleur Microsoft

Dans certains cas, les utilisateurs de votre organisation peuvent accéder aux produits ou services Microsoft dont Microsoft est le contrôleur de données. Dans ce cas, vos utilisateurs doivent initier leur propre DSR directement auprès de Microsoft et Microsoft répond aux demandes directement à l’utilisateur.

### <a name="third-party-products"></a>Produits tiers

Pour les produits et services tiers accessibles via l’authentification de compte Microsoft, les demandes des personnes concernées doivent être redirigées vers le tiers applicable.

## <a name="data-subject-request-admin-tools"></a>Outils d’administration sur les demandes des personnes concernées

- **Centre de sécurité et de conformité** : les données générées par l’utilisateur sont exportées par le [Centre de sécurité et de conformité](https://aka.ms/stpsecurityandcompliance) ou dans les fonctionnalités de l’application.
- **Centre d’administration Azure AD**: supprimez un objet de données d’Azure Active Directory et des services associés à l’aide du [Centre d’administration Azure AD](https://ms.portal.azure.com/#blade/Microsoft_AAD_IAM/UserManagementMenuBlade/Allusers/menuId/).
- **Exportation de journal de données Microsoft** : les journaux générés par le système peuvent être exportés par les administrateurs de locataire à l’aide de la fonction [Exportation de journal de données Microsoft](https://aka.ms/MicrosoftGDPR).

## <a name="learn-more"></a>En savoir plus

- [Centre de gestion de la confidentialité Microsoft](https://www.microsoft.com/trust-center/privacy/gdpr-overview)
