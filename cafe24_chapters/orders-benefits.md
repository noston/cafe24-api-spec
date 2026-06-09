# ORDERS BENEFITS


## Orders benefits

```json
Endpoints    GET /api/v2/admin/orders/benefits
```

```json
GET /api/v2/admin/orders/benefits
```

### Orders benefits property list

| Attribute | Description |
| --- | --- |
| shop_no | 멀티쇼핑몰 번호 |
| order_id | 주문번호 |
| order_item_code | 품주코드 |
| benefit_no | 혜택번호 |
| benefit_title | 혜택 유형 |
| benefit_name | 혜택명 |
| benefit_code | 혜택코드 |
| benefit_percent | 혜택 비율 |
| benefit_value | 혜택 금액 |
| benefit_app_key | 앱 클라이언트 ID |

### Retrieve a list of order benefits applied to an order   cafe24 youtube

#### 기본스펙

| Property | Description |
| --- | --- |
| SCOPE | 주문 읽기권한 (mall.read_order) |
| 호출건수 제한 | 40 |

#### 요청사양

| Parameter | Description |
| --- | --- |
| shop_no최소값: [1] | 멀티쇼핑몰 번호   DEFAULT 1 |
| order_idRequired주문번호 | 주문번호   ,(콤마)로 여러 건을 검색할 수 있다. |
| limit최소: [1]~최대: [500] | 조회결과 최대건수   DEFAULT 10 |
| offset최대값: [8000] | 조회결과 시작위치   DEFAULT 0 |

```bash
Retrieve a list of order benefits applied to an order        Retrieve a list of order benefits applied to an order       Request   cURL Java Python Node.js PHP Go  Copy     curl -X GET \  'https://{mallid}.cafe24api.com/api/v2/admin/orders/benefits?order_id=20201005-0000011' \  -H 'Authorization: Bearer {access_token}' \  -H 'Content-Type: application/json' \  -H 'X-Cafe24-Api-Version: {version}'    Response  Copy     {    "benefits": [        {            "shop_no": 1,            "order_id": "20201005-0000011",            "order_item_code": "20201005-0000011-01",            "benefit_no": 900,            "benefit_title": "bulk order discount",            "benefit_name": "bulk order discount name",            "benefit_code": 966,            "benefit_percent": "10%",            "benefit_value": "500.00",            "benefit_app_key": null        },        {            "shop_no": 1,            "order_id": "20201005-0000011",            "order_item_code": "20201005-0000011-01",            "benefit_no": 901,            "benefit_title": "customer discount",            "benefit_name": "customer discount name",            "benefit_code": 967,            "benefit_percent": null,            "benefit_value": "500.00",            "benefit_app_key": null        }    ]}
```

```bash
curl -X GET \  'https://{mallid}.cafe24api.com/api/v2/admin/orders/benefits?order_id=20201005-0000011' \  -H 'Authorization: Bearer {access_token}' \  -H 'Content-Type: application/json' \  -H 'X-Cafe24-Api-Version: {version}'
```

```json
{    "benefits": [        {            "shop_no": 1,            "order_id": "20201005-0000011",            "order_item_code": "20201005-0000011-01",            "benefit_no": 900,            "benefit_title": "bulk order discount",            "benefit_name": "bulk order discount name",            "benefit_code": 966,            "benefit_percent": "10%",            "benefit_value": "500.00",            "benefit_app_key": null        },        {            "shop_no": 1,            "order_id": "20201005-0000011",            "order_item_code": "20201005-0000011-01",            "benefit_no": 901,            "benefit_title": "customer discount",            "benefit_name": "customer discount name",            "benefit_code": 967,            "benefit_percent": null,            "benefit_value": "500.00",            "benefit_app_key": null        }    ]}
```
