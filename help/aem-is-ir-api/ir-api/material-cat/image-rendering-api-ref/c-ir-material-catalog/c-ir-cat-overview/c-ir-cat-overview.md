---
title: Materialkatalog - Übersicht
description: Materialkataloge stellen dem Server Informationen zu Vignetten, Materialien und unterstützenden Daten, wie z. B. ICC-Profilen, bereit.
solution: Experience Manager
feature: Dynamic Media Classic,SDK/API
role: Developer,User
exl-id: d26371da-e992-4f63-a5be-190ce60eca2f
TQID: 'https://experienceleague.adobe.com/wMShsstpVRBE4JNSUshejo0Qn6NXVB85YbLx5Pf9PEI'
product_v2: id: fd1f54a9-f50c-467d-8956-cebbaf4f3eb8
feature_v2: id: a01bfd36-4ab8-4bf8-9dc0-5b45b890552e
role_v2: id: b69b2659-1057-424e-8fc5-ed9e016dc554id: ff6a42d2-313e-452e-93a6-792e4fad9ff8
topic_v2: id: a004cc84-67b9-4a33-a3a7-8ec7273ef4dc
source-git-commit: 2ff64206b7448a1a122696facd2669be68b6b9ff
workflow-type: tm+mt
source-wordcount: 413
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

<!--
 **See also**

`PlatformServer::ir.catalogRootPath`
-->
