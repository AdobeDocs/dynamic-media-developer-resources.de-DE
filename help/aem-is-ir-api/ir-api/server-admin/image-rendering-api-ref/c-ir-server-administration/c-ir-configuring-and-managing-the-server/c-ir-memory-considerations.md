---
description: Der beim Image Rendering verwendete Arbeitsspeicher kann stark variieren und hängt stark von der tatsächlichen Serverlast und -nutzung ab (z. B. wenige bzw. viele verschiedene Vignetten, Größe und Komplexität der Vignetten usw.).
solution: Experience Manager
title: Überlegungen zum Speicher
feature: Dynamic Media Classic, SDK/API
role: Entwickler, Administrator, Business Practitioner
translation-type: tm+mt
source-git-commit: d0bc88f55f857762b3bab4c76d1e3f3dd2733d60
workflow-type: tm+mt
source-wordcount: '136'
ht-degree: 0%

---


# Überlegungen zum Speicher{#memory-considerations}

Der beim Image Rendering verwendete Arbeitsspeicher kann stark variieren und hängt stark von der tatsächlichen Serverlast und -nutzung ab (z. B. wenige bzw. viele verschiedene Vignetten, Größe und Komplexität der Vignetten usw.).

Um eine optimale Leistung zu erzielen, sollten Speicherkarten (Austauschen) vermieden werden.

Image Rendering nutzt die Speicherverwaltung des Image-Servers. Bei Verwendung des Image Rendering sollte zusätzlicher Arbeitsspeicher zugewiesen werden. 30 bis 50 % des physischen Speichers können angemessen sein.

Informationen zum Ändern der Speicherzuordnung für den Image-Server (ImageServer::PhysicalMemory) finden Sie in der Dokumentation zum Image-Server.
