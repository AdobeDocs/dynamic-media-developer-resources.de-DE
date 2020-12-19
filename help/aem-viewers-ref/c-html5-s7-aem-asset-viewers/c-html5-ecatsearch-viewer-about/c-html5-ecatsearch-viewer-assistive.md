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
workflow-type: tm+mt
source-wordcount: '418'
ht-degree: 0%

---


# Unterstützung durch unterstützende Technologien{#assistive-technology-support}

Alle Viewer-Komponenten unterstützen ARIA-Rollen und -Attribute (Accessible Rich Internet Applications), um die Integration mit Hilfstechnologien wie Bildschirmlesehilfen zu verbessern.

Für das Viewer-Element der obersten Ebene sind die Attribute `region` und `aria-label` standardmäßig auf den Namen des Viewers eingestellt. Sie können die Bezeichnung mit dem Symbol für die lokale Anpassung `Container.LABEL` steuern.

Schaltflächen haben die Rolle `button` und beschreibenden Text mit dem Attribut `aria-label`. Der Wert des Attributs `aria-label` wird aus dem Wert des Schaltflächensymbols für die lokale Anpassung gefüllt. Wenn eine Schaltfläche deaktiviert ist, wird das `aria-disabled`-Attribut entsprechend eingestellt.

Die Hauptrolle der Ansicht ist `application`. Eine Kurzbeschreibung der Hauptkomponente finden Sie unter `aria-roledescription`, wobei der Ansicht durch das Symbol `ROLE_DESCRIPTION` der lokale Anpassung der entsprechenden Hauptkomponente der Ansicht definiert wird. Navigationshinweise für Tastaturbenutzer werden mit `aria-describedby` bereitgestellt. Der Text für den Verwendungshinweis stammt aus dem Symbol `USAGE_HINT` lokale Anpassung. Wenn für ein Asset im Feld UserData eine Beschriftung definiert ist, wird das Attribut `aria-label` mit dem Wert dieser Beschriftung festgelegt.

Hotspots, Regionen und Imagemaps haben die Rolle `button` und beschreibender Text mit dem Attribut `aria-label`, mit dem Wert der Hotspot- oder Imagemap-Beschriftung. Wenn der Benutzer den Fokus auf Hotspots oder Imagemaps legt, werden mit `aria-describedby` Navigationshinweise für Tastaturbenutzer bereitgestellt, wobei der Text für den Gebrauchshinweis aus dem Symbol `USAGE_HINT` der lokale Anpassung stammt.

Miniaturen haben die Rolle `dialog` mit dem Attribut `aria-label`, das durch das Symbol `ThumbnailGridView.LABEL` der lokale Anpassung gesteuert wird. Einzelne Miniaturansichten haben die Rolle `button`. Wenn eine Miniaturansicht ausgewählt ist, wird das Attribut `aria-selected` auf `true` gesetzt.

Komponenten, die Muster anzeigen, haben die lokale Anpassung `listbox`, wobei das Attribut `aria-label` auf den Wert des Symbols `LABEL` dieser Komponente eingestellt ist. Einzelne Muster haben die Rolle `option` mit den Attributen `aria-setsize` und `aria-posinset`, um die Musterposition im Satz zu beschreiben. Wenn ein Farbfeld ausgewählt ist, wird das `aria-selected`-Attribut auf `true` gesetzt.

Dropdown-Listen werden durch Schaltflächen aktiviert, wobei das zusätzliche `aria-haspopup`-Attribut auf `true` und das `aria-controls`-Attribut auf das tatsächliche Dropdown-Bedienfeldelement verweisen. Das Dropdown-Bedienfeld selbst hat die Rolle `menu` mit Unterelementen mit der Rolle `menuitem`. Für jedes Menüelement wird das Attribut `aria-label` angegeben.

Die Suchbenutzeroberfläche ist im Element mit der Rolle `search` gruppiert. Das Sucheingabefeld hat die Rolle `searchbox` und verweist auf die informative Beschriftung, die von `SearchPanel.INFO_PROMPT`-lokale Anpassung-Symbol mit `aria-describedby`-Attribut gesteuert wird.

Modale Dialogfelder haben die Rolle `dialog`. Das Header-Element des Dialogfelds wird durch das `aria-labelledby`-Attribut referenziert.
