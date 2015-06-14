# FOnce
GTM ruleset to fire tags once per session/day/user.

# Installation
Import file FOnce.json to your GTM container using merge option (screenshot: http://joxi.ru/l2ZVPD5uX0bD2J).

# Usage
Use rules "FOnce - Once a session", "FOnce - Once today", "FOnce - Once a user" to fire tags you need.
If you need to add more conditions (for example: fire once a session only on a specific page), you just add that condition to the FOnce rule you need.
Note. If you just add another rule to your tag (and not a condition to a FOnce tag), that won't work how you expect (in this case your tag will fire 2 times: 1 for each rule, but not when both rules are true together).

