---
description: 'null'
seo-description: 'null'
seo-title: Verwalten von Seitenbeschriftungen
solution: Experience Manager
title: Verwalten von Seitenbeschriftungen
topic: Dynamic media
uuid: 49444fe6-ef34-4e5b-a293-e23830a67b4d
translation-type: tm+mt
source-git-commit: 7bc7b3a86fbcdc57cfdc31745fae3afc06e44b15

---


# Verwalten von Seitenbeschriftungen{#managing-page-labels}

Es gibt zwei Stellen in der Benutzeroberfläche des Viewers, an denen Seitenbeschriftungen angezeigt werden: Miniaturansichten und das Inhaltsverzeichnis-Dropdown-Menü.

Es gibt drei Arten von Bezeichnungen, die definiert werden können:

* Vom Autor mithilfe der SYMBOL-lokale Anpassung definierte Bezeichnungen.
* Vom Autor definierte Beschriftungen im Backend, im Scene7 Publishing System.
* Vom Viewer automatisch generierte Bezeichnungen.

SYMBOL-basierte Beschriftungen werden mithilfe von `MediaSet.LABEL_XX[_YY]` und `MediaSet.LABEL_DELIM` SYMBOLs definiert, wie in der [Lokale Anpassung der Benutzeroberflächenelemente](../../c-html5-s7-aem-asset-viewers/c-html5-20-ecatalog-viewer-about/c-html5-20-ecatalog-viewer-localization.md#concept-cbfc39344c494eb7b9f6a272cff0cc74)beschrieben. Sie können diese Bezeichnungen entweder für den gesamten Katalog-Druckbogen definieren. In diesem Fall sollten Sie eine kurze SYMBOL-Syntax ( `MediaSet.LABEL_XX`) verwenden. Oder geben Sie es für jede Seite einzeln mit vollständiger SYMBOL-Syntax an ( `MediaSet.LABEL_XX_YY`).

Wenn Sie Beschriftungen für beide Seiten im E-Katalog definieren, verkettet der Viewer diese Beschriftungen mithilfe von `MediaSet.LABEL_DELIM` SYMBOL in eine Zeichenfolge. SYMBOL-basierte Beschriftungen haben Vorrang vor Beschriftungen, die auf dem Backend oder automatisch vom Viewer generierten Beschriftungen definiert werden.

Im Scene7 Publishing System definierte Bezeichnungen werden im UserData-Datensatz einzelner Seitenbilder gespeichert. Wie bei SYMBOL-basierten Beschriftungen. Das heißt, wenn beide Seiten im Katalog Beschriftungen definiert haben, werden sie mithilfe von `MediaSet.LABEL_DELIM` SYMBOL im Querformat verkettet. Die Bezeichnungen des Scene7 Publishing Systems haben Vorrang vor automatisch generierten Bezeichnungen, werden jedoch von SYMBOL-basierten Bezeichnungen überschrieben.

Automatisch generierte Beschriftungen sind fortlaufende Nummern, die allen Seiten im Katalog zugewiesen werden. Automatisch generierte Beschriftungen werden für den angegebenen Druckbogen ignoriert, wenn SYMBOL-basierte Beschriftungen oder Scene7 Publishing System-Beschriftungen definiert sind.

Im Inhaltsverzeichnis ist es möglich, die Anzeige automatisch generierter Bezeichnungen mithilfe von `showdefault` Parametern zu deaktivieren.
