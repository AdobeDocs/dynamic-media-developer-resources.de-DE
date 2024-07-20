---
title: Vorab-Bearbeitung anfordern
description: Das Bild-Rendering bietet einen einfachen Anforderungs-Vorprozessor, der auf Übereinstimmungs- und Ersatzregeln für reguläre Ausdrücke basiert.
solution: Experience Manager
feature: Dynamic Media Classic,SDK/API
role: Developer,User
exl-id: 79a358db-0fd6-4327-a305-b0b38ad62050
source-git-commit: 20f4922402bd31c71ae650a01597b574220809fa
workflow-type: tm+mt
source-wordcount: '210'
ht-degree: 0%

---

# Vorab-Bearbeitung anfordern{#request-pre-processing}

Das Bild-Rendering bietet einen einfachen Anforderungs-Vorprozessor, der auf Übereinstimmungs- und Ersatzregeln für reguläre Ausdrücke basiert.

Regelsammlungen (Regelsätze) können an jeden Materialkatalog angehängt werden, einschließlich des Standardkatalogs. Regeln werden mit XML-formatierten Dateien angegeben.

Vorab-Verarbeitungsregeln für Anfragen können den Pfad und die Abfrageabschnitte von Anforderungen ändern, bevor sie vom Image Rendering-Parser verarbeitet werden. Dieses Konzept umfasst die Bearbeitung des Pfads, das Hinzufügen von Befehlen, das Ändern von Befehlswerten und das Anwenden von Vorlagen oder Makros. Regeln können auch verwendet werden, um bestimmte Funktionen zu konfigurieren und zu überschreiben, die normalerweise nur mit Katalogattributen gesteuert werden, z. B. das Festlegen der standardmäßigen Antwortbildgröße oder das Eingrenzen des HTTP-Dienstes auf bestimmte Client-IP-Adressen.

Vorab-Verarbeitungsregeln für Anfragen eignen sich für verschiedene Anwendungen, von denen einige im Folgenden aufgelistet sind:

* Implementieren Sie einen Mechanismus *virtueller Pfade* , der eine Neukodifizierung des Anfragepfads zu Datei-, FTP- und HTTP-Pfaden ermöglicht.
* Die Verwendung von CPU-intensiven Befehlen wird untersagt, um Servermissbrauch zu verhindern.
* Steuern Sie die Bildqualitätseinstellungen (z. B. JPEG-Qualität oder Scharfzeichnen) je nach Anfragepfad oder Bildname.

Ausführliche Informationen zum Erstellen, Verwenden und Verwalten von Regelsätzen finden Sie in der Referenz zu Regelsätzen.

Siehe auch Regelsatzreferenz, attribute::RuleSetFile
