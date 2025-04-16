---
title: "Azure Blob Storage"
---

# <a name="set-up-for-azure-blob-storage"></a>Azure Blob Storage als Cloud-Speicher einrichten

In diesem Kapitel wird beschrieben, wie Sie Ihr Business Central (mithilfe von BEYOND CloudConnector) mit Azure Blob Storage verbinden.  
Die Anbindung von Azure Blob Storage ermöglicht Ihnen den direkten Zugriff und die Bearbeitung von in der Cloud gespeicherten Dateien, ohne Business Central verlassen zu müssen.  

>[!NOTE]  
>**Berechtigungen in Microsoft Azure erforderlich**  
Für die nachfolgenden Beschreibungen sind Administratorberechtigungen in Microsoft Azure erforderlich. Für die Einrichtung der Verbindung müssen dazu berechtigt sein, Speicherkonten und Container zu erstellen sowie SAS-Token zu erstellen. Wenn Sie Hilfe bei der Einrichtung benötigen oder diesbezüglich Fragen haben, können Sie uns gern unter 
<a href="mailto:info@beyondit.gmbh?cc=sascha.fischer@beyondit.gmbh&amp;subject=Azure Blob Storage als Cloud-Speicher einrichten">info@beyondit.gbmh</a> kontaktieren.  

Führen Sie die nachfolgenden Schritte durch, um Azure Blob Storage in Business Central anzubinden:  

Bitte laden Sie die Datei unter dem nachfolgenden Link herunter:  
<a href="http://docs.beyond365.de/de-DE/cloudconnector/assets/de_DE-CloudConnectorAzureBlobStorageSetup.pdf" download>
  <button>Download</button>
</a>
<a href="http://docs.beyond365.de/de-DE/cloudconnector/assets/de_DE-CloudConnectorAzureBlobStorageSetup.pdf">PDF-Datei herunterladen</a>

Führen Sie die nachfolgenden Schritte durch, um Azure Blob Storage in Business Central anzubinden:  

