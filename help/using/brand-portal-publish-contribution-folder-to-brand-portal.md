---
title: Configurare e pubblicare la cartella dei contributi da Experience Manager Assets a Brand Portal
seo-title: Configure and publish contribution folder from Experience Manager Assets to Brand Portal
description: Ottieni informazioni sulla configurazione e la pubblicazione di una cartella di contributi da Experience Manager Assets a Brand Portal.
seo-description: Get an insight into configuring and publishing a contribution folder from Experience Manager Assets to Brand Portal.
uuid: null
content-type: reference
contentOwner: Vishabh Gupta
topic-tags: brand-portal
products: SG_EXPERIENCEMANAGER/Brand_Portal
discoiquuid: null
exl-id: 9acad588-977a-45de-b544-f2cc8874ba12
source-git-commit: 3845d9fa17e75d59493383303ca0978349ca0401
workflow-type: tm+mt
source-wordcount: '1037'
ht-degree: 0%

---

# Configurare la cartella dei contributi in Experience Manager Assets {#configure-contribution-folder}

Per l&#39;origine collaborativa delle risorse, gli utenti di Experience Manager Assets (amministratori e utenti non amministratori autorizzati) possono creare nuove cartelle di tipo **Contributo risorse**, assicurandosi che la nuova cartella creata sia aperta all&#39;invio di risorse da parte degli utenti di Brand Portal.  Questo attiva automaticamente un flusso di lavoro che crea due sottocartelle aggiuntive, denominate **SHARED** e **NEW**, all&#39;interno della cartella **Contribution** appena creata.

L&#39;utente di Experience Manager Assets definisce quindi i requisiti delle risorse caricando una breve descrizione dei tipi di risorse da aggiungere alla cartella dei contributi, nonché un set di risorse di base, nella cartella **SHARED** per garantire che gli utenti di Brand Portal dispongano delle informazioni necessarie. L’amministratore può quindi concedere agli utenti di Brand Portal attivi l’accesso alla cartella dei contributi prima di pubblicare in Brand Portal la cartella dei contributi appena creata.

Il video seguente illustra come configurare una cartella Contributi in Experience Manager Assets:

