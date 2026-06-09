# COUPONS ISSUANCECUSTOMERS


## Coupons issuancecustomers

```json
Endpoints    GET /api/v2/admin/coupons/{coupon_no}/issuancecustomers
```

```json
GET /api/v2/admin/coupons/{coupon_no}/issuancecustomers
```

### Coupons issuancecustomers property list

| Attribute | Description |
| --- | --- |
| shop_no | 멀티쇼핑몰 번호 DEFAULT 1 |
| coupon_no | 쿠폰번호 |
| member_id | 회원아이디 |
| group_no | 발급대상 회원등급 번호 |
| issued_date | 쿠폰 발급일자 |
| expiration_date | 만료일 |
| used_coupon | 쿠폰사용 여부 |
| used_date | 쿠폰 사용 일자 |
| related_order_id | 관련 주문번호 |

### Retrieve a list of eligible customers for conditional issuance   cafe24

#### 기본스펙

| Property | Description |
| --- | --- |
| SCOPE | 프로모션 읽기권한 (mall.read_promotion) |
| 호출건수 제한 | 40 |

#### 요청사양

| Parameter | Description |
| --- | --- |
| shop_no최소값: [1] | 멀티쇼핑몰 번호   DEFAULT 1 |
| coupon_noRequired | 쿠폰번호 |
| member_id최대글자수 : [20자] | 회원아이디 |
| group_no | 회원등급번호 |
| since_member_id최대글자수 : [20자] | 해당 쿠폰 회원 ID 이후 검색 |
| limit최소: [1]~최대: [500] | 조회결과 최대건수   DEFAULT 10 |
| offset최대값: [8000] | 조회결과 시작위치   DEFAULT 0 |

```bash
Retrieve a list of eligible customers for conditional issuance        Retrieve a list of eligible customers for conditional issuance       Request   cURL Java Python Node.js PHP Go  Copy         Response  Copy
```
