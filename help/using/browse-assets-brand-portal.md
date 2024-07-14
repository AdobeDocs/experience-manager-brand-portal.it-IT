---
title: Sfogliare le risorse in Brand Portal
seo-title: Browse assets on Brand Portal
description: Sfoglia le risorse, sfoglia le gerarchie di risorse e cerca le risorse, utilizzando diverse opzioni di visualizzazione ed elementi dell’interfaccia utente in Brand Portal.
seo-description: Browse through assets, traverse asset hierarchies, and search assets, using different view options and UI elements on Brand Portal.
uuid: 178ce217-0050-4922-a204-f4539d46f539
products: SG_EXPERIENCEMANAGER/Brand_Portal
content-type: reference
topic-tags: introduction
discoiquuid: a70ce694-81d1-4829-9e61-b6412e013e5c
exl-id: 405d7861-a140-44b1-ae1f-4f0839f05033
source-git-commit: a219adc020d63897b10dca83d9ce31fd3ebf847c
workflow-type: tm+mt
source-wordcount: '1006'
ht-degree: 7%

---

# Sfogliare le risorse in Brand Portal {#browsing-assets-on-brand-portal}

Experience Manager Assets Brand Portal fornisce varie funzionalità ed elementi dell’interfaccia utente che facilitano la navigazione tra le risorse, l’attraversamento delle gerarchie di risorse e la ricerca di risorse utilizzando diverse opzioni di visualizzazione.

Il logo di Experience Manager nella barra degli strumenti nella parte superiore facilita l’accesso degli utenti amministratori al pannello strumenti di amministrazione.

![](assets/aemlogo.png)

![](assets/admin-tools-panel-2.png)

![](assets/bp_subheader.png)

Il selettore della barra in alto a sinistra nell’elenco a discesa di Brand Portal mostra le opzioni per navigare nelle gerarchie di risorse, semplificare la ricerca e visualizzare le risorse.

![](assets/siderail-1.png)

Puoi visualizzare, navigare e selezionare le risorse utilizzando una qualsiasi delle viste disponibili (Scheda, Colonna ed Elenco) nel selettore di visualizzazione in alto a destra in Brand Portal.

![](assets/viewselector.png)

## Visualizzazione e selezione delle risorse {#viewing-and-selecting-resources}

La visualizzazione, la navigazione e la selezione di ciascuna vista sono concettualmente le stesse in tutte le viste, ma presentano piccole variazioni nella gestione, a seconda della vista in uso.

Puoi visualizzare, navigare e selezionare (per ulteriori azioni) le risorse in una qualsiasi delle viste disponibili:

* Vista a colonne
* Vista a schede
* Vista a elenco 

### Vista a schede

![](assets/card-view.png)

La vista a schede mostra le schede informative per ogni elemento al livello corrente, Queste schede forniscono i seguenti dettagli:

* Una rappresentazione visiva della risorsa/cartella.
* Tipo
* Titolo
* Nome
* Data e ora in cui la risorsa è stata pubblicata su Brand Portal dall’AEM
* Dimensione
* Dimensioni

Puoi spostarti verso il basso nella gerarchia toccando/facendo clic sulle schede (facendo attenzione a evitare le azioni rapide) oppure verso l&#39;alto utilizzando le [breadcrumb nell&#39;intestazione](https://experienceleague.adobe.com/docs/experience-manager-65/authoring/essentials/basic-handling.html).

![](assets/cardquickactions.png)

#### Vista a schede per utenti non amministratori

Le schede di cartelle, in Vista a schede, visualizzano le informazioni sulla gerarchia delle cartelle per gli utenti non amministratori (editor, visualizzatore e utente ospite). Questa funzionalità consente agli utenti di conoscere la posizione delle cartelle a cui accedono, rispetto alla gerarchia principale.
Le informazioni sulla gerarchia delle cartelle sono particolarmente utili per distinguere le cartelle con nomi simili ad altre cartelle condivise da una gerarchia di cartelle diversa. Se gli utenti non amministratori non sono a conoscenza della struttura delle cartelle delle risorse condivise con loro, le risorse o le cartelle con nomi simili sembrano confuse.

* I percorsi mostrati sulle rispettive schede vengono troncati per adattarsi alle dimensioni delle schede. Tuttavia, gli utenti possono vedere il percorso completo come una descrizione quando passano il mouse sul percorso troncato.

![](assets/folder-hierarchy1.png)

**Opzione Panoramica per visualizzare le proprietà della risorsa**

