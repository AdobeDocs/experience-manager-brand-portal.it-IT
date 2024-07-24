---
title: Domande frequenti
description: Ottieni informazioni sulle domande frequenti nell’Adobe Experience Manager Assets Brand Portal.
content-type: reference
contentOwner: Vishabh Gupta
topic-tags: frequently-asked-questions
products: SG_EXPERIENCEMANAGER/Brand_Portal
discoiquuid: null
exl-id: 4a8f7fbd-7485-421d-a8db-755324d2dbef
source-git-commit: 60104481e8f0b883fbf2cf25c1562e8376882e54
workflow-type: tm+mt
source-wordcount: '1495'
ht-degree: 0%

---

# Domande frequenti {#frequently-asked-questions}

Le domande frequenti su Brand Portal sono incentrate sulle query e sui problemi che gli utenti finali potrebbero incontrare durante l’utilizzo della versione più recente di Experience Manager Assets Brand Portal 6.4.6 o di versioni precedenti.


## Domande frequenti su Brand Portal 6.4.6 {#faqs-bp646}

**Domanda: l&#39;endpoint OAuth legacy esistente (`https://legacy-oauth.cloud.adobe.io/login`) non funziona. Quale potrebbe essere il motivo?**

**Risposta:** la configurazione OAuth legacy è obsoleta. Aggiorna le istanze di Experience Manager Assets Author al service pack più recente e configuralo tramite Adobe Developer Console. Per ulteriori dettagli, vedere [Configurare Experience Manager Assets con Brand Portal](configure-aem-assets-with-brand-portal.md). Tuttavia, affinché la configurazione OAuth legacy funzioni fino all&#39;aggiornamento, aggiorna l&#39;endpoint OAuth legacy a `https://hypnosisprod.ethos11-prod-or1.ethos.adobe.net/`.

**Domanda: non è possibile pubblicare le risorse della cartella Contributi da Brand Portal a Experience Manager Assets dopo l&#39;aggiornamento a Adobe Developer Console. La mia istanza di authoring è su Experience Manager Assets 6.5.4. Quale potrebbe essere il motivo?**

**Risposta:** Si è verificato un problema noto durante la pubblicazione delle risorse della cartella Contributi in Experience Manager Assets 6.5.4 tramite Adobe Developer Console.

Il problema è risolto in Experience Manager Assets 6.5.5. Puoi aggiornare l&#39;istanza di Experience Manager Assets al service pack più recente e [aggiornare le configurazioni](https://experienceleague.adobe.com/en/docs/experience-manager-65/content/assets/brandportal/configure-aem-assets-with-brand-portal#upgrade-integration-65) in Adobe Developer Console.


**Domanda: non vedo il contenuto della cartella dei contributi pubblicato da Brand Portal in Experience Manager Assets. Quale potrebbe essere il motivo?**

**Risposta:** Contatta l&#39;amministratore di Experience Manager Assets per verificare le configurazioni e assicurarti che il tuo tenant Brand Portal sia configurato con una sola istanza di Experience Manager Assets Author.

Questo problema può verificarsi quando hai configurato un tenant Brand Portal su più istanze di authoring Experience Manager Assets. Ad esempio, l’amministratore configura lo stesso tenant Brand Portal nell’istanza di authoring Experience Manager Assets di un ambiente di staging e produzione. In questo caso, la pubblicazione della risorsa viene attivata in Brand Portal, ma l’istanza di authoring di Experience Manager Assets non riesce a importare la risorsa perché l’agente di replica non riceve il token richiedente.


**Domanda: non è possibile pubblicare risorse da Experience Manager Assets a Brand Portal. Il registro di replica indica che la connessione è scaduta. È presente una correzione rapida?**

**Risposta:** In genere la pubblicazione non riesce e viene restituito un errore di timeout se nella coda di replica sono presenti più richieste in sospeso. Per risolvere questo problema, assicurati che gli agenti di replica siano configurati in modo da evitare il timeout.

Per configurare l’agente di replica, effettua le seguenti operazioni:

