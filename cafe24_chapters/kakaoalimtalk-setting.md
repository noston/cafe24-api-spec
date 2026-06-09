# KAKAOALIMTALK SETTING


## Kakaoalimtalk setting

```json
Endpoints    GET /api/v2/admin/kakaoalimtalk/setting
PUT /api/v2/admin/kakaoalimtalk/setting
```

```json
GET /api/v2/admin/kakaoalimtalk/setting
PUT /api/v2/admin/kakaoalimtalk/setting
```

### Kakaoalimtalk setting property list

| Attribute | Description |
| --- | --- |
| shop_no | 멀티쇼핑몰 번호 DEFAULT 1 |
| use_kakaoalimtalk | 카카오알림톡 사용 여부 T: 사용함 F: 사용안함 |

### Retrieve the Kakao Info-talk settings   cafe24

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
Retrieve the Kakao Info-talk settings        Retrieve the Kakao Info-talk settings       Request   cURL Java Python Node.js PHP Go  Copy     curl -X GET \  'https://{mallid}.cafe24api.com/api/v2/admin/kakaoalimtalk/setting' \  -H 'Authorization: Bearer {access_token}' \  -H 'Content-Type: application/json' \  -H 'X-Cafe24-Api-Version: {version}'    Response  Copy     {    "kakaoalimtalk": {        "shop_no": 1,        "use_kakaoalimtalk": "T"    }}
```

```bash
curl -X GET \  'https://{mallid}.cafe24api.com/api/v2/admin/kakaoalimtalk/setting' \  -H 'Authorization: Bearer {access_token}' \  -H 'Content-Type: application/json' \  -H 'X-Cafe24-Api-Version: {version}'
```

```json
{    "kakaoalimtalk": {        "shop_no": 1,        "use_kakaoalimtalk": "T"    }}
```

### Update the Kakao Info-talk settings   cafe24

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
| use_kakaoalimtalk | 카카오알림톡 사용 여부   T: 사용함 F: 사용안함 |

```bash
Update the Kakao Info-talk settings        Update the Kakao Info-talk settings       Request   cURL Java Python Node.js PHP Go  Copy     curl -X PUT \  'https://{mallid}.cafe24api.com/api/v2/admin/kakaoalimtalk/setting' \  -H 'Authorization: Bearer {access_token}' \  -H 'Content-Type: application/json' \  -H 'X-Cafe24-Api-Version: {version}' \  -d '{    "shop_no": 1,    "request": {        "use_kakaoalimtalk": "T"    }}'    Response  Copy     {    "kakaoalimtalk": {        "shop_no": 1,        "use_kakaoalimtalk": "T"    }}
```

```bash
curl -X PUT \  'https://{mallid}.cafe24api.com/api/v2/admin/kakaoalimtalk/setting' \  -H 'Authorization: Bearer {access_token}' \  -H 'Content-Type: application/json' \  -H 'X-Cafe24-Api-Version: {version}' \  -d '{    "shop_no": 1,    "request": {        "use_kakaoalimtalk": "T"    }}'
```

```json
{    "kakaoalimtalk": {        "shop_no": 1,        "use_kakaoalimtalk": "T"    }}
```
