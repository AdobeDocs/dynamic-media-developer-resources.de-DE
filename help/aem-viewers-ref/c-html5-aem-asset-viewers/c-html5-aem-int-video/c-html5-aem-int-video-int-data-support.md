---
description: Der Viewer für interaktive Videos unterstützt das Rendern interaktiver Muster basierend auf interaktiven Daten, die als Konfigurationsparameter an den Viewer übergeben werden.
solution: Experience Manager
title: Unterstützung interaktiver Daten
feature: Dynamic Media Classic,Viewer,SDK/API,interaktive Videos
role: Developer,User
exl-id: 9118bf02-16ae-4dab-92e4-17347e866cc9
source-git-commit: 206e4643e3926cb85b4be2189743578f88180be7
workflow-type: tm+mt
source-wordcount: '229'
ht-degree: 0%

---

# Unterstützung interaktiver Daten{#interactive-data-support}

Der Viewer für interaktive Videos unterstützt das Rendern interaktiver Muster basierend auf interaktiven Daten, die als Konfigurationsparameter an den Viewer übergeben werden.

Das derzeit sichtbare Muster entspricht dem Zeitbereich des Videos, mit dem es verknüpft ist. Durch Klicken oder Tippen auf das interaktive Muster wird die ihm zugewiesene Aktion zum Zeitpunkt der Erstellung Trigger.

Interaktive Muster können entweder eine Schnellansicht auf der Hosting-Webseite aktivieren, indem ein JavaScript-Rückruf ausgelöst wird, oder der Benutzer kann zu einer externen Webseite umgeleitet werden.

## Über Schnellansicht {#section-7990e44f641042d2a38ba20c9413b3f8}

Diese Arten interaktiver Muster sollten mit dem Aktionstyp &quot;Schnellansicht&quot;in AEM Assets - On-Demand erstellt werden. Wenn ein Benutzer ein solches Muster aktiviert, führt der Viewer den JavaScript-Rückruf `quickViewActivate` aus und übergibt ihm die Musterdaten. Es wird erwartet, dass die eingebettete Webseite diesen Rückruf überwacht und beim Trigger die Seite eine eigene Schnellansichtsimplementierung öffnet.

## Zu einer externen Webseite umleiten {#section-32ebe3c3a7f74892a428c5d48801de4d}

Für den Aktionstyp &quot;Schnellansicht&quot;in AEM Assets erstellte Muster - Benutzer werden bei Bedarf zu einer externen URL umgeleitet. Je nach den Einstellungen zum Zeitpunkt der Bearbeitung kann die URL entweder in einer neuen Browser-Registerkarte, im selben Fenster oder im benannten Browser-Fenster geöffnet werden.
