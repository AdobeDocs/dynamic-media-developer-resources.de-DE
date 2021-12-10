---
title: Unterstützung der Technologie
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

# Unterstützung der Technologie{#assistive-technology-support}

Alle Viewer-Komponenten unterstützen ARIA (Accessible Rich Internet Applications)-Rollen und -Attribute, um die Integration mit Hilfstechnologien wie Bildschirmlesehilfen zu verbessern.

Das Viewer-Element der obersten Ebene hat eine Rolle `region` und `aria-label` -Attribut, das standardmäßig auf den Namen des Viewers gesetzt ist. Sie können den Titel mit der `Container.LABEL` Lokalisierungssymbol.

Schaltflächen haben die Rolle `button` und beschreibendem Text mit der `aria-label` -Attribut. Der Wert von `aria-label` -Attribut wird aus dem Wert des Lokalisierungssymbols der Schaltfläche gefüllt. Wenn eine Schaltfläche deaktiviert ist, wird die `aria-disabled` -Attribut entsprechend festgelegt ist.

Die Hauptansicht hat eine Rolle `application`. Eine kurze Beschreibung der Hauptansicht finden Sie unter `aria-roledescription`, wobei der durch die Variable `ROLE_DESCRIPTION` Lokalisierungssymbol der entsprechenden Hauptansichtskomponente. Navigationshinweise für Tastaturbenutzer werden über `aria-describedby`, kommt der Text für den Nutzungshinweis aus dem `USAGE_HINT` Lokalisierungssymbol. Wenn für ein Asset eine Beschriftung im Feld UserData definiert ist, wird die `aria-label` -Attribut mit dem Wert dieser Beschriftung festgelegt ist.

Hotspots, Regionen und Imagemaps haben die Rolle `button` und beschreibender Text mit `aria-label` -Attribut mit dem Wert der Hotspot- oder Imagemap-Beschriftung. Wenn der Benutzer den Fokus auf Hotspots oder Imagemaps legt, werden Navigationshinweise für Tastaturbenutzer mit `aria-describedby`, wobei der Text für den Nutzungshinweis aus dem `USAGE_HINT` Lokalisierungssymbol.

Miniaturen haben die Rolle `dialog` mit `aria-label` durch das `ThumbnailGridView.LABEL` Lokalisierungssymbol. Einzelne Miniaturen haben eine Rolle `button`. Wenn eine Miniaturansicht ausgewählt ist, wird sie `aria-selected` -Attribut auf `true`.

Komponenten, die Muster anzeigen, haben die Rolle `listbox` mit `aria-label` -Attribut auf den Wert der `LABEL` Lokalisierungssymbol dieser Komponente. Einzelne Muster haben die Rolle `option` mit `aria-setsize` und `aria-posinset` -Attribute, um die Musterposition im Satz zu beschreiben. Wenn ein Muster ausgewählt ist, erhält es die `aria-selected` -Attribut auf `true`.

Dropdown-Listen werden durch Schaltflächen mit zusätzlichen `aria-haspopup` -Attribut auf `true` und `aria-controls` -Attribut, das auf das tatsächliche Dropdown-Bedienfeldelement verweist. Das Dropdown-Bedienfeld selbst hat die Rolle `menu` mit Unterelementen mit Rolle `menuitem`. Jedes Menüelement verfügt über `aria-label` -Attribut angegeben.

Modale Dialogfelder haben die Rolle `dialog`. Das Kopfzeilenelement des Dialogfelds wird durch die `aria-labelledby` -Attribut.
