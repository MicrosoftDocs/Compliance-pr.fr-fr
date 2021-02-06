---
title: Résilience des données Exchange Online dans Microsoft 365
description: Dans cet article, vous trouverez une explication des différents aspects de la résilience des données dans Exchange Online et Microsoft 365.
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
- MS-Compliance
f1.keywords:
- NOCSH
ms.custom: seo-marvel-apr2020
titleSuffix: Microsoft Service Assurance
ms.openlocfilehash: 044bd637241c566a5e44df6522fca4dcab8b8534
ms.sourcegitcommit: 21ed42335efd37774ff5d17d9586d5546147241a
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 02/05/2021
ms.locfileid: "50120523"
---
# <a name="exchange-online-data-resiliency-in-microsoft-365"></a>Résilience des données Exchange Online dans Microsoft 365

>[!IMPORTANT]
>À mesure que nous continuons d’investir de différentes manières pour conserver le contenu des boîtes aux lettres, nous andélisons le retrait des conservations In-Place dans le Centre d’administration Exchange (EAC) dans Exchange Online. À compter du 1er juillet 2020, vous ne pourrez pas créer de nouvelles In-Place de la place. Toutefois, vous pourrez toujours gérer les In-Place dans le EAC ou à l’aide de la cmdlet **Set-MailboxSearch** dans Exchange Online PowerShell. Toutefois, à compter du 1er octobre 2020, vous ne pourrez plus gérer les In-Place' Vous ne pourrez les supprimer que dans le EAC ou à l’aide de la cmdlet **Remove-MailboxSearch.** L'In-Place de Exchange Server et les déploiements hybrides Exchange seront toujours pris en charge. Pour plus d’informations sur le retrait des In-Place dans Exchange Online, voir Retrait des outils [eDiscovery hérités.](/microsoft-365/compliance/legacy-ediscovery-retirement)

Une conservation inaltérable conserve tout le contenu d’une boîte aux lettres, y compris les éléments supprimés et les versions originales des éléments modifiés. Tous ces éléments de boîte aux lettres sont renvoyés dans une recherche de [Découverte électronique locale](/exchange/security-and-compliance/in-place-ediscovery/in-place-ediscovery). Lorsque vous placez une In-Place sur la boîte aux lettres d’un utilisateur, le contenu de la boîte aux lettres d’archivage correspondante (si elle est activée) est également mis en attente et renvoyé dans une recherche de découverte électronique.

Il existe deux types d’altération qui peuvent affecter une base de données Exchange : l’altération physique, qui est généralement causée par des problèmes matériels (notamment le matériel de stockage) et l’altération logique, qui se produit en raison d’autres facteurs. En règle générale, il existe deux types d’altération logique qui peuvent se produire au sein d’une base de données Exchange :

- **Corruption logique de la base de** données : la base de données de la page de contrôle correspond, mais les données de la page sont erronées logiquement. Cela peut se produire lorsque le moteur de base de données (ESE) tente d’écrire une page de base de données et même si le système d’exploitation renvoie un message de réussite, les données ne sont jamais écrites sur le disque ou au mauvais endroit. Il s’agit d’un *vidage perdu*. ESE inclut de nombreuses fonctionnalités et protections conçues pour empêcher l’altération physique d’une base de données et d’autres scénarios de perte de données. Pour éviter que des purges perdues ne perdent des données, ESE inclut un mécanisme de détection de purge perdue dans la base de données, ainsi qu’une fonctionnalité (restauration d’une seule page) pour les corriger.
- **Altération logique du magasin** : les données sont ajoutées, supprimées ou manipulées d’une manière que l’utilisateur ne s’attend pas. Ces cas sont dus à des applications tierces. Elle est généralement corrompue dans le sens où l’utilisateur considère qu’elle est corrompue. La banque d'informations Exchange considère la transaction qui est à l'origine de l'altération logique comme une série d'opérations MAPI valides. Les [fonctionnalités](/exchange/security-and-compliance/create-or-remove-in-place-holds) de la mise en attente sur place dans Exchange Online offrent une protection contre l’altération logique de la boutique (car elles empêchent la suppression définitive du contenu par un utilisateur ou une application). 

