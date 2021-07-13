---
description: Alle Viewer-Komponenten unterstützen ARIA (Accessible Rich Internet Applications)-Rollen und -Attribute, um die Integration mit Hilfstechnologien wie Bildschirmlesehilfen zu verbessern.
solution: Experience Manager
title: Unterstützung der Technologie
feature: Dynamic Media Classic,Viewers,SDK/API,eCatalog,Accessibility
role: Developer,User
exl-id: 46ccea4e-4314-453e-a987-68644467ab12
source-git-commit: 206e4643e3926cb85b4be2189743578f88180be7
workflow-type: tm+mt
source-wordcount: '373'
ht-degree: 0%

---

# Unterstützung der Technologie{#assistive-technology-support}

Alle Viewer-Komponenten unterstützen ARIA (Accessible Rich Internet Applications)-Rollen und -Attribute, um die Integration mit Hilfstechnologien wie Bildschirmlesehilfen zu verbessern.

Das Viewer-Element der obersten Ebene hat die Rolle `region` und das Attribut `aria-label`, die standardmäßig auf den Namen des Viewers festgelegt sind. Sie können den Titel mit dem Lokalisierungssymbol `Container.LABEL` steuern.

Schaltflächen haben die Rolle `button` und beschreibender Text mit dem Attribut `aria-label`. Der Wert des Attributs `aria-label` wird aus dem Wert des Lokalisierungssymbols der Schaltfläche abgeleitet. Wenn eine Schaltfläche deaktiviert ist, wird das Attribut `aria-disabled` entsprechend festgelegt.

Die Hauptansicht hat die Rolle `application`. Eine kurze Beschreibung der Hauptansicht finden Sie unter `aria-roledescription`, wobei der Wert durch das Lokalisierungssymbol `ROLE_DESCRIPTION` der entsprechenden Hauptansichtskomponente definiert wird. Navigationshinweise für Tastaturbenutzer werden mit `aria-describedby` bereitgestellt, der Text für den Nutzungshinweis stammt aus dem Lokalisierungssymbol `USAGE_HINT`. Wenn für ein Asset eine Beschriftung im Feld UserData definiert ist, wird das Attribut `aria-label` mit dem Wert dieser Beschriftung festgelegt.

Hotspots, Regionen und Imagemaps haben die Rolle `button` und beschreibenden Text mit dem Attribut `aria-label` mit dem Wert der Hotspot- oder Imagemap-Beschriftung. Wenn der Benutzer den Fokus auf Hotspots oder Imagemaps legt, werden Navigationshinweise für Tastaturbenutzer mit `aria-describedby` bereitgestellt, wobei der Text für den Nutzungshinweis aus dem Lokalisierungssymbol `USAGE_HINT` stammt.

Miniaturansichten haben die Rolle `dialog` mit dem Attribut `aria-label` , das durch das Lokalisierungssymbol `ThumbnailGridView.LABEL` gesteuert wird. Einzelne Miniaturansichten haben die Rolle `button`. Wenn eine Miniaturansicht ausgewählt ist, wird das Attribut `aria-selected` auf `true` gesetzt.

Komponenten, die Muster anzeigen, haben die Rolle `listbox` , wobei das Attribut `aria-label` auf den Wert des Lokalisierungssymbols `LABEL` dieser Komponente gesetzt ist. Einzelne Muster haben die Rolle `option` mit den Attributen `aria-setsize` und `aria-posinset` , um die Musterposition im Satz zu beschreiben. Wenn ein Muster ausgewählt ist, wird das `aria-selected` -Attribut auf `true` gesetzt.

Dropdown-Listen werden durch Schaltflächen aktiviert, wobei das zusätzliche Attribut `aria-haspopup` auf `true` und das Attribut `aria-controls` auf das tatsächliche Dropdown-Bedienfeldelement verweisen. Das Dropdown-Bedienfeld selbst hat die Rolle `menu` mit Unterelementen mit der Rolle `menuitem`. Für jedes Menüelement ist das Attribut `aria-label` angegeben.

Modale Dialogfelder haben die Rolle `dialog`. Das Header-Element des Dialogfelds wird durch das Attribut `aria-labelledby` referenziert.
