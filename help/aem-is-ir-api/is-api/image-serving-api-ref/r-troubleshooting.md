---
description: In diesem Abschnitt finden Sie Lösungen zu Problemen, die gelegentlich bei der Bereitstellung von Bildern aufgetreten sind.
solution: Experience Manager
title: Fehlerbehebung
feature: Dynamic Media Classic,SDK/API
role: Developer,User
exl-id: b80d3c9a-a0c4-4944-9f91-e791a072cd5f
source-git-commit: 4f81f755789613222a66bed2961117604ae19e62
workflow-type: tm+mt
source-wordcount: '522'
ht-degree: 0%

---

# Fehlerbehebung{#troubleshooting}

In diesem Abschnitt finden Sie Lösungen zu Problemen, die gelegentlich bei der Bereitstellung von Bildern aufgetreten sind.

**Allgemein**

ImageServer führt jetzt ein Installationsprotokoll und einen Backup-Ordner aller Dateien, die während einer Upgrade-Installation geändert wurden. Diese Datei und dieser Ordner befinden sich möglicherweise im Stammverzeichnis des Image-Serving-Installationsverzeichnisses.

**Beim Starten des Image-Servers wird das Startskript mit der Meldung „Start ausstehend“ angehalten (nur LINUX)**

Dies kann auf ein Problem mit der Image-Serving-Lizenz hinweisen, z. B. auf eine fehlende Lizenzdatei oder eine abgelaufene temporäre Lizenz. In [!DNL /usr/local/scene7/licenses] muss sich eine gültige Lizenzdatei befinden.

**Image-Server stürzt ab oder wird angehalten, und die Image-Server-Protokolldatei zeigt an, dass nicht genügend Speicherplatz vorhanden ist oder „Ressource in Datei [!DNL IgcVirtualMemory.cpp] vorübergehend nicht verfügbar ist“**

Der Grund für diese Fehlermeldung ist, dass der Image-Server die Menge an Speicher, für die er konfiguriert wurde, nicht zuordnen konnte.

* Überprüfen Sie die Einstellung des physischen Speichers in [!DNL ImageServerRegistry.xml]. Es sollte nicht mehr als 50 % betragen, weniger, wenn andere speicherintensive Anwendungen auf demselben System ausgeführt werden. Der Standardwert lautet 20 %.
* Stellen Sie sicher, dass der Auslagerungsspeicher auf dem Server mindestens doppelt so groß ist wie der physische RAM. Niedrige Swap-Einstellungen können dieses Problem verursachen.

**Der tatsächliche Speicherplatz, der vom Cache-Ordner belegt wird, überschreitet ` *[!DNL cache.maxSize]*`in festgelegt[!DNL PlatformServer.conf]**

Dies weist nicht auf ein Problem hin. Der Dateisystemmehraufwand ist nicht in der Einstellung für den Datenträger-Cache des [!DNL Platform Server] enthalten. Die vom System gemeldete Gesamtmenge kann erheblich größer sein als die Einstellung. Es wird empfohlen, doppelt so viel Festplattenspeicher zu reservieren, wie in ` *[!DNL cache.maxSize]*` angegeben ist.

**Beschädigte Bilder in den Beispielen für is-docs**

Dies tritt auf, wenn der Bildserver nicht ausgeführt wird. Es tritt auch auf, wenn der Katalogstammpfad oder Bildstammpfad gegenüber der standardmäßigen -Installation geändert wurde, die Beispielbilder und -kataloge jedoch nicht an die neuen Speicherorte verschoben wurden. Überprüfen Sie den Wert für „Image-Server-Stammpfad“ in den Konfigurationsdateien. Verschieben Sie bei Bedarf den Demoordner mit den Beispielbildern in den aktuellen Bildstamm und verschieben Sie [!DNL sample*.*] in den aktuellen Katalogstamm.

In den Beispielen wird außerdem davon ausgegangen, dass bestimmte Einstellungen in [!DNL default.ini] standardmäßig sind (z. B. darf die Verschleierung oder Sperrung nicht aktiviert sein).

**Zu viele Cache-Fehler nach erheblicher Betriebszeit**

Je nach Server-Nutzung kann die Leistung durch Vergrößerung [!DNL Platform Server] Festplatten-Cache verbessert werden, wenn Speicherplatz verfügbar ist. Einstellungen können durch manuelles Bearbeiten von Konfigurationsdateien geändert werden. Siehe die Dokumentation.

**Protokolldateien beanspruchen zu viel Speicherplatz**

Der Bild-Server und [!DNL Platform Server] starten jeden Tag eine neue Protokolldatei. Diese werden standardmäßig in [!DNL *[!DNL install_root]*/ImageServing/logs] abgelegt. Die Größe der Protokolldatei, die Anzahl der gespeicherten Protokolle und der Protokollinhalt können konfiguriert werden. Siehe die Dokumentation.

**Wenn auf Ihrem Server Antiviren-Software installiert ist**

Es wird empfohlen, die Suche nach Image-Serving-Verzeichnissen zu deaktivieren. Andernfalls kann das Scannen von Lese-/Schreibordnern mit hohem Volumen (z. B. Cache, Bilder, Schriftarten, Profile und Katalogverzeichnisse) Probleme verursachen.

**Digimarc verursacht Leistungsprobleme bei Zoom-Bildern**

Verwenden Sie Digimarc nicht für gezoomte Bilder. Die Leistung ist nicht akzeptabel. Erstellen Sie ggf. einen separaten Katalog für Bilder, die zum Zoomen verwendet werden sollen, und deaktivieren Sie Digimarc für diesen Katalog.
