---
title: Asset Sourcing in Brand Portal
seo-title: Asset Sourcing in Brand Portal
description: Ottieni informazioni sulla funzione di asset sourcing rilasciata in Adobe Experience Manager Assets Brand Portal.
seo-description: Get an insight into the asset sourcing feature released in the Adobe Experience Manager Assets Brand Portal.
uuid: null
content-type: reference
contentOwner: Vishabh Gupta
topic-tags: brand-portal
products: SG_EXPERIENCEMANAGER/Brand_Portal
discoiquuid: null
sub-product: assets
topics: collaboration, content-velocity, sharing
doc-type: feature-video
activity: use
audience: author, marketer
version: 6.5
kt: 3838
exl-id: 2c132a7a-ed10-4856-8378-67939167ea60
source-git-commit: 955cd8afe939ff47e9f08f312505e230e2f38495
workflow-type: tm+mt
source-wordcount: '646'
ht-degree: 1%

---

# Panoramica su Asset Sourcing {#overview-asset-sourcing-in-bp}

**Asset Sourcing** consente agli utenti di Experience Manager Assets (amministratori/utenti non amministratori) di creare nuove cartelle con un **Contributo risorse** garantendo che la nuova cartella creata sia aperta all’invio di risorse da parte degli utenti di Brand Portal. Questo attiva automaticamente un flusso di lavoro che crea due sottocartelle aggiuntive, denominate **CONDIVISO** e **NUOVO**, all&#39;interno del nuovo **Contributo** cartella. L’amministratore definisce quindi il requisito caricando una breve descrizione dei tipi di risorse da aggiungere alla cartella dei contributi, nonché un set di risorse previste, nella **CONDIVISO** per garantire che gli utenti BP dispongano delle informazioni di riferimento necessarie. L’amministratore può quindi concedere agli utenti Brand Portal attivi l’accesso alla cartella dei contributi prima di pubblicare la nuova **Contributo** in Brand Portal. Una volta che l’utente ha finito di aggiungere il contenuto nel **NUOVO** possono pubblicare nuovamente la cartella dei contributi nell’ambiente di authoring Experience Manager. Potrebbero essere necessari alcuni minuti per completare l’importazione e riflettere il contenuto appena pubblicato in Experience Manager Assets.

Inoltre, tutte le funzionalità esistenti rimangono invariate. Gli utenti di Brand Portal possono visualizzare, cercare e scaricare le risorse dalla cartella dei contributi e dalle altre cartelle consentite. Gli amministratori possono inoltre condividere ulteriormente la cartella dei contributi, modificare le proprietà e aggiungere risorse alle raccolte.

![Brand Portal Asset Sourcing](assets/asset-sourcing.png)

