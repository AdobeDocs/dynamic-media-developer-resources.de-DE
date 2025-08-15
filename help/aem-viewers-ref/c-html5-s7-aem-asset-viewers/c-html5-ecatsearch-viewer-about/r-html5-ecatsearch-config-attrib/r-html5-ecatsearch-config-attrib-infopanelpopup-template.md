---
description: InfoPanelPopup.template
solution: Experience Manager
title: InfoPanelPopup.template
feature: Dynamic Media Classic,Viewers,SDK/API,eCatalog Search
role: Developer,User
exl-id: b792cddb-f3d2-4609-95b7-105d76fb3d6f
source-git-commit: 206e4643e3926cb85b4be2189743578f88180be7
workflow-type: tm+mt
source-wordcount: '201'
ht-degree: 1%

---

# InfoPanelPopup.template{#infopanelpopup-template}

`[InfoPanelPopup.|<containerId>_infoPanelPopup.]template= *`template`*`

<table id="table_A6B1B446A7AE4A4A8B552C07EC88E518"> 
 <tbody> 
  <tr> 
   <td> <p> <span class="codeph"><span class="varname"> Vorlage</span></span> </p> </td> 
   <td> <p>Die Inhaltsvorlage, in der die vom Info-Server zurückgegebenen Daten zusammengeführt werden. </p> <p>Die Inhaltsvorlage ist eine XML, die dieser DTD folgt: </p> <p> <code>&lt;!DOCTYPE&nbsp;info&nbsp;&lbrack;
      &lt;!ELEMENT&nbsp;info&nbsp;(var&nbsp;#PCDATA)
      &lt;!ELEMENT&nbsp;var&nbsp;(#PCDATA)&gt;
      &lt;!ATTLIST&nbsp;var&nbsp;
      name&nbsp;CDATA&nbsp;#REQUIRED
      rollover&nbsp;CDATA&nbsp;#IMPLIED&nbsp;&gt;
      &rbrack;&gt;</code> </p> <p>Die tatsächliche Syntax für die Inhaltsvorlage lautet wie folgt: </p> <p> <code>&lt;info&gt;
      &lt;var&nbsp;name='VAR_NAME'&nbsp;rollover='ROLLOVER_KEY'&gt;&lt;!CDATA[&nbsp;VAR_VALUE&nbsp;]&gt;
      &lt;!&lbrack;CDATA[&nbsp;TEMPLATE_CONTENT&nbsp;]&gt;
      &lt;/info&gt;</code> </p> <p>Das heißt, die Vorlage muss mit dem <span class="codeph"> &lt;info&gt;</span> beginnen, das optionale <span class="codeph"> &lt;var&gt;</span> enthalten kann. Der Vorlageninhalt selbst, <span class="codeph"> TEMPLATE_CONTENT</span> ist HTML-Text. Darüber hinaus kann die Inhaltsvorlage Variablennamen enthalten, die in <span class="codeph"> $</span>-Zeichen eingeschlossen sind. Diese Zeichen werden durch die Variablenwerte ersetzt, die der Info-Server zurückgibt, oder durch Standardwerte. </p> <p>Standardvariablen, die in der Vorlage definiert sind, können entweder global (wenn das rollover-Attribut nicht festgelegt ist) oder spezifisch für einen bestimmten rollover-Schlüssel (wenn das rollover-Attribut vorhanden ist) sein. </p> <p>Bei der Vorlagenverarbeitung haben Variablen, die für Rollover-Schlüssel spezifisch sind, Vorrang vor globalen Variablen. </p> </td> 
  </tr> 
 </tbody> 
</table>

>[!NOTE]
>
>Beachten Sie, dass beim Konfigurieren des Infobedienfeld-Popup der an das Infobedienfeld übergebene HTML- und JavaScript-Code auf dem Client-Computer ausgeführt wird. Stellen Sie daher sicher, dass dieser HTML- und JavaScript-Code sicher sind.

## Eigenschaften {#section-6dd7785357d740d095fa9f7fd0f67da4}

Optional.

## Standard {#section-cd5db06d08aa4de49e37d6c938b41570}

Keine.

## Beispiel {#section-16d184665c484964af9a22f79ff3f840}

Angenommen, die Antwort des Info-Servers gibt den Produktnamen als Variable `$1$` und die Produktbild-URL wird als Variable `$2$` zurückgegeben.

`template=<info><![CDATA[Product description:$1$<br>Product image:<img src="$2$">]]></info>`
