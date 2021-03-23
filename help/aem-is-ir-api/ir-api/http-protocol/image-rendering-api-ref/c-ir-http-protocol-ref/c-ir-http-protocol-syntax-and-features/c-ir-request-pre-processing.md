---
description: Das Image Rendering bietet einen einfachen Anforderungs-Vorprozessor basierend auf Übereinstimmungs- und Substitutionsregeln für reguläre Ausdruck.
seo-description: Das Image Rendering bietet einen einfachen Anforderungs-Vorprozessor basierend auf Übereinstimmungs- und Substitutionsregeln für reguläre Ausdruck.
seo-title: Vorverarbeitung anfordern *
solution: Experience Manager
title: Vorverarbeitung anfordern *
uuid: ef69ea23-753c-40c8-9edd-eab9c8820c98
feature: Dynamic Media Classic, SDK/API
role: Entwickler, Geschäftspraktiker
translation-type: tm+mt
source-git-commit: 469d1a5c43a972116a8a2efb0de5708800130a99
workflow-type: tm+mt
source-wordcount: '234'
ht-degree: 0%

---


# Vorverarbeitung anfordern *{#request-pre-processing}

Das Image Rendering bietet einen einfachen Anforderungs-Vorprozessor basierend auf Übereinstimmungs- und Substitutionsregeln für reguläre Ausdruck.

Regelsammlungen (Regelsätze) können an jeden Materialkatalog, einschließlich des Standardkatalogs, angehängt werden. Regeln werden mit XML-formatierten Dateien angegeben.

Vorverarbeitungsregeln für Anfragen können die Pfad- und Abfrage von Anforderungen ändern, bevor sie vom Image Rendering-Parser verarbeitet werden. Dazu gehören die Änderung des Pfads, das Hinzufügen von Befehlen, das Ändern von Befehlswerten und das Anwenden von Vorlagen oder Makros. Regeln können auch verwendet werden, um bestimmte Funktionen zu konfigurieren und außer Kraft zu setzen, die normalerweise nur mit Katalogattributen gesteuert werden, wie z. B. das Festlegen der standardmäßigen Antwortbildgröße oder die Beschränkung des HTTP-Dienstes auf bestimmte Client-IP-Adressen.

Vorverarbeitungsregeln für Anfragen sind für eine Vielzahl von Anwendungen geeignet, von denen einige im Folgenden aufgeführt sind:

* Implementieren Sie einen *Virtual Pfade*-Mechanismus, der eine Neuzuordnung des Anforderungspfads zu Datei-, FTP- und HTTP-Pfaden ermöglicht.
* Die Verwendung von CPU-intensiven Befehlen zur Verhinderung von Servermissbrauch wird untersagt.
* Kontrollieren Sie die Bildqualitätseinstellungen (z. B. JPEG-Qualität oder Scharfzeichnen) je nach Anforderungspfad oder Bildname.

Ausführliche Informationen zum Erstellen, Verwenden und Verwalten von Regelsätzen finden Sie in der Regelsatzreferenz.

Siehe auch Regelsatzreferenz, Attribut::RuleSetFile
