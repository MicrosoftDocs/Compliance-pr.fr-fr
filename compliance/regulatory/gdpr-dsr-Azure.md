---
title: Demandes des personnes concernées en lien avec des données Azure dans le cadre du RGPD et du CCPA
description: Découvrez comment utiliser les produits Azure, les services et les outils d’administration pour rechercher et agir sur des données personnelles afin de répondre aux DSRs.
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
hideEdit: true
titleSuffix: Microsoft GDPR
ms.custom: seo-marvel-mar2020
ms.openlocfilehash: cc71af74f88592e13f5dacf78d92193cea8ea356
ms.sourcegitcommit: 626b0076d133e588cd28598c149a7f272fc18bae
ms.translationtype: HT
ms.contentlocale: fr-FR
ms.lasthandoff: 11/30/2020
ms.locfileid: "49507180"
---
# <a name="azure-data-subject-requests-for-the-gdpr-and-ccpa"></a>Demandes des personnes concernées en lien avec des données Azure dans le cadre du RGPD et du CCPA

## <a name="introduction-to-data-subject-requests-dsrs"></a>Présentation des demandes des personnes concernées (DPC)

Le [Règlement général sur la protection des données (RGPD)](https://ec.europa.eu/justice/data-protection/reform/index_en.htm) de l’UE permet aux utilisateurs (désignés dans le règlement comme étant les *personnes concernées*) de gérer les données à caractère personnel collectées par un employeur ou tout autre type d’agence ou organisation (appelés *responsable du traitement des données* ou *responsable du traitement*). Les données à caractère personnel sont définies dans le RGPD de manière très générale comme étant les données associées à une personne physique identifiée ou identifiable. Le RGPD octroie aux personnes concernées des droits spécifiques sur leurs données à caractère personnel. Ces droits incluent l’obtention de copies des données à caractère personnel, la demande de corrections de ces dernières, la restriction de leur traitement, leur suppression ou leur réception dans un format électronique afin de les transférer à un autre responsable du traitement des données. Toute demande formelle adressée par une personne concernée à un responsable du traitement des données dans le but d’agir sur ses données à caractère personnel est appelée *demande de la personne concernée* ou DPC.

De même, le CCPA (California Consumer Privacy Act), prévoit des droits de confidentialité et des obligations pour les consommateurs de la Californie, y compris des droits similaires aux droits des personnes concernées du RGPD, tels que le droit de supprimer, d’accéder et de recevoir (portabilité) leurs informations personnelles. Le CCPA prévoit également des publications d’informations, des protections contre la discrimination des personnes faisant usage de leurs droits et la possibilité d’opter pour ou contre certains transferts de données classés en tant que « ventes ». Les ventes sont largement définies pour inclure le partage de données à des fins importantes. Pour plus d’informations sur le CCPA, voir le [California Consumer Privacy Act](offering-ccpa.md) et le [Forum aux questions California Consumer Privacy Act](ccpa-faq.md).

Le guide explique comment utiliser les produits, services et outils d’administration Microsoft pour aider les clients de notre entité de contrôle à rechercher des données personnelles et à prendre des mesures pour répondre aux DPC. Plus précisément, il explique comment rechercher des données personnelles qui sont stockées dans le cloud Microsoft, comment y accéder et comment entreprendre une action sur ces données. Voici un aperçu rapide des processus présentés dans ce guide :

- **Découvrir** : utilisez les outils de recherche et de détection pour rechercher plus facilement les données du client qui peuvent faire l’objet d’une demande DPC. Une fois que vous avez collecté les documents susceptibles de répondre à la demande, vous pouvez effectuer une ou plusieurs des actions DPC décrites ci-après. Vous pouvez également décider que la demande ne satisfait pas aux directives de votre organisation en termes de réponse à une demande DPC.
- **Accéder :** récupérez des données à caractère personnel qui résident dans le cloud Microsoft et, si nécessaire, effectuez-en une copie pour la personne concernée.
- **Rectifier :** modifiez ou mettez en œuvre d’autres actions demandées sur les données à caractère personnel, le cas échéant.
- **Limiter** : limiter le traitement des données personnelles en supprimant les licences de différents services Azure ou en désactivant les services souhaités lorsque c’est possible. Vous pouvez également supprimer les données du cloud Microsoft et les conserver localement ou à un autre emplacement.
- **Supprimer :** supprimez définitivement des données à caractère personnel qui résidaient dans le cloud Microsoft.
- **Exporter/Recevoir (Portabilité) :** fournit une copie électronique (dans un format lisible par un ordinateur) des données ou des informations personnelles à la personne concernée. Les informations à caractère personnel sous CCPA englobent toutes les informations relatives à une personne identifiée ou identifiable. Aucune distinction n’est faite entre les rôles privé, public et professionnel d’une personne. Le terme défini « informations personnelles » est à peu près aligné sur celui de « données personnelles » dans le RGPD. Toutefois, le CCPA inclut également les données relatives à la famille et au foyer. Pour plus d’informations sur le CCPA, voir le [California Consumer Privacy Act](offering-ccpa.md) et le [Forum aux questions California Consumer Privacy Act](ccpa-faq.md).

Chaque section de ce guide décrit les procédures techniques qu’une organisation étant une entité de contrôle des données peut suivre pour répondre à une DPC pour des données personnelles dans le cloud Microsoft.

## <a name="terminology"></a>Terminologie

Vous trouverez ci-dessous des définitions de termes utilisés dans ce guide.

- **Responsable du traitement des données :** la personne physique ou morale, l’autorité publique, le service ou tout autre organisme qui, seul ou conjointement avec d’autres, détermine les finalités et les moyens du traitement des données à caractère personnel ; lorsque les finalités et les moyens du traitement sont déterminés par la législation de l’Union ou des États membres, le responsable du traitement peut être désigné, ou les critères spécifiques relatifs à sa nomination être définis, par la législation de l’Union ou des États membres.
- **Données personnelles et personne concernée par le traitement des données :** informations relatives à une personne physique identifiée ou identifiable (« la personne concernée par le traitement des données ») ; une personne physique identifiable est une personne qui peut être identifiée, directement ou indirectement, notamment par référence à un identificateur par exemple, un nom, un numéro d’identification, des données de localisation, un identificateur en ligne, ou un ou plusieurs facteurs spécifiques de l’identité physique, physiologique, génétique, mentale, économique, culturelle ou sociale de cette personne physique.
- **Sous-traitant de données :** la personne physique ou morale, l’autorité publique, le service ou tout autre organisme qui traite des données à caractère personnel pour le compte du responsable du traitement.
- **Données client :** toutes les données, y compris tous les fichiers texte, son, vidéo ou image et les logiciels qui ont été fournis à Microsoft par le client ou pour son compte dans le cadre du service d’entreprise. Les données client incluent à la fois les (1) informations d’identification personnelle des utilisateurs finaux (par exemple, les noms d’utilisateur et les informations de contact dans Azure Active Directory) et le Contenu Client chargé ou créé par un client dans des services spécifiques (par exemple, le contenu client dans un compte de stockage Azure, le contenu client d’une base de données Azure SQL ou l’image de la machine virtuelle d’un client dans des machines virtuelles Azure).
- **Journaux générés par le système :** journaux et données associées générés par Microsoft qui permettent à Microsoft de fournir des services d’entreprise aux utilisateurs. Les journaux générés par le système contiennent essentiellement des données pseudonymes, généralement un numéro généré par le système qui ne permet pas, en soi, d’identifier une personne individuelle, mais qui est utilisé pour fournir les services d’entreprise aux utilisateurs. Les journaux générés par le système peuvent également contenir des informations d’identification personnelle sur les utilisateurs finaux, telles qu’un nom d’utilisateur.

## <a name="how-to-use-this-guide"></a>Comment utiliser ce guide

Ce guide est composé de deux parties :

- **Partie 1 : Répondre aux demandes des personnes concernées pour des données client** : la première partie de ce guide explique comment rectifier, limiter, supprimer et exporter des données dans des applications dans lesquelles vous avez créé des données, et comment y accéder.  Cette section explique en détail comment exécuter des DPC par rapport à un contenu client et des informations d’identification personnelle d’utilisateurs finaux.
- **Partie 2 : répondre aux demandes de personnes concernées pour les journaux générés par le système** : lorsque vous utilisez les services d’entreprise de Microsoft, Microsoft génère des informations appelées Journaux générés par le système, pour fournir le service.  La deuxième partie de ce guide explique comment supprimer et exporter ces informations pour Azure, et comment y accéder.

## <a name="understanding-dsrs-for-azure-active-directory-and-microsoft-service-accounts"></a>Présentation des DPC pour les comptes de service Microsoft et Azure Active Directory

Lorsqu’il est question des services fournis aux clients d’entreprise, l’exécution des DPC doit toujours être comprise dans le contexte d’un client Azure Active Directory (AAD) spécifique. Ces DPC sont notamment toujours exécutées dans un client AAD donné. Si un utilisateur participe à plusieurs clients, il est important de souligner qu’une DPC donnée est exécutée *uniquement* dans le contexte du client spécifique dans lequel la demande a été reçue. Il est essentiel de le comprendre, car cela signifie que l’exécution d’une DPC par un client d’entreprise n’aura **pas** d’impact sur les données d’un client d’entreprise adjacent.

Il en est de même pour les comptes de service Microsoft dans le contexte des services fournis à un client d’entreprise : l’exécution d’une DPC par rapport à un compte de service Microsoft *associé à un client AAD* **concernera uniquement** les données du client. Par ailleurs, il est important de comprendre les éléments suivants lors de la gestion de comptes de service Microsoft dans un client :

- Si l’utilisateur d’un compte de service Microsoft crée un abonnement Azure, l’abonnement sera géré comme s’il s’agissait d’un client AAD. Par conséquent, les DPC sont limitées au client, comme décrit ci-dessus.
- Si un abonnement Azure créé via un compte de service Microsoft est supprimé, **il n’affectera pas** le compte de service Microsoft réel. Encore une fois, comme noté précédemment, les DPC exécutées dans l’abonnement à Azure sont limitées à l’étendue du client lui-même.

Les DPC par rapport à un compte de service Microsoft lui-même, **en dehors d’un client donné**, sont exécutées via le tableau de bord de confidentialité du consommateur. Consultez le Guide des demandes des personnes concernées par le traitement des données de Windows pour plus d’informations.

## <a name="part-1-dsr-guide-for-customer-data"></a>Partie 1 : Guide des DPC pour les données client

### <a name="executing-dsrs-against-customer-data"></a>Exécution des DPC par rapport aux données client

Microsoft permet de supprimer et d’exporter certaines données client, et d’y accéder, via le portail Azure et directement aussi via des interfaces de programmation d’applications (API) ou des interfaces utilisateur (UI) préexistantes pour des services spécifiques (également appelées *expériences intégrées au produit*). Vous trouverez des informations sur ces expériences intégrées au produit dans la documentation de référence des services respectifs.

>[!IMPORTANT]  
> Les services qui prennent en charge les DPC intégrées au produit requièrent l’utilisation directe de l’API ou de l’UI du service, décrivant les applications CRUD (créer, lire, mettre à jour, supprimer) applicables. Par conséquent, l’exécution des DPC dans un service donné doit être effectuée en plus de l’exécution d’une DPC dans le portail Azure afin d’effectuer une demande complète pour une personne concernée par le traitement des données. Consultez la documentation de référence des services spécifiques pour plus d’informations.

### <a name="step-1-discover"></a>Étape 1 : Découvrir

La première étape pour répondre à un DPC consiste à trouver les données personnelles faisant l’objet de la demande. Cette première étape, rechercher et réviser les données personnelles en cause, vous permet de déterminer si un DPC répond aux besoins de votre organisation en matière de respect ou de refus d’un DPC. Par exemple, après avoir trouvé et consulté les données personnelles en cause, vous pouvez déterminer si la demande ne respecte pas les exigences de votre organisation, car cela peut nuire aux droits et libertés d’autres personnes.

Lorsque vous avez trouvé les données, vous pouvez ensuite effectuer l’action spécifique pour satisfaire la demande de la personne concernée.

[Azure Active Directory](https://azure.microsoft.com/services/active-directory/) est le service de gestion des identités et des annuaires basés sur le Cloud de Microsoft. Vous pouvez localiser les informations d’identification personnelle des utilisateurs finaux, telles que les profils utilisateur d’un client et d’un employé et les informations professionnelles d’un utilisateur qui contiennent des données personnelles dans votre environnement [Azure Active Directory](https://azure.microsoft.com/services/active-directory/) (AAD) à l’aide du [ portail Azure](https://portal.azure.com/).

Cette fonctionnalité est particulièrement utile si vous voulez rechercher ou modifier des données personnelles pour un utilisateur spécifique. Vous pouvez également ajouter ou modifier des informations de profil utilisateur et de travail. Vous devez vous connecter avec un compte d’administrateur général pour l’annuaire.

#### <a name="how-do-i-locate-or-view-user-profile-and-work-information"></a>Comment localiser ou afficher le profil utilisateur et les informations professionnelles ?

1. Connectez-vous au [portail Azure](https://portal.azure.com/) avec un compte Administrateur général pour l’annuaire.

2. Sélectionner **Azure Active Directory**.

     ![Sélectionner Tous les services](../media/gdpr-azure-dsr-azure-portal.png)

3. Sélectionner **Utilisateurs**.

     ![Sélectionner les utilisateurs](../media/gdpr-azure-dsr-azure-all-users.png)

4. Dans le volet **Tous les utilisateurs**, sélectionnez un utilisateur dans la liste, puis, dans le volet de l’utilisateur choisi, sélectionnez **Profil** pour afficher les informations de profil utilisateur pouvant contenir des données à caractère personnel.

    ![Sélectionner le profil](../media/gdpr-azure-dsr-azure-user-profile.png)

5. Si vous souhaitez ajouter ou modifier les informations de profil utilisateur, vous pouvez le faire en sélectionnant **Modifier** dans la barre de commandes puis **Enregistrer** après avoir effectué les modifications.

#### <a name="service-specific-interfaces"></a>Interfaces propres au service

Microsoft permet de découvrir des données client directement via des interfaces de programmation d’applications (API) ou des interfaces utilisateur (UI) pré-existantes pour des services spécifiques. Vous trouverez des détails dans la documentation de référence des services respectifs, décrivant les opérations CRUD (créer, lire, mettre à jour, supprimer) applicables.

### <a name="step-2-access"></a>Étape 2 : Accéder

Lorsque vous avez trouvé les données client contenant des données personnelles répondant potentiellement à une DPC, vous et votre organisation devez décider quelles données fournir à la personne concernée par le traitement des données. Vous pouvez les fournir avec une copie du document réel, une version correctement rédigée ou une capture d’écran des parties que vous considérez pouvoir partager. Pour chacune de ces réponses à une demande d’accès, vous devrez récupérer une copie du document ou de tout autre élément contenant les données pertinentes.

Lorsque vous fournissez une copie à la personne concernée, vous devrez peut-être supprimer ou modifier des informations personnelles sur d’autres personnes concernées et des informations confidentielles.

#### <a name="azure-active-directory"></a>Azure Active Directory

Microsoft offre un portail et des expériences intégrées au produit permettant à l’administrateur client de l’entreprise cliente de gérer les demandes d’accès de personne concernée. Les demandes d’accès de personne concernée autorisent l’accès aux données à caractère personnel de l’utilisateur, à savoir : (a) les informations identifiables sur un utilisateur final et (b) les journaux générés par le service.

#### <a name="service-specific-interfaces"></a>Interfaces propres au service

Microsoft permet de découvrir des données client directement via des interfaces de programmation d’applications (API) ou des interfaces utilisateur (UI) pré-existantes pour des services spécifiques. Vous trouverez des détails dans la documentation de référence des services respectifs, décrivant les opérations CRUD (créer, lire, mettre à jour, supprimer) applicables.

### <a name="step-3-rectify"></a>Étape 3 : Rectifier

Si un objet de données vous a demandé de rectifier les données personnelles qui résident dans les données de votre organisation, vous et votre organisation devez déterminer s’il est approprié d’honorer la demande. La rectification des données peut inclure la prise d’actions telles que la modification, rédaction ou la suppression de données personnelles d’un document ou d’un autre type ou élément. La façon la plus simple d’effectuer cette opération pour le support Microsoft et les données FastTrack est indiquée ci-dessous.

#### <a name="azure-active-directory"></a>Azure Active Directory

Les clients d’entreprise peuvent gérer les demandes de rectification corrélatives à une DPC, y compris les fonctionnalités d’édition limitées par la nature d’un service Microsoft donné. En tant que responsable du traitement des données, Microsoft ne permet pas de corriger les journaux générés par le système car il reflète les activités factuelles et constitue un enregistrement historique des événements au sein des services Microsoft. Par rapport à Azure Active Directory, des fonctionnalités d’édition limitées permettent de rectifier les informations d’identification personnelle concernant un utilisateur final, comme décrit plus loin ci-dessous.

##### <a name="azure-active-directory-rectifycorrect-inaccurate-or-incomplete-personal-data"></a>Azure Active Directory : rectifier/corriger des données personnelles inexactes ou incomplètes

Vous pouvez corriger, mettre à jour ou supprimer des informations d’identification personnelle concernant des utilisateurs finaux, comme par exemple les profils utilisateur du client et de l’employé et les informations professionnelles de l’utilisateur qui contiennent des données personnelles, comme par exemple, le nom d’un utilisateur, son poste, son adresse ou son numéro de téléphone, dans votre environnement [Azure Active Directory](https://azure.microsoft.com/services/active-directory/) (AAD) à l’aide du [portail Azure](https://portal.azure.com/).  Vous devez vous connecter avec un compte d’administrateur général pour l’annuaire.

###### <a name="how-do-i-correct-or-update-user-profile-and-work-information-in-azure-active-directory"></a>Comment corriger ou mettre à jour les informations de profil utilisateur et les informations professionnelles dans Azure Active Directory ?

1. Connectez-vous au [portail Azure](https://portal.azure.com/) avec un compte Administrateur général pour l’annuaire.

2. Sélectionner **Azure Active Directory**.

    ![Sélectionner Tous les services](../media/gdpr-azure-dsr-azure-portal.png)

3. Sélectionner **Utilisateurs**.

    ![Sélectionner les utilisateurs](../media/gdpr-azure-dsr-azure-all-users.png)

4. Dans le volet **Tous les utilisateurs**, sélectionnez un utilisateur dans la liste, puis, dans le volet de l’utilisateur sélectionné, sélectionnez **Profil** pour afficher les informations de profil utilisateur à corriger ou mettre à jour.

    ![Sélectionner un profil utilisateur](../media/gdpr-azure-dsr-azure-user-profile.png)

5. Corrigez ou mettez à jour les informations de profil utilisateur, y compris les informations sur le travail, en sélectionnant **Modifier** dans la barre de commandes puis  **Enregistrer** après avoir effectué les modifications.

    ![Sélectionnez Modifier.](../media/gdpr-azure-dsr-azure-edit-user-profile.png)

#### <a name="service-specific-interfaces"></a>Interfaces propres au service

Microsoft permet de découvrir des données client directement via des interfaces de programmation d’applications (API) ou des interfaces utilisateur (UI) pré-existantes pour des services spécifiques. Vous trouverez des détails dans la documentation de référence des services respectifs, décrivant les opérations CRUD (créer, lire, mettre à jour, supprimer) applicables.

### <a name="step-4-restrict"></a>Étape 4 : Restreindre

Les personnes concernées peuvent vous demander de restreindre le traitement de leurs données à caractère personnel. Nous fournissons le portail Azure et les interfaces de programmation d’applications (API) ou interfaces utilisateur (UI) préexistantes. Ces expériences permettent à l’administrateur client de l’entreprise cliente de gérer ces DPC via une combinaison d’exportation et de suppression de données. Un client peut (1) exporter une copie électronique des données à caractère personnel de l’utilisateur, y compris (a) des comptes, (b) des journaux générés par le système et (c) des journaux associés, puis (2) supprimer le compte et les données associées résidant dans les systèmes Microsoft.

### <a name="step-5-delete"></a>Étape 5 : Supprimer

Le « droit à l’effacement » moyennant la suppression des données personnelles des données client d’une organisation est une protection essentielle du RGPD. La suppression des données personnelles inclut la suppression de toutes les données personnelles et journaux générés par le système, à l’exception des informations du journal d’audit. Quand un utilisateur est **supprimé de façon douce** (voir les détails ci-dessous), le compte est désactivé pendant 30 jours. Si aucune autre action n’est prise pendant cette période de 30 jours, l’utilisateur **est définitivement supprimé** (voir les détails ci-dessous). Lors d'**une suppression définitive**, le compte d’utilisateur, les données personnelles et les journaux générés par le système sont supprimés dans un délai de 30 jours supplémentaires. Si un administrateur du client émet immédiatement **une suppression définitive**, le compte d’utilisateur, les données personnelles et les journaux générés par le système sont supprimés dans les 30 jours suivants.

> [!IMPORTANT]
> Vous devez être un administrateur client pour supprimer un utilisateur du client.

#### <a name="delete-a-user-and-associated-data-through-the-azure-portal"></a>Supprimer un utilisateur et les données associées via le portail Azure

Lorsque que vous recevez une demande de suppression de la part d’une personne concernée par le traitement des données, vous pouvez utiliser le portail Azure pour supprimer un utilisateur et les informations personnelles associées ainsi que les journaux générés par le système.

La suppression de ces données implique également celle de l’utilisateur du client. Les utilisateurs sont initialement supprimés de façon réversible, ce qui signifie que le compte peut être récupéré par un administrateur client dans un délai de 30 jours après avoir été marqué pour une suppression réversible. Au bout de 30 jours, le compte est supprimé du client de façon automatique et définitive. Avant ces 30 jours, vous pouvez supprimer manuellement un utilisateur supprimé de façon réversible dans la corbeille.

Voici le processus de haut niveau permettant de supprimer des utilisateurs de votre client.

1. Accédez au portail Azure et localisez l’utilisateur.

2. Supprimez l’utilisateur. Lorsque vous supprimez l’utilisateur pour la première fois, le compte de l’utilisateur est envoyé à la corbeille. **À ce stade, l’utilisateur est supprimé de manière douce, ce qui signifie que le compte est désactivé, mais pas supprimé d’Azure Active Directory.**

3. Accédez à la liste des utilisateurs récemment supprimés et supprimez définitivement l’utilisateur. **À ce stade, l’utilisateur est supprimé définitivement (suppression définitive), ce qui signifie que le compte a été vidé d’Azure Active Directory**

###### <a name="to-delete-a-user-from-an-azure-tenant"></a>Pour supprimer un utilisateur d’un client Azure

1. Connectez-vous au [portail Azure](https://portal.azure.com/) avec un compte Administrateur général pour l’annuaire.

2. Sélectionner **Azure Active Directory**.

    ![Sélectionner Tous les services](../media/gdpr-azure-dsr-azure-portal.png)

3. Sélectionner **Utilisateurs**.

    ![Sélectionner les utilisateurs](../media/gdpr-azure-dsr-azure-all-users.png)

4. Cochez la case en regard de l’utilisateur à supprimer, sélectionnez **Supprimer l’utilisateur**, puis **Oui** dans la zone vous demandant si vous souhaitez supprimer l’utilisateur.

    ![Gestion des utilisateurs](../media/gdpr-azure-dsr-azure-selected-user.png)

5. Dans le  volet  **Tous les utilisateurs**, sélectionnez  **Utilisateurs supprimés**.

    ![Afficher le profil utilisateur](../media/gdpr-azure-dsr-azure-deleted-user.png)

4. Sélectionnez de nouveau le même utilisateur, sélectionnez  **Supprimer définitivement** dans la barre de commandes, puis  **Oui** dans la zone vous demandant de confirmer la suppression définitive.

>[!IMPORTANT]  
>Lorsque vous cliquez sur **Oui** vous supprimez définitivement et irrévocablement l’utilisateur ainsi que toutes les données associées et les journaux générés par le système. Si vous effectuez cette opération par erreur, vous devrez rajouter manuellement l’utilisateur au client. Les données associées et les journaux générés par le système ne sont pas récupérables.

   ![Afficher les informations professionnelles de l’utilisateur](../media/gdpr-azure-dsr-azure-permanently-deleted-user.png)

#### <a name="service-specific-interfaces"></a>Interfaces propres au service

Microsoft permet de découvrir des données client directement via des interfaces de programmation d’applications (API) ou des interfaces utilisateur (UI) pré-existantes pour des services spécifiques. Vous trouverez des détails dans la documentation de référence des services respectifs, décrivant les opérations CRUD (créer, lire, mettre à jour, supprimer) applicables.

## <a name="step-6-export"></a>Étape 6 : Exporter

Le « Droit à la portabilité des données » permet à une personne concernée de demander une copie de ses données à caractère personnel dans un format électronique (c’est-à-dire un « format structuré, fréquemment utilisé, lisible par une machine et interopérable ») qui peut être transmis à un autre responsable du traitement des données. Azure prend cela en charge en permettant à votre organisation d’exporter les données au format JSON natif vers votre conteneur de stockage Azure spécifié.

>[!IMPORTANT]
>Pour exporter des données utilisateur à partir du client, vous devez être un administrateur client.

### <a name="azure-active-directory"></a>Azure Active Directory

Pour des données client, Microsoft offre un portail et des expériences intégrées au produit permettant à l’administrateur client de l’entreprise cliente de gérer les demandes d’exportation d’informations identifiables sur un utilisateur final.

### <a name="service-specific-interfaces"></a>Interfaces propres au service

Microsoft permet de découvrir des données client directement via des interfaces de programmation d’applications (API) ou des interfaces utilisateur (UI) pré-existantes pour des services spécifiques. Vous trouverez des détails dans la documentation de référence des services respectifs, décrivant les opérations CRUD (créer, lire, mettre à jour, supprimer) applicables.

## <a name="part-2-system-generated-logs"></a>Partie 2 : Journaux générés par le système

Microsoft vous permet de supprimer et d’exporter certains journaux générés par le système, associés à l’utilisation d’Azure par un utilisateur, ainsi que d’y accéder.

>[!IMPORTANT]
> Il n’est pas possible de restreindre ni de rectifier les journaux générés par le système. Les journaux générés par le système forment des actions factuelles effectuées dans le cloud Microsoft et les données de diagnostic, et des modifications apportées à ces données compromettraient l’enregistrement historique des actions, augmentant ainsi les risques de fraude et de sécurité.

### <a name="executing-dsrs-against-system-generated-logs"></a>Exécution de DPC par rapport aux journaux générés par le système

Microsoft permet de supprimer et d’exporter certains journaux générés par le système, et d’y accéder, via le portail Azure et aussi directement via les interfaces de programmation ou les interfaces utilisateur des services spécifiques.  Vous trouverez des détails dans la documentation de référence des services respectifs.

>[!IMPORTANT]  
> Les services qui prennent en charge les DSRs du service nécessitent l’utilisation directe de l’interface de programmation d’application (API) ou de l’interface utilisateur (UI) du service. Par conséquent, l’exécution des DPC intégrées dans un produit **doit être effectuée en plus de l’exécution d’une DPC dans le portail Azure afin d’effectuer une demande complète pour une personne concernée par le traitement des données. Consultez la documentation de référence des services spécifiques pour plus d’informations.**

### <a name="step-1-access"></a>Étape 1 : Accéder

L’administrateur du client est la seule personne au sein de votre organisation qui peut accéder aux journaux générés par le système associé à l’utilisation d’Azure par un utilisateur particulier. Les données récupérées pour une demande d’accès seront fournies dans un format lisible par l’ordinateur et seront fournies dans des fichiers qui permettront à l’utilisateur de savoir à quels services les données sont associées. Comme indiqué ci-dessus, les données récupérées n’incluent pas de données susceptibles de compromettre la sécurité du service.

#### <a name="azure-active-directory"></a>Azure Active Directory

Microsoft offre un portail et des expériences intégrées au produit permettant à l’administrateur client de l’entreprise cliente de gérer les demandes d’accès. Les demandes d’accès autorisent l’accès aux données personnelles de l’utilisateur, notamment: (a) les informations identifiables d’un utilisateur final et (b) les journaux générés par le service. Le processus est identique à celui décrit dans la section Azure Active Directory de la Partie 1, Étape 2 : accès.

#### <a name="service-specific-interfaces"></a>Interfaces propres au service

Microsoft permet de découvrir des données client directement via des interfaces de programmation d’applications (API) ou des interfaces utilisateur (UI) pré-existantes pour des services spécifiques. Vous trouverez des détails dans la documentation de référence des services respectifs, décrivant les opérations CRUD (créer, lire, mettre à jour, supprimer) applicables.

### <a name="step-2-delete"></a>Étape 2 : Supprimer

L’administrateur client est la seule personne au sein de votre organisation qui peut exécuter la demande de suppression d’une DPC pour un utilisateur particulier dans un client Azure.

#### <a name="azure-active-directory"></a>Azure Active Directory

Microsoft offre un portail et des expériences intégrées au produit permettant à l’administrateur client de l’entreprise cliente de gérer les demandes de suppression de DSR de personne concernée. Les demandes de suppression DSR suivent la même procédure que celles décrites dans la section supprimer un utilisateur et les données associées via le portail Azure de la partie 1, étape 5 : supprimer.

#### <a name="service-specific-interfaces"></a>Interfaces propres au service

Microsoft permet de découvrir des données client directement via des interfaces de programmation d’applications (API) ou des interfaces utilisateur (UI) pré-existantes pour des services spécifiques. Vous trouverez des détails dans la documentation de référence des services respectifs, décrivant les opérations CRUD (créer, lire, mettre à jour, supprimer) applicables.

### <a name="step-3-export"></a>Étape 3 : Exporter

L’administrateur du client est la seule personne au sein de votre organisation qui peut accéder aux journaux générés par le système associé à l’utilisation d’Azure par un utilisateur particulier. Les données récupérées pour une demande d’exportation seront fournies dans un format lisible par l’ordinateur et seront fournies dans des fichiers qui permettront à l’utilisateur de savoir à quels services les données sont associées. Comme indiqué ci-dessus, les données récupérées n’incluent pas de données susceptibles de compromettre la sécurité ou la stabilité du service.

#### <a name="export-system-generated-logs-using-the-azure-portal"></a>Exporter les journaux générés par le système à l’aide du portail Azure

Une fois que vous recevez une demande d’exportation pour une personne concernée par le traitement des données, vous pouvez utiliser le portail Azure pour exporter les journaux générés par le système associés à un utilisateur donné.

Voici le processus de haut niveau permettant d’exporter des données à partir de votre client.

1. Accédez au portail Azure et créez une demande d’exportation pour le compte de l’utilisateur.
2. Exportez les données et envoyez le fichier à l’utilisateur.

###### <a name="to-export-a-users-info-from-an-azure-tenant"></a>Exporter les informations d’un utilisateur à partir d’un client Azure

1. Ouvrez le portail Azure, sélectionnez **Tous les services**, tapez *stratégie* dans le filtre, puis sélectionnez **Stratégie**.

     ![Filtre Tous les services ](../media/gdpr-azure-dsr-azure-policy.png)

2. Dans le volet **Stratégie**, sélectionnez **Confidentialité de l’utilisateur**, **Gérer les demandes utilisateur**, puis **Ajouter une demande d’exportation**.

    ![Ajouter une demande d’exportation ](../media/gdpr-azure-dsr-azure-add-export-request.png)

3. Terminez la **demande d’exportation des données** :

    ![Nouvelle demande d’exportation des données](../media/gdpr-azure-dsr-azure-export-data-request.png)

- **Utilisateur.** Tapez l’adresse e-mail de l’utilisateur Azure Active Directory qui a demandé l’exportation.
- **Abonnement.** Sélectionnez le compte que vous utilisez pour générer le rapport sur l’utilisation des ressources et facturer les services. C’est également l’emplacement de votre compte de stockage Azure.
- **Compte de stockage.** Sélectionnez l’emplacement de votre espace de stockage Azure (BLOB). Pour plus d’informations, voir l’article[présentation de Stockage Microsoft Azure, stockage BLOB](https://docs.microsoft.com/azure/storage/common/storage-introduction#blob-storage).
- **Conteneur.** Créez un conteneur (ou sélectionnez un conteneur existant) comme emplacement de stockage pour les données confidentielles exportées de l’utilisateur.

4. Sélectionnez **Créer**.

La demande d’exportation passe **en attente**. Vous pouvez afficher l’état du rapport **dans la rubrique confidentialité de l’utilisateur - Aperçu**.

>[!IMPORTANT]  
>Étant donné que les données personnelles peuvent provenir de plusieurs systèmes, il est possible que le processus d’exportation dure un mois.

#### <a name="service-specific-interfaces"></a>Interfaces propres au service

Microsoft permet de découvrir des données client directement via des interfaces de programmation d’applications (API) ou des interfaces utilisateur (UI) pré-existantes pour des services spécifiques. Vous trouverez des détails dans la documentation de référence des services respectifs, décrivant les opérations CRUD (créer, lire, mettre à jour, supprimer) applicables.

### <a name="notify-about-exporting-or-deleting-issues"></a>Notification des problèmes d’exportation ou de suppression

Si vous rencontrez des problèmes lorsque vous exportez ou supprimez des données sur le portail Azure, accédez au panneau **Aide + Support** du portail Azure et envoyez un nouveau ticket sous **Gestion des abonnements > Autre demande de conformité et de sécurité > Confidentialité et demandes dans le cadre du RGPD**.

## <a name="learn-more"></a>En savoir plus

- [Centre de gestion de la confidentialité Microsoft](https://www.microsoft.com/trust-center/privacy/gdpr-overview)
