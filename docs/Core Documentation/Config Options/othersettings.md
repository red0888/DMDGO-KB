# Other Settings
This page covers other miscallaneous settings in the `config.yml` file.

## `disable_keep_alives`
**Type: BOOLEAN**

**Recommended Value: false**

Opens a new underlying TCP connection for each request. Highly detectable. Always keep false. But helps to rotate a rotating proxy's IP on each request when set in environment using the depracated proxy field in ProxySettings object.



## `constant_cookies`
**Type: BOOLEAN**

**Recommended Value: false**

When set to true, uses the same cookie multiple times when making requests. Sometimes, using this option gives better results, sometimes worser results.

!!!info "Additional Info"
    This cookie is provided by Discord when you login via their site/app. This cookie is required to make valid requests. Many old selfbots were patched due to this.


## `censor_token`
**Type: BOOLEAN**

**Recommended Value: NIL**

Censors the second half of the token displayed on terminal when enabled. Useful to prevent users stealing your **💎 precious 
💎**  tokkies!



## `x_super_properties`
**Type: STRING**

**Recommended Value: NIL**

Uses the `x_super_properties` parameter supplied by you. Useful to avoid detection.


## `useragent`
**Type: STRING**

**Recommended Value: NIL**

Uses the supplied useragent when making requests. You can retrieve your own useragent by visiting [here.](https://www.whatsmyua.info/)


## `logs`
**Type: BOOLEAN**

**Recommended Value: false**

Outputs a logfile when enabled, which has detailed logs covering most functions. Useful to check if an anti raid bot is present, or simply a good proof to send it to your customers if any.

## `gateway_status`
**Type: INT**

**Recommended Value: 4**

The status (ONLINE/DND/IDLE/OFFLINE) when performing scrape function. Set `4` to have a random status.