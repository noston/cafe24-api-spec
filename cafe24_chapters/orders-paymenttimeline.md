# ORDERS PAYMENTTIMELINE


## Orders paymenttimeline

```json
Endpoints    GET /api/v2/admin/orders/{order_id}/paymenttimeline
GET /api/v2/admin/orders/{order_id}/paymenttimeline/{payment_no}
```

```json
GET /api/v2/admin/orders/{order_id}/paymenttimeline
GET /api/v2/admin/orders/{order_id}/paymenttimeline/{payment_no}
```

### Orders paymenttimeline property list

| Attribute | Description |
| --- | --- |
| shop_no | 멀티쇼핑몰 번호 |
| payment_no | 결제번호 |
| payment_settle_type | 결제유형 O : 최초결제  R : 추가결제  P : 환불 |
| order_amount | 주문금액 |
| additional_payment_amount | 보조 결제금액 |
| paid_amount | 결제금액 |
| payment_methods | 결제수단 |
| payment_datetime | 결제일 |
| created_datetime | 입력일 |
| claim_code | 취소/교환/반품 번호 |
| payment_method_detail | 결제수단별 결제금액 payment_method_detail code |
| order_amount_detail | 주문금액 상세 order_amount_detail code |

### Retrieve payment history of an order   cafe24 youtube

#### 기본스펙

| Property | Description |
| --- | --- |
| SCOPE | 주문 읽기권한 (mall.read_order) |
| 호출건수 제한 | 40 |

#### 요청사양

| Parameter | Description |
| --- | --- |
| shop_no최소값: [1] | 멀티쇼핑몰 번호   DEFAULT 1 |
| order_idRequired | 주문번호 |
| start_date날짜 | 검색 시작일 |
| end_date날짜 | 검색 종료일 |
| date_type | 검색날짜 유형   시작일과 종료일 기준으로 기간 검색시 date_type 미입력시 created_datetime 기준으로 검색 진행   created_datetime : 입력일 payment_datetime : 결제일 |

```bash
Retrieve payment history of an order        Retrieve payment history of an order Retrieve paymentstimeline with fields parameter Retrieve a specific paymentstimeline with date_type parameter       Request   cURL Java Python Node.js PHP Go  Copy         Response  Copy
```

### Retrieve payment details of an order   cafe24 youtube

#### 기본스펙

| Property | Description |
| --- | --- |
| SCOPE | 주문 읽기권한 (mall.read_order) |
| 호출건수 제한 | 40 |

#### 요청사양

| Parameter | Description |
| --- | --- |
| shop_no최소값: [1] | 멀티쇼핑몰 번호   DEFAULT 1 |
| order_idRequired | 주문번호 |
| payment_noRequired최소값: [1] | 결제번호 |

```bash
Retrieve payment details of an order        Retrieve payment details of an order       Request   cURL Java Python Node.js PHP Go  Copy         Response  Copy
```
