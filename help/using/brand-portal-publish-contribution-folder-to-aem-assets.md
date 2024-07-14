---
title: Caricare le risorse e pubblicare la cartella Contributi da Brand Portal a Experience Manager Assets
seo-title: Upload assets and publish the Contribution folder from Brand Portal to Experience Manager Assets
description: Ottieni informazioni sul caricamento di nuove risorse e sulla pubblicazione della cartella dei contributi da Brand Portal a Experience Manager Assets.
seo-description: Get an insight into uploading new assets and publishing the contribution folder from Brand Portal to Experience Manager Assets.
uuid: null
content-type: reference
contentOwner: Vishabh Gupta
topic-tags: brand-portal
products: SG_EXPERIENCEMANAGER/Brand_Portal
discoiquuid: null
exl-id: 7dcf445d-97ed-4fa5-959c-c4c48e325766
source-git-commit: 606f4389780025f5cf92b11bf8cac464e36be44a
workflow-type: tm+mt
source-wordcount: '1475'
ht-degree: 0%

---

# Cartella dei contributi di Publish a Experience Manager Assets {#using-asset-souring-in-bp}

Gli utenti di Brand Portal con le autorizzazioni appropriate possono caricare più risorse, o cartelle contenenti più risorse, nella cartella Contributi. Tuttavia, gli utenti di Brand Portal possono caricare solo risorse nella cartella **NEW**. La cartella **SHARED** è destinata alla distribuzione delle risorse di base (contenuto di riferimento) che possono essere utilizzate dagli utenti di Brand Portal durante la creazione di nuove risorse per il contributo.

L’utente di Brand Portal che dispone dell’autorizzazione per accedere alla cartella dei contributi può eseguire le seguenti attività:

