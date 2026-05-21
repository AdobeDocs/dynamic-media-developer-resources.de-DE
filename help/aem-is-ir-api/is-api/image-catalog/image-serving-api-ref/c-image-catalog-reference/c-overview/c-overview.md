---
description: Bildkataloge werden verwendet, um dem Server Informationen über Bilder und unterstützende Daten (wie Schriftarten und ICC-Profile) bereitzustellen.
solution: Experience Manager
title: Überblick
feature: Dynamic Media Classic,SDK/API
role: Developer,User
exl-id: 36cdd833-6fcb-4be6-a4f8-ba8d20580f29
TQID: 'https://experienceleague.adobe.com/RFHaFaMFjOo2Igk-pQRXrQSCtSMmVCWarO6wu0mv4g8'
product_v2: id: fd1f54a9-f50c-467d-8956-cebbaf4f3eb8
feature_v2: id: a01bfd36-4ab8-4bf8-9dc0-5b45b890552e
role_v2: id: b69b2659-1057-424e-8fc5-ed9e016dc554id: ff6a42d2-313e-452e-93a6-792e4fad9ff8
topic_v2: id: a004cc84-67b9-4a33-a3a7-8ec7273ef4dc
source-git-commit: 2ff64206b7448a1a122696facd2669be68b6b9ff
workflow-type: tm+mt
source-wordcount: 275
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

In diesem Dokument wird das Bildkatalogdateiformat für das Dynamic Media-Bildbereitstellungssystem beschrieben. Die Zielgruppe sind erfahrene Programmierer und Website-Entwickler, die Dynamic Media Image Serving für ein Web- oder benutzerdefiniertes Programm nutzen möchten.

Es wird davon ausgegangen, dass der Leser im Allgemeinen mit dem Dynamic Media Image Serving-System, allgemeinen HTTP-Protokollstandards und -Konventionen und grundlegender Bildterminologie vertraut ist.
