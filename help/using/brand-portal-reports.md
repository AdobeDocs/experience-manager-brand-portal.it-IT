---
title: Utilizzare i rapporti
seo-title: Work with reports
description: Gli amministratori di Experience Manager Assets Brand Portal possono visualizzare i rapporti sull’utilizzo di Brand Portal e creare, gestire e visualizzare i rapporti sulle risorse scaricate, scadute, pubblicate e condivise tramite Brand Portal.
seo-description: Experience Manager Assets Brand Portal Administrators can view report about Brand Portal usage, and create, manage, and view reports around assets downloaded, expired, published, and link shared through Brand Portal.
uuid: dc4e5275-a614-4b95-8c70-2b7e470c50a7
content-type: reference
topic-tags: administration
products: SG_EXPERIENCEMANAGER/Brand_Portal
discoiquuid: 7683074f-b6ea-42e0-a411-3b13eb88d1f2
role: Admin
exl-id: 03d0292c-23c2-4ea0-9781-eb27768e6c33
source-git-commit: 955cd8afe939ff47e9f08f312505e230e2f38495
workflow-type: tm+mt
source-wordcount: '1000'
ht-degree: 1%

---

# Utilizzare i rapporti {#work-with-reports}

La funzionalità di reporting è fondamentale per valutare l’utilizzo di Brand Portal e conoscere il modo in cui gli utenti interni ed esterni interagiscono con le risorse approvate. Gli amministratori possono visualizzare il rapporto sull’utilizzo di Brand Portal, sempre disponibile nella pagina Rapporti sulle risorse. Tuttavia, i rapporti per gli accessi degli utenti e le risorse scaricate, scadute, pubblicate e condivise tramite collegamenti possono essere generati e visualizzati dalla pagina Rapporti sulle risorse. Questi rapporti sono utili per l’analisi della distribuzione delle risorse, che consente di derivare metriche di successo chiave per misurare il livello di adozione delle risorse approvate all’interno e all’esterno dell’organizzazione.

L’interfaccia di gestione dei rapporti è intuitiva e include opzioni e controlli dettagliati per accedere ai rapporti salvati. Puoi visualizzare, scaricare o eliminare i rapporti dalla pagina Rapporti su risorse, in cui sono elencati tutti i rapporti generati in precedenza.

## Visualizzare i rapporti {#view-reports}

Per visualizzare un rapporto, effettua le seguenti operazioni:

1. Dalla barra degli strumenti nella parte superiore, tocca o fai clic sul logo dell’Experience Manager per accedere agli strumenti di amministrazione.

   ![](assets/aemlogo.png)

1. Dal pannello Strumenti di amministrazione, fai clic su **[!UICONTROL Crea/Gestisci rapporti]** per aprire la pagina **[!UICONTROL Rapporti su risorse]**.

   ![](assets/access-asset-reports.png)

1. Accedi al report **[!UICONTROL Utilizzo]** e ad altri report generati dalla pagina Report risorse.

   >[!NOTE]
   >
   >Il rapporto di utilizzo è un rapporto predefinito generato in Brand Portal. Non può essere creata o eliminata. Tuttavia, puoi creare, scaricare ed eliminare i rapporti Scarica, Scadenza, Publish, Condivisione collegamenti e Accessi utente.

   Per visualizzare un rapporto, fai clic sul collegamento al rapporto. In alternativa, seleziona il rapporto e tocca o fai clic sull’icona Visualizza nella barra degli strumenti.

   **[!UICONTROL Report utilizzo]** visualizza informazioni sul numero di utenti Brand Portal attivi, lo spazio di archiviazione occupato da tutte le risorse e il numero totale di risorse in Brand Portal. Gli utenti di Brand Portal che non sono assegnati ad alcun profilo di prodotto nell&#39;Admin Console sono considerati utenti inattivi e non sono inclusi nel **[!UICONTROL Report utilizzo]**.
Il rapporto mostra anche la capacità consentita per ciascuna di queste metriche informative.

   ![](assets/usage-report.png)

   Il report **[!UICONTROL Accessi utente]** fornisce informazioni sugli utenti che hanno effettuato l&#39;accesso a Brand Portal. Il rapporto mostra nomi visualizzati, ID e-mail, utenti tipo (amministratore, visualizzatore, editor, ospite), gruppi, ultimo accesso, stato attività e conteggio di accesso di ogni utente dalla distribuzione di Brand Portal 6.4.2 fino al momento della generazione del rapporto.

   ![](assets/user-logins.png)

   Il report **[!UICONTROL Scarica]** elenca e fornisce dettagli su tutte le risorse scaricate in un intervallo di date e ore specifico.

   ![](assets/download-report.png)

   >[!NOTE]
   >
   >Nel rapporto delle risorse **[!UICONTROL Scarica]** sono visualizzate solo le risorse selezionate e scaricate singolarmente da Brand Portal. Se un utente ha scaricato una cartella contenente risorse, il rapporto non visualizza la cartella o le risorse all’interno della cartella.

   **[!UICONTROL Il rapporto Scadenza]** elenca e fornisce i dettagli di tutte le risorse scadute in un intervallo di tempo specifico.

   ![](assets/expiration-report.png)

   Il report **[!UICONTROL Publish]** elenca e fornisce informazioni su tutte le risorse pubblicate da Experience Manager Assets a Brand Portal in un intervallo di tempo specificato.

   ![](assets/publish-report.png)

   >[!NOTE]
   >
   >Nel rapporto di Publish non vengono visualizzate informazioni sui frammenti di contenuto, poiché questi non possono essere pubblicati in Brand Portal.

   **[!UICONTROL Rapporto Condivisione collegamenti]** elenca tutte le risorse condivise tramite collegamenti dall&#39;interfaccia di Brand Portal in un intervallo di tempo specifico. Il rapporto indica anche quando la risorsa è stata condivisa tramite collegamento, da quale utente, quando scade il collegamento e il numero di collegamenti condivisi per il tenant (e gli utenti con cui è stato condiviso il collegamento alla risorsa). Le colonne del rapporto Condivisione collegamenti non sono personalizzabili.

   ![](assets/link-share-report.png)

   >[!NOTE]
   >
   >Nel rapporto Condivisione collegamenti non vengono visualizzati gli utenti che hanno accesso alla risorsa condivisa tramite il collegamento o che hanno scaricato la risorsa tramite il collegamento.
   >
   >Per tenere traccia dei download tramite il collegamento condiviso, devi generare il report di download dopo aver selezionato l&#39;opzione **[!UICONTROL Solo download da condivisione collegamenti]** nella pagina **[!UICONTROL Crea report]**. Tuttavia, in questo caso, l’utente (scaricato da) è anonimo.

