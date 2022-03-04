---
title: Eingebettete Image-Server-Anforderungen
description: Eine Image Server (IS)-Anfrage kann als Materialbild verwendet werden.
solution: Experience Manager
feature: Dynamic Media Classic,SDK/API
role: Developer,User
exl-id: 4ece9738-45e0-43c0-ba1c-2a05ef1f39be
source-git-commit: 790ce3aa4e9aadc019d17e663fc93d7c69772b23
workflow-type: tm+mt
source-wordcount: '180'
ht-degree: 0%

---

# Eingebettete Image-Server-Anforderungen{#embedded-image-server-requests}

Eine Image Server (IS)-Anfrage kann als Materialbild verwendet werden.

Geben Sie die Anforderung im `src=` -Befehl wie folgt:

` …&src=is( *[!DNL imageServingRequest]*)&…`

Die `is` Beim Token wird zwischen Groß- und Kleinschreibung unterschieden.

Die verschachtelte Anforderung darf nicht den Root-Pfad &quot;Image Serving&quot;enthalten (normalerweise [!DNL http:// *[!DNL server]*/is/image/"]), kann aber Vorab-Verarbeitungsregel-Token enthalten.

Die folgenden IS-Befehle werden ignoriert, wenn sie in verschachtelten Anforderungen angegeben werden (entweder in der Anforderungs-URL oder in `catalog::Modifier` oder `catalog::PostModifier`):

* `bgc=`
* `fmt=`
* `icc=`
* `iccEmbed=`
* `printRes=`
* `qlt=`
* `quantize=`
* `req=`

Auch ignoriert `attribute::MaxPix` und `attribute::DefaultPix` des Bildkatalogs, der für die eingebettete IS-Anforderung gilt.

Wenn das Ergebnisbild der verschachtelten Anforderung Maskendaten (Alpha) enthält, wird es immer an das Material übergeben. Verwenden Sie eine einfarbige Hintergrundbildschicht, um unerwünschte Alpha zu vermeiden.

Das Bildergebnis einer eingebetteten IS-Anforderung kann optional zwischengespeichert werden, indem `cache=on`. Standardmäßig ist die Zwischenspeicherung von Zwischendaten deaktiviert. Die Zwischenspeicherung sollte nur aktiviert werden, wenn das Zwischenbild innerhalb eines angemessenen Zeitraums in einer anderen Anforderung wiederverwendet wird. Es gilt die standardmäßige serverseitige Cacheverwaltung. Die Daten werden verlustfrei zwischengespeichert.
