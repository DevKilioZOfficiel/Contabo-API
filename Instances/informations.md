# CURL
```curl
curl --location --request GET 'https://api.contabo.com/v1/compute/instances/ID SERVICE HERE' \
--header 'Content-Type: application/json' \
--header 'Authorization: Bearer TOKEN HERE' \
--header 'x-request-id: 51A87ECD-754E-4104-9C54-D01AD0F83406' \
--header 'x-trace-id: 294206'
```

# PHP cURL

```php
<?php

$curl = curl_init();

curl_setopt_array($curl, array(
  CURLOPT_URL => 'https://api.contabo.com/v1/compute/instances/ID%20SERVICE%20HERE',
  CURLOPT_RETURNTRANSFER => true,
  CURLOPT_ENCODING => '',
  CURLOPT_MAXREDIRS => 10,
  CURLOPT_TIMEOUT => 0,
  CURLOPT_FOLLOWLOCATION => true,
  CURLOPT_HTTP_VERSION => CURL_HTTP_VERSION_1_1,
  CURLOPT_CUSTOMREQUEST => 'GET',
  CURLOPT_HTTPHEADER => array(
    'Content-Type: application/json',
    'Authorization: Bearer TOKEN HERE',
    'x-request-id: 51A87ECD-754E-4104-9C54-D01AD0F83406',
    'x-trace-id: 294206'
  ),
));

$response = curl_exec($curl);

curl_close($curl);
echo $response;
```

# JS
```
var axios = require('axios');

var config = {
  method: 'get',
  url: 'https://api.contabo.com/v1/compute/instances/ID SERVICE HERE',
  headers: {
    'Content-Type': 'application/json',
    'Authorization': 'Bearer TOKEN HERE',
    'x-request-id': '51A87ECD-754E-4104-9C54-D01AD0F83406',
    'x-trace-id': '294206'
  }
};

axios(config)
.then(function (response) {
  console.log(JSON.stringify(response.data));
})
.catch(function (error) {
  console.log(error);
});
```
