# ORDERS SALESCHANNELS


## Orders saleschannels

```json
Endpoints    GET /api/v2/admin/orders/saleschannels
POST /api/v2/admin/orders/saleschannels
PUT /api/v2/admin/orders/saleschannels/{sales_channel_id}
DELETE /api/v2/admin/orders/saleschannels/{sales_channel_id}
```

```json
GET /api/v2/admin/orders/saleschannels
POST /api/v2/admin/orders/saleschannels
PUT /api/v2/admin/orders/saleschannels/{sales_channel_id}
DELETE /api/v2/admin/orders/saleschannels/{sales_channel_id}
```

### Orders saleschannels property list

| Attribute | Description |
| --- | --- |
| sales_channel_id | 판매처 아이디 |
| sales_channel_name | 판매처 이름 |
| sales_channel_icon | 판매처 아이콘 |

### Retrieve a list of sales channels   cafe24

#### 기본스펙

| Property | Description |
| --- | --- |
| SCOPE | 주문 읽기권한 (mall.read_order) |
| 호출건수 제한 | 40 |

#### 요청사양

| Parameter | Description |
| --- | --- |
| limit최소: [1]~최대: [500] | 조회결과 최대건수   DEFAULT 10 |
| offset최대값: [10000] | 조회결과 시작위치   DEFAULT 0 |

```bash
Retrieve a list of sales channels        Retrieve a list of sales channels Retrieve saleschannels with fields parameter Retrieve saleschannels using paging       Request   cURL Java Python Node.js PHP Go  Copy     curl -X GET \  'https://{mallid}.cafe24api.com/api/v2/admin/orders/saleschannels' \  -H 'Authorization: Bearer {access_token}' \  -H 'Content-Type: application/json' \  -H 'X-Cafe24-Api-Version: {version}'    Response  Copy     {    "saleschannels": [        {            "sales_channel_id": "MORUGI",            "sales_channel_name": "MORUGI",            "sales_channel_icon": "https://img.echosting.cafe24.com/icon/ico_route_morugi.jpg"        },        {            "sales_channel_id": "gmarket",            "sales_channel_name": "gmarket",            "sales_channel_icon": "https://img.echosting.cafe24.com/icon/ico_route_gmarket.jpg"        }    ]}
```

```bash
curl -X GET \  'https://{mallid}.cafe24api.com/api/v2/admin/orders/saleschannels' \  -H 'Authorization: Bearer {access_token}' \  -H 'Content-Type: application/json' \  -H 'X-Cafe24-Api-Version: {version}'
```

```json
{    "saleschannels": [        {            "sales_channel_id": "MORUGI",            "sales_channel_name": "MORUGI",            "sales_channel_icon": "https://img.echosting.cafe24.com/icon/ico_route_morugi.jpg"        },        {            "sales_channel_id": "gmarket",            "sales_channel_name": "gmarket",            "sales_channel_icon": "https://img.echosting.cafe24.com/icon/ico_route_gmarket.jpg"        }    ]}
```

### Create a sales channel   cafe24

#### 기본스펙

| Property | Description |
| --- | --- |
| SCOPE | 주문 쓰기권한 (mall.write_order) |
| 호출건수 제한 | 40 |
| 1회당 요청건수 제한 | 1 |

#### 요청사양

| Parameter | Description |
| --- | --- |
| sales_channel_idRequired최대글자수 : [40자]형식 : [a-zA-Z0-9] | 판매처 아이디 |
| sales_channel_nameRequired최대글자수 : [100자] | 판매처 이름 |
| sales_channel_iconRequiredURL최대글자수 : [500자] | 판매처 아이콘 |

```bash
Create a sales channel        Create a sales channel Register sales channel by using only required fields Try registering sales channel by without sales_channel_id field Try registering sales channel by without sales_channel_name field       Request   cURL Java Python Node.js PHP Go  Copy     curl -X POST \  'https://{mallid}.cafe24api.com/api/v2/admin/orders/saleschannels' \  -H 'Authorization: Bearer {access_token}' \  -H 'Content-Type: application/json' \  -H 'X-Cafe24-Api-Version: {version}' \  -d '{    "request": {        "sales_channel_id": "MORUGI",        "sales_channel_name": "MORUGI",        "sales_channel_icon": "https://img.echosting.cafe24.com/icon/ico_route_morugi.jpg"    }}'    Response  Copy     {    "saleschannel": {        "sales_channel_id": "MORUGI",        "sales_channel_name": "MORUGI",        "sales_channel_icon": "https://img.echosting.cafe24.com/icon/ico_route_morugi.jpg"    }}
```

