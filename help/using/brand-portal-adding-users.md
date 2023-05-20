---
title: Gestire utenti, gruppi e ruoli utente
seo-title: Manage users, groups, and user roles
description: Gli amministratori possono utilizzare Adobe Admin Console per creare utenti e profili di prodotto di Brand Portal e gestire i loro ruoli mediante l’interfaccia utente di Brand Portal. Questo privilegio non è disponibile per visualizzatori ed editor.
seo-description: Administrators can use Adobe Admin Console to create Brand Portal users and product profiles, and manage their roles using the Brand Portal user interface. This privilege is not available to Viewers and Editors.
uuid: 0dc1867c-6d1b-4d0d-a25e-0df207c269b8
content-type: reference
topic-tags: administration
products: SG_EXPERIENCEMANAGER/Brand_Portal
discoiquuid: ba468e80-d077-4af6-b782-238fc557e22b
role: Admin
exl-id: 35b1fd75-f9e4-4145-80bd-84de091f8b2b
source-git-commit: 955cd8afe939ff47e9f08f312505e230e2f38495
workflow-type: tm+mt
source-wordcount: '2185'
ht-degree: 0%

---

# Gestione di utenti, gruppi e ruoli utente {#manage-users-groups-and-user-roles}

Gli amministratori possono utilizzare Adobe Admin Console per creare utenti e profili di prodotto di Experience Manager Assets Brand Portal e gestirne i ruoli mediante l’interfaccia utente di Brand Portal. Questo privilegio non è disponibile per visualizzatori ed editor.

