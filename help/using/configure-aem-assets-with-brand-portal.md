---
title: Configurare Experience Manager Assets con Brand Portal
description: Introduzione a un insight nella configurazione di Experience Manager Assets con Brand Portal.
content-type: reference
contentOwner: Vishabh Gupta
topic-tags: brand-portal
products: SG_EXPERIENCEMANAGER/Brand_Portal
role: Admin
exl-id: 261c0e84-6b3d-459c-b6b9-a9af106d6943
source-git-commit: f4add370fd3242f5506e5cc4d921362e2b14141a
workflow-type: tm+mt
source-wordcount: '361'
ht-degree: 18%

---

# Configurare Experience Manager Assets con Brand Portal {#configure-integration}

La configurazione di Adobe Experience Manager Assets con Brand Portal consente agli utenti di Brand Portal di pubblicare risorse, distribuirle e usufruire delle funzioni di contributo alle risorse. Consente agli utenti di Experience Manager Assets di pubblicare e distribuire risorse con gli utenti di Brand Portal. Gli utenti di Brand Portal possono accedere alle risorse condivise e contribuire caricando nuove risorse nelle cartelle di contributo delle risorse e pubblicandole nuovamente in Experience Manager Assets.

La configurazione di Experience Manager Assets con Brand Portal è supportata su:

* Experience Manager Assets as a Cloud Service
* Experience Manager Assets (on-premise e managed service) 6.5 e versioni successive

Experience Manager Assets as a Cloud Service viene configurato automaticamente con Brand Portal attivando Brand Portal da Cloud Manager. Il flusso di lavoro di attivazione crea le configurazioni richieste nel backend e attiva Brand Portal nella stessa organizzazione IMS dell’istanza Experience Manager Assets as a Cloud Service.

Mentre Experience Manager Assets (on-premise e managed service) viene configurato manualmente con Brand Portal utilizzando Adobe Developer Console, che fornisce un token Adobe Identity Management Services (IMS) per l’autorizzazione del tenant Brand Portal.

>[!NOTE]
>
>***Per Experience Manager Assets, versione 6.5 e successive***
>
>In precedenza, l’interfaccia classica configurava Brand Portal utilizzando il gateway OAuth legacy, che utilizza lo scambio JSON Web Token (JWT) per ottenere un token IMS per l’autorizzazione.
>
>La configurazione tramite OAuth legacy non è più supportata a partire dal 6 aprile 2020 e viene modificata in configurazione tramite Adobe Developer Console.


>[!TIP]
>
>***Solo per i clienti esistenti (servizio locale e gestito)***
>
>La configurazione del gateway OAuth legacy continua a funzionare per i clienti esistenti.
>
>In caso di problemi con la configurazione del gateway OAuth legacy, elimina la configurazione esistente e crea una nuova configurazione tramite Adobe Developer Console.

Per configurare AEM Assets con Brand Portal si seguono passaggi diversi a seconda della versione di AEM in uso e se si tratta della prima configurazione o dell’aggiornamento di configurazioni esistenti:

| **Versione di AEM** | **Nuova configurazione** | **Aggiornamento della configurazione** |
|---|---|---|
| **AEM Assets as a Cloud Service** | [Attiva Brand Portal](https://experienceleague.adobe.com/it/docs/experience-manager-cloud-service/content/assets/brand-portal/configure-aem-assets-with-brand-portal) | - |
| **AEM 6.5 (6.5.4.0 e versioni successive)** | [Creare una configurazione](https://experienceleague.adobe.com/it/docs/experience-manager-65/content/assets/brandportal/configure-aem-assets-with-brand-portal) | [Aggiornare una configurazione](https://experienceleague.adobe.com/it/docs/experience-manager-65/content/assets/brandportal/configure-aem-assets-with-brand-portal#upgrade-integration-65) |
