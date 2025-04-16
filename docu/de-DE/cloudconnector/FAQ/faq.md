---
title: "FAQ"
---

# <a name="faq"></a>FAQ

In diesem Bereich gehen wir auf häufig gestellte Fragen zu BeyondCloudConnector ein.  

Wenn Sie eine Frage haben, die nicht in diesem Kapitel aufgeführt ist, kontaktieren Sie uns unter 
<a href="mailto:info@beyondit.gmbh?cc=sascha.fischer@beyondit.gmbh&amp;subject=Frage zu BeyondCloudConnector">info@beyondit.gbmh</a>.  

<br>

## <a name="how-to-set-up-user-permissions"></a>Ich habe mehrere neue Benutzer, die BeyondCloudConnector verwenden sollen. Wie stelle ich die Benutzerberechtigungen ein?

Sie haben mehrere Optionen zur Erteilung von Benutzerberechtigungen:  

Sie können die Berechtigungen eines vorhandenen Benutzers für den neuen Benutzer kopieren oder gleichzeitig alle Berechtigungen für die Anzeige der Dropzone/s und Dateivorschau definieren. Weitere Informationen dazu erhalten Sie unter dem Kapitel [Benutzer einrichten](../setup/set-up-users.md).  

<br>

## <a name="no-connection"></a>BeyondCloudConnector konnte in der Vergangenheit eine Verbindung zum Cloud-Speicher herstellen, dies funktioniert aber jetzt nicht mehr. Was soll ich tun?

