# STORE SETTING


## Store setting

```json
Endpoints    GET /api/v2/admin/store/setting
PUT /api/v2/admin/store/setting
```

```json
GET /api/v2/admin/store/setting
PUT /api/v2/admin/store/setting
```

### Store setting property list

| Attribute | Description |
| --- | --- |
| shop_no | 멀티쇼핑몰 번호 |
| name_input_style | 이름 입력 방식 SEPARATE: 성/이름 각각 입력 COMBINED: 성/이름 한번에 입력 |

### Retrieve store security settings   cafe24

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
Retrieve store security settings        Retrieve store security settings       Request   cURL Java Python Node.js PHP Go  Copy     curl -X GET \  'https://{mallid}.cafe24api.com/api/v2/admin/store/setting' \  -H 'Authorization: Bearer {access_token}' \  -H 'Content-Type: application/json' \  -H 'X-Cafe24-Api-Version: {version}'    Response  Copy     {    "store": {        "shop_no": 1,        "name_input_style": "SEPARATE"    }}
```

```bash
curl -X GET \  'https://{mallid}.cafe24api.com/api/v2/admin/store/setting' \  -H 'Authorization: Bearer {access_token}' \  -H 'Content-Type: application/json' \  -H 'X-Cafe24-Api-Version: {version}'
```

```json
{    "store": {        "shop_no": 1,        "name_input_style": "SEPARATE"    }}
```

### Edit store security settings   cafe24

#### 기본스펙

| Property | Description |
| --- | --- |
| SCOPE | 상점 쓰기권한 (mall.write_store) |
| 호출건수 제한 | 30 |
| 1회당 요청건수 제한 | 1 |

#### 요청사양

| Parameter | Description |
| --- | --- |
| shop_no최소값: [1] | 멀티쇼핑몰 번호   DEFAULT 1 |
| name_input_style | 이름 입력 방식   SEPARATE: 성/이름 각각 입력 COMBINED: 성/이름 한번에 입력 |

```bash
Edit store security settings        Edit store security settings       Request   cURL Java Python Node.js PHP Go  Copy     curl -X PUT \  'https://{mallid}.cafe24api.com/api/v2/admin/store/setting' \  -H 'Authorization: Bearer {access_token}' \  -H 'Content-Type: application/json' \  -H 'X-Cafe24-Api-Version: {version}' \  -d '{    "shop_no": 1,    "request": {        "name_input_style": "SEPARATE"    }}'    Response  Copy     {    "store": {        "shop_no": 1,        "name_input_style": "SEPARATE"    }}
```

```bash
curl -X PUT \  'https://{mallid}.cafe24api.com/api/v2/admin/store/setting' \  -H 'Authorization: Bearer {access_token}' \  -H 'Content-Type: application/json' \  -H 'X-Cafe24-Api-Version: {version}' \  -d '{    "shop_no": 1,    "request": {        "name_input_style": "SEPARATE"    }}'
```

```json
{    "store": {        "shop_no": 1,        "name_input_style": "SEPARATE"    }}
```
