## Thursday, March 11, 2021, 8:45:00AM EST <1615470300>

Here's how I got rid of any line beginning with `!` or `#` in WeeChat
(which covers bot spam and 'back channel' Twitch chat that never hits
the screen):

```
/filter add ignore * * ^ *[!#]
```

