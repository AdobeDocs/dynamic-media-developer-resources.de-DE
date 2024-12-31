---
description: Der E-Katalog-Such-Viewer unterstützt das Rendern von Imagemap-Symbolen über der Hauptansicht.
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

Der E-Katalog-Such-Viewer unterstützt das Rendern von Imagemap-Symbolen über der Hauptansicht.

Das Erscheinungsbild von Zuordnungssymbolen wird über CSS gesteuert, wie unter [Imagemap-Effekt](../../c-html5-s7-aem-asset-viewers/c-html5-20-ecatalog-viewer-about/c-html5-20-ecatalog-viewer-customizingviewer/r-html5-ecatalog-viewer-20-customize-imagemapeffect.md#reference-261df27d1ed145c882b26b88e33a0289) beschrieben.

Imagemaps führen eine der folgenden drei Aktionen aus: Umleitung zu einer externen Web-Seite, Popup-Aktivierung des Infobereichs und interne Hyperlinks.

## Zu einer externen Webseite umleiten {#section-32ebe3c3a7f74892a428c5d48801de4d}

Das `href`-Attribut der Imagemap weist eine URL zu der externen Ressource auf, die entweder explizit angegeben oder in eine der unterstützten JavaScript-Vorlagenfunktionen eingeschlossen ist: `loadProduct()`, `loadProductCW()` und `loadProductPW()`.

Im Folgenden finden Sie ein Beispiel für eine einfache URL-Umleitung:

`href=http://www.adobe.com`

In diesem Beispiel wird dieselbe URL von der `loadProduct()` umschlossen:

`href=javascript:loadProduct("http://www.adobe.com");void(0);`

Beachten Sie, dass beim Hinzufügen des JavaScript-Codes zum `HREF`-Attribut Ihrer Imagemap der Code auf dem Computer des Clients ausgeführt wird. Stellen Sie daher sicher, dass der JavaScript-Code sicher ist.

## Popup-Aktivierung des Infobereichs {#section-7aa036420af646d1ad8cdc388add0b57}

Für das Arbeiten mit Info-Bedienfeldern ist in einer Imagemap das Attribut `ROLLOVER_KEY` festgelegt. Legen Sie außerdem gleichzeitig das Attribut `href` fest, da andernfalls die Verarbeitung der externen URLs die Aktivierung des Popup-Fensters „Info“ beeinträchtigt.

Stellen Sie abschließend sicher, dass die Viewer-Konfiguration die entsprechenden Werte für `InfoPanelPopup.template` und optional `InfoPanelPopup.infoServerUrl` Parameter enthält.

>[!NOTE]
>
>Beachten Sie, dass beim Konfigurieren des Infobedienfeld-Popup der HTML-Code und der JavaScript-Code, die an das Infobedienfeld übergeben werden, auf dem Client-Computer ausgeführt werden. Stellen Sie daher sicher, dass dieser HTML-Code und JavaScript-Code sicher sind.

## Interne Hyperlinks {#section-6afa4fb2fe564c429e0201f019a95849}

Durch Klicken auf eine Imagemap wird die interne Seite im Viewer ausgetauscht. Um diese Funktion zu verwenden, hat ein `href`-Attribut in der Imagemap das folgende spezielle Format:

` href=target: *`IDX`*`

Dabei `*`IDX`*` ein Index auf Nullbasis des Katalog-Spreads.

Im Folgenden finden Sie ein Beispiel für ein `href`-Attribut für eine Imagemap, das auf die 3D-Spreizung im E-Katalog verweist:

`href=target:2`
