---
description: Mit dem Viewer können Sie den Kataloginhalt an einen Drucker ausgeben.
solution: Experience Manager
title: Druckfunktion
feature: Dynamic Media Classic,Viewers,SDK/API,eCatalog Search
role: Developer,User
exl-id: eadcc105-4a86-40f7-867a-3b09a5599a41
source-git-commit: 206e4643e3926cb85b4be2189743578f88180be7
workflow-type: tm+mt
source-wordcount: '141'
ht-degree: 0%

---

# Druckfunktion{#print-feature}

Mit dem Viewer können Sie den Kataloginhalt an einen Drucker ausgeben.

Die Druckfunktion wird durch eine dedizierte Schaltfläche in der Symbolleiste ausgelöst. Durch Klicken auf die Schaltfläche kann der Benutzer einen Druckbereich und die Anzahl der Seiten pro Blatt auswählen.

Die Druckqualität kann mithilfe des Konfigurationsparameters `printquality` angepasst werden. Beachten Sie, dass es nicht empfohlen wird, `printquality` auf Werte festzulegen, die deutlich höher als der Standardwert sind. Der Grund dafür ist, dass dies zu einem sehr hohen Speicherverbrauch des Webbrowsers auf dem System des Clients führt. Stellen Sie außerdem sicher, dass die für Ihr Dynamic Media Classic-Unternehmen festgelegte maximale Bildreaktionsgröße größer ist als der konfigurierte Wert `printquality` .

>[!NOTE]
>
>Die Druckfunktion ist nur auf Desktop-Systemen verfügbar, mit Ausnahme von Internet Explorer 9.
