# CURL
```curl
curl --location --request PATCH 'https://api.contabo.com/v1/compute/instances/' \
--header 'Content-Type: application/json' \
--header 'Authorization: Bearer $ACCESS_TOKEN' \
--header 'x-request-id: 51A87ECD-754E-4104-9C54-D01AD0F83406' \
--header 'x-trace-id: 123213' \
--data-raw '{"imageId": "a2c26e8f-84a5-4f3e-9c0e-b06511928cc0", "sshKeys": [1,2], "rootPassword": 12}'
```

# PHP cURL

```php
<?php

$curl = curl_init();

curl_setopt_array($curl, array(
  CURLOPT_URL => 'https://api.contabo.com/v1/compute/instances/',
  CURLOPT_RETURNTRANSFER => true,
  CURLOPT_ENCODING => '',
  CURLOPT_MAXREDIRS => 10,
  CURLOPT_TIMEOUT => 0,
  CURLOPT_FOLLOWLOCATION => true,
  CURLOPT_HTTP_VERSION => CURL_HTTP_VERSION_1_1,
  CURLOPT_CUSTOMREQUEST => 'PATCH',
  CURLOPT_POSTFIELDS =>'{"imageId": "a2c26e8f-84a5-4f3e-9c0e-b06511928cc0", "sshKeys": [1,2], "rootPassword": 12}',
  CURLOPT_HTTPHEADER => array(
    'Content-Type: application/json',
    'Authorization: Bearer $ACCESS_TOKEN',
    'x-request-id: 51A87ECD-754E-4104-9C54-D01AD0F83406',
    'x-trace-id: 123213'
  ),
));

$response = curl_exec($curl);

curl_close($curl);
echo $response;
```

# JS
```
var axios = require('axios');
var data = JSON.stringify({
  "imageId": "a2c26e8f-84a5-4f3e-9c0e-b06511928cc0",
  "sshKeys": [
    1,
    2
  ],
  "rootPassword": 12
});

var config = {
  method: 'patch',
  url: 'https://api.contabo.com/v1/compute/instances/',
  headers: {
    'Content-Type': 'application/json',
    'Authorization': 'Bearer $ACCESS_TOKEN',
    'x-request-id': '51A87ECD-754E-4104-9C54-D01AD0F83406',
    'x-trace-id': '123213'
  },
  data : data
};

axios(config)
.then(function (response) {
  console.log(JSON.stringify(response.data));
})
.catch(function (error) {
  console.log(error);
});
```
