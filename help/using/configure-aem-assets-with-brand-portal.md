---
title: Configurare Experience Manager Assets con Brand Portal
seo-title: Configure Experience Manager Assets with Brand Portal
description: Informazioni sulla configurazione di Experience Manager Assets con Brand Portal.
seo-description: Get an insight into configuring Experience Manager Assets with Brand Portal.
uuid: null
content-type: reference
contentOwner: Vishabh Gupta
topic-tags: brand-portal
products: SG_EXPERIENCEMANAGER/Brand_Portal
discoiquuid: null
role: Admin
exl-id: 261c0e84-6b3d-459c-b6b9-a9af106d6943
source-git-commit: 454b05c05359a2068cc29124f826d5bd25a1bad1
workflow-type: tm+mt
source-wordcount: '357'
ht-degree: 2%

---

# Configurare Experience Manager Assets con Brand Portal {#configure-integration}

La configurazione di Adobe Experience Manager Assets con Brand Portal consente agli utenti di Brand Portal di pubblicare risorse, distribuirle e usufruire delle funzioni di contributo alle risorse. Consente agli utenti di Experience Manager Assets di pubblicare e distribuire le risorse con gli utenti di Brand Portal. Gli utenti di Brand Portal possono accedere alle risorse condivise e contribuire caricando nuove risorse nelle cartelle di contributo delle risorse e pubblicandole nuovamente in Experience Manager Assets.

La configurazione di Experience Manager Assets con Brand Portal è supportata su:

* Experience Manager Assets as a Cloud Service
* Experience Manager Assets (on-premise e managed service) 6.5 e versioni successive

Experience Manager Assets as a Cloud Service viene configurato automaticamente con Brand Portal attivando Brand Portal da Cloud Manager. Il flusso di lavoro di attivazione crea le configurazioni richieste nel backend e attiva Brand Portal nella stessa organizzazione IMS dell’istanza Experience Manager Assets as a Cloud Service.

A differenza di questo, Experience Manager Assets (on-premise e managed service) viene configurato manualmente con Brand Portal utilizzando Adobe Developer Console, che fornisce un token Identity Management Services (IMS) di Adobe per l’autorizzazione del tenant Brand Portal.

>[!NOTE]
>
>***Per Experience Manager Assets 6.5 e versioni successive***
>
>In precedenza, Brand Portal era configurato nell’interfaccia classica tramite il gateway OAuth legacy, che utilizza lo scambio JSON Web token (JWT) per ottenere un token IMS per l’autorizzazione.
>
>La configurazione tramite Legacy OAuth non è più supportata a partire dal 6 aprile 2020 e viene modificata in configurazione tramite Adobe Developer Console.


>[!TIP]
>
>***Solo per i clienti esistenti (servizio locale e gestito)***
>
>La configurazione del gateway OAuth legacy continuerà a funzionare per i clienti esistenti.
>
>In caso di problemi con la configurazione legacy del gateway OAuth, elimina la configurazione esistente e crea una nuova configurazione tramite Adobe Developer Console.

I passaggi per configurare AEM Assets con Brand Portal variano a seconda della versione dell’AEM in uso e dell’esecuzione della prima configurazione o dell’aggiornamento delle configurazioni esistenti:

| **Versione AEM** | **Nuova configurazione** | **Configurazione aggiornamento** |
|---|---|---|
| **AEM Assets as a Cloud Service** | [Attiva Brand Portal](https://experienceleague.adobe.com/docs/experience-manager-cloud-service/assets/brand-portal/configure-aem-assets-with-brand-portal.html) | - |
| **AEM 6.5 (6.5.4.0 e versioni successive)** | [Crea configurazione](https://experienceleague.adobe.com/docs/experience-manager-65/assets/brandportal/configure-aem-assets-with-brand-portal.html) | [Aggiorna configurazione](https://experienceleague.adobe.com/docs/experience-manager-65/assets/brandportal/configure-aem-assets-with-brand-portal.html#upgrade-integration-65) |
