---
title: Domande frequenti
seo-title: null
description: Ottieni informazioni sulle domande frequenti nell’Adobe Experience Manager Assets Brand Portal.
seo-description: null
uuid: null
content-type: reference
contentOwner: Vishabh Gupta
topic-tags: frequently-asked-questions
products: SG_EXPERIENCEMANAGER/Brand_Portal
discoiquuid: null
exl-id: 4a8f7fbd-7485-421d-a8db-755324d2dbef
source-git-commit: 4caa4263bd74b51af7504295161c421524e51f0c
workflow-type: tm+mt
source-wordcount: '1529'
ht-degree: 0%

---

# Domande frequenti {#frequently-asked-questions}

Le domande frequenti su Brand Portal sono incentrate sulle query e sui problemi che gli utenti finali potrebbero incontrare durante l’utilizzo della versione più recente di Experience Manager Assets Brand Portal 6.4.6 o di versioni precedenti.


## Domande frequenti su Brand Portal 6.4.6  {#faqs-bp646}

**Ques. L&#39;endpoint OAuth legacy esistente (`https://legacy-oauth.cloud.adobe.io/login`) non funziona. Quale potrebbe essere il motivo?**

**AnsLa configurazione OAuth legacy di** è obsoleta. È necessario aggiornare le istanze di Experience Manager Assets Author al service pack più recente e configurarlo tramite Adobe Developer Console. Per ulteriori dettagli, vedere [Configurare Experience Manager Assets con Brand Portal](configure-aem-assets-with-brand-portal.md). Tuttavia, affinché la configurazione OAuth legacy funzioni fino all&#39;aggiornamento, aggiorna l&#39;endpoint OAuth legacy a `https://hypnosisprod.ethos11-prod-or1.ethos.adobe.net/`.

<!--
**Ques. I have created a collection using the asset link shared by the administrator. But I am unable to create a share link for my collection. Do I need special permissions to do this?**

**Ans.** The functionality is by design, the viewer users are not permitted to share link for collections as they have limited privileges due to which they cannot add users to create a share link. It is a known issue that the share link for collections is currently visible to the viewer users. This issue will be fixed in the upcoming release, the option to share link for the collections will not be available to the viewer users.    
-->

**Ques. Dopo l&#39;aggiornamento a Adobe Developer Console, non è possibile pubblicare le risorse della cartella Contributi da Brand Portal a Experience Manager Assets. La mia istanza di authoring è su Experience Manager Assets 6.5.4. Quale potrebbe essere il motivo?**

**Ans** Sì, si è verificato un problema noto durante la pubblicazione delle risorse della cartella Contributi in Experience Manager Assets 6.5.4 tramite Adobe Developer Console.

Il problema è risolto in Experience Manager Assets 6.5.5. Puoi aggiornare l&#39;istanza di Experience Manager Assets al service pack più recente e [aggiornare le configurazioni](https://experienceleague.adobe.com/docs/experience-manager-65/assets/brandportal/configure-aem-assets-with-brand-portal.html#upgrade-integration-65) in Adobe Developer Console.

<!--
Broken link of download hotfix, comment out this section until we have the latest URL.

