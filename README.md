# slack-status-based-on-wifi-name
Set your status on Slack based on the WiFi network you are connected to.

## How does it work?

The script checks periodically the WiFi network name (SSID) you are connected to and sets your status on Slack according to the mapping defined in [config.js](./config.js).

## How to run it?

You need to obtain a Slack token for your account from https://api.slack.com/custom-integrations/legacy-tokens.
Copy and paste the token into [config.js] slackToken variable

You also need to have node.js installed to run the script. Currently it works on Windows and macOS only.
Install nodejs using this link: https://nodejs.org/en/download/

    node app.js

## Things to know

Be careful with defining a updateInterval value that is too low. Slack will block requests for status change if done too frequently.
Run this programa as a service (in Windows) using NSSM (the Non Sucking Service Manager) at http://nssm.cc/
Check the Indivirtual blog for more information on how to do this: http://blog.indivirtual.com/

## Shoutout
Thanks for Lukasz Wiktor for the initial code: https://github.com/LukaszWiktor/slack-status-based-on-wifi-name