L’opzione Panoramica è disponibile per gli utenti non amministratori (editor, visualizzatori, utenti ospiti) che possono visualizzare le proprietà delle risorse e cartelle selezionate. L’opzione Panoramica è visibile:

* nella barra degli strumenti in alto, seleziona una risorsa o una cartella.
* nel menu a discesa selezionando la barra Selettore.

Quando si seleziona l&#39;opzione **[!UICONTROL Panoramica]** mentre è selezionata una risorsa o una cartella, gli utenti possono visualizzare il titolo, il percorso e l&#39;ora di creazione della risorsa. Nella pagina dei dettagli della risorsa, invece, l’opzione Panoramica consente agli utenti di visualizzare i metadati della risorsa.

![](assets/overview-option.png)

![](assets/overview-rail-selector.png)

#### Visualizza impostazioni nella vista a schede

Viene visualizzata la finestra di dialogo **[!UICONTROL Visualizza impostazioni]** quando si seleziona **[!UICONTROL Visualizza impostazioni]** dal selettore di visualizzazione. Consente di ridimensionare le miniature delle risorse nella vista a schede. In questo modo, puoi personalizzare la visualizzazione e controllare il numero di miniature visualizzate.

![](assets/cardviewsettings.png)

### Vista a elenco

![](assets/list-view.png)

Nella vista a elenco vengono visualizzate le informazioni per ogni risorsa al livello corrente. La vista a elenco fornisce i seguenti dettagli:

* Miniatura delle risorse
* Nome
* Titolo
* Lingua
* Tipo
* Dimensione
* Dimensione
* Valutazione
* Percorso cartella che mostra la gerarchia delle risorse
* Data di pubblicazione della risorsa su Brand Portal

La colonna Percorso consente di identificare facilmente la posizione della risorsa nella gerarchia delle cartelle. Per spostarti verso il basso nella gerarchia, tocca o fai clic sul nome della risorsa; per tornare verso l&#39;alto utilizza le [breadcrumb nell&#39;intestazione](https://experienceleague.adobe.com/docs/experience-manager-65/authoring/essentials/basic-handling.html).

<!--
Comment Type: draft lastmodifiedby="mgulati" lastmodifieddate="2018-08-17T03:12:05.096-0400" type="annotation">Removed:- "Selecting assets in list view To select all items in the list, use the checkbox at the upper left of the list. When all items in the list are selected, this check box appears checked. To deselect all, click or tap the checkbox. When only some items are selected, it appears with a minus sign. To select all, click or tap the checkbox. To deselect all, click or tap the checkbox again. You can change the order of items using the dotted vertical bar at the far right of each item in the list. Tap/click the vertical selection bar and drag the item to a new position in the list."
 -->

### Visualizza impostazioni nella vista a elenco

La vista a elenco mostra la risorsa **[!UICONTROL Name]** come prima colonna per impostazione predefinita. Vengono inoltre visualizzate informazioni aggiuntive, ad esempio la risorsa **[!UICONTROL Titolo]**, **[!UICONTROL Impostazioni locali]**, **[!UICONTROL Tipo]**, **[!UICONTROL Dimension]**, **[!UICONTROL Dimensioni]**, **[!UICONTROL Valutazione]**, stato di pubblicazione. È tuttavia possibile selezionare le colonne da visualizzare utilizzando **[!UICONTROL Impostazioni visualizzazione]**.

![](assets/list-view-setting.png)

### Vista a colonne

![](assets/column-view.png)

Utilizzare la vista a colonne per spostarsi in una struttura del contenuto attraverso una serie di colonne a catena. Questa vista consente di visualizzare e scorrere la gerarchia delle risorse.

Selezionando una risorsa nella prima colonna (all’estrema sinistra), le risorse figlie vengono visualizzate nella seconda colonna a destra. Selezionando una risorsa nella seconda colonna vengono visualizzate le risorse figlie nella terza colonna a destra e così via.

Per spostarti verso l’alto o il basso nella struttura, tocca o fai clic sul nome della risorsa o sulla freccia a destra del nome della risorsa.

* Il nome della risorsa e la freccia vengono evidenziati quando tocchi o fai clic su tali elementi.
* Toccando o facendo clic sulla miniatura viene selezionata la risorsa.
* Se questa opzione è selezionata, sulla miniatura viene visualizzato un segno di spunta e il nome della risorsa viene evidenziato.
* I dettagli della risorsa selezionata sono visualizzati nella colonna finale.

Quando una risorsa viene selezionata nella vista a colonne, la sua rappresentazione visiva viene visualizzata nella colonna finale insieme ai seguenti dettagli:

