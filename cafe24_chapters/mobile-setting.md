# MOBILE SETTING


## Mobile setting

```json
Endpoints    GET /api/v2/admin/mobile/setting
PUT /api/v2/admin/mobile/setting
```

```json
GET /api/v2/admin/mobile/setting
PUT /api/v2/admin/mobile/setting
```

### Mobile setting property list

| Attribute | Description |
| --- | --- |
| shop_no | 멀티쇼핑몰 번호 |
| use_mobile_page | 모바일 쇼핑몰 사용설정 T : 사용함 F : 사용안함 |
| use_mobile_domain_redirection | 모바일 접속 주소 자동연결 설정 T : 사용함 F : 사용안함 |

### Retrieve mobile settings   cafe24

#### 기본스펙

| Property | Description |
| --- | --- |
| SCOPE | 상점 읽기권한 (mall.read_store) |
| 호출건수 제한 | 10 |

#### 요청사양

| Parameter | Description |
| --- | --- |
| shop_no | 멀티쇼핑몰 번호   DEFAULT 1 |

```bash
Retrieve mobile settings        Retrieve mobile settings       Request   cURL Java Python Node.js PHP Go  Copy     curl -X GET \  'https://{mallid}.cafe24api.com/api/v2/admin/mobile/setting' \  -H 'Authorization: Bearer {access_token}' \  -H 'Content-Type: application/json' \  -H 'X-Cafe24-Api-Version: {version}'    Response  Copy     {    "mobile": {        "shop_no": 1,        "use_mobile_page": "T",        "use_mobile_domain_redirection": "T"    }}
```

```bash
curl -X GET \  'https://{mallid}.cafe24api.com/api/v2/admin/mobile/setting' \  -H 'Authorization: Bearer {access_token}' \  -H 'Content-Type: application/json' \  -H 'X-Cafe24-Api-Version: {version}'
```

```json
{    "mobile": {        "shop_no": 1,        "use_mobile_page": "T",        "use_mobile_domain_redirection": "T"    }}
```

### Update mobile settings   cafe24

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
| use_mobile_page | 모바일 쇼핑몰 사용설정   T : 사용함 F : 사용안함 |

```bash
Update mobile settings        Update mobile settings       Request   cURL Java Python Node.js PHP Go  Copy     curl -X PUT \  'https://{mallid}.cafe24api.com/api/v2/admin/mobile/setting' \  -H 'Authorization: Bearer {access_token}' \  -H 'Content-Type: application/json' \  -H 'X-Cafe24-Api-Version: {version}' \  -d '{    "shop_no": 1,    "request": {        "use_mobile_page": "T"    }}'    Response  Copy     {    "mobile": {        "shop_no": 1,        "use_mobile_page": "T"    }}
```

```bash
curl -X PUT \  'https://{mallid}.cafe24api.com/api/v2/admin/mobile/setting' \  -H 'Authorization: Bearer {access_token}' \  -H 'Content-Type: application/json' \  -H 'X-Cafe24-Api-Version: {version}' \  -d '{    "shop_no": 1,    "request": {        "use_mobile_page": "T"    }}'
```

```json
{    "mobile": {        "shop_no": 1,        "use_mobile_page": "T"    }}
```
