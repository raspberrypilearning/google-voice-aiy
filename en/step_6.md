## Setting up the Assistant API

Once your Raspberry Pi has booted, you're going to need some credentials from Google, for this to work. Follow the steps below to enable the Google Assistant API.

[[[generic-api-google-assistant]]]

Your **secrets** file that you downloaded will be called something like `client_secret_89351974213-jsno1i2s7lu9mv4q9bjbf3pas6cpnbe5.apps.googleusercontent.com.json`. This needs renaming and placing in your `/home/pi` directory. The new name should be `assistant.json`.

To do this, open a terminal and type:

```bash
mv cline_secret* assistant.json
```
