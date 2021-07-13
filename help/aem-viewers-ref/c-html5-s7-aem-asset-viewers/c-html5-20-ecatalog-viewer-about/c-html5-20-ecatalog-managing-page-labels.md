---
description: Verwalten von Seitenbeschriftungen
solution: Experience Manager
title: Verwalten von Seitenbeschriftungen
feature: Dynamic Media Classic,Viewers,SDK/API,eCatalog
role: Developer,User
exl-id: b62b5cb8-6100-4d0f-afd8-e6daa6ce6539
source-git-commit: 206e4643e3926cb85b4be2189743578f88180be7
workflow-type: tm+mt
source-wordcount: '270'
ht-degree: 0%

---

# Verwalten von Seitenbeschriftungen{#managing-page-labels}

Es gibt zwei Stellen in der Viewer-Benutzeroberfläche, an denen Seitenbeschriftungen angezeigt werden: Miniaturansichten und das Dropdown-Menü des Inhaltsverzeichnisses.

Es gibt drei Arten von Beschriftungen, die definiert werden können:

* Vom Autor mithilfe des SYMBOL-Lokalisierungsmechanismus definierte Beschriftungen.
* Beschriftungen, die vom Autor im Backend in Dynamic Media Classic definiert werden.
* Vom Viewer automatisch generierte Beschriftungen.

SYMBOL-basierte Beschriftungen werden mit `MediaSet.LABEL_XX[_YY]` und `MediaSet.LABEL_DELIM` SYMBOLs definiert, wie unter [Lokalisierung von Benutzeroberflächenelementen](../../c-html5-s7-aem-asset-viewers/c-html5-20-ecatalog-viewer-about/c-html5-20-ecatalog-viewer-localization.md#concept-cbfc39344c494eb7b9f6a272cff0cc74) beschrieben. Sie können diese Beschriftungen entweder für den gesamten E-Katalog-Spread definieren. In diesem Fall sollten Sie die kurze Syntax von SYMBOL ( `MediaSet.LABEL_XX`) verwenden. Oder geben Sie es für jede Seite einzeln mithilfe der vollständigen SYMBOL-Syntax ( `MediaSet.LABEL_XX_YY`) an.

Wenn Sie Beschriftungen für beide Seiten im E-Katalog definieren, verkettet der Viewer diese Beschriftungen mithilfe von `MediaSet.LABEL_DELIM` SYMBOL zu einer Zeichenfolge. SYMBOL-basierte Beschriftungen haben Vorrang vor Beschriftungen, die im Backend definiert sind oder vom Viewer automatisch generierte Beschriftungen.

In Dynamic Media Classic definierte Beschriftungen werden im UserData-Datensatz einzelner Seitenbilder gespeichert. Wie bei SYMBOL-basierten Bezeichnungen. Wenn also für beide Seiten im E-Katalog Beschriftungen definiert sind, werden sie im Querformat mithilfe der SYMBOL `MediaSet.LABEL_DELIM` verkettet. Dynamic Media Classic-Beschriftungen haben Vorrang vor automatisch generierten Beschriftungen, werden jedoch von SYMBOL-basierten Beschriftungen überschrieben.

Automatisch generierte Bezeichnungen sind sequenzielle Zahlen, die allen Seiten im Katalog zugewiesen werden. Automatisch generierte Beschriftungen werden für den angegebenen Spread ignoriert, wenn SYMBOL-basierte Beschriftungen definiert sind oder Dynamic Media Classic-Beschriftungen definiert sind.

Im Inhaltsverzeichnis ist es möglich, die Anzeige automatisch generierter Bezeichnungen mithilfe des Parameters `showdefault` zu deaktivieren.
