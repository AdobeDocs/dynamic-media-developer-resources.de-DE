---
title: Unterstützung der Hilfstechnologien
description: Alle Viewer-Komponenten unterstützen ARIA-Rollen und -Attribute (Accessible Rich Internet Applications), um die Integration mit Hilfstechnologien wie der Sprachausgabe zu verbessern.
solution: Experience Manager
feature: Dynamic Media Classic,Viewers,SDK/API,360 VR Video,Accessibility
role: Developer,User
exl-id: 0d6bc444-a4c2-47e4-b408-a6df85ebff72
source-git-commit: 67e12fae514341137e4218ea950f34da0d9997f3
workflow-type: tm+mt
source-wordcount: '177'
ht-degree: 0%

---

# Unterstützung der Hilfstechnologien{#assistive-technology-support}

Alle Viewer-Komponenten unterstützen ARIA-Rollen und -Attribute (Accessible Rich Internet Applications), um die Integration mit Hilfstechnologien wie der Sprachausgabe zu verbessern.

Für das Viewer-Element der obersten Ebene sind Rolle `region` und `aria-label` Attribut standardmäßig auf den Namen des Viewers festgelegt. Sie können die Beschriftung mit dem `Container.LABEL` Lokalisierungssymbol steuern.

Für Schaltflächen sind der `button` und der beschreibende Text mit dem Attribut `aria-label` festgelegt. Der Wert `aria-label` Attributs wird aus dem Wert des Lokalisierungssymbols der Schaltfläche gefüllt. Wenn eine Schaltfläche deaktiviert ist, wird `aria-disabled` Attribut entsprechend festgelegt.

Schieberkomponenten haben die Rolle `slider` mit den Attributen `aria-valuenow`, `aria-valuemin` und `aria-valuemax`, um die aktuelle Schieberposition zu beschreiben.

Dropdown-Listen werden durch Schaltflächen aktiviert, wobei das zusätzliche `aria-haspopup`-Attribut auf `true` festgelegt ist und `aria-controls` Attribut auf das tatsächliche Dropdown-Bedienfeldelement verweist. Das Dropdown-Bedienfeld selbst hat die Rolle `menu` mit Unterelementen mit der Rolle `menuitem`. Für jedes Menüelement ist das `aria-label` Attribut angegeben.

Modale Dialogfelder haben die Rolle `dialog`. Das Kopfzeilenelement des Dialogfelds wird durch das Attribut `aria-labelledby` referenziert.
