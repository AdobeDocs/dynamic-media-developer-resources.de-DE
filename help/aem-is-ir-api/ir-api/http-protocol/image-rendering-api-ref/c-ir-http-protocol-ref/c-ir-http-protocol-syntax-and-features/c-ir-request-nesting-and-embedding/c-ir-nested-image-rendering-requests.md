---
description: Für erweiterte Anwendungen ist es möglich, das Ergebnis eines Rendervorgangs als Materialbild zu verwenden, genau wie ein Bild, das von Image Serving erhalten wurde.
solution: Experience Manager
title: Verschachtelte Image Rendering-Anforderungen
feature: Dynamic Media Classic, SDK/API
role: Entwickler, Geschäftspraktiker
translation-type: tm+mt
source-git-commit: f6c97606d7a4209427316d7367013ad9585a5cae
workflow-type: tm+mt
source-wordcount: '198'
ht-degree: 0%

---


# Verschachtelte Image Rendering-Anforderungen{#nested-image-rendering-requests}

Für erweiterte Anwendungen ist es möglich, das Ergebnis eines Rendervorgangs als Materialbild zu verwenden, genau wie ein Bild, das von Image Serving erhalten wurde.

Eine Render-Anforderung kann wie folgt als Materialbild verwendet werden, indem Sie sie im Befehl `src=` wie folgt angeben:

` …&src=ir{ *[!DNL renderRequest]*}&…`

Beim Token `ir` wird die Groß-/Kleinschreibung beachtet.

Die verschachtelte Anforderung darf nicht den Root-Pfad zum Image Rendering enthalten (typischerweise `http:// *[!DNL server]*/ir/render/'`), sondern kann Regeln-Token vor der Verarbeitung enthalten.

Die folgenden Befehle werden ignoriert, wenn sie in verschachtelten Anforderungen angegeben werden (entweder in der Anforderungs-URL oder in `catalog::Modifier` oder `catalog::PostModifier`):

* `fmt=`
* `qlt=`
* `icc=`
* `iccEmbed=`
* `printRes=`
* `req=`
* `bgc=`

Auch werden die Elemente `attribute::MaxPix` und `attribute::DefaultPix` des Materialkatalogs ignoriert, die für die verschachtelte Render-Anforderung gelten.

Das Bildergebnis einer verschachtelten IR-Anforderung kann optional mit `cache=on` zwischengespeichert werden. Standardmäßig ist die Zwischenspeicherung von Zwischendaten deaktiviert. Die Zwischenspeicherung sollte nur aktiviert werden, wenn erwartet wird, dass das Zwischenbild in einer anderen Anforderung innerhalb eines angemessenen Zeitraums wiederverwendet wird. Es gilt die standardmäßige serverseitige Cacheverwaltung. Die Daten werden im verlustfreien Format zwischengespeichert.
