---
title: Unterstützung der Hilfstechnologien
description: Alle Viewer-Komponenten unterstützen ARIA-Rollen und -Attribute (Accessible Rich Internet Applications), um die Integration mit Hilfstechnologien wie der Sprachausgabe zu verbessern.
solution: Experience Manager
feature: Dynamic Media Classic,Viewers,SDK/API,Carousel Banners,Accessibility
role: Developer,User
exl-id: 3ed943e8-4695-4561-9be0-1b6ed30294f8
source-git-commit: 4aaa77b1fb58b30b02ee15f6080169fa354d5907
workflow-type: tm+mt
source-wordcount: '267'
ht-degree: 0%

---

# Unterstützung der Hilfstechnologien{#assistive-technology-support}

Alle Viewer-Komponenten unterstützen ARIA-Rollen und -Attribute (Accessible Rich Internet Applications), um die Integration mit Hilfstechnologien wie der Sprachausgabe zu verbessern.

Für das Viewer-Element der obersten Ebene sind Rolle `region` und `aria-label` Attribut standardmäßig auf den Namen des Viewers festgelegt. Sie können die Beschriftung mit dem `Container.LABEL` Lokalisierungssymbol steuern.

Für Schaltflächen sind der `button` und der beschreibende Text mit dem Attribut `aria-label` festgelegt. Der Wert `aria-label` Attributs wird aus dem Wert des Lokalisierungssymbols der Schaltfläche gefüllt. Wenn eine Schaltfläche deaktiviert ist, wird `aria-disabled` Attribut entsprechend festgelegt.

Schaltflächen, mit denen Sie durch Karussellfolien navigieren können, verfügen über Beschriftungen, die zur Laufzeit je nach der aktuell ausgewählten Folie aktualisiert werden. Die Vorlage für diese Schaltflächenbeschriftung ist mit `CAROUSELVIEWER_TOOLTIP_GOTO` Lokalisierungssymbol festgelegt.

Die Hauptansicht hat `application`. Eine kurze Beschreibung der Hauptansicht finden Sie in `aria-roledescription` mit dem Wert, der durch das `ROLE_DESCRIPTION` Lokalisierungssymbol der entsprechenden Hauptansichtskomponente definiert wird. Navigationshinweise für Tastaturbenutzer werden mithilfe von `aria-describedby` bereitgestellt. Der Text für den Verwendungshinweis stammt vom `USAGE_HINT` Lokalisierungssymbol. Wenn für ein Asset im Feld UserData eine Beschriftung definiert ist, wird das `aria-label` mit dem Wert dieser Beschriftung festgelegt.

Für Hotspots, Regionen und Imagemaps sind die Rolle &quot;`button`&quot; und ein beschreibender Text mit `aria-label` Attribut festgelegt, wobei der Wert der Hotspot- oder Imagemap-Beschriftung ist. Wenn der Fokus auf Hotspots oder Imagemaps gelegt wird, werden Navigationshinweise für Tastaturbenutzer mithilfe von `aria-describedby` bereitgestellt, wobei der Text für den Verwendungshinweis vom `USAGE_HINT` Lokalisierungssymbol stammt.
