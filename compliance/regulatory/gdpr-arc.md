---
title: Listes de vérification de préparation sur la responsabilité concernant le RGPD
description: Dans cet articles, vous allez découvrir les listes de vérification de préparation sur la responsabilité pour accéder aux informations permettant de prendre en charge le RGPD lorsque vous utilisez les produits et services Microsoft.
keywords: Microsoft 365, Microsoft 365 Éducation, documentation Microsoft 365, RGPD
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
- GDPR
- M365-security-compliance
- MS-Compliance
ms.custom:
- seo-marvel-mar2020
titleSuffix: Microsoft GDPR
hideEdit: true
ms.openlocfilehash: f6b0582215242dd1de187b4cd0386e44b144dba8
ms.sourcegitcommit: 024137a15ab23d26cac5ec14c36f3577fd8a0cc4
ms.translationtype: HT
ms.contentlocale: fr-FR
ms.lasthandoff: 04/01/2021
ms.locfileid: "51496477"
---
# <a name="support-your-gdpr-program-with-accountability-readiness-checklists"></a>Prise en charge de votre programme RGPD avec des listes de vérification de préparation sur la responsabilité

Le règlement général sur la protection des données (RGPD) présente de nouvelles règles pour les organisations qui offrent des produits et des services aux membres de l’Union européenne (UE), ou qui collectent et analysent des données pour les résidents de l’UE quel que soit l’endroit où vous vous trouvez et celui où se trouve votre entreprise. Pour plus de détails, consultez la [rubrique Synthèse RGPD](gdpr.md).

## <a name="accountability-readiness-checklists"></a>Listes de vérification de préparation sur la responsabilité

Les listes de vérification de préparation sur la responsabilité permettent d’accéder en toute simplicité aux informations dont vous pouvez avoir besoin pour prendre en charge le RGPD lorsque vous utilisez les produits et services Microsoft. Cette liste de vérification répertorie les obligations potentielles que vous pouvez rencontrer dans le cadre du RGPD et vous oriente vers les informations nécessaires à la mise en conformité de votre organisation.

Il existe un guide spécifique pour quatre familles de produits et services Microsoft :

- [Office 365](gdpr-arc-Office365.md)
- [Dynamics 365](gdpr-arc-azure-dynamics.md)
- [Azure](gdpr-arc-azure-dynamics.md)
- [Support Microsoft et services professionnels](gdpr-arc-prof-services.md)

Vous pouvez gérer les éléments de cette liste de vérification à l’aide du [Gestionnaire de conformité](/microsoft-365/compliance/compliance-manager) en indiquant l’ID de contrôle et le titre de contrôle sous Contrôles gérés par le client dans la vignette RGPD.

Ces listes de vérification comprennent les quatre catégories de considérations de base pour un programme de confidentialité compatible avec le RGPD répertoriées ci-dessous, ainsi que des exemples de configuration.

1. Conditions de collecte et de traitement des données :

    - Quand est-ce que le consentement est obtenu ?  
    - Identifier et documenter l’objectif  
    - Analyse d’impact sur la confidentialité

2. Droits des personnes concernées par les données  

    - Déterminer les informations des propriétaires des données personnelles (personnes concernées par le traitement des données)  
    - Fournir un processus pour modifier ou retirer son consentement

3. Confidentialité liée à la conception et par défaut  

    - Limiter la collecte  
    - Respecter les niveaux d’identification  
    - Fichiers temporaires

4. Protection et sécurité des données  

    - Compréhension de l’organisation et de son contexte  
    - Planification  
    - Stratégies de sécurité des informations

## <a name="customer-agreements"></a>Contrats client

