---
title: Unterstützung bei der Technologie
description: Alle Viewer-Komponenten unterstützen ARIA (Accessible Rich Internet Applications)-Rollen und -Attribute, um die Integration mit Hilfstechnologien wie Bildschirmlesehilfen zu verbessern.
solution: Experience Manager
feature: Dynamic Media Classic,Viewers,SDK/API,eCatalog,Accessibility
role: Developer,User
exl-id: 46ccea4e-4314-453e-a987-68644467ab12
source-git-commit: a919130f0940d81a221b79563b6b3e41533ba788
workflow-type: tm+mt
source-wordcount: '365'
ht-degree: 0%

---

# Unterstützung bei der Technologie{#assistive-technology-support}

Alle Viewer-Komponenten unterstützen ARIA (Accessible Rich Internet Applications)-Rollen und -Attribute, um die Integration mit Hilfstechnologien wie Bildschirmlesehilfen zu verbessern.

Das Viewer-Element der obersten Ebene hat die Rolle `region` und das Attribut `aria-label`, die standardmäßig auf den Namen des Viewers festgelegt sind. Sie können die Bezeichnung mit dem Lokalisierungssymbol `Container.LABEL` steuern.

Schaltflächen haben die Rolle &quot;`button`&quot; und beschreibender Text wird mit dem Attribut &quot;`aria-label`&quot; festgelegt. Der Wert des Attributs `aria-label` wird aus dem Wert des Lokalisierungssymbols der Schaltfläche abgeleitet. Wenn eine Schaltfläche deaktiviert ist, wird das Attribut `aria-disabled` entsprechend eingestellt.

Die Hauptansicht hat die Rolle &quot;`application`&quot;. Eine kurze Beschreibung der Hauptansicht wird in `aria-roledescription` bereitgestellt, wobei der Wert durch das Lokalisierungssymbol `ROLE_DESCRIPTION` der entsprechenden Hauptansichtskomponente definiert wird. Navigationshinweise für Tastaturbenutzer werden mit `aria-describedby` bereitgestellt, der Text für den Nutzungshinweis stammt aus dem Lokalisierungssymbol `USAGE_HINT`. Wenn für ein Asset eine Beschriftung im Feld UserData definiert ist, wird das Attribut `aria-label` mit dem Wert dieser Beschriftung festgelegt.

Hotspots, Regionen und Imagemaps haben die Rolle &quot;`button`&quot;und beschreibenden Text mit dem Attribut &quot;`aria-label`&quot;, wobei der Wert der Hotspot- oder Imagemap-Beschriftung angegeben ist. Wenn der Benutzer den Fokus auf Hotspots oder Imagemaps legt, werden Navigationshinweise für Tastaturbenutzer mit `aria-describedby` bereitgestellt, wobei der Text für den Nutzungshinweis aus dem Lokalisierungssymbol `USAGE_HINT` stammt.

Miniaturansichten haben die Rolle &quot;`dialog`&quot;, wobei das Attribut &quot;`aria-label`&quot; durch das Lokalisierungssymbol &quot;`ThumbnailGridView.LABEL`&quot; gesteuert wird. Einzelne Miniaturansichten haben die Rolle &quot;`button`&quot;. Wenn eine Miniaturansicht ausgewählt ist, wird das Attribut `aria-selected` auf `true` gesetzt.

Komponenten, die Muster anzeigen, haben die Rolle &quot;`listbox`&quot;, wobei das Attribut &quot;`aria-label`&quot; auf den Wert des Lokalisierungssymbols `LABEL` dieser Komponente gesetzt ist. Einzelne Muster haben die Rolle `option` mit den Attributen `aria-setsize` und `aria-posinset` , um die Musterposition im Satz zu beschreiben. Wenn ein Muster ausgewählt ist, erhält es das `aria-selected` -Attribut, das auf `true` gesetzt ist.

Dropdown-Listen werden durch Schaltflächen aktiviert, wobei das zusätzliche Attribut `aria-haspopup` auf `true` und das Attribut `aria-controls` auf das tatsächliche Dropdown-Bedienfeldelement verweisen. Das Dropdown-Bedienfeld selbst hat die Rolle `menu` mit Unterelementen mit der Rolle `menuitem`. Für jedes Menüelement ist das Attribut `aria-label` angegeben.

Modale Dialogfelder haben die Rolle &quot;`dialog`&quot;. Das Kopfzeilenelement des Dialogfelds wird durch das Attribut `aria-labelledby` referenziert.
