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
# <a name="encryption-for-data-in-transit"></a><span data-ttu-id="c6e9a-103">Chiffrement des données en transit</span><span class="sxs-lookup"><span data-stu-id="c6e9a-103">Encryption for data-in-transit</span></span>

<span data-ttu-id="c6e9a-104">Microsoft utilise les technologies de chiffrement pour protéger les données des clients non seulement au repos, mais aussi en transit.</span><span class="sxs-lookup"><span data-stu-id="c6e9a-104">In addition to protecting customer data at rest, Microsoft uses encryption technologies to protect customer data in transit.</span></span> <span data-ttu-id="c6e9a-105">Les données sont en transit :</span><span class="sxs-lookup"><span data-stu-id="c6e9a-105">Data is in transit:</span></span>

- <span data-ttu-id="c6e9a-106">Lorsqu’un ordinateur client communique avec un serveur Microsoft ;</span><span class="sxs-lookup"><span data-stu-id="c6e9a-106">when a client machine communicates with a Microsoft server;</span></span>
- <span data-ttu-id="c6e9a-107">Lorsqu’un serveur Microsoft communique avec un autre serveur Microsoft ; les</span><span class="sxs-lookup"><span data-stu-id="c6e9a-107">when a Microsoft server communicates with another Microsoft server; and</span></span>
- <span data-ttu-id="c6e9a-108">Lorsqu’un serveur Microsoft communique avec un serveur non-Microsoft (par exemple, Exchange Online de remise de courrier électronique à un serveur de messagerie tiers).</span><span class="sxs-lookup"><span data-stu-id="c6e9a-108">when a Microsoft server communicates with a non-Microsoft server (for example, Exchange Online delivering email to a third-party email server).</span></span>

