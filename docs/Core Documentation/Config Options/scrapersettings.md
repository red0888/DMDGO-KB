# Scraper Settings
This page covers everything related to Scraper Configuration in the `config.yml` file.

## `scraper_delay`
**Type: INT**

**Recommended Value: 3000**

Delay in **milliseconds** between 2 scrape requests.
!!! info "NOTE"
        Applies to both OPCODE 8 and OPCODE 14 scrapers.


## `scrape_usernames`
**Type: BOOLEAN**

**Recommended Value: false**

Scrapes usernames and adds it to `names.txt` file while using the scraper.

## `scrape_avatars`
**Type: BOOLEAN**

**Recommended Value: false**

Scrapes and outputs avatars to `input/pfps` folder. Works when using OPCODE 8. 

!!! danger "WARNING"
        Using this may consume a lot of proxy bandwidth. Use at your caution!


## `query_brute_extra_chars`
**Type: STRING**

**Recommended Value: NIL**

When specified, scraper also looks for usernames with specified character while scraping. This is useful for scraping usernames with unicode and zalgo characters.
