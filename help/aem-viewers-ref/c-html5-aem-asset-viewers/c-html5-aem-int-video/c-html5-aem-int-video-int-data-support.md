---
description: Der interaktive Video-Viewer unterstützt das Rendern interaktiver Muster auf der Grundlage interaktiver Daten, die als Konfigurationsparameter an den Viewer übergeben werden.
solution: Experience Manager
title: Interaktive Datenunterstützung
feature: Dynamic Media Classic, Viewer, SDK/API, Interaktive Videos
role: Entwickler, Geschäftspraktiker
translation-type: tm+mt
source-git-commit: f6c97606d7a4209427316d7367013ad9585a5cae
workflow-type: tm+mt
source-wordcount: '232'
ht-degree: 0%

---


# Interaktive Datenunterstützung{#interactive-data-support}

Der interaktive Video-Viewer unterstützt das Rendern interaktiver Muster auf der Grundlage interaktiver Daten, die als Konfigurationsparameter an den Viewer übergeben werden.

Das derzeit sichtbare Farbfeld entspricht dem Videozeitbereich, mit dem es verknüpft ist. Durch Klicken auf oder Tippen auf das interaktive Farbfeld wird die Aktion Trigger, die ihm zum Zeitpunkt des Verfassers zugewiesen wurde.

Interaktives Farbfeld kann entweder eine Quick-Ansicht auf der Hosting-Webseite aktivieren, indem ein JavaScript-Rückruf ausgelöst wird, oder es kann den Benutzer zu einer externen Webseite umleiten.

## Info zur schnellen Ansicht {#section-7990e44f641042d2a38ba20c9413b3f8}

Diese Arten interaktiver Muster sollten mit dem Aktionstyp &quot;Schnellansicht&quot;in AEM Assets - On-Demand erstellt werden. Wenn ein Benutzer ein solches Farbfeld aktiviert, führt der Viewer den JavaScript-Rückruf `quickViewActivate` aus und übergibt die Musterdaten an dieses. Es wird erwartet, dass die eingebettete Webseite diesen Rückruf überwacht und die Seite beim Trigger ihre eigene Quick Ansicht-Implementierung öffnet.

## Zu einer externen Webseite umleiten{#section-32ebe3c3a7f74892a428c5d48801de4d}

Farbfelder, die für den Aktionstyp &quot;Quickview&quot;in AEM Assets erstellt wurden - On-Demand leitet den Benutzer zu einer externen URL um. Je nach den Einstellungen zum Zeitpunkt des Authoring kann die URL entweder in einer neuen Browser-Registerkarte, im selben Fenster oder im benannten Browserfenster geöffnet werden.
