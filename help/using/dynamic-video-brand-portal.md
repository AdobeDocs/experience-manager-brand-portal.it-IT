---
title: Supporto di video dinamici su Brand Portal
description: Supporto di video dinamici su Brand Portal
contentOwner: mgulati
products: SG_EXPERIENCEMANAGER/Brand_Portal
content-type: reference
topic-tags: download-install
exl-id: 08d6a0fb-061e-4bef-b8e2-bb8522e7482e
source-git-commit: e2e007550b557e790533204d49271c90b3b8647d
workflow-type: tm+mt
source-wordcount: '1194'
ht-degree: 0%

---

# Supporto di video dinamici su Brand Portal {#dynamic-video-support-on-brand-portal}

Anteprima e riproduzione di video in modo adattivo su Brand Portal con supporto Dynamic Medie. Scarica anche le rappresentazioni dinamiche dal portale e dai collegamenti condivisi.
Gli utenti di Brand Portal possono:

* Visualizza l’anteprima dei video nelle pagine Dettagli risorsa, Vista a schede e Anteprima condivisione collegamenti.
* Riproduci le codifiche video nella pagina Dettagli risorsa.
* Visualizza le rappresentazioni dinamiche nella scheda Rappresentazioni della pagina Dettagli risorsa.
* Scarica le codifiche video e le cartelle contenenti i video.

>[!NOTE]
>
>Per utilizzare i video e pubblicarli in Brand Portal, accertati che l’istanza Autore Experience Manager sia configurata in modalità ibrida Dynamic Medie o in modalità Dynamic Medie **[!DNL Scene7]**.

Per visualizzare in anteprima, riprodurre e scaricare i video, Brand Portal espone agli amministratori le due configurazioni seguenti:

