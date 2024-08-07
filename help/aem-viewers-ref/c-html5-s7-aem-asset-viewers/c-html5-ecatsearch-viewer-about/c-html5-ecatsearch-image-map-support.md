---
description: Der eCatalog Search Viewer unterstützt das Rendern von Imagemap-Symbolen über der Hauptansicht.
solution: Experience Manager
title: Unterstützung von Imagemaps
feature: Dynamic Media Classic,Viewers,SDK/API,eCatalog Search
role: Developer,User
exl-id: 58e7523f-1615-4da4-bb09-a995bf427bfc
source-git-commit: 206e4643e3926cb85b4be2189743578f88180be7
workflow-type: tm+mt
source-wordcount: '310'
ht-degree: 0%

---

# Unterstützung von Imagemaps{#image-map-support}

Der eCatalog Search Viewer unterstützt das Rendern von Imagemap-Symbolen über der Hauptansicht.

Das Erscheinungsbild von Zuordnungssymbolen wird über CSS gesteuert, wie unter [Bildarteffekt](../../c-html5-s7-aem-asset-viewers/c-html5-20-ecatalog-viewer-about/c-html5-20-ecatalog-viewer-customizingviewer/r-html5-ecatalog-viewer-20-customize-imagemapeffect.md#reference-261df27d1ed145c882b26b88e33a0289) beschrieben.

Bei Imagemaps wird eine der folgenden drei Aktionen ausgeführt: Umleitung zu einer externen Webseite, Popup-Aktivierung des Info-Bedienfelds und interne Hyperlinks.

## Zu einer externen Webseite umleiten {#section-32ebe3c3a7f74892a428c5d48801de4d}

Das Attribut `href` der Imagemap hat eine URL zur externen Ressource, die entweder explizit angegeben oder in eine der unterstützten JavaScript-Vorlagenfunktionen eingeschlossen ist: `loadProduct()`, `loadProductCW()` und `loadProductPW()`.

Im Folgenden finden Sie ein Beispiel für eine einfache URL-Umleitung:

`href=http://www.adobe.com`

In diesem Beispiel wird dieselbe URL mit der Funktion `loadProduct()` umschlossen:

`href=javascript:loadProduct("http://www.adobe.com");void(0);`

Beachten Sie, dass der Code auf dem Client-Computer ausgeführt wird, wenn Sie den JavaScript-Code zum Attribut `HREF` Ihrer Imagemap hinzufügen. Stellen Sie daher sicher, dass der JavaScript-Code sicher ist.

## Popup-Popup-Aktivierung für Info {#section-7aa036420af646d1ad8cdc388add0b57}

Für die Verwendung mit Info-Bedienfeldern ist für eine Imagemap das Attribut `ROLLOVER_KEY` festgelegt. Legen Sie außerdem das Attribut `href` gleichzeitig fest. Andernfalls stört die externe URL-Verarbeitung die Popup-Aktivierung des Bedienfelds &quot;Info&quot;.

Stellen Sie schließlich sicher, dass die Viewer-Konfiguration die entsprechenden Werte für die Parameter `InfoPanelPopup.template` und optional `InfoPanelPopup.infoServerUrl` enthält.

>[!NOTE]
>
>Beachten Sie, dass beim Konfigurieren von Popup für das Infofeld der HTML-Code und der JavaScript-Code, der an das Infofeld übergeben wird, auf dem Computer des Clients ausgeführt werden. Stellen Sie daher sicher, dass dieser HTML-Code und JavaScript-Code sicher sind.

## Interne Hyperlinks {#section-6afa4fb2fe564c429e0201f019a95849}

Durch Klicken auf eine Imagemap wird ein interner Seitenaustausch im Viewer durchgeführt. Um diese Funktion zu verwenden, hat ein `href` -Attribut in der Imagemap das folgende spezielle Format:

` href=target: *`idx`*`

wobei `*`idx`*` ein nullbasierter Index des Katalogplatzes ist.

Im Folgenden finden Sie ein Beispiel für ein `href` -Attribut für eine Imagemap, die auf den 3D-Stream im eCatalog verweist:

`href=target:2`
