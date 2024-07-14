---
title: Gestire i diritti digitali delle risorse
seo-title: Manage digital rights of assets
description: La concessione di licenze per le risorse e la fissazione della scadenza per le risorse e i collegamenti condivisi garantiscono l’utilizzo controllato di tali risorse e la loro salvaguardia.
seo-description: Licensing assets and setting expiration for assets and shared links ensure controlled usage of these assets and safeguard them.
uuid: ce30e398-0109-41bf-a4d2-2fcca476f499
contentOwner: bdhar
topic-tags: download-install
products: SG_EXPERIENCEMANAGER/Brand_Portal
content-type: reference
discoiquuid: f77003ba-31fe-4a9e-96c8-dbc4c2eba79e
role: Admin
exl-id: 86c31891-0627-41ca-b571-8dac3a074d55
source-git-commit: d1487434b10b01eaf55f34672267490fd8fd907e
workflow-type: tm+mt
source-wordcount: '901'
ht-degree: 3%

---

# Gestire i diritti digitali delle risorse {#manage-digital-rights-of-assets}

Per proteggere il marchio è fondamentale garantire la sicurezza della distribuzione e dell&#39;utilizzo delle risorse creative e del materiale del marchio. Questo può essere applicato sia all’interno che all’esterno dell’organizzazione associando una data di scadenza (e un’ora) alle risorse approvate pubblicate dall’AEM a Brand Portal, oppure concedendo in licenza tali risorse per un uso condizionale. Inoltre, Brand Portal consente di specificare una data di scadenza per i collegamenti alle risorse condivise da Brand Portal.

Continua a leggere per sapere come vengono protette le risorse su Brand Portal e per comprendere le relative autorizzazioni di utilizzo.

## Scadenza risorsa {#asset-expiration}

La scadenza delle risorse è un modo efficace per controllare l’utilizzo delle risorse approvate su Brand Portal in un’organizzazione. Tutte le risorse pubblicate da AEM Assets in Brand Portal possono avere una data di scadenza, che limita l’utilizzo di tali risorse da parte di diversi ruoli utente.

### Autorizzazioni di utilizzo relative alle risorse scadute {#usage-permissions-expired-assets}

In Brand Portal, gli amministratori possono visualizzare, scaricare e aggiungere risorse scadute alle raccolte. Mentre, gli editor e i visualizzatori possono solo visualizzare e aggiungere risorse scadute alle raccolte.

Gli amministratori possono pubblicare le risorse scadute da AEM Assets a Brand Portal. Tuttavia, le risorse scadute non possono essere condivise tramite input penna da Brand Portal. Se selezioni una risorsa scaduta da una cartella contenente sia risorse scadute che non scadute, l&#39;azione **[!UICONTROL Condividi collegamento]** non è disponibile. Tuttavia, se selezioni una cartella contenente risorse scadute e non scadute, sono disponibili le azioni [!UICONTROL Condividi] e **[!UICONTROL Condividi collegamento]**.

>[!NOTE]
>
>Una cartella può comunque essere condivisa come collegamento, anche se contiene risorse scadute. In questo caso, il collegamento non elenca le risorse scadute e vengono condivise solo le risorse non scadute.

Nella tabella seguente vengono visualizzate le autorizzazioni di utilizzo delle risorse scadute:

|   | **[!UICONTROL Condivisione collegamento]** | **[!UICONTROL Download]** | **[!UICONTROL Proprietà]** | **[!UICONTROL Aggiungi alla raccolta]** | **[!UICONTROL Elimina]** |
|---|---|---|---|---|---|
| **[!UICONTROL Amministratore]** | Non disponibile | Disponibile | Disponibile | Disponibile | Disponibile |
| **[!UICONTROL Editor]** | Non disponibile | Non disponibile | Disponibile | Disponibile | Non disponibile |
| **[!UICONTROL Visualizzatore]** | Non disponibile | Non disponibile | Disponibile | Disponibile | Non disponibile |
| **[!UICONTROL Utente ospite]** | Non disponibile | Non disponibile | Disponibile | Disponibile | Non disponibile |

>[!NOTE]
>
>Se i visualizzatori e gli editor scaricano una cartella contenente risorse scadute e non scadute, vengono scaricate solo le risorse non scadute. Se una cartella contiene solo risorse scadute, viene scaricata una cartella vuota.

### Stato di scadenza delle risorse {#expiration-status-of-assets}

Puoi visualizzare lo stato di scadenza delle risorse nella **[!UICONTROL Vista a schede]**. Un flag rosso sulla scheda indica che la risorsa è scaduta.

![](assets/expired_assets_cardview.png)

