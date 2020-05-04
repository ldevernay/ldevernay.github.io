---
layout: post
title:  "Performance"
date:   2019-11-12 10:59:53 +0200
categories: green
---
J'avais annoncé une série de billets suite à [celui sur les valeurs du développeur](https://ldevernay.github.io/green/2019/09/03/valeurs.html).
Celui sur [l'accessibilité est déjà dispo](https://ldevernay.github.io/green/2019/10/20/accessibilite.html).
Voici celui sur la performance.  

### Performance pour le web
#### Problématique
La performance web, si on veut un résumé approximatif, a trait à la vitesse à laquelle votre site web (ou votre appli) s'affiche et permet à l'utilisateur d'interagir avec. En soi, le lien avec les valeurs du web (pour un numérique soutenable et éthique) n'est pas toujours évident.   
Voici donc d'autres façons d'aborder ce sujet : 
- Le fait de proposer des contenus trop lourds à charger contribue à la fracture numérique. Tout le monde n'a pas la chance d'avoir un appareil dernier cri et une connexion internet rapide. [Un petit exemple chez Youtube](https://blog.chriszacharias.com/page-weight-matters)
- Le plus souvent, on change nos équipements électroniques parce qu'ils rament et non parce qu'ils ne fonctionnent plus. Proposer des sites et applis plus légers est donc une bonne façon de contribuer à l'allongement de la durée de vie des équipements. 
- Bien souvent, un site ou une appli sont moins rapides quand le contenu est trop volumineux. Réduire ce contenu permet par la même occasion de réduire l'impact écologique (mois de données transférées). 
- Si votre site met plus de 3 secondes à charger sur mobile, [vous perdez la moitié des visiteurs](https://neilpatel.com/blog/loading-time/)
- Bonus : Google prend la performance en compte dans son algorithme de classement des sites. 

La performance va donc influer sur l'accessibilité et l'impact écologique de votre site. [Why performance matters](https://developers.google.com/web/fundamentals/performance/why-performance-matters/) resitue le contexte et, en fouillant un peu, vous trouverez sur le même site une doc technique hyper complète sur le sujet.

#### Mise en place
Partons donc du principe que vous êtes convaincus de l'importance de la performance.  
Pour avancer rapidement sur ce sujet, [ce cours Udacity est particulièrement bien fichu](https://www.udacity.com/course/website-performance-optimization--ud884). Il est dispensé par [Ilya Grigorik](https://developers.google.com/web/resources/contributors/ilyagrigorik), une référence sur ce sujet chez Google. Voici ce qu'il faut en retirer :     
- Critical Rendering path : comprendre comment le navigateur charge une page pour le faire de façon aussi efficace que possible. 
- Pensez à minifier et compresser les ressources textuelles HTML/CSS/JS : [un topo complet](https://developers.google.com/web/fundamentals/performance/optimizing-content-efficiency/optimize-encoding-and-transfer#text-compression-with-gzip).
- Avoir le moins de ressources bloquantes possibles en nettoyant son CSS et en s'appuyant sur les media queries. 
- Décaler le chargement des ressources qui bloquent la construction de la page (en utilisant defer ou async sur les scripts JS externes qui peuvent attendre que la page soit affichée pour être lancés).
- Optimiser le contenu non-textuel (vidéo, audio, images) en s'intéressant à des formats modernes (WebP) et en veillant à la taille et à l'encodage. Rien que les images, c'est déjà un gros morceau (voir le [guide d'optimisation des images par Addy Osmani](https://images.guide/))
- Prendre en compte [le cache](https://jakearchibald.com/2016/caching-best-practices/).
- Attention aux polices spécifiques qu'il faut charger. [Au-delà de ces conseils pour optimiser le chargement](https://css-tricks.com/three-techniques-performant-custom-font-usage/), vous pouvez aussi trouver des outils pour créer un subset d'une police (et ne garder que les caractères dont vous avez besoin).

Pas mal de tâches peuvent être [automatisées grâce à Gulp](https://ldevernay.github.io/green/2019/08/13/eco-gulp.html) (entre autres).

Si le cours Udacity est trop long pour vous (comptez une petite demi-journée pour le suivre en entier) ou si le format ne vous convient pas, voici [une série d'articles très bien fichus sur le sujet](https://buttercms.com/blog/front-end-performance-for-beginners).   
Sinon, O'Reilly propose l'ouvrage [Designing for Performance](http://shop.oreilly.com/product/0636920033578.do). Toutes les étapes d'un projet y sont considérées, jusqu'à la mise en place de bonnes pratiques au niveau d'une entreprise.  
Gardez à l'esprit que la performance entre dans le cadre d'une démarche d'amélioration continue. Tout ne se fera pas du jour au lendemain et il est important de suivre régulièrement les stats de votre site. C'est justement ce qu'on va voir dans la section suivante.  

#### Les outils d'audit
Les outils ne manquent pas et se recoupent sur pas mal d'items remontés (ce qui est normal). A vous de tester et de voir ceux qui vous conviennent le mieux. La plupart proposent également des pistes concrètes pour remédier aux problèmes rencontrés.   
Sachant que Firefox et Chrome proposent les outils pour ça dans leurs dev tools.   
* [Lighthouse](https://web.dev/measure/) fait une grosse partie du boulot, permet de faire des [audits personnalisés](https://www.aymen-loukil.com/en/blog-en/google-lighthouse-custom-audits/) et peut même depuis peu être incorporé directement dans votre process d'intégration continue. C'est lui qu'on retrouve dans Chrome et il "mesure" aussi l'accessibilité, aide à la mise en place d'une [PWA](https://ldevernay.github.io/green/2019/09/16/pwa.html), etc.
* [PurifyCSS](https://purifycss.online/#) et [UnusedCSS](https://www.jitbit.com/unusedcss/) vous aident à nettoyer votre CSS
* [Dareboost](https://www.dareboost.com/en), [GTmetrix](https://gtmetrix.com/), [Webpagetest](https://www.webpagetest.org/), [PageSpeed Insights] et [Pingdom](https://tools.pingdom.com/) valent également le détour
Note : les apprenants de Simplon Carbonne sont en train de travailler sur un comparatif de plein d'outils d'audit afin d'en sortir une boîte à outils ne contenant que l'essentiel (ainsi que la démarche pour mener un audit). Je ne manquerai bien sûr pas de vous tenir au courant.  


#### Exigez la qualité
Dans la mesure où la performance se met en place via de l'amélioration continue, il est important de [se fixer un budget](https://developers.google.com/web/tools/lighthouse/audits/budgets). Gardez à l'esprit que tout le monde n'a pas accès à la 4G ou à un appareil dernier cri. [Un calculateur de budget de performance](https://www.performancebudget.io/) permet de prendre en compte tout un panel de cas.   
Pour rappel, [utiliser le web avec un budget de 50 Mb](https://www.smashingmagazine.com/2019/07/web-on-50mb-budget/), ce n'est pas anodin.  

#### Le cas particulier de Wordpress
La performance est souvent négligée pour Wordpress.  
C'est d'autant plus dommage qu'il existe plein de plugins gratuits qui font le job assez facilement (notamment via l'optimisation des images et du cache). Voici [une liste d'outils pour creuser ce sujet](https://github.com/davidsonfellipe/awesome-wpo/blob/master/README.md). Vous verrez que ces ressources vont bien au-delà de Wordpress et qu'il y a de quoi y passer beaucoup de temps.   
Une petite pépite au passage : [des chiffres concrets sur l'impact de la performance sur certains sites](https://wpostats.com/) (avec en prime les études de cas correspondantes).   
Si vous cherchez une solution rapide et gratuite pour Wordpress, regardez du côté de [Smush](https://wordpress.org/plugins/wp-smushit/) pour les images et [W3 Total Cache](https://wordpress.org/plugins/w3-total-cache/) pour d'autres optimisations. 


#### Aller plus loin
Ok, ça fait déjà beaucoup d'infos.   
Si toutefois vous voulez en savoir plus, vous trouverez encore plus de matos sur [mon raindrop](https://raindrop.io/collection/7265129).    
Vous avez aussi plusieurs sites qui référencent des tonnes de ressources sur le sujet (un peu comme celui pour Wordpress vu plus haut) :
* [perf.rocks](https://perf.rocks/)
* [perf-tooling.today](http://www.perf-tooling.today/)
* [Une checklist très complète](https://www.smashingmagazine.com/2019/01/front-end-performance-checklist-2019-pdf-pages/)

#### Conclusion
La performance est un sujet à part entière dans le cadre du développement web. Si vous voulez contribuer à un web accessible pour tous, c'est une composante indispensable.     
Les utilisateurs y sont de façon générale très sensibles et c'est de toute façon quelque chose qui risque d'empêcher certains d'accéder à vos sites, que ce soit pour trouver des informations, effectuer un achat ou autres. Comme on le verra dans un prochain article, c'est également une composante majeure lorsque l'on veut aborder l'éco-conception.
