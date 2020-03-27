---
description: Materialkataloge liefern dem Server Informationen über Vignetten, Materialien und unterstützende Daten, wie z. B. ICC-Profile.
seo-description: Materialkataloge liefern dem Server Informationen über Vignetten, Materialien und unterstützende Daten, wie z. B. ICC-Profile.
seo-title: Übersicht über den Materialkatalog *
solution: Experience Manager
title: Übersicht über den Materialkatalog *
topic: Scene7 Image Serving - Image Rendering API
uuid: f2128b64-8caf-4a59-b11f-604fe62bae69
translation-type: tm+mt
source-git-commit: 7bc7b3a86fbcdc57cfdc31745fae3afc06e44b15

---


# Übersicht über den Materialkatalog *{#material-catalog-overview}

Materialkataloge liefern dem Server Informationen über Vignetten, Materialien und unterstützende Daten, wie z. B. ICC-Profile.

Jeder Materialkatalog besteht aus einer erforderlichen *Katalogattributdatei* und einem Satz optionaler *Katalogdatendateien*:

* Die Vignettenzuordnungsdatei, die Vignetten und Vorlagen und die zugehörigen Metadaten infiziert.
* Die Materialdatendatei, die die Materialien infiziert und die zugehörigen Texturbilddateien und Metadaten angibt.
* Die Datei mit den Makrodefinitionen, die Definitionen für Anforderungsmakros bereitstellt.
* Die Profil-Map-Datei, die ICC-Profile itemisiert.

Katalogdatendateien werden mit Materialkatalogen nach Dateiverweisen in der Katalogattributdatei verknüpft. Die gleiche Katalogdatendatei kann für mehrere Materialkataloge freigegeben werden.

Katalogattributdateien müssen über ein Suffix [!DNL .ini] verfügen und sich im *Katalogordner* &quot;Image Rendering&quot;befinden ( [!DNL PlatformServer::ir.catalogRootPath]). Katalogdatendateien können sich im selben Ordner oder in einem anderen Ordner befinden, auf den der Render-Server zugreifen kann.

**Aktualisieren von Materialkatalogen**

Der Server überwacht kontinuierlich den Katalogordner und lädt automatisch einen Materialkatalog einschließlich der zugehörigen Katalogdatendateien neu, wenn er feststellt, dass die Hauptkatalogattributdatei geändert wurde. Um also Materialkataloge auf dem Server zu aktualisieren, ersetzen Sie zunächst alle Katalogdatendateien, die geändert werden müssen, und ersetzen Sie dann die Katalogattributdatei (oder &quot;berühren&quot;), um das Neuladen des Katalogs auszulösen.

**Standardkatalog**

Der Standardkatalog enthält Standardwerte für alle Katalogattribute für alle Materialkataloge. Wenn ein bestimmtes Attribut nicht in einem bestimmten Materialkatalog gefunden werden kann, verwendet der Server stattdessen den entsprechenden Wert aus dem Standardkatalog. Gleichermaßen kann der Standardkatalog verwendet werden, um Standardwerte für bestimmte Katalogdatensätze (Materialien und ICC-Profile) bereitzustellen. Wenn ein bestimmter Datensatz nicht in einem bestimmten Materialkatalog gefunden werden kann, versucht der Server, ihn stattdessen im Standardkatalog zu finden. Dadurch können Materialkataloge dünn gefüllt werden und die Verwaltung globaler Attribute und Daten, wie freigegebene Vorlagen, Makros, Schriftarten usw., wird vereinfacht.

Darüber hinaus stellt der Standardkatalog alle Attribute und Datensätze (ICC-Profile) bereit, wenn kein spezifischer Materialkatalog an einem Vorgang beteiligt ist.

Damit der Render-Server ordnungsgemäß funktioniert, muss die Katalogattributdatei für den Standardkatalog benannt werden, muss immer im Katalogordner vorhanden sein und muss vollständig mit allen erforderlichen Attributen gefüllt sein, mit Ausnahme [!DNL default.ini]`attribute::RootId` und der Verweise auf die verschiedenen Katalogdatendateien, die alle optional sind.

**Verwandte Themen**

`PlatformServer::ir.catalogRootPath`
