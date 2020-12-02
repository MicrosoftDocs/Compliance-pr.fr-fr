---
title: ISO/IEC 27017:2015 Code de pratique international des contrôles de sécurité des informations
description: Les services Cloud Microsoft ont mis en œuvre ce code de pratique pour les contrôles de sécurité des informations.
keywords: Offres pour la conformité Microsoft 365
localization_priority: Priority
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
ms.openlocfilehash: b51d7879b0b20773f76ed194a0080b2ae88c1fb8
ms.sourcegitcommit: 626b0076d133e588cd28598c149a7f272fc18bae
ms.translationtype: HT
ms.contentlocale: fr-FR
ms.lasthandoff: 11/30/2020
ms.locfileid: "49507597"
---
# <a name="isoiec-270172015-code-of-practice-for-information-security-controls"></a><span data-ttu-id="dbad5-104">ISO/IEC 27017:2015 Code de pratique international des contrôles de sécurité des informations</span><span class="sxs-lookup"><span data-stu-id="dbad5-104">ISO/IEC 27017:2015 Code of Practice for Information Security Controls</span></span>

## <a name="iso-iec-27017-overview"></a><span data-ttu-id="dbad5-105">Présentation de la norme ISO-IEC 27017</span><span class="sxs-lookup"><span data-stu-id="dbad5-105">ISO-IEC 27017 Overview</span></span>

<span data-ttu-id="dbad5-p101">Le code de conduite ISO/IEC 27017:2015 est conçu comme une référence permettant aux entreprises de sélectionner les contrôles de sécurité des informations des services cloud lors de la mise en œuvre d’un système de gestion de la sécurité des informations de cloud computing basé sur la norme ISO/IEC 27002:2013. Il peut également être utilisé par les fournisseurs de services cloud en tant que document guide pour l’implémentation de contrôles de protection couramment admis.</span><span class="sxs-lookup"><span data-stu-id="dbad5-p101">The ISO/IEC 27017:2015 code of practice is designed for organizations to use as a reference for selecting cloud services information security controls when implementing a cloud computing information security management system based on ISO/IEC 27002:2013. It can also be used by cloud service providers as a guidance document for implementing commonly accepted protection controls.</span></span>

<span data-ttu-id="dbad5-p102">Cette norme internationale fournit des conseils d'implémentation supplémentaires spécifiques au cloud basés sur la norme ISO/IEC 27002 et fournit d’autres contrôles pour traiter les menaces et les risques de sécurité des informations spécifiques au cloud conformément aux clauses 5-18 de la norme ISO/IEC 27002: 2013 pour les contrôles, les conseils d'implémentation, ainsi que d'autres informations. Plus précisément, cette norme fournit des conseils sur les 37 contrôles de la norme ISO/IEC 27002 et contient également 7 nouveaux contrôles non dupliqués dans la norme ISO/IEC 27002. Ces nouveaux contrôles portent sur les aspects importants suivants :</span><span class="sxs-lookup"><span data-stu-id="dbad5-p102">This international standard provides additional cloud-specific implementation guidance based on ISO/IEC 27002, and provides additional controls to address cloud-specific information security threats and risks referring to clauses 5-18 in ISO/IEC 27002: 2013 for controls, implementation guidance, and other information. Specifically, this standard provides guidance on 37 controls in ISO/IEC 27002, and it also features seven new controls that are not duplicated in ISO/IEC 27002. These new controls address the following important areas:</span></span>

- <span data-ttu-id="dbad5-111">Rôles et responsabilités partagés dans un environnement de cloud computing</span><span class="sxs-lookup"><span data-stu-id="dbad5-111">Shared roles and responsibilities within a cloud computing environment</span></span>
- <span data-ttu-id="dbad5-112">Retrait et restitution des biens des clients des services cloud à la fin du contrat</span><span class="sxs-lookup"><span data-stu-id="dbad5-112">Removal and return of cloud service customer assets upon contract termination</span></span>
- <span data-ttu-id="dbad5-113">Protection et séparation de l’environnement virtuel d'un client de celui des autres clients</span><span class="sxs-lookup"><span data-stu-id="dbad5-113">Protection and separation of a customer's virtual environment from environments of other customers</span></span>
- <span data-ttu-id="dbad5-114">Durcissement des exigences des machines virtuelles pour répondre aux besoins des entreprises</span><span class="sxs-lookup"><span data-stu-id="dbad5-114">Virtual machine hardening requirements to meet business needs</span></span>
- <span data-ttu-id="dbad5-115">Procédures pour les opérations administratives d'un environnement de cloud computing</span><span class="sxs-lookup"><span data-stu-id="dbad5-115">Procedures for administrative operations of a cloud computing environment</span></span>
- <span data-ttu-id="dbad5-116">Possibilité donnée aux clients de surveiller les activités pertinentes dans un environnement de cloud computing</span><span class="sxs-lookup"><span data-stu-id="dbad5-116">Enabling customers to monitor relevant activities within a cloud computing environment</span></span>
- <span data-ttu-id="dbad5-117">Alignement de la gestion de la sécurité pour les réseaux virtuels et physiques</span><span class="sxs-lookup"><span data-stu-id="dbad5-117">Alignment of security management for virtual and physical networks</span></span>

