---
description: Alle Viewer-Komponenten unterstützen ARIA-Rollen und -Attribute (Accessible Rich Internet Applications), um die Integration mit Hilfstechnologien wie Bildschirmlesehilfen zu verbessern.
seo-description: Alle Viewer-Komponenten unterstützen ARIA-Rollen und -Attribute (Accessible Rich Internet Applications), um die Integration mit Hilfstechnologien wie Bildschirmlesehilfen zu verbessern.
seo-title: Unterstützung von Technologien
solution: Experience Manager
title: Unterstützung von Technologien
topic: Dynamic media
uuid: 72b414f4-b647-4afa-a409-a8ba90227d3f
translation-type: tm+mt
source-git-commit: 7bc7b3a86fbcdc57cfdc31745fae3afc06e44b15
workflow-type: tm+mt
source-wordcount: '292'
ht-degree: 0%

---


# Unterstützung durch unterstützende Technologien{#assistive-technology-support}

Alle Viewer-Komponenten unterstützen ARIA-Rollen und -Attribute (Accessible Rich Internet Applications), um die Integration mit Hilfstechnologien wie Bildschirmlesehilfen zu verbessern.

Für das Viewer-Element der obersten Ebene sind die Attribute `region` und `aria-label` standardmäßig auf den Namen des Viewers eingestellt. Sie können die Bezeichnung mit dem Symbol für die lokale Anpassung `Container.LABEL` steuern.

Schaltflächen haben die Rolle `button` und einen beschreibenden Text mit dem Attribut `aria-label`. Der Wert des Attributs `aria-label` wird aus dem Wert des Schaltflächensymbols für die lokale Anpassung gefüllt. Wenn eine Schaltfläche deaktiviert ist, wird das Attribut `aria-disabled` entsprechend eingestellt.

Schaltflächen, mit denen Sie durch Karussellfolien navigieren können, haben Beschriftungen, die in der Laufzeit aktualisiert werden, je nach der aktuell ausgewählten Folie. Die Vorlage für die Beschriftung dieser Schaltfläche wird mit dem Symbol für die lokale Anpassung `CAROUSELVIEWER_TOOLTIP_GOTO` festgelegt.

Die Hauptrolle der Ansicht ist `application`. Eine Kurzbeschreibung der Hauptkomponente finden Sie unter `aria-roledescription`, wobei der Ansicht durch das Symbol `ROLE_DESCRIPTION` der lokale Anpassung der entsprechenden Hauptkomponente der Ansicht definiert wird. Navigationshinweise für Tastaturbenutzer werden mit `aria-describedby` bereitgestellt. Der Text für den Verwendungshinweis stammt aus dem Symbol `USAGE_HINT` lokale Anpassung. Wenn für ein Asset im Feld UserData eine Beschriftung definiert ist, wird das Attribut `aria-label` mit dem Wert dieser Beschriftung festgelegt.

Hotspots, Regionen und Imagemaps haben die Rolle `button` und beschreibender Text mit dem Attribut `aria-label`, mit dem Wert der Hotspot- oder Imagemap-Beschriftung. Wenn der Benutzer den Fokus auf Hotspots oder Imagemaps legt, werden mit `aria-describedby` Navigationshinweise für Tastaturbenutzer bereitgestellt, wobei der Text für den Gebrauchshinweis aus dem Symbol `USAGE_HINT` der lokale Anpassung stammt.
