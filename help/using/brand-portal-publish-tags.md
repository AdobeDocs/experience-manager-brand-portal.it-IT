---
title: Tag Publish per Brand Portal
description: Scopri come pubblicare i tag da Experience Manager Assets a Brand Portal.
topic-tags: publish
products: SG_EXPERIENCEMANAGER/Brand_Portal
content-type: reference
exl-id: 842656a6-1a2b-4b64-954d-1e663923a1a1
source-git-commit: 32a67abf466dd3bf635b851b02377ed23591915e
workflow-type: tm+mt
source-wordcount: '603'
ht-degree: 1%

---

# Tag Publish per Brand Portal {#publish-tags-to-brand-portal}

Scopri come pubblicare i tag da Experience Manager Assets a Brand Portal.

I tag sono utili per organizzare le risorse e migliorare la ricercabilità delle risorse a cui sono associati. I tag possono essere considerati come parole chiave o etichette (metadati) associate alle risorse e consentono di trovare rapidamente le risorse come risultato di una ricerca. Per informazioni su come assegnare tag alle risorse in Experience Manager Assets, consulta [Utilizzare i tag per organizzare le risorse](https://experienceleague.adobe.com/en/docs/experience-manager-65/content/assets/managing/organize-assets).

I tag (associati alle risorse e alle raccolte in AEM) vengono pubblicati automaticamente in Brand Portal quando le risorse (e le raccolte) con i tag associati vengono pubblicate in Brand Portal. I tag pubblicati sono utili per consentire alle ricerche di trovare le risorse associate.

>[!NOTE]
>
>L’Adobe consiglia di pubblicare esclusivamente i tag in Brand Portal prima di pubblicare le risorse (e le raccolte) a cui sono associati i tag. Questo approccio garantisce una pubblicazione più rapida delle risorse (e delle raccolte) in Brand Portal.

## Gestire i tag {#manage-tags}

Puoi utilizzare i tag preesistenti per allegare una risorsa o creare nuovi tag dalla console Tag AEM (**[!UICONTROL Strumenti | Assegnazione tag | Tag AEM]**). In entrambi gli scenari, devi innanzitutto pubblicare i tag in Brand Portal e quindi associarli alle risorse appropriate.

Per creare tag su AEM, pubblicarli su Brand Portal e associarli alle risorse (o raccolte) appropriate, effettua le seguenti operazioni:

1. **Crea tag**
Accedi a un&#39;istanza Autore AEM con privilegi amministrativi e accedi alla console **[!UICONTROL Tag AEM]** dalla navigazione globale:

   1. Seleziona **[!UICONTROL Strumenti]**

   1. Seleziona **[!UICONTROL Generale]**

   1. Seleziona **[!UICONTROL assegnazione tag]**

1. Seleziona **[!UICONTROL Crea]**, quindi seleziona l&#39;opzione **[!UICONTROL Crea tag]**.
1. Specifica:

   * **[!UICONTROL Titolo]**
     *(obbligatorio)* Titolo visualizzato per il tag.
   * **[!UICONTROL Nome]**
     *(obbligatorio)* Nome per il tag. Se non viene specificato, viene creato un nome di nodo valido dal titolo. Vedi [TagID](https://experienceleague.adobe.com/en/docs/experience-manager-65/content/implementing/developing/platform/tagging/framework).
   * **Descrizione**
     *(facoltativo)* Descrizione del tag.
   * **Percorso tag**
Percorso JCR del tag.

1. Seleziona **[!UICONTROL Invia]** per creare il tag.

   Dopo aver creato un tag su un’istanza AEM, il tag è disponibile per l’allegato a una risorsa (utilizzando la sezione Proprietà o la sezione Gestisci tag di tale risorsa).

1. **Publish il tag in Brand Portal**.

   Vai alla console **[!UICONTROL Tag AEM]** ([!UICONTROL Strumenti | Assegnazione tag | Tag AEM]), selezionare il tag desiderato e Publish in Brand Portal.

1. **Allega il tag a una risorsa (o raccolta)**.

   Seleziona una risorsa (o una raccolta) e allega il tag desiderato utilizzando la sezione Proprietà o la sezione Gestisci tag di tale risorsa. Per ulteriori informazioni su come assegnare tag alle risorse in AEM Assets, vai a [utilizzare i tag per organizzare le risorse](https://experienceleague.adobe.com/en/docs/experience-manager-65/content/assets/managing/organize-assets).

1. **Risorse Publish (o raccolte) in Brand Portal**.\
   Quando pubblichi una risorsa (o raccolta) in Brand Portal, il tag allegato è disponibile anche in Brand Portal.

   Per visualizzare il tag allegato alla rispettiva risorsa (o raccolta) in Brand Portal, accedi a Brand Portal, quindi seleziona la risorsa. Nella sezione Proprietà puoi vedere il tag allegato.

## Promozione ricerca {#search-promote}

AEM Assets Brand Portal consente di impostare risorse specifiche come risultati principali per le ricerche basate su un tag parola chiave.

Per elevare una risorsa a livello di parola chiave di ricerca, effettua le seguenti operazioni:

1. Apri la pagina **[!UICONTROL Proprietà]** di una risorsa nell&#39;istanza di authoring AEM.
1. Passa alla scheda **[!UICONTROL Avanzate]**.
1. Nella sezione **[!UICONTROL Promozione ricerca]** all&#39;interno della sezione **[!UICONTROL Privilegi elevati per parole chiave di ricerca]**, selezionare **[!UICONTROL Aggiungi]** per aggiungere parole chiave o tag di ricerca.

   ![](assets/search-promote.png)

1. Salva le modifiche.
1. Publish la risorsa in Brand Portal.
1. Accedi a Brand Portal. Visualizza la scheda **[!UICONTROL Avanzate]** nella sezione **[!UICONTROL Proprietà]** della risorsa.
La parola chiave **[!UICONTROL Search Promote]** è visibile anche nelle proprietà della risorsa.
