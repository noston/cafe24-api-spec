# ORDERS COUPONS


## Orders coupons

```json
Endpoints    GET /api/v2/admin/orders/coupons
```

```json
GET /api/v2/admin/orders/coupons
```

### Orders coupons property list

| Attribute | Description |
| --- | --- |
| shop_no | 멀티쇼핑몰 번호 |
| order_id | 주문번호 |
| order_item_code | 품주코드 |
| coupon_name | 쿠폰명 |
| coupon_code | 쿠폰번호 |
| coupon_percent | 쿠폰 비율 |
| coupon_value | 쿠폰 금액 |
| coupon_value_final | 최종 쿠폰 금액 |

### Retrieve a list of coupons applied to an order   cafe24

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
Retrieve a list of coupons applied to an order        Retrieve a list of coupons applied to an order       Request   cURL Java Python Node.js PHP Go  Copy     curl -X GET \  'https://{mallid}.cafe24api.com/api/v2/admin/orders/coupons?order_id=20201005-0000011' \  -H 'Authorization: Bearer {access_token}' \  -H 'Content-Type: application/json' \  -H 'X-Cafe24-Api-Version: {version}'    Response  Copy     {    "coupons": [        {            "shop_no": 1,            "order_id": "20201005-0000011",            "order_item_code": "20201005-0000011-01",            "coupon_name": "coupon setting name",            "coupon_code": "6069019282400000002",            "coupon_percent": "1%",            "coupon_value": "900.00",            "coupon_value_final": "0.00"        },        {            "shop_no": 1,            "order_id": "20201005-0000011",            "order_item_code": "20201005-0000011-01",            "coupon_name": "coupon setting name",            "coupon_code": "6069019278500000001",            "coupon_percent": null,            "coupon_value": "500.00",            "coupon_value_final": "0.00"        }    ]}
```

```bash
curl -X GET \  'https://{mallid}.cafe24api.com/api/v2/admin/orders/coupons?order_id=20201005-0000011' \  -H 'Authorization: Bearer {access_token}' \  -H 'Content-Type: application/json' \  -H 'X-Cafe24-Api-Version: {version}'
```

```json
{    "coupons": [        {            "shop_no": 1,            "order_id": "20201005-0000011",            "order_item_code": "20201005-0000011-01",            "coupon_name": "coupon setting name",            "coupon_code": "6069019282400000002",            "coupon_percent": "1%",            "coupon_value": "900.00",            "coupon_value_final": "0.00"        },        {            "shop_no": 1,            "order_id": "20201005-0000011",            "order_item_code": "20201005-0000011-01",            "coupon_name": "coupon setting name",            "coupon_code": "6069019278500000001",            "coupon_percent": null,            "coupon_value": "500.00",            "coupon_value_final": "0.00"        }    ]}
```
