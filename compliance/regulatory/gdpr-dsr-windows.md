---
title: Service de processeur de données pour les demandes des personnes concernées Windows Entreprise pour le RGPD et le CCPA
description: Découvrez comment utiliser les produits Microsoft, les services et les outils d’administration pour rechercher et agir sur des données personnelles afin de répondre aux DSRs.
keywords: Microsoft 365, Microsoft 365 Éducation, documentation Microsoft 365, RGPD
localization_priority: Priority
ROBOTS: NOINDEX, NOFOLLOW
ms.prod: microsoft-365-enterprise
ms.topic: article
f1.keywords:
- NOCSH
ms.author: daniha
author: DaniHalfin
manager: dansimp
audience: itpro
ms.collection:
- GDPR
- M365-security-compliance
- MS-Compliance
ms.openlocfilehash: 196796cbbfe7755f2639ed5acc163cce130d98d8
ms.sourcegitcommit: 626b0076d133e588cd28598c149a7f272fc18bae
ms.translationtype: HT
ms.contentlocale: fr-FR
ms.lasthandoff: 11/30/2020
ms.locfileid: "49507053"
---
# <a name="data-processor-service-for-windows-enterprise-data-subject-requests-for-the-gdpr-and-ccpa"></a>Service de processeur de données pour les demandes des personnes concernées Windows Entreprise pour le RGPD et le CCPA 

