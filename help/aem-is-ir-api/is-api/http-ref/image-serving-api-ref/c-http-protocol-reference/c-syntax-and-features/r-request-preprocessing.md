---
description: Image Serving bietet einen einfachen Anforderungsvorprozessor basierend auf Übereinstimmungs- und Substitutionsregeln für reguläre Ausdruck.
solution: Experience Manager
title: Vorverarbeitung anfordern
feature: Dynamic Media Classic,SDK/API
role: Developer,Business Practitioner
translation-type: tm+mt
source-git-commit: f6c97606d7a4209427316d7367013ad9585a5cae
workflow-type: tm+mt
source-wordcount: '292'
ht-degree: 0%

---


# Anforderungsvorverarbeitung{#request-preprocessing}

Image Serving bietet einen einfachen Anforderungsvorprozessor basierend auf Übereinstimmungs- und Substitutionsregeln für reguläre Ausdruck.

Regelsammlungen (Regelsätze) können an jeden Bildkatalog, einschließlich des Standardkatalogs, angehängt werden. Regeln werden mit XML-formatierten Dateien angegeben.

Vorverarbeitungsregeln für Anfragen können den Pfad und die Abfrage von Anforderungen ändern, bevor sie vom Parser des Plattformservers verarbeitet werden. Dazu gehören die Änderung des Pfads, das Hinzufügen von Befehlen, das Ändern von Befehlswerten und das Anwenden von Vorlagen oder Makros. Regeln können auch verwendet werden, um bestimmte Sicherheitsfunktionen zu konfigurieren und außer Kraft zu setzen, die normalerweise nur mit Katalogattributen gesteuert werden, wie z. B. Anforderungsvertuschung, Wasserkennzeichnung und Beschränkung des HTTP-Dienstes auf bestimmte Client-IP-Adressen.

Vorverarbeitungsregeln für Anfragen sind für eine Vielzahl von Anwendungen geeignet, von denen einige im Folgenden aufgeführt sind:

* Implementieren Sie einen *Virtual Pfade*-Mechanismus, der eine Neuzuordnung des Anforderungspfads zu Datei-, FTP- und HTTP-Pfaden ermöglicht.
* Selektives Erzwingen von Sicherheitsfunktionen wie Wasserzeichen, gefiltert nach Bildname oder Pfad.
* Auslassen von Wasserzeichen oder anderen Sicherheitsfunktionen beim Zugriff auf den Server über bestimmte IP-Adressen.
* Erzwingen der Anwendung von Befehlen wie `defaultImage=` für alle Anforderungen oder Anforderungen, die ein bestimmtes Muster im URL-Pfad oder in den Zeichenfolgen der Abfrage aufweisen.
* Untersagen der Verwendung von CPU-intensiven Befehlen zur Verhinderung von Servermissbrauch.
* Quellbilder können auf HTTP- oder FTP-Servern gespeichert werden, während sie weiterhin im Anforderungspfad anstatt mit `src=` angegeben werden.
* Kontrollieren Sie die Bildqualitätseinstellungen (z. B. JPEG-Qualität oder Scharfzeichnen) je nach Anforderungspfad oder Bildname.

Ausführliche Informationen zum Erstellen, Verwenden und Verwalten von Regelsätzen finden Sie in der [Regelsatzreferenz](../../../../../is-api/image-catalog/image-serving-api-ref/c-image-catalog-reference/c-rule-set-reference/c-rule-set-reference.md#concept-3e5058cf3507470b82cac638df23ea8e).

## Verwandte Themen {#see-also}

[Regelsatzreferenz](../../../../../is-api/image-catalog/image-serving-api-ref/c-image-catalog-reference/c-rule-set-reference/c-rule-set-reference.md#concept-3e5058cf3507470b82cac638df23ea8e),  [Attribut::RuleSetFile](../../../../../is-api/image-catalog/image-serving-api-ref/c-image-catalog-reference/c-overview/c-file-formats/r-rule-set-files.md#reference-3e54cb5f4d74411a84889fed056ac093)
