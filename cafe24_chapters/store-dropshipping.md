# STORE DROPSHIPPING


## Store dropshipping

```json
Endpoints    GET /api/v2/admin/store/dropshipping
PUT /api/v2/admin/store/dropshipping
```

```json
GET /api/v2/admin/store/dropshipping
PUT /api/v2/admin/store/dropshipping
```

### Store dropshipping property list

| Attribute | Description |
| --- | --- |
| shop_no | 멀티쇼핑몰 번호 |
| name | 드롭쉬핑 공급사명 |
| use | 드롭쉬핑 계정연동 여부 T : 연동함 F : 연동안함 |

### Retrieve dropshipping settings   cafe24

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
Retrieve dropshipping settings        Retrieve dropshipping settings       Request   cURL Java Python Node.js PHP Go  Copy     curl -X GET \  'https://{mallid}.cafe24api.com/api/v2/admin/store/dropshipping?shop_no=1' \  -H 'Authorization: Bearer {access_token}' \  -H 'Content-Type: application/json' \  -H 'X-Cafe24-Api-Version: {version}'    Response  Copy     {    "dropshipping": [        {            "shop_no": 1,            "name": "ALI",            "use": "T"        },        {            "shop_no": 1,            "name": "SAMPLE",            "use": "F"        }    ]}
```

```bash
curl -X GET \  'https://{mallid}.cafe24api.com/api/v2/admin/store/dropshipping?shop_no=1' \  -H 'Authorization: Bearer {access_token}' \  -H 'Content-Type: application/json' \  -H 'X-Cafe24-Api-Version: {version}'
```

```json
{    "dropshipping": [        {            "shop_no": 1,            "name": "ALI",            "use": "T"        },        {            "shop_no": 1,            "name": "SAMPLE",            "use": "F"        }    ]}
```

### Manage dropshipping settings   cafe24

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
| nameRequired최대글자수 : [50자] | 드롭쉬핑 공급사명 |
| useRequired | 드롭쉬핑 계정연동 여부   T : 연동함 F : 연동안함 |

```bash
Manage dropshipping settings        Manage dropshipping settings       Request   cURL Java Python Node.js PHP Go  Copy     curl -X PUT \  'https://{mallid}.cafe24api.com/api/v2/admin/store/dropshipping' \  -H 'Authorization: Bearer {access_token}' \  -H 'Content-Type: application/json' \  -H 'X-Cafe24-Api-Version: {version}' \  -d '{    "shop_no": 1,    "request": {        "name": "ALI",        "use": "T"    }}'    Response  Copy     {    "dropshipping": [        {            "shop_no": 1,            "name": "ALI",            "use": "T"        },        {            "shop_no": 1,            "name": "SAMPLE",            "use": "F"        }    ]}
```

```bash
curl -X PUT \  'https://{mallid}.cafe24api.com/api/v2/admin/store/dropshipping' \  -H 'Authorization: Bearer {access_token}' \  -H 'Content-Type: application/json' \  -H 'X-Cafe24-Api-Version: {version}' \  -d '{    "shop_no": 1,    "request": {        "name": "ALI",        "use": "T"    }}'
```

```json
{    "dropshipping": [        {            "shop_no": 1,            "name": "ALI",            "use": "T"        },        {            "shop_no": 1,            "name": "SAMPLE",            "use": "F"        }    ]}
```
