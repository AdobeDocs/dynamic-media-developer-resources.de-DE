---
description: Verwenden Sie diese Schritte, um Image Serving zum ersten Mal unter Windows zu installieren.
solution: Experience Manager
title: Erstmalige Installation
feature: Dynamic Media Classic,SDK/API
role: Developer,User
exl-id: 4e34d78c-1b5b-45cf-acc5-ff12cbc6ed01
source-git-commit: 206e4643e3926cb85b4be2189743578f88180be7
workflow-type: tm+mt
source-wordcount: '380'
ht-degree: 0%

---

# Erstmalige Installation{#installing-for-the-first-time}

Verwenden Sie diese Schritte, um Image Serving zum ersten Mal unter Windows zu installieren.

1. Melden Sie sich mit Administratorrechten bei Ihrem Serverhost an.
1. Wenn Sie bereits eine Lizenz erhalten haben, kopieren Sie sie auf Ihren Server und führen Sie dann die Lizenzinstallation durch einen Doppelklick auf die Datei aus.

   Wenn Sie noch keine Lizenz haben, können Sie mit der Installation fortfahren und die Lizenz später installieren.
1. Extrahieren Sie den Inhalt der Zip-Datei für die Image Serving-Distribution.
1. Führen Sie [!DNL setup]/ [!DNL setup.exe] aus, um den Installationsassistenten zu starten.
1. Klicken Sie auf &quot;Weiter&quot;, um zur Endbenutzer-Lizenzvereinbarung (EULA) zu wechseln, lesen Sie die Lizenzvereinbarung und klicken Sie auf **[!UICONTROL Ja]**.

   Das Dialogfeld [!DNL Authentication] wird als Nächstes angezeigt.
1. Wenn bereits eine Lizenz installiert ist und die Lizenzinformationen im Dialogfeld [!DNL Authentication] angezeigt werden, klicken Sie auf **[!UICONTROL Weiter]**, um fortzufahren.

   Wenn Sie keine Lizenz haben, klicken Sie auf **[!UICONTROL Lizenz anfordern]**. Im nächsten Dialogfeld wird eine der MAC-Adressen der Netzwerkschnittstellenkarte Ihres Computers angezeigt. Senden Sie eine E-Mail an diese MAC-Adresse, Ihren Firmennamen und das Produkt, das Sie installieren, wie von der Eingabeaufforderung angegeben.

   **Wichtig:** Die Lizenz basiert auf der MAC-Adresse einer der auf diesem Host installierten Netzwerkschnittstellenkarten. Wenn Sie diese Karte deaktivieren, entfernen oder ersetzen, wird die Lizenz nicht mehr als gültig anerkannt. Stellen Sie sicher, dass Sie eine Lizenz für die Hardware-Konfiguration erhalten, die Sie für IS verwenden werden.

   Sie können IS ohne gültige Lizenz weiterhin installieren und die Lizenz später installieren. Um fortzufahren, klicken Sie auf **[!UICONTROL Zurück]**, um zum Dialogfeld [!DNL Authentication] zurückzukehren, und klicken Sie dann auf **[!UICONTROL Weiter]**.
1. Gehen Sie zur Seite &quot;Platform Server Admin Settings&quot;. Geben Sie bei Bedarf neue Werte ein oder übernehmen Sie die Standardeinstellungen.

   Sie können die folgenden Elemente konfigurieren:

<table id="table_AA5D7674BBBE4AD4B373066AEF413FFD"> 
 <tbody> 
  <tr> 
   <td> <p> HTTP-Verbindungsanschluss für Platform Server </p> </td> 
   <td> <p>HTTP-Haupt-Listening-Anschluss für Image Serving und Image Rendering </p> </td> 
  </tr> 
  <tr> 
   <td> <p> Admin-Listening-Port </p> </td> 
   <td> <p>Admin-Listening-Port </p> </td> 
  </tr> 
  <tr> 
   <td> <p> Server-Cache-Größe des Platform-Servers in MB </p> </td> 
   <td> <p>Anfangsgröße des Hauptantwort-Cache </p> </td> 
  </tr> 
  <tr> 
   <td> <p> Speicherort des Platform Server-Cache </p> </td> 
   <td> <p>PS-Cache-Ordner </p> </td> 
  </tr> 
 </tbody> 
</table>

Die angegebenen Portnummern müssen eindeutig sein und dürfen nicht von anderen Anwendungen oder Diensten verwendet werden.

Der nächste Bildschirm bietet die Möglichkeit, die ausgewählten Einstellungen zu überprüfen.
1. Klicken Sie auf **[!UICONTROL Zurück]**, um Änderungen vorzunehmen, oder klicken Sie auf **[!UICONTROL Weiter]**, um die Installation zu starten.
1. Klicken Sie auf **[!UICONTROL Beenden]** , um den Installationsassistenten zu beenden.
