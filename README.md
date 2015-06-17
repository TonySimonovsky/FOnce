# FOnce
Ruleset for Google Tag Manager (GTM) to fire any tags once per session/day/user.

Currently only Google tags (like Doubleclick) have options within GTM to choose uniqueness of a pixel firing. The idea of FOnce is to give the ability to fire any tags or pixels you need uniquely.

> _Note_, that a session in terms of FOnce is not the same as a Google Analytics's session. FOnce operates following idea of session: _set of pageviews with an interval between seperate pageviews not more than 30 minutes_ (or whatever you set in the "FOnce - Session lifetime minutes" variable). This is pretty close to what Google Analytics consideres a session, but not totally same. There will be some discrepancy. I'm open to any suggestions how to improve this or any other part of FOnce. Please, write your suggestions to [42@stony.me](mailto:42@stony.me).

## Disclaimer
FOnce is made for GTM v2. Though it will work in GTM v1 after some simple tweaks (which will require some GTM knowledge from you), I recommend migrating to v2 if you haven't done so.

## Installation
Import file FOnce.json to your GTM container using merge option (screenshot: http://joxi.ru/l2ZVPD5uX0bD2J).

## Usage
Use rules "FOnce - Once a session", "FOnce - Once today", "FOnce - Once a user" to fire tags you need.

If you need to add more conditions (say, fire not just once a session, but once a session only on a specific page), you do simply like it is said: add a condition to the FOnce rule you are using.

> Note. If you just add another rule to your tag, that won't work how you expect (in this case your tag will fire 2 times: 1 for each rule, but not when both rules are met at the same time). So, for example, this http://joxi.ru/GrqenNbiDppWrz will fire test_tag 2 times: on the first pageview of the session and when foo-page will be opened. Instead you need to add second condition to the rule "FOnce - Once a session", like this: http://joxi.ru/8An0RyJu4bBVmO (don't forget you need to turn on "Page URL" in Variables section to see it in the list of conditions).
