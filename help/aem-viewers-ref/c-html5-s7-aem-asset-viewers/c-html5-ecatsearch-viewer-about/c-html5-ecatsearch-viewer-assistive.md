---
description: Alle Viewer-Komponenten unterstützen ARIA-Rollen und -Attribute (Accessible Rich Internet Applications), um die Integration mit Hilfstechnologien wie der Sprachausgabe zu verbessern.
solution: Experience Manager
title: Unterstützung der Hilfstechnologien
feature: Dynamic Media Classic,Viewers,SDK/API,eCatalog Search,Accessibility
role: Developer,User
exl-id: fbfc9415-6ab8-466c-9a1f-d33565eff2a4
TQID: 'https://experienceleague.adobe.com/iaM1o85zC7GNh-RZcMYfjGk99eb8RfobLSGLzwtbOqk'
product_v2: id: fd1f54a9-f50c-467d-8956-cebbaf4f3eb8
feature_v2: id: a01bfd36-4ab8-4bf8-9dc0-5b45b890552e
role_v2: id: b69b2659-1057-424e-8fc5-ed9e016dc554id: ff6a42d2-313e-452e-93a6-792e4fad9ff8
topic_v2: id: cc72dcf1-72e1-48cc-b434-e7c27d62d67c
source-git-commit: f6432244ef9faba7a81488e9de8e438154ae6123
workflow-type: tm+mt
source-wordcount: 398
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

Die Benutzeroberfläche für die Suche ist in dem Element mit der Rolle `search` gruppiert. Das Sucheingabefeld hat die Rolle `searchbox` und verweist auf die informative Beschriftung, die durch `SearchPanel.INFO_PROMPT` Lokalisierungssymbol mit `aria-describedby` Attribut gesteuert wird.

Modale Dialogfelder haben die Rolle `dialog`. Das Kopfzeilenelement des Dialogfelds wird durch das Attribut `aria-labelledby` referenziert.

