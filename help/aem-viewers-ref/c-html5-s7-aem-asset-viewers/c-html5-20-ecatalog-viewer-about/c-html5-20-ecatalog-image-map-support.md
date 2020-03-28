---
description: Der E-Katalog-Viewer unterstützt das Rendering von Imagemap-Symbolen über der Haupt-Ansicht.
seo-description: Der E-Katalog-Viewer unterstützt das Rendering von Imagemap-Symbolen über der Haupt-Ansicht.
seo-title: Unterstützung von Imagemaps
solution: Experience Manager
title: Unterstützung von Imagemaps
topic: Dynamic media
uuid: 69aeda21-909d-45da-bcf5-73ade8c5adda
translation-type: tm+mt
source-git-commit: 7bc7b3a86fbcdc57cfdc31745fae3afc06e44b15

---


# Unterstützung von Imagemaps{#image-map-support}

Der E-Katalog-Viewer unterstützt das Rendering von Imagemap-Symbolen über der Haupt-Ansicht.

Das Erscheinungsbild von Imagemap-Symbolen wird über CSS gesteuert, wie im [Imagemap-Effekt](../../c-html5-s7-aem-asset-viewers/c-html5-20-ecatalog-viewer-about/c-html5-20-ecatalog-viewer-customizingviewer/r-html5-ecatalog-viewer-20-customize-imagemapeffect.md#reference-261df27d1ed145c882b26b88e33a0289)beschrieben.

Imagemaps führen eine der folgenden drei Aktionen aus: Umleitung zu einer externen Webseite, Popup-Aktivierung im Infofeld und internen Hyperlinks.

## Zu einer externen Webseite umleiten {#section-32ebe3c3a7f74892a428c5d48801de4d}

Das `href` Attribut der Imagemap hat eine URL zur externen Ressource, entweder explizit angegeben oder in eine der unterstützten JavaScript-Vorlagenfunktionen eingeschlossen: `loadProduct()`, `loadProductCW()`und `loadProductPW()`.

Im Folgenden finden Sie ein Beispiel für eine einfache URL-Umleitung:

`href=http://www.adobe.com`

In diesem Beispiel wird dieselbe URL mit der `loadProduct()` Funktion umschlossen:

`href=javascript:loadProduct("http://www.adobe.com");void(0);`

Be aware that when you add the JavaScript code into the `HREF` attribute of your image map, the code is run on the client’s computer. Stellen Sie daher sicher, dass der JavaScript-Code sicher ist.

## Popup-Aktivierung des Infofelds {#section-7aa036420af646d1ad8cdc388add0b57}

Zum Arbeiten mit Infofeldern wird für eine Imagemap die `ROLLOVER_KEY` Attributeinstellung festgelegt. Legen Sie das `href` Attribut gleichzeitig fest, da sonst die externe URL-Verarbeitung die Popup-Aktivierung des Infofelds beeinträchtigt.

Stellen Sie abschließend sicher, dass die Viewer-Konfiguration die entsprechenden Werte für `InfoPanelPopup.template` und optional `InfoPanelPopup.infoServerUrl` Parameter enthält.

>[!NOTE]
>
>Beachten Sie, dass beim Konfigurieren des Infofeld-Popup der HTML-Code und der an das Infofeld übergebene JavaScript-Code auf dem Client-Computer ausgeführt werden. Stellen Sie daher sicher, dass der HTML-Code und der JavaScript-Code sicher sind.

## Interne Hyperlinks {#section-6afa4fb2fe564c429e0201f019a95849}

Durch Klicken auf eine Imagemap wird ein interner Seitenwechsel im Viewer durchgeführt. Um diese Funktion zu verwenden, hat ein `href` Attribut in der Imagemap das folgende spezielle Format:

` href=target: *`idx`*`

wobei ` *`idx`*` ein auf null basierender Index des Katalogspreads ist.

Im Folgenden finden Sie ein Beispiel für ein `href` Attribut für eine Imagemap, das auf den 3D-Druckbogen im E-Katalog verweist:

`href=target:2`
