---
title: RGPD pour Skype Entreprise Server
description: Découvrez comment satisfaire aux exigences du RGPD dans les environnements locaux Skype Entreprise Server et Lync Server.
f1.keywords:
- NOCSH
ms.author: mikeplum
author: MikePlumleyMSFT
manager: pamgreen
audience: ITPro
ms.topic: article
ms.service: O365-seccomp
localization_priority: Priority
titleSuffix: Microsoft GDPR
ms.collection: MS-Compliance
ms.openlocfilehash: 7a3739afc42ba6397bb0b465b6f4a9c5806d2c16
ms.sourcegitcommit: 626b0076d133e588cd28598c149a7f272fc18bae
ms.translationtype: HT
ms.contentlocale: fr-FR
ms.lasthandoff: 11/30/2020
ms.locfileid: "49507371"
---
# <a name="gdpr-for-skype-for-business-server-and-lync-server"></a>RGPD pour Skype Entreprise Server et Lync Server

La plupart des données de Skype Entreprise Server et de Lync Server sont stockées dans Exchange Server. Ces données incluent les éléments suivants :

-   Historique des conversations

-   Notifications de messagerie vocale et transcriptions

-   Invitations aux réunions

Reportez-vous aux procédures définies pour le [RGPD pour Exchange Server](gdpr-for-exchange-server.md) afin de rechercher, exporter ou supprimer ces types de données dans le cadre de demandes liées au RGPD.

Les listes de contacts sont stockées dans la base de données SQL Server. Elles peuvent être exportées de plusieurs manières, décrites ci-dessous :

-   Les utilisateurs finaux eux-mêmes peuvent exporter des contacts en cliquant avec le bouton droit de la souris sur l’en-tête du groupe et en sélectionnant Copier. Tous les contacts de ce groupe seront ainsi copiés dans le Presse-papiers et pourront ensuite être collés dans n’importe quelle application.

-   Vous pouvez utiliser la cmdlet [Export-CsUserData](https://docs.microsoft.com/powershell/module/skype/export-csuserdata) pour exporter ces données.

Le contenu chargé dans des réunions (comme des documents ou fichiers PowerPoint) ou le contenu généré lors d’une réunion (comme le tableau blanc, des sondages ou des questions et réponses) est stocké dans l’organisateur de fichiers. Il peut également être exporté si des utilisateurs finaux se reconnectent à une réunion qui n’a pas expiré et téléchargent un contenu qui y a été chargé ou prennent des captures d’écran dans le cas où le contenu a été généré.

Les réunions MeetNow qui ne se trouvent pas dans le calendrier Exchange, tout comme la liste de contacts et les droits des contacts (famille, collègue, etc.) se trouvent dans la base de données utilisateur. Dans Lync Server 2013 et les versions ultérieures, vous pouvez utiliser la cmdlet [Export-CsUserData](https://docs.microsoft.com/powershell/module/skype/export-csuserdata) pour exporter ces données.
