# SHIPMENTS


## Shipments

```json
Endpoints    POST /api/v2/admin/shipments
PUT /api/v2/admin/shipments
```

```json
POST /api/v2/admin/shipments
PUT /api/v2/admin/shipments
```

### Shipments property list

| Attribute | Description |
| --- | --- |
| shop_no | 멀티쇼핑몰 번호 |
| tracking_no | 송장번호 |
| shipping_company_code | 배송업체 코드 shipping_company_code |
| status | 주문상태 standby : 배송대기  shipping : 배송중  shipped : 배송완료 |
| order_id | 주문번호 |
| shipping_code | 배송번호 |
| order_item_code | 품주코드 |
| carrier_id | 배송사 아이디 |
| status_additional_info | 주문상태 추가정보 |

### Create shipping information for multiple orders   cafe24 youtube

#### 기본스펙

| Property | Description |
| --- | --- |
| SCOPE | 주문 쓰기권한 (mall.write_order) |
| 호출건수 제한 | 40 |
| 1회당 요청건수 제한 | 100 |

#### 요청사양

| Parameter | Description |
| --- | --- |
| shop_no | 멀티쇼핑몰 번호   DEFAULT 1 |
| tracking_noRequired최대글자수 : [40자] | 송장번호 |
| shipping_company_codeRequired | 배송업체 코드   shipping_company_code |
| statusRequired | 주문상태   standby : 배송대기  shipping : 배송중 |
| order_id | 주문번호 |
| shipping_code | 배송번호 |
| order_item_code | 품주코드 |
| carrier_id | 배송사 아이디 |

```bash
Create shipping information for multiple orders        Create shipping information for multiple orders Standby multiple shipments with tracking number Process multiple shipments with tracking number Process specific item of multiple orders Process multiple shipments with shipping code       Request   cURL Java Python Node.js PHP Go  Copy     curl -X POST \  'https://{mallid}.cafe24api.com/api/v2/admin/shipments' \  -H 'Authorization: Bearer {access_token}' \  -H 'Content-Type: application/json' \  -H 'X-Cafe24-Api-Version: {version}' \  -d '{    "shop_no": 1,    "requests": [        {            "tracking_no": "101080903",            "shipping_company_code": "0001",            "status": "shipping",            "order_id": "20190320-0000024",            "shipping_code": "D-20190320-0000024-00",            "order_item_code": [                "20190320-0000024-01",                "20190320-0000024-02"            ],            "carrier_id": 1        },        {            "tracking_no": "101080904",            "shipping_company_code": "0001",            "status": "shipping",            "order_id": "20190320-0000019",            "shipping_code": "D-20190320-0000019-00",            "order_item_code": [                "20190320-0000019-01",                "20190320-0000019-02"            ],            "carrier_id": 1        }    ]}'    Response  Copy     {    "shipments": [        {            "shop_no": 1,            "tracking_no": "101080903",            "shipping_company_code": "0001",            "status": "shipping",            "order_id": "20190320-0000024",            "shipping_code": "D-20190320-0000024-00",            "order_item_code": [                "20190320-0000024-01",                "20190320-0000024-02"            ],            "carrier_id": 1        },        {            "shop_no": 1,            "tracking_no": "101080904",            "shipping_company_code": "0001",            "status": "shipping",            "order_id": "20190320-0000019",            "shipping_code": "D-20190320-0000019-01",            "order_item_code": [                "20190320-0000019-01",                "20190320-0000019-02"            ],            "carrier_id": 1        }    ]}
```

```bash
curl -X POST \  'https://{mallid}.cafe24api.com/api/v2/admin/shipments' \  -H 'Authorization: Bearer {access_token}' \  -H 'Content-Type: application/json' \  -H 'X-Cafe24-Api-Version: {version}' \  -d '{    "shop_no": 1,    "requests": [        {            "tracking_no": "101080903",            "shipping_company_code": "0001",            "status": "shipping",            "order_id": "20190320-0000024",            "shipping_code": "D-20190320-0000024-00",            "order_item_code": [                "20190320-0000024-01",                "20190320-0000024-02"            ],            "carrier_id": 1        },        {            "tracking_no": "101080904",            "shipping_company_code": "0001",            "status": "shipping",            "order_id": "20190320-0000019",            "shipping_code": "D-20190320-0000019-00",            "order_item_code": [                "20190320-0000019-01",                "20190320-0000019-02"            ],            "carrier_id": 1        }    ]}'
```

