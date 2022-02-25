---
title: Unterstützung der Technologie
description: Alle Viewer-Komponenten unterstützen ARIA (Accessible Rich Internet Applications)-Rollen und -Attribute, um die Integration mit Hilfstechnologien wie Bildschirmlesehilfen zu verbessern.
solution: Experience Manager
feature: Dynamic Media Classic,Viewers,SDK/API,Zoom,Accessibility
role: Developer,User
exl-id: f2f36520-f6dd-4baa-abf0-48a846882acb
source-git-commit: 7eddc50fb9803eacdd1f513c6132380793b6f88d
workflow-type: tm+mt
source-wordcount: '180'
ht-degree: 0%

---

# Unterstützung der Technologie{#assistive-technology-support}

Alle Viewer-Komponenten unterstützen ARIA (Accessible Rich Internet Applications)-Rollen und -Attribute, um die Integration mit Hilfstechnologien wie Bildschirmlesehilfen zu verbessern.

Das Viewer-Element der obersten Ebene hat eine Rolle `region` und `aria-label` -Attribut, das standardmäßig auf den Namen des Viewers gesetzt ist. Sie können den Titel mit der `Container.LABEL` Lokalisierungssymbol.

Schaltflächen haben die Rolle `button` und beschreibendem Text mit der `aria-label` -Attribut. Der Wert von `aria-label` -Attribut wird aus dem Wert des Lokalisierungssymbols der Schaltfläche gefüllt. Wenn eine Schaltfläche deaktiviert ist, wird die `aria-disabled` -Attribut entsprechend festgelegt ist.

Die Hauptansicht hat eine Rolle `application`. Eine kurze Beschreibung der Hauptansicht finden Sie unter `aria-roledescription`, wobei der durch die Variable `ROLE_DESCRIPTION` Lokalisierungssymbol der entsprechenden Hauptansichtskomponente. Navigationshinweise für Tastaturbenutzer werden über `aria-describedby`, kommt der Text für den Nutzungshinweis aus dem `USAGE_HINT` Lokalisierungssymbol. Wenn für ein Asset eine Beschriftung im Feld UserData definiert ist, wird die `aria-label` -Attribut mit dem Wert dieser Beschriftung festgelegt ist.
