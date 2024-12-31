---
description: Verwalten von Seitenbeschriftungen
solution: Experience Manager
title: Verwalten von Seitenbeschriftungen
feature: Dynamic Media Classic,Viewers,SDK/API,eCatalog Search
role: Developer,User
exl-id: 73c3904f-678f-47c4-b895-86671402df79
source-git-commit: 206e4643e3926cb85b4be2189743578f88180be7
workflow-type: tm+mt
source-wordcount: '263'
ht-degree: 0%

---

# Verwalten von Seitenbeschriftungen{#managing-page-labels}

In der Viewer-Benutzeroberfläche gibt es zwei Stellen, an denen Seitenbeschriftungen angezeigt werden: im Miniaturansichtsmodus und in der Dropdown-Liste Inhaltsverzeichnis .

Es gibt drei Arten von Beschriftungen, die definiert werden können:

* Vom Autor mithilfe des SYMBOL-Lokalisierungsmechanismus definierte Beschriftungen.
* Vom Autor definierte Kennzeichnungen im Backend innerhalb von Dynamic Media Classic.
* Vom Viewer automatisch generierte Kennzeichnungen.

SYMBOL-basierte Kennzeichnungen werden mithilfe von `MediaSet.LABEL_XX[_YY]` und `MediaSet.LABEL_DELIM`-SYMBOLEN definiert, wie in [Lokalisierung von Benutzeroberflächenelementen“ ](../../c-html5-s7-aem-asset-viewers/c-html5-20-ecatalog-viewer-about/c-html5-20-ecatalog-viewer-localization.md#concept-cbfc39344c494eb7b9f6a272cff0cc74). Sie können solche Kennzeichnungen entweder für den gesamten eCatalog-Spread definieren. In diesem Fall sollten Sie die kurze SYMBOL-Syntax ( `MediaSet.LABEL_XX`) verwenden. Oder geben Sie sie für jede Seite einzeln mit der vollständigen SYMBOL-Syntax ( `MediaSet.LABEL_XX_YY`) an.

Wenn Sie Beschriftungen für beide Seiten im E-Katalog-Spread definieren, verkettet der Viewer diese Beschriftungen mithilfe `MediaSet.LABEL_DELIM` SYMBOLS zu einer Zeichenfolge. SYMBOLBASIERTE Beschriftungen haben Vorrang vor Beschriftungen, die im Backend definiert oder automatisch vom Viewer generiert werden.

In Dynamic Media Classic definierte Kennzeichnungen werden im Benutzerdatensatz der einzelnen Seitenbilder gespeichert. Wie bei SYMBOL-basierten Kennzeichnungen. Das heißt, wenn auf beiden Seiten im E-Katalog-Spread Beschriftungen definiert sind, werden sie mit `MediaSet.LABEL_DELIM` SYMBOL im Querformat verkettet. Dynamic Media Classic-Kennzeichnungen haben Vorrang vor automatisch generierten Kennzeichnungen, werden jedoch durch SYMBOL-basierte Kennzeichnungen überschrieben.

Automatisch generierte Beschriftungen sind fortlaufende Nummern, die allen Seiten im E-Katalog zugewiesen werden. Automatisch generierte Kennzeichnungen werden für den angegebenen Spread ignoriert, wenn SYMBOL-basierte Kennzeichnungen oder Dynamic Media Classic-Kennzeichnungen definiert sind.

Im Inhaltsverzeichnis ist es möglich, die Anzeige automatisch generierter Kennzeichnungen mit `showdefault` Parameter zu deaktivieren.
