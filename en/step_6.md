## Setting up the Assistant API

Once your Raspberry Pi has booted, you're going to need some credentials from Google for the kit to work. Follow the steps below to enable the Google Assistant API.

[[[generic-api-google-assistant]]]

The **secrets** file that you downloaded will be called something like `client_secret_89351974213-jsno1i2s7lu9mv4q9bjbf3pas6cpnbe5.apps.googleusercontent.com.json`. You need to rename it `assistant.json` and place it in your `/home/pi` directory.

To do this, open a terminal and type:

```bash
cd ~/
mv Downloads/client_secret* assistant.json
```