```bash
curl -X POST \  'https://{mallid}.cafe24api.com/api/v2/admin/orders/saleschannels' \  -H 'Authorization: Bearer {access_token}' \  -H 'Content-Type: application/json' \  -H 'X-Cafe24-Api-Version: {version}' \  -d '{    "request": {        "sales_channel_id": "MORUGI",        "sales_channel_name": "MORUGI",        "sales_channel_icon": "https://img.echosting.cafe24.com/icon/ico_route_morugi.jpg"    }}'
```

```json
{    "saleschannel": {        "sales_channel_id": "MORUGI",        "sales_channel_name": "MORUGI",        "sales_channel_icon": "https://img.echosting.cafe24.com/icon/ico_route_morugi.jpg"    }}
```

### Update a sales channel   cafe24

#### 기본스펙

| Property | Description |
| --- | --- |
| SCOPE | 주문 쓰기권한 (mall.write_order) |
| 호출건수 제한 | 40 |
| 1회당 요청건수 제한 | 1 |

#### 요청사양

| Parameter | Description |
| --- | --- |
| sales_channel_idRequired최대글자수 : [40자]형식 : [a-zA-Z0-9] | 판매처 아이디 |
| sales_channel_name최대글자수 : [100자] | 판매처 이름 |
| sales_channel_iconURL최대글자수 : [500자] | 판매처 아이콘 |

```bash
Update a sales channel        Update a sales channel       Request   cURL Java Python Node.js PHP Go  Copy     curl -X PUT \  'https://{mallid}.cafe24api.com/api/v2/admin/orders/saleschannels/MORUGI' \  -H 'Authorization: Bearer {access_token}' \  -H 'Content-Type: application/json' \  -H 'X-Cafe24-Api-Version: {version}' \  -d '{    "request": {        "sales_channel_name": "MORUGI",        "sales_channel_icon": "https://img.echosting.cafe24.com/icon/ico_route_morugi.jpg"    }}'    Response  Copy     {    "saleschannel": {        "sales_channel_id": "MORUGI",        "sales_channel_name": "MORUGI",        "sales_channel_icon": "https://img.echosting.cafe24.com/icon/ico_route_morugi.jpg"    }}
```

```bash
curl -X PUT \  'https://{mallid}.cafe24api.com/api/v2/admin/orders/saleschannels/MORUGI' \  -H 'Authorization: Bearer {access_token}' \  -H 'Content-Type: application/json' \  -H 'X-Cafe24-Api-Version: {version}' \  -d '{    "request": {        "sales_channel_name": "MORUGI",        "sales_channel_icon": "https://img.echosting.cafe24.com/icon/ico_route_morugi.jpg"    }}'
```

```json
{    "saleschannel": {        "sales_channel_id": "MORUGI",        "sales_channel_name": "MORUGI",        "sales_channel_icon": "https://img.echosting.cafe24.com/icon/ico_route_morugi.jpg"    }}
```

### Delete a sales channel   cafe24

#### 기본스펙

| Property | Description |
| --- | --- |
| SCOPE | 주문 쓰기권한 (mall.write_order) |
| 호출건수 제한 | 40 |

#### 요청사양

| Parameter | Description |
| --- | --- |
| sales_channel_idRequired최대글자수 : [40자]형식 : [a-zA-Z0-9] | 판매처 아이디 |

```bash
Delete a sales channel        Delete a sales channel       Request   cURL Java Python Node.js PHP Go  Copy     curl -X DELETE \  'https://{mallid}.cafe24api.com/api/v2/admin/orders/saleschannels/MORUGI' \  -H 'Authorization: Bearer {access_token}' \  -H 'Content-Type: application/json' \  -H 'X-Cafe24-Api-Version: {version}'    Response  Copy     {    "saleschannel": {        "sales_channel_id": "MORUGI"    }}
```

```bash
curl -X DELETE \  'https://{mallid}.cafe24api.com/api/v2/admin/orders/saleschannels/MORUGI' \  -H 'Authorization: Bearer {access_token}' \  -H 'Content-Type: application/json' \  -H 'X-Cafe24-Api-Version: {version}'
```

```json
{    "saleschannel": {        "sales_channel_id": "MORUGI"    }}
```
