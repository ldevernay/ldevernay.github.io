---
layout: post
title:  "Audits d'écoconception - bonus"
date:   2020-07-20 10:59:53 +0200
categories: green
description: Pour conclure les billets sur les audits d'éco-conception, on se penche plus en détails sur la question de l'hébergeur, de la stack technique et de la sobriété numérique.  
---
  
Vous trouverez tous les articles autour des audits d'écoconception web sur [la page dédiée](/Audits.html).   
Comme annoncé précédemment, on va ici s'intéresser au choix de l'hébergeur et de la stack technique ainsi qu'à la notion de sobriété fonctionnelle.
  
## Stack technique 
Le choix des outils utilisés constitue une étape fondamentale et trop souvent survolée. Parce qu'on reste sur ce qu'on connaît, parce qu'on veut tester le dernier outil à la mode ou parce qu'on ne nous laisse pas forcément le choix.    
Il n'y a pas forcément d'outil ultime qui viendra résoudre tous les problèmes d'un coup. Il n'y a que peu d'outils qui soient intrinséquement de mauvais choix. En revanche, il est important d'avoir pu appliquer en amont les principes d'écoconception web et en particulier de sobriété fonctionnelle afin de choisir l'outil qui correspondra le mieux au besoin du client en se basant sur les fonctionnalités dont il a vraiment besoin.     
Actuellement, quelques outils autour des PWA et de la JAMSTACK ont le vent en poupe. En parallèle, beaucoup dénigrent Wordpress. Pour autant, une JAMSTACK mal utilisée aura un impact écologique plus désastreux qu'un Wordpress correctement pensé pour l'écoconception.           

