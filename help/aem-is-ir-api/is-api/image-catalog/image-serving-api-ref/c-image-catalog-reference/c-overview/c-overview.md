---
description: Bildkataloge werden verwendet, um dem Server Informationen über Bilder und unterstützende Daten (wie Schriftarten und ICC-Profile) bereitzustellen.
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

Bildkataloge werden verwendet, um dem Server Informationen über Bilder und unterstützende Daten (wie Schriftarten und ICC-Profile) bereitzustellen.

Bildkataloge werden verwendet, um dem Server Informationen über Bilder und unterstützende Daten (wie Schriftarten und ICC-Profile) bereitzustellen.

Jeder Bildkatalog besteht aus einer erforderlichen Katalogattributdatei und einem Satz optionaler Katalogdatendateien:

* Die Bilddatendatei, in der Bilder und Vorlagen und die zugehörigen Metadaten aufgeführt sind.
* Die SVG-Datendatei, in der SVG-Dateien und die zugehörigen Metadaten aufgeführt sind.
* Die Datei mit den Makrodefinitionen, die Definitionen für Anforderungsmakros bereitstellt.
* Die Schriftzuordnungsdatei, in der Textschriftarten nachverfolgt werden.
* Die Profilzuordnungsdatei, in der ICC-Farbprofile aufgeführt sind.
* Die Regelsatzdatei, die Regeln zur Vorverarbeitung von HTTP-Anfragen definiert.

Katalogdatendateien werden über Dateiverweise in der Katalogattributdatei mit Bildkatalogen verknüpft. Dieselbe Katalogdatendatei kann von mehreren Bildkatalogen gemeinsam genutzt werden.

Katalogattributdateien müssen ein [!DNL .ini] Dateisuffix aufweisen und sich im Katalogordner des [!DNL Platform Server] befinden ( `PlatformServer::catalog.rootPath`). Katalogdatendateien können sich im selben Ordner oder in einem anderen Ordner befinden, auf den die [!DNL Platform Server] zugreifen kann.

In diesem Dokument wird das Dateiformat des Bildkatalogs für das Dynamic Media Image Serving-System beschrieben. Die Zielgruppe sind erfahrene Programmierer und Website-Entwickler, die Dynamic Media Image Serving für eine Web- oder benutzerdefinierte Anwendung nutzen möchten.

Es wird davon ausgegangen, dass der Leser im Allgemeinen mit dem Dynamic Media Image Serving-System, allgemeinen HTTP-Protokollstandards und -Konventionen und grundlegender Bildterminologie vertraut ist.
