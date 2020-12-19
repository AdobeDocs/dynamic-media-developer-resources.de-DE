---
description: Bevor Sie Scene7 Image Serving verwenden, stellen Sie sicher, dass Ihr System die Systemanforderungen erfüllt.
seo-description: Bevor Sie Scene7 Image Serving verwenden, stellen Sie sicher, dass Ihr System die Systemanforderungen erfüllt.
seo-title: Systemanforderungen und -voraussetzungen
solution: Experience Manager
title: Systemanforderungen und -voraussetzungen
topic: Scene7 Image Serving - Image Rendering API
uuid: 80196574-f5a2-4298-880a-cc36f90b6e21
translation-type: tm+mt
source-git-commit: e8e5b07329bde3e23ee095d5022da62d67e9478c
workflow-type: tm+mt
source-wordcount: '411'
ht-degree: 0%

---


# Systemanforderungen und Voraussetzungen{#system-requirements-and-prerequisites}

Bevor Sie Scene7 Image Serving verwenden, stellen Sie sicher, dass Ihr System die Systemanforderungen erfüllt.

## Server-Hardware {#section-f3c14a7bc1b745118602659628df779f}

Ihr Server sollte die folgenden Hardwareanforderungen erfüllen.

>[!NOTE]
>
>Systeme mit Prozessoren mit AMD64 und Intel® EM64T werden in der Regel als NUMA-Plattformen (Nicht-Uniform Memory Architecture) konfiguriert. Das bedeutet, dass der Kernel beim Booten mehrere Speicherknoten erstellt, anstatt einen einzelnen Speicherknoten zu erstellen. Das Mehrfach-Node-Konstrukt kann zu einer Speicherbelegung auf einem oder mehreren Knoten führen, bevor andere Knoten erschöpft werden. Wenn die Speicherbelegung eintritt, kann der Kernel selbst dann Prozesse abbrechen (z. B. Image Server oder Platform Server), wenn verfügbarer Speicher vorhanden ist. Daher empfiehlt Adobe Systems, dass Sie NUMA deaktivieren, wenn Sie ein solches System ausführen. Verwenden Sie die Option `numa=off` Beginn, um zu vermeiden, dass der Kernel diese Vorgänge stoppt.

**Windows**

* Intel Xeon® oder AMD® Opteron-CPU mit mindestens 4 Kernen.
* Mindestens 16 GB RAM.
* Swap-Raum, der mindestens doppelt so groß ist wie der physische Arbeitsspeicher (RAM).
* 2 GB freier Festplattenspeicher für die Installation und den einfachen Betrieb, zusätzlicher Speicherplatz für Quellbilder, Protokolle, Datencache und Manifestdateien erforderlich.
* Fast-Ethernet-Netzwerkschnittstellenkarte.

**Linux**

* Intel Xeon® oder AMD® Opteron-CPU mit mindestens 4 Kernen.
* Mindestens 16 GB RAM.
* Austausch deaktiviert (empfohlen).
* 2 GB freier Festplattenspeicher für die Installation und den einfachen Betrieb, zusätzlicher Speicherplatz für Quellbilder, Protokolle, Datencache und Manifestdateien erforderlich.
* Fast-Ethernet-Netzwerkschnittstellenkarte.

**Hinweis (Linux):** Image Serving funktioniert nicht mit aktiviertem SELinux. Diese Option ist standardmäßig aktiviert. Um SELinux zu deaktivieren, bearbeiten Sie die [!DNL /etc/selinux/config]-Datei und ändern Sie den SELinux-Wert von:

`SELINUX=enforcing`

in / zu

`SELINUX=disabled`

**Hinweis (Linux):** Stellen Sie sicher, dass der Hostname des Servers auf eine IP-Adresse aufgelöst werden kann. Wenn dies nicht möglich ist, fügen Sie den vollständig qualifizierten Hostnamen und die IP-Adresse zu [!DNL /etc/hosts] hinzu, wie im folgenden Beispiel.

`<ip address> <fully qualified hostname>`

## Server-Software {#section-5c9aad2e6b8a4bca989e17a2c8476fc4}

Für Scene7 Image Serving ist folgende Serversoftware erforderlich.

**Windows**

* Microsoft® Windows 2008 Server.
* 64-Bit-Betriebssystem.

**Linux**

* Red Hat® Enterprise 5 oder CentOS 5.5 und höher, mit neuesten Fix-Patches.
* 64-Bit-Betriebssystem.

**Hinweis:** Um Image Serving unter Windows verwenden zu können, müssen Sie Microsoft Visual Studio 2010 neu verteilen. Die Redistributable ist unter folgender Adresse verfügbar:

[http://www.microsoft.com/en-us/download/details.aspx?id=13523](http://www.microsoft.com/en-us/download/details.aspx?id=13523)

