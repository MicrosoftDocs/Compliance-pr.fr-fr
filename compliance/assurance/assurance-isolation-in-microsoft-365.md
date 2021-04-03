---
title: Isolation et contrôle d’accès dans Microsoft 365
description: 'Résumé : Explication de l’isolation et du contrôle d’accès dans les différentes applications de Microsoft 365.'
ms.author: robmazz
author: robmazz
manager: laurawi
ms.reviewer: sosstah
audience: ITPro
ms.topic: article
ms.service: O365-seccomp
localization_priority: Normal
search.appverid:
- MET150
ms.collection:
- Strat_O365_IP
- M365-security-compliance
- SPO_Content
- MS-Compliance
f1.keywords:
- NOCSH
titleSuffix: Microsoft Service Assurance
hideEdit: true
ms.openlocfilehash: f1166ce766c2b1158d50242b9411f051992bf121
ms.sourcegitcommit: 024137a15ab23d26cac5ec14c36f3577fd8a0cc4
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 04/01/2021
ms.locfileid: "51497052"
---
# <a name="isolation-and-access-control-in-microsoft-365"></a>Isolation et contrôle d’accès dans Microsoft 365

Azure Active Directory (Azure AD) et Microsoft 365 utilisent un modèle de données très complexe qui inclut des dizaines de services, des centaines d’entités, des milliers de relations et des dizaines de milliers d’attributs. À un niveau élevé, Azure AD et les annuaires de services sont les conteneurs de clients et de destinataires synchronisés à l’aide de protocoles de réplication basés sur l’état. En plus des informations d’annuaire détenues dans Azure AD, chacune des charges de travail de service possède sa propre infrastructure de services d’annuaire.
 
![Synchronisation des données du client Microsoft 365](../media/office-365-isolation-tenant-data-sync.png)

Dans ce modèle, il n’existe pas de source unique de données d’annuaire. Des systèmes spécifiques possèdent des données individuelles, mais aucun système unique ne contient toutes les données. Les services Microsoft 365 collaborent avec Azure AD dans ce modèle de données. Azure AD est le « système de vrai » pour les données partagées, qui est généralement de petites données statiques utilisées par chaque service. Le modèle fédéré utilisé dans Microsoft 365 et Azure AD fournit l’affichage partagé des données.

Microsoft 365 utilise à la fois le stockage physique et le stockage cloud Azure. Exchange Online (y compris Exchange Online Protection) et Skype Entreprise utilisent leur propre stockage pour les données client. SharePoint Online utilise à la fois SQL Server stockage azure et le stockage Azure, d’où la nécessité d’une isolation supplémentaire des données client au niveau du stockage.

## <a name="exchange-online"></a>Exchange Online

Exchange Online stocke les données client dans les boîtes aux lettres. Les boîtes aux lettres sont hébergées dans des bases de données ESE (Extensible Storage Engine) appelées bases de données de boîtes aux lettres. Cela inclut les boîtes aux lettres utilisateur, les boîtes aux lettres liées, les boîtes aux lettres partagées et les boîtes aux lettres de dossiers publics. Les boîtes aux lettres utilisateur incluent le contenu Skype Entreprise enregistré, tel que les historiques des conversations.

Le contenu de la boîte aux lettres de l’utilisateur inclut :

- Courriers électroniques et pièces jointes
- Informations de calendrier et de libre/occupé
- Contacts
- Tâches
- Notes
- Groupes
- Données d’inférence

Chaque base de données de boîtes aux lettres dans Exchange Online contient des boîtes aux lettres de plusieurs clients. Un code d’autorisation sécurisation chaque boîte aux lettres, y compris au sein d’une location. Par défaut, seul l’utilisateur affecté a accès à une boîte aux lettres. La liste de contrôle d’accès (ACL) qui sécurisation une boîte aux lettres contient une identité authentifiée par Azure AD au niveau du client. Les boîtes aux lettres de chaque client sont limitées aux identités authentifiées auprès du fournisseur d’authentification du client, qui inclut uniquement les utilisateurs de ce client. Le contenu du client A ne peut en aucune façon être obtenu par les utilisateurs du client B, sauf si le client A l’a explicitement approuvé.

## <a name="skype-for-business"></a>Skype Entreprise

Skype Entreprise stocke les données à différents endroits :