>[!VIDEO](https://video.tv.adobe.com/v/30547)

L’utente di Experience Manager Assets esegue le seguenti attività durante la configurazione di una cartella di contributi:

* [Crea cartella contributi](#create-contribution-folder)
* [Carica fabbisogni di risorse e assegna collaboratori](#configure-contribution-folder-properties)
* [Carica risorse di base](#uplad-new-assets-to-contribution-folder)
* [Cartella dei contributi di Publish da Experience Manager Assets a Brand Portal](#publish-contribution-folder-to-brand-portal)

## Crea cartella contributi {#create-contribution-folder}


Gli amministratori di Experience Manager Assets e gli utenti non amministratori autorizzati a creare una nuova cartella possono creare una cartella Contributi in Experience Manager Assets.
Per creare una cartella di contributi, crea una nuova cartella di tipo Contributo risorse, in modo che la nuova cartella creata sia aperta all’invio di risorse da parte degli utenti di Brand Portal.  Questo attiva automaticamente un flusso di lavoro che crea due sottocartelle aggiuntive, denominate CONDIVISO e NUOVO, all’interno della cartella dei contributi.


>[!NOTE]
>
>Gli amministratori possono creare più cartelle di contributi alle risorse all’interno di una cartella.
>
>Una cartella di contributi per le risorse contiene cartelle NUOVE e CONDIVISE per la distribuzione e il contributo delle risorse. Non creare una cartella di risorse, cartelle o contributi all&#39;interno di una cartella di contributi.


Puoi configurare le proprietà della cartella dei contributi separatamente e durante la creazione della cartella dei contributi. In questo esempio, stiamo configurando le proprietà separatamente.

**Per creare una cartella contributi:**

1. Accedi all’istanza di Experience Manager Assets.

1. Passa a **[!UICONTROL Assets]** > **[!UICONTROL File]**. Elenca tutte le cartelle esistenti nell’archivio di Experience Manager Assets.

1. Fai clic su **[!UICONTROL Crea]** per creare una nuova cartella. Viene visualizzata la finestra di dialogo **[!UICONTROL Crea cartella]**.

1. Immetti **[!UICONTROL Titolo]** e **[!UICONTROL Nome]** della cartella e seleziona la casella di controllo **[!UICONTROL Contributo risorsa]**.
Si consiglia di utilizzare lettere minuscole senza spazio per denominare la cartella.

1. Fai clic su **[!UICONTROL Crea]**. Puoi visualizzare la cartella dei contributi elencata nell’archivio Experience Manager Assets.

   >[!NOTE]
   >
   >Un utente che non è amministratore può creare e condividere una cartella di contributi per le risorse, ma non può modificarla o eliminarla.


   ![](assets/create-contribution-folder.png)

1. Fare clic per aprire la cartella dei contributi. Verranno visualizzate due sottocartelle: **[!UICONTROL CONDIVISO]** e **[!UICONTROL NUOVO]** create automaticamente nella cartella dei contributi.

   ![](assets/contribution-folder.png)


## Configurare le proprietà della cartella contributi {#configure-contribution-folder-properties}

L’amministratore di Experience Manager Assets esegue le seguenti attività durante la configurazione delle proprietà di una cartella di contributi.

* **Aggiungi descrizione**: fornire una descrizione di alto livello della cartella dei contributi.
* **Descrizione del caricamento**: carica il documento dei requisiti delle risorse contenente le informazioni relative alle risorse.
* **Aggiungi collaboratori**: aggiungi gli utenti Brand Portal per concedere loro l&#39;accesso alla cartella dei contributi.

Il requisito risorsa si riferisce ai dettagli forniti dagli amministratori per aiutare i collaboratori (utenti Brand Portal) a comprendere le esigenze e i requisiti della cartella dei contributi. L’amministratore carica un documento sui requisiti delle risorse che contiene una descrizione del tipo di risorse da aggiungere alla cartella Contributi e informazioni relative alle risorse, ad esempio scopo, tipo di immagini, dimensione massima e così via.

**Per configurare le proprietà della cartella dei contributi:**

1. Accedi all’istanza di Experience Manager Assets.

1. Passa a **[!UICONTROL Assets > File]** e individua la cartella dei contributi.
1. Selezionare la cartella dei contributi e fare clic su **[!UICONTROL Proprietà]** per aprire la finestra Proprietà cartella.

   ![](assets/properties.png)

   ![](assets/contribution-folder-property1.png)

1. Passa alla scheda **[!UICONTROL Contributo risorse]**.
1. Immetti **[!UICONTROL Descrizione]** di alto livello della cartella dei contributi.
1. Fai clic su **[!UICONTROL Carica descrizione]** per sfogliare dal computer locale e caricare un **documento fabbisogno risorse**.

   ![](assets/upload.png)

1. Nel campo **[!UICONTROL Aggiungi utente]**, aggiungi gli utenti Brand Portal con cui vuoi condividere la cartella dei contributi. Questi utenti possono accedere e caricare contenuti nella cartella dei contributi tramite l’interfaccia di Brand Portal.
1. Fai clic su **[!UICONTROL Salva]**.

   ![](assets/contribution-folder-property3.png)

>[!NOTE]
>
>I risultati della ricerca si basano sull’elenco di utenti di Brand Portal configurato in Experience Manager Assets. Verifica di disporre dell’elenco aggiornato degli utenti di Brand Portal.

Gli amministratori possono scaricare il file `user.csv` da [!DNL Admin Console] e utilizzarlo come modello di base per l&#39;aggiunta di utenti Brand Portal. Vai a [!UICONTROL Utenti] e fai clic sull&#39;opzione [!UICONTROL Esporta elenco utenti in csv] per scaricare il file `users.csv`. L’elenco di utenti di esempio seguente descrive gli attributi necessari per aggiungere gli utenti. L&#39;unico attributo obbligatorio per una voce utente è `Email` e tutti gli altri attributi sono facoltativi.

[Ottieni file](assets/users.csv)

## Carica risorse nella cartella dei contributi {#uplad-new-assets-to-contribution-folder}

L&#39;utente di Experience Manager Assets carica un set di risorse di base nella cartella **SHARED** per garantire che gli utenti di Brand Portal dispongano delle informazioni necessarie.

**Per caricare le risorse di base:**

1. Accedi all’istanza di Experience Manager Assets.

1. Passa a **[!UICONTROL Assets > File]** e individua la cartella dei contributi.

1. Selezionare la cartella dei contributi e fare clic per aprirla.

1. Fai clic sulla cartella **[!UICONTROL NEW]**.

   ![](assets/upload-new-assets1.png)

1. Fai clic su **[!UICONTROL Crea]** > **[!UICONTROL File]** per caricare singoli file o cartelle (.zip) contenenti più risorse.

   ![](assets/upload-new-assets2.png)

1. Sfoglia e carica le risorse (file o cartelle) nella cartella **[!UICONTROL NEW]**.

   ![](assets/upload-asset4.png)

Dopo aver caricato tutte le risorse o cartelle nella nuova cartella, pubblica la cartella dei contributi in Experience Manager Assets.


## Cartella dei contributi di Publish a Brand Portal {#publish-contribution-folder-to-brand-portal}

Una volta configurata la cartella dei contributi, l’utente di Experience Manager Assets (amministratore/non amministratore) può pubblicarla da Experience Manager Assets a Brand Portal. Gli utenti di Brand Portal che dispongono dell’autorizzazione per accedere alla cartella dei contributi riceveranno una notifica e-mail/impulso al completamento dell’azione di pubblicazione.


**Per pubblicare la cartella dei contributi:**

1. Accedi all’istanza di Experience Manager Assets.

1. Passa a **[!UICONTROL Assets > File]** e individua la cartella dei contributi in cui desideri pubblicare in Brand Portal.
1. Seleziona la cartella dei contributi e fai clic su **[!UICONTROL Publish rapido]** > **[!UICONTROL Publish a Brand Portal]**.

   ![](assets/publish-contribution-folder-to-bp.png)

   Riceverai un messaggio di successo dopo la pubblicazione della cartella dei contributi in Brand Portal.

Viene inviata una notifica e-mail/impulso agli utenti Brand Portal assegnati alla cartella Contributi. Gli utenti di Brand Portal possono accedere alla cartella dei contributi e iniziare a contribuire. Vedi [Caricare risorse nella cartella dei contributi e pubblicarle in Experience Manager Assets](brand-portal-publish-contribution-folder-to-aem-assets.md).
