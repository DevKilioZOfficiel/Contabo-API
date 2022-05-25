# CURL
```curl
curl --location --request POST 'https://auth.contabo.com/auth/realms/contabo/protocol/openid-connect/token' \
--data-urlencode 'client_id=API CLIENT ID HERE' \
--data-urlencode 'client_secret=API CLIENT SECRET HERE' \
--data-urlencode 'grant_type=password' \
--data-urlencode 'username=EMAIL ACCOUNT HERE' \
--data-urlencode 'password=PASSWORD API ONLY !!!'
```

# PHP cURL

```php
<?php

$curl = curl_init();

curl_setopt_array($curl, array(
  CURLOPT_URL => 'https://auth.contabo.com/auth/realms/contabo/protocol/openid-connect/token',
  CURLOPT_RETURNTRANSFER => true,
  CURLOPT_ENCODING => '',
  CURLOPT_MAXREDIRS => 10,
  CURLOPT_TIMEOUT => 0,
  CURLOPT_FOLLOWLOCATION => true,
  CURLOPT_HTTP_VERSION => CURL_HTTP_VERSION_1_1,
  CURLOPT_CUSTOMREQUEST => 'POST',
  CURLOPT_POSTFIELDS => 'client_id=API%20CLIENT%20ID%20HERE&client_secret=API%20CLIENT%20SECRET%20HERE&grant_type=password&username=EMAIL%20ACCOUNT%20HERE&password=PASSWORD%20API%20ONLY%20!!!',
));

$response = curl_exec($curl);

curl_close($curl);
echo $response;
```

# JS
```
var axios = require('axios');
var qs = require('qs');
var data = qs.stringify({
  'client_id': 'API CLIENT ID HERE',
  'client_secret': 'API CLIENT SECRET HERE',
  'grant_type': 'password',
  'username': 'EMAIL ACCOUNT HERE',
  'password': 'PASSWORD API ONLY !!!'
});
var config = {
  method: 'post',
  url: 'https://auth.contabo.com/auth/realms/contabo/protocol/openid-connect/token',
  headers: { },
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
