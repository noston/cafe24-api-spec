# CUSTOMERS COUPONS


## Customers coupons

```json
Endpoints    GET /api/v2/admin/customers/{member_id}/coupons
GET /api/v2/admin/customers/{member_id}/coupons/count
DELETE /api/v2/admin/customers/{member_id}/coupons/{coupon_no}
```

```json
GET /api/v2/admin/customers/{member_id}/coupons
GET /api/v2/admin/customers/{member_id}/coupons/count
DELETE /api/v2/admin/customers/{member_id}/coupons/{coupon_no}
```

### Customers coupons property list

| Attribute | Description |
| --- | --- |
| shop_no | 멀티쇼핑몰 번호 |
| coupon_no | 쿠폰번호 |
| issue_no | 쿠폰 발급번호 |
| coupon_name | 쿠폰명 |
| available_price_type | 사용가능 구매 금액 유형 U : 제한 없음 O : 주문 금액 기준 P : 상품 금액 기준 |
| available_price_type_detail | 사용가능 구매 금액 유형 상세 U : 모든 상품의 주문 금액 I : 쿠폰 적용 상품의 주문 금액 |
| available_min_price | 사용가능 구매 금액 |
| available_payment_methods | 사용가능 결제수단 all : 제한없음 R : 무통장입금 E : 가상계좌 C : 신용카드 A : 계좌이체 H : 휴대폰 M : 적립금 K : 케이페이 P : 페이나우 N : 페이코 O : 카카오페이 S : 스마일페이 V : 네이버페이 B : 편의점 D : 토스 |
| benefit_type | 혜택 구분 A : 할인금액 B : 할인율 C : 적립금액 D : 적립율 E : 기본배송비 할인(전액할인) I : 기본배송비 할인(할인율) H : 기본배송비 할인(할인금액) F : 즉시적립 G : 예치금 |
| benefit_price | 혜택 금액 |
| benefit_percentage | 혜택 비율 |
| benefit_percentage_round_unit | 혜택 비율 절사 단위 |
| benefit_percentage_max_price | 혜택 비율 최대 금액 |
| credit_amount | 예치금 지급 금액 |
| issued_date | 발행일 |
| available_begin_datetime | 사용 기간 시작 일시 |
| available_end_datetime | 사용 기간 종료 일시 |

### Retrieve a list of customer coupons   cafe24

#### 기본스펙

| Property | Description |
| --- | --- |
| SCOPE | 프로모션 읽기권한 (mall.read_promotion) |
| 호출건수 제한 | 40 |

#### 요청사양

| Parameter | Description |
| --- | --- |
| shop_no | 멀티쇼핑몰 번호   DEFAULT 1 |
| member_idRequired | 회원아이디 |
| offset최대값: [10000] | 조회결과 시작위치   DEFAULT 0 |
| limit최소: [1]~최대: [100] | 조회결과 최대건수   DEFAULT 10 |

```bash
Retrieve a list of customer coupons        Retrieve a list of customer coupons Retrieve coupons with fields parameter Retrieve coupons using paging       Request   cURL Java Python Node.js PHP Go  Copy         Response  Copy
```

### Retrieve a count of customer coupons   cafe24

#### 기본스펙

| Property | Description |
| --- | --- |
| SCOPE | 프로모션 읽기권한 (mall.read_promotion) |
| 호출건수 제한 | 40 |

#### 요청사양

| Parameter | Description |
| --- | --- |
| shop_no | 멀티쇼핑몰 번호   DEFAULT 1 |
| member_idRequired | 회원아이디 |

```bash
Retrieve a count of customer coupons        Retrieve a count of customer coupons       Request   cURL Java Python Node.js PHP Go  Copy         Response  Copy
```

### Delete a customer coupon   cafe24

#### 기본스펙

| Property | Description |
| --- | --- |
| SCOPE | 프로모션 쓰기권한 (mall.write_promotion) |
| 호출건수 제한 | 40 |

#### 요청사양

| Parameter | Description |
| --- | --- |
| shop_no | 멀티쇼핑몰 번호   DEFAULT 1 |
| member_idRequired | 회원아이디 |
| coupon_noRequired | 쿠폰번호 |
| issue_no | 쿠폰 발급번호 |

```bash
Delete a customer coupon        Delete a customer coupon       Request   cURL Java Python Node.js PHP Go  Copy         Response  Copy
```
