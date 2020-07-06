---
layout: post
title:  "Audits d'écoconception - conclusion"
date:   2020-07-06 10:59:53 +0200
categories: green
description: Après tous ces audits, voici les premières conclusions et notamment des pistes pour auditer rapidement un site web sur des critères d'éco-conception. 
---

Après plusieurs audits d'éco-conception, les premières conclusions s'imposent. Celles-ci ont pour objectif de faciliter la vie de ceux qui souhaiteraient aussi vérifier si un site respecte les bonnes pratiques d'éco-conception.   
Vous trouverez tous les articles autour des audits d'écoconception web sur [la page dédiée](https://ldevernay.github.io/Audits.html).  
   
## Méthodo retenue
Nous étions partis sur ces audits avec toute une liste d'outils gratuits et pas mal de pistes sur la méthodo à adopter. Nous en ressortons donc avec de nombreuses informations. Reste à faire un peu de tri dans tout ça.    

### Les outils retenus         
Chaque outil d'audit renvoie de nombreux indicateurs.    
Nous avons retenu ceux qui vont dans le sens de l'écoconception (alléger ce qui est envoyé au client, alléger le parcours utilisateur, etc). Afin de mieux identifier les bonnes pratiques à mettre en place et les prioriser, nous nous sommes appuyés sur le [recueil des 115 bonnes pratiques d'écoconception](https://collectif.greenit.fr/ecoconception-web/115-bonnes-pratiques-eco-conception_web.html).       
Il semblerait judicieux de privilégier un outil comme [web.dev](https://web.dev/measure/) qui permet de mesurer simultanément la performance, les bonnes pratiques, le SEO et l'accessibilité. Cependant, cet outil est moins visuel et concret que d'autres outils plus spécialisés. Au final, nous avons réussi à identifier un panel d'outils, moyennant quelques cas particuliers à prendre en compte.    
* [GreenIT Analysis](https://chrome.google.com/webstore/detail/greenit-analysis/mofbfhffeklkbebfclfaiifefjflcpad) : idéal pour mesurer des indicateurs d'écoconception sur une page donnée et vérifier les bonnes pratiques. La version Chrome du plugin est à privilégier car plus complète (pour la bonne raison que l'API de Firefox est pour l'instant moins complète sur certains aspects). Pour mesurer un parcours utilisateur dans son intégralité, le plus pratique reste [le plugin Ecoindex](https://addons.mozilla.org/fr/firefox/addon/ecoindex/). 
* [PageSpeed Insights :](https://developers.google.com/speed/pagespeed/insights/) très bien pour mesurer la performance et obtenir des recommandations concrètes ainsi que les bénéfices attendus suite à leur mise en application. [Pingdom](https://tools.pingdom.com) ou [GT Metrix](https://gtmetrix.com/analyze.html) peuvent être utilisés en complément, de même que les DevTools Firefox ou Chrome. C'est pour cela que nous l'avons utilisé en priorité pour les audits. Entre-temps, un autre outil a fait son apparition ([Fast Or Slow](https://www.fastorslow.com/app)) et il est bien parti pour changer la donne. Il semble plus complet que ses concurrents et très visuel. Aujourd'hui, il est donc pertinent de préférer Fast or Slow.
* [Wave](https://wave.webaim.org/) : permet de mesurer l'accessibilité. Il y en a évidemment d'autres mais celui-ci peut être installé directement dans le navigateur et va droit à l'essentiel.
* Pour les sites Wordpress et à défaut de disposer d'un accès à l'administration, [WPScan](https://wpscan.org/) permet d'avoir un aperçu des plugins installés et du thème utilisé. Même si ceci permet de vérifier s'il existe des failles de sécurité, le plus simple reste d'aller chercher les informations directement auprès du propriétaire du site concerné par l'audit. Surtout si vous voulez une liste des plugins utilisés, le nom du thème. Ce sera beaucoup plus simple.   
    
Au final, les autres outils ont été laissés de côté car jugés redondants ou moins pertinents.  
> A l'usage, il n'a pas semblé pertinent d'évaluer directement le SEO (car les bénéfices sur le SEO se retrouvent essentiellement en agissant sur l'écoconception, notamment performance et accessibilité) ni les indicateurs liés à la sécurité (car il s'agit plutôt d'un effet secondaire appréciable de l'écoconception). Toutefois, il est important de retenir que le SEO est lié à un impact indirect des sites web : si un site est difficile à trouver, les recherches de l'internaute auront un impact environnemental plus conséquent. 

#### Pourquoi mesurer tout ça?
L'éco-conception est étroitement liée à d'autres domaines de la qualité web. 
* L'accessibilité est essentielle car, si on n'y fait pas attention, l'accès sera plus compliqué pour certains internautes. Concrètement, ceci peut les empêcher d'accéder au service souhaité et alourdir l'empreinte environnementale en allongeant leur parcours sur le site. 
* La performance est intéressante à mesurer car l'éco-conception tend à l'améliorer. Attention toutefois car l'inverse n'est pas forcément vrai : certaines pratiques pour améliorer la performance d'un site peuvent dégrader son impact environnemental. En gros, si un site n'est pas performant, l'éco-conception est un bon filtre pour identifier commme y remédier. Inversement, si un site est performant, regardez comment on arrive à ce résultat, notamment en vérifiant les bonnes pratiques d'éco-conception. 
* Comme nous l'avons déjà évoqué, le SEO conditionne l'accès au site web. Plus le site sera facile à trouver et à identifier, plus le parcours utilisateur sera allégé. 

### Les indicateurs   
Comme indiqué plus haut, nous avons choisi de mettre en avant les indicateurs suivants : 
* Taille de la page (mesuré) => GreenIT-Analysis
* Nombre de requêtes HTTP (mesuré) => GreenIT-Analysis
* Nombre d'éléments dans le DOM (mesuré) => GreenIT-Analysis
* Eco-index (calculé) => GreenIT-Analysis
* Emission de gaz à effet de serre en équivalent CO2 (calculé) => GreenIT-Analysis
* Consommation d'eau (calculé) => GreenIT-Analysis
* Performance Score (calculé) => Fast or Slow 

Au sujet de ce dernier, il peut être pertinent d'aller plus précisément vers des indicateurs de performance plus précis si le propriétaire du site peut être plus réceptif sur ce sujet (First Contentful Paint, Time to Interactive ou autre).  
> Le Performance Score remplace le PageSpeed Index de PageSpeed Insights utilisé précédemment. La logique reste la même mais nous préconisons d'utiliser plutôt Fast or Slow.  

L'idée générale pour ces indicateurs est de fournir des éléments de comparaison et, au-delà des bonnes pratiques, d'avoir des ordres de grandeur dont on pourra mesurer l'évolution au fil du temps.

#### Et l'accessibilité?
Après tout ce que j'ai écrit plus haut, vous pouvez vous étonner de ne pas trouver d'indicateur lié à l'accessibilité. Ceci est dû au fait que l'audit d'accessibilité se base plutôt sur des non-conformités ou le respect de bonnes pratiques. Mais il n'y a pas à proprement parler d'indicateur d'accessibilité, sauf à vouloir construire un indicateur chiffré de conformité. 
  

### Ce qu'il faut auditer 
Comme nous l'avons vu plus haut, plusieurs cas se dessinent : 

#### Page unique
Si le site ne contient qu'une seule page, il suffit d'analyser cette page.  
Ca semble évident, dit comme ça.   

#### Site multi-pages
Si le site est composé de plusieurs pages, la page d'accueil est incontournable. Il faut ensuite déterminer un échantillon d'environ 5 pages parmi les plus visitées. Parfois, ce ne sont pas forcément les plus utiles du point de vue du client (et inversement). Avoir des statistiques sur l'utilisation du site (Google Analytics, Matomo ou autres) peut constituer un bon point de départ pour identifier les pages à analyser en priorité. 

Le RGAA (Référentiel Général d'Amélioration de l'Accessibilité) propose [sa propre liste de pages à auditer en priorité](https://www.numerique.gouv.fr/publications/rgaa-accessibilite/obligations/#%C3%89chantillon) : 
* Page d'accueil
* Page de contact
* Page mentions légales
* Page plan du site
* Page d'aide
* Page d'authentification
* Au moins une page pertinente pour chaque type de service fourni
* Toute page ayant un aspect ou un contenu distinct. 
   
#### Découpage en services numériques
Si des parcours utilisateur clairs se précisent, il faut auditer chacun de ces parcours en détail (contacter l'administrateur du site, commander un article, effectuer une réclamation, trouver un trajet, etc).     
Ceci s'avère parfois compliqué pour un site-vitrine mais cette démarche reste indispensable. Un site web doit toujours être créé avec un objectif clair en tête, quelque chose que l'on veut faire pour l'utilisateur ou que l'on veut que l'utilisateur fasse sur le site. Il est indispensable de garder cette notion en tête, notamment dans une démarche de sobriété numérique. 

### Comment auditer?
Une fois les pages et/ou parcours utilisateurs identifiés, je vous recommande d'utiliser l'ensemble des outils indiqués plus haut et de mesurer les indicateurs listés. Vous aurez ainsi une idée de la maturité du site (ou du service numérique) du point de vue de l'éco-conception. 
L'idée est ensuite de préparer un document présentant le résultat de votre audit. Là aussi, le RGAA est fourni avec ce qu'il vous faut : [des modèles de rapport d'audit](https://www.numerique.gouv.fr/publications/rgaa-accessibilite/kit/#contenu). Il est assez facile de s'en inspirer pour produire un document propre. Celui-ci devrait contenir au moins : 
* le nom et l'adresse du site web
* la description de chaque service numérique audité
* le nom de la personne ou structure ayant réalisé l'audit
* la date de l'audit  
* les outils utilisés
* la stack technique du site
* l'environnement de test (navigateur, OS)
  
Pour chaque service audité : 
* la liste des pages (et l'adresse de chacune)
* la liste des bonnes pratiques mises en oeuvre
* la liste des axes d'amélioration et bonnes pratiques à mettre en oeuvre
  
Conclusion : 
* avis général sur le site ou service numérique, les points forts et bonnes pratiques respectées
* axes d'amélioration et corrections à apporter. 
   
Tout au long du rapport, il est essentiel de souligner ce qui est bien fait.  
Autant que possible, les éléments relevés doivent rester de l'ordre de l'objectif et du concret.  
La première partie de la conclusion doit être aussi compréhensible que possible.  
Les axes d'amélioration peuvent être techniques et doivent être priorisés, en fonction de la difficulté de mise en oeuvre et de l'impact potentiel. Une fois n'est pas coutume, vous pouvez ressortir votre [recueil des 115 bonnes pratiques d'écoconception](https://collectif.greenit.fr/ecoconception-web/115-bonnes-pratiques-eco-conception_web.html).  
Attention, dans le cas de Wordpress, ces axes d'amélioration reposent souvent sur le choix du thème (mais l'audit a souvent lieu trop tard dans le cycle de vie pour qu'il soit possible de le changer) et des plugins. Pour autant, il n'y a pas de solution unique et incontournable, seulement des suggestions et, dans l'idéal, des préconisations techniques qui débouchent sur l'analyse d'un panel de plugins. 


#### Le mode rapide
Si vous êtes pressé ou que vous voulez juste une idée générale de la maturité du site du point de vue de l'éco-conception, contentez-vous de lancer GreenIT-Analysis sur la page d'accueil du site. C'est souvent un bon moyen de vous faire une idée de ce à quoi vous attendre. Le mieux est d'avoir un eco-index de A ou B mais, même si c'est le cas, ce n'est pas pour autant qu'il n'y aura pas d'axes d'amélioration. Toutefois, sur certains sites, vous verrez très vite où vous mettez les pieds.   
Pour compléter, vous pouvez aussi lancer Wave et Fast or Slow.  
Cette pratique ne saurait en aucun cas remplacer un audit mais c'est un bon moyen de voir où placer le curseur de votre regard critique sur le site.  
  
### Et après?
Une fois le rapport d'audit construit, il reste une étape indispensable : garder à l'esprit que ce n'est là que le début du chemin. Par la suite, il est recommandé d'auditer régulièrement le site afin de mesurer son évolution, d'autant plus si des mesures correctives sont mises en place. Fast or Slow vous permet de suivre la performance de votre site au fil du temps. Si vous voyez celle-ci se dégrader subitement, regardez si certaines bonnes pratiques d'éco-conception n'ont pas été laissées de côté.    
Gardez aussi à l'esprit qu'un service numérique a une vie au-delà de sa phase de développement. Même si vous réalisez toutes les optimisations techniques imaginables, ceci sera vain si la notion de sobriété éditoriale n'est pas respectée (attention entre autres aux images et vidéos non-optimisées). Les gains seront d'autant plus importants si vous choisissez avec soin les fonctionnalités à mettre en place ainsi que les outils utilisés pour la réalisation du site. Même avec la meilleure volonté du monde, ce sera plus compliqué d'optimiser un site s'il est réalisé avec des outils inadaptés au besoin (souvent parce qu'ils sont surdimensionnés).   
Vous avez aussi la possibilité de définir un budget pour votre site. Vous pouvez vous fixer un Eco-index à ne pas dépasser (A ou B, c'est déjà bien) voire aller plus loin (et plus concret) en définissant des limites sur les trois indicateurs qui servent à le calculer : 
* Taille de la page 
* Nombre de requêtes HTTP 
* Nombre d'éléments dans le DOM 
  
Rappelez-vous que l'éco-conception nécessite de remettre l'utilisateur au coeur du process. Dans ces conditions, il est indispensable de regarder plus largement la qualité web. Et vous pouvez bien sûr vous appuyer sur [Opquast](https://checklists.opquast.com/fr/qualiteweb/) pour cela. Vous trouverez d'ailleurs chez eux [des check-lists dédiées à certaines thématiques indispensables](https://checklists.opquast.com/fr): Accessibilité, Webperf, SEO, GreenIT mais aussi Web Mobile.  
Même si on en voit de moins en moins, pensez à tous ces sites web non-optimisés pour le mobile et au temps perdu pour naviguer dessus. Et dites-vous que, dans ce cas, les développeurs n'ont pas forcément penser à optimiser les images pour des appareils mobiles.  


### Conclusion 
On se retrouve donc avec un set d'outils dont la plupart peuvent être installés directement dans le navigateur pour plus de commodité.              
En renfort, une fois de plus, le recueil des 115 bonnes pratiques permet de faire du tri dans les bonnes pratiques et de les prioriser (en évaluant l'impact de chacune mais aussi leur facilité de mise en oeuvre). Notamment parce que certaines ne peuvent pas être mesurées directement (autoplay, flash, etc).   
Toutefois, on reste ici sur des pistes d'optimisations techniques. Comme nous l'avons déjà vu, l'écoconception web doit être abordée de façon transverse : avec tous les membres de l'équipe projet, sur toutes les phases du cycle de vie du service numérique.   
Au cours d'un audit, on pourra ainsi fournir des préconisations sur : 
* La stack technique (mais c'est souvent difficile à mettre en oeuvre dès lors qu'on a commencé à développer le site) 
* L'hébergeur (même si le client va parfois rechigner à en changer... et qu'il peut être difficile de trouver l'hébergeur idéal) 
* La sobriété fonctionnelle (ce qui peut être retiré ou modifié pour alléger le site et/ou le parcours utilisateur) 
  
Ca tombe bien, on reviendra là-dessus dans le prochain article (qui conclura vraiment cette série d'articles sur les audits d'éco-conception, c'est promis).