<span data-ttu-id="c6e9a-109">Les communications du centre interdonnées entre les serveurs Microsoft ont lieu sur TLS ou IPsec, et tous les serveurs faisant face au client négocient une session sécurisée à l’aide de TLS avec des machines client (par exemple, Exchange Online utilise TLS 1,2 avec la force de chiffrement 256 bits est utilisée (FIPS 140-2 niveau 2 validé).</span><span class="sxs-lookup"><span data-stu-id="c6e9a-109">Inter-data center communications between Microsoft servers take place over TLS or IPsec, and all customer-facing servers negotiate a secure session using TLS with client machines (for example, Exchange Online uses TLS 1.2 with 256-bit cipher strength is used (FIPS 140-2 Level 2-validated).</span></span> <span data-ttu-id="c6e9a-110">(Consultez les [Détails de référence technique sur le chiffrement](https://docs.microsoft.com/microsoft-365/compliance/technical-reference-details-about-encryption) pour obtenir la liste des suites de chiffrement TLS prises en charge par Office 365.) Cela s’applique aux protocoles utilisés par des clients tels qu’Outlook, Skype entreprise, Microsoft teams et Outlook sur le Web (par exemple, HTTP, POP3, etc.).</span><span class="sxs-lookup"><span data-stu-id="c6e9a-110">(See [Technical reference details about encryption](https://docs.microsoft.com/microsoft-365/compliance/technical-reference-details-about-encryption) for a list of TLS cipher suites supported by Office 365.) This applies to the protocols that are used by clients such as Outlook, Skype for Business, Microsoft Teams, and Outlook on the web (for example, HTTP, POP3, etc.).</span></span>

<span data-ttu-id="c6e9a-111">Les certificats publics sont émis par Microsoft IT SSL à l’aide de SSLAdmin, un outil Microsoft interne permettant de protéger la confidentialité des informations transmises.</span><span class="sxs-lookup"><span data-stu-id="c6e9a-111">The public certificates are issued by Microsoft IT SSL using SSLAdmin, an internal Microsoft tool to protect confidentiality of transmitted information.</span></span> <span data-ttu-id="c6e9a-112">Tous les certificats émis par le service informatique de Microsoft ont une longueur minimale de 2048 bits et la conformité WebTrust nécessite SSLAdmin pour s’assurer que les certificats sont émis uniquement vers des adresses IP publiques appartenant à Microsoft.</span><span class="sxs-lookup"><span data-stu-id="c6e9a-112">All certificates issued by Microsoft IT have a minimum of 2048 bits in length, and Webtrust compliance requires SSLAdmin to make sure that certificates are issued only to public IP addresses owned by Microsoft.</span></span> <span data-ttu-id="c6e9a-113">Toutes les adresses IP qui ne satisfont pas à ce critère sont routées via un processus d’exception.</span><span class="sxs-lookup"><span data-stu-id="c6e9a-113">Any IP addresses that fail to meet this criterion are routed through an exception process.</span></span>

<span data-ttu-id="c6e9a-114">Tous les détails de l’implémentation, tels que la version de TLS utilisée, si le protocole FS (Forward Secrecy) est activé, l’ordre des suites de chiffrement, etc., sont disponibles publiquement.</span><span class="sxs-lookup"><span data-stu-id="c6e9a-114">All implementation details such as the version of TLS being used, whether Forward Secrecy (FS) is enabled, the order of cipher suites, etc., are available publicly.</span></span> <span data-ttu-id="c6e9a-115">Pour voir ces informations, vous pouvez utiliser un site Web tiers, tel que les [ateliers de Qualys SSL](https://www.ssllabs.com).</span><span class="sxs-lookup"><span data-stu-id="c6e9a-115">One way to see these details is to use a third-party website, such as [Qualys SSL Labs](https://www.ssllabs.com).</span></span> <span data-ttu-id="c6e9a-116">Vous trouverez ci-dessous les liens vers les pages de test automatisées de Qualys qui affichent des informations sur les services suivants :</span><span class="sxs-lookup"><span data-stu-id="c6e9a-116">Below are the links to automated test pages from Qualys that display information for the following services:</span></span>

- [<span data-ttu-id="c6e9a-117">Portail Office 365</span><span class="sxs-lookup"><span data-stu-id="c6e9a-117">Office 365 Portal</span></span>](https://www.ssllabs.com/ssltest/analyze.html?d=portal.office.com&hideResults=on)
- [<span data-ttu-id="c6e9a-118">Exchange Online</span><span class="sxs-lookup"><span data-stu-id="c6e9a-118">Exchange Online</span></span>](https://www.ssllabs.com/ssltest/analyze.html?d=outlook.office365.com&hideResults=on)
- [<span data-ttu-id="c6e9a-119">SharePoint Online</span><span class="sxs-lookup"><span data-stu-id="c6e9a-119">SharePoint Online</span></span>](https://www.ssllabs.com/ssltest/analyze.html?d=microsoft-my.sharepoint.com&hideResults=on)
- [<span data-ttu-id="c6e9a-120">Skype entreprise (SIP)</span><span class="sxs-lookup"><span data-stu-id="c6e9a-120">Skype for Business (SIP)</span></span>](https://www.ssllabs.com/ssltest/analyze.html?d=sipdir.online.lync.com)
- [<span data-ttu-id="c6e9a-121">Skype entreprise (Web)</span><span class="sxs-lookup"><span data-stu-id="c6e9a-121">Skype for Business (Web)</span></span>](https://www.ssllabs.com/ssltest/analyze.html?d=webdir.online.lync.com&hideResults=on)
- [<span data-ttu-id="c6e9a-122">Exchange Online Protection</span><span class="sxs-lookup"><span data-stu-id="c6e9a-122">Exchange Online Protection</span></span>](https://ssl-tools.net/mailservers/microsoft-com.mail.protection.outlook.com)
- [<span data-ttu-id="c6e9a-123">Microsoft Teams</span><span class="sxs-lookup"><span data-stu-id="c6e9a-123">Microsoft Teams</span></span>](https://www.ssllabs.com/ssltest/analyze.html?d=teams.microsoft.com&latest)

<span data-ttu-id="c6e9a-124">Pour Exchange Online Protection, les URL varient en fonction des noms de client ; Toutefois, tous les clients peuvent tester Microsoft 365 à l’aide de **Microsoft-com.mail.protection.Outlook.com**.</span><span class="sxs-lookup"><span data-stu-id="c6e9a-124">For Exchange Online Protection, URLs vary by tenant names; however, all customers can test Microsoft 365 using **microsoft-com.mail.protection.outlook.com**.</span></span>
