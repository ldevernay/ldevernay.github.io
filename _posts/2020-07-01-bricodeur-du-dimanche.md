---
layout: post
title:  Le bricodeur du dimanche
date:   2020-07-01 08:59:53 +0200
categories: green
description: Dans cet article, je vous explique comment j'ai bidouillé mon site pour qu'il fasse tout comme les grands tout en gardant un impact environnemental aussi limité que possible. 
---

Après deux articles sur les audits d'éco-conception, une pause s'impose.  
Le saviez-vous? "Bricodeur" était pressenti comme magnifique néologisme pour traduire "hacker".  
Bref, voici un petit topo sur comment l'éco-conception peut servir à se triturer le cerveau pour rendre des trucs simples stimulants à développer.  

## A la recherche du billet perdu
Quand on s'intéresse à la qualité web et à l'éco-conception, tout le monde vous le dira : il vous faut un outil de recherche interne sur votre site. A ce sujet, [voir la bonne pratique 163 d'Opquast](https://checklists.opquast.com/fr/qualiteweb/le-site-propose-un-moteur-de-recherche-interne).   
A première vue, on se dit "ok, Jekyll doit bien avoir un petit plugin pour ça". Et puis, deux constats s'imposent rapidement : 
* il faut éviter de multiplier les plugins (pour garder en tête l'impact environnemental du site)
* la plupart des gens utilisent des services tiers pour la recherche interne (Google, Algolia ou autres). 
  
Bref, deux bonnes raisons de chercher une alternative. 
Celle-ci existe et elle est plutôt astucieuse : [Jekyll Instant Search](https://blog.webjeda.com/instant-jekyll-search/).  
L'idée est vraiment chouette : 
* On utilise le moteur Liquid de Jekyll pour générer un fichier JSON qui contient les infos (titre, url, description, tags, etc) des billets du site lors du build
* On crée un petit script avec un peu d'AJAX au niveau du champ de recherche pour filtrer le fichier JSON et proposer les résultats correspondants
* On intègre le script dans une page dédiée pour ne pas alourdir le site

La mise en place demande un peu de bricolage mais ce n'est vraiment pas compliqué et c'est surtout très élégant et léger.  
J'en ai profité pour ajouter une description sur tous mes billets, ce qui permet au passage de l'afficher dans la liste des billets et de rendre l'affichage un peu plus parlant.   
Bref, [la recherche, c'est fait](/search.html).  

## Apprendre à compter (version Node.js)
Récemment, je travaillais avec apprenants sur un projet pédagogique très intéressant : proposer une appli mobile permettant à des SDF et autres personnes en situation de précarité de localiser autour d'eux les services et ressources disponibles.  
Déjà, le principe est top.   
Ensuite, histoire de proposer quelque chose de propre, léger et qui tienne le coup en l'absence d'internet, j'avais décidé de pimenter le truc en proposant aux apprenants de [créer une PWA]({% post_url 2019-09-16-pwa %}).  
Tout se passe bien jusqu'au moment où le client demande s'il peut avoir un décompte des installations effectuées. Dans l'absolu, rien d'insurmontable. Sauf si on veut rester sur l'idée d'un site aussi statique et léger que possible, sans avoir recours à des services tiers (bye bye Google... et les autres).   
Cette fois, j'ai trouvé la solution [chez Flavio Copes](https://flaviocopes.com/count-visits-static-site/). Si vous ne le connaissez pas déjà, allez sur son site, c'est très complet sur le développement web.  Et, une fois de plus, on voit bien que DuckDuckGo est le meilleur ami du développeur quand il s'agit de trouver des réponses à des questions très tordues/spécifiques.  
La solution en question consiste reprendre une veille astuce de mails commerciaux, à savoir une image invisible (un SVG d'un pixel de côté) chargé depuis un autre serveur. Le serveur en question est un simple serveur Node.js/Express qui incrémente un compteur à chaque fois que l'image est chargée.   
Le défaut de la solution d'origine était que le compteur était remis à zéro à chaque redémarrage/modif du serveur. J'ai donc pris le parti de l'écrire directement dans un fichier JSON, ce qui laisse de plus la porte ouverte pour faire du comptage un peu plus subtil par la suite.  
Histoire de ne pas s'embêter, le serveur est directement hébergé chez [Glitch](https://www.glitch.com).   
Au final, j'ai donc trouvé une solution technique très basique pour compter les vues sur mon site perso et qui sera réutilisable pour la PWA. Je me dis même qu'en feintant un peu, il y aura moyen de bidouiller le service worker pour ne compte que les installations. 
   
Mais c'est une aventure pour une prochaine fois. 

## Conclusion
On peut assez facilement faire tout ce qu'on veut sur le web et il suffit d'une simple recherche pour trouver son bonheur.   
L'intérêt de s'ajouter des contraintes (dans le cas présent, l'éco-conception) est de permettre de remettre en queston les fondamentaux pour faire émerger de nouvelles idées. 