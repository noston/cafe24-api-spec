# LABELS


## Labels

```json
Endpoints    GET /api/v2/admin/labels
POST /api/v2/admin/labels
```

```json
GET /api/v2/admin/labels
POST /api/v2/admin/labels
```

### Labels property list

| Attribute | Description |
| --- | --- |
| shop_no | 멀티쇼핑몰 번호 |
| names | 주문 라벨명 |
| name | 주문 라벨명 |
| order_item_code | 품주코드 |

### Retrieve order labels   cafe24

#### 기본스펙

| Property | Description |
| --- | --- |
| SCOPE | 주문 읽기권한 (mall.read_order) |
| 호출건수 제한 | 40 |

#### 요청사양

| Parameter | Description |
| --- | --- |
| limit최소: [1]~최대: [1000] | 조회결과 최대건수   DEFAULT 100 |
| offset최대값: [15000] | 조회결과 시작위치   DEFAULT 0 |

```bash
Retrieve order labels        Retrieve order labels       Request   cURL Java Python Node.js PHP Go  Copy     curl -X GET \  'https://{mallid}.cafe24api.com/api/v2/admin/labels' \  -H 'Authorization: Bearer {access_token}' \  -H 'Content-Type: application/json' \  -H 'X-Cafe24-Api-Version: {version}'    Response  Copy     {    "labels": {        "shop_no": 1,        "names": [            "label_1",            "label_2"        ]    },    "links": [        {            "rel": "next",            "href": "https://{mallid}.cafe24api.com/api/v2/admin/labels?limit=100&offset=100"        }    ]}
```

```bash
curl -X GET \  'https://{mallid}.cafe24api.com/api/v2/admin/labels' \  -H 'Authorization: Bearer {access_token}' \  -H 'Content-Type: application/json' \  -H 'X-Cafe24-Api-Version: {version}'
```

```json
{    "labels": {        "shop_no": 1,        "names": [            "label_1",            "label_2"        ]    },    "links": [        {            "rel": "next",            "href": "https://{mallid}.cafe24api.com/api/v2/admin/labels?limit=100&offset=100"        }    ]}
```

### Create multiple order labels   cafe24

#### 기본스펙

| Property | Description |
| --- | --- |
| SCOPE | 주문 쓰기권한 (mall.write_order) |
| 호출건수 제한 | 40 |
| 1회당 요청건수 제한 | 10 |

#### 요청사양

| Parameter | Description |
| --- | --- |
| shop_no최소값: [1] | 멀티쇼핑몰 번호   DEFAULT 1 |
| nameRequired | 주문 라벨명 |
| order_item_codeRequired | 품주코드 |

```bash
Create multiple order labels        Create multiple order labels       Request   cURL Java Python Node.js PHP Go  Copy     curl -X POST \  'https://{mallid}.cafe24api.com/api/v2/admin/labels' \  -H 'Authorization: Bearer {access_token}' \  -H 'Content-Type: application/json' \  -H 'X-Cafe24-Api-Version: {version}' \  -d '{    "shop_no": 1,    "requests": [        {            "name": "label_1",            "order_item_code": [                "20220928-0000013-01",                "20220928-0000030-01"            ]        },        {            "name": "label_2",            "order_item_code": [                "20220928-0000013-01",                "20220928-0000030-01"            ]        }    ]}'    Response  Copy     {    "labels": [        {            "shop_no": 1,            "name": "label_1",            "order_item_code": [                "20220928-0000013-01",                "20220928-0000030-01"            ]        },        {            "shop_no": 1,            "name": "label_2",            "order_item_code": [                "20220928-0000013-01",                "20220928-0000030-01"            ]        }    ]}
```

```bash
curl -X POST \  'https://{mallid}.cafe24api.com/api/v2/admin/labels' \  -H 'Authorization: Bearer {access_token}' \  -H 'Content-Type: application/json' \  -H 'X-Cafe24-Api-Version: {version}' \  -d '{    "shop_no": 1,    "requests": [        {            "name": "label_1",            "order_item_code": [                "20220928-0000013-01",                "20220928-0000030-01"            ]        },        {            "name": "label_2",            "order_item_code": [                "20220928-0000013-01",                "20220928-0000030-01"            ]        }    ]}'
```

```json
{    "labels": [        {            "shop_no": 1,            "name": "label_1",            "order_item_code": [                "20220928-0000013-01",                "20220928-0000030-01"            ]        },        {            "shop_no": 1,            "name": "label_2",            "order_item_code": [                "20220928-0000013-01",                "20220928-0000030-01"            ]        }    ]}
```
