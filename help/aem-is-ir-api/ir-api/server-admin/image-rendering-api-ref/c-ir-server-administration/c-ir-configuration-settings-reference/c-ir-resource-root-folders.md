---
description: Die Liste der Pfade, getrennt durch Semikolons, dient als Wurzeln für alle Datendateien mit relativen Dateipfaden.
solution: Experience Manager
title: Ressourcen-Stammordner (ir.resourceRootPaths)
feature: Dynamic Media Classic,SDK/API
role: Developer,Administrator,User
exl-id: 49fd45da-1af9-4016-8fc6-6ec17b7e553b
source-git-commit: 206e4643e3926cb85b4be2189743578f88180be7
workflow-type: tm+mt
source-wordcount: '84'
ht-degree: 0%

---

# Ressourcen-Stammordner (ir.resourceRootPaths){#resource-root-folders-ir-resourcerootpaths}

Die Liste der Pfade, getrennt durch Semikolons, dient als Wurzeln für alle Datendateien mit relativen Dateipfaden.

Kann entweder absolute Pfade oder Pfade sein, die relativ zu *[!DNL install_folder]* sind. Wenn mehrere Pfade angegeben sind, versucht der Server jeden Stamm in der angegebenen Reihenfolge, bis die Datei gefunden wird. Der Standardwert ist [!DNL ./resources] für einen standardmäßigen Stammpfad von [!DNL install_folder/resources].
