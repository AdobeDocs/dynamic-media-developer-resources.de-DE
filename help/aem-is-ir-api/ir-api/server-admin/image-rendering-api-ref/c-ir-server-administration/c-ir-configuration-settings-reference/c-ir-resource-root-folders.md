---
title: Ressourcen-Stammordner (ir.resourceRootPaths)
description: Eine Liste von Pfaden, durch Semikolons getrennt, dient als Stamm für alle Datendateien mit relativen Dateipfaden.
solution: Experience Manager
feature: Dynamic Media Classic,SDK/API
role: Developer,Admin,User
exl-id: 49fd45da-1af9-4016-8fc6-6ec17b7e553b
source-git-commit: 6a4c1f4425199cfa6088fc42137552748c1a9dcf
workflow-type: tm+mt
source-wordcount: '82'
ht-degree: 0%

---

# Ressourcen-Stammordner (ir.resourceRootPaths){#resource-root-folders-ir-resourcerootpaths}

Eine Liste von Pfaden, durch Semikolons getrennt, dient als Stamm für alle Datendateien mit relativen Dateipfaden.

Es kann sich entweder um absolute Pfade oder um Pfade relativ zu *[!DNL install_folder]* handeln. Wenn mehrere Pfade angegeben sind, versucht der Server jeden Stamm in der angegebenen Reihenfolge, bis die Datei gefunden wird. Der Standardwert lautet [!DNL ./resources] für einen standardmäßigen Stammpfad von [!DNL install_folder/resources].
