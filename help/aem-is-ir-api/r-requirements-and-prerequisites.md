---
title: Systemanforderungen und Voraussetzungen
description: Stellen Sie vor der Verwendung von Dynamic Media-Bildbereitstellung sicher, dass Ihr System die Systemanforderungen erfüllt.
solution: Experience Manager
feature: Dynamic Media Classic,SDK/API
role: Developer,User
exl-id: ea2dfec9-0a42-4ccb-8442-6f7c4a39eda1
source-git-commit: 163ac6a6f44193f1b66ae24059630521d7247eae
workflow-type: tm+mt
source-wordcount: '382'
ht-degree: 0%

---

# Systemanforderungen und Voraussetzungen{#system-requirements-and-prerequisites}

Stellen Sie vor der Verwendung von Dynamic Media-Bildbereitstellung sicher, dass Ihr System die Systemanforderungen erfüllt.

## Serverhardware {#section-f3c14a7bc1b745118602659628df779f}

Ihr Server sollte die folgenden Hardware-Anforderungen erfüllen.

>[!NOTE]
>
>Systeme mit Prozessoren mit AMD64 und Intel® EM64T sind normalerweise als NUMA-Plattformen (Non-Uniform Memory Architecture) konfiguriert. Das bedeutet, dass der Kernel beim Booten mehrere Speicherknoten erstellt, anstatt einen einzelnen Speicherknoten zu erstellen. Das Konstrukt mit mehreren Knoten kann zu einer Speichererschöpfung auf einem oder mehreren Knoten führen, bevor andere Knoten erschöpft sind. Wenn die Speichererschöpfung eintritt, kann der Kernel Prozesse abbrechen (z. B. den Image-Server oder [!DNL Platform Server]), obwohl verfügbarer Speicher vorhanden ist. Daher empfiehlt Adobe, NUMA zu deaktivieren, wenn Sie ein solches System ausführen. Verwenden Sie die `numa=off` Start-Option, um zu vermeiden, dass der Kernel diese Prozesse stoppt.

**Windows**

* Intel Xeon® oder AMD® Opteron CPU mit mindestens vier Kernen.
* Mindestens 1 GB RAM.
* Der Auslagerungsspeicher beträgt mindestens das Doppelte des physischen Speichers (RAM).
* 2 GB verfügbarer Festplattenspeicher für die Installation und den grundlegenden Betrieb. Für Quellbilder, Protokolle, Daten-Caches und Manifestdateien ist zusätzlicher Festplattenspeicher erforderlich.
* Fast Ethernet-Netzwerkkarte.

**Linux®**

* Intel Xeon® oder AMD® Opteron CPU mit mindestens vier Kernen.
* Mindestens 16 GB RAM.
* Austausch deaktiviert (empfohlen).
* 2 GB verfügbarer Festplattenspeicher für die Installation und den grundlegenden Betrieb. Für Quellbilder, Protokolle, Daten-Caches und Manifestdateien ist zusätzlicher Festplattenspeicher erforderlich.
* Fast Ethernet-Netzwerkkarte.

**Hinweis (Linux®):** Bildbereitstellung funktioniert nicht, wenn SELinux aktiviert ist. Diese Option ist standardmäßig aktiviert. Um SELinux zu deaktivieren, bearbeiten Sie die [!DNL /etc/selinux/config] und ändern Sie den SELinux-Wert von:

`SELINUX=enforcing`

bis

`SELINUX=disabled`

**Hinweis (Linux®):** Stellen Sie sicher, dass der Hostname des Servers in eine IP-Adresse aufgelöst werden kann. Wenn dies nicht möglich ist, fügen Sie den vollqualifizierten Hostnamen und die IP-Adresse [!DNL /etc/hosts] hinzu, wie im folgenden Beispiel gezeigt.

`<ip address> <fully qualified hostname>`

## Serversoftware {#section-5c9aad2e6b8a4bca989e17a2c8476fc4}

Für die Dynamic Media-Bildbereitstellung ist die folgende Serversoftware erforderlich.

**Windows**

* Microsoft® Windows Server 2008.
* 64-Bit-Betriebssystem.

**Linux®**

* Red Hat® Enterprise 5 oder CentOS 5.5 und höher mit den neuesten Fehlerbehebungen.
* 64-Bit-Betriebssystem.

**Hinweis** Um Image Serving unter Windows zu verwenden, müssen Sie Microsoft® Visual Studio 2010 installieren.
