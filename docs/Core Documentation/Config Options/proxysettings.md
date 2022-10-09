# Proxy Settings
This page covers everything related to Proxy Configuration in the `config.yml` file.

## `proxy_from_file`
**Type: BOOLEAN**

**Recommended Value: true**

Uses proxies present in `proxies.txt` file for all functions. If using a sticky proxy, the same proxy is used for the entire duration of the thread. The supported format is `username:password@ip:port` or `ip:port`. 
!!!warning "WARNING"
        DMDGO does not rotate proxies on it's own via an external API. However, most rotating proxies auto rotate at every request (backconnect rotating proxies) and it is advisable to use these.


## `proxy_for_captcha`
**Type: BOOLEAN**

**Recommended Value: false**

Passes the proxy to the captcha service to mimic captcha solve from the same IP address. Helps to avoid detection and may give better results.

!!! tip "PRO TIP"
        Each captcha service has it's own documentation on what proxy is acceptable for them. Usually they don't support IP Authorization and disallow hostnames. You can ping your proxy hostname to resolve it's IP Address and use that! (open cmd and type `ping xyz.com`)


## `use_proxy_for_gateway`
**Type: BOOLEAN**

**Recommended Value: false**
use proxy for websocket functions. Same proxy is used as the one for other actions on Discord.

## `proxy_protocol` **[DEPRECATED AS OF v1.11]**
**Type: STRING**

**Recommended Value: http**

Proxy protocol of your proxies, used for actions on Discord and sent to captcha APIs as well.

## `timeout`
**Type: INT**

**Recommended Value: 60-75**

Maximum time to wait before timing out incase of slow proxies or incase a proxy does not connect.