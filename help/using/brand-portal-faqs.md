---
title: Domande frequenti
description: Ottieni informazioni approfondite sulle domande frequenti in Adobe Experience Manager Assets Brand Portal.
content-type: reference
contentOwner: Vishabh Gupta
topic-tags: frequently-asked-questions
products: SG_EXPERIENCEMANAGER/Brand_Portal
discoiquuid: null
exl-id: 4a8f7fbd-7485-421d-a8db-755324d2dbef
source-git-commit: 32a67abf466dd3bf635b851b02377ed23591915e
workflow-type: ht
source-wordcount: '1500'
ht-degree: 100%

---

# Domande frequenti {#frequently-asked-questions}

Le domande frequenti su Brand Portal sono incentrate sulle query e sui problemi che gli utenti finali potrebbero riscontrare durante l’utilizzo della versione più recente di Experience Manager Assets Brand Portal 6.4.6 o di versioni precedenti.


## Domande frequenti su Brand Portal 6.4.6 {#faqs-bp646}

**Domanda: l’endpoint OAuth precedente esistente (`https://legacy-oauth.cloud.adobe.io/login`) non funziona. Quale potrebbe essere il motivo?**

**Risposta:** la configurazione OAuth precedente è obsoleta. Aggiorna le istanze di authoring di Experience Manager Assets al Service Pack più recente e configuralo tramite Adobe Developer Console. Per i dettagli, consulta [Configurare Experience Manager Assets con Brand Portal](configure-aem-assets-with-brand-portal.md). Tuttavia, affinché la configurazione OAuth precedente funzioni fino all’aggiornamento, aggiorna l’endpoint OAuth precedente su `https://hypnosisprod.ethos11-prod-or1.ethos.adobe.net/`.

**Domanda: non è possibile pubblicare le risorse della cartella contributi da Brand Portal a Experience Manager Assets dopo l’aggiornamento a Adobe Developer Console. La mia istanza di authoring si trova su Experience Manager Assets 6.5.4. Quale potrebbe essere il motivo?**

**Risposta:** Sì, si è verificato un problema noto durante la pubblicazione delle risorse della cartella contributi in Experience Manager Assets 6.5.4 tramite Adobe Developer Console.

