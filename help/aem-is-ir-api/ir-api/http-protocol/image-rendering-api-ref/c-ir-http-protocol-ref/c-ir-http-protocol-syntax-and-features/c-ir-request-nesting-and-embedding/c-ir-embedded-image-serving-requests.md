---
description: Eine Image Server-(IS-)Anforderung kann als Materialbild verwendet werden.
seo-description: Eine Image Server-(IS-)Anforderung kann als Materialbild verwendet werden.
seo-title: Eingebettete Image-Server-Anforderungen
solution: Experience Manager
title: Eingebettete Image-Server-Anforderungen
topic: Scene7 Image Serving - Image Rendering API
uuid: dd72880d-8824-40b3-a5da-0f6ff4922939
translation-type: tm+mt
source-git-commit: 7bc7b3a86fbcdc57cfdc31745fae3afc06e44b15

---


# Eingebettete Image-Server-Anforderungen{#embedded-image-server-requests}

Eine Image Server-(IS-)Anforderung kann als Materialbild verwendet werden.

Geben Sie die Anforderung im `src=` Befehl wie folgt an:

` …&src=is( *[!DNL imageServingRequest]*)&…`

Beim `is` Token muss die Groß-/Kleinschreibung beachtet werden.

Die verschachtelte Anforderung darf nicht den Image Serving-Stammpfad enthalten (typischerweise [!DNL http:// *[!DNL server]*/is/image/&quot;]), kann aber vorverarbeitende Regeltokens enthalten.

Die folgenden IS-Befehle werden ignoriert, wenn sie in verschachtelten Anforderungen angegeben werden (entweder in der Anforderungs-URL oder in `catalog::Modifier` oder `catalog::PostModifier`):

* `bgc=`
* `fmt=`
* `icc=`
* `iccEmbed=`
* `printRes=`
* `qlt=`
* `quantize=`
* `req=`

Auch werden ignoriert `attribute::MaxPix` und `attribute::DefaultPix` der Bildkatalog, der für die eingebettete IS-Anforderung gilt.

Wenn das Ergebnisbild der verschachtelten Anforderung Maskendaten (Alpha-Daten) enthält, wird es immer an das Material übergeben. Verwenden Sie eine Hintergrundbild-Ebene mit fester Farbe, um unerwünschtes Alpha zu vermeiden.

Das Bildergebnis einer eingebetteten IS-Anforderung kann optional zwischengespeichert werden, indem `cache=on`sie einbezogen wird. Standardmäßig ist die Zwischenspeicherung von Zwischendaten deaktiviert. Die Zwischenspeicherung sollte nur aktiviert werden, wenn erwartet wird, dass das Zwischenbild in einer anderen Anforderung innerhalb eines angemessenen Zeitraums wiederverwendet wird. Es gilt die standardmäßige serverseitige Cacheverwaltung. Die Daten werden im verlustfreien Format zwischengespeichert.
