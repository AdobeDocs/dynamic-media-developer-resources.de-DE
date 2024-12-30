---
title: Materialkatalog - Übersicht
description: Materialkataloge stellen dem Server Informationen zu Vignetten, Materialien und unterstützenden Daten, wie z. B. ICC-Profilen, bereit.
solution: Experience Manager
feature: Dynamic Media Classic,SDK/API
role: Developer,User
exl-id: d26371da-e992-4f63-a5be-190ce60eca2f
source-git-commit: 8454991568374ecd1c4babdd3210250ea7988c4c
workflow-type: tm+mt
source-wordcount: '413'
ht-degree: 0%

---

# Materialkatalog - Übersicht{#material-catalog-overview}

Materialkataloge stellen dem Server Informationen zu Vignetten, Materialien und unterstützenden Daten, wie z. B. ICC-Profilen, bereit.

Jeder Materialkatalog besteht aus einer erforderlichen *Katalogattributdatei* und einem Satz optionaler *Katalogdatendateien*:

* Die Vignettenzuordnungsdatei, in der Vignetten und Vorlagen und die zugehörigen Metadaten aufgeführt sind.
* Die Materialdatendatei, in der Materialien aufgelistet werden und die die zugehörigen Texturbilddateien und Metadaten angegeben sind.
* Die Datei mit den Makrodefinitionen, die Definitionen für Anforderungsmakros bereitstellt.
* Die Profilzuordnungsdatei, in der ICC-Farbprofile aufgeführt sind.

Katalogdatendateien werden über Dateiverweise in der Katalogattributdatei mit Materialkatalogen verknüpft. Eine Katalogdatendatei kann von mehreren Materialkatalogen gemeinsam genutzt werden.

Katalogattributdateien müssen eine [!DNL `.ini`] Dateiendung und im Image Rendering-*Katalogordner)*[!DNL PlatformServer::ir.catalogRootPath]) enthalten. Katalogdatendateien können sich im selben Ordner oder einem beliebigen anderen Ordner befinden, auf den der Render-Server zugreifen kann.

**Aktualisieren von Materialkatalogen**

Der Server überwacht kontinuierlich den Katalogordner. Ein Materialkatalog wird automatisch neu geladen - einschließlich der zugehörigen Katalogdatendateien -, wenn festgestellt wird, dass die Hauptkatalogattributdatei geändert wurde. Um Materialkataloge auf dem Server zu aktualisieren, ersetzen Sie daher zunächst alle zu ändernden Katalogdatendateien und ersetzen (oder „berühren„) Sie dann die Katalogattributdatei, um das erneute Laden des Katalogs in den Trigger aufzunehmen.

**Standardkatalog**

Der Standardkatalog stellt Standardwerte für alle Katalogattribute für alle Materialkataloge bereit. Wenn ein bestimmtes Attribut in einem bestimmten Materialkatalog nicht gefunden werden kann, verwendet der Server stattdessen den entsprechenden Wert aus dem Standardkatalog. Ebenso kann der Standardkatalog verwendet werden, um Standardwerte für bestimmte Katalogdatensätze (Materialien und ICC-Profile) bereitzustellen. Wenn ein bestimmter Datensatz nicht in einem bestimmten Materialkatalog gefunden werden kann, versucht der Server stattdessen, ihn im Standardkatalog zu finden. Dies ermöglicht es, Materialkataloge spärlich auszufüllen und vereinfacht die Verwaltung globaler Attribute und Daten wie freigegebene Vorlagen, Makros und Schriftarten.

Darüber hinaus stellt der Standardkatalog alle Attribute und Datensätze (ICC-Profile) bereit, wenn an einem Vorgang kein bestimmter Materialkatalog beteiligt ist.

Damit der Render-Server ordnungsgemäß funktioniert, muss die Katalogattributdatei für den Standardkatalog [!DNL default.ini] benannt sein. Sie muss auch immer im Katalogordner vorhanden sein und vollständig mit allen erforderlichen Attributen gefüllt sein, mit Ausnahme von `attribute::RootId` und den Verweisen auf die verschiedenen Katalogdatendateien, die alle optional sind.

<!-- **See also**

`PlatformServer::ir.catalogRootPath` -->
