# Setup Messenger
***

## Create Facebook App & Page
Create a new [Facebook App](https://developers.facebook.com/quickstarts/?platform=web) and [Page](https://www.facebook.com/pages/create) or simply use existing ones. Your Facebook App can remain in sandbox mode and your Page does NOT have to be publicly visibile. The Page profile picture and name will be used to form the "identity" of your bot and is what people will see when they engage it.

## Setup Webhook

In your Facebook App. Navigate to Webhooks menu item, click New Subscription, then choose Page. A dialog will shows up:
	
![New Page Subscription](/images/page-subscription.png)

- In "Callback URL", enter your webhook URL (default is `https://domain.com/messenger/`).
- In "Verify Token", enter `GigaAI`
- In "Subscription Field", check `message_deliveries`, `messages`, `messaging_optins`, `messaging_postbacks`, `message_echoes`, `message_reads`, and `messaging_account_linking`.
- Click <kbd>Verify and Save</kbd>

## Setup Messenger

The next step is make a connection between Website <=> App <=> Page, so all messages come from page pass through app to website and vice versa.

- In your Facebook App. Navigate Messenger, below Webhooks item.
- In `Token Generation` section, select a your page, you'll need to confirm permission for that page. After that step, you'll got Page Access Token.
	![Page Access Token](/images/page-access-token.png)
- Click to copy that token, then Click <kbd>Save Changes</kbd>.
- Navigate to **WP Admin\Giga AI** and paste that copied text to **Page Access Token** section.
- Paste your page id to **Page ID** section.

Now, visit your subscribe URL (default is `https://domain.com/messenger/subscribe`). You should see this message:

<div class="h1">Congratulation! Facebook Bot is successfully subscribed your webhook.</div>

> Please remember that you can visit this subscribe URL anytime to check connection status.

## Test Your First Message

Try to send `hi` to your page with your app's administrator account. If you get reply from your page. Congratulation! Otherwise, please check your server requirements or previous steps.

![Greeting](/images/greeting.jpg)
