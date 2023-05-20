---
title: Risolvere i problemi relativi alla pubblicazione parallela in Brand Portal
seo-title: Troubleshoot issues in parallel publishing to Brand Portal
description: Risoluzione dei problemi relativi alla pubblicazione parallela.
seo-description: Troubleshoot parallel publishing.
uuid: 51e45cca-8c96-4c69-84ef-2ef34f3bcde2
products: SG_EXPERIENCEMANAGER/Brand_Portal
content-type: reference
topic-tags: brand-portal
discoiquuid: a4801024-b509-4c51-afd8-e337417e658b
role: Admin
exl-id: 631beabc-b145-49ba-a8e4-f301497be6da
source-git-commit: 72cd0ebbf05067287d94e1dc4e1b68f5fb6c2888
workflow-type: tm+mt
source-wordcount: '953'
ht-degree: 1%

---

# Risolvere i problemi relativi alla pubblicazione parallela in Brand Portal {#troubleshoot-issues-in-parallel-publishing-to-brand-portal}

Brand Portal è configurato con Experience Manager Assets in modo che le risorse del brand approvate vengano acquisite (o pubblicate) direttamente dall’istanza di authoring di Experience Manager Assets. Una volta [configurato](../using/configure-aem-assets-with-brand-portal.md), Experience Manager Author utilizza un agente di replica per replicare le risorse selezionate in Brand Portal Cloud Service per l’utilizzo approvato dagli utenti di Brand Portal. Per consentire la pubblicazione parallela ad alta velocità, vengono utilizzati più agenti di replica come Experience Manager 6.2 SP1-CFP5, Experience Manager CFP 6.3.0.2 e versioni successive.

>[!NOTE]
>
>L’Adobe consiglia di eseguire l’aggiornamento all’Experience Manager 6.4.1.0 per garantire che Experience Manager Assets Brand Portal sia configurato correttamente con Experience Manager Assets. Una limitazione nell’Experience Manager 6.4 genera un errore durante la configurazione di Experience Manager Assets con Brand Portal e la replica non riesce.

Sulla configurazione del servizio cloud per Brand Portal in **[!UICONTROL /etc/cloudservice]**, tutti gli utenti e i token necessari vengono generati e salvati automaticamente nell’archivio. Viene creata la configurazione del servizio cloud, vengono creati anche gli utenti del servizio necessari per gli agenti di replica e replica per replicare i contenuti. Vengono creati quattro agenti di replica. Quando si pubblicano numerose risorse da Experience Manager a Brand Portal, le risorse vengono messe in coda e distribuite tra gli agenti di replica tramite Round Robin.

Tuttavia, la pubblicazione può non riuscire in modo intermittente a causa di processi sling di grandi dimensioni, aumento della rete e **[!UICONTROL I/O disco]** nell’istanza Autore Experience Manager o ha rallentato le prestazioni dell’istanza Autore Experience Manager. Si consiglia pertanto di verificare la connessione con gli agenti di replica prima di iniziare la pubblicazione.

![](assets/test-connection.png)

## Risolvere i problemi relativi agli errori durante la prima pubblicazione: convalida della configurazione di pubblicazione {#troubleshoot-failures-in-first-time-publishing-validating-your-publish-configuration}

Per convalidare le configurazioni di pubblicazione:

1. Controlla i registri degli errori
1. Verifica se l’agente di replica è stato creato
1. Verifica connessione

**Registri code durante la creazione del Cloud Service**

Controlla i registri di coda. Controlla se l’agente di replica è stato creato o meno. Se la creazione dell’agente di replica non riesce, modifica il servizio cloud apportando modifiche minori al servizio cloud. Convalida e verifica di nuovo se l’agente di replica è stato creato o meno. In caso contrario, modifica nuovamente il servizio.

Se modificando ripetutamente il servizio cloud non è configurato correttamente, segnala un ticket di assistenza diurna.

**Verificare la connessione con gli agenti di replica**

Visualizza registro, se vengono rilevati errori nel registro di replica:

1. Contatta l’Assistenza clienti.

