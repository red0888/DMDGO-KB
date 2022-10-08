# Captcha Settings
This page covers everything related to Captcha Configuration in the `config.yml` file.

## `captcha_api_key`
**Type: STRING**

**Recommended Value: NIL**

Add the API key of your service. It is needed for DMDGO to interact with captcha solver API.

## `captcha_api`
**Type: STRING**

**Recommended Value: 2captcha.com**

Captcha service which DMDGO should use to solve captchas.

??? example "Supported Services"
    ```
        rucaptcha.com
        2captcha.com
        anti-captcha.com
        capmonster.cloud
        capcat.xyz
        invisifox.com
        captchaai.com
    ```

## `max_captcha_wait`
**Type: INT**

**Recommended Value: 120**

The maximum time to wait for captcha to solve. Duration depends on captcha service used. Human based services take lot more time than AI base

## `max_captcha_retry_dm`
**Type: INT**

**Recommended Value: 0**

The maximum number of retries when captcha service provides you with an unaccepted solution. Added to prevent users from wiping out their _entire_ captcha balances! 💀💀



## `max_captcha_retry_invite`
**Type: INT**

**Recommended Value: 3**

Same as `max_captcha_retry_dm` but applies for captchas on server joins.
