---
title: Configuration de données de diagnostic Windows pour les demandes des personnes concernées pour le RGPD et le CCPA
description: Découvrez comment utiliser les produits Microsoft, les services et les outils d’administration pour rechercher et agir sur des données personnelles afin de répondre aux DSRs.
keywords: Microsoft 365, Microsoft 365 Éducation, documentation Microsoft 365, RGPD
localization_priority: Priority
ROBOTS: NOINDEX, NOFOLLOW
ms.prod: microsoft-365-enterprise
ms.topic: article
f1.keywords:
- NOCSH
ms.author: robmazz
author: robmaz
manager: laurawi
ms.reviewer: delinat
audience: itpro
ms.collection:
- GDPR
- M365-security-compliance
- MS-Compliance
hideEdit: true
ms.openlocfilehash: b79d856591566aa1e13633377600c605429ee68e
ms.sourcegitcommit: 8bf2602d56eedee4447ddb374ef95b0587f254e7
ms.translationtype: HT
ms.contentlocale: fr-FR
ms.lasthandoff: 07/12/2021
ms.locfileid: "53377961"
---
# <a name="windows-diagnostic-data-processor-configuration-data-subject-requests-for-the-gdpr-and-ccpa"></a>Configuration de données de diagnostic Windows pour les demandes des personnes concernées pour le RGPD et le CCPA

>[!NOTE]
>Cette rubrique s’applique aux éditions Windows 10 Entreprise, Pro et Éducation, version 1809 avec mise à jour de juillet 2021 et versions ultérieures.

## <a name="introduction-to-data-subject-requests-dsrs"></a>Introduction aux demandes des personnes concernées (DSR)

Le Règlement général sur la protection des données (RGPD) de l’UE permet aux utilisateurs (désignés dans le règlement comme étant les _personnes concernées_) de gérer les données personnelles collectées par un employeur ou tout autre type d’agence ou organisation (le _contrôleur des données_ ou le _contrôleur_ uniquement). Les données personnelles sont définies de manière générale dans le cadre du RGPD comme correspondant aux données associées à une personne physique identifiée ou identifiable. Le RGPD octroie aux personnes concernées des droits spécifiques sur leurs données personnelles. Ces droits incluent l’obtention de copies des données personnelles, les demandes de corrections de ces dernières, la restriction de leur traitement, leur suppression ou leur réception dans un format électronique afin de les transférer à un autre contrôleur. Toute demande formelle effectuée par une personne concernée à un contrôleur au sujet de la prise de mesure sur ses données personnelles est appelée _demande de personne concernée_ ou DSR. 

De même, le CCPA (California Consumer Privacy Act) prévoit des droits de confidentialité et des obligations pour les consommateurs de la Californie, y compris des droits similaires aux droits des personnes concernées en vertu du RGPD, tels que le droit de supprimer, d’accéder et de recevoir (portabilité) leurs informations personnelles. Le CCPA prévoit également des publications d’informations, des protections contre la discrimination des personnes faisant usage de leurs droits et la possibilité d’opter pour ou contre certains transferts de données classés en tant que « ventes ». Les ventes sont largement définies pour inclure le partage de données à des fins importantes. Pour plus d’informations sur le CCPA, voir le [California Consumer Privacy Act](/microsoft-365/compliance/offering-ccpa) et le [Forum aux questions California Consumer Privacy Act](/microsoft-365/compliance/ccpa-faq).

Le guide explique comment utiliser les produits, services et outils d’administration Microsoft pour aider les clients de notre entité de contrôle à rechercher des données personnelles et à prendre des mesures pour répondre aux DPC. Plus précisément, cela inclut la façon de rechercher, d’accéder aux données personnelles et d’agir sur celles-ci dans les données de diagnostic Windows collectées par Microsoft lorsque la configuration du processeur données de diagnostic Windows est activée. Voici un aperçu rapide des processus présentés dans ce guide :

1. **Accéder**: récupérez les données de diagnostic Windows associées à un objet de données et, si nécessaire, effectuez une copie de celle-ci qui peut être disponible pour la personne concernée.
2. **Supprimer**: supprimer définitivement les données de diagnostic Windows associées à un objet de données.
3. **Exporter** : fournissez une copie électronique (dans un format lisible par une machine) des données de diagnostic Windows à la personne concernée.

