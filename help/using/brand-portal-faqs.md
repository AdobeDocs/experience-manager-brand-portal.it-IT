---
title: Domande frequenti
seo-title: null
description: Ottieni informazioni approfondite sulle domande frequenti nel portale del marchio Adobe Experience Manager Assets.
seo-description: null
uuid: null
content-type: reference
topic-tags: frequently-asked-questions
products: SG_EXPERIENCEMANAGER/Brand_Portal
discoiquuid: null
translation-type: tm+mt
source-git-commit: 22b327619eb73c0099f903bb7314d2cb2d796bc4

---


# Domande frequenti {#frequently-asked-questions}

Nelle domande frequenti sul Brand Portal gli utenti finali sono interessati alle domande e ai problemi che potrebbero incontrare durante l’utilizzo della versione più recente di AEM Assets Brand Portal 6.4.5 o versioni precedenti.



**Ques. Qual è la modifica principale nella versione 6.4.5 di Brand Portal?**

**Ans.** AEM Assets Brand Portal 6.4.5 è una release che consente agli utenti di Brand Portal di caricare contenuti dall’istanza Brand Portal e di pubblicare nuovamente la cartella Contribution in AEM Assets senza richiedere diritti di amministratore.
Per ulteriori informazioni, consultate [Asset Sourcing in Brand Portal](brand-portal-asset-sourcing.md).



**Ques. Perderò l’accesso a risorse, funzionalità o configurazioni già esistenti?**

**Ans.** Tutte le funzioni e le configurazioni esistenti rimangono intatte. Gli utenti finali non sono interessati e il contenuto rimane intatto.



**Ques. Quando si passa alla nuova versione di Brand Portal?**

**Ans.** Brand Portal 6.4.5 è stato rilasciato in produzione a ottobre 2019. La prossima versione di Brand Portal verrà rilasciata nel 3° trimestre 2020.
Per aggiornamenti e modifiche di versione, si consiglia di tenere traccia delle note [di](brand-portal-release-notes.md) rilascio e delle [novità di Brand Portal](whats-new.md).



**Ques. I miei utenti saranno interessati?**

**Ans.** La versione di Brand Portal 6.4.5 è disponibile esclusivamente all’interno di Brand Portal, pertanto non ha alcun impatto sugli utenti finali.



**Ques. In qualità di utente del Brand Portal, è necessaria un&#39;azione?**

**Ans.** La versione di Brand Portal 6.4.5 include una nuova funzione denominata Asset Sourcing. L’amministratore di AEM deve configurare la funzione di origine delle risorse in Risorse AEM per abilitare la funzione per gli utenti del Brand Portal. Per ulteriori informazioni, consultate [Abilita origine](brand-portal-configure-asset-sourcing.md)risorse.



**Ques. Chi può creare una cartella Contribution?**

**Ans.** Qualsiasi utente AEM che disponga delle autorizzazioni necessarie per creare una nuova cartella in Risorse AEM, può creare una cartella **Contribution** . Per creare una cartella **Contribution** , create una nuova cartella di tipo **Asset Contribution**.
Questa cartella viene condivisa con gli utenti attivi di Brand Portal per ottenere un contributo.



**Ques. Cosa contiene una cartella Contribution?**

**Ans.** La cartella **Contribution** contiene due sottocartelle **NEW** e **SHARED**. Inizialmente, la cartella NEW è vuota e la cartella SHARED contiene il contenuto di riferimento (risorse riutilizzabili) per gli utenti di Brand Portal.
Gli utenti di Brand Portal accedono alla cartella **Contribution** e caricano il contenuto nella cartella **NEW** .



**Ques.  È possibile modificare il nome di una cartella di contributi esistente?**

**Ans.** **No**, non è possibile modificare il nome di una cartella **Contribution** esistente.



**Ques. Che cos&#39;è il requisito patrimoniale con il contributo?**

**Ans.** Il documento **Breve** allegato alla cartella **Contribution** e al contenuto di riferimento (risorse riutilizzabili) caricato nella cartella **SHARED** aiuta l’utente del Brand Portal a comprendere la necessità di contributi e aspettative come collaboratore ed è collettivamente chiamato come requisiti delle risorse.



**Ques. Posso caricare le risorse in una qualsiasi cartella consentita?**

**Ans.** Non tutte le cartelle consentite. Un utente di Brand Portal può caricare contenuto solo nella cartella **Contribution** condivisa dall’amministratore AEM o Brand Portal.



**Ques. Come posso accedere a una cartella Contribution?**

