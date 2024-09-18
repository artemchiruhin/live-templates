# Основные шаблоны и сниппеты кода

## PHP

`filedump` - вывод чего-либо в файл в текущей директории
```php
file_put_contents(
    __DIR__ . '/aaaaaaaaaaaaaaaaaaaaaaaa.php',
    "<?php \$dump = " . var_export($end$, true) . "; ?>\n",
    FILE_APPEND
);
```

`predump` - вывод чего-либо в тэг `<pre>`
```php
echo '<pre>';
var_dump($end$);
echo '</pre>';
```

`php` - пишет php-тег
```php
<?php $end$ ?>
```

`dd` - Dump and die
```php
var_dump($dump$); die();
```

## 1С-Битрикс

`asset` - добавляет менеджер ассетов в D7
```php
use Bitrix\Main\Page\Asset;
$asset = Asset::getInstance();
$asset->add$file_type$('$file_path$');
```

`app` - сокращение для глобальной переменной APPLICATION
```php
$APPLICATION
```

`prologbefore` - подключает prolog_before.php
```php
require_once($_SERVER['DOCUMENT_ROOT'].'/bitrix/modules/main/include/prolog_before.php');
```

`prologincluded` - добавляет проверку на подключенный пролог
```php
if (!defined('B_PROLOG_INCLUDED') || B_PROLOG_INCLUDED !== true) die();
```

`stp` - константа SITE_TEMPLATE_PATH
```php
SITE_TEMPLATE_PATH
```

To be continued...
