# Invite Joiner
This page covers everything related to Invite Joiner function (opcode 1).

## Single Invite
Tokens join only 1 server with the specified invite. Works in most cases.

## Multiple Invites From File
Tokens join multiple servers, using invite codes specified in `invites.txt` in input folder.

## Other Inputs
Apart from the main inputs above, you will be required to specify other inputs being:

Name | Description |
-|-|
Number of Threads | Number of threads to use while joining tokens. If you wish to use delay, specify thread as 1.
Use additional reaction verification | Makes joined tokens react to an emoji if enabled.
ID of channel with verification message | The channel ID with the verification message to add reaction to.
ID of the message with verification reaction | The message ID of the message to add reaction to.
Enter Emoji | The emoji to react to. You can either use unicode character ("🦄") or `emojiname:id` which can be retrieved from emoji URL.
Base Delay Per Thread | The base level of delay between join of each token, applied to each thread. For example, if you set 2 threads with a base delay of 1 second, it means that 2 tokens join the server every 1 second.
Random Delay Per Thread | Approximate random delay added on top of base delay while joining tokens.

## Important Information
- As on **04-08-2022** Discord has introduced TLS fingerprinting of various paramaters such as JA3 and X_Superproperties. Accordingly, the config file now allows you to obtain your own fingerprint and provide which may help bypass it. You can obtain details from:
    - https://www.whatsmyua.info/ (User Agent)
    - https://www.youtube.com/watch?v=94u_rv50iuE (X Superproperties)
    - https://tls.peet.ws/api/clean (JA3)

- In spite of this, your fingerprint may have been flagged by Discord, which would lead to fails. To bypass this, you could try purchasing useragents and device fingerprints online.

- You would also need unflagged and tokens of high quality. Keep an eye out on quality and reputable token vendors.

- If your tokens are unable to Mass DM after inviting, try using the server checker to check if tokens are still present in the server. Many servers use anti-raid bots such as Wick and Beemo these days which use advanced algorithms to counter bots. 
In order to bypass them, you would need to first online your tokens to random status', use tokens of varying age, and finally use a single thread with a considerable amount of delay on top of random delay. 

!!! info "Note"
    Do not specify entire invite links such as `https://discord.gg/xyz` but rather just the invite code (`xyz`)
