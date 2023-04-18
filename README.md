# Dojo PHP make Menu

## Instructions

1. Dans le fichier `public/script.php`, écrire une fonction `makeMenu` qui accepte deux paramètres :
- `$pages` : un tableau multi-dimensionnel contenant des noms de pages associés à leurs fichiers `["name" => "", "file" => ""]`
- `$current` : une chaîne de caractères (vide par défaut)
2. La fonction doit retourner le code HTML d'une liste `<ul>` contenant chaque élement du tableau inscrits dans une balise `<a>` dont l'attribut href pointera vers le fichier. Le texte du lien affichera le nom.   

Exemple pour le tableau suivant:
```php
$pages = [
    ["name" => "Home", "file" => "/index.php"], 
    ["name" => "About us", "file" => "/about.php"],
    ["name" => "Contac", "file" => "/contact.php"],
];
```

La fonction devra retourner
```html
<ul>
    <li>
        <a href='/index.php'>Home</a>
    </li>
    <li>
        <a href='/about.php'>About us</a>
    </li>
    <li>
        <a href='/contact.php'>Contact</a>
    </li>
</ul>
```

## Bonus
Si le champ `file` d'un des éléments de la liste correspond à la chaîne passée en deuxième paramètre `$current`, alors ajouter la classe css "active" au lien &lt;a&gt;.

exemple :
```php
$current = "/about.php";
```
affichera 
```html
<ul>
    <li>
        <a href='/index.php'>Home</a>
    </li>
    <li>
        <a class='active' href='/about.php'>About us</a>
    </li>
    <li>
        <a href='/contact.php'>Contact</a>
    </li>
</ul>
```

## Test navigateur

 `php -S localhost:8000 -t public`

## Test PHPUnit
1. `composer install`
2. `./vendor/bin/phpunit tests`