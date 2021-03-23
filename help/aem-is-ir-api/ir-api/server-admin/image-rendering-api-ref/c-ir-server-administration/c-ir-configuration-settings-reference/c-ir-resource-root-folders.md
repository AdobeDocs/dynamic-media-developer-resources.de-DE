---
description: Die Liste von Pfaden, die durch Semikolons getrennt sind, dient als Grundlage für alle Datendateien mit relativen Dateipfaden.
seo-description: Die Liste von Pfaden, die durch Semikolons getrennt sind, dient als Grundlage für alle Datendateien mit relativen Dateipfaden.
seo-title: Ressourcenstammordner (ir.resourceRootPaths)
solution: Experience Manager
title: Ressourcenstammordner (ir.resourceRootPaths)
uuid: a2a8ecd1-ddfe-46c5-bb70-4640e0992de8
feature: Dynamic Media Classic, SDK/API
role: Entwickler, Administrator, Business Practitioner
translation-type: tm+mt
source-git-commit: 469d1a5c43a972116a8a2efb0de5708800130a99
workflow-type: tm+mt
source-wordcount: '109'
ht-degree: 0%

---


# Ressourcenstammordner (ir.resourceRootPaths){#resource-root-folders-ir-resourcerootpaths}

Die Liste von Pfaden, die durch Semikolons getrennt sind, dient als Grundlage für alle Datendateien mit relativen Dateipfaden.

Kann entweder absolute Pfade oder Pfade relativ zu *[!DNL install_folder]* sein. Wenn mehrere Pfade angegeben sind, versucht der Server jeden Stamm in der angegebenen Reihenfolge, bis die Datei gefunden wurde. Der Standardwert ist [!DNL ./resources] für einen Standard-Stammpfad von [!DNL install_folder/resources].
