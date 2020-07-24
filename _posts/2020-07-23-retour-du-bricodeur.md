---
layout: post
title:  Le retour du bricodeur
date:   2020-07-23 08:59:53 +0200
categories: green
description: Précédemment, j'avais bidouillé mon site pour ajouter une fonctionnalité de recherche et de comptage des visites. Je m'attaque cette fois à une de mes arlésiennes, trouver un outil léger pour gérer mes présentations. Jekyll et reveal.js, l'histoire d'une belle rencontre. 
---

L'éco-conception et plus généralement la réduction de notre impact environnemental, c'est top mais parfois ça bouffe un peu la tête. Depuis un bon moment déjà, je cherchais un outil léger et non-propriétaire pour gérer mes présentations. Et là je pense que je tiens un truc.

## Origines secrètes
Powerpoint est plein à craquer de fonctionnalités qui ne me servent à rien et Google Slides n'est pas vraiment mieux, d'autant plus qu'il incite à bidouiller ses slides en ligne. [Slides.com](https://slides.com/ldevernay) est un peu plus léger mais uniquement en ligne. Bref, je ne suis jamais content.  
J'ai cherché pendant un bon moment une solution, sans succès. En creusant du côté de slides.com, j'avais regardé de plus près [reveal.js](https://revealjs.com/) mais c'était encore trop lourd.  
Cette semaine, en bossant sur un projet de site qui se veut léger (pour permettre à une promo d'apprenants de centraliser ses réalisations et de se présenter) est apparue l'idée de s'en servir aussi pour qu'ils réalisent leurs veilles quotidiennes. Oui, chez Simplon.co, on aime bien que les apprenants présentent chaque jour (à tour de rôle) un sujet tech (ou non) de leur choix. Mais comment concilier ça avec le site web sans alourdir le tout de façon inconsidérée?   

## Au début, il y avait une idée
Le site est basé sur Jekyll, comme mon site perso. On l'a un peu tordu dans tous les sens mais ça a surtout provoqué un déclic : on a choisi le markdown pour la rédaction du contenu du site, pourquoi ne pas l'utiliser pour les présentations aussi?   
Et c'est là qu'est ressorti reveal.js!  
Sauf que ça reste une librairie plutôt lourde. Avec les polices, les styles et pléthore de plugins disponibles, ça peut vite déraper.  
J'ai donc décidé de me lancer dans un prototype allégé avec une méthodo sobrement appelée "méthode de la roulette russe". On prend un exemple qui marche et on enlève des composants petit à petit en veillant à ce que ça continue à marcher. Si ça pète à un moment, on remet ce qu'on vient d'enlever.   
![Jenga](/assets/jenga.png)   
A la fin, la bonne nouvelle est que c'était beaucoup plus léger (forcément).  
Restait à brancher ça avec Jekyll.  
Pour ça, j'ai décidé de procéder en plusieurs étapes. 
* Ajouter une collection "presentations" dans *_config.yml*, dans les *collections* et les *defaults* (avec output true pour les afficher individuellement). On verra juste après pour créer le layout qui va bien.  
  
```
    collections: 
        presentations:
        output: true 
    (...)
    defaults: 
    - scope:
      path: ""
      type: "presentations"
    values:
      layout: "presentation"
```
  
* On peut ensuite passer au *layout* (dans _layouts/presentation.html). Il s'agit d'un genre de modèle qui va définir, au niveau du thème, comment afficher chaque présentation.  En gros, on reprend juste le JS et le CSS dont on a absolument besoin pour afficher les slides, proposer de la coloration syntaxique pour les bouts de code qu'on mettra dedans et prendre en charge le markdown (et se laisser l'opportunité de prendre en charge par la suite les notes du présentateur). On pointe vers cdn.rawgit, c'est plus propre et ça permet d'être sûr d'avoir les dernières versions à jour. Aussi, une petite condition pour définir un style par défaut pour chaque présentation. Plusieurs possibilités, qu'on retrouve directement dans [le repo de reveal.js](https://github.com/hakimel/reveal.js/tree/master/dist/theme). Le choix du thème par défaut est bien sûr totalement arbitraire (même si on pourra avancer que ce pseudo-dark mode est légèrement moins énergivore).

```

---

---

<!doctype html>
<html>

<head>
	<meta charset="utf-8">
	<meta name="viewport" content="width=device-width, initial-scale=1.0, maximum-scale=1.0, user-scalable=no">

	<title>{{page.name}}</title>

	<link rel="stylesheet" href="https://cdn.rawgit.com/hakimel/reveal.js/master/dist/reset.css">
	<link rel="stylesheet" href="https://cdn.rawgit.com/hakimel/reveal.js/master/dist/reveal.css">
	{% if page.style %}
	<link rel="stylesheet" href="https://cdn.rawgit.com/hakimel/reveal.js/master/dist/theme/{{page.style}}.css"
		id="theme">
	{% else %}
	<link rel="stylesheet" href="https://cdn.rawgit.com/hakimel/reveal.js/master/dist/theme/black.css" id="theme">
	{% endif %}

	<!-- Theme used for syntax highlighted code -->
	<link rel="stylesheet" href="https://cdn.rawgit.com/hakimel/reveal.js/master/plugin/highlight/monokai.css"
		id="highlight-theme">
</head>

<body>
	<div class="reveal">
		<div class="slides">
				<section data-markdown data-separator="///">
						<script type="text/template">
							\{\{content\}\}
						</script>
					</section>
		</div>
	</div>
	<script src="https://cdn.rawgit.com/hakimel/reveal.js/master/plugin/notes/notes.js"></script>
	<script src="https://cdn.rawgit.com/hakimel/reveal.js/master/dist/reveal.js"></script>
	<script src="https://cdn.rawgit.com/hakimel/reveal.js/master/plugin/markdown/markdown.js"></script>
	<script src="https://cdn.rawgit.com/hakimel/reveal.js/master/plugin/highlight/highlight.js"></script>
	<script>
		Reveal.initialize({
			hash: true,
			plugins: [RevealMarkdown, RevealHighlight, RevealNotes]
		});
	</script>
</body>

</html>
```
* Ensuite, il ne restera qu'à créer nos présentations dans le dossier *_presentations*. En voici un petit exemple pour se donner une idée :  
  
```
---
style: league
---
## Demo 1  
### Sommaire
* Partie 1
* Partie 2
                
Pour bien garder en tête.
>Citation  
///
## Demo 1  
    let a = 2;
    let b = 3;
    console.log(a+b);
///
## Demo 1  
  
Slide 3
(...)
```
   
Vous pouvez contempler ce que ça donne [ici](https://ldevernay.github.io/presentations/code.html). Le temps de les migrer sur le présent site et vous y trouverez bientôt [mes présentations](https://ldevernay.github.io/presentations). 

## Conclusion et axes d'amélioration
Déjà, je suis content d'avoir trouvé une solution pour mes présentations.  
C'est toujours aussi plaisant de bidouiller Jekyll.  
Je garde aussi en tête de regarder si je ne peux pas encore plus alléger ce qui reste de reveal.js (minifier, compresser et virer ce qui ne sert pas).  
Mais je trouve que c'est déjà un bon début. 
Je me demande aussi, si ça intéresse d'autres utilisateurs de Jekyll, s'il n'y a pas moyen d'en faire un petit truc "plug and play" (genre un plugin). Ou carrément de créer un boilerplate de site jekyll minimaliste pour que chacun puisse mettre à dispo ses présentations (via un hébergement sur gitlab, github ou autres). Mais pas de raison de s'emballer tant qu'il n'y a pas vraiment de besoin là-dessus. #sobriete

### Bonus
Pour le fun (on sait s'amuser, ici), j'ai comparé :
* la prez exemple hébergée sur mon site
* une prez vierge fraîchement créée sur slides.com


**Note**: ici, on s'intéresse au service numérique "Afficher une présentation". Les gains sont d'autant plus considérables sur le service numérique "Créer une présentation", dans la mesure où celui-ci se fait désormais hors-ligne.

#### Slides.com  
   
| Indicateur | Valeur |  
| ------ | ------ |	  
| Request number |	22 |  
| Page Size (Kb) | 	3626.944 |  
| Dom Size |	162 |  
| Greenhouse Gases Emission (gCO2e)	| 1.62 |  
| Water Consumption (cl) 	| 2.43 |  
| Eco Index |	69 |  
| Grade |	B |  
  
#### Présentation exemple ici-même
  
| Indicateur | Valeur |
| ------ | ------ |	
| Request number |	19 |  
| Page Size (Kb) | 	473.038 |  
| Dom Size |	84 |  
| Greenhouse Gases Emission (gCO2e)	| 1.36 |  
| Water Consumption (cl) 	| 2.04 |  
| Eco Index |	82 |  
| Grade |	A |  
  
  