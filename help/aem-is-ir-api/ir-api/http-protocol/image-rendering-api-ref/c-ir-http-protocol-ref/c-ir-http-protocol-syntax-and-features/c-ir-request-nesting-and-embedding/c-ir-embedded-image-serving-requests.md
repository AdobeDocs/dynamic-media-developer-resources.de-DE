---
title: Anforderungen des eingebetteten Bild-Servers
description: Eine Image Server (IS)-Anfrage kann als Materialbild verwendet werden.
solution: Experience Manager
feature: Dynamic Media Classic,SDK/API
role: Developer,User
exl-id: 4ece9738-45e0-43c0-ba1c-2a05ef1f39be
TQID: 'https://experienceleague.adobe.com/dt-baBh9jAyJdjqopFR3AoqRvz5zqLzi8B3SnE04xEs'
product_v2: id: fd1f54a9-f50c-467d-8956-cebbaf4f3eb8
feature_v2: id: a01bfd36-4ab8-4bf8-9dc0-5b45b890552e
role_v2: id: b69b2659-1057-424e-8fc5-ed9e016dc554id: ff6a42d2-313e-452e-93a6-792e4fad9ff8
source-git-commit: 4339f336345d7d7f3c05c7f5a18fbd28bcfd382b
workflow-type: tm+mt
source-wordcount: 183
ht-degree: 0%

---

# Anforderungen des eingebetteten Bild-Servers{#embedded-image-server-requests}

Eine Image Server (IS)-Anfrage kann als Materialbild verwendet werden.

Geben Sie die Anfrage im `src=` wie folgt an:

` …&src=is( *[!DNL imageServingRequest]*)&…`

Beim `is`-Token wird zwischen Groß- und Kleinschreibung unterschieden.

Die verschachtelte Anfrage darf nicht den Stammpfad für die Bildbereitstellung enthalten (normalerweise [!DNL http:// *[!DNL server]*/is/image/"]), kann aber Token für Vorverarbeitungsregeln enthalten.

Die folgenden IS-Befehle werden ignoriert, wenn sie in verschachtelten Anfragen angegeben werden (entweder in der Anfrage-URL oder in `catalog::Modifier` oder `catalog::PostModifier`):

* `bgc=`
* `fmt=`
* `icc=`
* `iccEmbed=`
* `printRes=`
* `qlt=`
* `quantize=`
* `req=`

Ignoriert werden auch die `attribute::MaxPix` und `attribute::DefaultPix` des Bildkatalogs, der für die eingebettete IS-Anfrage gilt.

Wenn das Ergebnisbild der verschachtelten Anfrage Maskendaten (Alpha) enthält, werden diese immer an das Material übergeben. Verwenden Sie eine einfarbige Hintergrundbildebene, um unerwünschte Alpha-Effekte zu vermeiden.

Das Bildergebnis einer eingebetteten IS-Anfrage kann optional zwischengespeichert werden, indem `cache=on` eingeschlossen wird. Standardmäßig ist das Zwischenspeichern von Zwischendaten deaktiviert. Die Zwischenspeicherung sollte nur aktiviert werden, wenn das Zwischenbild in einer anderen Anfrage innerhalb eines angemessenen Zeitraums wiederverwendet wird. Es gilt die standardmäßige Server-seitige Cache-Verwaltung. Daten werden in einem verlustfreien Format zwischengespeichert.

