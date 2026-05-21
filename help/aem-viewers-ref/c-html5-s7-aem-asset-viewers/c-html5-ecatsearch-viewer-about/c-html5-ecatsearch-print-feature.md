---
description: Mit dem Viewer können Sie den Kataloginhalt an einen Drucker ausgeben.
solution: Experience Manager
title: Druckfunktion
feature: Dynamic Media Classic,Viewers,SDK/API,eCatalog Search
role: Developer,User
exl-id: eadcc105-4a86-40f7-867a-3b09a5599a41
TQID: 'https://experienceleague.adobe.com/mbsxiwsrZch87oSFFhXUNp892iQSmfyAFaY7bzDn2MM'
product_v2: id: fd1f54a9-f50c-467d-8956-cebbaf4f3eb8
feature_v2: id: a01bfd36-4ab8-4bf8-9dc0-5b45b890552e
role_v2: id: b69b2659-1057-424e-8fc5-ed9e016dc554id: ff6a42d2-313e-452e-93a6-792e4fad9ff8
source-git-commit: 2ff64206b7448a1a122696facd2669be68b6b9ff
workflow-type: tm+mt
source-wordcount: 134
ht-degree: 0%

---

# Druckfunktion{#print-feature}

Mit dem Viewer können Sie den Kataloginhalt an einen Drucker ausgeben.

Die Druckfunktion wird durch eine spezielle Schaltfläche in der Symbolleiste ausgelöst. Durch Klicken auf die Schaltfläche kann der Benutzer einen Druckbereich und die Anzahl der Seiten pro Blatt auswählen.

Die Druckqualität kann mit dem Konfigurationsparameter `printquality` angepasst werden. Beachten Sie, dass das Festlegen von `printquality` auf Werte, die deutlich höher als der Standardwert sind, nicht empfohlen wird. Der Grund dafür ist, dass dies zu einem sehr hohen Speicherverbrauch durch den Webbrowser auf dem Client-System führt. Stellen Sie außerdem sicher, dass die für Ihr Dynamic Media Classic-Unternehmen festgelegte maximale Bildantwortgröße größer ist als der konfigurierte `printquality`.

>[!NOTE]
>
>Die Druckfunktion ist nur auf Desktop-Systemen verfügbar, mit Ausnahme von Internet Explorer 9.
