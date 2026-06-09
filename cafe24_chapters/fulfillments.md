# FULFILLMENTS


## Fulfillments

```json
Endpoints    POST /api/v2/admin/fulfillments
```

```json
POST /api/v2/admin/fulfillments
```

### Fulfillments property list

| Attribute | Description |
| --- | --- |
| shop_no | 멀티쇼핑몰 번호 DEFAULT 1 |
| tracking_no | 송장번호 |
| shipping_company_code | 배송업체 코드 |
| status | 주문상태 standby : 배송대기  shipping : 배송중 |
| order_id | 주문번호 |
| shipping_code | 배송번호 |
| order_item_code | 품주코드 |
| carrier_id | 배송사 아이디 |
| post_express_flag | 우체국 택배연동 |

### Create shipping information for multiple orders via Fulfillment   cafe24

#### 기본스펙

| Property | Description |
| --- | --- |
| SCOPE | 주문 쓰기권한 (mall.write_order) |
| 호출건수 제한 | 40 |
| 1회당 요청건수 제한 | 100 |

#### 요청사양

| Parameter | Description |
| --- | --- |
| shop_no최소값: [1] | 멀티쇼핑몰 번호   DEFAULT 1 |
| tracking_noRequired최대글자수 : [30자] | 송장번호 |
| shipping_company_codeRequired | 배송업체 코드 |
| statusRequired | 주문상태   standby : 배송대기  shipping : 배송중 |
| order_id | 주문번호 |
| shipping_code | 배송번호 |
| order_item_code | 품주코드 |
| carrier_id | 배송사 아이디 |
| post_express_flag | 우체국 택배연동   S : 송장 전송 완료 |

```bash
Create shipping information for multiple orders via Fulfillment        Create shipping information for multiple orders via Fulfillment       Request   cURL Java Python Node.js PHP Go  Copy     curl -X POST \  'https://{mallid}.cafe24api.com/api/v2/admin/fulfillments' \  -H 'Authorization: Bearer {access_token}' \  -H 'Content-Type: application/json' \  -H 'X-Cafe24-Api-Version: {version}' \  -d '{    "shop_no": 1,    "requests": [        {            "tracking_no": "101080903",            "shipping_company_code": "0001",            "status": "shipping",            "order_id": "20190320-0000024",            "shipping_code": "D-20190320-0000024-00",            "order_item_code": [                "20190320-0000024-01",                "20190320-0000024-02"            ],            "carrier_id": 1,            "post_express_flag": "S"        },        {            "tracking_no": "101080904",            "shipping_company_code": "0001",            "status": "shipping",            "order_id": "20190320-0000019",            "shipping_code": "D-20190320-0000019-00",            "order_item_code": [                "20190320-0000019-01",                "20190320-0000019-02"            ],            "carrier_id": 1,            "post_express_flag": "S"        }    ]}'    Response  Copy     {    "fulfillments": [        {            "shop_no": 1,            "tracking_no": "101080903",            "shipping_company_code": "0001",            "status": "shipping",            "order_id": "20190320-0000024",            "shipping_code": "D-20190320-0000024-00",            "order_item_code": [                "20190320-0000024-01",                "20190320-0000024-02"            ],            "carrier_id": 1,            "post_express_flag": "S"        },        {            "shop_no": 1,            "tracking_no": "101080904",            "shipping_company_code": "0001",            "status": "shipping",            "order_id": "20190320-0000019",            "shipping_code": "D-20190320-0000019-01",            "order_item_code": [                "20190320-0000019-01",                "20190320-0000019-02"            ],            "carrier_id": 1,            "post_express_flag": "S"        }    ]}
```

```bash
curl -X POST \  'https://{mallid}.cafe24api.com/api/v2/admin/fulfillments' \  -H 'Authorization: Bearer {access_token}' \  -H 'Content-Type: application/json' \  -H 'X-Cafe24-Api-Version: {version}' \  -d '{    "shop_no": 1,    "requests": [        {            "tracking_no": "101080903",            "shipping_company_code": "0001",            "status": "shipping",            "order_id": "20190320-0000024",            "shipping_code": "D-20190320-0000024-00",            "order_item_code": [                "20190320-0000024-01",                "20190320-0000024-02"            ],            "carrier_id": 1,            "post_express_flag": "S"        },        {            "tracking_no": "101080904",            "shipping_company_code": "0001",            "status": "shipping",            "order_id": "20190320-0000019",            "shipping_code": "D-20190320-0000019-00",            "order_item_code": [                "20190320-0000019-01",                "20190320-0000019-02"            ],            "carrier_id": 1,            "post_express_flag": "S"        }    ]}'
```

```json
{    "fulfillments": [        {            "shop_no": 1,            "tracking_no": "101080903",            "shipping_company_code": "0001",            "status": "shipping",            "order_id": "20190320-0000024",            "shipping_code": "D-20190320-0000024-00",            "order_item_code": [                "20190320-0000024-01",                "20190320-0000024-02"            ],            "carrier_id": 1,            "post_express_flag": "S"        },        {            "shop_no": 1,            "tracking_no": "101080904",            "shipping_company_code": "0001",            "status": "shipping",            "order_id": "20190320-0000019",            "shipping_code": "D-20190320-0000019-01",            "order_item_code": [                "20190320-0000019-01",                "20190320-0000019-02"            ],            "carrier_id": 1,            "post_express_flag": "S"        }    ]}
```
