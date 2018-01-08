## Install the packages

## Copy the colorscheme

## Dark Theme
Copy the theme folder to 
/Users/gabri/Library/Application Support/Sublime Text 3/Packages/Material Theme
<br>

## PSR2 autoformatting with CS-Fixer
Installation:
```
composer global require friendsofphp/php-cs-fixer
```
Add to the settings:<br>
"show_panel_on_build": false<br>
Set Tools->BuildSystem->PSR-2<br>
Command+B to compile<br><br>

## Autocomplete Laravel Sublime

```
composer require --dev barryvdh/laravel-ide-helper
```

<br>
Add in the app/config.php

```
Barryvdh\LaravelIdeHelper\IdeHelperServiceProvider::class,
```

<br>
Add to the Composer.json<br>

```
"scripts":{
    "post-update-cmd": [
        "Illuminate\\Foundation\\ComposerScripts::postUpdate",
        "php artisan ide-helper:generate",
        "php artisan ide-helper:meta",
        "php artisan optimize"
    ]
},
```

```
php artisan ide-helper:generate

Composer update
```
