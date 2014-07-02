node-gracenote
==============

A node.js wrapper for the Gracenote API - https://developer.gracenote.com



## Register

Function - `api.register(req callback)`

```
var Gracenote = require("./lib/Gracenote.js");
var clientId = "XXX";
var clientTag = "YYY";
var userId = null;
var api = new Gracenote(clientId,clientTag,userId);
api.register(function(uid) {
	// store this somewhere for the next session
})`;
```

## Search For Track

Function - `api.searchTrack(req artistName, req albumTitle, req trackTitle, req callback, opt matchMode)`

```
var Gracenote = require("./lib/Gracenote.js");
var clientId = "XXX";
var clientTag = "YYY";
var userId = "ZZZ";
var api = new Gracenote(clientId,clientTag,userId);
api.searchTrack("Kings of Leon", "Only by the Night", "Sex on fire", function(result) {
	// Search Result as array
});
```

## Search for Artist

Function - `api.searchArtist(req artistName, req callback, opt matchMode)`

```
var Gracenote = require("./lib/Gracenote.js");
var clientId = "XXX";
var clientTag = "YYY";
var userId = "ZZZ";
var api = new Gracenote(clientId,clientTag,userId);
api.searchArtist("Kings of Leon", function(result) {
	// Search Result as array
});
```

## Search for Album

Function - `api.searchAlbum(req artistName, req albumTitle, req callback, opt matchMode)`

```
var Gracenote = require("./lib/Gracenote.js");
var clientId = "XXX";
var clientTag = "YYY";
var userId = "ZZZ";
var api = new Gracenote(clientId,clientTag,userId);
api.searchAlbum("Kings of Leon", "Only by the Night", function(result) {
	// Search Result as array
});
```

## Config options

`matchMode`- can be either `Gracenote.BEST_MATCH_ONLY`or `Gracenote.ALL_RESULTS`(default)
