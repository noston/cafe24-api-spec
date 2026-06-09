# FINANCIALS MONTHLYSALES


## Financials monthlysales

```json
Endpoints    GET /api/v2/admin/financials/monthlysales
```

```json
GET /api/v2/admin/financials/monthlysales
```

### Financials monthlysales property list

| Attribute | Description |
| --- | --- |
| shop_no | 멀티쇼핑몰 번호 |
| month | 년월 |
| payment_amount | 결제 금액 |
| refund_amount | 환불 금액 |
| sales_count | 판매건수 |

### Retrieve a list of monthly sales   cafe24 youtube

#### 기본스펙

| Property | Description |
| --- | --- |
| SCOPE | 매출통계 읽기권한 (mall.read_salesreport) |
| 호출건수 제한 | 1 |

#### 요청사양

| Parameter | Description |
| --- | --- |
| start_monthRequired | 검색 시작월 |
| end_monthRequired | 검색 종료월 |
| payment_gateway_name | PG 이름 |
| partner_id | PG사 발급 가맹점 ID |
| payment_method | 결제수단 코드   card : 신용카드 tcash : 계좌이체 icash : 가상계좌 point : 선불금 cell : 휴대폰 |

```bash
Retrieve a list of monthly sales        Retrieve a list of monthly sales Retrieve monthlysales with fields parameter       Request   cURL Java Python Node.js PHP Go  Copy     curl -X GET \  'https://{mallid}.cafe24api.com/api/v2/admin/financials/monthlysales?start_month=2020-09&end_month=2020-10&payment_gateway_name=inicis&partner_id=sampleid' \  -H 'Authorization: Bearer {access_token}' \  -H 'Content-Type: application/json' \  -H 'X-Cafe24-Api-Version: {version}'    Response  Copy     {    "monthlysales": [        {            "shop_no": 1,            "month": "2020-09",            "payment_amount": "150000.00",            "refund_amount": "50000.00",            "sales_count": 5        },        {            "shop_no": 1,            "month": "2020-10",            "payment_amount": "270000.00",            "refund_amount": "20000.00",            "sales_count": 8        }    ]}
```

```bash
curl -X GET \  'https://{mallid}.cafe24api.com/api/v2/admin/financials/monthlysales?start_month=2020-09&end_month=2020-10&payment_gateway_name=inicis&partner_id=sampleid' \  -H 'Authorization: Bearer {access_token}' \  -H 'Content-Type: application/json' \  -H 'X-Cafe24-Api-Version: {version}'
```

```json
{    "monthlysales": [        {            "shop_no": 1,            "month": "2020-09",            "payment_amount": "150000.00",            "refund_amount": "50000.00",            "sales_count": 5        },        {            "shop_no": 1,            "month": "2020-10",            "payment_amount": "270000.00",            "refund_amount": "20000.00",            "sales_count": 8        }    ]}
```
