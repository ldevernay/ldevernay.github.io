---
layout: post
title:  Audits d'écoconception - Simplon & Ecole de la Transition Ecologique
date:   2020-06-29 08:59:53 +0200
categories: green
description: Le cinquième article sur les audits d’écoconception web réalisés dans le cadre de la formation à Simplon Carbonne. Nous verrons ici la suite et fin des audits réalisés, cette fois avec Simplon et l'Ecole de la Transition Ecologique. 
---

Voici le cinquième article sur les audits d’écoconception web réalisés dans le cadre de la formation à Simplon Carbonne.   
Vous trouverez tous les articles autour des audits d'écoconception web sur [la page dédiée](/Audits.html).   
Nous verrons ici la suite et fin des audits réalisés, cette fois avec Simplon et l'Ecole de la Transition Ecologique. 


## Sites audités
Suite aux audits déjà décrits dans le précédent article, il reste ceux-ci :
* Site du plaidoyer Simplon
* Simplon For All
* Simplon Inside
* Ecole de la Transition Ecologique
  
### Rappel
Pour réaliser ces audits, nous avons commencé par lister un ensemble d'outils d'audit gratuits disponibles en ligne.   
L'idée était de tester ces outils pour progressivement réduire la liste, dans l'objectif d'obtenir un ensemble d'outils aussi restreint et complet que possible.   
Le second objectif était d'identifier les problèmes récurrents et de prioriser les bonnes pratiques à mettre en place. Ainsi, on obtient les points de vigilance et axes d'amélioration prioritaires lors de l'analyse d'un site. Ceci rejoint la volonté plus globale de sensibiliser à l'écoconception web et de rendre l'amélioration d'un site plus facilement accessible (en gros, lister des quick wins).  
Enfin (et ce sera l'objet d'un article ultérieur), c'était l'occasion de mettre en avant les bons et mauvais usages de sobriété numérique et éditoriale. En effet, la sobriété numérique est un axe très avantageux pour améliorer l'écoconception d'un site mais le sujet reste relativement peu documenté (ou en tout cas, à mon goût, pas de façon assez concrète). A noter que le travail en cours à [l'INR](https://institutnr.org/) sur un référentiel d'écoconception devrait aider à y remédier. 

## Présentation des résultats des audits
Pour chaque audit réalisé, nous nous contenterons ici de présenter les éléments qui en sont ressortis. 
Les éléments retenus sont ceux qui paraissent les plus impactants. Pour cela, nous nous sommes appuyés entre autres sur [les 115 bonnes pratiques](https://collectif.greenit.fr/ecoconception-web/115-bonnes-pratiques-eco-conception_web.html) mises en avant par le collectif GreenIT.  
Les personnes concernées par les audits se sont vues adresser les résultats complets obtenus avec les différents outils utilisés ainsi que les conclusions. Nous n'avons gardé ici que les éléments les plus significatifs et compréhensibles par tout un chacun. Ce choix est discutable et la discussion à ce sujet reste d'ailleurs ouverte pour ceux qui le souhaitent.  

## Présentation des clients
[Simplon](https://simplon.co/) est un organisme de formation préparant des personnes de tous horizons aux métiers du numérique. C'est aussi mon employeur. Pour autant, je n'ai pas pris de pincettes pour les audits réalisé. 
[L'Ecole de la Transition Ecologique](https://www.ecole-transition.eu/) est également une organisme de formation professionnelle mais dont les cursus se construisent autour de la transition écologique. 
  
### Simplon 
#### Simplon4all 
[Simplon4all](https://simplonforall.simplon.co/)           
   
| Page testée | Perf environnementale | Complexité (nb d'elts sur la page) | Bande passante (poids de la page) | Charge serveur (nb de req HTTP) | Empreinte GES (gC02e) | Empreinte eau (cl) |   
| ------ | ------ | ------ | ------ | ------ | ------ | ------ |    
| Accueil | 72.7 (B) | 161 |1339 Ko | 35 |1.55 |2.32 |     
     
*(source : Ecoindex)*   
[PageSpeed Index :](https://developers.google.com/speed/pagespeed/insights/) 99 
* Le bandeau en haut de page prend énormément de place alors qu'il n'apporte que peu d'infos. 
* Le choix de faire un site statique en une page est top mais attention à la stack technique utilisée (Larave+Vue.js?). Regarder par exemple la [JAMstack](https://jamstack.wtf/).   
  
Les optimisations techniques à explorer sont : 
* Revoir la gestion du cache
* Eviter le @import de CSS 
* Optimiser les images (taille et format, prévoir en plus le lazy-load sur celles qui sont below the fold donc non visibles tant que l'utilisateur n'a pas scrollé) 
* Optimiser le CSS (sélecteurs inutilisés, minifier, compresser) 
* Attention au contraste des couleurs 
* 1 erreur HTML à corriger 
* Optimiser les fonts custom (subset consistant à ne garder que les caractères utilisés) 

Si possible: 
* Se passer de jQuery (alternatives plus légères) 
* Ajouter Content Security Policy 
* Ajouter noscript 
* Ajouter un CSS print si ça semble pertinent 

####  Plaidoyer Simplon 
[Plaidoyer Simplon](https://plaidoyer.simplon.co/)      
          
| Page testée | Perf environnementale | Complexité (nb d'elts sur la page) | Bande passante (poids de la page) | Charge serveur (nb de req HTTP) | Empreinte GES (gC02e) | Empreinte eau (cl) |   
| ------ | ------ | ------ | ------ | ------ | ------ | ------ |  
| Accueil | 68 (B) | 304 |1673 Ko | 24 |2.46 |1.64|    
   
*(source : Ecoindex)*   
[PageSpeed Index :](https://developers.google.com/speed/pagespeed/insights/) 100 
Très bien, quasiment rien à redire. 
* Redimensionner les images avec une hauteur de 100px (=> alléger la page) 
* Rassembler les images dans un seul sprite CSS (=> diminuer de moitié le nombre de requêtes HTTP) 
* Ajouter les directives de cache pour les svg et la page d'accueil 
* Externaliser, minifier et mettre en cache les parties communes du CSS et du JS 
* Fournir une feuille print CSS (avec media-query HTML>link et CSS), d'autant plus que le site contient essentiellement du texte. 
* Corriger l'erreur JS résiduelle. 
* 2 polices de caractères spécifiques sont utilisées. Elles pourraient être remplacées. 

#### Simplon Inside 
Il s'agit là d'un portail interne réservé aux employés Simplon (donc je ne donne pas ici de lien pour y accéder).    
            
| Page testée | Perf environnementale | Complexité (nb d'elts sur la page) | Bande passante (poids de la page) | Charge serveur (nb de req HTTP) | Empreinte GES (gC02e) | Empreinte eau (cl) |   
| ------ | ------ | ------ | ------ | ------ | ------ | ------ |    
| Accueil | 29 (F) | 1313 |3097 Ko | 58 |2.42 |3.63|   
   
*(source : GreenIT Analysis)*   
On est ici dans le cas d'un site Google. Le besoin d'origine était de pouvoir déployer facilement un site statique et le mettre à jour régulièrement, sans aucune compétence technique. Même si le choix technique reste discutable pour des questions de performance et d'impact environnemental, les principaux axes d'amélioration relèvent plutôt de la communication responsable.   
L'axe prioritaire serait de veiller à optimiser les images avant leur mise en ligne. Il faudrait dans un second temps limiter les vidéos et éviter les carrousels ainsi que les plugins Discord/Twitter. 

### Ecole de la transition écologique 
[Ecole de la transition écologique](https://www.ecole-transition.eu/)               

| Page testée | Perf environnementale | Complexité (nb d'elts sur la page) | Bande passante (poids de la page) | Charge serveur (nb de req HTTP) | Empreinte GES (gC02e) | Empreinte eau (cl) |   
| ------ | ------ | ------ | ------ | ------ | ------ | ------ |   
| Accueil | 27 (E) | 780 |6181 Ko | 106 |2.46 |3.69 |   
| Contacter l'école | 8 (F) | 1351 | 10512 Ko | 208 | 2.84 | 4.26 |    
| Découvrir l'école | 14 (F) | 1051 | 10148 Ko | 166 | 2.72 | 4.08 |    
| Témoignages | 20 (F) | 926 | 5092 Ko | 137 | 2.6 | 3.9 |    
| Recrutement | 16 (F) | 938 | 9956 Ko | 165 | 2.68 | 4.02 | 
        

*(source : Ecoindex)*   
[PageSpeed Index :](https://developers.google.com/speed/pagespeed/insights/) 33     
* Eviter d'inclure une vidéo sur la page d'accueil du site (image + lien vers la vidéo) et au moins enlever l'autoplay. 
* Eviter le texte sur des images (accueil, témoignages). 
* S'assurer de ne pas garder des plugins inutiles. 
* Eviter les fils Twitter et Facebook, surtout sur plusieurs pages. 
* Trouver des alternatives pour le partage sur les réseaux sociaux. 
* Eviter la carte Google Maps (préférer image + lien). 
  
Le souci avec Wordpress est qu'on remarque souvent plein de bonnes pratiques à mettre en oeuvre mais qu'on a difficilement la main pour le faire. Il semble donc plus judicieux de regarder directement du côté des plugins disponibles.  
Pour ce qui est des erreurs d'accessibilité, mieux vaut regarder du côté du thème. 
Il faudrait envisager des modules Wordpress (gratuits ou non mais il y a moyen de faire avec seulement du gratuit) : 
* Un module d'optimisation d'images (smush, ewww, robin, etc) 
* Un module d'optimisation du code (autoptimize) 
* Un module d'optimisation du cache (WP Super Cache, WP Rocket ou W3 Total Cache)       
Pour le cas particulier de Wordpress, je me permets de vous renvoyer à un article publié ici-même : [Wordpress et éco-conception]({% post_url 2019-12-13-wordpress_eco %})       



## Conclusion
Nous avons désormais fait le tour des audits réalisés. Le panel est relativement réduit mais la masse de travail conséquente. En effet, il s'agissait d'éprouver de nombreux outils gratuits et de comparer des indicateurs tout en fournissant aux propriétaires des différents sites des conclusions concises et (autant que possible) compréhensibles.  
Il ne reste donc plus que deux articles à venir dans cette série sur les audits d'éco-conception web : 
* un premier article qui présente les conclusions des audits et en particulier les outils et indicateurs préconisés. En gros, il s'agira de mon parti-pris pour réaliser des audits d'éco-conception web simplifiés. 
* le second article, en bonus, reviendra sur tout ce qu'il faut regarder au-delà de ce que peuvent mesurer les outils, y compris la sobriété fonctionnelle.
