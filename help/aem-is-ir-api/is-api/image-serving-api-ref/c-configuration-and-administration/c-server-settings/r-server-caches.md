---
description: Verwenden Sie diese Servereinstellungen für Server-Caches.
seo-description: Verwenden Sie diese Servereinstellungen für Server-Caches.
seo-title: Server-Cache
solution: Experience Manager
title: Server-Cache
topic: Scene7 Image Serving - Image Rendering API
uuid: 73745363-2011-453f-b7a0-96de4b44186d
translation-type: tm+mt
source-git-commit: 7bc7b3a86fbcdc57cfdc31745fae3afc06e44b15

---


# Server-Cache{#server-caches}

Verwenden Sie diese Servereinstellungen für Server-Caches.

## PS::cache.rootPaths - Cache-Datenordner {#section-f0aa808304d74ecdb0c3644f11906c53}

Die Stammordner für den Datenträgercache des Plattformservers. Ein oder mehrere absolute Dateipfade oder Pfade relativ zu *[!DNL install_folder]*(durch Semikolons (;) getrennt). Die Daten für den HTTP-Antwort-Cache werden gleichmäßig über alle angegebenen Ordner verteilt. Die Zwischenspeicher für die zusätzlichen Zwischenspeicher (kompilierte Bildkataloge und ausländische Bilddaten) befinden sich im primären Cache-Ordner (dem ersten Ordner in der Liste).

## PS::cache.maxSize - Cache-Größe der Antwortdaten {#section-ed2e1e7ba4bd4e13b77bb20c4cacddb4}

Die maximale Größe des HTTP-Antwort-Cache in Byte. Diese Einstellung begrenzt die Menge der tatsächlich zwischengespeicherten Daten; Der Dateisystemaufwand wird nicht berücksichtigt. (Siehe [Antwortdaten-Cache](../../../../is-api/image-serving-api-ref/c-configuration-and-administration/c-data-caches/c-response-data-cache.md#concept-81ea996c242441f2a69f7e9d9b3a29ca).) Wenn mehrere Cache-Datenordner angegeben sind, werden die Cachedaten gleichmäßig über alle Ordner verteilt. Der Wert von `cache.maxSize` in [!DNL PlatformServer.conf] Byte.

## PS::cache.maxEntries - Max. Einträge im Cache für Antwortdaten {#section-5603e327e90542a5b50aeeb27b080410}

Die Anzahl der Einträge, die für den Cache-Index für HTTP-Antworten im Arbeitsspeicher zugewiesen wurden.

>[!NOTE] {class=&quot;- topic/note &quot;
>
>Stellen Sie unter Linux sicher, dass genügend i-Nodes für die Cache-Partition zugeordnet sind, um zu vermeiden, dass i-Nodes ausgehen.

## IS::TempDirectory - Temporärer Ordner für Bildserver {#section-42ea1e7a68c444878f7245c5bbcb1672}

Der Image-Server muss gelegentlich Zwischendaten auf dem Datenträger speichern. Der Pfad kann absolut oder relativ zu *[!DNL install_folder]* sein.

>[!NOTE] {class=&quot;- topic/note &quot;
>
>Der neue Ordner muss erstellt werden, bevor diese Einstellung geändert werden kann. Vergewissern Sie sich, dass die Zugriffsberechtigungen so festgelegt sind, dass der Image-Server die vollständige Kontrolle über den Ordner hat.

## SV::temp - Ordner für temporäre Dateien für den Server Supervisor {#section-fd2cd5ef7e814a4bb56aaf5525e1a154}

Der Server Supervisor muss gelegentlich Zwischendaten auf dem Datenträger speichern. Der Pfad kann absolut oder relativ zu *[!DNL install_folder]* sein. Die Standardeinstellung ist [!DNL *[!DNL install_folder]*/temp].

>[!NOTE] {class=&quot;- topic/note &quot;
>
>Der neue Ordner muss erstellt werden, bevor diese Einstellung geändert werden kann. Stellen Sie sicher, dass die Zugriffsberechtigungen festgelegt sind, damit der Server Supervisor die vollständige Kontrolle über den Ordner hat.