Exchange Online effectue plusieurs vérifications de cohérence sur les fichiers journaux répliqués lors de l’inspection et de la relecture des journaux. Ces vérifications de cohérence empêchent la réplication de l’altération physique par le système. Par exemple, lors de l’inspection du journal, il existe une vérification de l’intégrité physique qui vérifie le fichier journal et vérifie que la valeur de contrôle enregistrée dans le fichier journal correspond à la valeur de contrôle générée en mémoire. En outre, l’en-tête du fichier journal est examiné pour s’assurer que la signature du fichier journal enregistrée dans l’en-tête du journal correspond à celle du fichier journal. Pendant la relecture du journal, le fichier journal fait l’objet d’un examen approfondi. Par exemple, l’en-tête de base de données contient également la signature du journal comparée à la signature du fichier journal pour s’assurer qu’elles correspondent. 

La protection contre l’altération des données de boîtes aux lettres dans Exchange Online est obtenue à l’aide d’Exchange Native Data Protection, une stratégie de résilience qui tire parti de la réplication au niveau de l’application sur plusieurs serveurs et plusieurs centres de données, ainsi que d’autres fonctionnalités qui permettent de protéger les données contre la perte en raison d’une altération ou d’autres raisons. Ces fonctionnalités incluent des fonctionnalités natives gérées par Microsoft ou l’application Exchange Online elle-même, telles que :

- [Groupes de disponibilité des données](/exchange/back-up-email)
- Correction à bit unique 
- Analyse de base de données en ligne 
- Détection de purge perdue 
- Restauration d’une seule page 
- Service de réplication de boîte aux lettres 
- Vérifications des fichiers journaux 
- Déploiement sur un système de fichiers résilient 

Pour plus d’informations sur les fonctionnalités natives répertoriées précédemment, sélectionnez les liens hypertexte et consultez les informations suivantes pour plus d’informations et pour plus d’informations sur les éléments sans liens hypertexte. En plus de ces fonctionnalités natives, Exchange Online inclut également des fonctionnalités de résilience des données que les clients peuvent gérer, telles que : 
- [Récupération d’élément unique (activée par défaut)](/exchange/recipients-in-exchange-online/manage-user-mailboxes/recover-deleted-messages) 
- [Conservation inaltérable et conservation pour litige](/exchange/security-and-compliance/in-place-and-litigation-holds) 
- [Rétention des éléments supprimés et Soft-Deleted boîtes aux lettres (activées par défaut)](/exchange/recipients-in-exchange-online/delete-or-restore-mailboxes) 

## <a name="database-availability-groups"></a>Groupes de disponibilité de base de données 
Chaque base de données de boîtes aux lettres dans Microsoft 365 est hébergée dans un groupe de disponibilité de base de données [(DAG)](/exchange/back-up-email) et répliquée dans des centres de données géographiquement distincts au sein de la même région. La configuration la plus courante est de quatre copies de base de données dans quatre centres de données . toutefois, certaines régions ont moins de centres de données (les bases de données sont répliquées vers trois centres de données en Inde et deux centres de données en Australie et au Japon). Toutefois, dans tous les cas, chaque base de données de boîtes aux lettres possède quatre copies distribuées dans plusieurs centres de données, garantissant ainsi que les données de boîte aux lettres sont protégées contre les défaillances logicielles, matérielles et même de centres de données. 

Sur ces quatre copies, trois d’entre elles sont configurées comme hautement disponibles. La quatrième copie est configurée en tant que [copie de base de données retardée.](/Exchange/high-availability/manage-ha/activate-lagged-db-copies) La copie de base de données retardée n’est pas destinée à la récupération de boîte aux lettres individuelle ou à la récupération d’élément de boîte aux lettres. Son objectif est de fournir un mécanisme de récupération pour les rares événements d’altération logique catastrophique à l’échelle du système. 

