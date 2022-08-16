# yii2-lightbox

## Info about this repo

I created this repo as hotfix for my project, because the original repo yeesoft/yii2-lightbox was gone. I just copied files from the vendor folder to this repo.
Please note that there is no package published on packigst. You have to add the following to your composer.json into the "repositories" section

```  
 "repositories": [
        {
            "type": "composer",
            "url": "https://asset-packagist.org"
        },
        {
            "url": "https://github.com/passierschein-a38/yii2-lightbox.git",
            "type": "git"
        }
    ],
    "require": {
        ...
        "passierschein-a38/yii2-lightbox": "dev-main"
        ...
    },
```

:fire: Original content starting from here :fire:

## Lightbox Widget for Yii 2

This module is a wrapper for Lightbox2

Installation
------------

The preferred way to install this extension is through [composer](http://getcomposer.org/download/).

Either run

```
composer require --prefer-dist yeesoft/yii2-lightbox "~0.1.0"
```

or add

```json
"yeesoft/yii2-lightbox": "~0.1.0"
```

to the require section of your `composer.json` file.

Usage
------------
Once the extension is installed, simply add widget to your page as follows:

```php
use yeesoft\lightbox\Lightbox;

echo Lightbox::widget([
    'options' => [
        'fadeDuration' => '2000',
        'albumLabel' => "Image %1 of %2",
    ],
    'linkOptions' => ['class' => 'pull-left'],
    'imageOptions' => ['class' => 'thumbnail'],
    'items' => [
        [
            'thumb' => '/images/image01-120x90.jpg',
            'image' => '/images/image01.jpg',
            'title' => 'Image 1',
            'group' => 'image-set1',
        ],
        [
            'thumb' => '/images/image02-120x90.jpg',
            'image' => '/images/image02.jpg',
            'title' => 'Image 2',
            'group' => 'image-set1',
        ],
    ],
]);
```

