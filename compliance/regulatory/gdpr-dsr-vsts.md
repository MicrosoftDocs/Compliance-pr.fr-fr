---
title: Demandes des personnes concernées par les données Azure DevOps concernant le RGPD et le CCPA
description: Découvrez comment utiliser les outils Microsoft pour exporter ou supprimer des données personnelles collectées pendant une session authentifiée des services Azure DevOps.
keywords: Visual Studio Team Services, VSTS, documentation Azure DevOps, confidentialité, RGPD, CCPA
localization_priority: Priority
audience: itpro
ms.prod: devops
ms.topic: article
author: robmazz
ms.author: robmazz
f1.keywords:
- NOCSH
manager: laurawi
ms.collection:
- GDPR
- M365-security-compliance
- MS-Compliance
ms.workload:
- multiple
titleSuffix: Microsoft GDPR
ms.custom: seo-marvel-mar2020
ms.openlocfilehash: ec2152d2039b7626c0562869a9a549f0361f7270
ms.sourcegitcommit: 21ed42335efd37774ff5d17d9586d5546147241a
ms.translationtype: HT
ms.contentlocale: fr-FR
ms.lasthandoff: 02/05/2021
ms.locfileid: "50121903"
---
# <a name="azure-devops-services-data-subject-requests-for-the-gdpr-and-ccpa"></a>Demandes des personnes concernées par les données Azure DevOps Services pour le RGPD et le CCPA

