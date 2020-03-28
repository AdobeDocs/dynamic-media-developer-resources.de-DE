---
description: 'null'
seo-description: 'null'
seo-title: Hotspot-Unterstützung
solution: Experience Manager
title: Hotspot-Unterstützung
topic: Dynamic media
uuid: 62e0e55a-55a3-417d-ad51-ec77a7c16ac3
translation-type: tm+mt
source-git-commit: 7bc7b3a86fbcdc57cfdc31745fae3afc06e44b15

---


# Hotspot-Unterstützung{#hotspot-support}

Der Viewer unterstützt das Rendering von Hotspot-Symbolen über der Haupt-Ansicht. Das Erscheinungsbild von Hotspot-Symbolen wird über CSS gesteuert, wie im Abschnitt Hotspots beschrieben.

Siehe [Hotspots](../../c-html5-aem-asset-viewers/c-html5-aem-interactive-images/c-html5-aem-interactive-image-customizingviewer/r-html5-aem-int-image-customize-hotspots.md#reference-2ac3cc414ef2467390bf53145f1d8d74).

Hotspots können entweder eine Schnellfunktion auf der Hosting-Webseite aktivieren, indem sie einen JavaScript-Rückruf auslösen, oder einen Benutzer zu einer externen Ansicht umleiten.

## Hotspots für die schnelle Ansicht {#section-cda48fc9730142d0bb3326bac7df3271}

Diese Arten von Hotspots sollten mit dem Aktionstyp &quot;Schnellere Ansicht&quot;in dynamischen Medien von AEM Assets - On Demand erstellt werden. Wenn ein Benutzer einen solchen Hotspot aktiviert, führt der Viewer den `quickViewActivate` JavaScript-Rückruf aus und übergibt die Hotspot-Daten an ihn. Es wird erwartet, dass die eingebettete Webseite diesen Rückruf überwacht. Wenn die Seite ausgelöst wird, öffnet sie ihre eigene Quick Ansicht-Implementierung.

## Zu externer Webseite umleiten {#section-ef820c71251e4215800bb99c0c9ebe16}

Hotspots, die für den Aktionstyp &quot;Schnellere Ansicht&quot;in dynamischen Medien von AEM Assets erstellt wurden, werden bei Bedarf an eine externe URL weitergeleitet. Abhängig von den beim Authoring vorgenommenen Einstellungen wird die URL in einer neuen Browser-Registerkarte, im selben Fenster oder im benannten Browserfenster geöffnet.
