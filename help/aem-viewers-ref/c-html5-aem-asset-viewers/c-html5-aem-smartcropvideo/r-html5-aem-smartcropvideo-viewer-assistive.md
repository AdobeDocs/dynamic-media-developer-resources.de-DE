---
title: Unterstützung bei der Technologie
description: Alle Viewer-Komponenten unterstützen ARIA (Accessible Rich Internet Applications)-Rollen und -Attribute, um die Integration mit Hilfstechnologien wie Bildschirmlesehilfen zu verbessern.
solution: Experience Manager
feature: Dynamic Media Classic,Viewers,SDK/API,Smart Crop,Video,Accessibility
role: Developer,User
exl-id: b2bfd93b-707e-4a03-a14e-14ec23328fdd
source-git-commit: 1aa8be858b0ba8ec9b99753d43c202b35ed58c30
workflow-type: tm+mt
source-wordcount: '177'
ht-degree: 0%

---

# Unterstützung bei der Technologie{#assistive-technology-support}

Alle Viewer-Komponenten unterstützen ARIA (Accessible Rich Internet Applications)-Rollen und -Attribute, um die Integration mit Hilfstechnologien wie Bildschirmlesehilfen zu verbessern.

Das Viewer-Element der obersten Ebene hat die Rolle `region` und das Attribut `aria-label`, die standardmäßig auf den Namen des Viewers festgelegt sind. Sie können die Bezeichnung mit dem Lokalisierungssymbol `Container.LABEL` steuern.

Schaltflächen haben die Rolle &quot;`button`&quot; und beschreibender Text wird mit dem Attribut &quot;`aria-label`&quot; festgelegt. Der Wert des Attributs `aria-label` wird aus dem Wert des Lokalisierungssymbols der Schaltfläche abgeleitet. Wenn eine Schaltfläche deaktiviert ist, wird das Attribut `aria-disabled` entsprechend eingestellt.

Reglerkomponenten haben die Rolle `slider` mit den Attributen `aria-valuenow`, `aria-valuemin` und `aria-valuemax`, um die aktuelle Reglerposition zu beschreiben.

Dropdown-Listen werden durch Schaltflächen aktiviert, wobei das zusätzliche Attribut `aria-haspopup` auf das Attribut `true` und das Attribut `aria-controls` eingestellt ist, die auf das tatsächliche Dropdown-Bedienfeldelement verweisen. Das Dropdown-Bedienfeld selbst hat die Rolle `menu` mit Unterelementen mit der Rolle `menuitem`. Für jedes Menüelement ist das Attribut `aria-label` angegeben.

Modale Dialogfelder haben die Rolle &quot;`dialog`&quot;. Das Kopfzeilenelement des Dialogfelds wird durch das Attribut `aria-labelledby` referenziert.
