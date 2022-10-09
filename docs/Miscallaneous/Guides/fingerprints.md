
# Fingerprint Guide

## Fingerprint Setup

In the recent update, Discord has implemented a fingerprint check for requests made. You are now required to provide your **x-super-properties and JA3** along with **Device Useragent**. ja3 tracking is a common way of TLS fingerprinting users.

!!! warning
    Sometimes, your own fingerprint could have been **flagged** by Discord! In that case, follow the method on a different device.

#### Get JA3

To get your JA3 fingerprint, you can visit [this website](https://tls.peet.ws/api/clean) and copy the fingerprint provided under the `ja3` field. **Don't copy the `ja3_hash` field!**

#### Get X-Super-Properties and Useragent

Watch the video below to get your `X-Super-Properties` and `Useragent`.

<iframe allowfullscreen="allowfullscreen" frameborder="0" height="315" src="https://www.youtube-nocookie.com/embed/94u_rv50iuE" title="YouTube video player" width="560"></iframe>

!!! info
    **Alternatively, you can buy JA3 and Useragents from the following sellers:**   
    **[Botdiscord Sellix](https://botdiscord.sellix.io/product/6328c2d447694)** (Run by [Effe](https://t.me/effe_tg))  
    **[Mr. Token Sellix](https://mr-token.sellix.io/product/6321745b5c999)** (Run by [MrToken](https://t.me/mr_tokenman))  
  
<span style="text-decoration: underline;">**Note:**</span> We are not responsible if you get scammed by these sellers! At the time of writing, they are legitimate sellers. Once again, we are in **no way affiliated** with them nor do we earn any commissions!</p>

# About Fingerprints

### What is Browser Fingerprinting?

Browser fingerprinting (also called **device fingerprinting** or **online fingerprinting**) refers to tracking techniques that websites use to collect information about you. Modern website functions require the use of scripts — sets of instructions that tell your browser what to do. Working silently in the background, scripts can identify lots of information about your device and browser that, when stitched together, forms your unique online “fingerprint.” This fingerprint can then be traced back to you across the internet and different browsing sessions. (*skidded from: [Avast](https://www.avast.com/c-what-is-browser-fingerprinting))*

There are many ways to fingerprint users, but we will only cover the ones relevant to DMDGO.

#### Useragent

As defined by [Mozilla](https://developer.mozilla.org/en-US/docs/Web/HTTP/Headers/User-Agent), a Useragent is a request header, which contains a string allowing websites to identify the **application, operating system, vendor** and many other things.

A user agent for example, might look like this:

1. `Mozilla/5.0 (Linux; Android 9; Redmi Note 8T) AppleWebKit/537.36 (KHTML, like Gecko) Chrome/83.0.4103.96 Mobile Safari/537.36`
2. `Mozilla/5.0 (Linux; Android 9; RMX2030) AppleWebKit/537.36 (KHTML, like Gecko) Chrome/83.0.4103.83 Mobile Safari/537.36,gzip(gfe),gzip(gfe)`

The common format is:

```
User-Agent: <product> / <product-version> <comment>
```

#### JA3

JA3 is a method to fingerprint a SSL/TLS client connection based on fields in the Client Hello message from the SSL/TLS handshake. The following fields within the Client Hello message are used: SSL/TLS Version, Accepted Ciphers, List of Extensions, Elliptic Curves, and Elliptic Curve Formats. The end result being a MD5 hash serving as the purpose for the fingerprint. (*skidded from: [cqure](https://www.cqure.nl/nl/kennisplatform/hunting-with-ja3#:~:text=JA3%20is%20a%20method%20to,Curves%2C%20and%20Elliptic%20Curve%20Formats.))*

This method of fingerprinting is a bit more advanced, and harder to bypass. If you'd like to know more about bypassing ja3, you can check out [this](https://medium.com/cu-cyber/impersonating-ja3-fingerprints-b9f555880e42) article on Medium which shows how a person can impersonate ja3 by mixing cipher suites.

#### Additional Links

- [https://user-agents.net/random](https://user-agents.net/random) (Generate Useragents)
- [https://useragents.io/random](https://useragents.io/random) (Generate Useragents)
- [https://github.com/KhafraDev/discord-verify/wiki/X-Super-Properties](https://github.com/KhafraDev/discord-verify/wiki/X-Super-Properties) (About X-Super-Properties although the article may be outdated)