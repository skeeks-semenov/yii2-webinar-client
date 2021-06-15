API Dadata.ru
===================================

Info
------------
* https://dadata.ru/api/

Installation
------------

The preferred way to install this extension is through [composer](http://getcomposer.org/download/).

Either run

```
php composer.phar require --prefer-dist skeeks/yii2-dadata-client "*"
```

or add

```
"skeeks/yii2-dadata-client": "*"
```

How to use
----------

```php
//App config
[
    'components'    =>
    [
    //....
        'dadataClient' =>
        [
            'class'                 => 'skeeks\yii2\dadataClient\dadataClient',
            'token'   => 'token',
            'secret'   => 'secret',
            'timeout'               => 12,
        ],
    //....
    ]
]

```

Examples
----------

### Адресные подсказки
```php
$response = \Yii::$app->dadataClient->suggest->address("Москва");
print_r($response); //Array response data
```

### Определение положения пользователя по ip
```php
$response = \Yii::$app->dadataSuggestApi->detectAddressByIp(\Yii::$app->request->userIP);
```


### Подсказки email
```php
$response = \Yii::$app->dadataClient->suggest->email("test@ya");
print_r($response); //Array response data
```

### Подсказки фио
```php
$response = \Yii::$app->dadataClient->suggest->fio("Семен");
print_r($response); //Array response data
```

___

> [![skeeks!](https://skeeks.com/img/logo/logo-no-title-80px.png)](https://skeeks.com)  
<i>SkeekS CMS (Yii2) — quickly, easily and effectively!</i>  
[skeeks.com](https://skeeks.com) | [cms.skeeks.com](https://cms.skeeks.com)
