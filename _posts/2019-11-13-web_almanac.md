---
layout: post
title:  "Comprendre le web grâce à HTTPArchive"
date:   2019-11-13 10:59:53 +0200
categories: green
description: Utiliser HTTPArchive pour prendre le pouls de l'impact environnemental du web (et l'application des bonnes pratiques).
---
[HTTPArchive](https://httparchive.org/) récolte en continu des données relatives aux sites web.  
Sur un échantillon de plusieurs millions de site, ils sont capables de fournir des tonnes d'indicateurs très intéressants.  
C'est un excellent moyen de mieux comprendre comment sont construits les sites web.  
Toutes ces données sont d'ailleurs facilement accessibles [via BigQuery](https://github.com/HTTPArchive/httparchive.org/blob/master/docs/gettingstarted_bigquery.md).  
Pour la première fois cette année, une analyse de toutes ces données a été mise à disposition [sous la forme d'un almanach](https://almanac.httparchive.org/en/2019).  
En creusant un peu, il est facile de faire remonter des infos qui touchent à l'impact écologique des sites web ([la section sur l'accessibilité](https://almanac.httparchive.org/en/2019/accessibility) est assez inquiétante aussi).  


### Optimisation technique des sites web
Voici quelques faits en vrac qui ressortent de cette étude : 
La moitié des sites :
* utilisent plus de 373 Kb de JS
* mettent au moins 2,437s à charger uniquement le JS
* utilisent plus de 18 requêtes rien que pour récupérer les scripts JS
* utilisent au moins 6 feuilles de style
* comportent plus de 1MB d'images

* jQuery est encore utilisé sur plus de 83% des sites
* Bootstrap est utilisé sur plus d'un quart des sites
* Un peu moins de la moitié des sites utilisent une media-query de type print (pour adapter la page en cas d'impression)
* [La plupart des images sont encore retaillées dans le navigateur](https://docs.google.com/spreadsheets/d/e/2PACX-1vSViHIntdF6-bHAI0cl1HelY_X8rR4lf0P3W2Y8I5SyVMxG-ptggTHfWA0qrrU47RvuAydLE6Zex6L3/pubchart?oid=2027393897&format=interactive) (ce qui signifie qu'on charge plus de données qu'on en a besoin pour l'affichage)  
* Le nombre d'éléments dans le DOM est en constante augmentation et [la répartition fait peur](https://docs.google.com/spreadsheets/d/e/2PACX-1vTbHgqcSepZye6DrCTpifFAUYxKT1hEO56585awyMips8oiPMLYu20GETuIE8mALkm814ObJyktEe2P/pubchart?oid=2141583176&format=interactive). D'autant plus quand on voit [quels éléments restent les plus utilisés](https://docs.google.com/spreadsheets/d/e/2PACX-1vTbHgqcSepZye6DrCTpifFAUYxKT1hEO56585awyMips8oiPMLYu20GETuIE8mALkm814ObJyktEe2P/pubchart?oid=1694360298&format=interactive)
* Seuls 4.2% des sites utilisent le format WebP  
* Pour améliorer la performance d'un site et réduire la taille des contenus textuels chargés, la compression peut jouer un rôle essentiel. [Retrouvez plus d'info sur une section dédiée à ce sujet](https://almanac.httparchive.org/en/2019/compression)
* Si vous cherchez à mieux comprendre [l'impact de la performance](https://ldevernay.github.io/green/2019/11/12/performance.html), une section est entièrement [dédiée à ce sujet](https://almanac.httparchive.org/en/2019/performance). Elle vous aidera à mieux comprendre comment les utilisateurs perçoivent la performance d'un site et comment cela peut varier en fonction de leur localisation géographique  
* [Plus de 96% des sites pourraient mettre en cache davantage de ressources](https://almanac.httparchive.org/en/2019/caching). Rappel: pour repérer les opportunités liées au cache et comprendre la mise en oeuvre de cette solution, [Lighthouse](https://web.dev/measure/) est un excellent outil

### Taille des pages
La [section dédiée à la taille des pages](https://almanac.httparchive.org/en/2019/page-weight) apport plein de chiffres très pertinents du point de vue de l'éco-conception.  
* La taille médiane d'une page est de 1.9Mb et celle-ci contient 74 requêtes  
* La présence d'un trop grand nombre d'images ou d'éléments dans le DOM font diminuer le taux de conversion  
* Depuis 2018, la taille médiane des pages a augmenté de 434 Kb pour les version desktop et de 179 Kb pour les versions mobile. Ceci est principalement dû à une augmentation du volume d'images utilisées  

### Conclusion
Il y a encore plein de choses à améliorer sur le web, sans compter tout ce qu'on ne peut pas tout à fait mesurer (éthique, dark patterns, etc). Cette étude donne déjà une bonne vue d'ensemble de ce qui se fait, voire des points sur lesquels se concentrer pour espérer améliorer la situation. 
