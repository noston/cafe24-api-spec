# ORDERS SHIPPINGFEECANCELLATION


## Orders shippingfeecancellation

```json
Endpoints    GET /api/v2/admin/orders/{order_id}/shippingfeecancellation
POST /api/v2/admin/orders/{order_id}/shippingfeecancellation
```

```json
GET /api/v2/admin/orders/{order_id}/shippingfeecancellation
POST /api/v2/admin/orders/{order_id}/shippingfeecancellation
```

### Orders shippingfeecancellation property list

| Attribute | Description |
| --- | --- |
| shop_no | 멀티쇼핑몰 번호 |
| order_id | 주문번호 |
| default_shipping_fee | 기본 배송비 |
| supplier_shipping_fee | 공급사배송비 |
| individual_shipping_fee | 개별배송비 |
| international_shipping_fee | 해외배송비 |
| international_shipping_insurance_fee | 해외배송 보험료 |
| additional_shipping_fee | 추가 배송비 |
| additional_handling_fee | 해외배송 부가금액 |
| regional_surcharge_amount | 지역별 배송비 |
| claim_code | 취소 번호 |
| claim_reason_type | 구분 A:고객변심B:배송지연J:배송오류C:배송불가지역L:수출/통관 불가D:포장불량E:상품 불만족F:상품정보상이K:상품불량G:서비스불만족H:품절I:기타 |
| claim_reason | 사유 |
| refund_method | 환불 방식 |
| shipping_discount_amount | 배송비할인 취소액 |
| coupon_discount_amount | 쿠폰할인 취소액 |
| refund_amount | 환불금액 |
| point_used | 사용된 적립금 반환액 |
| credit_used | 사용된 예치금 반환액 |
| mixed_refund_amount | 복합 환불 금액 |
| mixed_refund_methods | 복합 환불 방식 |
| status | 주문상태 canceled: 취소완료canceling : 취소처리중 |
| include_tax | 가격에 세금 포함 T: 세금포함 F: 세금제외 |
| tax | 세금 정보 세금 관리자 앱을 사용 안 할 경우 null로 반환 |

### Retrieve shipping fee cancellation details of an order   cafe24 youtube

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

```bash
Retrieve shipping fee cancellation details of an order        Retrieve shipping fee cancellation details of an order       Request   cURL Java Python Node.js PHP Go  Copy         Response  Copy
```

### Create an order shipping fee cancellation   cafe24 youtube

#### 기본스펙

| Property | Description |
| --- | --- |
| SCOPE | 주문 쓰기권한 (mall.write_order) |
| 호출건수 제한 | 40 |
| 1회당 요청건수 제한 | 1 |

#### 요청사양

| Parameter | Description |
| --- | --- |
| shop_no최소값: [1] | 멀티쇼핑몰 번호   DEFAULT 1 |
| order_idRequired | 주문번호 |
| reason최대글자수 : [2000자] | 취소사유 |
| claim_reason_type | 취소사유 구분   A:고객변심B:배송지연J:배송오류C:배송불가지역L:수출/통관 불가D:포장불량E:상품 불만족F:상품정보상이K:상품불량G:서비스불만족H:품절I:기타 |
| recover_coupon | 쿠폰 복원   Youtube shopping 이용 시에는 미제공   T : 복구함 F : 복구안함   DEFAULT F |
| refund_method_code | 환불 방식   T : 현금 F : 신용카드 M : 적립금 G : 계좌이체 C : 휴대폰 D : 예치금 Z : 후불 O : 선불금 V : 편의점 J : 제휴상품권 K : 제휴포인트 I : 기타 |
| refund_bank_code | 환불 은행 코드 |
| refund_bank_name최대글자수 : [250자] | 환불은행명 |
| refund_bank_account_no | 환불 계좌번호 |
| refund_bank_account_holder최대글자수 : [30자] | 환불계좌 예금주 명의 |
| payment_gateway_cancel | PG 취소 요청 여부   T : 취소함 F : 취소안함   DEFAULT F |

```bash
Create an order shipping fee cancellation        Create an order shipping fee cancellation Cancel the shipping fee by using only required fields Try cancel the shipping fee when shipping fee is already free       Request   cURL Java Python Node.js PHP Go  Copy         Response  Copy
```
