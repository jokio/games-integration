Jok Games Integration
=====================


Basic
-----
If you want to give your users ability to play games & have fun, it's very simple, just follow the link:
```
http://[GAME_NAME].jok.io/play/[CHANNEL]?exitUrl=[EXIT_URL]
```
Just replace values:
* [GAME_NAME] - name of the game, which you want to integrate on your site (please see reserved game key-s below)
* [CHANNEL] - there is possibiliy to group players using channels, empty channel means it is public
* [EXIT_URL] - when player press exit button, where to redirect



Advanced
--------
You can use your users system and integrate them at jok games. In advanced mode there are two more steps:

1. Create http handler on your server using following parameters
```
Input:
token - your site user token
```

```json
Output (JSON):
{
  ID,         -- Unique identifier in your system [MANDATORY]
  Email,      -- User email address [OPTIONAL]
  Fullname,   -- User Full name [OPTIONAL]
  Gender      -- User Gender [OPTIONAL]
}
```

```
example:
http://path.to.your.handler/?token=[YOUR_SITE_USER_TOKEN]
```


2. Register your handler 

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

