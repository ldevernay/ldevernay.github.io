---
layout: post
title:  Audits d'écoconception - ADEME & Act for climate
date:   2020-06-24 08:59:53 +0200
categories: green
---

Voici le quatrième article sur les audits d’écoconception web réalisés dans le cadre de la formation à Simplon Carbonne.   
Vous trouverez tous les articles autour des audits d'écoconception web sur [la page dédiée](https://ldevernay.github.io/Audits.html).   
Nous attaquons le vif du sujet avec la présentation des audits réalisés pour l'ADEME et pour Act for Climate.  


## Echantillon de départ 
Pour lancer ce chantier autour de l'audit de sites web, nous disposions de plusieurs sites. 

*La présence de nombreux sites Wordpress dans le lot (ce qui, statistiquement, est logique vu que Wordpress représente une grosse part du marché) a incité à ajouter [WPScan](https://wpscan.org/) aux outils utilisés et à prévoir un process particulier (voir plus loin).*   

La liste des sites (un ou deux qui sont arrivés en cours de route) : 
* Observatoire DPE (ADEME)
* Simul'Aid€s (ADEME)
* Act for Climate
* Site du plaidoyer Simplon
* Simplon For All
* Simplon Inside
* Ecole de la Transition Ecologique
  
**Merci à tous ceux qui ont accepté de mettre à disposition leurs sites pour ces audits!**
  
### Rappel
Pour réaliser ces audits, nous avons commencé par lister un ensemble d'outils d'audit gratuits disponibles en ligne.   
L'idée était de tester ces outils pour progressivement réduire la liste, dans l'objectif d'obtenir un ensemble d'outils aussi restreint et complet que possible.   
Le second objectif était d'identifier les problèmes récurrents et de prioriser les bonnes pratiques à mettre en place. Ainsi, on obtient les points de vigilance et axes d'amélioration prioritaires lors de l'analyse d'un site. Ceci rejoint la volonté plus globale de sensibiliser à l'écoconception web et de rendre l'amélioration d'un site plus facilement accessible (en gros, lister des quick wins).  
Enfin (et ce sera l'objet d'un article ultérieur), c'était l'occasion de mettre en avant les bons et mauvais usages de sobriété numérique et éditoriale. En effet, la sobriété numérique est un axe très avantageux pour améliorer l'écoconception d'un site mais le sujet reste relativement peu documenté (ou en tout cas, à mon goût, pas de façon assez concrète). A noter que le travail en cours à [l'INR](https://institutnr.org/) sur un référentiel d'écoconception devrait aider à y remédier. 

### Présentation des résultats des audits
Pour chaque audit réalisé, nous nous contenterons ici de présenter les éléments qui en sont ressortis. 
Les éléments retenus sont ceux qui paraissent les plus impactants. Pour cela, nous nous sommes appuyés entre autres sur [les 115 bonnes pratiques](https://collectif.greenit.fr/ecoconception-web/115-bonnes-pratiques-eco-conception_web.html) mises en avant par le collectif GreenIT.  
Les personnes concernées par les audits se sont vues adresser les résultats complets obtenus avec les différents outils utilisés ainsi que les conclusions. Nous n'avons gardé ici que les éléments les plus significatifs et compréhensibles par tout un chacun. Ce choix est discutable et la discussion à ce sujet reste d'ailleurs ouverte pour ceux qui le souhaitent.  

## Présentation des clients
L'ADEME est l'[Agence de la Transition Ecologique](https://www.ademe.fr/). Dans le cadre de la Transition Ecologique, l'ADEME est très impliquée sur la question de l'impact du numérique. On lui doit entre autres la plaquette sur [la face cachée du numérique](https://www.ademe.fr/sites/default/files/assets/documents/guide-pratique-face-cachee-numerique.pdf). L'ADEME a également appuyé le projet GreenConcept évoqué précédemment ([lien vers le PDF du bilan](http://www.greenconcept-innovation.fr/wp-content/uploads/2020/02/greenconcept_21022020.pdf)).   
[Act for Climate](https://www.act-for-climate.fr/) est un événement ayant eu lieu à Toulouse l'année dernière afin de sensibiliser à l'urgence climatique. 
  
## ADEME 
### Observatoire DPE  
[Observatoire DPE](https://www.observatoire-dpe.fr/)     
         
| Page testée | Perf environnementale | Complexité (nb d'elts sur la page) | Bande passante (poids de la page)    | Charge serveur (nb de req HTTP) | Empreinte GES (gC02e) | Empreinte eau (cl) |    
| ------ | ------ | ------ | ------ | ------ | ------ | ------ |   
| Accueil | 77 (A) | 216 |633 Ko | 24 |1.46 |2.19 |  


*(source : GreenIT-Analysis)*   
[PageSpeed Index :](https://developers.google.com/speed/pagespeed/insights/) 76 
* La page "Simuler un DPE" est-elle vraiment utile? 
* La page "Rechercher un diagnostiqueur" (redirection vers un autre site) mériterait sûrement un audit à part entière mais non-prioritaire car l'ADEME n'a pas forcément la main dessus.  
Les optimisations techniques à explorer sont : 
* Optimisation des images (format, taille et en regrouper autant que possible dans un sprite CSS). 
* Externalisation, nettoyage, minification et compression des assets (HTML/CSS/JS). Y compris pour les librairies externes. 
* Mise en place d'une politique de cache. 
* Mise à jour de jQuery (envisager si possible une alternative plus légère). 
* Corriger les erreurs dans le HTML : id dupliqués, libellés manquants (entre autres). 
* Ajouter une meta-description dans le HTML. 
* Optimiser HTML/CSS pour usage mobile. 
* [Accessibilité] Ajouter les libellés manquants sur le formulaire de connexion 
* [Accessibilité] Remédier aux erreurs de contraste de couleurs.   
   
Si possible: 
* Sortir de Google Analytics (mesurer la pertinence des indicateurs récupérés, envisager de passer sur une solution d'analyse plus légère et moins invasive comme Matomo). 
* Différer le chargement de certains scripts (attention, l'impact se verra sur la performance mais pas forcément sur l'impact environnemental du site).   

### Simul'aid€s 
[Simul'aid€s](http://www.normandie.infoenergie.org/vos-aides/simuler-vos-aides/)     
(audit réalisé par [Morgane Echeveste, apprenante à Simplon Carbonne et créatrice du Studio Osmo](https://twitter.com/Moetxea))       
   
| Page testée | Perf environnementale | Complexité (nb d'elts sur la page) | Bande passante (poids de la page) | Charge serveur (nb de req HTTP) | Empreinte GES (gC02e) | Empreinte eau (cl) |   
| ------ | ------ | ------ | ------ | ------ | ------ | ------ |   
| Accueil | 53.3 (C) | 329 |3130 Ko | 70 |1.93 |2.9 |    
    
*(source : Ecoindex)* 
[PageSpeed Index :](https://developers.google.com/speed/pagespeed/insights/) 4    
* Le site est alourdi par des nombreux scripts JS et autres feuilles de style CSS externalisés et non-compressés.    
* Des images non-optimisées sont présentes.   
* La mise en cache doit être mieux configurée (pour éviter de charger plusieurs fois certains éléments depuis le serveur). 
* Le parcours utilisateur est long et complexe, ce qui alourdit d'autant l'impact environnemental du site.   
  
Au final, on a un site qui est dans la moyenne et qui pourrait facilement arriver sur un Eco-index B voire A moyennant quelques optimisations techniques. Toutefois, les plus gros gains pourraient avoir lieu en revoyant le parcours utilisateur.   


## Act for Climate 
[Le site de l'événement Act for climate](https://www.act-for-climate.fr/)       
          
| Page testée | Perf environnementale | Complexité (nb d'elts sur la page) | Bande passante (poids de la page) | Charge serveur (nb de req HTTP) | Empreinte GES (gC02e) | Empreinte eau (cl) |   
| ------ | ------ | ------ | ------ | ------ | ------ | ------ |    
| Accueil | 26 (E) | 1251 |3498 Ko | 71 |2.48 |3.72 |     
   
*(source : Ecoindex)* 
[PageSpeed Index :](https://developers.google.com/speed/pagespeed/insights/) 31 
* Eviter d'inclure une vidéo sur la page d'accueil du site (utiliser plutôt une image comportant un lien vers la vidéo). 
* Limiter encore plus le nombre d'intervenants sur la page d'accueil. 
* Beaucoup d'images sont incluses, il faudrait en diminuer le nombre. Sinon, voir si le site ne pourrait pas être découpé en davantage de pages.
* S'assurer de ne pas garder des plugins inutiles. 

Etant donné qu'il s'agit d'un site Wordpress, les optimisations techniques reposent principalement sur l'installation des plugins adéquats (W3 Total Cache, Smush, etc) afin d'optimiser la compression des ressources, les images et le cache (entre autres).  
Le thème devrait être abandonné en faveur d'un autre plus accessible et léger.   
Je vous renvoie au passage sur [mon article sur l'écoconception web avec Wordpress](https://ldevernay.github.io/green/2019/12/13/wordpress_eco.html). 

## Conclusion
Nous avons donc vu ici seulement la première moitié des audits réalisés (et seulement leurs conclusions, pour des raisons évidentes de place). Quelques tendances se dégagent déjà, à voir si elles se confirmeront par la suite.  
La prochaine fois, nous compléterons avec les autres audits afin de pouvoir par la suite passer aux conclusions. Celles-ci sont assez denses et seront elles aussi découpées en plusieurs parties afin de présenter les bonnes pratiques et axes d'amélioration, les éléments relatifs à la sobriété numérique et le panel d'outils retenus. Enfin, tout ceci nous permettra de construire une méthodo pour des audits d'écoconception web "allégés". 