## Generare rapporti {#generate-reports}

Gli amministratori possono generare e gestire i seguenti rapporti standard; una volta generati, vengono salvati per essere [accessibili](../using/brand-portal-reports.md#main-pars-header) in un secondo momento:

* Accessi utenti
* Scarica
* Scadenza
* Pubblicazione
* Condivisione collegamenti

Le colonne nei rapporti Scarica, Scadenza e Publish possono essere personalizzate per la visualizzazione. Per generare un rapporto, effettua le seguenti operazioni:

1. Dalla barra degli strumenti nella parte superiore, tocca o fai clic sul logo dell’Experience Manager per accedere agli strumenti di amministrazione.

1. Dal pannello Strumenti di amministrazione, tocca o fai clic su **[!UICONTROL Crea/Gestisci rapporti]** per aprire la pagina **[!UICONTROL Rapporti su risorse]**.

   ![](assets/asset-reports.png)

1. Nella pagina Rapporti su risorse, tocca o fai clic su **[!UICONTROL Crea]**.
1. Dalla pagina **[!UICONTROL Crea report]**, seleziona un report da creare e tocca o fai clic su **[!UICONTROL Avanti]**.

   ![](assets/crete-report.png)

1. Configurare i dettagli del rapporto. Specifica il titolo, la descrizione, la struttura delle cartelle (in cui il report deve essere eseguito e generare statistiche) e l&#39;intervallo di date per i report **[!UICONTROL Download]**, **[!UICONTROL Scadenza]** e **[!UICONTROL Publish]**.

   ![](assets/create-report-page.png)

   Il **[!UICONTROL rapporto Condivisione collegamenti]** richiede invece solo i parametri di titolo, descrizione e intervallo di date.

   ![](assets/create-link-share-report.png)

   >[!NOTE]
   >
   >I caratteri speciali # e % nel titolo del rapporto sono sostituiti da un trattino (-) nella generazione del rapporto.

1. Tocca o fai clic su **[!UICONTROL Avanti]** per configurare le colonne dei rapporti Scarica, Scadenza e Publish.
1. Seleziona o deseleziona le caselle di controllo appropriate, in base alle esigenze. Ad esempio, per visualizzare i nomi degli utenti (che hanno scaricato le risorse) nel report **[!UICONTROL Scarica]**, seleziona **[!UICONTROL Scaricato da]**. L’immagine seguente illustra come selezionare le colonne predefinite nel rapporto di download.

   ![](assets/createdownloadreport.png)

   Puoi anche aggiungere colonne personalizzate a questi rapporti per visualizzare più dati per i requisiti personalizzati.

   Per aggiungere colonne personalizzate al rapporto Download, Publish o Scadenza, effettua le seguenti operazioni:

   1. Per visualizzare una colonna personalizzata, tocca o fai clic su **[!UICONTROL Aggiungi]** in [!UICONTROL Colonne personalizzate].
   1. Specificare il nome della colonna nel campo **[!UICONTROL Nome colonna]**.
   1. Seleziona la proprietà a cui mappare la colonna utilizzando il selettore delle proprietà.

      ![](assets/property-picker.png)
In alternativa, digita il percorso nel campo percorso proprietà.

      ![](assets/property-path.png)

      Per aggiungere altre colonne personalizzate, tocca o fai clic su **Aggiungi** e ripeti i passaggi 2 e 3.

1. Tocca o fai clic su **[!UICONTROL Crea]**. Un messaggio notifica che la generazione del rapporto è stata avviata.

## Scaricare i rapporti {#download-reports}

Per salvare e scaricare un report come file .csv, effettuare una delle seguenti operazioni:

* Seleziona un rapporto nella pagina Rapporti su risorse, quindi tocca o fai clic su **[!UICONTROL Scarica]** nella barra degli strumenti nella parte superiore.

![](assets/download-asset-report.png)

* Dalla pagina Rapporti su risorse, apri un rapporto. Seleziona l&#39;opzione **[!UICONTROL Scarica]** nella parte superiore della pagina del report.

![](assets/download-report-fromwithin.png)

## Eliminare i rapporti {#delete-reports}

Per eliminare un rapporto esistente, selezionalo dalla pagina **[!UICONTROL Rapporti risorse]** e tocca o fai clic su **[!UICONTROL Elimina]** nella barra degli strumenti nella parte superiore.

>[!NOTE]
>
>Impossibile eliminare il report **[!UICONTROL Usage]**.
