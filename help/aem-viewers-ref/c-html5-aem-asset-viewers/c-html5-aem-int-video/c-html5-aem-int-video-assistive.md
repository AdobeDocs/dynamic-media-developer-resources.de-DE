---
description: Alle Viewer-Komponenten unterstützen ARIA-Rollen und -Attribute (Accessible Rich Internet Applications), um die Integration mit Hilfstechnologien wie Bildschirmlesehilfen zu verbessern.
seo-description: Alle Viewer-Komponenten unterstützen ARIA-Rollen und -Attribute (Accessible Rich Internet Applications), um die Integration mit Hilfstechnologien wie Bildschirmlesehilfen zu verbessern.
seo-title: Unterstützung von Technologien
solution: Experience Manager
title: Unterstützung von Technologien
topic: Dynamic media
uuid: 0abed8d4-9754-47b1-9de7-cce665de03b4
translation-type: tm+mt
source-git-commit: 7bc7b3a86fbcdc57cfdc31745fae3afc06e44b15
workflow-type: tm+mt
source-wordcount: '274'
ht-degree: 0%

---


# Unterstützung durch unterstützende Technologien{#assistive-technology-support}

Alle Viewer-Komponenten unterstützen ARIA-Rollen und -Attribute (Accessible Rich Internet Applications), um die Integration mit Hilfstechnologien wie Bildschirmlesehilfen zu verbessern.

Für das Viewer-Element der obersten Ebene sind die Attribute `region` und `aria-label` standardmäßig auf den Namen des Viewers eingestellt. Sie können die Bezeichnung mit dem Symbol für die lokale Anpassung `Container.LABEL` steuern.

Schaltflächen haben die Rolle `button` und einen beschreibenden Text mit dem Attribut `aria-label`. Der Wert des Attributs `aria-label` wird aus dem Wert des Schaltflächensymbols für die lokale Anpassung gefüllt. Wenn eine Schaltfläche deaktiviert ist, wird das Attribut `aria-disabled` entsprechend eingestellt.

Slider-Komponenten haben die Rolle `slider` mit den Attributen `aria-valuenow`, `aria-valuemin` und `aria-valuemax`, um die aktuelle Reglerposition zu beschreiben.

Miniaturen haben die Rolle `dialog` mit dem Attribut `aria-label`, das durch das Symbol `ThumbnailGridView.LABEL` der lokale Anpassung gesteuert wird. Einzelne Miniaturansichten haben die Rolle `button`. Wenn eine Miniaturansicht ausgewählt ist, wird das Attribut `aria-selected` auf `true` gesetzt.

Komponenten, die Muster anzeigen, haben die lokale Anpassung `listbox`, wobei das Attribut `aria-label` auf den Wert des Symbols `LABEL` dieser Komponente eingestellt ist. Einzelne Muster haben die Rolle `option` mit den Attributen `aria-setsize` und `aria-posinset`, um die Musterposition im Satz zu beschreiben. Wenn ein Farbfeld ausgewählt ist, wird das `aria-selected`-Attribut auf `true` gesetzt.

Dropdown-Listen werden durch Schaltflächen aktiviert, wobei das zusätzliche `aria-haspopup`-Attribut auf `true` und das `aria-controls`-Attribut gesetzt ist und auf das tatsächliche Dropdown-Bedienfeldelement verweist. Das Dropdown-Bedienfeld selbst hat die Rolle `menu` mit Unterelementen mit der Rolle `menuitem`. Für jedes Menüelement wird das Attribut `aria-label` angegeben.

Modale Dialogfelder haben die Rolle `dialog`. Das Header-Element des Dialogfelds wird durch das `aria-labelledby`-Attribut referenziert.
