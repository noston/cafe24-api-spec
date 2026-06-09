# SOCIALS NAVERLOGIN


## Socials naverlogin

```json
Endpoints    GET /api/v2/admin/socials/naverlogin
PUT /api/v2/admin/socials/naverlogin
```

```json
GET /api/v2/admin/socials/naverlogin
PUT /api/v2/admin/socials/naverlogin
```

### Socials naverlogin property list

| Attribute | Description |
| --- | --- |
| shop_no | 멀티쇼핑몰 번호 |
| use_naverlogin | 네이버 로그인 사용여부 |
| client_id | 클라이언트 아이디 |
| client_secret | 클라이언트 시크릿 키 |

### Naver login details   cafe24

#### 기본스펙

| Property | Description |
| --- | --- |
| SCOPE | 상점 읽기권한 (mall.read_store) |
| 호출건수 제한 | 40 |

#### 요청사양

| Parameter | Description |
| --- | --- |
| shop_no최소값: [1] | 멀티쇼핑몰 번호   DEFAULT 1 |

```bash
Naver login details        Naver login details       Request   cURL Java Python Node.js PHP Go  Copy     curl -X GET \  'https://{mallid}.cafe24api.com/api/v2/admin/socials/naverlogin' \  -H 'Authorization: Bearer {access_token}' \  -H 'Content-Type: application/json' \  -H 'X-Cafe24-Api-Version: {version}'    Response  Copy     {    "naverlogin": {        "shop_no": 1,        "use_naverlogin": "T",        "client_id": "d3t09cT11SNX22U5swHK",        "client_secret": "XxT3QPuMkU"    }}
```

```bash
curl -X GET \  'https://{mallid}.cafe24api.com/api/v2/admin/socials/naverlogin' \  -H 'Authorization: Bearer {access_token}' \  -H 'Content-Type: application/json' \  -H 'X-Cafe24-Api-Version: {version}'
```

```json
{    "naverlogin": {        "shop_no": 1,        "use_naverlogin": "T",        "client_id": "d3t09cT11SNX22U5swHK",        "client_secret": "XxT3QPuMkU"    }}
```

### Update Naver login settings   cafe24

#### 기본스펙

| Property | Description |
| --- | --- |
| SCOPE | 상점 쓰기권한 (mall.write_store) |
| 호출건수 제한 | 40 |
| 1회당 요청건수 제한 | 1 |

#### 요청사양

| Parameter | Description |
| --- | --- |
| shop_no최소값: [1] | 멀티쇼핑몰 번호   DEFAULT 1 |
| use_naverloginRequired | 네이버 로그인 사용여부   T:사용함 F:사용안함 |
| client_id형식 : [a-zA-Z0-9_-]최대글자수 : [255자] | 클라이언트 아이디 |
| client_secret형식 : [a-zA-Z0-9_-]최대글자수 : [255자] | 클라이언트 시크릿 키 |

```bash
Update Naver login settings        Update Naver login settings       Request   cURL Java Python Node.js PHP Go  Copy     curl -X PUT \  'https://{mallid}.cafe24api.com/api/v2/admin/socials/naverlogin' \  -H 'Authorization: Bearer {access_token}' \  -H 'Content-Type: application/json' \  -H 'X-Cafe24-Api-Version: {version}' \  -d '{    "shop_no": 1,    "request": {        "use_naverlogin": "T",        "client_id": "d3t09cT11SNX22U5swHK",        "client_secret": "XxT3QPuMkU"    }}'    Response  Copy     {    "naverlogin": {        "shop_no": 1,        "use_naverlogin": "T",        "client_id": "d3t09cT11SNX22U5swHK",        "client_secret": "XxT3QPuMkU"    }}
```

```bash
curl -X PUT \  'https://{mallid}.cafe24api.com/api/v2/admin/socials/naverlogin' \  -H 'Authorization: Bearer {access_token}' \  -H 'Content-Type: application/json' \  -H 'X-Cafe24-Api-Version: {version}' \  -d '{    "shop_no": 1,    "request": {        "use_naverlogin": "T",        "client_id": "d3t09cT11SNX22U5swHK",        "client_secret": "XxT3QPuMkU"    }}'
```

```json
{    "naverlogin": {        "shop_no": 1,        "use_naverlogin": "T",        "client_id": "d3t09cT11SNX22U5swHK",        "client_secret": "XxT3QPuMkU"    }}
```
