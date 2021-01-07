---
title: Notification de violation dans le cadre du RGPD
description: Protection de Microsoft vis-à-vis des violations de données personnelles, et réponse et notification de Microsoft en cas de violation.
keywords: Office 365, Microsoft 365, Microsoft 365 Éducation, documentation Microsoft 365, RGPD
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
titleSuffix: Microsoft GDPR
ms.openlocfilehash: 317a5bf64a5d10099b3fcf73190bb6e20ffc2999
ms.sourcegitcommit: 7864222909b7d8d0b1dbdbbdee66f5697dac7940
ms.translationtype: HT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/05/2021
ms.locfileid: "49757839"
---
# <a name="breach-notification-under-the-gdpr"></a>Notification de violation dans le cadre du RGPD

Conformément à son rôle de responsable du traitement des données, Office 365 veille à ce que nos clients puissent remplir leur rôle d’entité de contrôle des données en répondant aux obligations du RGPD concernant la notification des violations de données. À cet effet, nous nous engageons à effectuer les actions suivantes :

- Permettre aux clients la possibilité de spécifier un contact dédié à la protection des données personnelles qui sera informé en cas de violation de données.  Les clients peuvent spécifier ce contact à l’aide des paramètres de rôle de lecteur de Confidentialité pour le Centre de messages.
- Notifier les clients d’une violation de données personnelles dans les 72 heures qui suivent la violation. Les notifications seront publiées dans le Centre de messages qui est accessible via le Centre d’administration Microsoft 365. Accessoirement, les notifications d’e-mail sont envoyées aux contacts spécifiés indiquant d’un nouveau billet a été publié dans le Centre de messages.
- préciser, au minimum, dans la notification initiale la nature de la violation, une estimation de l’impact de cette violation sur les utilisateurs et les mesures d’atténuation des risques à prendre (le cas échéant). Si notre enquête n’est pas terminée au moment de la notification initiale, nous indiquerons dans cette notification quelles seront les prochaines étapes et quand nous vous recontacterons.

Microsoft reconnaît que les entités de contrôle des données doivent réaliser des évaluations des risques et déterminer si l’autorité de régulation dont dépend le client doit être informée d’une violation de données. Par conséquent, les notifications que nous enverrons aux clients comporteront les informations nécessaires à la réalisation de ces évaluations. Microsoft notifiera donc les clients d’une violation de données personnelles, sauf dans les cas où il a été vérifié que les données personnelles sont illisibles (par exemple, dans le cas de données protégées par un chiffrement où l’intégrité des clés a été vérifiée).

## <a name="office-365-investments-in-data-security"></a>Investissements d’Office 365 dans la sécurité des données

En plus de nous engager à notifier les clients d’une violation dans les meilleurs délais, Office 365 investit massivement dans des systèmes, des processus et du personnel pour réduire le risque de violation de données personnelles et pour détecter rapidement et limiter les conséquences d’une violation dans le cas où elle se produirait.

Voici quelques exemples d’investissements que nous avons réalisés dans ce domaine :

- **Systèmes de contrôle d’accès.** Office 365 poursuit une politique d’« accès non permanent ». Ainsi, les ingénieurs n’ont pas accès au service, sauf s’ils y sont autorisés en réponse à un incident spécifique nécessitant un accès plus élevé. Chaque accès est accordé selon le principe du moindre privilège : une autorisation accordée pour une demande spécifique permet à l’ingénieur d’entreprendre un nombre limité d’actions pour répondre à celle-ci. À cette fin, Office 365 maintient une séparation nette entre les « rôles d’élévation », qui n’autorisent à entreprendre que certaines actions prédéfinies. Le rôle « Accès aux données client » est différent des autres rôles les plus fréquemment utilisés pour administrer le service et fait l’objet d’un examen poussé avant d’être approuvé. Tous nos investissements réalisés dans le domaine du contrôle des accès réduisent considérablement le risque qu’un ingénieur accède indûment à des données client dans Office 365.

- **Systèmes de surveillance de la sécurité et automatisation :** Office 365 gère des systèmes robustes de surveillance de la sécurité en temps réel. À titre d’exemple, ces systèmes déclenchent des alertes en cas de tentative d’accès illicite aux données client ou de transfert illicite des données en dehors de notre service. Pour en revenir au contrôle des accès, nos systèmes de surveillance de la sécurité créent des rapports détaillés des demandes d’élévation envoyées et des mesures prises pour chaque demande d’élévation. Office 365 investit également dans la résolution automatique des problèmes pour parer aux menaces en réponse aux problèmes détectés, ainsi que dans des équipes dédiées pour répondre aux alertes qui ne peuvent pas être résolues automatiquement. Pour nous assurer de la performance de nos systèmes de surveillance de la sécurité, Office 365 réalise régulièrement des exercices de mise en situation au cours desquels une équipe de test interne reproduit le comportement d’un utilisateur malveillant dans l’environnement réel. Ces exercices nous permettent d’améliorer constamment nos fonctionnalités de surveillance de la sécurité et d’intervention.

- **Personnel et processus :** outre l’automatisation, Office 365 met en place des processus et des équipes chargées de sensibiliser l’entreprise sur les questions de confidentialité et les processus de gestion des incidents, et d’exécuter ces processus dans le cas d’une violation de données. Par exemple, une procédure d’exploitation standard en cas de violation de données est appliquée et communiquée aux équipes dans l’ensemble de l’organisation. Cette procédure décrit en détail les rôles et les responsabilités des équipes individuelles d’Office 365 et des équipes centralisées de réponse aux incidents. Ces rôles et responsabilités exposent les mesures que ces équipes doivent prendre pour améliorer leur propre système de sécurité (génération de rapports de sécurité, intégration avec les systèmes de surveillance de la sécurité centralisés et autres bonnes pratiques), ainsi que les mesures à prendre en cas de violation réelle des données (remontée rapide de l’incident pour y réagir, gestion et communication de sources de données spécifiques pour accélérer le processus de réponse). Ces équipes sont également régulièrement formées sur la classification des données et sur les bonnes procédures de gestion et de stockage des données personnelles.

