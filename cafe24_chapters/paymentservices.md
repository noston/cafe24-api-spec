# PAYMENTSERVICES


## Paymentservices

```json
Endpoints    GET /api/v2/admin/paymentservices
```

```json
GET /api/v2/admin/paymentservices
```

### Paymentservices property list

| Attribute | Description |
| --- | --- |
| shop_no | 멀티쇼핑몰 번호 |
| payment_gateway_name | PG사 명 |
| partner_id | PG사 발급 가맹점 ID |
| hash_code | PG사 해시코드 |
| etc_code | PG사 기타정보 |
| payment_methods | 등록 결제수단 리스트 |

### Retrieve a list of PG settings   cafe24

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
Retrieve a list of PG settings        Retrieve a list of PG settings       Request   cURL Java Python Node.js PHP Go  Copy     curl -X GET \  'https://{mallid}.cafe24api.com/api/v2/admin/paymentservices?shop_no=1' \  -H 'Authorization: Bearer {access_token}' \  -H 'Content-Type: application/json' \  -H 'X-Cafe24-Api-Version: {version}'    Response  Copy     {    "paymentservices": [        [            {                "shop_no": 1,                "payment_gateway_name": "cafe24pay",                "partner_id": "dummy_partner_id_01",                "hash_code": "dummy_hash_code_01",                "etc_code": "dummy_etc_code_01",                "payment_methods": [                    {                        "code": "card",                        "use": "T"                    }                ]            },            {                "shop_no": 1,                "payment_gateway_name": "cafe24pay",                "partner_id": "dummy_partner_id_02",                "hash_code": "dummy_hash_code_01",                "etc_code": "dummy_etc_code_01",                "payment_methods": [                    {                        "code": "icash",                        "use": "T"                    }                ]            },            {                "shop_no": 1,                "payment_gateway_name": "inicis",                "partner_id": "dummy_partner_id_03",                "hash_code": "dummy_hash_code_02",                "etc_code": "dummy_etc_code_02",                "payment_methods": [                    {                        "code": "card",                        "use": "T"                    }                ]            },            {                "shop_no": 1,                "payment_gateway_name": "inicis",                "partner_id": "dummy_partner_id_04",                "hash_code": "dummy_hash_code_02",                "etc_code": "dummy_etc_code_02",                "payment_methods": [                    {                        "code": "tcash",                        "use": "T"                    }                ]            },            {                "shop_no": 1,                "payment_gateway_name": "inicis",                "partner_id": "dummy_partner_id_05",                "hash_code": "dummy_hash_code_02",                "etc_code": "dummy_etc_code_02",                "payment_methods": [                    {                        "code": "cvs",                        "use": "F"                    }                ]            }        ]    ]}
```

```bash
curl -X GET \  'https://{mallid}.cafe24api.com/api/v2/admin/paymentservices?shop_no=1' \  -H 'Authorization: Bearer {access_token}' \  -H 'Content-Type: application/json' \  -H 'X-Cafe24-Api-Version: {version}'
```

```json
{    "paymentservices": [        [            {                "shop_no": 1,                "payment_gateway_name": "cafe24pay",                "partner_id": "dummy_partner_id_01",                "hash_code": "dummy_hash_code_01",                "etc_code": "dummy_etc_code_01",                "payment_methods": [                    {                        "code": "card",                        "use": "T"                    }                ]            },            {                "shop_no": 1,                "payment_gateway_name": "cafe24pay",                "partner_id": "dummy_partner_id_02",                "hash_code": "dummy_hash_code_01",                "etc_code": "dummy_etc_code_01",                "payment_methods": [                    {                        "code": "icash",                        "use": "T"                    }                ]            },            {                "shop_no": 1,                "payment_gateway_name": "inicis",                "partner_id": "dummy_partner_id_03",                "hash_code": "dummy_hash_code_02",                "etc_code": "dummy_etc_code_02",                "payment_methods": [                    {                        "code": "card",                        "use": "T"                    }                ]            },            {                "shop_no": 1,                "payment_gateway_name": "inicis",                "partner_id": "dummy_partner_id_04",                "hash_code": "dummy_hash_code_02",                "etc_code": "dummy_etc_code_02",                "payment_methods": [                    {                        "code": "tcash",                        "use": "T"                    }                ]            },            {                "shop_no": 1,                "payment_gateway_name": "inicis",                "partner_id": "dummy_partner_id_05",                "hash_code": "dummy_hash_code_02",                "etc_code": "dummy_etc_code_02",                "payment_methods": [                    {                        "code": "cvs",                        "use": "F"                    }                ]            }        ]    ]}
```
