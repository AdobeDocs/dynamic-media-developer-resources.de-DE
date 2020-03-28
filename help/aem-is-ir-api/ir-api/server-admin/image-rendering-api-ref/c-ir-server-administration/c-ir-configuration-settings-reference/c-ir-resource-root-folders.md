---
description: Die Liste von Pfaden, die durch Semikolons getrennt sind, dient als Grundlage für alle Datendateien mit relativen Dateipfaden.
seo-description: Die Liste von Pfaden, die durch Semikolons getrennt sind, dient als Grundlage für alle Datendateien mit relativen Dateipfaden.
seo-title: Ressourcenstammordner (ir.resourceRootPaths)
solution: Experience Manager
title: Ressourcenstammordner (ir.resourceRootPaths)
topic: Scene7 Image Serving - Image Rendering API
uuid: a2a8ecd1-ddfe-46c5-bb70-4640e0992de8
translation-type: tm+mt
source-git-commit: 7bc7b3a86fbcdc57cfdc31745fae3afc06e44b15

---


# Ressourcenstammordner (ir.resourceRootPaths){#resource-root-folders-ir-resourcerootpaths}

Die Liste von Pfaden, die durch Semikolons getrennt sind, dient als Grundlage für alle Datendateien mit relativen Dateipfaden.

Kann entweder absolute Pfade oder Pfade relativ zu [!DNL *[!DNL install_folder]*] sein. Wenn mehrere Pfade angegeben sind, versucht der Server jeden Stamm in der angegebenen Reihenfolge, bis die Datei gefunden wurde. Die Standardeinstellung ist [!DNL ./ resources], für einen Standard-Stammpfad von [!DNL *[!DNL install_folder]*/resources].