## Hébergeur 
Lorsque l'on cherche à réduire l'impact environnemental de son site web, l'hébergeur est une question cruciale. Dans l'idéal, il faut trouver une entreprise locale (ou pas loin) qui prenne des engagements sur la question (et fournisse si possible des éléments de preuve).   
Le collectif GreenIT propose déjà [pas mal d'éléments sur le sujet](https://www.greenit.fr/2009/05/18/quels-criteres-pour-identifier-un-hebergeur-vert/).    
A titre personnel, j'ai tendance à recommander principalement deux hébergeurs : 
* [Infomaniak](https://www.infomaniak.com/fr/hebergeur-ecologique/charte-ecologique) 
* [O2Switch](https://www.o2switch.fr/)    
  
## Sobriété fonctionnelle 
Des retours d'expérience commencent à paraître un peu partout. C'est une très bonne chose car, petit à petit, ces informations aident à se construire des bonnes pratiques sur le volet de la sobriété fonctionnelle.  Ceci ne peut pas être mesuré ni automatisé, même si c'est souvent là que vont se trouver les plus gros impacts. Ainsi, au cours des audits, il est fréquent de repérer des éléments qui n'apportent que peu ou pas à l'utilisateur (voire qui nuisent à l'UX) : les [pubs](https://thecorrespondent.com/100/the-new-dot-com-bubble-is-here-its-called-online-advertising/13228924500-22d5fd24) et trackers, les vidéos à outrance, etc. De même qu'on connaît (de plus en plus) les [Dark Patterns](https://darkpatterns.org/) qui viennent gâcher l'expérience utilisateur (à des fins de manipulation, ni plus ni moins), peut-être pouvons-nous déjà lister quelques mauvaises pratiques liées à la sobriété fonctionnelle. 
* L'affichage de fil Twitter/Facebook/Instagram est souvent lourd, d'autant plus qu'il apporte son lot de trackers et de scripts. 
* Même chose pour les boutons de partage sur les réseaux sociaux proposés par les réseaux en question. Un bon point de départ peut être de trouver [des alternatives en CSS](https://saeedalipoor.github.io/icono/). 
* Les vidéos (qui proviennent le plus souvent de Youtube) doivent être au moins [optimisées au préalable](https://www.mightybytes.com/blog/swd-video/). L'autoplay est à proscrire absolument, entre autres pour des raisons d'accessibilité. Le plus simple peut être de proposer une image (extraite de la vidéo) permettant de cliquer dessus pour accéder directement au site où se trouve la vidéo. 
* Les cartes Google Maps apportent de nombreuses fonctionnalités mais aussi leur lot de scripts, feuilles de style et trackers. Bien souvent, une simple image suffit pour aider l'internaute à localiser des endroits. Un clic sur l'image peut conduire à Google Maps. A noter que des alternatives libres et gratuites comme [OpenStreetMap](https://www.openstreetmap.org/#map=5/51.500/-0.100) existent. 
* Les images doivent être retaillées et [optimisées](https://images.guide/) au préalable. Le format WebP, par exemple, est de mieux en mieux supporté et bien plus léger que ses "ancêtres". 
* Si Google Analytics est utilisé, il revient de se demander quels indicateurs sont réellement utiles. Si ces indicateurs sont indispensables, il peut être intéressant de se tourner vers une alternative plus éthique comme [Matomo](https://matomo.org/). Des alternatives plus légères comme [GoAccess](https://goaccess.io/) méritent également qu'on s'y intéresse. 
* jQuery est souvent à proscrire (en raison de sa lourdeur et de ses failles de sécurité). Des alternatives plus légères existent, comme [Cash](https://github.com/kenwheeler/cash). Plus généralement, [le site microjs](http://microjs.com/#jquery) propose des alternatives plus légères à de nombreuses librairies JS. 
* [Les carousels](http://shouldiuseacarousel.com/) posent souvent des soucis d'accessibilité et de performance. Le plus simple peut être de composer les images sous forme de patchwork ou de disposer autrement la page pour que l'utilisateur ait directement accès à l'ensemble des informations qu'on veut lui transmettre.  
* Soyez également vigilants sur [les polices utilisées](https://www.wholegraindigital.com/blog/performant-web-fonts/).   
* Envisagez d'ajouter une fonctionnalité de recherche interne sur votre site si cela peut faciliter la vie de vos utilisateurs. Quitte à faire, essayez de [gérer cette fonctionnalité aussi légèrement que possible]({% post_url 2020-07-01-bricodeur-du-dimanche %}).
* Il y a quelques années, tout le monde voulait un forum. Ensuite, on est passés aux commentaires sur le site. Aujourd'hui, il faut à tout prix faire le lien avec les réseaux sociaux. Est-ce toujours pertinent ou nécessaire?      

Et surtout...
# Ne gardez que les fonctionnalités dont VOS UTILISATEURS ont VRAIMENT besoin.  
  
Les astuces et bonnes pratiques sont nombreuses mais la principale reste de ne pas inclure quelque chose dont l'utilisateur final n'a pas besoin. Celui-ci se rend de toute façon sur votre site dans un but précis et n'a pas besoin d'être noyé sous les informations et gadgets. Essayez donc avant tout d'alléger le parcours utilisateur.   
Bref, là aussi, les changements vont plus loin que l'optimisation technique et doivent être réfléchies dès le lancement du projet et tout au long de celui-ci.

## Conclusions 
Au final, cette série d'audits a déjà permis de fournir des retours concrets sur certains sites web. Au-delà de ça, elle a permis d'arrêter une liste de 3 (ou 4) outils automatiques permettant déjà d'identifier les bonnes pratiques à mettre en oeuvre ainsi que des indicateurs sur l'impact environnemental. De ce point de vue, GreenIT Analysis fait déjà une grosse part du boulot mais Fast or Slow et Wave permettent de qualifier la performance et l'accessibilité du site (qui sont parfois des indicateurs plus parlants et restent en tout cas complémentaires).    
Il en ressort également que des points de vigilance récurrents comme l'optimisation des images (format, taille, etc), du cache et des ressources textuelles (minification, compression) ainsi que des scripts (externes dont trackers).   
Le recueil des 115 bonnes pratiques d'écoconception web reste une référence pour qualifier et prioriser les actions à mettre en oeuvre.       
Au-delà de ces optimisations techniques, la sobriété numérique reste un levier important qui doit intervenir aussi tôt que possible dans la création du site.   
L'idée pour la suite consiste à continuer à communiquer sur ces résultats et à auditer d'autres sites. L'idéal serait que d'autres personnes puissent s'approprier cette stratégie d'audit et l'adapter à leurs besoins. En effet, tout ne s'arrête pas après l'audit, au contraire. 
L'écoconception web intervient tout au long de la création du site et s'inscrit dans une démarche d'amélioration continue. Les audits doivent pouvoir être effectués régulièrement sur un même site, notamment quand celui-ci est modifié (maintenance, évolution, ajout de contenu). 
      
Enfin, je tiens à remercier tous ceux qui ont contribué à ce chantier : l'ADEME, l'agence ICOM , l'Ecole de la Transition Ecologique et Simplon (en particulier SimplonProd, Nicolas Maronnier et les apprenants de Simplon Carbonne).

