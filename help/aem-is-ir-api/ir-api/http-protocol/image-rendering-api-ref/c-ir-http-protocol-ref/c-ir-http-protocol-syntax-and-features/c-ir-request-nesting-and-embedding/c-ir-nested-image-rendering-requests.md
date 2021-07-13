---
description: Für erweiterte Anwendungen ist es möglich, das Ergebnis eines Rendervorgangs als Materialbild zu verwenden, wie es ein Bild vom Image Serving hat.
solution: Experience Manager
title: Verschachtelte Image Rendering-Anforderungen
feature: Dynamic Media Classic,SDK/API
role: Developer,User
exl-id: 52c12786-bbe7-4410-87bb-6245d782a68c
source-git-commit: 206e4643e3926cb85b4be2189743578f88180be7
workflow-type: tm+mt
source-wordcount: '195'
ht-degree: 0%

---

# Verschachtelte Image Rendering-Anforderungen{#nested-image-rendering-requests}

Für erweiterte Anwendungen ist es möglich, das Ergebnis eines Rendervorgangs als Materialbild zu verwenden, wie es ein Bild vom Image Serving hat.

Eine Render-Anfrage kann als Materialbild verwendet werden, indem sie sie wie folgt im Befehl `src=` angibt:

` …&src=ir{ *[!DNL renderRequest]*}&…`

Beim `ir`-Token wird zwischen Groß- und Kleinschreibung unterschieden.

Die verschachtelte Anforderung darf nicht den Stammpfad für das Bild-Rendering enthalten (typischerweise `http:// *[!DNL server]*/ir/render/'`), kann aber Regeln-Token für die Vorverarbeitung enthalten.

Die folgenden Befehle werden ignoriert, wenn sie in verschachtelten Anforderungen angegeben werden (entweder in der Anfrage-URL oder in `catalog::Modifier` oder `catalog::PostModifier`):

* `fmt=`
* `qlt=`
* `icc=`
* `iccEmbed=`
* `printRes=`
* `req=`
* `bgc=`

Außerdem werden `attribute::MaxPix` und `attribute::DefaultPix` des Materialkatalogs ignoriert, der für die verschachtelte Renderanforderung gilt.

Das Bildergebnis einer verschachtelten IR-Anfrage kann optional zwischengespeichert werden, indem `cache=on` eingeschlossen wird. Standardmäßig ist die Zwischenspeicherung von Zwischendaten deaktiviert. Die Zwischenspeicherung sollte nur aktiviert werden, wenn erwartet wird, dass das Zwischenbild innerhalb eines angemessenen Zeitraums in einer anderen Anforderung wiederverwendet wird. Es gilt die standardmäßige serverseitige Cacheverwaltung. Die Daten werden verlustfrei zwischengespeichert.
