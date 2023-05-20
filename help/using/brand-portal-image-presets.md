---
title: Applicare predefiniti immagine o rappresentazioni dinamiche
seo-title: Apply image presets or dynamic renditions
description: Analogamente a una macro, un predefinito immagine è un insieme predefinito di comandi di ridimensionamento e formattazione salvati con un nome. I predefiniti per immagini consentono a Experience Manager Assets Brand Portal di distribuire dinamicamente immagini di dimensioni, formati e proprietà diversi.
seo-description: Like a macro, an image preset is a predefined collection of sizing and formatting commands saved under a name. Image presets enable Experience Manager Assets Brand Portal to dynamically deliver images of different sizes, formats, and properties.
uuid: a3c8705c-5fbd-472c-8b61-f65b3e552c1b
content-type: reference
topic-tags: administration
products: SG_EXPERIENCEMANAGER/Brand_Portal
discoiquuid: a512dfa0-fef3-4c3f-a389-a0a3a7415bac
role: Admin
exl-id: 212a1b3a-686f-4250-be06-b679b6039887
source-git-commit: 955cd8afe939ff47e9f08f312505e230e2f38495
workflow-type: tm+mt
source-wordcount: '814'
ht-degree: 3%

---

# Applicare predefiniti immagine o rappresentazioni dinamiche {#apply-image-presets-or-dynamic-renditions}

Analogamente a una macro, un predefinito immagine è un insieme predefinito di comandi di ridimensionamento e formattazione salvati con un nome. I predefiniti per immagini consentono a Experience Manager Assets Brand Portal di distribuire dinamicamente immagini di dimensioni, formati e proprietà diversi.

Un predefinito per immagini viene utilizzato per generare rappresentazioni dinamiche di immagini che possono essere visualizzate in anteprima e scaricate. Quando visualizzi l’anteprima delle immagini e delle relative rappresentazioni, puoi scegliere un predefinito per riformattare le immagini in base alle specifiche impostate dall’amministratore.

(*Se l’istanza di authoring di Experience Manager Assets è in esecuzione su **Modalità Dynamic Media Hybrid***) Per visualizzare le rappresentazioni dinamiche di una risorsa in Brand Portal, accertati che la relativa rappresentazione TIFF piramidale sia presente nell’istanza di authoring di Experience Manager Assets da dove pubblichi in Brand Portal. Quando pubblichi la risorsa, anche la relativa rappresentazione PTIFF viene pubblicata in Brand Portal.

