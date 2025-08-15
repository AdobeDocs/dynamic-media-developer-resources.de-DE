---
description: Die Bildbereitstellung bietet einen einfachen Anforderungspräprozessor, der auf Übereinstimmungs- und Ersetzungsregeln für reguläre Ausdrücke basiert.
solution: Experience Manager
title: Vorab-Bearbeitung einer Anfrage
feature: Dynamic Media Classic,SDK/API
role: Developer,User
exl-id: f855c36f-29f2-4ada-a103-1eb9b7b0c1a0
source-git-commit: bf31e5226cbb763e2fb82391772b64e5d5c89fae
workflow-type: tm+mt
source-wordcount: '283'
ht-degree: 0%

---

# Vorab-Bearbeitung einer Anfrage{#request-preprocessing}

Die Bildbereitstellung bietet einen einfachen Anforderungspräprozessor, der auf Übereinstimmungs- und Ersetzungsregeln für reguläre Ausdrücke basiert.

Sammlungen von Regeln (Regelsätze) können an jeden Bildkatalog angehängt werden, einschließlich des Standardkatalogs. Regeln werden mit XML-formatierten Dateien angegeben.

Regeln für die Anfragevorverarbeitung können den Pfad und die Abfrageabschnitte von Anfragen ändern, bevor sie vom Parser des [!DNL Platform Server] verarbeitet werden, einschließlich der Bearbeitung des Pfads, des Hinzufügens von Befehlen, des Änderns von Befehlswerten und des Anwenden von Vorlagen oder Makros. Regeln können auch verwendet werden, um bestimmte Sicherheitsfunktionen zu konfigurieren und zu überschreiben, die normalerweise nur mit Katalogattributen gesteuert werden, z. B. Anfrageverschleierung, Wasserzeichen sowie die Beschränkung des HTTP-Service auf bestimmte Client-IP-Adressen.

Regeln zur Anfragevorverarbeitung eignen sich für eine Vielzahl von Anwendungen, von denen einige unten aufgeführt sind:

* Implementieren Sie *Mechanismus &quot;* Pfade“, der die Neuzuordnung des Anfragepfads zu Datei-, FTP- und HTTP-Pfaden ermöglicht.
* Selektive Durchsetzung von Sicherheitsfunktionen wie Wasserzeichen, gefiltert nach Bildnamen oder Pfad.
* Auslassen von Wasserzeichen oder anderen Sicherheitsfunktionen beim Zugriff auf den Server über bestimmte IP-Adressen.
* Erzwungene Anwendung von Befehlen wie `defaultImage=` auf alle Anfragen oder auf Anfragen, die ein bestimmtes Muster im URL-Pfad oder in Abfragezeichenfolgen aufweisen.
* Deaktivieren der Verwendung von CPU-intensiven Befehlen, um Servermissbrauch zu verhindern.
* Quellbilder können auf HTTP- oder FTP-Servern gespeichert werden, während sie weiterhin im Anfragepfad und nicht mit `src=` angegeben werden.
* Steuern der Bildqualitätseinstellungen (z. B. JPEG-Qualität oder Scharfzeichnung) je nach Anfragepfad oder Bildname.

Ausführliche Informationen zum Erstellen, Verwenden und Verwalten von Regelsätzen finden Sie [ „Regelsatzreferenz](../../../../../is-api/image-catalog/image-serving-api-ref/c-image-catalog-reference/c-rule-set-reference/c-rule-set-reference.md#concept-3e5058cf3507470b82cac638df23ea8e).

## Verwandte Themen {#see-also}

[Regelsatzreferenz](../../../../../is-api/image-catalog/image-serving-api-ref/c-image-catalog-reference/c-rule-set-reference/c-rule-set-reference.md#concept-3e5058cf3507470b82cac638df23ea8e), [attribute::RuleSetFile](../../../../../is-api/image-catalog/image-serving-api-ref/c-image-catalog-reference/c-overview/c-file-formats/r-rule-set-files.md#reference-3e54cb5f4d74411a84889fed056ac093)
