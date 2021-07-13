---
description: Unterstützung von Hotspots und Imagemaps
solution: Experience Manager
title: Unterstützung von Hotspots und Imagemaps
feature: Dynamic Media Classic,Viewer,SDK/API,Karussellbanner
role: Developer,User
exl-id: b441e241-809e-47cf-a309-57283bd0532b
source-git-commit: 206e4643e3926cb85b4be2189743578f88180be7
workflow-type: tm+mt
source-wordcount: '222'
ht-degree: 0%

---

# Unterstützung von Hotspots und Imagemaps{#hotspot-and-image-maps-support}

Der Viewer unterstützt das Rendern von Hotspot-Symbolen und Imagemap-Bereichen über der Hauptansicht. Das Erscheinungsbild von Hotspot-Symbolen und -Regionen wird über CSS gesteuert, wie im Abschnitt Hotspots und Imagemaps anpassen beschrieben.

Siehe [Hotspots und Imagemaps](../../c-html5-aem-asset-viewers/c-html5-aem-carousel/c-html5-aem-carousel-customizingviewer/r-html5-aem-carousel-customize-hotspots-imagemaps.md#reference-2ac3cc414ef2467390bf53145f1d8d74).

Hotspots und Regionen können entweder eine Schnellansichtsfunktion auf der Hostingwebseite aktivieren, indem sie einen JavaScript-Rückruf auslösen oder einen Benutzer zu einer externen Webseite umleiten.

## Schnellansichts-Hotspots {#section-cda48fc9730142d0bb3326bac7df3271}

Diese Arten von Hotspots oder Imagemaps sollten mit dem Aktionstyp &quot;Schnellansicht&quot;in Dynamic Media von AEM erstellt werden. Wenn ein Benutzer einen solchen Hotspot oder eine solche Imagemap aktiviert, führt der Viewer den JavaScript-Rückruf `quickViewActivate` aus und übergibt ihm den Hotspot oder die Imagemap-Daten. Es wird erwartet, dass die eingebettete Webseite diesen Rückruf überwacht. Wenn die Seite Trigger wird, öffnet sie ihre eigene Schnellansichtsimplementierung.

## Zu externer Webseite umleiten {#section-ef820c71251e4215800bb99c0c9ebe16}

Hotspots oder Imagemaps, die für den Aktionstyp &quot;Schnellansicht&quot;in Dynamic Media von AEM erstellt wurden, leiten den Benutzer zu einer externen URL weiter. Abhängig von den bei der Bearbeitung vorgenommenen Einstellungen wird die URL in einer neuen Browser-Registerkarte, im selben Fenster oder im benannten Browser-Fenster geöffnet.
