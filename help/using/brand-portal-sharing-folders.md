---
title: Condividere le cartelle
description: Brand Portal richiede che le risorse vengano pubblicate da un’istanza Experience Manager Assets Author preconfigurata. Gli utenti non amministratori possono accedere alle risorse pubblicate solo se sono configurate con Experience Manager durante la configurazione della replica e le risorse devono essere condivise con loro.
content-type: reference
topic-tags: sharing
products: SG_EXPERIENCEMANAGER/Brand_Portal
exl-id: d28cf927-60e8-437e-9cba-92f7e19020e7
source-git-commit: 32a67abf466dd3bf635b851b02377ed23591915e
workflow-type: tm+mt
source-wordcount: '1090'
ht-degree: 1%

---

# Condividere cartelle su Brand Portal {#share-folders}

Assets deve essere pubblicato in Brand Portal da un’istanza Experience Manager Author preconfigurata, in quanto Brand Portal non supporta l’acquisizione di risorse.

## Flusso di lavoro di condivisione cartelle in Brand Portal {#folder-sharing-workflow-in-brand-portal}

Di seguito sono descritti il flusso di lavoro di condivisione cartelle e l&#39;accesso utente:

* Per impostazione predefinita, tutte le cartelle pubblicate da Experience Manager Assets a Brand Portal sono visibili solo all’amministratore di Brand Portal, a meno che non siano contrassegnate come pubbliche durante la configurazione della replica.
* L&#39;amministratore utilizza la console **[!UICONTROL Proprietà cartella]** per condividere una cartella con utenti o gruppi selettivi. Solo gli utenti o i gruppi con cui è condivisa la cartella potranno visualizzarla dopo l&#39;accesso a Brand Portal. La cartella non è visibile ad altri utenti.
* L&#39;amministratore può anche scegliere di rendere pubblica una cartella tramite la casella di controllo **[!UICONTROL Cartella pubblica]** nella console **[!UICONTROL Proprietà cartella]**. Una cartella pubblica è visibile a tutti gli utenti.

* Indipendentemente dai ruoli utente e dai privilegi, quando gli utenti accedono a Brand Portal, visualizzano tutte le cartelle pubbliche e le cartelle condivise direttamente con loro o con un gruppo a cui appartengono. Le cartelle private o condivise con altri utenti non sono visibili a tutti gli utenti.

### Condividere cartelle con gruppi di utenti su Brand Portal {#sharing-folders-with-user-groups-on-brand-portal}