En résumé, Office 365 engage des investissements considérables pour réduire les risques et les conséquences des violations de données personnelles qui affectent nos clients. En cas de violation de données personnelles, nous nous engageons à notifier rapidement nos clients dès que cette violation est confirmée.

## <a name="what-to-expect-in-the-event-of-breach"></a>À quoi vous devez vous attendre en cas de violation

La section ci-dessus décrit les investissements qu’Office 365 prend pour réduire la probabilité de divulgation de données. Dans le cas peu probable où la violation se produit, les clients doivent s’attendre à obtenir une expérience prévisible en termes des réponses suivantes :

- Un processus de réponse aux incidents cohérent au sein d’Office 365. Comme décrit ci-dessus, Office 365 applique des procédures de réponse aux incidents détaillées qui décrivent comment les équipes doivent se préparer à des violations de données et comment elles doivent opérer si une violation se produit. Ces procédures nous permettent de garantir l’application de nos protections et de nos processus dans l’ensemble du service.

- Des critères cohérents pour notifier les clients. Nos critères de notification portent sur la confidentialité, l’intégrité et la disponibilité des données client. Office 365 notifiera directement les clients si la confidentialité ou l’intégrité des données client est compromise. Autrement dit, nous informerons les clients en cas d’accès non autorisé à leurs données, de destruction ou de perte inappropriée des données. Office 365 signalera également les problèmes affectant la disponibilité des données, même si cette action est généralement affichée sur le tableau de bord d’état du service.

- Des notifications détaillées et cohérentes. Quand Office 365 notifie une violation de données, des informations précises seront communiquées aux clients, notamment :

    - le minutage de la violation et de la découverte de la violation ;
    - le nombre approximatif d’utilisateurs affectés ;
    - le type de données utilisateur concernées ;
    - les mesures que l’entité de contrôle des données ou le responsable du traitement des données doit prendre pour atténuer les conséquences de cette violation.

Les clients doivent également savoir qu’Office 365, conformément à son rôle de responsable du traitement des données, ne déterminera pas le niveau de risque de violation de données. Quand une violation de données personnelles est détectée, nous notifierons nos clients et leur communiquerons toutes les informations dont ils ont besoin pour déterminer avec précision le niveau de risque pour les utilisateurs concernés et pour déterminer s’ils doivent signaler l’incident aux autorités de régulation compétentes. À cet effet, les entités de contrôle des données doivent déterminer ce qui suit sur l’incident :

- la gravité de la violation (autrement dit, le niveau de risque) ;
- si les utilisateurs finaux doivent en être informés ;
- si l’autorité de régulation doit en être informée ;
- les mesures spécifiques qui seront prises par l’entité de contrôle des données pour atténuer les conséquences de la violation.

## <a name="contacting-microsoft"></a>Contacter Microsoft

Quand un client détecte une violation de données, il peut souhaiter en informer Microsoft. Conformément au protocole en vigueur, les clients doivent le notifier au Support Microsoft, qui relaiera l’information aux équipes techniques pour obtenir plus de renseignements. Dans ce cas précis, les équipes techniques Microsoft s’engagent elles aussi à communiquer aux clients, via leur interlocuteur du Support, les informations dont ils ont besoin dans les meilleurs délais.

## <a name="call-to-action-for-customers"></a>Ce que les clients doivent faire

Comme indiqué précédemment, Office 365 s’engage à notifier les clients d’une violation de données dans les 72 heures suivant l’incident. L’administrateur client du client en sera informé. Par ailleurs, Office 365 recommande aux clients de désigner un alias pour le Contact international chargé de la confidentialité dans le portail Azure Active Directory. En cas de violation de données personnelles, cet alias peut recevoir un e-mail en plus de la notification qui sera envoyée aux administrateurs.

Le contact chargé de la confidentialité du client peut être une personne de l’organisation, une liste de distribution ou une personne externe à l’organisation. Office 365 demande uniquement aux clients de fournir une adresse de courrier pour ce contact, et les clients peuvent spécifier cette adresse dans le portail Azure Active Directory, sous le champ « contact de confidentialité globale ». Ce champ est lié au champ « Contact technique » dans Azure Active Directory (même s’il s’agit bien d’un champ distinct). Si les clients décident de spécifier une liste de distribution pour ce contact, ils doivent s’assurer que cette liste autorise la réception de messages provenant d’expéditeurs externes.

En résumé, Office 365 demande aux clients de prendre les mesures suivantes pour bénéficier de nos processus de notification de violation :

- Choisissez un contact qui recevra les notifications par e-mail en cas de violation de données personnelles. Ce contact doit avoir connaissance des obligations de l’entité de contrôle des données fixées par le RGPD. Il doit également être prêt à contacter le délégué à la protection des données de l’organisation et, éventuellement, l’autorité de régulation dès qu’il reçoit une notification. Les administrateurs clients recevront également des notifications de violation et doivent eux aussi avoir connaissance des obligations de l’entité de contrôle des données fixées par le RGPD.
- Entrez l’adresse e-mail du contact chargé de la confidentialité dans le portail Azure Active Directory. Si aucune information sur le contact international chargé de la confidentialité n’est fournie, Microsoft en informera uniquement l’administrateur client.
