# API Overview

## 1. API Base Link

### Based on the contracts deployed on Polygon Mainnet

[https://api.tako.so](https://testapi.takoyaki.so/)

### Based on the contracts deployed on Mumbai Testnet

[https://testapi.tako.so](https://testapi.takoyaki.so/)

## 2. How To Use

### For GET Method API

Assume you will use the API GetLensCuratorAccepted. Its route is "/v2/lens/curator/accepted".

The first step you should compose the base link with the API route:

`https://api.tako.so/v2/lens/curator/accepted?profileId=36113&cursor=0`

Please refer to the API documentation for specific parameters and requirements.

Now, you can request the full link using JavaScript, Python, cURL, etc. Then, you will receive a response from the Tako server.

### For POST method API

Like the GET method, you must pass the parameters in the request body as application/json.

## 3. Rate Limit

The cumulative number of API accesses from the same IP address should not exceed <mark style="color:red;">**180 times per minute**</mark>.

## 4. Request Format

* GET method: All parameters are included in the URL.
* POST method: All parameters are formatted as JSON data and put in the request body.

## 5. Response Format

The response is JSON format. There are four parameters at the top level:&#x20;

* status
* data
* error\_code
* error\_message

<table><thead><tr><th width="182">Parameter</th><th width="183">Data Type</th><th width="169">Visibility</th><th>Description</th></tr></thead><tbody><tr><td>status</td><td>string</td><td>Always visible</td><td>Indicate whether the API access is successful.</td></tr><tr><td>data</td><td>The return value of each API determines it.</td><td>Visible only when API access is successful</td><td>The return value of API</td></tr><tr><td>error_code</td><td>int</td><td>Visible only when API access fails</td><td>See the table “Error Code” below</td></tr><tr><td>error_message</td><td>string</td><td>Visible only when API access fails</td><td>The reason for the error</td></tr></tbody></table>

### 6. Response Example

#### When API access is successful

```json
{
    "status": "success",
    "data": {
        Object
    }
}
```

#### When API access fails

```json
{
  "status": "error",
  "error_code": 600,
  "error_msg": "The reason for error."
}
```

## 7. Error Code

<table><thead><tr><th width="122.33333333333331">Code</th><th width="208">Title</th><th>Description</th></tr></thead><tbody><tr><td>1100</td><td>InvalidRequestBody</td><td>Invalid Request Body</td></tr><tr><td>1101</td><td>InvalidParameter</td><td>Invalid Parameter</td></tr><tr><td>3000</td><td>InvalidAddress</td><td>Invalid address</td></tr><tr><td>3001</td><td>VerifyOwnerProofFail</td><td>Verify ownerProof fail</td></tr><tr><td>3002</td><td>TimeExpired</td><td>Time is expired</td></tr><tr><td>3003</td><td>TimeInvalid</td><td>Invalid time</td></tr><tr><td>3004</td><td>DuplicateVote</td><td>Duplicate vote</td></tr><tr><td>1000</td><td>InternalSystemError</td><td>System Error(1000)</td></tr><tr><td>1001</td><td>DatabaseError</td><td>System Busy(1001)</td></tr><tr><td>1002</td><td>RedisError</td><td>System Busy(1002)</td></tr><tr><td>1003</td><td>FilesystemError</td><td>System Busy(1003)</td></tr><tr><td>1004</td><td>RemoteServiceError</td><td>System Busy(1004)</td></tr></tbody></table>
