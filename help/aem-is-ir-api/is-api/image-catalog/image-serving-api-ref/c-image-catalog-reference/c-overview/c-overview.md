---
description: Bildkataloge werden verwendet, um Informationen über Bilder und unterstützende Daten (wie Schriftarten und ICC-Profile) für den Server bereitzustellen.
solution: Experience Manager
title: Überblick
feature: Dynamic Media Classic,SDK/API
role: Developer,User
exl-id: 36cdd833-6fcb-4be6-a4f8-ba8d20580f29
source-git-commit: 206e4643e3926cb85b4be2189743578f88180be7
workflow-type: tm+mt
source-wordcount: '282'
ht-degree: 0%

---

# Überblick{#overview}

Bildkataloge werden verwendet, um Informationen über Bilder und unterstützende Daten (wie Schriftarten und ICC-Profile) für den Server bereitzustellen.

Bildkataloge werden verwendet, um Informationen über Bilder und unterstützende Daten (wie Schriftarten und ICC-Profile) für den Server bereitzustellen.

Jeder Bildkatalog besteht aus einer erforderlichen Katalogattributdatei und einer Reihe optionaler Katalogdatendateien:

* Die Bilddatendatei, in der Bilder und Vorlagen sowie die zugehörigen Metadaten itemisiert werden.
* Die SVG-Datendatei, die SVG-Dateien und die zugehörigen Metadaten auflistet.
* Die Makro-Definitionsdatei, die Definitionen für Anforderungsmakros bereitstellt.
* Die Schriftzuordnungsdatei, die die Textschriftarten verfolgt.
* Die Profilzuordnungsdatei, die ICC-Farbprofile auflistet.
* Die Regelsatzdatei, die die Vorverarbeitungsregeln für HTTP-Anforderungen definiert.

Katalogdatendateien sind Bildkatalogen nach Dateiverweisen in der Katalogattributdatei zugeordnet. Dieselbe Katalogdatendatei kann für mehrere Bildkataloge freigegeben werden.

Katalogattributdateien müssen das Suffix [!DNL .ini] aufweisen und sich im Katalogordner des Platform-Servers ( `PlatformServer::catalog.rootPath`) befinden. Katalogdatendateien können sich im selben Ordner oder in einem anderen Ordner befinden, auf den der Platform-Server zugreifen kann.

In diesem Dokument wird das Bildkatalog-Dateiformat für das Dynamic Media Image Serving-System beschrieben. Die Zielgruppe sind erfahrene Programmierer und Website-Entwickler, die Dynamic Media Image Serving für eine Web- oder benutzerdefinierte Anwendung nutzen möchten.

Es wird davon ausgegangen, dass der Leser im Allgemeinen mit dem Dynamic Media Image Serving-System, allgemeinen HTTP-Protokollstandards und -Konventionen sowie der grundlegenden Imaging-Terminologie vertraut ist.
