---
description: Eine Image Server-(IS-)Anforderung kann als Materialbild verwendet werden.
solution: Experience Manager
title: Eingebettete Image-Server-Anforderungen
feature: Dynamic Media Classic, SDK/API
role: Entwickler, Geschäftspraktiker
translation-type: tm+mt
source-git-commit: f6c97606d7a4209427316d7367013ad9585a5cae
workflow-type: tm+mt
source-wordcount: '195'
ht-degree: 0%

---


# Eingebettete Image-Server-Anforderungen{#embedded-image-server-requests}

Eine Image Server-(IS-)Anforderung kann als Materialbild verwendet werden.

Geben Sie die Anforderung im Befehl `src=` wie folgt an:

` …&src=is( *[!DNL imageServingRequest]*)&…`

Beim Token `is` wird die Groß-/Kleinschreibung beachtet.

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

Auch werden die Zeichen `attribute::MaxPix` und `attribute::DefaultPix` des Bildkatalogs ignoriert, der für die eingebettete IS-Anforderung gilt.

Wenn das Ergebnisbild der verschachtelten Anforderung Maskendaten (Alpha-Daten) enthält, wird es immer an das Material übergeben. Verwenden Sie eine Hintergrundbild-Ebene mit fester Farbe, um unerwünschtes Alpha zu vermeiden.

Das Bildergebnis einer eingebetteten IS-Anforderung kann optional zwischengespeichert werden, indem `cache=on` einbezogen wird. Standardmäßig ist die Zwischenspeicherung von Zwischendaten deaktiviert. Die Zwischenspeicherung sollte nur aktiviert werden, wenn erwartet wird, dass das Zwischenbild in einer anderen Anforderung innerhalb eines angemessenen Zeitraums wiederverwendet wird. Es gilt die standardmäßige serverseitige Cacheverwaltung. Die Daten werden im verlustfreien Format zwischengespeichert.
