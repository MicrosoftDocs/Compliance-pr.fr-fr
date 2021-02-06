---
title: Contrôles d’accès administratif dans Microsoft 365
description: Cet article fournit une vue d’ensemble des contrôles d’accès administratifs et de la catégorisation des données dans Microsoft 365.
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
f1.keywords:
- NOCSH
ms.collection:
- Strat_O365_IP
- M365-security-compliance
- MS-Compliance
ms.custom: seo-marvel-apr2020
titleSuffix: Microsoft Service Assurance
ms.openlocfilehash: d3d6cd30fbe682de979d5c04943c57cedc86552f
ms.sourcegitcommit: 21ed42335efd37774ff5d17d9586d5546147241a
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 02/05/2021
ms.locfileid: "50120713"
---
# <a name="administrative-access-controls-in-microsoft-365"></a><span data-ttu-id="4c558-103">Contrôles d’accès administratif dans Microsoft 365</span><span class="sxs-lookup"><span data-stu-id="4c558-103">Administrative access controls in Microsoft 365</span></span> 

<span data-ttu-id="4c558-104">Microsoft a lourdement investi dans les systèmes et les contrôles qui automatisent la plupart des opérations De Microsoft 365 tout en limitant intentionnellement l’accès au contenu client par Microsoft.</span><span class="sxs-lookup"><span data-stu-id="4c558-104">Microsoft has invested heavily in systems and controls that automate most Microsoft 365 operations while intentionally limiting access to customer content by Microsoft.</span></span> <span data-ttu-id="4c558-105">Les humains régissent le service et les logiciels le gèrent.</span><span class="sxs-lookup"><span data-stu-id="4c558-105">Humans govern the service, and software operates the service.</span></span> <span data-ttu-id="4c558-106">Cette structure permet à Microsoft de gérer Microsoft 365 à grande échelle et de gérer les risques de menaces internes sur le contenu des clients.</span><span class="sxs-lookup"><span data-stu-id="4c558-106">This structure enables Microsoft to manage Microsoft 365 at scale and manage the risks of internal threats to customer content.</span></span>

<span data-ttu-id="4c558-107">Par défaut, les ingénieurs Microsoft n’ont aucun privilège administratif permanent et aucun accès permanent au contenu client dans Microsoft 365.</span><span class="sxs-lookup"><span data-stu-id="4c558-107">By default, Microsoft engineers have zero standing administrative privileges and zero standing access to customer content in Microsoft 365.</span></span> <span data-ttu-id="4c558-108">Un ingénieur Microsoft peut avoir un accès limité, audité et sécurisé au contenu d’un client pendant une durée limitée.</span><span class="sxs-lookup"><span data-stu-id="4c558-108">A Microsoft engineer can have limited, audited, and secured access to a customer's content for a limited amount of time.</span></span> <span data-ttu-id="4c558-109">L’accès est uniquement nécessaire pour les opérations de service et uniquement lorsqu’il est approuvé par un membre de la direction de Microsoft.</span><span class="sxs-lookup"><span data-stu-id="4c558-109">Access is only when necessary for service operations and only when approved by a member of Microsoft senior management.</span></span> <span data-ttu-id="4c558-110">Pour les clients titulaires d’une licence Customer Lockbox, le client fournit l’approbation de l’accès à son contenu hébergé sur Microsoft 365.</span><span class="sxs-lookup"><span data-stu-id="4c558-110">For Customer Lockbox licensed customers, the customer provides access approval to their content hosted on Microsoft 365.</span></span>

<span data-ttu-id="4c558-111">Microsoft fournit des services en ligne à l’aide de plusieurs formes de distribution cloud :</span><span class="sxs-lookup"><span data-stu-id="4c558-111">Microsoft provides online services using multiple forms of cloud delivery:</span></span>

