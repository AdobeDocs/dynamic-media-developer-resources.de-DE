---
description: Materialkataloge liefern dem Server Informationen über Vignetten, Materialien und unterstützende Daten wie ICC-Profile.
solution: Experience Manager
title: Übersicht über den Materialkatalog *
feature: Dynamic Media Classic,SDK/API
role: Developer,User
exl-id: d26371da-e992-4f63-a5be-190ce60eca2f
source-git-commit: 206e4643e3926cb85b4be2189743578f88180be7
workflow-type: tm+mt
source-wordcount: '423'
ht-degree: 0%

---

# Übersicht über den Materialkatalog *{#material-catalog-overview}

Materialkataloge liefern dem Server Informationen über Vignetten, Materialien und unterstützende Daten wie ICC-Profile.

Jeder Materialkatalog besteht aus einer erforderlichen *Katalogattributdatei* und einer Reihe optionaler *Katalogdatendateien*:

* Die Vignettenzuordnungsdatei, in der Vignetten und Vorlagen sowie die zugehörigen Metadaten auflistet werden.
* Die Materialdatendatei, die Materialien auflistet und die zugehörigen Texturbilddateien und Metadaten angibt.
* Die Makro-Definitionsdatei, die Definitionen für Anforderungsmakros bereitstellt.
* Die Profilzuordnungsdatei, die ICC-Farbprofile auflistet.

Katalogdatendateien sind Materialkatalogen nach Dateiverweisen in der Katalogattributdatei zugeordnet. Dieselbe Katalogdatendatei kann für mehrere Materialkataloge freigegeben werden.

Katalogattributdateien müssen das Suffix [!DNL .ini] aufweisen und sich im Ordner &quot;Image Rendering *catalog* ( [!DNL PlatformServer::ir.catalogRootPath]) befinden. Katalogdatendateien können sich im selben Ordner oder in einem anderen Ordner befinden, auf den der Render Server zugreifen kann.

**Aktualisieren von Materialkatalogen**

Der Server überwacht kontinuierlich den Katalogordner und lädt automatisch einen Materialkatalog einschließlich der zugehörigen Katalogdatendateien neu, wenn er feststellt, dass die Hauptkatalogattributdatei geändert wurde. Um also Materialkataloge auf dem Server zu aktualisieren, ersetzen Sie zunächst alle Katalogdatendateien, die geändert werden müssen, und ersetzen Sie dann die Katalogattributdatei (oder &quot;berühren&quot;), um das Neuladen des Katalogs Trigger.

**Standardkatalog**

Der Standardkatalog enthält Standardwerte für alle Katalogattribute für alle Materialkataloge. Wenn ein bestimmtes Attribut nicht in einem bestimmten Materialkatalog gefunden werden kann, verwendet der Server stattdessen den entsprechenden Wert aus dem Standardkatalog. Ebenso kann der Standardkatalog verwendet werden, um Standardwerte für bestimmte Katalogdatensätze (Materialien und ICC-Profile) bereitzustellen. Wenn ein bestimmter Datensatz nicht in einem bestimmten Materialkatalog gefunden werden kann, versucht der Server, ihn stattdessen im Standardkatalog zu finden. Dadurch können Materialkataloge spärlich befüllt werden und die Verwaltung globaler Attribute und Daten wie freigegebener Vorlagen, Makros, Schriftarten usw. wird vereinfacht.

Darüber hinaus stellt der Standardkatalog alle Attribute und Datensätze (ICC-Profile) bereit, wenn kein bestimmter Materialkatalog an einem Vorgang beteiligt ist.

Damit der Render Server ordnungsgemäß funktioniert, muss die Katalogattributdatei für den Standardkatalog den Namen [!DNL default.ini] haben, muss immer im Katalogordner vorhanden sein und mit allen erforderlichen Attributen gefüllt sein, mit Ausnahme von `attribute::RootId` und den Verweisen auf die verschiedenen Katalogdatendateien, die alle optional sind.

**Verwandte Themen**

`PlatformServer::ir.catalogRootPath`
