## How to Install

$ git clone https://github.com/adyoi/Yii2-Advanced-Bootstrap4.git

$ cd Yii2-Advanced-Bootstrap4

$ composer update

$ git clone https://github.com/adyoi/Glyphicons-CSS.git /vendor/yiisoft/yii2-debug/src/assets

$ git clone https://github.com/adyoi/Glyphicons-CSS.git /vendor/yiisoft/yii2-gii/src/assets

$ init #0: Development 1: Production

<br>

## Little Modification

Edit File /vendor/yiisoft/yii2-bootstrap/BootstrapAsset.php
```
public $sourcePath = '@bower/bootstrap/dist';
```

Edit File /vendor/yiisoft/yii2-bootstrap/BootstrapPluginAsset.php
```
public $sourcePath = '@bower/bootstrap/dist';
public $js = [
    'js/bootstrap.bundle.js',
];
```

Edit File /vendor/yiisoft/yii2-debug/src/DebugAsset.php
```
public $css = [
    'main.css',
    'toolbar.css',
    'glyphicons-halflings-regular.min.css',
];
```

Edit File /vendor/yiisoft/yii2-gii/src/GiiAsset.php
```
public $css = [
    'main.css',
    'glyphicons-halflings-regular.min.css',
];
```

<br>

## Enjoy

Frontend:
http://{path}/Yii2-Advanced-Bootstrap4/frontend/web/index.php

Backend:
http://{path}/Yii2-Advanced-Bootstrap4/backend/web/index.php
