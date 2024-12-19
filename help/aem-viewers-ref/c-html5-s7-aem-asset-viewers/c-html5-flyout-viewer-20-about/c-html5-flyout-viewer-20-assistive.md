---
title: Unterstützung der Hilfstechnologien
description: Alle Viewer-Komponenten unterstützen ARIA-Rollen und -Attribute (Accessible Rich Internet Applications), um die Integration mit Hilfstechnologien wie der Sprachausgabe zu verbessern.
solution: Experience Manager
feature: Dynamic Media Classic,Viewers,SDK/API,Flyout,Accessibility
role: Developer,User
exl-id: 0f96939b-0ecc-4d4d-a084-60b023b2a5f2
source-git-commit: 50dddf148345d2ca5243d5d7108fefa56d23dad6
workflow-type: tm+mt
source-wordcount: '227'
ht-degree: 0%

---

# Unterstützung der Hilfstechnologien{#assistive-technology-support}

Alle Viewer-Komponenten unterstützen ARIA-Rollen und -Attribute (Accessible Rich Internet Applications), um die Integration mit Hilfstechnologien wie der Sprachausgabe zu verbessern.

Für das Viewer-Element der obersten Ebene sind Rolle `region` und `aria-label` Attribut standardmäßig auf den Namen des Viewers festgelegt. Sie können die Beschriftung mit dem `Container.LABEL` Lokalisierungssymbol steuern.

Für Schaltflächen sind die `button` und der beschreibende Text mit dem Attribut `aria-label` festgelegt. Der Wert `aria-label` Attributs wird aus dem Wert des Lokalisierungssymbols der Schaltfläche gefüllt. Wenn eine Schaltfläche deaktiviert ist, wird das `aria-disabled` entsprechend festgelegt.

Die Hauptansicht hat `application`. Eine kurze Beschreibung der Hauptansicht finden Sie in `aria-roledescription` mit dem Wert, der durch das `ROLE_DESCRIPTION` Lokalisierungssymbol der entsprechenden Hauptansichtskomponente definiert wird. Navigationshinweise für Tastaturbenutzer werden mithilfe von `aria-describedby` bereitgestellt. Der Text für den Verwendungshinweis stammt vom `USAGE_HINT` Lokalisierungssymbol. Wenn für ein Asset im Feld UserData eine Beschriftung definiert ist, wird das `aria-label` mit dem Wert dieser Beschriftung festgelegt.

Komponenten, die Farbfelder anzeigen, haben die Rolle `listbox`, wobei `aria-label` Attribut auf den Wert des `LABEL` Lokalisierungssymbols dieser Komponente gesetzt ist. Einzelne Farb-/Bildmuster haben die Rolle `option` mit `aria-setsize`- und `aria-posinset`-Attributen, um die Farb-/Bildmuster-Position im Set zu beschreiben. Wenn ein Farbfeld ausgewählt ist, wird das `aria-selected` auf `true` gesetzt.
