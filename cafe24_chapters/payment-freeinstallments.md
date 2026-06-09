# PAYMENT FREEINSTALLMENTS


## Payment freeinstallments

```json
Endpoints    GET /api/v2/admin/payment/freeinstallments
```

```json
GET /api/v2/admin/payment/freeinstallments
```

### Payment freeinstallments property list

| Attribute | Description |
| --- | --- |
| shop_no | 멀티쇼핑몰 번호 |
| payment_gateway_name | PG 이름 |
| installments | 무이자 할부 정보 목록 |

### Retrieve interest-free installment information   cafe24

#### 기본스펙

| Property | Description |
| --- | --- |
| SCOPE | 상점 읽기권한 (mall.read_store) |
| 호출건수 제한 | 40 |

#### 요청사양

| Parameter | Description |
| --- | --- |
| shop_no최소값: [1] | 멀티쇼핑몰 번호   DEFAULT 1 |

```bash
Retrieve interest-free installment information        Retrieve interest-free installment information       Request   cURL Java Python Node.js PHP Go  Copy     curl -X GET \  'https://{mallid}.cafe24api.com/api/v2/admin/payment/freeinstallments?shop_no=1' \  -H 'Authorization: Bearer {access_token}' \  -H 'Content-Type: application/json' \  -H 'X-Cafe24-Api-Version: {version}'    Response  Copy     {    "freeinstallments": {        "shop_no": 1,        "payment_gateway_name": "allat",        "installments": [            {                "card_code": "SA",                "card_name": "삼성",                "installment_months": [                    1,                    2,                    3                ],                "event_start_date": "2026-04-01T00:00:00+09:00",                "event_end_date": "2026-04-30T23:59:59+09:00"            },            {                "card_code": "SH",                "card_name": "신한",                "installment_months": [                    1,                    2,                    3                ],                "event_start_date": "2026-04-01T00:00:00+09:00",                "event_end_date": "2026-04-30T23:59:59+09:00"            },            {                "card_code": "HY",                "card_name": "현대",                "installment_months": [                    1,                    2,                    3                ],                "event_start_date": "2026-04-01T00:00:00+09:00",                "event_end_date": "2026-04-30T23:59:59+09:00"            }        ]    }}
```

```bash
curl -X GET \  'https://{mallid}.cafe24api.com/api/v2/admin/payment/freeinstallments?shop_no=1' \  -H 'Authorization: Bearer {access_token}' \  -H 'Content-Type: application/json' \  -H 'X-Cafe24-Api-Version: {version}'
```

```json
{    "freeinstallments": {        "shop_no": 1,        "payment_gateway_name": "allat",        "installments": [            {                "card_code": "SA",                "card_name": "삼성",                "installment_months": [                    1,                    2,                    3                ],                "event_start_date": "2026-04-01T00:00:00+09:00",                "event_end_date": "2026-04-30T23:59:59+09:00"            },            {                "card_code": "SH",                "card_name": "신한",                "installment_months": [                    1,                    2,                    3                ],                "event_start_date": "2026-04-01T00:00:00+09:00",                "event_end_date": "2026-04-30T23:59:59+09:00"            },            {                "card_code": "HY",                "card_name": "현대",                "installment_months": [                    1,                    2,                    3                ],                "event_start_date": "2026-04-01T00:00:00+09:00",                "event_end_date": "2026-04-30T23:59:59+09:00"            }        ]    }}
```
