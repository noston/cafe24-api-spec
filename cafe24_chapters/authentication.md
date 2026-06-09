# AUTHENTICATION


## Authentication

### Get Authentication Code

```json
예시 코드 (요청)    GET 'https://{mallid}.cafe24api.com/api/v2/oauth/authorize?response_type=code&client_id={client_id}&state={state}&redirect_uri={redirect_uri}&scope={scope}'    예시 코드 (응답)    HTTP/1.1 302 Found
Location: {redirect_uri}?code={authorize_code}&state={state}
```

```json
GET 'https://{mallid}.cafe24api.com/api/v2/oauth/authorize?response_type=code&client_id={client_id}&state={state}&redirect_uri={redirect_uri}&scope={scope}'
```

```json
HTTP/1.1 302 Found
Location: {redirect_uri}?code={authorize_code}&state={state}
```

### Get Access Token

```bash
예시 코드 (요청)   cURL Java Python Node.js PHP Go      curl -X POST \  'https://{mallid}.cafe24api.com/api/v2/oauth/token' \  -H 'Authorization: Basic {base64_encode({client_id}:{client_secret})}' \  -H 'Content-Type: application/x-www-form-urlencoded' \  -d 'grant_type=authorization_code&code={code}&redirect_uri={redirect_uri}'    예시 코드 (응답)    HTTP/1.1 200 OK
{
    "access_token": "0iqR5nM5EJIq..........",
    "expires_at": "2021-03-01T14:00:00.000",
    "refresh_token": "JeTJ7XpnFC0P..........",
    "refresh_token_expires_at": "2021-03-15T12:00:00.000",
    "client_id": "BrIfqEKoPxeE..........",
    "mall_id": "yourmall",
    "user_id": "test",
    "scopes": [
        "mall.read_order",
        "mall.read_product",
        "mall.read_store",
        "...etc...",
    ],
    "issued_at": "2021-03-01T12:00:00.000",
    "shop_no": "1",
    "token_type": "Bearer"
}
```

```bash
curl -X POST \  'https://{mallid}.cafe24api.com/api/v2/oauth/token' \  -H 'Authorization: Basic {base64_encode({client_id}:{client_secret})}' \  -H 'Content-Type: application/x-www-form-urlencoded' \  -d 'grant_type=authorization_code&code={code}&redirect_uri={redirect_uri}'
```

```json
HTTP/1.1 200 OK
{
    "access_token": "0iqR5nM5EJIq..........",
    "expires_at": "2021-03-01T14:00:00.000",
    "refresh_token": "JeTJ7XpnFC0P..........",
    "refresh_token_expires_at": "2021-03-15T12:00:00.000",
    "client_id": "BrIfqEKoPxeE..........",
    "mall_id": "yourmall",
    "user_id": "test",
    "scopes": [
        "mall.read_order",
        "mall.read_product",
        "mall.read_store",
        "...etc...",
    ],
    "issued_at": "2021-03-01T12:00:00.000",
    "shop_no": "1",
    "token_type": "Bearer"
}
```

### Get Access Token using refresh token

```bash
예시 코드 (요청)   cURL Java Python Node.js PHP Go      curl -X POST \  'https://{mallid}.cafe24api.com/api/v2/oauth/token' \  -H 'Authorization: Basic {base64_encode({client_id}:{client_secret})}' \  -H 'Content-Type: application/x-www-form-urlencoded' \  -d 'grant_type=refresh_token&refresh_token={refresh_token}'    예시 코드 (응답)    HTTP/1.1 200 OK
{
    "access_token": "21EZes0dGSfN..........",
    "expires_at": "2021-03-01T15:50:00.000",
    "refresh_token": "xLlhWztQHBik............",
    "refresh_token_expires_at": "2021-03-15T13:50:00.000",
    "client_id": "BrIfqEKoPxeE..........",
    "mall_id": "yourmall",
    "user_id": "test",
    "scopes": [
        "mall.read_order",
        "mall.read_product",
        "mall.read_store",
        "...etc...",
    ],
    "issued_at": "2021-03-01T13:50:00.000",
    "shop_no": "1",
    "token_type": "Bearer"
}
```

```bash
curl -X POST \  'https://{mallid}.cafe24api.com/api/v2/oauth/token' \  -H 'Authorization: Basic {base64_encode({client_id}:{client_secret})}' \  -H 'Content-Type: application/x-www-form-urlencoded' \  -d 'grant_type=refresh_token&refresh_token={refresh_token}'
```

```json
HTTP/1.1 200 OK
{
    "access_token": "21EZes0dGSfN..........",
    "expires_at": "2021-03-01T15:50:00.000",
    "refresh_token": "xLlhWztQHBik............",
    "refresh_token_expires_at": "2021-03-15T13:50:00.000",
    "client_id": "BrIfqEKoPxeE..........",
    "mall_id": "yourmall",
    "user_id": "test",
    "scopes": [
        "mall.read_order",
        "mall.read_product",
        "mall.read_store",
        "...etc...",
    ],
    "issued_at": "2021-03-01T13:50:00.000",
    "shop_no": "1",
    "token_type": "Bearer"
}
```

### Revoke Access Token

```bash
예시 코드 (요청)   cURL Java Python Node.js PHP Go      curl -X POST \  'https://{mallid}.cafe24api.com/api/v2/oauth/revoke' \  -H 'Authorization: Basic {base64_encode({client_id}:{client_secret})}' \  -H 'Content-Type: application/x-www-form-urlencoded' \  -d 'token={token}&token_hint={token_hint}'    예시 코드 (응답)    HTTP/1.1 200 OK
```

```bash
curl -X POST \  'https://{mallid}.cafe24api.com/api/v2/oauth/revoke' \  -H 'Authorization: Basic {base64_encode({client_id}:{client_secret})}' \  -H 'Content-Type: application/x-www-form-urlencoded' \  -d 'token={token}&token_hint={token_hint}'
```

```json
HTTP/1.1 200 OK
```