* [Configurazione ibrida di Dynamic Medie](#configure-dm-hybrid-settings)
Se l’istanza Autore Experience Manager è in esecuzione in modalità Dynamic Medie - Hybrid.
* [Dynamic Medie [!DNL Scene7] configurazione](#configure-dm-scene7-settings)
Se l&#39;istanza Autore Experience Manager è in esecuzione in modalità Dynamic Medie - **[!DNL Scene7]**.
Imposta una di queste configurazioni in base alle configurazioni impostate nell’istanza Autore Experience Manager con cui viene replicato il tenant Brand Portal.

>[!NOTE]
>
>I video dinamici non sono supportati nei tenant di Brand Portal configurati con Experience Manager Author in esecuzione in modalità di esecuzione **[!UICONTROL Scene7 Connect]**.

## Come vengono riprodotti i video dinamici? {#how-are-dynamic-videos-played}

![Le codifiche video sono state recuperate dal cloud](assets/VideoEncodes.png)

Se le configurazioni di Dynamic Medie ([Ibrido](../using/dynamic-video-brand-portal.md#configure-dm-hybrid-settings) o [[!DNL Scene7]](../using/dynamic-video-brand-portal.md#configure-dm-scene7-settings)) sono impostate in Brand Portal, le rappresentazioni dinamiche vengono recuperate dal server **[!DNL Scene7]**. Le codifiche video vengono quindi visualizzate in anteprima e riprodotte senza ritardi e con una distorsione della qualità.

L&#39;archivio Brand Portal non memorizza le codifiche video e le recupera dal server **[!DNL Scene7]**. Assicurati che le configurazioni di Dynamic Medie nell’istanza di authoring di Adobe Experience Manager e in Brand Portal siano le stesse.

>[!NOTE]
>
>I visualizzatori video e i predefiniti visualizzatore non sono supportati in Brand Portal. I video vengono visualizzati in anteprima e riprodotti sui visualizzatori predefiniti in Brand Portal.

## Prerequisiti {#prerequisites}

Per lavorare con i video dinamici su Brand Portal, assicurati di:

* **Avvia Autore Experience Manager in modalità Dynamic Medie**

  Avvia l&#39;istanza Autore Experience Manager (con cui è configurato Brand Portal) in [Dynamic Medie - [!DNL Scene7] modalità](https://experienceleague.adobe.com/en/docs/experience-manager-65/content/assets/dynamic/config-dms7#enabling-dynamic-media-in-scene-mode) o in [Dynamic Medie - modalità ibrida](https://experienceleague.adobe.com/en/docs/experience-manager-65/content/assets/dynamic/config-dynamic) oppure

* **Configura Cloud Service Dynamic Medie nell&#39;istanza Autore Experience Manager**

  In base alla modalità Dynamic Medie (modalità Scene7 o modalità ibrida) su cui è in esecuzione Experience Manager Author, impostare [Cloud Service Dynamic Medie ([!DNL Scene7] modalità)](https://experienceleague.adobe.com/en/docs/experience-manager-65/content/assets/dynamic/config-dms7#configuring-dynamic-media-cloud-services) o [Cloud Service Dynamic Medie (modalità ibrida)](https://experienceleague.adobe.com/en/docs/experience-manager-65/content/assets/dynamic/config-dms7#configuring-dynamic-media-cloud-services) per Experience Manager Author da **Strumenti** | **Cloud Service** | **Dynamic Medie**.

* **Configura Dynamic Medie in Brand Portal**

  In base alle configurazioni di Dynamic Medie Cloud per Experience Manager Author, configura [le impostazioni di Dynamic Medie](#configure-dm-hybrid-settings) o [[!DNL Scene7] le impostazioni](#configure-dm-scene7-settings) dagli strumenti di amministrazione di Brand Portal.

  Assicurati che [tenant Brand Portal separati](#separate-tenants) siano utilizzati per Experience Manager per le istanze Autore configurate in Dynamic Medie - modalità **[!UICONTROL Scene7]** e Dynamic Medie - modalità ibrida. Se utilizzi le funzionalità di Dynamic Medie **[!UICONTROL S7]** e Dynamic Medie Hybrid, questo approccio è particolarmente importante.

* **Cartelle Publish con codifiche video applicate a Brand Portal**

  Applica [codifiche video](https://experienceleague.adobe.com/en/docs/experience-manager-65/content/assets/dynamic/video-profiles) e pubblica la cartella contenente le risorse rich media dall&#39;istanza Experience Manager Author a Brand Portal.

* **se l&#39;anteprima protetta è abilitata, gli indirizzi IP in uscita in SPS verranno Inseriti nell&#39;elenco Consentiti**

  Se si utilizza Dynamic Medie-**[!DNL Scene7]** (con [anteprima protetta abilitata](https://experienceleague.adobe.com/en/docs/dynamic-media-classic/using/upload-publish/testing-assets-making-them-public) per una società), si consiglia all&#39;amministratore **[!DNL Scene7]** della società [di inserire nell&#39;elenco Consentiti gli IP pubblici in uscita](https://experienceleague.adobe.com/en/docs/dynamic-media-classic/using/upload-publish/testing-assets-making-them-public#testing-the-secure-testing-service) per le rispettive aree tramite l&#39;interfaccia utente flash di SPS (**[!UICONTROL Scene7]** Publishing System).

  Gli IP in uscita sono i seguenti:

  | **Area** | **IP in uscita** |
  |--- |--- |
  | ND | 130.248.160.68, 20.94.203.130 |
  | EMEA | 185.34.189.3, 51.132.146.75 |
  | APAC | 63 140 44 54 |

  Inserire nell&#39;elenco Consentiti Per uno di questi IP in uscita, consulta [Preparare il tuo account per un servizio di test sicuro](https://experienceleague.adobe.com/en/docs/dynamic-media-classic/using/upload-publish/testing-assets-making-them-public#testing-the-secure-testing-service).

## Best practice

Assicurati che le risorse video dinamiche siano state visualizzate in anteprima, riprodotte e scaricate correttamente da Brand Portal (e dai collegamenti condivisi), segui queste procedure:

### Tenant separati per le modalità Dynamic Medie - Scene7 e Dynamic Medie - Ibrido {#separate-tenants}

Se si utilizzano entrambe le funzionalità di Dynamic Medie - modalità **[!DNL Scene7]** e Dynamic Medie - modalità ibrida, utilizzare tenant di Brand Portal diversi, ad Experience Manager istanze di authoring configurate con le modalità ibrida Dynamic Medie - **[!DNL Scene7]** e Dynamic Medie.


![Mappatura uno a uno dell&#39;autore e della BP](assets/BPDynamicMedia.png)

### Stessi dettagli di configurazione nell’istanza Experience Manager Author e in Brand Portal

Assicurati che i dettagli di configurazione siano gli stessi in Brand Portal e **[!UICONTROL Configurazione cloud Experience Manager]**. Gli stessi dettagli di configurazione includono:

* **[!UICONTROL Titolo]**
* **[!UICONTROL ID registrazione]**
* **[!UICONTROL URL servizio video]** in **[!UICONTROL Dynamic Medie - Modalità ibrida]**
* **[!UICONTROL Titolo]**
* Credenziali (**[!UICONTROL E-mail]** e password)
* **[!UICONTROL Area]**
* **[!UICONTROL Società]** in Dynamic Medie - modalità **[!DNL Scene7]**

### Inserire nell&#39;elenco Consentiti IP pubblici in uscita per la modalità Dynamic Medie Scene7

Se Dynamic Medie **[!UICONTROL Scene7]** - con [anteprima protetta abilitata](https://experienceleague.adobe.com/en/docs/dynamic-media-classic/using/upload-publish/testing-assets-making-them-public) - viene utilizzato per distribuire risorse video a Brand Portal, **[!UICONTROL Scene7]** stabilisce un server immagini dedicato per gli ambienti di gestione temporanea o le applicazioni interne. Qualsiasi richiesta inviata a questo server controlla l’indirizzo IP di origine. Se la richiesta in ingresso non si trova nell’elenco approvato di indirizzi IP, viene restituita una risposta di errore.
L&#39;amministratore della società **[!UICONTROL Scene7]** configura quindi un elenco approvato di indirizzi IP per l&#39;ambiente **[!UICONTROL Secure Testing]** della propria società tramite l&#39;interfaccia utente flash **[!UICONTROL SPS]** (Scene7 Publishing System). Accertati che l’IP in uscita per la tua rispettiva regione (dal seguente) sia aggiunto all’elenco approvato.
Inserire nell&#39;elenco Consentiti Per uno di questi IP in uscita, consulta [Preparare il tuo account per un servizio di test sicuro](https://experienceleague.adobe.com/en/docs/dynamic-media-classic/using/upload-publish/testing-assets-making-them-public#testing-the-secure-testing-service).
Gli IP in uscita sono i seguenti:

| **Area** | **IP in uscita** |
|--- |--- |
| ND | 130.248.160.68, 20.94.203.130 |
| EMEA | 51 132 146 75, 130 248 244 202, 130 248 244 203, 130 248 244 204, 130 248 210, 130 248 210, 130 248 244 211, 130 244 8 244 212 |
| APAC | 63 140 44 54 |

## Configurare le impostazioni di Dynamic Medie (ibrido) {#configure-dm-hybrid-settings}

Se l&#39;istanza Autore Experience Manager è in esecuzione in modalità ibrida per elementi multimediali dinamici, utilizzare il riquadro **[!UICONTROL Video]** del pannello Strumenti di amministrazione per configurare le impostazioni del gateway Dynamic Medie.

>[!NOTE]
>
>[profili di codifica video](https://experienceleague.adobe.com/en/docs/experience-manager-65/content/assets/dynamic/video-profiles) non pubblicati in Brand Portal. Vengono invece recuperati dal server **[!UICONTROL Scene7]**. Pertanto, affinché le codifiche video vengano riprodotte correttamente in Brand Portal, assicurati che i dettagli di configurazione siano gli stessi dei [Cloud Service Dynamic Medie ([!DNL Scene7] modalità)](https://experienceleague.adobe.com/en/docs/experience-manager-65/content/assets/dynamic/config-dms7#configuring-dynamic-media-cloud-services) nell&#39;istanza Autore Experience Manager.

Per impostare le configurazioni di Dynamic Medie sui tenant Brand Portal:

1. Seleziona il logo di Experience Manager per accedere agli strumenti di amministrazione dalla barra degli strumenti nella parte superiore di Brand Portal.
1. Dal pannello Strumenti di amministrazione, seleziona il riquadro **[!UICONTROL Video]**.

   ![Configurazione ibrida Dynamic Medie in Brand Portal](assets/DMHybrid-Video.png)

   **[!UICONTROL Viene visualizzata la pagina Modifica configurazione Dynamic Medie]**.

   ![Configurazione ibrida di Dynamic Medie in Brand Portal](assets/edit-dynamic-media-config.png)

1. Specificare **[!UICONTROL ID registrazione]** e **[!UICONTROL URL servizio video]** (URL DM-Gateway). Assicurati che questi dettagli siano identici a quelli presenti in **[!UICONTROL Strumenti > Cloud Service]** nell&#39;istanza Autore Experience Manager.
1. Seleziona **Salva** per salvare la configurazione.

## Configurare le impostazioni di Dynamic Medie Scene7 {#configure-dm-scene7-settings}

Se l&#39;istanza Autore Experience Manager è in esecuzione in modalità Dynamic Medie- **[!UICONTROL Scene7]**, utilizzare il riquadro **[!UICONTROL Configurazione Dynamic Medie]** del pannello Strumenti di amministrazione per configurare le impostazioni del server **[!UICONTROL Scene7]**.

Per configurare le configurazioni di Dynamic Medie **[!UICONTROL Scene7]** sui tenant Brand Portal:

1. Seleziona il logo di Experience Manager per accedere agli strumenti di amministrazione dalla barra degli strumenti nella parte superiore di Brand Portal.

2. Dal pannello Strumenti di amministrazione, selezionare il riquadro **[!UICONTROL Configurazione Dynamic Medie]**.

   ![DM [!UICONTROL Configurazione Scene 7] in Brand Portal](assets/DMS7-Tile.png)

   **[!UICONTROL Viene visualizzata la pagina Modifica configurazione Dynamic Medie]**.

   ![Configurazione Scene7 in Brand Portal](assets/S7Config.png)

3. Fornisci:

   * **[!UICONTROL Titolo]**
   * Credenziali (**[!UICONTROL ID e-mail]** e **[!UICONTROL Password]**) per accedere al server Scene7
   * **[!UICONTROL Area]**

   Assicurati che questi valori siano identici a quelli presenti nell’istanza Autore dell’Experience Manager.

4. Selezionare **[!UICONTROL Connetti a Dynamic Medie]**.

5. Fornisci **[!UICONTROL Nome società]** e **[!UICONTROL Salva]** la configurazione.
