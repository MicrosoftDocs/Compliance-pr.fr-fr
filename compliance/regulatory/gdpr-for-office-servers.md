---
title: RGPD pour les serveurs Office
description: Découvrez comment répondre aux exigences en matière de Règlement général sur la protection des données (RGPD) dans les serveurs locaux d’Office.
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
ms.custom: seo-marvel-apr2020
hideEdit: true
ms.openlocfilehash: 58f3d9108fe36175c2ce879054a35c2cc94d93c8
ms.sourcegitcommit: 024137a15ab23d26cac5ec14c36f3577fd8a0cc4
ms.translationtype: HT
ms.contentlocale: fr-FR
ms.lasthandoff: 04/01/2021
ms.locfileid: "51496078"
---
# <a name="gdpr-for-office-on-premises-servers"></a><span data-ttu-id="4674a-103">RGPD pour les serveurs Office locaux</span><span class="sxs-lookup"><span data-stu-id="4674a-103">GDPR for Office on-premises Servers</span></span>

<span data-ttu-id="4674a-p101">Le Règlement général sur la protection des données (RGPD) présente les exigences que doivent respecter les organisations pour protéger les données personnelles et répondre aux demandes de personnes concernées de façon appropriée. Cette série d’articles présente les approches recommandées pour les charges de travail locales :</span><span class="sxs-lookup"><span data-stu-id="4674a-p101">The General Data Protection Regulation (GDPR) introduces requirements for organizations to protect personal data and respond appropriately to data subject requests. This series of articles provides recommended approaches for on-premises workloads:</span></span>

- [<span data-ttu-id="4674a-106">SharePoint Server</span><span class="sxs-lookup"><span data-stu-id="4674a-106">SharePoint Server</span></span>](gdpr-for-sharepoint-server.md)

- [<span data-ttu-id="4674a-107">Exchange Server</span><span class="sxs-lookup"><span data-stu-id="4674a-107">Exchange Server</span></span>](gdpr-for-exchange-server.md)

- [<span data-ttu-id="4674a-108">Skype Entreprise Server</span><span class="sxs-lookup"><span data-stu-id="4674a-108">Skype for Business Server</span></span>](gdpr-for-skype-for-business-server.md)

- [<span data-ttu-id="4674a-109">Project Server</span><span class="sxs-lookup"><span data-stu-id="4674a-109">Project Server</span></span>](gdpr-for-project-server.md)

- [<span data-ttu-id="4674a-110">Office Web Apps Server et Office Online Server</span><span class="sxs-lookup"><span data-stu-id="4674a-110">Office Web Apps Server and Office Online Server</span></span>](gdpr-for-office-online-server.md)

- [<span data-ttu-id="4674a-111">Partages de fichiers en local</span><span class="sxs-lookup"><span data-stu-id="4674a-111">On-premises file shares</span></span>](gdpr-for-on-premises-file-shares.md)

<span data-ttu-id="4674a-112">Pour plus d’informations sur le RGPD et sur l’aide que peut vous apporter Microsoft, reportez-vous au [centre de gestion de la confidentialité](https://www.microsoft.com/trust-center/privacy/gdpr-overview
).</span><span class="sxs-lookup"><span data-stu-id="4674a-112">For more information about the GDPR and how Microsoft can help you, see the [Microsoft Trust Center](https://www.microsoft.com/trust-center/privacy/gdpr-overview
).</span></span>

