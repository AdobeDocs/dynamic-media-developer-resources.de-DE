---
title: Unterstützung bei der Technologie
description: Alle Viewer-Komponenten unterstützen ARIA (Accessible Rich Internet Applications)-Rollen und -Attribute, um die Integration mit Hilfstechnologien wie Bildschirmlesehilfen zu verbessern.
solution: Experience Manager
feature: Dynamic Media Classic,Viewers,SDK/API,Inline Zoom,Accessibility
role: Developer,User
exl-id: 8aa88456-b78b-434b-a98f-effce83ccd21
source-git-commit: 50dddf148345d2ca5243d5d7108fefa56d23dad6
workflow-type: tm+mt
source-wordcount: '192'
ht-degree: 0%

---

# Unterstützung bei der Technologie{#assistive-technology-support}

Alle Viewer-Komponenten unterstützen ARIA (Accessible Rich Internet Applications)-Rollen und -Attribute, um die Integration mit Hilfstechnologien wie Bildschirmlesehilfen zu verbessern.

Das Viewer-Element der obersten Ebene hat die Rolle `region` und das Attribut `aria-label`, die standardmäßig auf den Namen des Viewers festgelegt sind. Sie können die Bezeichnung mit dem Lokalisierungssymbol `Container.LABEL` steuern.

Die Hauptansicht hat die Rolle &quot;`application`&quot;. Eine kurze Beschreibung der Hauptansicht wird in `aria-roledescription` bereitgestellt, wobei der Wert durch das Lokalisierungssymbol `ROLE_DESCRIPTION` der entsprechenden Hauptansichtskomponente definiert wird. Navigationshinweise für Tastaturbenutzer werden mit `aria-describedby` bereitgestellt, der Text für den Nutzungshinweis stammt aus dem Lokalisierungssymbol `USAGE_HINT`. Wenn für ein Asset eine Beschriftung im Feld UserData definiert ist, wird das Attribut `aria-label` mit dem Wert dieser Beschriftung festgelegt.

Komponenten, die Muster anzeigen, haben die Rolle &quot;`listbox`&quot;, wobei das Attribut &quot;`aria-label`&quot; auf den Wert des Lokalisierungssymbols `LABEL` dieser Komponente gesetzt ist. Einzelne Muster haben die Rolle `option` mit den Attributen `aria-setsize` und `aria-posinset` , um die Musterposition im Satz zu beschreiben. Wenn ein Muster ausgewählt ist, erhält es das `aria-selected` -Attribut, das auf `true` gesetzt ist.
