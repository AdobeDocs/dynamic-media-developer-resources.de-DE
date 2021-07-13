---
description: Regelsatzdateien sind XML-formatierte Textdateien und müssen den entsprechenden Standards und Konventionen entsprechen.
solution: Experience Manager
title: Regelsatzdateien
feature: Dynamic Media Classic,SDK/API
role: Developer,User
exl-id: 7f3d700f-1941-4220-b91d-54e78fae6aaf
source-git-commit: 206e4643e3926cb85b4be2189743578f88180be7
workflow-type: tm+mt
source-wordcount: '81'
ht-degree: 0%

---

# Regelsatzdateien{#rule-set-files}

Regelsatzdateien sind XML-formatierte Textdateien und müssen den entsprechenden Standards und Konventionen entsprechen.

[!DNL RuleSet.xsd] ist im Standardkatalogordner installiert und sollte verwendet werden, um Regelsatzdateien zu validieren, bevor sie an Image Serving gesendet werden. Es wird striktes Parsen angewendet und Regelsatzdateien, die nicht [!DNL RuleSet.xsd] entsprechen, werden nicht geladen.
