---
title: Microsoft 365 journalisation interne pour Microsoft 365'ingénierie
description: Dans cet article, trouvez une explication du fonctionnement de la journalisation interne Microsoft 365'équipes d’ingénierie.
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
ms.openlocfilehash: 71b08509ae920ad88ecfa1566b9a11d640b0534f
ms.sourcegitcommit: fb379d1110a9a86c7f9bab8c484dc3f4b3dfd6f0
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 06/23/2021
ms.locfileid: "53088593"
---
# <a name="internal-logging-for-microsoft-365-engineering"></a><span data-ttu-id="22ff8-103">Journalisation interne pour Microsoft 365 Engineering</span><span class="sxs-lookup"><span data-stu-id="22ff8-103">Internal logging for Microsoft 365 engineering</span></span>

<span data-ttu-id="22ff8-104">En plus des événements et des données de journal disponibles pour les clients, Microsoft maintient un système interne de collecte de données de journal qui est disponible pour Microsoft 365 ingénieurs.</span><span class="sxs-lookup"><span data-stu-id="22ff8-104">In addition to the events and log data available for customers, Microsoft maintains an internal log data collection system that is available to Microsoft 365 engineers.</span></span> <span data-ttu-id="22ff8-105">De nombreux types différents de données de journal sont téléchargés à partir de serveurs Microsoft 365 vers une solution de surveillance de la sécurité propriétaire pour l’analyse en temps quasi réel (NRT) et un service interne de big data computing (Cosmos) pour le stockage à long terme.</span><span class="sxs-lookup"><span data-stu-id="22ff8-105">Many different types of log data are uploaded from Microsoft 365 servers to a proprietary security monitoring solution for near real-time (NRT) analysis and an internal, big data computing service (Cosmos) for long-term storage.</span></span> <span data-ttu-id="22ff8-106">Ce transfert de données se produit via une connexion TLS validée PAR LA FIPS 140-2 sur des ports et protocoles approuvés à l’aide d’un outil d’automatisation propriétaire appelé odl Office Data Loader( ODL).</span><span class="sxs-lookup"><span data-stu-id="22ff8-106">This data transfer occurs over a FIPS 140-2-validated TLS connection on approved ports and protocols using a proprietary automation tool called the Office Data Loader (ODL).</span></span> <span data-ttu-id="22ff8-107">Les outils utilisés dans Microsoft 365 pour collecter et traiter les enregistrements d’audit n’autorisent pas les modifications définitives ou irréversibles apportées au contenu ou à l’ordre des enregistrements d’audit d’origine.</span><span class="sxs-lookup"><span data-stu-id="22ff8-107">The tools used in Microsoft 365 to collect and process audit records do not allow permanent or irreversible changes to the original audit record content or time ordering.</span></span>

<span data-ttu-id="22ff8-108">Les équipes de service utilisent Cosmos comme référentiel centralisé pour effectuer une analyse de l’utilisation des applications, pour mesurer les performances système et opérationnelles, et pour rechercher des anomalies et des modèles qui peuvent indiquer des problèmes ou des problèmes de sécurité.</span><span class="sxs-lookup"><span data-stu-id="22ff8-108">Service teams use Cosmos as a centralized repository to conduct an analysis of application usage, to measure system and operational performance, and to look for abnormalities and patterns that may indicate problems or security issues.</span></span> <span data-ttu-id="22ff8-109">Chaque équipe de service charge une ligne de base qui inclut :</span><span class="sxs-lookup"><span data-stu-id="22ff8-109">Each service team uploads a baseline that includes:</span></span>

