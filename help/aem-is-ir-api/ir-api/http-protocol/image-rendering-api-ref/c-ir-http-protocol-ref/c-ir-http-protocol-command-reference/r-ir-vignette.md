---
description: Vignette-Datei. Gibt die Vignette an, die für diese Anforderung verwendet werden soll.
solution: Experience Manager
title: Vignette
feature: Dynamic Media Classic,SDK/API
role: Developer,User
exl-id: 8419d68d-7579-4e62-abbd-7dc0a736ae23
source-git-commit: 206e4643e3926cb85b4be2189743578f88180be7
workflow-type: tm+mt
source-wordcount: '127'
ht-degree: 4%

---

# Vignette{#vignette}

Vignette-Datei. Gibt die Vignette an, die für diese Anforderung verwendet werden soll.

`vignette=[ *``*/] *``*|[catId/] *`catIdrecIdfile`*`

<table id="simpletable_432EC5501CA3431B83A762C3EE4E8DD2"> 
 <tr class="strow"> 
  <td class="stentry"> <p><span class="varname"> catId</span> </p> </td> 
  <td class="stentry"> <p>Materialkatalog-ID (Übereinstimmung mit <span class="codeph"> Attribut::RootId</span>). </p></td> 
 </tr> 
 <tr class="strow"> 
  <td class="stentry"> <p><span class="varname"> recId</span> </p></td> 
  <td class="stentry"> <p>Vignette-ID (Übereinstimmung mit <span class="codeph"> Vignette::Id</span>). </p></td> 
 </tr> 
 <tr class="strow"> 
  <td class="stentry"> <p><span class="varname"> Datei</span> </p></td> 
  <td class="stentry"> <p>Relativer Vignettendateipfad und -name. </p></td> 
 </tr> 
</table>

Sie können entweder einen Vignettenzuordnungseintrag oder eine Vignettendatei angeben. Remote-URLs sind nicht zulässig.

`vignette=` kann als Alternative zur Angabe der Vignette im Anfragepfad-URL verwendet werden. Wird hauptsächlich verwendet, um Vignetten über Variablen in Vorlagen anzugeben.

Wenn *`catId`* nicht angegeben ist, wird der Sitzungskatalog verwendet.

## Eigenschaften {#section-f58661fc78d7496e8e3d0fb98b945c4b}

Kann an einer beliebigen Stelle in der Anfrage auftreten. Überschreibt die Vignette, die mit dem Anforderungs-URL-Pfad angegeben wurde.

## Standard {#section-db0618d48bc84dc8abcc989550349ccc}

Keine.

## Verwandte Themen {#section-dc2668cc2cd54a74b08cff68a12d4edd}

[Materialkataloge](../../../../../ir-api/http-protocol/image-rendering-api-ref/c-ir-http-protocol-ref/c-ir-http-protocol-syntax-and-features/c-ir-http-material-catalogs/c-ir-http-material-catalogs.md#concept-772742c1688f420a88a56f5136ad1db2),  [benutzerdefinierte Variablen](../../../../../ir-api/http-protocol/image-rendering-api-ref/c-ir-http-protocol-ref/c-ir-http-protocol-syntax-and-features/c-ir-custom-variables/c-ir-custom-variables.md#concept-8a1d9a50d09a4b7b97b8c83365971f96)