>[!VIDEO](https://video.tv.adobe.com/v/29365/?quality=12)

## Prerequisiti {#prerequisites}

* istanza Experience Manager Assets as a Cloud Service, Experience Manager Assets 6.5.2 o versione successiva.
* Assicurati che l’istanza di Experience Manager Assets sia configurata con Brand Portal. Vedi, [Configurare Experience Manager Assets con Brand Portal](../using/configure-aem-assets-with-brand-portal.md).

<!--
* Ensure that your Brand Portal tenant is configured with one AEM Assets author instance.
-->

>[!NOTE]
>
>Per impostazione predefinita, la funzione Asset Sourcing è abilitata in Experience Manager Assets as a Cloud Service, Experience Manager Assets 6.5.9 e versioni successive.
>
>Le configurazioni esistenti continueranno a funzionare sulle versioni precedenti.

>[!NOTE]
>
>Esiste un problema noto in Experience Manager Assets 6.5.4. Gli utenti di Brand Portal non possono pubblicare le risorse della cartella Contributi in Experience Manager Assets quando si esegue l’aggiornamento alla console Adobe Developer.
>
>Il problema è risolto in Experience Manager Assets 6.5.5. È possibile aggiornare l’istanza di Experience Manager Assets al service pack più recente e [aggiornare le configurazioni](https://experienceleague.adobe.com/docs/experience-manager-65/assets/brandportal/configure-aem-assets-with-brand-portal.html#upgrade-integration-65) sulla console Adobe Developer.

<!--

>For immediate fix on AEM 6.5.4, it is recommended to [download the hotfix](https://www.adobeaemcloud.com/content/marketplace/marketplaceProxy.html?packagePath=/content/companies/public/adobe/packages/cq650/hotfix/cq-6.5.0-hotfix-33041) and install on your author instance.
-->

<!--
## Configure Asset Sourcing {#configure-asset-sourcing}

**Asset Sourcing** is configured from within the AEM Assets author instance. The administrators can enable the Asset Sourcing feature flag configuration from the **AEM Web Console Configuration** and upload the active Brand Portal users list in **AEM Assets**.

>[!NOTE]
>
>Asset Sourcing is by default enabled on AEM Assets as a Cloud Service. The AEM administrator can directly upload the active Brand Portal users to allow them access to the Asset Sourcing feature.

>[!NOTE]
>
>Before you begin with the configuration, ensure that your AEM Assets instance is configured with Brand Portal. See, [Configure AEM Assets with Brand Portal](../using/configure-aem-assets-with-brand-portal.md). 

The following video demonstrates, how to configure Asset Sourcing on your AEM Assets author instance:

>[!VIDEO](https://video.tv.adobe.com/v/29771)
-->

<!--
### Enable Asset Sourcing {#enable-asset-sourcing}

AEM administrators can enable the Asset Sourcing feature flag from within the AEM Web Console Configuration (a.k.a Configuration Manager).

>[!NOTE]
>
>This step is not applicable for AEM Assets as a Cloud Service.


**To enable Asset Sourcing:**
1. Log in to your AEM Assets author instance and open Configuration Manager. 
Default URL: http:// localhost:4502/system/console/configMgr.
1. Search using the keyword **Asset Sourcing** to locate **[!UICONTROL Asset Sourcing Feature Flag Config]**.
1. Click **[!UICONTROL Asset Sourcing Feature Flag Config]** to open the configuration window.
1. Select the **[!UICONTROL feature.flag.active.status]** check box.
1. Click **[!UICONTROL Save]**.

![](assets/enable-asset-sourcing.png)
-->


### Carica elenco utenti di Brand Portal {#upload-bp-user-list}

Gli amministratori di Experience Manager Assets possono caricare in Experience Manager Assets il file di configurazione utente di Brand Portal (con estensione csv) contenente l’elenco utenti di Brand Portal attivo per consentire loro di accedere alla funzione Asset Sourcing.

Una cartella di contributi può essere condivisa solo con gli utenti Brand Portal attivi definiti nell’elenco di utenti. L’amministratore può anche aggiungere nuovi utenti nel file di configurazione e caricare l’elenco di utenti modificato.

>[!NOTE]
>
>Assicurati che l’istanza di Experience Manager Assets sia configurata con Brand Portal. Vedi, [Configurare Experience Manager Assets con Brand Portal](../using/configure-aem-assets-with-brand-portal.md).

>[!NOTE]
>
>Il formato del file CSV è lo stesso supportato nell’Admin Console per l’importazione in blocco da parte dell’utente. E-mail, nome e cognome sono obbligatori.

Gli amministratori possono aggiungere nuovi utenti in Admin Console, vedi [Gestisci utenti](brand-portal-adding-users.md) per informazioni dettagliate. Dopo aver aggiunto gli utenti in Admin Console, è possibile aggiungerli al file di configurazione utente di Brand Portal e quindi assegnare loro l’autorizzazione per accedere alla cartella dei contributi.

**Per caricare l’elenco degli utenti di Brand Portal:**

1. Accedi all’istanza di Experience Manager Assets.
1. Dalla sezione **Strumenti**  , passa a **[!UICONTROL Risorse]** > **[!UICONTROL Utenti Brand Portal]**.

1. Viene visualizzata la finestra Carica collaboratori di Brand Portal.
Sfoglia dal computer locale e carica **file di configurazione (.csv)** contenente l&#39;elenco degli utenti attivi di Brand Portal.
1. Fai clic su **[!UICONTROL Salva]**.

   ![](assets/upload-user-list2.png)


Gli amministratori possono fornire l’accesso a utenti specifici da questo elenco di utenti durante la configurazione di una cartella di contributi. Solo gli utenti assegnati a una cartella di contributi avranno accesso a tale cartella e pubblicheranno le risorse da Brand Portal a Experience Manager Assets.

## Consulta anche {#reference-articles}

* [Configurare e pubblicare la cartella dei contributi in Brand Portal](brand-portal-publish-contribution-folder-to-brand-portal.md)

* [Pubblicare la cartella dei contributi in Experience Manager Assets](brand-portal-publish-contribution-folder-to-aem-assets.md)
