---
description: Es gibt zwei Möglichkeiten, Image Serving unter Linux zu starten oder zu beenden.
solution: Experience Manager
title: Starten oder Beenden unter Linux
feature: Dynamic Media Classic,SDK/API
role: Developer,User
exl-id: eb4c60b2-5491-40e9-b105-d4b05006a9ca
source-git-commit: 206e4643e3926cb85b4be2189743578f88180be7
workflow-type: tm+mt
source-wordcount: '64'
ht-degree: 0%

---

# Starten oder Beenden unter Linux{#starting-or-stopping-on-linux}

Es gibt zwei Möglichkeiten, Image Serving unter Linux zu starten oder zu beenden.

* Das Skript zum Starten, Stoppen und Überprüfen des Status von Image Serving befindet sich im Ordner [!DNL ImageServing/bin] :

   `ImageServing.sh {start|stop|restart|status}`
* Die folgende Alternative sollte Systemadministratoren kennen:

   `/sbin/service ImageServing {start|stop|status}`
