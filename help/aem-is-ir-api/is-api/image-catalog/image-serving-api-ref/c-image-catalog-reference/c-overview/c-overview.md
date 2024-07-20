---
description: Bildkataloge werden verwendet, um Informationen über Bilder und unterstützende Daten (wie Schriftarten und ICC-Profile) für den Server bereitzustellen.
solution: Experience Manager
title: Überblick
feature: Dynamic Media Classic,SDK/API
role: Developer,User
exl-id: 36cdd833-6fcb-4be6-a4f8-ba8d20580f29
source-git-commit: bf31e5226cbb763e2fb82391772b64e5d5c89fae
workflow-type: tm+mt
source-wordcount: '274'
ht-degree: 0%

---

# Überblick{#overview}

Bildkataloge werden verwendet, um Informationen über Bilder und unterstützende Daten (wie Schriftarten und ICC-Profile) für den Server bereitzustellen.

Bildkataloge werden verwendet, um Informationen über Bilder und unterstützende Daten (wie Schriftarten und ICC-Profile) für den Server bereitzustellen.

Jeder Bildkatalog besteht aus einer erforderlichen Katalogattributdatei und einer Reihe optionaler Katalogdatendateien:

* Die Bilddatendatei, in der Bilder und Vorlagen sowie die zugehörigen Metadaten itemisiert werden.
* Die SVG-Datendatei, die SVG-Dateien und die zugehörigen Metadaten auflistet.
* Die Makrodefinitionsdatei, die Definitionen für Anforderungsmakros bereitstellt.
* Die Schriftzuordnungsdatei, die die Textschriftarten verfolgt.
* Die Profilzuordnungsdatei, die ICC-Farbprofile auflistet.
* Die Regelsatzdatei, die die Vorverarbeitungsregeln für HTTP-Anforderungen definiert.

Katalogdatendateien sind Bildkatalogen nach Dateiverweisen in der Katalogattributdatei zugeordnet. Dieselbe Katalogdatendatei kann für mehrere Bildkataloge freigegeben werden.

Katalogattributdateien müssen das Suffix &quot;[!DNL .ini]&quot; aufweisen und sich im Katalogordner &quot;[!DNL Platform Server]&quot;( `PlatformServer::catalog.rootPath`) befinden. Katalogdatendateien können sich im selben Ordner oder in einem anderen Ordner befinden, auf den die [!DNL Platform Server] zugreifen kann.

In diesem Dokument wird das Bildkatalog-Dateiformat für das Dynamic Media Image Serving-System beschrieben. Die Zielgruppe sind erfahrene Programmierer und Website-Entwickler, die Dynamic Media Image Serving für eine Web- oder benutzerdefinierte Anwendung nutzen möchten.

Es wird davon ausgegangen, dass der Leser im Allgemeinen mit dem Dynamic Media Image Serving-System, allgemeinen HTTP-Protokollstandards und -Konventionen sowie der grundlegenden Imaging-Terminologie vertraut ist.
