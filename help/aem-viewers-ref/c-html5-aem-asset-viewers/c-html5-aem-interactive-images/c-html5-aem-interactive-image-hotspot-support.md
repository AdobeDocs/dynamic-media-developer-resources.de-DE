---
description: Hotspot-Unterstützung
solution: Experience Manager
title: Hotspot-Unterstützung
feature: Dynamic Media Classic, Viewer, SDK/API, Interaktive Bilder
role: Entwickler, Geschäftspraktiker
exl-id: 9b9ccdf4-4639-4ba8-988c-c68d81192619
translation-type: tm+mt
source-git-commit: b4344397f82eb7d2d61020909f4acc7fddea210b
workflow-type: tm+mt
source-wordcount: '195'
ht-degree: 0%

---

# Hotspot-Unterstützung{#hotspot-support}

Der Viewer unterstützt das Rendering von Hotspot-Symbolen über der Haupt-Ansicht. Das Erscheinungsbild von Hotspot-Symbolen wird über CSS gesteuert, wie im Abschnitt Hotspots beschrieben.

Siehe [Hotspots](../../c-html5-aem-asset-viewers/c-html5-aem-interactive-images/c-html5-aem-interactive-image-customizingviewer/r-html5-aem-int-image-customize-hotspots.md#reference-2ac3cc414ef2467390bf53145f1d8d74).

Hotspots können entweder eine Schnellfunktion auf der Hosting-Webseite aktivieren, indem sie einen JavaScript-Rückruf auslösen, oder einen Benutzer zu einer externen Ansicht umleiten.

## Hotspots für die schnelle Ansicht {#section-cda48fc9730142d0bb3326bac7df3271}

Diese Hotspots sollten mit dem Aktionstyp &quot;Schnellere Ansicht&quot;in Dynamic Media, AEM Assets - auf Anfrage erstellt werden. Wenn ein Benutzer einen solchen Hotspot aktiviert, führt der Viewer den JavaScript-Rückruf `quickViewActivate` aus und übergibt die Hotspot-Daten an ihn. Es wird erwartet, dass die eingebettete Webseite diesen Rückruf überwacht. Wenn die Seite Trigger wird, öffnet sie ihre eigene Quick Ansicht-Implementierung.

## Zu externer Webseite umleiten{#section-ef820c71251e4215800bb99c0c9ebe16}

Hotspots, die für den Aktionstyp &quot;Schnellere Ansicht&quot;in Dynamic Media von AEM Assets erstellt wurden, werden bei Bedarf an eine externe URL weitergeleitet. Abhängig von den beim Authoring vorgenommenen Einstellungen wird die URL in einer neuen Browser-Registerkarte, im selben Fenster oder im benannten Browserfenster geöffnet.
