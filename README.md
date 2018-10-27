E-conomic PHP REST CLIENT
===================
[![Build Status](https://travis-ci.org/Lenius/economic-php-client.svg)](https://travis-ci.org/Lenius/economic-php-client) [![StyleCI](https://styleci.io/repos/63632645/shield)](https://styleci.io/repos/63632645) [![Code Coverage](https://scrutinizer-ci.com/g/Lenius/economic-php-client/badges/coverage.png?b=master)](https://scrutinizer-ci.com/g/Lenius/economic-php-client/?branch=master) [![Scrutinizer Code Quality](https://scrutinizer-ci.com/g/Lenius/economic-php-client/badges/quality-score.png?b=master)](https://scrutinizer-ci.com/g/Lenius/economic-php-client/?branch=master) [![Latest Stable Version](https://poser.pugx.org/Lenius/economic-php-client/v/stable)](https://packagist.org/packages/Lenius/economic-php-client) [![Total Downloads](https://poser.pugx.org/Lenius/economic-php-client/downloads)](https://packagist.org/packages/Lenius/economic-php-client) [![License](https://poser.pugx.org/Lenius/economic-php-client/license)](https://packagist.org/packages/Lenius/economic-php-client)

https://restdocs.e-conomic.com

### Access all debitors
Call the Customers url /Customers
```php
$appToken = 'demo';
$grant    = 'demo';

$client = new Lenius\Economic\RestClient($appToken,$grant);

$parms = ['pagesize'=>100];

$response = $client->request->get('customers',$parms);

$status = $response->httpStatus();

if( $status == 200 ) {
    // Successful request
    $data = $response->asArray();
    print_r($data);
}
```
