steam-api-php
=============
[![Build Status](https://travis-ci.org/DaMitchell/steam-api-php.png?branch=master)](https://travis-ci.org/DaMitchell/steam-api-php)

A PHP wrapper for the Steam API

An Example
----------
```php
use JMS\Serializer\SerializerBuilder;
use Steam\Adapter\Guzzle;
use Steam\Configuration;
use Steam\Api\User;

$config = new Configuration(array(
    'steamKey' => {STEAM_KEY},
));

$adapter = new Guzzle($config);
$adapter->setSerializer(SerializerBuilder::create()->build());

$user = new User();
$user->setAdapter($adapter);

$result = $user->getFriendList(76561198049450178);
```