Les copies de base de données retardées dans Exchange Online sont configurées avec un retard de relecture du fichier journal de sept jours. En outre, le Gestionnaire de retard de relecture Exchange est activé pour fournir la lecture dynamique des fichiers journaux pour les copies retardées afin de permettre aux copies de base de données retardées de se réparer et de gérer la croissance des fichiers journaux. Bien que les copies de base de données retardées soient utilisées dans Exchange Online, il est important de comprendre qu’il ne s’agit pas d’une sauvegarde à un point dans le temps garantie. Les copies de base de données retardées dans Exchange Online ont un seuil de disponibilité, généralement autour de 90 %, en raison des périodes où le disque contenant une copie retardée est perdu en raison d’une défaillance du disque, de la copie retardée devient une copie hautement disponible (en raison de la lecture automatique), ainsi que des périodes où la copie de base de données retardée reconstruit la file d’attente de relecture de journal. 

## <a name="transport-resilience"></a>Résilience de transport 
Exchange Online inclut deux principales fonctionnalités de résilience de transport : la redondance des ombres et le dispositif de sécurité. La redondance des ombres conserve une copie redondante d’un message pendant son transit. Safety Net conserve une copie redondante d’un message une fois le message remis. 

Avec la redondance des ombres, chaque serveur de transport Exchange Online effectue une copie de chaque message qu’il reçoit avant d’accusé de réception du message au serveur d’envoi. Ainsi, tous les messages du pipeline de transport sont redondants en transit. Si Exchange Online détermine que le message d’origine a été perdu en transit, une copie redondante du message est redé perdue. 

Safety Net est une file d’attente de transport associée au service de transport sur un serveur de boîtes aux lettres. Cette file d'attente stocke des copies des messages qui ont été correctement traités par le serveur. Lorsqu’une défaillance d’une base de données de boîtes aux lettres ou d’un serveur nécessite l’activation d’une copie de la base de données de boîtes aux lettres, les messages de la file d’attente Safety Net sont automatiquement renvoyés vers la nouvelle copie active de la base de données de boîtes aux lettres. Safety Net est également redondant, ce qui élimine le transport comme point de défaillance unique. Il utilise le concept d’un dispositif de sécurité principal et d’un dispositif de sécurité de ombre dans lequel si le dispositif de sécurité principal n’est pas disponible pendant plus de 12 heures, les demandes de resoumettre deviennent des demandes de resoumettre de l’ombre et les messages sont redétransmités à partir du dispositif de sécurité de l’ombre.

Les redémissions de messages à partir de Safety Net sont automatiquement lancées par le composant Active Manager du service de réplication Microsoft Exchange qui gère les DG et les copies de base de données de boîtes aux lettres. Aucune action manuelle n’est requise pour resoumettre des messages à partir de Safety Net. 

## <a name="single-bit-correction"></a>Correction à bit unique 
ESE inclut un mécanisme permettant de détecter et de résoudre les erreurs CRC à bit unique (également appelées retournements à bit unique) qui sont le résultat d’erreurs matérielles (et en tant que telles, elles représentent une altération physique). Lorsque ces erreurs se produisent, ESE les corrige automatiquement et enregistre un événement dans le journal des événements. 

## <a name="online-database-scanning"></a>Analyse de base de données en ligne 
L’analyse de base de données en ligne (également appelée somme de vérification de base de *données)* est le processus dans lequel un ESE utilise un outil de vérification de cohérence de base de données pour lire chaque page et vérifier qu’elle est corrompue. L’objectif principal est de détecter les altérations physiques et les purges perdues qui ne sont peut-être pas détectées par les opérations transactionnelles. L’analyse de base de données effectue également des opérations d’incident post-store. L’espace peut être perdu en raison de pannes, et l’analyse de base de données en ligne recherche et récupère l’espace perdu. Le système est conçu avec l’attente que chaque base de données soit entièrement analysée tous les sept jours. 

