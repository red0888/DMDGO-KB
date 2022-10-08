# Direct Message Settings
This page covers everything related to Direct Message settings in the `config.yml` file.

## `individual_delay`
**Type: INT**

**Recommended Value: 120**

Delay between 2 consecutive DM's sent by a single token in a single DMDGO instance.

## `ratelimit_delay`
**Type: INT**

**Recommended Value: 300**

Duration in seconds where a single token sleeps (stops attempting to send DM) when it gets hit with a ratelimit.

## `offset`
**Type: INT**

**Recommended Value: 100**

The delay in milliseconds by which individual threads starts one after the other. Suppose you have set a 100 millisecond delay and set 5 threads. It means that each of the 5 thread would start after a delay of 100 seconds. 

That is, in simple words, `thread 1 start -> wait 100 ms -> thread 2 start ->wait 100 ms -> thread 3 start` and so on. It is a very important feature that affects results.

!!! tip "Pro Tip"
    Recommended offset is `(60/number of tokens) * 1000` but it does not matter with a few tokens and can be set to any small value.


## `max_dms_per_token`
**Type: INT**

**Recommended Value: 0**

Self explanatory. Limits the maximum number of DM's a single token sends in total. Good option to use if you plan to reuse tokens.

## `skip_completed`
**Type: BOOLEAN**

**Recommended Value: true**

Enabling this option would skip ID's that have already been DM'ed. Completed ID's are put into `completed.txt`


## `call`
**Type: BOOLEAN**

**Recommended Value: false**

Enabling this option would make the tokens to make a missed voice call and send DM. Good for grabbing attention of users. However this is not tested much and may possibly lead to faster token locks! **USE AT YOUR OWN RISK!**

!!! info "Info"
    The user must be added as a friend with the token to make a call.


## `remove_completed_members`
**Type: BOOLEAN**

**Recommended Value: true**

Removes members who have been DM'd from `memberids.txt` once DMs are sent.

## `stop_dead_tokens`
**Type: BOOLEAN**

**Recommended Value: true**

Stops using the tokens which have been locked or disabled.

!!! tip "Info"
    It is different from `remove_dead_tokens` as enabling this option does not actually remove dead tokens from `tokens.txt` file.


## `check_mutual`
**Type: BOOLEAN**

**Recommended Value: false**

Checks mutual servers and Username before attempting to DM.

## `friend_before_DM`
**Type: BOOLEAN**

**Recommended Value: true**

Attempts to friend user before sending DM.

!!! warning "Warning"
    Requires `check_mutual` enabled to get username and discriminator.


## `online_tokens`
**Type: BOOLEAN**

**Recommended Value: false**

Onlines Discord Tokens via websockets while DM'ing.

## ` receive_messages`
**Type: BOOLEAN**

**Recommended Value: false**

Receives user messages when someone DM's a token.

!!! warning "Warning"
    Requires `online_tokens` and messages are saved to `received.txt`


## `skip_failed`
**Type: BOOLEAN**

**Recommended Value: false**

Skips Users who have been attempted to DM but failed. Uses the list from `failed.txt`.

## `block_after_dm`
**Type: BOOLEAN**

**Recommended Value: false**

Blocks the user after sending DM.

## `close_dm_after_message`
**Type: BOOLEAN**

**Recommended Value: false**

Closes the DM after sending a successful DM to the user.

## `multiple_message`
**Type: BOOLEAN**

**Recommended Value: false**

If enabled, will send multiple message to the user. You can add multiple messages to `message.json`. If disabled, tokens would randomly pick a message and DM once. If enabled however, tokens would message every single message provided to the same user with each message being sent after the delay specified in `delay_between_multiple_messages`.

??? example "Sample Config"
    ```json
    [
      {
        "content": "Hi <user> join my telegram server https://t.me/tosviolators"
      },
      {
        "content": "We had a discord but it got terminated"
      },
      {
        "content": "We might make one again but too lazy to do so"
      }
    ]
    ```




## `delay_between_multiple_messages`
**Type: INT**

**Recommended Value: 10**

Delay between sending the second message in seconds.

!!! warning "Warning"
    Multiple Messages are still experimental. You may face issues while using these. It is advised to keep it disabled by default.
