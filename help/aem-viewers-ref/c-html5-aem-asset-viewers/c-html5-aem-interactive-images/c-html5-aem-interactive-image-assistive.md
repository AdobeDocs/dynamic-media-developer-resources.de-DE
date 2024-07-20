---
title: Unterstützung bei der Technologie
description: Alle Viewer-Komponenten unterstützen ARIA (Accessible Rich Internet Applications)-Rollen und -Attribute, um die Integration mit Hilfstechnologien wie Bildschirmlesehilfen zu verbessern.
solution: Experience Manager
feature: Dynamic Media Classic,Viewers,SDK/API,Interactive Images,Accessibility
role: Developer,User
exl-id: 39e64f35-543f-4977-a97a-0daa93786ff3
source-git-commit: 24667a5ebab54ba22c4a3f6b52d19d7a31a93576
workflow-type: tm+mt
source-wordcount: '203'
ht-degree: 0%

---

# Unterstützung bei der Technologie{#assistive-technology-support}

Alle Viewer-Komponenten unterstützen ARIA (Accessible Rich Internet Applications)-Rollen und -Attribute, um die Integration mit Hilfstechnologien wie Bildschirmlesehilfen zu verbessern.

Das Viewer-Element der obersten Ebene hat die Rolle `region` und das Attribut `aria-label`, die standardmäßig auf den Namen des Viewers festgelegt sind. Sie können die Bezeichnung mit dem Lokalisierungssymbol `Container.LABEL` steuern.

Die Hauptansicht hat die Rolle &quot;`application`&quot;. Eine kurze Beschreibung der Hauptansicht wird in `aria-roledescription` bereitgestellt, wobei der Wert durch das Lokalisierungssymbol `ROLE_DESCRIPTION` der entsprechenden Hauptansichtskomponente definiert wird. Navigationshinweise für Tastaturbenutzer werden mit `aria-describedby` bereitgestellt, der Text für den Nutzungshinweis stammt aus dem Lokalisierungssymbol `USAGE_HINT`. Wenn für ein Asset eine Beschriftung im Feld UserData definiert ist, wird das Attribut `aria-label` mit dem Wert dieser Beschriftung festgelegt.

Hotspots, Regionen und Imagemaps haben die Rolle &quot;`button`&quot;und beschreibenden Text mit dem Attribut &quot;`aria-label`&quot;, wobei der Wert der Hotspot- oder Imagemap-Beschriftung angegeben ist. Wenn der Benutzer den Fokus auf Hotspots oder Imagemaps legt, werden Navigationshinweise für Tastaturbenutzer mit `aria-describedby` bereitgestellt, wobei der Text für den Nutzungshinweis aus dem Lokalisierungssymbol `USAGE_HINT` stammt.
