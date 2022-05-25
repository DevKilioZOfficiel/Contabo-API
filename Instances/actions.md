# CURL
```curl
curl --location --request POST 'https://api.contabo.com/v1/compute/instances/:instances_id/actions/:action' \
--header 'Authorization: Bearer $ACCESS_TOKEN' \
--header 'x-request-id: 04e0f898-37b4-48bc-a794-1a57abe6aa31' \
--header 'x-trace-id: 123213'
```

# PHP cURL

```php
<?php

$curl = curl_init();

curl_setopt_array($curl, array(
  CURLOPT_URL => 'https://api.contabo.com/v1/compute/instances/:instances_id/actions/:action',
  CURLOPT_RETURNTRANSFER => true,
  CURLOPT_ENCODING => '',
  CURLOPT_MAXREDIRS => 10,
  CURLOPT_TIMEOUT => 0,
  CURLOPT_FOLLOWLOCATION => true,
  CURLOPT_HTTP_VERSION => CURL_HTTP_VERSION_1_1,
  CURLOPT_CUSTOMREQUEST => 'POST',
  CURLOPT_HTTPHEADER => array(
    'Authorization: Bearer $ACCESS_TOKEN',
    'x-request-id: 04e0f898-37b4-48bc-a794-1a57abe6aa31',
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

var config = {
  method: 'post',
  url: 'https://api.contabo.com/v1/compute/instances/:instances_id/actions/:action',
  headers: {
    'Authorization': 'Bearer $ACCESS_TOKEN',
    'x-request-id': '04e0f898-37b4-48bc-a794-1a57abe6aa31',
    'x-trace-id': '123213'
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
