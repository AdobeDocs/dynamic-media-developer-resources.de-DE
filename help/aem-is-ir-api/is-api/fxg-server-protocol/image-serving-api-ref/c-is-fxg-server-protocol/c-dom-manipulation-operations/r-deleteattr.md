---
description: Löschen Sie alle Attribute für eine angegebene s7 elementID.
solution: Experience Manager
title: deleteAttr
feature: Dynamic Media Classic,SDK/API
role: Developer,Business Practitioner
translation-type: tm+mt
source-git-commit: d0bc88f55f857762b3bab4c76d1e3f3dd2733d60
workflow-type: tm+mt
source-wordcount: '57'
ht-degree: 1%

---


# deleteAttr{#deleteattr}

Löschen Sie alle Attribute für eine gegebene s7:elementID.

`deleteAttr.elementID={attributeName%26attributeName}`

Wenn für ein FXG-Knotenelement ein `s7:elementID` definiert ist, können die Attribute für diesen Knoten mit diesem Befehl gelöscht werden.

## Beispiel {#section-dece7192384a412c9afdfbda6f08bc97}

`<Group x="130.494" y="102.2246" d:id="4" d:type="layer" d:userLabel="WhiteFrame" visible="true" s7:elementID="middle_area">`

`deleteAttr.middle_area={x%26y%26visible}`

`<Group d:id="4" d:type="layer" d:userLabel="WhiteFrame" s7:elementID="middle_area">`

In diesem Beispiel werden die Attribute *[!DNL x]*, *[!DNL y]* und *[!DNL visible]* aus dem ursprünglichen FXG-Knoten entfernt.