Le [Règlement général sur la protection des données (RGPD)](https://ec.europa.eu/justice/data-protection/reform/index_en.htm) de l’Union européenne permet aux utilisateurs, désignés dans le règlement comme les *personnes concernées*, de gérer les données personnelles collectées par le *contrôleur des données*. Le contrôleur des données, ou simplement *contrôleur*, est un employeur ou tout autre type d’agence ou organisation. Les données personnelles sont définies de manière générale dans le cadre du RGPD comme étant les données associées à une personne physique identifiée ou identifiable. Le RGPD octroie aux personnes concernées des droits spécifiques sur leurs données personnelles. Ces droits incluent l’obtention de copies des données personnelles, les demandes de correction de ces dernières, la restriction de leur traitement, leur suppression ou leur réception dans un format électronique afin de les transférer à un autre contrôleur. Toute demande formelle effectuée par une personne concernée à un contrôleur au sujet de la prise de mesure sur ses données personnelles est appelée *demande de personne concernée* ou DSR.

De même, le CCPA (California Consumer Privacy Act), prévoit des droits de confidentialité et des obligations pour les consommateurs de la Californie, y compris des droits similaires aux droits des personnes concernées du RGPD, tels que le droit de supprimer, d’accéder et de recevoir (portabilité) leurs informations personnelles.  Le CCPA prévoit également des publications d’informations, des protections contre la discrimination des personnes faisant usage de leurs droits et la possibilité d’opter pour ou contre certains transferts de données classés en tant que « ventes ». Les ventes sont largement définies pour inclure le partage de données à des fins importantes. Pour plus d’informations sur le CCPA, voir le [California Consumer Privacy Act](offering-ccpa.md) et le [Forum aux questions California Consumer Privacy Act](ccpa-faq.md).

Pour obtenir des informations générales sur le RGPD, consultez la [section RGPD du portail d’approbation de services](https://servicetrust.microsoft.com/ViewPage/GDPRGetStarted).

Ce guide explique comment utiliser les outils de Microsoft pour exporter ou supprimer des données personnelles collectées pendant une session connectée (ayant requis une authentification) d’Azure DevOps Services (anciennement nommé Visual Studio Team Services).

## <a name="additional-privacy-information"></a>Informations supplémentaires sur la confidentialité

Les articles [Déclaration de confidentialité Microsoft](https://privacy.microsoft.com/privacystatement), [Conditions des services en ligne (OST)](https://www.microsoft.com/licensing/product-licensing/products.aspx) et [Engagements de Microsoft concernant le RGPD](/legal/gdpr) décrivent nos pratiques de traitement des données.

## <a name="personal-data-we-collect"></a>Données personnelles collectées

Microsoft collecte des données auprès des utilisateurs pour son fonctionnement et afin d’améliorer les services Azure DevOps. Azure DevOps Services recueille deux catégories de données : les données client et les journaux générés par le système. Les données client incluent les données transactionnelles et interactionnelles spécifiques à un utilisateur dont Azure DevOps Services a besoin pour fonctionner. Les journaux générés par le système incluent les données d’utilisation du service agrégées pour chaque zone de produit et fonctionnalité.

## <a name="delete-azure-devops-data"></a>Supprimer des données Azure DevOps

La première étape pour supprimer les données client associées Azure DevOps Services et rendre anonymes les données personnelles identifiables dans les journaux générés par le système consiste à fermer votre compte d’identité Azure Active Directory (AAD) ou votre compte Microsoft (MSA). Azure DevOps Services est un système d’enregistrement à l’intégrité, la traçabilité et aux règles d’audit strictes. Ces obligations existantes ont une incidence sur les obligations de suppression et de rétention pour le RGPD. La fermeture du compte d’identité n’altère pas, ne supprime ni ne modifie les artefacts et les enregistrements associés à l’identité individuelle dans l’organisation Azure DevOps. Nous garantissons qu’une fois l’ensemble d’une organisation DevOps supprimé, toutes les données personnellement identifiables associées ainsi que les journaux générés par le système détectés dans cette organisation sont supprimés de notre système (après la période requise de 30 jours de suppression réversible).

## <a name="export-azure-devops-data"></a>Exporter des données Azure DevOps

Les contrôleurs des données peuvent exporter les données client et les journaux générés par le système collectés auprès des personnes concernées via l’une de deux méthodes, selon le fournisseur d’identité (MSA ou AAD) utilisé pour la connexion au service Azure DevOps.

- Les utilisateurs qui s’authentifient à l’aide d’un compte lié à un client Azure, par exemple, un compte AAD ou un compte de service Microsoft associé à un abonnement Azure, peuvent suivre les instructions indiquées dans [Demandes des personnes associées aux données pour Azure concernant le RGPD](gdpr-dsr-azure.md).

- Les utilisateurs qui s’authentifient à l’aide d’une identité MSA peuvent utiliser ce [site de gestion des demandes relatives aux données confidentielles](https://www.microsoft.com/concern/privacyrequest-msa) pour connaître les données d’activité liées à leur identité MSA pour plusieurs services Microsoft. Dans ce cas de figure, l’utilisateur est un contrôleur de ses propres données personnelles.

## <a name="export-or-delete-issues"></a>Problèmes d’exportation ou de suppression

Pour les identités AAD, si vous rencontrez des problèmes lorsque vous exportez ou supprimez des données sur le portail Azure, accédez au panneau **Aide + Support** du portail Azure et envoyez un nouveau ticket sous **Gestion des abonnements** > **Autre demande de conformité et de sécurité** > **Confidentialité et demandes dans le cadre du RGPD**.

Pour les identités MSA, si vous rencontrez des problèmes lors de l’exportation de données à partir du [site de gestion des demandes relatives aux données confidentielles](https://www.microsoft.com/concern/privacyrequest-msa), connectez-vous au site et envoyez une demande d’aide à l’équipe Microsoft chargée de la confidentialité via le formulaire web de demande.

## <a name="learn-more"></a>En savoir plus

Microsoft mettra tout en œuvre pour que vos données Azure DevOps Services restent privées et sûres, sans exception. Consultez notre [vue d’ensemble sur la protection des données Azure DevOps Services](/vsts/articles/team-services-security-whitepaper) pour en savoir plus sur la façon dont nous protégeons vos données Azure DevOps Services.

## <a name="see-also"></a>Voir aussi

- [Engagements du RGPD pris par Microsoft envers les clients de nos produits logiciels d’entreprise généralement disponibles](/legal/gdpr)
- [Centre de gestion de la confidentialité Microsoft](https://www.microsoft.com/trust-center/privacy/gdpr-overview)
- [Portail d’approbation de service](https://servicetrust.microsoft.com/ViewPage/GDPRGetStarted)
- [Tableau de bord de confidentialité Microsoft](https://account.microsoft.com/privacy)
- [Centre de réponse de confidentialité Microsoft](https://aka.ms/userprivacysite)
- [Demandes des personnes associées aux données pour Azure concernant le RGPD](gdpr-dsr-azure.md)
