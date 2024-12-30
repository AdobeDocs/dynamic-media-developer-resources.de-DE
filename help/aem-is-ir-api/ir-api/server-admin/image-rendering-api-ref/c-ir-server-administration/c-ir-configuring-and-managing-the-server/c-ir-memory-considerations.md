---
description: Der für das Bild-Rendering verwendete Arbeitsspeicher kann stark variieren und hängt stark von der tatsächlichen Server-Last und -Nutzung ab (z. B. wenige im Vergleich zu vielen verschiedenen Vignetten, Größe und Komplexität von Vignetten usw.).
solution: Experience Manager
title: Überlegungen zum Arbeitsspeicher
feature: Dynamic Media Classic,SDK/API
role: Developer,Admin,User
exl-id: 62eaa41c-a61c-4bcd-8dd9-9c3423bf82ef
source-git-commit: 38afaf2ed0f01868f02e236e941b23eed5b790aa
workflow-type: tm+mt
source-wordcount: '129'
ht-degree: 0%

---

# Überlegungen zum Arbeitsspeicher{#memory-considerations}

Der für das Bild-Rendering verwendete Arbeitsspeicher kann stark variieren und hängt stark von der tatsächlichen Server-Last und -Nutzung ab (z. B. wenige im Vergleich zu vielen verschiedenen Vignetten, Größe und Komplexität von Vignetten usw.).

Um eine optimale Leistung zu erzielen, sollte das Auslagern des Arbeitsspeichers (Austauschen) vermieden werden.

Beim Rendern von Bildern wird die Speicherverwaltung des Bild-Servers gemeinsam genutzt. Bei Verwendung des Bild-Renderings sollte zusätzlicher Speicher zugewiesen werden. 30 bis 50 % des physischen Speichers können angemessen sein.

Informationen zum Ändern der Speicherzuweisung für den Image-Server (ImageServer::PhysicalMemory) finden Sie in der Image-Serving-Dokumentation .
