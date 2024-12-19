---
title: Druckfunktion
description: Mit dem Viewer können Sie den Kataloginhalt an einen Drucker ausgeben.
solution: Experience Manager
feature: Dynamic Media Classic,Viewers,SDK/API,eCatalog
role: Developer,User
exl-id: d7c8a0da-ad8b-440e-b27b-ea85dd975d9d
source-git-commit: a919130f0940d81a221b79563b6b3e41533ba788
workflow-type: tm+mt
source-wordcount: '130'
ht-degree: 0%

---

# Druckfunktion{#print-feature}

Mit dem Viewer können Sie den Kataloginhalt an einen Drucker ausgeben.

Die Druckfunktion wird durch eine spezielle Schaltfläche in der Symbolleiste ausgelöst. Durch Klicken auf die Schaltfläche kann der Benutzer einen Druckbereich und die Anzahl der Seiten pro Blatt auswählen.

Die Druckqualität kann mit dem Konfigurationsparameter `printquality` angepasst werden. Es wird nicht empfohlen, `printquality` auf Werte oberhalb des Standardwerts festzulegen. Der Grund dafür ist, dass dies zu einem hohen Speicherverbrauch durch den Webbrowser auf dem Client-System führt. Stellen Sie außerdem sicher, dass die für Ihr Dynamic Media Classic-Unternehmen festgelegte maximale Bildantwortgröße größer ist als der konfigurierte `printquality`.

>[!NOTE]
>
>Die Druckfunktion ist nur auf Desktop-Systemen verfügbar, mit Ausnahme von Internet Explorer 9.
