---
title: Chiffrement pour Skype, OneDrive, SharePoint et Exchange
description: 'Résumé : Description du chiffrement pour Skype, OneDrive, SharePoint, Microsoft Teams et Exchange Online.'
ms.author: krowley
author: kccross
manager: laurawi
ms.reviewer: sosstah
f1.keywords:
- NOCSH
audience: ITPro
ms.topic: article
ms.service: O365-seccomp
localization_priority: None
search.appverid:
- MET150
ms.collection:
- Strat_O365_Enterprise
- M365-security-compliance
- Strat_O365_Enterprise
- SPO_Content
- MS-Compliance
titleSuffix: Microsoft Service Assurance
hideEdit: true
ms.openlocfilehash: 3907a9a3f085af3d778daa2a385209f4dc9699a4
ms.sourcegitcommit: 024137a15ab23d26cac5ec14c36f3577fd8a0cc4
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 04/01/2021
ms.locfileid: "51497551"
---
# <a name="encryption-for-skype-for-business-onedrive-for-business-sharepoint-online-microsoft-teams-and-exchange-online"></a>Chiffrement pour Skype Entreprise, OneDrive Entreprise, SharePoint Online, Microsoft Teams et Exchange Online

Microsoft 365 est un environnement hautement sécurisé qui offre une protection étendue en plusieurs couches : sécurité du centre de données physique, sécurité réseau, sécurité d’accès, sécurité des applications et sécurité des données.

## <a name="skype-for-business"></a>Skype Entreprise

Les données client Skype Entreprise peuvent être stockées au repos sous la forme de fichiers ou de présentations téléchargés par les participants à la réunion. Le serveur de conférence Web chiffre les données client à l’aide d’AES avec une clé 256 bits. Les données client chiffrées sont stockées sur un partage de fichiers. Chaque élément de données client est chiffré à l’aide d’une clé 256 bits générée de manière aléatoire. Lorsqu’un élément de données client est partagé dans une conférence, le serveur de conférence Web demande aux clients de conférence de télécharger les données client chiffrées via HTTPS. Il envoie la clé correspondante aux clients afin que les données client soient déchiffrées. Le serveur de conférence Web authentifiera également les clients de conférence avant d’autoriser les clients à accéder aux données client de conférence. Lorsque vous rejoignez une conférence Web, chaque client de conférence établit une boîte de dialogue SIP avec le composant focus de conférence s’exécutant d’abord à l’intérieur du serveur frontal sur TLS. Le focus de conférence transmet au client de conférence un cookie d’authentification généré par le serveur de conférence Web. Le client de conférence se connecte ensuite au serveur de conférence Web en présentant le cookie d’authentification à authentifier par le serveur.

## <a name="sharepoint-online-and-onedrive-for-business"></a>Sharepoint Online et OneDrive Entreprise

Tous les fichiers clients dans SharePoint Online sont protégés par des clés uniques par fichier qui sont toujours exclusives à un seul client. Les clés sont créées et gérées par le service SharePoint Online, ou lorsque la clé client est utilisée, créée et gérée par les clients. Lorsqu’un fichier est téléchargé, le chiffrement est effectué par SharePoint Online dans le contexte de la demande de chargement, avant d’être envoyé au stockage Azure. Lorsqu’un fichier est téléchargé, SharePoint Online récupère les données client chiffrées à partir du stockage Azure en fonction de l’identificateur de document unique et déchiffre les données client avant de les envoyer à l’utilisateur. Le stockage Azure n’a pas la possibilité de déchiffrer, ni même d’identifier ou de comprendre les données client. Tout le chiffrement et le déchiffrement se produisent dans les mêmes systèmes qui appliquent l’isolation du client, à l’est d’Azure Active Directory et de SharePoint Online.

Plusieurs charges de travail dans Microsoft 365 stockent des données dans SharePoint Online, notamment Microsoft Teams, qui stocke tous les fichiers dans SharePoint Online, et OneDrive Entreprise, qui utilise SharePoint Online pour son stockage. Toutes les données client stockées dans SharePoint Online sont chiffrées (avec une ou plusieurs clés AES 256 bits) et distribuées dans le centre de données comme suit. (Chaque étape de ce processus de chiffrement est validée au niveau 2 fiPS 140-2. Pour plus d’informations sur la conformité FIPS 140-2, consultez la conformité [FIPS 140-2.)](/previous-versions/sql/sql-server-2008-r2/bb326611(v=sql.105))

