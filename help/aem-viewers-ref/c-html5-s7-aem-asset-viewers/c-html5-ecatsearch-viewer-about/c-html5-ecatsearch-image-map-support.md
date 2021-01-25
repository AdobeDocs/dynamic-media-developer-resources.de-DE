---
description: Der E-Katalog-Search-Viewer unterstützt das Rendering von Imagemap-Symbolen über der Haupt-Ansicht.
seo-description: Der E-Katalog-Search-Viewer unterstützt das Rendering von Imagemap-Symbolen über der Haupt-Ansicht.
seo-title: Unterstützung von Imagemaps
solution: Experience Manager
title: Unterstützung von Imagemaps
topic: Dynamic media
uuid: 22ba8168-b384-4eda-a147-ce8172cfed11
translation-type: tm+mt
source-git-commit: 97a84e8e7edd3d834ca42069eae7c09c00d57938
workflow-type: tm+mt
source-wordcount: '328'
ht-degree: 0%

---


# Unterstützung für Imagemaps{#image-map-support}

Der E-Katalog-Search-Viewer unterstützt das Rendering von Imagemap-Symbolen über der Haupt-Ansicht.

Das Erscheinungsbild von Imagemap-Symbolen wird über CSS gesteuert, wie unter [Imagemap-Effekt](../../c-html5-s7-aem-asset-viewers/c-html5-20-ecatalog-viewer-about/c-html5-20-ecatalog-viewer-customizingviewer/r-html5-ecatalog-viewer-20-customize-imagemapeffect.md#reference-261df27d1ed145c882b26b88e33a0289) beschrieben.

Imagemaps führen eine der folgenden drei Aktionen aus: Umleitung zu einer externen Webseite, Popup-Aktivierung im Infofeld und internen Hyperlinks.

## Zu einer externen Webseite umleiten{#section-32ebe3c3a7f74892a428c5d48801de4d}

Das `href`-Attribut der Imagemap hat eine URL zur externen Ressource, entweder explizit angegeben oder in eine der unterstützten JavaScript-Vorlagenfunktionen eingeschlossen: `loadProduct()`, `loadProductCW()` und `loadProductPW()`.

Im Folgenden finden Sie ein Beispiel für eine einfache URL-Umleitung:

`href=http://www.adobe.com`

In diesem Beispiel wird dieselbe URL mit der Funktion `loadProduct()` umschlossen:

`href=javascript:loadProduct("http://www.adobe.com");void(0);`

Beachten Sie, dass der Code auf dem Client-Computer ausgeführt wird, wenn Sie den JavaScript-Code zum `HREF`-Attribut Ihrer Imagemap hinzufügen. Stellen Sie daher sicher, dass der JavaScript-Code sicher ist.

## Popup-Aktivierung für Infofeld {#section-7aa036420af646d1ad8cdc388add0b57}

Zum Arbeiten mit Infofeldern ist für eine Imagemap das Attribut `ROLLOVER_KEY` festgelegt. Legen Sie außerdem gleichzeitig das Attribut `href` fest, da sonst die externe URL-Verarbeitung die Popup-Aktivierung des Infofelds stört.

Stellen Sie abschließend sicher, dass die Viewer-Konfiguration die entsprechenden Werte für die Parameter `InfoPanelPopup.template` und optional `InfoPanelPopup.infoServerUrl` enthält.

>[!NOTE]
>
>Beachten Sie, dass beim Konfigurieren des Infofeld-Popup der HTML-Code und der an das Infofeld übergebene JavaScript-Code auf dem Client-Computer ausgeführt werden. Stellen Sie daher sicher, dass der HTML-Code und der JavaScript-Code sicher sind.

## Interne Hyperlinks {#section-6afa4fb2fe564c429e0201f019a95849}

Durch Klicken auf eine Imagemap wird ein interner Seitenwechsel im Viewer durchgeführt. Um diese Funktion zu verwenden, hat ein `href`-Attribut in der Imagemap das folgende spezielle Format:

` href=target: *`idx`*`

wobei `*`idx`*` ein auf null basierender Index des Katalogspreads ist.

Das folgende Beispiel zeigt ein `href`-Attribut für eine Imagemap, die auf den 3D-Druckbogen im E-Katalog verweist:

`href=target:2`
