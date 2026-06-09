# REDIRECTS


## Redirects

```json
Endpoints    GET /api/v2/admin/redirects
POST /api/v2/admin/redirects
PUT /api/v2/admin/redirects/{id}
DELETE /api/v2/admin/redirects/{id}
```

```json
GET /api/v2/admin/redirects
POST /api/v2/admin/redirects
PUT /api/v2/admin/redirects/{id}
DELETE /api/v2/admin/redirects/{id}
```

### Redirects property list

| Attribute | Description |
| --- | --- |
| shop_no최소값: [1]최대값: [2147483647] | 멀티쇼핑몰 번호 |
| id최대값: [2147483647] | 리다이렉트 아이디 |
| path | 리다이렉트 경로 |
| target | 대상 위치 |

### Retrieve a list of redirects   cafe24

#### 기본스펙

| Property | Description |
| --- | --- |
| SCOPE | 상점 읽기권한 (mall.read_store) |
| 호출건수 제한 | 10 |

#### 요청사양

| Parameter | Description |
| --- | --- |
| shop_no최소값: [1]최대값: [2147483647] | 멀티쇼핑몰 번호   DEFAULT 1 |
| id최소값: [1]최대값: [2147483647] | 리다이렉트 아이디 |
| path | 리다이렉트 경로 |
| target | 대상 위치 |

```bash
Retrieve a list of redirects        Retrieve a list of redirects       Request   cURL Java Python Node.js PHP Go  Copy     curl -X GET \  'https://{mallid}.cafe24api.com/api/v2/admin/redirects?shop_no=1' \  -H 'Authorization: Bearer {access_token}' \  -H 'Content-Type: application/json' \  -H 'X-Cafe24-Api-Version: {version}'    Response  Copy     {    "redirects": [        {            "shop_no": 1,            "id": 1,            "path": "/cafe24",            "target": "https://www.cafe24.com"        },        {            "shop_no": 1,            "id": 2,            "path": "/developers",            "target": "https://developers.cafe24.com"        }    ]}
```

```bash
curl -X GET \  'https://{mallid}.cafe24api.com/api/v2/admin/redirects?shop_no=1' \  -H 'Authorization: Bearer {access_token}' \  -H 'Content-Type: application/json' \  -H 'X-Cafe24-Api-Version: {version}'
```

```json
{    "redirects": [        {            "shop_no": 1,            "id": 1,            "path": "/cafe24",            "target": "https://www.cafe24.com"        },        {            "shop_no": 1,            "id": 2,            "path": "/developers",            "target": "https://developers.cafe24.com"        }    ]}
```

### Create a redirect   cafe24

#### 기본스펙

| Property | Description |
| --- | --- |
| SCOPE | 상점 쓰기권한 (mall.write_store) |
| 호출건수 제한 | 10 |
| 1회당 요청건수 제한 | 1 |

#### 요청사양

| Parameter | Description |
| --- | --- |
| shop_no최소값: [1]최대값: [2147483647] | 멀티쇼핑몰 번호   DEFAULT 1 |
| pathRequired | 리다이렉트 경로 |
| targetRequired | 대상 위치 |

```bash
Create a redirect        Create a redirect       Request   cURL Java Python Node.js PHP Go  Copy     curl -X POST \  'https://{mallid}.cafe24api.com/api/v2/admin/redirects' \  -H 'Authorization: Bearer {access_token}' \  -H 'Content-Type: application/json' \  -H 'X-Cafe24-Api-Version: {version}' \  -d '{    "shop_no": 1,    "request": {        "path": "/cafe24",        "target": "https://www.cafe24.com"    }}'    Response  Copy     {    "redirects": {        "shop_no": 1,        "id": 1,        "path": "/cafe24",        "target": "https://www.cafe24.com"    }}
```

```bash
curl -X POST \  'https://{mallid}.cafe24api.com/api/v2/admin/redirects' \  -H 'Authorization: Bearer {access_token}' \  -H 'Content-Type: application/json' \  -H 'X-Cafe24-Api-Version: {version}' \  -d '{    "shop_no": 1,    "request": {        "path": "/cafe24",        "target": "https://www.cafe24.com"    }}'
```

```json
{    "redirects": {        "shop_no": 1,        "id": 1,        "path": "/cafe24",        "target": "https://www.cafe24.com"    }}
```

### Update a redirect   cafe24

#### 기본스펙

| Property | Description |
| --- | --- |
| SCOPE | 상점 쓰기권한 (mall.write_store) |
| 호출건수 제한 | 10 |
| 1회당 요청건수 제한 | 1 |

#### 요청사양

| Parameter | Description |
| --- | --- |
| shop_no최소값: [1]최대값: [2147483647] | 멀티쇼핑몰 번호   DEFAULT 1 |
| idRequired최소값: [1]최대값: [2147483647] | 리다이렉트 아이디 |
| path | 리다이렉트 경로 |
| target | 대상 위치 |

```bash
Update a redirect        Update a redirect       Request   cURL Java Python Node.js PHP Go  Copy     curl -X PUT \  'https://{mallid}.cafe24api.com/api/v2/admin/redirects/1' \  -H 'Authorization: Bearer {access_token}' \  -H 'Content-Type: application/json' \  -H 'X-Cafe24-Api-Version: {version}' \  -d '{    "shop_no": 1,    "request": {        "path": "/cafe24",        "target": "https://www.cafe24.com"    }}'    Response  Copy     {    "redirects": {        "shop_no": 1,        "id": 1,        "path": "/cafe24",        "target": "https://www.cafe24.com"    }}
```

```bash
curl -X PUT \  'https://{mallid}.cafe24api.com/api/v2/admin/redirects/1' \  -H 'Authorization: Bearer {access_token}' \  -H 'Content-Type: application/json' \  -H 'X-Cafe24-Api-Version: {version}' \  -d '{    "shop_no": 1,    "request": {        "path": "/cafe24",        "target": "https://www.cafe24.com"    }}'
```

```json
{    "redirects": {        "shop_no": 1,        "id": 1,        "path": "/cafe24",        "target": "https://www.cafe24.com"    }}
```

### Delete a redirect   cafe24

#### 기본스펙

| Property | Description |
| --- | --- |
| SCOPE | 상점 쓰기권한 (mall.write_store) |
| 호출건수 제한 | 10 |

#### 요청사양

| Parameter | Description |
| --- | --- |
| shop_no최소값: [1]최대값: [2147483647] | 멀티쇼핑몰 번호   DEFAULT 1 |
| idRequired최소값: [1]최대값: [2147483647] | 리다이렉트 아이디 |

```bash
Delete a redirect        Delete a redirect       Request   cURL Java Python Node.js PHP Go  Copy     curl -X DELETE \  'https://{mallid}.cafe24api.com/api/v2/admin/redirects/1?shop_no=1' \  -H 'Authorization: Bearer {access_token}' \  -H 'Content-Type: application/json' \  -H 'X-Cafe24-Api-Version: {version}'    Response  Copy     {    "redirects": {        "shop_no": 1,        "id": 1    }}
```

```bash
curl -X DELETE \  'https://{mallid}.cafe24api.com/api/v2/admin/redirects/1?shop_no=1' \  -H 'Authorization: Bearer {access_token}' \  -H 'Content-Type: application/json' \  -H 'X-Cafe24-Api-Version: {version}'
```

```json
{    "redirects": {        "shop_no": 1,        "id": 1    }}
```
