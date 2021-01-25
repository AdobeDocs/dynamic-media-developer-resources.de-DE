---
description: Enthält Konfigurationseinstellungen für den Server-Supervisor.
solution: Experience Manager
title: SupervisorRegistry.xml
topic: Dynamic Media Image Serving - Image Rendering API
translation-type: tm+mt
source-git-commit: 97a84e8e7edd3d834ca42069eae7c09c00d57938
workflow-type: tm+mt
source-wordcount: '72'
ht-degree: 0%

---


# SupervisorRegistry.xml{#supervisorregistry-xml}

Enthält Konfigurationseinstellungen für den Server-Supervisor.

Achten Sie beim Bearbeiten dieser XML-Datei darauf, die gültige XML-Syntax beizubehalten, da andernfalls der Image-Server möglicherweise nicht in Beginn geraten kann.

Starten Sie Image Serving nach der Bearbeitung dieser Datei neu, um sicherzustellen, dass Ihre Änderungen wirksam werden. Nur die unten hervorgehobenen Element-/Attributwerte werden für Änderungen unterstützt. Bearbeiten Sie alle anderen Inhalte dieser Datei nur, wenn Sie vom technischen Support von Dynamic Media beraten werden.

```
<supervisor>
    <config>
        <tcpport>9910</tcpport>
        <log>SV::log</log>
        <temp>SV::temp</temp>
        <tracelevel>SV::tracelevel</tracelevel>
        <tracestatsinterval>600</tracestatsinterval>
    </config>
    <servers>
        <server id="is">
            <description>Dynamic Media Image Server</description>
            <profile ref="SV::ImageServerMode"/>
            <startPriority>1</startPriority>
            <startDelay>5</startDelay>
            <stopTimeout>60</stopTimeout>
        </server>
        <server id="svg">
            <description>Dynamic Media SVG server</description>
            <profile ref="Java32"/>
            <profile ref="SVG"/>
            <arguments>
                <argument>-XmxSV::SvgHeapSize</argument>
                <argument>-XX:MaxPermSize=200m</argument>
                <argument>-Dcom.sun.management.jmxremote.port=9998</argument>
            </arguments>
            <startPriority>1</startPriority>
            <startDelay>5</startDelay>
            <stopTimeout>60</stopTimeout>
        </server>
        <server id="ps">
            <description>Dynamic Media Platform Server</description>
            <profile ref="Java32"/>
            <profile ref="PlatformServer"/>
            <profile ref="Tomcat"/>
            <arguments>
                <argument>-XmxSV::PsHeapSize</argument>
                <argument>-XX:MaxPermSize=200m</argument>
                <argument>-Dcom.sun.management.jmxremote.port=9999</argument>
            </arguments>
            <startPriority>2</startPriority>
            <startDelay>5</startDelay>
            <stopTimeout>60</stopTimeout>
        </server>
    </servers>
</supervisor>
```

