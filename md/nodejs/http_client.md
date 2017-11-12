---
layout: default 
---
## http client 

```js
const querystring = require('querystring');
var http = require('http');

var request = http.request({
	hostname: 'localhost',
	port: 80,
	path: '/auth/test.php',
	method: 'POST',
	headers: {
        // 'Content-Type' : 'application/json',
        'Content-Type': 'application/x-www-form-urlencoded'
	}

}, function(response) {
	var body = "";
	response.on('data', function(contents) {
		body += contents;
	});
	response.on('end', function() {
		console.log(response.statusCode);
		console.log(body.toString());
	});
});
request.on('error', function(e) {
	console.log("Error!", e.message);
});
request.write(querystring.stringify({
    'msg': 'Hello World!&'
}));
request.end();
```