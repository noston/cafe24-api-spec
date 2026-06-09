# PAYMENTGATEWAY PAYMENTMETHODS


## Paymentgateway paymentmethods

```json
Endpoints    GET /api/v2/admin/paymentgateway/{client_id}/paymentmethods
POST /api/v2/admin/paymentgateway/{client_id}/paymentmethods
PUT /api/v2/admin/paymentgateway/{client_id}/paymentmethods/{payment_method_code}
DELETE /api/v2/admin/paymentgateway/{client_id}/paymentmethods/{payment_method_code}
```

```json
GET /api/v2/admin/paymentgateway/{client_id}/paymentmethods
POST /api/v2/admin/paymentgateway/{client_id}/paymentmethods
PUT /api/v2/admin/paymentgateway/{client_id}/paymentmethods/{payment_method_code}
DELETE /api/v2/admin/paymentgateway/{client_id}/paymentmethods/{payment_method_code}
```

### Paymentgateway paymentmethods property list

| Attribute | Description |
| --- | --- |
| client_id | 앱 클라이언트 ID |
| payment_method_code | 결제수단 코드 |
| payment_method | 결제수단 card : 신용카드 tcash : 계좌이체 icash : 가상계좌 cell : 휴대폰 cvs : 편의점 deferpay : 후불결제 etc : 기타 |
| payment_method_name | 결제수단명 |
| payment_method_url | 결제수단 이미지 경로 |
| available_shop_no | 이용가능한 멀티쇼핑몰 번호 |

### Retrieve a list of Payment Gateway methods   cafe24

#### 기본스펙

| Property | Description |
| --- | --- |
| SCOPE | 상점 읽기권한 (mall.read_store) |
| 호출건수 제한 | 40 |

#### 요청사양

| Parameter | Description |
| --- | --- |
| client_idRequired최대글자수 : [50자] | 앱 클라이언트 ID |

```bash
Retrieve a list of Payment Gateway methods        Retrieve a list of Payment Gateway methods Retrieve paymentmethods with fields parameter       Request   cURL Java Python Node.js PHP Go  Copy         Response  Copy
```

### Create a Payment Gateway method   cafe24

#### 기본스펙

| Property | Description |
| --- | --- |
| SCOPE | 상점 쓰기권한 (mall.write_store) |
| 호출건수 제한 | 40 |
| 1회당 요청건수 제한 | 1 |

#### 요청사양

| Parameter | Description |
| --- | --- |
| client_idRequired최대글자수 : [50자] | 앱 클라이언트 ID |
| payment_method_codeRequired최대글자수 : [50자] | 결제수단 코드 |
| payment_methodRequired | 결제수단   card : 신용카드 tcash : 계좌이체 icash : 가상계좌 cell : 휴대폰 cvs : 편의점 deferpay : 후불결제 etc : 기타 |
| payment_method_nameRequired최대글자수 : [50자] | 결제수단명 |
| payment_method_urlRequired최대글자수 : [200자] | 결제수단 이미지 경로   지원 확장자 : 'png', 'jpg', 'jpeg' |
| available_shop_no | 이용가능한 멀티쇼핑몰 번호 |

```bash
Create a Payment Gateway method        Create a Payment Gateway method       Request   cURL Java Python Node.js PHP Go  Copy         Response  Copy
```

### Update a payment method of a Payment Gateway   cafe24

#### 기본스펙

| Property | Description |
| --- | --- |
| SCOPE | 상점 쓰기권한 (mall.write_store) |
| 호출건수 제한 | 40 |
| 1회당 요청건수 제한 | 1 |

#### 요청사양

| Parameter | Description |
| --- | --- |
| client_idRequired최대글자수 : [50자] | 앱 클라이언트 ID |
| payment_method_codeRequired최대글자수 : [50자] | 결제수단 코드 |
| payment_method | 결제수단   card : 신용카드 tcash : 계좌이체 icash : 가상계좌 cell : 휴대폰 cvs : 편의점 deferpay : 후불결제 etc : 기타 |
| payment_method_name최대글자수 : [50자] | 결제수단명 |
| payment_method_url최대글자수 : [200자] | 결제수단 이미지 경로   지원 확장자 : 'png', 'jpg', 'jpeg' |
| available_shop_no | 이용가능한 멀티쇼핑몰 번호 |

```bash
Update a payment method of a Payment Gateway        Update a payment method of a Payment Gateway       Request   cURL Java Python Node.js PHP Go  Copy         Response  Copy
```

### Delete a payment method of a Payment Gateway   cafe24

#### 기본스펙

| Property | Description |
| --- | --- |
| SCOPE | 상점 쓰기권한 (mall.write_store) |
| 호출건수 제한 | 40 |

#### 요청사양

| Parameter | Description |
| --- | --- |
| client_idRequired최대글자수 : [50자] | 앱 클라이언트 ID |
| payment_method_codeRequired최대글자수 : [50자] | 결제수단 코드 |

```bash
Delete a payment method of a Payment Gateway        Delete a payment method of a Payment Gateway       Request   cURL Java Python Node.js PHP Go  Copy         Response  Copy
```
