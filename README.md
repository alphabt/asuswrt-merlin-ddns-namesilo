# Asuswrt-Merlin DDNS for NameSilo

This is a custom shell script for Asuswrt-Merlin router firmware to update DDNS via NameSilo.

## Setup

1. Get an API key from [NameSilo](https://www.namesilo.com/account_api.php).

1. Add an A record in [NameSilo](https://www.namesilo.com/account_domain_manage_dns.php) for your domain (and host if you need one). IP for the record can be anything since we will update it with a script later anyway.

1. Download [ddns-start](ddns-start) file and modify the following variables with your own settings:

    `APIKEY` is your NameSilo API key

    `DOMAIN` is your domain in the A record, e.g. example.com

    `HOST` is your host/subdomain in the A record (leave it blank if you don't have one)

1. SSH to your router and place `ddns-start` under `/jffs/scripts/`

1. Make sure it's executable chmod +x /jffs/scripts/ddns-start

1. Log into the router web UI

    1. Go to `Advanced Settings` > `WAN` > `DDNS`
    1. Set `Server` to `Custom`
    1. Click the `Apply` button

## References

- <https://github.com/RMerl/asuswrt-merlin.ng/wiki/Custom-DDNS>
- <https://github.com/RMerl/asuswrt-merlin.ng/wiki/User-scripts>