+ [Speicherkonto in Microsoft Azure erstellen](#create-storage-account)
+ [Shared Access Signatures erstellen](#create-sas)
+ [CloudConnector mit Azure Blob Storage in Business Central anbinden](#connect-cloudconnector-in-business-central)

## <a name="create-storage-account"></a>Speicherkonto in Microsoft Azure erstellen

In diesem Abschnitt wird beschrieben, wie Sie ein Speicherkonto in Microsoft Azure erstellen. Das Speicherkonto stellt einen eindeutigen Namespace für Ihre Azure Storage-Daten bereit, auf den von jedem Ort der Welt aus über HTTP oder HTTPS zugegriffen werden kann. Daten in Ihrem Speicherkonto sind dauerhaft und hochverfügbar, sicher und extrem skalierbar.  

1. Öffnen Sie die Webseite [http://www.portal.azure.com/](http://www.portal.azure.com/) und melden Sie sich an.  
1. Klicken Sie in der Menüleiste von Microsoft Azure auf den Menüpunkt **Speicherkonten**.  
    ![microsoft-azure-new-storage-account](../assets/microsoft-azure-new-storage-account.png)  
1. Klicken Sie in der Menüleiste auf **Erstellen**.  
1. Vervollständigen Sie die erforderlichen Informationen zur Erstellung eines neuen Speicherkontos. Wir empfehlen, das Speicherkonto mit dem Namen **beyondcloudconnector** zu versehen. Da die Speicherkontoeinstellungen maßgeblich von den Richtlinien Ihres Unternehmens abhängen, geben wir Ihnen keine Werte vor. Weitere Informationen zu Speicherkontoeinstellungen und wie Sie ein Speicherkonto erstellen, erhalten Sie in der Hilfe zu Microsoft Azure unter dem Kapitel [Speicherkonto erstellen](https://learn.microsoft.com/de-de/azure/storage/common/storage-account-create?tabs=azure-portal).  
1. Klicken Sie für das Speicherkonto unter dem Menüpunkt **Einstellungen** auf **Endpunkte**.  
1. Kopieren Sie den Wert für den **Dateidienst** und tragen Sie diesen in die PDF-Datei unter dem Feld **Konto-URL** ein.  
1. Erstellen Sie einen Container für das Speicherkonto.  
1. Tragen Sie den Namen des erstellten Containers in die PDF-Datei unter dem Feld **Freigabename** ein. 

Sie haben ein neues Speicherkonto mit einem Container erstellt. Für die Einrichtung des Cloudspeichers fehlen noch zwei Shared Access Signatures (SAS). Die SAS werden unter dem Abschnitt [Shared Access Signatures erstellen](#create-sas) erstellt.  

## <a name="create-sas"></a>Shared Access Signatures erstellen

In diesem Abschnitt wird beschrieben, wie Sie die beiden Shared Access Signatures (SAS) erstellen zur Einrichtung von Azure Blob Storage für BEYOND CloudConnector erstellen.  

1. Öffnen Sie die Webseite [http://www.portal.azure.com/](http://www.portal.azure.com/) und melden Sie sich an.  
1. Klicken Sie in der Menüleiste von Microsoft Azure auf den Menüpunkt **Speicherkonten**.  
1. Wählen Sie das Speicherkonto aus, das Sie im Schritt [Speicherkonto in Microsoft Azure erstellen](#create-storage-account) erstellt haben.  
1. Klicken Sie in der Menüleiste unter dem Bereich **Sicherheit + Netzwerkbetrieb** auf **Shared Access Signature**.  
    ![microsoft-azure-sas](../assets/microsoft-azure-sas.png)  
1. Aktivieren Sie unter dem Bereich **Zugelassene Berechtigungen** alle Berechtigungen für die SAS.  
1. Generieren Sie die SAS und tragen Sie diese in das PDF-Dokument unter dem Feld **SAS Token** ein.  
1. Generieren Sie anschließend erneut eine SAS. Bei dieser SAS deaktivieren Sie alle Kontrollkästchen unter dem Bereich **Zugelassene Berechtigungen** mit Ausnahme der Berechtigung **Lesezugriff**.  
1. Kopieren Sie die Zeichenfolge der SAS (Lesezugriff) in die PDF-Datei in das Feld **Lesezugriff SAS-Token**.  

Sie haben die SAS erstellt.  

## <a name="connect-cloudconnector-in-business-central"></a>CloudConnector mit Azure Blob Storage in Business Central anbinden

In diesem Abschnitt wird beschrieben, wie Sie Azure Blob Storage über Beyond CloudConnector in Microsoft Business Central anbinden.  

Um Azure Blob Storage über die Extension Beyond CloudConnector in Microsoft Dynamics 365 Business Central anzubinden, gehen Sie wie folgt vor:  

1. Öffnen Sie Ihr Business Central und die PDF-Datei mit den gesammelten Daten.  
1. Rufen Sie aus dem Rollencenter die Suchfunktion auf (**ALT+Q**) 🔍.  
1. Suchen Sie nach der Seite **[Cloud Anwendungen](https://businesscentral.dynamics.com/?page=70838580)** und klicken Sie auf das entsprechende Suchergebnis.  
1. Die Seite **Cloud Anwendungen** wird angezeigt.  
1. Um Azure Blob Storage an ihr Business Central anzubinden, klicken Sie in der Menüleiste auf **Neu**.  
1. Die Seite **Cloud Anwendung** wird angezeigt.  
    ![connect-azure-files](../assets/connect-azure-blob-storage.png)  
1. Geben Sie im Feld **Code** den Wert **Azure Blob Storage** an.  
1. Im Feld **Anwendungsart** wählen Sie aus dem Dropdownmenü den Wert **Azure Blob Storage** aus.  
1. Im Feld **Beschreibung** können Sie eine Beschreibung für die neue Cloud-Anwendung eingeben.  
1. Über den Schieberegler **Dateilöschung erlaubt** steuern Sie, ob in der Cloud gespeicherte Dateien über Business Central gelöscht werden können.  
1. Öffnen Sie die PDF-Datei für die Einrichtung von Azure Blob Storage, die Sie in den vorigen Abschnitten mit Informationen gefüllt haben, und übertragen Sie die Werte in die entsprechenden Felder in Business Central.  

Sie haben Azure Blob Storage an Microsoft Dynamics 365 Business Central angebunden.  
Für eine vollständige Einrichtung müssen Sie noch die Tabellen definieren, auf denen die Dropzones zur Ablage von Dateien aus Business Central in Azure Blob Storage angezeigt werden sollen. Weitere Informationen zur Einrichtung von Dropzones erhalten Sie unter dem Kapitel [Dropzone einrichten](set-up-dropzone.md).  

Sie können auch eine automatische Berichtsarchivierung einrichten. Weitere Informationen dazu finden Sie unter dem Kapitel [Berichtsarchivierung einrichten](set-up-report-archive.md).  

