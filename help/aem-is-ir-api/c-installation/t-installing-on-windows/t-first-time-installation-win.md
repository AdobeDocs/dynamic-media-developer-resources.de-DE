---
description: Führen Sie diese Schritte aus, um Image Serving unter Windows zum ersten Mal zu installieren.
seo-description: Führen Sie diese Schritte aus, um Image Serving unter Windows zum ersten Mal zu installieren.
seo-title: Erstmalige Installation
solution: Experience Manager
title: Erstmalige Installation
topic: Scene7 Image Serving - Image Rendering API
uuid: 3b28fbc7-6bc9-4619-8f92-c0ae610b8b30
translation-type: tm+mt
source-git-commit: 7bc7b3a86fbcdc57cfdc31745fae3afc06e44b15

---


# Erstmalige Installation{#installing-for-the-first-time}

Führen Sie diese Schritte aus, um Image Serving unter Windows zum ersten Mal zu installieren.

1. Melden Sie sich mit Administratorrechten beim Serverhost an.
1. Wenn Sie bereits eine Lizenz erhalten haben, kopieren Sie diese auf Ihren Server und führen Sie dann die Lizenzinstallation durch, indem Sie die Dublette auf die Datei klicken.

   Wenn Sie noch keine Lizenz haben, können Sie mit der Installation fortfahren und die Lizenz später installieren.
1. Extrahieren Sie den Inhalt der ZIP-Datei für die Image Serving-Distribution.
1. Führen Sie [!DNL setup]/ [!DNL setup.exe] aus, um den Installationsassistenten zu starten.
1. Klicken Sie auf &quot;Weiter&quot;, um zur Endbenutzer-Lizenzvereinbarung (EULA) zu wechseln, lesen Sie die Lizenzvereinbarung und klicken Sie auf **[!UICONTROL Ja]**.

   Das [!DNL Authentication] Dialogfeld wird als Nächstes angezeigt.
1. Wenn bereits eine Lizenz installiert ist und die Lizenzinformationen im [!DNL Authentication] Dialogfeld angezeigt werden, klicken Sie auf **[!UICONTROL Weiter]** , um fortzufahren.

   Wenn Sie keine Lizenz haben, klicken Sie auf Lizenz **[!UICONTROL anfordern]**. Im nächsten Dialogfeld wird eine der MAC-Adressen der Netzwerkschnittstellenkarte Ihres Computers angezeigt. Senden Sie diese MAC-Adresse, Ihren Firmen-Namen und das Produkt, das Sie installieren, wie von der Eingabeaufforderung angegeben per E-Mail.

   **Wichtig:** Die Lizenz basiert auf der MAC-Adresse einer der auf diesem Host installierten Netzwerkschnittstellenkarten. Wenn Sie diese Karte deaktivieren, entfernen oder ersetzen, wird die Lizenz nicht mehr als gültig erkannt. Stellen Sie sicher, dass Sie eine Lizenz für die Hardwarekonfiguration erhalten, die Sie für IS verwenden werden.

   Sie können IS ohne gültige Lizenz weiter installieren und die Lizenz später installieren. Um fortzufahren, klicken Sie auf **[!UICONTROL Zurück]** , um zum [!DNL Authentication] Dialogfeld zurückzukehren, und klicken Sie dann auf **[!UICONTROL Weiter]**.
1. Gehen Sie zur Seite &quot;Plattformserver-Administrationseinstellungen&quot;. Geben Sie bei Bedarf neue Werte ein oder übernehmen Sie die Standardwerte.

   Sie können die folgenden Elemente konfigurieren:

<table id="table_AA5D7674BBBE4AD4B373066AEF413FFD"> 
 <tbody> 
  <tr> 
   <td> <p> HTTP-Anschluss für den Plattformserver </p> </td> 
   <td> <p>HTTP-Listening-Anschluss für Image Serving und Image Rendering </p> </td> 
  </tr> 
  <tr> 
   <td> <p> Admin-Listening-Anschluss </p> </td> 
   <td> <p>Admin-Listening-Anschluss </p> </td> 
  </tr> 
  <tr> 
   <td> <p> Cache-Größe des Plattformservers in MB </p> </td> 
   <td> <p>Anfangsgröße des Hauptreaktionscache </p> </td> 
  </tr> 
  <tr> 
   <td> <p> Cache-Speicherort des Plattformservers </p> </td> 
   <td> <p>PS-Cache-Ordner </p> </td> 
  </tr> 
 </tbody> 
</table>

Die angegebenen Anschlussnummern müssen eindeutig sein und dürfen nicht von anderen Anwendungen oder Diensten verwendet werden.

Der nächste Bildschirm bietet die Möglichkeit, die ausgewählten Einstellungen zu überprüfen.
1. Klicken Sie auf **[!UICONTROL Zurück]** , um Änderungen vorzunehmen, oder auf **[!UICONTROL Weiter]** , um die Installation Beginn.
1. Klicken Sie auf **[!UICONTROL Fertig stellen]** , um den Installationsassistenten zu beenden.
