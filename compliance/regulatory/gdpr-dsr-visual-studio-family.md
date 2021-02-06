---
title: Demandes des personnes concernées par le traitement des données pour Visual Studio Family concernant le RGPD et le CCPA
description: Découvrez comment utiliser les outils Microsoft pour gérer les demandes de la personne concernée familiales dans Visual Studio pour les RGPD et CCPA.
keywords: Visual Studio, Visual Studio Code, Visual Studio pour Mac, documentation Visual Studio, confidentialité, RGPD, CCPA
localization_priority: Priority
audience: itpro
ms.prod: visual-studio-family
ms.topic: article
author: robmazz
f1.keywords:
- NOCSH
ms.author: robmazz
manager: laurawi
ms.collection:
- GDPR
- M365-security-compliance
- MS-Compliance
ms.workload:
- multiple
titleSuffix: Microsoft GDPR
ms.custom: seo-marvel-apr2020
ms.openlocfilehash: 29d845c1b9e1c60169db56ba76d731892302bff0
ms.sourcegitcommit: 21ed42335efd37774ff5d17d9586d5546147241a
ms.translationtype: HT
ms.contentlocale: fr-FR
ms.lasthandoff: 02/05/2021
ms.locfileid: "50121923"
---
# <a name="visual-studio-family-data-subject-requests-for-the-gdpr-and-ccpa"></a>Demandes des personnes concernées par le traitement des données pour Visual Studio Family concernant le RGPD et le CCPA

