---
description: Der vom Image Rendering verwendete Speicher kann stark variieren und hängt stark von der tatsächlichen Auslastung und Nutzung des Servers ab (z. B. wenige bzw. viele verschiedene Vignetten, Größe und Komplexität von Vignetten usw.).
solution: Experience Manager
title: Überlegungen zum Speicher
feature: Dynamic Media Classic,SDK/API
role: Developer,Admin,User
exl-id: 62eaa41c-a61c-4bcd-8dd9-9c3423bf82ef
source-git-commit: 38afaf2ed0f01868f02e236e941b23eed5b790aa
workflow-type: tm+mt
source-wordcount: '132'
ht-degree: 0%

---

# Überlegungen zum Speicher{#memory-considerations}

Der vom Image Rendering verwendete Speicher kann stark variieren und hängt stark von der tatsächlichen Auslastung und Nutzung des Servers ab (z. B. wenige bzw. viele verschiedene Vignetten, Größe und Komplexität von Vignetten usw.).

Um eine optimale Leistung zu erzielen, sollte das Paging (Austauschen) des Speichers vermieden werden.

Das Bild-Rendering nutzt die Speicherverwaltung des Image-Servers. Bei Verwendung des Bild-Renderings sollte zusätzlicher Arbeitsspeicher zugewiesen werden. 30 bis 50% des physischen Speichers können vernünftig sein.

Informationen zum Ändern der Speicherzuordnung für den Image-Server (ImageServer::PhysicalMemory) finden Sie in der Dokumentation zum Image-Serving .
