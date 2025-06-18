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

## Releases

The [CHANGELOG.md](/ably/ably-php/blob/main/CONTRIBUTING.md) contains details of the latest releases for this SDK. You can also view all Ably releases on [changelog.ably.com](https://changelog.ably.com).

---

## Contributing

Read the [CONTRIBUTING.md](./CONTRIBUTING.md) guidelines to contribute to Ably.

---

## Support, Feedback, and Troubleshooting

For help or technical support, visit the [Ably Support page](https://ably.com/support).

### Ably REST API

This SDK currently supports only the [Ably REST API](https://www.ably.com/docs/rest). For realtime capabilities, you can use the [MQTT adapter](https://www.ably.com/docs/mqtt) alongside [Mosquitto PHP](https://github.com/mgdm/Mosquitto-PHP) to implement [Ably's Realtime features](https://www.ably.com/docs/realtime).