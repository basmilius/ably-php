![Ably Pub/Sub PHP Header](images/phpSDK-github.png)
![Latest Stable Version](https://poser.pugx.org/ably/ably-php/v/stable)
![License](https://poser.pugx.org/ably/ably-php/license)

---

# Ably Pub/Sub PHP SDK

Build any realtime experience using Ably’s Pub/Sub PHP SDK, supported on all popular platforms and frameworks.

Ably Pub/Sub provides flexible APIs that deliver features such as pub-sub messaging, message history, presence, and push notifications. Utilizing Ably’s realtime messaging platform, applications benefit from its highly performant, reliable, and scalable infrastructure.

Find out more:

* [Ably Pub/Sub docs.](https://ably.com/docs/basics)
* [Ably Pub/Sub examples.](https://ably.com/examples?product=pubsub)

---

## Getting started

Everything you need to get started with Ably:

- [Quickstart in Pub/Sub using PHP.](https://ably.com/docs/getting-started/quickstart?lang=php)

---

## Supported platforms

Ably aims to support a wide range of platforms. If you experience any compatibility issues, open an issue in the repository or contact [Ably support](https://ably.com/support).

This SDK supports the following platforms:

| Platform | Support |
|----------|---------|
| PHP      | >= 7.2, including PHP 8.0+. |

> [!IMPORTANT]
> PHP SDK versions < 1.1.9 will be [deprecated](https://ably.com/docs/platform/deprecate/protocol-v1) from November 1, 2025.

---


## Known Limitations

Currently, this SDK only supports [Ably REST](https://www.ably.com/docs/rest). However, you can use the [MQTT adapter](https://www.ably.com/docs/mqtt) to implement [Ably's Realtime](https://www.ably.com/docs/realtime) features using [Mosquitto PHP](https://github.com/mgdm/Mosquitto-PHP).

### Via composer

The client library is available as a [composer package on packagist](https://packagist.org/packages/ably/ably-php). If you don't have composer already installed, you can get it from https://getcomposer.org/.

Install Ably from the shell with:

    $ composer require ably/ably-php --update-no-dev

Then simply require composer's autoloader:

```php
require_once __DIR__ . '/vendor/autoload.php';
```

### Manual installation
Clone or download Ably from this repo and require `ably-loader.php`:
```php
require_once __DIR__ . '/ably-php/ably-loader.php';
```

## Contributing

1. Fork it
2. Create your feature branch (`git checkout -b my-new-feature`)
3. Commit your changes (`git commit -am 'Add some feature'`)
4. Ensure you have added suitable tests and the test suite is passing (run `vendor/bin/phpunit`)
4. Push to the branch (`git push origin my-new-feature`)
5. Create a new Pull Request
