---
layout: post
title:  "Tester avec Laravel"
date:   2017-09-05 12:00:00 +0200
categories: code
description: Il paraît que tester, c'est douter. Voici comment tester avec Laravel.
---

Pour resituer, Laravel est un framework PHP basé entre autres sur Symfony. L'intérêt est qu'il embarque tout un tas d'outils (ORM, générateur de templates, etc) afin de vous faciliter la vie.    
Ici, nous allons nous intéresser à un sujet essentiel et pourtant difficile pour ceux qui débuteraient avec Laravel : les tests. Pour cela, le framework s'appuie sur l'incontournable PHPUnit.    
Au moins, avec Laravel, on a la chance d'avoir de la bonne documentation. Ce qui ne rend pas les débuts faciles pour autant.     

> Les étapes qui suivent ont été testées (mais pas unitairement) pas à pas, avec un environnement de travail Ubuntu.

## Premiers pas
Les classes de tests sont réparties dans deux dossiers :
* tests/Unit : pour les tests unitaires (sur un bout de code isolé)
* tests/Feature : pour le reste (interaction entre composants, etc)

Dans chacun de ces répertoires, un fichier ExampleTest.php est proposé mais ne vous mènera pas bien loin.    
Les tests à lancer sont répertoriés dans votre fichier phpunit.xml.    
Pour les lancer, rien de plus simple. Allez dans le terminal, directement à la racine du dossier de votre projet, pour lancer :   

```
phpunit
```

Pour créer une nouvelle classe de test, remerciez une fois de plus Artisan :    

```
php artisan make:test BobTest 
```    
Votre fichier BobTest.php est alors créé dans le dossier Feature.     
Pour l'ajouter dans le fichier Unit, lancez :     

```
php artisan make:test BobTest - - unit
```

Prenons le fichier Feature/ExampleTest.php. La méthode utilsée est simple :   

```
public function testBasicTest()
    {
        $response = $this->get('/');

        $response->assertStatus(200);
    }
``` 

On se connecte à la racine du site, on vérifie que la requête s'est bien passée (statut 200).   

## Premiers tests
### Visiter le site avec un utilisateur connecté
Imaginons que vous redirigiez votre utilisateur non-connecté vers la page de connexion. Pour cela, on ajoute la méthode suivante :

```
public function unauthentifiedTest()
 {
    $response = $this->get('/'); //On se connecte à la racine du site
    $response->assertStatus(302); // On est redirigé
    $response->assertRedirect('/login'); // On est bien redirigé vers la route de connexion
 }
 ```

Tout devrait bien se passer, non?    
Sauf que phpunit nous retourne un warning. En effet, le nommage de la méthode l'empêche d'être prise en compte. Pour corriger cela, mieux vaux appeler sa méthode testUnauthentified. Le préfixe "test" est utilisé par PHPUnit pour repérer les méthodes qu'il doit lancer. Au passage, dans le phpunit.xml, vous voyez que phpunit n'utilise pour lancer les tests que les classes avec un suffixe "Test" dans leur nom de fichier, pour peu qu'elles soient placées dans les répertoires Unit ou Feature.     
Après modification, soudain, tout se passe bien.    

```
public function testUnauthentified()
 {
    $response = $this->get('/'); //On se connecte à la racine du site
    $response->assertStatus(302); // On est redirigé
    $response->assertRedirect('/login'); // On est bien redirigé vers la route de connexion
 }
 ```   

### Contrôler les données en base
Pour cela, il y a tout ce qu'il faut dans les assertions proposées par défaut.    
Envie de vérifier que vous avez bien un utilisateur (dans la table users) ayant pour email "admin@admin.com"?

```
public function testAdminExists()
 {
    $this->assertDatabaseHas('users', [
    'email' => 'admin@admin.com'
    ]);
}
```

Si, soudain, une erreur apparaît en lançant PHPUnit, allez voir plus loin dans cet article, du côté des Erreurs Fréquentes.     
Pour vos tests, vous pouvez avoir besoin d'avoir des données existantes en base. Vous pouvez pour cela utiliser des seeds. Cette fonctionnalité de Laravel vous facilitera souvent la vie, surtout en phase de développement.     
Nous sommes désormais en mesure de tester les différentes pages et routes de votre site ainsi que ce qui se trouve en base. Passons à l'étape suivante : simuler la navigation et la saisie de données sur le site.    

## Tester via un navigateur
### Installation
Nous allons par la suite utiliser Dusk. Il y a quelques petites choses à savoir au préalable :    
* Dusk n'est pas installé de base avec Laravel, il va vous falloir l'installer avec Composer, l'enregistrer dans votre AppServiceProvider puis l'installer pour de bon avec Artisan. Toutes les instructions se trouvent ici et sont reprises en détail plus loin dans cet article.
* Dusk utilise Chrome pour simuler la navigation.
* Dusk fonctionne indépendamment de PHPUnit, il est donc géré à part dans l'arborescence de fichiers et pour le lancement des tests.
* Pensez à bien limiter Dusk à vos environnements de dev et de test, sous peine d'ouvrir la porte à des petits malins une fois votre site en production.    

