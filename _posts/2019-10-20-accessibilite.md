---
layout: post
title:  "Accessibilité"
date:   2019-10-20 10:59:53 +0200
categories: green
---

J'avais annoncé une série de billets suite à [celui sur les valeurs du développeur](https://ldevernay.github.io/green/2019/09/03/valeurs.html).
Voici celui sur l'accessibilité.  
Les autres suivront à leur rythme, le temps que je m'y replonge et que je fasse du tri dans les ressources à ma disposition.  

### Valeurs épisode 2 : accessibilité
#### Problématique
La prise de conscience pour l'accessibilité se fera principalement sur les axes suivants : 
* bien comprendre ce qui peut entraver l'utilisation du web par un utilisateur. [Voici quelques mises en situation](https://www.atalan.fr/agissons/fr/),
* prendre conscience des personnes concernées par ces handicaps. [Microsoft propose un guide très bien fait sur l'inclusive design.](https://www.microsoft.com/design/inclusive/)    
En très résumé, il s'agit de revoir notre perception de l'accessibilité et, par extension, du handicap. Le but de l'accessibilité est de rendre un outil utilisable par tous (ce qui est un peu la mission première du développeur/designer/concepteur/etc). On oublie trop souvent les handicaps temporaires ou situationnels. Voici quelques exemples pour resituer : 
* utiliser un smartphone avec un bras dans le plâtre ou dans un environnement trop lumineux
* s'appuyer sur de la reconnaissance vocale lorsqu'on a une défaut d'élocution ou un fort accent
* naviguer sur un site web lorsqu'on a oublié sa souris ou qu'elle ne fonctionne plus

[La liste est longue](https://the-pastry-box-project.net/anne-gibson/2014-july-31) mais l'idée est de comprendre que l'accessibilité agit pour le bénéfice de tous les utilisateurs et permet donc de toucher un public (ou une clientèle) plus large. 

En plus, l'accessibilité est inscrite dans [les réglementations française et européenne](https://blog.ipedis.com/legislation-europeenne-francaise-accessibilite-numerique). Pour autant, [la grande majorité des sites internet présentent des problèmes d'accessibilité](https://webaim.org/projects/million/).

Pour finir, voici [quelques vérités à garder à l'esprit](https://ericwbailey.design/writing/truths-about-digital-accessibility.html).

#### Diagnostic
Les outils sont nombreux, certains sont même inclus nativement dans Firefox (F12 -> Accessibility) et Chrome (F12 -> Audits -> cocher la case "Accessibility"). 

Comme souvent, il est illusoire d'espérer trouver un outil qui fasse tout automatiquement. Voici donc quelques exemples de procédures utilisées pour tester l'accessibilité d'un site : 
* https://daverupert.com/2018/07/assistive-technologies-i-test-with/
* https://www.a11ywithlindsey.com/blog/web-accessibility-testing-process
* https://benrobertson.io/accessibility/how-to-run-quick-accessibility-audit
Partant de là, c'est en pratiquant que vous construirez votre propre procédure (et je vous invite alors à la partager à votre tour).

#### Mise en place
Pour partir sur de bonnes bases, [Udacity propose une formation très bien conçue sur ce sujet.](https://www.udacity.com/course/web-accessibility--ud891)  
Les ressources sur le sujet ne manquent pas et il est rapide d'acquérir suffisamment de bagage pour dégager les actions à prioriser. Voici déjà quelques pistes pour commencer :    
* [L'introduction ultime - FreeCodeCamp](https://www.freecodecamp.org/news/pragmatic-rules-of-web-accessibility-that-will-stick-to-your-mind-9d3eb85a1a28/)
* [The A11y project](https://a11yproject.com/)
* [Introduction par WebAIM](https://webaim.org/intro/)
* [Maximiser l'impact avec des astuces simples - CSS-Tricks](https://css-tricks.com/small-tweaks-can-make-huge-impact-websites-accessibility/)
* [Des tutoriels proposés par la WAI (Web Accessibility Initiative)](https://www.w3.org/WAI/tutorials/)

Pour ceux qui préfèrent une bonne checklist en français, Opquast est (comme souvent) le bon endroit pour commencer : [premier pas vers WCAG](https://checklists.opquast.com/fr/accessibility-first-step/)

Et, en bonus, [la newsletter qui va bien pour découvrir le sujet aussi bien que se tenir au courant](https://a11yweekly.com/). 


#### Actions prioritaires
[Commençons par une fiche résumant l'essentiel](https://moritzgiessmann.de/accessibility-cheatsheet/).  
Voici quelques notions qui sont à mon avis à regarder en priorité (et que vous retrouverez dans le cours Udacity indiqué plus haut) :
* Alt, sous-titres: il est important de prévoir des alternatives (le plus souvent textuelles) aux contenus visuels ou audio. Et s'il était encore besoin de vous rappeler que l'accessibilité ne touche pas que les personnes en situation de handicap, pensez aux contenus sous-titrés qu'on retrouve un peu partout pour les séries et les films. 
* [ARIA](https://developer.mozilla.org/en-US/docs/Web/Accessibility/ARIA)
* Commencez par utiliser du [HTML sémantique](https://css-tricks.com/why-how-and-when-to-use-semantic-html-and-aria/), il n'en sera que plus propre (et de même pour votre CSS). Et gardez toujours à l'esprit que HTML propose bien plus de fonctionnalités que ce qu'on connaît.     

#### Bénéfices attendus
Un site plus accessible le sera aussi pour les robots, ce qui améliorera notamment votre référencement naturel.  
Enfin, on ne le dira jamais assez, améliorer l'accessibilité de votre site revient à améliorer l'expérience de l'ensemble de vos utilisateurs.  

#### Conclusion
Le chantier de l'accessibilité pour le web est déjà très riche et encadré par plusieurs réglementations. Pour autant, l'état des lieux dressé par WebAIM souligne tout ce qu'il reste encore à faire. En incorporant la notion d'accessibilité dès aujourd'hui dans vos méthodes de travail, vous verrez rapidement que (comme pour les autres valeurs abordées dans la présente série d'articles), il est facile d'identifier des mesures simples avec un impact plus que conséquent.  
La question de l'accessibilité pour les applis mobiles reste entière. Les bonnes pratiques de conception existent (car c'est souvent à ce niveau que tout se joue) mais je ne connais pas forcément d'outils pour mesurer l'accessibilité similaires à ceux utilisés pour les sites internet. Toutefois, c'est aussi pour moi une bonne raison supplémentaire de se pencher plutôt que les Progressive Web Apps ([voir mon billet précédent à ce sujet](https://ldevernay.github.io/green/2019/09/16/pwa.html)).
