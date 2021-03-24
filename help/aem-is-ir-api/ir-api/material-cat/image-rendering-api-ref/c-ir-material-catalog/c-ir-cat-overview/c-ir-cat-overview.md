---
description: Materialkataloge liefern dem Server Informationen über Vignetten, Materialien und unterstützende Daten, wie z. B. ICC-Profile.
solution: Experience Manager
title: Übersicht über den Materialkatalog *
feature: Dynamic Media Classic, SDK/API
role: Entwickler, Geschäftspraktiker
translation-type: tm+mt
source-git-commit: f6c97606d7a4209427316d7367013ad9585a5cae
workflow-type: tm+mt
source-wordcount: '426'
ht-degree: 0%

---


# Übersicht über den Materialkatalog *{#material-catalog-overview}

Materialkataloge liefern dem Server Informationen über Vignetten, Materialien und unterstützende Daten, wie z. B. ICC-Profile.

Jeder Materialkatalog besteht aus einer erforderlichen *Katalogattributdatei* und einem Satz optionaler *Katalogdatendateien*:

* Die Vignettenzuordnungsdatei, die Vignetten und Vorlagen und die zugehörigen Metadaten infiziert.
* Die Materialdatendatei, die die Materialien infiziert und die zugehörigen Texturbilddateien und Metadaten angibt.
* Die Datei mit den Makrodefinitionen, die Definitionen für Anforderungsmakros bereitstellt.
* Die Profil-Map-Datei, die ICC-Profile itemisiert.

Katalogdatendateien werden mit Materialkatalogen nach Dateiverweisen in der Katalogattributdatei verknüpft. Die gleiche Katalogdatendatei kann für mehrere Materialkataloge freigegeben werden.

Katalogattributdateien müssen über das Suffix [!DNL .ini] verfügen und sich im Ordner *Katalog* ( [!DNL PlatformServer::ir.catalogRootPath]) befinden. Katalogdatendateien können sich im selben Ordner oder in einem anderen Ordner befinden, auf den der Render-Server zugreifen kann.

**Aktualisieren von Materialkatalogen**

Der Server überwacht kontinuierlich den Katalogordner und lädt automatisch einen Materialkatalog einschließlich der zugehörigen Katalogdatendateien neu, wenn er feststellt, dass die Hauptkatalogattributdatei geändert wurde. Um Materialkataloge auf dem Server zu aktualisieren, ersetzen Sie zunächst alle Katalogdatendateien, die geändert werden müssen, und ersetzen Sie dann die Katalogattributdatei (oder &quot;berühren&quot;), um den Trigger des Katalogneuladens zu erhalten.

**Standardkatalog**

Der Standardkatalog enthält Standardwerte für alle Katalogattribute für alle Materialkataloge. Wenn ein bestimmtes Attribut nicht in einem bestimmten Materialkatalog gefunden werden kann, verwendet der Server stattdessen den entsprechenden Wert aus dem Standardkatalog. Gleichermaßen kann der Standardkatalog verwendet werden, um Standardwerte für bestimmte Katalogdatensätze (Materialien und ICC-Profile) bereitzustellen. Wenn ein bestimmter Datensatz nicht in einem bestimmten Materialkatalog gefunden werden kann, versucht der Server, ihn stattdessen im Standardkatalog zu finden. Dadurch können Materialkataloge dünn gefüllt werden und die Verwaltung globaler Attribute und Daten, wie freigegebene Vorlagen, Makros, Schriftarten usw., wird vereinfacht.

Darüber hinaus stellt der Standardkatalog alle Attribute und Datensätze (ICC-Profile) bereit, wenn kein spezifischer Materialkatalog an einem Vorgang beteiligt ist.

Damit der Render-Server ordnungsgemäß funktioniert, muss die Katalogattributdatei für den Standardkatalog mit dem Namen [!DNL default.ini], immer im Katalogordner vorhanden sein und mit allen erforderlichen Attributen gefüllt werden, mit Ausnahme von `attribute::RootId` und der Verweise auf die verschiedenen Katalogdatendateien, die alle optional sind.

**Verwandte Themen**

`PlatformServer::ir.catalogRootPath`
