---
description: Alle Viewer-Komponenten unterstützen ARIA-Rollen und -Attribute (Accessible Rich Internet Applications), um die Integration mit Hilfstechnologien wie Bildschirmlesehilfen zu verbessern.
solution: Experience Manager
title: Unterstützung von Technologien
feature: Dynamic Media Classic,Viewers,SDK/API,Mix Media Sets,Accessibility
role: Developer,Business Practitioner
translation-type: tm+mt
source-git-commit: f6c97606d7a4209427316d7367013ad9585a5cae
workflow-type: tm+mt
source-wordcount: '252'
ht-degree: 0%

---


# Unterstützung durch unterstützende Technologien{#assistive-technology-support}

Alle Viewer-Komponenten unterstützen ARIA-Rollen und -Attribute (Accessible Rich Internet Applications), um die Integration mit Hilfstechnologien wie Bildschirmlesehilfen zu verbessern.

Für das Viewer-Element der obersten Ebene sind die Attribute `region` und `aria-label` standardmäßig auf den Namen des Viewers eingestellt. Sie können die Bezeichnung mit dem Symbol für die lokale Anpassung `Container.LABEL` steuern.

Schaltflächen haben die Rolle `button` und einen beschreibenden Text mit dem Attribut `aria-label`. Der Wert des Attributs `aria-label` wird aus dem Wert des Schaltflächensymbols für die lokale Anpassung gefüllt. Wenn eine Schaltfläche deaktiviert ist, wird das Attribut `aria-disabled` entsprechend eingestellt.

Die Hauptrolle der Ansicht ist `application`. Eine Kurzbeschreibung der Hauptkomponente finden Sie unter `aria-roledescription`, wobei der Ansicht durch das Symbol `ROLE_DESCRIPTION` der lokale Anpassung der entsprechenden Hauptkomponente der Ansicht definiert wird. Navigationshinweise für Tastaturbenutzer werden mit `aria-describedby` bereitgestellt. Der Text für den Verwendungshinweis stammt aus dem Symbol `USAGE_HINT` lokale Anpassung. Wenn für ein Asset im Feld UserData eine Beschriftung definiert ist, wird das Attribut `aria-label` mit dem Wert dieser Beschriftung festgelegt.

Komponenten, die Muster anzeigen, haben die lokale Anpassung `listbox`, wobei das Attribut `aria-label` auf den Wert des Symbols `LABEL` dieser Komponente eingestellt ist. Einzelne Muster haben die Rolle `option` mit den Attributen `aria-setsize` und `aria-posinset`, um die Musterposition im Satz zu beschreiben. Wenn ein Farbfeld ausgewählt ist, wird das `aria-selected`-Attribut auf `true` gesetzt.

Slider-Komponenten haben die Rolle `slider` mit den Attributen `aria-valuenow`, `aria-valuemin` und `aria-valuemax`, um die aktuelle Reglerposition zu beschreiben.
