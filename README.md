# GSM Arena API (gsmarena.com)

PHP Class for grab data on [gsmarena.com](https://gsmarena.com/) website and output Array or JSON using cURL and simple html dom.

### Usage:

```php

use EvgeniyPP\GsmArena\GsmArenaApi;
require_once 'vendor/autoload.php';

// Create object
$gsm = new GsmArenaApi();
```

### Getting array of brands:

```php
$data = $gsm->getBrands();
```

### Search by a brand name to find models:

```php
$data = $gsm->search('zenfone');
```

### Get concrete model details:

```php
$data = $gsm->getDeviceDetail('asus_zenfone_max_zc550kl-7476'); // Slug
```

### Return array of details:

```php
print_r($data);
```

### Return JSON of details:

```php
// Convert ARRAY to JSON
header('Content-Type: application/json');
echo json_encode($data, JSON_PRETTY_PRINT);
```
