---
description: Der interaktive Video-Viewer unterstützt das Rendern interaktiver Muster auf der Grundlage interaktiver Daten, die als Konfigurationsparameter an den Viewer übergeben werden.
seo-description: Der interaktive Video-Viewer unterstützt das Rendern interaktiver Muster auf der Grundlage interaktiver Daten, die als Konfigurationsparameter an den Viewer übergeben werden.
seo-title: Interaktive Datenunterstützung
solution: Experience Manager
title: Interaktive Datenunterstützung
topic: Dynamic media
uuid: 70b2ec2e-0ea7-461d-a185-731fb0ef8f3e
translation-type: tm+mt
source-git-commit: 16838d04b005224fad6df215ab5bf8c25ef86fc7

---


# Interaktive Datenunterstützung{#interactive-data-support}

Der interaktive Video-Viewer unterstützt das Rendern interaktiver Muster auf der Grundlage interaktiver Daten, die als Konfigurationsparameter an den Viewer übergeben werden.

Das derzeit sichtbare Farbfeld entspricht dem Videozeitbereich, mit dem es verknüpft ist. Durch Klicken auf oder Tippen auf das interaktive Farbfeld wird die ihm zugewiesene Aktion zum Zeitpunkt des Autors ausgelöst.

Interaktives Farbfeld kann entweder eine Quick-Ansicht auf der Hosting-Webseite aktivieren, indem ein JavaScript-Rückruf ausgelöst wird, oder es kann den Benutzer zu einer externen Webseite umleiten.

## Informationen zur schnellen Ansicht {#section-7990e44f641042d2a38ba20c9413b3f8}

Diese Arten interaktiver Muster sollten mit dem Aktionstyp &quot;Schnellansicht&quot;in AEM Assets - On-Demand erstellt werden. Wenn ein Benutzer ein solches Farbfeld aktiviert, führt der Viewer einen `quickViewActivate` JavaScript-Rückruf aus und übergibt die Musterdaten an dieses. Es wird erwartet, dass die eingebettete Webseite diesen Rückruf überwacht. Wenn er ausgelöst wird, öffnet die Seite ihre eigene Quick Ansicht-Implementierung.

## Zu einer externen Webseite umleiten {#section-32ebe3c3a7f74892a428c5d48801de4d}

Für den Aktionstyp &quot;Schnellansicht&quot;in AEM Assets erstellte Farbfelder - On-Demand-Konvertierung des Benutzers zu einer externen URL. Je nach den Einstellungen zum Zeitpunkt des Authoring kann die URL entweder in einer neuen Browser-Registerkarte, im selben Fenster oder im benannten Browserfenster geöffnet werden.