## <a name="lost-flush-detection"></a>Détection de purge perdue 
Une purge perdue se produit lorsqu’une opération d’écriture de base de données renvoyée comme terminée par le sous-système de disque ou le système d’exploitation n’a pas réellement été écrite sur le disque ou qu’elle a été écrite au mauvais emplacement. Les incidents de purge perdus peuvent entraîner une altération logique de la base de données. Par conséquent, pour éviter que des purges perdues entraînent la perte de données, ESE inclut un mécanisme de détection de purge perdu. Lorsque des pages de base de données sont écrites sur des copies passives, une vérification est effectuée pour les purges perdues sur la copie active. Si un purgement perdu est détecté, ESE peut réparer le processus à l’aide d’un processus de correction de page. 

## <a name="single-page-restore"></a>Restauration d’une seule page 
La restauration d’une seule page, également appelée correction de *page,* est un processus automatique dans lequel les pages de base de données endommagées sont remplacées par des copies saines à partir d’un réplica sain. Le processus de réparation d’une page endommagée varie selon que la copie de base de données est active ou passive. Lorsqu’une copie de base de données active rencontre une page endommagée, elle peut copier une page à partir de l’un de ses réplicas, à condition que la page qu’elle copie soit à jour. Pour ce faire, vous pouvez placer une demande pour la page dans le flux de journal, qui est la base de la réplication de base de données de boîtes aux lettres. Dès qu’un réplica rencontre la demande de page, il répond en envoyant une copie de la page à la copie de base de données à l’aide de la demande. La restauration d’une seule page fournit également un mécanisme de communication asynchrone permettant aux utilisateurs actifs de demander une page à des réplicas, même si les réplicas sont actuellement hors connexion. 

En cas d’altération dans une copie passive de base de données, y compris une copie de base de données retardée, étant donné que ces copies sont toujours derrière leur copie active, il est toujours sûr de copier n’importe quelle page de la copie active vers une copie passive. Une copie de base de données passive est par nature hautement disponible. Ainsi, pendant le processus de mise à jour des pages, la relecture des journaux est suspendue, mais la copie des journaux continue. La copie passive de la base de données récupère une copie de la page endommagée à partir de la copie active, attend que le fichier journal qui répond à l’exigence maximale de génération du journal soit copié et inspecté, puis correctifs de la page endommagée. Une fois que la page a été corrigé, la relecture du journal reprend. Le processus est le même pour la copie de base de données retardée, sauf que la base de données retardée relect d’abord tous les fichiers journaux nécessaires pour obtenir un état correctif. 

## <a name="mailbox-replication-service"></a>Service de réplication de boîte aux lettres 
Le déplacement de boîtes aux lettres est un élément clé de la gestion d’un service de messagerie à grande échelle. Il existe toujours des technologies mises à jour et des mises à niveau matérielles et de version à gérer. Par conséquent, il est essentiel de disposer d’un système robuste et limitée qui permet à nos ingénieurs d’effectuer ce travail tout en conservant la transparence des déplacements de boîtes aux lettres pour les utilisateurs (en s’assurer qu’ils restent en ligne tout au long du processus) et de s’assurer que le processus s’actualise normalement à mesure que les boîtes aux lettres s’agrandissent. 

Le service de réplication de boîte aux lettres Exchange (MRS) est responsable du déplacement des boîtes aux lettres entre les bases de données. Pendant le déplacement, mrs effectue une vérification de cohérence sur tous les éléments de la boîte aux lettres. Si un problème de cohérence est trouvé, mrs corrige le problème ou ignore les éléments endommagés, supprimant ainsi l’altération de la boîte aux lettres. 

