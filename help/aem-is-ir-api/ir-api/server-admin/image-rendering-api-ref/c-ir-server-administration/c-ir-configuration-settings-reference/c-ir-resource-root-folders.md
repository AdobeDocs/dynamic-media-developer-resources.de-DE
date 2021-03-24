---
description: Die Liste von Pfaden, die durch Semikolons getrennt sind, dient als Grundlage für alle Datendateien mit relativen Dateipfaden.
solution: Experience Manager
title: Ressourcenstammordner (ir.resourceRootPaths)
feature: Dynamic Media Classic, SDK/API
role: Entwickler, Administrator, Business Practitioner
translation-type: tm+mt
source-git-commit: d0bc88f55f857762b3bab4c76d1e3f3dd2733d60
workflow-type: tm+mt
source-wordcount: '88'
ht-degree: 0%

---


# Ressourcenstammordner (ir.resourceRootPaths){#resource-root-folders-ir-resourcerootpaths}

Die Liste von Pfaden, die durch Semikolons getrennt sind, dient als Grundlage für alle Datendateien mit relativen Dateipfaden.

Kann entweder absolute Pfade oder Pfade relativ zu *[!DNL install_folder]* sein. Wenn mehrere Pfade angegeben sind, versucht der Server jeden Stamm in der angegebenen Reihenfolge, bis die Datei gefunden wurde. Der Standardwert ist [!DNL ./resources] für einen Standard-Stammpfad von [!DNL install_folder/resources].