- Les informations utilisateur et de compte, qui incluent les points de terminaison de connexion, les ID de client, les plans de numérotation, les paramètres d’itinérance, l’état de présence, les listes de contacts, etc., sont stockées dans les serveurs Active Directory de Skype Entreprise et dans différents serveurs de base de données Skype Entreprise. Les listes de contacts sont stockées dans la boîte aux lettres Exchange Online de l’utilisateur si l’utilisateur est activé pour les deux produits, ou sur des serveurs Skype Entreprise si ce n’est pas le cas. Les serveurs de base de données Skype Entreprise ne sont pas partitionés par client, mais l’isolation des données par plusieurs clients est appliquée via le contrôle d’accès basé sur un rôle (RBAC).
- Le contenu de réunion et les données téléchargées sont stockés sur des partages de système de fichiers distribués (DFS). Ce contenu peut également être archivé dans Exchange Online s’il est activé. Les partages DFS ne sont pas partitionés par client. Le contenu est sécurisé avec des AAC et l’location multiple est appliquée par le biais du RBAC.
- Les enregistrements des détails des appels, qui sont l’historique des activités, tels que l’historique des appels, les sessions de messagerie instantanée, le partage d’application, l’historique de messagerie instantanée, etc., peuvent également être stockés dans Exchange Online, mais la plupart des enregistrements des détails des appels sont temporairement stockés sur des serveurs d’enregistrement des détails des appels. Le contenu n’est pas partitioné par client, mais l’location multiple est appliquée par le biais du RBAC.

## <a name="sharepoint-online"></a>SharePoint Online

SharePoint Online dispose de plusieurs mécanismes indépendants qui assurent l’isolation des données. Il stocke les objets sous forme de code abstrait dans les bases de données d’application. Par exemple, lorsqu’un utilisateur télécharge un fichier vers SharePoint Online, le fichier est désassembler, converti en code d’application et stocké dans plusieurs tables dans plusieurs bases de données.

Si un utilisateur peut accéder directement au stockage contenant les données, le contenu n’est pas interprétable par un système humain ou autre que SharePoint Online. Ces mécanismes incluent le contrôle d’accès de sécurité et les propriétés. Toutes les ressources SharePoint Online sont sécurisées par le code d’autorisation et la stratégie RBAC, y compris au sein d’une location. La liste de contrôle d’accès (ACL) qui sécurisation une ressource contient une identité authentifiée au niveau du client. Les données SharePoint Online pour un client sont limitées aux identités authentifiées par le fournisseur d’authentification pour le client.

Outre les ACA, une propriété au niveau du client qui spécifie le fournisseur d’authentification (qui est azure AD propre au client) est écrite une seule fois et ne peut pas être modifiée une fois définie. Une fois que la propriété du client du fournisseur d’authentification a été définie pour un client, elle ne peut pas être modifiée à l’aide d’API exposées à un client.

Un *SubscriptionId* unique est utilisé pour chaque client. Tous les sites clients sont la propriété d’un client et un *SubscriptionId* est attribué au client. La *propriété SubscriptionId* d’un site est écrite une seule fois et est permanente. Une fois affecté à un client, un site ne peut pas être déplacé vers un autre client. SubscriptionId *est* la clé utilisée pour créer l’étendue de sécurité pour le fournisseur d’authentification et est liée au client.

SharePoint Online utilise SQL Server stockage Azure pour le stockage des métadonnées de contenu. La clé de partition pour le magasin de contenu est *SiteId* dans SQL. Lors de l’exécution SQL requête, SharePoint Online utilise un *SiteId* vérifié dans le cadre d’une vérification *SubscriptionId* au niveau du client.

SharePoint Online stocke le contenu de fichier chiffré dans les blobs Microsoft Azure. Chaque batterie de serveurs SharePoint Online possède son propre compte Microsoft Azure et tous les blobs enregistrés dans Azure sont chiffrés individuellement avec une clé stockée dans le magasin de contenu SQL. Clé de chiffrement protégée dans le code par la couche d’autorisation et non exposée directement à l’utilisateur final. SharePoint Online dispose d’une surveillance en temps réel pour détecter lorsqu’une demande HTTP lit ou écrit des données pour plusieurs clients. L’identité de la *demande SubscriptionId* est suivi par rapport à *l’SubscriptionId* de la ressource accessible. Les demandes d’accès aux ressources de plusieurs clients ne doivent jamais avoir lieu par les utilisateurs finaux. Les demandes de service dans un environnement multi-clients sont la seule exception. Par exemple, le robot de recherche tire les modifications de contenu d’une base de données entière en même temps. Cela implique généralement l’interrogation de sites de plusieurs clients dans une demande de service unique, ce qui est effectué pour des raisons d’efficacité.

