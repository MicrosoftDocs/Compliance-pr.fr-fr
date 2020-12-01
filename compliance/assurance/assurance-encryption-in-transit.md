---
title: Chiffrement des données en transit
description: Dans cet article, vous trouverez une brève explication de la manière dont Microsoft chiffre les données client Microsoft 365 en transit.
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
ms.openlocfilehash: d1587e4bc315f99dc554158500638645606fbcec
ms.sourcegitcommit: 626b0076d133e588cd28598c149a7f272fc18bae
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 11/30/2020
ms.locfileid: "49506739"
---
# <a name="encryption-for-data-in-transit"></a>Chiffrement des données en transit

Microsoft utilise les technologies de chiffrement pour protéger les données des clients non seulement au repos, mais aussi en transit. Les données sont en transit :

- Lorsqu’un ordinateur client communique avec un serveur Microsoft ;
- Lorsqu’un serveur Microsoft communique avec un autre serveur Microsoft ; les
- Lorsqu’un serveur Microsoft communique avec un serveur non-Microsoft (par exemple, Exchange Online de remise de courrier électronique à un serveur de messagerie tiers).

Les communications du centre interdonnées entre les serveurs Microsoft ont lieu sur TLS ou IPsec, et tous les serveurs faisant face au client négocient une session sécurisée à l’aide de TLS avec des machines client (par exemple, Exchange Online utilise TLS 1,2 avec la force de chiffrement 256 bits est utilisée (FIPS 140-2 niveau 2 validé). (Consultez les [Détails de référence technique sur le chiffrement](https://docs.microsoft.com/microsoft-365/compliance/technical-reference-details-about-encryption) pour obtenir la liste des suites de chiffrement TLS prises en charge par Office 365.) Cela s’applique aux protocoles utilisés par des clients tels qu’Outlook, Skype entreprise, Microsoft teams et Outlook sur le Web (par exemple, HTTP, POP3, etc.).

Les certificats publics sont émis par Microsoft IT SSL à l’aide de SSLAdmin, un outil Microsoft interne permettant de protéger la confidentialité des informations transmises. Tous les certificats émis par le service informatique de Microsoft ont une longueur minimale de 2048 bits et la conformité WebTrust nécessite SSLAdmin pour s’assurer que les certificats sont émis uniquement vers des adresses IP publiques appartenant à Microsoft. Toutes les adresses IP qui ne satisfont pas à ce critère sont routées via un processus d’exception.

Tous les détails de l’implémentation, tels que la version de TLS utilisée, si le protocole FS (Forward Secrecy) est activé, l’ordre des suites de chiffrement, etc., sont disponibles publiquement. Pour voir ces informations, vous pouvez utiliser un site Web tiers, tel que les [ateliers de Qualys SSL](https://www.ssllabs.com). Vous trouverez ci-dessous les liens vers les pages de test automatisées de Qualys qui affichent des informations sur les services suivants :

- [Portail Office 365](https://www.ssllabs.com/ssltest/analyze.html?d=portal.office.com&hideResults=on)
- [Exchange Online](https://www.ssllabs.com/ssltest/analyze.html?d=outlook.office365.com&hideResults=on)
- [SharePoint Online](https://www.ssllabs.com/ssltest/analyze.html?d=microsoft-my.sharepoint.com&hideResults=on)
- [Skype entreprise (SIP)](https://www.ssllabs.com/ssltest/analyze.html?d=sipdir.online.lync.com)
- [Skype entreprise (Web)](https://www.ssllabs.com/ssltest/analyze.html?d=webdir.online.lync.com&hideResults=on)
- [Exchange Online Protection](https://ssl-tools.net/mailservers/microsoft-com.mail.protection.outlook.com)
- [Microsoft Teams](https://www.ssllabs.com/ssltest/analyze.html?d=teams.microsoft.com&latest)

Pour Exchange Online Protection, les URL varient en fonction des noms de client ; Toutefois, tous les clients peuvent tester Microsoft 365 à l’aide de **Microsoft-com.mail.protection.Outlook.com**.
