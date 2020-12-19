---
description: Die Liste von Pfaden, die durch Semikolons getrennt sind, dient als Grundlage für alle Datendateien mit relativen Dateipfaden.
seo-description: Die Liste von Pfaden, die durch Semikolons getrennt sind, dient als Grundlage für alle Datendateien mit relativen Dateipfaden.
seo-title: Ressourcenstammordner (ir.resourceRootPaths)
solution: Experience Manager
title: Ressourcenstammordner (ir.resourceRootPaths)
topic: Scene7 Image Serving - Image Rendering API
uuid: a2a8ecd1-ddfe-46c5-bb70-4640e0992de8
translation-type: tm+mt
source-git-commit: 2bc6fe0369808990642cf7afdccff647c48260d9
workflow-type: tm+mt
source-wordcount: '100'
ht-degree: 0%

---


# Ressourcenstammordner (ir.resourceRootPaths){#resource-root-folders-ir-resourcerootpaths}

Die Liste von Pfaden, die durch Semikolons getrennt sind, dient als Grundlage für alle Datendateien mit relativen Dateipfaden.

Kann entweder absolute Pfade oder Pfade relativ zu *[!DNL install_folder]* sein. Wenn mehrere Pfade angegeben sind, versucht der Server jeden Stamm in der angegebenen Reihenfolge, bis die Datei gefunden wurde. Der Standardwert ist [!DNL ./resources] für einen Standard-Stammpfad von [!DNL install_folder/resources].