Pour installer Dusk, commencez par aller dans le terminal, directement à la racine du dossier de votre projet.

```
composer require --dev laravel/dusk:^1.0
```

NB : on n'installe Dusk que pour notre environnement de dev (voir plus haut).   
Ensuite, allez dans votre projet, dans app/Providers et ajoutez les éléments suivants dans votre AppServiceProvider.php :     

```
use Laravel\Dusk\DuskServiceProvider;

/**
 * Register any application services.
 *
 * @return void
 */
public function register()
{
    if ($this->app->environment('local', 'testing')) {
        $this->app->register(DuskServiceProvider::class);
    }
}
```

Enfin, de retour dans votre terminal, lancez la dernière commande :

```
php artisan dusk:install
```

Vous vous souvenez du répertoire où se trouvent tous vos tests pour PHPUnit? A côté de Feature et Unit, un nouveau dossier Browser a fait son apparition. Dedans, vous trouverez un premier exemple de test, dans le fichier ExampleTest.php. Il s'agit de se connecter au site afin de vérifier que le nom "Laravel" s'affiche bien à l'écran.    
Pour lancer ce test et vérifier que tout se passe bien, lancez la commande suivante dans votre terminal :  

```
php artisan dusk
```

Si vous rencontrez une erreur, allez jeter un oeil en bas de cet article dans Erreurs Fréquentes.    
Normalement, tout devrait bien se passer. Si ce n'est pas le cas, StackOverflow et Laracasts sont vos amis (et DuckDuckGo, évidemment).   

### Se connecter
Le premier test qu'il semble logique d'effectuer consiste à se connecter au site. Heureusement, grâce aux seeds et à Faker, j'ai en base tout un tas d'utilisateurs prévus pour ça. Histoire de me faciliter la vie, imaginons que je leur ai tous attribué le mot de passe "pouet". La méthode à tester ressemble donc à ça :

```
public function testConnection() {
    $user = User::find(2);
    $this->browse(function ($browser) use ($user) {
    $browser->visit('/login')
    ->type('email', $user->email)
    ->type('password', 'pouet')
    ->press('Login')
    ->assertPathIs('/home');
    });
 }
 ```

* Je récupère un utilisateur qui existe en base (arbitrairement, ce sera celui avec l'ID 2).
* Je me connecte à la page de login.
* Je saisis le mail de l'utilisateur et son mot de passe.
* J'appuie sur le bouton "Login".
* Je vérifie que l'utilisateur est bien redirigé vers l'URL "/home".
   
Et voilà!  

## Erreurs fréquentes
**Houlala, j'ai une erreur quand je teste ce que j'ai en base de données (assertDatabaseHas ou autres).**   
    
Parfois, c'est parce que vous avez sur votre poste une version de PHPUnit plus récente que celle utilisée par Laravel. Pour y remédier, une solution peut être d'installer une version plus ancienne de PHPUnit sur votre poste.    
[Pour plus d'infos.](https://laracasts.com/discuss/channels/testing/assertdatabasehas-throws-typeerror)    

       
**Quand je lance mon test Dusk, j'ai une erreur. On dirait que la méthode curl_init n'existe pas.**

Pour y remédier, il vous suffit d'installer php-curl.  
[Pour plus d'infos.](https://medium.com/r/?url=https%3A%2F%2Fgithub.com%2Facacha%2Fadminlte-laravel%2Fissues%2F251)   
   

**Quand je lance mon test Dusk, il échoue.**

Astuce : quand votre test échoue, Dusk crée une capture d'écran dans tests/Browser/screenshots.   
Si vous voyez un "Not Found" sur cette capture d'écran, assurez-vous que l'URL du site présente dans votre fichier .env (APP_URL) est correcte, y compris le port.  


## En bref
Avec PHPUnit, nous avons vu comment tester une route ou une URL mais aussi comment se faire passer pour un utilisateur. Enfin, nous avons vérifié que certaines données existaient bien en base.   
Avec Dusk, nous avons vu comment simuler la navigation sur le site via Chrome.   
Rien qu'avec ça, nous avons déjà de quoi tester une bonne partie des fonctionnalités de notre site.  
   
    
## Aller plus loin
Pour continuer dans votre lancée, je vous recommande une fois de plus la documentation Laravel. Sinon, jetez un oeil au [cours OpenClassrooms sur le sujet](https://openclassrooms.com/courses/decouvrez-le-framework-php-laravel/les-tests-unitaires-4).   
Bonne lecture!   