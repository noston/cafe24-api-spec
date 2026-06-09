# ORDERS SHIPMENTS


## Orders shipments

```json
Endpoints    GET /api/v2/admin/orders/{order_id}/shipments
POST /api/v2/admin/orders/{order_id}/shipments
PUT /api/v2/admin/orders/{order_id}/shipments/{shipping_code}
DELETE /api/v2/admin/orders/{order_id}/shipments/{shipping_code}
```

```json
GET /api/v2/admin/orders/{order_id}/shipments
POST /api/v2/admin/orders/{order_id}/shipments
PUT /api/v2/admin/orders/{order_id}/shipments/{shipping_code}
DELETE /api/v2/admin/orders/{order_id}/shipments/{shipping_code}
```

### Orders shipments property list

| Attribute | Description |
| --- | --- |
| shop_no | 멀티쇼핑몰 번호 DEFAULT 1 |
| shipping_code | 배송번호 |
| order_id | 주문번호 |
| tracking_no | 송장번호 |
| tracking_no_updated_date | 송장번호입력일 |
| shipping_company_code | 배송업체 코드 shipping_company_code |
| items | 품주 목록 |
| status | 주문상태 standby : 배송대기  shipping : 배송중  shipped : 배송완료 |
| order_item_code | 품주코드 |
| carrier_id | 배송사 아이디 |
| status_additional_info | 주문상태 추가정보 |

### Retrieve a list of shipping information of an order   cafe24 youtube

#### 기본스펙

| Property | Description |
| --- | --- |
| SCOPE | 주문 읽기권한 (mall.read_order) |
| 호출건수 제한 | 40 |

#### 요청사양

| Parameter | Description |
| --- | --- |
| shop_no최소값: [1] | 멀티쇼핑몰 번호   DEFAULT 1 |
| order_idRequired주문번호 | 주문번호 |

```bash
Retrieve a list of shipping information of an order        Retrieve a list of shipping information of an order Retrieve shipments with fields parameter       Request   cURL Java Python Node.js PHP Go  Copy         Response  Copy
```

### Create an order shipping information   cafe24 youtube

#### 기본스펙

| Property | Description |
| --- | --- |
| SCOPE | 주문 쓰기권한 (mall.write_order) |
| 호출건수 제한 | 40 |
| 1회당 요청건수 제한 | 1 |

#### 요청사양

| Parameter | Description |
| --- | --- |
| shop_no | 멀티쇼핑몰 번호   DEFAULT 1 |
| order_idRequired | 주문번호 |
| tracking_noRequired최대글자수 : [40자] | 송장번호 |
| shipping_company_codeRequired | 배송업체 코드   shipping_company_code |
| order_item_code | 품주코드 |
| statusRequired | 주문상태   standby : 배송대기  shipping : 배송중 |
| shipping_code | 배송번호 |
| carrier_id | 배송사 아이디 |

```bash
Create an order shipping information        Create an order shipping information Register shipment information using only tracking_no, shipping_company_code, and status fields Try registering shipment information without tracking_no field Try registering shipment information without shipping_company_code field Try registering shipment information without status field Standby a shipment with tracking number Process a shipment with tracking number Process specific item of the order Process a shipments with shipping code       Request   cURL Java Python Node.js PHP Go  Copy         Response  Copy
```

### Update an order shipping   cafe24 youtube

#### 기본스펙

| Property | Description |
| --- | --- |
| SCOPE | 주문 쓰기권한 (mall.write_order) |
| 호출건수 제한 | 40 |
| 1회당 요청건수 제한 | 1 |

#### 요청사양

| Parameter | Description |
| --- | --- |
| shop_no | 멀티쇼핑몰 번호   DEFAULT 1 |
| order_idRequired | 주문번호 |
| shipping_codeRequired | 배송번호 |
| status | 주문상태   status 사용하여 배송상태 수정시 tracking_no, shipping_company_code는 사용 불가   standby : 배송대기  shipping : 배송중  shipped : 배송완료 |
| status_additional_info최대글자수 : [30자] | 주문상태 추가정보 |
| tracking_no최대글자수 : [40자] | 송장번호   tracking_no 사용시 shipping_company_code를 함께 사용해야 하며, 송장번호 수정시 status는 사용 불가 |
| shipping_company_code | 배송업체 코드   shipping_company_code   tracking_no 사용시 shipping_company_code를 함께 사용해야 하며, 송장번호 수정시 status는 사용 불가 |

```bash
Update an order shipping        Update an order shipping Update shipment status of the order to standby Change tracking number and shipping company of the order       Request   cURL Java Python Node.js PHP Go  Copy         Response  Copy
```

### Delete an order shipping   cafe24 youtube

#### 기본스펙

| Property | Description |
| --- | --- |
| SCOPE | 주문 쓰기권한 (mall.write_order) |
| 호출건수 제한 | 40 |

#### 요청사양

| Parameter | Description |
| --- | --- |
| shop_no최소값: [1] | 멀티쇼핑몰 번호   DEFAULT 1 |
| order_idRequired | 주문번호 |
| shipping_codeRequired | 배송번호 |

```bash
Delete an order shipping        Delete an order shipping       Request   cURL Java Python Node.js PHP Go  Copy         Response  Copy
```