Überprüfen Sie, ob die Cloud-Anwendung korrekt eingerichtet ist. Möglicherweise ist ein geheimer Schlüssel (für Sharepoint-Einrichtungen: [Geheimen Schlüssel erzeugen und kopieren](../setup/set-up-for-sharepoint.md#create-and-copy-secret)) oder die Shared Access Signature in Mircosoft Azure abgelaufen. Weitere Informationen zu diesem Thema erhalten Sie für Azure Files-Einrichtungen unter [Einrichten > Azure Files als Cloud-Speicher einrichten > Shared Access Signatures erstellen](../setup/set-up-for-azure-files.md#create-sas) und für Azure Blob Storage-Einrichtungen unter [Einrichten > Azure Blob Storage als Cloud-Speicher einrichten > Shared Access Signatures erstellen](../setup/set-up-for-azure-blob-storage.md#create-sas).  

Sollte das Problem fortbestehen, kontaktieren Sie uns unter 
<a href="mailto:info@beyondit.gmbh?cc=sascha.fischer@beyondit.gmbh&amp;subject=Problem mit der Verbindung (BeyondCloudConnector)">info@beyondit.gbmh</a>.  

<br>

## <a name="license-expired"></a>Mir wird angezeigt, dass meine Lizenz abgelaufen ist. Was muss ich tun? 

Wenn Sie BeyondCloudConnector weiter verwenden möchten, müssen Sie eine Lizenz oder mehrere Lizenzen erwerben. Weitere Informationen zu aktuellen Preisen sowie laufende Marketingkampagnen oder Sonderangebote erhalten Sie auf unserer Webseite [https://www.beyond-cloudconnector.de/](https://www.beyond-cloudconnector.de/).  

Falls Sie BeyondCloudConnector nicht weiter verwenden möchten, können Sie die App über die Erweiterungsverwaltung deinstallieren.  

<br>

## <a name="which-license-is-best"></a>Welches Lizenzmodell eignet sich für mein Unternehmen?

Wir bieten verschiedene Lizenzmodelle an. 
Die Lizenzierung erfolgt nach der Anzahl der Benutzer im System. Es werden <u>alle Benutzer</u> des Systems gezählt, unabhängig davon, ob diese Zugriff auf BeyondCloudConnector haben.  

Weitere Informationen zu aktuellen Preisen sowie laufende Marketingkampagnen oder Sonderangebote erhalten Sie auf unserer Webseite [https://www.beyond-cloudconnector.de/](https://www.beyond-cloudconnector.de/). 

<br>

## <a name="new-version"></a>Ich wurde darüber informiert, dass eine neue Version von BeyondCloudConnector verfügbar ist. Wie aktualisiere ich die App?  

Die neue Version der Anwendung wird mit jedem Update von Microsoft automatisch aktualisiert. Falls Sie nicht auf das nächste Update von Microsoft warten möchten, können Sie die Anwendung manuell aktualisieren. Um die Anwendung manuell zu aktualisieren, gehen Sie wie unter dem Abschnitt [Update zur neuesten Version des CloudConnectors](update-your-cloudconnector-version.md) beschrieben vor.  

<br>

## <a name="which-cloud-storage-is-the-cheapest"></a>Welcher Cloud-Speicher ist am günstigsten?

Standardmäßig ist in einem Office 365-Abonnement Speicherplatz für **SharePoint Online** enthalten. 
Sie müssen also keine Extrakosten für Speicherplatz bezahlen. 
Die Speichergröße von Sharepoint hängt von den Lizenzen in Ihrer Organisation ab. 
Die Größe des Speichers für Sharepoint können Sie im Sharepoint Admin Center ablesen.  

Wenn Sie Azure Files oder Azure Blob Storage als Cloudspeicher auswählen fallen je nach Größe und Eigenschaften des Speichervolumens zusätzlich Kosten an. Weitere Informationen zu den verbundenen Kosten für Speicherplatz erhalten Sie unter:  

[Informationen zu Preisen für Sharepoint Online](https://www.microsoft.com/de-de/microsoft-365/sharepoint/compare-sharepoint-plans)  
[Informationen zu Preisen für Azure Files](https://azure.microsoft.com/de-de/pricing/details/storage/files/)  
[Informationen zu Preisen für Azure Blob Storage](https://azure.microsoft.com/de-de/pricing/details/storage/blobs/)  

<br>

## <a name="edit-structure"></a>Ich möchte die Ordnerstruktur in Sharepoint/Azure Files oder Azure Blob Storage ändern. Muss ich dabei etwas beachten?  

Ja, Sie sollten die Dateien vor der Veränderung der Struktur sichern. Löschen Sie dann die Daten aus Business Central und dem Cloudspeicher und bauen Sie die Struktur dann neu auf. Durch die Veränderung der Ordnerstruktur im Cloudspeicher gehen die Verbindungen zwischen Business Central und dem Cloudspeicher verloren, d.h. Sie müssen die Dateien neu einspielen, damit die Verbindungen zwischen Business Central und dem Cloudspeicher erstellt werden.  

<br>

## <a name="import-files-from-onpremise-to-cloud"></a>Ich möchte Datei-Anhänge von einer OnPremise-Umgebung in die Cloud migrieren. Ist das möglich und wenn ja wie?  

Ja, das ist möglich. Wir haben extra für diesen Fall eine Codeunit programmiert, die es Ihnen ermöglicht, die Dateianhänge einer OnPremise-Umgebung zu exportieren, damit Sie diese über den CloudConnector in die Cloud hochladen können. Beachten Sie dabei, dass zum Zeitpunkt des Dateiexports noch kein Cloudspeicher im **Beyond CloudConnector** eingerichtet sein darf.  

Laden Sie sich die Dateiexport-Codeunit herunter: [Codeunit zum Export von Dateien](https://github.com/byndit/BeyondCloudConnector-Example/blob/main/BeyondCC/src/ExportData/ExportfromAttachments.Codeunit.al)  

Exportieren Sie die Dateien und laden Sie diese anschließend in Azure Files hoch.  
Gehen Sie dann wie unter dem Kapitel [Dateien aus Azure Files importieren](../setup/set-up-for-azure-files.md#import-files-from-azure-files) beschrieben vor. Beachten Sie dabei, dass die JSON-Datei ebenfalls in Azure Files hochgeladen werden muss.  

Anschließend können Sie die Dateien auch in einen anderen Cloudspeicher verschieben (beispielsweise Sharepoint oder Azure Blob). Gehen Sie dazu wie unter dem Kapitel [Dateien in einen anderen Cloud-Speicher verschieben](../features/move-files-to-different-storage.md) beschrieben vor.  

<br>