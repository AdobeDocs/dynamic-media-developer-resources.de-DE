---
title: Unterstützung der Technologie
description: Alle Viewer-Komponenten unterstützen ARIA (Accessible Rich Internet Applications)-Rollen und -Attribute, um die Integration mit Hilfstechnologien wie Bildschirmlesehilfen zu verbessern.
solution: Experience Manager
feature: Dynamic Media Classic,Viewers,SDK/API,Video,Accessibility
role: Developer,User
exl-id: e0652730-60ee-41db-890b-e223b279e47d
source-git-commit: 11acb9151d3ea247eecde3cfbbd295a95c10829c
workflow-type: tm+mt
source-wordcount: '177'
ht-degree: 0%

---

# Unterstützung der Technologie{#assistive-technology-support}

Alle Viewer-Komponenten unterstützen ARIA (Accessible Rich Internet Applications)-Rollen und -Attribute, um die Integration mit Hilfstechnologien wie Bildschirmlesehilfen zu verbessern.

Das Viewer-Element der obersten Ebene hat eine Rolle `region` und `aria-label` -Attribut, das standardmäßig auf den Namen des Viewers gesetzt ist. Sie können den Titel mit der `Container.LABEL` Lokalisierungssymbol.

Schaltflächen haben die Rolle `button` und beschreibender Text mit `aria-label` -Attribut. Der Wert von `aria-label` -Attribut wird aus dem Wert des Lokalisierungssymbols der Schaltfläche gefüllt. Wenn eine Schaltfläche deaktiviert ist, `aria-disabled` -Attribut entsprechend festgelegt ist.

Reglerkomponenten haben die Rolle `slider` mit Attributen `aria-valuenow`, `aria-valuemin`und `aria-valuemax` um die aktuelle Reglerposition zu beschreiben.

Dropdown-Listen werden durch Schaltflächen mit zusätzlichen `aria-haspopup` -Attribut auf `true` und `aria-controls` -Attribut, das auf das tatsächliche Dropdown-Bedienfeldelement verweist. Das Dropdown-Bedienfeld selbst hat die Rolle `menu` mit Unterelementen mit Rolle `menuitem`. Jedes Menüelement verfügt über `aria-label` -Attribut angegeben.

Modale Dialogfelder haben die Rolle `dialog`. Das Kopfzeilenelement des Dialogfelds wird durch die `aria-labelledby` -Attribut.
