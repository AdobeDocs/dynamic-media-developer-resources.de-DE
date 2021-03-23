---
description: Verwalten von Seitenbeschriftungen
solution: Experience Manager
title: Verwalten von Seitenbeschriftungen
uuid: ab3df37d-113b-4762-ba9c-b92ffc41f1a2
feature: Dynamic Media Classic, Viewer, SDK/API, E-Katalog
role: Entwickler, Geschäftspraktiker
translation-type: tm+mt
source-git-commit: 469d1a5c43a972116a8a2efb0de5708800130a99
workflow-type: tm+mt
source-wordcount: '273'
ht-degree: 0%

---


# Verwalten von Seitenbeschriftungen{#managing-page-labels}

Es gibt zwei Stellen in der Benutzeroberfläche des Viewers, an denen Seitenbeschriftungen angezeigt werden: Miniaturansichten und das Inhaltsverzeichnis-Dropdown-Menü.

Es gibt drei Arten von Bezeichnungen, die definiert werden können:

* Vom Autor mithilfe der SYMBOL-lokale Anpassung definierte Bezeichnungen.
* Vom Autor definierte Bezeichnungen im Backend, in Dynamic Media Classic.
* Vom Viewer automatisch generierte Bezeichnungen.

SYMBOL-basierte Beschriftungen werden mithilfe von `MediaSet.LABEL_XX[_YY]`- und `MediaSet.LABEL_DELIM`-SYMBOLs definiert, wie in [Lokale Anpassung der Elemente der Benutzeroberfläche](../../c-html5-s7-aem-asset-viewers/c-html5-20-ecatalog-viewer-about/c-html5-20-ecatalog-viewer-localization.md#concept-cbfc39344c494eb7b9f6a272cff0cc74) beschrieben. Sie können diese Beschriftungen entweder für den gesamten Katalog-Druckbogen definieren. In diesem Fall sollten Sie eine kurze SYMBOL-Syntax ( `MediaSet.LABEL_XX`) verwenden. Oder geben Sie es für jede Seite einzeln mit vollständiger SYMBOL-Syntax ( `MediaSet.LABEL_XX_YY`) an.

Wenn Sie Beschriftungen für beide Seiten im E-Katalog definieren, verkettet der Viewer diese Beschriftungen mit `MediaSet.LABEL_DELIM` SYMBOL in einer Zeichenfolge. SYMBOL-basierte Beschriftungen haben Vorrang vor Beschriftungen, die auf dem Backend oder automatisch vom Viewer generierten Beschriftungen definiert werden.

In Dynamic Media Classic definierte Bezeichnungen werden im UserData-Datensatz einzelner Seitenbilder gespeichert. Wie bei SYMBOL-basierten Beschriftungen. Das heißt, wenn beide Seiten im E-Katalog Beschriftungen definiert haben, werden sie mit `MediaSet.LABEL_DELIM` SYMBOL im Querformat verkettet. Dynamic Media Classic-Beschriftungen haben Vorrang vor automatisch generierten Beschriftungen, werden jedoch von SYMBOL-basierten Beschriftungen überschrieben.

Automatisch generierte Beschriftungen sind fortlaufende Nummern, die allen Seiten im Katalog zugewiesen werden. Automatisch generierte Beschriftungen werden für den angegebenen Druckbogen ignoriert, wenn SYMBOL-basierte Beschriftungen definiert oder Dynamic Media Classic-Beschriftungen definiert sind.

Im Inhaltsverzeichnis ist es möglich, die Anzeige automatisch generierter Beschriftungen mit dem Parameter `showdefault` zu deaktivieren.