- Chaque fichier est divisé en un ou plusieurs blocs, selon la taille du fichier. Chaque bloc est chiffré à l’aide de sa propre clé AES 256 bits unique.
- Lorsqu’un fichier est mis à jour, la mise à jour est gérée de la même manière : la modification est divisée en un ou plusieurs blocs, et chaque bloc est chiffré avec une clé unique distincte.
- Ces blocs (fichiers, parties de fichiers et deltas de mise à jour) sont stockés sous forme d’objets blob dans le stockage Azure et répartis de manière aléatoire sur plusieurs comptes de stockage Azure.
- L’ensemble des clés de chiffrement pour ces blocs de données client est lui-même chiffré.

    - Les clés utilisées pour chiffrer les blobs sont stockées dans la base de données de contenu SharePoint Online.
    - La base de données de contenu est protégée par les contrôles d’accès à la base de données et le chiffrement au repos. Le chiffrement est effectué à l’aide du chiffrement [transparent](/sql/relational-databases/security/encryption/transparent-data-encryption-tde) des données (TDE) dans [azure SQL base de données.](/azure/sql-database/sql-database-technical-overview) (Azure SQL Database est un service de base de données relationnelle à usage général dans Microsoft Azure qui prend en charge des structures telles que les données relationnelles, JSON, spatial et XML.) Ces secrets sont au niveau du service pour SharePoint Online, et non au niveau du client. Ces clés secrètes (parfois appelées clés principales) sont stockées dans un référentiel sécurisé distinct appelé magasin de clés. TDE assure la sécurité au repos pour la base de données active, les sauvegardes de base de données et les journaux de transactions.
    - Lorsque les clients fournissent la clé facultative, la clé client est stockée dans Azure Key Vault et le service utilise la clé pour chiffrer une clé de client, qui est utilisée pour chiffrer une clé de site, qui est ensuite utilisée pour chiffrer les clés de niveau fichier. En fait, une nouvelle hiérarchie de clés est introduite lorsque le client fournit une clé.
- La carte utilisée pour assembler à nouveau le fichier est stockée dans la base de données de contenu avec les clés chiffrées, séparément de la clé principale nécessaire pour les déchiffrer.
- Chaque compte de stockage Azure possède ses propres informations d’identification uniques par type d’accès (lecture, écriture, éumérer et supprimer). Chaque jeu d’informations d’identification est conservé dans le magasin de clés sécurisé et est régulièrement actualisé. Comme décrit ci-dessus, il existe trois types différents de magasins, chacun avec une fonction distincte :
    - Les données client sont stockées en tant qu’objets blob chiffrés dans le stockage Azure. La clé de chaque bloc de données client est chiffrée et stockée séparément dans la base de données de contenu. Les données client elles-mêmes ne sont pas des indices quant à la façon dont elles peuvent être déchiffrées.
    - La base de données de contenu est une base de données SQL Server. Il contient la carte requise pour localiser et réassembler les blobs de données client détenus dans le stockage Azure, ainsi que les clés nécessaires pour chiffrer ces objets blob. Toutefois, l’ensemble de clés est lui-même chiffré (comme expliqué ci-dessus) et conservé dans un magasin de clés distinct.
    - Le magasin de clés est physiquement distinct de la base de données de contenu et du stockage Azure. Il contient les informations d’identification de chaque conteneur de stockage Azure et la clé principale de l’ensemble de clés chiffrées dans la base de données de contenu.

Chacun de ces trois composants de stockage (le magasin d’objets blob Azure, la base de données de contenu et le magasin de clés) est physiquement distinct. Les informations détenues dans l’un des composants ne sont pas utilisables seules. Sans l’accès aux trois, il est impossible d’extraire les clés des blocs, de les déchiffrer pour les rendre utilisables, d’associer les clés à leurs blocs correspondants, de déchiffrer chaque bloc ou de reconstruire un document à partir de ses blocs constituants.

Les certificats BitLocker, qui protègent les volumes de disque physique sur les ordinateurs du centre de données, sont stockés dans un référentiel sécurisé (banque secrète SharePoint Online) protégé par la clé de batterie de serveurs.

Les clés TDE qui protègent les clés par objet blob sont stockées à deux emplacements :

- Référentiel sécurisé, qui héberge les certificats BitLocker et est protégé par la clé de batterie de serveurs ; et
- Dans un référentiel sécurisé géré par Azure SQL Database.

Les informations d’identification utilisées pour accéder aux conteneurs de stockage Azure sont également conservées dans le magasin secret SharePoint Online et déléguées à chaque batterie de serveurs SharePoint Online si nécessaire. Ces informations d’identification sont des signatures SAS de stockage Azure, avec des informations d’identification distinctes utilisées pour lire ou écrire des données, et avec une stratégie appliquée afin qu’elles expirent automatiquement tous les 60 jours. Des informations d’identification différentes sont utilisées pour lire ou écrire des données (pas les deux) et les batteries de serveurs SharePoint Online ne sont pas autorisées à l’émanation.

> [!NOTE]
> Pour les clients Office 365 pour le gouvernement américain, les objets blob de données sont stockés dans le stockage Azure U.S. Government. En outre, l’accès aux clés SharePoint Online dans Office 365 pour le gouvernement américain est limité au personnel Office 365 qui a été spécifiquement projeté. Azure U.S. Government operations staff do not have access to the SharePoint Online key store that is used for encrypting data blobs.

