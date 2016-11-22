# Ersteinrichtung
- [Installation](#installation)
	- [Site Requirements](#site-requirements)
	- [Installing Giga Messenger Bot](#installing-giga-messenger-bot)
	- [Secure Tunnels to Localhost](#secure-tunnels-to-localhost)

***
> 
- Du solltest die [Facebook Messenger Übersicht](https://developers.facebook.com/docs/messenger-platform/product-overview) gelesen haben bevor du hier mit der Dokumentation weiter machst.
- Diese Dokumentation ist ausschließlich für WordPress Version. Falls du die Standalone (PHP) benutzen möchtest, findest du hier [PHP Standalone](/docs/standalone) die aktuelle Dokumentation.

<a name="installation"></a>
## Installation

<a name="site-requirements"></a>
### Server Voraussetzungen
Damit der Giga Messenger Bot (GigaAI) läuft prüfe bitte ob dein Server die Minimalvoraussetzungen erfüllt:

- PHP 5.3.2+
- `cURL` erlaubt
- Die Seite muß SSL Verschlüsselt sein `https`

However, it's highly recommended that you run latest WordPress & PHP version.

<a name="installing-giga-messenger-bot"></a>
### Installing Giga Messenger Bot

Like other WordPress plugins, you just do some simple steps to install.

1. Download `giga-messenger-bot.zip` and unzip the package.
1. Copy `giga-messenger-bot` directory to `/wp-content/plugins` directory.
1. Set CHMOD read-writable permission to your `/giga-messenger-bot/cache/` directory.
1. Activate plugin through `wp-admin/plugins` screen.

<a name="configure-webhook"></a>
### Configure Webhook
After activated, if your website has **permalink** enabled, FMB will automatically creates two links which are: `https://domain.com/messenger/` (webhook) and `https://domain.com/messenger/subscribe` (subscribe). Try accessing these URLs to verify if it works (They shouldn't show 404 or some of your pages with content).

If your website doesn't have **permalink** enabled, or `/messenger/` and `/messenger/subscribe` doesn't work. Don't worry! You can create them manually by go to `Dashboard\Pages\Add New` and then create page with template `Messenger Subscribe` and `Messenger Webhook`. You're free to name their URLs.

<a name="secure-tunnels-to-localhost"></a>
### Secure Tunnels to Localhost
Let's assume that you want to test your bots in your development machine before deploy. You'll need to let Facebook connect to your pc and it should have SSL enabled. We'd recommend that you use [ngrok](https://ngrok.com), it will automatically creates a secure public URL to your local webserver with format: `https://random.ngrok.io`.
