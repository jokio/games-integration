Jok Games Integration
=====================
In 5 minute - You will have 5 online games integrated in your portal, it's super easy! Just follow the documentation.

Basic
=====
If you want to give your users ability to play games & have fun, it's very simple, follow the link:
```
http://[GAME_NAME].jok.io/play/[CHANNEL]?exitUrl=[EXITURL]
```
Just replace values:
* [GAME_NAME] - name of the game, which you want to integrate on your site (please see game name-s below)
* [CHANNEL] - there is possibiliy to group players using channels, empty channel means it is public
* [EXITURL] - when player press exit button, where to redirect
<br/>
<br/>

<b>GAME_NAME</b><br/>
Use one of the following game name:

```
pool - Online billiard game
reversi - Online reversi game
bg - Online backgammon game
battleship - Online battleship game
checkers - Online checkers game
```

example: ``` http://pool.jok.io/play ```
<br/>
<br/>

<b>CHANNEL</b><br/>
There are some reserved words in channel which you can't use:
```
[empty] - Public channel, where text messaging is limited.  Users can send only smiles
private - It will redirect to random private channel (random GUID)
tournament - It will redirect to tournament table, only avaliable when tournament is started
```
Use any other string as channel and group your users together

example: ``` http://pool.jok.io/play/mychannel ```
<br/>
<br/>

<b>EXITURL</b><br/>
You can pass your site url here, when player leaves table, he will be redirected to EXITURL

example: ``` http://pool.jok.io/play/mychannel?exitUrl=https://github.com/jokio/games-integration ```


<br/>
<br/>


Advanced
================================
If you want to integrate your users system, you will need to pass some extra parameters

Mandatory Paramteres:
```
ExternalID - User's unique identification in your system
Email - User's email
Fullname - First Name + ' ' + Last Name
```

Optional Parameters:
```
Nick - Users nickname, otherwise there will be auto-generated nick like Jok32952
Gender - for avatar, true - male, false - female, none - unknown
```

example: <br/>
``` http://pool.jok.io/play/mychannel?ExternalID=1&Email=contact@jok.io&Fullname=Name Surename&Nick=NinjaPlayer&Gender=true ```

<br/>
<b>Warning:</b> User must be redirected from your portal, otherwise it will not work!
