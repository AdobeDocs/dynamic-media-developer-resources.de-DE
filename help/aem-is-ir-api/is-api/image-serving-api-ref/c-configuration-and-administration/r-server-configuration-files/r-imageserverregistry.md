---
description: Enthält Image-Server-Konfigurationseinstellungen.
solution: Experience Manager
title: ImageServerRegistry.xml
feature: Dynamic Media Classic, SDK/API
role: Entwickler, Administrator, Business Practitioner
translation-type: tm+mt
source-git-commit: f6c97606d7a4209427316d7367013ad9585a5cae
workflow-type: tm+mt
source-wordcount: '172'
ht-degree: 0%

---


# ImageServerRegistry.xml{#imageserverregistry-xml}

Enthält Image-Server-Konfigurationseinstellungen.

Beim Ändern dieser XML-Datei muss darauf geachtet werden, dass die gültige XML-Syntax beibehalten wird. Andernfalls kann der Image-Server nicht in Beginn geraten.

Damit die Änderungen wirksam werden, starten Sie den Image-Server nach der Bearbeitung dieser Datei neu. Nur die unten aufgeführten Elementwerte werden für Änderungen unterstützt. Bearbeiten Sie alle anderen Inhalte dieser Datei nur, wenn Sie vom technischen Support von Dynamic Media beraten werden.

>[!NOTE]
>
>Ändern Sie nicht die Struktur von `<imageserverregistry>`, einschließlich der Reihenfolge der Elemente. Gehen Sie beim Bearbeiten dieser Datei mit Bedacht vor, da andernfalls der Image-Server möglicherweise nicht in Beginn gehen kann.

Im Folgenden wird veranschaulicht, welche Elemente geändert werden können. Andere Elemente sind vorhanden, die nicht geändert werden dürfen. Die Reihenfolge der unten aufgeführten Elemente spiegelt nicht die Reihenfolge wider, in der sie in der Datei enthalten sein müssen.

```
<imageserverregistry>
    <TcpPort> 27345 </TcpPort>    
    <RootPath ./images </RootPath>
    <TempDirectory ./temp </TempDirectory>
    <Log> ./logs/ImageServer.log </Log>
    <TraceClient> 2 </TraceClient>
    <TraceStatsInterval> 600 </TraceStatsInterval>
    <PhysicalMemory> 20 </PhysicalMemory>
    <WorkerThreads> 0 </WorkerThreads>
    <SVGTcpPort> 27346 </SVGTcpPort>
    <MaxRenderRgnPixels> 16 </MaxRenderRgnPixels>
    <MaxSavePixels> 100 </MaxSavePixels>
    <MaxMessageSize> 16 </MaxMessageSize>
    <CacheServerUrl> http://localhost:8080/is/cache/secondary </CacheServerUrl>
    <NumberOfTextServers> 0 </NumberOfTextServers>
    <TextServerTcpPortRange> 27347-27380 </TextServerTcpPortRange>
    <SaveDirectory> ./ </SaveDirectory>
    <RemoteUrlDefaultExpiration> 36000 </RemoteUrlDefaultExpiration>
    <RemoteUrlTimeout> 60 </RemoteUrlTimeout>
    <MaxNonDsfSize> 4 </MaxNonDsfSize>
</imageserverregistry>
```

## Anmerkungen {#section-7217f011f69f41e7af4f3983d7776d6f}

Es können mehrere `<RootPath>`-Elemente vorhanden sein (eines für jeden Ordner der Quelldatendatei). Image Server durchsucht die Stammpfade in der angegebenen Reihenfolge, um eine bestimmte Quelldatei zu finden.
