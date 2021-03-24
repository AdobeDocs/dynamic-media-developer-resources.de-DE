---
description: Bildkataloge werden verwendet, um Informationen über Bilder und unterstützende Daten (z. B. Schriftarten und ICC-Profile) für den Server bereitzustellen.
solution: Experience Manager
title: Überblick
feature: Dynamic Media Classic, SDK/API
role: Entwickler, Geschäftspraktiker
translation-type: tm+mt
source-git-commit: f6c97606d7a4209427316d7367013ad9585a5cae
workflow-type: tm+mt
source-wordcount: '285'
ht-degree: 0%

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

In diesem Dokument wird das Dateiformat des Bildkatalogs für das Dynamic Media Image Serving-System beschrieben. Die beabsichtigte Audience sind erfahrene Programmierer und Website-Entwickler, die Dynamic Media Image Serving für eine Web- oder benutzerdefinierte Anwendung nutzen möchten.

Es wird davon ausgegangen, dass der Leser im Allgemeinen mit dem Dynamic Media Image Serving-System, den allgemeinen Standards und Konventionen des HTTP-Protokolls und der grundlegenden Terminologie der Bildbearbeitung vertraut ist.
