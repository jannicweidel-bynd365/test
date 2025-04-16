---
title: Vorwort
---

<!-- Brief Feature Description -->

<!-- Beschreibung Produkt -->
Beyond CloudConnector ist eine Microsoft Dynamics 365 Business Central Erweiterung zur Anbindung von Sharepoint, Azure Files und Azure BLOB Storage.  

Mit dieser Erweiterung können Sie zusätzliche Dateien, chaotisch oder strukturiert, direkt aus Business Central in Ihrer eigenen Microsoft Cloud speichern und verknüpfen, so dass die entsprechenden Dateien schnell und einfach aus nur einer Anwendung heraus abgerufen werden können.  

Je nach Verbindung können die in der Cloud gespeicherten Dateien unter in der Vorschau angezeigt oder direkt im Webclient heruntergeladen werden.

## <a name="storage-locations"></a>Speicherorte

Die folgenden Cloud-Speicheroptionen können in dieser Erweiterung verwendet werden:  

+ **Azure Blob Storage** 
 "Azure Blob Storage ist die Objektspeicherlösung von Microsoft für die Cloud. Blob Storage ist für die Speicherung großer Mengen unstrukturierter Daten optimiert. Unstrukturierte Daten sind Daten, die sich nicht an ein bestimmtes Datenmodell oder eine bestimmte Definition halten, wie z. B. Text- oder Binärdaten."  

    Weitere Informationen erhalten Sie auf der offiziellen Seite von Microsoft:  

[Was ist Azure Blob Storage? | Microsoft Docs](https://learn.microsoft.com/de-de/azure/storage/blobs/storage-blobs-overview)

+ **Azure Files**  
    “Azure Files bietet vollständig verwaltete Dateifreigaben in der Cloud, die über das branchenübliche SMB-Protokoll (Server Message Block), das NFS-Protokoll (Network File System) und die Azure Files REST API zugänglich sind. Azure-Dateifreigaben können gleichzeitig von Cloud- oder On-Premises-Bereitstellungen gemountet werden. SMB-Azure-Dateifreigaben sind von Windows-, Linux- und macOS-Clients aus zugänglich. NFS Azure-Dateifreigaben sind von Linux- oder macOS-Clients aus zugänglich. Darüber hinaus können SMB-Azure-Dateifreigaben auf Windows-Servern mit Azure File Sync zwischengespeichert werden, um einen schnellen Zugriff in der Nähe des Ortes zu ermöglichen, an dem die Daten verwendet werden.“  

    Weitere Informationen erhalten Sie auf der offiziellen Website von Microsoft:  

[Was ist Azure Files? | Microsoft Docs](https://learn.microsoft.com/de-de/azure/storage/files/storage-files-introduction)

+ **Sharepoint**  
    “Unternehmen verwenden Microsoft SharePoint, um Websites zu erstellen. Sie können es als sicheren Ort zum Speichern, Organisieren, Freigeben und Abrufen von Informationen von jedem Gerät aus verwenden. Alles, was Sie brauchen, ist ein Webbrowser wie Microsoft Edge, Internet Explorer, Chrome oder Firefox.“

    Weitere Informationen erhalten Sie auf der offiziellen Website von Microsoft:  

[Was ist SharePoint? - Office-Support (microsoft.com)](https://support.microsoft.com/de-de/office/was-ist-sharepoint-97b915e6-651b-43b2-827d-fb25777f446f)

Mit diesen 3 Anbindungsmöglichkeiten können Dateien nach eigenem Ermessen bequem in einem separaten Cloud-Speicher abgelegt werden. Dies hat zum einen den Vorteil, dass die eigentliche Datenbank nicht unnötig an Größe zunimmt und zum anderen, dass die
Dateien einen zentralen Speicherort haben und von überall mit allen Geräten sofort abgerufen werden können. Stehen mehrere Cloud-Dienste zur Verfügung, liegt es an Ihnen, den entsprechenden Speicherplatz einer bestimmten Entität zuzuordnen, so dass am Ende der von Ihnen priorisierte Dienst genutzt werden kann. All dies lässt sich in Business Central definieren und einrichten.

<!-- General Notes -->

<!-- :::caution -->
Das Verschieben oder Löschen von Daten im Cloud-Speicher muss unter allen Umständen verhindert werden, da eine Verbindung zu Business Central besteht und entsprechende Verknüpfungen irreparabel und damit unbrauchbar werden. Administratoren haben die Möglichkeit, Dateien, die nicht mehr mit den Datensätzen verknüpft sind, zu löschen. Dies ist z.B. der Fall, wenn eine Datei aus dem Cloud-Speicher entfernt wurde, aber noch in Business Central verlinkt ist.
<!-- ::: -->

<!-- :::info   -->  
Die Funktion **Cloud Dateisuche** wird mit jedem weiteren Suchkriterium langsamer, da jeder Begriff erneut die Datensätze inklusive aller Metadaten durchsuchen und das Teilergebnis in der Datenbank zwischenlagern muss.
<!-- ::: -->