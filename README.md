# FOnce
GTM ruleset to fire tags once per session/day/user.

## Disclaimer
FOnce is made for GTM v2. Though it will work in GTM v1 after some simple tweaks (which will require some GTM knowledge from you), I recommend migrating to v2 if you haven't done so.

## Installation
Import file FOnce.json to your GTM container using merge option (screenshot: http://joxi.ru/l2ZVPD5uX0bD2J).

## Usage
Use rules "FOnce - Once a session", "FOnce - Once today", "FOnce - Once a user" to fire tags you need.
If you need to add more conditions (say, fire not just once a session, but once a session only on a specific page), you just add that condition to the FOnce rule you need (example: http://joxi.ru/DmBEbkQsl0ekrP).

> Note. If you just add another rule to your tag (and not a condition to a FOnce tag), that won't work how you expect (in this case your tag will fire 2 times: 1 for each rule, but not when both rules are true together).

