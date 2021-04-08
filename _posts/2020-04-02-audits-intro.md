---
layout: post
title:  "Audits d'écoconception - introduction"
date:   2020-04-02 10:59:53 +0200
categories: green
description: Le début d'une série de plusieurs articles issus d'un gros chantier autour de l'éconception web. Où l'on présente le contexte et la démarche.
---

Attention, voici le début d'une série de plusieurs articles issus d'un gros chantier autour de l'éconception web. Comme toujours ici, la fréquence de mise en ligne sera aléatoire mais une bonne partie des textes sont déjà prêts donc croisons les doigts.    
Vous trouverez tous les articles autour des audits d'écoconception web sur [la page dédiée au Numérique Responsable](/Numérique responsable.html).  
   
## Contexte
Depuis plusieurs mois s'amorce une grosse prise de conscience autour de l'impact écologique du numérique. Il en découle entre autres la nécessité de s'intéresser à l'écoconception de service numérique.  
Cette série d'articles a pour but de présenter le résultat d'une suite de plusieurs audits sur des sites web ainsi que sur les outils et procédures utilisés. Cette expérimentation s'est faite dans le cadre d'[une formation Simplon](https://simplon.co/) de Développeur Web & Web Mobile amenant vers le diplôme de niveau Bac+2 du même nom. Cette formation se déroule à Carbonne (appelons cela de l'ironie). Elle intègre un module autour de l'écoconception web afin que les apprenants en comprennent les enjeux, sachent analyser un site et puissent mettre en oeuvre des bonnes pratiques sur leurs projets. Bref, leur donner les outils pour qu'ils soient force de proposition et aient du recul sur leur pratique professionnelle.     
Commençons donc par voir en quoi consiste l'impact écologique du numérique et pourquoi ce constat pousse à s'intéresser plus particulièrement aux sites web. 

## Résumé
L'impact environnemental du numérique est loin d'être négligeable. Le principal impact se situe au niveau des utilisateurs et plus particulièrement de la production des équipements. Afin de prolonger la durée de vie de ceux-ci, il est essentiel de s'intéresser à l'écoconception de services numériques (réduction de l'impact des logiciels, applications et sites web). Comme nous le verrons, les bénéfices de cette démarche sont nombreux, la rendant attractive pour les entreprises.   
Ici, nous nous intéressons principalement aux sites web. L'objectif est de s'inspirer des méthodes existantes (ACV et autres) afin de proposer un process d'audit aussi léger et pertinent que possible.  
Pour cela, toutes les phases du cycle de vie d'un service numérique sont importantes (approche holistique).  
Afin de mener cette démarche (car il s'agit bien d'un process et non d'un projet), il est important de mener des audits réguliers, dans le but d'avoir un état des lieux de la situation et de son évolution.   
Pour les sites web, le plus pertinent est de mesurer l'impact de la page d'accueil, ainsi que d'un échantillon de pages parmi les plus fréquentées. Se concentrer sur un parcours utilisateur permet d'améliorer l'expérience utilisateur et d'adopter une démarche plus globale.  
Les outils de mesure retenus sont : 
* [GreenIT Analysis](https://chrome.google.com/webstore/detail/greenit-analysis/mofbfhffeklkbebfclfaiifefjflcpad), avec [EcoIndex](https://addons.mozilla.org/fr/firefox/addon/ecoindex/) en complément pour la mesure d'un parcours utilisateur complet.
* [Wave](https://wave.webaim.org/)
* [PageSpeed Insights](https://developers.google.com/speed/pagespeed/insights/) 
* [WPScan](https://wpscan.org/) (dans le cas particulier de sites Wordpress).  

En complément, le recueil des [115 bonnes pratiques d'écoconception web](https://collectif.greenit.fr/ecoconception-web/115-bonnes-pratiques-eco-conception_web.html) permet de prioriser les actions identifiées. 

Les indicateurs retenus afin d'obtenir des éléments de comparaison sont : 
* Taille de la page 
* Nombre de requêtes HTTP 
* Nombre d'éléments dans [le DOM](https://developer.mozilla.org/en-US/docs/Web/API/Document_Object_Model) 
* Eco-index 
* Emission de gaz à effet de serre en équivalent CO2 
* Consommation d'eau 
* PageSpeed Index  
     
Il est également essentiel de vérifier l'accessibilité afin d'améliorer l'expérience utilisateur et ainsi réduire le temps nécessaire pour trouver des informations sur le site. 

## Impact écologique du numérique   
Le numérique apparaît souvent comme quelque chose d'immatériel. Pourtant, son impact sur l'environnement n'est pas négligeable.   
Actuellement, le numérique pollue davantage que l'aviation civile et le transport maritime (mais pour l'instant moins que le secteur automobile). Ramené à l'empreinte environnementale de l'humanité, le numérique représente la proportion suivante : 
    
| Consommation d'énergie primaire | 4.2 % |   
| Emissions de gaz à effet de serre | 3.8 % |   
| Consommation d'eau | 0.2 %  |   
| Consommation d'électricité | **5.6 %** |   
    
**[Source](https://www.greenit.fr/etude-empreinte-environnementale-du-numerique-mondial/)**  
     
Pendant longtemps, les data centers étaient pointés du doigt. Même si leur rôle est important, le principal impact se situe au niveau des équipements des utilisateurs. En cause, l'[extraction des matières premières et la fabrication des appareils](https://www.ethicalconsumer.org/technology/shopping-guide/mobile-phones)). De plus, ces deux étapes ont un fort impact sociétal (conflits armés, exploitation, etc).  
    
| Pourcentage | Energie | GES | Eau | Electricité | Ressources abiotiques |    
| ------ | ------ | ------ | ------ | ------ | ------- |    
| Utilisateurs           | 60  | 63  | 83  | 44  | 75 |    
| Réseaux                | 23  | 22  | 9   | 32  | 16 |    
| Centres informatiques  | 17  | 15  | 7   | 24  | 8  |   
   
**[Source](https://www.greenit.fr/etude-empreinte-environnementale-du-numerique-mondial/)** 
   
   
Plus généralement, dans l'ordre décroissant des impacts, on trouve : 
1. Fabrication des équipements utilisateurs 
2. Consommation électrique des équipements utilisateurs 
3. Consommation électrique du réseau 
4. Consommation électrique des centres informatiques 
5. Fabrication des équipements réseau 
6. Fabrication des équipements et des centres informatiques (serveurs, etc.) 

**[Source](https://www.greenit.fr/etude-empreinte-environnementale-du-numerique-mondial/)** 
   
  
Les documents suivants sont riches en informations sur ce sujet : 
* [Plaquette ADEME : la face cachée du numérique](https://www.ademe.fr/sites/default/files/assets/documents/guide-pratique-face-cachee-numerique.pdf) 
* [Etude du collectif GreenIT sur l'impact environnemental du numérique mondial](https://www.greenit.fr/etude-empreinte-environnementale-du-numerique-mondial/)  
  
Au niveau individuel, un premier pas consiste à n'acheter que des appareils dont nous avons vraiment besoin et à faire autant que possible durer ceux que nous possédons déjà.   
En effet, lorsque nous remplaçons un appareil, ce n'est bien souvent pas parce qu'il ne fonctionne plus mais parce qu'il rame.   
Deux lois complémentaires illustrent ce principe : 
* [Loi de Moore (1965!!)](https://www.futura-sciences.com/tech/definitions/informatique-loi-moore-2447/ ) : tous les 18 mois, la capacité de calcul des équipements augmente.    
* [Loi de Wirth](https://wikimonde.com/article/Loi_de_Wirth) : les programmes ralentissent plus vite que le matériel accélère.       

La loi de Wirth s'explique par le poids grandissant des sites web, logiciels et applications mobiles ([notion d'obésiciel](https://tonsky.me/blog/disenchantment/)). Ainsi que par [le volume de nos usages (mails, streaming et autres)](https://www.visualcapitalist.com/what-happens-in-an-internet-minute-in-2019/).   
  
![Internet minute 2019](/assets/2019.jpg)    
    
Dans le cas des sites web, [le site HttpArchive](https://httparchive.org/) suit en continu l'évolution du web, en particulier la taille des pages ainsi que divers indicateurs techniques. On peut ainsi voir que [la taille des pages web augmente de façon considérable](https://s3.amazonaws.com/media-p.slid.es/uploads/618299/images/6936704/Screenshot_2020-01-07_State_of_the_Web.png).   
Là aussi, les explications peuvent être nombreuses (stack technique inappropriée ou mal maîtrisée, contenus non-optimisés, etc). 
Enfin, le [streaming](https://theshiftproject.org/article/climat-insoutenable-usage-video/?fbclid=IwAR2qbrWtgeuUL4xAktYYano3KTYx0I2OaVE9u7wxOXklvexRqnX4yGcvZbc) et la [publicité en ligne](https://www.greenit.fr/2015/09/01/la-publicite-represente-39-du-poids-des-pages-web/) consomment par exemple énormément de bande passante.    
    
Sachant que les sites web sont massivement utilisés chaque jour, il est vite apparu nécessaire de lancer une série d'audits d'écoconception sur des sites web. L'idée est de dégager des indicateurs pertinents, de valider l'application de certaines bonnes pratiques d'optimisation mais aussi de mettre en place une procédure simple d'audit. L'objectif final est de sensibiliser à la démarche d'écoconception et de la rendre aussi accessible que possible.            
  
C'est ce que nous verrons dans la partie suivante (avec une petite remise en contexte de l'écoconception web). 
