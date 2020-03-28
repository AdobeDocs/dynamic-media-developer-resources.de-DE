---
description: Alle Viewer-Komponenten unterstützen ARIA-Rollen und -Attribute (Accessible Rich Internet Applications), um die Integration mit Hilfstechnologien wie Bildschirmlesehilfen zu verbessern.
seo-description: Alle Viewer-Komponenten unterstützen ARIA-Rollen und -Attribute (Accessible Rich Internet Applications), um die Integration mit Hilfstechnologien wie Bildschirmlesehilfen zu verbessern.
seo-title: Unterstützung von Technologien
solution: Experience Manager
title: Unterstützung von Technologien
topic: Dynamic media
uuid: 525ab400-c022-4f33-a0e3-bafb6019f1a7
translation-type: tm+mt
source-git-commit: 7bc7b3a86fbcdc57cfdc31745fae3afc06e44b15

---


# Unterstützung von Technologien{#assistive-technology-support}

Alle Viewer-Komponenten unterstützen ARIA-Rollen und -Attribute (Accessible Rich Internet Applications), um die Integration mit Hilfstechnologien wie Bildschirmlesehilfen zu verbessern.

Für das Viewer-Element der obersten Ebene sind Rollen `region` und `aria-label` -Attribute standardmäßig auf den Namen des Viewers eingestellt. Sie können die Beschriftung mit dem Symbol `Container.LABEL` lokale Anpassung steuern.

Schaltflächen haben die Rolle `button` und den beschreibenden Text mit dem `aria-label` Attribut. Der `aria-label` Attributwert wird aus dem lokale Anpassungen-Symbol der Schaltfläche gefüllt. Wenn eine Schaltfläche deaktiviert ist, wird das `aria-disabled` Attribut entsprechend eingestellt.

Die wichtigste Ansicht spielt eine Rolle `application`. Eine kurze Beschreibung der Hauptkomponente `aria-roledescription`mit dem durch das `ROLE_DESCRIPTION` lokale Anpassung-Symbol der jeweiligen Hauptkomponente definierten Wert wird in bereitgestellt. Navigationshinweise für Tastaturbenutzer werden bereitgestellt, `aria-describedby`der Text für den Verwendungshinweis stammt aus dem Symbol `USAGE_HINT` lokale Anpassung. Wenn für ein Asset eine Beschriftung im Feld UserData definiert ist, wird das `aria-label` -Attribut mit dem Wert dieser Beschriftung festgelegt.

Hotspots, Regionen und Imagemaps haben die Rolle `button` und den beschreibenden Text mit dem `aria-label` Attribut und dem Wert der Hotspot- oder Imagemap-Beschriftung. Wenn der Benutzer den Fokus auf Hotspots oder Imagemaps legt, werden Navigationshinweise für Tastaturbenutzer bereitgestellt, `aria-describedby`wobei der Text für den Verwendungshinweis aus dem Symbol &quot; `USAGE_HINT` lokale Anpassung&quot;stammt.

Miniaturansichten haben die Funktion `dialog` mit dem `aria-label` Attribut, das vom Symbol für die `ThumbnailGridView.LABEL` lokale Anpassung gesteuert wird. Einzelne Miniaturansichten haben eine Rolle `button`. Wenn eine Miniaturansicht ausgewählt ist, wird das `aria-selected` Attribut auf `true`.

Komponenten, die Muster anzeigen, haben die Rolle `listbox` mit dem `aria-label` Attribut, das auf den Wert des `LABEL` Komponentensymbols gesetzt ist. Einzelne Muster haben die Rolle `option` mit `aria-setsize` und `aria-posinset` Attributen, um die Musterposition im Satz zu beschreiben. Wenn ein Farbfeld ausgewählt ist, wird das `aria-selected` Attribut auf `true`.

Dropdown-Listen werden über Schaltflächen aktiviert, bei denen zusätzliche `aria-haspopup` Attribute auf `true` und das `aria-controls` Attribut auf das tatsächliche Dropdown-Bedienfeldelement verweisen. Das Dropdown-Feld selbst hat die Rolle `menu` der Unterelemente `menuitem`. Für jedes Menüelement wird das `aria-label` Attribut angegeben.

Die Suchbenutzeroberfläche ist im Element mit der Rolle gruppiert `search`. Das Sucheingabefeld hat die Funktion `searchbox` und verweist auf die informative Beschriftung, die durch das `SearchPanel.INFO_PROMPT` lokale Anpassung-Symbol mit `aria-describedby` Attribut gesteuert wird.

Modale Dialogfelder haben die Rolle `dialog`. Das Kopfzeilenelement des Dialogfelds wird durch das `aria-labelledby` Attribut referenziert.
