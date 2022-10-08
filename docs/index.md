# Quick Start
To start using DMDGO quickly, you need the following:

- Captcha API Key (capcat.xyz preferrably)
- Proxies
- [Discord Tokens](https://www.online-tech-tips.com/computer-tips/what-is-a-discord-token-and-how-to-get-one/)

!!! warning "WARNING"
  
    This guide is written keeping in mind the **Windows Operating System**. In most cases, steps are the same in any operating system, however some steps such as compiling (building from source) **_will differ_** on MacOS and Linux!



## Setting Up Captcha API
Head over to [capcat](http://capcat.xyz "Capcat does not work right now based on reports!") and add funds after creating your account. Now, copy the API key and keep it somewhere safe. This will be important later on.


## Building DMDGO From Source
- Download and install Golang and verify your installation
- Download [Source Code](https://github.com/V4NSH4J/discord-mass-DM-GO/archive/refs/heads/main.zip) and Unzip
- Open a terminal window/command prompt _in the directory_ of the source code and type `go build`
- A binary compatible with your OS should be made.

!!! info "For MACOS/LINUX"
    If there are some problems on MacOS/Linux with executing the binary as a program. You can run this command `chmod +x ./discord-mass-dm-GO` or go to `properties -> permissions -> Allow executing file as program`.


## Preparing Config
Now, we will set up the config to Mass DM. In most cases, the default config settings are OK. However, some settings could be tweaked to achieve better results.

!!! danger "CAREFUL!"
    **Only edit the other config settings if you know what you are doing. If you don't know, stick to defaults. Using the wrong config settings could potentially kill your tokens instantly!**


Now, let us use the default config. Below is a reference.
??? example "Config File"
  
    ``` yaml title="Sample Config"
    direct_message_settings:
      individual_delay: 120
      rate_limit_delay: 400
      offset: 150
      max_dms_per_token: 0
      skip_completed: true
      call: false
      remove_dead_tokens: true 
      remove_completed_members: true 
      stop_dead_tokens: true 
      check_mutual: false
      friend_before_DM: false
      online_tokens: false
      receive_messages: false
      skip_failed: false
      block_after_dm: false
      close_dm_after_message: false
      multiple_message: false
      delay_between_multiple_messages: 10

    proxy_settings:
      proxy_from_file: true
      proxy_for_captcha: true
      use_proxy_for_gateway: false
      proxy_protocol: "http"
      timeout: 60

    scraper_settings:
      scraper_delay: 3000
      scrape_usernames: false
      scrape_avatars: false
      query_brute_extra_chars: ""

    captcha_settings:
      captcha_api_key: "<your captcha API key which you saved before>"
      captcha_api: "capcat.xyz"
      max_captcha_wait: 120
      max_captcha_retry_dm: 0
      max_captcha_retry_invite: 3

    other_settings: 
      disable_keep_alives: false
      constant_cookies: false
      censor_token: true
      logs: false
      gateway_status: 4
      cfbm: false
      x_super_properties: ""
      useragent: ""

    suspicion_avoidance:
      random_individual_delay: 60
      random_rate_limit_delay: 0
      random_delay_before_dm: 10
      typing: false
      typing_variation: 250
      typing_speed: 450
      typing_base: 200

    dm_on_react:
      observer_token: ""
      change_name: true
      change_avatar: true 
      invite: ""
      server_id: ""
      channel_id: ""
      message_id: ""
      emoji: ""
      skip_completed: true 
      skip_failed: true 
      leave_token_on_ratelimit: true 
      rotate_tokens: true
      max_anti_raid_queue: 20
      max_dms_per_token: 10

    ```


## Proxy Configuration
  Depending on your proxy service, you will either need a single rotating proxy (If it rotates on each request) or several sticky proxies. Some proxies work with a `user:pass` authentication while some just require an IP authorization. 
  
 -  Now, either auth your IP address in the proxy dashboard (Proxiware requires IP auth) or Download the rotating proxy/sticky proxies. Ensure proxies are **http(s)** and not socks4/5.

!!! warning "WARNING"
    If you use a `user:pass` authenticated proxies, make sure to format the proxies as `username:password@ip:port` format! Other formats will not work and lead to an error!

- After you have the proxies, copy and paste the list to `input -> proxies.txt` file.

## Discord Tokens
Discord Tokens are necessary to use the software. Tokens are basically authorization tokens to log into a Discord Account. 

Each Discord Token is a Discord Account. They usually look like this `OTg2ODY2NDU3NjU0NzIyNjQw.GjCK44.VQ2Yqa-BxKg7-hUwf1Mzci6LK5Ay9C_oWJbY30` or `orstengemme9@hotmail.com:cq1r5K14:OTg2ODY2NDU3NjU0NzIyNjQw.GjCK44.VQ2Yqa-BxKg7-hUwf1Mzci6LK5Ay9C_oWJbY30`.

Copy the list of tokens and paste it into `input -> tokens.txt` file. Ensure your tokens are valid before you add them. You can either use DMDGO's built-in token checker (now updated to make it more feature rich!) or use [RANKTW's Checker](https://github.com/RANKTW/Discord-Token-Checker)!

!!! tip "INFO"
    DMDGO supports either just tokens or `email:password:token` format. However functions such as username and avatar changer **need email and password** to work!


## Message Config
Edit `message.json` file and enter your desired message. Note that you cannot send embeds natively anymore, hence you can only send regular text messages.

!!! info "INFO"
    Discord has recently removed embed endpoints for regular accounts. This means that users can no longer send rich embed messages. As an alternative, you can use open graph meta data to create your own embeds. Check out [Chasa's Embed Builder API](https://e.chasa.wtf/) which allows you to easily create your own URL embeds!


## Some Other Important Things
- If you wish to join tokens into the server with a delay, make sure that join threads are set to 1 to ensure proper delay is used.
- A guide to bypass anti raid bots such as Wick and Beemo are underway.
- In general, aged tokens (1-3 months) yield better results. On a new token, you get about 8-10 DM's on average for email verified, and about 30 DM's on a phone verified token. 
- Don't join more than 50 tokens at a time or use high delay of at least 20+ seconds if you wish to join more than 50 tokens.
- Just as a normal user cannot DM users without a mutual server, the same applies to DMDGO. In order to send a successful DM, the receipent must have enabled direct messages and have a mutual server with the token.

It is completely normal for tokens to use captcha/get locked after a certain number of DM's sent, owing to Discord's anti spam countermeasures.

## What Next?
Now that you've set up DMDGO, you can either check out expert guides curated by experienced users or use the `Core Documentation` to find out more about specific settings!

<div class="grid cards" markdown>
-   :material-tools:{ .lg .middle } __Start Reading Our Core Docs__

    ---

    Core documentation helps you understand the deeper nuances of DMDGO alowing you to achieve unparalleled levels of customizability and speed

    [:material-transfer-right: Get Started Now](https://red0888.github.io/DMDGO-KB/Core%20Documentation/Config%20Options/captcha%20settings/)

</div>