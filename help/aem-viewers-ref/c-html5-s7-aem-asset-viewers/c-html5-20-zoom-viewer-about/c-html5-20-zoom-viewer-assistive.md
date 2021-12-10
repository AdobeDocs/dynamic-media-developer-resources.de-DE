---
title: Unterstützung der Technologie
description: Alle Viewer-Komponenten unterstützen ARIA (Accessible Rich Internet Applications)-Rollen und -Attribute, um die Integration mit Hilfstechnologien wie Bildschirmlesehilfen zu verbessern.
solution: Experience Manager
feature: Dynamic Media Classic,Viewers,SDK/API,Zoom,Accessibility
role: Developer,User
exl-id: ef2cf58a-bdf0-4136-8d91-692c899cfef7
source-git-commit: ec2a15e2e76bae5da4fbabc9b6912b12dc080f66
workflow-type: tm+mt
source-wordcount: '225'
ht-degree: 0%

---

# Unterstützung der Technologie{#assistive-technology-support}

Alle Viewer-Komponenten unterstützen ARIA (Accessible Rich Internet Applications)-Rollen und -Attribute, um die Integration mit Hilfstechnologien wie Bildschirmlesehilfen zu verbessern.

Das Viewer-Element der obersten Ebene hat eine Rolle `region` und `aria-label` -Attribut, das standardmäßig auf den Namen des Viewers gesetzt ist. Sie können den Titel mit der `Container.LABEL` Lokalisierungssymbol.

Schaltflächen haben die Rolle `button` und beschreibender Text mit `aria-label` -Attribut. Der Wert von `aria-label` -Attribut wird aus dem Wert des Lokalisierungssymbols der Schaltfläche gefüllt. Wenn eine Schaltfläche deaktiviert ist, `aria-disabled` -Attribut entsprechend festgelegt ist.

Die Hauptansicht hat eine Rolle `application`. Eine kurze Beschreibung der Hauptansicht finden Sie unter `aria-roledescription`, wobei der durch die Variable `ROLE_DESCRIPTION` Lokalisierungssymbol der entsprechenden Hauptansichtskomponente. Navigationshinweise für Tastaturbenutzer werden über `aria-describedby`, kommt der Text für den Nutzungshinweis aus dem `USAGE_HINT` Lokalisierungssymbol. Wenn für ein Asset eine Beschriftung im Feld UserData definiert ist, wird die `aria-label` -Attribut mit dem Wert dieser Beschriftung festgelegt ist.

Komponenten, die Muster anzeigen, haben die Rolle `listbox` mit `aria-label` -Attribut auf den Wert der `LABEL` Lokalisierungssymbol dieser Komponente. Einzelne Muster haben die Rolle `option` mit `aria-setsize` und `aria-posinset` -Attribute, um die Musterposition im Satz zu beschreiben. Wenn ein Muster ausgewählt ist, erhält es die `aria-selected` -Attribut auf `true`.