* Titolo
* Nome
* Dimensioni
* Data e ora in cui la risorsa è stata pubblicata su Brand Portal dall’AEM
* Dimensione
* Tipo
* Opzione Maggiori dettagli, per passare alla pagina dei dettagli della risorsa

<!--
Comment Type: draft

<h3>Selecting Resources</h3>
-->

<!--
Comment Type: draft

<p>Selecting a specific resource depends on a combination of the view and the device:</p>
-->

<!--
Comment Type: draft

<table border="1" cellpadding="1" cellspacing="0" width="100%">
<tbody>
<tr>
<td> </td>
<td>Select</td>
<td>Deselect</td>
</tr>
<tr>
<td>Column View<br /> </td>
<td>
<ul>
<li>Desktop:<br /> Mouseover, then use the check mark quick action</li>
<li>Mobile device:<br /> Tap the thumbnail</li>
</ul> </td>
<td>
<ul>
<li>Desktop:<br /> Click the thumbnail</li>
<li>Mobile device:<br /> Tap the thumbnail</li>
</ul> </td>
</tr>
<tr>
<td>Card View<br /> </td>
<td>
<ul>
<li>Desktop:<br /> Mouseover, then use the check mark quick action</li>
<li>Mobile device:<br /> Tap-and-hold the card</li>
</ul> </td>
<td>
<ul>
<li>Desktop:<br /> Click the card</li>
<li>Mobile device:<br /> Tap the card</li>
</ul> </td>
</tr>
<tr>
<td>List View</td>
<td>
<ul>
<li>Desktop:<br /> Mouseover, then use the check mark quick action</li>
<li>Mobile device:<br /> Tap the thumbnail</li>
</ul> </td>
<td>
<ul>
<li>Desktop:<br /> Click the thumbnail</li>
<li>Mobile device:<br /> Tap the thumbnail</li>
</ul> </td>
</tr>
</tbody>
</table>
-->

<!--
Comment Type: draft

Deselecting All
-->

<!--
Comment Type: draft

<p>In all cases, as you select items the count of the items selected is displayed at the upper right of the toolbar.</p>
<p>You can deselect all items and exit selection mode by clicking or tapping the X next to the count.</p>
-->

<!--
Comment Type: draft

<p>In all views, all items can be deselected by tapping escape on the keyboard if you are using a desktop device.</p>
-->

## Struttura contenuto {#content-tree}

Oltre a queste visualizzazioni, utilizza la struttura ad albero per espandere la gerarchia delle risorse mentre visualizzi e selezioni le risorse o le cartelle desiderate.

Per aprire la visualizzazione struttura, tocca o fai clic sul selettore della barra in alto a sinistra e seleziona **[!UICONTROL Struttura contenuto]** dal menu.

![](assets/contenttree.png)

Dalla gerarchia dei contenuti, individua la risorsa desiderata.

![](assets/content-tree.png)

## Dettagli risorsa {#asset-details}

La pagina dei dettagli della risorsa consente di visualizzare una risorsa, scaricarla, condividerne il collegamento, spostarla in una raccolta o visualizzarne la pagina delle proprietà. Consente inoltre di spostarsi nella pagina dei dettagli di altre risorse della stessa cartella in successione.

![](assets/asset-detail.png)

Per visualizzare i metadati della risorsa o le varie rappresentazioni, utilizza il selettore della barra nella pagina dei dettagli della risorsa.

![](assets/asset-overview.png)

Puoi visualizzare tutte le rappresentazioni disponibili della risorsa nella pagina dei dettagli della risorsa e selezionare una rappresentazione dal pannello **[!UICONTROL Rappresentazioni]** per visualizzarne l&#39;anteprima.

![](assets/renditions.png)

<!-- removed as it is fixed in 2022.02.0 release
>[!CAUTION]
>
>(**Experience Manager Assets as a Cloud Service** only) The following known issues will be fixed in the upcoming release:
>
>The **[!UICONTROL Renditions]** panel does not list all the static renditions of the assets that are published to Brand Portal after December 16, 2021.
>
>The **[!UICONTROL Renditions]** panel lists the smart crop renditions of the asset, however, the user cannot preview or download the smart crop renditions.
-->

Per aprire la pagina delle proprietà della risorsa, utilizza l&#39;opzione **[!UICONTROL Proprietà (p)]** nella barra superiore.

![](assets/asset-properties.png)

È inoltre possibile visualizzare un elenco di tutte le risorse correlate (risorse di origine o derivate su AEM) nella pagina delle proprietà di una risorsa, in quanto anche la relazione tra risorse viene pubblicata da AEM a Brand Portal.