>[!NOTE]
>Cette rubrique est destinée aux participants au programme de prévisualisation du service de traitement des données pour Windows et nécessite l'acceptation de conditions d'utilisation spécifiques. Pour en savoir plus sur le programme et accepter les conditions d’utilisation, voir [https://aka.ms/WindowsEnterprisePublicPreview](https://aka.ms/WindowsEnterprisePublicPreview).

## <a name="introduction-to-data-subject-requests-dsrs"></a>Introduction aux demandes des personnes concernées (DSR) 

Le Règlement général sur la protection des données (RGPD) de l’UE permet aux utilisateurs (désignés dans le règlement comme étant les _personnes concernées_) de gérer les données personnelles collectées par un employeur ou tout autre type d’agence ou organisation (le _contrôleur des données_ ou le _contrôleur_ uniquement). Les données personnelles sont définies de manière générale dans le cadre du RGPD comme correspondant aux données associées à une personne physique identifiée ou identifiable. Le RGPD octroie aux personnes concernées des droits spécifiques sur leurs données personnelles. Ces droits incluent l’obtention de copies des données personnelles, les demandes de corrections de ces dernières, la restriction de leur traitement, leur suppression ou leur réception dans un format électronique afin de les transférer à un autre contrôleur. Toute demande formelle effectuée par une personne concernée à un contrôleur au sujet de la prise de mesure sur ses données personnelles est appelée _demande de personne concernée_ ou DSR.  

Similarly, the California Consumer Privacy Act (CCPA), provides privacy rights and obligations to California consumers, including rights similar to GDPR’s Data Subject Rights, such as the right to delete, access, and receive (portability) their personal information. The CCPA also provides for certain disclosures, protections against discrimination when electing exercise rights, and “opt-out/ opt-in” requirements for certain data transfers classified as “sales". Sales are broadly defined to include the sharing of data for a valuable consideration. For more information about the CCPA, see the [California Consumer Privacy Act](https://docs.microsoft.com/microsoft-365/compliance/offering-ccpa) and the [California Consumer Privacy Act FAQ](https://docs.microsoft.com/microsoft-365/compliance/ccpa-faq).

Le guide explique comment utiliser les produits, services et outils administratifs de Microsoft pour aider nos clients responsables du traitement à trouver et à traiter les données à caractère personnel afin de répondre aux RQV. Plus précisément, il explique comment trouver, accéder et agir sur les données personnelles qui résident dans le nuage Microsoft. Voici un bref aperçu des processus décrits dans ce guide : 

1. **Accéder** : récupérez des données personnelles qui résident dans le cloud Microsoft et, si nécessaire, effectuez-en une copie pour la personne concernée. 
2. **Supprimer** : Supprimer définitivement les données personnelles qui résidaient dans le cloud Microsoft. 
3. **Exportation** :Fournir à la personne concernée une copie électronique (dans un format lisible par machine) des données à caractère personnel. Aux termes de la CCPA, on entend par « renseignements personnels » toute information concernant une personne identifiée ou identifiable.

Les informations personnelles sous CCPA sont toutes les informations relatives à une personne identifiée ou identifiable. Il n’existe aucune distinction entre le rôle privé, public ou professionnel d’une personne. Le terme défini « informations personnelles » s’aligne approximativement sur « données personnelles » sous RGPD. Toutefois, le CCPA inclut également les données familiales et familiales. Pour plus d’informations sur le CCPA, voir le [California Consumer Privacy Act](https://docs.microsoft.com/microsoft-365/compliance/offering-ccpa) et le[Forum aux questions California Consumer Privacy Act](https://docs.microsoft.com/microsoft-365/compliance/ccpa-faq).

Chaque section de ce guide décrit les procédures techniques qu'une organisation de contrôle des données peut suivre pour répondre à un DSR concernant des données personnelles dans le nuage Microsoft. 

## <a name="terminology"></a>Terminologie

Vous trouverez ci-dessous la liste des définitions de termes utilisés dans ce guide. 

* _Responsable du traitement des données :_ la personne physique ou morale, l’autorité publique, le service ou tout autre organisme qui, seul ou conjointement avec d’autres, détermine les finalités et les moyens du traitement des données à caractère personnel ; lorsque les finalités et les moyens du traitement sont déterminés par la législation de l’Union ou des États membres, le responsable du traitement peut être désigné, ou les critères spécifiques relatifs à sa nomination être définis, par la législation de l’Union ou des États membres. 

* _Données personnelles et personne concernée par le traitement des données :_ informations relatives à une personne physique identifiée ou identifiable (« la personne concernée par le traitement des données ») ; une personne physique identifiable est une personne qui peut être identifiée, directement ou indirectement, notamment par référence à un identificateur par exemple, un nom, un numéro d’identification, des données de localisation, un identificateur en ligne, ou un ou plusieurs facteurs spécifiques de l’identité physique, physiologique, génétique, mentale, économique, culturelle ou sociale de cette personne physique. 

* _Sous-traitant :_ une personne physique ou morale, une autorité publique, une agence ou un autre organisme qui traite les données à caractère personnel pour le compte du responsable du traitement. 

* _Données sur les clients_ : Toutes les données, y compris tous les fichiers texte, son, vidéo ou image, et les logiciels, qui sont fournis à Microsoft par un client ou en son nom par l'utilisation du service aux entreprises. 

* _Données de diagnostic Windows_ : Données techniques essentielles des appareils Windows concernant l'appareil et les performances de Windows et des logiciels associés. Elles sont utilisées pour maintenir Windows à jour, sécurisé, fiable, performant et améliorer Windows grâce à l'analyse globale de l'utilisation de Windows. Le type de matériel utilisé, les applications installées avec leur utilisation respective et les informations de fiabilité sur les pilotes de périphériques sont quelques exemples de données de diagnostic de Windows. Certains composants et applications Windows se connectent directement aux services Microsoft, mais les données qu'ils échangent ne sont pas des Données de diagnostic Windows. Par exemple, l'échange de la localisation d'un utilisateur pour la météo ou les nouvelles locales n'est pas un exemple de données de diagnostic Windows. 

## <a name="how-to-use-this-guide"></a>Comment utiliser ce guide 

Lorsque vous utilisez le service de traitement des données pour les appareils inscrits à Windows Entreprises, Windows génère des informations, connues sous le nom de données de diagnostic Windows, afin de fournir le service.

## <a name="windows-diagnostic-data"></a>Données de diagnostic Windows 

Microsoft vous offre la possibilité d'accéder, de supprimer et d'exporter les données de diagnostic Windows associées à l'utilisation par un utilisateur du service de traitement des données pour Windows Enterprise.

>[!IMPORTANT]
>La possibilité de rectifier les données de diagnostic de Windows n'est pas prise en charge. Les Données de diagnostic Windows constituent des actions factuelles menées au sein de Windows, et toute modification de ces données compromettrait l'historique des actions, augmentant les risques de sécurité et nuisant à la fiabilité. Toutes les données couvertes dans ce document sont considérées comme des Données de diagnostic Windows. 

## <a name="executing-dsrs-against-windows-diagnostic-data"></a>Exécution des DSR à partir des données de diagnostic de Windows 

Microsoft permet de supprimer et d’exporter certaines données de diagnostic Windows, et d’y accéder, via le portail Azure et directement aussi via des interfaces de programmation d’applications (API).

### <a name="step-1-access"></a>Étape 1 : Accéder 

L'administrateur du locataire est la seule personne au sein de votre organisation qui peut accéder aux données de diagnostic Windows associées à l'utilisation par un utilisateur particulier d'un service de traitement de données pour le dispositif Windows Enterprise inscrit. Les données récupérées pour une demande d'accès seront fournies, via l'exportation, dans un format lisible par la machine et seront fournies dans des fichiers qui permettront à l'utilisateur de savoir à quels appareils et services les données sont associées. Comme indiqué précédemment, les données récupérées ne comprendront pas de données susceptibles de compromettre la sécurité ou la stabilité du dispositif Windows. 

Microsoft offre une expérience de portail, en fournissant à l'administrateur des locataires de l'entreprise cliente la possibilité de gérer les demandes d'accès au RSD. [ Azure DSR, Part 2, Step 3 : Export](https://docs.microsoft.com/microsoft-365/compliance/gdpr-dsr-azure#step-3-export), décrit comment exécuter une demande d'accès au DSR, via l'exportation, par le portail Azure.

### <a name="step-2-delete"></a>Étape 2 : Supprimer 

Microsoft fournit un moyen d'exécuter des demandes de suppression DSR basées sur l'objet Active Directory Azure d'un utilisateur particulier.

Pour les demandes de suppression basées sur l'utilisateur, Microsoft offre une expérience de portail, qui permet à l'administrateur locataire de l'entreprise cliente de gérer les demandes de suppression de DSR. [Azure DSR, Part 1, Step 5 : Supprimer](https://docs.microsoft.com/microsoft-365/compliance/gdpr-dsr-azure#step-5-delete), décrit comment exécuter une demande de suppression de DSR via le portail Azure. 

Microsoft offre la possibilité de supprimer des utilisateurs, qui à leur tour supprimeront les données des clients, directement via une interface de programmation d'application (API) préexistante. Les détails sont décrits dans la [documentation de référence de l'API](https://docs.microsoft.com/graph/api/directory-deleteditems-delete). 

>[!IMPORTANT]  
>La suppression des données collectées ne met pas fin à la collecte ultérieure. Pour désactiver la collecte de données, suivez la procédure décrite dans la [documentation de référence du service concerné](https://docs.microsoft.com/windows/privacy/configure-windows-diagnostic-data-in-your-organization#enterprise-management).
 
 En outre, les demandes de suppression basées sur l'utilisateur nécessitent la suppression du compte d'utilisateur lui-même. 

### <a name="step-3-export"></a>Étape 3 : Exporter 

L'administrateur du locataire est la seule personne au sein de votre organisation qui peut accéder aux données de diagnostic Windows associées à l'utilisation par un utilisateur particulier d'un service de traitement de données pour le dispositif Windows Enterprise inscrit. Les données récupérées pour une demande d'exportation seront fournies dans un format lisible par la machine et seront fournies dans des fichiers qui permettront à l'utilisateur de savoir à quels appareils et services les données sont associées. Comme indiqué précédemment, les données récupérées ne comprendront pas de données susceptibles de compromettre la sécurité ou la stabilité du dispositif Windows. [Azure DSR, Part 2, Step 3 : Export](https://docs.microsoft.com/microsoft-365/compliance/gdpr-dsr-azure#step-3-export) , décrit comment exécuter une demande d'exportation DSR via le portail Azure. 

Microsoft offre la possibilité d'exporter les données des clients directement via une interface de programmation d'application (API) préexistante. Les détails sont décrits dans la [documentation de référence de l'API](https://docs.microsoft.com/graph/api/user-exportpersonaldata).

## <a name="notify-about-exporting-or-deleting-issues"></a>Notification de l'exportation ou de la suppression de problèmes 

Si vous rencontrez des problèmes lorsque vous exportez ou supprimez des données sur le portail Azure, accédez au panneau **Aide + Support** du portail Azure et envoyez un nouveau ticket sous **Gestion des abonnements > Autre demande de conformité et de sécurité > Confidentialité et demandes dans le cadre du RGPD**. 
