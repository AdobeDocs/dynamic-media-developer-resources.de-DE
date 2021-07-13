---
description: Dieses Verfahren zeigt, wie man Image Serving zum ersten Mal unter Linux installiert.
solution: Experience Manager
title: Erstmalige Installation
feature: Dynamic Media Classic,SDK/API
role: Developer,User
exl-id: f27e6b27-641c-4a88-9ed0-94ada9ba75a9
source-git-commit: 206e4643e3926cb85b4be2189743578f88180be7
workflow-type: tm+mt
source-wordcount: '387'
ht-degree: 0%

---

# Erstmalige Installation{#installing-for-the-first-time}

Dieses Verfahren zeigt, wie man Image Serving zum ersten Mal unter Linux installiert.

1. Melden Sie sich mit Root-Berechtigungen bei Ihrem Serverhost an.
1. Erstellen Sie den Ordner [!DNL /usr/local/scene7/licenses].

   Wenn die Lizenzschlüsseldatei Image Serving und/oder Image Rendering (mit dem Dateisuffix [!DNL .sc8] ) verfügbar ist, kopieren Sie sie in diesen Ordner. Andernfalls fahren Sie mit der Installation fort und installieren Sie den Lizenzschlüssel später.
1. Dekomprimieren Sie die Tar-Datei Image Serving und entpacken Sie sie.
1. Führen Sie [!DNL ./install-is] im Ordner [!DNL Setup] aus, um den Installationsassistenten zu starten.

   Wenn kein Lizenzschlüssel gefunden wird, werden Anweisungen zum Abrufen einer Lizenzdatei angezeigt. Führen Sie dies an dieser Stelle aus oder fahren Sie mit der Image Serving-Installation fort und installieren Sie den Lizenzschlüssel später.
1. Wenn die Endbenutzer-Lizenzvereinbarung (EULA) angezeigt wird, lesen Sie die Lizenzvereinbarung und geben Sie `y` ein, um fortzufahren.

   Das Installationsprogramm zeigt die in der folgenden Tabelle aufgelisteten Eingabeaufforderungen an.

<table id="table_0E7B673CAD8E4C5EB72F8283A0DDEFC8"> 
 <tbody> 
  <tr> 
   <td colname="col1"> <p><span class="codeph"> Hauptüberwachungsanschluss [8080]:</span> </p> </td> 
   <td colname="col2"> <p>Haupt-HTTP-Listening-Anschluss für Image Serving und Image Rendering. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p><span class="codeph"> Admin-Listening-Anschluss [8083]:</span> </p> </td> 
   <td colname="col2"> <p>Admin-Listening-Anschluss. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p><span class="codeph"> Maximale HTTP-Cache-Größe (MB) [2000]:</span> </p> </td> 
   <td colname="col2"> <p>Anfangsgröße des Hauptantwort-Cache. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p><span class="codeph"> Cache Root Folder [/usr/local/scene7/ImageServing/cache]:</span> </p> </td> 
   <td colname="col2"> <p>PS-Cache-Ordner. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p><span class="codeph"> Image Server Owner ID [Stamm]:</span> </p> </td> 
   <td colname="col2"> <p>Das Benutzerkonto, unter dem Image Serving-Server installiert werden sollen. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p><span class="codeph"> Image Server Group ID [Stamm]:</span> </p> </td> 
   <td colname="col2"> <p>Das Gruppenkonto, unter dem Image Serving-Server installiert werden sollen. </p> </td> 
  </tr> 
 </tbody> 
</table>

1. Drücken Sie **[!UICONTROL Enter]**, um den Standardwert zu akzeptieren oder einen anderen Wert anzugeben.

   Stellen Sie sicher, dass alle angegebenen Portnummern eindeutig sind und auf diesem Host anderweitig nicht verwendet werden.

   >[!IMPORTANT]
   >
   >Wenn ein anderes Konto als der Stammordner angegeben ist, müssen Sie sicherstellen, dass die Zugriffsberechtigungen für alle Dateien und Ordner, die der Image-Server lesen und/oder schreiben muss, korrekt eingerichtet sind, wenn diese Ordner in den Konfigurationsdateien neu konfiguriert werden.
   >
   >Image Serving ist jetzt auf [!DNL /usr/local/Scene7/ImageServing] installiert. Bestimmte Image Rendering-Inhalte werden in [!DNL /usr/local/Scene7/ImageRendering] installiert.
   >
   >Gegen Ende der Installation versucht der Installationsassistent, Image Server zu starten. Wenn kein gültiger Lizenzschlüssel gefunden wird, kann der Image-Server nicht starten. Wenn eine gültige Lizenz vorhanden ist und Image Server noch nicht gestartet ist, lesen Sie die Protokolldateien.

>[!NOTE]
>
>Wenn die Lizenz nach der Installation von Image Serving installiert ist, muss der Image-Server vor der Verwendung manuell gestartet werden.
