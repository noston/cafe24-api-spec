# ORDERS PAYMENTS


## Orders payments

```json
Endpoints    PUT /api/v2/admin/orders/{order_id}/payments
```

```json
PUT /api/v2/admin/orders/{order_id}/payments
```

### Orders payments property list

| Attribute | Description |
| --- | --- |
| shop_no | 멀티쇼핑몰 번호 |
| order_id | 주문번호 |
| change_payment_amount | 결제금액 변경 여부 T : 사용함 F : 사용안함 |
| change_payment_method | 결제수단 변경 여부 T : 사용함 F : 사용안함 |
| payment_method | 결제수단 |
| payment_gateway_failure_message | PG 결제 취소 실패 메시지 |
| admin_additional_amount | 관리자 입력 금액 |
| commission | 결제 수수료 |
| initial_estimated_payment_amount | 최초 결제 예정 금액 |
| change_payment_amount_reason | 결제금액 변경 사유 |

### Update an order payment status   cafe24

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
| change_payment_amountRequired | 결제금액 변경 여부   입금전 상태에서만 결제금액 변경 가능  단, CS주문상태 또는 CS처리이력이 존재하는 경우에는 결제금액 변경 불가능함  ※ 결제수단별 입금전 주문상태 - 무통장입금 : 입금전 - 다이비키 : 상품준비중 ~ 배송완료 [다이비키 입금전]   T : 사용함 F : 사용안함 |
| change_payment_methodRequired | 결제수단 변경 여부   T : 사용함 F : 사용안함 |
| payment_method | 결제수단   cash: 무통장 입금 daibiki : 다이비키 |
| billing_name최대글자수 : [40자] | 입금자명   결제수단을 무통장입금으로 변경할 경우("change_payment_method:"T"이고 "payment_method":"cash"일 경우) 사용 가능 |
| bank_account_id | 무통장 입금 은행 ID   결제수단을 무통장입금으로 변경할 경우("change_payment_method:"T"이고 "payment_method":"cash"일 경우) 사용 가능 |
| admin_additional_amount최소값: [0]최대값: [10000000] | 관리자 입력 금액   결제금액을 변경할 경우("change_payment_amount":"T"일 경우) 사용 가능 |
| commission최소값: [0]최대값: [10000000] | 결제 수수료   결제수단을 다이비키로 변경할 경우("change_payment_amount:"T"이고 "payment_method":"daibiki"일 경우) 사용 가능 |
| change_payment_amount_reason최대글자수 : [255자] | 결제금액 변경 사유   결제금액을 변경할 경우("change_payment_amount":"T"일 경우) 사용 가능 |

```bash
Update an order payment status        Update an order payment status       Request   cURL Java Python Node.js PHP Go  Copy         Response  Copy
```
