# API Overview

## 1. API Base Link

### Based on Optimistic Mainnet

[https://api.tako.so](https://testapi.takoyaki.so/)

## 2. How To Use

### For GET Method API

Assume you will use the API GetLensCuratorAccepted. Its route is "/v2/lens/curator/accepted".

The first step you should compose the base link with the API route:

`https://api.tako.so/token/profile/v1/content/discover?ecosystem=farcaster`

Please refer to the API documentation for specific parameters and requirements.

Now, you can request the full link using JavaScript, Python, cURL, etc. Then, you will receive a response from the Tako server.

### For POST method API

Like the GET method, you must pass the parameters in the request body as application/json.

## 3. Rate Limit

The cumulative number of API accesses from the same IP address should not exceed <mark style="color:red;">**60 times per minute**</mark>.

## 4. Request Format

* GET method: All parameters are included in the URL.
* POST method: All parameters are formatted as JSON data and put in the request body.
