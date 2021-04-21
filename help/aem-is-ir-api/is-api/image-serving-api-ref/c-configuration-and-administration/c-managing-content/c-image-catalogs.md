---
description: Bildkataloge bieten viele Serverkonfigurationseinstellungen sowie Schriftarten, ICC-Profile und Befehlsmakros.
solution: Experience Manager
title: Bildkataloge
feature: Dynamic Media Classic,SDK/API
role: Developer,Administrator,Business Practitioner
translation-type: tm+mt
source-git-commit: f6c97606d7a4209427316d7367013ad9585a5cae
workflow-type: tm+mt
source-wordcount: '126'
ht-degree: 0%

---


# Bildkataloge{#image-catalogs}

Bildkataloge bieten viele Serverkonfigurationseinstellungen sowie Schriftarten, ICC-Profile und Befehlsmakros.

Sie ordnen Bild- und statische Inhalts-IDs, die in Anforderungen verwendet werden, den tatsächlichen Dateipfaden zu, speichern verschiedene Bildmetadaten wie Imagemaps und bieten Container für Vorlagen und Bildsätze.

Auf Bildkataloge kann nur vom Plattformserver zugegriffen werden, nie vom Image-Server. Katalogattributdateien müssen das Suffix .ini haben und im Katalogordner des Plattformservers ( `PS::CatalogFolder`) abgelegt werden. Mindestens der Standardbildkatalog ist erforderlich und muss mit allen Attributen gefüllt werden, damit der Plattformserver ordnungsgemäß funktioniert.
