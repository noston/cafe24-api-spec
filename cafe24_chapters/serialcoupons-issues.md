# SERIALCOUPONS ISSUES


## Serialcoupons issues

```json
Endpoints    GET /api/v2/admin/serialcoupons/{coupon_no}/issues
POST /api/v2/admin/serialcoupons/{coupon_no}/issues
```

```json
GET /api/v2/admin/serialcoupons/{coupon_no}/issues
POST /api/v2/admin/serialcoupons/{coupon_no}/issues
```

### Serialcoupons issues property list

| Attribute | Description |
| --- | --- |
| shop_no | 멀티쇼핑몰 번호 DEFAULT 1 |
| coupon_no | 쿠폰번호 |
| serial_code | 시리얼코드 |
| member_id | 회원아이디 |
| verify | 인증여부 Y:인증 N:미인증 |
| verify_datetime | 인증일시 |
| used_datetime | 사용일시 |
| deleted | 쿠폰삭제 여부 T : 삭제 F : 삭제되지 않음 |

### Retrieve a code of coupon codes   cafe24

#### 기본스펙

| Property | Description |
| --- | --- |
| SCOPE | 프로모션 읽기권한 (mall.read_promotion) |
| 호출건수 제한 | 40 |

#### 요청사양

| Parameter | Description |
| --- | --- |
| shop_no | 멀티쇼핑몰 번호   DEFAULT 1 |
| coupon_no | 쿠폰번호 |
| offset최대값: [10000] | 조회결과 시작위치   DEFAULT 0 |
| limit최소: [1]~최대: [500] | 조회결과 최대건수   DEFAULT 100 |

```bash
Retrieve a code of coupon codes        Retrieve a code of coupon codes       Request   cURL Java Python Node.js PHP Go  Copy         Response  Copy
```

### Register a code of coupon codes   cafe24

#### 기본스펙

| Property | Description |
| --- | --- |
| SCOPE | 프로모션 쓰기권한 (mall.write_promotion) |
| 호출건수 제한 | 40 |
| 1회당 요청건수 제한 | 1 |

#### 요청사양

| Parameter | Description |
| --- | --- |
| shop_no | 멀티쇼핑몰 번호   DEFAULT 1 |
| coupon_no | 쿠폰번호 |
| serial_code_listRequired배열 최대사이즈: [10000] | 시리얼넘버 목록 |

```bash
Register a code of coupon codes        Register a code of coupon codes       Request   cURL Java Python Node.js PHP Go  Copy         Response  Copy
```
