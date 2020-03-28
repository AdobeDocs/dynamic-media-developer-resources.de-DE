---
description: Alle Viewer-Komponenten unterstützen ARIA-Rollen und -Attribute (Accessible Rich Internet Applications), um die Integration mit Hilfstechnologien wie Bildschirmlesehilfen zu verbessern.
seo-description: Alle Viewer-Komponenten unterstützen ARIA-Rollen und -Attribute (Accessible Rich Internet Applications), um die Integration mit Hilfstechnologien wie Bildschirmlesehilfen zu verbessern.
seo-title: Unterstützung von Technologien
solution: Experience Manager
title: Unterstützung von Technologien
topic: Dynamic media
uuid: 52f5dad9-7309-4385-99bc-79d02d3ba2d9
translation-type: tm+mt
source-git-commit: 7bc7b3a86fbcdc57cfdc31745fae3afc06e44b15

---


# Unterstützung von Technologien{#assistive-technology-support}

Alle Viewer-Komponenten unterstützen ARIA-Rollen und -Attribute (Accessible Rich Internet Applications), um die Integration mit Hilfstechnologien wie Bildschirmlesehilfen zu verbessern.

Für das Viewer-Element der obersten Ebene sind Rollen `region` und `aria-label` -Attribute standardmäßig auf den Namen des Viewers eingestellt. Sie können die Beschriftung mit dem Symbol `Container.LABEL` lokale Anpassung steuern.

Schaltflächen haben die Rolle `button` und den beschreibenden Text mit dem `aria-label` Attribut. Der `aria-label` Attributwert wird aus dem lokale Anpassungen-Symbol der Schaltfläche gefüllt. Wenn eine Schaltfläche deaktiviert ist, wird das `aria-disabled` Attribut entsprechend eingestellt.

Slider-Komponenten haben die Rolle `slider` mit Attributen `aria-valuenow`, `aria-valuemin`und `aria-valuemax` beschreiben die aktuelle Reglerposition.

Dropdown-Listen werden über Schaltflächen aktiviert, bei denen zusätzliche `aria-haspopup` Attribute auf das tatsächliche Dropdown-Bedienfeldelement festgelegt `true` und `aria-controls` Attribute referenziert werden. Das Dropdown-Feld selbst hat die Rolle `menu` der Unterelemente `menuitem`. Für jedes Menüelement wird das `aria-label` Attribut angegeben.

Modale Dialogfelder haben die Rolle `dialog`. Das Kopfzeilenelement des Dialogfelds wird durch das `aria-labelledby` Attribut referenziert.
