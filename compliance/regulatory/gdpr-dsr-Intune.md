---
title: Demandes des données Intune des personnes concernées pour le RGPD et le CCPA
description: Découvrez comment trouver des données personnelles et agir sur celles-ci, et de répondre aux demandes DSR et CCPA par des clients à l’aide de Microsoft Intune.
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
ms.custom:
- seo-marvel-mar2020
hideEdit: true
titleSuffix: Microsoft GDPR
ms.openlocfilehash: fabaa7487da2dae72cc2aa8aa050b43713154fbe
ms.sourcegitcommit: 21ed42335efd37774ff5d17d9586d5546147241a
ms.translationtype: HT
ms.contentlocale: fr-FR
ms.lasthandoff: 02/05/2021
ms.locfileid: "50120933"
---
# <a name="intune-data-subject-requests-for-the-gdpr-and-ccpa"></a>Demandes des données Intune des personnes concernées pour le RGPD et le CCPA

Le [Règlement général sur la protection des données (RGPD)](https://ec.europa.eu/justice/data-protection/reform/index_en.htm) de l’UE permet aux utilisateurs (désignés dans le règlement comme étant les *personnes concernées*) de gérer les données à caractère personnel collectées par un employeur ou tout autre type d’agence ou organisation (appelés *responsable du traitement des données* ou *responsable du traitement*). Les données à caractère personnel sont définies dans le RGPD de manière générale comme étant les données associées à une personne physique identifiée ou identifiable. Le RGPD octroie aux personnes concernées des droits spécifiques sur leurs données à caractère personnel. Ces droits incluent l’obtention de copies des données à caractère personnel, la demande de corrections de ces dernières, la restriction de leur traitement, leur suppression ou leur réception dans un format électronique afin de les transférer à un autre responsable du traitement des données. Toute demande formelle adressée par une personne concernée à un responsable du traitement des données dans le but d’agir sur ses données à caractère personnel est appelée *demande de la personne concernée* ou DPC.

De même, le CCPA (California Consumer Privacy Act) prévoit des droits de confidentialité et des obligations pour les consommateurs de la Californie, y compris des droits similaires aux droits des personnes concernées en vertu du RGPD, tels que le droit de supprimer, d’accéder et de recevoir (portabilité) leurs informations personnelles.  Le CCPA prévoit également des publications d’informations, des protections contre la discrimination des personnes faisant usage de leurs droits et la possibilité d’opter pour ou contre certains transferts de données classés en tant que « ventes ». Les ventes sont largement définies pour inclure le partage de données à des fins importantes. Pour plus d’informations sur le CCPA, voir le [California Consumer Privacy Act](offering-ccpa.md) et le [Forum aux questions California Consumer Privacy Act](ccpa-faq.md).

Le guide explique comment utiliser les produits, services et outils d’administration Microsoft pour aider les clients de notre entité de contrôle à rechercher des données personnelles et à prendre des mesures pour répondre aux DPC. Plus précisément, ces instructions expliquent comment rechercher des données ou des informations personnelles qui sont stockées dans le cloud Microsoft, comment y accéder et comment entreprendre une action sur ces données. Voici un aperçu rapide des processus présentés dans ce guide :

- **Découvrir** : utilisez les outils de recherche et de détection pour rechercher plus facilement les données du client qui peuvent faire l’objet d’une demande DPC. Une fois que vous avez collecté les documents susceptibles de répondre à la demande, vous pouvez effectuer une ou plusieurs des actions DPC décrites ci-après. Vous pouvez également décider que la demande ne satisfait pas aux directives de votre organisation en termes de réponse à une demande DPC.
- **Accéder :** récupérez des données à caractère personnel qui résident dans le cloud Microsoft et, si nécessaire, effectuez-en une copie pour la personne concernée.
- **Rectifier :** modifiez ou mettez en œuvre d’autres actions demandées sur les données à caractère personnel, le cas échéant.
- **Limiter** : limiter le traitement des données personnelles en supprimant les licences de différents services Azure ou en désactivant les services souhaités lorsque c’est possible. Vous pouvez également supprimer les données du cloud Microsoft et les conserver localement ou à un autre emplacement.
- **Supprimer :** supprimez définitivement des données à caractère personnel qui résidaient dans le cloud Microsoft.
- **Exporter/Recevoir (Portabilité) :** fournit une copie électronique (dans un format lisible par un ordinateur) des données ou des informations personnelles à la personne concernée. Les informations à caractère personnel sous CCPA englobent toutes les informations relatives à une personne identifiée ou identifiable. Aucune distinction n’est faite entre les rôles privé, public et professionnel d’une personne. Le terme défini « informations personnelles » est à peu près aligné sur celui de « données personnelles » dans le RGPD. Toutefois, le CCPA inclut également les données relatives à la famille et au foyer. Pour plus d’informations sur le CCPA, voir le [California Consumer Privacy Act](offering-ccpa.md) et le [Forum aux questions California Consumer Privacy Act](ccpa-faq.md).

Chaque section de ce guide décrit les procédures techniques qu’une organisation étant une entité de contrôle des données peut suivre pour répondre à une DPC pour des données personnelles dans le cloud Microsoft.

#### <a name="terminology"></a>Terminologie

Vous trouverez ci-dessous la liste des définitions de termes utilisés dans ce guide.

- **Responsable du traitement des données :** la personne physique ou morale, l’autorité publique, le service ou tout autre organisme qui, seul ou conjointement avec d’autres, détermine les finalités et les moyens du traitement des données à caractère personnel ; lorsque les finalités et les moyens du traitement sont déterminés par la législation de l’Union ou des États membres, le responsable du traitement peut être désigné, ou les critères spécifiques relatifs à sa nomination être définis, par la législation de l’Union ou des États membres.
- **Données personnelles et personne concernée par le traitement des données :** informations relatives à une personne physique identifiée ou identifiable (« la personne concernée par le traitement des données ») ; une personne physique identifiable est une personne qui peut être identifiée, directement ou indirectement, notamment par référence à un identificateur par exemple, un nom, un numéro d’identification, des données de localisation, un identificateur en ligne, ou un ou plusieurs facteurs spécifiques de l’identité physique, physiologique, génétique, mentale, économique, culturelle ou sociale de cette personne physique.
- **Sous-traitant de données :** la personne physique ou morale, l’autorité publique, le service ou tout autre organisme qui traite des données à caractère personnel pour le compte du responsable du traitement.
- **Données client :** toutes les données, y compris tous les fichiers texte, son, vidéo ou image et les logiciels qui ont été fournis à Microsoft par le client ou pour son compte dans le cadre du service d’entreprise. Les données client incluent à la fois les (1) informations d’identification personnelle des utilisateurs finaux (par exemple, les noms d’utilisateur et les informations de contact dans Azure Active Directory) et le Contenu Client chargé ou créé par un client dans des services spécifiques (par exemple, le contenu client dans un compte de stockage Azure, le contenu client d’une base de données Azure SQL ou l’image de la machine virtuelle d’un client dans des machines virtuelles Azure).
- **Journaux générés par le système :** journaux et données associées générés par Microsoft qui permettent à Microsoft de fournir des services d’entreprise aux utilisateurs. Les journaux générés par le système contiennent essentiellement des données pseudonymes, généralement un numéro généré par le système qui ne permet pas, en soi, d’identifier une personne individuelle, mais qui est utilisé pour fournir les services d’entreprise aux utilisateurs. Les journaux générés par le système peuvent également contenir des informations d’identification personnelle sur les utilisateurs finaux, telles qu’un nom d’utilisateur.

#### <a name="how-to-use-this-guide"></a>Comment utiliser ce guide

Ce guide est composé de deux parties :

- **Partie 1 : Répondre aux demandes des personnes concernées pour des données client** : la première partie de ce guide explique comment rectifier, limiter, supprimer et exporter des données dans des applications dans lesquelles vous avez créé des données, et comment y accéder.  Cette section explique en détail comment exécuter des DPC par rapport à un contenu client et des informations d’identification personnelle d’utilisateurs finaux.
- **Partie 2 : répondre aux demandes de personnes concernées pour les journaux générés par le système** : lorsque vous utilisez les services d’entreprise de Microsoft, Microsoft génère des informations appelées Journaux générés par le système, pour fournir le service.  La deuxième partie de ce guide explique comment supprimer et exporter ces informations pour Azure, et comment y accéder.

### <a name="understanding-dsrs-for-azure-active-directory-and-microsoft-intune"></a>Présentation des DPC pour Azure Active Directory et Microsoft Intune

Lorsqu’il est question des services fournis aux clients d’entreprise, l’exécution des DSR doit toujours être comprise dans le contexte d’un client Azure Active Directory spécifique. Ces DSR sont notamment toujours exécutées dans un client Azure Active Directory donné. Si un utilisateur participe à plusieurs clients, il est important de souligner qu’une DSR donnée est exécutée *uniquement* dans le contexte du client spécifique dans lequel la demande a été reçue. Ce contexte est essentiel de le comprendre car cela signifie que l’exécution d’une DSR par un client d’entreprise n’aura **pas** d’impact sur les données d’un client d’entreprise adjacent.

Il en est de même pour Microsoft Intune fourni à un client d’entreprise : l’exécution d’une DSR par rapport à un compte de Intune *associé à un client Azure Active Directory* **concernera uniquement** les données du client. Par ailleurs, il est important de comprendre les éléments suivants lors de la gestion de comptes Intune dans un client :

- Si l’utilisateur d’un compte Intune crée un abonnement Azure, l’abonnement sera géré comme s’il s’agissait d’un client Azure Active Directory. Par conséquent, les DSR sont limitées au client, comme décrit précédemment.
- Si un abonnement Azure créé via un compte Intune est supprimé, **il n’affectera pas** le compte Intune en question. Une fois de plus, comme indiqué précédemment, les DSR exécutées dans l’abonnement Azure sont limitées à l’étendue du client lui-même.

Les DSR par rapport à un compte Intune lui-même, **en dehors d’un client donné**, sont exécutées via le tableau de bord de confidentialité du consommateur. Consultez le Guide des demandes des personnes associées aux données de Windows pour obtenir plus d’informations.

## <a name="part-1-dsr-guide-for-customer-data"></a>Partie 1 : Guide des DSR pour les données client

### <a name="executing-dsrs-against-customer-data"></a>Exécution des DPC par rapport aux données client

Microsoft permet de supprimer et d’exporter certaines données client, et d’y accéder, via le portail Azure et directement aussi via des interfaces de programmation d’applications (API) ou des interfaces utilisateur (UI) préexistantes pour des services spécifiques (également appelées *expériences intégrées au produit*). Vous trouverez des informations sur ces expériences intégrées au produit dans la documentation de référence des services respectifs.

>[!IMPORTANT]  
>Les services qui prennent en charge les DPC intégrées au produit requièrent l’utilisation directe de l’API ou de l’UI du service, décrivant les applications CRUD (créer, lire, mettre à jour, supprimer) applicables. Par conséquent, l’exécution des DPC dans un service donné doit être effectuée en plus de l’exécution d’une DPC dans le portail Azure afin d’effectuer une demande complète pour une personne concernée par le traitement des données. Consultez la documentation de référence des services spécifiques pour plus d’informations.

### <a name="step-1-discover"></a>Étape 1 : Découvrir

La première étape de la réponse à une DSR consiste à rechercher les données personnelles qui font l’objet de la demande. Cette première étape (recherche et passer en revue les données personnelles en question) vous aidera à déterminer si une DSR répond aux besoins de votre organisation pour accepter ou refuser une DSR. Par exemple, après avoir recherché et passé en revue les données personnelles en question, vous pouvez déterminer que la demande ne répond pas aux exigences de votre organisation, car cette action peut affecter défavorablement les droits et libertés d’autres personnes.

Une fois que vous avez trouvé les données, vous pouvez ensuite effectuer l’action spécifique pour satisfaire la demande de la personne associée aux données. Pour obtenir plus d’informations, consultez les ressources suivantes :

- [Collecte de données](/intune/privacy-data-collect)
- [Traitement et stockage des données](/intune/privacy-data-store-process)
- [Afficher les données personnelles](/intune/privacy-data-view-correct#view-personal-data)

### <a name="step-2-access"></a>Étape 2 : Accéder

Lorsque vous avez trouvé les données client contenant des données personnelles répondant potentiellement à une DPC, vous et votre organisation devez décider quelles données fournir à la personne concernée par le traitement des données. Vous pouvez les fournir avec une copie du document réel, une version correctement rédigée ou une capture d’écran des parties que vous considérez pouvoir partager. Pour chacune de ces réponses à une demande d’accès, vous devrez récupérer une copie du document ou de tout autre élément contenant les données pertinentes.

Lorsque vous fournissez une copie à la personne concernée, vous devrez peut-être supprimer ou modifier des informations personnelles sur d’autres personnes concernées et des informations confidentielles.

La section suivante explique comment obtenir une copie de données pour répondre à la demande d’accès d’une DPC.

#### <a name="azure-active-directory"></a>Azure Active Directory

Microsoft offre un portail et des expériences intégrées au produit permettant à l’administrateur client de l’entreprise cliente de gérer les demandes d’accès de personne concernée. Les demandes d’accès de personne concernée autorisent l’accès aux données à caractère personnel de l’utilisateur, à savoir : (a) les informations identifiables sur un utilisateur final et (b) les journaux générés par le service.

#### <a name="service-specific-interfaces"></a>Interfaces propres au service

Microsoft Intune permet de [découvrir des données client](#step-1-discover) directement via les interfaces utilisateur (IU) ou les interfaces de programmation d’applications préexistantes (API).

### <a name="step-3-rectify"></a>Étape 3 : Rectifier

Si une personne associée aux données vous a demandé de rectifier les données personnelles qui figurent dans les données de votre organisation, vous et votre organisation devez déterminer s’il convient d’honorer cette demande. Rectifier les données peut éventuellement signifier prendre des mesures telles que la modification, la rédaction ou la suppression des données personnelles d’un document ou d’un autre type ou élément.

En qualité de responsable du traitement des données, Microsoft ne permet pas de corriger les journaux générés par le système, car ils représentent des activités factuelles et constituent un enregistrement historique d’événements au sein des services Microsoft. Par rapport à Intune, les administrateurs ne peuvent pas mettre à jour les informations spécifiques d’appareils ou d’applications. Si un utilisateur final souhaite corriger des données personnelles (par exemple, le nom de l’appareil), il doit le faire directement sur son appareil. Ces modifications sont synchronisées lors de la prochaine connexion à Intune.

### <a name="step-4-restrict"></a>Étape 4 : Restreindre

Les personnes concernées peuvent vous demander de restreindre le traitement de leurs données à caractère personnel. Nous fournissons le portail Azure et les interfaces de programmation d’applications (API) ou interfaces utilisateur (UI) préexistantes. Ces expériences permettent à l’administrateur client de l’entreprise cliente de gérer ces DPC via une combinaison d’exportation et de suppression de données. Pour plus d’informations, voir [traitement de données personnelles](/intune/privacy-data-store-process#processing-personal-data).

### <a name="step-5-delete"></a>Étape 5 : Supprimer

Le « droit à l’effacement » par la suppression des données personnelles des données client d’une organisation est une protection clé du RGPD. La suppression des données personnelles inclut l’élimination de l’ensemble des données personnelles et des journaux générés par le système à l’exception des informations du journal d’audit. Pour obtenir plus d’informations, consultez l’article [Supprimer les données personnelles de l’utilisateur final](/intune/privacy-data-audit-export-delete#delete-end-user-personal-data).

## <a name="part-2-system-generated-logs"></a>Partie 2 : Journaux générés par le système

Les journaux d’audit fournissent aux administrateurs client un enregistrement d’activités entraînant une modification dans Microsoft Intune. Les journaux d’audit sont disponibles pour de nombreuses activités de gestion et généralement des actions comme la création, la mise à jour (modification), la suppression et l’affectation. Les tâches à distance qui permettent de générer des événements d’audit peuvent aussi être révisées. Ces journaux d’audit contiennent parfois des données personnelles d’utilisateurs dont les appareils sont enregistrés dans Intune. Les administrateurs ne peuvent pas supprimer les journaux d’audit. Pour obtenir plus d’informations, consultez l’article [Données personnelles d’audit](/intune/privacy-data-audit-export-delete#audit-personal-data).

## <a name="notify-about-exporting-or-deleting-issues"></a>Notification des problèmes d’exportation ou de suppression

Si vous rencontrez des problèmes lorsque vous exportez ou supprimez des données sur le portail Azure, accédez au panneau **Aide + Support** du portail Azure et envoyez un nouveau ticket sous **Gestion des abonnements > Autre demande de conformité et de sécurité > Confidentialité et demandes dans le cadre du RGPD**.

## <a name="learn-more"></a>En savoir plus

- [Centre de gestion de la confidentialité Microsoft](https://www.microsoft.com/trust-center/privacy/gdpr-overview)
