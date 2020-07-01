---
layout: post
title:  "Wordpress et éco-conception"
date:   2019-12-13 10:59:53 +0200
categories: green
description : Wordpress, c'est super, on peut tout faire avec. Mais ce n'est pas une raison pour faire n'importe quoi. Voici donc quelques pistes pour réduire l'impact environnemental d'un site Wordpress.
---

Wordpress, c'est super, on peut tout faire avec. Mais ce n'est pas une raison pour faire n'importe quoi. Ca fait donc un petit moment que je me pose la question d'un Wordpress éco-conçu.    
Quand on commence à aborder l'éco-conception et qu'on entend parler de Wordpress, la première réaction est souvent de sortir les fourches et les torches. C'est un peu radical et ça reviendrait à laisser de côté ceux qui n'ont pas le choix. Je parle en particulier de ceux qui sont experts en Wordpress et ne se voient pas changer de techno du jour au lendemain. Sont également concernés ceux qui ont déjà un site Wordpress et qui aimeraient limiter les dégâts (et les dépenses).    
Arrivés là, on a plusieurs possibilités : 
* continuer à faire du Wordpress mais se débrouiller pour le faire plus proprement
* continuer à faire du Wordpress mais avec un prestataire qui l'allège à votre place
* passer sur une autre techno

