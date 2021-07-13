---
description: InfoPanelPopup.template
solution: Experience Manager
title: InfoPanelPopup.template
feature: Dynamic Media Classic,Viewers,SDK/API,eCatalog Search
role: Developer,User
exl-id: b792cddb-f3d2-4609-95b7-105d76fb3d6f
source-git-commit: 206e4643e3926cb85b4be2189743578f88180be7
workflow-type: tm+mt
source-wordcount: '209'
ht-degree: 3%

---

# InfoPanelPopup.template{#infopanelpopup-template}

`[InfoPanelPopup.|<containerId>_infoPanelPopup.]template= *`Vorlage`*`

<table id="table_A6B1B446A7AE4A4A8B552C07EC88E518"> 
 <tbody> 
  <tr> 
   <td> <p> <span class="codeph"><span class="varname"> Vorlage</span></span> </p> </td> 
   <td> <p>Die Inhaltsvorlage, in der die vom Infoserver zurückgegebenen Daten zusammengeführt werden. </p> <p>Die Inhaltsvorlage ist eine XML-Datei, die dieser DTD folgt: </p> <p> <code>&lt;!DOCTYPE&nbsp;info&nbsp;[
      &lt;!ELEMENT&nbsp;info&nbsp;(var&nbsp;#PCDATA)
      &lt;!ELEMENT&nbsp;var&nbsp;(#PCDATA)&gt;
      &lt;!ATTLIST&nbsp;var&nbsp;
      name&nbsp;CDATA&nbsp;#REQUIRED
      rollover&nbsp;CDATA&nbsp;#IMPLIED&nbsp;&gt;
      ]&gt;</code> </p> <p>Die eigentliche Syntax für die Inhaltsvorlage lautet: </p> <p> <code>&lt;info&gt;
      &lt;var&nbsp;name='VAR_NAME'&nbsp;rollover='ROLLOVER_KEY'&gt;&lt;!CDATA[&nbsp;VAR_VALUE&nbsp;]&gt;
      &lt;![CDATA[&nbsp;TEMPLATE_CONTENT&nbsp;]&gt;
      &lt;/info&gt;</code> </p> <p>Das heißt, die Vorlage muss mit dem Element <span class="codeph"> &lt;info&gt;</span> beginnen, das optionale Standardelemente <span class="codeph"> &lt;var&gt;</span> enthalten kann. Der Vorlageninhalt selbst <span class="codeph"> TEMPLATE_CONTENT</span> ist HTML-Text. Darüber hinaus kann die Inhaltsvorlage Variablennamen enthalten, die in <span class="codeph"> $</span> -Zeichen eingeschlossen sind. Diese Zeichen werden durch die Variablenwerte ersetzt, die der Infoserver zurückgibt, oder durch Standardwerte. </p> <p>Standardvariablen, die in der Vorlage definiert sind, können entweder global (wenn das Rollover-Attribut nicht festgelegt ist) oder spezifisch für einen bestimmten Rollover-Schlüssel sein (wenn das Rollover-Attribut vorhanden ist). </p> <p>Während der Vorlagenverarbeitung haben Variablen, die spezifisch für das Rollout von Schlüsseln sind, Vorrang vor globalen Variablen. </p> </td> 
  </tr> 
 </tbody> 
</table>

>[!NOTE]
>
>Beachten Sie, dass beim Konfigurieren von &quot;Info Panel Popup&quot;der HTML-Code und der JavaScript-Code, der an das Info Panel übergeben wird, auf dem Computer des Clients ausgeführt werden. Stellen Sie daher sicher, dass dieser HTML-Code und JavaScript-Code sicher sind.

## Eigenschaften {#section-6dd7785357d740d095fa9f7fd0f67da4}

Optional.

## Standard {#section-cd5db06d08aa4de49e37d6c938b41570}

Keine.

## Beispiel {#section-16d184665c484964af9a22f79ff3f840}

Angenommen, die Infoserver-Antwort gibt den Produktnamen als Variable `$1$` zurück und die Produktbild-URL wird als Variable `$2$` zurückgegeben.

`template=<info><![CDATA[Product description:$1$<br>Product image:<img src="$2$">]]></info>`