1. Accedi all’istanza Autore Experience Manager Assets.
1. Dal pannello **Strumenti**, passa a **[!UICONTROL Distribuzione]** > **[!UICONTROL Replica]**.
1. Nella pagina Replica fare clic su **[!UICONTROL `Agents on author`]**. Puoi visualizzare i quattro agenti di replica per il tenant Brand Portal.
1. Fai clic sull’URL dell’agente di replica per aprire i dettagli dell’agente.
1. Fai clic su **[!UICONTROL Modifica]** per modificare le impostazioni dell&#39;agente di replica.
1. In Impostazioni agente fare clic sulla scheda **[!UICONTROL Esteso]**.
1. Selezionare la casella di controllo **[!UICONTROL Chiudi connessione]**.
1. Ripeti i passaggi da 4 a 7 per configurare tutti e quattro gli agenti di replica.
1. Riavvia il server e verifica la connessione.


## Domande frequenti su Brand Portal 6.4.5 {#faqs-bp645}

**Domanda: qual è la modifica principale nella versione di Brand Portal 6.4.5?**

**Risposta:** Experience Manager Assets Brand Portal 6.4.5 consente agli utenti di caricare contenuto e pubblicare nuovamente la cartella Contributi in Experience Manager Assets direttamente da Brand Portal, senza richiedere i diritti di amministratore. Per ulteriori informazioni, vedere [Asset Sourcing in Brand Portal](brand-portal-asset-sourcing.md).



**Domanda: ho perso l&#39;accesso a risorse, funzionalità o configurazioni esistenti create?**

**Risposta:** tutte le caratteristiche e le configurazioni esistenti rimangono intatte. Gli utenti finali non sono interessati e il contenuto rimane intatto.



**Domanda: quando si passa alla nuova versione di Brand Portal?**

**Risposta:** Brand Portal 6.4.5 è stato rilasciato in produzione a ottobre 2019. La prossima versione di Brand Portal è prevista per marzo 2020.
Per aggiornamenti e modifiche alla versione, l&#39;Adobe consiglia di tenere traccia delle [note sulla versione](brand-portal-release-notes.md) e [novità di Brand Portal](whats-new.md).



**Domanda: sono interessati i miei utenti?**

**Risposta:** la versione di Brand Portal 6.4.5 è disponibile esclusivamente in Brand Portal, quindi non ha alcun impatto sugli utenti finali.



**Domanda: è necessaria un&#39;azione da parte mia in qualità di utente di Brand Portal?**

**Risposta:** la versione di Brand Portal 6.4.5 include una nuova funzionalità denominata Asset Sourcing. L’amministratore deve configurare la funzione Asset Sourcing in Experience Manager Assets per abilitare tale funzione per gli utenti di Brand Portal. Per ulteriori informazioni, consulta [Abilita Asset Sourcing](brand-portal-asset-sourcing.md).



**Domanda: chi può creare una cartella Contributi?**

**Risposta:** qualsiasi utente di Experience Manager Assets che dispone delle autorizzazioni per la creazione di una cartella in Experience Manager Assets può creare una cartella **Contribution**. Per creare una cartella **Contribution**, crea una cartella di tipo **Asset Contribution**.
Questa cartella è condivisa con gli utenti Brand Portal attivi per il contributo.



**Domanda: cosa contiene una cartella Contributi?**

**Risposta:** **La cartella Contribution** contiene due sottocartelle **NEW** e **SHARED**. Inizialmente, la cartella NEW è vuota e la cartella SHARED contiene il contenuto di riferimento (risorse riutilizzabili) per gli utenti di Brand Portal.
Gli utenti di Brand Portal accedono alla cartella **Contribution** e caricano il contenuto nella cartella **NEW**.



**Domanda: posso modificare il nome di una cartella Contributi esistente?**

**Risposta:** **No**, impossibile modificare il nome di una cartella **Contribution** esistente.



**Domanda: qual è il contributo W.r.t per i requisiti delle risorse?**

**Risposta:** Il documento **Brief** nella cartella **Contribution** e il contenuto di riferimento nella cartella **SHARED** consentono agli utenti di Brand Portal di comprendere le esigenze e le aspettative relative ai contributi. Insieme, sono noti come requisiti delle risorse.

**Domanda: posso caricare le risorse in una cartella consentita?**

**Risposta:** Non tutte le cartelle consentite. Un utente di Brand Portal può caricare contenuto solo nella cartella **Contribution** condivisa dall&#39;amministratore di Experience Manager Assets o Brand Portal.



**Domanda: come posso accedere a una cartella Contributi?**

