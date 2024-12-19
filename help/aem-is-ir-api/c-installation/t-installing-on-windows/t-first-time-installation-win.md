---
title: Erstmalige Installation
description: Führen Sie diese Schritte aus, um Image Serving zum ersten Mal unter Windows zu installieren.
solution: Experience Manager
feature: Dynamic Media Classic,SDK/API
role: Developer,User
exl-id: 4e34d78c-1b5b-45cf-acc5-ff12cbc6ed01
source-git-commit: bf31e5226cbb763e2fb82391772b64e5d5c89fae
workflow-type: tm+mt
source-wordcount: '366'
ht-degree: 0%

---

# Erstmalige Installation{#installing-for-the-first-time}

Führen Sie diese Schritte aus, um Image Serving zum ersten Mal unter Windows zu installieren.

1. Melden Sie sich bei Ihrem Serverhost mit Administratorrechten an.
1. Wenn Sie bereits eine Lizenz erhalten haben, kopieren Sie diese auf Ihren Server und führen Sie die Lizenzinstallation durch Doppelklicken auf die Datei aus.

   Wenn Sie noch keine Lizenz haben, können Sie mit der Installation fortfahren und die Lizenz später installieren.

1. Extrahieren Sie den Inhalt der ZIP-Datei der Image-Serving-Verteilung.
1. Starten Sie den Installationsassistenten, indem Sie [!DNL setup]/[!DNL setup.exe] ausführen.
1. Wählen Sie **[!UICONTROL Weiter]**, um zum Endbenutzer-Lizenzvertrag (EULA) zu gelangen, lesen Sie die Lizenzvereinbarung und wählen Sie **[!UICONTROL Ja]**.

   Das Dialogfeld [!DNL Authentication] wird als Nächstes angezeigt.
1. Wenn eine Lizenz bereits installiert ist und die Lizenzinformationen im Dialogfeld [!DNL Authentication] angezeigt werden, klicken Sie auf **[!UICONTROL Weiter]**, um fortzufahren.

   Wenn Sie keine Lizenz haben, wählen Sie **[!UICONTROL Lizenz anfordern]**. Im nächsten Dialogfeld wird eine der MAC-Adressen der Netzwerkschnittstellenkarte Ihres Computers angezeigt. Senden Sie eine E-Mail an diese MAC-Adresse, Ihren Firmennamen und das Produkt, das Sie installieren möchten, wie in der Eingabeaufforderung beschrieben.

   **Wichtig:** Die Lizenz basiert auf der MAC-Adresse einer der auf diesem Host installierten Netzwerkschnittstellenkarten. Wenn Sie diese Karte deaktivieren, entfernen oder ersetzen, wird die Lizenz nicht mehr als gültig anerkannt. Stellen Sie sicher, dass Sie eine Lizenz für die Hardwarekonfiguration erhalten, die Sie für Image-Serving verwenden.

   Sie können die Installation von IS ohne gültige Lizenz fortsetzen und die Lizenz später installieren. Um fortzufahren, wählen Sie **[!UICONTROL Zurück]** aus, um zum Dialogfeld &quot;[!DNL Authentication]&quot; zurückzukehren, und klicken Sie dann auf **[!UICONTROL Weiter]**.
1. Navigieren Sie zur Seite &quot;[!DNL Platform Server] Admin-Einstellungen“. Geben Sie bei Bedarf neue Werte ein oder übernehmen Sie die Standardwerte.

   Sie können die folgenden Elemente konfigurieren:

   <table id="table_AA5D7674BBBE4AD4B373066AEF413FFD"> 
   <tbody> 
   <tr> 
      <td> <p> [!DNL Platform Server] HTTP-Verbindungs-Port </p> </td>
      <td> <p>Haupt-HTTP-Überwachungs-Port für Bildbereitstellung und Bild-Rendering </p> </td>
   </tr> 
   <tr> 
      <td> <p> Admin-Listening-Port </p> </td>
      <td> <p>Admin-Listening-Port </p> </td>
   </tr> 
   <tr> 
      <td> <p> Cache-Größe in MB [!DNL Platform Server] </p> </td>
      <td> <p>Anfangsgröße des Hauptantwort-Caches </p> </td>
   </tr>
   <tr> 
      <td> <p> [!DNL Platform Server] Cache-Speicherort </p> </td>
      <td> <p>PS-Cache-Ordner </p> </td>
   </tr>
   </tbody>
   </table>

   Die angegebenen Portnummern müssen eindeutig sein und dürfen nicht von anderen Anwendungen oder Diensten verwendet werden.

   Der nächste Bildschirm bietet die Möglichkeit, die ausgewählten Einstellungen zu überprüfen.

1. Wählen Sie **[!UICONTROL Zurück]** aus, um Änderungen vorzunehmen, oder wählen Sie **[!UICONTROL Weiter]** aus, um die Installation zu starten.

1. Wählen Sie **[!UICONTROL Beenden]**, um den Installationsassistenten zu beenden.
