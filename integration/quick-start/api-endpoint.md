# API Endpoint

> Tips:
>
> The Polygon network for Lens dApps
>
> The Optimistic network for Farcaster dApps

## API Base Link

### Based on Polygon Mainnet & Optimistic Mainnet

[https://api.tako.so](https://testapi.takoyaki.so/)

### Based on Mumbai Testnet

[https://testapi.tako.so](https://testapi.takoyaki.so/)

## How To Use

### For GET Method API

Assume you will use the API GetLensCuratorAccepted. Its route is "/v2/lens/curator/accepted".

The first step you should compose the base link with the API route:

`https://api.tako.so/v2/lens/curator/accepted?profileId=36113&cursor=0`

Please refer to the API documentation for specific parameters and requirements.

Now, you can request the full link using JavaScript, Python, cURL, etc. Then, you will receive a response from the Tako server.

### For POST method API

Like the GET method, you must pass the parameters in the request body as application/json.
