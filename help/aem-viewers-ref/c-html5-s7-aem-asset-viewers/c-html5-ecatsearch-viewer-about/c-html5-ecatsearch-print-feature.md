---
description: Mit dem Viewer können Sie den Kataloginhalt an einen Drucker ausgeben.
solution: Experience Manager
title: Druckfunktion
feature: Dynamic Media Classic,Viewers,SDK/API,eCatalog Search
role: Developer,User
exl-id: eadcc105-4a86-40f7-867a-3b09a5599a41
source-git-commit: 206e4643e3926cb85b4be2189743578f88180be7
workflow-type: tm+mt
source-wordcount: '134'
ht-degree: 0%

---

# Druckfunktion{#print-feature}

Mit dem Viewer können Sie den Kataloginhalt an einen Drucker ausgeben.

Die Druckfunktion wird durch eine spezielle Schaltfläche in der Symbolleiste ausgelöst. Durch Klicken auf die Schaltfläche kann der Benutzer einen Druckbereich und die Anzahl der Seiten pro Blatt auswählen.

Die Druckqualität kann mit dem Konfigurationsparameter `printquality` angepasst werden. Beachten Sie, dass das Festlegen von `printquality` auf Werte, die deutlich höher als der Standardwert sind, nicht empfohlen wird. Der Grund dafür ist, dass dies zu einem sehr hohen Speicherverbrauch durch den Webbrowser auf dem Client-System führt. Stellen Sie außerdem sicher, dass die für Ihr Dynamic Media Classic-Unternehmen festgelegte maximale Bildantwortgröße größer ist als der konfigurierte `printquality`.

>[!NOTE]
>
>Die Druckfunktion ist nur auf Desktop-Systemen verfügbar, mit Ausnahme von Internet Explorer 9.