Pour plus d’informations sur le chiffrement des données dans SharePoint Online et OneDrive Entreprise, voir Chiffrement de données dans OneDrive Entreprise [et SharePoint Online.](https://technet.microsoft.com/library/dn905447.aspx)

### <a name="list-items-in-sharepoint-online"></a>Éléments de liste dans SharePoint Online

Les éléments de liste sont des blocs plus petits de données client créés ad hoc ou qui peuvent être dynamiquement au sein d’un site, tels que des lignes dans une liste créée par l’utilisateur, des billets individuels dans un blog SharePoint Online ou des entrées dans une page Wiki SharePoint Online. Les éléments de liste sont stockés dans la base de données de contenu (base de données Azure SQL) et protégés avec TDE.

## <a name="encryption-of-data-in-transit"></a>Chiffrement des données lors de leur transport

Dans OneDrive Entreprise et SharePoint Online, il existe deux scénarios dans lesquels les données entrent et sortent des centres de données.

- **Communication du client avec le serveur** : la communication avec SharePoint Online et OneDrive Entreprise sur Internet utilise des connexions TLS.
- **Déplacement de données entre des centres** de données : la principale raison de déplacer des données entre des centres de données est la réplication géographique afin d’activer la récupération d’urgence. Par exemple, les deltas de stockage d'objets blob et les journaux de transaction SQL Server transitent par ce canal. Alors que ces données sont déjà transmises par le biais d'un réseau privé, elles sont encore mieux protégées à l'aide du meilleur chiffrement de sa catégorie.

## <a name="exchange-online"></a>Exchange Online

Exchange Online utilise BitLocker pour toutes les données de boîte aux lettres, et la configuration BitLocker est décrite dans [BitLocker pour le chiffrement.](/microsoft-365/compliance/office-365-bitlocker-and-distributed-key-manager-for-encryption) Le chiffrement au niveau du service chiffre toutes les données de boîte aux lettres au niveau de la boîte aux lettres. 

En plus du chiffrement de service, Microsoft 365 prend en charge la clé client, qui est conçue sur le chiffrement de service. La clé client est une option de clé gérée par Microsoft pour le chiffrement de service Exchange Online, qui se trouve également dans la feuille de route de Microsoft. Cette méthode de chiffrement offre une protection accrue non offerte par BitLocker, car elle assure la séparation des administrateurs de serveur et des clés de chiffrement nécessaires au déchiffrement des données, et parce que le chiffrement est appliqué directement aux données (contrairement à BitLocker, qui applique le chiffrement au volume de disque logique), toutes les données client copiées à partir d’un serveur Exchange restent chiffrées.

L’étendue du chiffrement du service Exchange Online est celle des données client stockées au repos dans Exchange Online. (Skype Entreprise stocke presque tout le contenu généré par l’utilisateur dans la boîte aux lettres Exchange Online de l’utilisateur et hérite donc de la fonctionnalité de chiffrement de service d’Exchange Online.)


## <a name="microsoft-teams"></a>Microsoft Teams

Teams utilise TLS et MTLS pour chiffrer les messages instantanés. Tout le trafic de serveur à serveur nécessite MTLS, que le trafic soit limité au réseau interne ou qu’il traverse le périmètre du réseau interne.

Ce tableau récapitule les protocoles utilisés par Teams.

|**Type de trafic**|**Chiffré par**|
|:-----|:-----|
|Serveur à serveur|MTLS|
|Client à serveur (par exemple, messagerie instantanée et présence)|TLS|
|Flux multimédias (par exemple, partage audio et vidéo des médias)|TLS|
|Partage audio et vidéo des médias|SRTP/TLS|
|Signalisation|TLS|

#### <a name="media-encryption"></a>Chiffrement des données multimédias

Le trafic multimédia est chiffré à l’aide du protocole SRTP (Secure RTP), un profil du protocole RTP (Real-Time Transport Protocol). SRTP utilise une clé de session générée à l’aide d’un générateur de nombres aléatoires sécurisé et est échangée à l’aide du canal TLS de signalisation. Le trafic multimédia client à client est négocié via une signalisation de connexion client à serveur, mais il est chiffré à l’aide de SRTP lors de la connexion client à client directement.

Teams utilise un jeton basé sur les informations d’identification pour un accès sécurisé aux relais multimédias sur TURN. Les relais multimédias échangent le jeton sur un canal TLS sécurisé.

#### <a name="fips"></a>FIPS

Teams utilise des algorithmes conformes FIPS (Federal Information Processing Standard) pour les échanges de clés de chiffrement. Pour plus d’informations sur l’implémentation de FIPS, consultez la publication [fiPS (Federal Information Processing Standard) 140-2.](/microsoft-365/compliance/offering-fips-140-2)
