---
title: Unterstützung interaktiver Daten
description: Der interaktive Video-Viewer unterstützt das Rendern interaktiver Muster, die auf interaktiven Daten basieren, die als Konfigurationsparameter an den Viewer übergeben werden.
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

Der interaktive Video-Viewer unterstützt das Rendern interaktiver Muster, die auf interaktiven Daten basieren, die als Konfigurationsparameter an den Viewer übergeben werden.

Der aktuell sichtbare Farbfeld entspricht dem Video-Zeitbereich, mit dem es verknüpft ist. Durch Klicken oder Tippen auf die interaktiven Musteraktionen wird die Trigger bei der Bearbeitung mit der ihnen zugewiesenen Aktion verknüpft.

Interaktive Farb-/Bildmuster können entweder eine Schnellansicht auf der Host-Web-Seite aktivieren, indem sie einen JavaScript-Callback auslösen, oder sie können den Benutzer zu einer externen Web-Seite umleiten.

## Über Schnellansichten {#section-7990e44f641042d2a38ba20c9413b3f8}

Diese Arten interaktiver Muster sollten unter Verwendung des Aktionstyps „Schnellansicht“ in Adobe Experience Manager Assets - On-Demand erstellt werden. Wenn Benutzende einen solchen Musterabschnitt aktivieren, führt der Viewer `quickViewActivate` JavaScript-Rückruf aus und übergibt ihm die Musterdaten. Es wird erwartet, dass die einbettende Web-Seite auf diesen Callback wartet. Wenn er Trigger hat, öffnet die Seite ihre eigene Schnellansichtsimplementierung.

## Zu einer externen Webseite umleiten {#section-32ebe3c3a7f74892a428c5d48801de4d}

Für den Aktionstyp „Schnellansicht“ in Experience Manager Assets erstellte Muster leiten den Benutzer bei Bedarf zu einer externen URL weiter. Je nach den Einstellungen zum Zeitpunkt der Bearbeitung kann die URL entweder in einer neuen Browser-Registerkarte, im selben Fenster oder im benannten Browser-Fenster geöffnet werden.
