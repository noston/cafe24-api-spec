# ORDERS STATUS


## Orders status

```json
Endpoints    GET /api/v2/admin/orders/status
PUT /api/v2/admin/orders/status
```

```json
GET /api/v2/admin/orders/status
PUT /api/v2/admin/orders/status
```

### Orders status property list

| Attribute | Description |
| --- | --- |
| status_name_id | 주문상태 표기명 일련번호 |
| status_type | 주문상태 유형 P: 결제 및 배송 D: 후불 결제 C: 취소 R: 반품 E: 교환 U: 환불 O: 기타 |
| basic_name | 기본 표기 주문상태명 |
| custom_name | 사용자 정의 주문상태명 |
| reservation_custom_name | 예약주문 사용자 정의 주문상태명 |

### Retrieve order status displayed   cafe24

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
Retrieve order status displayed        Retrieve order status displayed       Request   cURL Java Python Node.js PHP Go  Copy     curl -X GET \  'https://{mallid}.cafe24api.com/api/v2/admin/orders/status?shop_no=1' \  -H 'Authorization: Bearer {access_token}' \  -H 'Content-Type: application/json' \  -H 'X-Cafe24-Api-Version: {version}'    Response  Copy     {    "status": [        {            "status_name_id": 1,            "status_type": "P",            "basic_name": "Awaiting Shipment",            "custom_name": "We are preparing for delivery.",            "reservation_custom_name": "Course confirmed"        },        {            "status_name_id": 35,            "status_type": "P",            "basic_name": "Pending",            "custom_name": "We're preparing a product",            "reservation_custom_name": "Application for classes"        }    ]}
```

```bash
curl -X GET \  'https://{mallid}.cafe24api.com/api/v2/admin/orders/status?shop_no=1' \  -H 'Authorization: Bearer {access_token}' \  -H 'Content-Type: application/json' \  -H 'X-Cafe24-Api-Version: {version}'
```

```json
{    "status": [        {            "status_name_id": 1,            "status_type": "P",            "basic_name": "Awaiting Shipment",            "custom_name": "We are preparing for delivery.",            "reservation_custom_name": "Course confirmed"        },        {            "status_name_id": 35,            "status_type": "P",            "basic_name": "Pending",            "custom_name": "We're preparing a product",            "reservation_custom_name": "Application for classes"        }    ]}
```

### Update order status displayed   cafe24

#### 기본스펙

| Property | Description |
| --- | --- |
| SCOPE | 상점 쓰기권한 (mall.write_store) |
| 호출건수 제한 | 40 |
| 1회당 요청건수 제한 | 100 |

#### 요청사양

| Parameter | Description |
| --- | --- |
| shop_no | 멀티쇼핑몰 번호   DEFAULT 1 |
| status_name_idRequired | 주문상태 표기명 일련번호 |
| custom_name | 사용자 정의 주문상태명 |
| reservation_custom_name | 예약주문 사용자 정의 주문상태명 |

```bash
Update order status displayed        Update order status displayed       Request   cURL Java Python Node.js PHP Go  Copy     curl -X PUT \  'https://{mallid}.cafe24api.com/api/v2/admin/orders/status' \  -H 'Authorization: Bearer {access_token}' \  -H 'Content-Type: application/json' \  -H 'X-Cafe24-Api-Version: {version}' \  -d '{    "shop_no": 1,    "requests": [        {            "status_name_id": 1,            "custom_name": "Preparing for delivery",            "reservation_custom_name": "Waiting for classes"        },        {            "status_name_id": 35,            "custom_name": "Preparing products",            "reservation_custom_name": "Application for classes"        }    ]}'    Response  Copy     {    "status": [        {            "status_name_id": 1,            "status_type": "P",            "basic_name": "Awaiting Shipment",            "custom_name": "Preparing for delivery",            "reservation_custom_name": "Waiting for classes"        },        {            "status_name_id": 35,            "status_type": "P",            "basic_name": "Pending",            "custom_name": "Preparing products",            "reservation_custom_name": "Application for classes"        }    ]}
```

```bash
curl -X PUT \  'https://{mallid}.cafe24api.com/api/v2/admin/orders/status' \  -H 'Authorization: Bearer {access_token}' \  -H 'Content-Type: application/json' \  -H 'X-Cafe24-Api-Version: {version}' \  -d '{    "shop_no": 1,    "requests": [        {            "status_name_id": 1,            "custom_name": "Preparing for delivery",            "reservation_custom_name": "Waiting for classes"        },        {            "status_name_id": 35,            "custom_name": "Preparing products",            "reservation_custom_name": "Application for classes"        }    ]}'
```

```json
{    "status": [        {            "status_name_id": 1,            "status_type": "P",            "basic_name": "Awaiting Shipment",            "custom_name": "Preparing for delivery",            "reservation_custom_name": "Waiting for classes"        },        {            "status_name_id": 35,            "status_type": "P",            "basic_name": "Pending",            "custom_name": "Preparing products",            "reservation_custom_name": "Application for classes"        }    ]}
```
