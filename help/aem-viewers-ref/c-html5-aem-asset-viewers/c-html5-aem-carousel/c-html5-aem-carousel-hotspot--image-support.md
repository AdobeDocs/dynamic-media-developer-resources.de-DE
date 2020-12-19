---
description: 'null'
seo-description: 'null'
seo-title: Hotspot- und Imagemaps-Unterstützung
solution: Experience Manager
title: Hotspot- und Imagemaps-Unterstützung
topic: Dynamic media
uuid: 839b6a7f-4f6f-43ad-8eb8-254959c7fbac
translation-type: tm+mt
source-git-commit: 7bc7b3a86fbcdc57cfdc31745fae3afc06e44b15
workflow-type: tm+mt
source-wordcount: '216'
ht-degree: 0%

---


# Hotspot- und Imagemaps-Unterstützung{#hotspot-and-image-maps-support}

Der Viewer unterstützt das Rendering von Hotspot-Symbolen und Imagemap-Bereichen über der Haupt-Ansicht. Das Erscheinungsbild von Hotspot-Symbolen und -Regionen wird über CSS gesteuert, wie im Abschnitt Hotspots und Imagemaps anpassen beschrieben.

Siehe [Hotspots und Imagemaps](../../c-html5-aem-asset-viewers/c-html5-aem-carousel/c-html5-aem-carousel-customizingviewer/r-html5-aem-carousel-customize-hotspots-imagemaps.md#reference-2ac3cc414ef2467390bf53145f1d8d74).

Hotspots und Regionen können entweder eine Schnellfunktion auf der Hosting-Webseite aktivieren, indem sie einen JavaScript-Rückruf auslösen, oder einen Benutzer zu einer externen Webseite umleiten.

## Hotspots für die schnelle Ansicht {#section-cda48fc9730142d0bb3326bac7df3271}

Diese Arten von Hotspots oder Imagemaps sollten mit dem Aktionstyp &quot;Schnellere Ansicht&quot;in Dynamic Media AEM erstellt werden. Wenn ein Benutzer einen solchen Hotspot oder eine Imagemap aktiviert, führt der Viewer den JavaScript-Rückruf `quickViewActivate` aus und übergibt den Hotspot oder die Imagemap-Daten an ihn. Es wird erwartet, dass die eingebettete Webseite diesen Rückruf überwacht. Wenn die Seite ausgelöst wird, öffnet sie ihre eigene Quick Ansicht-Implementierung.

## Zu externer Webseite umleiten{#section-ef820c71251e4215800bb99c0c9ebe16}

Hotspots oder Imagemaps, die für den Aktionstyp &quot;Quick Ansicht&quot;in Dynamic Media erstellt wurden, leiten den Benutzer AEM an eine externe URL weiter. Abhängig von den beim Authoring vorgenommenen Einstellungen wird die URL in einer neuen Browser-Registerkarte, im selben Fenster oder im benannten Browserfenster geöffnet.