## <a name="teams"></a>Teams

Vos données Teams sont stockées différemment, en fonction du type de contenu. 

Consultez la [session de discussion Ignite sur l’architecture De Microsoft Teams](https://channel9.msdn.com/Events/Ignite/Microsoft-Ignite-Orlando-2017/BRK3071) pour une discussion détaillée.

### <a name="core-teams-customer-data"></a>Données client principales de Teams

Si votre client est provisioné en Australie, au Canada, dans l’Union européenne, en France, en Allemagne, en Inde, au Japon, en Afrique du Sud, en Corée du Sud, en Suisse (qui inclut le Liechtenstein), aux Émirats arabes unis, au Royaume-Uni ou aux États-Unis, Microsoft stocke les données client suivantes au repos uniquement à cet emplacement :

- Conversations Teams, conversations d’équipe et de canal, images, messages vocaux et contacts.
- contenu du site SharePoint Online et fichiers stockés dans ce site ;
- Fichiers téléchargés vers OneDrive pour le travail ou l’école.

#### <a name="chat-channel-messages-team-structure"></a>Conversation, messages de canal, structure d’équipe

Chaque équipe dans Teams est backed par un groupe Microsoft 365, son site SharePoint et sa boîte aux lettres Exchange. Les conversations privées (y compris les conversations de groupe), les messages envoyés dans le cadre d’une conversation dans un canal et la structure des équipes et des canaux sont stockés dans un service de conversation s’exécutant dans Azure. Les données sont également stockées dans un dossier masqué dans les boîtes aux lettres d’utilisateur et de groupe pour activer les fonctionnalités de protection des informations.

#### <a name="voicemail-and-contacts"></a>Messagerie vocale et contacts

Les messages vocaux sont stockés dans Exchange. Les contacts sont stockés dans un magasin de données cloud Exchange. Exchange et le magasin cloud Exchange fournissent déjà une résidence des données dans chacune des géos du centre de données mondial. Pour toutes les équipes, la messagerie vocale et les contacts sont stockés dans le pays pour l’Australie, le Canada, la France, l’Allemagne, l’Inde, le Japon, les Émirats arabes unis, le Royaume-Uni, l’Afrique du Sud, la Corée du Sud, la Suisse (qui inclut le Liechtenstein) et les États-Unis. Pour tous les autres pays, les fichiers sont stockés aux États-Unis, en Europe ou Asia-Pacific en fonction de l’affinité client.

#### <a name="images-and-media"></a>Images et médias

Le média utilisé dans les conversations (à l’exception des GIF Giphy qui ne sont pas stockés mais qui sont un lien de référence vers l’URL du service Giphy d’origine, Giphy est un service non-Microsoft) est stocké dans un service multimédia Azure qui est déployé aux mêmes emplacements que le service de conversation.

#### <a name="files"></a>Fichiers

Les fichiers (y compris OneNote et Wiki) que quelqu’un partage dans un canal sont stockés sur le site SharePoint de l’équipe. Les fichiers partagés dans une conversation privée ou une conversation au cours d’une réunion ou d’un appel sont téléchargés et stockés dans le compte OneDrive entreprise ou scolaire de l’utilisateur qui partage le fichier. Exchange, SharePoint et OneDrive fournissent déjà la résidence des données dans chacune des géos du centre de données mondial. Ainsi, pour les clients existants, tous les fichiers, les blocs-notes OneNote, le contenu Wiki Teams et les boîtes aux lettres qui font partie de l’expérience Teams sont déjà stockés à l’emplacement en fonction de l’affinité de votre client. Les fichiers sont stockés dans le pays pour l’Australie, le Canada, la France, l’Allemagne, l’Inde, le Japon, les Émirats arabes unis, le Royaume-Uni, l’Afrique du Sud, la Corée du Sud et la Suisse (y compris le Liechtenstein). Pour tous les autres pays, les fichiers sont stockés aux États-Unis, en Europe ou en Asie-Pacifique en fonction de l’affinité client.