Le [Règlement général sur la protection des données (RGPD)](https://ec.europa.eu/justice/data-protection/reform/index_en.htm) de l’Union européenne permet aux utilisateurs (désignés dans le règlement comme étant les _personnes concernées par le traitement des données_) de gérer leurs données personnelles. Les données personnelles sont définies de manière générale dans le cadre du RGPD comme toutes données associées à une personne physique identifiée ou identifiable. Le RGPD octroie aux personnes concernées par le traitement des données des droits spécifiques sur leurs données personnelles. Ces droits incluent l’obtention de copies des données personnelles, les demandes de corrections de ces dernières, la restriction de leur traitement, leur suppression ou leur réception dans un format électronique. Toute demande formelle effectuée par une personne concernée par le traitement des données à une entité de contrôle des données (un employeur ou tout autre type d’agence ou d’organisation qui contrôle des données personnelles) au sujet de la prise de mesure sur ses données personnelles est appelée _demande de la personne concernée par le traitement des données_ ou « DPC ».

De même, le CCPA (California Consumer Privacy Act), prévoit des droits de confidentialité et des obligations pour les consommateurs de la Californie, y compris des droits similaires aux droits des personnes concernées du RGPD, tels que le droit de supprimer, d’accéder et de recevoir (portabilité) leurs informations personnelles.  Le CCPA prévoit également des publications d’informations, des protections contre la discrimination des personnes faisant usage de leurs droits et la possibilité d’opter pour ou contre certains transferts de données classés en tant que « ventes ». Les ventes sont largement définies pour inclure le partage de données à des fins importantes. Pour plus d’informations sur le CCPA, voir le [California Consumer Privacy Act](offering-ccpa.md) et le [Forum aux questions California Consumer Privacy Act](ccpa-faq.md).

Pour obtenir des informations générales sur le RGPD, consultez la [section RGPD du portail d’approbation de services](https://servicetrust.microsoft.com/ViewPage/GDPRGetStarted).

## <a name="products-covered-by-this-guide"></a>Produits couverts par ce guide

Ce guide explique comment utiliser les outils Microsoft pour exporter ou supprimer des données personnelles collectées pendant une session connectée (ayant requis une authentification) de Visual Studio et Visual Studio pour Mac et les extensions Microsoft pour ces produits et pour Visual Studio Code. Ce guide décrit également comment formuler des demandes des personnes concernées par les données personnelles collectées lors de l’utilisation de Visual Studio Developer Community, NuGet.org et du site ASP.NET. Ces produits peuvent activer l’utilisation d’outils et d’extensions qui ne dépendent pas de Microsoft, et Microsoft n’est pas un processeur de données ou une entité de contrôle pour ces outils et extensions. Les utilisateurs doivent contacter le fournisseur de l’outil ou de l’extension pour être avertis des règles de collecte des données personnelles pour ces outils et extensions.

## <a name="additional-privacy-information"></a>Informations supplémentaires sur la confidentialité

Les termes du contrat de licence du logiciel Microsoft accompagnant les produits, la [déclaration de confidentialité Microsoft](https://go.microsoft.com/fwlink/?LinkId=660726) et [les engagements Microsoft en vertu du RGPD](/legal/gdpr) décrivent nos pratiques en matière de traitement des données.

## <a name="visual-studio-visual-studio-for-mac-and-visual-studio-code"></a>Visual Studio, Visual Studio pour Mac et Visual Studio Code

### <a name="personal-data-we-collect"></a>Données personnelles collectées

En qualité de responsable du traitement de données en vertu du RGPD, Microsoft collecte les données nécessaires auprès des utilisateurs pour améliorer Visual Studio, Visual Studio pour Mac, les extensions Microsoft de ces produits, ainsi que celles de Visual Studio Code. Il existe deux catégories de données : les données client et les journaux générés par le système. Les données client incluent des données de diagnostic utilisateur et des données fonctionnelles nécessaires à ces produits pour effectuer le service qu’ils fournissent. Par exemple, pour offrir aux utilisateurs des expériences personnalisées comme des paramètres d’itinérance, nous devons collecter des données de paramètres et d’informations du compte utilisateur. Les journaux générés par le système correspondant aux données d’utilisation ou de diagnostic utilisées pour vous aider à identifier et à résoudre les problèmes et à améliorer nos produits et services. Elles peuvent également contenir des informations d’identification personnelle sur les utilisateurs finals, comme le nom d’utilisateur. Les journaux générés par le système sont conservés pendant 18 mois maximum. Par exemple, les journaux générés par le système sont conservés pour chaque jour d’utilisation du produit et incluent la date d’utilisation, le produit utilisé (par exemple, « Visual Studio 2017 »), l’action que vous avez effectuée (par exemple, « vs/core/packagecostsummary/solutionload ») et la durée de l’action, comme illustrée dans cet exemple :

```Log
{Time":"2/23/2018 12:00:00 AM","AppName":"Visual Studio 2017","Action":"vs/core/packagecostsummary/solutionload","Target":"1 times",
"DevicePlatform":"Windows 10 Enterprise","IP":null,"InputMethod":null,
"SearchTerm":null,"SearchResult":null}

{Time":"2/23/2018 12:00:00 AM","AppName":"Visual Studio 2017","Action":"vs/ide/connected/accountmanagement/account","Target":"1 times",
"DevicePlatform": "Windows 10 Enterprise","IP":null,"InputMethod":null,
"SearchTerm":null,"SearchResult":null}

{"Time":"2/27/2018 12:00:00 AM","AppName":"Visual Studio 2017","Action":"vs/core/perf/satellitepagefileusage","Target":"23 times",
"DevicePlatform":"Windows 10 Enterprise","IP":null,"InputMethod":null,
"SearchTerm":null,"SearchResult":null}
```

Pour obtenir plus d’informations, consultez l’article relatif aux [journaux générés par le système et collectés par Visual Studio](/visualstudio/ide/diagnostic-data-collection).

Seules les données personnelles associées aux identités authentifiées peuvent être traitées par une DSR. Par conséquent, étant donné que Visual Studio Code ne permet pas de s’identifier, les journaux générés par le système à partir de ce produit ne sont pas associés à une identité authentifiée et ne peuvent pas être pris en charge. Toutefois, certaines extensions Microsoft de Visual Studio Code peuvent fournir des données authentifiées, qui peuvent être traitées par une DSR. Pour obtenir plus d’informations, consultez [RGPD et Visual Studio Code](https://code.visualstudio.com/docs/supporting/faq#_gdpr-and-vs-code). En règle générale, nous ne stockons pas de données pour Visual Studio 2013 et les versions antérieures. Cependant, certaines extensions et certains composants peuvent fournir des données associées à des identités authentifiées pouvant être traitées par une DSR, comme indiqué ci-dessous.

### <a name="how-users-can-control-personal-data"></a>Contrôle des utilisateurs sur leurs données personnelles

Visual Studio 2015 et les versions ultérieures, Visual Studio pour Mac et Visual Studio Code permettent à vos utilisateurs d’arrêter la collecte de données, et vous permettent, en qualité de contrôleur, d’exporter ou de supprimer des données qui ont déjà été collectées.

#### <a name="in-app-settings"></a>Paramètres intégrés à l’application

Les utilisateurs peuvent contrôler les paramètres de confidentialité pour ces produits. Pour obtenir plus d’informations, consultez les articles suivants :

- [Gérer les paramètres de confidentialité dans Visual Studio](/visualstudio/ide/visual-studio-experience-improvement-program)
- [Gérer les paramètres de confidentialité dans Visual Studio pour Mac](/visualstudio/mac/visual-studio-experience-improvement-program)
- [Désactiver la création de rapports de télémétrie dans Visual Studio Code](https://code.visualstudio.com/docs/supporting/faq#_how-to-disable-telemetry-reporting)

#### <a name="exporting-or-deleting-data"></a>Exportation ou suppression des données

Les contrôleurs peuvent gérer les données client et les journaux générés par le système collectés auprès des personnes associées aux données de deux méthodes distinctes, selon la façon dont le produit Visual Studio Family ou les extensions Microsoft ont été enregistrés. Dans certains cas, les deux méthodes doivent être utilisées. Les deux méthodes permettent aux contrôleurs de télécharger une copie de l’historique de leurs activités gérées par cette méthode. La fermeture d’un compte AAD ou de service Microsoft entraîne la suppression des données client Visual Studio connexes, et l’anonymisation des données d’identification personnelle contenues dans les journaux générés par le système se rapportant à ces produits. Les journaux générés par le système rendus anonymes sont conservés pendant 18 mois maximum.

- Les utilisateurs ayant enregistré un produit Visual Studio Family à l’aide d’un compte lié à un client Azure, par exemple, un compte AAD ou un compte MSA associé à un abonnement Azure, peuvent suivre les instructions indiquées dans [Demande des personnes concernées par le traitement des données pour Azure concernant le RGPD](gdpr-dsr-azure.md).
- Les utilisateurs ayant enregistré un produit Visual Studio Family sans utiliser de compte lié à un client Azure, par exemple de nombreux comptes à l’aide d’un compte de service Microsoft (MSA), peuvent utiliser le [Centre de réponse de confidentialité Microsoft basé sur le web](https://aka.ms/userprivacysite) disponible via leur compte Microsoft afin d’afficher, de contrôler et de supprimer des données d’activité liées à leur compte Microsoft sur plusieurs services Microsoft. Dans ce scénario, l’utilisateur agit en qualité de contrôleur de ses données personnelles.

> [!NOTE]
> Quand le titulaire d’un compte de service Microsoft supprime son compte, toutes ses données d’identification personnelle se rapportant à ces produits sont supprimées, peu importe si le compte est lié à un client Azure ou non, et les journaux générés par le système sont rendus anonymes.

Pour Visual Studio 2013, les données que nous recueillons sont rendues anonymes. Pour Visual Studio 2012 et les versions antérieures, nous supprimons immédiatement les données dès leur réception. Dans les deux cas, il n’y a rien à afficher, à exporter ou à supprimer ultérieurement.

## <a name="visual-studio-developer-community"></a>Communauté de développeurs Visual Studio

Nous prenons en charge les demandes concernant le [Règlement général sur la protection des données (RGPD)](https://ec.europa.eu/justice/data-protection/reform/index_en.htm) par l’intermédiaire du site web [Communauté des développeurs](https://developercommunity.visualstudio.com). Vous pouvez afficher, exporter ou supprimer vos données de commentaires.

### <a name="personal-data-we-collect"></a>Données personnelles collectées

Microsoft collecte des données pour nous aider à reproduire et à résoudre les problèmes que vous signalez au sujet des produits Visual Studio Family. Ces données incluent des données personnelles et des commentaires publics. Les données personnelles incluent :

- les informations de votre profil [Communauté des développeurs](https://developercommunity.visualstudio.com) ;
- les préférences et les notifications ;
- les pièces jointes et les journaux générés par le système fournis lorsque vous avez [signalé un problème dans Visual Studio](/visualstudio/ide/how-to-report-a-problem-with-visual-studio-2017) ou par l’intermédiaire de [Communauté des développeurs](https://developercommunity.visualstudio.com) ;
- vos votes.

Les commentaires publics incluent les problèmes signalés, les commentaires et les solutions.

### <a name="how-users-can-control-personal-data"></a>Contrôle des utilisateurs sur leurs données personnelles

#### <a name="view"></a>Vue

Pour afficher les données liées à vos commentaires, procédez comme suit :

1. Connectez-vous à [Communauté de développeurs](https://developercommunity.visualstudio.com). Dans l’angle supérieur droit, cliquez sur votre profil, puis sélectionnez **Profil et préférences**.
2. Cliquez sur les onglets **Profil**, **Notifications**, **Activité** et **Pièces jointes** pour afficher les données envoyées aux systèmes de commentaires.
   1. **Profil** fait référence à votre profil [Communauté des développeurs](https://developercommunity.visualstudio.com), notamment le nom d’utilisateur, l’adresse e-mail, les informations générales, etc.
   2. **Les notifications vous permettent de contrôler les notifications électroniques que vous recevez.
   3. **Activité** vous fournit les éléments de commentaires que vous avez utilisés (publiés, commentés, etc.) et les activités effectuées.
   4. **Pièces jointes** est une liste de l’historique de vos pièces jointes dans un format comme `FileName was attached to the problem "ProblemName" Tue, Apr 10, 18 2:27 PM`.

#### <a name="export"></a>Exporter

Vous pouvez exporter vos données de commentaires dans le cadre de la DSR. Nous allons créer une ou plusieurs archives .zip qui incluent :

- les informations de votre profil [Communauté des développeurs](https://developercommunity.visualstudio.com) ;
- les préférences et les paramètres de notification ;
- les pièces jointes fournies lorsque vous avez [signalé un problème dans Visual Studio](/visualstudio/ide/how-to-report-a-problem-with-visual-studio-2017) ou par l’intermédiaire de [Communauté des développeurs](https://developercommunity.visualstudio.com).

> [!NOTE]
> Nous excluons les commentaires publics suivants fournis à partir de vos archives : commentaires, solutions et problèmes signalés.

Pour commencer une exportation, procédez comme suit :

1. Connectez-vous à [Communauté de développeurs](https://developercommunity.visualstudio.com). Dans l’angle supérieur droit, cliquez sur votre profil, puis sélectionnez **Profil et préférences**.
2. Cliquez sur l’onglet **Confidentialité**, puis cliquez sur **Créer une archive** pour demander l’exportation de vos données.
3. **État d’archivage** est actualisé pour montrer que nous préparons les données. Le délai avant que les données soient disponibles dépend de la quantité de données à exporter.
4. Une fois que les données sont prêtes, nous vous envoyons un e-mail.
5. Cliquez sur **Télécharger l’archive** dans l’e-mail, ou revenez à l’onglet Confidentialité pour télécharger vos données.

> [!NOTE]
> - Nous n’envoyons pas d’e-mail si vous choisissez de ne pas recevoir de notifications dans l’onglet Notifications.
> - Si vous demandez une nouvelle exportation, nous supprimons les anciennes archives et nous en créons de nouvelles.

#### <a name="delete"></a>Supprimer

L’action de suppression permet d’éliminer de [Communauté de développeurs](https://developercommunity.visualstudio.com) les informations suivantes à votre sujet :

- Informations de profil
- Préférences et paramètres de notification
- Pièces jointes fournies lorsque vous avez [signalé un problème dans Visual Studio](/visualstudio/ide/how-to-report-a-problem-with-visual-studio-2017) ou par l’intermédiaire de [Communauté des développeurs](https://developercommunity.visualstudio.com)
- Vos votes

> [!NOTE]
> Nous ne supprimons pas les informations publiques suivantes, mais les rendons anonymes : vos commentaires, vos solutions, les problèmes que vous avez signalés.
>
> [!IMPORTANT]
> La suppression d’un compte AAD ou de service Microsoft déclenche le processus de suppression de [Communauté des développeurs](https://developercommunity.visualstudio.com).

Pour lancer une suppression, procédez comme suit :

1. Connectez-vous à [Communauté des développeurs](https://developercommunity.visualstudio.com). Dans l’angle supérieur droit, cliquez sur votre profil, puis sélectionnez **Profil et préférences**.
2. Cliquez sur l’onglet **Confidentialité**, puis cliquez sur **Supprimer vos données et votre compte** pour lancer la suppression de vos données.
3. Un écran de confirmation s’affiche.
4. Saisissez « supprimer » dans la zone, puis cliquez sur **Supprimer mon compte**.

Lorsque vous cliquez sur **Supprimer mon compte** :

- Vous êtes déconnecté.
- Nous supprimons votre compte [Communauté des développeurs](https://developercommunity.visualstudio.com), vos données personnelles et les pièces jointes.
- Nous rendons anonymes vos commentaires publics. Vos commentaires publics restent disponibles sur Communauté des développeurs et sont indiqués comme provenant d’un utilisateur anonyme.
- Nous ne vous envoyons pas d’e-mail après avoir supprimé votre compte, car vous n’appartenez plus au système.
- Si vous signalez un nouveau problème ou si vous vous connectez à [Communauté des développeurs](https://developercommunity.visualstudio.com), vous êtes identifié comme un nouvel utilisateur.
- Si vous supprimez votre compte à partir de [Communauté des développeurs](https://developercommunity.visualstudio.com), nous ne le supprimons pas d’autres services Microsoft.

## <a name="xamarin-forums"></a>Forums Xamarin

### <a name="personal-data-we-collect"></a>Données personnelles collectées

Par le biais de la communauté d’utilisateurs [ des forums Xamarin](https://forums.xamarin.com/), Microsoft collecte les données que vous fournissez pour nous aider à reproduire et résoudre les problèmes que vous pouvez rencontrer avec les produits et services Microsoft. Ces données incluent les données personnelles et les commentaires publics. Les données personnelles que nous recueillons sont les données de compte d’utilisateur (par exemple, les noms d’utilisateur et les adresses de messagerie associées à vos forums Xamarin) et les commentaires publics que nous recueillons incluent les bogues, les problèmes, les commentaires et les solutions que vous proposez via les forums Xamarin.

### <a name="how-you-can-control-your-data"></a>Contrôler vos données

#### <a name="xamarin-forums"></a>Xamarin Forums

##### <a name="view"></a>Vue

Les utilisateurs disposant de comptes Xamarin Forums actifs peuvent afficher leurs données personnelles et commentaires publics (par exemple, tous leurs threads et billets publiés) à partir de leur compte Xamarin Forums. Les utilisateurs peuvent également modifier leurs données personnelles via leur compte.

##### <a name="export"></a>Exporter

La communauté Xamarin Forums est hébergée par un tiers, Vanilla Forums. Pour demander l’exportation de vos données publiques, les utilisateurs doivent contacter forums@xamarin.com (géré par l’équipe Xamarin). Ensuite, nous communiquerons directement avec Vanilla Forums pour traiter cette demande.

##### <a name="delete"></a>Delete

La communauté Xamarin Forums est hébergée par un tiers, Vanilla Forums. Pour demander la suppression des données personnelles et publiques, les utilisateurs doivent contacter forums@xamarin.com (géré par l’équipe Xamarin). Ensuite, nous traitons manuellement la demande de suppression des données personnelles de l’utilisateur.

> [!NOTE]
> Bugzilla pour Xamarin n’accepte plus les nouveaux problèmes. Les anciens propriétaires de comptes Xamarin Bugzilla peuvent afficher une archive de tous les bogues qu’ils ont rapportés et de tous les commentaires qu’ils ont ajoutés aux bogues sur: [https://xamarin.github.io/bugzilla-archives/](https://xamarin.github.io/bugzilla-archives/). Pour demander la suppression de données personnelles contenues dans l’archive, les utilisateurs peuvent remplir et envoyer à [https://github.com/xamarin/bugzilla-archives/issues/new/choose](https://github.com/xamarin/bugzilla-archives/issues/new/choose). Les commentaires publics (par exemple, bogues, problèmes, commentaires et solutions) que les utilisateurs ont publiés sur le Xamarin Bugzilla ne sont pas supprimés après réception d’une demande de suppression. Les commentaires publics sont alors enregistrés de façon anonyme en supprimant le nom et l’adresse e-mail associés aux commentaires publics créés par l’utilisateur qui envoie la demande de suppression.

## <a name="nuget"></a>NuGet

Pour obtenir plus d’informations relatives aux DSR pour NuGet.org, consultez l’article [Demandes de données utilisateur NuGet](/nuget/policies/data-requests).

## <a name="aspnet"></a>ASP.NET

Pour obtenir plus d’informations relatives aux DSR pour le site web ASP.NET, consultez l’article relatif au [traitement des demandes de personnes associées aux données pour le RGPD et le site web ASP.NET](https://www.asp.net/gdpr).

## <a name="iisnet"></a>IIS.NET

Pour obtenir plus d’informations relatives aux DSR pour le site web IIS.NET, consultez l’article relatif au [traitement des demandes de personnes associées aux données pour le RGPD et le site web IIS.NET](https://www.iis.net/gdpr).

## <a name="other-visual-studio-family-services"></a>Autres services Visual Studio Family

### <a name="surveymonkey"></a>SurveyMonkey

De temps à autre, nous invitons des clients à fournir des commentaires sur ces produits par l’intermédiaire de SurveyMonkey. Ces données sont supprimées dans un délai de 28 jours. Lors du traitement des demandes des personnes concernées par le traitement des données pour ces produits, si nous avons des réponses de sondage authentifiées, nous les incluons dans l’exportation et la suppression desdites demandes.

## <a name="learn-more"></a>En savoir plus

- [Engagements du RGDP pris par Microsoft envers les clients de nos produits logiciels d’entreprise généralement disponibles](/legal/gdpr)
- [Centre de gestion de la confidentialité Microsoft](https://www.microsoft.com/trust-center/privacy/gdpr-overview)
- [Portail d’approbation de service](https://servicetrust.microsoft.com/ViewPage/GDPRGetStarted)
- [Tableau de bord de confidentialité Microsoft](https://account.microsoft.com/privacy)
- [Centre de réponse de confidentialité Microsoft](https://aka.ms/userprivacysite)
- [Demandes des personnes associées aux données pour Azure concernant le RGPD](gdpr-dsr-azure.md)
