---
title: Unterstützung bei der Technologie
description: Alle Viewer-Komponenten unterstützen ARIA (Accessible Rich Internet Applications)-Rollen und -Attribute, um die Integration mit Hilfstechnologien wie Bildschirmlesehilfen zu verbessern.
solution: Experience Manager
feature: Dynamic Media Classic,Viewers,SDK/API,Carousel Banners,Accessibility
role: Developer,User
exl-id: 3ed943e8-4695-4561-9be0-1b6ed30294f8
source-git-commit: 4aaa77b1fb58b30b02ee15f6080169fa354d5907
workflow-type: tm+mt
source-wordcount: '267'
ht-degree: 0%

---

# Unterstützung bei der Technologie{#assistive-technology-support}

Alle Viewer-Komponenten unterstützen ARIA (Accessible Rich Internet Applications)-Rollen und -Attribute, um die Integration mit Hilfstechnologien wie Bildschirmlesehilfen zu verbessern.

Das Viewer-Element der obersten Ebene hat die Rolle `region` und das Attribut `aria-label`, die standardmäßig auf den Namen des Viewers festgelegt sind. Sie können die Bezeichnung mit dem Lokalisierungssymbol `Container.LABEL` steuern.

Schaltflächen haben die Rolle &quot;`button`&quot; und beschreibender Text wird mit dem Attribut &quot;`aria-label`&quot; festgelegt. Der Wert des Attributs `aria-label` wird aus dem Wert des Lokalisierungssymbols der Schaltfläche abgeleitet. Wenn eine Schaltfläche deaktiviert ist, wird das Attribut `aria-disabled` entsprechend eingestellt.

Schaltflächen, mit denen Sie durch Karussellfolien navigieren können, verfügen über Beschriftungen, die zur Laufzeit entsprechend der aktuell ausgewählten Folie aktualisiert werden. Die Vorlage für diese Schaltflächenbeschriftung wird mit dem Lokalisierungssymbol `CAROUSELVIEWER_TOOLTIP_GOTO` festgelegt.

Die Hauptansicht hat die Rolle &quot;`application`&quot;. Eine kurze Beschreibung der Hauptansicht wird in `aria-roledescription` bereitgestellt, wobei der Wert durch das Lokalisierungssymbol `ROLE_DESCRIPTION` der entsprechenden Hauptansichtskomponente definiert wird. Navigationshinweise für Tastaturbenutzer werden mit `aria-describedby` bereitgestellt, der Text für den Nutzungshinweis stammt aus dem Lokalisierungssymbol `USAGE_HINT`. Wenn für ein Asset eine Beschriftung im Feld UserData definiert ist, wird das Attribut `aria-label` mit dem Wert dieser Beschriftung festgelegt.

Hotspots, Regionen und Imagemaps haben die Rolle &quot;`button`&quot;und beschreibenden Text mit dem Attribut &quot;`aria-label`&quot;, wobei der Wert der Hotspot- oder Imagemap-Beschriftung angegeben ist. Wenn der Benutzer den Fokus auf Hotspots oder Imagemaps legt, werden Navigationshinweise für Tastaturbenutzer mit `aria-describedby` bereitgestellt, wobei der Text für den Nutzungshinweis aus dem Lokalisierungssymbol `USAGE_HINT` stammt.