1. Riprova [pulizia](../using/troubleshoot-parallel-publishing.md#clean-up-existing-config) e crea di nuovo la configurazione di pubblicazione.

<!--
Comment Type: remark
Last Modified By: Mini Gulati (mgulati)
Last Modified Date: 2018-06-21T22:56:21.256-0400
<p>?? check and compare public key. At times public key is different</p>
<p>?? another thing to check in /useradmin</p>
-->

## Pulisci configurazioni di pubblicazione Brand Portal esistenti {#clean-up-existing-config}

Nella maggior parte dei casi, quando la pubblicazione non funziona, il motivo può essere che l’utente che esegue la pubblicazione (ad esempio: `mac-<tenantid>-replication` non dispone della chiave privata più recente, pertanto la pubblicazione non riesce con un errore &quot;401 unauthorized&quot; e nei registri dell’agente di replica non viene segnalato alcun altro errore. In alternativa, potrebbe essere utile evitare la risoluzione dei problemi e creare una configurazione. Per il corretto funzionamento della nuova configurazione, ripulisci quanto segue dalla configurazione di Experience Manager Author:

1. Vai a `localhost:4502/crx/de/` (considerando che stai eseguendo l’istanza di authoring su localhost:4502:\
   i. sopprimere `/etc/replication/agents.author/mp_replication`
ii. elimina 
`/etc/cloudservices/mediaportal/<config_name>`

1. Vai a localhost:4502/useradmin:\
   i. cerca utente `mac-<tenantid>replication`
ii. elimina questo utente

Ora il sistema è tutto pulito. Ora è possibile tentare di creare una configurazione del servizio cloud e continuare a utilizzare l’applicazione JWT esistente. Non è necessario creare un’applicazione, ma devi aggiornare la chiave pubblica dalla nuova configurazione cloud creata.

>[!NOTE]
>
>Non modificare le impostazioni generate automaticamente.


## Problema di visibilità del tenant dell’applicazione JWT per Developer Connection {#developer-connection-jwt-application-tenant-visibility-issue}

Se attivato `https://legacy-oauth.cloud.adobe.io/`, vengono elencate tutte le organizzazioni (tenant) per le quali gli utenti correnti detengono l’amministratore di sistema. Se non trovi il nome dell’organizzazione qui o non riesci a creare un’applicazione per un tenant richiesto qui, verifica di disporre di diritti sufficienti (per amministratori di sistema).

Nell’interfaccia utente è presente un problema noto: per ogni tenant sono visibili solo le prime dieci applicazioni. Quando crei l’applicazione, resta su quella pagina e applica un segnalibro all’URL. Non è necessario passare alla pagina dell&#39;elenco dell&#39;applicazione e trovare l&#39;applicazione creata. Puoi premere direttamente questo URL con segnalibro e aggiornare/eliminare l’applicazione quando necessario.

L’applicazione JWT potrebbe non essere elencata correttamente. È consigliabile, pertanto, annotare o inserire nei segnalibri l’URL durante la creazione dell’applicazione JWT.

## La configurazione in esecuzione smette di funzionare {#running-configuration-stops-working}

<!--
Comment Type: draft

<p>If the running configuration stops working, either of the following two possibilities
<g class="gr_ gr_15 gr-alert gr_gramm gr_inline_cards gr_run_anim Grammar multiReplace" data-gr-id="15" id="15" style="font-size: 12px;">
are
</g> there:</p>
<p>1.
<g class="gr_ gr_14 gr-alert gr_gramm gr_inline_cards gr_run_anim Grammar only-ins doubleReplace replaceWithoutSep" data-gr-id="14" id="14">
Connection
</g> has failed, or</p>
<p>2. Publish has failed with permission to dam-replication-service denied, while connection has passed </p>
<p>If the connection has failed [1], the
<g class="gr_ gr_10 gr-alert gr_spell gr_inline_cards gr_run_anim ContextualSpelling ins-del multiReplace" data-gr-id="10" id="10">
fail safe
</g> way to fix it is to <a href="../using/troubleshoot-parallel-publishing.md#main-pars-header-1664955658">clean up</a> the existing Brand Portal publish configuration and recreate a publish configuration. </p>
<p>However, if the
<g class="gr_ gr_18 gr-alert gr_spell gr_inline_cards gr_run_anim ContextualSpelling" data-gr-id="18" id="18">
publish
</g> has failed with
<g class="gr_ gr_16 gr-alert gr_gramm gr_inline_cards gr_run_anim Grammar only-ins doubleReplace replaceWithoutSep" data-gr-id="16" id="16">
permission
</g> denied to dam-replication-service, raise a support ticket.</p>
-->

Se un agente di replica (che stava effettuando la pubblicazione in Brand Portal al limite) interrompe l’elaborazione dei processi di pubblicazione, controlla i registri di replica. Experience Manager incorpora un nuovo tentativo automatico; pertanto, se una particolare risorsa non viene pubblicata correttamente, viene ritentata automaticamente. In caso di problemi intermittenti, ad esempio un errore di rete, l&#39;operazione potrebbe avere esito positivo durante un nuovo tentativo.

Se si verificano continui errori di pubblicazione e la coda è bloccata, seleziona **[!UICONTROL verifica connessione]** e cercare di risolvere gli errori segnalati.

In base agli errori, si consiglia di registrare un ticket di supporto, in modo che il team di progettazione Brand Portal possa aiutarti a risolvere i problemi.

## Token di configurazione IMS Brand Portal scaduto {#token-expired}

Se l’ambiente Brand Portal si arresta bruscamente, è possibile che le configurazioni IMS non funzionino correttamente. Il sistema mostra una configurazione IMS non integra e visualizza un messaggio di errore (simile al seguente) indicante che il token di accesso è scaduto.

`com.adobe.granite.auth.oauth.AccessTokenProvider failed to get access token from authorization server status: 400 response: Unknown macro: {"error"}`

Per risolvere questo problema, si consiglia di salvare e chiudere manualmente la configurazione IMS e di controllare nuovamente lo stato di integrità. Se le configurazioni non funzionano, eliminale e creane una nuova.


## Configurare gli agenti di replica per evitare errori di timeout della connessione {#connection-timeout}

In genere, il processo di pubblicazione non riesce e genera un errore di timeout se nella coda di replica sono presenti più richieste in sospeso. Per risolvere questo problema, assicurati che gli agenti di replica siano configurati in modo da evitare il timeout.

Per configurare gli agenti di replica:

1. Accedi all’istanza Autore di AEM Assets.
1. Dalla sezione **Strumenti** , passa a **[!UICONTROL Distribuzione]** > **[!UICONTROL Replica]**.
1. Nella pagina Replica, fai clic su **[!UICONTROL Agenti per creazione]**. Puoi vedere i quattro agenti di replica del tuo tenant Brand Portal.
1. Fai clic sull’URL dell’agente di replica e fai clic su **[!UICONTROL Modifica]**.
1. In Impostazioni agente , fai clic su **[!UICONTROL Esteso]** scheda.
1. Seleziona la **[!UICONTROL Chiudi connessione]** casella di controllo.
1. Ripeti i passaggi da 4 a 7 per configurare tutti e quattro gli agenti di replica.
1. Riavviare il server.
