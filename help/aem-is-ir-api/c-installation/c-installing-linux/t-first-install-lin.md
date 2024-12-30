---
title: Erstmalige Installation
description: Dieses Verfahren zeigt, wie Sie Image Serving zum ersten Mal auf Linux® installieren.
solution: Experience Manager
feature: Dynamic Media Classic,SDK/API
role: Developer,User
exl-id: f27e6b27-641c-4a88-9ed0-94ada9ba75a9
source-git-commit: 3be1d948ac22f907169ef09b509f1cebceaec5c4
workflow-type: tm+mt
source-wordcount: '383'
ht-degree: 0%

---

# Erstmalige Installation{#installing-for-the-first-time}

Dieses Verfahren zeigt, wie Sie Image Serving zum ersten Mal auf Linux® installieren.

1. Melden Sie sich bei Ihrem Serverhost mit Root-Berechtigungen an.
1. Erstellen Sie die [!DNL /usr/local/scene7/licenses].

   Wenn die Lizenzschlüsseldatei für Image-Serving und/oder Image-Rendering (mit [!DNL .sc8] Dateiendung) verfügbar ist, kopieren Sie sie in diesen Ordner. Fahren Sie andernfalls mit der Installation fort und installieren Sie den Lizenzschlüssel später.
1. Dekomprimieren und entpacken Sie die TAR-Datei der Image-Serving-Verteilung.
1. Starten Sie im [!DNL Setup] den Installationsassistenten, indem Sie [!DNL ./install-is] ausführen.

   Wenn kein Lizenzschlüssel gefunden wird, wird eine Anleitung zum Abrufen einer Lizenzdatei angezeigt. Tun Sie dies zu diesem Zeitpunkt oder fahren Sie mit der Image-Serving-Installation fort und installieren Sie den Lizenzschlüssel später.
1. Wenn der Endbenutzer-Lizenzvertrag (EULA) angezeigt wird, lesen Sie den Lizenzvertrag durch und geben Sie dann `y` ein, um fortzufahren.

   Das Installationsprogramm zeigt die in der folgenden Tabelle aufgeführten Eingabeaufforderungen an.

<table id="table_0E7B673CAD8E4C5EB72F8283A0DDEFC8"> 
 <tbody> 
  <tr> 
   <td colname="col1"> <p><span class="codeph"> Haupt-Listening-Port [8080]:</span> </p> </td>
   <td colname="col2"> <p>Haupt-HTTP-Überwachungs-Port für Bildbereitstellung und Bild-Rendering. </p> </td>
  </tr> 
  <tr> 
   <td colname="col1"> <p><span class="codeph"> Admin-Listening-Port [8083]:</span> </p> </td> 
   <td colname="col2"> <p>Lauschender Port des Administrators. </p> </td>
  </tr> 
  <tr> 
   <td colname="col1"> <p><span class="codeph"> Maximale HTTP-Cache-Größe (MB) [2000]:</span> </p> </td> 
   <td colname="col2"> <p>Anfangsgröße des Hauptantwort-Caches. </p> </td>
  </tr>
  <tr> 
   <td colname="col1"> <p><span class="codeph"> Cache-Stammordner [/usr/local/scene7/ImageServing/cache]:</span> </p> </td> 
   <td colname="col2"> <p>PS-Cache-Ordner. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p>Besitzer-ID des <span class="codeph">-Bildservers [root]:</span> </p> </td>
   <td colname="col2"> <p>Das Benutzerkonto, unter dem der Image-Serving-Server installiert werden soll. </p> </td>
  </tr>
  <tr> 
   <td colname="col1"> <p><span class="codeph"> Image-Server-Gruppen-ID [root]:</span> </p> </td>
   <td colname="col2"> <p>Das Gruppenkonto, unter dem der Image Serving-Server installiert werden soll. </p> </td>
  </tr>
 </tbody>
</table>

1. Drücken Sie **[!UICONTROL Eingabetaste]**, um den Standardwert zu übernehmen oder einen anderen Wert festzulegen.

   Stellen Sie sicher, dass alle angegebenen Portnummern eindeutig sind und nicht anderweitig auf diesem Host verwendet werden.

   >[!IMPORTANT]
   >
   >Wenn ein anderes Konto als das Stammkonto angegeben wird, müssen Sie sicherstellen, dass die Zugriffsberechtigungen für alle Dateien und Ordner, die der Bildserver lesen und schreiben muss, korrekt eingerichtet sind, wenn diese Ordner in den Konfigurationsdateien neu konfiguriert werden.
   >
   >Image Serving ist jetzt in [!DNL /usr/local/Scene7/ImageServing] installiert. Bestimmte Inhalte zum Rendern von Bildern werden in [!DNL /usr/local/Scene7/ImageRendering] installiert.
   >
   >Gegen Ende der Installation versucht der Installationsassistent, Image Server zu starten. Wenn kein gültiger Lizenzschlüssel gefunden wird, kann der Image-Server nicht gestartet werden. Wenn eine gültige Lizenz vorhanden ist und der Image-Server immer noch nicht gestartet wird, sehen Sie sich die Protokolldateien an.

>[!NOTE]
>
>Wenn die Lizenz nach der Installation von Image Serving installiert wird, muss der Image-Server vor der Verwendung manuell gestartet werden.
