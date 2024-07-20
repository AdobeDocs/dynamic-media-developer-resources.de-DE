---
title: Seitenbezeichnungen verwalten
description: Seitenbezeichnungen verwalten
solution: Experience Manager
feature: Dynamic Media Classic,Viewers,SDK/API,eCatalog
role: Developer,User
exl-id: b62b5cb8-6100-4d0f-afd8-e6daa6ce6539
source-git-commit: a919130f0940d81a221b79563b6b3e41533ba788
workflow-type: tm+mt
source-wordcount: '263'
ht-degree: 0%

---

# Seitenbezeichnungen verwalten{#managing-page-labels}

Es gibt zwei Stellen in der Viewer-Benutzeroberfläche, an denen Seitenbezeichnungen angezeigt werden: den Modus Miniaturansichten und das Dropdown-Menü Inhaltsverzeichnis.

Es gibt drei Arten von Beschriftungen, die definiert werden können:

* Vom Autor mithilfe des SYMBOL-Lokalisierungsmechanismus definierte Beschriftungen.
* Beschriftungen, die vom Autor im Backend in Dynamic Media Classic definiert werden.
* Vom Viewer automatisch generierte Beschriftungen.

SYMBOL-basierte Beschriftungen werden mit &quot;`MediaSet.LABEL_XX[_YY]`&quot; und &quot;`MediaSet.LABEL_DELIM` SYMBOLs definiert, wie unter &quot;[Lokalisierung von Elementen der Benutzeroberfläche](../../c-html5-s7-aem-asset-viewers/c-html5-20-ecatalog-viewer-about/c-html5-20-ecatalog-viewer-localization.md#concept-cbfc39344c494eb7b9f6a272cff0cc74)&quot; beschrieben. Sie können diese Beschriftungen entweder für den gesamten E-Katalog definieren. In diesem Fall sollten Sie die kurze Syntax von SYMBOL ( `MediaSet.LABEL_XX`) verwenden. Oder geben Sie es für jede Seite einzeln mithilfe der vollständigen SYMBOL-Syntax ( `MediaSet.LABEL_XX_YY`) an.

Wenn Sie Beschriftungen für beide Seiten im E-Katalog definieren, verkettet der Viewer diese Beschriftungen mithilfe der SYMBOL `MediaSet.LABEL_DELIM` in einer Zeichenfolge. SYMBOL-basierte Beschriftungen haben Vorrang vor Beschriftungen, die im Backend definiert sind oder vom Viewer automatisch generierte Beschriftungen.

In Dynamic Media Classic definierte Beschriftungen werden im UserData-Datensatz einzelner Seitenbilder gespeichert. Wie bei SYMBOL-basierten Bezeichnungen. Das heißt, wenn für beide Seiten im E-Katalog Beschriftungen definiert sind, werden sie im Querformat mit `MediaSet.LABEL_DELIM` SYMBOL verkettet. Dynamic Media Classic-Beschriftungen haben Vorrang vor automatisch generierten Beschriftungen, werden jedoch durch SYMBOL-basierte Beschriftungen überschrieben.

Automatisch generierte Bezeichnungen sind sequenzielle Zahlen, die allen Seiten im Katalog zugewiesen werden. Automatisch generierte Bezeichnungen werden für den angegebenen Spread ignoriert, wenn SYMBOL-basierte Bezeichnungen definiert oder Dynamic Media Classic-Bezeichnungen definiert sind.

Im Inhaltsverzeichnis ist es möglich, die Anzeige automatisch generierter Bezeichnungen mithilfe des Parameters `showdefault` zu deaktivieren.
