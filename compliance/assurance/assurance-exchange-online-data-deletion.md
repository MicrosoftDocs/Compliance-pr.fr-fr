---
title: Suppression de données Microsoft 365 Exchange Online
description: Découvrez comment les suppressions de données soft et hard pour les boîtes aux lettres et les éléments dans les boîtes aux lettres sont gérées dans Exchange Online.
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
hideEdit: true
ms.openlocfilehash: c88e7359931fb964fbc4cb6531c5151072a50df0
ms.sourcegitcommit: 024137a15ab23d26cac5ec14c36f3577fd8a0cc4
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 04/01/2021
ms.locfileid: "51497201"
---
# <a name="exchange-online-data-deletion-in-microsoft-365"></a>Suppression de données Exchange Online dans Microsoft 365

Dans Exchange Online, il existe deux types de suppressions : les suppressions soft et les suppressions dures. Cela s’applique aux boîtes aux lettres et aux éléments d’une boîte aux lettres.

## <a name="soft-deleted-and-hard-deleted-mailboxes"></a>Boîtes aux lettres supprimées (supprimées(ou supprimées) ou supprimées (supprimées définitivement)

Une boîte aux lettres utilisateur supprimée (récupération) est une boîte aux lettres qui a été supprimée à l’aide du Centre d’administration Microsoft 365 ou de la cmdlet Remove-Mailbox et qui se trouve toujours dans la Corbeille Azure Active Directory depuis moins de 30 jours. Une boîte aux lettres peut être supprimée (suppression possible) de l’une des manières suivantes :

- Le compte d’utilisateur Azure Active Directory associé à la boîte aux lettres utilisateur est supprimé (l’objet utilisateur est hors de portée ou dans le conteneur de la Corbeille).
- Le compte d’utilisateur Azure Active Directory associé à la boîte aux lettres utilisateur a été supprimé définitivement, mais la boîte aux lettres Exchange Online fait l’objet d’une mise en attente pour litige ou d’une mise en attente eDiscovery.
- Le compte d’utilisateur Azure Active Directory associé à la boîte aux lettres utilisateur a été purgé au cours des 30 derniers jours . qui est la durée maximale de rétention pendant laquelle Exchange Online conserve la boîte aux lettres dans un état supprimé (suppression possible) avant qu’elle ne soit définitivement purgée et irrécable.

Une boîte aux lettres utilisateur supprimée définitivement est une boîte aux lettres qui a été supprimée de l’une des manières suivantes :

- La boîte aux lettres de l’utilisateur a été supprimée (temporaire) depuis plus de 30 jours et l’utilisateur Azure Active Directory associé a été supprimé définitivement. Tout le contenu de boîte aux lettres, tel que les e-mails, les contacts et les fichiers, est définitivement supprimé.
- Le compte d’utilisateur associé à la boîte aux lettres utilisateur a été supprimé définitivement d’Azure Active Directory. La boîte aux lettres de l’utilisateur est désormais supprimée (de nouveau) dans Exchange Online et reste dans un état de suppression (suppression automatique) pendant 30 jours. Si au cours de la période de 30 jours un nouvel utilisateur Azure Active Directory est synchronisé à partir du compte de destinataire d’origine avec le même **ExchangeGuid** ou **ArchiveGuid**, et que ce nouveau compte est sous licence pour Exchange Online, cela entraîne une suppression difficile de la boîte aux lettres utilisateur d’origine. Tout le contenu de boîte aux lettres, tel que les e-mails, les contacts et les fichiers, est définitivement supprimé.
- Une boîte aux lettres supprimée (suppression temporaire) est supprimée à l’aide de **Remove-Mailbox -PermanentlyDelete**.