>[!NOTE]
>
>Nelle viste a elenco e a colonna non viene visualizzato lo stato di scadenza delle risorse.

## Scadenza collegamento risorsa {#asset-link-expiration}

Durante la condivisione delle risorse tramite collegamenti, gli amministratori e gli editor possono impostare una data e un&#39;ora di scadenza utilizzando il campo **[!UICONTROL Scadenza]** nella finestra di dialogo **[!UICONTROL Condivisione collegamenti]**. La scadenza predefinita del collegamento è di sette giorni dalla data in cui il collegamento viene condiviso.

![](assets/asset-link-sharing.png)

In questo modo, le risorse condivise come collegamenti scadono alla data e all’ora impostate dagli amministratori e dagli editor di Brand Portal e non possono più essere visualizzate e scaricate dopo la data di scadenza. Poiché le risorse condivise tramite i collegamenti possono essere visualizzate anche da utenti esterni che non fanno parte dell’organizzazione, specificando la scadenza puoi assicurarti che le risorse approvate siano protette e non esposte a entità sconosciute oltre un periodo di tempo specificato.

Per ulteriori informazioni sulla condivisione dei collegamenti, consulta [Condividere le risorse come collegamento](../using/brand-portal-link-share.md).

## Assets con licenza {#licensed-assets}

Le risorse concesse in licenza sono soggette all’accettazione di un contratto di licenza prima del download da Brand Portal. Il presente contratto per le risorse concesse in licenza viene stipulato quando si scarica la risorsa direttamente da Brand Portal o tramite un collegamento condiviso. Che siano scadute o meno, le risorse protette da licenza possono essere visualizzate da tutti gli utenti. Tuttavia, il download e l’utilizzo delle risorse concesse in licenza scadute sono limitati. Per informazioni sul comportamento delle risorse con licenza scadute e sulle attività consentite in base ai ruoli utente, consulta [autorizzazioni di utilizzo delle risorse scadute](../using/manage-digital-rights-of-assets.md#usage-permissions-expired-assets).

Alle risorse protette da licenza è allegato [il contratto di licenza](https://experienceleague.adobe.com/docs/experience-manager-65/assets/administer/drm.html), che viene eseguito impostando la proprietà dei metadati della risorsa in [!DNL Experience Manager Assets].

Una risorsa è considerata protetta se contiene una delle seguenti proprietà di metadati (o entrambe):

* `xmpRights:WebStatement`: questa proprietà fa riferimento al percorso della pagina che contiene il contratto di licenza per la risorsa. `xmpRights:WebStatement` deve essere un percorso valido nell&#39;archivio.
* `adobe_dam:restrictions`: il valore di questa proprietà è un HTML non elaborato che specifica il contratto di licenza.


Se scegli di scaricare risorse protette da licenza, verrai reindirizzato alla pagina **[!UICONTROL Gestione copyright]** in base alle proprietà dei metadati.

| `adobe_dam:restrictions` | `xmpRights:WebStatement` | Gestione copyright |
| --- | --- | --- |
| Sì | - | L’interfaccia viene visualizzata in Assets e Brand Portal |
| - | Sì (percorso non valido) | Nessuna interfaccia |
| Sì | Sì (percorso non valido) | Nessuna interfaccia |
| Sì | Sì (percorso valido) | L&#39;interfaccia viene visualizzata in Assets o Brand Portal </br> a seconda che il percorso sia valido per Assets o Brand Portal (o entrambi). |

![](assets/asset-copyright-mgmt.png)

Qui devi selezionare la risorsa da scaricare e accettare il relativo contratto di licenza. Se non si accetta il contratto di licenza, il pulsante **[!UICONTROL Scarica]** non è abilitato.

![](assets/licensed-asset-download-2.png)

Se la selezione contiene più risorse protette, seleziona una risorsa alla volta, accetta il contratto di licenza e procedi al download della risorsa.

## Genera report sulle risorse scadute {#generate-report-about-expired-assets}

Gli amministratori possono generare e scaricare un rapporto in cui sono elencate tutte le risorse scadute entro un intervallo di tempo specifico. Questo rapporto include informazioni dettagliate sulle risorse scadute, ad esempio dimensione, tipo e percorso per specificare la posizione della risorsa nella gerarchia delle risorse, quando è scaduta e quando è stata pubblicata. Le colonne di questo rapporto possono essere personalizzate per visualizzare più dati in base ai requisiti degli utenti.

![](assets/assets-expired.png)

Per ulteriori informazioni sulla funzionalità dei report, fare riferimento a [Operazioni con i report](../using/brand-portal-reports.md#work-with-reports).