Il problema è risolto in Experience Manager Assets 6.5.5. Puoi aggiornare l’istanza di Experience Manager Assets al Service Pack più recente e [aggiornare le configurazioni](https://experienceleague.adobe.com/it/docs/experience-manager-65/content/assets/brandportal/configure-aem-assets-with-brand-portal#upgrade-integration-65) in Adobe Developer Console.


**Domanda: non è possibile visualizzare il contenuto della cartella contributi pubblicato da Brand Portal in Experience Manager Assets. Quale potrebbe essere il motivo?**

**Risposta:** contatta l’amministratore di Experience Manager Assets per verificare le configurazioni e assicurarti che il tenant di Brand Portal sia configurato con una sola istanza di authoring di Experience Manager Assets.

Questo problema può verificarsi quando hai configurato un tenant di Brand Portal in più istanze di authoring Experience Manager Assets. Ad esempio, l’amministratore configura lo stesso tenant di Brand Portal nell’istanza di authoring Experience Manager Assets in un ambiente di staging e produzione. In questo caso, la pubblicazione della risorsa viene attivata in Brand Portal, ma l’istanza di authoring di Experience Manager Assets non riesce a importarla perché l’agente di replica non riceve il token di richiesta.


**Domanda: non è possibile pubblicare risorse da Experience Manager Assets su Brand Portal. Il registro di replica indica che la connessione è scaduta. È presente una correzione rapida?**

**Risposta:** in genere la pubblicazione non riesce e viene restituito un errore di timeout se nella coda di replica sono presenti più richieste in sospeso. Per risolvere questo problema, assicurati che gli agenti di replica siano configurati in modo da evitare il timeout.

Esegui i passaggi seguenti per configurare l’agente di replica:

1. Accedi all’istanza di authoring di Experience Manager Assets.
1. Dal pannello **Strumenti**, passa a **[!UICONTROL Distribuzione]** > **[!UICONTROL Replica]**.
1. Nella pagina Replica, fai clic su **[!UICONTROL `Agents on author`]**. Puoi visualizzare i quattro agenti di replica per il tenant di Brand Portal.
1. Fai clic sull’URL dell’agente di replica per aprire i dettagli dell’agente.
1. Fai clic su **[!UICONTROL Modifica]** per modificare le impostazioni dell’agente di replica.
1. Nelle impostazioni dell’agente, fai clic sulla scheda **[!UICONTROL Esteso]**.
1. Seleziona la casella di controllo **[!UICONTROL Chiudi connessione]**.
1. Ripeti i passaggi da 4 a 7 per configurare tutti e quattro gli agenti di replica.
1. Riavvia il server e verifica la connessione.


## Domande frequenti su Brand Portal 6.4.5 {#faqs-bp645}

**Domanda: qual è la modifica principale nella versione di Brand Portal 6.4.5?**

**Risposta:** Experience Manager Assets Brand Portal 6.4.5 consente agli utenti di caricare contenuti e pubblicare la cartella Contributi in Experience Manager Assets direttamente da Brand Portal, senza richiedere i diritti di amministratore. Per ulteriori informazioni, consulta [Fornitura di risorse in Brand Portal](brand-portal-asset-sourcing.md).



**Domanda: ho perso l’accesso a risorse, funzioni o configurazioni esistenti che ho creato?**

**Risposta:** tutte le funzioni e le configurazioni esistenti rimangono intatte. Gli utenti finali non sono interessati e il contenuto rimane intatto.



**Domanda: quando potrò passare alla nuova versione di Brand Portal?**

**Risposta:** Brand Portal 6.4.5 è stato rilasciato in produzione a ottobre 2019. La prossima versione di Brand Portal è prevista per marzo 2020.
Per aggiornamenti e modifiche alla versione, Adobe consiglia di tenere traccia delle [note sulla versione](brand-portal-release-notes.md) e delle [novità di Brand Portal](whats-new.md).



**Domanda: sono interessati i miei utenti?**

**Risposta:** la versione di Brand Portal 6.4.5 è disponibile esclusivamente in Brand Portal, quindi non ha alcun impatto sugli utenti finali.



**Domanda: è necessaria un’azione da parte mia in qualità di utente di Brand Portal?**

**Risposta:** la versione di Brand Portal 6.4.5 offre una nuova funzione denominata Fornitura di risorse. L’amministratore deve configurare la funzione Fornitura di risorse in Experience Manager Assets per abilitare tale funzione per gli utenti di Brand Portal. Per ulteriori informazioni, consulta [Abilitare la funzione Fornitura di risorse](brand-portal-asset-sourcing.md).



**Domanda: chi può creare una cartella Contributi?**

**Risposta:** qualsiasi utente di Experience Manager Assets che dispone delle autorizzazioni per la creazione di una cartella in Experience Manager Assets può creare una cartella **Contributi**. Per creare una cartella **Contributi**, crea una cartella di tipo **Contributo risorsa**.
Questa cartella viene condivisa con gli utenti di Brand Portal attivi per il contributo.



**Domanda: cosa contiene una cartella di contributi?**

**Risposta:** la cartella **Contributi** contiene due sottocartelle **NUOVO** e **CONDIVISO**. Inizialmente, la cartella NUOVO è vuota e la cartella CONDIVISO contiene il contenuto di riferimento (risorse riutilizzabili) per gli utenti di Brand Portal.
Gli utenti di Brand Portal accedono alla cartella **Contributi** e caricano il contenuto nella cartella **NUOVO**.



**Domanda: posso modificare il nome di una cartella Contributi esistente?**

**Risposta:** **no**, non puoi modificare il nome di una cartella **Contributi** esistente.



**Domanda: qual è il contributo in merito ai requisiti delle risorse?**

**Risposta:** il documento **Resoconto** nella cartella **Contributi** e il contenuto di riferimento nella cartella **CONDIVISO** consentono agli utenti di Brand Portal di comprendere le esigenze e le aspettative relative al contributo. Insieme, sono noti come requisiti delle risorse.

**Domanda: posso caricare le risorse in una cartella consentita?**

**Risposta:** non in tutte le cartelle consentite. Un utente di Brand Portal può caricare contenuti solo nella cartella **Contributi**, che l’amministratore di Experience Manager Assets o Brand Portal condivide.



**Domanda: come posso accedere a una cartella Contributi?**

**Risposta:** puoi accedere a una cartella **Contributi** solo se è stata condivisa con te. Ricevi una notifica e-mail/pulse ogni volta che una cartella di contributi viene condivisa con te. Puoi accedere alla cartella di contributi tramite il collegamento condiviso nell’e-mail. In alternativa, è possibile accedere all’istanza di Brand Portal e passare all’icona a forma di campanello delle notifiche per accedere alla cartella Contributi.

>[!NOTE]
>
>Se non sei un utente di Brand Portal, richiedi all’amministratore di Experience Manager Assets di crearne uno in Admin Console. Quindi, aggiungi il tuo profilo al file di configurazione utente nell’elenco degli utenti di Brand Portal.


**Domanda: qual è il formato del file CSV per l’importazione dell’utente?**

**Risposta:** il formato corrisponde a quello supportato da Admin Console per l’importazione in blocco degli utenti. E-mail, nome e cognome sono obbligatori.



**Domanda: cosa compila l’elenco degli utenti (collaboratori Brand Portal) nel menu a discesa degli utenti di Contributo risorse?**

**Risposta:** gli utenti nel menu a discesa vengono compilati dal file di configurazione utente di Brand Portal (con estensione .csv) caricato in Experience Manager Assets.



**Domanda: dove posso visualizzare lo stato dei processi di importazione e pubblicazione?**

**Risposta:** in Experience Manager Assets è possibile visualizzare lo stato di un’importazione nella pagina relativa al processo **asincrono**. In Brand Portal puoi visualizzare lo stato di un processo di pubblicazione in **[!UICONTROL Strumenti > Stato contributo risorse]**.



**Domanda: qual è la frequenza di un processo di importazione eseguito periodicamente in Experience Manager?**

**Risposta:** in Experience Manager Assets il polling viene eseguito ogni cinque minuti.



**Domanda: esiste una soglia per il numero di volte in cui una cartella può essere pubblicata da Brand Portal in Experience Manager Assets?**

**Risposta:** no, tutte le risorse nella cartella **NUOVO** vengono pubblicate in Experience Manager Assets indipendentemente dal fatto che siano state pubblicate in precedenza. Ogni volta che una cartella **Contributi** viene pubblicata da Brand Portal su Experience Manager Assets, sostituisce il contenuto della cartella **NUOVO**.



**Domanda: come caricare nuove risorse in una cartella Contributi?**

**Risposta:** consulta la documentazione dettagliata relativa al [Caricamento delle risorse nella cartella Contributi](brand-portal-publish-contribution-folder-to-brand-portal.md).



**Domanda: non è possibile visualizzare miniature o anteprime per le risorse caricate nella cartella NUOVO.**

**Risposta:** è progettato in questo modo in quanto non esiste alcun flusso di lavoro eseguito alla fine di Brand Portal.



**Domanda: cosa succede se da Experience Manager Assets su Brand Portal viene pubblicata una cartella che è in continuo cambiamento?**

**Risposta:** in Experience Manager Assets, i registri vengono mantenuti per ogni pubblicazione di una cartella in Brand Portal. Al momento della pubblicazione, tutte le risorse non pubblicate in Brand Portal vengono aggiunte a una coda di replica. Tutte le risorse aggiunte alla cartella dopo l’attivazione del processo di pubblicazione non vengono pubblicate in Brand Portal. Quando un utente di Experience Manager Assets pubblica nuovamente la cartella, in Brand Portal vengono pubblicate solo le risorse non pubblicate in precedenza (presenti nella coda di replica). Questo processo è valido per tutte le cartelle pubblicate da Experience Manager Assets su Brand Portal e per la cartella CONDIVISO interna alla cartella Contributi.

**Domanda: chi posso contattare per domande?**

**Risposta:** contatta il responsabile dell’account Adobe o l’Assistenza clienti.

>[!NOTE]
>
>La pianificazione del rilascio è provvisoria e soggetta a modifiche. Per ottenere la pianificazione aggiornata del rilascio, contatta il responsabile dell’account Adobe o l’Assistenza clienti.


## Accesso al prodotto e supporto (siti con restrizioni) {#product-access-and-support-restricted-sites}

Questi siti sono disponibili solo per la clientela. Se fai parte della clientela e necessiti dell’accesso, contatta il responsabile dell’account Adobe.

<!--
* [](https://daycare.day.com) [Product Access](https://login.marketing.adobe.com)

* [Adobe Customer Support]()
-->
