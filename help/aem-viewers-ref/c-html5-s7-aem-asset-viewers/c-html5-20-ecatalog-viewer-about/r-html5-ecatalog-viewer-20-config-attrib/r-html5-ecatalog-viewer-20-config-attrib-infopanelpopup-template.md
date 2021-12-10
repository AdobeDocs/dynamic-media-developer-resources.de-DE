---
title: InfoPanelPopup.template
description: InfoPanelPopup.template
solution: Experience Manager
feature: Dynamic Media Classic,Viewers,SDK/API,eCatalog
role: Developer,User
exl-id: 20618017-2f73-4951-baa9-2063a0f4efcb
source-git-commit: a919130f0940d81a221b79563b6b3e41533ba788
workflow-type: tm+mt
source-wordcount: '197'
ht-degree: 3%

---

# InfoPanelPopup.template{#infopanelpopup-template}

` [InfoPanelPopup.|<containerId>_infoPanelPopup.]template= *`Vorlage`*`

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
      &lt;var&nbsp;name='VAR_NAME'&nbsp;rollover='ROLLOVER_KEY'&gt;&lt;!CDATA[&nbsp;VAR_VALUE&nbsp;]]&gt;
      &lt;![CDATA[&nbsp;TEMPLATE_CONTENT&nbsp;]]&gt;
      &lt;/info&gt;</code> </p> <p>Das heißt, die Vorlage muss mit der <span class="codeph"> &lt;info&gt;</span> -Element, das optionale Standardwerte enthalten kann <span class="codeph"> &lt;var&gt;</span> -Elemente. den Vorlageninhalt selbst, <span class="codeph"> TEMPLATE_CONTENT</span> ist HTML-Text. Darüber hinaus kann die Inhaltsvorlage Variablennamen enthalten, die in <span class="codeph"> $</span> Zeichen, die durch die vom Infoserver zurückgegebenen Variablenwerte oder durch Standardwerte ersetzt werden. </p> <p>Standardvariablen, die in der Vorlage definiert sind, können entweder global (wenn das Rollover-Attribut nicht festgelegt ist) oder spezifisch für einen bestimmten Rollover-Schlüssel sein (wenn das Rollover-Attribut vorhanden ist). </p> <p>Während der Vorlagenverarbeitung haben Variablen, die spezifisch für das Rollout von Schlüsseln sind, Vorrang vor globalen Variablen. </p> </td> 
  </tr> 
 </tbody> 
</table>

>[!NOTE]
>
>Wenn Sie das Popup für das Infofeld konfigurieren, werden der HTML-Code und der JavaScript-Code, der an das Infofeld übergeben wird, auf dem Clientcomputer ausgeführt. Stellen Sie daher sicher, dass dieser HTML-Code und JavaScript-Code sicher sind.

## Eigenschaften {#section-6dd7785357d740d095fa9f7fd0f67da4}

Optional.

## Standard {#section-cd5db06d08aa4de49e37d6c938b41570}

Keine.

## Beispiel {#section-16d184665c484964af9a22f79ff3f840}

Angenommen, die Info-Server-Antwort gibt den Produktnamen als Variable zurück `$1$` und die Produkt-Bild-URL wird als Variable zurückgegeben `$2$`.

`template=<info><![CDATA[Product description:$1$<br>Product image:<img src="$2$">]]></info>`
