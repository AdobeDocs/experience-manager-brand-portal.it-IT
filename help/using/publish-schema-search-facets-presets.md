---
title: Predefiniti, schemi e facet di Publish per Brand Portal
seo-title: Publish presets, schema, and facets to Brand Portal
description: Scopri come pubblicare predefiniti, schemi e facet in Brand Portal.
seo-description: Learn how to publish presets, schema, and facets to Brand Portal.
uuid: c836d9bb-074a-4113-9c91-b2bf7658b88d
topic-tags: publish
products: SG_EXPERIENCEMANAGER/Brand_Portal
content-type: reference
discoiquuid: bc305abc-9373-4d33-9179-0a5f3904b352
exl-id: 9b585606-6538-459b-87a9-2e68df0087b3
source-git-commit: 133ea1fc342e4460e7d0661205c7411a509143eb
workflow-type: tm+mt
source-wordcount: '1133'
ht-degree: 0%

---

# Predefiniti, schemi e facet di Publish per Brand Portal {#publish-presets-schema-and-facets-to-brand-portal}

L’articolo si occupa della pubblicazione di predefiniti immagine, schemi di metadati e facet di ricerca personalizzata dall’istanza Autore AEM a Brand Portal. La funzionalità di pubblicazione consente alle organizzazioni di riutilizzare i predefiniti per immagini, gli schemi di metadati e i facet di ricerca creati/modificati nell’istanza di authoring dell’AEM, riducendo in tal modo le attività di duplicazione.

>[!NOTE]
>
>La funzionalità per pubblicare i predefiniti immagine, lo schema metadati e i facet di ricerca dall’istanza di creazione dell’AEM a Brand Portal è disponibile da AEM 6.2 SP1-CFP7 e AEM 6.3 SP 1-CFP 1 (6.3.1.1) in poi.

## Predefiniti immagine Publish per Brand Portal {#publish-image-presets-to-brand-portal}

I predefiniti per immagini sono un set di comandi di ridimensionamento e formattazione applicati all’immagine al momento della consegna. I predefiniti per immagini possono essere creati e modificati in Brand Portal. In alternativa, se l’istanza di authoring dell’AEM è in esecuzione in modalità Dynamic Media, gli utenti possono creare predefiniti in corrispondenza dell’istanza di authoring dell’AEM e pubblicarli in AEM Assets Brand Portal, evitando di ricreare gli stessi predefiniti in Brand Portal.\
Una volta creato, il predefinito viene elencato come rappresentazione dinamica nella barra delle rappresentazioni dei dettagli delle risorse e nella finestra di dialogo per il download.

>[!NOTE]
>
>Se l&#39;istanza Autore AEM non è in esecuzione in **[!UICONTROL Modalità Dynamic Medie]** (il cliente non ha acquistato Dynamic Medie), la rappresentazione **[!UICONTROL Pyramid TIFF]** delle risorse non viene creata al momento del caricamento. I predefiniti immagine o le rappresentazioni dinamiche funzionano su **[!UICONTROL Pyramid TIFF]** di una risorsa, quindi se **[!UICONTROL Pyramid TIFF]** non è disponibile nell&#39;istanza AEM Author, non sarà disponibile anche su Brand Portal. Di conseguenza, nella barra delle rappresentazioni della pagina dei dettagli delle risorse e nella finestra di dialogo per il download non sono presenti rappresentazioni dinamiche.

Per pubblicare i predefiniti immagine in Brand Portal:

1. Nell&#39;istanza Autore AEM, tocca o fai clic sul logo AEM per accedere alla console di navigazione globale, quindi tocca o fai clic sull&#39;icona Strumenti e passa a **[!UICONTROL Assets > Predefiniti immagine]**.
1. Seleziona il predefinito immagine o più predefiniti immagine dall&#39;elenco dei predefiniti immagine e tocca o fai clic su **[!UICONTROL Publish in Brand Portal]**.

![](assets/publishpreset.png)

>[!NOTE]
>
>Quando gli utenti fanno clic su **[!UICONTROL Publish in Brand Portal]**, i predefiniti immagine sono in coda per la pubblicazione. Si consiglia agli utenti di monitorare il registro degli agenti di replica per verificare se la pubblicazione è stata eseguita correttamente.

Per annullare la pubblicazione di un predefinito immagine da Brand Portal:

1. Nell&#39;istanza Autore AEM, tocca o fai clic sul logo AEM per accedere alla console di navigazione globale, fai clic sull&#39;icona **[!UICONTROL Strumenti]** e passa a **[!UICONTROL Assets > Predefiniti immagine]**.
1. Selezionare un predefinito immagine e selezionare **[!UICONTROL Rimuovi da Brand Portal]** tra le opzioni disponibili nella parte superiore.

## Schema metadati Publish in Brand Portal  {#publish-metadata-schema-to-brand-portal}

Lo schema metadati descrive il layout e le proprietà visualizzati nella pagina delle proprietà di risorse/raccolte.

![](assets/metadata-schema-editor.png) ![](assets/asset-properties-1.png)

Se gli utenti hanno modificato lo schema predefinito sull’istanza di AEM Author e sono disposti a utilizzare lo stesso schema come schema predefinito in Brand Portal, possono semplicemente pubblicare i moduli schema metadati in Brand Portal. In questo caso, lo schema predefinito in Brand Portal viene sovrascritto dagli schemi predefiniti pubblicati dall’istanza Autore AEM.

Se nell’istanza Autore AEM è stato creato uno schema personalizzato, gli utenti possono pubblicarlo in Brand Portal anziché ricrearlo. Gli utenti possono quindi applicare questo schema personalizzato a qualsiasi cartella/raccolta in Brand Portal.