Les informations à caractère personnel sous CCPA englobent toutes les informations relatives à une personne identifiée ou identifiable. Aucune distinction n’est faite entre les rôles privé, public et professionnel d’une personne. Le terme défini « informations personnelles » est à peu près aligné sur celui de « données personnelles » dans le RGPD. Toutefois, le CCPA inclut également les données relatives à la famille et au foyer. Pour plus d’informations sur le CCPA, voir le [California Consumer Privacy Act](/microsoft-365/compliance/offering-ccpa) et le [Forum aux questions California Consumer Privacy Act](/microsoft-365/compliance/ccpa-faq).

Chaque section de ce guide décrit les procédures techniques qu’une organisation de contrôle de données peut suivre pour répondre à une DPC pour Données de diagnostic Windows collectées par Microsoft lorsque la configuration du processeur Données de diagnostic Windows est activée.

## <a name="terminology"></a>Terminologie

Vous trouverez ci-dessous la liste des définitions de termes utilisés dans ce guide.

* _Responsable du traitement des données :_ la personne physique ou morale, l’autorité publique, le service ou tout autre organisme qui, seul ou conjointement avec d’autres, détermine les finalités et les moyens du traitement des données à caractère personnel ; lorsque les finalités et les moyens du traitement sont déterminés par la législation de l’Union ou des États membres, le responsable du traitement peut être désigné, ou les critères spécifiques relatifs à sa nomination être définis, par la législation de l’Union ou des États membres.

* _Données personnelles et personne concernée par le traitement des données :_ informations relatives à une personne physique identifiée ou identifiable (« la personne concernée par le traitement des données ») ; une personne physique identifiable est une personne qui peut être identifiée, directement ou indirectement, notamment par référence à un identificateur par exemple, un nom, un numéro d’identification, des données de localisation, un identificateur en ligne, ou un ou plusieurs facteurs spécifiques de l’identité physique, physiologique, génétique, mentale, économique, culturelle, ou sociale de cette personne physique.

* _Sous-traitant :_ une personne physique ou morale, une autorité publique, une agence ou un autre organisme qui traite les données à caractère personnel pour le compte du responsable du traitement.

* _Données client_ : toutes les données, y compris tous les fichiers texte, son, vidéo ou image et les logiciels qui ont été fournis à Microsoft par le client ou pour son compte dans le cadre du service d’entreprise. 

* _Les données de diagnostic Windows_ : donnés techniques des appareils Windows, relatives aux appareils et aux performances de Windows et des logiciels associés. Ceci est utilisé pour maintenir Windows à jour, sécurisé, fiable, performant et apporter des améliorations aux produits. Voici quelques exemples de données de diagnostic Windows : type de matériel utilisé, applications installées avec leur utilisation respective et informations de fiabilité sur les pilotes d’appareils. Certains composants et applications Windows se connectent directement aux services Microsoft, mais les données échangées ne correspondent pas à des données de diagnostic Windows. Par exemple, l’échange d’un emplacement d’utilisateur pour la météo locale ou les actualités n’est pas un exemple de données de diagnostic de Windows.

## <a name="how-to-use-this-guide"></a>Comment utiliser ce guide

Lorsque vous activez la configuration du processeur données de diagnostic Windows, vous devenez le contrôleur des données de diagnostic Windows collectées à partir des appareils. Pour plus d’informations sur cette configuration, consultez [Configurer les données de diagnostic Windows dans votre organisation](/windows/privacy/configure-windows-diagnostic-data-in-your-organization).

## <a name="windows-diagnostic-data"></a>Données de diagnostic Windows

Microsoft vous offre la possibilité d’accéder, de supprimer et d’exporter des données de diagnostic Windows associées à l’utilisation par un utilisateur des appareils activés avec la configuration du processeur données de diagnostic Windows.

> [!IMPORTANT]
> Certaines données de diagnostic Windows sont uniquement associées à un identificateur d’appareil et ne sont pas associées à un utilisateur spécifique. Ce type de données au niveau de l’appareil n’est pas exporté et est supprimé de nos systèmes dans les 30 jours.<br><br>
> La possibilité de rectifier les données de diagnostic Windows n’est pas prise en charge. Les données de diagnostic Windows constituent des actions factuelles effectuées au sein de Windows, et les modifications apportées à ces données compromettent l'historique des actions, ce qui augmente les risques de sécurité et nuit à la fiabilité.

La section suivante explique comment exécuter une demande de sujet de données pour données de diagnostic Windows associée à un ID d’utilisateur Azure Active Directory (AAD). Pour plus d’informations, consultez [Windows 10 & Conformité à la confidentialité : Guide pour les professionnels de l’informatique et de la Conformité](/windows/privacy/windows-10-and-privacy-compliance).