I diritti di accesso alle risorse di una cartella dipendono dai diritti di accesso della relativa cartella principale, indipendentemente dalle impostazioni delle cartelle secondarie. [Gli ACL](https://experienceleague.adobe.com/it/docs/experience-manager-65/content/security/security) in AEM gestiscono questo comportamento, con le cartelle secondarie che ereditano gli ACL dalle cartelle principali. Si supponga, ad esempio, che la cartella A contenga la cartella B, che contiene la cartella C. Un gruppo di utenti (o utenti) con diritti di accesso sulla cartella A dispone quindi degli stessi diritti di accesso anche sulla cartella B e sulla cartella C. La cartella B, che è la cartella secondaria di A, eredita le ACL, mentre la cartella C, che è la cartella secondaria di B, le eredita.

Analogamente, i gruppi di utenti (o gli utenti) che dispongono delle autorizzazioni per accedere solo alla cartella B dispongono delle stesse autorizzazioni di accesso per la cartella C ma non per la cartella A. L’Adobe consiglia di organizzare il contenuto in modo che le risorse più esposte vengano posizionate in cartelle secondarie, consentendo di limitare l’accesso dalle cartelle secondarie fino alla cartella principale.

### Pubblicazione cartella pubblica {#public-folder-publish}

Gli utenti non amministratori (ad esempio Editor e Visualizzatori) possono accedere alle risorse pubblicate da AEM Assets a Brand Portal solo se durante la configurazione della replica di Brand Portal è selezionata l&#39;opzione **[!UICONTROL Cartella pubblica Publish]**.

![](assets/assetbpreplication.png)

Se l&#39;opzione **[!UICONTROL Cartella pubblica Publish]** è disabilitata, gli amministratori devono condividere queste risorse specificatamente con utenti non amministratori utilizzando la funzionalità di condivisione.

>[!NOTE]
>
>L&#39;opzione per abilitare **[!UICONTROL Publish delle cartelle pubbliche]** è disponibile da AEM 6.3.2.1 in poi.

## Accesso alle cartelle condivise {#access-to-shared-folders}

La matrice seguente illustra i diritti di accesso e i diritti di condivisione o annullamento della condivisione di risorse per vari ruoli utente:

|               | Accesso a tutte le cartelle pubblicate da AEM Assets a Brand Portal | Accesso alle cartelle condivise | Condividere o annullare la condivisione dei diritti della cartella |
|---------------|-----------|-----------|------------|
| Amministratore | Sì | Sì | Sì |
| Editor | No* | Sì, solo se condiviso con loro o con il gruppo a cui appartengono | Sì, solo per le cartelle condivise con loro o con il gruppo a cui appartengono |
| Visualizzatore | No* | Sì, solo se condiviso con loro o con il gruppo a cui appartengono | No |
| Utente ospite | No* | Sì, solo se condiviso con loro o con il gruppo a cui appartengono | No |

>[!NOTE]
>
>Per impostazione predefinita, l&#39;opzione **[!UICONTROL Cartella pubblica Publish]** è disabilitata durante la configurazione della replica di Brand Portal con AEM Author. Se l’opzione è abilitata, le cartelle pubblicate in Brand Portal sono accessibili a tutti gli utenti (anche a quelli non amministratori) per impostazione predefinita.

### Accesso degli utenti non amministratori alle cartelle condivise {#non-admin-user-access-to-shared-folders}

Gli utenti non amministratori possono accedere solo alle cartelle condivise con loro su Brand Portal. Tuttavia, la modalità di visualizzazione di queste cartelle nel portale al momento dell&#39;accesso dipende dalle impostazioni della configurazione di **[!UICONTROL Abilita gerarchia cartelle]**.

**Se la configurazione è disabilitata**

Gli utenti non amministratori possono visualizzare tutte le cartelle condivise con loro nella pagina di destinazione al momento dell’accesso a Brand Portal.

![](assets/disabled-folder-hierarchy1-1.png)

**Se la configurazione è abilitata**

Al momento dell’accesso a Brand Portal, gli utenti non amministratori visualizzano la struttura delle cartelle (a partire dalla cartella principale) e le cartelle condivise organizzate all’interno delle rispettive cartelle principali.

Queste cartelle principali sono cartelle virtuali e non è possibile eseguire alcuna azione su di esse. È possibile riconoscere queste cartelle virtuali con un&#39;icona di blocco.

Nessuna attività di azione visibile al passaggio del mouse o alla selezione in **[!UICONTROL Vista a schede]**, a differenza delle cartelle condivise. Il pulsante **[!UICONTROL Panoramica]** viene visualizzato quando si seleziona una cartella virtuale in **[!UICONTROL Vista a colonne]** e **[!UICONTROL Vista a elenco]**.

>[!NOTE]
>
>La miniatura predefinita delle cartelle virtuali è l&#39;immagine miniatura della prima cartella condivisa.

![](assets/enabled-hierarchy1-1.png) ![](assets/hierarchy1-nonadmin-1.png) ![](assets/hierarchy-nonadmin-1.png) ![](assets/hierarchy2-nonadmin-1.png)

## Condividere le cartelle {#how-to-share-folders}

Per condividere una cartella con gli utenti su Brand Portal, effettua le seguenti operazioni:

1. Fai clic sull&#39;icona di sovrapposizione a sinistra e scegli **[!UICONTROL Navigazione]**.

   ![](assets/selectorrail.png)

1. Dalla barra laterale a sinistra, seleziona **[!UICONTROL File]**.

   ![](assets/access_files.png)

1. Dall’interfaccia di Brand Portal, seleziona la cartella da condividere.

   ![](assets/share-folders.png)

1. Dalla barra degli strumenti nella parte superiore, seleziona **[!UICONTROL Condividi]**.

   ![](assets/share_icon.png)

   Viene visualizzata la console [!UICONTROL Proprietà cartella].

   ![](assets/folder_properties.png)

1. Nella console **[!UICONTROL Proprietà cartella]**, specifica il titolo della cartella nel campo **[!UICONTROL Titolo cartella]** se non desideri che il nome predefinito venga visualizzato agli utenti.
1. Dall&#39;elenco **[!UICONTROL Aggiungi utente]**, selezionare gli utenti o i gruppi con cui si desidera condividere la cartella e fare clic su **[!UICONTROL Aggiungi]**.
Per condividere la cartella solo con utenti guest e nessun altro utente, selezionare **[!UICONTROL Utenti anonimi]** dal menu a discesa **[!UICONTROL Membri]**.

   ![](assets/only-anonymous.png)

   >[!NOTE]
   >
   >Per rendere la cartella disponibile a tutti gli utenti indipendentemente dall&#39;appartenenza al gruppo e dal ruolo, renderla pubblica selezionando la casella di controllo **[!UICONTROL Cartella pubblica]**.

1. Se necessario, fare clic su **[!UICONTROL Cambia miniatura]** per modificare l&#39;immagine miniatura per la cartella.
1. Fai clic su **[!UICONTROL Salva]**.

1. Per accedere alla cartella condivisa, accedi a Brand Portal con le credenziali dell’utente con cui hai condiviso la cartella. Controlla la cartella condivisa nell’interfaccia.

## Annullare la condivisione delle cartelle {#unshare-the-folders}

Per annullare la condivisione di una cartella condivisa in precedenza, effettua le seguenti operazioni:

1. Dall’interfaccia di Brand Portal, seleziona la cartella di cui vuoi annullare la condivisione.

   ![](assets/share-folders-1.png)

1. Dalla barra degli strumenti nella parte superiore, fai clic su **[!UICONTROL Condividi]**.
1. Nella console **[!UICONTROL Proprietà cartella]**, in **[!UICONTROL Membri]**, fai clic sul simbolo **[!UICONTROL x]** accanto a un utente per rimuoverlo dall&#39;elenco degli utenti con cui hai condiviso la cartella.

   ![](assets/folder_propertiesunshare.png)

1. Nella finestra del messaggio di avviso, fare clic su **[!UICONTROL Conferma]** per confermare l&#39;annullamento della condivisione.
Fai clic su **[!UICONTROL Salva]**.

1. Accedi a Brand Portal con le credenziali dell’utente rimosso dall’elenco condiviso. La cartella non è più disponibile per l’utente nell’interfaccia di Brand Portal.
