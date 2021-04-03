---
title: Immuabilité des données dans Microsoft 365
description: Découvrez comment Microsoft 365 conserve les données sous une forme découvrable pour répondre à la conformité réglementaire, aux exigences de gouvernance interne et aux risques de litige.
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
ms.openlocfilehash: 2e86cdfe082ec35fd7fd111a13a4def6f1b01806
ms.sourcegitcommit: 024137a15ab23d26cac5ec14c36f3577fd8a0cc4
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 04/01/2021
ms.locfileid: "51497628"
---
# <a name="data-immutability-in-microsoft-365"></a>Immuabilité des données dans Microsoft 365

La conformité réglementaire, les exigences de gouvernance interne ou les risques de litige nécessitent que les organisations conservent la messagerie électronique et les données associées sous une forme découvrable. Toutes les données du système doivent être découvrables et aucune d’entre elles ne peut être détruite ou modifiée. Le terme standard du secteur est « immuabilité ».

Les méthodes traditionnelles d’immuabilité fonctionnaient généralement en déplaçant les messages électroniques vers un emplacement de stockage distinct en lecture seule. Bien que ces systèmes servent à préserver les éléments de boîte aux lettres à des fins de découverte, ils affectent souvent l’expérience utilisateur en supprimant les éléments conservés du flux de travail quotidien insérante. Pour les professionnels de l’informatique, cette approche d’immuabilité nécessite le déploiement et la maintenance continue d’un serveur et d’une infrastructure de stockage distincts. La découverte est effectuée avec des outils externes au système de messagerie et inclut les coûts de déploiement et de maintenance associés.

Grâce aux fonctionnalités de stratégie de conservation et de rétention sur place de l’archivage dans Microsoft 365 et ses services, vous pouvez conserver et conserver de nombreuses classes de données entrantes, internes et sortantes. Cela inclut les opérations suivantes :

- Communications par messagerie entrantes et sortantes
- Livres et enregistrements contenus dans un formulaire de courrier électronique ou dans des documents en ligne partagés
- Demandes de réunion
- Télécopies
- Messages instantanés
- Documents partagés pendant des réunions en ligne
- Messages vocaux

En outre, Microsoft a développé des [](https://support.office.com/article/Archiving-third-party-data-in-Office-365-0ce338d5-3666-4a18-86ab-c6910ff408cc) fonctionnalités de modules supplémentaires pour permettre l’archivage des données à partir d’autres sources via l’intégration à des solutions tierces de capture et de gestion des données. Une fois les données tierces importées, vous pouvez appliquer les fonctionnalités de conformité Microsoft 365 aux données, notamment :

- [Conservation pour litige](/microsoft-365/compliance/create-a-litigation-hold)
- [Découverte électronique et conservation inaltérable](/microsoft-365/compliance/manage-legal-investigations)
- [Recherche de conformité](/microsoft-365/compliance/search-for-content)
- [Archivage local](/microsoft-365/compliance/enable-archive-mailboxes)
- [Audit de boîte aux lettres](/microsoft-365/compliance/enable-mailbox-auditing)
- [Stratégies de rétention](/microsoft-365/compliance/retention-policies)

Par exemple, lorsqu’une boîte aux lettres est placée en conservation pour litige, les données tierces sont conservées. Vous pouvez rechercher des données tierces à l’aide In-Place eDiscovery ou la recherche de conformité. Vous pouvez également appliquer des stratégies d’archivage et de rétention à des données tierces comme vous le pouvez pour les données Microsoft. L’archivage de données tierces dans Microsoft 365 permet à votre organisation de rester conforme aux stratégies gouvernementales et réglementaires.

L’archivage dans Microsoft 365 fournit un stockage conforme à la règle 17a-4 de la SEC (Securities and Exchange Commission). Microsoft 365 conserve les fichiers permanents de toutes les données collectées dans un format non réécritable et non effaçable à l’aide des stratégies de rétention et des stratégies de conservation sur place, y compris le verrouillage de conservation.

Notamment :

- Tous les enregistrements stockés à l’aide des stratégies de rétention mentionnés ci-dessus sont conservés dans une zone de stockage dédiée hors du ressort de l’utilisateur ordinaire. Seuls les utilisateurs autorisés peuvent accéder à ces enregistrements et y effectuer des recherches, mais ils ne peuvent pas les modifier ni les effacer.
- Les métadonnées de chaque élément incluent un timestamp utilisé dans le calcul de la durée de rétention. Les timestamps sont appliqués lorsqu’un nouvel élément est reçu ou créé et ne peuvent pas être modifiés ou supprimés des métadonnées.
- L’archivage dans Microsoft 365 permet aux utilisateurs de combiner différentes stratégies de rétention et de conserver des actions pour créer des stratégies de rétention granulaires. Ces stratégies définissent le type ou l’emplacement des éléments conservés et la durée de conservation.
- La fonctionnalité verrouillage de conservation permet aux utilisateurs de choisir s’il faut rendre la stratégie restrictive. Une stratégie restrictive empêche toute personne d’avoir la possibilité de supprimer, de désactiver ou d’apporter des modifications à la stratégie de rétention. Cela signifie qu’une fois le verrouillage de conservation activé, il ne peut pas être désactivé et qu’il n’existe aucun mécanisme sous lequel les données provenant de dépositaires existants qui ont été collectées par les stratégies de rétention en place peuvent être écrasées, modifiées, effacées ou supprimées pendant la période de conservation. En outre, la période de conservation définie par le verrouillage de conservation peut ne pas être raccourcie ou diminuée. Il peut toutefois être plus long, dans le cas d’une obligation légale de conserver les données stockées, comme indiqué ci-dessus. Le verrouillage de conservation garantit que personne, pas même les administrateurs ou ceux ayant un certain accès aux contrôles, ne peut modifier les paramètres ou modifier ou effacer les données qui ont été stockées, en mettant l’archivage dans Microsoft 365 en ligne avec les instructions définies dans la version 2003 de la règle SEC 17a-4.

Pour comprendre comment Microsoft 365 vous aide à respecter les obligations réglementaires, en particulier [](https://www.microsoft.com/microsoft-365/blog/wp-content/uploads/2015/11/Microsoft-EOA-White-Paper.pdf) par rapport aux exigences de la règle 17a-4, consultez le livre blanc qui couvre Archivage Exchange Online, SharePoint Online, OneDrive Entreprise et Skype Entreprise. Le livre blanc fournit également une analyse approfondie des fonctionnalités et des fonctionnalités d’archivage De Microsoft 365 par rapport à chacune des exigences de la règle SEC 17a-4 et montre aux clients réglementés comment l’archivage Microsoft 365 peut leur permettre de répondre à ces exigences.