**Ans.** Puoi accedere a una cartella **Contribution** solo se è stata condivisa con te. Riceverai una notifica e-mail/impulso ogni volta che una cartella Contribution viene condivisa con te. Potete accedere alla cartella Contribution tramite il collegamento condiviso nell’e-mail oppure accedere all’istanza Brand Portal e passare all’icona Bell per la notifica e accedere alla cartella Contribution.

>[!NOTE]
>
>Se non siete già utenti di Brand Portal, chiedete all’amministratore AEM di creare l’utente nella console di amministrazione di AEM e di aggiungere il vostro profilo al file di configurazione dell’utente nell’elenco degli utenti di Brand Portal. Fate riferimento a [Aggiunta di utenti](brand-portal-configure-asset-sourcing.md)del portale dei marchi.



**Ques. Qual è il formato del file CSV per l’importazione da parte degli utenti?**

**Ans.** Il formato è uguale a quello supportato da Admin Console per l’importazione in massa di utenti. E-mail, nome e cognome sono obbligatori.



**Ques. Cosa compila l’elenco di utenti (collaboratori di Brand Portal) nel menu a discesa degli utenti Contribution?**

**Ans.** Gli utenti nel menu a discesa vengono popolati dal file di configurazione utente (.csv) del Portale marchio caricato in AEM.



**Ques. Dove è possibile visualizzare lo stato dei processi di importazione e pubblicazione?**

**Ans.** In AEM, potete visualizzare lo stato di un’importazione nella pagina del processo **asincrono** . In Brand Portal, potete visualizzare lo stato di un processo di pubblicazione in **[!UICONTROL Strumenti > Stato]**contributo risorsa.



**Ques. Qual è la frequenza di un processo di importazione che viene eseguito periodicamente in AEM?**

**Ans.** In AEM, il sondaggio viene eseguito ogni 5 minuti.



**Ques. Esiste una riduzione del numero di volte che una cartella può essere pubblicata da Brand Portal a Risorse AEM?**

**Ans.** No, tutte le risorse presenti nella cartella **NEW** vengono pubblicate su AEM Assets indipendentemente dal fatto che siano state pubblicate in precedenza. Ogni volta che una cartella **Contribution** viene pubblicata da Brand Portal a Risorse AEM, sostituisce il contenuto della cartella **NEW** .



**Ques. Come caricare nuove risorse in una cartella Contribution?**

**Ans.** Consultate la documentazione dettagliata per il [caricamento delle risorse nella cartella](brand-portal-upload-assets-to-contribution-folder.md)Contribution.



**Ques. Non vengono visualizzate miniature/anteprime delle risorse caricate nella cartella NEW da un utente di Brand Portal?**

**Ans.** È così come è stato progettato, poiché non è in esecuzione alcun flusso di lavoro alla fine del Portale marchio.



**Ques. Cosa succede se una cartella viene pubblicata da Risorse AEM al Portale del marchio che si trova in piena fase di elaborazione?**

**Ans.** In AEM, i file di registro vengono conservati ogni volta che una cartella viene pubblicata nel Brand Portal. Al momento della pubblicazione, tutte le risorse che non vengono pubblicate in Brand Portal vengono messe in coda di replica. Eventuali risorse aggiunte alla cartella dopo l’attivazione del processo di pubblicazione non vengono pubblicate in Brand Portal. Quando l’utente AEM pubblica nuovamente la cartella, solo le risorse che non erano state pubblicate in precedenza (esistenti nella coda di replica) vengono pubblicate nel Brand Portal.
Ciò vale per qualsiasi cartella pubblicata da Risorse AEM al Portale dei marchi e cartella CONDIVISA all’interno di una cartella Contribution.



**Ques. Chi posso contattare con le domande?**

**Ans.** Contatta il tuo Adobe Account Manager o l&#39;Assistenza clienti.


>[!NOTE]
>
>Il programma di rilascio è provvisorio e soggetto a modifiche. Contatta il tuo Adobe Account Manager o l&#39;Assistenza clienti per ottenere la pianificazione della versione aggiornata.




## Product Access and Support (Restricted Sites) {#product-access-and-support-restricted-sites}

Questi siti sono disponibili solo per i clienti. Se siete un cliente e richiedete l&#39;accesso, contattate il vostro account manager Adobe.

* [](https://daycare.day.com) Accesso [al prodotto](https://login.marketing.adobe.com)

* [Assistenza clienti Adobe](https://helpx.adobe.com/contact.html)