---
title: Systemanforderungen und Voraussetzungen
description: Bevor Sie Dynamic Media Image Serving verwenden, stellen Sie sicher, dass Ihr System die Systemanforderungen erfüllt.
solution: Experience Manager
feature: Dynamic Media Classic,SDK/API
role: Developer,User
exl-id: ea2dfec9-0a42-4ccb-8442-6f7c4a39eda1
source-git-commit: 163ac6a6f44193f1b66ae24059630521d7247eae
workflow-type: tm+mt
source-wordcount: '379'
ht-degree: 0%

---

# Systemanforderungen und Voraussetzungen{#system-requirements-and-prerequisites}

Bevor Sie Dynamic Media Image Serving verwenden, stellen Sie sicher, dass Ihr System die Systemanforderungen erfüllt.

## Serverhardware {#section-f3c14a7bc1b745118602659628df779f}

Ihr Server sollte die folgenden Hardwareanforderungen erfüllen.

>[!NOTE]
>
>Systeme mit Prozessoren mit AMD64 und Intel® EM64T werden normalerweise als NUMA-Plattformen (Non-Uniform Memory Architecture) konfiguriert. Dies bedeutet, dass der Kernel mehrere Speicherknoten beim Booten erstellt, anstatt einen einzelnen Speicherknoten zu erstellen. Das Konstrukt mit mehreren Knoten kann zu einer Speichererschöpfung auf einem oder mehreren Knoten führen, bevor andere Knoten erschöpft sind. Wenn die Speichererschöpfung eintritt, kann der Kernel entscheiden, Prozesse abzubrechen (z. B. der Image-Server oder [!DNL Platform Server]), obwohl verfügbarer Speicher vorhanden ist. Daher empfiehlt Adobe, dass Sie NUMA deaktivieren, wenn Sie ein solches System ausführen. Verwenden Sie die `numa=off` start -Option, um zu vermeiden, dass der Kernel diese Prozesse stoppt.

**Windows**

* Intel Xeon® oder AMD® Opteron-CPU mit mindestens vier Kernen.
* Mindestens 1 GB RAM.
* Der Swap-Speicherplatz entspricht mindestens dem doppelten Speicher (RAM).
* 2 GB verfügbarer Festplattenspeicher für die Installation und den grundlegenden Betrieb, zusätzlicher Speicherplatz für Quellbilder, Protokolle, Daten-Caches und Manifestdateien.
* Fast-Ethernet-Netzwerkkarte.

**Linux®**

* Intel Xeon® oder AMD® Opteron-CPU mit mindestens vier Kernen.
* Mindestens 16 GB RAM.
* Swapping deaktiviert (empfohlen).
* 2 GB verfügbarer Festplattenspeicher für die Installation und den grundlegenden Betrieb, zusätzlicher Speicherplatz für Quellbilder, Protokolle, Daten-Caches und Manifestdateien.
* Fast-Ethernet-Netzwerkkarte.

**Hinweis (Linux®):** Image Serving funktioniert nicht, wenn SELinux aktiviert ist. Diese Option ist standardmäßig aktiviert. Um SELinux zu deaktivieren, bearbeiten Sie die [!DNL /etc/selinux/config] und ändern Sie den SELinux-Wert von:

`SELINUX=enforcing`

nach

`SELINUX=disabled`

**Hinweis (Linux®):** Stellen Sie sicher, dass der Hostname des Servers in eine IP-Adresse aufgelöst werden kann. Wenn dies nicht möglich ist, fügen Sie den vollständig qualifizierten Hostnamen und die IP-Adresse zu [!DNL /etc/hosts] wie im folgenden Beispiel gezeigt.

`<ip address> <fully qualified hostname>`

## Server-Software {#section-5c9aad2e6b8a4bca989e17a2c8476fc4}

Dynamic Media Image Serving erfordert die folgende Serversoftware.

**Windows**

* Microsoft® Windows Server 2008.
* 64-Bit-Betriebssystem.

**Linux®**

* Red Hat® Enterprise 5 oder CentOS 5.5 und höher mit den neuesten Fix-Patches.
* 64-Bit-Betriebssystem.

**Hinweis:** Um Image Serving unter Windows zu verwenden, müssen Sie Microsoft® Visual Studio 2010 installieren.
