---
title: Unterstützung von Imagemaps
description: Der E-Katalog-Viewer unterstützt das Rendern von Imagemap-Symbolen über der Hauptansicht.
solution: Experience Manager
feature: Dynamic Media Classic,Viewers,SDK/API,eCatalog
role: Developer,User
exl-id: 7a2a58f9-852e-4205-96bc-08332507b6cd
source-git-commit: a919130f0940d81a221b79563b6b3e41533ba788
workflow-type: tm+mt
source-wordcount: '301'
ht-degree: 0%

---

# Unterstützung von Imagemaps{#image-map-support}

Der E-Katalog-Viewer unterstützt das Rendern von Imagemap-Symbolen über der Hauptansicht.

Das Erscheinungsbild von Zuordnungssymbolen wird über CSS gesteuert, wie unter [Bild-Map-Effekt](../../c-html5-s7-aem-asset-viewers/c-html5-20-ecatalog-viewer-about/c-html5-20-ecatalog-viewer-customizingviewer/r-html5-ecatalog-viewer-20-customize-imagemapeffect.md#reference-261df27d1ed145c882b26b88e33a0289).

Bei Imagemaps wird eine der folgenden drei Aktionen ausgeführt: zu einer externen Webseite, Popup-Aktivierung des Infofelds und internen Hyperlinks umleiten.

## Zu einer externen Webseite umleiten {#section-32ebe3c3a7f74892a428c5d48801de4d}

Die `href` -Attribut der Imagemap hat eine URL zur externen Ressource, entweder explizit angegeben oder in eine der unterstützten JavaScript-Vorlagenfunktionen eingeschlossen: `loadProduct()`, `loadProductCW()`und `loadProductPW()`.

Im Folgenden finden Sie ein Beispiel für eine einfache URL-Umleitung:

`href=http://www.adobe.com`

In diesem Beispiel wird dieselbe URL mit der `loadProduct()` Funktion:

`href=javascript:loadProduct("http://www.adobe.com");void(0);`

Wenn Sie den JavaScript-Code zum `HREF` -Attribut Ihrer Imagemap verwenden, wird der Code auf dem Computer des Clients ausgeführt. Stellen Sie daher sicher, dass der JavaScript-Code sicher ist.

## Popup-Popup-Aktivierung für Info {#section-7aa036420af646d1ad8cdc388add0b57}

Um mit Info-Bedienfeldern zu arbeiten, verfügt eine Imagemap über die `ROLLOVER_KEY` -Attributsatz. Legen Sie außerdem die `href` gleichzeitig zuordnen, andernfalls stört die externe URL-Verarbeitung die Popup-Aktivierung des Info-Bedienfelds.

Stellen Sie abschließend sicher, dass die Viewer-Konfiguration die entsprechenden Werte für `InfoPanelPopup.template` und optional `InfoPanelPopup.infoServerUrl` Parameter.

>[!NOTE]
>
>Wenn Sie das Popup für das Infofeld konfigurieren, werden der HTML-Code und der JavaScript-Code, der an das Infofeld übergeben wird, auf dem Clientcomputer ausgeführt. Stellen Sie daher sicher, dass dieser HTML-Code und JavaScript-Code sicher sind.

## Interne Hyperlinks {#section-6afa4fb2fe564c429e0201f019a95849}

Beim Auswählen einer Imagemap wird ein interner Seitenaustausch im Viewer durchgeführt. Um diese Funktion zu verwenden, muss eine `href` -Attribut in der Imagemap hat das folgende spezielle Format:

` href=target: *`idx`*`

Wo `*`idx`*` ist ein nullbasierter Index des Katalogspreads.

Im Folgenden finden Sie ein Beispiel für eine `href` -Attribut für eine Imagemap, die auf den 3D-Spread im eCatalog verweist:

`href=target:2`