Étant donné que mrs est un composant d’Exchange Online, nous pouvons apporter des modifications dans son code pour résoudre les nouvelles formes d’altération détectées à l’avenir. Par exemple, si nous détectons un problème de cohérence que mrs n’est pas en mesure de résoudre, nous pouvons analyser l’altération, modifier le code MRS et corriger l’incohérence (si nous comprenons comment). 

## <a name="log-file-checks"></a>Vérifications des fichiers journaux 
Tous les fichiers journaux de transactions générés par une base de données Exchange font l’objet de plusieurs formes de vérifications de cohérence. Lorsqu’un fichier journal est créé, la première chose à faire est qu’un modèle de bits est écrit, puis qu’une série d’écritures de journaux est effectuée. Cette structure permet à Exchange Online d’exécuter une série de vérifications ( purge perdue, CRC et autres vérifications) pour valider chaque fichier journal tel qu’il est écrit, et à nouveau lors de sa réplication. 

## <a name="deployment-on-resilient-file-system"></a>Déploiement sur un système de fichiers résilient 
Pour éviter toute altération au niveau du système de fichiers, Exchange Online est déployé sur des partitions de système de fichiers résilient (ReFS) afin de fournir des fonctionnalités de récupération améliorées. ReFS est un système de fichiers dans Windows Server 2012 et les ultérieures conçu pour être plus résilient contre la corruption des données, optimisant ainsi la disponibilité et l’intégrité des données. Plus précisément, ReFS apporte des améliorations dans la mise à jour des métadonnées, ce qui offre une meilleure protection des données et réduit les cas d’altération des données. Il utilise également des checksums pour vérifier l’intégrité des données de fichier et des métadonnées afin de s’assurer que l’altération des données est facilement trouvée et réparée. 

Exchange Online tire parti de plusieurs avantages de ReFS : 
- Une plus grande résilience de l’intégrité des données signifie moins d’incidents de corruption de données. La réduction du nombre d’incidents de corruption implique moins de réassages de base de données inutiles. 
- Checksum s’exécutant sur des métadonnées permettant de détecter plus rapidement et plus déterministement les cas de corruption, ce qui nous permet de corriger l’altération des données client avant que des échecs gris ne se produisent sur les volumes de données.
- Conçu pour fonctionner avec des jeux de données volumineux (pétaoctets et plus grands) sans impact sur les performances
- Prise en charge d’autres fonctionnalités utilisées par Exchange Online, telles que le chiffrement BitLocker. 

Exchange Online bénéficie également d’autres fonctionnalités ReFS : 
- **Intégrité (flux d’intégrité)** : ReFS stocke les données d’une manière qui les protège contre de nombreuses erreurs courantes qui peuvent normalement provoquer une perte de données. Microsoft 365 Search (recherche Microsoft) utilise des flux d’intégrité pour vous aider à détecter les problèmes de disque et les contrôles de contenu de fichier. La fonctionnalité réduit également les incidents de corruption causés par « Écritures en écriture » (lorsqu’une opération d’écriture ne se termine pas en raison de pannes d’alimentation, etc.). 
- **Disponibilité (récupération)** : ReFS hiérarchise la disponibilité des données. Historiquement, les systèmes de fichiers étaient souvent susceptibles d’être corrompus par des données qui exigeaient que le système soit mis hors connexion pour réparation. Bien que rarement, si une altération se produit, ReFS implémente la récupération, une fonctionnalité qui supprime les données endommagées de l’espace de noms sur un volume en direct et garantit que les données de qualité ne sont pas affectées par des données endommagées non réparables. L’application de la fonctionnalité récupération et l’isolation de l’altération des données aux volumes de base de données Exchange Online signifie que nous pouvons conserver les bases de données non affectées sur un volume endommagé en bon état entre le moment de l’altération et de l’action de réparation. Cette structure augmente la disponibilité des bases de données qui seraient normalement affectées par ces problèmes d’altération du disque. 
