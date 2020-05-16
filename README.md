
``` js
var request = require('request');

var headers = {
    'Content-Type': 'application/x-www-form-urlencoded; charset=UTF-8', //<-- :D
    'Authorization': 'Basic ODRh...wNGE='
};

var dataString = 'grant_type=refresh_token&refresh_token=AQCF....A3hU';

var options = {
    url: 'https://accounts.spotify.com/api/token',
    method: 'POST',
    headers: headers,
    body: dataString
};

request(options, function(error, response, body) {
  console.log(body);
});
```
