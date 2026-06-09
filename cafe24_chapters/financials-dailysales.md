# FINANCIALS DAILYSALES


## Financials dailysales

```json
Endpoints    GET /api/v2/admin/financials/dailysales
```

```json
GET /api/v2/admin/financials/dailysales
```

### Financials dailysales property list

| Attribute | Description |
| --- | --- |
| shop_no | 멀티쇼핑몰 번호 |
| date | 날짜 |
| payment_amount | 결제 금액 |
| refund_amount | 환불 금액 |
| sales_count | 판매건수 |

### Retrieve a list of daily sales   cafe24 youtube

#### 기본스펙

| Property | Description |
| --- | --- |
| SCOPE | 매출통계 읽기권한 (mall.read_salesreport) |
| 호출건수 제한 | 1 |

#### 요청사양

| Parameter | Description |
| --- | --- |
| start_dateRequired | 검색 시작일 |
| end_dateRequired | 검색 종료일 |
| payment_gateway_name | PG 이름 |
| partner_id | PG사 발급 가맹점 ID |
| payment_method | 결제수단 코드   card : 신용카드 tcash : 계좌이체 icash : 가상계좌 point : 선불금 cell : 휴대폰 |

```bash
Retrieve a list of daily sales        Retrieve a list of daily sales Retrieve dailysales with fields parameter       Request   cURL Java Python Node.js PHP Go  Copy     curl -X GET \  'https://{mallid}.cafe24api.com/api/v2/admin/financials/dailysales?start_date=2020-12-01&end_date=2020-12-15&payment_gateway_name=inicis&partner_id=sampleid' \  -H 'Authorization: Bearer {access_token}' \  -H 'Content-Type: application/json' \  -H 'X-Cafe24-Api-Version: {version}'    Response  Copy     {    "dailysales": [        {            "shop_no": 1,            "date": "2020-12-01",            "payment_amount": "150000.00",            "refund_amount": "50000.00",            "sales_count": 5        },        {            "shop_no": 1,            "date": "2020-12-02",            "payment_amount": "270000.00",            "refund_amount": "20000.00",            "sales_count": 8        }    ]}
```

```bash
curl -X GET \  'https://{mallid}.cafe24api.com/api/v2/admin/financials/dailysales?start_date=2020-12-01&end_date=2020-12-15&payment_gateway_name=inicis&partner_id=sampleid' \  -H 'Authorization: Bearer {access_token}' \  -H 'Content-Type: application/json' \  -H 'X-Cafe24-Api-Version: {version}'
```

```json
{    "dailysales": [        {            "shop_no": 1,            "date": "2020-12-01",            "payment_amount": "150000.00",            "refund_amount": "50000.00",            "sales_count": 5        },        {            "shop_no": 1,            "date": "2020-12-02",            "payment_amount": "270000.00",            "refund_amount": "20000.00",            "sales_count": 8        }    ]}
```
