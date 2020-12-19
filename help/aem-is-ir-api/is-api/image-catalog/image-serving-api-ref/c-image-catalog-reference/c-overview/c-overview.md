---
description: Bildkataloge werden verwendet, um Informationen über Bilder und unterstützende Daten (z. B. Schriftarten und ICC-Profile) für den Server bereitzustellen.
seo-description: Bildkataloge werden verwendet, um Informationen über Bilder und unterstützende Daten (z. B. Schriftarten und ICC-Profile) für den Server bereitzustellen.
seo-title: Überblick
solution: Experience Manager
title: Überblick
topic: Scene7 Image Serving - Image Rendering API
uuid: e8c0401b-9161-4624-babb-6c7afb443e65
translation-type: tm+mt
source-git-commit: 7bc7b3a86fbcdc57cfdc31745fae3afc06e44b15
workflow-type: tm+mt
source-wordcount: '296'
ht-degree: 1%

---


# Überblick{#overview}

Bildkataloge werden verwendet, um Informationen über Bilder und unterstützende Daten (z. B. Schriftarten und ICC-Profile) für den Server bereitzustellen.

Bildkataloge werden verwendet, um Informationen über Bilder und unterstützende Daten (z. B. Schriftarten und ICC-Profile) für den Server bereitzustellen.

Jeder Bildkatalog besteht aus einer erforderlichen Katalogattributdatei und einem Satz optionaler Katalogdatendateien:

* Die Bilddatendatei, in der Bilder und Vorlagen und die zugehörigen Metadaten itemisiert werden.
* Die SVG-Datendatei, die SVG-Dateien und die zugehörigen Metadaten itemisiert.
* Die Datei mit den Makrodefinitionen, die Definitionen für Anforderungsmakros bereitstellt.
* Die Schriftartzuordnungsdatei, die die Schriftarten verfolgt.
* Die Profil-Map-Datei, die ICC-Profile itemisiert.
* Die Regelsatzdatei, die die Regeln zur Vorverarbeitung einer HTTP-Anforderung definiert.

Katalogdatendateien werden nach Dateiverweisen in der Katalogattributdatei mit Bildkatalogen verknüpft. Die gleiche Katalogdatendatei kann für mehrere Bildkataloge freigegeben werden.

Katalogattributdateien müssen über ein [!DNL .ini]-Dateisuffix verfügen und sich im Katalogordner des Plattformservers ( `PlatformServer::catalog.rootPath`) befinden. Katalogdatendateien können sich im selben Ordner oder in einem anderen Ordner befinden, auf den der Plattformserver zugreifen kann.

In diesem Dokument wird das Dateiformat des Bildkatalogs für das Scene7 Image Serving-System beschrieben. Die beabsichtigte Audience sind erfahrene Programmierer und Website-Entwickler, die Scene7 Image Serving für eine Web- oder benutzerdefinierte Anwendung nutzen möchten.

Es wird davon ausgegangen, dass der Leser im Allgemeinen mit dem Scene7 Image Serving-System, den allgemeinen Standards und Konventionen des HTTP-Protokolls und der grundlegenden Terminologie der Bildbearbeitung vertraut ist.
