---
title: Département de la Défense (DoD) Impact Niveau 2 (IL2)
description: Découvrez comment Microsoft répond aux normes d’impact de niveau 2 (IL2) du département de la Défense (DoD).
keywords: Offres pour la conformité Microsoft 365
localization_priority: None
ms.prod: microsoft-365-enterprise
ms.topic: article
f1.keywords:
- NOCSH
ms.author: robmazz
author: robmazz
manager: laurawi
audience: itpro
ms.collection:
- M365-security-compliance
- MS-Compliance
hideEdit: true
titleSuffix: Microsoft Compliance
ms.openlocfilehash: 77e8cb50f815c167e50293d495b4a548a73d022e
ms.sourcegitcommit: 9b0c8852e73e2be54a0f9c6570da67f4964f616c
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 07/12/2021
ms.locfileid: "53385722"
---
# <a name="department-of-defense-dod-impact-level-2-il2"></a><span data-ttu-id="9f744-104">Département de la Défense (DoD) Impact Niveau 2 (IL2)</span><span class="sxs-lookup"><span data-stu-id="9f744-104">Department of Defense (DoD) Impact Level 2 (IL2)</span></span>

## <a name="dod-il2-overview"></a><span data-ttu-id="9f744-105">Vue d’ensemble de DoD IL2</span><span class="sxs-lookup"><span data-stu-id="9f744-105">DoD IL2 overview</span></span>