```json
{    "shipments": [        {            "shop_no": 1,            "tracking_no": "101080903",            "shipping_company_code": "0001",            "status": "shipping",            "order_id": "20190320-0000024",            "shipping_code": "D-20190320-0000024-00",            "order_item_code": [                "20190320-0000024-01",                "20190320-0000024-02"            ],            "carrier_id": 1        },        {            "shop_no": 1,            "tracking_no": "101080904",            "shipping_company_code": "0001",            "status": "shipping",            "order_id": "20190320-0000019",            "shipping_code": "D-20190320-0000019-01",            "order_item_code": [                "20190320-0000019-01",                "20190320-0000019-02"            ],            "carrier_id": 1        }    ]}
```

### Update multiple order shippings   cafe24 youtube

#### 기본스펙

| Property | Description |
| --- | --- |
| SCOPE | 주문 쓰기권한 (mall.write_order) |
| 호출건수 제한 | 40 |
| 1회당 요청건수 제한 | 100 |

#### 요청사양

| Parameter | Description |
| --- | --- |
| shop_no | 멀티쇼핑몰 번호   DEFAULT 1 |
| shipping_codeRequired | 배송번호 |
| order_id | 주문번호 |
| status | 주문상태   status 사용하여 배송상태 수정시 tracking_no, shipping_company_code는 사용 불가   standby : 배송대기  shipping : 배송중  shipped : 배송완료 |
| status_additional_info최대글자수 : [30자] | 주문상태 추가정보 |
| tracking_no최대글자수 : [40자] | 송장번호   tracking_no 사용시 shipping_company_code를 함께 사용해야 하며, 송장번호 수정시 status는 사용 불가 |
| shipping_company_code | 배송업체 코드   해당 주문의 송장번호와 함께 배송사를 변경할 수 있다.  shipping_company_code   tracking_no 사용시 shipping_company_code를 함께 사용해야 하며, 송장번호 수정시 status는 사용 불가 |

```bash
Update multiple order shippings        Update multiple order shippings Update shipment status of multiple orders to standby Change tracking number and shipping company of mutiple orders       Request   cURL Java Python Node.js PHP Go  Copy     curl -X PUT \  'https://{mallid}.cafe24api.com/api/v2/admin/shipments' \  -H 'Authorization: Bearer {access_token}' \  -H 'Content-Type: application/json' \  -H 'X-Cafe24-Api-Version: {version}' \  -d '{    "shop_no": 1,    "requests": [        {            "shipping_code": "D-20190108-0000791-00",            "order_id": "20190108-0000791",            "status": "shipped",            "status_additional_info": null,            "tracking_no": null,            "shipping_company_code": null        },        {            "shipping_code": "D-20190108-0000801-00",            "order_id": "20190108-0000801",            "status": "shipped",            "status_additional_info": null,            "tracking_no": null,            "shipping_company_code": null        }    ]}'    Response  Copy     {    "shipments": [        {            "shop_no": 1,            "shipping_code": "D-20190108-0000791-00",            "order_id": "20190108-0000791",            "status": "shipped",            "status_additional_info": "Arrived at Sorting Hub",            "tracking_no": null,            "shipping_company_code": null        },        {            "shop_no": 1,            "shipping_code": "D-20190108-0000801-00",            "order_id": "20190108-0000801",            "status": "shipped",            "status_additional_info": "Arrived at Sorting Hub",            "tracking_no": null,            "shipping_company_code": null        }    ]}
```

```bash
curl -X PUT \  'https://{mallid}.cafe24api.com/api/v2/admin/shipments' \  -H 'Authorization: Bearer {access_token}' \  -H 'Content-Type: application/json' \  -H 'X-Cafe24-Api-Version: {version}' \  -d '{    "shop_no": 1,    "requests": [        {            "shipping_code": "D-20190108-0000791-00",            "order_id": "20190108-0000791",            "status": "shipped",            "status_additional_info": null,            "tracking_no": null,            "shipping_company_code": null        },        {            "shipping_code": "D-20190108-0000801-00",            "order_id": "20190108-0000801",            "status": "shipped",            "status_additional_info": null,            "tracking_no": null,            "shipping_company_code": null        }    ]}'
```

```json
{    "shipments": [        {            "shop_no": 1,            "shipping_code": "D-20190108-0000791-00",            "order_id": "20190108-0000791",            "status": "shipped",            "status_additional_info": "Arrived at Sorting Hub",            "tracking_no": null,            "shipping_company_code": null        },        {            "shop_no": 1,            "shipping_code": "D-20190108-0000801-00",            "order_id": "20190108-0000801",            "status": "shipped",            "status_additional_info": "Arrived at Sorting Hub",            "tracking_no": null,            "shipping_company_code": null        }    ]}
```
