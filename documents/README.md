## How to Install

$ git clone https://github.com/adyoi/Yii2-Advanced-Bootstrap4.git

$ cd Yii2-Advanced-Bootstrap4

$ composer update

$ git clone https://github.com/adyoi/Glyphicons-CSS.git ./vendor/yiisoft/yii2-debug/src/assets

$ git clone https://github.com/adyoi/Glyphicons-CSS.git ./vendor/yiisoft/yii2-gii/src/assets

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

Edit File /vendor/yiisoft/yii2-gii/src/views/layouts/main.php
```
<?php
use yii\bootstrap\NavBar;
use yii\bootstrap\Nav;
use yii\helpers\Html;

/* @var $this \yii\web\View */
/* @var $content string */

$asset = yii\gii\GiiAsset::register($this);
?>
<?php $this->beginPage() ?>
<!DOCTYPE html>
<html lang="en">
<head>
    <meta charset="utf-8"/>
    <meta name="viewport" content="width=device-width, initial-scale=1">
    <meta name="robots" content="none">
    <?php $this->registerCsrfMetaTags() ?>
    <title><?= Html::encode($this->title) ?></title>
    <?php $this->head() ?>
</head>
<body>
    <div class="container-fluid page-container">
        <?php $this->beginBody() ?>
        <?php
        \yii\bootstrap4\NavBar::begin([
            'brandLabel' => Html::img($asset->baseUrl . '/logo.png'),
            'brandUrl' => ['default/index'],
            'options' => ['class' => 'navbar navbar-expand-lg navbar-dark bg-dark'],
        ]);
        echo \yii\bootstrap4\Nav::widget([
            'options' => ['class' => 'navbar-nav'],
            'items' => [
                ['label' => 'Home', 'url' => ['default/index']],
                ['label' => 'Help', 'url' => 'http://www.yiiframework.com/doc-2.0/ext-gii-index.html'],
                ['label' => 'Application', 'url' => Yii::$app->homeUrl],
            ],
        ]);
        \yii\bootstrap4\NavBar::end();
        ?>
        <div class="container content-container">
            <?= $content ?>
        </div>
        <div class="footer-fix"></div>
    </div>
    <footer class="footer">
        <div class="container">
            <p class="float-left">A Product of <a href="http://www.yiisoft.com/">Yii Software LLC</a></p>
            <p class="float-right"><?= Yii::powered() ?></p>
        </div>
    </footer>
<?php $this->endBody() ?>
</body>
</html>
<?php $this->endPage() ?>
```

<br>

## Enjoy

Frontend:
http://{webroot}/Yii2-Advanced-Bootstrap4/frontend/web/index.php

Backend:
http://{webroot}/Yii2-Advanced-Bootstrap4/backend/web/index.php
