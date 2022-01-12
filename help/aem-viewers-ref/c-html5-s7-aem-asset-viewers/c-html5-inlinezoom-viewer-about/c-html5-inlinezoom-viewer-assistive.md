---
title: Unterstützung der Technologie
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

# Unterstützung der Technologie{#assistive-technology-support}

Alle Viewer-Komponenten unterstützen ARIA (Accessible Rich Internet Applications)-Rollen und -Attribute, um die Integration mit Hilfstechnologien wie Bildschirmlesehilfen zu verbessern.

Das Viewer-Element der obersten Ebene hat eine Rolle `region` und `aria-label` -Attribut, das standardmäßig auf den Namen des Viewers gesetzt ist. Sie können den Titel mit der `Container.LABEL` Lokalisierungssymbol.

Die Hauptansicht hat eine Rolle `application`. Eine kurze Beschreibung der Hauptansicht finden Sie unter `aria-roledescription`, wobei der durch die Variable `ROLE_DESCRIPTION` Lokalisierungssymbol der entsprechenden Hauptansichtskomponente. Navigationshinweise für Tastaturbenutzer werden über `aria-describedby`, kommt der Text für den Nutzungshinweis aus dem `USAGE_HINT` Lokalisierungssymbol. Wenn für ein Asset eine Beschriftung im Feld UserData definiert ist, wird die `aria-label` -Attribut mit dem Wert dieser Beschriftung festgelegt ist.

Komponenten, die Muster anzeigen, haben die Rolle `listbox` mit `aria-label` -Attribut auf den Wert der `LABEL` Lokalisierungssymbol dieser Komponente. Einzelne Muster haben die Rolle `option` mit `aria-setsize` und `aria-posinset` -Attribute, um die Musterposition im Satz zu beschreiben. Wenn ein Muster ausgewählt ist, erhält es die `aria-selected` -Attribut auf `true`.
