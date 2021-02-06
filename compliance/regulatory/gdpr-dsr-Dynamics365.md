---
title: Demandes des personnes concernées par le traitement des données pour Dynamics 365 concernant le RGPD et le CCPA
description: Découvrez comment trouver des données personnelles et agir sur celles-ci, et de répondre aux demandes DPC et CCPA des clients Dynamics 365.
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
ms.custom:
- seo-marvel-mar2020
titleSuffix: Microsoft GDPR
ms.openlocfilehash: 231021c75031a290686027f55bca868f4d7ac317
ms.sourcegitcommit: 21ed42335efd37774ff5d17d9586d5546147241a
ms.translationtype: HT
ms.contentlocale: fr-FR
ms.lasthandoff: 02/05/2021
ms.locfileid: "50120943"
---
# <a name="dynamics-365-data-subject-requests-for-the-gdpr-and-ccpa"></a>Demandes des personnes concernées par le traitement des données pour Dynamics 365 concernant le RGPD et le CCPA

Le [Règlement général sur la protection des données (RGPD)](https://ec.europa.eu/justice/data-protection/reform/index_en.htm) de l’UE permet aux utilisateurs (désignés dans le règlement comme *personnes concernées*) de gérer les données à caractère personnel collectées par un employeur ou tout autre type d’organisme ou d’organisation (*responsable du traitement des données* ou *responsable du traitement*). Les données à caractère personnel sont définies de manière générale dans le cadre du RGPD comme correspondant aux données associées à une personne physique identifiée ou identifiable. Le RGPD octroie aux personnes concernées des droits spécifiques sur leurs données à caractère personnel. Ces droits incluent l’obtention de copies des données à caractère personnel, les demandes de changements de ces dernières, la restriction de leur traitement, leur suppression ou leur réception dans un format électronique afin de les transférer à un autre responsable du traitement. Toute demande formelle effectuée par une personne concernée à un responsable du traitement au sujet de la prise de mesure sur ses données à caractère personnel est appelée dans ce document *demande de droits de personne concernée* ou DPC.

De même, le CCPA (California Consumer Privacy Act) prévoit des droits de confidentialité et des obligations pour les consommateurs de la Californie, y compris des droits similaires aux droits des personnes concernées en vertu du RGPD, tels que le droit de supprimer, d’accéder et de recevoir (portabilité) leurs informations personnelles.  Le CCPA prévoit également des publications d’informations, des protections contre la discrimination des personnes faisant usage de leurs droits et la possibilité d’opter pour ou contre certains transferts de données classés en tant que « ventes ». Les ventes sont largement définies pour inclure le partage de données à des fins importantes. Pour plus d’informations sur le CCPA, voir le [California Consumer Privacy Act](offering-ccpa.md) et le [Forum aux questions California Consumer Privacy Act](ccpa-faq.md).

Le guide décrit comment utiliser les produits, les services et les outils d’administration de Microsoft pour aider les clients de notre entité de contrôle à rechercher des données personnelles et à prendre des mesures pour répondre aux demandes DPC. Plus précisément, il explique comment rechercher des données personnelles qui résident dans Microsoft Stream, comment y accéder et comment entreprendre une action sur ces données. Voici un aperçu rapide des processus présentés dans ce guide :

- **Découvrir** : utilisez les outils de recherche et de détection pour rechercher plus facilement les données du client qui peuvent faire l’objet d’une demande DPC. Une fois que vous avez collecté les documents susceptibles de répondre à la demande, vous pouvez effectuer une ou plusieurs des actions DPC décrites ci-après. Vous pouvez également décider que la demande ne satisfait pas aux directives de votre organisation en termes de réponse à une demande DPC.
- **Accéder :** récupérez des données à caractère personnel qui résident dans le cloud Microsoft et, si nécessaire, effectuez-en une copie pour la personne concernée.
- **Rectifier :** modifiez ou mettez en œuvre d’autres actions demandées sur les données à caractère personnel, le cas échéant.
- **Limiter** : limiter le traitement des données personnelles en supprimant les licences de différents services en ligne ou en désactivant les services souhaités lorsque c’est possible. Vous pouvez
- **Supprimer :** supprime définitivement des données à caractère personnel qui résidaient dans le cloud Microsoft.
- **Exporter/Recevoir (Portabilité) :** fournit une copie électronique (dans un format lisible par un ordinateur) des données ou des informations personnelles à la personne concernée. Les informations à caractère personnel sous CCPA englobent toutes les informations relatives à une personne identifiée ou identifiable. Aucune distinction n’est faite entre les rôles privé, public et professionnel d’une personne. Le terme défini « informations personnelles » est à peu près aligné sur celui de « données personnelles » dans le RGPD. Toutefois, le CCPA inclut également les données relatives à la famille et au foyer. Pour plus d’informations sur le CCPA, voir le [California Consumer Privacy Act](offering-ccpa.md) et le [Forum aux questions California Consumer Privacy Act](ccpa-faq.md).

Chaque section de ce guide décrit les procédures techniques qu’une organisation de contrôleur des données peut suivre pour répondre à une demande DCP pour des données personnelles dans le cloud de Microsoft.

## <a name="gdpr-terminology"></a>Terminologie RGPD

Vous trouverez ci-dessous la liste des définitions de termes utilisés dans ce guide :

- **Responsable du traitement des données :** la personne physique ou morale, l’autorité publique, le service ou tout autre organisme qui, seul ou conjointement avec d’autres, détermine les finalités et les moyens du traitement des données à caractère personnel ; lorsque les finalités et les moyens du traitement sont déterminés par la législation de l’Union ou des États membres, le responsable du traitement peut être désigné, ou les critères spécifiques relatifs à sa nomination être définis, par la législation de l’Union ou des États membres.
- **Données personnelles et personne concernée par le traitement des données :** informations relatives à une personne physique identifiée ou identifiable (« la personne concernée par le traitement des données ») ; une personne physique identifiable est une personne qui peut être identifiée, directement ou indirectement, notamment par référence à un identificateur par exemple, un nom, un numéro d’identification, des données de localisation, un identificateur en ligne, ou un ou plusieurs facteurs spécifiques de l’identité physique, physiologique, génétique, mentale, économique, culturelle ou sociale de cette personne physique.
- **Sous-traitant de données :** la personne physique ou morale, l’autorité publique, le service ou tout autre organisme qui traite des données à caractère personnel pour le compte du responsable du traitement.
- **Données client :** toutes les données, y compris tous les fichiers texte, son, vidéo ou image et les logiciels qui ont été fournis à Microsoft par le client ou pour son compte dans le cadre du service d’entreprise. Les données client incluent à la fois les (1) informations d’identification personnelle des utilisateurs finaux (par exemple, les noms d’utilisateur et les informations de contact dans Azure Active Directory) et le Contenu Client chargé ou créé par un client dans des services spécifiques (par exemple, le contenu client dans un compte de stockage Azure, le contenu client d’une base de données Azure SQL ou l’image de la machine virtuelle d’un client dans des machines virtuelles Azure).
- **Journaux générés par le système :** journaux et données associées générés par Microsoft qui permettent à Microsoft de fournir des services d’entreprise aux utilisateurs. Les journaux générés par le système contiennent essentiellement des données pseudonymes, généralement un numéro généré par le système qui ne permet pas, en soi, d’identifier une personne individuelle, mais qui est utilisé pour fournir les services d’entreprise aux utilisateurs. Les journaux générés par le système peuvent également contenir des informations d’identification personnelle sur les utilisateurs finaux, telles qu’un nom d’utilisateur.

## <a name="how-this-guide-can-help-you-meet-your-controller-responsibilities"></a>Assumer vos responsabilités de contrôleur grâce à ce guide

Le guide, divisé en deux parties, explique comment utiliser les produits, services et outils d’administration Dynamics 365 pour rechercher et manipuler les données dans le cloud Microsoft en réponse aux demandes des personnes concernées qui exercent leurs droits en vertu du GDPR. La première partie traite des données à caractère personnel incluses dans les données client. Elle est suivie d’une partie traitant des autres données à caractère personnel pseudonymes, consignées dans des journaux générés par le système.

- **Partie 1 : Répondre à des demandes de droits de la personne concernée (DPC) pour des données à caractère personnel incluses dans des données client.** La première partie de ce guide explique comment accéder à des données à caractère personnel, les rectifier, les limiter, les supprimer et les exporter à partir d’applications Dynamics 365 (software as a service – SaaS), qui sont traitées avec les données client que vous avez fournies au service en ligne.
- **Partie 2 : Répondre aux demandes de droits de la personne concernée pour les données sous pseudonyme :** lorsque vous utilisez les services Dynamics 365 Enterprise, Microsoft génère des informations (intitulées dans ce document *journaux générés par le système*) afin de fournir le service, limité à l’empreinte d’utilisation laissée par les utilisateurs finaux pour identifier leurs actions dans le système. Bien que ces données ne puissent pas être affectées à un sujet de données spécifique sans utiliser d’informations supplémentaires, certaines d’entre elles peuvent être considérées comme personnelles dans le cadre du RGPD . La deuxième partie de ce guide explique comment consulter, supprimer et exporter des journaux générés par le système produits par Dynamics 365.

## <a name="preparing-for-data-subject-rights-investigations"></a>Préparation des examens de droits des personnes concernées par le traitement des données

Lorsque des personnes associées aux données exercent leurs droits et effectuent des demandes, tenez compte des points suivants :

- Identifiez correctement la personne et le rôle (par exemple, employé, client, fournisseur) à l’aide des informations fournies par la personne concernée dans le cadre de sa demande. Ces informations peuvent être un nom, un ID d’employé ou un numéro de client, ou un autre identificateur.
- Enregistrez la date et l’heure de la demande. (Vous avez 30 jours pour effectuer la demande.)
- Vérifiez que la demande répond aux exigences de votre organisation pour honorer ou refuser la demande d’une personne concernée. Par exemple, vous devez vous assurer que l’exécution de la demande n’entre pas en conflit avec d’autres obligations réglementaires, juridiques ou financières que vous avez ou qu’elle n’enfreint pas les droits et les libertés d’autres individus.
- Vérifiez que vous disposez des informations liées à la demande.

## <a name="part-1-responding-to-data-subject-rights-requests-for-personal-data-included-in-customer-data"></a>Partie 1 : Répondre aux demandes de droits des personnes concernées relatives aux données à caractère personnel dans les données client

Dans les articles suivants, vous trouverez des informations qui vous aideront à préparer des DPC et à y répondre pour des données personnelles incluses dans des données client traitées dans Dynamics 365. Il est important de noter que des données personnelles peuvent être présentes dans d’autres catégories de données traitées par Microsoft au cours du service d’un abonnement à des services en ligne (comme, par exemple, des données administrateur ou des données de support définies dans la déclaration de confidentialité de Microsoft). Ce document n’a pour but que de vous aider dans la découverte et la gestion des DPC qui concernent les données personnelles présentes dans les données client que vous avez fournies à Dynamics 365.

Dynamics 365 est un service en ligne qui propose plusieurs fonctionnalités de traitement des données comme un service SaaS. Ainsi, Dynamics 365 offre un large éventail de fonctionnalités conçues pour traiter une collection diversifiée de données, pouvant varier par nature, objectif ou autres attributs spécifiques (données de ventes, transactions, données financières, informations de RH, etc.). Compte tenu de cette diversité, Dynamics 365 propose plusieurs formulaires, champs, schémas, points de terminaison et logiques pour traiter les données client, et ceci se reflète aussi dans les différentes façons qui permettent de traiter des demandes DSR dans chaque application. Lorsque des applications Dynamics 365 proposent plusieurs méthodes pour traiter des demandes DSR spécifiques, nous les noterons dans ce guide en pointant vers les descriptions techniques offertes par chaque application.

### <a name="dynamics-365"></a>Dynamics 365

#### <a name="finding-customer-data"></a>Consultation des données client

La première étape pour répondre à une demande de droits de la personne concernée consiste à rechercher et identifier les données client faisant l’objet de la demande.

La classification appropriée des données client est à la base de la gestion des données personnelles dans les applications métier Dynamics 365 Customer Engagement. Dynamics 365 for Customer Engagement permet de créer une extension d’application autour de la classification des données avec une grande souplesse. La classification vous permet d’identifier les informations comme données personnelles, et ainsi de les localiser et les récupérer lorsque vous répondez aux demandes d’une personne concernée. Elle permet également d’assurer la conformité avec les exigences réglementaires et législatives pour la collecte et la gestion des données personnelles.

Microsoft offre des fonctionnalités qui vous aident à répondre aux demandes de droits de la personne concernée par le traitement des données, et par conséquent d’accéder aux données client. Toutefois, il est de votre responsabilité de vérifier que les données personnelles sont localisées et classées de façon appropriée.

L’offre ***Dynamics 365 for Customer Engagement*** fournit plusieurs méthodes qui vous permettent de rechercher des données personnelles dans des enregistrements, telles que : la recherche avancée et la recherche d’enregistrements. Toutes ces fonctions vous permettent d’identifier (rechercher) des données personnelles.

- [Recherche avancée](/dynamics365/customer-engagement/basics/save-advanced-find-search)
- [Recherche d’enregistrements](/dynamics365/customer-engagement/basics/search-records) dans plusieurs types d’enregistrements

Dans Dynamics 365 for Marketing, vous disposez des fonctionnalités supplémentaires suivantes :

1. [Générer des rapports Power BI](/power-bi/service-connect-to-microsoft-dynamics-crm) afin de filtrer et identifier des données client.
2. Utilisez les affichages Insight sur les contacts et les objets de l’exécution marketing pour identifier des points de données supplémentaires pouvant contenir des données client.

***Dynamics 365 Customer Service Insights*** propose une liste de ressources destinée à vous aider à [trouver des données client](/dynamics365/ai/customer-service-insights/gdpr-discovery) afin de répondre aux demandes RGPD des clients.

L’offre ***Dynamics 365 for Finance and Operations*** permet de rechercher des données client de plusieurs façons. En tant qu’administrateur client, vous pouvez rechercher des données client en effectuant les opérations suivantes :

- Organisez vos données client de façon à découvrir rapidement des données personnelles ; à cette fin, apprenez à [classifier l’inventaire des données](/dynamics365/unified-operations/dev-itpro/gdpr/gdpr-guide#detailed-inventory).
- Utilisez le [rapport de recherche de données personnelles](/dynamics365/unified-operations/dev-itpro/gdpr/gdpr-guide#the-person-search-report) pour rechercher et collecter des données personnelles.
- [Étendez le rapport de recherche de données personnelles](/dynamics365/unified-operations/dev-itpro/gdpr/gdpr-extend-person-search-report) en créant une entité ou en étendant une entité existante.
- Utilisez les fonctionnalités de recherche et de filtre pour rechercher des données personnelles spécifiques et les exporter à l’aide de la fonctionnalité Exporter de Microsoft Office ou imprimez ces informations dans un fichier .pdf à l’aide d’extensions de navigateur.
- Créez un formulaire personnalisé qui localise et exporte les données personnelles.
- Créez un portail externe ou un site web qui permet à un client authentifié d’afficher ses données personnelles.

***Dynamics 365 Business Central*** offre plusieurs façons de rechercher des données client. Pour plus d’informations, consultez [Recherche, filtrage et tri de données](/dynamics365/business-central/ui-enter-criteria-filters).

Dynamics 365 for Talent fournit des fonctionnalités de recherche et de filtre avancées permettant de rechercher des données personnelles spécifiques ainsi que la fonctionnalité Exporter de Microsoft Office pour exporter ou imprimer ces informations dans un fichier .pdf à l’aide d’extensions de navigateur.

- Utilisez le [rapport de recherche de données personnelles](/dynamics365/unified-operations/dev-itpro/gdpr/gdpr-guide#the-person-search-report) pour rechercher et collecter des données client.
- [Étendez le rapport de recherche de données personnelles](/dynamics365/unified-operations/dev-itpro/gdpr/gdpr-extend-person-search-report) en créant une entité ou en étendant une entité existante.

### <a name="providing-a-copy-of-customer-data"></a>Fourniture d’une copie des données client

Les données client contenues dans ***Dynamics 365 for Customer Engagement*** peuvent être exportées à l’aide des fonctionnalités d’exportation d’entités complètes. Les données client peuvent être exportées dans un fichier Excel statique pour faciliter une demande de portabilité des données. En utilisant Excel, vous pouvez alors modifier les données personnelles à inclure dans la demande de portabilité et les enregistrer ensuite dans un format courant lisible par un ordinateur comme .csv ou .xml. Dynamics 365 for Customer Engagement peut également être exporté via [l’API Web Common Data Service](/powerapps/developer/common-data-service/webapi/overview).

En outre, pour Dynamics 365 for Marketing, une [API dédiée](/dynamics365/customer-engagement/marketing/developer/retrieve-interactions-contact) est fournie pour permettre au client de générer des extensions qui récupèrent des enregistrements supplémentaires des interactions client capturées pouvant contenir des données personnelles. L’API charge toutes les informations pertinentes à partir du système principal et les assemble dans un document unique portable.

***Dynamics 365 Customer Service Insights*** vous permet de [fournir une copie des données client](/dynamics365/ai/customer-service-insights/gdpr-export) via l’exportation de données.

Les données des clients dans ***Dynamics 365 pour les finances et les opérations** _ peuvent être exportées en utilisant les capacités d'exportation complètes des entités. En utilisant [_les entités de gestion et d'intégration des données*](/dynamics365/unified-operations/dev-itpro/data-entities/data-management-integration-data-entity), l'administration des locataires peut utiliser les entités fournies, créer de nouvelles entités ou étendre les entités existantes pour une exportation répétable de données personnelles vers Excel ou un certain nombre d'autres formats communs en utilisant [*les tâches d'importation et d'exportation de données*](/dynamics365/unified-operations/dev-itpro/data-entities/data-import-export-job).  De nombreuses listes peuvent aussi être exportées dans un fichier Excel statique pour faciliter une demande de portabilité des données. Une fois que les données client sont exportées dans Excel, vous pouvez modifier les données personnelles à inclure dans la demande de portabilité et enregistrer ensuite le fichier dans un format courant lisible par un ordinateur comme .csv ou .xml. Vous pouvez aussi envisager d’utiliser le *Rapport de recherche de données personnelles* pour fournir à la personne concernée les données que vous avez classifiées en tant que données personnelles.

Dans ***Dynamics 365 Business Central***, vous pouvez utiliser deux fonctionnalités pour fournir une copie des données client à une personne concernée :

Vous pouvez exporter les données client dans un fichier Excel. Dans Excel, vous pouvez ensuite modifier les données client à inclure dans la demande de portabilité et les enregistrer dans un format courant lisible par un ordinateur comme .csv ou .xml. Pour plus d’informations, consultez [Exportation de vos données métier dans Excel.](/dynamics365/business-central/about-export-data)

Dans ***Dynamics 365 for Talent***, vous pouvez utiliser [Étendre le rapport de recherche des données personnelles](/dynamics365/unified-operations/dev-itpro/gdpr/gdpr-extend-person-search-report) pour collecter des informations et répondre à une demande de copie des données personnelles de la personne concernée.

### <a name="rectifying-customer-data"></a>Rectification des données client

L’offre ***Dynamics 365 for Customer Engagement*** propose les méthodes suivantes pour corriger des données client inexactes ou incorrectes, ou effacer des données client :

- Recherchez des données client à l’aide des fonctionnalités mentionnées dans « Consultation des données client » et modifiez directement les données dans les formulaires Customer Engagement. Les modifications peuvent être effectuées au niveau d’une ligne unique ou plusieurs lignes peuvent être modifiées directement.
- Grâce à la modification en bloc de plusieurs enregistrements Customer Engagement, vous pouvez utiliser le complément Microsoft Office pour exporter des données vers Microsoft Excel, apporter vos changements puis importer ces données modifiées dans Dynamics 365 for Customer Engagement.

En outre, pour Dynamics 365 for Marketing, vous pouvez aussi :

- Mettre à jour la page d’accueil de vos données en modifiant une ou plusieurs lignes directement
- Préparez une page de [centres d’abonnement](/dynamics365/customer-engagement/marketing/set-up-subscription-center) comportant autant de champs de contact modifiables que possible. Cette page permet à un utilisateur final de mettre à jour ses informations autant que possible.

***Dynamics 365 Customer Service Insights*** offre également des fonctionnalités qui permettent aux organisations de [rectifier ou d’apporter des modifications aux données client](/dynamics365/ai/customer-service-insights/gdpr-summary).

Dans ***Dynamics 365 pour les finances et les opérations** _, vous pouvez également utiliser des [_outils de personnalisation*](/dynamics365/unified-operations/dev-itpro/dev-tools/developer-home-page), mais la décision et la mise en œuvre sont de votre responsabilité.

L’offre ***Dynamics 365 Business Central*** propose deux façons de corriger des données client inexactes ou incomplètes.

Pour modifier en bloc plusieurs enregistrements Business Central, vous pouvez exporter des listes vers Excel à l’aide du [complément Excel de Business Central](/dynamics365/business-central/finance-analyze-excel#the--excel-add-in) afin de corriger plusieurs enregistrements, puis publier les données modifiées dans Excel dans Business Central. Pour plus d’informations, consultez la section [Exportation de vos données métiers dans Excel](/dynamics365/business-central/about-export-data).

Vous pouvez modifier les données client stockées dans un champ (par exemple, les informations sur un client dans sa fiche) en modifiant manuellement l’élément de données contenant les données personnelles cibles. Pour plus d’informations, consultez [Entrée de données](/dynamics365/business-central/ui-enter-data).

#### <a name="brief-note-about-modifying-entries-in-business-transactions"></a>Remarque sur la modification des entrées dans les transactions commerciales

Les enregistrements de transaction tels que les entrées de comptabilité grand livre, client et générale sont essentiels pour l’intégrité du système de planification des ressources d’une entreprise. Les données personnelles faisant partie d’une transaction financière ou autre sont conservées « telles quelles » à des fins de conformité avec les lois financières (législation fiscale, par exemple), prévention contre les fraudes (piste d’audit de sécurité) ou conformité avec les certifications de l’industrie. Par conséquent, Dynamics 365 for Finance and Operations et Dynamics 365 Business Central limitent la modification des données dans les enregistrements de ce type.

Si vous stockez des données personnelles dans des enregistrements de transaction commerciale, la seule façon de corriger, supprimer ou limiter le traitement des données personnelles pour honorer la demande d’une personne concernée est d’utiliser les [fonctionnalités de personnalisation](/dynamics365/business-central/dev-itpro/index) de Dynamics 365 Business Central. [La décision d’honorer la demande de modification](/dynamics365/unified-operations/dev-itpro/gdpr/gdpr-guide#reasons-why-certain-personal-data-may-not-be-modified-or-deleted) et d’implémentation d’une personne concernée relève de votre responsabilité.

### <a name="restricting-the-processing-of-customer-data"></a>Restriction du traitement des données client

Quand vous recevez une demande d’une personne concernée pour limiter le traitement de données client, vous pouvez facilement extraire les données client en question du service en ligne et les stocker dans un conteneur distinct (stockage local ou service web distinct doté de fonctionnalités d’isolation des données) isolé des fonctions de traitement offertes par les applications cloud.

Un mécanisme de substitution comme le blocage du traitement des données est proposé par ***Dynamics 365 Business Central***, qui permet aux utilisateurs de bloquer l’enregistrement d’une personne concernée par le traitement des données. Pour plus d’informations, consultez [Restreindre le traitement des données pour un sujet données](/dynamics365/business-central/admin-responding-to-requests-about-personal-data#restrict-data-processing-for-a-data-subject). Quand un enregistrement est marqué comme étant bloqué, Dynamics 365 Business Central interrompt le traitement des données de la personne concernée. Vous ne pouvez pas créer des transactions qui utilisent un enregistrement bloqué ; par exemple, vous ne pouvez pas créer une facture pour un client, du moment que ledit client ou le commercial est bloqué.

### <a name="deleting-customer-data"></a>Suppression des données client

Quand une personne concernée vous demande de supprimer ses données client, vous pouvez le faire de plusieurs façons :

- Grâce à la modification en bloc de plusieurs enregistrements Dynamics 365, vous pouvez utiliser le complément Microsoft Office pour exporter des données vers Microsoft Excel, apporter vos changements puis importer ces données modifiées d’Excel dans le service en ligne.
- Vous pouvez supprimer des données client stockées dans un champ en localisant les données à supprimer puis en supprimant manuellement l’élément de données contenant les données client cibles (par exemple, en supprimant définitivement l’enregistrement de contact représentant la personne concernée et d’autres enregistrements contenant des données personnelles).

Par ailleurs, dans le cas de Dynamics 365 Marketing, la suppression d’un contact s’accompagne de la suppression des données d’interaction avec les informations personnelles. Pour les entités ou les champs personnalisés, vous devez personnaliser votre système pour faire en sorte qu’il supprime toutes les données client des enregistrements connexes et/ou les dissocie de l’enregistrement de contact afin que toutes les informations personnelles soient supprimées. Pour plus d’informations, consultez le [Guide du développeur (Marketing)](/dynamics365/customer-engagement/marketing/developer/marketing-developer-guide).

***Dynamics 365 Customer Service Insights*** dote également les organisations de fonctionnalités permettant de [supprimer les données client](/dynamics365/ai/customer-service-insights/gdpr-delete).

Alternativement, dans ***Dynamics 365 pour les finances et les opérations** _, vous pouvez utiliser des [_outils de personnalisation*](/dynamics365/unified-operations/dev-itpro/dev-tools/developer-home-page)pour effacer/modifier les données des clients.

Dans ***Dynamics 365 Business Central***, quand une personne concernée vous demande de supprimer ses données personnelles qui se trouvent dans vos données client, vous pouvez satisfaire cette demande de différentes façons :

- Pour modifier en bloc plusieurs enregistrements Business Central, vous pouvez exporter des données vers Excel à l’aide du [complément Excel de Business Central](/dynamics365/business-central/finance-analyze-excel#the--excel-add-in) afin de supprimer plusieurs enregistrements, puis publier ces changements d’Excel dans Business Central. Pour plus d’informations, consultez la section [Exportation de vos données métiers dans Excel](/dynamics365/business-central/about-export-data).
- Vous pouvez supprimer les données client stockées dans un champ en supprimant manuellement l’élément de données contenant les données client cibles. Pour plus d’informations, consultez [Entrée de données](/dynamics365/business-central/ui-enter-data).
- Vous pouvez supprimer des données client directement, par exemple en supprimant un contact et en exécutant ensuite le traitement par lot Supprimer les écritures journal d’interaction annulées pour supprimer les interactions pour ce contact.
- Vous pouvez [supprimer des documents](/dynamics365/business-central/admin-manage-documents) contenant des données client (par exemple, des mémos, des ventes enregistrées et des factures d’achat).

Outre la suppression en bloc ou individuelle d’enregistrements distincts, veuillez noter que seuls les travailleurs licenciés peuvent être totalement supprimés de ***Dynamics 365 for Talent***. [Suivez ces étapes pour supprimer des travailleurs licenciés](/dynamics365/unified-operations/dev-itpro/gdpr/respond-dsr-request-talent#additional-notes-that-apply-to-requests-for-personal-data).

### <a name="exporting-customer-data"></a>Exportation des données client

Pour répondre à une demande de portabilité des données, les données client contenues dans ***Dynamics 365 for Customer Engagement*** peuvent être exportées à l’aide des fonctionnalités d’exportation d’entités complètes. Les données client peuvent être exportées dans un fichier Excel statique pour faciliter une demande de portabilité des données. En utilisant Excel, vous pouvez alors modifier les données personnelles à inclure dans la demande de portabilité et les enregistrer ensuite dans un format courant lisible par un ordinateur comme .csv ou .xml.

En outre, pour Dynamics 365 for Marketing, une [API dédiée](/dynamics365/customer-engagement/marketing/developer/retrieve-interactions-contact) est fournie pour permettre au client de générer des extensions qui récupèrent des enregistrements supplémentaires des interactions client capturées pouvant contenir des données personnelles. L’API charge toutes les informations pertinentes à partir du système principal et les assemble dans un document unique portable.

Pour ***Dynamics 365 Customer Service Insights***, vous devez [exporter les données clients](/dynamics365/ai/customer-service-insights/gdpr-export) via le portail de gestion Azure.

***Dynamics 365 pour la finance et les opérations*** offre [Entités de gestion des données et d’intégration qui permet aux entités fournies, aux entités nouvellement créées ou aux entités étendues d’une exportation de données personnelles répétitives vers Excel ou divers autres formats courants utilisant les [tâches d’importation et d’exportation de données](/dynamics365/unified-operations/dev-itpro/data-entities/data-import-export-job).  De nombreuses listes peuvent aussi être exportées dans un fichier Excel statique pour faciliter une demande de portabilité des données. Quand les données client sont exportées dans Excel de cette façon, vous pouvez modifier les données personnelles à inclure dans la demande de portabilité et enregistrer ensuite le fichier dans un format courant lisible par un ordinateur comme .csv ou .xml.

Dynamics 365 for Finance and Operations et ***Dynamics 365 for Talent*** fournissent un rapport de recherche des données personnelles pour fournir les données que vous avez classées comme données personnelles à la personne concernée par le traitement des données.

L’offre ***Dynamics 365 Business Central*** propose les fonctionnalités suivantes :

- Vous pouvez exporter les données client dans un fichier Excel. Dans Excel, vous pouvez ensuite modifier les données client à inclure dans la demande de portabilité et les enregistrer dans un format courant lisible par un ordinateur comme .csv ou .xml. Pour plus d’informations, consultez [Exportation de vos données métier dans Excel](/dynamics365/business-central/about-export-data).
- Vous pouvez exporter les données client dans un fichier Excel. Dans Excel, vous pouvez ensuite modifier les données client à inclure dans la demande de portabilité et les enregistrer dans un format courant lisible par un ordinateur comme .csv ou .xml. Pour plus d’informations, consultez [Exportation de vos données métier dans Excel](/dynamics365/business-central/about-export-data).


## <a name="part-2-responding-to-dsrs-for-system-generated-logs"></a>Partie 2 : Répondre à des DSR pour les journaux générés par le système

Microsoft permet également de consulter, d’exporter et de supprimer les journaux générés par le système qui peuvent être considérés personnels en vertu de la définition large des « données personnelles » du RGPD. Voici des exemples de journaux générés par le système qui peuvent être considérés comme personnels en vertu du RGPD :

- Données relatives à l’utilisation de produits et de services tels que les journaux d’activité des utilisateurs
- Requêtes de recherche et données de requête des utilisateurs
- Données générées par les produits et services comme étant un produit des fonctionnalités du système et de l’interaction par les utilisateurs ou d’autres systèmes

La possible de limiter ni de rectifier les données contenues dans des journaux générés par le système. Les données contenues dans des journaux générés par le système forment des actions factuelles effectuées dans le cloud Microsoft et les données de diagnostic, et des modifications apportées à ces données compromettraient l’enregistrement historique des actions, augmentant ainsi les risques de fraude et de sécurité.

### <a name="accessing-and-exporting-system-generated-logs"></a>Consultation et exportation des journaux générés par le système

Les administrateurs peuvent accéder aux journaux générés par le système associés à une utilisation particulière d’un utilisateur des applications et des services Dynamics 365. Pour accéder aux journaux générés par le système et les exporter, procédez comme suit :

1. Accédez au [portail d’approbation de service Microsoft](https://servicetrust.microsoft.com/) et connectez-vous en utilisant les identifiants d’un administrateur général Dynamics 365.
2. Dans la liste déroulante **Confidentialité** en haut de la page, cliquez sur **Demande des personnes concernées**.
3. Dans la page **Demande des personnes concernées**, sous **Journaux générés par le système**, cliquez sur **Exportation des journaux de données**.
    > [!NOTE]
    > L’**Exportation des journaux de données** s’affiche. Notez que la liste des demandes de données d’exportation transmises par votre organisation s’affiche.
4. Pour créer une demande pour un utilisateur, cliquez sur **Créer une demande de données d’exportation**.

Une fois la demande créée, elle apparaît sur la page **Exportation des journaux de données** où vous pouvez suivre son statut. Lorsqu’une demande est terminée, vous pouvez cliquer sur un lien pour accéder aux journaux générés par le système qui sont exportés vers l’emplacement de stockage Azure de votre organisation dans les 30 jours suivant la création de la demande. Les données sont enregistrées dans un format de fichier courant lisible par une machine tel que JSON ou XML. Si vous n’avez pas de compte Azure ni d’emplacement de stockage Azure, vous devez créer un compte Azure ou un emplacement de stockage Azure pour votre organisation de sorte que l’outil Exportation des journaux de données puisse exporter les journaux générés par le système. 

Azure prend en charge cette demande en permettant à votre organisation d’exporter les données au format JSON natif vers votre conteneur de stockage Azure spécifié[. Article de présentation du Stockage Microsoft Azure – Stockage Blob](/azure/storage/common/storage-introduction#blob-storage). Les données récupérées n’incluent pas de données susceptibles de compromettre la sécurité et la stabilité du service.

> [!IMPORTANT]
> Pour exporter des données utilisateur à partir du client, vous devez être un administrateur client.

Le tableau suivant récapitule la consultation et l’exportation des journaux générés par le système :

| **Question** | **Réponse** |
|:----|:---|
|**Combien de temps faut-il à l’outil Exportation des journaux de données de Microsoft pour exécuter une demande ?**| Cela peut dépendre de plusieurs facteurs. Dans la plupart des cas, il nécessite un ou deux jours, mais cela peut prendre jusqu’à 30 jours. |
|**Quel est le format de sortie ?**| La sortie sera structurée sous forme de fichiers lisibles par une machine, comme XML, CSV ou JSON. |
|**Quelles données l’outil d’exportation des journaux de données renvoie-t-il ?**| L’outil Exportation des journaux de données renvoie les journaux générés par le système que Microsoft stocke. Les données exportées englobent différents services Microsoft, dont Office 365, Azure et Dynamics. |
|***Qui a accès à l’outil Exportation des journaux de données pour demander l’accès à des journaux générés par le système ?**| Les administrateurs généraux Dynamics 365 auront accès à l’utilitaire du gestionnaire des journaux du RGPD. |
|**Comment les données sont-elles renvoyées à l’utilisateur ?**| Les données sont exportées vers l’emplacement de stockage Azure de votre organisation. Les administrateurs de votre organisation doivent ensuite déterminer comment ils souhaitent afficher/renvoyer ces données aux utilisateurs. |
|**À quoi ressemblent les données dans les journaux générés par le système ?**| Exemple d’enregistrement de journal généré par le système au format JSON : <br><br> "DateTime": "2017-04-28T12:09:29-07:00", <br> "AppName": "SharePoint", <br> "Action": "OpenFile", <br> "IP": "154.192.13.131", <br> "DevicePlatform": "Windows 1.0.1607" |

### <a name="deleting-system-generated-logs"></a>Suppression des journaux générés par le système

Pour supprimer les journaux générés par le système récupérés via une demande d’accès, vous devez supprimer l’utilisateur du service et supprimer définitivement son compte Azure Active Directory. Pour obtenir des instructions sur la suppression définitive d’un utilisateur, consultez la section [Étape 5 : supprimer](gdpr-dsr-azure.md#step-5-delete) dans la rubrique demandes d’objet Azure Data. Il est important de noter que la suppression définitive d’un compte d’utilisateur est irréversible une fois lancée. La suppression définitive d’un compte d’utilisateur supprimera les données de l’utilisateur des journaux générés par le système, à l’exception des données qui peuvent compromettre la sécurité ou la stabilité du service, pour pratiquement tous les services Dynamics 365 dans un délai de 30 jours.

## <a name="learn-more"></a>En savoir plus

- [Centre de gestion de la confidentialité Microsoft](https://www.microsoft.com/trust-center/privacy/gdpr-overview)