## <a name="microsoft-and-isoiec-27017"></a><span data-ttu-id="dbad5-118">Microsoft et la norme ISO/IEC 27017</span><span class="sxs-lookup"><span data-stu-id="dbad5-118">Microsoft and ISO/IEC 27017</span></span>

<span data-ttu-id="dbad5-p103">La norme ISO/IEC 27017 est la seule à fournir des conseils à la fois aux fournisseurs de services cloud et aux clients des services cloud. Elle fournit également aux clients de services cloud des informatiques pratiques sur ce à quoi ils doivent s'attendre de la part des fournisseurs de services cloud. Les clients peuvent directement tirer parti de la norme ISO/IEC 27017 en s’assurant qu’ils ont bien compris les responsabilités partagées dans le cloud.</span><span class="sxs-lookup"><span data-stu-id="dbad5-p103">ISO/IEC 27017 is unique in providing guidance for both cloud service providers and cloud service customers. It also provides cloud service customers with practical information on what they should expect from cloud service providers. Customers can benefit directly from ISO/IEC 27017 by ensuring they understand the shared responsibilities in the cloud.</span></span>

## <a name="microsoft-in-scope-cloud-services"></a><span data-ttu-id="dbad5-122">Services Cloud Microsoft concernés</span><span class="sxs-lookup"><span data-stu-id="dbad5-122">Microsoft in-scope cloud services</span></span>