- <span data-ttu-id="4c558-112">**Clouds publics :** Inclut des versions multi-clients de Microsoft 365, Azure et d’autres services hébergés en Amérique du Nord, en Amérique du Sud, en Europe, en Asie, en Australie, etc.</span><span class="sxs-lookup"><span data-stu-id="4c558-112">**Public clouds:** Includes multi-tenant versions of Microsoft 365, Azure, and other services hosted in North America, South America, Europe, Asia, Australia, etc.</span></span>
- <span data-ttu-id="4c558-113">**Clouds nationaux :** Inclut tous les clouds souverains et tiers gérés en dehors des États-Unis (à l’exception de ceux mentionnés précédemment), tels que Microsoft 365 en Chine (géré par 21Vianet) et Microsoft 365 en Allemagne (géré par Microsoft, mais selon un modèle dans lequel un tiers de confiance allemand, Deutsche Telekom, contrôle et surveille l’accès de Microsoft aux données client et aux systèmes qui contiennent des données client).</span><span class="sxs-lookup"><span data-stu-id="4c558-113">**National clouds:** Includes all sovereign and third party-operated clouds outside of the United States (except ones noted previously), such as Microsoft 365 in China (operated by 21Vianet), and Microsoft 365 in Germany (operated by Microsoft, but under a model in which a German data trustee, Deutsche Telekom, controls and monitors Microsoft's access to customer data and systems that contain customer data).</span></span>
- <span data-ttu-id="4c558-114">**Clouds pour le gouvernement :** Inclut les services Microsoft 365 et Azure disponibles pour les clients du gouvernement des États-Unis.</span><span class="sxs-lookup"><span data-stu-id="4c558-114">**Government clouds:** Includes Microsoft 365 and Azure services that are available to United States government customers.</span></span>

<span data-ttu-id="4c558-115">Dans le cadre de cet article, les services Microsoft 365 incluent :</span><span class="sxs-lookup"><span data-stu-id="4c558-115">For purposes of this article, Microsoft 365 services include:</span></span>

- [<span data-ttu-id="4c558-116">Exchange Online</span><span class="sxs-lookup"><span data-stu-id="4c558-116">Exchange Online</span></span>](/Exchange/exchange-online)
- [<span data-ttu-id="4c558-117">Exchange Online Protection</span><span class="sxs-lookup"><span data-stu-id="4c558-117">Exchange Online Protection</span></span>](/Office365/SecurityCompliance/eop/exchange-online-protection-overview)
- [<span data-ttu-id="4c558-118">SharePoint Online</span><span class="sxs-lookup"><span data-stu-id="4c558-118">SharePoint Online</span></span>](/sharepoint/sharepoint-online)
- [<span data-ttu-id="4c558-119">OneDrive Entreprise</span><span class="sxs-lookup"><span data-stu-id="4c558-119">OneDrive for Business</span></span>](/OneDrive/onedrive)
- [<span data-ttu-id="4c558-120">Skype Entreprise</span><span class="sxs-lookup"><span data-stu-id="4c558-120">Skype for Business</span></span>](/SkypeForBusiness/skype-for-business-online)
- [<span data-ttu-id="4c558-121">Microsoft Teams</span><span class="sxs-lookup"><span data-stu-id="4c558-121">Microsoft Teams</span></span>](/MicrosoftTeams/Teams-overview)
- [<span data-ttu-id="4c558-122">Yammer</span><span class="sxs-lookup"><span data-stu-id="4c558-122">Yammer</span></span>](/yammer/yammer-landing-page)

## <a name="microsoft-365-access-controls"></a><span data-ttu-id="4c558-123">Contrôles d’accès Microsoft 365</span><span class="sxs-lookup"><span data-stu-id="4c558-123">Microsoft 365 access controls</span></span>

<span data-ttu-id="4c558-124">À des fins de contrôle d’accès, Microsoft classe les données Microsoft 365 en tant que données client ou d’autres types de données.</span><span class="sxs-lookup"><span data-stu-id="4c558-124">For access control purposes, Microsoft categorizes Microsoft 365 data as customer data or other types of data.</span></span>

### <a name="customer-data"></a><span data-ttu-id="4c558-125">Données client</span><span class="sxs-lookup"><span data-stu-id="4c558-125">Customer data</span></span>

<span data-ttu-id="4c558-126">Les données client sont toutes les données fournies par ou pour le compte d’un client lors de l’utilisation des services Microsoft 365.</span><span class="sxs-lookup"><span data-stu-id="4c558-126">Customer data is all data provided by or on behalf of a customer when using Microsoft 365 services.</span></span> <span data-ttu-id="4c558-127">Ces données sont du contenu client directement créé ou téléchargé par les utilisateurs de Microsoft 365, notamment :</span><span class="sxs-lookup"><span data-stu-id="4c558-127">This data is customer content directly created or uploaded by Microsoft 365 users, including:</span></span>

- <span data-ttu-id="4c558-128">Messages électroniques</span><span class="sxs-lookup"><span data-stu-id="4c558-128">Emails</span></span>
- <span data-ttu-id="4c558-129">Contenu SharePoint Online</span><span class="sxs-lookup"><span data-stu-id="4c558-129">SharePoint Online content</span></span>
- <span data-ttu-id="4c558-130">Messages instantanés</span><span class="sxs-lookup"><span data-stu-id="4c558-130">Instant messages</span></span>
- <span data-ttu-id="4c558-131">Éléments de calendrier</span><span class="sxs-lookup"><span data-stu-id="4c558-131">Calendar items</span></span>
- <span data-ttu-id="4c558-132">Documents</span><span class="sxs-lookup"><span data-stu-id="4c558-132">Documents</span></span>
- <span data-ttu-id="4c558-133">Contacts</span><span class="sxs-lookup"><span data-stu-id="4c558-133">Contacts</span></span>
- <span data-ttu-id="4c558-134">Informations d’identification de l’utilisateur final (EUII) (données qui sont propres à un utilisateur ou qui sont accessibles à un utilisateur individuel, mais qui n’incluent pas de contenu client)</span><span class="sxs-lookup"><span data-stu-id="4c558-134">End-user identifiable information (EUII) (data that is unique to a user or that is linkable to an individual user but does not include customer content)</span></span>

### <a name="other-types-of-data"></a><span data-ttu-id="4c558-135">Autres types de données</span><span class="sxs-lookup"><span data-stu-id="4c558-135">Other types of data</span></span>

<span data-ttu-id="4c558-136">Les autres types de données sont les suivants :</span><span class="sxs-lookup"><span data-stu-id="4c558-136">Other types of data include:</span></span>

- <span data-ttu-id="4c558-137">**Données de compte :** Inclut les données administratives (informations fournies par les administrateurs lors de l’inscription ou de l’achat de services) et les données de paiement (informations sur les instrument de paiement, telles que les détails de carte de crédit).</span><span class="sxs-lookup"><span data-stu-id="4c558-137">**Account data:** Includes administrative data (information provided by administrators when they sign-up or purchase services), and payment data (information about payment instruments, such as credit card details).</span></span>
- <span data-ttu-id="4c558-138">**Informations d’identification organisationnelle :** Inclut les données utilisées pour identifier un client, les données d’utilisation et non accessibles à un utilisateur individuel ou incluses dans le contenu client.</span><span class="sxs-lookup"><span data-stu-id="4c558-138">**Organizationally identifiable information:** Includes data used to identify a tenant, usage data, and not linkable to an individual user or included in customer content.</span></span>
- <span data-ttu-id="4c558-139">**Métadonnées système :** Inclut les journaux de service qui contiennent les paramètres de configuration, l’état du système, les adresses IP Microsoft et des informations techniques sur les abonnements et les clients.</span><span class="sxs-lookup"><span data-stu-id="4c558-139">**System metadata:** Includes service logs that contain configuration settings, system status, Microsoft IP addresses, and technical information about subscriptions and tenants.</span></span>

<span data-ttu-id="4c558-140">Microsoft a mis en place des mécanismes de contrôle d’accès pour s’assurer que personne n’a un accès non autorisé aux données client ou aux données de contrôle d’accès.</span><span class="sxs-lookup"><span data-stu-id="4c558-140">Microsoft has established access control mechanisms to ensure that no one has unapproved access to Customer Data or access control data.</span></span> <span data-ttu-id="4c558-141">Les données de contrôle d’accès gèrent l’accès à d’autres types de données ou de fonctions au sein de l’environnement, y compris l’accès au contenu client ou à l’EUII, aux mots de passe Microsoft, aux certificats de sécurité et à d’autres données relatives à l’authentification.</span><span class="sxs-lookup"><span data-stu-id="4c558-141">Access control data manages access to other types of data or functions within the environment, including access to customer content or EUII, Microsoft passwords, security certificates, and other authentication-related data.</span></span> <span data-ttu-id="4c558-142">Les mécanismes de contrôle d’accès se prémunir également contre l’accès physique, logique ou distant non autorisé à l’environnement de production Microsoft 365.</span><span class="sxs-lookup"><span data-stu-id="4c558-142">Access control mechanisms also guard against unapproved physical, logical, or remote access to the Microsoft 365 production environment.</span></span>

<span data-ttu-id="4c558-143">Il existe trois catégories de contrôles d’accès utilisées par Microsoft pour l’exploitation de Microsoft 365 :</span><span class="sxs-lookup"><span data-stu-id="4c558-143">There are three categories of access controls used by Microsoft for operating Microsoft 365:</span></span>

- <span data-ttu-id="4c558-144">Contrôles d’isolation</span><span class="sxs-lookup"><span data-stu-id="4c558-144">Isolation controls</span></span>
- <span data-ttu-id="4c558-145">Contrôles du personnel</span><span class="sxs-lookup"><span data-stu-id="4c558-145">Personnel controls</span></span>
- <span data-ttu-id="4c558-146">Contrôles de technologie</span><span class="sxs-lookup"><span data-stu-id="4c558-146">Technology controls</span></span>

<span data-ttu-id="4c558-147">Lorsqu’ils sont combinés, ces contrôles permettent de prévenir et de détecter les actions malveillantes dans Microsoft 365.</span><span class="sxs-lookup"><span data-stu-id="4c558-147">When combined, these controls help prevent and detect malicious actions in Microsoft 365.</span></span> <span data-ttu-id="4c558-148">Outre les contrôles d’isolation, de personnel et de technologie utilisés par Microsoft, il existe une quatrième catégorie de contrôles : ces contrôles implémentés par les clients.</span><span class="sxs-lookup"><span data-stu-id="4c558-148">In addition to the isolation, personnel, and technology controls used by Microsoft, there is a fourth category of controls: those controls implemented by customers.</span></span>

<span data-ttu-id="4c558-149">Microsoft 365 vous permet de gérer les données de la même façon que dans les environnements locaux.</span><span class="sxs-lookup"><span data-stu-id="4c558-149">Microsoft 365 allows you to manage data the same way data is managed in on-premises environments.</span></span> <span data-ttu-id="4c558-150">La personne qui a signé une organisation pour Microsoft 365 devient automatiquement un administrateur général.</span><span class="sxs-lookup"><span data-stu-id="4c558-150">The person who signs up an organization for Microsoft 365 automatically becomes a global administrator.</span></span> <span data-ttu-id="4c558-151">L’administrateur global a accès à toutes les fonctionnalités des portails de gestion et peut :</span><span class="sxs-lookup"><span data-stu-id="4c558-151">The global admin has access to all features in Management Portals and can:</span></span>

- <span data-ttu-id="4c558-152">Créer ou modifier des utilisateurs</span><span class="sxs-lookup"><span data-stu-id="4c558-152">Create or edit users</span></span>
- <span data-ttu-id="4c558-153">Attribuer des rôles d’administrateur à d’autres personnes</span><span class="sxs-lookup"><span data-stu-id="4c558-153">Assign admin roles to others</span></span>
- <span data-ttu-id="4c558-154">Réinitialiser les mots de passe des utilisateurs</span><span class="sxs-lookup"><span data-stu-id="4c558-154">Reset user passwords</span></span>
- <span data-ttu-id="4c558-155">Gérer les licences utilisateur</span><span class="sxs-lookup"><span data-stu-id="4c558-155">Manage user licenses</span></span>
- <span data-ttu-id="4c558-156">Gérer les domaines</span><span class="sxs-lookup"><span data-stu-id="4c558-156">Manage domains</span></span>
- <span data-ttu-id="4c558-157">Approuver les demandes Customer Lockbox</span><span class="sxs-lookup"><span data-stu-id="4c558-157">Approve Customer Lockbox requests</span></span>

<span data-ttu-id="4c558-158">Il est recommandé que chaque organisation configure au moins deux comptes d’administrateur.</span><span class="sxs-lookup"><span data-stu-id="4c558-158">We recommend that each organization configure at least two admin accounts.</span></span> <span data-ttu-id="4c558-159">Pour les grandes entreprises, nous recommandons des comptes d’administrateur spécialisés qui servent différentes fonctions.</span><span class="sxs-lookup"><span data-stu-id="4c558-159">For large enterprise organizations, we recommend specialized admin accounts that serve different functions.</span></span>

<span data-ttu-id="4c558-160">Pour plus d’informations sur l’attribution de rôles d’administrateur et d’autorisations, voir Attribuer des rôles [d’administrateur](/microsoft-365/admin/add-users/assign-admin-roles) et [À propos des rôles d’administrateur.](/microsoft-365/admin/add-users/about-admin-roles)</span><span class="sxs-lookup"><span data-stu-id="4c558-160">For information about assigning admin roles and permissions, see [Assign admin roles](/microsoft-365/admin/add-users/assign-admin-roles) and [About admin roles](/microsoft-365/admin/add-users/about-admin-roles).</span></span>

## <a name="related-links"></a><span data-ttu-id="4c558-161">Liens connexes</span><span class="sxs-lookup"><span data-stu-id="4c558-161">Related Links</span></span>

- [<span data-ttu-id="4c558-162">Isolation dans Microsoft 365</span><span class="sxs-lookup"><span data-stu-id="4c558-162">Isolation in Microsoft 365</span></span>](assurance-isolation-in-microsoft-365.md)
- [<span data-ttu-id="4c558-163">Filtrage avant l’embauche chez Microsoft Corporation</span><span class="sxs-lookup"><span data-stu-id="4c558-163">Microsoft pre-employment screening</span></span>](assurance-pre-employment-screening.md)
- [<span data-ttu-id="4c558-164">Vérification des antécédents de Microsoft Cloud</span><span class="sxs-lookup"><span data-stu-id="4c558-164">Microsoft cloud background check</span></span>](assurance-cloud-background-check.md)
- [<span data-ttu-id="4c558-165">Surveillance et audit des contrôles d’accès</span><span class="sxs-lookup"><span data-stu-id="4c558-165">Monitoring and Auditing Access Controls</span></span>](assurance-monitoring-and-auditing-access-controls.md)
- [<span data-ttu-id="4c558-166">Contrôles d’accès de Yammer Entreprise</span><span class="sxs-lookup"><span data-stu-id="4c558-166">Yammer Enterprise Access Controls</span></span>](assurance-yammer-enterprise-access-controls.md)
