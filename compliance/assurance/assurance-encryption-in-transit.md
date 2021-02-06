---
title: Chiffrement des données en transit
description: Dans cet article, trouvez une brève explication de la façon dont Microsoft chiffre les données client Microsoft 365 en transit.
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
- MS-Compliance
ms.custom: seo-marvel-apr2020
titleSuffix: Microsoft Service Assurance
ms.openlocfilehash: b6d6ae53ef2ade842e0e9205c01b44fe17891a97
ms.sourcegitcommit: 21ed42335efd37774ff5d17d9586d5546147241a
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 02/05/2021
ms.locfileid: "50120533"
---
# <a name="encryption-for-data-in-transit"></a>Chiffrement des données en transit

Microsoft utilise les technologies de chiffrement pour protéger les données des clients non seulement au repos, mais aussi en transit. Les données sont en transit :

- lorsqu’un ordinateur client communique avec un serveur Microsoft ;
- lorsqu’un serveur Microsoft communique avec un autre serveur Microsoft ; et
- lorsqu’un serveur Microsoft communique avec un serveur non-Microsoft (par exemple, Exchange Online qui envoie du courrier électronique à un serveur de messagerie tiers).

Les communications entre les serveurs Du centre de données entre les serveurs Microsoft ont lieu via TLS ou IPsec, et tous les serveurs orientés client négocient une session sécurisée à l’aide de TLS avec des ordinateurs clients (par exemple, Exchange Online utilise TLS 1.2 avec une puissance de chiffrement 256 bits est utilisée (fiPS 140-2 niveau 2 validé). (Voir [les détails de référence technique sur](/microsoft-365/compliance/technical-reference-details-about-encryption) le chiffrement pour obtenir la liste des suites de chiffrement TLS pris en charge par Office 365.) Cela s’applique aux protocoles utilisés par des clients tels qu’Outlook, Skype Entreprise, Microsoft Teams et Outlook sur le web (par exemple, HTTP, POP3, etc.).

Les certificats publics sont émis par Microsoft IT SSL à l’aide de SSLAdmin, un outil Microsoft interne qui protège la confidentialité des informations transmises. Tous les certificats émis par microsoft it ont une longueur minimale de 2 048 bits et la conformité Webtrust nécessite SSLAdmin pour s’assurer que les certificats sont émis uniquement aux adresses IP publiques de Microsoft. Toutes les adresses IP qui ne répondent pas à ce critère sont acheminées via un processus d’exception.

Tous les détails d’implémentation tels que la version de TLS utilisée, si le secret de forward (FS) est activé, l’ordre des suites de chiffrement, etc., sont disponibles publiquement. Une façon de consulter ces détails consiste à utiliser un site web tiers, tel que [les ateliers SSL Qualys.](https://www.ssllabs.com) Vous trouverez ci-dessous des liens vers des pages de test automatisées de Qualys qui affichent des informations pour les services suivants :

- [Portail Office 365](https://www.ssllabs.com/ssltest/analyze.html?d=portal.office.com&hideResults=on)
- [Exchange Online](https://www.ssllabs.com/ssltest/analyze.html?d=outlook.office365.com&hideResults=on)
- [SharePoint Online](https://www.ssllabs.com/ssltest/analyze.html?d=microsoft-my.sharepoint.com&hideResults=on)
- [Skype Entreprise (SIP)](https://www.ssllabs.com/ssltest/analyze.html?d=sipdir.online.lync.com)
- [Skype Entreprise (Web)](https://www.ssllabs.com/ssltest/analyze.html?d=webdir.online.lync.com&hideResults=on)
- [Exchange Online Protection](https://ssl-tools.net/mailservers/microsoft-com.mail.protection.outlook.com)
- [Microsoft Teams](https://www.ssllabs.com/ssltest/analyze.html?d=teams.microsoft.com&latest)

Pour Exchange Online Protection, les URL varient en fonction des noms de client . toutefois, tous les clients peuvent tester Microsoft 365 à **l’aide de microsoft-com.mail.protection.outlook.com**.
