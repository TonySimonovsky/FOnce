# FOnce
GTM ruleset to fire tags once per session/day/user.

Currently only Google tags (like Doubleclick) have options within GTM to choose uniqueness of a pixel firing. The idea of FOnce is to give the ability to fire any tags or pixels you need uniquely.

This ruleset was initially created for Australian advertising company <a href="http://benchmarketing.com.au/" target="_blank">Benchmarketing</a>.

## Disclaimer
FOnce is made for GTM v2. Though it will work in GTM v1 after some simple tweaks (which will require some GTM knowledge from you), I recommend migrating to v2 if you haven't done so.

## Installation
Import file FOnce.json to your GTM container using merge option (screenshot: http://joxi.ru/l2ZVPD5uX0bD2J).

## Usage
Use rules "FOnce - Once a session", "FOnce - Once today", "FOnce - Once a user" to fire tags you need.

If you need to add more conditions (say, fire not just once a session, but once a session only on a specific page), you do simply like it is said: add a condition to the FOnce rule you are using.

> Note. If you just add another rule to your tag, that won't work how you expect (in this case your tag will fire 2 times: 1 for each rule, but not when both rules are met at the same time). So, for example, this http://joxi.ru/GrqenNbiDppWrz will fire test_tag 2 times: on the first pageview of the session and when foo-page will be opened. Instead you need to add second condition to the rule "FOnce - Once a session", like this: http://joxi.ru/8An0RyJu4bBVmO (don't forget you need to turn on "Page URL" in Variables section to see it in the list of conditions).