<span data-ttu-id="9f744-106">La Defense Information Systems Agency (DISA) est une agence du département américain de la Défense (DoD) qui est responsable du développement et de la maintenance du Guide dod cloud computing [security requirements (SRG)](https://dl.dod.cyber.mil/wp-content/uploads/cloud/SRG/index.html).</span><span class="sxs-lookup"><span data-stu-id="9f744-106">The Defense Information Systems Agency (DISA) is an agency of the US Department of Defense (DoD) that is responsible for developing and maintaining the DoD Cloud Computing [Security Requirements Guide (SRG)](https://dl.dod.cyber.mil/wp-content/uploads/cloud/SRG/index.html).</span></span> <span data-ttu-id="9f744-107">Le SRG définit les exigences de sécurité de base utilisées par DoD pour évaluer la posture de sécurité d’un fournisseur de services cloud (CSP), en appuyant la décision d’accorder une autorisation provisoire DoD (PA) qui permet à un fournisseur CSP d’héberger des missions DoD.</span><span class="sxs-lookup"><span data-stu-id="9f744-107">The SRG defines the baseline security requirements used by DoD to assess the security posture of a cloud service provider (CSP), supporting the decision to grant a DoD Provisional Authorization (PA) that allows a CSP to host DoD missions.</span></span> <span data-ttu-id="9f744-108">Il incorpore, annule et annule le modèle CSM (DoD Cloud Security Model) publié précédemment et se mappe sur DoD Risk Management Framework (RMF).</span><span class="sxs-lookup"><span data-stu-id="9f744-108">It incorporates, supersedes, and rescinds the previously published DoD Cloud Security Model (CSM) and maps to the DoD Risk Management Framework (RMF).</span></span>

<span data-ttu-id="9f744-109">DISA guide les agences et services DoD dans la planification et l’autorisation de l’utilisation d’un programme CSP.</span><span class="sxs-lookup"><span data-stu-id="9f744-109">DISA guides DoD agencies and departments in planning and authorizing the use of a CSP.</span></span> <span data-ttu-id="9f744-110">Il évalue également les offres de CSP pour la conformité avec le SRG, un processus d’autorisation dans lequel les CSP peuvent fournir de la documentation sur leur conformité aux normes DoD.</span><span class="sxs-lookup"><span data-stu-id="9f744-110">It also evaluates CSP offerings for compliance with the SRG, an authorization process whereby CSPs can furnish documentation outlining their compliance with DoD standards.</span></span> <span data-ttu-id="9f744-111">Les autorisations provisoires DoD sont émises le cas échéant, de sorte que les agences DoD et les organisations de support peuvent utiliser les services cloud sans avoir à passer par un processus d’approbation complet, ce qui permet de gagner du temps et des efforts.</span><span class="sxs-lookup"><span data-stu-id="9f744-111">It issues DoD Provisional Authorizations (PAs) when appropriate, so DoD agencies and supporting organizations can use cloud services without having to go through a full approval process on their own, saving time and effort.</span></span>

<span data-ttu-id="9f744-112">Le mémo DoD CIO du [15 décembre 2014](https://www.esi.mil/contentview.aspx?id=585) concernant les conseils mis à jour sur l’acquisition et l’utilisation des services cloud *computing* commerciaux indique que « FedRAMP servira de base de sécurité minimale pour tous les services cloud DoD ».</span><span class="sxs-lookup"><span data-stu-id="9f744-112">The [15 December 2014 DoD CIO memo](https://www.esi.mil/contentview.aspx?id=585) regarding *Updated Guidance on the Acquisition and Use of Commercial Cloud Computing Services* states that 'FedRAMP will serve as the minimum security baseline for all DoD cloud services'.</span></span> <span data-ttu-id="9f744-113">Le SRG utilise la ligne de base modéré FedRAMP à tous les niveaux d’impact sur les informations (IL) et prend en compte la ligne de base élevée à certains niveaux.</span><span class="sxs-lookup"><span data-stu-id="9f744-113">The SRG uses the FedRAMP Moderate baseline at all information impact levels (IL) and considers the High Baseline at some.</span></span>

<span data-ttu-id="9f744-114">La [section SRG 5.1.1](https://dl.dod.cyber.mil/wp-content/uploads/cloud/SRG/index.html#5SECURITYREQUIREMENTS) Utilisation dod des contrôles de sécurité *FedRAMP* indique que les informations IL2 peuvent être hébergées dans un CSP qui contient au minimum une pa modéré FedRAMP et une autorité de sécurité DoD Level 2, sous réserve de conformité avec les exigences de sécurité du personnel décrites à la section 5.6.2.</span><span class="sxs-lookup"><span data-stu-id="9f744-114">[SRG Section 5.1.1](https://dl.dod.cyber.mil/wp-content/uploads/cloud/SRG/index.html#5SECURITYREQUIREMENTS) *DoD use of FedRAMP Security Controls* states that IL2 information may be hosted in a CSP that minimally holds a FedRAMP Moderate PA and a DoD Level 2 PA, subject to compliance with the personnel security requirements outlined in Section 5.6.2.</span></span> <span data-ttu-id="9f744-115">Toutefois, cette approche ne permet pas au programme CSP de répondre aux autres exigences de sécurité et d’intégration requises par le propriétaire de la mission.</span><span class="sxs-lookup"><span data-stu-id="9f744-115">However, this approach does not alleviate the CSP from meeting other security and integration requirements as required by the Mission Owner.</span></span> <span data-ttu-id="9f744-116">Conformément à la [section SRG 5.2.2.1](https://dl.dod.cyber.mil/wp-content/uploads/cloud/SRG/index.html#5.2LegalConsiderations) IL2 Location *and Separation Requirements,* DoD IL2 PA est correctement couvert par une pa modéré FedRAMP de telle manière que les exigences ne seront pas évaluées en plus pour une pa IL2.</span><span class="sxs-lookup"><span data-stu-id="9f744-116">According to [SRG Section 5.2.2.1](https://dl.dod.cyber.mil/wp-content/uploads/cloud/SRG/index.html#5.2LegalConsiderations) *IL2 Location and Separation Requirements*, DoD IL2 PA is adequately covered by a FedRAMP Moderate PA such that the requirements will not be additionally assessed for an IL2 PA.</span></span>

## <a name="microsoft-in-scope-cloud-platforms--services"></a><span data-ttu-id="9f744-117">Plateformes cloud microsoft dans l’étendue & services</span><span class="sxs-lookup"><span data-stu-id="9f744-117">Microsoft in-scope cloud platforms & services</span></span>

- <span data-ttu-id="9f744-118">Azure</span><span class="sxs-lookup"><span data-stu-id="9f744-118">Azure</span></span>
- <span data-ttu-id="9f744-119">Dynamics 365</span><span class="sxs-lookup"><span data-stu-id="9f744-119">Dynamics 365</span></span>
- <span data-ttu-id="9f744-120">Microsoft Cloud App Security</span><span class="sxs-lookup"><span data-stu-id="9f744-120">Microsoft Cloud App Security</span></span>
- <span data-ttu-id="9f744-121">Microsoft Defender pour point de terminaison</span><span class="sxs-lookup"><span data-stu-id="9f744-121">Microsoft Defender for Endpoint</span></span>
- <span data-ttu-id="9f744-122">Microsoft Graph</span><span class="sxs-lookup"><span data-stu-id="9f744-122">Microsoft Graph</span></span>
- <span data-ttu-id="9f744-123">Microsoft Intune</span><span class="sxs-lookup"><span data-stu-id="9f744-123">Microsoft Intune</span></span>
- <span data-ttu-id="9f744-124">Microsoft Stream</span><span class="sxs-lookup"><span data-stu-id="9f744-124">Microsoft Stream</span></span>
- <span data-ttu-id="9f744-125">Office 365 Gouvernement américain, Office 365 pour le gouvernement américain - Élevé</span><span class="sxs-lookup"><span data-stu-id="9f744-125">Office 365 U.S. Government, Office 365 U.S. Government - High</span></span>
- <span data-ttu-id="9f744-126">Power Apps</span><span class="sxs-lookup"><span data-stu-id="9f744-126">Power Apps</span></span>
- <span data-ttu-id="9f744-127">Power Automate</span><span class="sxs-lookup"><span data-stu-id="9f744-127">Power Automate</span></span>
- <span data-ttu-id="9f744-128">Power BI</span><span class="sxs-lookup"><span data-stu-id="9f744-128">Power BI</span></span>

## <a name="azure-dynamics-365-and-dod-il2"></a><span data-ttu-id="9f744-129">Azure, Dynamics 365 et DoD IL2</span><span class="sxs-lookup"><span data-stu-id="9f744-129">Azure, Dynamics 365, and DoD IL2</span></span>

<span data-ttu-id="9f744-130">Pour plus d’informations sur Azure, Dynamics 365 et d’autres services en ligne, voir l’offre [Azure DoD IL2.](/azure/compliance/offerings/offering-dod-il2)</span><span class="sxs-lookup"><span data-stu-id="9f744-130">For more information about Azure, Dynamics 365, and other online services compliance, see the [Azure DoD IL2 offering](/azure/compliance/offerings/offering-dod-il2).</span></span>

## <a name="office-365-and-dod-il2"></a><span data-ttu-id="9f744-131">Office 365 et DoD IL2</span><span class="sxs-lookup"><span data-stu-id="9f744-131">Office 365 and DoD IL2</span></span>

### <a name="office-365-cloud-environments"></a><span data-ttu-id="9f744-132">Office 365 cloud</span><span class="sxs-lookup"><span data-stu-id="9f744-132">Office 365 cloud environments</span></span>

[!INCLUDE [Office 365 offering intro](../includes/o365-offering-introduction.md)]

### <a name="office-365-applicability-and-in-scope-services"></a><span data-ttu-id="9f744-133">Office 365 applicabilité et services dans l’étendue</span><span class="sxs-lookup"><span data-stu-id="9f744-133">Office 365 applicability and in-scope services</span></span>

<span data-ttu-id="9f744-134">Utilisez le tableau suivant pour déterminer l’applicabilité de vos services Office 365 et de votre abonnement :</span><span class="sxs-lookup"><span data-stu-id="9f744-134">Use the following table to determine applicability for your Office 365 services and subscription:</span></span>

| <span data-ttu-id="9f744-135">**Applicabilité**</span><span class="sxs-lookup"><span data-stu-id="9f744-135">**Applicability**</span></span> | <span data-ttu-id="9f744-136">**Services dans l’étendue**</span><span class="sxs-lookup"><span data-stu-id="9f744-136">**In-scope services**</span></span> |
|:------------------|:----------------------|
| <span data-ttu-id="9f744-137">**GCC**</span><span class="sxs-lookup"><span data-stu-id="9f744-137">**GCC**</span></span> | <span data-ttu-id="9f744-138">Service Informations sur les activités, services Bing, Delve, Exchange Online Protection, Exchange Online, Services intelligents, Microsoft Teams, portail client Office 365, Office Online, infrastructure de service Office, rapports d’utilisation Office, OneDrive Entreprise, carte de visite, SharePoint Online, Skype Entreprise, Windows Ink</span><span class="sxs-lookup"><span data-stu-id="9f744-138">Activity Feed Service, Bing Services, Delve, Exchange Online Protection, Exchange Online, Intelligent Services, Microsoft Teams, Office 365 Customer Portal, Office Online, Office Service Infrastructure, Office Usage Reports, OneDrive for Business, People Card, SharePoint Online, Skype for Business, Windows Ink</span></span> |
| <span data-ttu-id="9f744-139">**GCC High**</span><span class="sxs-lookup"><span data-stu-id="9f744-139">**GCC High**</span></span> | <span data-ttu-id="9f744-140">Service Informations sur les activités, services Bing, Delve, Exchange Online Protection, Exchange Online, Services intelligents, Microsoft Teams, portail client Office 365, Office Online, infrastructure de service Office, rapports d’utilisation Office, OneDrive Entreprise, carte de visite, SharePoint Online, Skype Entreprise, Windows Ink</span><span class="sxs-lookup"><span data-stu-id="9f744-140">Activity Feed Service, Bing Services, Delve, Exchange Online Protection, Exchange Online, Intelligent Services, Microsoft Teams, Office 365 Customer Portal, Office Online, Office Service Infrastructure, Office Usage Reports, OneDrive for Business, People Card, SharePoint Online, Skype for Business, Windows Ink</span></span> |

### <a name="resources"></a><span data-ttu-id="9f744-141">Ressources</span><span class="sxs-lookup"><span data-stu-id="9f744-141">Resources</span></span>

- [<span data-ttu-id="9f744-142">Solutions microsoft pour le gouvernement</span><span class="sxs-lookup"><span data-stu-id="9f744-142">Microsoft government solutions</span></span>](https://www.microsoft.com/enterprise/government)
- [<span data-ttu-id="9f744-143">Guide des conditions requises pour la sécurité dans le Cloud Computing DoD</span><span class="sxs-lookup"><span data-stu-id="9f744-143">DoD Cloud Computing Security Requirements Guide</span></span>](https://dl.dod.cyber.mil/wp-content/uploads/cloud/SRG/index.html)
- [<span data-ttu-id="9f744-144">Documents FedRAMP</span><span class="sxs-lookup"><span data-stu-id="9f744-144">FedRAMP documents</span></span>](https://www.fedramp.gov/documents/)
- <span data-ttu-id="9f744-145">[NIST SP 800-37](https://csrc.nist.gov/publications/detail/sp/800-37/rev-2/final) *Risk Management Framework for Information Systems and Organizations: A System Life-Cycle Approach for Security and Privacy*</span><span class="sxs-lookup"><span data-stu-id="9f744-145">[NIST SP 800-37](https://csrc.nist.gov/publications/detail/sp/800-37/rev-2/final) *Risk Management Framework for Information Systems and Organizations: A System Life-Cycle Approach for Security and Privacy*</span></span>
- <span data-ttu-id="9f744-146">Contrôles de sécurité et de confidentialité [NIST SP 800-53](https://csrc.nist.gov/Projects/risk-management/sp800-53-controls/release-search#!/800-53) *pour les systèmes d’information et les organisations*</span><span class="sxs-lookup"><span data-stu-id="9f744-146">[NIST SP 800-53](https://csrc.nist.gov/Projects/risk-management/sp800-53-controls/release-search#!/800-53) *Security and Privacy Controls for Information Systems and Organizations*</span></span>
- <span data-ttu-id="9f744-147">[Instruction DoD 8510.01](https://www.esd.whs.mil/Portals/54/Documents/DD/issuances/dodi/851001p.pdf) *DoD Risk Management Framework (RMF) pour* les technologies de l’information DoD</span><span class="sxs-lookup"><span data-stu-id="9f744-147">[DoD Instruction 8510.01](https://www.esd.whs.mil/Portals/54/Documents/DD/issuances/dodi/851001p.pdf) *DoD Risk Management Framework (RMF) for DoD Information Technology (IT)*</span></span>
