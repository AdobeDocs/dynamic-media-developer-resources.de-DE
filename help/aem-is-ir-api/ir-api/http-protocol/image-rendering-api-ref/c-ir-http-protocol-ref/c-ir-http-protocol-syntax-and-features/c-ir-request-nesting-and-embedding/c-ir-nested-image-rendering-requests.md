---
title: Verschachtelte Image-Rendering-Anfragen
description: Für fortgeschrittene Anwendungen ist es möglich, das Ergebnis eines Render-Vorgangs als Materialbild zu verwenden, genau wie ein Bild, das von Image Serving abgerufen wurde.
solution: Experience Manager
feature: Dynamic Media Classic,SDK/API
role: Developer,User
exl-id: 52c12786-bbe7-4410-87bb-6245d782a68c
TQID: 'https://experienceleague.adobe.com/Fqiu-HsaRtrWMjBQudUBzr1iu3WLg7173Kf-71ikejI'
product_v2:
  - id: fd1f54a9-f50c-467d-8956-cebbaf4f3eb8
feature_v2:
  - id: a01bfd36-4ab8-4bf8-9dc0-5b45b890552e
role_v2:
  - id: b69b2659-1057-424e-8fc5-ed9e016dc554
  - id: ff6a42d2-313e-452e-93a6-792e4fad9ff8
source-git-commit: null
workflow-type: tm+mt
source-wordcount: 190
ht-degree: 0%

---

# Verschachtelte Image-Rendering-Anfragen{#nested-image-rendering-requests}

Für fortgeschrittene Anwendungen ist es möglich, das Ergebnis eines Render-Vorgangs als Materialbild zu verwenden, genau wie ein Bild, das von Image Serving abgerufen wurde.

Eine Render-Anfrage kann als Materialbild verwendet werden, indem sie im `src=` wie folgt angegeben wird:

` …&src=ir{ *[!DNL renderRequest]*}&…`

Beim `ir`-Token wird zwischen Groß- und Kleinschreibung unterschieden.

Die verschachtelte Anfrage darf nicht den Stammpfad für die Bildwiedergabe enthalten (normalerweise `http:// *[!DNL server]*/ir/render/'`), kann aber Regeltoken für die Vorverarbeitung enthalten.

Die folgenden Befehle werden ignoriert, wenn sie in verschachtelten Anfragen angegeben werden (entweder in der Anfrage-URL oder in `catalog::Modifier` oder `catalog::PostModifier`):

* `fmt=`
* `qlt=`
* `icc=`
* `iccEmbed=`
* `printRes=`
* `req=`
* `bgc=`

Ignoriert werden auch die `attribute::MaxPix` und `attribute::DefaultPix` des Materialkatalogs, der für die verschachtelte Render-Anfrage gilt.

Das Bildergebnis einer verschachtelten IR-Anfrage kann optional zwischengespeichert werden, indem `cache=on` eingeschlossen wird. Standardmäßig ist das Zwischenspeichern von Zwischendaten deaktiviert. Die Zwischenspeicherung sollte nur aktiviert werden, wenn das Zwischenbild in einer anderen Anfrage innerhalb eines angemessenen Zeitraums wiederverwendet wird. Es gilt die standardmäßige Server-seitige Cache-Verwaltung. Daten werden in einem verlustfreien Format zwischengespeichert.
