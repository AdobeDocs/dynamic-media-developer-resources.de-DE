---
title: Unterstützung interaktiver Daten
description: Der Viewer für interaktive Videos unterstützt das Rendern interaktiver Muster basierend auf interaktiven Daten, die als Konfigurationsparameter an den Viewer übergeben werden.
solution: Experience Manager
feature: Dynamic Media Classic,Viewers,SDK/API,Interactive Videos
role: Developer,User
exl-id: 9118bf02-16ae-4dab-92e4-17347e866cc9
source-git-commit: 17556c64af32c957ac25312e2a3288a8d86b5679
workflow-type: tm+mt
source-wordcount: '221'
ht-degree: 0%

---

# Unterstützung interaktiver Daten{#interactive-data-support}

Der Viewer für interaktive Videos unterstützt das Rendern interaktiver Muster basierend auf interaktiven Daten, die als Konfigurationsparameter an den Viewer übergeben werden.

Das derzeit sichtbare Muster entspricht dem Zeitbereich des Videos, mit dem es verknüpft ist. Durch Klicken oder Tippen auf das interaktive Muster wird die ihm zugewiesene Aktion zum Zeitpunkt der Erstellung Trigger.

Interaktive Muster können entweder eine Schnellansicht auf der Hosting-Web-Seite aktivieren, indem ein JavaScript-Rückruf ausgelöst wird, oder der Benutzer kann zu einer externen Web-Seite weitergeleitet werden.

## Über Schnellansicht {#section-7990e44f641042d2a38ba20c9413b3f8}

Diese Arten interaktiver Muster sollten mit dem Aktionstyp &quot;Schnellansicht&quot;in Adobe Experience Manager Assets - On-Demand erstellt werden. Wenn ein Benutzer ein solches Muster aktiviert, führt der Viewer den JavaScript-Rückruf `quickViewActivate` aus und übergibt ihm die Musterdaten. Es wird erwartet, dass die eingebettete Web-Seite diesen Rückruf überwacht und beim Trigger die Seite eine eigene Schnellansichtsimplementierung öffnet.

## Zu einer externen Webseite umleiten {#section-32ebe3c3a7f74892a428c5d48801de4d}

Muster, die für den Aktionstyp &quot;Schnellansicht&quot;in Experience Manager-Assets erstellt wurden - On-Demand leitet den Benutzer zu einer externen URL um. Je nach den Einstellungen zum Zeitpunkt der Bearbeitung kann die URL entweder in einer neuen Browser-Registerkarte, im selben Fenster oder im benannten Browser-Fenster geöffnet werden.