- **Conditions d’utilisation du service en ligne** :.les engagements contractuels de Microsoft en ce qui concerne le RGPD sont accessibles dans les [Conditions d’utilisation des services en ligne](https://go.microsoft.com/fwlink/p/?linkid=2052208).
- **Conditions d’utilisation des produits Microsoft Terms** : Microsoft étend les [engagements des conditions d’utilisation du RGPD](https://go.microsoft.com/fwlink/p/?linkid=2052213) à tous les clients de licences en volume.
- **Addendum à la protection des données** : les services Microsoft [s’étendent les engagements](https://go.microsoft.com/fwlink/p/?linkid=2052215) aux clients et autres utilisateurs de Microsoft Consulting Services.

## <a name="gdpr-compliance-controls"></a>Contrôles de conformité RGPD

- **Utiliser le Gestionnaire de conformité**: révisez et incorporez les contrôles utilisés par Microsoft pour prendre en charge les obligations dans le RGPD avec le [Gestionnaire de conformité](/microsoft-365/compliance/compliance-manager).
- **Mappage de contrôle du RGPD**: accédez à un [Mappage complet](https://go.microsoft.com/fwlink/p/?linkid=2052220) de contrôles Microsoft aux obligations RGPD.

## <a name="records-of-processing-for-processors"></a>Enregistrements de Traitement pour les Processeurs

En raison de l’échelle et de l’ampleur des services en ligne que nous fournissons à nos clients de contrôle, nous attendons que les clients identifient les services dont ils cherchent les enregistrements de traitement et récupèrent les journaux pertinents dans les outils en ligne que nous fournissons. Par exemple, pour les enregistrements de traitement pour Azure dans lesquels les clients seraient invités à identifier les types d’activité de traitement dont ils recherchent les enregistrements.

### <a name="azure-logs"></a>Journaux Azure

En règle générale, les clients seraient intéressés par les journaux d’Activité et potentiellement les journaux de Diagnostics:

- **Journaux d’activité**: [Journaux d’activité](/azure/azure-monitor/platform/platform-logs-overview) fournissent un aperçu des opérations effectuées sur les ressources d’un abonnement. Les journaux d’activité peuvent aider à déterminer l’initiateur, l’heure et le statut de l’opération.
- **Journaux de diagnostic**: [Journaux de diagnostic](/azure/azure-monitor/platform/platform-logs-overview) sont tous les journaux émis par chaque ressource. Ces journaux comprennent les journaux du système d’événements Windows, les journaux de stockage Azure, les journaux d’audit Key Vault, et les journaux d’accès et de pare-feu Application Gateway.
- **Archivage de Journaux**: Tous les journaux de diagnostics écrivent à un compte de stockage Azure centralisé et chiffré pour l’archivage. La rétention peut être configurée par l’utilisateur, jusqu’à 730 jours, afin de répondre aux exigences de rétention propres à l’organisation. Ces journaux se connectent aux journaux du Moniteur Azure pour le traitement, le stockage et les données de tableaux de bord.

### <a name="other-logs"></a>D’autres journaux

De plus, les solutions de surveillance suivantes sont installées en tant que composantes de cette architecture. Il incombe au client de configurer ces solutions pour qu’elles s’alignent sur les contrôles de sécurité FedRAMP:

- [Evaluation Azure Directory](/azure/azure-monitor/insights/ad-assessment): La solution de Vérification Azure Directory évalue le risque et l’intégrité des environnements serveur on à intervalles réguliers et fournit une liste de recommandations hiérarchisées propres à l’infrastructure serveur déployée.
- [Evaluation contre les Programmes Malveillants](/azure/security-center/security-center-services?tabs=features-windows#supported-endpoint-protection-solutions-): la solution anti-programme malveillant signale les programmes malveillants, les menaces et l’état de protection.
- [Automatisation Azure](/azure/automation/automation-hybrid-runbook-worker): La solution d’Automatisation Azure stocke, exécute et gère les runbooks.
- [Sécurité et Audit](/azure/security-center/security-center-introduction): Le tableau de bord Sécurité et Audit fournit une vue d’ensemble élevée de l’état de la sécurité des ressources en fournissant des mesures sur les domaines de sécurité, les problèmes notables, les détections, les menaces et les requêtes de sécurité courantes.
- [ Evaluation SQL](/azure/azure-monitor/insights/sql-assessment): La solution de Vérification de l’Intégrité de SQL évalue le risque et l’état d’intégrité des environnements serveur à intervalles réguliers, et fournit une liste hiérarchisée de recommandations propres à l’infrastructure serveur déployée.
- [Gestion des mises à jour](/azure/automation/update-management/update-mgmt-overview): La solution de Gestion des Mises à jour permet aux clients de gérer les mises à jour de sécurité du système d’exploitation, notamment l’état des mises à jour disponibles et le processus d’installation des mises à jour requises.
- [Intégrité de l’Agent](/azure/azure-monitor/insights/solution-agenthealth): La solution d’Intégrité des Agents indique le nombre d’agents déployés et leur distribution géographique, ainsi que le nombre d’agents qui ne répondent pas et le nombre d’agents qui envoient des données opérationnelles.
- [Journaux d’Activité Azure](/azure/azure-monitor/platform/activity-log): La solution d’Analyse des Journaux d’Activité aide à analyser les journaux d’activité Azure sur tous les abonnements Azure pour un client.
- [Suivi des Modifications](/azure/azure-monitor/platform/activity-log): La solution Suivi des Modifications permet aux clients d’identifier facilement les modifications apportées à l’environnement.

Pour plus d’informations sur les mesures techniques et de sécurité pour Azure, les clients de contrôle doivent consulter la [Documentation de Sécurité Azure](/azure/security/). Dans la mesure où Microsoft ne sait pas si les Données Client sont des Données Personnelles ou non, Azure traite toutes les Données Client comme s’il s’agissait de Données Personnelles, de telle sorte qu’un client envisagerait tout le matériel pertinent.

### <a name="processor-information"></a>Informations sur le processeur

Un autre produit dont le client pourrait avoir besoin des enregistrements des informations de traitement pour les processeurs est Office 365. Pour afficher les informations relatives à Office 365, voir l’article[Rechercher le journal d’audit dans le Centre de Sécurité et Conformité](/microsoft-365/compliance/search-the-audit-log-in-security-and-compliance) article.

Vous pouvez également consulter les informations sur Dynamics 365 à l’aide du centre de Sécurité et Conformité.  Pour afficher la page Centre de Sécurité et Conformité, assurez-vous que vous disposez de la licence appropriée. En savoir plus sur les licences avec l’article [Description du service Centre de Sécurité et Conformité](/office365/servicedescriptions/office-365-platform-service-description/office-365-securitycompliance-center). Pour rechercher les événements Dynamics 365, visitez le Journal d'Audit Unifié dans le [centre de Sécurité et Conformité](https://protection.office.com/unifiedauditlog).

### <a name="professional-services-information"></a>Informations des services professionnels

En ce qui concerne les services professionnels, les données de support des services professionnels sont fournies par le client à l’ingénieur du support par le représentant du client.  Cela peut se produire lorsqu’un client envoie une Demande de Service via le portail de produit en ligne, le Hub Services ou par téléphone.

Les informations sont stockées dans nos systèmes CRM et utilisées uniquement aux fins suivantes:

- Offrir des services professionnels, notamment un support technique, une planification professionnelle, des conseils, des instructions, la migration de données, le déploiement et les services de développement de solutions/logiciels.  
- Résolution des problèmes (prévention, détection, examen, atténuation et réparation des problèmes, notamment les incidents de sécurité); et 
- Une amélioration continue (la gestion des services professionnels, notamment l’installation des dernières mises à jour et l’amélioration de la fiabilité, de l’efficacité, de la qualité et de la sécurité). 

En raison de l’échelle de nos opérations de support, Microsoft utilise le système CRM basé sur un groupe de produits. Les enregistrements du traitement sont contenus dans ces systèmes.
Un historique du traitement est reflété dans les enregistrements gérés dans nos systèmes CRM.  Dans la plupart des cas, l’Historique des Demandes de Service est disponible sur les portails ou le Hub de service.
Pour consulter toutes les informations spécifiques qui ne sont pas disponibles sur les portails ou toute autre demande de renseignement sur le traitement de vos données, contactez votre Gestionnaire de Compte Technique ou contactez [Support Technique Microsoft](https://support.microsoft.com/contactus/).

## <a name="learn-more"></a>En savoir plus

- [Centre de gestion de la confidentialité Microsoft](https://www.microsoft.com/trust-center/privacy/gdpr-overview)