>[!NOTE]
>
>Gli schemi predefiniti non possono essere pubblicati in Brand Portal se sono bloccati nell’istanza AEM (ossia se non sono modificati).

![](assets/default-schema-form.png)

>[!NOTE]
>
>Se a una cartella è applicato uno schema nell’istanza di authoring dell’AEM, lo stesso schema deve esistere anche in Brand Portal per mantenere la coerenza nella pagina delle proprietà delle risorse in AEM Author e Brand Portal.

Per pubblicare uno schema di metadati dall’istanza di authoring AEM a Brand Portal:

1. Nell&#39;istanza Autore AEM, tocca o fai clic sul logo AEM per accedere alla console di navigazione globale, quindi fai clic sull&#39;icona Strumenti e passa a **[!UICONTROL Assets > Schemi di metadati]**.
1. Selezionare uno schema metadati e selezionare **[!UICONTROL Publish in Brand Portal]** tra le opzioni disponibili nella parte superiore.

>[!NOTE]
>
>Quando gli utenti fanno clic su **[!UICONTROL Publish in Brand Portal]**, gli schemi di metadati vengono messi in coda per la pubblicazione. Si consiglia agli utenti di monitorare il registro degli agenti di replica per verificare se la pubblicazione è stata eseguita correttamente.

Per annullare la pubblicazione di uno schema di metadati da Brand Portal:

1. Nell&#39;istanza Autore AEM, tocca o fai clic sul logo AEM per accedere alla console di navigazione globale, quindi fai clic sull&#39;icona Strumenti e passa a **[!UICONTROL Assets > Schemi di metadati]**.
1. Selezionare uno schema metadati e selezionare **[!UICONTROL Rimuovi da Brand Portal]** tra le opzioni disponibili nella parte superiore.

## Facet di ricerca Publish in Brand Portal {#publish-search-facets-to-brand-portal}

I moduli di ricerca forniscono agli utenti di Brand Portal la funzionalità di [ricerca sfaccettata](../using/brand-portal-search-facets.md). I facet di ricerca conferiscono maggiore granularità alle ricerche su Brand Portal. Tutti i [predicati aggiunti](https://experienceleague.adobe.com/docs/experience-manager-65/assets/administer/search-facets.html) nel modulo di ricerca sono disponibili come facet di ricerca nei filtri di ricerca.

![](assets/property-predicate-removed.png)
![](assets/search-form.png)

Se si desidera utilizzare il modulo di ricerca personalizzato **[!UICONTROL Barra di ricerca amministrazione Assets]** dall&#39;istanza Autore AEM, invece di ricreare lo stesso modulo su Brand Portal è possibile pubblicare il modulo di ricerca personalizzato dall&#39;istanza Autore AEM a Brand Portal.

>[!NOTE]
>
>Il modulo di ricerca bloccato **[!UICONTROL Barra di ricerca amministrazione Assets]** su AEM Assets non può essere pubblicato in Brand Portal se non modificato. Dopo essere stato modificato e pubblicato in Brand Portal, questo modulo di ricerca ha la precedenza su quello in Brand Portal.

Per pubblicare il facet di ricerca modificato dall’istanza di creazione AEM in Brand Portal:

1. Fare clic sul logo dell&#39;AEM, quindi passare a **[!UICONTROL Strumenti > Generale > Cerca in Forms]**.
1. Selezionare il modulo di ricerca modificato e selezionare **[!UICONTROL Da Publish a Brand Portal]**.

   >[!NOTE]
   >
   >Quando gli utenti fanno clic su **[!UICONTROL Publish in Brand Portal]**, i facet di ricerca vengono messi in coda per la pubblicazione. Si consiglia agli utenti di monitorare il registro degli agenti di replica per verificare se la pubblicazione è stata eseguita correttamente.

Per annullare la pubblicazione dei moduli di ricerca da Brand Portal:

1. Nell&#39;istanza Autore AEM, tocca o fai clic sul logo AEM per accedere alla console di navigazione globale, quindi fai clic sull&#39;icona Strumenti e passa a **[!UICONTROL Generale > Cerca in Forms]**.
1. Selezionare il modulo di ricerca e selezionare **[!UICONTROL Rimuovi da Brand Portal]** tra le opzioni disponibili nella parte superiore.

>[!NOTE]
>
>L&#39;azione **[!UICONTROL Annulla pubblicazione da Brand Portal]** lascia il modulo di ricerca predefinito su Brand Portal e non ripristina l&#39;ultimo modulo di ricerca utilizzato prima della pubblicazione.

### Limitazioni {#limitations}

1. Pochi predicati di ricerca non sono applicabili ai filtri di ricerca sul Brand Portal. Quando questi predicati di ricerca vengono pubblicati come parte del modulo di ricerca dall’istanza di authoring AEM a Brand Portal, vengono filtrati. Gli utenti, pertanto, visualizzano meno predicati nel modulo pubblicato in Brand Portal. Vedi [predicati di ricerca applicabili ai filtri in Brand Portal](../using/brand-portal-search-facets.md#list-of-search-predicates).

1. Per il predicato [!UICONTROL Options], se un utente utilizza un percorso personalizzato per leggere le opzioni nell&#39;istanza di creazione dell&#39;AEM, non funzionerà in Brand Portal. Questi percorsi e opzioni aggiuntivi non vengono pubblicati in Brand Portal con il modulo di ricerca. In questo caso, gli utenti possono selezionare l&#39;opzione **[!UICONTROL Manuale]** in **[!UICONTROL Aggiungi opzioni]** all&#39;interno di **[!UICONTROL Predicato opzioni]** per aggiungere queste opzioni manualmente in Brand Portal.

![](assets/options-predicate-manual.png)
