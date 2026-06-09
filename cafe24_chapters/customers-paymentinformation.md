# CUSTOMERS PAYMENTINFORMATION


## Customers paymentinformation

```json
Endpoints    GET /api/v2/admin/customers/{member_id}/paymentinformation
DELETE /api/v2/admin/customers/{member_id}/paymentinformation
DELETE /api/v2/admin/customers/{member_id}/paymentinformation/{payment_method_id}
```

```json
GET /api/v2/admin/customers/{member_id}/paymentinformation
DELETE /api/v2/admin/customers/{member_id}/paymentinformation
DELETE /api/v2/admin/customers/{member_id}/paymentinformation/{payment_method_id}
```

### Customers paymentinformation property list

| Attribute | Description |
| --- | --- |
| shop_no | 멀티쇼핑몰 번호 |
| member_id최대글자수 : [20자] | 회원아이디 |
| payment_method | 결제수단명 |
| payment_gateway | PG 이름 |
| created_date | 생성일 |
| payment_proiority | 결제 우선순위 |
| payment_method_id | 정기배송 결제수단 번호 |

### Retrieve a customer's list of payment methods   cafe24

#### 기본스펙

| Property | Description |
| --- | --- |
| SCOPE | 회원 읽기권한 (mall.read_customer) |
| 호출건수 제한 | 40 |

#### 요청사양

| Parameter | Description |
| --- | --- |
| shop_no최소값: [1] | 멀티쇼핑몰 번호   DEFAULT 1 |
| member_idRequired최대글자수 : [20자] | 회원아이디 |

```bash
Retrieve a customer's list of payment methods        Retrieve a customer's list of payment methods Retrieve paymentinformation with fields parameter       Request   cURL Java Python Node.js PHP Go  Copy         Response  Copy
```

### Delete customer's payment information   cafe24

#### 기본스펙

| Property | Description |
| --- | --- |
| SCOPE | 회원 쓰기권한 (mall.write_customer) |
| 호출건수 제한 | 40 |

#### 요청사양

| Parameter | Description |
| --- | --- |
| shop_no최소값: [1] | 멀티쇼핑몰 번호   DEFAULT 1 |
| member_idRequired최대글자수 : [20자] | 회원아이디 |

```bash
Delete customer's payment information        Delete customer's payment information       Request   cURL Java Python Node.js PHP Go  Copy         Response  Copy
```

### Delete customer's payment information by payment method ID   cafe24

#### 기본스펙

| Property | Description |
| --- | --- |
| SCOPE | 회원 쓰기권한 (mall.write_customer) |
| 호출건수 제한 | 40 |

#### 요청사양

| Parameter | Description |
| --- | --- |
| shop_no최소값: [1] | 멀티쇼핑몰 번호   DEFAULT 1 |
| member_idRequired최대글자수 : [20자] | 회원아이디 |
| payment_method_idRequired주문번호 | 정기배송 결제수단 번호 |

```bash
Delete customer's payment information by payment method ID        Delete customer's payment information by payment method ID       Request   cURL Java Python Node.js PHP Go  Copy         Response  Copy
```
