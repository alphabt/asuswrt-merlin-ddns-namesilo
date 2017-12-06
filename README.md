This is a custom shell script for Asuswrt-Merlin router firmware to update DDNS via Namesilo domain registar.

## Setup

1. Get an API key from [Namesilo](https://www.namesilo.com/account_api.php).
1. Add an A record in [Namesilo](https://www.namesilo.com/account_domain_manage_dns.php) for your domain (and host if you need one). IP for the record can be anything since we will update it with a script later anyway.
1. Download [ddns-start](https://github.com/iczman/asuswrt-merlin-namesilo-ddns/blob/master/ddns-start) file and modify the following variables with your own settings

    ```
    APIKEY="apikey"
    DOMAIN="domain"
    HOST="host" # should be blank if you don't have one
    ```

1. SSH to your router and place the script to /jffs/scripts/ddns-start
1. Log into the router web UI, go to Advanced Settings > WAN > DDNS and then set "Server" to "custom", then click the Apply button.
1. If everything goes well you should see a popup alert that says the registeration is successful.

More info on writing your own custom DDNS script:

- https://github.com/RMerl/asuswrt-merlin/wiki/Custom-DDNS
- https://github.com/RMerl/asuswrt-merlin/wiki/User-scripts
