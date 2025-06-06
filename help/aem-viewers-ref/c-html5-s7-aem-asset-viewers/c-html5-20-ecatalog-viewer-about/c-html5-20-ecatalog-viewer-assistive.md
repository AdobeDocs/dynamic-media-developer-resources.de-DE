---
title: Unterstützung der Hilfstechnologien
description: Alle Viewer-Komponenten unterstützen ARIA-Rollen und -Attribute (Accessible Rich Internet Applications), um die Integration mit Hilfstechnologien wie der Sprachausgabe zu verbessern.
solution: Experience Manager
feature: Dynamic Media Classic,Viewers,SDK/API,eCatalog,Accessibility
role: Developer,User
exl-id: 46ccea4e-4314-453e-a987-68644467ab12
source-git-commit: a919130f0940d81a221b79563b6b3e41533ba788
workflow-type: tm+mt
source-wordcount: '365'
ht-degree: 0%

---

# Unterstützung der Hilfstechnologien{#assistive-technology-support}

Alle Viewer-Komponenten unterstützen ARIA-Rollen und -Attribute (Accessible Rich Internet Applications), um die Integration mit Hilfstechnologien wie der Sprachausgabe zu verbessern.

Für das Viewer-Element der obersten Ebene sind Rolle `region` und `aria-label` Attribut standardmäßig auf den Namen des Viewers festgelegt. Sie können die Beschriftung mit dem `Container.LABEL` Lokalisierungssymbol steuern.

Für Schaltflächen sind die `button` und der beschreibende Text mit dem Attribut `aria-label` festgelegt. Der Wert `aria-label` Attributs wird aus dem Wert des Lokalisierungssymbols der Schaltfläche gefüllt. Wenn eine Schaltfläche deaktiviert ist, wird das `aria-disabled` entsprechend festgelegt.

Die Hauptansicht hat `application`. Eine kurze Beschreibung der Hauptansicht finden Sie in `aria-roledescription` mit dem Wert, der durch das `ROLE_DESCRIPTION` Lokalisierungssymbol der entsprechenden Hauptansichtskomponente definiert wird. Navigationshinweise für Tastaturbenutzer werden mithilfe von `aria-describedby` bereitgestellt. Der Text für den Verwendungshinweis stammt vom `USAGE_HINT` Lokalisierungssymbol. Wenn für ein Asset im Feld UserData eine Beschriftung definiert ist, wird das `aria-label` mit dem Wert dieser Beschriftung festgelegt.

Für Hotspots, Regionen und Imagemaps sind die Rolle &quot;`button`&quot; und ein beschreibender Text mit `aria-label` Attribut festgelegt, wobei der Wert der Hotspot- oder Imagemap-Beschriftung ist. Wenn der Fokus auf Hotspots oder Imagemaps gelegt wird, werden Navigationshinweise für Tastaturbenutzer mithilfe von `aria-describedby` bereitgestellt, wobei der Text für den Verwendungshinweis vom `USAGE_HINT` Lokalisierungssymbol stammt.

Miniaturen haben die Rolle `dialog` mit `aria-label` Attribut , das durch das `ThumbnailGridView.LABEL` Lokalisierungssymbol gesteuert wird. Einzelne Miniaturen haben die Rolle `button`. Wenn Sie eine Miniaturansicht auswählen, wird `aria-selected` Attribut auf `true` gesetzt.

Komponenten, die Farbfelder anzeigen, haben die Rolle `listbox`, wobei `aria-label` Attribut auf den Wert des `LABEL` Lokalisierungssymbols dieser Komponente gesetzt ist. Einzelne Farb-/Bildmuster haben die Rolle `option` mit `aria-setsize`- und `aria-posinset`-Attributen, um die Farb-/Bildmuster-Position im Set zu beschreiben. Wenn ein Farbfeld ausgewählt ist, wird das `aria-selected` auf `true` gesetzt.

Dropdown-Listen werden durch Schaltflächen aktiviert, wobei das zusätzliche `aria-haspopup`-Attribut auf `true` und das `aria-controls`-Attribut auf das tatsächliche Dropdown-Bedienfeldelement verweist. Das Dropdown-Bedienfeld selbst hat die Rolle `menu` mit Unterelementen mit der Rolle `menuitem`. Für jedes Menüelement ist das `aria-label` Attribut angegeben.

Modale Dialogfelder haben die Rolle `dialog`. Das Kopfzeilenelement des Dialogfelds wird durch das Attribut `aria-labelledby` referenziert.