## Wordpress forever
Si vous voulez à tout prix créer un nouveau site Wordpress aussi léger que possible, [voici un article qui résume très bien tout ce qui est possible](https://www.capybara.consulting/2019/12/10/l-eco-conception-en-wordpress-c-est-possible/).   
C'est vraiment un super article qui vous donne toutes les clés pour améliorer votre site dès la conception et vous indique aussi tous les outils pour valider que ce que vous avez fait va dans le bon sens.    
Ce qu'il en ressort, c'est qu'il faut si possible s'y mettre dès la conception en limitant les ressources visuelles (images, vidéos, etc), faire attention aux plugins qu'on installe et bien choisir son thème. Sur ce dernier point, [certains vont très loin](https://blog.jacklenox.com/2018/06/04/delivering-wordpress-in-7kb/).     
Au final, il y a vraiment moyen de faire beaucoup mieux avec tout un panel de thèmes et de plugins gratuits. Alors autant ne pas s'en priver.    
Comme d'habitude avec les sites web, évitez les gadgets trop gourmands : 
* les vidéos non-optimisées et à volonté (et bannissez l'autoplay)
* une map google (à la limite, remplacez-la par une image + un lien vers la map google)
* les caroussels, c'est poubelle (ça, c'est du slogan accrocheur! Je le range avec "quand je vois jQuery, je vomis") 
* attention à Google Analytics
* [allez-y mollo sur les pubs](https://www.greenit.fr/2015/09/01/la-publicite-represente-39-du-poids-des-pages-web/)
* limitez le nombre d'éléments affichés (articles, photos, produits, etc)
* Si vous devez afficher des articles, contentez-vous d'un extrait   
Pensez aussi à retirer les fonctionnalités inutiles.   

Certaines optimisations techniques ont aussi toutes les chances de vous faciliter la vie : 
* Wordpress propose [des plugins pour optimiser les images](https://www.wholegraindigital.com/blog/best-image-optimiser-2018/)
* Il y a également ce qu'il faut optimiser le cache mais [W3 Total Cache](https://wordpress.org/plugins/w3-total-cache/) a le mérite d'être efficace et gratuit. Il existe bien sûr des alternatives, notamment si vous êtes prêts à payer.    
Pour finir, [un article qui donne plein de pistes d'amélioration](https://www.sparringmind.com/speed-up-wordpress/). J'ajouterais juste par rapport à l'article sur Wordpress et éco-conception, la nécessité de [choisir un plugin pour la sécurité](https://www.codeinwp.com/blog/sucuri-vs-wordfence-vs-malcare/). 

### Bonus
Si vous partez dans la folle aventure d'optimiser votre Wordpress, sachez que certains ont déjà tenté l'aventure : 
* [Romain Petiot](https://www.youtube.com/watch?v=CbGCG0glAnc)
* [Wholegraindigital](https://wordpress.tv/2019/06/11/a-study-in-green/)

### Attention!!!
Même si vous appliquez la sobriété fonctionnelle et que vous faites toutes les optimisations imaginables pour que votre site soit aussi éco-conçu que possible, n'oubliez pas que le process d'éco-conception couvre toutes les étapes du projet. Ainsi, n'oubliez pas de sensibiliser ceux qui maintiennent le site (pour ne pas voir apparaître un élémént trop gourmand qui viendra gâcher une bonne partie de vos efforts) mais aussi ceux qui produisent du contenu pour votre site.    
Enfin, rappelez-vous que l'éco-conception est aussi une affaire de compromis (avec le client, les utilisateurs, les designers, etc). La meilleure solution possible serait de ne pas créer le site mais proposer un site sans aucun contenu visuel risque de ne pas être satisfaisant pour l'utilisateur final non plus.    
Ok, venant de quelqu'un qui a choisi de n'avoir aucune image ou vidéo sur son site, c'est un peu limite.   

## Ceux qui peuvent le faire à votre place
De plus en plus, on voit apparaître des offres de prestataires qui proposent de créer ou modifier votre site Wordpress pour qu'il tende davantage vers l'écoconception. Je ne suis pas là pour faire de la pub mais en voici tout de même deux qui savent de quoi ils parlent : 
* [WP°GREEN à Toulouse](https://wp-green.fr/)
* [I Have a Green à Nantes - pour info, c'est Romain Petiot](https://ihaveagreen.fr/offre-wp-eco-start-600/)    
Il y en a sûrement d'autres, qu'ils n'hésitent pas à me contacter.   

## Wordpress à la poubelle
Le grand jour est arrivé et vous décidez d'aller voir du côté des autres outils disponibles. Avant que vous ne fassiez le tour des autres CMS (même si [Translucide vaut le coup d'oeil](https://www.translucide.net/)), laissez-moi vous suggérer le truc qui va vous faciliter la vie et vous permettre de briller en soirée : la JAMSTACK.
* [La quoi?!](https://jamstack.wtf/)
* [Un super bouquin gratuit sur le sujet chez O'Reilly](https://www.netlify.com/oreilly-jamstack/)
* [Les outils pour ça](https://css-tricks.com/jamstack-tools-and-the-spectrum-of-classification/)

En gros, vous allez servir des pages statiques aux utilisateurs (ce qui est très léger de base), tout en trouvant des solutions pour que les administrateurs et créateurs de contenus aient accès à une interface qui ne va pas trop les dépayser. 
* [Passer de Wordpress à Hugo](https://jamstatic.fr/2019/02/06/de-wordpress-a-hugo-un-nouvel-etat-d-esprit/)
* [Une interface admin qui dépote](https://forestry.io/)
* [Un exemple de site de e-commerce](https://ecommerce-netlify.netlify.com/) et le [mode d'emploi](https://css-tricks.com/lets-build-a-jamstack-e-commerce-store-with-netlify-functions/)

En revanche, attention, ce n'est pas parce que vous optez pour la JAMSTACK que vous aurez automatiquement une solution éco-conçue. Gardez en tête la sobriété et méfiez-vous des services en ligne censés vous faciliter la vie. En revanche, en tant que développeur, vous pourrez tirer pleinement profit de votre workflow (et de git) pour gagner considérablement en efficacité. 

## Conclusion
Wordpress n'est pas une fin en soi et, si vous restez sur cette voie, faites-le en connaissance de cause. Les outils gratuits pour alléger l'outil et améliorer l'expérience utilisateur sont nombreux. Prenez-en connaissance et vous verrez qu'ils sont faciles à mettre en oeuvre. Les clients et utilisateurs vous en remercieront. 