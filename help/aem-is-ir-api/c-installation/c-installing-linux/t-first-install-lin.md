---
description: Dieses Verfahren zeigt, wie Image Serving unter Linux zum ersten Mal installiert wird.
seo-description: Dieses Verfahren zeigt, wie Image Serving unter Linux zum ersten Mal installiert wird.
seo-title: Erstmalige Installation
solution: Experience Manager
title: Erstmalige Installation
topic: Scene7 Image Serving - Image Rendering API
uuid: 6a9a6dd2-2c69-447a-9628-eba08dc4f6c8
translation-type: tm+mt
source-git-commit: c5b68038fa5980c7051fae916520b40e17890a7f

---


# Erstmalige Installation{#installing-for-the-first-time}

Dieses Verfahren zeigt, wie Image Serving unter Linux zum ersten Mal installiert wird.

1. Melden Sie sich mit Stammberechtigungen beim Serverhost an.
1. Erstellen Sie den Ordner [!DNL /usr/local/scene7/licenses].

   Wenn die Lizenzschlüssel-Datei Image Serving und/oder Image Rendering (mit [!DNL .sc8] Dateisuffix) verfügbar ist, kopieren Sie sie in diesen Ordner. Andernfalls fahren Sie mit der Installation fort und installieren Sie den Lizenzschlüssel später.
1. Dekomprimieren Sie die Image Serving-Distribution-Tar-Datei und entfernen Sie sie.
1. Führen Sie [!DNL ./install-is]den Installationsassistenten aus, der sich im [!DNL Setup] Ordner befindet.

   Wenn kein Lizenzschlüssel gefunden wird, werden Anweisungen zum Abrufen einer Lizenzdatei angezeigt. Führen Sie dies an dieser Stelle aus oder fahren Sie mit der Image Serving-Installation fort und installieren Sie den Lizenzschlüssel später.
1. Wenn die Endbenutzer-Lizenzvereinbarung (EULA) angezeigt wird, lesen Sie die Lizenzvereinbarung und geben Sie dann ein, `y` um fortzufahren.

   Das Installationsprogramm zeigt die in der folgenden Tabelle aufgeführten Eingabeaufforderungen an.

<table id="table_0E7B673CAD8E4C5EB72F8283A0DDEFC8"> 
 <tbody> 
  <tr> 
   <td colname="col1"> <p><span class="codeph"> Haupt-Listening-Anschluss [8080]:</span> </p> </td> 
   <td colname="col2"> <p>HTTP-Listening-Anschluss für Image Serving und Image Rendering. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p><span class="codeph"> Admin-Listening-Anschluss [8083]:</span> </p> </td> 
   <td colname="col2"> <p>Überwachungsanschluss des Administrators. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p><span class="codeph"> Maximale HTTP-Cache-Größe (MB) [2000]:</span> </p> </td> 
   <td colname="col2"> <p>Anfangsgröße des Hauptreaktionscache. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p><span class="codeph"> Cache-Stammordner [/usr/local/scene7/ImageServing/cache]:</span> </p> </td> 
   <td colname="col2"> <p>PS-Cache-Ordner. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p><span class="codeph"> Image Server Owner ID [root]:</span> </p> </td> 
   <td colname="col2"> <p>Das Benutzerkonto, unter dem Image Serving-Server installiert werden sollen. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p><span class="codeph"> Image-Server-Gruppen-ID [Stammordner]:</span> </p> </td> 
   <td colname="col2"> <p>Das Gruppenkonto, unter dem Image Serving-Server installiert werden sollen. </p> </td> 
  </tr> 
 </tbody> 
</table>

1. Drücken Sie die **[!UICONTROL Eingabetaste]** , um den Standardwert anzunehmen oder einen anderen Wert anzugeben.

   Vergewissern Sie sich, dass alle angegebenen Anschlussnummern eindeutig sind und auf diesem Host nicht anders verwendet werden.

   **Wichtig: **Wenn ein anderes Konto als Root angegeben ist, müssen Sie sicherstellen, dass die Zugriffsberechtigungen für alle Dateien und Ordner, die der Image-Server lesen und/oder schreiben muss, korrekt eingerichtet sind, wenn diese Ordner in den Konfigurationsdateien neu konfiguriert wurden.
>Image Serving ist jetzt auf installiert [!DNL /usr/local/Scene7/ImageServing]. Bestimmte Bildwiedergabeinhalte werden installiert [!DNL /usr/local/Scene7/ImageRendering].
>
>Gegen Ende der Installation versucht der Installationsassistent, Image Server Beginn. Wenn kein gültiger Lizenzschlüssel gefunden wird, kann der Image-Server keinen Beginn ausführen. Wenn eine gültige Lizenz vorhanden ist und Image Server immer noch nicht gestartet wird, lesen Sie die Protokolldateien.
>[!NOTE]
Wenn die Lizenz nach der Installation von Image Serving installiert wurde, muss der Image-Server vor der Verwendung manuell gestartet werden.
>
>
>

