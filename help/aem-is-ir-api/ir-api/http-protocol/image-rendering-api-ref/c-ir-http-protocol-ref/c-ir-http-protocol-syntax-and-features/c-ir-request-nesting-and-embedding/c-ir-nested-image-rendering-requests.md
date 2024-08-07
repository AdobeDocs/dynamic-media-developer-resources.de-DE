---
title: Verschachtelte Image Rendering-Anforderungen
description: Bei erweiterten Anwendungen ist es möglich, das Ergebnis eines Rendervorgangs als materielles Bild zu verwenden, genau wie ein Bild, das von Image Serving stammt.
solution: Experience Manager
feature: Dynamic Media Classic,SDK/API
role: Developer,User
exl-id: 52c12786-bbe7-4410-87bb-6245d782a68c
source-git-commit: 790ce3aa4e9aadc019d17e663fc93d7c69772b23
workflow-type: tm+mt
source-wordcount: '187'
ht-degree: 0%

---

# Verschachtelte Image Rendering-Anforderungen{#nested-image-rendering-requests}

Bei erweiterten Anwendungen ist es möglich, das Ergebnis eines Rendervorgangs als materielles Bild zu verwenden, genau wie ein Bild, das von Image Serving stammt.

Eine Render-Anfrage kann als Materialbild verwendet werden, indem sie sie wie folgt im Befehl `src=` angibt:

` …&src=ir{ *[!DNL renderRequest]*}&…`

Beim `ir` -Token wird zwischen Groß- und Kleinschreibung unterschieden.

Die verschachtelte Anforderung darf nicht den Stammpfad für das Rendern von Bildern enthalten (normalerweise `http:// *[!DNL server]*/ir/render/'`), kann aber Vorab-Verarbeitungsregel-Token enthalten.

Die folgenden Befehle werden ignoriert, wenn sie in verschachtelten Anforderungen angegeben werden (entweder in der Anfrage-URL oder in `catalog::Modifier` oder `catalog::PostModifier`):

* `fmt=`
* `qlt=`
* `icc=`
* `iccEmbed=`
* `printRes=`
* `req=`
* `bgc=`

Außerdem werden `attribute::MaxPix` und `attribute::DefaultPix` des Materialkatalogs ignoriert, der für die verschachtelte Renderanforderung gilt.

Das Bildergebnis einer verschachtelten IR-Anfrage kann optional zwischengespeichert werden, indem `cache=on` eingeschlossen wird. Standardmäßig ist die Zwischenspeicherung von Zwischendaten deaktiviert. Die Zwischenspeicherung sollte nur aktiviert werden, wenn das Zwischenbild innerhalb eines angemessenen Zeitraums in einer anderen Anforderung wiederverwendet wird. Es gilt die standardmäßige serverseitige Cacheverwaltung. Die Daten werden verlustfrei zwischengespeichert.