<span data-ttu-id="4674a-p102">Avant d’entreprendre toute action concernant des données locales, consultez vos équipes juridiques et de conformité pour leur demander conseil et pour en savoir plus sur les schémas de classification existants et les approches en matière d’utilisation de données personnelles. Microsoft fournit des recommandations pour développer et améliorer les schémas de classification dans son Kit de détection de données du RGPD à l’adresse [https://aka.ms/gdprpartners](<https://aka.ms/gdprpartners>). Ce kit décrit également les approches possibles pour déplacer des données locales vers le cloud, dans lequel vous pouvez utiliser des fonctionnalités de gouvernance des données plus avancées si vous le souhaitez. Les articles de cette section fournissent des recommandations pour les données qui sont destinées à rester au niveau local.</span><span class="sxs-lookup"><span data-stu-id="4674a-p102">Before doing any work with on-premises data, consult with your legal and compliance teams to seek guidance and to learn about existing classification schemas and approaches to working with personal data. Microsoft provides recommendations for developing and extending classifications schemas in the Microsoft GDPR Data Discovery Toolkit at [https://aka.ms/gdprpartners](<https://aka.ms/gdprpartners>). This toolkit also describes approaches for moving on-premises data to the cloud where you can use more sophisticated data governance capabilities, if this is desired. The articles in this section provide recommendations for data that is intended to remain on premises.</span></span>

<span data-ttu-id="4674a-p103">L’illustration suivante regroupe les fonctionnalités que nous vous recommandons d’utiliser pour chacune des charges de travail suivantes afin de repérer, classer, protéger et surveiller les données personnelles. Consultez les articles de cette section pour obtenir plus d’informations.</span><span class="sxs-lookup"><span data-stu-id="4674a-p103">The following illustration lists recommended capabilities to use across each of these workloads to discover, classify, protect, and monitor personal data. See the articles in this section for more information.</span></span>

![Diagramme décrivant les fonctionnalités de découverte, de classement, de protection et de surveillance des données personnelles dans les charges de travail](../media/gdpr-for-office-servers-image1.png)

## <a name="illustration-description"></a><span data-ttu-id="4674a-120">Description de l’illustration</span><span class="sxs-lookup"><span data-stu-id="4674a-120">Illustration description</span></span>

<span data-ttu-id="4674a-121">Concernant l’accessibilité, le tableau suivant fournit les mêmes exemples dans l’illustration.</span><span class="sxs-lookup"><span data-stu-id="4674a-121">For accessibility, the following table provides the same examples in the illustration.</span></span>

****

|<span data-ttu-id="4674a-122">Action</span><span class="sxs-lookup"><span data-stu-id="4674a-122">Action</span></span>|<span data-ttu-id="4674a-123">Partages de fichiers Windows Server</span><span class="sxs-lookup"><span data-stu-id="4674a-123">Windows Server file shares</span></span>|<span data-ttu-id="4674a-124">SharePoint Server</span><span class="sxs-lookup"><span data-stu-id="4674a-124">SharePoint Server</span></span>|<span data-ttu-id="4674a-125">Exchange Server</span><span class="sxs-lookup"><span data-stu-id="4674a-125">Exchange Server</span></span>|<span data-ttu-id="4674a-126">Skype Entreprise</span><span class="sxs-lookup"><span data-stu-id="4674a-126">Skype for Business</span></span>|<span data-ttu-id="4674a-127">Project Server</span><span class="sxs-lookup"><span data-stu-id="4674a-127">Project Server</span></span>|
|---|---|---|---|---|---|
|<span data-ttu-id="4674a-128">Découvrir</span><span class="sxs-lookup"><span data-stu-id="4674a-128">Discover</span></span>|<span data-ttu-id="4674a-129">Scanneur Azure Information Protection<sup>\*</sup></span><span class="sxs-lookup"><span data-stu-id="4674a-129">Azure Information Protection scanner<sup>\*</sup></span></span>|<span data-ttu-id="4674a-130">Centre de recherche ou eDiscovery (une fois les données classées)</span><span class="sxs-lookup"><span data-stu-id="4674a-130">Search Center or eDiscovery (after data is classified)</span></span> <br/><br/> <span data-ttu-id="4674a-131">Scanneur Azure Information Protection<sup>\*</sup></span><span class="sxs-lookup"><span data-stu-id="4674a-131">Azure Information Protection scanner<sup>\*</sup></span></span>|<span data-ttu-id="4674a-132">Portail eDiscovery Exchange</span><span class="sxs-lookup"><span data-stu-id="4674a-132">Exchange eDiscovery Portal</span></span>|<span data-ttu-id="4674a-133">Portail eDiscovery Exchange</span><span class="sxs-lookup"><span data-stu-id="4674a-133">Exchange eDiscovery portal</span></span>|<span data-ttu-id="4674a-134">Scripts SQL de découverte et d’exportation</span><span class="sxs-lookup"><span data-stu-id="4674a-134">SQL scripts for discovery and exporting</span></span>|
|<span data-ttu-id="4674a-135">Classer</span><span class="sxs-lookup"><span data-stu-id="4674a-135">Classify</span></span>|<span data-ttu-id="4674a-136">Scanneur Azure Information Protection<sup>\*</sup></span><span class="sxs-lookup"><span data-stu-id="4674a-136">Azure Information Protection scanner<sup>\*</sup></span></span> <br/><br/> <span data-ttu-id="4674a-137">Types d'informations sensibles Office 365</span><span class="sxs-lookup"><span data-stu-id="4674a-137">Office 365 sensitive information types</span></span>|<span data-ttu-id="4674a-138">Scanneur Azure Information Protection<sup>\*</sup></span><span class="sxs-lookup"><span data-stu-id="4674a-138">Azure Information Protection scanner<sup>\*</sup></span></span> <br/><br/> <span data-ttu-id="4674a-139">Types d'informations sensibles Office 365</span><span class="sxs-lookup"><span data-stu-id="4674a-139">Office 365 sensitive information types</span></span>|<span data-ttu-id="4674a-140">Balises et stratégies de rétention Exchange</span><span class="sxs-lookup"><span data-stu-id="4674a-140">Exchange retention tags and retention policies</span></span>|<span data-ttu-id="4674a-141">Balises et stratégies de rétention Exchange</span><span class="sxs-lookup"><span data-stu-id="4674a-141">Exchange retention tags and retention policies</span></span>||
|<span data-ttu-id="4674a-142">Protéger</span><span class="sxs-lookup"><span data-stu-id="4674a-142">Protect</span></span>||<span data-ttu-id="4674a-143">Règles de protection contre la perte de données Exchange Server</span><span class="sxs-lookup"><span data-stu-id="4674a-143">Exchange Server data loss prevention rules</span></span> <br/><br/> <span data-ttu-id="4674a-144">Autorisations, protection par IRM pour les bibliothèques</span><span class="sxs-lookup"><span data-stu-id="4674a-144">Permissions, IRM-protection for libraries</span></span>|<span data-ttu-id="4674a-145">Règles de protection contre la perte de données Exchange Server</span><span class="sxs-lookup"><span data-stu-id="4674a-145">Exchange Server data loss prevention rules</span></span> <br/><br/> <span data-ttu-id="4674a-146">Intégration IRM à Exchange Server</span><span class="sxs-lookup"><span data-stu-id="4674a-146">IRM integration with Exchange Server</span></span>|||
|<span data-ttu-id="4674a-147">Surveiller</span><span class="sxs-lookup"><span data-stu-id="4674a-147">Monitor</span></span>|<span data-ttu-id="4674a-148">Intégrer des outils SIEM aux journaux</span><span class="sxs-lookup"><span data-stu-id="4674a-148">Integrate logs with SIEM tools</span></span>|<span data-ttu-id="4674a-149">Intégrer des outils SIEM aux journaux</span><span class="sxs-lookup"><span data-stu-id="4674a-149">Integrate logs with SIEM tools</span></span>|<span data-ttu-id="4674a-150">Intégrer des outils SIEM aux journaux</span><span class="sxs-lookup"><span data-stu-id="4674a-150">Integrate logs with SIEM tools</span></span>|<span data-ttu-id="4674a-151">Intégrer des outils SIEM aux journaux</span><span class="sxs-lookup"><span data-stu-id="4674a-151">Integrate logs with SIEM tools</span></span>|<span data-ttu-id="4674a-152">Intégrer des outils SIEM aux journaux</span><span class="sxs-lookup"><span data-stu-id="4674a-152">Integrate logs with SIEM tools</span></span>|
|

<span data-ttu-id="4674a-153"><sup>\*</sup>Veuillez noter qu’une protection chiffre le fichier.</span><span class="sxs-lookup"><span data-stu-id="4674a-153"><sup>\*</sup> Note that protection encrypts the file.</span></span> <span data-ttu-id="4674a-154">Cela empêche SharePoint Server de trouver les types d’informations sensibles dans les fichiers protégés.</span><span class="sxs-lookup"><span data-stu-id="4674a-154">Consequently, SharePoint Server can't find the sensitive information types in protected files.</span></span>