For immediate fix on AEM 6.5.4, it is recommended to [download the hotfix](https://www.adobeaemcloud.com/content/marketplace/marketplaceProxy.html?packagePath=/content/companies/public/adobe/packages/cq650/hotfix/cq-6.5.0-hotfix-33041) and install on your AEM author instance.
-->

**Ques. Non viene visualizzato il contenuto della cartella Contributi pubblicato da Brand Portal in Experience Manager Assets. Quale potrebbe essere il motivo?**

**Ans** Contatta l&#39;amministratore di Experience Manager Assets per verificare le configurazioni e assicurarti che il tuo tenant Brand Portal sia configurato con una sola istanza di authoring Experience Manager Assets.

Questo problema può verificarsi quando hai configurato un tenant Brand Portal su più istanze di authoring Experience Manager Assets. Ad esempio, l’amministratore configura lo stesso tenant Brand Portal nell’istanza di authoring Experience Manager Assets dell’ambiente di staging e produzione. In questo caso, i trigger di pubblicazione delle risorse in Brand Portal ma l’istanza di authoring di Experience Manager Assets non ha potuto importare il codice risorsa che l’agente di replica non riceve il token richiedente.


**Ques. Non è possibile pubblicare risorse da Experience Manager Assets a Brand Portal. Il registro di replica indica che la connessione è scaduta. È presente una correzione rapida?**

**Ans** In genere la pubblicazione non riesce e si verifica un errore di timeout se nella coda di replica sono presenti più richieste in sospeso. Per risolvere questo problema, assicurati che gli agenti di replica siano configurati in modo da evitare il timeout.

Per configurare l’agente di replica, effettua le seguenti operazioni:

1. Accedi all’istanza Autore Experience Manager Assets.
1. Dal pannello **Strumenti**, passa a **[!UICONTROL Distribuzione]** > **[!UICONTROL Replica]**.
1. Nella pagina Replica fare clic su **[!UICONTROL Agenti sull&#39;autore]**. Puoi visualizzare i quattro agenti di replica per il tenant Brand Portal.
1. Fai clic sull’URL dell’agente di replica per aprire i dettagli dell’agente.
1. Fai clic su **[!UICONTROL Modifica]** per modificare le impostazioni dell&#39;agente di replica.
1. In Impostazioni agente fare clic sulla scheda **[!UICONTROL Esteso]**.
1. Selezionare la casella di controllo **[!UICONTROL Chiudi connessione]**.
1. Ripeti i passaggi da 4 a 7 per configurare tutti e quattro gli agenti di replica.
1. Riavvia il server e verifica la connessione.


## Domande frequenti su Brand Portal 6.4.5  {#faqs-bp645}

**Ques. Qual è la modifica principale nella versione di Brand Portal 6.4.5?**

**Ans** Experience Manager Assets Brand Portal 6.4.5 è una versione di funzionalità che consente agli utenti di Brand Portal di caricare contenuto dall&#39;istanza di Brand Portal e pubblicare nuovamente la cartella Contributi in Experience Manager Assets senza dover disporre dei diritti di amministratore.
Per ulteriori informazioni, vedere [Asset Sourcing in Brand Portal](brand-portal-asset-sourcing.md).



**Ques. Perderò l&#39;accesso alle risorse, alle funzionalità o alle configurazioni create?**

**Ans** Tutte le funzioni e le configurazioni esistenti rimangono intatte. Gli utenti finali non sono interessati e il contenuto rimane intatto.



**Ques. Quando si passa alla nuova versione di Brand Portal?**

**Ans** Brand Portal 6.4.5 è stato rilasciato in produzione a ottobre 2019. La prossima versione di Brand Portal dovrebbe essere rilasciata nel terzo trimestre del 2020.
Per aggiornamenti e modifiche alla versione, si consiglia di tenere traccia delle [note sulla versione](brand-portal-release-notes.md) e [novità di Brand Portal](whats-new.md).



**Ques. Saranno interessati i miei utenti?**

**Ans** La versione di Brand Portal 6.4.5 è disponibile esclusivamente in Brand Portal, quindi non vi è alcun impatto per gli utenti finali.



**Ques. È necessaria un&#39;azione da parte mia in qualità di utente di Brand Portal?**

**Ans** Brand Portal versione 6.4.5 viene fornito con una nuova funzionalità denominata Asset Sourcing. L’amministratore deve configurare la funzione Asset Sourcing in Experience Manager Assets per abilitare tale funzione per gli utenti di Brand Portal. Per ulteriori informazioni, consulta [Abilita Asset Sourcing](brand-portal-asset-sourcing.md).



**Ques. Chi può creare una cartella Contributi?**

**Ans** Qualsiasi utente di Experience Manager Assets con le autorizzazioni per la creazione di una nuova cartella in Experience Manager Assets può creare una cartella **Contribution**. Per creare una cartella **Contribution**, crea una nuova cartella di tipo **Asset Contribution**.
Questa cartella è condivisa con gli utenti Brand Portal attivi per il contributo.



**Ques. Cosa contiene una cartella Contributi?**

**AnsLa cartella** **Contribution** contiene due sottocartelle **NEW** e **SHARED**. Inizialmente, la cartella NEW è vuota e la cartella SHARED contiene il contenuto di riferimento (risorse riutilizzabili) per gli utenti di Brand Portal.
Gli utenti di Brand Portal accedono alla cartella **Contribution** e caricano il contenuto nella cartella **NEW**.



**Ques.  È possibile modificare il nome di una cartella Contributi esistente?**

**Ans** **No**, impossibile modificare il nome di una cartella **Contribution** esistente.



**Ques. Cos&#39;è il contributo w.r.t per i requisiti delle risorse?**

**Ans** Il documento **Brief** allegato alla cartella **Contribution** e il contenuto di riferimento (risorse riutilizzabili) caricato nella cartella **SHARED** consentono all&#39;utente di Brand Portal di comprendere la necessità di contributi e aspettative come collaboratore e viene collettivamente chiamato come requisito della risorsa.



**Ques. Posso caricare risorse in una cartella consentita?**

**Ans** Non tutte le cartelle consentite. Un utente di Brand Portal può caricare contenuto solo nella cartella **Contribution** condivisa dall&#39;amministratore di Experience Manager Assets o Brand Portal.



**Ques. Come si accede a una cartella Contributi?**

**Ans** Puoi accedere a una cartella **Contribution** solo se è stata condivisa con te. Riceverai una notifica e-mail/impulso ogni volta che una cartella Contributi viene condivisa con te. Puoi accedere alla cartella Contributi tramite il collegamento condiviso nell’e-mail oppure alla tua istanza di Brand Portal e passare all’icona a forma di campanello per la notifica di accesso alla cartella Contributi.

>[!NOTE]
>
>Se non sei un utente Brand Portal esistente, richiedi all’amministratore di Experience Manager Assets di creare l’utente in Admin Console e di aggiungere il tuo profilo al file di configurazione utente nell’elenco Utenti di Brand Portal.

**Ques. Qual è il formato del file CSV per l&#39;importazione da parte dell&#39;utente?**

**Ans** Il formato è uguale a quello supportato da Admin Console per l&#39;importazione di utenti in blocco. E-mail, nome e cognome sono obbligatori.



**Ques. Cosa popola l&#39;elenco di utenti (collaboratori Brand Portal) nel menu a discesa degli utenti di Asset Contribution?**

**Ans** Gli utenti nel menu a discesa sono compilati dal file di configurazione utente di Brand Portal (con estensione csv) caricato in Experience Manager Assets.



**Ques. Dove posso vedere lo stato dei processi di importazione e pubblicazione?**

**Ans** In Experience Manager Assets è possibile visualizzare lo stato di un&#39;importazione nella pagina del processo **async**. In Brand Portal puoi visualizzare lo stato di un processo di pubblicazione in **[!UICONTROL Strumenti > Stato contributo risorsa]**.



**Ques. Qual è la frequenza di un processo di importazione eseguito periodicamente in Experience Manager?**

**Ans** In Experience Manager Assets, il polling viene eseguito ogni 5 minuti.



**Ques. Esiste un limite al numero di volte in cui una cartella può essere pubblicata da Brand Portal a Experience Manager Assets?**

**Ans** No, tutte le risorse nella cartella **NEW** vengono pubblicate in Experience Manager Assets indipendentemente dal fatto che siano state pubblicate in precedenza. Ogni volta che una cartella **Contribution** viene pubblicata da Brand Portal a Experience Manager Assets, sostituisce il contenuto della cartella **NEW**.



**Ques. Come si caricano le nuove risorse in una cartella Contributi?**

**Ans** Consulta la documentazione dettagliata per [Caricamento delle risorse nella cartella Contributi](brand-portal-publish-contribution-folder-to-brand-portal.md).



**Ques. Non visualizzo miniature/anteprime sulle risorse caricate nella NUOVA cartella da un utente di Brand Portal?**

**Ans** È progettato in modo che non sia in esecuzione alcun flusso di lavoro alla fine di Brand Portal.



**Ques. Cosa succede se una cartella pubblicata da Experience Manager Assets a Brand Portal è in continua evoluzione?**

**Ans** In Experience Manager Assets, i registri vengono mantenuti per ogni pubblicazione di una cartella in Brand Portal. Al momento della pubblicazione, tutte le risorse non pubblicate in Brand Portal vengono inserite in una coda di replica. Tutte le risorse aggiunte alla cartella dopo l’attivazione del processo di pubblicazione non vengono pubblicate in Brand Portal. Quando l’utente di Experience Manager Assets pubblica nuovamente la cartella, in Brand Portal vengono pubblicate solo le risorse non pubblicate in precedenza (esistenti nella coda di replica).
Ciò vale per tutte le cartelle pubblicate da Experience Manager Assets a Brand Portal e per le cartelle CONDIVISE all’interno di una cartella Contributi.

**Ques. Chi devo contattare per le domande?**

**Ans** Contatta il tuo Adobe Account Manager o l&#39;Assistenza clienti.

>[!NOTE]
>
>La pianificazione del rilascio è provvisoria e soggetta a modifiche. Per ottenere la pianificazione aggiornata del rilascio, contatta il tuo Adobe Account Manager o l’Assistenza clienti.


## Accesso e supporto ai prodotti (siti con restrizioni) {#product-access-and-support-restricted-sites}

Questi siti sono disponibili solo per i clienti. Se sei un cliente e vuoi accedervi, contatta il tuo account manager Adobe.

<!--
* [](https://daycare.day.com) [Product Access](https://login.marketing.adobe.com)

* [Adobe Customer Support]()
-->
