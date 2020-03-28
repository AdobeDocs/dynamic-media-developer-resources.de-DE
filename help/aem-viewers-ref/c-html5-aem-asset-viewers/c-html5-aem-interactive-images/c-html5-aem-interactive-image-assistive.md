---
description: Alle Viewer-Komponenten unterstützen ARIA-Rollen und -Attribute (Accessible Rich Internet Applications), um die Integration mit Hilfstechnologien wie Bildschirmlesehilfen zu verbessern.
seo-description: Alle Viewer-Komponenten unterstützen ARIA-Rollen und -Attribute (Accessible Rich Internet Applications), um die Integration mit Hilfstechnologien wie Bildschirmlesehilfen zu verbessern.
seo-title: Unterstützung von Technologien
solution: Experience Manager
title: Unterstützung von Technologien
topic: Dynamic media
uuid: 5f6a021f-750c-40e1-be01-86c3750fd25f
translation-type: tm+mt
source-git-commit: 7bc7b3a86fbcdc57cfdc31745fae3afc06e44b15

---


# Unterstützung von Technologien{#assistive-technology-support}

Alle Viewer-Komponenten unterstützen ARIA-Rollen und -Attribute (Accessible Rich Internet Applications), um die Integration mit Hilfstechnologien wie Bildschirmlesehilfen zu verbessern.

Für das Viewer-Element der obersten Ebene sind Rollen `region` und `aria-label` -Attribute standardmäßig auf den Namen des Viewers eingestellt. Sie können die Beschriftung mit dem Symbol `Container.LABEL` lokale Anpassung steuern.

Die wichtigste Ansicht spielt eine Rolle `application`. Eine kurze Beschreibung der Hauptkomponente `aria-roledescription`mit dem durch das `ROLE_DESCRIPTION` lokale Anpassung-Symbol der jeweiligen Hauptkomponente definierten Wert wird in bereitgestellt. Navigationshinweise für Tastaturbenutzer werden bereitgestellt, `aria-describedby`der Text für den Verwendungshinweis stammt aus dem Symbol `USAGE_HINT` lokale Anpassung. Wenn für ein Asset eine Beschriftung im Feld UserData definiert ist, wird das `aria-label` -Attribut mit dem Wert dieser Beschriftung festgelegt.

Hotspots, Regionen und Imagemaps haben die Rolle `button` und den beschreibenden Text mit dem `aria-label` Attribut und dem Wert der Hotspot- oder Imagemap-Beschriftung. Wenn der Benutzer den Fokus auf Hotspots oder Imagemaps legt, werden Navigationshinweise für Tastaturbenutzer bereitgestellt, `aria-describedby`wobei der Text für den Verwendungshinweis aus dem Symbol &quot; `USAGE_HINT` lokale Anpassung&quot;stammt.
