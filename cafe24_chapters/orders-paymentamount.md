# ORDERS PAYMENTAMOUNT


## Orders paymentamount

```json
Endpoints    GET /api/v2/admin/orders/paymentamount
```

```json
GET /api/v2/admin/orders/paymentamount
```

### Orders paymentamount property list

| Attribute | Description |
| --- | --- |
| shop_no | 멀티쇼핑몰 번호 |
| order_item_code | 품주코드 |
| items | 품목 정보 |
| order_price_amount | 상품구매금액 |
| order_discount_amount | 주문 할인금액 |
| item_discount_amount | 상품 할인금액 |
| additional_payment_amount | 보조 결제금액 |
| payment_amount | 품목별 결제금액 |
| cancel_fee_amount | 취소수수료 |

### Retrieve a payment amount   cafe24 youtube

#### 기본스펙

| Property | Description |
| --- | --- |
| SCOPE | 주문 읽기권한 (mall.read_order) |
| 호출건수 제한 | 40 |

#### 요청사양

| Parameter | Description |
| --- | --- |
| shop_no최소값: [1] | 멀티쇼핑몰 번호   DEFAULT 1 |
| order_item_codeRequired | 품주코드   ,(콤마)로 여러 건을 검색할 수 있다. |

```bash
Retrieve a payment amount        Retrieve a payment amount       Request   cURL Java Python Node.js PHP Go  Copy     curl -X GET \  'https://{mallid}.cafe24api.com/api/v2/admin/orders/paymentamount?order_item_code=20210511-0000011-01,20210511-0000022-01' \  -H 'Authorization: Bearer {access_token}' \  -H 'Content-Type: application/json' \  -H 'X-Cafe24-Api-Version: {version}'    Response  Copy     {    "paymentamount": [        {            "shop_no": 1,            "order_item_code": "20210511-0000011-01",            "items": {                "product_price": "9000.00",                "option_price": "1000.00",                "quantity": 1            },            "order_price_amount": "10000.00",            "order_discount_amount": {                "membership_discount_amount": "0.00",                "coupon_discount_price": "0.00",                "app_discount_amount": "0.00"            },            "item_discount_amount": {                "additional_discount_price": "300.00",                "coupon_discount_price": "0.00",                "app_discount_amount": "0.00"            },            "additional_payment_amount": "200.00",            "payment_amount": "9500.00",            "cancel_fee_amount": null        },        {            "shop_no": 1,            "order_item_code": "20210511-0000022-01",            "items": {                "product_price": "5000.00",                "option_price": "0.00",                "quantity": 1            },            "order_price_amount": "5000.00",            "order_discount_amount": {                "membership_discount_amount": "0.00",                "coupon_discount_price": "0.00",                "app_discount_amount": "0.00"            },            "item_discount_amount": {                "additional_discount_price": "200.00",                "coupon_discount_price": "0.00",                "app_discount_amount": "0.00"            },            "additional_payment_amount": "100.00",            "payment_amount": "4700.00",            "cancel_fee_amount": null        }    ]}
```

```bash
curl -X GET \  'https://{mallid}.cafe24api.com/api/v2/admin/orders/paymentamount?order_item_code=20210511-0000011-01,20210511-0000022-01' \  -H 'Authorization: Bearer {access_token}' \  -H 'Content-Type: application/json' \  -H 'X-Cafe24-Api-Version: {version}'
```

```json
{    "paymentamount": [        {            "shop_no": 1,            "order_item_code": "20210511-0000011-01",            "items": {                "product_price": "9000.00",                "option_price": "1000.00",                "quantity": 1            },            "order_price_amount": "10000.00",            "order_discount_amount": {                "membership_discount_amount": "0.00",                "coupon_discount_price": "0.00",                "app_discount_amount": "0.00"            },            "item_discount_amount": {                "additional_discount_price": "300.00",                "coupon_discount_price": "0.00",                "app_discount_amount": "0.00"            },            "additional_payment_amount": "200.00",            "payment_amount": "9500.00",            "cancel_fee_amount": null        },        {            "shop_no": 1,            "order_item_code": "20210511-0000022-01",            "items": {                "product_price": "5000.00",                "option_price": "0.00",                "quantity": 1            },            "order_price_amount": "5000.00",            "order_discount_amount": {                "membership_discount_amount": "0.00",                "coupon_discount_price": "0.00",                "app_discount_amount": "0.00"            },            "item_discount_amount": {                "additional_discount_price": "200.00",                "coupon_discount_price": "0.00",                "app_discount_amount": "0.00"            },            "additional_payment_amount": "100.00",            "payment_amount": "4700.00",            "cancel_fee_amount": null        }    ]}
```
