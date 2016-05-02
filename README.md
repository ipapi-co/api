
# Introduction

### Documentation for IP address location API from [ipapi.co](https://ipapi.co).  
You can use our API to lookup an IP address and get its location information. This includes city, region, country, latitude, longitude and time zone.
Both IPv4 & IPv6 type addresses are supported. 

## Get Location from a specific IP Address

This endpoint retrieves location for the IP address specified in the URL.

`GET https://ipapi.co/<IP>/json/`

### URL Parameters

Parameter | Description
--------- | -----------
IP | The IP address for which you want to retrieve the location


[`curl https://ipapi.co/8.8.8.8/json/`](https://ipapi.co/8.8.8.8/json/)



> The above command returns JSON structured like this:

 
```json
{
    "ip" : "8.8.8.8", 
    "city" : "Mountain View", 
    "region" : "California", 
    "country" : "US", 
    "postal" : "94040", 
    "latitude" : 37.3845, 
    "longitude" : -122.0881,
    "timezone" : "America/Los_Angeles"
}
```

#### Code samples in common languages 

`ruby`
```ruby
require 'net/http'
require 'json'

loc = Net::HTTP.get(URI('https://ipapi.co/8.8.8.8/json/'))
puts JSON.parse(loc)
```

`python`
```
from requests import get

loc = get('https://ipapi.co/8.8.8.8/json/')
print loc.json()
```

`php`
```
<?php
    $loc = file_get_contents('https://ipapi.co/8.8.8.8/json/');
    echo $loc;
    $obj = json_decode($loc);
?>
```

`Node.js`
```
var https = require('https');

https.get('https://ipapi.co/8.8.8.8/json/', function(resp){
    var body = ''
    resp.on('data', function(data){
        body += data;
    });

    resp.on('end', function(){
        var loc = JSON.parse(body);
        console.log(loc);
    });
});
```

`jQuery`
```
$.getJSON('https://ipapi.co/8.8.8.8/json/', function(data){
  console.log(data)
})
```


## Find your public IP Address and get its location

This endpoint retrieves location for your IP address.

`GET https://ipapi.co/json/`


[`curl https://ipapi.co/json/`](https://ipapi.co/json/)


> Retrieve location for your IP address formatted as JSON  
> (say your IP address is "208.67.222.222")

```json
{
    "ip" : "208.67.222.222", 
    "city" : "San Francisco", 
    "region" : "California", 
    "country" : "US", 
    "postal" : "94107", 
    "latitude" : 37.7697, 
    "longitude" : -122.3933,
    "timezone" : "America/Los_Angeles"
}
```

#### Code samples in common languages 

`ruby`
```
require 'net/http'
require 'json'

loc = Net::HTTP.get(URI('https://ipapi.co/json/'))
puts JSON.parse(loc)
```

`python`
```
from requests import get

loc = get('https://ipapi.co/json/')
print loc.json()
```

`php`
```
<?php
    $loc = file_get_contents('https://ipapi.co/json/');
    echo $loc;
    $obj = json_decode($loc);
?>
```

`Node.js`
```
var https = require('https');

https.get('https://ipapi.co/json/', function(resp){
    var body = ''
    resp.on('data', function(data){
        body += data;
    });

    resp.on('end', function(){
        var loc = JSON.parse(body);
        console.log(loc);
    });
});
```

`jQuery`
```
$.getJSON('https://ipapi.co/json/', function(data){
  console.log(data)
})
```