**Risposta:** Puoi accedere a una cartella **Contribution** solo se è stata condivisa con te. Ricevi una notifica e-mail/impulso ogni volta che una cartella Contributi viene condivisa con te. Puoi accedere alla cartella Contributi tramite il collegamento condiviso nell’e-mail. In alternativa, puoi accedere alla tua istanza di Brand Portal e passare all’icona a forma di campanello per le notifiche di accesso alla cartella Contributi.

>[!NOTE]
>
>Se non sei un utente di Brand Portal, chiedi all’amministratore di Experience Manager Assets di crearlo nell’Admin Console. Quindi, aggiungi il tuo profilo al file di configurazione utente nell’elenco degli utenti di Brand Portal.


**Domanda: qual è il formato del file CSV per l&#39;importazione da parte dell&#39;utente?**

**Risposta:** Il formato corrisponde a quello supportato da Admin Console per l&#39;importazione in blocco degli utenti. E-mail, nome e cognome sono obbligatori.



**Domanda: cosa popola l&#39;elenco di utenti (collaboratori Brand Portal) nel menu a discesa degli utenti di Asset Contribution?**

**Risposta:** gli utenti nel menu a discesa sono compilati dal file di configurazione utente di Brand Portal (con estensione csv) caricato in Experience Manager Assets.



**Domanda: dove posso vedere lo stato dei processi di importazione e pubblicazione?**

**Risposta:** In Experience Manager Assets è possibile visualizzare lo stato di un&#39;importazione nella pagina del processo **async**. In Brand Portal puoi visualizzare lo stato di un processo di pubblicazione in **[!UICONTROL Strumenti > Stato contributo risorsa]**.



**Domanda: qual è la frequenza di un processo di importazione eseguito periodicamente in Experience Manager?**

**Risposta:** In Experience Manager Assets, il polling viene eseguito ogni 5 minuti.



**Domanda: esiste una soglia sul numero di volte in cui una cartella può essere pubblicata da Brand Portal a Experience Manager Assets?**

**Risposta:** No, tutte le risorse nella cartella **NEW** vengono pubblicate in Experience Manager Assets indipendentemente dal fatto che siano state pubblicate in precedenza. Ogni volta che una cartella **Contribution** viene pubblicata da Brand Portal a Experience Manager Assets, sostituisce il contenuto della cartella **NEW**.



**Domanda: come caricare nuove risorse in una cartella Contributi?**

**Risposta:** Consulta la documentazione dettagliata per [Caricamento delle risorse nella cartella Contributi](brand-portal-publish-contribution-folder-to-brand-portal.md).



**Domanda: non è possibile visualizzare miniature o anteprime per le risorse caricate nella NUOVA cartella.**

**Risposta:** è progettato in quanto non esiste alcun flusso di lavoro eseguito alla fine di Brand Portal.



**Domanda: cosa succede se una cartella pubblicata da Experience Manager Assets a Brand Portal è in continua evoluzione?**

**Risposta:** In Experience Manager Assets, i registri vengono mantenuti per ogni pubblicazione di una cartella in Brand Portal. Al momento della pubblicazione, tutte le risorse non pubblicate in Brand Portal vengono aggiunte a una coda di replica. Tutte le risorse aggiunte alla cartella dopo l’attivazione del processo di pubblicazione non vengono pubblicate in Brand Portal. Quando un utente di Experience Manager Assets pubblica nuovamente la cartella, in Brand Portal vengono pubblicate solo le risorse non pubblicate in precedenza (presenti nella coda di replica). Questa procedura è valida per tutte le cartelle pubblicate da Experience Manager Assets a Brand Portal e per le cartelle CONDIVISE all’interno di una cartella Contributi.

**Domanda: chi posso contattare per le domande?**

**Risposta:** Contatta il tuo Adobe Account Manager o l&#39;Assistenza clienti.

>[!NOTE]
>
>La pianificazione del rilascio è provvisoria e soggetta a modifiche. Per ottenere la pianificazione aggiornata del rilascio, contatta il tuo Adobe Account Manager o l’Assistenza clienti.


## Accesso e supporto ai prodotti (siti con restrizioni) {#product-access-and-support-restricted-sites}

Questi siti sono disponibili solo per i clienti. Se sei un cliente e vuoi accedervi, contatta il tuo Adobe Account Manager.

<!--
* [](https://daycare.day.com) [Product Access](https://login.marketing.adobe.com)

* [Adobe Customer Support]()
-->
