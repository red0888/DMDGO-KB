# DM On React
This page covers everything related to DM on react settings in `config.yml` file.

## `observer_token`
**Type: STRING**

**Recommended Value: NIL**

The token that scans for new reactions added. This token is only used for scanning reacts and not used to DM.



## `change_name`
**Type: BOOLEAN**

**Recommended Value: true**

An instance token changes name before sending DMs to people approved by observer token. Requires tokens in format `email:pass:token`.

## `change_avatar`
**Type: BOOLEAN**

**Recommended Value: false**

An instance token changes avatar before sending DMs to people apporved by observer token.



## `invite`
**Type: STRING**

**Recommended Value: NIL**

Invite to the server where you're running DM on react, to join tokens when they're needed so they don't get kicked. If not specified, the bot will assume the tokens are already present in the server


## `server_id`
**Type: STRING**

**Recommended Value: NIL**

Server ID where you're running the DM on react. If not specified, tokens will try to send to every reaction regardless of server sniffed by observer token. This is required for other things like checking if Token is in server or not, it's highly recommended you specify this field.

## `channel_id`

**Type: STRING**

**Recommended Value: NIL**

Channel ID where you want to send messages to reactions. If left blank, bot will send DMs to reacts in all channels in the server.


## `message_id`

**Type: STRING**

**Recommended Value: NIL**

Message ID of the message on which you want to send people DMs who react. If left blank, would send DMs to all messages in the channel.

## `emoji`

**Type: STRING**

**Recommended Value: emojiname:id**

The emoji when reacted with the message will be sent. Unicode emojis have to be entered just as the emoji. Example: `"🚀"`

For custom/nitro emojis you have to input `emoji_name:emoji_id` which you can get from the emoji's URL. If left blank, messages will be sent to every reaction on the message.

## `rotate_tokens`

**Type: BOOLEAN**

**Recommended Value: true**

Re-uses tokens from a pool. Suppose if token was rate limited, it would be switched but later be returned to to be reused.

## `max_anti_raid_queue`

**Type: INT**

**Recommended Value: 20**

To ensure someone does not spam reactions to jam your bot and lock your instances, you can set the maximum queue size. Any reactions above this would be discarded. This will easily help bypass mass emoji reacts breaking the bot.

## `max_dms_per_token`

**Type: INT**

**Recommended Value: 0**

Maximum DMs you want your tokens to send. Set 0 for unlimited.