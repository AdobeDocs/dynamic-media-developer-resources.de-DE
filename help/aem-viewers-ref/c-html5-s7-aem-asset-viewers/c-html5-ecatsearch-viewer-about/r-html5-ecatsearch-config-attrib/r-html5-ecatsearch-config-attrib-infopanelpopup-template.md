---
description: InfoPanelPopup.template
solution: Experience Manager
title: InfoPanelPopup.template
topic: Dynamic media
uuid: a7b49f82-9a8b-45f8-b933-9880659770de
translation-type: tm+mt
source-git-commit: bf5873e5a6bdb859e19b15584ba85e9c106f853b
workflow-type: tm+mt
source-wordcount: '201'
ht-degree: 3%

---


# InfoPanelPopup.template{#infopanelpopup-template}

`[InfoPanelPopup.|<containerId>_infoPanelPopup.]template= *`Vorlage`*`

<table id="table_A6B1B446A7AE4A4A8B552C07EC88E518"> 
 <tbody> 
  <tr> 
   <td> <p> <span class="codeph"><span class="varname"> Vorlage</span></span> </p> </td> 
   <td> <p>Die Inhaltsvorlage, in die die vom Infoserver zurückgegebenen Daten zusammengeführt werden. </p> <p>Die Inhaltsvorlage ist eine XML nach dieser DTD: </p> <p> <code>&lt;!DOCTYPE&nbsp;info&nbsp;[
      &lt;!ELEMENT&nbsp;info&nbsp;(var&nbsp;#PCDATA)
      &lt;!ELEMENT&nbsp;var&nbsp;(#PCDATA)&gt;
      &lt;!ATTLIST&nbsp;var&nbsp;
      name&nbsp;CDATA&nbsp;#REQUIRED
      rollover&nbsp;CDATA&nbsp;#IMPLIED&nbsp;&gt;
      ]&gt;</code> </p> <p>Die eigentliche Syntax für die Inhaltsvorlage lautet wie folgt: </p> <p> <code>&lt;info&gt;
      &lt;var&nbsp;name='VAR_NAME'&nbsp;rollover='ROLLOVER_KEY'&gt;&lt;!CDATA[&nbsp;VAR_VALUE&nbsp;]&gt;
      &lt;![CDATA[&nbsp;TEMPLATE_CONTENT&nbsp;]&gt;
      &lt;/info&gt;</code> </p> <p>Das heißt, die Vorlage muss mit dem <span class="codeph"> &lt;info&gt;</span>-Element Beginn werden, das optionale Elemente <span class="codeph"> &lt;var&gt;</span> enthalten kann. Der Vorlageninhalt selbst, <span class="codeph"> TEMPLATE_CONTENT</span>, ist HTML-Text. Darüber hinaus kann die Inhaltsvorlage Variablennamen enthalten, die in &lt; a0/&gt; $</span>-Zeichen eingeschlossen sind. <span class="codeph"> Diese Zeichen werden durch die Variablenwerte ersetzt, die der Infoserver zurückgibt, oder durch Standardwerte. </span></p> <p>Standardvariablen, die in der Vorlage definiert werden, können entweder global (wenn das Rollover-Attribut nicht festgelegt ist) oder spezifisch für einen bestimmten Rollover-Schlüssel sein (wenn das Rollover-Attribut vorhanden ist). </p> <p>Bei der Vorlagenverarbeitung haben Variablen, die spezifisch für die Übertragung von Schlüsseln sind, Vorrang vor globalen Variablen. </p> </td> 
  </tr> 
 </tbody> 
</table>

>[!NOTE]
>
>Beachten Sie, dass beim Konfigurieren des Infofeld-Popup der HTML-Code und der an das Infofeld übergebene JavaScript-Code auf dem Client-Computer ausgeführt werden. Stellen Sie daher sicher, dass der HTML-Code und der JavaScript-Code sicher sind.

## Eigenschaften {#section-6dd7785357d740d095fa9f7fd0f67da4}

Optional.

## Standard {#section-cd5db06d08aa4de49e37d6c938b41570}

Keine.

## Beispiel {#section-16d184665c484964af9a22f79ff3f840}

Unter der Annahme, dass die Info-Server-Antwort den Produktnamen als Variable `$1$` und die Produkt-Bild-URL als Variable `$2$` zurückgibt.

`template=<info><![CDATA[Product description:$1$<br>Product image:<img src="$2$">]]></info>`