* [Scaricare i requisiti delle risorse](#download-asset-requirements)
* [Carica nuove risorse nella cartella Contributi](#uplad-new-assets-to-contribution-folder)
* [Cartella dei contributi di Publish a Experience Manager Assets](#publish-contribution-folder-to-aem)

## Scaricare i requisiti delle risorse {#download-asset-requirements}

Gli utenti di Brand Portal ricevono automaticamente notifiche e-mail/impulsi ogni volta che un utente di Experience Manager Assets condivide una cartella di contributi, consentendo loro di scaricare il documento breve (requisito risorsa) e le risorse di base (contenuto di riferimento) dalla cartella **SHARED** per assicurarsi di comprendere i requisiti delle risorse.

L’utente di Brand Portal esegue le seguenti attività per scaricare i requisiti delle risorse:

* **Download della descrizione**: scarica la descrizione (documento sui requisiti delle risorse) allegata alla cartella dei contributi che contiene informazioni relative alle risorse come tipo di risorse, finalità, formati supportati, dimensioni massime delle risorse e così via.
* **Scarica risorse di base**: scarica le risorse di base che possono essere utilizzate per comprendere i tipi di risorse richiesti. Gli utenti di Brand Portal possono utilizzare queste risorse come riferimento per creare nuove risorse da aggiungere.

Il dashboard di Brand Portal include tutte le cartelle esistenti consentite all’utente di Brand Portal, insieme alla cartella dei contributi appena condivisa. In questo esempio, l’utente di Brand Portal ha accesso solo alla cartella dei contributi appena creata e non viene condivisa con l’utente alcuna altra cartella esistente.

**Per scaricare i requisiti delle risorse:**

1. Accedi all’istanza di Brand Portal.
1. Seleziona cartella contributi dal dashboard di Brand Portal.
1. Fare clic su **[!UICONTROL Proprietà]**. Viene visualizzata la finestra Proprietà contenente i dettagli della cartella dei contributi.

   ![](assets/properties.png)

   ![](assets/download-asset-requirement2.png)

1. Fai clic sull&#39;opzione **[!UICONTROL Scarica resoconto]** per scaricare il documento sui requisiti delle risorse nel computer locale.

   ![](assets/download.png)

1. Torna alla dashboard di Brand Portal.
1. Fare clic per aprire la cartella dei contributi. Nella cartella dei contributi verranno visualizzate due sottocartelle: **[!UICONTROL CONDIVISO]** e **[!UICONTROL NUOVO]**. La cartella SHARED contiene tutte le risorse di base (contenuto di riferimento) condivise dagli amministratori.
1. Puoi scaricare la cartella **[!UICONTROL SHARED]** contenente tutte le risorse della linea di base sul computer locale.
In alternativa, è possibile aprire la cartella **[!UICONTROL SHARED]** e fare clic sull&#39;icona **Scarica** per scaricare singoli file o cartelle.

   ![](assets/download.png)

   ![](assets/download-asset-requirement5.png)

Consulta la descrizione (documento sui requisiti delle risorse) e fai riferimento alle risorse di base per comprenderne i requisiti. Ora puoi creare nuove risorse per il contributo e caricarle nella cartella Contributi.


## Carica risorse nella cartella dei contributi {#upload-new-assets-to-contribution-folder}

Dopo aver valutato i requisiti delle risorse, gli utenti di Brand Portal possono creare nuove risorse da assegnare ai contributi e caricarle nella cartella NEW all’interno della cartella Contributi. Un utente può caricare più risorse in una cartella di contributi risorse. Tuttavia, è possibile creare una sola cartella alla volta.

>[!NOTE]
>
>Gli utenti di Brand Portal possono caricare le risorse (massimo **2** GB per dimensione di file) nella NUOVA cartella.
>
>Il limite massimo di caricamento per qualsiasi tenant Brand Portal è **10** GB, applicato cumulativamente a tutte le cartelle dei contributi.
>
>Le risorse caricate in Brand Portal non vengono elaborate per le rappresentazioni e non contengono anteprime.

>[!NOTE]
>
>Si consiglia di rilasciare lo spazio di caricamento dopo la pubblicazione della cartella Contributi in Experience Manager Assets in modo che sia disponibile per il contributo degli altri utenti di Brand Portal.
>
>Se è necessario estendere il limite di caricamento del tenant Brand Portal oltre **10** GB, contatta l&#39;Assistenza clienti specificando il requisito.


**Per caricare nuove risorse:**

1. Accedi all’istanza di Brand Portal.
Il dashboard di Brand Portal include tutte le cartelle esistenti consentite all’utente di Brand Portal, insieme alla cartella dei contributi appena condivisa.

1. Selezionare la cartella dei contributi e fare clic per aprirla. La cartella dei contributi contiene due sottocartelle: **[!UICONTROL SHARED]** e **[!UICONTROL NEW]**.

1. Fai clic sulla cartella **[!UICONTROL NEW]**.

   ![](assets/upload-new-assets4.png)

1. Fai clic su **[!UICONTROL Crea]** > **[!UICONTROL File]** per caricare singoli file o cartelle (.zip) contenenti più risorse.

   ![](assets/upload-new-assets5.png)

1. Sfoglia e carica le risorse (file o cartelle) nella cartella **[!UICONTROL NEW]**.

   ![](assets/upload-asset4.png)

Dopo aver caricato tutte le risorse o cartelle nella nuova cartella, pubblica la cartella dei contributi in Experience Manager Assets.


## Cartella dei contributi di Publish a Experience Manager Assets {#publish-contribution-folder-to-aem}

Gli utenti di Brand Portal possono pubblicare la cartella dei contributi in Experience Manager Assets senza dover accedere all’istanza di authoring di Experience Manager.

Verifica di aver soddisfatto i requisiti delle risorse e carica le nuove risorse create nella cartella **NEW** all&#39;interno della cartella Contributi.

**Per pubblicare la cartella dei contributi:**

1. Accedi all’istanza di Brand Portal.

1. Seleziona cartella contributi dal dashboard di Brand Portal.
1. Fare clic su **[!UICONTROL Publish per AEM]**.

   ![](assets/export.png)

   ![](assets/publish-contribution-folder-to-aem1.png)

Una notifica e-mail/impulso viene inviata all’utente di Brand Portal e agli amministratori in diverse fasi del flusso di lavoro di pubblicazione:

1. **In coda** - Viene inviata una notifica all&#39;utente di Brand Portal e agli amministratori di Brand Portal quando viene attivato un flusso di lavoro di pubblicazione in Brand Portal.

1. **Completo** - Viene inviata una notifica all&#39;utente di Brand Portal e agli amministratori di Brand Portal quando la cartella Contributi viene pubblicata correttamente in Experience Manager Assets.

Dopo aver pubblicato in Experience Manager Assets le nuove risorse create, gli utenti di Brand Portal possono eliminarle dalla cartella NEW. L’amministratore di Brand Portal può invece eliminare le risorse sia dalla cartella NUOVA che da QUELLA CONDIVISA.

Una volta raggiunto l’obiettivo di creare la cartella dei contributi, l’amministratore di Brand Portal può eliminarla per liberare lo spazio di caricamento per altri utenti.

## Stato processo di pubblicazione {#publishing-job-status}

Esistono due rapporti che gli amministratori possono utilizzare per visualizzare lo stato delle cartelle di contributo alle risorse pubblicate da Brand Portal a Experience Manager Assets.

* In Brand Portal, passa a **[!UICONTROL Strumenti]** > **[!UICONTROL Stato contributo risorse]**. Questo rapporto riflette lo stato di tutti i processi di pubblicazione nelle diverse fasi del flusso di lavoro di pubblicazione.

  ![](assets/contribution-folder-status-v2.png)

* In Experience Manager Assets (servizio locale o gestito), passa a **[!UICONTROL Assets]** > **[!UICONTROL Jobs]**. Questo rapporto riflette lo stato finale (Completato o Errore) di tutti i processi di pubblicazione.

  ![](assets/publishing-status.png)

* In Experience Manager Assets as a Cloud Service, passa a **[!UICONTROL Assets]** > **[!UICONTROL Jobs]**.

  In alternativa, puoi passare direttamente a **[!UICONTROL Processi]** dalla navigazione globale.

  Questo rapporto riflette lo stato finale (Completato o Errore) di tutti i processi di pubblicazione, inclusa l’importazione di risorse da Brand Portal a Experience Manager Assets in as a Cloud Service.

  ![](assets/cloud-service-job-status.png)

<!--
>[!NOTE]
>
>Currently, no report is generated in AEM Assets as a Cloud Service for the Asset Sourcing workflow. 
-->

## Eliminazione automatica delle risorse pubblicate in Experience Manager Assets dalla cartella Contributi {#automatically-delete-published-assets-from-contribution-folder}

Brand Portal ora esegue processi automatici ogni dodici ore per analizzare tutte le cartelle Contributi ed eliminare tutte le risorse pubblicate nell’AEM. Di conseguenza, non è necessario eliminare manualmente le risorse nella cartella Contributi per mantenere la dimensione della cartella al di sotto del [limite di soglia](#upload-new-assets-to-contribution-folder). È inoltre possibile monitorare lo stato dei processi di eliminazione eseguiti automaticamente negli ultimi sette giorni. Il rapporto di un job fornisce i dettagli riportati di seguito.

* Ora di inizio processo
* Ora di fine processo
* Stato processo
* Totale risorse incluse in un processo
* Totale risorse eliminate correttamente in un processo
* Memoria totale resa disponibile in seguito all&#39;esecuzione del processo

  ![Rapporto di eliminazione](assets/deletion-reports.png)

Puoi anche eseguire un drill-down per visualizzare i dettagli di ciascuna risorsa inclusa in un processo di eliminazione. Dettagli quali titolo della risorsa, dimensione, autore, stato di eliminazione e ora di eliminazione sono inclusi nel rapporto.

![Rapporto di eliminazione dettagliato](assets/deletion-reports-detailed.png)

>[!NOTE]
>
> * I clienti possono richiedere all’Assistenza clienti Adobe di disabilitare e riabilitare la funzionalità del processo di eliminazione automatico o di modificarne la frequenza di esecuzione.
> * Questa funzione è disponibile con Experience Manager 6.5.13.0 e versioni successive.

### Visualizzare e scaricare i rapporti di eliminazione {#view-delete-jobs}

Per visualizzare e scaricare i rapporti per un processo di eliminazione:

1. In Brand Portal, passa all&#39;opzione **[!UICONTROL Strumenti]**>**[!UICONTROL Stato contributo risorse]**>**[!UICONTROL Rapporti eliminazione]**.

1. Selezionare un processo e fare clic su **[!UICONTROL Visualizza]** per visualizzare il report.

   Visualizzare i dettagli di ciascuna risorsa inclusa in un processo di eliminazione. Dettagli quali titolo della risorsa, dimensione, autore, stato di eliminazione e ora di eliminazione sono inclusi nel rapporto. Fai clic su **[!UICONTROL Scarica]** per scaricare il rapporto per il processo in formato CSV.

   Lo stato di eliminazione di una risorsa nel rapporto può avere i seguenti valori possibili:

   * **Eliminata** - La risorsa è stata eliminata dalla cartella Contributi.

   * **Non trovato** - Brand Portal non è riuscito a trovare la risorsa nella cartella Contributi. La risorsa è già stata eliminata manualmente dalla cartella.

   * **Ignorato** - Brand Portal ha ignorato l&#39;eliminazione della risorsa perché è disponibile una nuova versione della risorsa nella cartella Contribution, non ancora pubblicata in Experience Manager.

   * **Non riuscito** - Brand Portal non è riuscito a eliminare la risorsa. Sono disponibili tre tentativi per eliminare una risorsa con stato di eliminazione `Failed`. Se la risorsa non riesce al terzo tentativo di eliminazione, devi eliminarla manualmente.

### Eliminare un rapporto

Brand Portal consente inoltre di selezionare uno o più rapporti ed eliminarli manualmente.

Per eliminare un rapporto:

1. Passa all&#39;opzione **[!UICONTROL Strumenti]**>**[!UICONTROL Stato contributo risorse]**>**[!UICONTROL Rapporti eliminazione]**.

1. Selezionare uno o più report e fare clic su **[!UICONTROL Elimina]**.


