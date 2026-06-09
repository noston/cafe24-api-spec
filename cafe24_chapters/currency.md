# CURRENCY


## Currency

```json
Endpoints    GET /api/v2/admin/currency
PUT /api/v2/admin/currency
```

```json
GET /api/v2/admin/currency
PUT /api/v2/admin/currency
```

### Currency property list

| Attribute | Description |
| --- | --- |
| exchange_rate | 결제 화폐 환율 정보 |
| standard_currency_code | 기준 화폐 코드 해당 쇼핑몰의 기본쇼핑몰에서 사용하는 화폐 코드. 기준 화폐란 일반적으로 쇼핑몰 운영자가 속한 국가에서 통용되는 화폐를 의미한다. |
| standard_currency_symbol | 기준 화폐 심볼 해당 쇼핑몰의 기본쇼핑몰에서 사용하는 화폐의 화폐 기호. 기준 화폐란 일반적으로 쇼핑몰 운영자가 속한 국가에서 통용되는 화폐를 의미한다. |
| shop_currency_code | 결제 화폐 코드 |
| shop_currency_symbol | 결제 화폐 심볼 |
| shop_currency_format | 결제 화폐 표시 방식 |

### Retrieve currency settings   cafe24

#### 기본스펙

| Property | Description |
| --- | --- |
| SCOPE | 상점 읽기권한 (mall.read_store) |
| 호출건수 제한 | 40 |

```bash
Retrieve currency settings        Retrieve currency settings       Request   cURL Java Python Node.js PHP Go  Copy     curl -X GET \  'https://{mallid}.cafe24api.com/api/v2/admin/currency' \  -H 'Authorization: Bearer {access_token}' \  -H 'Content-Type: application/json' \  -H 'X-Cafe24-Api-Version: {version}'    Response  Copy     {    "currency": {        "exchange_rate": "1004.00",        "standard_currency_code": "KRW",        "standard_currency_symbol": "￦",        "shop_currency_code": "USD",        "shop_currency_symbol": "$",        "shop_currency_format": "￦[:PRICE:]"    }}
```

```bash
curl -X GET \  'https://{mallid}.cafe24api.com/api/v2/admin/currency' \  -H 'Authorization: Bearer {access_token}' \  -H 'Content-Type: application/json' \  -H 'X-Cafe24-Api-Version: {version}'
```

```json
{    "currency": {        "exchange_rate": "1004.00",        "standard_currency_code": "KRW",        "standard_currency_symbol": "￦",        "shop_currency_code": "USD",        "shop_currency_symbol": "$",        "shop_currency_format": "￦[:PRICE:]"    }}
```

### Update a currency   cafe24

#### 기본스펙

| Property | Description |
| --- | --- |
| SCOPE | 상점 쓰기권한 (mall.write_store) |
| 호출건수 제한 | 40 |
| 1회당 요청건수 제한 | 1 |

#### 요청사양

| Parameter | Description |
| --- | --- |
| shop_noRequired최소값: [1] | 멀티쇼핑몰 번호   DEFAULT 1 |
| exchange_rateRequired | 결제 화폐 환율 정보 |

```bash
Update a currency        Update a currency       Request   cURL Java Python Node.js PHP Go  Copy     curl -X PUT \  'https://{mallid}.cafe24api.com/api/v2/admin/currency' \  -H 'Authorization: Bearer {access_token}' \  -H 'Content-Type: application/json' \  -H 'X-Cafe24-Api-Version: {version}' \  -d '{    "shop_no": 2,    "request": {        "exchange_rate": "9.5697"    }}'    Response  Copy     {    "currency": {        "exchange_rate": "9.5697"    }}
```

```bash
curl -X PUT \  'https://{mallid}.cafe24api.com/api/v2/admin/currency' \  -H 'Authorization: Bearer {access_token}' \  -H 'Content-Type: application/json' \  -H 'X-Cafe24-Api-Version: {version}' \  -d '{    "shop_no": 2,    "request": {        "exchange_rate": "9.5697"    }}'
```

```json
{    "currency": {        "exchange_rate": "9.5697"    }}
```
