# PAYMENTMETHODS PAYMENTPROVIDERS


## Paymentmethods paymentproviders

```json
Endpoints    GET /api/v2/admin/paymentmethods/{code}/paymentproviders
PUT /api/v2/admin/paymentmethods/{code}/paymentproviders/{name}
```

```json
GET /api/v2/admin/paymentmethods/{code}/paymentproviders
PUT /api/v2/admin/paymentmethods/{code}/paymentproviders/{name}
```

### Paymentmethods paymentproviders property list

| Attribute | Description |
| --- | --- |
| shop_no | 멀티쇼핑몰 번호 |
| name | PG 이름 |
| display | 결제수단 노출여부 T : 노출함 F : 노출안함 |

### Retrieve a list of providers by payment method   cafe24

#### 기본스펙

| Property | Description |
| --- | --- |
| SCOPE | 상점 읽기권한 (mall.read_store) |
| 호출건수 제한 | 40 |

#### 요청사양

| Parameter | Description |
| --- | --- |
| shop_no최소값: [1] | 멀티쇼핑몰 번호   DEFAULT 1 |
| codeRequired | 결제수단 코드 |
| name | PG 이름 |
| display | 결제수단 노출여부   T : 노출함 F : 노출안함 |

```bash
Retrieve a list of providers by payment method        Retrieve a list of providers by payment method       Request   cURL Java Python Node.js PHP Go  Copy         Response  Copy
```

### Update the display status of a payment method   cafe24

#### 기본스펙

| Property | Description |
| --- | --- |
| SCOPE | 상점 쓰기권한 (mall.write_store) |
| 호출건수 제한 | 40 |
| 1회당 요청건수 제한 | 1 |

#### 요청사양

| Parameter | Description |
| --- | --- |
| shop_no최소값: [1] | 멀티쇼핑몰 번호   DEFAULT 1 |
| codeRequired | 결제수단 코드 |
| nameRequired | PG 이름 |
| displayRequired | 결제수단 노출여부   T : 노출함 F : 노출안함 |

```bash
Update the display status of a payment method        Update the display status of a payment method       Request   cURL Java Python Node.js PHP Go  Copy         Response  Copy
```
