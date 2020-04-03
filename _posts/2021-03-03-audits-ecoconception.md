---
layout: post
title:  "Audits d'écoconception - écoconception web, kezako?"
date:   2021-03-03 10:59:53 +0200
categories: green
---

### Ecoconception web 
En général, on parlera plutôt d'écoconception de service numérique, dans la mesure où on travaille sur une unité fonctionnelle. Ici, dans la mesure où notre démarche se limitera aux sites web, nous opérons ce raccourci et parlons d'écoconception web.    L'écoconception web est un process d'amélioration continue visant à minimiser l'impact environnemental d'un site web. Cette approche intervient tout au long du cycle de vie du site web (de l'idée à la fin de vie en passant par la conception et le développement).   
* Dans un premier temps de déterminer si le site web est vraiment utile (sinon, autant s'en passer). 
* Cerner au plus près les fonctionnalités vraiment indispensables. 
* Penser la conception afin d'optimiser le parcours utilisateur : l'internaute doit pouvoir accomplir ce pourquoi il vient sur le site le plus rapidement/facilement possible. 
* L'architecture technique (et le choix de la stack technique) doit être calée au plus près du besoin afin de minimiser les impacts. 
* Le développement doit être effectué en gardant en tête [les bonnes pratiques](https://collectif.greenit.fr/ecoconception-web/115-bonnes-pratiques-eco-conception_web.html).  
* L'hébergeur doit donner des éléments de preuve sur son impact environnemental. C'est presque un sujet à part entière, nous y reviendrons plus tard. 
* Une fois le site en ligne, les ajouts, modifications, corrections ainsi que la communication doivent respecter ce qui a été mis en place pour réduire son impact environnemental. Il faut garder à l'esprit que l'écoconception web est un process, pas un projet. Il est ici vital d'avoir une procédure rapide d'audit d'écoconception afin de pouvoir mesurer régulièrement l'impact du site. 
* Lorsque le site n'est plus utile (événementiel, etc), il n'a pas besoin de rester en ligne.     Souvent, l'écoconception repose uniquement sur les développeurs. Cette démarche n'est pas viable car plus de la moitié des impacts se trouvent en amont de leur intervention. Il est donc essentiel que toute l'équipe intervenant sur et autour du projet soit sensibilisée et que la démarche s'inscrive dans le temps.   
   
Pour un exemple d'audits d'écoconception sur des services numériques et les retours correspondants : [[PDF] GreenConcept](http://www.greenconcept-innovation.fr/wp-content/uploads/2020/02/greenconcept_21022020.pdf)    
#### Bénéfices de l'écoconception web 
Les valeurs et bonnes pratiques du web sont nombreuses. Concernant la notion de qualité web, je me permets de vous orienter [directement vers Opquast](https://www.opquast.com/). Ces valeurs sont liées à l'écoconception web : 
* Accessibilité : s'assurer que le site sera utilisable par tout internaute, quel que soit sa situation. Si l'on veut optimiser le parcours utilisateur, il est indispensable de garder cette notion à l'esprit. De plus, l'écoconception web permet souvent d'alléger un site web, ce qui aide à limiter les risques de non-accessibilité.    
* Performance : l'écoconception web vise souvent l'efficience. En allégeant un site web, on améliore sa performance. En conséquence, le site est plus rapide, l'expérience utilisateur s'améliore et [les conséquences peuvent être très concrètes](https://wpostats.com/). 
* Référencement : lorsqu'un site devient plus accessible pour les utilisateurs, il l'est également pour les robots en charge du référencement. Un site plus rapide sera lui aussi mieux référencé. Inversement, si l'on reste dans l'optique d'optimiser le parcours utilisateur, il est indispensable que l'internaute puisse facilement trouver le site. 
* Sécurité : en allégeant un site, on réduit la surface d'attaque. 
* Finances : les items précédents de cette liste ont déjà en soi un impact financier. De plus, l'écoconception web peut améliorer l'image de marque et s'impose comme facteur de différenciation. D'autant plus, qu'il est essentiel de communiquer autour de cette démarche (ne serait-ce que pour partager les bonnes pratiques et mettre en avant son utilité).
   
*Note :* la performance est un cas particulier. Souvent, dans les mesures, on se rend compte que performance et écoconception sont étroitement liées (notamment au niveau des bonnes pratiques à mettre en place). Attention toutefois à bien différencier les deux. En effet, la performance vise avant tout à rendre le site plus rapide, quitte à ajouter des surcouches et outils pour cela. Dans ce cas, on peut s'éloigner de l'écoconception. On peut donc dire, pour résumer, que l'écoconception rejoint la performance uniquement sur la question de l'efficience. Il s'agit bien d'aller plus vite en allégeant (les contenus, les fichiers transmis au navigateur, etc) plutôt qu'en ajoutant (des outils et autres solutions techniques). Pour autant, il y a donc plein de choses que l'écoconception peut apprendre de la performance. Jusque dans la marche à suivre pour faire entrer la performance dans la culture d'une entreprise et favoriser son adoption auprès des équipes. 
## Quel type d'analyse? 
Comme nous venons de le voir, il est apparu important de mesurer l'impact des sites web car c'est quelque chose que chacun utilise au quotidien. Il en va de même pour les applications mobiles mais l'avantage des sites web est que l'on dispose d'énormément d'outils de mesure (c'est ce que nous verrons dans la partie suivante).    
Pour mesurer un impact environnemental, il est souvent judicieux de parler d'unité fonctionnelle ou de service numérique. Ainsi, on s'intéresse à l'action que cherche à accomplir l'utilisateur : 
* réserver un billet de train aller-retour Toulouse-Bordeaux pour une date et une heure données 
* trouver le numéro de téléphone d'un restaurant libanais près de chez soi 
* Contacter l'entreprise Tartempion 
   
On peut alors s'intéresser au parcours de l'utilisateur et sur les équipements utilisés pour mener ce qu'on appelle [une ACV (Analyse du Cycle de Vie)](https://fr.wikipedia.org/wiki/Analyse_du_cycle_de_vie). Le [cycle de vie d'un produit](https://external-content.duckduckgo.com/iu/?u=https%3A%2F%2Fblog.nicolashachet.com%2Fwp-content%2Fuploads%2F2019%2F12%2Fecoconception-cycle-de-vie-service-numerique-informatique-1013x1024.jpg&f=1&nofb=1) (numérique ou autre) va de sa fabrication à sa fin de vie. Ce type d'analyse très complet permet de prendre en compte tout ce qui sera impactant : le site web mais aussi les équipements utilisés pour y accéder. Dans le cas d'un acte d'achat en ligne, on pourra aussi considérer les ressources utilisées pour emballer le produit et l'amener jusqu'à l'utilisateur.   L'avantage est qu'on a alors une analyse très complète, avec suffisamment d'éléments pour pouvoir grandement diminuer les impacts. De plus, prendre en compte l'ensemble du cycle de vie permet de limiter les risques de transfert d'impact (prévoir un frigo mieux isolé réduit sa consommation d'énergie en cours d'utilisation mais peut augmenter l'impact de sa fabrication). Cependant, ce type d'analyse est complexe et nécessite du temps (souvent plusieurs jours) et des experts (donc un budget conséquent).    
Dans le cas qui nous intéresse, nous avons fait le choix d'une démarche simplifiée. L'idée est de pouvoir analyser un site web dans son ensemble en quelques heures. La démarche ne se veut donc pas forcément exhaustive mais facile à mettre en oeuvre. En particulier, comme je l'indiquais plus haut, par des apprenants en cours de formation au métier de développeur web. La procédure à laquelle nous sommes parvenus (et que nous exposerons plus loin) est accessible pour des néophytes. Si les outils automatiques sont facilement accessibles et utilisables, on notera deux limitations : 
* l'analyse des résultats demande un minimum d'expertise en raison de nombreuses notions techniques 
* le volet sobriété numérique/fonctionnelle demande une certaine expertise aussi et ne peut pas être automatisé. Nous sommes donc partis dans l'idée de trouver une démarche d'audit simplifié de site web. Pour cela, nous nous sommes fixés plusieurs objectifs : 
* identifier les outils automatiques en trouvant le ratio idéal entre le nombre d'outils et leur pertinence 
* identifier des indicateurs mesurables et pertinents (indispensables pour mettre en place une démarche durable d'écoconception web) 
* mettre au point un process d'audit efficace 
   
### Outils identifiés 
On trouve tout un panel d'outils, pour la plupart gratuits, permettant d'analyser un site web. Nous avons décidé de nous concentrer sur plusieurs outils. En priorité, ceux mesurant l'impact environnemental d'un site web voire le respect des bonnes pratiques. Mais aussi les outils de mesure de performance et d'accessibilité (pour l'amélioration de l'expérience utilisateur voire, dans le cas de la performance, pour alléger le site). Enfin, les outils d'audit de SEO/référencement apportent un éclairage intéressant. 
* [webhint](https://webhint.io/) 
* [GreenIT Analysis - Chrome](https://chrome.google.com/webstore/detail/greenit-analysis/mofbfhffeklkbebfclfaiifefjflcpad) 
* [Eco-index - Firefox](https://addons.mozilla.org/fr/firefox/addon/ecoindex/) 
* [web.dev](https://web.dev/measure): l'équivalent en ligne des outils présentés dans les chrome dev tools > audits et fournis par [Lighthouse](https://developers.google.com/web/tools/lighthouse/). Utilise aXe pour l'accessibilité. L'avantage de la version en ligne est de permettre de générer un rapport consultable par la suite. 
* [Sucuri](https://sitecheck.sucuri.net/) 
* [Dareboost](https://www.dareboost.com/en) 
* [Validator HTML W3C](https://validator.w3.org/) 
* [GTmetrix](https://gtmetrix.com/) : inclut PageSpeed et YSlow. 
* [Wave](http://wave.webaim.org/) 
* [WebsiteCarbon](https://www.websitecarbon.com/) 
* [WebPageTest](https://www.webpagetest.org/) 
* [PageSpeedInsights](https://developers.google.com/speed/pagespeed/insights/) 
* [Pingdom](https://tools.pingdom.com/) 
* [Yellow Lab](https://yellowlab.tools/) 
* [ThinkWithGoogle](https://www.thinkwithgoogle.com/feature/testmysite/) 
* [Mobile-friendly](https://search.google.com/test/mobile-friendly) 
* [WPScan](https://wpscan.org/) 
Pour les tous premiers audits, nous avons fait le choix d'utiliser tous ces outils pour ensuite pouvoir réduire la liste. Pour cela, nous avons évalué la pertinence des remontées de chaque outil du point de vue de l'écoconception web mais aussi été vigilants sur les outils qui peuvent parfois remonter les mêmes éléments que d'autres outils. Notamment dans le cas de certains outils comme Lighthouse qui effectuent de nombreuses mesures très pertinentes, dans des domaines très différents. 
   
#### Le cas particulier du CSS inutilisé 
Le pourcentage de CSS inutilisé est un bon indicateur mais [reste difficile à mesurer](https://css-tricks.com/how-do-you-remove-unused-css-from-a-site/). En effet, à quoi bon envoyer au navigateur du code qui ne sera jamais utilisé? Les premiers outils trouvés étaient les suivants : 
* [Détecter le CSS inutilisé à la main](https://web.dev/unused-css-rules/): très long et nécessite une très bonne connaissance du projet 
* [PurifyCSS](https://purifycss.online/#) 
* [JitBit-UnusedCSS](https://www.jitbit.com/unusedcss/)       
Chacun présente ses propres défauts, notamment liés au fait que le test n'est lancé que sur une seule page (le CSS pourrait donc être utilisé sur une autre page) voire ne prend pas en compte le JS (ce qui pose souci par exemple quand une partie du DOM est manipulée ou générée par le JS).   
La meilleure solution serait de déléguer cette tâche à un développeur connaissant bien le projet et d'incorporer cette démarche tout au long du process de développement et de maintenance.  

Sinon, [Purgecss est relativement complet](https://www.purgecss.com/), sans être parfait. Il doit obligatoirement être incorporé au process de développement ou nécessite au moins d'avoir accès au code.  
Dans le cadre des audits, PurifyCSS et UnusedCSS ont été utilisés en gardant à l'esprit que les résultats sont dans la plupart des cas trop élevés (soit parce que l'outil ne mesure qu'une page du site ou parce qu'il ne tient pas compte du JS).  
   
### Indicateurs 
Souvent, pour mesurer l'impact environnemental du numérique et plus particulièrement d'un site web, on utilise les indicateurs suivants : 
* Taille de la page 
* Nombre de requêtes HTTP 
* Nombre d'éléments dans le DOM    
On en déduit [l'écoindex](http://www.ecoindex.fr/), une estimation de la production de gaz à effet de serre (en équivalent CO2) et la consommation d'eau (en cl).   
Comme nous l'avons vu, nous pouvons aussi regarder du côté des indicateurs liées à la performance, à l'accessibilité voire au référencement. Dans l'optique d'améliorer l'expérience utilisateur (et étant donné la proportion d'internautes accédant aux sites depuis leurs smartphones), nous avons été vigilants à l'aspect responsif.       
Dans tous les cas, le fait de faire plusieurs audits avec un panel très large d'outils a permis de dégager un ensemble d'indicateurs et de trier parmi ceux-ci les plus pertinents.  
   
### Procédure d'audit 
Comme nous l'avons vu sur les différents types d'analyse possible, nous avons fait le choix de partir sur un audit simplifié de site web. Une fois les outils identifiés et une idée des indicateurs en tête, il reste à voir comment procéder pour chaque site.   
Il est possible de s'appuyer sur plusieurs ressources : 
* [Le RGAA (Référentiel Général d'Amélioration de l'Accessibilité](https://www.numerique.gouv.fr/publications/rgaa-accessibilite/obligations/#%C3%89chantillon) décrit comment constituer un échantillon de test 
* [Le cours OpenClassrooms sur le GreenIT](https://openclassrooms.com/fr/courses/6227476-appliquez-les-principes-du-green-it-dans-votre-entreprise/6699634-reduisez-l-empreinte-ecologique-de-votre-site-web) décrit lui aussi comment mener une démarche d'audit.     
**Au passage, ce cours vaut le détour et permet en plus d'aborder rapidement et concrètement le sujet de l'écoconception de service numérique.**  
En conséquence, il a été décidé de distinguer plusieurs cas : 
* Si le site ne contient qu'une seule page, il suffit d'analyser cette page 
* Si le site est composé de plusieurs pages, la page d'accueil est incontournable. Il faut ensuite déterminer un échantillon d'environ 5 pages parmi les plus visitées. Parfois, ce ne sont pas forcément les plus utiles du point de vue du client (et inversement). Avoir des statistiques sur l'utilisation du site (Google Analytics, Matomo ou autres) peut constituer un bon point de départ pour identifier les pages à analyser en priorité.    
Dans tous les cas, il peut être bon de discuter avec le propriétaire du site des unités fonctionnelles qu'il a en tête pour son site. Il faut en effet garder en tête le besoin auquel répond le site et le parcours utilisateur qui va en découler. Ce sera un levier important pour proposer des axes d'amélioration de l'expérience utilisateur. 

### Dichotomie Client/Utilisateurs (et l'écoconception au milieu) 
Parfois, les attentes du propriétaire du site (ou client) et des utilisateurs ne sont pas les mêmes. C'est pour cela qu'on trouve des [Dark Patterns](https://www.darkpatterns.org/), de la pub et des trackers sur les sites par exemple.   
Ces éléments nuisent généralement à l'expérience utilisateur et bien souvent à l'écoconception web.    Ceci n'empêche pas de les mentionner dans les préconisations, en fournissant les arguments au client pour qu'il fasse un choix éclairé lorsqu'il s'agira de les conserver ou pas.     
Il en va de même pour tout ce qui a trait à la communication responsable. L'internaute ne se lève pas le matin en ayant le besoin impérieux d'être bombardé de pubs, de vidéos et fils Twitter/Facebook/Instagram. Il est indispensable que le client connaisse les conséquences de ces choix mais la décision finale lui revient.   
   
## Echantillon de départ 
Pour lancer ce chantier autour de l'audit de sites web, nous disposions de plusieurs sites. La présence de nombreux sites Wordpress dans le lot (ce qui, statistiquement, est logique vu que Wordpress représente une grosse part du marché) a incité à ajouter [WPScan](https://wpscan.org/) aux outils utilisés et à prévoir un process particulier (voir plus loin).    
La liste des sites (un ou deux qui sont arrivés en cours de route) :  

### ADEME 

#### Observatoire DPE [Observatoire DPE](https://www.observatoire-dpe.fr/)     
         
| Page testée | Perf environnementale | Complexité (nb d'elts sur la page) | Bande passante (poids de la page)    | Charge serveur (nb de req HTTP) | Empreinte GES (gC02e) | Empreinte eau (cl) |    
| ------ | ------ | ------ | ------ | ------ | ------ | ------ |   
| Accueil | 77 (A) | 216 |633 Ko | 24 |1.46 |2.19 |  


*(source : GreenIT-Analysis)*   
[PageSpeed Index :](https://developers.google.com/speed/pagespeed/insights/) 76 
* La page "Simuler un DPE" est-elle vraiment utile? 
* La page "Rechercher un diagnostiqueur" (redirection vers un autre site) mériterait sûrement un audit à part entière mais non-prioritaire car l'ADEME n'a pas forcément la main dessus. Les optimisations techniques à explorer sont : 
* Optimisation des images (format, taille et en regrouper autant que possible dans un sprite CSS). 
* Externalisation, nettoyage, minification et compression des assets (HTML/CSS/JS). Y compris pour les librairies externes. 
* Mise en place d'une politique de cache. 
* Mise à jour de jQuery (envisager si possible une alternative plus légère). 
* Corriger les erreurs dans le HTML : id dupliqués, valign erroné, libellés manquants. 
* Ajouter une meta-description dans le HTML. 
* Optimiser HTML/CSS pour usage mobile. 
* [Accessibilité] Ajouter les libellés manquants sur le formulaire de connexion 
* [Accessibilité] Remédier aux erreurs de contraste de couleurs.   
   
Si possible: 
* sortir de Google Analytics (mesurer la pertinence des indicateurs récupérés, envisager de passer sur Matomo). 
* Différer le chargement de certains scripts.   
#### Simul'aid€s 
[Simul'aid€s](http://www.normandie.infoenergie.org/vos-aides/simuler-vos-aides/)     
(audit réalisé par Morgane Echeveste, apprenante à Simplon Carbonne)       
   
| Page testée | Perf environnementale | Complexité (nb d'elts sur la page) | Bande passante (poids de la page) | Charge serveur (nb de req HTTP) | Empreinte GES (gC02e) | Empreinte eau (cl) |   
| ------ | ------ | ------ | ------ | ------ | ------ | ------ |   
| Accueil | 53.3 (C) | 329 |3130 Ko | 70 |1.93 |2.9 |    
    
*(source : Ecoindex)* 
[PageSpeed Index :](https://developers.google.com/speed/pagespeed/insights/) 4    
* Le site est alourdi par des nombreux scripts JS et autres feuilles de style CSS externalisés et non-compressés.    
* Des images non-optimisées sont présentes.   
* La mise en cache doit être mieux configurée (pour éviter de charger plusieurs fois certains éléments depuis le serveur). 
* Le parcours utilisateur est long et complexe, ce qui alourdit d'autant l'impact environnemental du site.   
Au final, on a un site qui est dans la moyenne et qui pourrait facilement arriver sur un Eco-index B voire A moyennant quelques optimisations techniques. Toutefois, les plus gros gains pourraient avoir lieu en revoyant le parcours utilisateurs.   

### Simplon 
#### Simplon4all 
[Simplon4all](https://simplonforall.simplon.co/)           
   
| Page testée | Perf environnementale | Complexité (nb d'elts sur la page) | Bande passante (poids de la page) | Charge serveur (nb de req HTTP) | Empreinte GES (gC02e) | Empreinte eau (cl) |   | ------ | ------ | ------ | ------ | ------ | ------ | ------ |    
| Accueil | 72.7 (B) | 161 |1339 Ko | 35 |1.55 |2.32 |     
     
*(source : Ecoindex)* 
[PageSpeed Index :](https://developers.google.com/speed/pagespeed/insights/) 99 
* Le bandeau en haut de page prend énormément de place alors qu'il n'apporte que peu d'infos. 
* Le choix de faire un site statique en une page est top mais attention à la stack technique utilisée (Larave+Vue.js?). Regarder par exemple la [JAMstack](https://jamstack.wtf/). Les optimisations techniques à explorer sont : 
* Revoir le cache
* Eviter le @import de CSS 
* Optimiser les images (taille et format, prévoir en plus le lazy-load sur celles qui sont below the fold) 
* Optimiser le CSS (sélecteurs inutilisés, minifier, compresser) 
* Attention au contraste des couleurs 
* 1 erreur HTML à corriger 
* Optimiser les fonts custom (subset) 

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
Très bien, quasiment rien redire. 
* Redimensionner les images avec une hauteur de 100px (=> alléger la page) 
* Rassembler les images résultants dans un seul sprite CSS (=> diminuer de moitié le nombre de requêtes HTTP) 
* Ajouter les directives de cache pour les svg et la page d'accueil 
* Externaliser, minifier et mettre en cache les parties communes du CSS et du JS 
* Fournir une feuille print CSS (avec media-query HTML>link et CSS), d'autant plus que le site contient essentiellement du texte. 
* Corriger l'erreur JS résiduelle. 
* 2 polices de caractères spécifiques sont utilisées. Elles pourraient être remplacées. 

#### Simplon Inside 
Il s'agit là d'un portail interne réservé aux employés Simplon.    
            
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
Pour le cas particulier de Wordpress, je me permets de vous renvoyer à un article publié ici-même : [Wordpress et éco-conception](https://ldevernay.github.io/green/2019/12/13/wordpress_eco.html)       

### Act for Climate 
[Le site de l'événement Act for climate](https://www.act-for-climate.fr/)       
          
| Page testée | Perf environnementale | Complexité (nb d'elts sur la page) | Bande passante (poids de la page) | Charge serveur (nb de req HTTP) | Empreinte GES (gC02e) | Empreinte eau (cl) |   
| ------ | ------ | ------ | ------ | ------ | ------ | ------ |    
| Accueil | 26 (E) | 1251 |3498 Ko | 71 |2.48 |3.72 |     
   
*(source : Ecoindex)* 
[PageSpeed Index :](https://developers.google.com/speed/pagespeed/insights/) 31 
* Eviter d'inclure une vidéo sur la page d'accueil du site (image + lien vers la vidéo). 
* Limiter encore plus le nombre d'intervenants sur la page d'accueil. 
* Beaucoup d'images donc peut-être nécessaire de découper en plusieurs pages. 
* S'assurer de ne pas garder des plugins inutiles. 

Etant donné qu'il s'agit encore une fois d'un site Wordpress, les optimisations techniques reposent sur l'installation des plugins adéquats (W3 Total Cache, Smush, etc) afin d'optimiser la compression des ressources, les images et le cache (entre autres). 
Le thème devrait être modifié pour un autre plus accessible et léger. 

## Process retenu 
Nous sommes donc ressortis de ces audits avec de nombreuses informations. Restait à faire un peu de tri dans tout ça.    

### Les outils retenus         
Chaque outil d'audit renvoie de nombreux indicateurs.    
Nous avons retenu ceux qui vont dans le sens de l'écoconception (alléger ce qui est envoyé au client, améliorer le SEO et l'accessibilité). Afin de mieux identifier les bonnes pratiques à mettre en place mais aussi de les prioriser, il est possible d'avoir recours au [recueil des 115 bonnes pratiques d'écoconception](https://collectif.greenit.fr/ecoconception-web/115-bonnes-pratiques-eco-conception_web.html).       
Il semblerait judicieux de privilégier un outil comme web.dev qui permet de mesurer simultanément la performance, les bonnes pratiques, le SEO et l'accessibilité. Cependant, cet outil est moins visuel et concret que d'autres outils plus spécialisés. Au final, nous avons réussi à identifier un panel d'outils, moyennant quelques cas particuliers à prendre en compte.    
* [GreenIT Analysis](https://chrome.google.com/webstore/detail/greenit-analysis/mofbfhffeklkbebfclfaiifefjflcpad) : idéal pour mesurer des indicateurs d'écoconception sur une page donnée et vérifier les bonnes pratiques. La version Chrome du plugin est à privilégier car plus complète. Pour mesurer un parcours utilisateur, peut être moins pratique que [le plugin Ecoindex](https://addons.mozilla.org/fr/firefox/addon/ecoindex/). 
* [PageSpeed Insights :](https://developers.google.com/speed/pagespeed/insights/) très bien pour mesurer la performance et obtenir des recommandations concrètes ainsi que les bénéfices attendus suite à leur mise en application. [Pingdom](https://tools.pingdom.com) ou [GT Metrix](https://gtmetrix.com/analyze.html) peuvent être utilisés en complément, de même que les DevTools Firefox ou Chrome. 
* [Wave](https://wave.webaim.org/) : permet de mesurer l'accessibilité. 
* Pour les sites Wordpress et à défaut de disposer d'un accès à l'administration, [WPScan](https://wpscan.org/) permet d'avoir un aperçu des plugins installés et du thème utilisé. Même si ceci permet également de vérifier s'il existe des failles de sécurité, le plus simple reste de demander ces informations directement au propriétaire du site concerné par l'audit.   
Au final, les autres outils ont été laissés de côté. A l'usage, il n'a pas semblé pertinent de mesurer directement liés au SEO (car les bénéfices sur le SEO se retrouvent essentiellement en agissant sur l'écoconception, notamment performance et accessibilité) et à la sécurité (car il s'agit plutôt d'un effet secondaire appréciable de l'écoconception).

### Les indicateurs   
Comme indiqué plus haut, nous avons choisi de mettre en avant les indicateurs suivants : 
* Taille de la page 
* Nombre de requêtes HTTP 
* Nombre d'éléments dans le DOM 
* Eco-index 
* Emission de gaz à effet de serre en équivalent CO2 
* Consommation d'eau 
* PageSpeed Index      

Sur ce dernier, il peut être pertinent d'aller plus précisément vers des indicateurs de performance plus précis si le propriétaire du site peut être plus réceptif sur ce sujet (First Contentful Paint, Time to Interactive ou autre).    
L'idée générale pour ces indicateurs est de fournir des éléments de comparaison et, au-delà des bonnes pratiques, d'avoir des ordres de grandeur dont on pourra mesurer l'évolution au fil du temps.     
### Ce qu'il faut auditer 
Comme nous l'avons vu plus haut, plusieurs cas se dessinent : 
* Si le site ne contient qu'une seule page, il suffit d'analyser cette page 
* Si le site est composé de plusieurs pages, la page d'accueil est incontournable. Il faut ensuite déterminer un échantillon d'environ 5 pages parmi les plus visitées. Parfois, ce ne sont pas forcément les plus utiles du point de vue du client (et inversement). Avoir des statistiques sur l'utilisation du site (Google Analytics, Matomo ou autres) peut constituer un bon point de départ pour identifier les pages à analyser en priorité. 
* Si des parcours utilisateur clairs se précisent, il faut auditer l'ensemble chacun de ces parcours en détail (contactez l'administrateur du site, commander un article, effectuer une réclamation, trouver un trajet, etc).          

### Conclusion 
On se retrouve donc avec un set de 3 outils dont la plupart peuvent être installés directement dans le navigateur pour plus de commodité.              
En renfort, une fois de plus, le recueil des 115 bonnes pratiques permet de faire du tri dans les bonnes pratiques et de les prioriser (en évaluant l'impact de chacune, ce qui peut être confirmé à l'usage par ce que propose PageSpeed Insights).   
Toutefois, on reste ici sur des pistes d'optimisations techniques. Comme nous l'avons déjà vu, l'écoconception web doit être abordée de façon transverse : avec tous les membres de l'équipe projet, sur toutes les phases du cycle de vie.   
Au cours d'un audit, on pourra ainsi fournir des préconisations sur : 
* La stack technique (mais c'est souvent difficile à mettre en oeuvre dès lors qu'on a commencé à développer le site) 
* L'hébergeur (même si le client va parfois rechigner à en changer) 
* La sobriété fonctionnelle (ce qui peut être retiré ou modifié pour alléger le site et/ou le parcours utilisateur) 

## Stack technique 
Le choix des outils utilisés constitue une étape fondamentale et trop souvent survolée. Parce qu'on reste sur ce qu'on connaît, parce qu'on veut tester le dernier outil à la mode ou parce qu'on ne nous laisse pas forcément le choix.    
Il n'y a pas forcément d'outil ultime qui viendra résoudre tous les problèmes d'un coup. Il n'y a que peu d'outils qui soient intrinséquement de mauvais choix. En revanche, il est important d'avoir pu appliquer en amont les principes d'écoconception web et en particulier de sobriété fonctionnelle afin de choisier l'outil qui correspondra le mieux au besoin du client.     
Actuellement, quelques outils autour des PWA et de la JAMSTACK ont le vent en poupe. En parallèle, beaucoup dénigrent Wordpress. Pour autant une JAMSTACK mal utilisée aura un impact écologique plus désastreux qu'un Wordpress correctement pensé pour l'écoconception.           

## Hébergeur 
Lorsque l'on cherche à réduire l'impact environnemental de son site web, l'hébergeur est une question cruciale. Dans l'idéal, il faut trouver un entreprise locale (ou pas loin) qui prenne des engagements sur la question (et fournisse si possible des éléments de preuve).    
En s'en tenant à ces deux critères, on trouve en France (ou à proximité) principalement deux candidats : 
* [Infomaniak](https://www.infomaniak.com/fr/hebergeur-ecologique/charte-ecologique) 
* [O2Switch](https://www.o2switch.fr/)      
(avec une préférence pour le premier)    

## Sobriété fonctionnelle 
Des retours d'expérience commencent à paraître un peu partout. C'est une très bonne chose car, petit à petit, ces informations aident à se construire des bonnes pratiques sur le volet de la sobriété numérique. Ceci ne peut pas être mesuré ni automatisé, même si c'est souvent là que vont se trouver les plus gros impacts. Ainsi, au cours des audits, il est fréquent de repérer des éléments qui n'apportent que peu ou pas à l'utilisateur (voire qui nuisent à l'UX) : les pubs et trackers, les vidéos à outrance, etc. De même qu'on connaît (de plus en plus) les Dark Patterns qui viennent gâcher l'expérience utilisateur (à des fins de manipulation, ni plus ni moins), peut-être pouvons-nous déjà lister quelques mauvaises pratiques liées à la sobriété fonctionnelle. 
* L'affichage de fil Twitter/Facebook/Instagram est souvent lourd, d'autant plus qu'il apporte son lot de trackers et de scripts. 
* Même chose pour les boutons de partage sur les réseaux sociaux proposés par les réseaux en question. 
* Les vidéos (qui proviennent le plus souvent de Youtube) doivent être au moins [optimisées au préalable](http://carbonclap.ecoprod.com/). L'autoplay est à proscrire absolument, entre autres pour des raisons d'accessibilité. Le plus simple peut être de proposer une image (extraite de la vidéo) permettant de cliquer dessus pour accéder directement au site où se trouve la vidéo. 
* Les cartes Google Maps apportent de nombreuses fonctionnalités mais aussi de scripts, feuilles de style et trackers. Le plus souvent une simple image suffit pour aider l'internaute à localiser des endroits. Un clic sur l'image peut conduire à Google Maps. A noter que des alternatives libres et gratuites comme OpenStreetMap existent. 
* Les images doivent être retaillées et optimisées au préalable. Le format WebP, par exemple, est de mieux en mieux supporté et bien plus léger que ses "ancêtres". 
* Si Google Analytics est utilisé, il revient de se demander quels indicateurs sont réellement utiles. Si ces indicateurs sont indispensables, il peut être intéressant de se tourner vers une alternative plus éthique comme [Matomo](https://matomo.org/). Des alternatives plus légères comme [Volument](https://volument.com/) méritent également qu'on s'y intéresse. 
* jQuery est souvent à proscrire (en raison de sa lourdeur et de ses failles de sécurité). Des alternatives plus légères existent, comme [Cash](https://github.com/kenwheeler/cash). Plus généralement, [le site microjs](http://microjs.com/#jquery) propose des alternatives plus légères à de nombreuses librairies JS. 
* [Les carousels](http://shouldiuseacarousel.com/) posent souvent des soucis d'accessibilité et de performance. Le plus simple peut être de composer les images sous forme de patchwork ou de disposer autrement la page pour que l'utilisateur ait directement accès à l'ensemble des informations qu'on veut lui transmettre.         

Les astuces et bonnes pratiques sont nombreuses mais la principale est de ne tout simplement pas inclure quelque chose dont l'utilisateur final n'a pas besoin. Celui-ci se rend de toute façon sur votre site dans un but précis et n'a pas besoin d'être noyé sous les informations et gadgets.  

## Conclusions 
Au final, cette série d'audits a déjà permis de fournir des retours concrets sur certains sites web. Au-delà de ça, elle a permis d'identifier une liste de 3 (ou 4) outils automatiques permettant déjà d'identifier les bonnes pratiques à mettre en oeuvre ainsi que des indicateurs sur l'impact environnemental. De ce point de vue, GreenIT Analysis fait déjà une grosse part du boulot mais PageSpeed Insights et Wave permettent de qualifier la performance et l'accessibilité du site (qui sont parfois des indicateurs plus parlants et restent en tout cas complémentaires).    
Il en ressort également que les principaux points de vigilance concernant l'impact écologique sont l'optimisation des images (format, taille, etc), du cache et des ressources textuelles (minification, compression), les scripts (externes dont trackers).   
Le recueil des 115 bonnes pratiques d'écoconception web reste une référence pour qualifier et prioriser les actions à mettre en oeuvre.       
Au-delà de ces optimisations techniques, la sobriété numérique reste un levier important qui doit intervenir aussi tôt que possible dans la création du site.   
L'idée pour la suite consiste à continuer à communiquer sur ces résultats et à auditer d'autres sites. L'idéal serait que d'autres personnes puissent s'approprier cette stratégie d'audit ou l'adapter à leurs besoins. En effet, tout ne s'arrête pas après l'audit, au contraire. 
L'écoconception web intervient tout au long de la création du site et s'inscrit dans une démarche d'amélioration continue. Les audits doivent pouvoir être effectués régulièrement sur un même site, notamment quand celui-ci est modifié (maintenance, évolution, ajout de contenu). Nous y reviendrons dans des articles ultérieurs évoquant la place de l'écoconception web dans le cycle de vie d'un site, l'importance de se fixer un budget d'écoconception ainsi que sur l'importance de raisonner en termes de service numérique.     
Enfin, je tiens à remercier tous ceux qui ont contribué à ce chantier : Simplon (en particulier SimplonProd, Nicolas Maronnier et les apprenants de Simplon Carbonne), l'ADEME, l'agence ICOM et l'Ecole de la Transition Ecologique.


