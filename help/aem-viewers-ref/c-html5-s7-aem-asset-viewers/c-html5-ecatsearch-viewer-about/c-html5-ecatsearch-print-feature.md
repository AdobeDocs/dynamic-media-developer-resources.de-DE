---
description: Mit dem Viewer können Sie den Kataloginhalt auf einem Drucker ausgeben.
solution: Experience Manager
title: Druckfunktion
feature: Dynamic Media Classic, Viewer, SDK/API, E-Katalog-Suche
role: Entwickler, Geschäftspraktiker
translation-type: tm+mt
source-git-commit: f6c97606d7a4209427316d7367013ad9585a5cae
workflow-type: tm+mt
source-wordcount: '144'
ht-degree: 0%

---


# Druckfunktion{#print-feature}

Mit dem Viewer können Sie den Kataloginhalt auf einem Drucker ausgeben.

Die Druckfunktion wird durch eine entsprechende Schaltfläche in der Symbolleiste ausgelöst. Durch Klicken auf die Schaltfläche können Benutzer einen Druckbereich und die Anzahl der Seiten pro Blatt auswählen.

Die Druckqualität kann mit dem Konfigurationsparameter `printquality` angepasst werden. Beachten Sie, dass die Einstellung von `printquality` auf Werte, die deutlich höher als der Standardwert sind, nicht empfohlen wird. Der Grund dafür ist, dass es zu einem sehr hohen Speicherverbrauch des Webbrowsers auf dem Client-System führt. Achten Sie außerdem darauf, dass die für Ihre Dynamic Media Classic-Firma festgelegte maximale Bildreaktionsgröße größer ist als der konfigurierte Wert `printquality`.

>[!NOTE]
>
>Die Druckfunktion ist nur auf Desktop-Systemen verfügbar, mit Ausnahme von Internet Explorer 9.

