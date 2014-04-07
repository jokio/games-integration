Jok Games Integration on your site
==================================


When player press 'Play' on your site, document must be redirected to the following url:
```
http://[GAME_NAME].jok.io/play/[CHANNEL]?token=[TOKEN_HERE]&exitUrl=[EXIT_URL]
```
<br/>

Variables must be replaced with correct ones:
```
[GAME_NAME] - name of the game, which you want to integrate on your site
[CHANNEL] - there is possibiliy to group players using channels, empty channel means it is public
[TOKEN_HERE] - token which identifies your user in your system
[EXIT_URL] - when player press exit button, to redirect on your site
```
<br/>

Example:
```
http://bg.jok.io/play/?token=55ad340609f4b302&exitUrl=http://forum.ge
```


