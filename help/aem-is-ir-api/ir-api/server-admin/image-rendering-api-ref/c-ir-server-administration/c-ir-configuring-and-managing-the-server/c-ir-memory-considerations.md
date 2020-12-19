---
description: Der beim Image Rendering verwendete Arbeitsspeicher kann stark variieren und hängt stark von der tatsächlichen Serverlast und -nutzung ab (z. B. wenige bzw. viele verschiedene Vignetten, Größe und Komplexität der Vignetten usw.).
seo-description: Der beim Image Rendering verwendete Arbeitsspeicher kann stark variieren und hängt stark von der tatsächlichen Serverlast und -nutzung ab (z. B. wenige bzw. viele verschiedene Vignetten, Größe und Komplexität der Vignetten usw.).
seo-title: Überlegungen zum Speicher
solution: Experience Manager
title: Überlegungen zum Speicher
topic: Scene7 Image Serving - Image Rendering API
uuid: 21247081-ff27-4237-93da-5fc996417dfd
translation-type: tm+mt
source-git-commit: 7bc7b3a86fbcdc57cfdc31745fae3afc06e44b15
workflow-type: tm+mt
source-wordcount: '164'
ht-degree: 0%

---


# Überlegungen zum Speicher{#memory-considerations}

Der beim Image Rendering verwendete Arbeitsspeicher kann stark variieren und hängt stark von der tatsächlichen Serverlast und -nutzung ab (z. B. wenige bzw. viele verschiedene Vignetten, Größe und Komplexität der Vignetten usw.).

Um eine optimale Leistung zu erzielen, sollten Speicherkarten (Austauschen) vermieden werden.

Image Rendering nutzt die Speicherverwaltung des Image-Servers. Bei Verwendung des Image Rendering sollte zusätzlicher Arbeitsspeicher zugewiesen werden. 30 bis 50 % des physischen Speichers können angemessen sein.

Informationen zum Ändern der Speicherzuordnung für den Image-Server (ImageServer::PhysicalMemory) finden Sie in der Dokumentation zum Image-Server.
