---
layout: post
title:  "Laravel - constantes et traduction"
date:   2017-09-29 12:00:00 +0200
categories: code
---

Cet article présente quelques astuces très utiles pour gérer ses constantes dans Laravel (5.4 et autres).


## Des constantes, pour quoi faire?
Dans le cas qui m'a intéressé, il s'agissait surtout de stocker les valeurs pour des menus déroulants dans des formulaires. Je n'avais pas envie de les stocker "en dur" ni en base. Déjà parce que ce n'est pas très propre mais surtout pas pratique à maintenir.   

## Des constantes, comment?
Laravel propose quelque chose de très utile pour cela : les fichiers de config. Ceux-ci sont chargés automatiquement. Libre à vous de stocker vos constantes dedans.   
Voici un petit exemple :

```
// config/situation_constants.php
<?php
return [
 'transportation' => array(
 'public' => 'Transports en commun',
 'car' => 'Voiture',
 'other' => 'Autre…'
 )
];
?>
```

Ensuite, dans votre blade, il ne vous reste plus qu'à récupérer ces données dans votre menu déroulant :

```
<div class="form-group">
 {!! Form::label('transportation', 'Moyen de locomotion', ['class' => 'control-label']) !!}
 {!! Form::select('transportation', Config::get('situation_constants.transportation')); !!}
 </div>
``` 

Et c'est tout!   
  
## Des constantes, are you sure?
Arrivé là, on se dit "cool, je gère mes constantes proprement".   
Seulement voilà, tout se complique si vous devez gérer la traduction de votre site. Comme ça, ça n'a pas l'air très impressionnant. On intégre les traductions dans le fichier de config contenant les constantes et le tour est joué.
Sauf que les fichiers de config sont chargés avant l'initialisation de la traduction, ce qui vous expose à une ReflectionException un rien obscure.  
La solution consiste à gérer vos constantes directement dans vos fichiers de traduction :

```
// lang/fr/situation.php
<?php
return [
'transportation' => 'Moyen de locomotion',
'transportation_select' => [
 'transportation' => array(
 'public' => 'Transports en commun',
 'car' => 'Voiture',
 'other' => 'Autre…'
 ]
];
```

Il ne vous reste alors plus qu'à reprendre votre blade pour piocher dans ce fichier (et à écrire un fichier similaire pour les autres langues sélectionnables sur votre site) :

```
<div class="form-group">
 {!! Form::label('transportation', __('situation.transportation'), ['class' => 'control-label']) !!}
 {!! Form::select('transportation', __('situation.transportation_select')); !!}
 </div>
 ```
 
Et voilà, le tour est joué!