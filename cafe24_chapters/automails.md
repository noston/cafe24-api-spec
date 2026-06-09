# AUTOMAILS


## Automails

```json
Endpoints    GET /api/v2/admin/automails
PUT /api/v2/admin/automails
```

```json
GET /api/v2/admin/automails
PUT /api/v2/admin/automails
```

### Automails property list

| Attribute | Description |
| --- | --- |
| shop_no | 멀티쇼핑몰 번호 |
| type | 메일 항목 automails_typecode |
| use_customer | 고객 |
| use_admin | 운영자 |
| use_supplier | 공급사 |

### Retrieve automated email settings   cafe24 youtube

#### 기본스펙

| Property | Description |
| --- | --- |
| SCOPE | 알림 읽기권한 (mall.read_notification) |
| 호출건수 제한 | 40 |

#### 요청사양

| Parameter | Description |
| --- | --- |
| shop_no최소값: [1] | 멀티쇼핑몰 번호   DEFAULT 1 |

```bash
Retrieve automated email settings        Retrieve automated email settings       Request   cURL Java Python Node.js PHP Go  Copy     curl -X GET \  'https://{mallid}.cafe24api.com/api/v2/admin/automails' \  -H 'Authorization: Bearer {access_token}' \  -H 'Content-Type: application/json' \  -H 'X-Cafe24-Api-Version: {version}'    Response  Copy     {    "automails": [        {            "shop_no": 1,            "type": "G",            "use_customer": "T",            "use_admin": "T",            "use_supplier": "T"        },        {            "shop_no": 1,            "type": "H",            "use_customer": "T",            "use_admin": "T",            "use_supplier": "T"        }    ]}
```

```bash
curl -X GET \  'https://{mallid}.cafe24api.com/api/v2/admin/automails' \  -H 'Authorization: Bearer {access_token}' \  -H 'Content-Type: application/json' \  -H 'X-Cafe24-Api-Version: {version}'
```

```json
{    "automails": [        {            "shop_no": 1,            "type": "G",            "use_customer": "T",            "use_admin": "T",            "use_supplier": "T"        },        {            "shop_no": 1,            "type": "H",            "use_customer": "T",            "use_admin": "T",            "use_supplier": "T"        }    ]}
```

### Update automated email settings   cafe24 youtube

#### 기본스펙

| Property | Description |
| --- | --- |
| SCOPE | 알림 쓰기권한 (mall.write_notification) |
| 호출건수 제한 | 40 |
| 1회당 요청건수 제한 | 100 |

#### 요청사양

| Parameter | Description |
| --- | --- |
| shop_no최소값: [1] | 멀티쇼핑몰 번호   DEFAULT 1 |
| typeRequired | 메일 항목   automails_typecode |
| use_customer | 고객   T : 사용함 F : 사용안함 |
| use_admin | 운영자   T : 사용함 F : 사용안함 |
| use_supplier | 공급사   T : 사용함 F : 사용안함 |

```bash
Update automated email settings        Update automated email settings       Request   cURL Java Python Node.js PHP Go  Copy     curl -X PUT \  'https://{mallid}.cafe24api.com/api/v2/admin/automails' \  -H 'Authorization: Bearer {access_token}' \  -H 'Content-Type: application/json' \  -H 'X-Cafe24-Api-Version: {version}' \  -d '{    "shop_no": 1,    "requests": [        {            "type": "G",            "use_customer": "T",            "use_admin": "F",            "use_supplier": "T"        },        {            "type": "H",            "use_customer": "T",            "use_admin": "F",            "use_supplier": "T"        }    ]}'    Response  Copy     {    "automails": [        {            "shop_no": 1,            "type": "G",            "use_customer": "T",            "use_admin": "F",            "use_supplier": "T"        },        {            "shop_no": 1,            "type": "H",            "use_customer": "T",            "use_admin": "F",            "use_supplier": "T"        }    ]}
```

```bash
curl -X PUT \  'https://{mallid}.cafe24api.com/api/v2/admin/automails' \  -H 'Authorization: Bearer {access_token}' \  -H 'Content-Type: application/json' \  -H 'X-Cafe24-Api-Version: {version}' \  -d '{    "shop_no": 1,    "requests": [        {            "type": "G",            "use_customer": "T",            "use_admin": "F",            "use_supplier": "T"        },        {            "type": "H",            "use_customer": "T",            "use_admin": "F",            "use_supplier": "T"        }    ]}'
```

```json
{    "automails": [        {            "shop_no": 1,            "type": "G",            "use_customer": "T",            "use_admin": "F",            "use_supplier": "T"        },        {            "shop_no": 1,            "type": "H",            "use_customer": "T",            "use_admin": "F",            "use_supplier": "T"        }    ]}
```
