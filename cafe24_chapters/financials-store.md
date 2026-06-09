# FINANCIALS STORE


## Financials store

```json
Endpoints    GET /api/v2/admin/financials/store
```

```json
GET /api/v2/admin/financials/store
```

### Financials store property list

| Attribute | Description |
| --- | --- |
| shop_no | 멀티쇼핑몰 번호 |
| first_payment_date | 최초 결제일 |
| payment_gateway_name | PG 이름 |

### Retrieve the transaction information of a store   cafe24

#### 기본스펙

| Property | Description |
| --- | --- |
| SCOPE | 상점 읽기권한 (mall.read_store) |
| 호출건수 제한 | 1 |

#### 요청사양

| Parameter | Description |
| --- | --- |
| shop_no최소값: [1] | 멀티쇼핑몰 번호   DEFAULT 1 |
| payment_methodRequired | 결제수단 코드   card : 신용카드 tcash : 계좌이체 icash : 가상계좌 cell : 휴대폰 deferpay : 후불 cvs : 편의점 point : 선불금 etc : 기타 |

```bash
Retrieve the transaction information of a store        Retrieve the transaction information of a store       Request   cURL Java Python Node.js PHP Go  Copy     curl -X GET \  'https://{mallid}.cafe24api.com/api/v2/admin/financials/store?payment_method=card' \  -H 'Authorization: Bearer {access_token}' \  -H 'Content-Type: application/json' \  -H 'X-Cafe24-Api-Version: {version}'    Response  Copy     {    "store": {        "shop_no": 1,        "first_payment_date": "2020-01-01",        "payment_gateway_name": "cafe24payTest"    }}
```

```bash
curl -X GET \  'https://{mallid}.cafe24api.com/api/v2/admin/financials/store?payment_method=card' \  -H 'Authorization: Bearer {access_token}' \  -H 'Content-Type: application/json' \  -H 'X-Cafe24-Api-Version: {version}'
```

```json
{    "store": {        "shop_no": 1,        "first_payment_date": "2020-01-01",        "payment_gateway_name": "cafe24payTest"    }}
```
