---
description: Alle Viewer-Komponenten unterstützen ARIA (Accessible Rich Internet Applications)-Rollen und -Attribute, um die Integration mit Hilfstechnologien wie Bildschirmlesehilfen zu verbessern.
solution: Experience Manager
title: Unterstützung der Technologie
feature: Dynamic Media Classic,Viewer,SDK/API,360 VR Video,Barrierefreiheit
role: Developer,User
exl-id: 0d6bc444-a4c2-47e4-b408-a6df85ebff72
source-git-commit: 206e4643e3926cb85b4be2189743578f88180be7
workflow-type: tm+mt
source-wordcount: '186'
ht-degree: 0%

---

# Unterstützung der Technologie{#assistive-technology-support}

Alle Viewer-Komponenten unterstützen ARIA (Accessible Rich Internet Applications)-Rollen und -Attribute, um die Integration mit Hilfstechnologien wie Bildschirmlesehilfen zu verbessern.

Das Viewer-Element der obersten Ebene hat die Rolle `region` und das Attribut `aria-label`, die standardmäßig auf den Namen des Viewers festgelegt sind. Sie können den Titel mit dem Lokalisierungssymbol `Container.LABEL` steuern.

Schaltflächen haben die Rolle `button` und einen beschreibenden Text mit dem Attribut `aria-label`. Der Wert des Attributs `aria-label` wird aus dem Wert des Lokalisierungssymbols der Schaltfläche abgeleitet. Wenn eine Schaltfläche deaktiviert ist, wird das Attribut `aria-disabled` entsprechend eingestellt.

Reglerkomponenten haben die Rolle `slider` mit den Attributen `aria-valuenow`, `aria-valuemin` und `aria-valuemax`, um die aktuelle Reglerposition zu beschreiben.

Dropdown-Listen werden durch Schaltflächen aktiviert, wobei das zusätzliche Attribut `aria-haspopup` auf `true` und das Attribut `aria-controls` gesetzt sind, die auf das tatsächliche Dropdown-Bedienfeldelement verweisen. Das Dropdown-Bedienfeld selbst hat die Rolle `menu` mit Unterelementen mit der Rolle `menuitem`. Für jedes Menüelement ist das Attribut `aria-label` angegeben.

Modale Dialogfelder haben die Rolle `dialog`. Das Header-Element des Dialogfelds wird durch das Attribut `aria-labelledby` referenziert.