- [<span data-ttu-id="dbad5-123">Azure, Azure Gouvernement et Azure Allemagne</span><span class="sxs-lookup"><span data-stu-id="dbad5-123">Azure, Azure Government, and Azure Germany</span></span>](https://aka.ms/AzureCompliance)
- <span data-ttu-id="dbad5-124">Microsoft Cloud App Security</span><span class="sxs-lookup"><span data-stu-id="dbad5-124">Microsoft Cloud App Security</span></span>
- [<span data-ttu-id="dbad5-125">Dynamics 365, Dynamics 365 et Dynamics 365 Allemagne</span><span class="sxs-lookup"><span data-stu-id="dbad5-125">Dynamics 365, Dynamics 365, and Dynamics 365 Germany</span></span>](https://aka.ms/d365-compliance-list)
- <span data-ttu-id="dbad5-126">Microsoft Defender – Protection avancée contre les menaces</span><span class="sxs-lookup"><span data-stu-id="dbad5-126">Microsoft Defender Advanced Threat Protection</span></span>
- <span data-ttu-id="dbad5-127">Microsoft Graph</span><span class="sxs-lookup"><span data-stu-id="dbad5-127">Microsoft Graph</span></span>
- <span data-ttu-id="dbad5-128">Microsoft Healthcare Bot</span><span class="sxs-lookup"><span data-stu-id="dbad5-128">Microsoft Healthcare Bot</span></span>
- <span data-ttu-id="dbad5-129">Intune</span><span class="sxs-lookup"><span data-stu-id="dbad5-129">Intune</span></span>
- <span data-ttu-id="dbad5-130">Bureau géré Microsoft</span><span class="sxs-lookup"><span data-stu-id="dbad5-130">Microsoft Managed Desktop</span></span>
- <span data-ttu-id="dbad5-131">Service Cloud Power Automate (anciennement Microsoft Flow), soit en service autonome, soit inclus dans un plan ou une suite Office 365 ou Dynamics 365</span><span class="sxs-lookup"><span data-stu-id="dbad5-131">Power Automate (formerly Microsoft Flow) cloud service either as a standalone service or as included in an Office 365 or Dynamics 365 branded plan or suite</span></span>
- <span data-ttu-id="dbad5-132">Office 365, Office 365 U.S. Government, Office 365 U.S. Government Defense et Office 365 Allemagne</span><span class="sxs-lookup"><span data-stu-id="dbad5-132">Office 365, Office 365 U.S. Government, Office 365 U.S. Government Defense, and Office 365 Germany</span></span>
- <span data-ttu-id="dbad5-133">Service Cloud Microsoft PowerApps, soit en service autonome, soit inclus dans un plan ou une suite Office 365 ou Dynamics 365</span><span class="sxs-lookup"><span data-stu-id="dbad5-133">PowerApps cloud service either as a standalone service or as included in an Office 365 or Dynamics 365 branded plan or suite</span></span>
- <span data-ttu-id="dbad5-134">Service Cloud Power BI soit en service autonome, soit inclus dans un plan ou une suite Office 365</span><span class="sxs-lookup"><span data-stu-id="dbad5-134">Power BI cloud service either as a standalone service or as included in an Office 365 branded plan or suite</span></span>
- <span data-ttu-id="dbad5-135">Power BI intégré</span><span class="sxs-lookup"><span data-stu-id="dbad5-135">Power BI Embedded</span></span>
- <span data-ttu-id="dbad5-136">Microsoft Stream</span><span class="sxs-lookup"><span data-stu-id="dbad5-136">Microsoft Stream</span></span>
- <span data-ttu-id="dbad5-137">Consultez une [liste détaillée](https://go.microsoft.com/fwlink/p/?linkid=2077751) des services couverts dans Office 365</span><span class="sxs-lookup"><span data-stu-id="dbad5-137">See a [detailed list](https://go.microsoft.com/fwlink/p/?linkid=2077751) of covered services in Office 365</span></span>

## <a name="audits-reports-and-certificates"></a><span data-ttu-id="dbad5-138">Audits, rapports et certificats</span><span class="sxs-lookup"><span data-stu-id="dbad5-138">Audits, reports, and certificates</span></span>

<span data-ttu-id="dbad5-139">Les services Cloud Microsoft font l’objet d’un audit une fois par an pour le code de pratique ISO/IEC 27017:2015 dans le cadre du processus de certification pour ISO/IEC 27001:2013.</span><span class="sxs-lookup"><span data-stu-id="dbad5-139">Microsoft cloud services are audited once a year for the ISO/IEC 27017:2015 code of practice as part of the certification process for ISO/IEC 27001:2013.</span></span>

- [<span data-ttu-id="dbad5-140">Certificat ISO 27017 Azure</span><span class="sxs-lookup"><span data-stu-id="dbad5-140">Azure ISO 27017 Certificate</span></span>](https://aka.ms/azureiso27017cert)
- [<span data-ttu-id="dbad5-141">Rapport d’évaluation d’Azure ISO 27017</span><span class="sxs-lookup"><span data-stu-id="dbad5-141">Azure ISO 27017 Assessment report</span></span>](https://aka.ms/azureiso27017report)
- [<span data-ttu-id="dbad5-142">Office 365 : rapport d’évaluation d’audit ISO 27001, 27018 et 27017</span><span class="sxs-lookup"><span data-stu-id="dbad5-142">Office 365: ISO 27001, 27018, and 27017 Audit Assessment Report</span></span>](https://aka.ms/o365isoreport)

## <a name="frequently-asked-questions"></a><span data-ttu-id="dbad5-143">Foire aux questions</span><span class="sxs-lookup"><span data-stu-id="dbad5-143">Frequently asked questions</span></span>

<span data-ttu-id="dbad5-144">À qui la norme s'applique-t-elle ?</span><span class="sxs-lookup"><span data-stu-id="dbad5-144">To whom does the standard apply?</span></span>

<span data-ttu-id="dbad5-p104">Ce code de pratique fournit des contrôles et des conseils de mise en œuvre aux fournisseurs de services Cloud et à leurs clients. Il est organisé dans un format similaire à celui de la norme ISO/IEC 27002:2013.</span><span class="sxs-lookup"><span data-stu-id="dbad5-p104">This code of practice provides controls and implementation guidance for both cloud service providers and cloud service customers. It is structured in a format similar to ISO/IEC 27002:2013.</span></span>

<span data-ttu-id="dbad5-147">**Où puis-je consulter les informations de conformité de Microsoft concernant la norme ISO/IEC 27017:2015?**</span><span class="sxs-lookup"><span data-stu-id="dbad5-147">**Where can I view Microsoft's compliance information for ISO/IEC 27017:2015?**</span></span>

<span data-ttu-id="dbad5-148">Vous pouvez télécharger le certificat [ISO/IEC 27017:2015](https://aka.ms/azureiso27017) pour Azure, Intune et Power BI.</span><span class="sxs-lookup"><span data-stu-id="dbad5-148">You can download the [ISO/IEC 27017:2015 certificate](https://aka.ms/azureiso27017) for Azure, Intune, and Power BI.</span></span>

<span data-ttu-id="dbad5-149">**Puis-je utiliser la conformité ISO/IEC 27017 des services Microsoft dans le processus de certification de mon entreprise?**</span><span class="sxs-lookup"><span data-stu-id="dbad5-149">**Can I use the ISO/IEC 27017 compliance of Microsoft services in my organization's certification process?**</span></span>

<span data-ttu-id="dbad5-p105">Oui. Si votre entreprise est à la recherche d’une certification pour des implémentations déployées sur des services cloud Entreprise Microsoft concernés, vous pouvez utiliser les certifications pertinentes de Microsoft dans votre évaluation de la conformité. Il vous incombe cependant d’engager un évaluateur pour mesurer votre mise en œuvre de la conformité ainsi que les contrôles et processus au sein de votre propre organisation.</span><span class="sxs-lookup"><span data-stu-id="dbad5-p105">Yes. If your business is seeking certification for implementations deployed on any Microsoft in-scope enterprise cloud services, you can use Microsoft's relevant certifications in your compliance assessment. However, you are responsible for engaging an assessor to evaluate your implementation for compliance, and for the controls and processes within your own organization.</span></span>

<span data-ttu-id="dbad5-153">**Comment puis-je me procurer des copies des rapports d’audit applicables ?**</span><span class="sxs-lookup"><span data-stu-id="dbad5-153">**How can I get copies of the applicable audit reports?**</span></span>

<span data-ttu-id="dbad5-p106">Le [Portail d'approbation de service](https://aka.ms/stphelp) fournit des rapports d'audit tiers indépendants, ainsi que toute autre documentation. Vous pouvez utiliser le portail pour télécharger et examiner cette documentation afin d’obtenir une aide concernant vos propres exigences réglementaires.</span><span class="sxs-lookup"><span data-stu-id="dbad5-p106">The [Service Trust Portal](https://aka.ms/stphelp) provides independent, third-party audit reports and other related documentation. You can use the portal to download and review this documentation for assistance with your own regulatory requirements.</span></span>

## <a name="use-microsoft-compliance-manager-to-assess-your-risk"></a><span data-ttu-id="dbad5-156">Utilisez le Gestionnaire de conformité Microsoft pour évaluer vos risques</span><span class="sxs-lookup"><span data-stu-id="dbad5-156">Use Microsoft Compliance Manager to assess your risk</span></span>

<span data-ttu-id="dbad5-p107">Le [Gestionnaire de conformité Microsoft](https://docs.microsoft.com/microsoft-365/compliance/compliance-manager) est une fonctionnalité du [Centre de conformité Microsoft 365](https://docs.microsoft.com/microsoft-365/compliance/microsoft-365-compliance-center) qui vous permet de comprendre l’état de conformité de votre organisation et de prendre des mesures pour réduire les risques. Le Gestionnaire de conformité propose un modèle premium pour créer une évaluation pour ce règlement. Recherchez le modèle dans la page des **modèles d’évaluation** dans le Gestionnaire de conformité. Découvrez comment [créer des évaluations dans le Gestionnaire de conformité](https://docs.microsoft.com/microsoft-365/compliance/compliance-manager-assessments).</span><span class="sxs-lookup"><span data-stu-id="dbad5-p107">[Microsoft Compliance Manager](https://docs.microsoft.com/microsoft-365/compliance/compliance-manager) is a feature in the [Microsoft 365 compliance center](https://docs.microsoft.com/microsoft-365/compliance/microsoft-365-compliance-center) to help you understand your organization's compliance posture and take actions to help reduce risks. Compliance Manager offers a premium template for building an assessment for this regulation. Find the template in the **assessment templates** page in Compliance Manager. Learn how to [build assessments in Compliance Manager](https://docs.microsoft.com/microsoft-365/compliance/compliance-manager-assessments).</span></span>

## <a name="resources"></a><span data-ttu-id="dbad5-161">Ressources</span><span class="sxs-lookup"><span data-stu-id="dbad5-161">Resources</span></span>

- [<span data-ttu-id="dbad5-162">Code de pratique ISO/IEC 27017:2015</span><span class="sxs-lookup"><span data-stu-id="dbad5-162">ISO/IEC 27017:2015 code of practice</span></span>](https://www.iso.org/iso/iso_catalogue/catalogue_tc/catalogue_detail.htm?csnumber=43757)
- [<span data-ttu-id="dbad5-163">Conditions de Microsoft Online Services</span><span class="sxs-lookup"><span data-stu-id="dbad5-163">Microsoft Online Services Terms</span></span>](https://aka.ms/Online-Services-Terms)
- [<span data-ttu-id="dbad5-164">Conformité sur le site Microsoft Trust Center</span><span class="sxs-lookup"><span data-stu-id="dbad5-164">Compliance on the Microsoft Trust Center</span></span>](https://www.microsoft.com/trust-center/compliance/compliance-overview)
