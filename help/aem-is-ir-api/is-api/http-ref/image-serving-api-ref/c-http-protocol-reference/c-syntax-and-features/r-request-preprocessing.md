---
description: Image Serving bietet einen einfachen Anforderungs-Präprozessor, der auf Übereinstimmungs- und Ersatzregeln für reguläre Ausdrücke basiert.
solution: Experience Manager
title: Vorverarbeitung anfordern
feature: Dynamic Media Classic,SDK/API
role: Developer,User
exl-id: f855c36f-29f2-4ada-a103-1eb9b7b0c1a0
source-git-commit: bf31e5226cbb763e2fb82391772b64e5d5c89fae
workflow-type: tm+mt
source-wordcount: '283'
ht-degree: 0%

---

# Vorverarbeitung anfordern{#request-preprocessing}

Image Serving bietet einen einfachen Anforderungs-Präprozessor, der auf Übereinstimmungs- und Ersatzregeln für reguläre Ausdrücke basiert.

Regelsammlungen (Regelsätze) können an jeden Bildkatalog einschließlich des Standardkatalogs angehängt werden. Regeln werden mit XML-formatierten Dateien angegeben.

Die Regeln zur Vorverarbeitung von Anfragen können den Pfad und die Abfrageabschnitte von Anforderungen ändern, bevor sie vom Parser der [!DNL Platform Server] verarbeitet werden. Dazu gehören das Manipulieren des Pfads, das Hinzufügen von Befehlen, das Ändern von Befehlswerten und das Anwenden von Vorlagen oder Makros. Regeln können auch verwendet werden, um bestimmte Sicherheitsfunktionen zu konfigurieren und zu überschreiben, die normalerweise nur mit Katalogattributen gesteuert werden, z. B. Anforderungsverschleierung, Wasserzeichen und die Beschränkung des HTTP-Dienstes auf bestimmte Client-IP-Adressen.

Vorverarbeitungsregeln für Anfragen eignen sich für eine Vielzahl von Anwendungen, von denen einige im Folgenden aufgeführt sind:

* Implementieren Sie einen Mechanismus *virtueller Pfade* , der eine Neukodifizierung des Anfragepfads zu Datei-, FTP- und HTTP-Pfaden ermöglicht.
* Selektives Erzwingen von Sicherheitsfunktionen wie Wasserzeichen, gefiltert nach Bildname oder Pfad.
* Auslassen von Wasserzeichen oder anderen Sicherheitsfunktionen beim Zugriff auf den Server über bestimmte IP-Adressen.
* Erzwingen der Anwendung von Befehlen wie `defaultImage=` für alle Anforderungen oder Anforderungen, die ein bestimmtes Muster im URL-Pfad oder in Abfragezeichenfolgen aufweisen.
* Die Verwendung von CPU-intensiven Befehlen zur Vermeidung von Servermissbrauch wird untersagt.
* Zulassen, dass Quellbilder auf HTTP- oder FTP-Servern gespeichert werden, während sie weiterhin im Anfragepfad anstatt mit `src=` angegeben werden.
* Steuern Sie die Bildqualitätseinstellungen (z. B. JPEG-Qualität oder Scharfzeichnen) je nach Anfragepfad oder Bildname.

Ausführliche Informationen zum Erstellen, Verwenden und Verwalten von Regelsätzen finden Sie in der [Referenz zu Regelsätzen](../../../../../is-api/image-catalog/image-serving-api-ref/c-image-catalog-reference/c-rule-set-reference/c-rule-set-reference.md#concept-3e5058cf3507470b82cac638df23ea8e).

## Verwandte Themen {#see-also}

[Referenz zum Regelsatz](../../../../../is-api/image-catalog/image-serving-api-ref/c-image-catalog-reference/c-rule-set-reference/c-rule-set-reference.md#concept-3e5058cf3507470b82cac638df23ea8e), [Attribut::RuleSetFile](../../../../../is-api/image-catalog/image-serving-api-ref/c-image-catalog-reference/c-overview/c-file-formats/r-rule-set-files.md#reference-3e54cb5f4d74411a84889fed056ac093)
