---
description: Für erweiterte Anwendungen ist es möglich, das Ergebnis eines Rendervorgangs als Materialbild zu verwenden, genau wie ein Bild, das von Image Serving erhalten wurde.
seo-description: Für erweiterte Anwendungen ist es möglich, das Ergebnis eines Rendervorgangs als Materialbild zu verwenden, genau wie ein Bild, das von Image Serving erhalten wurde.
seo-title: Verschachtelte Image Rendering-Anforderungen
solution: Experience Manager
title: Verschachtelte Image Rendering-Anforderungen
topic: Scene7 Image Serving - Image Rendering API
uuid: 12551bd5-ff5f-45d6-81e9-5ba0be47a425
translation-type: tm+mt
source-git-commit: 7bc7b3a86fbcdc57cfdc31745fae3afc06e44b15

---


# Verschachtelte Image Rendering-Anforderungen{#nested-image-rendering-requests}

Für erweiterte Anwendungen ist es möglich, das Ergebnis eines Rendervorgangs als Materialbild zu verwenden, genau wie ein Bild, das von Image Serving erhalten wurde.

Eine Render-Anforderung kann wie folgt als Materialbild verwendet werden, indem Sie sie wie folgt im `src=` Befehl angeben:

` …&src=ir{ *[!DNL renderRequest]*}&…`

Beim `ir` Token muss die Groß-/Kleinschreibung beachtet werden.

Die verschachtelte Anforderung darf nicht den Root-Pfad zum Image Rendering enthalten (in der Regel `http:// *[!DNL server]*/ir/render/'`), sondern kann Regeln-Token vor der Verarbeitung enthalten.

Die folgenden Befehle werden ignoriert, wenn sie in verschachtelten Anforderungen angegeben werden (entweder in der Anforderungs-URL oder in `catalog::Modifier` oder `catalog::PostModifier`):

* `fmt=`
* `qlt=`
* `icc=`
* `iccEmbed=`
* `printRes=`
* `req=`
* `bgc=`

Auch werden ignoriert `attribute::MaxPix` und `attribute::DefaultPix` der Materialkatalog, der für die verschachtelte Render-Anforderung gilt.

Das Bildergebnis einer verschachtelten IR-Anforderung kann optional zwischengespeichert werden, indem auch `cache=on`die Option einbezogen wird. Standardmäßig ist die Zwischenspeicherung von Zwischendaten deaktiviert. Die Zwischenspeicherung sollte nur aktiviert werden, wenn erwartet wird, dass das Zwischenbild in einer anderen Anforderung innerhalb eines angemessenen Zeitraums wiederverwendet wird. Es gilt die standardmäßige serverseitige Cacheverwaltung. Die Daten werden im verlustfreien Format zwischengespeichert.