- <span data-ttu-id="22ff8-110">Journaux d’événements</span><span class="sxs-lookup"><span data-stu-id="22ff8-110">Event logs</span></span>
- <span data-ttu-id="22ff8-111">Journaux AppLocker</span><span class="sxs-lookup"><span data-stu-id="22ff8-111">AppLocker logs</span></span>
- <span data-ttu-id="22ff8-112">Données de performances</span><span class="sxs-lookup"><span data-stu-id="22ff8-112">Performance data</span></span>
- <span data-ttu-id="22ff8-113">System Center données</span><span class="sxs-lookup"><span data-stu-id="22ff8-113">System Center data</span></span>
- <span data-ttu-id="22ff8-114">Enregistrements des détails des appels</span><span class="sxs-lookup"><span data-stu-id="22ff8-114">Call detail records</span></span>
- <span data-ttu-id="22ff8-115">Données de qualité de l’expérience</span><span class="sxs-lookup"><span data-stu-id="22ff8-115">Quality of experience data</span></span>
- <span data-ttu-id="22ff8-116">Journaux du serveur web IIS</span><span class="sxs-lookup"><span data-stu-id="22ff8-116">IIS Web Server logs</span></span>
- <span data-ttu-id="22ff8-117">SQL Server journaux</span><span class="sxs-lookup"><span data-stu-id="22ff8-117">SQL Server logs</span></span>
- <span data-ttu-id="22ff8-118">Données Syslog</span><span class="sxs-lookup"><span data-stu-id="22ff8-118">Syslog data</span></span>
- <span data-ttu-id="22ff8-119">Journaux d’audit de sécurité</span><span class="sxs-lookup"><span data-stu-id="22ff8-119">Security audit logs</span></span>

<span data-ttu-id="22ff8-120">Avant le chargement, l’application ODL utilise un service de nettoyage pour supprimer les champs qui contiennent des données client, telles que les informations client et les informations d’identification de l’utilisateur final, et remplacer ces champs par une valeur de hachage.</span><span class="sxs-lookup"><span data-stu-id="22ff8-120">Prior to uploading, the ODL application uses a scrubbing service to remove any fields that contain customer data, such as tenant information and end-user identifiable information, and replace those fields with a hash value.</span></span> <span data-ttu-id="22ff8-121">Les journaux nettoyés sont téléchargés vers Cosmos et vers la solution de surveillance de la sécurité NRT qui analyse les journaux pour les événements de sécurité potentiels et les indicateurs de performances.</span><span class="sxs-lookup"><span data-stu-id="22ff8-121">The scrubbed logs are uploaded to Cosmos and to the NRT security monitoring solution that analyzes the logs for potential security events and performance indicators.</span></span> <span data-ttu-id="22ff8-122">La période de rétention des données du journal d’audit dans Cosmos est déterminée par les équipes de service ; la plupart des données du journal d’audit sont conservées pendant 90 jours ou plus pour prendre en charge les enquêtes sur les incidents de sécurité et pour répondre aux exigences de rétention réglementaires.</span><span class="sxs-lookup"><span data-stu-id="22ff8-122">The period of audit log data retention in Cosmos is determined by the service teams; most audit log data is retained for 90 days or longer to support security incident investigations and to meet regulatory retention requirements.</span></span>

<span data-ttu-id="22ff8-123">L’accès Microsoft 365 données stockées dans Cosmos est limité au personnel autorisé.</span><span class="sxs-lookup"><span data-stu-id="22ff8-123">Access to Microsoft 365 data stored in Cosmos is restricted to authorized personnel.</span></span> <span data-ttu-id="22ff8-124">Microsoft limite la gestion des journaux d’audit à un sous-ensemble limité de membres de l’équipe de sécurité responsables des fonctionnalités d’audit.</span><span class="sxs-lookup"><span data-stu-id="22ff8-124">Microsoft restricts the management of audit logs to a limited subset of Security Team members responsible for audit functionality.</span></span> <span data-ttu-id="22ff8-125">L’équipe de sécurité n’a pas d’accès administratif permanent aux Cosmos, et toutes les modifications sont enregistrées et auditées.</span><span class="sxs-lookup"><span data-stu-id="22ff8-125">The Security Team does not have standing administrative access to Cosmos, and all changes are recorded and audited.</span></span>

<span data-ttu-id="22ff8-126">Après l’analyse NRT, chaque équipe de service peut utiliser des outils d’analyse et des tableaux de bord pour la corrélation de données, les requêtes interactives et l’analyse des données.</span><span class="sxs-lookup"><span data-stu-id="22ff8-126">After NRT analysis, each service team can use analysis tools and dashboards for data correlation, interactive queries, and data analytics.</span></span> <span data-ttu-id="22ff8-127">Ces rapports sont utilisés pour surveiller et améliorer les performances globales du service.</span><span class="sxs-lookup"><span data-stu-id="22ff8-127">These reports are used to monitor and improve the overall performance of the service.</span></span>
