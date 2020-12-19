---
description: Alle Viewer-Komponenten unterstützen ARIA-Rollen und -Attribute (Accessible Rich Internet Applications), um die Integration mit Hilfstechnologien wie Bildschirmlesehilfen zu verbessern.
seo-description: Alle Viewer-Komponenten unterstützen ARIA-Rollen und -Attribute (Accessible Rich Internet Applications), um die Integration mit Hilfstechnologien wie Bildschirmlesehilfen zu verbessern.
seo-title: Unterstützung von Technologien
solution: Experience Manager
title: Unterstützung von Technologien
topic: Dynamic media
uuid: 99fdb4fd-5a3d-4c4e-b1c5-10651c08bf39
translation-type: tm+mt
source-git-commit: 7bc7b3a86fbcdc57cfdc31745fae3afc06e44b15
workflow-type: tm+mt
source-wordcount: '205'
ht-degree: 0%

---


# Unterstützung durch unterstützende Technologien{#assistive-technology-support}

Alle Viewer-Komponenten unterstützen ARIA-Rollen und -Attribute (Accessible Rich Internet Applications), um die Integration mit Hilfstechnologien wie Bildschirmlesehilfen zu verbessern.

Für das Viewer-Element der obersten Ebene sind die Attribute `region` und `aria-label` standardmäßig auf den Namen des Viewers eingestellt. Sie können die Bezeichnung mit dem Symbol für die lokale Anpassung `Container.LABEL` steuern.

Schaltflächen haben die Rolle `button` und beschreibenden Text mit dem Attribut `aria-label`. Der Wert des Attributs `aria-label` wird aus dem Wert des Schaltflächensymbols für die lokale Anpassung gefüllt. Wenn eine Schaltfläche deaktiviert ist, wird das `aria-disabled`-Attribut entsprechend eingestellt.

Die Hauptrolle der Ansicht ist `application`. Eine Kurzbeschreibung der Hauptkomponente finden Sie unter `aria-roledescription`, wobei der Ansicht durch das Symbol `ROLE_DESCRIPTION` der lokale Anpassung der entsprechenden Hauptkomponente der Ansicht definiert wird. Navigationshinweise für Tastaturbenutzer werden mit `aria-describedby` bereitgestellt. Der Text für den Verwendungshinweis stammt aus dem Symbol `USAGE_HINT` lokale Anpassung. Wenn für ein Asset im Feld UserData eine Beschriftung definiert ist, wird das Attribut `aria-label` mit dem Wert dieser Beschriftung festgelegt.