>[!NOTE]
>
>Quando si scaricano le immagini e le relative rappresentazioni, non è possibile scegliere tra i predefiniti esistenti. È invece possibile specificare le proprietà di un predefinito immagine personalizzato. Per ulteriori informazioni, consulta [Applicare predefiniti immagine durante il download di immagini](../using/brand-portal-image-presets.md#main-pars-text-1403412644).


Per ulteriori informazioni sui parametri necessari per la creazione dei predefiniti immagine, consultate [Gestione dei predefiniti per le immagini](../using/brand-portal-image-presets.md).

## Creare un predefinito immagine {#create-an-image-preset}

Gli amministratori di Experience Manager Assets possono creare predefiniti per immagini da visualizzare come rappresentazioni dinamiche nella pagina dei dettagli della risorsa. Potete creare un predefinito immagine da zero o salvarne uno esistente con un nuovo nome. Quando crei un predefinito immagine, scegli una dimensione per la consegna delle immagini e i comandi di formattazione. Quando un’immagine viene distribuita per la visualizzazione, il suo aspetto viene ottimizzato in base ai comandi scelti.

>[!NOTE]
>
>Le rappresentazioni dinamiche di un’immagine vengono create utilizzando il relativo Pyramid TIFF. Se Pyramid TIFF non è disponibile per alcuna risorsa, non è possibile recuperare le relative rappresentazioni dinamiche in Brand Portal.
>
>Se l’istanza di authoring di Experience Manager Assets è in esecuzione su **Modalità Dynamic Media Hybrid**, quindi le rappresentazioni piramidali TIFF delle risorse immagine vengono create e salvate nell’archivio Experience Manager Assets.
>
>Mentre, se l’istanza di authoring di Experience Manager Assets è in esecuzione su **Modalità Dynamic Media Scene 7** Quindi esistono rappresentazioni piramidali TIFF delle risorse di immagini nel server Scene 7.
>
>Quando tali risorse vengono pubblicate in Brand Portal, vengono applicati i predefiniti immagine e vengono visualizzate le rappresentazioni dinamiche.


1. Dalla barra degli strumenti nella parte superiore, fai clic sul logo dell’Experience Manager per accedere agli strumenti di amministrazione.

1. Nel pannello Strumenti di amministrazione, fate clic su **[!UICONTROL Predefiniti immagine]**.

   ![](assets/admin-tools-panel-4.png)

1. Nella pagina dei predefiniti immagine, fai clic su **[!UICONTROL Crea]**.

   ![](assets/image_preset_homepage.png)

1. In **[!UICONTROL Modifica predefinito immagine]** , immettere i valori nella **[!UICONTROL Base]** e **[!UICONTROL Avanzate]** schede appropriate, compreso un nome. I predefiniti vengono visualizzati nel riquadro a sinistra e possono essere usati all’istante con altre risorse.

   ![](assets/image_preset_create.png)

   >[!NOTE]
   >
   >È inoltre possibile utilizzare **[!UICONTROL Modifica predefinito immagine]** per modificare le proprietà di un predefinito immagine esistente. Per modificare un predefinito immagine, selezionalo dalla pagina dei predefiniti immagine e fai clic su **[!UICONTROL Modifica]**.

1. Fai clic su **[!UICONTROL Salva]**. Il predefinito immagine viene creato e visualizzato nella pagina dei predefiniti immagine.
1. Per eliminare un predefinito immagine, selezionalo dalla pagina dei predefiniti immagine e fai clic su **[!UICONTROL Elimina]**. Nella pagina di conferma, fai clic su **[!UICONTROL Elimina]** per confermare l’eliminazione. Il predefinito immagine viene rimosso dalla pagina dei predefiniti immagine.

## Applicare predefiniti immagine durante l&#39;anteprima delle immagini  {#apply-image-presets-when-previewing-images}

Quando visualizzate l&#39;anteprima delle immagini e delle relative rappresentazioni, scegliete uno dei predefiniti esistenti per riformattare le immagini in base alle specifiche impostate dall&#39;amministratore.

1. Dall’interfaccia di Brand Portal, fai clic su un’immagine per aprirla.
1. Fai clic sull’icona della sovrapposizione a sinistra, quindi scegli **[!UICONTROL Rappresentazioni]**.

   ![](assets/image-preset-previewrenditions.png)

1. Dalla sezione **[!UICONTROL Rappresentazioni]** selezionare la rappresentazione dinamica appropriata, ad esempio **[!UICONTROL Miniatura]**. Il rendering dell’immagine di anteprima viene eseguito in base alla scelta della rappresentazione.

   ![](assets/image-preset-previewrenditionthumbnail.png)

## Applicare predefiniti immagine durante il download di immagini {#apply-image-presets-when-downloading-images}

Quando scarichi le immagini e le relative rappresentazioni da Brand Portal, non puoi scegliere tra i predefiniti immagine esistenti. Tuttavia, potete personalizzare le proprietà dei predefiniti immagine in base alle quali desiderate riformattare le immagini.

1. Dall’interfaccia di Brand Portal, effettua una delle seguenti operazioni:

   * Passa il puntatore sull&#39;immagine da scaricare. Dalle miniature delle azioni rapide disponibili, fai clic su **[!UICONTROL Scarica]** icona.

   ![](assets/downloadsingleasset.png)

   * Seleziona l’immagine da scaricare. Dalla barra degli strumenti nella parte superiore, fai clic su **[!UICONTROL Scarica]** icona.

   ![](assets/downloadassets.png)

1. Dalla sezione **[!UICONTROL Scarica]** , seleziona le opzioni richieste a seconda che desideri scaricare la risorsa con o senza le relative rappresentazioni.

   ![](assets/donload-assets-dialog.png)

1. Per scaricare le rappresentazioni dinamiche della risorsa, seleziona la **[!UICONTROL Rappresentazioni dinamiche]** opzione.
1. Personalizza le proprietà del predefinito immagine in base al quale desideri riformattare dinamicamente l’immagine e le relative rappresentazioni durante il download. Specificate le dimensioni, il formato, lo spazio colore, la risoluzione e il modificatore immagine.

   ![](assets/dynamicrenditions.png)

1. Fai clic su **[!UICONTROL Scarica]**. Le rappresentazioni dinamiche personalizzate vengono scaricate in un file ZIP insieme all’immagine e alle rappresentazioni che hai scelto di scaricare. Tuttavia, se viene scaricata una singola risorsa, non viene creato alcun file zip, il che assicura un download rapido.