In entrata [[!UICONTROL Admin Console]](https://adminconsole.adobe.com/enterprise/overview), puoi visualizzare tutti i prodotti associati alla tua organizzazione. Un prodotto può essere una qualsiasi soluzione di Experience Cloud, ad esempio Adobe Analytics, Adobe Target o Experience Manager Assets Brand Portal. Devi scegliere il prodotto AEM Brand Portal e creare i profili di prodotto.

<!--
Comment Type: draft

<note type="note">
<p>Product Profiles (formerly known as product configurations*). </p>
<p>* The nomenclature has changed from product configurations to product profiles in the new Adobe Admin Console.</p>
</note>
-->
![](assets/create-user-group.png)

Questi profili di prodotto vengono sincronizzati con l’interfaccia utente di Brand Portal ogni 8 ore e sono visibili come gruppi in Brand Portal. Dopo aver aggiunto gli utenti, creato i profili di prodotto e aggiunto gli utenti a tali profili di prodotto, puoi assegnare ruoli a utenti e gruppi in Brand Portal.

>[!NOTE]
>
>Per creare gruppi in Brand Portal, da Adobe [!UICONTROL Admin Console], utilizza **[!UICONTROL Prodotti > Profili di prodotto]**, invece di **[!UICONTROL Pagina utente > Gruppi di utenti]**. Profili di prodotto in Adobe [!UICONTROL Admin Console] vengono utilizzati per creare gruppi in Brand Portal.

## Aggiungi un utente {#add-a-user}

Se sei un amministratore di prodotto, utilizza Adobe [[!UICONTROL Admin Console]](https://adminconsole.adobe.com/enterprise/overview) per creare utenti e assegnarli a profili di prodotto (*precedentemente noti come configurazioni di prodotto*), visualizzati come gruppi in Brand Portal. Puoi utilizzare i gruppi per eseguire operazioni in blocco, ad esempio la gestione dei ruoli e la condivisione delle risorse.

>[!NOTE]
>
>I nuovi utenti che non hanno accesso a Brand Portal possono richiedere l’accesso dalla schermata di accesso di Brand Portal. Per ulteriori informazioni, consulta [Richiedi accesso a Brand Portal](../using/brand-portal.md#request-access-to-brand-portal). Dopo aver ricevuto le notifiche di richiesta di accesso nell&#39;area di notifica, fare clic sulla notifica appropriata e quindi su **[!UICONTROL Concedi l&#39;accesso]**. In alternativa, segui il collegamento nell’e-mail di richiesta di accesso ricevuta. Quindi, per aggiungere un utente [Adobe [!UICONTROL Admin Console]](https://adminconsole.adobe.com/enterprise/overview), seguire i passaggi 4-7 nella procedura seguente.

>[!NOTE]
>
>Puoi accedere a [Adobe [!UICONTROL Admin Console]](https://adminconsole.adobe.com/enterprise/overview) direttamente o da Brand Portal. Se effettui l’accesso direttamente, segui i passaggi 4-7 della procedura seguente per aggiungere un utente.

1. Dalla barra degli strumenti AEM in alto, fai clic sul logo dell’Adobe per accedere agli strumenti di amministrazione.

   ![Logo AEM](assets/aemlogo.png)

1. Nel pannello Strumenti di amministrazione, fate clic su **[!UICONTROL Utenti]**.

   ![Pannello Strumenti di amministrazione](assets/admin-tools-panel-5.png)

1. In [!UICONTROL Ruoli utente] , fare clic su **[!UICONTROL Gestione]** , quindi fai clic su **[!UICONTROL Admin Console lancio]**.

   ![Admin Console sui ruoli utente da avviare](assets/launch_admin_console.png)

1. Ad Admin Console, per creare un nuovo utente, effettuare una delle seguenti operazioni:

   * Dalla barra degli strumenti nella parte superiore, fai clic su **[!UICONTROL Panoramica]**. In [!UICONTROL Panoramica] pagina, fai clic su **[!UICONTROL Assegna utenti]** dalla scheda del prodotto Brand Portal.

   ![Panoramica Admin Console](assets/admin_console_overviewadduser.png)

   * Dalla barra degli strumenti nella parte superiore, fai clic su **[!UICONTROL Utenti]**. In [!UICONTROL Utenti] pagina, [!UICONTROL Utenti] nella barra a sinistra è selezionato per impostazione predefinita. Clic **[!UICONTROL Aggiungi utente]**.

   ![Admin Console Aggiungi utenti](assets/admin_console_adduseruserpage.png)

1. Nella finestra di dialogo Aggiungi utente digitare l&#39;ID e-mail dell&#39;utente che si desidera aggiungere o selezionare l&#39;utente dall&#39;elenco di suggerimenti visualizzato durante la digitazione.

   ![Aggiungi utente a Brand Portal](assets/add_user_to_aem_bp.png)

1. Assegna l’utente ad almeno un profilo di prodotto (precedentemente noto come configurazioni di prodotto) in modo che possa accedere a Brand Portal. Seleziona il profilo di prodotto appropriato da **[!UICONTROL Seleziona un profilo per questo prodotto]** campo.
1. Fai clic su **[!UICONTROL Salva]**. Viene inviata un’e-mail di benvenuto al nuovo utente aggiunto. L’utente invitato può fare clic sul collegamento nell’e-mail di benvenuto per accedere a Brand Portal. L’utente può accedere utilizzando l’ID e-mail ([!UICONTROL Adobe ID], [!UICONTROL Enterprise ID], o [!UICONTROL ID federato]) configurato in Admin Console. Per ulteriori informazioni, consulta [Esperienza del primo accesso](../using/brand-portal-onboarding.md).

   >[!NOTE]
   >
   >Se un utente non è in grado di accedere a Brand Portal, l’amministratore dell’organizzazione visita Adobe [!UICONTROL Admin Console] e verifica se l’utente è presente e è stato aggiunto ad almeno un profilo di prodotto.

   Per informazioni sulla concessione di privilegi amministrativi all&#39;utente, vedere [Fornire privilegi di amministratore agli utenti](../using/brand-portal-adding-users.md#provideadministratorprivilegestousers).

## Aggiungere un profilo di prodotto {#add-a-product-profile}

Profili di prodotto (precedentemente noti come configurazioni di prodotto) in [!UICONTROL Admin Console] vengono utilizzati per creare gruppi in Brand Portal in modo da poter eseguire operazioni in blocco, come la gestione dei ruoli e la condivisione di risorse in Brand Portal. **Brand Portal** è il profilo di prodotto predefinito disponibile; puoi creare più profili di prodotto e aggiungere utenti ai nuovi profili di prodotto.

>[!NOTE]
>
>Puoi accedere a [[!UICONTROL Admin Console]](https://adminconsole.adobe.com/enterprise/overview) direttamente o da Brand Portal. Se accedi a [!UICONTROL Admin Console] segui direttamente i passaggi 4-7 nella procedura seguente per aggiungere un profilo di prodotto.

1. Dalla barra degli strumenti AEM in alto, fai clic sul logo dell’Adobe per accedere agli strumenti di amministrazione.

   ![Logo AEM](assets/aemlogo.png)

1. Nel pannello Strumenti di amministrazione, fate clic su **[!UICONTROL Utenti]**.

   ![Pannello Strumenti di amministrazione](assets/admin-tools-panel-6.png)

1. In [!UICONTROL Ruoli utente] , fare clic su **[!UICONTROL Gestione]** , quindi fai clic su **[!UICONTROL Admin Console lancio]**.

   ![Admin Console lancio](assets/launch_admin_console.png)

1. Dalla barra degli strumenti nella parte superiore, fai clic su **[!UICONTROL Prodotti]**.
1. In [!UICONTROL Prodotti] pagina, [!UICONTROL Profili di prodotto] è selezionato per impostazione predefinita. Clic **[!UICONTROL Nuovo profilo]**.

   ![Aggiungi nuovo profilo prodotto](assets/admin_console_addproductprofile.png)

1. In [!UICONTROL Crea un nuovo profilo] , fornisci il nome del profilo, il nome visualizzato, la descrizione del profilo e scegli se desideri avvisare gli utenti via e-mail quando vengono aggiunti o rimossi dal profilo.

   ![Crea profilo prodotto](assets/admin_console_addaproductprofilecreatenewprofile.png)

1. Clic **[!UICONTROL Fine]**. Il gruppo di configurazione del prodotto, ad esempio **[!UICONTROL Gruppo vendite]**, viene aggiunto a Brand Portal.

   ![Profili di prodotto](assets/admin_console_productprofileadded.png)

## Aggiungere utenti a un profilo di prodotto {#add-users-to-a-product-profile}

Per aggiungere utenti a un gruppo Brand Portal, aggiungili al profilo di prodotto corrispondente (precedentemente noto come configurazioni di prodotto) in [!UICONTROL Admin Console]. Puoi aggiungere gli utenti singolarmente o in blocco.

>[!NOTE]
>
>Puoi accedere a [[!UICONTROL Admin Console]](https://adminconsole.adobe.com/enterprise/overview) direttamente o da Brand Portal. Se accedi direttamente all’Admin Console, segui i passaggi 4-7 della procedura seguente per aggiungere utenti a un profilo di prodotto.

1. Dalla barra degli strumenti nella parte superiore, fai clic sul logo dell’Experience Manager per accedere agli strumenti di amministrazione.

   ![Logo AEM](assets/aemlogo.png)

1. Nel pannello Strumenti di amministrazione, fate clic su **[!UICONTROL Utenti]**.

   ![Pannello Strumenti di amministrazione](assets/admin-tools-panel-7.png)

1. In [!UICONTROL Ruoli utente] , fare clic su **[!UICONTROL Gestione]** , quindi fai clic su **[!UICONTROL Admin Console lancio]**.

   ![Lancio [!DNL Admin Console]](assets/launch_admin_console.png)

1. Dalla barra degli strumenti nella parte superiore, fai clic su **[!UICONTROL Prodotti]**.
1. In [!UICONTROL Prodotti] pagina, [!UICONTROL Profili di prodotto] è selezionato per impostazione predefinita. Apri il profilo di prodotto a cui desideri aggiungere un utente, ad esempio, [!UICONTROL Gruppo vendite].

   ![Profili di prodotto](assets/admin_console_productprofileadded.png)

1. Per aggiungere singoli utenti al profilo di prodotto, effettua le seguenti operazioni:

   * Clic **[!UICONTROL Aggiungi utente]**.

   ![Gruppo per la mappatura del profilo di prodotto in Brand Portal](assets/admin_console_productprofilesalesgroup.png)

   * In [!UICONTROL Aggiungi utente a gruppo vendite] digitare l&#39;ID e-mail dell&#39;utente che si desidera aggiungere o selezionare l&#39;utente dall&#39;elenco di suggerimenti visualizzato durante la digitazione.

   ![Aggiungere un utente a un gruppo](assets/admin_console_addusertosalesgroup.png)

   * Fai clic su **[!UICONTROL Salva]**.



1. Per aggiungere utenti in blocco al profilo di prodotto, effettua le seguenti operazioni:

   * Scegli **[!UICONTROL puntini di sospensione (...) > Aggiungi utenti tramite CSV]**.

   ![Aggiungere utenti in blocco](assets/admin_console_addbulkusers.png)

   * In **[!UICONTROL Aggiungi utenti per CSV]** , scaricare un modello CSV o trascinare un file CSV.

   ![Aggiungi utenti per CSV](assets/admin_console_addbulkuserscsv.png)

   * Clic **[!UICONTROL Carica]**.
   Se hai aggiunto degli utenti al profilo di prodotto predefinito, ovvero Brand Portal, un messaggio e-mail di benvenuto viene inviato all’ID e-mail degli utenti che hai aggiunto. Gli utenti invitati possono accedere a Brand Portal facendo clic sul collegamento nell’e-mail di benvenuto e accedendo utilizzando un [!UICONTROL Adobe ID]. Per ulteriori informazioni, consulta [Esperienza del primo accesso](../using/brand-portal-onboarding.md).

   Gli utenti aggiunti a un profilo di prodotto personalizzato o nuovo non ricevono le notifiche e-mail.

## Fornire privilegi di amministratore agli utenti {#provide-administrator-privileges-to-users}

È possibile fornire l&#39;amministratore di sistema o il privilegio di amministratore di prodotto a un utente Brand Portal. Non fornire altri diritti amministrativi disponibili in [!UICONTROL Admin Console], ad esempio amministratore del profilo di prodotto, amministratore del gruppo di utenti e amministratore del supporto. Per ulteriori informazioni su questi ruoli, consulta [Ruoli amministrativi](https://helpx.adobe.com/enterprise/using/admin-roles.html).

>[!NOTE]
>
>Puoi accedere a [[!UICONTROL Admin Console]](https://adminconsole.adobe.com/enterprise/overview) direttamente o da Brand Portal. Se accedi a [!UICONTROL Admin Console] segui direttamente i passaggi 4-8 nella procedura seguente per aggiungere un utente a un profilo di prodotto.

1. Dalla barra degli strumenti AEM in alto, fai clic sul logo dell’Adobe per accedere agli strumenti di amministrazione.

   ![AEMLogo](assets/aemlogo.png)

1. Nel pannello Strumenti di amministrazione, fate clic su **[!UICONTROL Utenti]**.

   ![Pannello Strumenti di amministrazione](assets/admin-tools-panel-8.png)

1. In [!UICONTROL Ruoli utente] , fare clic su **[!UICONTROL Gestione]** , quindi fai clic su **[!UICONTROL Admin Console lancio]**.

   ![Admin Console lancio](assets/launch_admin_console.png)

1. Dalla barra degli strumenti nella parte superiore, fai clic su **[!UICONTROL Utenti]**.
1. In [!UICONTROL Utenti] pagina, [!UICONTROL Utenti] nella barra a sinistra è selezionato per impostazione predefinita. Fare clic sul nome utente dell&#39;utente a cui si desidera assegnare i privilegi di amministratore.

   ![Aggiungere utenti nell’Admin Console](assets/admin_console_adduseruserpage.png)

1. Nella pagina del profilo utente, individua **[!UICONTROL Diritti amministrativi]** in basso e scegliere **[!UICONTROL puntini di sospensione (...) > Modifica diritti amministratore]**.
   ![Diritti di amministrazione in Admin Console](assets/admin_console_editadminrights.png)

1. In [!UICONTROL Modifica amministratore] , selezionare System Administrator o Product Administrator.

   ![Modificare i diritti di amministratore in Admin Console](assets/admin_console_editadminrightsselection.png)

   >[!NOTE]
   >
   >Brand Portal supporta solo i ruoli Amministratore di sistema e Amministratore di prodotto.
   >
   >L&#39;Adobe consiglia di evitare di utilizzare il ruolo Amministratore di sistema, in quanto concede privilegi di amministratore a livello di organizzazione per tutti i prodotti di un&#39;organizzazione. Ad esempio, un amministratore di sistema di un’organizzazione che include tre prodotti marketing cloud dispone dell’intero set di privilegi per tutti e tre i prodotti. Solo un amministratore di sistema può configurare Experience Manager Assets in modo che le risorse possano essere pubblicate da Experience Manager Assets a Brand Portal. Per ulteriori informazioni, consulta [Configurare Experience Manager Assets con Brand Portal](../using/configure-aem-assets-with-brand-portal.md).
   >
   >Al contrario, il ruolo di amministratore di prodotto concede privilegi di amministratore solo per un prodotto specifico. Se desideri applicare un controllo di accesso più granulare in Brand Portal, utilizza il ruolo Amministratore prodotto e seleziona il prodotto come Brand Portal.

   >[!NOTE]
   >
   >Brand Portal non supporta i privilegi di amministratore del profilo di prodotto (precedentemente noto come amministratore di configurazione). Evita di assegnare a un utente i diritti di amministratore del profilo di prodotto.

1. Controlla la selezione del tipo di amministratore e fai clic su **[!UICONTROL Salva]**.

   >[!NOTE]
   >
   >Per revocare i privilegi di amministratore a un utente, apportare le modifiche appropriate nel **[!UICONTROL Modifica amministratore]** e quindi fare clic su **[!UICONTROL Salva]**.


## Gestire i ruoli utente {#manage-user-roles}

Un amministratore può modificare i ruoli per gli utenti in Brand Portal.

Oltre al ruolo Amministratore, Brand Portal supporta i seguenti ruoli:

* [!UICONTROL Visualizzatore]: gli utenti con questo ruolo possono visualizzare i file e le cartelle condivisi da un amministratore. I visualizzatori possono anche cercare e scaricare le risorse. Tuttavia, i visualizzatori non possono condividere il contenuto (file, cartelle, [!UICONTROL raccolte]) con altri utenti.
* [!UICONTROL Editor]: gli utenti con questo ruolo dispongono di tutti i privilegi di un visualizzatore. Inoltre, gli editor possono condividere i contenuti (cartelle, [!UICONTROL raccolte], collegamenti ) con altri utenti.

1. Dalla barra degli strumenti AEM in alto, fai clic sul logo dell’Adobe per accedere agli strumenti di amministrazione.

   ![AEMLogo](assets/aemlogo.png)

1. Nel pannello Strumenti di amministrazione, fate clic su **[!UICONTROL Utenti]**.

   ![Pannello Strumenti di amministrazione](assets/admin-tools-panel-9.png)

1. In [!UICONTROL Ruoli utente] pagina, la [!UICONTROL Utenti] è selezionata per impostazione predefinita. Per l’utente di cui desideri modificare il ruolo, seleziona **[!UICONTROL Editor]** o **[!UICONTROL Visualizzatore]** dal **[!UICONTROL Ruolo]** a discesa.

   ![Modifica ruoli utenti](assets/modify_user_role.png)

   Per modificare il ruolo di più utenti contemporaneamente, selezionare gli utenti e scegliere il ruolo appropriato dal **[!UICONTROL Ruolo]** a discesa.

   >[!NOTE]
   >
   >Il [!UICONTROL Ruolo] L&#39;elenco per gli utenti amministratori è disabilitato. Non puoi selezionare questi utenti per modificare i loro ruoli.


   >[!NOTE]
   >
   >Il ruolo utente è disabilitato anche se l&#39;utente è membro del gruppo Editor. Per revocare all&#39;utente i privilegi di modifica, rimuovere l&#39;utente dal gruppo Editor o modificare il ruolo dell&#39;intero gruppo in Visualizzatore.


1. Fai clic su **[!UICONTROL Salva]**. Il ruolo viene modificato per l&#39;utente corrispondente. Se hai selezionato più utenti, i ruoli di tutti gli utenti vengono modificati contemporaneamente.

   >[!NOTE]
   >
   >Le modifiche alle autorizzazioni utente si riflettono nel **[!UICONTROL Ruoli utente]** solo dopo che gli utenti hanno effettuato di nuovo l’accesso a Brand Portal.

## Gestire ruoli e privilegi del gruppo {#manage-group-roles-and-privileges}

Un amministratore può associare privilegi specifici a un [gruppo](../using/brand-portal-adding-users.md#main-pars-title-278567577) di utenti su Brand Portal. Il **[!UICONTROL Gruppi]** scheda della **[!UICONTROL Ruoli utente]** consente agli amministratori di:

* Assegnare ruoli a gruppi di utenti
* Limita i gruppi di utenti a scaricare le rappresentazioni originali dei file di immagine (.jpeg, .tiff, .png, .bmp, .gif, .pjpeg, x-portable-anymap, x-portable-bitmap, x-portable-graymap, x-portable-pixmap, x-rgb, x-xbitmap, x-xpixmap, x-icon, image/photoshop, .psd, image/vnd.adobe.photoshop) da Brand Portal.

>[!NOTE]
>
>Per le risorse condivise come collegamento, l’autorizzazione per accedere alle rappresentazioni originali dei file immagine verrà applicata in base alle autorizzazioni dell’utente che condivide le risorse.

Per modificare il ruolo e il diritto di accesso alle rappresentazioni originali per membri specifici del gruppo, effettuare le seguenti operazioni:

1. Il giorno **[!UICONTROL Ruoli utente]** , passare alla pagina **[!UICONTROL Gruppi]** scheda.
1. Selezionare i gruppi per i quali si desidera modificare i ruoli.
1. Seleziona il ruolo appropriato dalla **[!UICONTROL Ruolo]** elenco a discesa.

   Per consentire ai membri di un gruppo di avere accesso alle rappresentazioni originali dei file immagine (.jpeg, .tiff, .png, .bmp, .gif, .pjpeg, x-portable-anymap, x-portable-bitmap, x-portable-graymap, x-portable-pixmap, x-rgb, x-xbitmap, x-xpixmap, x-icon, image/photoshop, image/x-photoshop, .psd, image/vnd.adobe.photoshop) che scaricano dal portale o dal collegamento condiviso, conserva il **[!UICONTROL Accesso all&#39;originale]** selezionata per il gruppo. Per impostazione predefinita, **[!UICONTROL Accesso all&#39;originale]** viene selezionata per tutti gli utenti. Per impedire a un gruppo di utenti di accedere alle rappresentazioni originali, deseleziona l’opzione corrispondente a tale gruppo.

   ![Ruoli dei gruppi di utenti](assets/access-original-rend.png)

   >[!NOTE]
   >
   >Se un utente viene aggiunto a più gruppi e uno di questi gruppi ha delle restrizioni, le restrizioni verranno applicate a tale utente.
   >
   >Inoltre, le restrizioni per l&#39;accesso alle rappresentazioni originali dei file di immagine non si applicano agli amministratori anche se sono membri di gruppi con restrizioni.


1. Fai clic su **[!UICONTROL Salva]**. Il ruolo viene modificato per i gruppi corrispondenti.

   >[!NOTE]
   >
   >L’associazione utente-gruppo, o l’appartenenza al gruppo di un utente, viene sincronizzata in Brand Portal ogni 8 ore. Le modifiche ai ruoli utente o gruppo vengono applicate dopo l&#39;esecuzione del successivo processo di sincronizzazione.
