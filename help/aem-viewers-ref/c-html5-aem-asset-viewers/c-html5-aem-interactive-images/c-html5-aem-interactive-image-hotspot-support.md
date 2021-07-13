---
description: Hotspot-Support
solution: Experience Manager
title: Hotspot-Support
feature: Dynamic Media Classic,Viewer,SDK/API,Interaktive Bilder
role: Developer,User
exl-id: 9b9ccdf4-4639-4ba8-988c-c68d81192619
source-git-commit: 206e4643e3926cb85b4be2189743578f88180be7
workflow-type: tm+mt
source-wordcount: '192'
ht-degree: 0%

---

# Hotspot-Support{#hotspot-support}

Der Viewer unterstützt das Rendern von Hotspot-Symbolen über der Hauptansicht. Das Erscheinungsbild von Hotspot-Symbolen wird über CSS gesteuert, wie im Abschnitt Hotspots beschrieben.

Siehe [Hotspots](../../c-html5-aem-asset-viewers/c-html5-aem-interactive-images/c-html5-aem-interactive-image-customizingviewer/r-html5-aem-int-image-customize-hotspots.md#reference-2ac3cc414ef2467390bf53145f1d8d74).

Hotspots können entweder eine Schnellansichtsfunktion auf der Hosting-Webseite aktivieren, indem sie einen JavaScript-Rückruf auslösen oder einen Benutzer zu einer externen Webseite umleiten.

## Schnellansichts-Hotspots {#section-cda48fc9730142d0bb3326bac7df3271}

Diese Arten von Hotspots sollten mit dem Aktionstyp &quot;Schnellansicht&quot;in Dynamic Media, AEM Assets - On-Demand erstellt werden. Wenn ein Benutzer einen solchen Hotspot aktiviert, führt der Viewer den JavaScript-Rückruf `quickViewActivate` aus und übergibt ihm die Hotspot-Daten. Es wird erwartet, dass die eingebettete Webseite diesen Rückruf überwacht. Wenn die Seite Trigger wird, öffnet sie ihre eigene Schnellansichtsimplementierung.

## Zu externer Webseite umleiten {#section-ef820c71251e4215800bb99c0c9ebe16}

Hotspots, die in Dynamic Media von AEM Assets für den Aktionstyp &quot;Schnellansicht&quot;erstellt wurden - On-Demand leitet den Benutzer zu einer externen URL um. Abhängig von den bei der Bearbeitung vorgenommenen Einstellungen wird die URL in einer neuen Browser-Registerkarte, im selben Fenster oder im benannten Browser-Fenster geöffnet.