Les scénarios de suppression ci-dessus supposent que la boîte aux lettres de l’utilisateur n’est dans aucun des états de la boîte aux lettres de l’utilisateur, comme la boîte aux lettres pour litige ou la découverte électronique. S’il existe un type de hold sur la boîte aux lettres, la boîte aux lettres ne peut pas être supprimée. Pour tous les types de [](https://support.office.com/article/manage-legal-investigations-in-office-365-2e5fbe9f-ee4d-4178-8ff8-4356bc1b168e?ui=en-US&rs=en-US&ad=US) destinataires d’utilisateur de messagerie, tous les paramètres de mise en attente sont ignorés et n’ont aucun effet sur les suppressions dures ou les suppressions soft.

## <a name="soft-deleted-and-hard-deleted-items"></a>Éléments supprimés (supprimés(s) et supprimés (supprimés définitivement)

Lorsqu’un utilisateur supprime un élément de boîte aux lettres (tel qu’un message électronique, un contact, un rendez-vous de calendrier ou une tâche), l’élément est déplacé vers le dossier Éléments récupérables et dans un sous-dossier nommé « Suppressions ». C’est ce qu’on appelle une suppression souple. La durée de conservation dans le dossier Suppressions des éléments supprimés dépend de la période de rétention des éléments supprimés qui est définie pour la boîte aux lettres. Une boîte aux lettres Exchange Online conserve les éléments supprimés pendant 14 jours par défaut, mais les administrateurs Exchange Online peuvent modifier ce paramètre pour augmenter la période jusqu’à un maximum de 30 jours. (Pour obtenir la procédure détaillée d’augmentation de la période de rétention des éléments supprimés pour une boîte aux lettres Exchange Online, voir Modifier la durée de conservation des éléments supprimés définitivement pour une boîte aux lettres [Exchange Online.)](/exchange/recipients-in-exchange-online/manage-user-mailboxes/change-deleted-item-retention) Les utilisateurs peuvent récupérer ou purger des éléments supprimés avant l’expiration de la durée de rétention d’un élément supprimé. Pour ce faire, ils utilisent la fonctionnalité Récupérer les éléments supprimés dans Microsoft Outlook ou Outlook sur le web.

Si un utilisateur purge un élément supprimé à l’aide de la fonctionnalité Récupérer les éléments supprimés dans Outlook ou Outlook sur le web, il s’agit d’une suppression dure. Dans Exchange Online, la récupération d’élément unique est activée par défaut [](/Exchange/recipients/user-mailboxes/recover-deleted-messages) lors de la création d’une boîte aux lettres, de sorte qu’un administrateur peut toujours récupérer des éléments supprimés définitivement avant l’expiration de la période de rétention des éléments supprimés. En outre, si un message est modifié par un utilisateur ou un processus, des copies de l'élément d'origine sont également conservées lorsque la fonctionnalité de récupération d'élément unique est activée.

## <a name="page-zeroing"></a>Zéro des pages

*La mise à* zéro est un mécanisme de sécurité qui écrit des zéros ou un modèle binaire sur les données supprimées afin que les données supprimées sont plus difficiles à récupérer. Dans Exchange Online, les bases de données de boîtes aux lettres utilisent des *pages* comme unité de stockage et implémentent un processus de réécriture appelé mise *à zéro des pages.* La zeroing des pages est activée par défaut et ne peut pas être désactivée par les clients ou par Microsoft. Les opérations de mise à zéro des pages sont enregistrées dans les fichiers journaux des transactions afin que toutes les copies d’une base de données donnée soient mise à zéro de la même manière. La mise à zéro d’une page sur une copie de base de données active entraîne la mise à zéro de la page sur les copies passives de la base de données.

La suppression des pages écrit un modèle binaire sur des enregistrements supprimés définitivement. Le modèle de mise à zéro des pages est spécifique aux opérations ESE (Extensible Storage Engine) (nom du moteur de base de données interne utilisé par les serveurs dans Exchange Online), et il est différent pour les opérations d’exécuter et les opérations de maintenance de base de données en arrière-plan. (La maintenance de base de données en arrière-plan est un processus qui vérifie et analyse en permanence chaque base de données. Sa fonction principale est de vérifier les pages de base de données, mais elle gère également le nettoyage de l’espace et la mise à zéro des enregistrements et des pages qui n’ont pas été mis à zéro en raison d’un incident du Store.)

Le tableau suivant répertorie les schémas de remplissage qui correspondent à des opérations d'exécution particulières.

| Opération d’exécution d’ESE   | Modèle de remplissage |
|--------------------------|--------------|
| Remplacement                  | R            |
| Suppression d'enregistrement/de valeur longue | D            |
| Espace de page libéré         | H            |

Le tableau suivant répertorie les schémas de remplissage correspondant à des opérations spécifiques effectuées pendant une opération de maintenance de base de données ESE en arrière-plan.

| Opération de maintenance de base de données ESE en arrière-plan | Modèle de remplissage |
|-----------------------------------------------|--------------|
| Suppression d’enregistrement                                 | D            |
| Suppression de valeur longue                             | L            |
| Espace libéré sur la page partiellement utilisée       | Z            |
| Espace libéré sur la page inutilisée               | U            |

### <a name="page-zeroing-process"></a>Processus de zéro des pages

Le processus de zéro des pages dépend du scénario de suppression. Le tableau suivant décrit les scénarios de suppression de base de données et les circonstances dans lesquelles les fonctions de mise à zéro des pages sont exécutées.

| Scénario de suppression de base de données | Processus et délai nécessaire à ESE pour mettre à zéro les données de la base de données |
|:--------------------------|:------------------------------------------------|
| L’élément expire en fonction de la période de rétention des éléments supprimés. | Un thread asynchrone écrit un masque binaire sur les données supprimées. Cette action se produit dans les millisecondes suivant la suppression de l'enregistrement. Si le processus store se crashe alors que le travail de mise à zéro asynchrone est toujours en suspens (ou si le nettoyage de la banque de versions est annulé en raison de la croissance du magasin de versions), la mise à zéro est terminée lorsque la maintenance de base de données en arrière-plan traite cette section de la base de données. |
| View Scenario: Expiration of items from Outlook/Outlook on the web folder view (for example, Conversation view) | La mise à zéro des données a lieu lorsque la maintenance de base de données en arrière-plan traite cette section de la base de données. |
| Scénario de déplacement/suppression de boîte aux lettres : boîte aux lettres source supprimée (expiration de la boîte aux lettres supprimée) | La mise à zéro des données a lieu lorsque la maintenance de base de données en arrière-plan traite cette section de la base de données. |

### <a name="mailbox-data-types-without-page-zeroing"></a>Types de données de boîte aux lettres sans zéro de page

Les types de données de boîte aux lettres suivants n’ont aucune disposition pour la zéroation des pages :

- Journaux des **transactions** de la base de données de boîtes aux lettres : lorsque les journaux des transactions sont supprimés dans le cadre d’opérations normales, il n’existe aucun processus pour supprimer les blocs du système de fichiers qui stockaient les fichiers journaux supprimés. Il est probable que le système de fichiers réutilise rapidement cet espace libre pour les journaux nouvellement créés, mais cela n’est pas garanti.
- **Fichiers catalogue d’indexation de** contenu : Exchange Online utilise Search Foundation (également appelé FAST) pour la fonctionnalité d’indexation de la recherche. Le catalogue d’index de recherche se compose de plusieurs dizaines de fichiers stockés sur le même volume que le fichier de base de données de boîtes aux lettres. Lorsqu'un message est définitivement supprimé de la base de données de boîtes aux lettres, le contenu associé dans le catalogue de recherche n'est pas immédiatement supprimé. La suppression de contenu se produit lorsque Search Foundation fait une ombre (ou fusion principale) de nombreux petits fichiers catalogue dans un seul fichier plus grand. Une fois la fusion principale terminée, les fichiers de catalogue plus petits sont supprimés. Il n’existe aucun processus pour supprimer les blocs qui stockaient les fichiers catalogue supprimés.

## <a name="continuous-replication"></a>Réplication continue

La réplication continue (également appelée copie des journaux de livraison et de relecture) est une technologie d’Exchange Online qui crée et maintient des copies de chaque base de données de boîtes aux lettres pour fournir une haute disponibilité, une résilience de site et une récupération d’urgence. La réplication continue utilise la prise en charge Exchange Server incident de la base de données pour fournir une technologie qui effectue une mise à jour asynchrone d’une ou plusieurs copies d’une base de données de boîtes aux lettres. Chaque serveur de boîtes aux lettres enregistre les mises à jour de base de données réalisées sur une base de données active (par exemple, l’activité de messagerie de l’utilisateur) en tant qu’enregistrements de journal dans un ensemble séquentiel de fichiers journaux des transactions de 1 Mo. Cet ensemble de fichiers est appelé flux de journal. Dans la réplication continue, le flux de journal est également utilisé pour mettre à jour de manière asynchrone une ou plusieurs copies d’une base de données. Pour ce faire, transmettez les journaux à un emplacement contenant une copie passive de la base de données active, puis relecturez-les dans la copie passive de la base de données. Si tous les journaux de la base de données active sont relectés par rapport à une copie passive de la base de données, les deux bases de données sont équivalentes et c’est par le biais de ce processus que toute modification physique d’une base de données active est répliquée sur toutes les copies passives de cette base de données.

Toute suppression d’une base de données de boîtes aux lettres, qu’il s’agit d’un élément de boîte aux lettres ou d’une boîte aux lettres entière, et qu’il s’agit d’une suppression ou d’une suppression matérielle, représente une modification physique de la base de données active. La mise à zéro des pages implique également d’apporter des modifications physiques à la base de données active. Ces modifications sont écrites dans les fichiers journaux par le biais d’un processus appelé réplication continue, et lorsque ces fichiers journaux sont relectés sur des copies passives de la base de données, les mêmes modifications physiques sont apportées à ces bases de données passives.