## <a name="executing-dsrs-against-windows-diagnostic-data"></a>Exécution des DPC à partir des données de diagnostic Windows

Microsoft permet de supprimer et d’exporter certaines données de diagnostic Windows, et d’y accéder, via le portail Azure et directement aussi via des interfaces de programmation d’applications (API).

### <a name="step-1-access"></a>Étape 1 : Accéder

Microsoft permet à l’administrateur client au sein de votre organisation d’accéder aux données de diagnostic Windows associées à l’utilisation par un utilisateur particulier d’un appareil activé avec la configuration du processeur données de diagnostic Windows. Les données récupérées pour une demande d’accès seront fournies par le biais de l’exportation dans un format lisible par l’ordinateur et seront fournies dans des fichiers qui permettront à l’utilisateur de savoir à quels appareils et services les données sont associées. Comme indiqué précédemment, les données récupérées n’incluent pas de données susceptibles de compromettre la sécurité ou la stabilité de l’appareil Windows.

Le Portail Azure fournit à l’administrateur client de l’entreprise la possibilité de gérer les demandes d’accès DPC. [Azure DPC, partie 2, Étape 3 : Exporter](/microsoft-365/compliance/gdpr-dsr-azure#step-3-export), décrit comment exécuter une demande d’accès DPC pour données de diagnostic Windows, via l’exportation, via le Portail Azure.

### <a name="step-2-delete"></a>Étape 2 : Supprimer

Microsoft permet d’exécuter des requêtes de suppression de DPC basées sur l’utilisateur en fonction de l’objet Azure Active Directory d’un utilisateur particulier.

Pour les demandes de suppression basées sur l’utilisateur, Microsoft propose deux solutions.  Il existe une expérience de portail qui permet à l’administrateur client du client d’entreprise de gérer les demandes de suppression DPC. [Azure DPC, partie 1, Étape 5 : Supprimer](/microsoft-365/compliance/gdpr-dsr-azure#step-5-delete), décrit comment exécuter une demande de suppression DPC pour données de diagnostic Windows via le Portail Azure en supprimant un utilisateur et les données associées.

Microsoft offre également la possibilité de supprimer des utilisateurs, qui à leur tour supprimeront les données de diagnostic Windows, directement via une interface de programmation d’applications (API) préexistante. Les détails sont décrits dans la [documentation de référence de l’API ](/graph/api/directory-deleteditems-delete).

>[!IMPORTANT]
>La suppression des données collectées n’arrête pas la collecte supplémentaire de l’appareil. Pour désactiver la collecte de données, suivez la procédure décrite dans la [documentation de référence de service correspondante](/windows/privacy/configure-windows-diagnostic-data-in-your-organization#enterprise-management).

### <a name="step-3-export"></a>Étape 3 : Exporter

L’administrateur client est la seule personne au sein de votre organisation qui peut accéder aux données de diagnostic Windows associées à l’utilisation par un utilisateur particulier d’un appareil activé avec la configuration du processeur données de diagnostic Windows. Les données récupérées pour une demande d’exportation seront fournies dans un format lisible par l’ordinateur et seront fournies dans des fichiers qui permettront à l’utilisateur de savoir à quels appareils et services les données sont associées. Comme indiqué précédemment, les données récupérées n’incluent pas de données susceptibles de compromettre la sécurité ou la stabilité de l’appareil Windows. [Azure DPC, partie 2, Étape 3 : Exporter](/microsoft-365/compliance/gdpr-dsr-azure#step-3-export), décrit comment exécuter une demande d’exportation DPC pour données de diagnostic Windows via le Portail Azure.

Microsoft offre également la possibilité d’exporter des données de diagnostic Windows directement via une interface de programmation d’applications (API) préexistante. Les détails sont décrits dans la [documentation de référence de l’API ](/graph/api/user-exportpersonaldata).

## <a name="notify-us-about-exporting-or-deleting-issues"></a>Nous avertir de l’exportation ou de la suppression des problèmes

Si vous rencontrez des problèmes lors de l’exportation ou de la suppression de données de diagnostic Windows à partir du Portail Azure, accédez au panneau Portail Azure **Aide + Support** et envoyez un nouveau ticket sous **Gestion des abonnements > Demandes de confidentialité et de conformité pour les abonnements > Panneau Confidentialité et demandes RGPD**.
