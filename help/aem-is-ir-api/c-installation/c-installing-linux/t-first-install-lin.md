---
title: Erstmalige Installation
description: Dieses Verfahren zeigt, wie man Image Serving zum ersten Mal unter Linux® installiert.
solution: Experience Manager
feature: Dynamic Media Classic,SDK/API
role: Developer,User
exl-id: f27e6b27-641c-4a88-9ed0-94ada9ba75a9
source-git-commit: 3be1d948ac22f907169ef09b509f1cebceaec5c4
workflow-type: tm+mt
source-wordcount: '380'
ht-degree: 0%

---

# Erstmalige Installation{#installing-for-the-first-time}

Dieses Verfahren zeigt, wie man Image Serving zum ersten Mal unter Linux® installiert.

1. Melden Sie sich mit Root-Berechtigungen bei Ihrem Serverhost an.
1. Erstellen des Ordners [!DNL /usr/local/scene7/licenses].

   Wenn die Lizenzschlüsseldatei für Image Serving und/oder Image Rendering (mit [!DNL .sc8] Dateisuffix) verfügbar ist, kopieren Sie es in diesen Ordner. Andernfalls fahren Sie mit der Installation fort und installieren Sie den Lizenzschlüssel später.
1. Dekomprimieren Sie die Tar-Datei Image Serving und entpacken Sie sie.
1. Im [!DNL Setup] Ordner, starten Sie den Installationsassistenten, indem Sie [!DNL ./install-is].

   Wenn kein Lizenzschlüssel gefunden wird, werden Anweisungen zum Abrufen einer Lizenzdatei angezeigt. Führen Sie dies an dieser Stelle aus oder fahren Sie mit der Image Serving-Installation fort und installieren Sie den Lizenzschlüssel später.
1. Wenn die Endbenutzer-Lizenzvereinbarung (EULA) angezeigt wird, lesen Sie die Lizenzvereinbarung und geben Sie `y` um fortzufahren.

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
   <td colname="col2"> <p>Das Benutzerkonto, unter dem der Image Serving-Server installiert werden soll. </p> </td>
  </tr>
  <tr> 
   <td colname="col1"> <p><span class="codeph"> Image Server Group ID [Stamm]:</span> </p> </td>
   <td colname="col2"> <p>Das Gruppenkonto, unter dem der Image Serving-Server installiert werden soll. </p> </td>
  </tr>
 </tbody>
</table>

1. Presse **[!UICONTROL Eingabe]** , um den Standardwert zu akzeptieren oder einen anderen Wert anzugeben.

   Stellen Sie sicher, dass alle angegebenen Portnummern eindeutig sind und auf diesem Host anderweitig nicht verwendet werden.

   >[!IMPORTANT]
   >
   >Wenn ein anderes Konto als der Stammordner angegeben ist, müssen Sie sicherstellen, dass die Zugriffsberechtigungen für alle Dateien und Ordner, die der Image-Server lesen und schreiben muss, korrekt eingerichtet sind, wenn diese Ordner in den Konfigurationsdateien neu konfiguriert werden.
   >
   >Image Serving ist jetzt in [!DNL /usr/local/Scene7/ImageServing]. Bestimmte Image Rendering-Inhalte werden in installiert. [!DNL /usr/local/Scene7/ImageRendering].
   >
   >Gegen Ende der Installation versucht der Installationsassistent, Image Server zu starten. Wenn kein gültiger Lizenzschlüssel gefunden wird, kann der Image-Server nicht starten. Wenn eine gültige Lizenz vorhanden ist und Image Server noch nicht gestartet ist, lesen Sie die Protokolldateien.

>[!NOTE]
>
>Wenn die Lizenz nach der Installation von Image Serving installiert ist, muss der Image-Server vor der Verwendung manuell gestartet werden.
