---
description: Es gibt zwei Möglichkeiten, Image Serving unter Linux zu starten oder zu beenden.
seo-description: Es gibt zwei Möglichkeiten, Image Serving unter Linux zu starten oder zu beenden.
seo-title: Starten oder Beenden unter Linux
solution: Experience Manager
title: Starten oder Beenden unter Linux
topic: Scene7 Image Serving - Image Rendering API
uuid: 92cf60c4-3f80-42bc-b135-17bc22ba151e
translation-type: tm+mt
source-git-commit: 7bc7b3a86fbcdc57cfdc31745fae3afc06e44b15
workflow-type: tm+mt
source-wordcount: '76'
ht-degree: 0%

---


# Starten oder Beenden unter Linux{#starting-or-stopping-on-linux}

Es gibt zwei Möglichkeiten, Image Serving unter Linux zu starten oder zu beenden.

* Das Skript zum Beginn, Beenden und Überprüfen des Status des Image-Servers befindet sich im Ordner [!DNL ImageServing/bin]:

   `ImageServing.sh {start|stop|restart|status}`
* Die folgende Alternative sollte Systemadministratoren kennen:

   `/sbin/service ImageServing {start|stop|status}`
