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

## Known limitations

1. This client library requires PHP version 5.4 or greater

## Running the tests

The client library uses the Ably sandbox environment to provision an app and run the tests against that app.  In order to run the tests, you need to:

	git clone https://github.com/ably/ably-php.git
	cd ably-php
    composer install
    git submodule init
    git submodule update
    ./vendor/bin/phpunit

Note - If there is a issue while running tests [SSL certificate error: unable to get local issuer certificate], please set SSL cert path in `php.ini`.  For more information, follow https://aboutssl.org/fix-ssl-certificate-problem-unable-to-get-local-issuer-certificate/

## Contributing

1. Fork it
2. Create your feature branch (`git checkout -b my-new-feature`)
3. Commit your changes (`git commit -am 'Add some feature'`)
4. Ensure you have added suitable tests and the test suite is passing (run `vendor/bin/phpunit`)
4. Push to the branch (`git push origin my-new-feature`)
5. Create a new Pull Request

## Release Process

This library uses [semantic versioning](http://semver.org/). For each release, the following needs to be done:

1. Update the version number in [src/Defaults.php](./src/Defaults.php)
2. Create a new branch for the release, named like `release/1.0.0` (where `1.0.0` is what you're releasing, being the new version).
3. Run [`github_changelog_generator`](https://github.com/github-changelog-generator/github-changelog-generator) to automate the update of the [CHANGELOG.md](CHANGELOG.md). This may require some manual intervention, both in terms of how the command is run and how the change log file is modified. Your mileage may vary:
- The command you will need to run will look something like this: `github_changelog_generator -u ably -p ably-php --since-tag 1.1.9 --output delta.md --token $GITHUB_TOKEN_WITH_REPO_ACCESS`. Generate token [here](https://github.com/settings/tokens/new?description=GitHub%20Changelog%20Generator%20token).
- Using the command above, `--output delta.md` writes changes made after `--since-tag` to a new file.
- The contents of that new file (`delta.md`) then need to be manually inserted at the top of the `CHANGELOG.md`, changing the "Unreleased" heading and linking with the current version numbers.
- Also ensure that the "Full Changelog" link points to the new version tag instead of the `HEAD`.
4. Commit generated [CHANGELOG.md](./CHANGELOG.md) file.
5. Make a PR against `main`.
6. Once the PR is approved, merge it into `main`.
7. Add a tag and push to origin such as `git tag 1.0.0 && git push origin 1.0.0`.
8. Visit https://github.com/ably/ably-php/tags and add release notes for the release including links to the changelog entry.
9. Visit https://packagist.org/packages/ably/ably-php, log in to Packagist, and click the "Update" button.
10. Remember to make a release update for [laravel-broadcaster](https://github.com/ably/laravel-broadcaster) and [ably-php-laravel](https://github.com/ably/ably-php-laravel).
