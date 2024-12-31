---
title: Unterstützung von Hotspot- und Imagemaps
description: Unterstützung von Hotspot- und Imagemaps
solution: Experience Manager
feature: Dynamic Media Classic,Viewers,SDK/API,Carousel Banners
role: Developer,User
exl-id: b441e241-809e-47cf-a309-57283bd0532b
source-git-commit: 8d5dbc2d2b5e228f8496fd71633bf1cb96218226
workflow-type: tm+mt
source-wordcount: '212'
ht-degree: 0%

---

# Unterstützung von Hotspot- und Imagemaps{#hotspot-and-image-maps-support}

Der Viewer unterstützt das Rendern von Hotspot-Symbolen und Imagemap-Bereichen über der Hauptansicht. Das Aussehen von Hotspot-Symbolen und -Regionen wird über CSS gesteuert, wie im Abschnitt Anpassen von Hotspots und Imagemaps beschrieben.

Siehe [Hotspots und Imagemaps](../../c-html5-aem-asset-viewers/c-html5-aem-carousel/c-html5-aem-carousel-customizingviewer/r-html5-aem-carousel-customize-hotspots-imagemaps.md#reference-2ac3cc414ef2467390bf53145f1d8d74).

Hotspots und Regionen können entweder eine Schnellansichtsfunktion auf der Host-Web-Seite aktivieren, indem sie einen JavaScript-Callback auslösen, oder einen Benutzer zu einer externen Web-Seite umleiten.

## Schnellansichts-Hotspots {#section-cda48fc9730142d0bb3326bac7df3271}

Diese Arten von Hotspots oder Imagemaps sollten mit dem Aktionstyp „Schnellansicht“ in Dynamic Media von Adobe Experience Manager erstellt werden. Wenn ein(e) Benutzende(r) einen solchen Hotspot oder eine solche Imagemap aktiviert, führt der Viewer den `quickViewActivate` JavaScript-Callback aus und übergibt ihm die Hotspot- oder Imagemap-Daten. Es wird erwartet, dass die einbettende Web-Seite auf diesen Callback wartet. Beim Trigger der Seite wird eine eigene Schnellansichtsimplementierung geöffnet.

## Zu externer Webseite umleiten {#section-ef820c71251e4215800bb99c0c9ebe16}

Hotspots oder Imagemaps, die für den Aktionstyp „Schnellansicht“ in Dynamic Media oder Experience Manager erstellt wurden, leiten den Benutzer an eine externe URL weiter. Je nach den beim Authoring vorgenommenen Einstellungen wird die URL in einer neuen Browser-Registerkarte, im selben Fenster oder im benannten Browser-Fenster geöffnet.
