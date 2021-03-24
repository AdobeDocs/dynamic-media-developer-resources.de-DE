---
description: Es gibt zwei Möglichkeiten, Image Serving unter Linux zu starten oder zu beenden.
solution: Experience Manager
title: Starten oder Beenden unter Linux
feature: Dynamic Media Classic, SDK/API
role: Entwickler, Geschäftspraktiker
translation-type: tm+mt
source-git-commit: f6c97606d7a4209427316d7367013ad9585a5cae
workflow-type: tm+mt
source-wordcount: '67'
ht-degree: 0%

---


# Starten oder Beenden unter Linux{#starting-or-stopping-on-linux}

Es gibt zwei Möglichkeiten, Image Serving unter Linux zu starten oder zu beenden.

* Das Skript zum Beginn, Beenden und Überprüfen des Status des Image-Servers befindet sich im Ordner [!DNL ImageServing/bin]:

   `ImageServing.sh {start|stop|restart|status}`
* Die folgende Alternative sollte Systemadministratoren kennen:

   `/sbin/service ImageServing {start|stop|status}`
