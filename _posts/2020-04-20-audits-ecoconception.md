---
layout: post
title:  "Audits d'écoconception - écoconception web"
date:   2020-04-20 10:59:53 +0200
categories: green
---

Voici le second article sur les audits d'écoconception web réalisés dans le cadre de la formation à Simplon Carbonne.   
Vous trouverez tous les articles autour des audits d'écoconception web sur [la page dédiée](https://ldevernay.github.io/Audits.html).  
Ici, nous allons nous intéresser à la notion d'écoconception web.  
Pour une fois, je vais essayer de faire court.
   
## Ecoconception web 
En général, on parle plutôt d'écoconception de service numérique, dans la mesure où on travaille sur une unité fonctionnelle. Ici, notre démarche se limite aux sites web donc nous opérons ce raccourci et parlons d'écoconception web (et tant pis pour les puristes).    
L'écoconception web est un processus d'amélioration continue visant à minimiser l'impact environnemental d'un site web. Cette approche intervient tout au long du cycle de vie du site web (de l'idée à la fin de vie en passant par la conception et le développement).   
Voici les éléments-clés de cette démarche :  
* Dans un premier temps, déterminer si le site web est vraiment utile (sinon, autant s'en passer). 
* Cerner au plus près les fonctionnalités (et ne garder que celles qui sont vraiment utiles pour les utilisateurs). 
* Penser la conception (au sens UX/UI) afin d'optimiser le parcours utilisateur : l'internaute doit pouvoir accomplir ce pour quoi il vient sur le site le plus rapidement/facilement possible. 
* L'architecture technique (et le choix de la stack technique) doit être calée au plus près du besoin afin de minimiser les impacts. Un framework/CMS qui fait tout c'est pratique mais c'est souvent trop.  
* Le développement doit être effectué en gardant en tête [les bonnes pratiques](https://collectif.greenit.fr/ecoconception-web/115-bonnes-pratiques-eco-conception_web.html).  
* L'hébergeur doit donner des éléments de preuve sur son impact environnemental. C'est presque un sujet à part entière, nous y reviendrons plus tard. 
* Une fois le site en ligne, les ajouts, modifications, corrections ainsi que la communication doivent respecter ce qui a été mis en place pour réduire son impact environnemental. Il faut garder à l'esprit que l'écoconception web est un processus, pas un projet. Il est ici vital d'avoir une procédure rapide d'audit d'écoconception afin de pouvoir mesurer régulièrement l'impact du site. *D'où la présente démarche autour des audits.*
* Lorsque le site n'est plus utile (événementiel, etc), il n'a pas besoin de rester en ligne.     
  
Souvent, l'écoconception repose uniquement sur les développeurs. Cette démarche n'est pas viable car plus de la moitié des impacts se trouvent en amont de leur intervention. Il est donc essentiel que toute l'équipe intervenant sur et autour du projet soit sensibilisée et que la démarche s'inscrive dans le temps.   
   
Pour un exemple d'audits d'écoconception sur des services numériques et les retours correspondants : [[PDF] Bilan GreenConcept](http://www.greenconcept-innovation.fr/wp-content/uploads/2020/02/greenconcept_21022020.pdf). *GreenConcept est une opération pilotée par la CCI d'Occitanie afin d'accompagner 28 entreprises vers l'écoconception de certains de leurs services numériques en s'appuyant sur une équipe d'experts.*    
  
### Bénéfices de l'écoconception web 
[Les valeurs](https://ldevernay.github.io/green/2019/09/03/valeurs.html) et bonnes pratiques du web sont nombreuses. Concernant la notion de qualité web, je me permets de vous orienter [directement vers Opquast](https://www.opquast.com/). Ces valeurs sont liées à l'écoconception web : 
* [Accessibilité](https://ldevernay.github.io/green/2019/10/20/accessibilite.html) : revient à s'assurer que le site sera utilisable par tout internaute, quelle que soit sa situation. Si l'on veut optimiser le parcours utilisateur, il est indispensable de garder cette notion à l'esprit. De base, l'écoconception web permet souvent d'alléger un site web, ce qui aide à limiter les risques de non-accessibilité. Toutefois, même si vous avez fait tout ce que vous pouviez sur l'accessibilité, un site trop lourd exclura automatiquement une partie des internautes ([un article sur les disparités de connexion à internet](https://www.smashingmagazine.com/2019/07/web-on-50mb-budget/)).    
* [Performance](https://ldevernay.github.io/green/2019/11/12/performance.html) : l'écoconception web vise souvent l'efficience. En allégeant un site web, on améliore sa performance. En conséquence, le site est plus rapide, l'expérience utilisateur s'améliore et [les conséquences sont très concrètes pour ne pas dire financières](https://wpostats.com/). 
* Référencement : lorsqu'un site devient plus accessible pour les utilisateurs, il le devient également pour les robots en charge du référencement. Un site plus rapide sera lui aussi mieux référencé. En poussant la logique de l'écoconception un peu plus loin, si l'on reste dans l'optique d'optimiser le parcours utilisateur, il est indispensable que l'internaute puisse facilement trouver le site. Aider l'utilisateur à trouver le site réduit mécaniquement l'impact environnemental de la navigation sur le web.  
* Sécurité : en allégeant un site, on réduit la surface d'attaque. Mettre en place moins de fonctionnalités réduit logiquement le nombre de fonctionnalités à sécuriser. Il y a fort longtemps, par exemple, la plupart des clients voulaient un forum sur leur site, avec tous les ennuis qui pouvaient en découler. 
* Economie de l'attention : le but n'est pas que l'utilisateur passe le plus de temps possible sur le site mais d'optimiser son parcours afin de le faire accéder plus facilement à ce qu'il veut. [Jean-Lou Fourquet explique très bien l'économie de l'attention.](https://avantlecafe.fr/2019/11/24/3-raisons-qui-font-du-temps-lenjeu-du-xxieme-siecle/)
* Vie privée et données personnelles : un article ultérieur reviendra sur les notions de données personnelles et de vie privée. La sobriété numérique incite à collecter seulement les données nécessaires, ce qui bénéficie à l'internaute (moins de données divulguées, formulaire d'inscription plus rapide à remplir, etc). On tend donc vers le [Privacy by design](https://www.smashingmagazine.com/2017/07/privacy-by-design-framework/) et on facilite ainsi les démarches liées au RGDP. 
* Finances : les items précédents de cette liste ont déjà en soi un impact financier. De plus, l'écoconception web peut améliorer l'image de marque et s'impose comme facteur de différenciation. D'autant plus qu'il est essentiel de communiquer autour de cette démarche (ne serait-ce que pour partager les bonnes pratiques et mettre en avant son utilité).
   
*Note :* la performance est un cas particulier. Performance et écoconception sont étroitement liées (notamment au niveau des bonnes pratiques à mettre en place). Attention toutefois à bien différencier les deux. En effet, la performance vise avant tout à rendre le site plus rapide, quitte à ajouter des surcouches et outils pour cela (différer certains chargements, multiplier les CDN, etc). Dans ce cas, on peut s'éloigner de l'écoconception. On peut donc dire, pour résumer, que l'écoconception rejoint la performance uniquement sur la question de l'efficience. Il s'agit bien d'aller plus vite en allégeant (les contenus, les fichiers transmis au navigateur, etc) plutôt qu'en ajoutant (des outils et autres solutions techniques). Pour autant, il y a donc plein de choses que l'écoconception peut apprendre de la performance. Jusque dans la marche à suivre pour [faire entrer la performance dans la culture d'une entreprise](https://calendar.perfplanet.com/2012/creating-a-performance-culture/) et favoriser son adoption auprès des équipes. 
  
## Conclusion  
En résumé, l'écoconception web repose sur un processus permettant de minimiser l'impact environnemental d'un site web. Ce processus intervient sur toutes les étapes du projet et implique tous les membres de l'équipe. Au-delà des optimisations techniques accessibles aux développeurs, la sobriété numérique apporte le plus de bénéfices (tri dans les fonctionnalités retenues). En se documentant un peu, il est rapide (et essentiel) d'identifier des compromis entre difficulté de mise en place et impact, dans le but de prioriser les actions.  
En agissant pour l'écoconception web, on entre dans un cercle vertueux tendant vers le numérique responsable. Ainsi, les liens avec l'accessibilité, la sécurité, la performance, le respect de la vie privée et l'économie de l'attention sont forts. Sans compter l'impact positif pour l'image de l'entreprise. Et les nombreux bénéfices pour les internautes.     
Afin d'en apprendre plus sur le sujet, je suis toujours disponible pour en parler.  
Sinon, une bonne première approche revient à regarder [ce que propose le Collectif Numérique Responsable](https://collectif.greenit.fr/outils.html). J'invite les plus téméraires à fouiller dans [la collection dédiée sur mon Raindrop](https://raindrop.io/collection/7258547).   
Dans le prochain article, nous verrons comment évaluer l'écoconception d'un site web et identifier les axes d'amélioration. 