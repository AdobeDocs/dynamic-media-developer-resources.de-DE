---
title: Hotspot-Unterstützung
description: Hotspot-Unterstützung
solution: Experience Manager
feature: Dynamic Media Classic,Viewers,SDK/API,Interactive Images
role: Developer,User
exl-id: 9b9ccdf4-4639-4ba8-988c-c68d81192619
source-git-commit: 24667a5ebab54ba22c4a3f6b52d19d7a31a93576
workflow-type: tm+mt
source-wordcount: '181'
ht-degree: 0%

---

# Hotspot-Unterstützung{#hotspot-support}

Der Viewer unterstützt das Rendern von Hotspot-Symbolen über der Hauptansicht. Das Aussehen von Hotspot-Symbolen wird über CSS gesteuert, wie im Abschnitt Hotspots beschrieben.

Siehe [Hotspots](../../c-html5-aem-asset-viewers/c-html5-aem-interactive-images/c-html5-aem-interactive-image-customizingviewer/r-html5-aem-int-image-customize-hotspots.md#reference-2ac3cc414ef2467390bf53145f1d8d74).

Hotspots können entweder eine Schnellansichtsfunktion auf der Hosting-Webseite aktivieren, indem sie einen JavaScript-Rückruf auslösen, oder einen Benutzer zu einer externen Webseite umleiten.

## Schnellansichts-Hotspots {#section-cda48fc9730142d0bb3326bac7df3271}

Diese Arten von Hotspots sollten mit dem Aktionstyp „Schnellansicht“ in Dynamic Media von Adobe Experience Manager Assets - On-Demand erstellt werden. Wenn ein(e) Benutzende(r) einen solchen Hotspot aktiviert, führt der Viewer den `quickViewActivate` JavaScript-Callback aus und übergibt ihm die Hotspot-Daten. Es wird erwartet, dass die einbettende Web-Seite auf diesen Callback wartet. Beim Trigger der Seite wird eine eigene Schnellansichtsimplementierung geöffnet.

## Zu externer Webseite umleiten {#section-ef820c71251e4215800bb99c0c9ebe16}

Hotspots, die für den Aktionstyp „Schnellansicht“ in Dynamic Media von Experience Manager Assets erstellt wurden - On-Demand leitet den Benutzer an eine externe URL weiter. Je nach den beim Authoring vorgenommenen Einstellungen wird die URL in einer neuen Browser-Registerkarte, im selben Fenster oder im benannten Browser-Fenster geöffnet.
